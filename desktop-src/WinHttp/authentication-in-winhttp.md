---
description: Einige HTTP-Server und Proxys erfordern eine Authentifizierung, bevor Sie den Zugriff auf Ressourcen im Internet zulassen. Die Microsoft Windows HTTP-Dienste (WinHTTP) unterstützen die Server-und Proxy Authentifizierung für HTTP-Sitzungen.
ms.assetid: 077d6275-8600-4091-b78e-419a41a2101a
title: Authentifizierung in WinHTTP
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4dd40e6da1f455e04e24fa740cf4d83da7e0472e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "104216172"
---
# <a name="authentication-in-winhttp"></a>Authentifizierung in WinHTTP

Einige HTTP-Server und Proxys erfordern eine Authentifizierung, bevor Sie den Zugriff auf Ressourcen im Internet zulassen. Die Microsoft Windows HTTP-Dienste (WinHTTP) unterstützen die Server-und Proxy Authentifizierung für HTTP-Sitzungen.

## <a name="about-http-authentication"></a>Informationen zur HTTP-Authentifizierung

Wenn eine Authentifizierung erforderlich ist, empfängt die HTTP-Anwendung den Statuscode 401 (Server erfordert Authentifizierung) oder 407 (Proxy erfordert Authentifizierung). Zusammen mit dem Statuscode sendet der Proxy oder Server einen oder mehrere Authentifizierungsheader: WWW-Authenticate (für die Server Authentifizierung) oder Proxy-Authenticate (für die Proxy Authentifizierung).

Jeder authentifizieren-Header enthält ein unterstütztes Authentifizierungsschema und für das Basis-und Digest-Schema einen Bereich. Wenn mehrere Authentifizierungs Schemas unterstützt werden, gibt der Server mehrere authentifizieren-Header zurück. Beim Bereichs Wert wird die Groß-/Kleinschreibung beachtet, und es wird eine Gruppe von Servern oder Proxys definiert, für die dieselben Anmelde Informationen akzeptiert werden Beispielsweise kann der Header "www-Authenticate: Basic Realm =" example "" zurückgegeben werden, wenn eine Server Authentifizierung erforderlich ist. Dieser Header gibt an, dass Benutzer Anmelde Informationen für die "Beispiel Domäne" angegeben werden müssen.

Eine HTTP-Anwendung kann ein Autorisierungs Header Feld mit einer Anforderung enthalten, die Sie an den Server sendet. Der Autorisierungs Header enthält das Authentifizierungsschema und die entsprechende Antwort, die für dieses Schema erforderlich ist. Beispielsweise würde die Kopfzeile "Authorization: Basic <username: Password>" der Anforderung hinzugefügt und an den Server gesendet, wenn der Client den Antwortheader "www-Authenticate: Basic Realm =" example "" empfangen hat.

> [!Note]  
> Obwohl Sie hier als nur-Text angezeigt werden, sind der Benutzername und das Kennwort tatsächlich [*Base64-codiert*](glossary.md).

 

Es gibt zwei allgemeine Arten von Authentifizierungs Schemas:

-   Standard Authentifizierungsschema, in dem der Benutzername und das Kennwort als Klartext an den Server gesendet werden.

    Das Standard Authentifizierungsschema basiert auf dem Modell, das von einem Client mit einem Benutzernamen und einem Kennwort für jeden Bereich identifiziert werden muss. Der Server verwendet die Anforderung nur, wenn die Anforderung mit einem Autorisierungs Header gesendet wird, der einen gültigen Benutzernamen und ein gültiges Kennwort enthält.

-   Challenge-Response-Schemas, wie z. b. Kerberos, bei denen der Client den Client mit [*Authentifizierungsdaten*](glossary.md)herausfordert. Der Client wandelt die Daten mit den Benutzer Anmelde Informationen um und sendet die transformierten Daten zur Authentifizierung an den Server zurück.

    Mit Challenge-Response-Schemas wird eine sicherere Authentifizierung ermöglicht. In einem Challenge-Response-Schema werden Benutzername und Kennwort niemals über das Netzwerk übertragen. Nachdem der Client ein Challenge-Response-Schema ausgewählt hat, gibt der Server einen entsprechenden Statuscode mit einer Herausforderung zurück, die die [*Authentifizierungsdaten*](glossary.md) für dieses Schema enthält. Der Client sendet die Anforderung dann erneut mit der richtigen Antwort, um den angeforderten Dienst abzurufen. Mit Challenge-Response-Schemas können mehrere Austausch Vorgänge ausgeführt werden.

Die folgende Tabelle enthält die Authentifizierungs Schemas, die von WinHTTP unterstützt werden, den Authentifizierungstyp und eine Beschreibung des Schemas.



| Schema            | type               | BESCHREIBUNG                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                        |
|-------------------|--------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Basic (nur-Text) | Basic              | Verwendet eine [*Base64-codierte*](glossary.md) Zeichenfolge, die den Benutzernamen und das Kennwort enthält.                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                      |
| Digest            | Challenge-Response | Herausforderungen bei der Verwendung eines Nonce-Werts (eine vom Server angegebene Daten Zeichenfolge). Eine gültige Antwort enthält eine Prüfsumme aus dem Benutzernamen, dem Kennwort, dem angegebenen Nonce-Wert, dem [*http-Verb*](glossary.md)und dem angeforderten Uniform Resource Identifier (URI).                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                  |
| NTLM              | Challenge-Response | Erfordert, dass die [*Authentifizierungsdaten*](glossary.md) mit den Benutzer Anmelde Informationen transformiert werden, um die Identität nachzuweisen. Damit die NTLM-Authentifizierung ordnungsgemäß funktioniert, müssen mehrere Austausch Vorgänge für dieselbe Verbindung stattfinden. Daher kann die NTLM-Authentifizierung nicht verwendet werden, wenn ein zwischengeschalteter Proxy keine Keep-Alive-Verbindungen unterstützt. Die NTLM-Authentifizierung schlägt auch fehl, wenn [**WinHttpSetOption**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpsetoption) mit dem WinHTTP-Flag " [**\_ Keep- \_ \_ Alive deaktivieren**](option-flags.md) " verwendet wird, das die Keep-Alive-Semantik deaktiviert.                                                                                                                                                                                                                                       |
| Passport          | Challenge-Response | Verwendet [Microsoft Passport 1,4](passport-authentication-in-winhttp.md).                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                             |
| Aushandeln         | Challenge-Response | Wenn sowohl der Server als auch der Client Windows 2000 oder höher verwenden, wird die Kerberos-Authentifizierung verwendet. Andernfalls wird die NTLM-Authentifizierung verwendet. Kerberos ist in Windows 2000 und höheren Betriebssystemen verfügbar und wird als sicherer als die NTLM-Authentifizierung eingestuft. Damit die Aushandlungs Authentifizierung ordnungsgemäß funktioniert, müssen mehrere Austausch Vorgänge für dieselbe Verbindung stattfinden. Daher können Aushandlungs Authentifizierung nicht verwendet werden, wenn ein zwischengeschalteter Proxy keine Keep-Alive-Verbindungen unterstützt. Bei der Aushandlung der Authentifizierung tritt auch dann ein Fehler auf, wenn [**WinHttpSetOption**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpsetoption) mit dem WinHTTP-Flag zum Aktivieren von [**\_ Keep- \_ \_ Alive**](option-flags.md) verwendet wird Das Aushandlungs Authentifizierungsschema wird manchmal als integrierte Windows-Authentifizierung bezeichnet. |



 

## <a name="authentication-in-winhttp-applications"></a>Authentifizierung in WinHTTP-Anwendungen

Die WinHTTP-API (Application Programming Interface) stellt zwei Funktionen bereit, die für den Zugriff auf Internet Ressourcen in Situationen verwendet werden, in denen eine Authentifizierung erforderlich ist: [**winhttpsetanmelde**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpsetcredentials) Informationen und [**winhttpqueryauthschemas**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpqueryauthschemes).

Wenn eine Antwort mit einem 401-oder 407-Statuscode empfangen wird, kann [**winhttpqueryauthschemas**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpqueryauthschemes) zum Analysieren der Authentifizierungs Header verwendet werden, um die unterstützten Authentifizierungs Schemas und das Authentifizierungs Ziel zu ermitteln. Das Authentifizierungs Ziel ist der Server oder Proxy, der die Authentifizierung anfordert. **Winhttpqueryauthschemas** bestimmt auch das erste Authentifizierungsschema aus den verfügbaren Schemas, basierend auf den vom Server empfohlenen Authentifizierungsschema Einstellungen. Diese Methode zum Auswählen eines Authentifizierungs Schemas ist das von [RFC 2616](https://www.ietf.org/rfc/rfc2616.txt)vorgeschlagene Verhalten.

Mit [**winhttpsetanmelde**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpsetcredentials) Informationen kann eine Anwendung das Authentifizierungsschema angeben, das zusammen mit einem gültigen Benutzernamen und Kennwort für die Verwendung auf dem Zielserver oder Proxy verwendet wird. Nachdem Sie die Anmelde Informationen festgelegt und die Anforderung erneut gesendet haben, werden die erforderlichen Header generiert und automatisch der Anforderung hinzugefügt. Da für einige Authentifizierungs Schemas mehrere Transaktionen erforderlich sind, kann [**WinHttpSendRequest**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpsendrequest) den Fehler "Fehler bei \_ WinHTTP \_ Resend Request" zurückgeben \_ . Wenn dieser Fehler auftritt, sollte die Anwendung die Anforderung weiter senden, bis eine Antwort empfangen wird, die keinen 401-oder 407-Statuscode enthält. Der 200-Statuscode gibt an, dass die Ressource verfügbar ist und die Anforderung erfolgreich ist. Weitere Status Codes, die zurückgegeben werden können, finden Sie unter [**HTTP-Statuscodes**](http-status-codes.md) .

Wenn ein akzeptables Authentifizierungsschema und Anmelde Informationen bekannt sind, bevor eine Anforderung an den Server gesendet wird, kann eine Anwendung [**winhttpsetanmelde**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpsetcredentials) Informationen aufrufen, bevor [**WinHttpSendRequest**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpsendrequest)aufgerufen wird. In diesem Fall versucht WinHTTP die Vorauthentifizierung beim Server durch Bereitstellen von Anmelde Informationen oder [*Authentifizierungsdaten*](glossary.md) in der ursprünglichen Anforderung an den Server. Die Vorauthentifizierung kann die Anzahl der Austausch Vorgänge im Authentifizierungsprozess verringern und somit die Anwendungsleistung verbessern.

Die Vorauthentifizierung kann mit den folgenden Authentifizierungs Schemas verwendet werden:

-   Basic: immer möglich.
-   Aushandlung in Kerberos aushandeln (sehr wahrscheinlich möglich) die einzige Ausnahme ist, wenn die Zeitverschiebung zwischen dem Client und dem Domänen Controller deaktiviert ist.
-   (Aushandeln in NTLM aushandeln)-nie möglich.
-   NTLM-möglich nur in Windows Server 2008 R2.
-   Digest: nie möglich.
-   Passport-nie möglich; nach der anfänglichen Abfrage Antwort verwendet WinHTTP Cookies, um sich vorab bei Passport zu authentifizieren.

Eine typische WinHTTP-Anwendung führt die folgenden Schritte aus, um die Authentifizierung zu verarbeiten.

-   Fordern Sie eine Ressource mit " [**winhttpopanrequest**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpopenrequest) " und " [**WinHttpSendRequest**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpsendrequest)" an.
-   Überprüfen Sie die Antwortheader mit [**WinHttpQueryHeaders**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpqueryheaders).
-   Wenn ein 401-oder 407-Statuscode zurückgegeben wird, der angibt, dass eine Authentifizierung erforderlich ist, wenden Sie [**winhttpqueryauthschemas**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpqueryauthschemes) an, um ein akzeptables Schema
-   Legen Sie das Authentifizierungsschema, den Benutzernamen und das Kennwort mit [**winhttpsetanmelde**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpsetcredentials)Informationen fest.
-   Senden Sie die Anforderung mit dem gleichen Anforderungs handle erneut, indem Sie [**WinHttpSendRequest**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpsendrequest)aufrufen.

Die von [**winhttpsetanmelde**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpsetcredentials) Informationen festgelegten Anmelde Informationen werden nur für eine Anforderung verwendet. WinHTTP speichert die Anmelde Informationen für die Verwendung in anderen Anforderungen nicht zwischen, was bedeutet, dass Anwendungen geschrieben werden müssen, die auf mehrere Anforderungen reagieren können. Wenn eine authentifizierte Verbindung wieder verwendet wird, werden andere Anforderungen möglicherweise nicht gestellt, aber Ihr Code sollte jederzeit auf eine Anforderung Antworten können.

### <a name="example-retrieving-a-document"></a>Beispiel: Abrufen eines Dokuments

Der folgende Beispielcode versucht, ein angegebenes Dokument von einem HTTP-Server abzurufen. Der Statuscode wird aus der Antwort abgerufen, um zu bestimmen, ob eine Authentifizierung erforderlich ist. Wenn ein 200-Statuscode gefunden wird, ist das Dokument verfügbar. Wenn ein Statuscode von 401 oder 407 gefunden wird, ist eine Authentifizierung erforderlich, bevor das Dokument abgerufen werden kann. Bei jedem anderen Statuscode wird eine Fehlermeldung angezeigt. Eine Liste der möglichen Status Codes finden Sie unter [**HTTP-Statuscodes**](http-status-codes.md) .


```C++
#include <windows.h>
#include <winhttp.h>
#include <stdio.h>

#pragma comment(lib, "winhttp.lib")

DWORD ChooseAuthScheme( DWORD dwSupportedSchemes )
{
  //  It is the server's responsibility only to accept 
  //  authentication schemes that provide a sufficient
  //  level of security to protect the servers resources.
  //
  //  The client is also obligated only to use an authentication
  //  scheme that adequately protects its username and password.
  //
  //  Thus, this sample code does not use Basic authentication  
  //  becaus Basic authentication exposes the client's username
  //  and password to anyone monitoring the connection.
  
  if( dwSupportedSchemes & WINHTTP_AUTH_SCHEME_NEGOTIATE )
    return WINHTTP_AUTH_SCHEME_NEGOTIATE;
  else if( dwSupportedSchemes & WINHTTP_AUTH_SCHEME_NTLM )
    return WINHTTP_AUTH_SCHEME_NTLM;
  else if( dwSupportedSchemes & WINHTTP_AUTH_SCHEME_PASSPORT )
    return WINHTTP_AUTH_SCHEME_PASSPORT;
  else if( dwSupportedSchemes & WINHTTP_AUTH_SCHEME_DIGEST )
    return WINHTTP_AUTH_SCHEME_DIGEST;
  else
    return 0;
}

struct SWinHttpSampleGet
{
  LPCWSTR szServer;
  LPCWSTR szPath;
  BOOL fUseSSL;
  LPCWSTR szServerUsername;
  LPCWSTR szServerPassword;
  LPCWSTR szProxyUsername;
  LPCWSTR szProxyPassword;
};

void WinHttpAuthSample( IN SWinHttpSampleGet *pGetRequest )
{
  DWORD dwStatusCode = 0;
  DWORD dwSupportedSchemes;
  DWORD dwFirstScheme;
  DWORD dwSelectedScheme;
  DWORD dwTarget;
  DWORD dwLastStatus = 0;
  DWORD dwSize = sizeof(DWORD);
  BOOL  bResults = FALSE;
  BOOL  bDone = FALSE;

  DWORD dwProxyAuthScheme = 0;
  HINTERNET  hSession = NULL, 
             hConnect = NULL,
             hRequest = NULL;

  // Use WinHttpOpen to obtain a session handle.
  hSession = WinHttpOpen( L"WinHTTP Example/1.0",  
                          WINHTTP_ACCESS_TYPE_DEFAULT_PROXY,
                          WINHTTP_NO_PROXY_NAME, 
                          WINHTTP_NO_PROXY_BYPASS, 0 );

  INTERNET_PORT nPort = ( pGetRequest->fUseSSL ) ? 
                        INTERNET_DEFAULT_HTTPS_PORT  :
                        INTERNET_DEFAULT_HTTP_PORT;

  // Specify an HTTP server.
  if( hSession )
    hConnect = WinHttpConnect( hSession, 
                               pGetRequest->szServer, 
                               nPort, 0 );

  // Create an HTTP request handle.
  if( hConnect )
    hRequest = WinHttpOpenRequest( hConnect, 
                                   L"GET", 
                                   pGetRequest->szPath,
                                   NULL, 
                                   WINHTTP_NO_REFERER, 
                                   WINHTTP_DEFAULT_ACCEPT_TYPES,
                                   ( pGetRequest->fUseSSL ) ? 
                                       WINHTTP_FLAG_SECURE : 0 );

  // Continue to send a request until status code 
  // is not 401 or 407.
  if( hRequest == NULL )
    bDone = TRUE;

  while( !bDone )
  {
    //  If a proxy authentication challenge was responded to, reset
    //  those credentials before each SendRequest, because the proxy  
    //  may require re-authentication after responding to a 401 or  
    //  to a redirect. If you don't, you can get into a 
    //  407-401-407-401- loop.
    if( dwProxyAuthScheme != 0 )
      bResults = WinHttpSetCredentials( hRequest, 
                                        WINHTTP_AUTH_TARGET_PROXY, 
                                        dwProxyAuthScheme, 
                                        pGetRequest->szProxyUsername,
                                        pGetRequest->szProxyPassword,
                                        NULL );
    // Send a request.
    bResults = WinHttpSendRequest( hRequest,
                                   WINHTTP_NO_ADDITIONAL_HEADERS,
                                   0,
                                   WINHTTP_NO_REQUEST_DATA,
                                   0, 
                                   0, 
                                   0 );

    // End the request.
    if( bResults )
      bResults = WinHttpReceiveResponse( hRequest, NULL );

    // Resend the request in case of 
    // ERROR_WINHTTP_RESEND_REQUEST error.
    if( !bResults && GetLastError( ) == ERROR_WINHTTP_RESEND_REQUEST)
        continue;

    // Check the status code.
    if( bResults ) 
      bResults = WinHttpQueryHeaders( hRequest, 
                                      WINHTTP_QUERY_STATUS_CODE |
                                      WINHTTP_QUERY_FLAG_NUMBER,
                                      NULL, 
                                      &dwStatusCode, 
                                      &dwSize, 
                                      NULL );

    if( bResults )
    {
      switch( dwStatusCode )
      {
        case 200: 
          // The resource was successfully retrieved.
          // You can use WinHttpReadData to read the 
          // contents of the server's response.
          printf( "The resource was successfully retrieved.\n" );
          bDone = TRUE;
          break;

        case 401:
          // The server requires authentication.
          printf(" The server requires authentication. Sending credentials...\n" );

          // Obtain the supported and preferred schemes.
          bResults = WinHttpQueryAuthSchemes( hRequest, 
                                              &dwSupportedSchemes, 
                                              &dwFirstScheme, 
                                              &dwTarget );

          // Set the credentials before resending the request.
          if( bResults )
          {
            dwSelectedScheme = ChooseAuthScheme( dwSupportedSchemes);

            if( dwSelectedScheme == 0 )
              bDone = TRUE;
            else
              bResults = WinHttpSetCredentials( hRequest, 
                                        dwTarget, 
                                        dwSelectedScheme,
                                        pGetRequest->szServerUsername,
                                        pGetRequest->szServerPassword,
                                        NULL );
          }

          // If the same credentials are requested twice, abort the
          // request.  For simplicity, this sample does not check
          // for a repeated sequence of status codes.
          if( dwLastStatus == 401 )
            bDone = TRUE;

          break;

        case 407:
          // The proxy requires authentication.
          printf( "The proxy requires authentication.  Sending credentials...\n" );

          // Obtain the supported and preferred schemes.
          bResults = WinHttpQueryAuthSchemes( hRequest, 
                                              &dwSupportedSchemes, 
                                              &dwFirstScheme, 
                                              &dwTarget );

          // Set the credentials before resending the request.
          if( bResults )
            dwProxyAuthScheme = ChooseAuthScheme(dwSupportedSchemes);

          // If the same credentials are requested twice, abort the
          // request.  For simplicity, this sample does not check 
          // for a repeated sequence of status codes.
          if( dwLastStatus == 407 )
            bDone = TRUE;
          break;

        default:
          // The status code does not indicate success.
          printf("Error. Status code %d returned.\n", dwStatusCode);
          bDone = TRUE;
      }
    }

    // Keep track of the last status code.
    dwLastStatus = dwStatusCode;

    // If there are any errors, break out of the loop.
    if( !bResults ) 
        bDone = TRUE;
  }

  // Report any errors.
  if( !bResults )
  {
    DWORD dwLastError = GetLastError( );
    printf( "Error %d has occurred.\n", dwLastError );
  }

  // Close any open handles.
  if( hRequest ) WinHttpCloseHandle( hRequest );
  if( hConnect ) WinHttpCloseHandle( hConnect );
  if( hSession ) WinHttpCloseHandle( hSession );
}

```



## <a name="automatic-logon-policy"></a>Richtlinie für automatische Anmeldung

Die Richtlinie für die automatische Anmeldung (automatische Anmeldung) bestimmt, wann WinHTTP die Standard Anmelde Informationen in eine Anforderung aufnehmen kann. Die Standard Anmelde Informationen sind entweder das aktuelle Thread Token oder das Sitzungs Token, abhängig davon, ob WinHTTP im synchronen oder asynchronen Modus verwendet wird. Das Thread Token wird im synchronen Modus verwendet, und das Sitzungs Token wird im asynchronen Modus verwendet. Diese Standard Anmelde Informationen sind häufig der Benutzername und das Kennwort, die für die Anmeldung bei Microsoft Windows verwendet werden.

Die Richtlinie für die automatische Anmeldung wurde implementiert, um zu verhindern, dass diese Anmelde Informationen für die Authentifizierung bei einem nicht vertrauenswürdigen Server verwendet werden. Standardmäßig ist die Sicherheitsstufe auf WinHTTP \_ Autologon \_ Security \_ Level Medium festgelegt, sodass \_ die Standard Anmelde Informationen nur für Intranetanforderungen verwendet werden können. Die Richtlinie für die automatische Anmeldung gilt nur für NTLM-und Aushandlungs Authentifizierungs Schemas. Anmelde Informationen werden nie automatisch mit anderen Schemas übertragen.

Die Richtlinie für die automatische Anmeldung kann mithilfe der [**WinHttpSetOption**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpsetoption) -Funktion mit der [**WinHTTP- \_ Option \_ Autologon \_**](option-flags.md) -Richtlinienflag festgelegt werden. Dieses Flag gilt nur für das Anforderungs handle. Wenn die Richtlinie auf WinHTTP \_ Autologon \_ Security Level Low festgelegt ist \_ \_ , können Standard Anmelde Informationen an alle Server gesendet werden. Wenn die Richtlinie auf WinHTTP \_ Autologon \_ Security Level High festgelegt ist \_ \_ , können keine Standard Anmelde Informationen für die Authentifizierung verwendet werden. Es wird dringend empfohlen, die automatische Anmeldung auf mittlerer Ebene zu verwenden.

## <a name="stored-user-names-and-passwords"></a>Gespeicherte Benutzernamen und Kennwörter

In Windows XP wurde das Konzept von gespeicherten Benutzernamen und Kenn Wörtern eingeführt. Wenn die Passport-Anmelde Informationen eines Benutzers über den **Passport-Registrierungs-Assistenten** oder das Standard **Dialogfeld** Anmelde Informationen gespeichert werden, werden diese in den gespeicherten Benutzernamen und Kenn Wörtern gespeichert. Bei Verwendung von WinHTTP unter Windows XP oder höher verwendet WinHTTP automatisch die Anmelde Informationen in den gespeicherten Benutzernamen und Kenn Wörtern, wenn die Anmelde Informationen nicht explizit festgelegt sind. Dies ähnelt der Unterstützung von Standard Anmelde Informationen für NTLM/Kerberos. Die Verwendung von standardmäßigen Passport-Anmelde Informationen unterliegt jedoch nicht den Einstellungen für die automatische Anmelde Richtlinie.

 

 



