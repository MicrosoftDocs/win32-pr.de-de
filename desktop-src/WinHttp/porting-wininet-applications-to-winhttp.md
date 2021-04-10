---
description: Die Microsoft Windows HTTP-Dienste (WinHTTP) sind auf Anwendungen der mittleren Ebene und Back-End-Server ausgerichtet, die Zugriff auf einen HTTP-Client Stapel benötigen.
ms.assetid: 5b0cf321-8f69-4526-a628-e6ca0f9d4a58
title: Portieren von WinINet-Anwendungen auf WinHTTP
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6f64c4ecc825934d32b1d363f010bd04e1484428
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "103960800"
---
# <a name="porting-wininet-applications-to-winhttp"></a>Portieren von WinINet-Anwendungen auf WinHTTP

Die Microsoft Windows HTTP-Dienste (WinHTTP) sind auf Anwendungen der mittleren Ebene und Back-End-Server ausgerichtet, die Zugriff auf einen HTTP-Client Stapel benötigen. [Microsoft Windows Internet (WinInet)](winhttp-start-page.md) stellt einen HTTP-Client Stapel für Client Anwendungen und Zugriff auf die Protokolle File Transfer Protocol (FTP), SOCKSv4 und Gopher bereit. Mithilfe dieser Übersicht können Sie feststellen, ob das Portieren ihrer WinINet-Anwendungen in WinHTTP von Vorteil ist. Außerdem werden bestimmte Konvertierungs Anforderungen beschrieben.

-   [Dinge, die vor dem Portieren ihrer WinInet-Anwendung zu berücksichtigen sind](#things-to-consider-before-porting-your-wininet-application)
-   [WinHTTP-Entsprechungen zu WinInet-Funktionen](#winhttp-equivalents-to-wininet-functions)
-   [Unterschiedliche Verarbeitung von asynchronen Anforderungen](#different-handling-of-asynchronous-requests)
-   [Unterschiede bei WinHTTP-Rückruf Benachrichtigungen](#differences-in-winhttp-callback-notifications)
-   [Authentifizierungs Unterschiede](#authentication-differences)
-   [Unterschiede bei sicheren HTTP-Transaktionen](#differences-in-secure-http-transactions)

## <a name="things-to-consider-before-porting-your-wininet-application"></a>Dinge, die vor dem Portieren ihrer WinInet-Anwendung zu berücksichtigen sind

Sie sollten ihre WinInet-Anwendung in WinHTTP portieren, wenn Ihre Anwendung von folgenden Vorteilen profitieren würde:

-   Ein Server sicherer http-Client Stapel.
-   Minimierte Stapel Verwendung.
-   Die Skalierbarkeit einer Serveranwendung.
-   Weniger Abhängigkeiten von Platt Form bezogenen APIs.
-   Unterstützung für Thread Identitätswechsel.
-   Ein Dienst freundlicher HTTP-Stapel.
-   Zugriff auf das Skript fähige- [**WinHttpRequest**](winhttprequest.md) -Objekt.

Sie sollten die WinInet-Anwendung nicht auf WinHTTP portieren, wenn eine oder mehrere der folgenden Aktionen unterstützt werden müssen:

-   Das FTP-oder Gopher-Protokoll aus dem HTTP-Stapel.
-   Unterstützung für SOCKSv4-Protokoll für die Kommunikation mit SOCKS-Proxys
-   Automatische Einwähldienste.

Wenn Sie Ihre Anwendung auf WinHTTP portieren möchten, werden Sie in den folgenden Abschnitten durch den Konvertierungs Vorgang geleitet.

Vergleichen Sie für eine Beispielanwendung für WinInet und WinHTTP das AsyncDemo-Beispiel für WinInet mit dem AsyncDemo-Beispiel für WinHTTP.

## <a name="winhttp-equivalents-to-wininet-functions"></a>WinHTTP-Entsprechungen zu WinInet-Funktionen

In der folgenden Tabelle werden die mit dem HTTP-Client Stapel verknüpften WinInet-Funktionen zusammen mit den WinHTTP-Entsprechungen aufgelistet.

Wenn Ihre Anwendung WinInet-Funktionen erfordert, die nicht aufgelistet sind, sollten Sie Ihre Anwendung nicht auf WinHTTP portieren.



| Wininet-Funktion                                                       | WinHTTP-Entsprechung                                                                                                                                                                                     | Wichtige Änderungen                                                                                                                                                                                                                                                                                                                      |
|------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**Httpadressquestheaders**](/windows/desktop/api/wininet/nf-wininet-httpaddrequestheadersa)             | [**Winhttpadressquestheaders**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpaddrequestheaders)                                                                                                                                           | Keine.                                                                                                                                                                                                                                                                                                                                |
| [**Httpdrequest**](/windows/desktop/api/wininet/nf-wininet-httpendrequesta)                           | [**WinHttpReceiveResponse**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpreceiveresponse)                                                                                                                                               | Der Kontextwert wird mit [**WinHttpSendRequest**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpsendrequest) oder [**WinHttpSetOption**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpsetoption)festgelegt. Anforderungs Optionen werden mit [**WinHttpOpenRequest**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpopenrequest)festgelegt. [**WinHttpReceiveResponse**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpreceiveresponse) muss nach dem Senden einer Anforderung aufgerufen werden.                      |
| [**Httpopanrequest**](/windows/desktop/api/wininet/nf-wininet-httpopenrequesta)                         | [**Winhttpopanrequest**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpopenrequest)                                                                                                                                                       | Der Kontextwert wird mit [**WinHttpSendRequest**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpsendrequest) oder [**WinHttpSetOption**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpsetoption)festgelegt.                                                                                                                                                                                                      |
| [**HttpQueryInfo**](/windows/desktop/api/wininet/nf-wininet-httpqueryinfoa)                             | [**WinHttpQueryHeaders**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpqueryheaders)                                                                                                                                                     | Keine.                                                                                                                                                                                                                                                                                                                                |
| [**HttpSendRequest**](/windows/desktop/api/wininet/nf-wininet-httpsendrequesta)                         | [**WinHttpSendRequest**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpsendrequest)                                                                                                                                                       | Der Kontextwert kann mit [**WinHttpSendRequest**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpsendrequest)festgelegt werden.                                                                                                                                                                                                                                                  |
| [**HttpSendRequestEx**](/windows/desktop/api/wininet/nf-wininet-httpsendrequestexa)                     | [**WinHttpSendRequest**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpsendrequest)                                                                                                                                                       | Puffer können nicht angegeben werden.                                                                                                                                                                                                                                                                                                          |
| [**Internetcanonicalizeurl**](/windows/desktop/api/wininet/nf-wininet-internetcanonicalizeurla)         | Keine Entsprechung                                                                                                                                                                                          | URLs werden nun in der kanonischen Form in [**winhttpopanrequest**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpopenrequest)abgelegt.                                                                                                                                                                                                                                              |
| [**Internetcheckconnection**](/windows/desktop/api/wininet/nf-wininet-internetcheckconnectiona)         | Keine Entsprechung                                                                                                                                                                                          | Nicht in WinHTTP implementiert.                                                                                                                                                                                                                                                                                                          |
| [**Internetclosehandle**](/windows/desktop/api/wininet/nf-wininet-internetclosehandle)                 | [**WinHttpCloseHandle**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpclosehandle)                                                                                                                                                       | Durch das Schließen eines übergeordneten Handles in WinHTTP werden die untergeordneten Handles nicht rekursiv geschlossen.                                                                                                                                                                                                                                                         |
| [**Internetcombineurl**](/windows/desktop/api/wininet/nf-wininet-internetcombineurla)                   | Keine Entsprechung                                                                                                                                                                                          | URLs können mit der [**winhttpkreateurl**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpcreateurl) -Funktion zusammengestellt werden.                                                                                                                                                                                                                                                |
| [**Internetconfirmzonecrossing**](/windows/desktop/api/wininet/nf-wininet-internetconfirmzonecrossing) | Keine Entsprechung                                                                                                                                                                                          | Nicht in WinHTTP implementiert.                                                                                                                                                                                                                                                                                                          |
| [**InternetConnect**](/windows/desktop/api/wininet/nf-wininet-internetconnecta)                         | [**WinHttpConnect**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpconnect)                                                                                                                                                               | Der Kontextwert wird mit [**WinHttpSendRequest**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpsendrequest) oder [**WinHttpSetOption**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpsetoption)festgelegt. Anforderungs Optionen werden mit [**WinHttpOpenRequest**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpopenrequest)festgelegt. Benutzer Anmelde Informationen werden mit [**winhttpsetanmelde**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpsetcredentials)Informationen festgelegt.                                 |
| [**Internetcrackurl**](/windows/desktop/api/wininet/nf-wininet-internetcrackurla)                       | [**Winhttpcrackurl**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpcrackurl)                                                                                                                                                             | Umgekehrtes Verhalten des ICU- \_ escapeflags: mit [**internetcrack URL**](/windows/desktop/api/wininet/nf-wininet-internetcrackurla)bewirkt dieses Flag, dass Escapesequenzen (% XX) in Zeichen konvertiert werden. mit [**winhttpcrackurl**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpcrackurl)werden jedoch Zeichen, die in einer HTTP-Anforderung mit Escapezeichen versehen werden müssen, in Escapesequenzen konvertiert. |
| [**Internetkreateurl**](/windows/desktop/api/wininet/nf-wininet-internetcreateurla)                     | [**Winhttpkreateurl**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpcreateurl)                                                                                                                                                           | Keine.                                                                                                                                                                                                                                                                                                                                |
| [**Internetzterrordlg**](/windows/desktop/api/wininet/nf-wininet-interneterrordlg)                       | Keine Entsprechung                                                                                                                                                                                          | Da WinHTTP auf serverseitige Anwendungen ausgerichtet ist, wird keine Benutzeroberfläche implementiert.                                                                                                                                                                                                                                   |
| [**InternetGetCookie**](/windows/desktop/api/wininet/nf-wininet-internetgetcookiea)                     | Keine Entsprechung                                                                                                                                                                                          | WinHTTP speichert keine Daten zwischen Sitzungen und kann nicht auf WinInet-Cookies zugreifen.                                                                                                                                                                                                                                                    |
| [**InternetOpen**](/windows/desktop/api/wininet/nf-wininet-internetopena)                               | [**WinHttpOpen**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpopen)                                                                                                                                                                     | Keine.                                                                                                                                                                                                                                                                                                                                |
| [**InternetOpenURL**](/windows/desktop/api/wininet/nf-wininet-internetopenurla)                         | [**WinHttpConnect**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpconnect), [**WinHttpOpenRequest**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpopenrequest), [**WinHttpSendRequest**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpsendrequest), [**WinHttpReceiveResponse**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpreceiveresponse) | Diese Funktionalität ist in den aufgeführten WinHTTP-Funktionen verfügbar.                                                                                                                                                                                                                                                                     |
| [**Internetquerydataavailable**](/windows/desktop/api/wininet/nf-wininet-internetquerydataavailable)   | [**WinHttpQueryDataAvailable**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpquerydataavailable)                                                                                                                                         | Keine reservierten Parameter.                                                                                                                                                                                                                                                                                                              |
| [**InternetQueryOption**](/windows/desktop/api/wininet/nf-wininet-internetqueryoptiona)                 | [**WinHttpQueryOption**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpqueryoption)                                                                                                                                                       | WinHTTP bietet einen anderen Satz von Optionen als Wininet. Weitere Informationen und Optionen, die von WinHTTP angeboten werden, finden Sie unter [**Optionsflags**](option-flags.md).                                                                                                                                                                               |
| [**Internetreadfile**](/windows/desktop/api/wininet/nf-wininet-internetreadfile)                       | [**WinHttpReadData**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpreaddata)                                                                                                                                                             | Keine.                                                                                                                                                                                                                                                                                                                                |
| [**Internetreadfileex**](/windows/desktop/api/wininet/nf-wininet-internetreadfileexa)                   | [**WinHttpReadData**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpreaddata)                                                                                                                                                             | Anstelle einer Struktur ist der Puffer ein Speicherbereich, der mit einem Zeiger adressiert wird.                                                                                                                                                                                                                                                  |
| [**Internettoption**](/windows/desktop/api/wininet/nf-wininet-internetsetoptiona)                     | [**WinHttpSetOption**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpsetoption)                                                                                                                                                           | Keine.                                                                                                                                                                                                                                                                                                                                |
| [**Internetsetstatus Callback**](/windows/desktop/api/wininet/nf-wininet-internetsetstatuscallback)     | [**Winhttpsetstatus-Rückruf**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpsetstatuscallback)                                                                                                                                           | Weitere Informationen finden Sie unter "unterschiedliche Verarbeitung von asynchronen Anforderungen" in diesem Thema.                                                                                                                                                                                                                                               |
| [**Internettimefromsystemtime**](/windows/desktop/api/wininet/nf-wininet-internettimefromsystemtime)   | [**Winhttptimefromsystemtime**](/windows/desktop/api/Winhttp/nf-winhttp-winhttptimefromsystemtime)                                                                                                                                         | Keine.                                                                                                                                                                                                                                                                                                                                |
| [**Internettimeto SYSTEMTIME**](/windows/desktop/api/wininet/nf-wininet-internettimetosystemtime)       | [**Winhttptimeumsystemtime**](/windows/desktop/api/Winhttp/nf-winhttp-winhttptimetosystemtime)                                                                                                                                             | Keine.                                                                                                                                                                                                                                                                                                                                |
| [**Internetschreibdatei**](/windows/desktop/api/wininet/nf-wininet-internetwritefile)                     | [**Winhttpschreitedata**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpwritedata)                                                                                                                                                           | Keine.                                                                                                                                                                                                                                                                                                                                |



 

## <a name="different-handling-of-asynchronous-requests"></a>Unterschiedliche Verarbeitung von asynchronen Anforderungen

Beachten Sie, dass einige Funktionen in WinInet und WinHTTP entweder synchron oder asynchron asynchrone Anforderungen ausführen können. Die Anwendung muss beide Situationen verarbeiten. Es gibt bedeutende Unterschiede in der Art und Weise, wie WinInet und WinHTTP diese potenziell asynchronen Funktionen verarbeiten.

WinInet

-   Synchrone Vervollständigung: Wenn ein potenziell asynchroner WinInet-Funktions aufrufgleich synchron abgeschlossen wird, geben die Out-Parameter der Funktion die Ergebnisse des Vorgangs zurück. Wenn ein Fehler auftritt, rufen Sie den Fehlercode ab, indem Sie [**GetLastError**](/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror) nach dem WinInet-Funktionsaufruf aufrufen.

-   Asynchroner Abschluss: Wenn ein potenziell asynchroner Funktionsaufruf asynchron abgeschlossen wird, sind die Ergebnisse des Vorgangs und alle Fehler in der Rückruffunktion zugänglich. Die Rückruffunktion wird für einen Arbeits Thread ausgeführt, nicht für den Thread, der den anfänglichen Funktionsaufrufs ausgeführt hat.

Anders ausgedrückt: die Anwendung muss die Logik duplizieren, um die Ergebnisse dieser Vorgänge an zwei Stellen verarbeiten zu können: unmittelbar nach dem Funktionsaufrufs und in der Rückruffunktion.

WinHTTP vereinfacht dieses Modell, indem es Ihnen ermöglicht wird, die Betriebs Logik nur in der Rückruffunktion zu implementieren, die eine Vervollständigungs Benachrichtigung erhält, unabhängig davon, ob der Vorgang synchron oder asynchron abgeschlossen wurde. Wenn der asynchrone Vorgang aktiviert ist, geben die Out-Parameter von WinHTTP-Funktionen keine aussagekräftigen Daten zurück und müssen auf **null** festgelegt werden.

Der einzige bedeutende Unterschied zwischen der asynchronen und synchronen Vervollständigung in WinHTTP liegt in der Anwendungsperspektive darin, wo die Rückruffunktion ausgeführt wird.

WinHTTP

-   Synchrone Vervollständigung: Wenn ein Vorgang synchron abgeschlossen wird, werden die Ergebnisse in einer Rückruffunktion zurückgegeben, die im gleichen Thread wie der ursprüngliche Funktionsaufrufs ausgeführt wird.

-   Asynchroner Abschluss: Wenn ein Vorgang asynchron abgeschlossen wird, werden die Ergebnisse in einer Rückruffunktion zurückgegeben, die in einem Arbeits Thread ausgeführt wird.

Obwohl die meisten Fehler auch vollständig innerhalb der Rückruffunktion behandelt werden können, müssen WinHTTP-Anwendungen trotzdem darauf vorbereitet sein,  dass eine Funktion aufgrund eines \_ ungültigen \_ Parameters oder eines anderen ähnlichen Fehlers, der durch Aufrufen von [**GetLastError**](/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror)abgerufen wurde, false zurückgibt.

Anders als bei WinInet, bei dem mehrere asynchrone Vorgänge gleichzeitig ausgeführt werden können, erzwingt WinHTTP eine Richtlinie mit einem ausstehenden asynchronen Vorgang pro Anforderungs handle. Wenn ein Vorgang aussteht und eine andere WinHTTP-Funktion aufgerufen wird, schlägt die zweite Funktion fehl, und [**GetLastError**](/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror) gibt einen \_ ungültigen \_ Vorgang zurück.

WinHTTP vereinfacht dieses Modell, indem es Ihnen ermöglicht wird, die Betriebs Logik nur in der Rückruffunktion zu implementieren, die eine Vervollständigungs Benachrichtigung erhält, unabhängig davon, ob der Vorgang synchron oder asynchron abgeschlossen wurde. Wenn der asynchrone Vorgang aktiviert ist, geben die Out-Parameter von WinHTTP-Funktionen keine aussagekräftigen Daten zurück und müssen auf **null** festgelegt werden.

## <a name="differences-in-winhttp-callback-notifications"></a>Unterschiede bei WinHTTP-Rückruf Benachrichtigungen

Die Status Rückruffunktion empfängt Updates über den Status von Vorgängen über Benachrichtigungsflags. In WinHTTP werden Benachrichtigungen mit dem *dwnotificationflags* -Parameter der [**winhttpsetstatus-Rückruf**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpsetstatuscallback) Funktion ausgewählt. Verwenden Sie das Flag für das **WinHTTP- \_ Rückruf \_ Flag \_ alle \_ Benachrichtigungen** , um über alle Statusaktualisierungen benachrichtigt zu werden.

Benachrichtigungen, die darauf hinweisen, dass ein bestimmter Vorgang abgeschlossen ist, werden als Vervollständigungs Benachrichtigungen oder nur Vervollständigungen bezeichnet. Jedes Mal, wenn die Rückruffunktion einen Abschluss empfängt, enthält der *lpvstatusinformation* -Parameter in WinInet eine asynchrone [**Internet \_ \_ Ergebnis**](/windows/desktop/api/wininet/ns-wininet-internet_async_result) Struktur. In WinHTTP ist diese Struktur nicht für alle Vervollständigungen verfügbar. Es ist wichtig, die Referenzseite für den [**WinHTTP- \_ Status \_ Rückruf**](/windows/win32/api/winhttp/nc-winhttp-winhttp_status_callback)zu überprüfen, der Informationen zu Benachrichtigungen und die Art der zu erwartenden Daten enthält.

In WinHTTP gibt eine einzelne Beendigung, **WinHTTP- \_ Rückruf \_ Status- \_ Anforderungs \_ Fehler**, an, dass ein Vorgang fehlgeschlagen ist. Alle anderen Vervollständigungen zeigen einen erfolgreichen Vorgang an.

Sowohl WinInet als auch WinHTTP verwenden einen benutzerdefinierten Kontextwert, um Informationen aus dem Haupt Thread an die Status Rückruffunktion zu übergeben, die für einen Arbeits Thread ausgeführt werden kann. In WinInet wird der von der Status Rückruffunktion verwendete Kontextwert festgelegt, indem eine von mehreren Funktionen aufgerufen wird. In WinHTTP wird der Kontextwert nur mit " [**WinHttpSendRequest**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpsendrequest) " oder " [**WinHttpSetOption**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpsetoption)" festgelegt. Daher ist es in WinHTTP möglich, dass eine Benachrichtigung auftritt, bevor ein Kontextwert festgelegt wird. Wenn die Rückruffunktion eine Benachrichtigung empfängt, bevor der Kontextwert festgelegt wird, muss die Anwendung auf den Empfang von **null** im *dwcontext* -Parameter der Rückruffunktion vorbereitet werden.

## <a name="authentication-differences"></a>Authentifizierungs Unterschiede

In WinInet werden Benutzer Anmelde Informationen festgelegt, indem die [**internettoption**](/windows/desktop/api/wininet/nf-wininet-internetsetoptiona) -Funktion aufgerufen wird. dabei wird Code verwendet, der dem im folgenden Codebeispiel ähnelt.

``` syntax
// Use the WinINet InternetSetOption function to set the 
// user credentials to the user name contained in strUsername 
// and the password to the contents of strPassword.
       
InternetSetOption( hRequest, INTERNET_OPTION_PROXY_USERNAME, 
                   strUsername, strlen(strUsername) + 1 );

InternetSetOption( hRequest, INTERNET_OPTION_PROXY_PASSWORD, 
                   strPassword, strlen(strPassword) + 1 );
```

Aus Kompatibilitätsgründen können Benutzer Anmelde Informationen auf ähnliche Weise in WinHTTP mithilfe der [**WinHttpSetOption**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpsetoption) -Funktion festgelegt werden. Dies wird jedoch nicht empfohlen, da Sie ein Sicherheitsrisiko darstellen kann.

Wenn eine Anwendung einen 401-Statuscode in WinHTTP empfängt, wird die empfohlene Methode zum Festlegen von Anmelde Informationen zuerst zum Identifizieren eines Authentifizierungs Schemas mithilfe von [**winhttpqueryauthschemas**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpqueryauthschemes) und zum zweiten Festlegen der Anmelde Informationen mithilfe von [**winhttpsetanmelde**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpsetcredentials)Informationen verwendet. Das folgende Codebeispiel zeigt, wie Sie dies tun.

``` syntax
DWORD dwSupportedSchemes;
DWORD dwPrefered;
DWORD dwTarget;

// Obtain the supported and first schemes.
WinHttpQueryAuthSchemes( hRequest, &dwSupportedSchemes, &dwPrefered, &dwTarget );

// Set the credentials before resending the request.
WinHttpSetCredentials( hRequest, dwTarget, dwPrefered, strUsername, strPassword, NULL );
```

Da es in WinHTTP keine Entsprechung für " [**internetterrordlg**](/windows/desktop/api/wininet/nf-wininet-interneterrordlg) " gibt, müssen Anwendungen, die Anmelde Informationen über eine Benutzeroberfläche abrufen, eine eigene Schnittstelle bereitstellen.

Anders als WinInet werden Kenn Wörter von WinHTTP nicht zwischengespeichert. Für jede Anforderung müssen gültige Benutzer Anmelde Informationen angegeben werden.

WinHTTP unterstützt das von WinInet unterstützte Schema für verteilte Kenn Wort Authentifizierung (dpa) nicht. WinHTTP unterstützt jedoch Microsoft Passport 1,4. Weitere Informationen zur Verwendung der Passport-Authentifizierung in WinHTTP finden Sie unter [Passport Authentication in WinHTTP (in WinHTTP](passport-authentication-in-winhttp.md)).

WinHTTP beruht nicht auf Internet Explorer-Einstellungen, um die Richtlinie für die automatische Anmeldung zu bestimmen. Stattdessen wird die Richtlinie für die automatische Anmeldung mit [**WinHttpSetOption**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpsetoption)festgelegt. Weitere Informationen zur Authentifizierung in WinHTTP, einschließlich der Richtlinie für die automatische Anmeldung, finden Sie unter [Authentifizierung in WinHTTP](authentication-in-winhttp.md).

## <a name="differences-in-secure-http-transactions"></a>Unterschiede bei sicheren HTTP-Transaktionen

Initiieren Sie in WinInet eine sichere Sitzung mithilfe von [**httpopzurequest**](/windows/desktop/api/wininet/nf-wininet-httpopenrequesta) oder [**InternetConnect**](/windows/desktop/api/wininet/nf-wininet-internetconnecta), aber in WinHTTP müssen Sie [**winhttpoperrequest**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpopenrequest) mit dem sicheren Flag **WinHTTP \_ - \_ Flag** aufruft.

In einer sicheren HTTP-Transaktion können Server Zertifikate verwendet werden, um einen Server für den Client zu authentifizieren. Wenn in WinInet ein Serverzertifikat Fehler enthält, schlägt [**HttpSendRequest**](/windows/desktop/api/wininet/nf-wininet-httpsendrequesta) fehl und stellt Details zu den Zertifikat Fehlern bereit.

In WinHTTP werden Serverzertifikat Fehler gemäß der-Version wie folgt behandelt:

-   Beginnend mit WinHTTP 5,1, wenn ein Serverzertifikat ausfällt oder Fehler enthält, meldet der [**WinHttpSendRequest**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpsendrequest) -Rückruf einen fehlerhaften **WinHTTP- \_ Rückruf \_ Status \_ \_** in der Rückruffunktion. Wenn der von **WinHttpSendRequest** generierte Fehler ignoriert wird, tritt bei nachfolgenden Aufrufen von [**WinHttpReceiveResponse**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpreceiveresponse) ein Fehler auf, wenn der \_ WinHTTP- \_ Vorgang \_ abgebrochen wurde.
-   In WinHTTP 5,0 bewirken Fehler in Server Zertifikaten standardmäßig nicht, dass eine Anforderung fehlschlägt. Stattdessen werden die Fehler in der Rückruffunktion mit der Benachrichtigung " **\_ \_ \_ sicherer \_ Fehler beim WinHTTP-Rückruf Status** " gemeldet.

Auf einigen früheren Plattformen unterstützte Wininet die Protokolle der private Kommunikationstechnologie (PCT) und/oder "Fortezza", aber nicht unter Windows XP.

WinHTTP unterstützt das PCT-und das Fortezza-Protokoll auf keiner Plattform und basiert stattdessen auf Secure Sockets Layer (SSL) 2,0, SSL 3,0 oder Transport Layer Security (TLS) 1,0.

 

 
