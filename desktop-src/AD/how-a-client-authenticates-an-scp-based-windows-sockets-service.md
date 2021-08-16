---
title: Authentifizieren eines SCP-basierten Windows Sockets Service durch einen Client
description: In diesem Thema wird der Code gezeigt, den eine Clientanwendung verwendet, um einen SPN für einen Dienst zu erstellen.
ms.assetid: b5ef79c6-e321-435c-b3de-817fdea8836a
ms.tgt_platform: multiple
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 40d35ad62e05ab925d2dedc10506ddb339c2aafd188487f2e1591713189f451a
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118188664"
---
# <a name="how-a-client-authenticates-an-scp-based-windows-sockets-service"></a>Authentifizieren eines SCP-basierten Windows Sockets Service durch einen Client

In diesem Thema wird der Code gezeigt, den eine Clientanwendung verwendet, um einen SPN für einen Dienst zu erstellen. Der Client wird an den Dienstverbindungspunkt (Service Connection Point, SCP) des Diensts gebunden, um die Daten abzurufen, die zum Herstellen einer Verbindung mit dem Dienst erforderlich sind. Der SCP enthält auch Daten, die der Client zum Erstellen des DIENST-SPN verwenden kann. Weitere Informationen und ein Codebeispiel, das an den SCP gebunden und die erforderlichen Eigenschaften abruft, finden Sie unter Suchen und Verwenden eines [Dienstverbindungspunkts](how-clients-find-and-use-a-service-connection-point.md)durch Clients.

In diesem Thema wird auch gezeigt, wie ein Client ein SSPI-Sicherheitspaket und den DIENST-SPN verwendet, um eine sich gegenseitig authentifizierte Verbindung mit dem Windows Sockets-Dienst herzustellen. Beachten Sie, dass dieser Code fast identisch mit dem Code ist, der in Microsoft Windows NT 4.0 und früher erforderlich ist, nur um den Client beim Server zu authentifizieren. Der einzige Unterschied ist, dass der Client den SPN angeben und das ISC \_ REQ \_ MUTUAL \_ AUTH-Flag angeben muss.

## <a name="client-code-to-make-an-spn-for-a-service"></a>Clientcode zum Machen eines SPN für einen Dienst


```C++
// Initialize these strings by querying the service's SCP.
TCHAR szDn[MAX_PATH],     // DN of the service's SCP.
      szServer[MAX_PATH], // DNS name of the service's server.
      szClass[MAX_PATH];  // Service class.
 
TCHAR szSpn[MAX_PATH];    // Buffer for SPN.
SOCKET sockServer;        // Socket connected to service.
DWORD dwRes, dwLen;
.
.
.
// Compose the SPN for the service using the DN, Class, and Server
// returned by ScpLocate.
dwLen = sizeof(szSpn);
dwRes = DsMakeSpn(
     szClass,    // Service class.
     szDn,       // DN of the service's SCP.
     szServer,   // DNS name of the server on which service is running.
     0,          // No port component in SPN.
     NULL,       // No referrer.
     &dwLen,     // Size of szSpn buffer.
     szSpn);     // Buffer to receive the SPN.

if (!DoAuthentication (sockServer, szSpn)) {
    closesocket (sockServer);
    return(FALSE);
}
.
.
.
```



## <a name="client-code-to-authenticate-the-service"></a>Clientcode zum Authentifizieren des Diensts

Dieses Codebeispiel besteht aus zwei Routinen: **DoAuthentication** und **GenClientContext**. Nachdem [**DsMakeSpn**](/windows/desktop/api/Dsparse/nf-dsparse-dsmakespna) aufgerufen wurde, um einen SPN für den Dienst zu erstellen, übergibt der Client den SPN an die **DoAuthentication-Routine,** die **GenClientContext** aufruft, um den anfänglichen Puffer zu generieren, der an den Dienst gesendet werden soll. **DoAuthentication** verwendet das Sockethandl, um den Puffer zu senden und die Antwort des Diensts zu empfangen, die durch einen anderen Aufruf von **GenClientContext** an das SSPI-Paket übergeben wird. Diese Schleife wird wiederholt, bis die Authentifizierung fehlschlägt oder **GenClientContext** ein Flag festgibt, das angibt, dass die Authentifizierung erfolgreich war.

Die **GenClientContext-Routine** interagiert mit dem SSPI-Paket, um die Authentifizierungsdaten zu generieren, die an den Dienst gesendet werden, und die vom Dienst empfangenen Daten zu verarbeiten. Die wichtigsten Komponenten der vom Client bereitgestellten Authentifizierungsdaten sind:

-   Der Dienstprinzipalname, der die Anmeldeinformationen identifiziert, die der Dienst authentifizieren muss.
-   Die Anmeldeinformationen des Clients. Die [**AcquireCredentialsHandle-Funktion**](../SecAuthN/acquirecredentialshandle--general.md) des Sicherheitspakets extrahiert diese Anmeldeinformationen aus dem Sicherheitskontext des Clients, der bei der Anmeldung eingerichtet wurde.
-   Zum Anfordern der gegenseitigen Authentifizierung muss der Client das ISC REQ MUTUAL AUTH-Flag angeben, wenn er die InitializeSecurityContext-Funktion während der \_ \_ \_ **GenClientContext-Routine** aufruft. [](../SecAuthN/initializesecuritycontext--general.md)


```C++
// Structure for storing the state of the authentication sequence.
typedef struct _AUTH_SEQ 
{
    BOOL _fNewConversation;
    CredHandle _hcred;
    BOOL _fHaveCredHandle;
    BOOL _fHaveCtxtHandle;
    struct _SecHandle  _hctxt;
} AUTH_SEQ, *PAUTH_SEQ;
 
/***************************************************************/
//   DoAuthentication routine for the client.
//
//   Manages the client's authentication conversation with the service 
//   using the supplied socket handle.
//
//   Returns TRUE if the mutual authentication is successful.
//   Otherwise, it returns FALSE.
//
/***************************************************************/
BOOL DoAuthentication (
        SOCKET s, 
        LPTSTR szSpn)
{
BOOL done = FALSE;
DWORD cbOut, cbIn;
 
// Call the security package to generate the initial buffer of 
// authentication data to send to the service.
cbOut = g_cbMaxMessage;
if (!GenClientContext (s, NULL, 0, g_pOutBuf, 
                       &cbOut, &done, szSpn))
    return(FALSE);
    
if (!SendMsg (s, g_pOutBuf, cbOut))
    return(FALSE);
 
// Pass the service's response back to the security package, and send 
// the package's output back to the service. Repeat until complete.
while (!done) 
{
    if (!ReceiveMsg (s, g_pInBuf, g_cbMaxMessage, &cbIn))
        return(FALSE);
 
    cbOut = g_cbMaxMessage;
    if (!GenClientContext (s, g_pInBuf, cbIn, g_pOutBuf, 
                           &cbOut, &done, szSpn))
        return(FALSE);
 
    if (!SendMsg (s, g_pOutBuf, cbOut))
        return(FALSE);
}
 
return(TRUE);
}
 
/***************************************************************/
//   GenClientContext routine
//
//   Handles the client's interactions with the security package.
//   Optionally takes an input buffer coming from the service 
//   and generates a buffer of data to send back to the 
//   service. Also returns an indication when the authentication
//   is complete.
//
//   Returns TRUE if the mutual authentication is successful.
//   Otherwise, it returns FALSE.
//
/***************************************************************/
BOOL GenClientContext (
            DWORD dwKey,     // Socket handle used as key.
            BYTE *pIn,
            DWORD cbIn,
            BYTE *pOut,
            DWORD *pcbOut,
            BOOL *pfDone,
            LPTSTR szSpn)
{
SECURITY_STATUS  ssStatus;
TimeStamp        Lifetime;
SecBufferDesc    OutBuffDesc;
SecBuffer        OutSecBuff;
SecBufferDesc    InBuffDesc;
SecBuffer        InSecBuff;
ULONG            ContextAttributes;
PAUTH_SEQ        pAS; // Structure to store state of authentication.
 
// Get structure that contains the state of the authentication sequence.
if (!GetEntry (dwKey, (PVOID*) &pAS))
    return(FALSE);
 
if (pAS->_fNewConversation)
{
    ssStatus = g_pFuncs->AcquireCredentialsHandle (
            NULL,    // Principal
            PACKAGE_NAME,
            SECPKG_CRED_OUTBOUND,
            NULL,    // LOGON id
            NULL,    // Authentication data
            NULL,    // Get key function.
            NULL,    // Get key argument.
            &pAS->_hcred,
            &Lifetime
            );
    if (SEC_SUCCESS (ssStatus))
        pAS->_fHaveCredHandle = TRUE;
    else 
    {
        fprintf (stderr, 
                 "AcquireCredentialsHandle failed: %u\n", ssStatus);
        return(FALSE);
    }
}
 
// Prepare output buffer.
OutBuffDesc.ulVersion = 0;
OutBuffDesc.cBuffers = 1;
OutBuffDesc.pBuffers = &OutSecBuff;
 
OutSecBuff.cbBuffer = *pcbOut;
OutSecBuff.BufferType = SECBUFFER_TOKEN;
OutSecBuff.pvBuffer = pOut;
 
// Prepare input buffer.
if (!pAS->_fNewConversation) 
{
    InBuffDesc.ulVersion = 0;
    InBuffDesc.cBuffers = 1;
    InBuffDesc.pBuffers = &InSecBuff;
 
    InSecBuff.cbBuffer = cbIn;
    InSecBuff.BufferType = SECBUFFER_TOKEN;
    InSecBuff.pvBuffer = pIn;
}
 
_tprintf(TEXT("InitializeSecurityContext: pszTarget=%s\n"),szSpn);
 
ssStatus = g_pFuncs->InitializeSecurityContext (
                     &pAS->_hcred,
                     pAS->_fNewConversation ? NULL : &pAS->_hctxt,
                     szSpn,
                     ISC_REQ_MUTUAL_AUTH,      // Context requirements
                     0,                        // Reserved1
                     SECURITY_NATIVE_DREP,
                     pAS->_fNewConversation ? NULL : &InBuffDesc,
                     0,                        // Reserved2
                     &pAS->_hctxt,
                     &OutBuffDesc,
                     &ContextAttributes,
                     &Lifetime
                     );
if (!SEC_SUCCESS (ssStatus)) 
{
    fprintf (stderr, "init context failed: %X\n", ssStatus);
    return FALSE;
}
 
pAS->_fHaveCtxtHandle = TRUE;
 
// Complete token if applicable.
if ( (SEC_I_COMPLETE_NEEDED == ssStatus) || 
     (SEC_I_COMPLETE_AND_CONTINUE == ssStatus))  
{
    if (g_pFuncs->CompleteAuthToken) 
    {
        ssStatus = g_pFuncs->CompleteAuthToken (&pAS->_hctxt, 
                                                &OutBuffDesc);
        if (!SEC_SUCCESS(ssStatus)) 
        {
            fprintf (stderr, "complete failed: %u\n", ssStatus);
            return FALSE;
        }
    } else 
    {
        fprintf (stderr, "Complete not supported.\n");
        return FALSE;
    }
}
 
*pcbOut = OutSecBuff.cbBuffer;
 
if (pAS->_fNewConversation)
    pAS->_fNewConversation = FALSE;
 
*pfDone = !((SEC_I_CONTINUE_NEEDED == ssStatus) ||
            (SEC_I_COMPLETE_AND_CONTINUE == ssStatus));
 
// Check the ISC_RET_MUTUAL_AUTH flag to verify that 
// mutual authentication was performed.
if (*pfDone && !(ContextAttributes && ISC_RET_MUTUAL_AUTH) )
    _tprintf(TEXT("Mutual Auth not set in returned context.\n"));
 
return TRUE;
}
```



 

 




