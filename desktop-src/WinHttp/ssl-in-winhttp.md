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
# <a name="ssl-in-winhttp"></a>SSL in WinHTTP

Die Microsoft Windows HTTP-Dienste (WinHTTP) unterstützen Secure Sockets Layer (SSL)-Transaktionen, einschließlich Client Zertifikate. In diesem Thema werden Konzepte erläutert, die an einer SSL-Transaktion beteiligt sind und wie Sie mit WinHTTP behandelt werden.

## <a name="secure-sockets-layer"></a>Secure Sockets Layer

SSL ist ein etablierter Standard, um sichere HTTP-Transaktionen sicherzustellen. SSL bietet einen Mechanismus, mit dem bis zu 128-Bit-Verschlüsselung für alle Transaktionen zwischen Client und Server durchgeführt werden können. Dadurch kann der Client überprüfen, ob der Server zu einer vertrauenswürdigen Entität gehört, indem Server Zertifikate verwendet werden. Außerdem kann der Server die Identität des Clients mit Client Zertifikaten bestätigen.

Bei jedem dieser Probleme werden Verschlüsselung, Server Identität und Client Identität im SSL-Handshake ausgehandelt, der auftritt, wenn ein Client zuerst eine Ressource von einem HTTPS-Server (Secure Hypertext Transfer Protocol) anfordert. Im Wesentlichen stellen Client und Server jeweils eine Liste der erforderlichen und bevorzugten Einstellungen dar. Wenn ein allgemeiner Satz von Anforderungen vereinbart und erfüllt werden kann, wird eine SSL-Verbindung hergestellt.

WinHTTP stellt eine allgemeine Schnittstelle für die Verwendung von SSL bereit. Während die Details des SSL-Handshakes und der Transaktion intern behandelt werden, können Sie mit WinHTTP Verschlüsselungsstufen abrufen, das Sicherheitsprotokoll angeben und mit Server-und Client Zertifikaten interagieren. Die folgenden Abschnitte enthalten ausführliche Informationen zum Erstellen von WinHTTP-basierten Anwendungen, die eine SSL-Protokollversion auswählen, Server Zertifikate untersuchen und Client Zertifikate auswählen, die an HTTPS-Server gesendet werden sollen.

## <a name="server-certificates"></a>Serverzertifikate

Server Zertifikate werden vom Server an den Client gesendet, sodass der Client einen öffentlichen Schlüssel für den Server abrufen und sicherstellen kann, dass der Server von einer Zertifizierungsstelle überprüft wurde. Zertifikate können verschiedene Datentypen enthalten. Ein X. 509-Zertifikat enthält z. b. das Format des Zertifikats, die Seriennummer des Zertifikats, den Algorithmus, der zum Signieren des Zertifikats verwendet wird, den Namen der Zertifizierungsstelle, die das Zertifikat ausgestellt hat, den Namen und den öffentlichen Schlüssel der Entität, die das Zertifikat anfordert, und die Signatur der Zertifizierungsstelle.

Wenn Sie die WinHTTP-API (Application Programming Interface) verwenden, können Sie ein Serverzertifikat abrufen, indem Sie [**WinHttpQueryOption**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpqueryoption) aufrufen und die [**WinHTTP- \_ Option \_ \_ sicherheitszertifikatstruktursflag \_**](option-flags.md) angeben. Das Serverzertifikat wird in einer [**WinHTTP- \_ Zertifikats \_ Informations**](/windows/win32/api/winhttp/ns-winhttp-winhttp_certificate_info) Struktur zurückgegeben. Wenn Sie den Zertifikat Kontext abrufen möchten, geben Sie stattdessen die [**WinHTTP- \_ Option \_ Server \_ CERT- \_ Kontext**](option-flags.md) Kennzeichen an.

Wenn ein Serverzertifikat Fehler enthält, können Details zu diesem Fehler in der Status Rückruffunktion abgerufen werden. Die Benachrichtigung "sicherer Fehler bei [**WinHTTP- \_ Rückruf \_ Status \_ \_**](/windows/win32/api/winhttp/nc-winhttp-winhttp_status_callback) " weist auf einen Fehler mit einem Serverzertifikat hin. Der *lpvstatusinformation* -Parameter enthält ein oder mehrere ausführliche Fehlerflags. Weitere Informationen finden Sie unter [**WinHTTP- \_ Status \_ Rückruf**](/windows/win32/api/winhttp/nc-winhttp-winhttp_status_callback) .

## <a name="client-certificates"></a>Clientzertifikate

Während des SSL-Handshakes benötigt der Server möglicherweise eine Authentifizierung. Der Client wird authentifiziert, indem ein gültiges Client Zertifikat für den Server bereitgestellt wird. WinHTTP ermöglicht das auswählen und Senden eines Zertifikats aus einem lokalen [*Zertifikat Speicher*](glossary.md). In den folgenden Abschnitten wird der Prozess beschrieben, der Client Zertifikate bereitstellt, wenn entweder die WinHTTP-API oder das [**WinHttpRequest**](winhttprequest.md) -Objekt verwendet wird.

### <a name="winhttp-api"></a>WinHTTP-API

Sowohl [**WinHttpSendRequest**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpsendrequest) als auch [**WinHttpReceiveResponse**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpreceiveresponse) können nicht angeben, dass eine Anforderung nicht erfolgreich war, weil der HTTPS-Server eine Authentifizierung erfordert. In diesen Fällen wird [**GetLastError**](/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror) aufgerufen, um den Fehler für das \_ WinHTTP-Client Authentifizierungszertifikat zurückgegeben \_ \_ \_ \_ . Verwenden Sie nach dem Empfang dieses Fehlers die entsprechenden [kryptoapi](/windows/desktop/SecCrypto/cryptography-functions) -Funktionen, um ein entsprechendes Zertifikat zu finden. Geben Sie an, dass dieses Zertifikat mit der nächsten Anforderung gesendet werden soll, indem Sie [**WinHttpSetOption**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpsetoption) mit der [**WinHTTP- \_ Option \_ Client \_ CERT- \_ Kontext**](option-flags.md) Kennzeichen aufrufen.

Im folgenden Codebeispiel wird veranschaulicht, wie Sie einen [*Zertifikat Speicher*](glossary.md) öffnen und nach einem nach dem Antragsteller Namen basierenden Zertifikat suchen, nachdem der Fehler " \_ WinHTTP-Client Authentifizierungszertifikat erforderlich" \_ \_ \_ \_ zurückgegeben wurde.


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



Vor dem erneuten Senden einer Anforderung, die ein Client Zertifikat enthält, können Sie bestimmen, ob die unterstützte Verschlüsselungs Stufe für Ihre Anwendung zulässig ist. Wenden Sie [**WinHttpQueryOption**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpqueryoption) an, und geben Sie das Flag für die [**WinHTTP- \_ Option \_ \_ sicherheitsflags**](option-flags.md) an, um die verwendete Verschlüsselungs Ebene zu bestimmen.

### <a name="issuer-list-retrieval-for-ssl-client-authentication"></a>Abrufen der Ausstellerliste für die SSL-Client Authentifizierung

Wenn die WinHTTP-Client Anwendung eine Anforderung an einen sicheren HTTP-Server sendet, der SSL-Client Authentifizierung erfordert, gibt WinHTTP einen Fehler zurück, der für das **\_ WinHTTP-Client Authentifizierungszertifikat \_ \_ \_ \_ erforderlich** ist, wenn die Anwendung kein Client Zertifikat bereitgestellt hat. Für Computer, die unter Windows Server 2008 und Windows Vista ausgeführt werden, ermöglicht WinHTTP der Anwendung das Abrufen der Zertifikat Ausstellerliste, die vom Server in der Authentifizierungs Aufforderung bereitgestellt wird. In der Liste Aussteller wird eine Liste der Zertifizierungsstellen (CAS) angegeben, die vom Server zum Ausstellen von Client Zertifikaten autorisiert werden. Die Anwendung filtert die Liste der Aussteller, um das erforderliche Zertifikat zu erhalten.

Die WinHTTP-Client Anwendung ruft die Ausstellerliste ab, wenn [**WinHttpSendRequest**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpsendrequest)oder [**WinHttpReceiveResponse**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpreceiveresponse) den **Fehler " \_ WinHTTP- \_ Client Authentifizierungs \_ \_ Zertifikat \_ erforderlich**" zurückgibt. Wenn dieser Fehler zurückgegeben wird, ruft die Anwendung [**WinHttpQueryOption**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpqueryoption) mit der Option **WinHTTP- \_ Option \_ Client \_ Zertifikat \_ Aussteller \_ Liste** auf. Der *lpBuffer* -Parameter muss groß genug sein, um einen Zeiger auf die [secpkgcontext \_ issuerlistinfoex](/windows/desktop/api/schannel/ns-schannel-secpkgcontext_issuerlistinfoex) -Struktur zu enthalten. Im folgenden Codebeispiel wird gezeigt, wie die Ausstellerliste abgerufen wird.


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



Die Informationen in der [secpkgcontext-Struktur \_ issuerlistinfoex](/windows/desktop/api/schannel/ns-schannel-secpkgcontext_issuerlistinfoex) , *cissuer* und *aaussteller* können verwendet werden, um nach dem Zertifikat zu suchen, wie im folgenden Codebeispiel gezeigt. Weitere Informationen finden Sie unter [**certfindchaininstore**](/windows/desktop/api/wincrypt/nf-wincrypt-certfindchaininstore).


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



### <a name="optional-client-ssl-certificates"></a>Optionale Client-SSL-Zertifikate

Ab Windows Server 2008 und Windows Vista unterstützt die WinHTTP-API optionale Client Zertifikate. Wenn der Server ein Client Zertifikat anfordert, gibt [**WinHttpSendRequest**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpsendrequest)oder [**winhttprecieveresponse**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpreceiveresponse) einen Fehler an, dass ein Fehler für das **\_ WinHTTP-Client Authentifizierungszertifikat \_ \_ \_ \_ erforderlich** ist. Wenn der Server das Zertifikat anfordert, dies jedoch nicht erfordert, kann die Anwendung diese Option angeben, um anzugeben, dass Sie über kein Zertifikat verfügt. Der Server kann ein anderes Authentifizierungsschema auswählen oder den anonymen Zugriff auf den Server zulassen. Die Anwendung gibt das **WinHTTP \_ No \_ Client \_ CERT- \_ Kontext** Makro im *lpBuffer* -Parameter von [**WinHttpSetOption**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpsetoption) an, wie im folgenden Codebeispiel gezeigt.

``` syntax
BOOL fRet = WinHttpSetOption ( hRequest,
                               WINHTTP_OPTION_CLIENT_CERT_CONTEXT,
                               WINHTTP_NO_CLIENT_CERT_CONTEXT,
                               0);
```

Wenn für den **WinHTTP- \_ \_ Client kein Client Zertifikat \_ \_ Kontext** festgelegt ist und für den Server weiterhin ein Client Zertifikat erforderlich ist, sendet er möglicherweise den HTTP-Statuscode 403. Weitere Informationen finden Sie in der Option **WinHTTP- \_ Option \_ Client \_ Zertifikat \_ Aussteller \_ Liste** .

### <a name="winhttprequest-object"></a>WinHttpRequest-Objekt

Verwenden Sie die [**setclientcertificate**](iwinhttprequest-setclientcertificate.md) -Methode des [**WinHttpRequest**](winhttprequest.md) -Objekts, um Client Zertifikate auszuwählen, die mit einer Anforderung an den Server gesendet werden sollen. Wählen Sie ein Zertifikat aus, indem Sie eine Zertifikat Auswahl Zeichenfolge mit der [**setclientcertificate**](iwinhttprequest-setclientcertificate.md) -Methode angeben. Die Zertifikat Auswahl Zeichenfolge besteht aus dem Zertifikat Speicherort, dem [*Zertifikat Speicher*](glossary.md)und dem Antragsteller Namen, die durch umgekehrte Schrägstriche voneinander getrennt sind. In der folgenden Tabelle sind die Komponenten für diese Auswahl Zeichenfolge aufgeführt.



| Komponente                                                  | BESCHREIBUNG                                                                                                                                                                                        | Mögliche Werte                                                                                                                                                                                                                                                                                                                       |
|------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Standort                                                   | Bestimmt den Registrierungsschlüssel, unter dem die Zertifikate gespeichert werden.                                                                                                                               | Mögliche Werte sind "lokaler \_ Computer", um anzugeben, dass sich der [*Zertifikat Speicher*](glossary.md) unter dem **lokalen HKEY- \_ \_ Computer** befindet.<br/> und "aktueller \_ Benutzer", um anzugeben, dass sich der *Zertifikat Speicher* unter dem **aktuellen HKEY- \_ \_ Benutzer** befindet, der nicht als Identitätswechsel verwendet wird.<br/> Bei dieser Komponente wird die Groß-/Kleinschreibung beachtet. |
| [*Zertifikat Speicher*](glossary.md) | Gibt den Namen des [*Zertifikat Speicher*](glossary.md) an, der das relevante Zertifikat enthält.                                                                       | Typische [*Zertifikat Speicher*](glossary.md) sind "My", "root" und "treudpeople". Bei dieser Komponente wird die Groß-/Kleinschreibung beachtet.                                                                                                                                                                                          |
| Antragstellername                                               | Identifiziert ein Zertifikat im angegebenen [*Zertifikat Speicher*](glossary.md). Das erste Zertifikat, das die für diese Komponente angegebene Zeichenfolge enthält, wird ausgewählt. | Der Antragsteller Name kann eine beliebige Zeichenfolge sein. Eine leere Zeichenfolge gibt an, dass das erste Zertifikat im [*Zertifikat Speicher*](glossary.md) verwendet werden soll. Bei dieser Komponente wird keine Groß-/Kleinschreibung beachtet.                                                                                                                         |



 

Der Name und Speicherort des [*Zertifikat Speicher*](glossary.md) sind optionale Komponenten. Wenn Sie jedoch einen *Zertifikat Speicher* angeben, müssen Sie auch den Speicherort dieses *Zertifikat Speicher* angeben. Der Standard Speicherort ist aktueller \_ Benutzer und der Standard *Zertifikat Speicher* "My".

Im folgenden Codebeispiel wird gezeigt, wie angegeben wird, dass ein Zertifikat mit dem Betreff "My Middle-Tier Certificate" aus dem [*Zertifikat Speicher*](glossary.md) "persönlich" in der Registrierung unter **HKEY \_ local \_ Machine** ausgewählt werden soll.

`HttpReq.SetClientCertificate("LOCAL_MACHINE\Personal\My Middle-Tier Certificate")`

> [!Note]  
> In manchen Sprachen ist der umgekehrte Schrägstrich ein Escapezeichen. Denken Sie daran, die Zertifikat Auswahl Zeichenfolge zu ändern, um dies zu berücksichtigen. Verwenden Sie z. b. in Microsoft JScript zwei aufeinander folgende umgekehrte Schrägstriche anstelle eines.

 

Wenn Sie kein Zertifikat angeben und ein HTTPS-Server ein Client Zertifikat erfordert, wählt WinHTTP das erste Zertifikat im Standard [*Zertifikat Speicher*](glossary.md)aus. Wenn keine Zertifikate vorhanden sind, wird ein Fehler ausgelöst. Wenn das Zertifikat nicht akzeptiert wird, gibt der Server den Statuscode 403 zurück, um anzugeben, dass die Anforderung nicht erfüllt werden kann. Sie können dann ein geeignetere Zertifikat mit [**setclientcertificate**](iwinhttprequest-setclientcertificate.md) auswählen und die Anforderung erneut senden.

 

