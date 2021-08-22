---
description: Microsoft Windows HTTP Services (WinHTTP) ist auf Anwendungen der mittleren Ebene und Back-End-Server ausgerichtet, die Zugriff auf einen HTTP-Clientstapel benötigen.
ms.assetid: 5b0cf321-8f69-4526-a628-e6ca0f9d4a58
title: Portieren von WinINet-Anwendungen zu WinHTTP
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b111cd79e7ce7edfb09d43993ee2735ce09275f51c58bcfad319fb073dccc5b7
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119052008"
---
# <a name="porting-wininet-applications-to-winhttp"></a>Portieren von WinINet-Anwendungen zu WinHTTP

Microsoft Windows HTTP Services (WinHTTP) ist auf Anwendungen der mittleren Ebene und Back-End-Server ausgerichtet, die Zugriff auf einen HTTP-Clientstapel benötigen. [Microsoft Windows Internet (WinINet)](winhttp-start-page.md) bietet einen HTTP-Clientstapel für Clientanwendungen sowie Zugriff auf die Protokolle File Transfer Protocol (FTP), SOCKSv4 und Gopher. Anhand dieser Übersicht können Sie ermitteln, ob das Portieren Ihrer WinINet-Anwendungen zu WinHTTP von Vorteil wäre. Außerdem werden spezifische Konvertierungsanforderungen beschrieben.

-   [Überlegungen vor dem Portieren Ihrer WinINet-Anwendung](#things-to-consider-before-porting-your-wininet-application)
-   [WinHTTP-Entsprechungen zu WinINet-Funktionen](#winhttp-equivalents-to-wininet-functions)
-   [Unterschiedliche Verarbeitung asynchroner Anforderungen](#different-handling-of-asynchronous-requests)
-   [Unterschiede bei WinHTTP-Rückrufbenachrichtigungen](#differences-in-winhttp-callback-notifications)
-   [Unterschiede bei der Authentifizierung](#authentication-differences)
-   [Unterschiede bei sicheren HTTP-Transaktionen](#differences-in-secure-http-transactions)

## <a name="things-to-consider-before-porting-your-wininet-application"></a>Überlegungen vor dem Portieren Ihrer WinINet-Anwendung

Erwägen Sie, Ihre WinINet-Anwendung zu WinHTTP zu portieren, wenn Ihre Anwendung von den vorteilen:

-   Ein serversicherer HTTP-Clientstapel.
-   Minimierte Stapelauslastung.
-   Die Skalierbarkeit einer Serveranwendung.
-   Weniger Abhängigkeiten von plattformbezogenen APIs.
-   Unterstützung für Threadidentitätswechsel.
-   Ein dienstfreundlicher HTTP-Stapel.
-   Zugriff auf das [**skriptfähige WinHttpRequest-Objekt.**](winhttprequest.md)

Erwägen Sie nicht, Ihre WinINet-Anwendung zu WinHTTP zu portieren, wenn sie mindestens eine der folgenden Möglichkeiten unterstützen muss:

-   Das FTP- oder Gopher-Protokoll aus dem HTTP-Stapel.
-   Unterstützung für das SOCKSv4-Protokoll für die Kommunikation mit SOCKS-Proxys.
-   Automatische DFÜ-Dienste.

Wenn Sie Ihre Anwendung zu WinHTTP portieren möchten, werden Sie in den folgenden Abschnitten durch den Konvertierungsprozess geleitet.

Für eine Beispielanwendung für WinINet und WinHTTP vergleichen Sie das AsyncDemo-Beispiel für WinINet mit dem AsyncDemo-Beispiel für WinHTTP.

## <a name="winhttp-equivalents-to-wininet-functions"></a>WinHTTP-Entsprechungen zu WinINet-Funktionen

In der folgenden Tabelle sind WinINet-Funktionen im Zusammenhang mit dem HTTP-Clientstapel zusammen mit den WinHTTP-Entsprechungen aufgeführt.

Wenn Ihre Anwendung WinINet-Funktionen erfordert, die nicht aufgeführt sind, portieren Sie Ihre Anwendung nicht zu WinHTTP.



| WinINet-Funktion                                                       | WinHTTP-Entsprechung                                                                                                                                                                                     | Wichtige Änderungen                                                                                                                                                                                                                                                                                                                      |
|------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**HttpAddRequestHeaders**](/windows/desktop/api/wininet/nf-wininet-httpaddrequestheadersa)             | [**WinHttpAddRequestHeaders**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpaddrequestheaders)                                                                                                                                           | Keine.                                                                                                                                                                                                                                                                                                                                |
| [**HttpEndRequest**](/windows/desktop/api/wininet/nf-wininet-httpendrequesta)                           | [**WinHttpReceiveResponse**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpreceiveresponse)                                                                                                                                               | Der Kontextwert wird mit [**WinHttpSendRequest**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpsendrequest) oder [**WinHttpSetOption**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpsetoption)festgelegt. Anforderungsoptionen werden mit [**WinHttpOpenRequest**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpopenrequest)festgelegt. [**WinHttpReceiveResponse**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpreceiveresponse) muss nach dem Senden einer Anforderung aufgerufen werden.                      |
| [**HttpOpenRequest**](/windows/desktop/api/wininet/nf-wininet-httpopenrequesta)                         | [**WinHttpOpenRequest**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpopenrequest)                                                                                                                                                       | Der Kontextwert wird mit [**WinHttpSendRequest**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpsendrequest) oder [**WinHttpSetOption**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpsetoption)festgelegt.                                                                                                                                                                                                      |
| [**HttpQueryInfo**](/windows/desktop/api/wininet/nf-wininet-httpqueryinfoa)                             | [**WinHttpQueryHeaders**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpqueryheaders)                                                                                                                                                     | Keine.                                                                                                                                                                                                                                                                                                                                |
| [**HttpSendRequest**](/windows/desktop/api/wininet/nf-wininet-httpsendrequesta)                         | [**WinHttpSendRequest**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpsendrequest)                                                                                                                                                       | Der Kontextwert kann mit [**WinHttpSendRequest**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpsendrequest)festgelegt werden.                                                                                                                                                                                                                                                  |
| [**HttpSendRequestEx**](/windows/desktop/api/wininet/nf-wininet-httpsendrequestexa)                     | [**WinHttpSendRequest**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpsendrequest)                                                                                                                                                       | Puffer können nicht bereitgestellt werden.                                                                                                                                                                                                                                                                                                          |
| [**InternetCanonicalizeUrl**](/windows/desktop/api/wininet/nf-wininet-internetcanonicalizeurla)         | Keine Entsprechung                                                                                                                                                                                          | URLs werden jetzt in kanonischer Form in [**WinHttpOpenRequest**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpopenrequest)gesetzt.                                                                                                                                                                                                                                              |
| [**InternetCheckConnection**](/windows/desktop/api/wininet/nf-wininet-internetcheckconnectiona)         | Keine Entsprechung                                                                                                                                                                                          | Nicht in WinHTTP implementiert.                                                                                                                                                                                                                                                                                                          |
| [**InternetCloseHandle**](/windows/desktop/api/wininet/nf-wininet-internetclosehandle)                 | [**WinHttpCloseHandle**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpclosehandle)                                                                                                                                                       | Beim Schließen eines übergeordneten Handles in WinHTTP werden untergeordnete Handles nicht rekursiv geschlossen.                                                                                                                                                                                                                                                         |
| [**InternetCombineUrl**](/windows/desktop/api/wininet/nf-wininet-internetcombineurla)                   | Keine Entsprechung                                                                                                                                                                                          | URLs können mit der [**WinHttpCreateUrl-Funktion**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpcreateurl) zusammengestellt werden.                                                                                                                                                                                                                                                |
| [**InternetConfirmZoneCrossing**](/windows/desktop/api/wininet/nf-wininet-internetconfirmzonecrossing) | Keine Entsprechung                                                                                                                                                                                          | Nicht in WinHTTP implementiert.                                                                                                                                                                                                                                                                                                          |
| [**InternetConnect**](/windows/desktop/api/wininet/nf-wininet-internetconnecta)                         | [**WinHttpConnect**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpconnect)                                                                                                                                                               | Der Kontextwert wird mit [**WinHttpSendRequest**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpsendrequest) oder [**WinHttpSetOption**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpsetoption)festgelegt. Anforderungsoptionen werden mit [**WinHttpOpenRequest**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpopenrequest)festgelegt. Benutzeranmeldeinformationen werden mit [**WinHttpSetCredentials**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpsetcredentials)festgelegt.                                 |
| [**InternetCrackUrl**](/windows/desktop/api/wininet/nf-wininet-internetcrackurla)                       | [**WinHttpCrackUrl**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpcrackurl)                                                                                                                                                             | Entgegengesetztes Verhalten des ICU \_ ESCAPE-Flags: Mit [**InternetCrackUrl**](/windows/desktop/api/wininet/nf-wininet-internetcrackurla)bewirkt dieses Flag, dass Escapesequenzen (%xx) in Zeichen konvertiert werden, aber mit [**WinHttpCrackUrl**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpcrackurl)bewirkt es, dass Zeichen, die aus in einer HTTP-Anforderung mit Escapezeichen gekennzeichnet werden müssen, in Escapesequenzen konvertiert werden. |
| [**InternetCreateUrl**](/windows/desktop/api/wininet/nf-wininet-internetcreateurla)                     | [**WinHttpCreateUrl**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpcreateurl)                                                                                                                                                           | Keine.                                                                                                                                                                                                                                                                                                                                |
| [**InternetErrorDlg**](/windows/desktop/api/wininet/nf-wininet-interneterrordlg)                       | Keine Entsprechung                                                                                                                                                                                          | Da WinHTTP auf serverseitige Anwendungen ausgerichtet ist, wird keine Benutzeroberfläche implementiert.                                                                                                                                                                                                                                   |
| [**InternetGetCookie**](/windows/desktop/api/wininet/nf-wininet-internetgetcookiea)                     | Keine Entsprechung                                                                                                                                                                                          | WinHTTP hält keine Daten zwischen Sitzungen bei und kann nicht auf WinINet-Cookies zugreifen.                                                                                                                                                                                                                                                    |
| [**InternetÖffnen**](/windows/desktop/api/wininet/nf-wininet-internetopena)                               | [**WinHttpOpen**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpopen)                                                                                                                                                                     | Keine.                                                                                                                                                                                                                                                                                                                                |
| [**InternetOpenUrl**](/windows/desktop/api/wininet/nf-wininet-internetopenurla)                         | [**WinHttpConnect,**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpconnect) [**WinHttpOpenRequest,**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpopenrequest) [**WinHttpSendRequest,**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpsendrequest) [**WinHttpReceiveResponse**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpreceiveresponse) | Diese Funktion ist in den aufgeführten WinHTTP-Funktionen verfügbar.                                                                                                                                                                                                                                                                     |
| [**InternetQueryDataAvailable**](/windows/desktop/api/wininet/nf-wininet-internetquerydataavailable)   | [**WinHttpQueryDataAvailable**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpquerydataavailable)                                                                                                                                         | Keine reservierten Parameter.                                                                                                                                                                                                                                                                                                              |
| [**InternetQueryOption**](/windows/desktop/api/wininet/nf-wininet-internetqueryoptiona)                 | [**WinHttpQueryOption**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpqueryoption)                                                                                                                                                       | WinHTTP bietet einen anderen Satz von Optionen als WinINet. Weitere Informationen und Optionen, die von WinHTTP angeboten werden, finden Sie unter [**Optionsflags.**](option-flags.md)                                                                                                                                                                               |
| [**InternetReadFile**](/windows/desktop/api/wininet/nf-wininet-internetreadfile)                       | [**WinHttpReadData**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpreaddata)                                                                                                                                                             | Keine.                                                                                                                                                                                                                                                                                                                                |
| [**InternetReadFileEx**](/windows/desktop/api/wininet/nf-wininet-internetreadfileexa)                   | [**WinHttpReadData**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpreaddata)                                                                                                                                                             | Anstelle einer -Struktur ist der Puffer ein Bereich des Arbeitsspeichers, der mit einem Zeiger adressiert wird.                                                                                                                                                                                                                                                  |
| [**InternetSetOption**](/windows/desktop/api/wininet/nf-wininet-internetsetoptiona)                     | [**WinHttpSetOption**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpsetoption)                                                                                                                                                           | Keine.                                                                                                                                                                                                                                                                                                                                |
| [**InternetSetStatusCallback**](/windows/desktop/api/wininet/nf-wininet-internetsetstatuscallback)     | [**WinHttpSetStatusCallback**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpsetstatuscallback)                                                                                                                                           | Weitere Informationen finden Sie unter "Unterschiedliche Verarbeitung asynchroner Anforderungen" in diesem Thema.                                                                                                                                                                                                                                               |
| [**InternetTimeFromSystemTime**](/windows/desktop/api/wininet/nf-wininet-internettimefromsystemtime)   | [**WinHttpTimeFromSystemTime**](/windows/desktop/api/Winhttp/nf-winhttp-winhttptimefromsystemtime)                                                                                                                                         | Keine.                                                                                                                                                                                                                                                                                                                                |
| [**InternetTimeToSystemTime**](/windows/desktop/api/wininet/nf-wininet-internettimetosystemtime)       | [**WinHttpTimeToSystemTime**](/windows/desktop/api/Winhttp/nf-winhttp-winhttptimetosystemtime)                                                                                                                                             | Keine.                                                                                                                                                                                                                                                                                                                                |
| [**InternetWriteFile**](/windows/desktop/api/wininet/nf-wininet-internetwritefile)                     | [**WinHttpWriteData**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpwritedata)                                                                                                                                                           | Keine.                                                                                                                                                                                                                                                                                                                                |



 

## <a name="different-handling-of-asynchronous-requests"></a>Unterschiedliche Verarbeitung asynchroner Anforderungen

Beachten Sie, dass in WinINet und WinHTTP einige Funktionen asynchrone Anforderungen entweder synchron oder asynchron abschließen können. Ihre Anwendung muss beide Situationen behandeln. Es gibt erhebliche Unterschiede in bezug darauf, wie WinINet und WinHTTP diese potenziell asynchronen Funktionen behandeln.

Wininet

-   Synchrone Vervollständigung: Wenn ein potenziell asynchroner WinINet-Funktionsaufruf synchron abgeschlossen wird, geben die OUT-Parameter der Funktion die Ergebnisse des Vorgangs zurück. Wenn ein Fehler auftritt, rufen Sie den Fehlercode ab, indem [**Sie GetLastError**](/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror) nach dem WinINet-Funktionsaufruf aufrufen.

-   Asynchrone Vervollständigung: Wenn ein potenziell asynchroner Funktionsaufruf asynchron abgeschlossen wird, sind die Ergebnisse des Vorgangs und alle Fehler in der Rückruffunktion zugänglich. Die Rückruffunktion wird für einen Arbeitsthread ausgeführt, nicht für den Thread, der den ersten Funktionsaufruf ausgeführt hat.

Anders ausgedrückt: Ihre Anwendung muss die Logik duplizieren, um die Ergebnisse solcher Vorgänge an zwei Stellen zu verarbeiten: sowohl unmittelbar nach dem Funktionsaufruf als auch in der Rückruffunktion.

WinHTTP vereinfacht dieses Modell, da Sie die Betriebslogik nur in der Rückruffunktion implementieren können, die eine Abschlussbenachrichtigung empfängt, unabhängig davon, ob der Vorgang synchron oder asynchron abgeschlossen wurde. Wenn der asynchrone Vorgang aktiviert ist, geben die OUT-Parameter von WinHTTP-Funktionen keine aussagekräftigen Daten zurück und müssen auf **NULL** festgelegt werden.

Der einzige signifikante Unterschied zwischen asynchroner und synchroner Vervollständigung in WinHTTP besteht aus Anwendungssicht darin, wo die Rückruffunktion ausgeführt wird.

WinHTTP

-   Synchrone Vervollständigung: Wenn ein Vorgang synchron abgeschlossen wird, werden die Ergebnisse in einer Rückruffunktion zurückgegeben, die im gleichen Thread wie der ursprüngliche Funktionsaufruf ausgeführt wird.

-   Asynchroner Abschluss: Wenn ein Vorgang asynchron abgeschlossen wird, werden die Ergebnisse in einer Rückruffunktion zurückgegeben, die in einem Arbeitsthread ausgeführt wird.

Obwohl die meisten Fehler auch vollständig innerhalb der Rückruffunktion behandelt werden können, müssen WinHTTP-Anwendungen dennoch darauf vorbereitet sein, dass eine Funktion **FALSE** aufgrund eines FEHLERS INVALID PARAMETER oder eines ähnlichen Fehlers zurückgibt, \_ der durch Aufrufen von \_ [**GetLastError**](/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror)abgerufen wird.

Im Gegensatz zu WinINet, das mehrere asynchrone Vorgänge gleichzeitig ausführen kann, erzwingt WinHTTP eine Richtlinie mit einem ausstehenden asynchronen Vorgang pro Anforderungshandle. Wenn ein Vorgang aussteht und eine andere WinHTTP-Funktion aufgerufen wird, schlägt die zweite Funktion fehl, und [**GetLastError**](/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror) gibt ERROR \_ INVALID OPERATION \_ zurück.

WinHTTP vereinfacht dieses Modell, da Sie die Betriebslogik nur in der Rückruffunktion implementieren können, die eine Abschlussbenachrichtigung empfängt, unabhängig davon, ob der Vorgang synchron oder asynchron abgeschlossen wurde. Wenn der asynchrone Vorgang aktiviert ist, geben die OUT-Parameter von WinHTTP-Funktionen keine aussagekräftigen Daten zurück und müssen auf **NULL** festgelegt werden.

## <a name="differences-in-winhttp-callback-notifications"></a>Unterschiede bei WinHTTP-Rückrufbenachrichtigungen

Die Statusrückruffunktion empfängt Aktualisierungen des Status von Vorgängen über Benachrichtigungsflags. In WinHTTP werden Benachrichtigungen mithilfe des *dwNotificationFlags-Parameters* der [**WinHttpSetStatusCallback-Funktion**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpsetstatuscallback) ausgewählt. Verwenden Sie das **WINHTTP \_ CALLBACK \_ FLAG ALL \_ \_ NOTIFICATIONS-Flag,** um über alle Statusupdates benachrichtigt zu werden.

Benachrichtigungen, die angeben, dass ein bestimmter Vorgang abgeschlossen ist, werden als Abschlussbenachrichtigungen oder nur als Vervollständigungen bezeichnet. In WinINet enthält der *lpvStatusInformation-Parameter* jedes Mal, wenn die Rückruffunktion eine Vervollständigung empfängt, eine [**INTERNET \_ ASYNC \_ RESULT-Struktur.**](/windows/desktop/api/wininet/ns-wininet-internet_async_result) In WinHTTP ist diese Struktur nicht für alle Vervollständigungen verfügbar. Es ist wichtig, die Referenzseite für [**WINHTTP \_ STATUS \_ CALLBACK**](/windows/win32/api/winhttp/nc-winhttp-winhttp_status_callback)zu überprüfen, die Informationen zu Benachrichtigungen enthält und welche Art von Daten für jeden erwartet werden kann.

In WinHTTP gibt ein einzelner Abschluss ( **WINHTTP \_ CALLBACK \_ STATUS REQUEST \_ \_ ERROR**) an, dass ein Vorgang fehlgeschlagen ist. Alle anderen Vervollständigungen weisen auf einen erfolgreichen Vorgang hin.

Sowohl WinINet als auch WinHTTP verwenden einen benutzerdefinierten Kontextwert, um Informationen vom Hauptthread an die Statusrückruffunktion zu übergeben, die in einem Arbeitsthread ausgeführt werden kann. In WinINet wird der von der Statusrückruffunktion verwendete Kontextwert durch Aufrufen einer von mehreren Funktionen festgelegt. In WinHTTP wird der Kontextwert nur mit [**WinHttpSendRequest**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpsendrequest) oder [**WinHttpSetOption**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpsetoption)festgelegt. Aus diesem Grund ist es in WinHTTP möglich, eine Benachrichtigung zu erhalten, bevor ein Kontextwert festgelegt wird. Wenn die Rückruffunktion eine Benachrichtigung empfängt, bevor der Kontextwert festgelegt wird, muss die Anwendung darauf vorbereitet sein, **NULL** im *dwContext-Parameter* der Rückruffunktion zu empfangen.

## <a name="authentication-differences"></a>Unterschiede bei der Authentifizierung

In WinINet werden Benutzeranmeldeinformationen durch Aufrufen der [**InternetSetOption-Funktion**](/windows/desktop/api/wininet/nf-wininet-internetsetoptiona) festgelegt. Dabei wird Code verwendet, der dem im folgenden Codebeispiel ähnelt.

``` syntax
// Use the WinINet InternetSetOption function to set the 
// user credentials to the user name contained in strUsername 
// and the password to the contents of strPassword.
       
InternetSetOption( hRequest, INTERNET_OPTION_PROXY_USERNAME, 
                   strUsername, strlen(strUsername) + 1 );

InternetSetOption( hRequest, INTERNET_OPTION_PROXY_PASSWORD, 
                   strPassword, strlen(strPassword) + 1 );
```

Aus Kompatibilitätsgründen können Benutzeranmeldeinformationen in WinHTTP mithilfe der [**WinHttpSetOption-Funktion**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpsetoption) auf ähnliche Weise festgelegt werden. Dies wird jedoch nicht empfohlen, da dies ein Sicherheitsrisiko darstellen kann.

Wenn eine Anwendung stattdessen einen 401-Statuscode in WinHTTP empfängt, wird empfohlen, Anmeldeinformationen festzulegen, indem Sie zunächst ein Authentifizierungsschema mit [**WinHttpQueryAuthSchemes**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpqueryauthschemes) identifizieren und anschließend die Anmeldeinformationen mit [**WinHttpSetCredentials**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpsetcredentials)festlegen. Im folgenden Codebeispiel wird dies veranschaulicht.

``` syntax
DWORD dwSupportedSchemes;
DWORD dwPrefered;
DWORD dwTarget;

// Obtain the supported and first schemes.
WinHttpQueryAuthSchemes( hRequest, &dwSupportedSchemes, &dwPrefered, &dwTarget );

// Set the credentials before resending the request.
WinHttpSetCredentials( hRequest, dwTarget, dwPrefered, strUsername, strPassword, NULL );
```

Da es keine Entsprechung zu [**InternetErrorDlg**](/windows/desktop/api/wininet/nf-wininet-interneterrordlg) in WinHTTP gibt, müssen Anwendungen, die Anmeldeinformationen über eine Benutzeroberfläche abrufen, eine eigene Schnittstelle bereitstellen.

Im Gegensatz zu WinINet werden Kennwörter von WinHTTP nicht zwischengespeichert. Gültige Benutzeranmeldeinformationen müssen für jede Anforderung angegeben werden.

WinHTTP unterstützt nicht das von WinINet unterstützte DPA-Schema (Distributed Password Authentication). WinHTTP unterstützt jedoch Microsoft Passport 1.4. Weitere Informationen zur Verwendung der Passport-Authentifizierung in WinHTTP finden Sie unter [Passport-Authentifizierung in WinHTTP.](passport-authentication-in-winhttp.md)

WinHTTP verwendet nicht Internet Explorer Einstellungen, um die Richtlinie für die automatische Anmeldung zu bestimmen. Stattdessen wird die Richtlinie für die automatische Anmeldung mit [**WinHttpSetOption**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpsetoption)festgelegt. Weitere Informationen zur Authentifizierung in WinHTTP, einschließlich der Richtlinie für die automatische Anmeldung, finden Sie unter [Authentifizierung in WinHTTP.](authentication-in-winhttp.md)

## <a name="differences-in-secure-http-transactions"></a>Unterschiede bei sicheren HTTP-Transaktionen

Initiieren Sie in WinINet eine sichere Sitzung entweder mit [**httpOpenRequest**](/windows/desktop/api/wininet/nf-wininet-httpopenrequesta) oder [**InternetConnect,**](/windows/desktop/api/wininet/nf-wininet-internetconnecta)aber in WinHTTP müssen Sie [**WinHttpOpenRequest**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpopenrequest) mithilfe des **WINHTTP \_ FLAG \_ SECURE-Flags** aufrufen.

In einer sicheren HTTP-Transaktion können Serverzertifikate verwendet werden, um einen Server beim Client zu authentifizieren. Wenn ein Serverzertifikat in WinINet Fehler enthält, schlägt [**HttpSendRequest**](/windows/desktop/api/wininet/nf-wininet-httpsendrequesta) fehl und stellt Details zu den Zertifikatfehlern bereit.

In WinHttp werden Serverzertifikatfehler gemäß der Version wie folgt behandelt:

-   Ab WinHttp 5.1 meldet der Aufruf von [**WinHttpSendRequest**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpsendrequest) einen **WINHTTP \_ CALLBACK \_ STATUS \_ SECURE \_ FAILURE** in der Rückruffunktion, wenn ein Serverzertifikat fehlschlägt oder Fehler enthält. Wenn der von **WinHttpSendRequest** generierte Fehler ignoriert wird, schlagen nachfolgende Aufrufe von [**WinHttpReceiveResponse**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpreceiveresponse) mit einem \_ FEHLER WINHTTP \_ OPERATION \_ CANCELLED-Fehler fehl.
-   In WinHTTP 5.0 führen Fehler in Serverzertifikaten standardmäßig nicht dazu, dass eine Anforderung fehlschlägt. Stattdessen werden die Fehler in der Rückruffunktion mit der **WINHTTP \_ CALLBACK \_ STATUS SECURE \_ \_ FAILURE-Benachrichtigung** gemeldet.

Auf einigen früheren Plattformen unterstützte WinINet die Protokolle PCT (Private Communication Technology) und/oder Fortezza, jedoch nicht auf Windows XP.

WinHTTP unterstützt die PROTOKOLLE PCT und Fortezza auf keiner Plattform und basiert stattdessen auf Secure Sockets Layer (SSL) 2.0, SSL 3.0 oder Transport Layer Security (TLS) 1.0.

 

 
