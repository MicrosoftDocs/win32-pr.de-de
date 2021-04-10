---
title: Aktivieren der Internet Funktionalität
description: Vor der Verwendung der WinInet-Funktionen sollte die Anwendung versuchen, mithilfe der internettattemptconnect-Funktion eine Verbindung mit dem Internet herzustellen.
ms.assetid: 80747c0d-5a09-4ffa-a0ca-b051b82acbf8
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: adb44fadaf0726b81618dde19105da7517673a00
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "104039473"
---
# <a name="enabling-internet-functionality"></a>Aktivieren der Internet Funktionalität

Vor der Verwendung der WinInet-Funktionen sollte die Anwendung versuchen, mithilfe der [**internettattemptconnect**](/windows/desktop/api/Wininet/nf-wininet-internetattemptconnect) -Funktion eine Verbindung mit dem Internet herzustellen. Diese Funktion Ruft das DFÜ-Dialogfeld auf, um eine Verbindung mit dem Internet zu initiieren oder zu überprüfen, ob bereits eine Verbindung vorhanden ist. Wenn diese Funktion fehlschlägt, kann die Anwendung in den Offline Modus wechseln, sodass Sie auf Informationen zugreifen kann, die während vorheriger Verbindungen mit dem Internet zwischengespeichert wurden.

Verwenden Sie die [**internetcheckconnection**](/windows/desktop/api/Wininet/nf-wininet-internetcheckconnectiona) -Funktion, um die Verbindung mit dem Internet zu überprüfen. Es wird versucht, den Server zu pingen, der durch die an die Funktion über gegebene URL festgelegt ist. Wenn das Flag \_ \_ für die agentforce \_ -Verbindung festgelegt ist und die URL **null** ist, überprüft die Funktion, ob ein Eintrag in der Server Datenbank für den nächstgelegenen Server vorhanden ist. Wenn eine solche vorhanden ist, sendet die Funktion einen Ping an diesen Server.

Verwenden Sie als nächstes die Funktion [**InternetOpen**](/windows/desktop/api/Wininet/nf-wininet-internetopena) , um die Merkmale der Internet Verbindung festzulegen, die von der Client Anwendung verwendet wird. [**InternetOpen**](/windows/desktop/api/Wininet/nf-wininet-internetopena) erstellt das Stamm- [**HINTERNET**](appendix-a-hinternet-handles.md) handle, das zum Einrichten von [http](http-sessions.md)-[FTP](ftp-sessions.md) -Sitzungen verwendet wird. [**InternetOpen**](/windows/desktop/api/Wininet/nf-wininet-internetopena) testet die Verbindung mit dem Internet nicht, um zu überprüfen, ob die an die Funktion übergebenen Merkmale korrekt sind.

Verwenden Sie die [**InternetConnect**](/windows/desktop/api/Wininet/nf-wininet-internetconnecta) -Funktion, um eine bestimmte Sitzung zu erstellen. [**InternetConnect**](/windows/desktop/api/Wininet/nf-wininet-internetconnecta) Initialisiert eine Sitzung für die angegebene Site mithilfe der an Sie über gebenden Argumente und erstellt ein [**hinternethandle**](appendix-a-hinternet-handles.md) , das eine Verzweigung vom Stamm Handle ist. [**InternetConnect**](/windows/desktop/api/Wininet/nf-wininet-internetconnecta) versucht nicht, auf eine Verbindung mit der angegebenen Site zuzugreifen oder eine Verbindung herzustellen, es sei denn, es handelt sich um eine FTP-Sitzung. Die Funktionen [**ftpfindfirstfile**](/windows/desktop/api/Wininet/nf-wininet-ftpfindfirstfilea), [**ftpopeinfile**](/windows/desktop/api/Wininet/nf-wininet-ftpopenfilea)und [**httpopaufrequest**](/windows/desktop/api/Wininet/nf-wininet-httpopenrequesta) verwenden das Handle, das von [**InternetConnect**](/windows/desktop/api/Wininet/nf-wininet-internetconnecta) erstellt wurde, um eine Verbindung mit der angegebenen Site herzustellen.

## <a name="using-internetopen"></a>Verwenden von InternetOpen

Um eine Verbindung mit dem Internet zu ermöglichen, muss ein [**HINTERNET**](appendix-a-hinternet-handles.md) -Stamm Handle mithilfe von [**InternetOpen**](/windows/desktop/api/Wininet/nf-wininet-internetopena)erstellt werden. Informationen über den Benutzer-Agent (die Anwendung, die die Internet Funktionen aufrufen), den Typ des Zugriffs auf das Internet, die Proxy Namen, die Hosts und Adressen, die den Proxy umgehen, und das Verhalten werden an [**InternetOpen**](/windows/desktop/api/Wininet/nf-wininet-internetopena)übermittelt.

### <a name="setting-the-user-agent"></a>Festlegen des Benutzer-Agents

Die aufrufende Anwendung sollte eine Zeichenfolge mit dem Namen der Anwendung oder Entität, die auf das Internet zugreift, auf den *lpszagent* -Parameter von [**InternetOpen**](/windows/desktop/api/Wininet/nf-wininet-internetopena)angeben. Diese Zeichenfolge wird als Benutzer-Agent im HTTP-Protokoll verwendet. Microsoft Internet Explorer verwendet beispielsweise "Microsoft Internet Explorer".

### <a name="setting-access-types"></a>Festlegen von Zugriffs Typen

[**InternetOpen**](/windows/desktop/api/Wininet/nf-wininet-internetopena) unterstützt drei Zugriffs Typen:

-   Verwenden Sie "Internet \_ Open \_ Type \_ Direct", wenn das System, auf dem die Anwendung ausgeführt wird, eine direkte Verbindung mit dem Internet verwendet. Die Parameter *lpszproxyname* und *lpszProxyBypass* von [**InternetOpen**](/windows/desktop/api/Wininet/nf-wininet-internetopena) werden nicht verwendet und sollten auf **null** festgelegt werden.
-   Verwenden \_ Sie den Internet Open- \_ \_ Typproxy, wenn das System, auf dem die Anwendung ausgeführt wird, einen oder mehrere Proxy Server für den Zugriff auf das Internet verwendet. [**InternetOpen**](/windows/desktop/api/Wininet/nf-wininet-internetopena) verwendet die durch *lpszproxyname* angegebenen Proxy Server und umgeht den Proxy für alle Hostnamen oder IP-Adressen, die von *lpszProxyBypass* angegeben werden.
-   Verwenden Sie \_ die Internet Open \_ Type \_ preconfig, um die Anwendung anzuweisen, die Konfiguration aus der Registrierung abzurufen. Dies ist in der Regel die beste Wahl, da die meisten Anwendungen, einschließlich Webbrowsern, diese Option verwenden.

Internet \_ Open \_ Type \_ preconfig prüft die Registrierungs Werte **ProxyEnable**, **Proxyserver** und **ProxyOverride**. Diese Werte befinden sich unter "HKEY \_ Current \_ User \\ Software \\ Microsoft \\ Windows \\ CurrentVersion \\ Internet Settings".

Wenn **ProxyEnable** gleich 0 (null) ist, verwendet die Anwendung Internet \_ Open \_ Type \_ Direct. Andernfalls verwendet die Anwendung den Internet \_ Open \_ \_ -Typproxy und verwendet die **Proxyserver** -und **ProxyOverride** -Informationen.

Die WinInet-Funktionen bieten nur dann Unterstützung für SOCKS-typproxys, wenn Internet Explorer installiert ist. Die Installation von Internet Explorer umfasst die Wsock32n.dll Datei, die zur Unterstützung von SOCKS-Proxys erforderlich ist. Wsock32n.dll ist nicht Verteil Bar.

### <a name="listing-proxy-servers"></a>Auflisten von Proxy Servern

WinInet erkennt zwei Typen von Proxys: CERN-typproxys (nur http) und tis-FTP-Proxys (nur FTP). Wenn Internet Explorer installiert ist, unterstützt WinInet auch SOCKS-typproxys. Bei [**InternetConnect**](/windows/desktop/api/Wininet/nf-wininet-internetconnecta) wird standardmäßig davon ausgegangen, dass es sich bei dem angegebenen Proxy um einen CERN-Proxy handelt. Wenn der Zugriffstyp auf Internet \_ Open \_ Type \_ Direct oder Internet \_ Open Type preconfig festgelegt ist \_ \_ , sollte der *lpszproxyname* -Parameter von [**InternetOpen**](/windows/desktop/api/Wininet/nf-wininet-internetopena) auf **null** festgelegt werden. Andernfalls muss der an *lpszproxyname* weiter gegebene Wert die Proxys in einer durch Leerzeichen getrennten Zeichenfolge enthalten. Die Proxy Listen können die Portnummer enthalten, die für den Zugriff auf den Proxy verwendet wird.

Zum Auflisten eines Proxys für ein bestimmtes Protokoll muss die Zeichenfolge dem Format "" <protocol> <protocol> ://<\_ Proxyname> "" entsprechen. Gültige Protokolle sind http, HTTPS und FTP. Zum Auflisten eines FTP-Proxys wäre z. b. "FTP = FTP://FTP \_ Proxy \_ Name: 21" ", wobei FTP- \_ Proxy \_ Name der Name des FTP-Proxys und 21 die Portnummer ist, die für den Zugriff auf den Proxy verwendet werden muss. Wenn der Proxy die Standard Portnummer für dieses Protokoll verwendet, kann die Portnummer ausgelassen werden. Wenn ein Proxy Name allein aufgeführt wird, wird er als Standard Proxy für alle Protokolle verwendet, für die kein bestimmter Proxy angegeben ist. "" Http = https://http\_proxy other "" verwendet beispielsweise http- \_ Proxy für http-Vorgänge, während für alle anderen Protokolle andere verwendet werden.

Standardmäßig geht die-Funktion davon aus, dass der von *lpszproxyname* angegebene Proxy ein CERN-Proxy ist. Eine Anwendung kann mehr als einen Proxy angeben, einschließlich verschiedener Proxys für die verschiedenen Protokolle. Wenn Sie z. b. "FTP = FTP://FTP-GW http = https://jericho:99 Proxy" "angeben, werden FTP-Anforderungen über den FTP-GW-Proxy hergestellt, der an Port 21 lauscht, und HTTP-Anforderungen werden über einen CERN-Proxy namens" Jericho "durchgeführt, der an Port 99 lauscht. Andernfalls werden HTTP-Anforderungen über den CERN-Proxy namens Proxy erfolgen, der an Port 80 lauscht. Beachten Sie Folgendes: Wenn die Anwendung nur FTP verwendet, muss Sie z. b. nicht "" FTP = FTP://FTP-GW: 21 "" angeben. Es kann nur "FTP-GW" angegeben werden. Eine Anwendung ist nur erforderlich, um die Protokollnamen anzugeben, wenn Sie mehr als ein Protokoll pro Handle verwendet, das von [**InternetOpen**](/windows/desktop/api/Wininet/nf-wininet-internetopena)zurückgegeben wurde.

### <a name="listing-the-proxy-bypass"></a>Auflisten der Proxy Umgehung

Hostnamen oder IP-Adressen, die nicht an den Proxy gesendet werden sollen, können in der Proxy Umgehungs Liste aufgeführt werden. Diese Liste kann Platzhalter enthalten, die \* bewirken, dass die Anwendung den Proxy Server für Adressen umgeht, die dem angegebenen Muster entsprechen. Wenn Sie mehrere Adressen und Hostnamen auflisten möchten, trennen Sie diese durch Semikolons in der Proxy Umgehungs Zeichenfolge. Wenn das <local> Makro "" angegeben wird, umgeht die Funktion den Proxy für jeden Hostnamen, der keinen Zeitraum enthält.

Standardmäßig umgeht WinInet den Proxy für Anforderungen, bei denen die Hostnamen "localhost", "Loopback", "127.0.0.1" oder " \[ :: 1" verwendet werden \] . Dieses Verhalten tritt auf, weil ein Remote Proxy Server diese Adressen in der Regel nicht ordnungsgemäß auflöst.

**Internet Explorer 9:** Sie können den lokalen Computer aus der Proxy Umgehungs Liste entfernen, indem Sie das Makro "<-Loopback>" verwenden.

Das folgende Beispiel zeigt Beispiel Aufrufe von [**InternetOpen**](/windows/desktop/api/Wininet/nf-wininet-internetopena) mithilfe verschiedener Proxy Umgehungs Zeichenfolgen. Die Kommentare über den einzelnen aufrufen beschreiben, welche Auswirkung die Umgehungs Zeichenfolge auf die Hostnamen hat, auf die über das erstellte [**HINTERNET**](appendix-a-hinternet-handles.md) -handle zugegriffen wird.


```C++
HINTERNET hInternetRoot;

/* bypass the proxy for any host name that does not 
    contain a period */
hInternetRoot = InternetOpen(TEXT("WinInet Example"), 
    INTERNET_OPEN_TYPE_PROXY,TEXT("proxy"),TEXT("<local>"), 0);

/* bypass the proxy for any host name that starts with the 
    letters "ms" */
hInternetRoot = InternetOpen(TEXT("WinInet Example"), 
    INTERNET_OPEN_TYPE_PROXY,TEXT("proxy"),TEXT("ms*"), 0);

/* bypass the proxy for any host name that contains "int", 
    such as "internet" and "painter" */
hInternetRoot = InternetOpen(TEXT("WinInet Example"), 
    INTERNET_OPEN_TYPE_PROXY,TEXT("proxy"),TEXT("*int*"), 0);

/* bypass the proxy for the host name "example" and any 
    host name that contains "test" */
hInternetRoot = InternetOpen(TEXT("WinInet Example"), 
    INTERNET_OPEN_TYPE_PROXY,TEXT("proxy"),TEXT("example *test*"), 0);

/* Disable the loopback proxy bypass for localhost */
hInternetRoot = InternetOpen(TEXT("WinInet Example"), 
    INTERNET_OPEN_TYPE_PROXY,TEXT("127.0.0.1:8888"),TEXT("<-loopback>"), 0);
```



## <a name="using-internetconnect"></a>Verwenden von InternetConnect

Um eine Sitzung zu beginnen, muss die [**InternetConnect**](/windows/desktop/api/Wininet/nf-wininet-internetconnecta) -Funktion ein Handle aus dem Stamm Handle erstellen, das von der [**InternetOpen**](/windows/desktop/api/Wininet/nf-wininet-internetopena) -Funktion zurückgegeben wird. [**InternetConnect**](/windows/desktop/api/Wininet/nf-wininet-internetconnecta) legt die Server Adresse, die Portnummer, den Benutzernamen, das Kennwort und den Diensttyp fest.

[**InternetConnect**](/windows/desktop/api/Wininet/nf-wininet-internetconnecta) verwendet das [**HINTERNET-**](appendix-a-hinternet-handles.md) Stamm handle, das von [**InternetOpen**](/windows/desktop/api/Wininet/nf-wininet-internetopena) erstellt wurde, um ein Sitzungs handle einzurichten. Wenn das [Internet \_ Flag " \_ Async](api-flags.md) "-Flag im Aufrufen von [**InternetOpen**](/windows/desktop/api/Wininet/nf-wininet-internetopena)festgelegt wurde, sollte der Internet [**Connect**](/windows/desktop/api/Wininet/nf-wininet-internetconnecta) -aufrufen einen Kontextwert ungleich 0 (null) enthalten.

Der Servername kann entweder den Hostnamen (z. b. "www.Servername.com") oder die IP-Nummer der Site im ASCII-Format mit gepunktetem Dezimaltrennzeichen (z. b. "10.0.1.45") enthalten.

Der Serverport ist die TCP/IP-Portnummer (Transmission Control Protocol/Internet Protocol), mit der auf dem Server eine Verbindung hergestellt werden soll. [**InternetConnect**](/windows/desktop/api/Wininet/nf-wininet-internetconnecta) verwendet den Standardport für den ausgewählten Diensttyp, wenn der \_ Wert Internet ungültige \_ Port \_ Nummer verwendet wird. Die folgenden Tabellen enthalten die Standardwerte für den Server Anschluss für Wininet.



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th>Wert</th>
<th>Bedeutung</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>INTERNET_DEFAULT_FTP_PORT</td>
<td>Verwenden Sie den Standardport für FTP-Server (Port 21).</td>
</tr>
<tr class="even">
<td>INTERNET_DEFAULT_GOPHER_PORT</td>
<td>Verwenden Sie den Standardport für Gopher-Server (Port 70).
<blockquote>
[!Note]<br />
Nur Windows XP und Windows Server 2003 R2 und früher.
</blockquote>
<br/></td>
</tr>
<tr class="odd">
<td>INTERNET_DEFAULT_HTTP_PORT</td>
<td>Verwenden Sie den Standardport für http-Server (Port 80).</td>
</tr>
<tr class="even">
<td>INTERNET_DEFAULT_HTTPS_PORT</td>
<td>Verwenden Sie den Standardport für HTTPS-Server (Port 443).</td>
</tr>
<tr class="odd">
<td>INTERNET_DEFAULT_SOCKS_PORT</td>
<td>Verwenden Sie den Standardport für die SOCKS-Firewallserver (Port 1080).</td>
</tr>
</tbody>
</table>



 

### <a name="defining-the-user-name-and-password"></a>Definieren von Benutzer Name und Kennwort

Der Wert von *lpszusername* ist die Adresse einer auf **null** endenden Zeichenfolge, die den Namen des Benutzers enthält, der sich anmeldet. Wenn dieser Parameter **null** ist, verwendet die Funktion einen passenden Standardwert, mit Ausnahme von http. Ein **null** -Parameter in http bewirkt, dass der Server einen Fehler zurückgibt. Der Standardwert für das FTP-Protokoll ist Anonymous.

Der Wert von *lpszpassword* ist die Adresse einer auf **null** endenden Zeichenfolge, die das Anmelde Kennwort enthält. Wenn sowohl *lpszusername* als auch *lpszpassword* **null** sind, verwendet die Funktion das anonyme Standard Kennwort. Im Fall von FTP ist das anonyme Standard Kennwort der e-Mail-Name des Benutzers. Wenn *lpszusername* nicht **null** und *lpszpassword* den Wert **null** hat, verwendet die Funktion ein leeres Kennwort. Es gibt vier mögliche Einstellungen von " *lpszusername* " und " *lpszpassword*", die die in der folgenden Tabelle dargestellten Verhalten ergeben.



| *lpszusername*      | *lpszpassword*      | An den FTP-Server gesendeter Benutzername | Kennwort an FTP-Server gesendet |
|---------------------|---------------------|------------------------------|-----------------------------|
| **NULL**            | **NULL**            | Anonymous                  | E-Mail-Name des Benutzers           |
| Zeichenfolge ungleich **null** | **NULL**            | *lpszusername*               | ""                          |
| **NULL**            | Zeichenfolge ungleich **null** | ERROR                        | ERROR                       |
| Zeichenfolge ungleich **null** | Zeichenfolge ungleich **null** | *lpszusername*               | *lpszpassword*              |



 

Diese Informationen können mithilfe der Funktionen [**InternetSetOption**](/windows/desktop/api/Wininet/nf-wininet-internetsetoptiona) und [**internetterrordlg**](/windows/desktop/api/Wininet/nf-wininet-interneterrordlg) geändert werden. [**InternetSetOption**](/windows/desktop/api/Wininet/nf-wininet-internetsetoptiona) ändert die Werte für Benutzername und Kennwort, während in [**internetterrordlg**](/windows/desktop/api/Wininet/nf-wininet-interneterrordlg) ein Dialogfeld angezeigt wird, in dem der richtige Benutzername und das Kennwort angefordert werden.

### <a name="defining-the-session"></a>Definieren der Sitzung

Legen Sie den Diensttyp, die Flags und den Kontextwert für [**InternetConnect**](/windows/desktop/api/Wininet/nf-wininet-internetconnecta)fest, um die Sitzung zu definieren, die erstellt wird.

Es stehen zwei Dienst Typen für [**InternetConnect**](/windows/desktop/api/Wininet/nf-wininet-internetconnecta)zur Verfügung: Internet \_ Dienst \_ FTP und Internet \_ Dienst \_ http. Internet \_ Dienst \_ http wird für http-und HTTPS-Sitzungen verwendet.

[Internet \_ Das Flag \_ passiv](api-flags.md) ist das einzige Dienst spezifische Flag, das von den WinInet-Funktionen verwendet wird. Dieses Flag kann festgelegt werden, wenn der Diensttyp "Internet Dienst-FTP" ist \_ \_ , um die passive FTP-Semantik zu verwenden.

Bei allen synchronen Vorgängen sollte der Wert von *dwcontext* auf 0 (null) festgelegt werden. Wenn asynchrone Vorgänge durch Festlegen des " [Internet \_ Flag \_ Async](api-flags.md) "-Flags im-Aufrufen von [**InternetOpen**](/windows/desktop/api/Wininet/nf-wininet-internetopena)erstellt wurden, sollte für *dwcontext* ein Wert ungleich 0 (null) angegeben werden. Weitere Informationen zu asynchronen Vorgängen finden [Sie unter Einrichten von asynchronen Vorgängen](common-functions.md).

Bei FTP-Sitzungen versucht [**InternetConnect**](/windows/desktop/api/Wininet/nf-wininet-internetconnecta) , eine Verbindung mit dem Server im Internet herzustellen. Für HTTP-Sitzungen stellt [**InternetConnect**](/windows/desktop/api/Wininet/nf-wininet-internetconnecta) keine Verbindung her, bis eine andere Funktion versucht, Informationen vom Server zu erhalten.

> [!Note]  
> WinInet unterstützt keine Server Implementierungen. Außerdem sollte Sie nicht von einem Dienst verwendet werden. Verwenden Sie für Server Implementierungen oder-Dienste [Microsoft Windows HTTP-Dienste (WinHTTP)](/windows/desktop/WinHttp/winhttp-start-page).

 

 

