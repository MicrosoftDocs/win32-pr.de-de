---
description: Einige HTTP-Server und Proxys erfordern eine Authentifizierung, bevor der Zugriff auf Ressourcen im Internet erlaubt wird. Die Microsoft Windows HTTP Services-Funktionen (WinHTTP) unterstützen die Server- und Proxyauthentifizierung für HTTP-Sitzungen.
ms.assetid: 077d6275-8600-4091-b78e-419a41a2101a
title: Authentifizierung in WinHTTP
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 810fadf470861b23ed2291bfa5665e1e429e86b7be77675f332267ee1d1c4de4
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119052118"
---
# <a name="authentication-in-winhttp"></a>Authentifizierung in WinHTTP

Einige HTTP-Server und Proxys erfordern eine Authentifizierung, bevor der Zugriff auf Ressourcen im Internet erlaubt wird. Die Microsoft Windows HTTP Services-Funktionen (WinHTTP) unterstützen die Server- und Proxyauthentifizierung für HTTP-Sitzungen.

## <a name="about-http-authentication"></a>Informationen zur HTTP-Authentifizierung

Wenn eine Authentifizierung erforderlich ist, erhält die HTTP-Anwendung den Statuscode 401 (Server erfordert Authentifizierung) oder 407 (Proxy erfordert Authentifizierung). Zusammen mit dem Statuscode sendet der Proxy oder Server mindestens einen Authentifizierungsheader: WWW-Authenticate (für Serverauthentifizierung) oder Proxy-Authenticate (für Proxyauthentifizierung).

Jeder Authentifizierungsheader enthält ein unterstütztes Authentifizierungsschema und für die Schemas Basic und Digest einen Bereich. Wenn mehrere Authentifizierungsschemas unterstützt werden, gibt der Server mehrere Authentifizierungsheader zurück. Beim Bereichswert wird die Kleinschreibung beachtet, und es wird eine Gruppe von Servern oder Proxys definiert, für die die gleichen Anmeldeinformationen akzeptiert werden. Beispielsweise kann der Header "WWW-Authenticate: Basic Realm="example"" zurückgegeben werden, wenn eine Serverauthentifizierung erforderlich ist. Dieser Header gibt an, dass Benutzeranmeldeinformationen für die "Beispieldomäne" angegeben werden müssen.

Eine HTTP-Anwendung kann ein Autorisierungsheaderfeld mit einer Anforderung enthalten, die sie an den Server sendet. Der Autorisierungsheader enthält das Authentifizierungsschema und die entsprechende Antwort, die für dieses Schema erforderlich ist. Beispielsweise würde der Header "Authorization: Basic" der Anforderung hinzugefügt und an den Server gesendet, wenn der Client den Antwortheader \<username:password> "WWW-Authenticate: Basic Realm="example" empfangen hat.

> [!Note]  
> Obwohl sie hier als Nur-Text angezeigt werden, sind Benutzername und Kennwort tatsächlich [*Base64-codiert.*](glossary.md)

 

Es gibt zwei allgemeine Arten von Authentifizierungsschemas:

-   Standardauthentifizierungsschema, bei dem Benutzername und Kennwort in Klartext an den Server gesendet werden.

    Das Standardauthentifizierungsschema basiert auf dem Modell, das sich ein Client mit einem Benutzernamen und Kennwort für jeden Bereich identifizieren muss. Der Server unterstützt die Anforderung nur, wenn die Anforderung mit einem Autorisierungsheader gesendet wird, der einen gültigen Benutzernamen und ein gültiges Kennwort enthält.

-   Challenge-Response-Schemas, z. B. Kerberos, bei denen der Server den Client mit [*Authentifizierungsdaten herausfordert.*](glossary.md) Der Client transformiert die Daten mit den Benutzeranmeldeinformationen und sendet die transformierten Daten zur Authentifizierung zurück an den Server.

    Challenge-Response-Schemas ermöglichen eine sicherere Authentifizierung. In einem Challenge-Response-Schema werden Benutzername und Kennwort nie über das Netzwerk übertragen. Nachdem der Client ein Challenge-Response-Schema ausgewählt hat, gibt der Server einen entsprechenden Statuscode mit einer Herausforderung zurück, die die Authentifizierungsdaten [*für*](glossary.md) dieses Schema enthält. Der Client gibt dann die Anforderung erneut mit der richtigen Antwort zurück, um den angeforderten Dienst zu erhalten. Für Challenge-Response-Schemas kann es mehrere Austauschzeiten geben.

Die folgende Tabelle enthält die von WinHTTP unterstützten Authentifizierungsschemas, den Authentifizierungstyp und eine Beschreibung des Schemas.



| Schema            | Typ               | Beschreibung                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                        |
|-------------------|--------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Basic (Klartext) | Basic              | Verwendet eine [*Base64-codierte Zeichenfolge,*](glossary.md) die den Benutzernamen und das Kennwort enthält.                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                      |
| Digest            | Challenge-Response | Herausforderungen bei der Verwendung eines Nonce-Werts (einer vom Server angegebenen Datenzeichenfolge). Eine gültige Antwort enthält eine Prüfsumme des Benutzernamens, des Kennworts, des angegebenen Nonce-Werts, des [*HTTP-Verbs*](glossary.md)und des angeforderten Uniform Resource Identifier (URI).                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                  |
| NTLM              | Challenge-Response | Erfordert, [*dass die Authentifizierungsdaten*](glossary.md) mit den Benutzeranmeldeinformationen transformiert werden, um die Identität nachzuweisen. Damit die NTLM-Authentifizierung ordnungsgemäß funktioniert, müssen mehrere Austausche für dieselbe Verbindung stattfinden. Daher kann die NTLM-Authentifizierung nicht verwendet werden, wenn ein intervening-Proxy keep-alive-Verbindungen nicht unterstützt. Die NTLM-Authentifizierung schlägt auch fehl, wenn [**WinHttpSetOption**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpsetoption) mit dem [**WINHTTP \_ DISABLE KEEP \_ \_ ALIVE-Flag**](option-flags.md) verwendet wird, das die Keep-Alive-Semantik deaktiviert.                                                                                                                                                                                                                                       |
| Passport          | Challenge-Response | Verwendet [Microsoft Passport 1.4](passport-authentication-in-winhttp.md).                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                             |
| Aushandeln         | Challenge-Response | Wenn sowohl der Server als auch der Client Windows 2000 oder höher verwenden, wird die Kerberos-Authentifizierung verwendet. Andernfalls wird die NTLM-Authentifizierung verwendet. Kerberos ist ab Windows 2000 verfügbar und gilt als sicherer als die NTLM-Authentifizierung. Damit die Negotiate-Authentifizierung ordnungsgemäß funktioniert, müssen mehrere Austausche für dieselbe Verbindung stattfinden. Daher kann die Negotiate-Authentifizierung nicht verwendet werden, wenn ein intervening-Proxy keep-alive-Verbindungen nicht unterstützt. Die Aushandlungsauthentifizierung schlägt auch fehl, wenn [**WinHttpSetOption**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpsetoption) mit dem [**WINHTTP \_ DISABLE KEEP \_ \_ ALIVE-Flag**](option-flags.md) verwendet wird, das die Keep-Alive-Semantik deaktiviert. Das Negotiate-Authentifizierungsschema wird manchmal als integrierte Windows bezeichnet. |



 

## <a name="authentication-in-winhttp-applications"></a>Authentifizierung in WinHTTP-Anwendungen

Die WinHTTP-API (Application Programming Interface) stellt zwei Funktionen für den Zugriff auf Internetressourcen in Situationen bereit, in denen eine Authentifizierung erforderlich ist: [**WinHttpSetCredentials**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpsetcredentials) und [**WinHttpQueryAuthSchemes**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpqueryauthschemes).

Wenn eine Antwort mit dem Statuscode 401 oder 407 empfangen wird, kann [**WinHttpQueryAuthSchemes**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpqueryauthschemes) verwendet werden, um die Authentifizierungsheader zu analysieren und die unterstützten Authentifizierungsschemas und das Authentifizierungsziel zu bestimmen. Das Authentifizierungsziel ist der Server oder Proxy, der die Authentifizierung an fordert. **WinHttpQueryAuthSchemes** bestimmt auch das erste Authentifizierungsschema anhand der verfügbaren Schemas basierend auf den vom Server vorgeschlagenen Authentifizierungsschemaeinstellungen. Diese Methode zum Auswählen eines Authentifizierungsschemas ist das verhalten, das von [RFC 2616 vorgeschlagen wird.](https://www.ietf.org/rfc/rfc2616.txt)

[**Mit WinHttpSetCredentials**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpsetcredentials) kann eine Anwendung das Authentifizierungsschema angeben, das zusammen mit einem gültigen Benutzernamen und Kennwort für die Verwendung auf dem Zielserver oder Proxy verwendet wird. Nach dem Festlegen der Anmeldeinformationen und dem erneuten Senden der Anforderung werden die erforderlichen Header generiert und der Anforderung automatisch hinzugefügt. Da einige Authentifizierungsschemas mehrere Transaktionen [**erfordern, könnte WinHttpSendRequest**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpsendrequest) den Fehler \_ "ERROR WINHTTP \_ RESEND \_ REQUEST" zurückgeben. Wenn dieser Fehler auftritt, sollte die Anwendung die Anforderung so lange erneut senden, bis eine Antwort empfangen wird, die keinen Statuscode 401 oder 407 enthält. Der Statuscode 200 gibt an, dass die Ressource verfügbar ist und die Anforderung erfolgreich war. Weitere [**Statuscodes, die**](http-status-codes.md) zurückgegeben werden können, finden Sie unter HTTP-Statuscodes.

Wenn ein akzeptables Authentifizierungsschema und Anmeldeinformationen bekannt sind, bevor eine Anforderung an den Server gesendet wird, kann eine Anwendung [**WinHttpSetCredentials**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpsetcredentials) vor dem Aufruf von [**WinHttpSendRequest aufrufen.**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpsendrequest) In diesem Fall versucht WinHTTP die Vorauthentifizierung beim Server, indem Anmeldeinformationen oder Authentifizierungsdaten [*in*](glossary.md) der ersten Anforderung an den Server bereitgestellt werden. Die Vorauthentifizierung kann die Anzahl der Austausche im Authentifizierungsprozess verringern und somit die Anwendungsleistung verbessern.

Die Vorauthentifizierung kann mit den folgenden Authentifizierungsschemas verwendet werden:

-   Basic : immer möglich.
-   Aushandeln der Auflösung in Kerberos – sehr wahrscheinlich möglich; Die einzige Ausnahme ist, wenn die Zeitverschniffene zwischen dem Client und dem Domänencontroller deaktiviert sind.
-   (Aushandeln der Auflösung in NTLM) – nie möglich.
-   NTLM: nur in Windows Server 2008 R2 möglich.
-   Digest: Nie möglich.
-   Passport : nie möglich; Nach der ersten Antwort auf die Herausforderung verwendet WinHTTP Cookies, um sich vorab bei Passport zu authentifizieren.

Eine typische WinHTTP-Anwendung schließt die folgenden Schritte ab, um die Authentifizierung zu verarbeiten.

-   Fordern Sie eine Ressource mit [**WinHttpOpenRequest und**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpopenrequest) [**WinHttpSendRequest an.**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpsendrequest)
-   Überprüfen Sie die Antwortheader mit [**WinHttpQueryHeaders**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpqueryheaders).
-   Wenn ein Statuscode 401 oder 407 zurückgegeben wird, der angibt, dass eine Authentifizierung erforderlich ist, rufen Sie [**WinHttpQueryAuthSchemes**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpqueryauthschemes) auf, um ein akzeptables Schema zu finden.
-   Legen Sie das Authentifizierungsschema, den Benutzernamen und das Kennwort mit [**WinHttpSetCredentials fest.**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpsetcredentials)
-   Senden Sie die Anforderung erneut mit dem gleichen Anforderungshand handle, indem [**Sie WinHttpSendRequest aufrufen.**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpsendrequest)

Die von [**WinHttpSetCredentials festgelegten**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpsetcredentials) Anmeldeinformationen werden nur für eine Anforderung verwendet. WinHTTP speichert die Anmeldeinformationen nicht zwischen, die in anderen Anforderungen verwendet werden sollen. Das bedeutet, dass Anwendungen geschrieben werden müssen, die auf mehrere Anforderungen reagieren können. Wenn eine authentifizierte Verbindung erneut verwendet wird, werden andere Anforderungen möglicherweise nicht in Frage gestellt, aber Ihr Code sollte jederzeit auf eine Anforderung reagieren können.

### <a name="example-retrieving-a-document"></a>Beispiel: Abrufen eines Dokuments

Der folgende Beispielcode versucht, ein angegebenes Dokument von einem HTTP-Server abzurufen. Der Statuscode wird aus der Antwort abgerufen, um zu bestimmen, ob eine Authentifizierung erforderlich ist. Wenn der Statuscode 200 gefunden wird, ist das Dokument verfügbar. Wenn der Statuscode 401 oder 407 gefunden wird, ist eine Authentifizierung erforderlich, bevor das Dokument abgerufen werden kann. Für jeden anderen Statuscode wird eine Fehlermeldung angezeigt. Eine [**Liste der möglichen Statuscodes**](http-status-codes.md) finden Sie unter HTTP-Statuscodes.


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



## <a name="automatic-logon-policy"></a>Richtlinie für die automatische Anmeldung

Die Richtlinie für die automatische Anmeldung (automatische Anmeldung) bestimmt, wann winHTTP die Standardanmeldeinformationen in einer Anforderung enthalten kann. Die Standardanmeldeinformationen sind entweder das aktuelle Threadtoken oder das Sitzungstoken, je nachdem, ob WinHTTP im synchronen oder asynchronen Modus verwendet wird. Das Threadtoken wird im synchronen Modus und das Sitzungstoken im asynchronen Modus verwendet. Diese Standardanmeldeinformationen sind häufig der Benutzername und das Kennwort für die Anmeldung bei Microsoft Windows.

Die Richtlinie für die automatische Anmeldung wurde implementiert, um zu verhindern, dass diese Anmeldeinformationen gelegentlich für die Authentifizierung bei einem nicht vertrauenswürdigen Server verwendet werden. Standardmäßig ist die Sicherheitsstufe auf WINHTTP \_ AUTOLOGON \_ SECURITY LEVEL MEDIUM \_ \_ festgelegt, wodurch die Standardanmeldeinformationen nur für Intranetanforderungen verwendet werden können. Die Richtlinie für die automatische Anmeldung gilt nur für die Authentifizierungsschemas NTLM und Negotiate. Anmeldeinformationen werden nie automatisch mit anderen Schemas übertragen.

Die Richtlinie für die automatische Anmeldung kann mithilfe der [**WinHttpSetOption-Funktion**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpsetoption) mit dem [**WINHTTP \_ OPTION \_ AUTOLOGON \_ POLICY-Flag**](option-flags.md) festgelegt werden. Dieses Flag gilt nur für das Anforderungshandle. Wenn die Richtlinie auf WINHTTP \_ AUTOLOGON SECURITY LEVEL LOW festgelegt \_ \_ \_ ist, können Standardanmeldeinformationen an alle Server gesendet werden. Wenn die Richtlinie auf WINHTTP \_ AUTOLOGON SECURITY LEVEL HIGH festgelegt \_ \_ \_ ist, können keine Standardanmeldeinformationen für die Authentifizierung verwendet werden. Es wird dringend empfohlen, die automatische Anmeldung auf der Ebene MEDIUM zu verwenden.

## <a name="stored-user-names-and-passwords"></a>Gespeicherte Benutzernamen und Kennwörter

Windows XP hat das Konzept von gespeicherten Benutzernamen und Kennwörtern eingeführt. Wenn die Passport-Anmeldeinformationen eines Benutzers über den **Passport-Registrierungs-Assistenten** oder das **Standarddialogfeld für Anmeldeinformationen** gespeichert werden, werden sie in den gespeicherten Benutzernamen und Kennwörtern gespeichert. Wenn WinHTTP auf Windows XP oder höher verwendet wird, verwendet WinHTTP automatisch die Anmeldeinformationen in den gespeicherten Benutzernamen und Kennwörtern, wenn die Anmeldeinformationen nicht explizit festgelegt sind. Dies ähnelt der Unterstützung von Standardanmeldeinformationen für NTLM/Kerberos. Die Verwendung von Passport-Standardanmeldeinformationen unterliegt jedoch nicht den Einstellungen für die automatische Anmeldungsrichtlinie.

 

 



