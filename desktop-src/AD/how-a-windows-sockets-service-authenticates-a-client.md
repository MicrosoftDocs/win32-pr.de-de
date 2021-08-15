---
title: Authentifizieren eines Clients durch einen Windows Sockets-Dienst
description: Wenn ein Client eine Verbindung mit dem Windows Sockets-Dienst herstellt, beginnt der Dienst seine Vorgänge für die sequenzbasierte Authentifizierung, wie in den folgenden Codebeispielen gezeigt.
ms.assetid: 32f62fb9-41c6-4932-9b91-753174919707
ms.tgt_platform: multiple
keywords:
- Authentifizieren eines Client-AD durch einen Windows Sockets-Dienst
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c2975d356de011818514d6999f03d1998e066a4b8bdadd6eaba8835541e4b8e5
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118188522"
---
# <a name="how-a-windows-sockets-service-authenticates-a-client"></a>Authentifizieren eines Clients durch einen Windows Sockets-Dienst

Wenn ein Client eine Verbindung mit dem Windows Sockets-Dienst herstellt, beginnt der Dienst seine Vorgänge für die sequenzbasierte Authentifizierung, wie in den folgenden Codebeispielen gezeigt.

Die **DoAuthentication-Routine** verwendet das Sockethandle, um das erste Authentifizierungspaket vom Client zu empfangen. Der Clientpuffer wird an die **GenServerContext-Funktion** übergeben, die den Puffer dann zur Authentifizierung an das SSPI-Sicherheitspaket übergibt. **DoAuthentication** sendet dann die Ausgabe des Sicherheitspakets zurück an den Client. Diese Schleife wird wiederholt, bis die Authentifizierung fehlschlägt oder **GenServerContext** ein Flag festlegt, das angibt, dass die Authentifizierung erfolgreich war.

**GenServerContext** ruft die folgenden Funktionen aus einem SSPI-Sicherheitspaket auf:

-   [**AcquireCredentialsHandle**](../SecAuthN/acquirecredentialshandle--general.md) extrahiert die Dienstanmeldeinformationen aus dem Dienstsicherheitskontext, der beim Starten des Diensts eingerichtet wurde.
-   [**AcceptSecurityContext**](../SecAuthN/acceptsecuritycontext--general.md) versucht, die gegenseitige Authentifizierung mit den Dienstanmeldeinformationen und den vom Client empfangenen Authentifizierungsdaten durchzuführen. Um gegenseitige Authentifizierung anzufordern, muss der **AcceptSecurityContext-Aufruf** das ASC \_ REQ \_ MUTUAL \_ AUTH-Flag angeben.
-   [**CompleteAuthToken**](/windows/desktop/api/sspi/nf-sspi-completeauthtoken) wird bei Bedarf aufgerufen, um den Authentifizierungsvorgang abzuschließen.

Im folgenden Codebeispiel wird das Negotiate-Paket aus der Secur32.dll Bibliothek von Sicherheitspaketen verwendet.


```C++
/***************************************************************/
//   DoAuthentication routine for the service
//
//   Manages the service authentication communication with the client 
//   using the supplied socket handle.
//
//   Returns TRUE if the mutual authentication succeeds.
//   Otherwise, it returns FALSE.
//
/***************************************************************/
 
BOOL DoAuthentication (SOCKET s)
{
DWORD cbIn, cbOut;
BOOL done = FALSE;

if(s==INVALID_SOCKET)
{
    return(FALSE);
}
 
// Receive authentication data from the client and pass
// it to the security package. Send the package output back
// to the client. Repeat until complete.
do 
{
    if (!ReceiveMsg (s, g_pInBuf, g_cbMaxMessage, &cbIn))
        return(FALSE);
 
    cbOut = g_cbMaxMessage;
    if (!GenServerContext (s, g_pInBuf, cbIn, g_pOutBuf, 
                               &cbOut, &done))
        return(FALSE);
 
    if (!SendMsg (s, g_pOutBuf, cbOut))
        return(FALSE);
} 
while(!done);
 
return(TRUE);
}
 
/***************************************************************/
//   GenServerContext routine 
//
//   Handles the service interactions with the security package.
//   Takes an input buffer coming from the client and generates a 
//   buffer of data to send back to the client. Also returns 
//   an indication when the authentication is complete.
//
//   Returns TRUE if the mutual authentication is successful.
//   Otherwise, it returns FALSE.
//
/***************************************************************/
BOOL GenServerContext (
            DWORD dwKey,
            BYTE *pIn,
            DWORD cbIn,
            BYTE *pOut,
            DWORD *pcbOut,
            BOOL *pfDone)
{
SECURITY_STATUS  ssStatus;
TimeStamp        Lifetime;
SecBufferDesc    OutBuffDesc;
SecBuffer        OutSecBuff;
SecBufferDesc    InBuffDesc;
SecBuffer        InSecBuff;
ULONG            ContextAttributes = 0;
PAUTH_SEQ        pAS = null;

if((pIn==NULL && cbIn>0) || (pOut==NULL) || (pcbOut==NULL) || (pfDone==NULL))
{
    return(FALSE);
}
 
// Get a structure that contains the state of the authentication sequence.
if (!GetEntry (dwKey, (PVOID*) &pAS))
    return(FALSE);
 
if (pAS->_fNewConversation)  
{
    ssStatus = g_pFuncs->AcquireCredentialsHandle (
                        NULL,    // principal
                        PACKAGE_NAME,
                        SECPKG_CRED_INBOUND,
                        NULL,    // LOGON id
                        NULL,    // authentication data
                        NULL,    // get key function
                        NULL,    // get key argument
                        &pAS->_hcred,
                        &Lifetime
                        );
    if (SEC_SUCCESS (ssStatus))
        pAS->_fHaveCredHandle = TRUE;
    else
    {
        fprintf (stderr, "AcquireCredentialsHandle failed: %u\n", 
                 ssStatus);
        return(FALSE);
    }
}
 
// Prepare the output buffer.
OutBuffDesc.ulVersion = 0;
OutBuffDesc.cBuffers  = 1;
OutBuffDesc.pBuffers  = &OutSecBuff;
 
OutSecBuff.cbBuffer   = *pcbOut;
OutSecBuff.BufferType = SECBUFFER_TOKEN;
OutSecBuff.pvBuffer   = pOut;
 
// Prepare the input buffer.
InBuffDesc.ulVersion  = 0;
InBuffDesc.cBuffers   = 1;
InBuffDesc.pBuffers   = &InSecBuff;
 
InSecBuff.cbBuffer    = cbIn;
InSecBuff.BufferType  = SECBUFFER_TOKEN;
InSecBuff.pvBuffer    = pIn;
 
ssStatus = g_pFuncs->AcceptSecurityContext (
                    &pAS->_hcred,
                    pAS->_fNewConversation ? NULL : &pAS->_hctxt,
                    &InBuffDesc,
                    ASC_REQ_MUTUAL_AUTH,  // Context requirements.
                    SECURITY_NATIVE_DREP,
                    &pAS->_hctxt,
                    &OutBuffDesc,
                    &ContextAttributes,
                    &Lifetime
                    );
if (!SEC_SUCCESS (ssStatus))  
{
    fprintf (stderr, "AcceptSecurityContext failed: %u\n", ssStatus);
    return FALSE;
}
if (!(ContextAttributes && ASC_RET_MUTUAL_AUTH)) 
    _tprintf(TEXT("Mutual Auth not set in returned context.\n"));
 
pAS->_fHaveCtxtHandle = TRUE;
 
// Complete the authentication token, if necessary.
if ((SEC_I_COMPLETE_NEEDED == ssStatus) || 
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
 
return TRUE;
}
```



 

 