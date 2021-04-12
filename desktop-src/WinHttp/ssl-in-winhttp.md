---
description: Die Microsoft Windows HTTP-Dienste (WinHTTP) unterstützen Secure Sockets Layer (SSL)-Transaktionen, einschließlich Client Zertifikate. In diesem Thema werden Konzepte erläutert, die an einer SSL-Transaktion beteiligt sind und wie Sie mit WinHTTP behandelt werden.
ms.assetid: cb0a04f5-1026-4ad5-bb5b-c854064a5167
title: SSL in WinHTTP
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d7952bb9a0227017927452502352c0354e69079c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "104216521"
---
# <a name="ssl-in-winhttp"></a><span data-ttu-id="305eb-104">SSL in WinHTTP</span><span class="sxs-lookup"><span data-stu-id="305eb-104">SSL in WinHTTP</span></span>

<span data-ttu-id="305eb-105">Die Microsoft Windows HTTP-Dienste (WinHTTP) unterstützen Secure Sockets Layer (SSL)-Transaktionen, einschließlich Client Zertifikate.</span><span class="sxs-lookup"><span data-stu-id="305eb-105">Microsoft Windows HTTP Services (WinHTTP) supports Secure Sockets Layer (SSL) transactions including client certificates.</span></span> <span data-ttu-id="305eb-106">In diesem Thema werden Konzepte erläutert, die an einer SSL-Transaktion beteiligt sind und wie Sie mit WinHTTP behandelt werden.</span><span class="sxs-lookup"><span data-stu-id="305eb-106">This topic explains concepts involved in an SSL transaction and how they are handled using WinHTTP.</span></span>

## <a name="secure-sockets-layer"></a><span data-ttu-id="305eb-107">Secure Sockets Layer</span><span class="sxs-lookup"><span data-stu-id="305eb-107">Secure Sockets Layer</span></span>

<span data-ttu-id="305eb-108">SSL ist ein etablierter Standard, um sichere HTTP-Transaktionen sicherzustellen.</span><span class="sxs-lookup"><span data-stu-id="305eb-108">SSL is an established standard for ensuring secure HTTP transactions.</span></span> <span data-ttu-id="305eb-109">SSL bietet einen Mechanismus, mit dem bis zu 128-Bit-Verschlüsselung für alle Transaktionen zwischen Client und Server durchgeführt werden können.</span><span class="sxs-lookup"><span data-stu-id="305eb-109">SSL provides a mechanism to perform up to 128-bit encryption on all transactions between the client and server.</span></span> <span data-ttu-id="305eb-110">Dadurch kann der Client überprüfen, ob der Server zu einer vertrauenswürdigen Entität gehört, indem Server Zertifikate verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="305eb-110">It enables the client to verify that the server belongs to a trusted entity through the use of server certificates.</span></span> <span data-ttu-id="305eb-111">Außerdem kann der Server die Identität des Clients mit Client Zertifikaten bestätigen.</span><span class="sxs-lookup"><span data-stu-id="305eb-111">It also enables the server to confirm the identity of the client with client certificates.</span></span>

<span data-ttu-id="305eb-112">Bei jedem dieser Probleme werden Verschlüsselung, Server Identität und Client Identität im SSL-Handshake ausgehandelt, der auftritt, wenn ein Client zuerst eine Ressource von einem HTTPS-Server (Secure Hypertext Transfer Protocol) anfordert.</span><span class="sxs-lookup"><span data-stu-id="305eb-112">Each of these issues encryption, server identity, and client identity are negotiated in the SSL handshake that occurs when a client first requests a resource from a Secure Hypertext Transfer Protocol (HTTPS) server.</span></span> <span data-ttu-id="305eb-113">Im Wesentlichen stellen Client und Server jeweils eine Liste der erforderlichen und bevorzugten Einstellungen dar.</span><span class="sxs-lookup"><span data-stu-id="305eb-113">Essentially, the client and server each present a list of required and preferred settings.</span></span> <span data-ttu-id="305eb-114">Wenn ein allgemeiner Satz von Anforderungen vereinbart und erfüllt werden kann, wird eine SSL-Verbindung hergestellt.</span><span class="sxs-lookup"><span data-stu-id="305eb-114">If a common set of requirements can be agreed upon and met, an SSL connection is established.</span></span>

<span data-ttu-id="305eb-115">WinHTTP stellt eine allgemeine Schnittstelle für die Verwendung von SSL bereit.</span><span class="sxs-lookup"><span data-stu-id="305eb-115">WinHTTP provides a high level interface for using SSL.</span></span> <span data-ttu-id="305eb-116">Während die Details des SSL-Handshakes und der Transaktion intern behandelt werden, können Sie mit WinHTTP Verschlüsselungsstufen abrufen, das Sicherheitsprotokoll angeben und mit Server-und Client Zertifikaten interagieren.</span><span class="sxs-lookup"><span data-stu-id="305eb-116">While the details of the SSL handshake and transaction are handled internally, WinHTTP enables you to retrieve encryption levels, specify the security protocol, and interact with server and client certificates.</span></span> <span data-ttu-id="305eb-117">Die folgenden Abschnitte enthalten ausführliche Informationen zum Erstellen von WinHTTP-basierten Anwendungen, die eine SSL-Protokollversion auswählen, Server Zertifikate untersuchen und Client Zertifikate auswählen, die an HTTPS-Server gesendet werden sollen.</span><span class="sxs-lookup"><span data-stu-id="305eb-117">The following sections provide details on creating WinHTTP based applications that elect an SSL protocol version, examine server certificates, and select client certificates to send to HTTPS servers.</span></span>

## <a name="server-certificates"></a><span data-ttu-id="305eb-118">Serverzertifikate</span><span class="sxs-lookup"><span data-stu-id="305eb-118">Server Certificates</span></span>

<span data-ttu-id="305eb-119">Server Zertifikate werden vom Server an den Client gesendet, sodass der Client einen öffentlichen Schlüssel für den Server abrufen und sicherstellen kann, dass der Server von einer Zertifizierungsstelle überprüft wurde.</span><span class="sxs-lookup"><span data-stu-id="305eb-119">Server certificates are sent from the server to the client so that the client can obtain a public key for the server and ensure that the server has been verified by a certification authority.</span></span> <span data-ttu-id="305eb-120">Zertifikate können verschiedene Datentypen enthalten.</span><span class="sxs-lookup"><span data-stu-id="305eb-120">Certificates can contain different types of data.</span></span> <span data-ttu-id="305eb-121">Ein X. 509-Zertifikat enthält z. b. das Format des Zertifikats, die Seriennummer des Zertifikats, den Algorithmus, der zum Signieren des Zertifikats verwendet wird, den Namen der Zertifizierungsstelle, die das Zertifikat ausgestellt hat, den Namen und den öffentlichen Schlüssel der Entität, die das Zertifikat anfordert, und die Signatur der Zertifizierungsstelle.</span><span class="sxs-lookup"><span data-stu-id="305eb-121">For example, an X.509 certificate includes the format of the certificate, the serial number of the certificate, the algorithm used to sign the certificate, the name of the certification authority (CA) that issued the certificate, the name and public key of the entity that requests the certificate, and the CA's signature.</span></span>

<span data-ttu-id="305eb-122">Wenn Sie die WinHTTP-API (Application Programming Interface) verwenden, können Sie ein Serverzertifikat abrufen, indem Sie [**WinHttpQueryOption**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpqueryoption) aufrufen und die [**WinHTTP- \_ Option \_ \_ sicherheitszertifikatstruktursflag \_**](option-flags.md) angeben.</span><span class="sxs-lookup"><span data-stu-id="305eb-122">When using the WinHTTP  application programming interface (API), you can retrieve a server certificate by calling [**WinHttpQueryOption**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpqueryoption) and specifying the [**WINHTTP\_OPTION\_SECURITY\_CERTIFICATE\_STRUCT**](option-flags.md) flag.</span></span> <span data-ttu-id="305eb-123">Das Serverzertifikat wird in einer [**WinHTTP- \_ Zertifikats \_ Informations**](/windows/win32/api/winhttp/ns-winhttp-winhttp_certificate_info) Struktur zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="305eb-123">The server certificate is returned in a [**WINHTTP\_CERTIFICATE\_INFO**](/windows/win32/api/winhttp/ns-winhttp-winhttp_certificate_info) structure.</span></span> <span data-ttu-id="305eb-124">Wenn Sie den Zertifikat Kontext abrufen möchten, geben Sie stattdessen die [**WinHTTP- \_ Option \_ Server \_ CERT- \_ Kontext**](option-flags.md) Kennzeichen an.</span><span class="sxs-lookup"><span data-stu-id="305eb-124">If you prefer to retrieve the certificate context, specify the [**WINHTTP\_OPTION\_SERVER\_CERT\_CONTEXT**](option-flags.md) flag instead.</span></span>

<span data-ttu-id="305eb-125">Wenn ein Serverzertifikat Fehler enthält, können Details zu diesem Fehler in der Status Rückruffunktion abgerufen werden.</span><span class="sxs-lookup"><span data-stu-id="305eb-125">If a server certificate contains errors, details about the error can be obtained in the status callback function.</span></span> <span data-ttu-id="305eb-126">Die Benachrichtigung "sicherer Fehler bei [**WinHTTP- \_ Rückruf \_ Status \_ \_**](/windows/win32/api/winhttp/nc-winhttp-winhttp_status_callback) " weist auf einen Fehler mit einem Serverzertifikat hin.</span><span class="sxs-lookup"><span data-stu-id="305eb-126">The [**WINHTTP\_CALLBACK\_STATUS\_SECURE\_FAILURE**](/windows/win32/api/winhttp/nc-winhttp-winhttp_status_callback) notification indicates an error with a server certificate.</span></span> <span data-ttu-id="305eb-127">Der *lpvstatusinformation* -Parameter enthält ein oder mehrere ausführliche Fehlerflags.</span><span class="sxs-lookup"><span data-stu-id="305eb-127">The *lpvStatusInformation* parameter contains one or more detailed error flags.</span></span> <span data-ttu-id="305eb-128">Weitere Informationen finden Sie unter [**WinHTTP- \_ Status \_ Rückruf**](/windows/win32/api/winhttp/nc-winhttp-winhttp_status_callback) .</span><span class="sxs-lookup"><span data-stu-id="305eb-128">See [**WINHTTP\_STATUS\_CALLBACK**](/windows/win32/api/winhttp/nc-winhttp-winhttp_status_callback) for more information.</span></span>

## <a name="client-certificates"></a><span data-ttu-id="305eb-129">Clientzertifikate</span><span class="sxs-lookup"><span data-stu-id="305eb-129">Client Certificates</span></span>

<span data-ttu-id="305eb-130">Während des SSL-Handshakes benötigt der Server möglicherweise eine Authentifizierung.</span><span class="sxs-lookup"><span data-stu-id="305eb-130">During the SSL handshake, the server might require authentication.</span></span> <span data-ttu-id="305eb-131">Der Client wird authentifiziert, indem ein gültiges Client Zertifikat für den Server bereitgestellt wird.</span><span class="sxs-lookup"><span data-stu-id="305eb-131">The client is authenticated by supplying a valid client certificate to the server.</span></span> <span data-ttu-id="305eb-132">WinHTTP ermöglicht das auswählen und Senden eines Zertifikats aus einem lokalen [*Zertifikat Speicher*](glossary.md).</span><span class="sxs-lookup"><span data-stu-id="305eb-132">WinHTTP enables you to select and send a certificate from a local [*certificate store*](glossary.md).</span></span> <span data-ttu-id="305eb-133">In den folgenden Abschnitten wird der Prozess beschrieben, der Client Zertifikate bereitstellt, wenn entweder die WinHTTP-API oder das [**WinHttpRequest**](winhttprequest.md) -Objekt verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="305eb-133">The following sections describe the process that provides client certificates when using either the WinHTTP API or the [**WinHttpRequest**](winhttprequest.md) object.</span></span>

### <a name="winhttp-api"></a><span data-ttu-id="305eb-134">WinHTTP-API</span><span class="sxs-lookup"><span data-stu-id="305eb-134">WinHTTP API</span></span>

<span data-ttu-id="305eb-135">Sowohl [**WinHttpSendRequest**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpsendrequest) als auch [**WinHttpReceiveResponse**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpreceiveresponse) können nicht angeben, dass eine Anforderung nicht erfolgreich war, weil der HTTPS-Server eine Authentifizierung erfordert.</span><span class="sxs-lookup"><span data-stu-id="305eb-135">Both [**WinHttpSendRequest**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpsendrequest) and [**WinHttpReceiveResponse**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpreceiveresponse) can fail to indicate that a request was unsuccessful because the HTTPS server requires authentication.</span></span> <span data-ttu-id="305eb-136">In diesen Fällen wird [**GetLastError**](/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror) aufgerufen, um den Fehler für das \_ WinHTTP-Client Authentifizierungszertifikat zurückgegeben \_ \_ \_ \_ .</span><span class="sxs-lookup"><span data-stu-id="305eb-136">In these cases, call [**GetLastError**](/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror) to returns ERROR\_WINHTTP\_CLIENT\_AUTH\_CERT\_NEEDED.</span></span> <span data-ttu-id="305eb-137">Verwenden Sie nach dem Empfang dieses Fehlers die entsprechenden [kryptoapi](/windows/desktop/SecCrypto/cryptography-functions) -Funktionen, um ein entsprechendes Zertifikat zu finden.</span><span class="sxs-lookup"><span data-stu-id="305eb-137">Upon receiving this error, use the appropriate [CryptoAPI](/windows/desktop/SecCrypto/cryptography-functions) functions to find an appropriate certificate.</span></span> <span data-ttu-id="305eb-138">Geben Sie an, dass dieses Zertifikat mit der nächsten Anforderung gesendet werden soll, indem Sie [**WinHttpSetOption**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpsetoption) mit der [**WinHTTP- \_ Option \_ Client \_ CERT- \_ Kontext**](option-flags.md) Kennzeichen aufrufen.</span><span class="sxs-lookup"><span data-stu-id="305eb-138">Indicate that this certificate should be sent with the next request by calling [**WinHttpSetOption**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpsetoption) with the [**WINHTTP\_OPTION\_CLIENT\_CERT\_CONTEXT**](option-flags.md) flag.</span></span>

<span data-ttu-id="305eb-139">Im folgenden Codebeispiel wird veranschaulicht, wie Sie einen [*Zertifikat Speicher*](glossary.md) öffnen und nach einem nach dem Antragsteller Namen basierenden Zertifikat suchen, nachdem der Fehler " \_ WinHTTP-Client Authentifizierungszertifikat erforderlich" \_ \_ \_ \_ zurückgegeben wurde.</span><span class="sxs-lookup"><span data-stu-id="305eb-139">The following code example shows how to open a [*certificate store*](glossary.md) and locate a certificate based on subject name after the ERROR\_WINHTTP\_CLIENT\_AUTH\_CERT\_NEEDED error has been returned.</span></span>


```C++
  if( !WinHttpReceiveResponse( hRequest, NULL ) )
  {
    if( GetLastError( ) == ERROR_WINHTTP_CLIENT_AUTH_CERT_NEEDED )
    {
      //MY is the store the certificate is in.
      hMyStore = CertOpenSystemStore( 0, TEXT("MY") );
      if( hMyStore )
      {
        pCertContext = CertFindCertificateInStore( hMyStore,
             X509_ASN_ENCODING | PKCS_7_ASN_ENCODING,
             0,
             CERT_FIND_SUBJECT_STR,
             (LPVOID) szCertName, //Subject string in the certificate.
             NULL );
        if( pCertContext )
        {
          WinHttpSetOption( hRequest, 
                            WINHTTP_OPTION_CLIENT_CERT_CONTEXT,
                            (LPVOID) pCertContext, 
                            sizeof(CERT_CONTEXT) );
          CertFreeCertificateContext( pCertContext );
        }
        CertCloseStore( hMyStore, 0 );

        // NOTE: Application should now resend the request.
      }
    }
  }
```



<span data-ttu-id="305eb-140">Vor dem erneuten Senden einer Anforderung, die ein Client Zertifikat enthält, können Sie bestimmen, ob die unterstützte Verschlüsselungs Stufe für Ihre Anwendung zulässig ist.</span><span class="sxs-lookup"><span data-stu-id="305eb-140">Before resending a request that contains a client certificate, you can determine if the supported level of encryption is acceptable for your application.</span></span> <span data-ttu-id="305eb-141">Wenden Sie [**WinHttpQueryOption**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpqueryoption) an, und geben Sie das Flag für die [**WinHTTP- \_ Option \_ \_ sicherheitsflags**](option-flags.md) an, um die verwendete Verschlüsselungs Ebene zu bestimmen.</span><span class="sxs-lookup"><span data-stu-id="305eb-141">Call [**WinHttpQueryOption**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpqueryoption) and specify the [**WINHTTP\_OPTION\_SECURITY\_FLAGS**](option-flags.md) flag to determine the level of encryption that is used.</span></span>

### <a name="issuer-list-retrieval-for-ssl-client-authentication"></a><span data-ttu-id="305eb-142">Abrufen der Ausstellerliste für die SSL-Client Authentifizierung</span><span class="sxs-lookup"><span data-stu-id="305eb-142">Issuer List Retrieval for SSL Client Authentication</span></span>

<span data-ttu-id="305eb-143">Wenn die WinHTTP-Client Anwendung eine Anforderung an einen sicheren HTTP-Server sendet, der SSL-Client Authentifizierung erfordert, gibt WinHTTP einen Fehler zurück, der für das **\_ WinHTTP-Client Authentifizierungszertifikat \_ \_ \_ \_ erforderlich** ist, wenn die Anwendung kein Client Zertifikat bereitgestellt hat.</span><span class="sxs-lookup"><span data-stu-id="305eb-143">When the WinHttp client application sends a request to a secure HTTP server that requires SSL client authentication, WinHttp returns an **ERROR\_WINHTTP\_CLIENT\_AUTH\_CERT\_NEEDED** if the application has not supplied a client certificate.</span></span> <span data-ttu-id="305eb-144">Für Computer, die unter Windows Server 2008 und Windows Vista ausgeführt werden, ermöglicht WinHTTP der Anwendung das Abrufen der Zertifikat Ausstellerliste, die vom Server in der Authentifizierungs Aufforderung bereitgestellt wird.</span><span class="sxs-lookup"><span data-stu-id="305eb-144">For computers running on Windows Server 2008 and Windows Vista, WinHttp enables the application to retrieve the certificate issuer list supplied by the server in the authentication challenge.</span></span> <span data-ttu-id="305eb-145">In der Liste Aussteller wird eine Liste der Zertifizierungsstellen (CAS) angegeben, die vom Server zum Ausstellen von Client Zertifikaten autorisiert werden.</span><span class="sxs-lookup"><span data-stu-id="305eb-145">The Issuer List specifies a list of Certificate Authorities (CAs) that are authorized by the server to issue client certificates.</span></span> <span data-ttu-id="305eb-146">Die Anwendung filtert die Liste der Aussteller, um das erforderliche Zertifikat zu erhalten.</span><span class="sxs-lookup"><span data-stu-id="305eb-146">The application filters the issuer list to obtain the required certificate.</span></span>

<span data-ttu-id="305eb-147">Die WinHTTP-Client Anwendung ruft die Ausstellerliste ab, wenn [**WinHttpSendRequest**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpsendrequest)oder [**WinHttpReceiveResponse**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpreceiveresponse) den **Fehler " \_ WinHTTP- \_ Client Authentifizierungs \_ \_ Zertifikat \_ erforderlich**" zurückgibt.</span><span class="sxs-lookup"><span data-stu-id="305eb-147">The WinHttp client application retrieves the issuer list when [**WinHttpSendRequest**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpsendrequest), or [**WinHttpReceiveResponse**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpreceiveresponse) returns **ERROR\_WINHTTP\_CLIENT\_AUTH\_CERT\_NEEDED**.</span></span> <span data-ttu-id="305eb-148">Wenn dieser Fehler zurückgegeben wird, ruft die Anwendung [**WinHttpQueryOption**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpqueryoption) mit der Option **WinHTTP- \_ Option \_ Client \_ Zertifikat \_ Aussteller \_ Liste** auf.</span><span class="sxs-lookup"><span data-stu-id="305eb-148">When this error is returned, the application calls [**WinHttpQueryOption**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpqueryoption) with the **WINHTTP\_OPTION\_CLIENT\_CERT\_ISSUER\_LIST** option.</span></span> <span data-ttu-id="305eb-149">Der *lpBuffer* -Parameter muss groß genug sein, um einen Zeiger auf die [secpkgcontext \_ issuerlistinfoex](/windows/desktop/api/schannel/ns-schannel-secpkgcontext_issuerlistinfoex) -Struktur zu enthalten.</span><span class="sxs-lookup"><span data-stu-id="305eb-149">The *lpBuffer* parameter must be large enough to contain a pointer to the [SecPkgContext\_IssuerListInfoEx](/windows/desktop/api/schannel/ns-schannel-secpkgcontext_issuerlistinfoex) structure.</span></span> <span data-ttu-id="305eb-150">Im folgenden Codebeispiel wird gezeigt, wie die Ausstellerliste abgerufen wird.</span><span class="sxs-lookup"><span data-stu-id="305eb-150">The following code example shows how to retrieve the issuer list.</span></span>


```C++
#include <windows.h>
#include <winhttp.h>
#include <schannel.h>

//...

void GetIssuerList(HINTERNET hRequest)
{
  SecPkgContext_IssuerListInfoEx* pIssuerList = NULL;
  DWORD dwBufferSize = sizeof(SecPkgContext_IssuerListInfoEx*);

  if (WinHttpQueryOption(hRequest,
           WINHTTP_OPTION_CLIENT_CERT_ISSUER_LIST,
           &pIssuerList,
           &dwBufferSize) == TRUE)
  {
    // Use the pIssuerList for cert store filtering.
    GlobalFree(pIssuerList); // Free the issuer list when done.
  }
}
```



<span data-ttu-id="305eb-151">Die Informationen in der [secpkgcontext-Struktur \_ issuerlistinfoex](/windows/desktop/api/schannel/ns-schannel-secpkgcontext_issuerlistinfoex) , *cissuer* und *aaussteller* können verwendet werden, um nach dem Zertifikat zu suchen, wie im folgenden Codebeispiel gezeigt.</span><span class="sxs-lookup"><span data-stu-id="305eb-151">The information in the [SecPkgContext\_IssuerListInfoEx](/windows/desktop/api/schannel/ns-schannel-secpkgcontext_issuerlistinfoex) structure, *cIssuers* and *aIssuers*, can be used to search for the certificate as shown in the code example below.</span></span> <span data-ttu-id="305eb-152">Weitere Informationen finden Sie unter [**certfindchaininstore**](/windows/desktop/api/wincrypt/nf-wincrypt-certfindchaininstore).</span><span class="sxs-lookup"><span data-stu-id="305eb-152">For more information, see [**CertFindChainInStore**](/windows/desktop/api/wincrypt/nf-wincrypt-certfindchaininstore).</span></span>


```C++
PCERT_CONTEXT pClientCert = NULL;
PCCERT_CHAIN_CONTEXT pClientCertChain = NULL;

CERT_CHAIN_FIND_BY_ISSUER_PARA SrchCriteria;
::ZeroMemory(&SrchCriteria, sizeof(CERT_CHAIN_FIND_BY_ISSUER_PARA));
SrchCriteria.cbSize = sizeof(CERT_CHAIN_FIND_BY_ISSUER_PARA);

SrchCriteria.cIssuer = pIssuerList->cIssuers;
SrchCriteria.rgIssuer = pIssuerList->aIssuers;

pClientCertChain = CertFindChainInStore(
            hClientCertStore,
            X509_ASN_ENCODING,
            CERT_CHAIN_FIND_BY_ISSUER_CACHE_ONLY_URL_FLAG |
            // Do not perform wire download when building chains.
            CERT_CHAIN_FIND_BY_ISSUER_CACHE_ONLY_FLAG,
            // Do not search pCacheEntry->_ClientCertStore 
            // for issuer certs.
            CERT_CHAIN_FIND_BY_ISSUER,
            &SrchCriteria,
            NULL);

if (pClientCertChain)
{
    pClientCert = (PCERT_CONTEXT) pClientCertChain->rgpChain[0]->rgpElement[0]->pCertContext;

    CertDuplicateCertificateContext(pClientCert);

    CertFreeCertificateChain(pClientCertChain);

    pClientCertChain = NULL;
}
```



### <a name="optional-client-ssl-certificates"></a><span data-ttu-id="305eb-153">Optionale Client-SSL-Zertifikate</span><span class="sxs-lookup"><span data-stu-id="305eb-153">Optional Client SSL Certificates</span></span>

<span data-ttu-id="305eb-154">Ab Windows Server 2008 und Windows Vista unterstützt die WinHTTP-API optionale Client Zertifikate.</span><span class="sxs-lookup"><span data-stu-id="305eb-154">Starting in Windows Server 2008 and Windows Vista, the WinHttp API supports optional client certificates.</span></span> <span data-ttu-id="305eb-155">Wenn der Server ein Client Zertifikat anfordert, gibt [**WinHttpSendRequest**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpsendrequest)oder [**winhttprecieveresponse**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpreceiveresponse) einen Fehler an, dass ein Fehler für das **\_ WinHTTP-Client Authentifizierungszertifikat \_ \_ \_ \_ erforderlich** ist.</span><span class="sxs-lookup"><span data-stu-id="305eb-155">When the server requests a client certificate, [**WinHttpSendRequest**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpsendrequest), or [**WinHttpRecieveResponse**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpreceiveresponse) returns an **ERROR\_WINHTTP\_CLIENT\_AUTH\_CERT\_NEEDED** error.</span></span> <span data-ttu-id="305eb-156">Wenn der Server das Zertifikat anfordert, dies jedoch nicht erfordert, kann die Anwendung diese Option angeben, um anzugeben, dass Sie über kein Zertifikat verfügt.</span><span class="sxs-lookup"><span data-stu-id="305eb-156">If the server requests the certificate, but does not require it, the application can specify this option to indicate that it does not have a certificate.</span></span> <span data-ttu-id="305eb-157">Der Server kann ein anderes Authentifizierungsschema auswählen oder den anonymen Zugriff auf den Server zulassen.</span><span class="sxs-lookup"><span data-stu-id="305eb-157">The server can choose another authentication scheme or allow anonymous access to the server.</span></span> <span data-ttu-id="305eb-158">Die Anwendung gibt das **WinHTTP \_ No \_ Client \_ CERT- \_ Kontext** Makro im *lpBuffer* -Parameter von [**WinHttpSetOption**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpsetoption) an, wie im folgenden Codebeispiel gezeigt.</span><span class="sxs-lookup"><span data-stu-id="305eb-158">The application specifies the **WINHTTP\_NO\_CLIENT\_CERT\_CONTEXT** macro in the *lpBuffer* parameter of [**WinHttpSetOption**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpsetoption) as shown in the following code example.</span></span>

``` syntax
BOOL fRet = WinHttpSetOption ( hRequest,
                               WINHTTP_OPTION_CLIENT_CERT_CONTEXT,
                               WINHTTP_NO_CLIENT_CERT_CONTEXT,
                               0);
```

<span data-ttu-id="305eb-159">Wenn für den **WinHTTP- \_ \_ Client kein Client Zertifikat \_ \_ Kontext** festgelegt ist und für den Server weiterhin ein Client Zertifikat erforderlich ist, sendet er möglicherweise den HTTP-Statuscode 403.</span><span class="sxs-lookup"><span data-stu-id="305eb-159">If the **WINHTTP\_NO\_CLIENT\_CERT\_CONTEXT** is set, and the server still requires a client certificate, it may send a 403 HTTP status code.</span></span> <span data-ttu-id="305eb-160">Weitere Informationen finden Sie in der Option **WinHTTP- \_ Option \_ Client \_ Zertifikat \_ Aussteller \_ Liste** .</span><span class="sxs-lookup"><span data-stu-id="305eb-160">For more information, see the **WINHTTP\_OPTION\_CLIENT\_CERT\_ISSUER\_LIST** option.</span></span>

### <a name="winhttprequest-object"></a><span data-ttu-id="305eb-161">WinHttpRequest-Objekt</span><span class="sxs-lookup"><span data-stu-id="305eb-161">WinHttpRequest Object</span></span>

<span data-ttu-id="305eb-162">Verwenden Sie die [**setclientcertificate**](iwinhttprequest-setclientcertificate.md) -Methode des [**WinHttpRequest**](winhttprequest.md) -Objekts, um Client Zertifikate auszuwählen, die mit einer Anforderung an den Server gesendet werden sollen.</span><span class="sxs-lookup"><span data-stu-id="305eb-162">Use the [**SetClientCertificate**](iwinhttprequest-setclientcertificate.md) method of the [**WinHttpRequest**](winhttprequest.md) object to select client certificates to send to the server with a request.</span></span> <span data-ttu-id="305eb-163">Wählen Sie ein Zertifikat aus, indem Sie eine Zertifikat Auswahl Zeichenfolge mit der [**setclientcertificate**](iwinhttprequest-setclientcertificate.md) -Methode angeben.</span><span class="sxs-lookup"><span data-stu-id="305eb-163">Select a certificate by specifying a certificate selection string with the [**SetClientCertificate**](iwinhttprequest-setclientcertificate.md) method.</span></span> <span data-ttu-id="305eb-164">Die Zertifikat Auswahl Zeichenfolge besteht aus dem Zertifikat Speicherort, dem [*Zertifikat Speicher*](glossary.md)und dem Antragsteller Namen, die durch umgekehrte Schrägstriche voneinander getrennt sind.</span><span class="sxs-lookup"><span data-stu-id="305eb-164">The certificate selection string consists of the certificate location, [*certificate store*](glossary.md), and subject name delimited by backslashes.</span></span> <span data-ttu-id="305eb-165">In der folgenden Tabelle sind die Komponenten für diese Auswahl Zeichenfolge aufgeführt.</span><span class="sxs-lookup"><span data-stu-id="305eb-165">The following table lists components for this selection string.</span></span>



| <span data-ttu-id="305eb-166">Komponente</span><span class="sxs-lookup"><span data-stu-id="305eb-166">Component</span></span>                                                  | <span data-ttu-id="305eb-167">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="305eb-167">Description</span></span>                                                                                                                                                                                        | <span data-ttu-id="305eb-168">Mögliche Werte</span><span class="sxs-lookup"><span data-stu-id="305eb-168">Possible values</span></span>                                                                                                                                                                                                                                                                                                                       |
|------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="305eb-169">Standort</span><span class="sxs-lookup"><span data-stu-id="305eb-169">Location</span></span>                                                   | <span data-ttu-id="305eb-170">Bestimmt den Registrierungsschlüssel, unter dem die Zertifikate gespeichert werden.</span><span class="sxs-lookup"><span data-stu-id="305eb-170">Determines the registry key under which the certificates are stored.</span></span>                                                                                                                               | <span data-ttu-id="305eb-171">Mögliche Werte sind "lokaler \_ Computer", um anzugeben, dass sich der [*Zertifikat Speicher*](glossary.md) unter dem **lokalen HKEY- \_ \_ Computer** befindet.</span><span class="sxs-lookup"><span data-stu-id="305eb-171">The possible values are "LOCAL\_MACHINE" to indicate that the [*certificate store*](glossary.md) is under **HKEY\_LOCAL\_MACHINE**</span></span><br/> <span data-ttu-id="305eb-172">und "aktueller \_ Benutzer", um anzugeben, dass sich der *Zertifikat Speicher* unter dem **aktuellen HKEY- \_ \_ Benutzer** befindet, der nicht als Identitätswechsel verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="305eb-172">and "CURRENT\_USER" to indicate that the *certificate store* is under the non-impersonated **HKEY\_CURRENT\_USER.**</span></span><br/> <span data-ttu-id="305eb-173">Bei dieser Komponente wird die Groß-/Kleinschreibung beachtet.</span><span class="sxs-lookup"><span data-stu-id="305eb-173">This component is case-sensitive.</span></span> |
| [<span data-ttu-id="305eb-174">*Zertifikat Speicher*</span><span class="sxs-lookup"><span data-stu-id="305eb-174">*Certificate store*</span></span>](glossary.md) | <span data-ttu-id="305eb-175">Gibt den Namen des [*Zertifikat Speicher*](glossary.md) an, der das relevante Zertifikat enthält.</span><span class="sxs-lookup"><span data-stu-id="305eb-175">Indicates the name of the [*certificate store*](glossary.md) that contains the relevant certificate.</span></span>                                                                       | <span data-ttu-id="305eb-176">Typische [*Zertifikat Speicher*](glossary.md) sind "My", "root" und "treudpeople".</span><span class="sxs-lookup"><span data-stu-id="305eb-176">Typical [*certificate stores*](glossary.md) are "MY", "Root", and "TrustedPeople".</span></span> <span data-ttu-id="305eb-177">Bei dieser Komponente wird die Groß-/Kleinschreibung beachtet.</span><span class="sxs-lookup"><span data-stu-id="305eb-177">This component is case-sensitive.</span></span>                                                                                                                                                                                          |
| <span data-ttu-id="305eb-178">Antragstellername</span><span class="sxs-lookup"><span data-stu-id="305eb-178">Subject name</span></span>                                               | <span data-ttu-id="305eb-179">Identifiziert ein Zertifikat im angegebenen [*Zertifikat Speicher*](glossary.md).</span><span class="sxs-lookup"><span data-stu-id="305eb-179">Identifies a certificate within the specified [*certificate store*](glossary.md).</span></span> <span data-ttu-id="305eb-180">Das erste Zertifikat, das die für diese Komponente angegebene Zeichenfolge enthält, wird ausgewählt.</span><span class="sxs-lookup"><span data-stu-id="305eb-180">The first certificate that contains the string specified for this component is selected.</span></span> | <span data-ttu-id="305eb-181">Der Antragsteller Name kann eine beliebige Zeichenfolge sein.</span><span class="sxs-lookup"><span data-stu-id="305eb-181">The subject name can be any string.</span></span> <span data-ttu-id="305eb-182">Eine leere Zeichenfolge gibt an, dass das erste Zertifikat im [*Zertifikat Speicher*](glossary.md) verwendet werden soll.</span><span class="sxs-lookup"><span data-stu-id="305eb-182">A blank string indicates that the first certificate in the [*certificate store*](glossary.md) should be used.</span></span> <span data-ttu-id="305eb-183">Bei dieser Komponente wird keine Groß-/Kleinschreibung beachtet.</span><span class="sxs-lookup"><span data-stu-id="305eb-183">This component is case-insensitive.</span></span>                                                                                                                         |



 

<span data-ttu-id="305eb-184">Der Name und Speicherort des [*Zertifikat Speicher*](glossary.md) sind optionale Komponenten.</span><span class="sxs-lookup"><span data-stu-id="305eb-184">The [*certificate store*](glossary.md) name and location are optional components.</span></span> <span data-ttu-id="305eb-185">Wenn Sie jedoch einen *Zertifikat Speicher* angeben, müssen Sie auch den Speicherort dieses *Zertifikat Speicher* angeben.</span><span class="sxs-lookup"><span data-stu-id="305eb-185">However, if you specify a *certificate store*, you must also specify the location of that *certificate store*.</span></span> <span data-ttu-id="305eb-186">Der Standard Speicherort ist aktueller \_ Benutzer und der Standard *Zertifikat Speicher* "My".</span><span class="sxs-lookup"><span data-stu-id="305eb-186">The default location is CURRENT\_USER and the default *certificate store* is "MY".</span></span>

<span data-ttu-id="305eb-187">Im folgenden Codebeispiel wird gezeigt, wie angegeben wird, dass ein Zertifikat mit dem Betreff "My Middle-Tier Certificate" aus dem [*Zertifikat Speicher*](glossary.md) "persönlich" in der Registrierung unter **HKEY \_ local \_ Machine** ausgewählt werden soll.</span><span class="sxs-lookup"><span data-stu-id="305eb-187">The following code example shows how to specify that a certificate with the subject "My Middle-Tier Certificate" should be chosen from the "Personal" [*certificate store*](glossary.md) in the registry under **HKEY\_LOCAL\_MACHINE**.</span></span>

`HttpReq.SetClientCertificate("LOCAL_MACHINE\Personal\My Middle-Tier Certificate")`

> [!Note]  
> <span data-ttu-id="305eb-188">In manchen Sprachen ist der umgekehrte Schrägstrich ein Escapezeichen.</span><span class="sxs-lookup"><span data-stu-id="305eb-188">In some languages the backslash is an escape character.</span></span> <span data-ttu-id="305eb-189">Denken Sie daran, die Zertifikat Auswahl Zeichenfolge zu ändern, um dies zu berücksichtigen.</span><span class="sxs-lookup"><span data-stu-id="305eb-189">Remember to modify the certificate selection string to account for this.</span></span> <span data-ttu-id="305eb-190">Verwenden Sie z. b. in Microsoft JScript zwei aufeinander folgende umgekehrte Schrägstriche anstelle eines.</span><span class="sxs-lookup"><span data-stu-id="305eb-190">For example, in Microsoft JScript, use two adjacent backslashes instead of one.</span></span>

 

<span data-ttu-id="305eb-191">Wenn Sie kein Zertifikat angeben und ein HTTPS-Server ein Client Zertifikat erfordert, wählt WinHTTP das erste Zertifikat im Standard [*Zertifikat Speicher*](glossary.md)aus.</span><span class="sxs-lookup"><span data-stu-id="305eb-191">If you do not specify a certificate and an HTTPS server requires a client certificate, WinHTTP selects the first certificate in the default [*certificate store*](glossary.md).</span></span> <span data-ttu-id="305eb-192">Wenn keine Zertifikate vorhanden sind, wird ein Fehler ausgelöst.</span><span class="sxs-lookup"><span data-stu-id="305eb-192">If no certificates exist, an error is raised.</span></span> <span data-ttu-id="305eb-193">Wenn das Zertifikat nicht akzeptiert wird, gibt der Server den Statuscode 403 zurück, um anzugeben, dass die Anforderung nicht erfüllt werden kann.</span><span class="sxs-lookup"><span data-stu-id="305eb-193">If the certificate is not accepted, the server returns a 403 status code to indicate that the request cannot be fulfilled.</span></span> <span data-ttu-id="305eb-194">Sie können dann ein geeignetere Zertifikat mit [**setclientcertificate**](iwinhttprequest-setclientcertificate.md) auswählen und die Anforderung erneut senden.</span><span class="sxs-lookup"><span data-stu-id="305eb-194">You can then choose a more appropriate certificate with [**SetClientCertificate**](iwinhttprequest-setclientcertificate.md) and resend the request.</span></span>

 

