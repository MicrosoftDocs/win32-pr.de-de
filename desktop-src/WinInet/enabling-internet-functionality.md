---
title: Aktivieren der Internetfunktionalität
description: Vor der Verwendung der WinINet-Funktionen sollte die Anwendung versuchen, mithilfe der InternetAttemptConnect-Funktion eine Verbindung mit dem Internet herzustellen.
ms.assetid: 80747c0d-5a09-4ffa-a0ca-b051b82acbf8
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 303567942bc94754c1f2a7735851501a4f53036dbd8059420a059a6b632576d0
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119570200"
---
# <a name="enabling-internet-functionality"></a>Aktivieren der Internetfunktionalität

Vor der Verwendung der WinINet-Funktionen sollte die Anwendung versuchen, mithilfe der [**InternetAttemptConnect-Funktion**](/windows/desktop/api/Wininet/nf-wininet-internetattemptconnect) eine Verbindung mit dem Internet herzustellen. Diese Funktion ruft das DFÜ-Dialogfeld auf, um eine Verbindung mit dem Internet zu initiieren oder zu überprüfen, ob bereits eine Verbindung vorhanden ist. Wenn diese Funktion fehlschlägt, kann die Anwendung in den Offlinemodus wechseln, wodurch sie auf Informationen zugreifen kann, die während vorheriger Verbindungen mit dem Internet zwischengespeichert wurden.

Verwenden Sie die [**InternetCheckConnection-Funktion,**](/windows/desktop/api/Wininet/nf-wininet-internetcheckconnectiona) um die Verbindung mit dem Internet zu überprüfen. Es wird versucht, den Server zu pingen, der durch die URL festgelegt ist, die an die Funktion übergeben wird. Wenn das FLAG FORCE FORCE CONNECTION-Flag festgelegt ist und die URL NULL ist, überprüft die Funktion, ob ein Eintrag in der Serverdatenbank für den \_ \_ \_ nächstgelegenen Server vorhanden ist.  Falls vorhanden, pingt die Funktion diesen Server.

Verwenden Sie als Nächstes die [**InternetOpen-Funktion,**](/windows/desktop/api/Wininet/nf-wininet-internetopena) um die Merkmale der Internetverbindung zu erstellen, die die Clientanwendung verwendet. [**InternetOpen erstellt**](/windows/desktop/api/Wininet/nf-wininet-internetopena) das [**HINTERNET-Stammhand**](appendix-a-hinternet-handles.md) handle, das zum Einrichten von [HTTP-FTP-Sitzungen](http-sessions.md)[verwendet](ftp-sessions.md) wird. [**InternetOpen teste**](/windows/desktop/api/Wininet/nf-wininet-internetopena) die Verbindung mit dem Internet nicht, um sicherzustellen, dass die an die Funktion übergebenen Merkmale korrekt sind.

Verwenden Sie die [**InternetConnect-Funktion,**](/windows/desktop/api/Wininet/nf-wininet-internetconnecta) um eine bestimmte Sitzung zu erstellen. [**InternetConnect**](/windows/desktop/api/Wininet/nf-wininet-internetconnecta) initialisiert eine Sitzung für den angegebenen Standort unter Verwendung der übergebenen Argumente und erstellt ein [**HINTERNET-Handle,**](appendix-a-hinternet-handles.md) bei dem es sich um eine Verzweigung vom Stammhand handle handelt. [**InternetConnect**](/windows/desktop/api/Wininet/nf-wininet-internetconnecta) versucht nicht, auf den angegebenen Standort zu zugreifen oder eine Verbindung mit diesem herzustellen, außer im Fall einer FTP-Sitzung. [**Die Funktionen FtpFindFirstFile,**](/windows/desktop/api/Wininet/nf-wininet-ftpfindfirstfilea) [**FtpOpenFile**](/windows/desktop/api/Wininet/nf-wininet-ftpopenfilea)und [**HttpOpenRequest**](/windows/desktop/api/Wininet/nf-wininet-httpopenrequesta) verwenden das von [**InternetConnect**](/windows/desktop/api/Wininet/nf-wininet-internetconnecta) erstellte Handle, um eine Verbindung mit der angegebenen Website herzustellen.

## <a name="using-internetopen"></a>Verwenden von InternetOpen

Um eine Verbindung mit dem Internet zu aktivieren, muss ein [**HINTERNET-Stammhand**](appendix-a-hinternet-handles.md) handle mit [**internetOpen erstellt werden.**](/windows/desktop/api/Wininet/nf-wininet-internetopena) Informationen über den Benutzer-Agent (die Anwendung, die die Internetfunktionen aufruft), die Art des Zugriffs auf das Internet, die Proxynamen, die Hosts und Adressen, die den Proxy umgehen, und das Verhalten werden [**an InternetOpen übergeben.**](/windows/desktop/api/Wininet/nf-wininet-internetopena)

### <a name="setting-the-user-agent"></a>Festlegen des Benutzer-Agents

Die aufrufende Anwendung sollte eine Zeichenfolge mit dem Namen der Anwendung oder Entität, die auf das Internet zutritt, für den *lpszAgent-Parameter* [**von InternetOpen angeben.**](/windows/desktop/api/Wininet/nf-wininet-internetopena) Diese Zeichenfolge wird als Benutzer-Agent im HTTP-Protokoll verwendet. Beispielsweise verwendet Microsoft Internet Explorer "Microsoft Internet Explorer".

### <a name="setting-access-types"></a>Festlegen von Zugriffstypen

[**InternetOpen unterstützt**](/windows/desktop/api/Wininet/nf-wininet-internetopena) drei Zugriffstypen:

-   Verwenden Sie INTERNET OPEN TYPE DIRECT, wenn das System, auf dem die Anwendung ausgeführt \_ \_ \_ wird, eine direkte Verbindung mit dem Internet verwendet. Die *Parameter lpszProxyName* und *lpszProxyBypass* von [**InternetOpen**](/windows/desktop/api/Wininet/nf-wininet-internetopena) werden nicht verwendet und sollten auf **NULL festgelegt werden.**
-   Verwenden Sie INTERNET OPEN TYPE PROXY, wenn das System, auf dem die Anwendung ausgeführt wird, einen oder mehrere Proxyserver für \_ den Zugriff auf das Internet \_ \_ verwendet. [**InternetOpen verwendet**](/windows/desktop/api/Wininet/nf-wininet-internetopena) die durch *lpszProxyName* angegebenen Proxyserver und umgeht den Proxy für alle Hostnamen oder IP-Adressen, die von *lpszProxyBypass angegeben werden.*
-   Verwenden Sie INTERNET \_ OPEN \_ TYPE \_ PRECONFIG, um Ihre Anwendung anweisen, die Konfiguration aus der Registrierung abzurufen. Dies ist in der Regel die beste Wahl, da die meisten Anwendungen einschließlich Webbrowser diese Option verwenden.

INTERNET \_ OPEN \_ TYPE \_ PRECONFIG untersucht die Registrierungswerte **ProxyEnable,** **ProxyServer** und **ProxyOverride.** Diese Werte befinden sich unter "HKEY \_ CURRENT USER Software Microsoft Windows \_ \\ \\ \\ \\ CurrentVersion Internet \\ Einstellungen".

Wenn **ProxyEnable 0** (null) ist, verwendet die Anwendung INTERNET \_ OPEN TYPE \_ \_ DIRECT. Andernfalls verwendet die Anwendung INTERNET \_ OPEN TYPE PROXY und die \_ \_ **ProxyServer-** und **ProxyOverride-Informationen.**

Die WinINet-Funktionen unterstützen SOCKS-Typproxies nur, wenn Internet Explorer installiert ist. Die Installation von Internet Explorer enthält die Wsock32n.dll, die zur Unterstützung von SOCKS-Proxys erforderlich ist. Wsock32n.dll nicht verteilbar.

### <a name="listing-proxy-servers"></a>Auflisten von Proxyservern

WinINet erkennt zwei Arten von Proxys: Proxys vom TYP CERN (nur HTTP) und FTP-Proxys (nur FTP). Wenn Internet Explorer installiert ist, unterstützt WinINet auch PROXYS vom Typ SOCKS. [**InternetConnect**](/windows/desktop/api/Wininet/nf-wininet-internetconnecta) geht standardmäßig davon aus, dass der angegebene Proxy ein CERN-Proxy ist. Wenn der Zugriffstyp auf INTERNET OPEN TYPE DIRECT oder INTERNET OPEN TYPE PRECONFIG festgelegt ist, sollte der \_ \_ \_ \_ \_ \_ *lpszProxyName-Parameter* von [**InternetOpen**](/windows/desktop/api/Wininet/nf-wininet-internetopena) auf **NULL festgelegt werden.** Andernfalls muss der an *lpszProxyName* übergebene Wert die Proxys in einer durch Leerzeichen getrennten Zeichenfolge enthalten. Die Proxyauflistungen können die Portnummer enthalten, die für den Zugriff auf den Proxy verwendet wird.

Um einen Proxy für ein bestimmtes Protokoll auflisten zu können, muss die Zeichenfolge das Format "" <protocol> <protocol> ://<\_ Proxyname>"" haben. Die gültigen Protokolle sind HTTP, HTTPS und FTP. Um beispielsweise einen FTP-Proxy auflisten zu können, wäre eine gültige Zeichenfolge ""ftp=ftp://ftp://Proxyname:21", wobei ftp proxy name der Name des FTP-Proxys und \_ 21 die Portnummer ist, die für den Zugriff auf den Proxy verwendet werden \_ \_ \_ muss. Wenn der Proxy die Standardportnummer für dieses Protokoll verwendet, kann die Portnummer weggelassen werden. Wenn ein Proxyname selbst aufgeführt wird, wird er als Standardproxy für alle Protokolle verwendet, für die kein bestimmter Proxy angegeben ist. Beispielsweise würde "http= other"" den HTTP-Proxy für alle HTTP-Vorgänge verwenden, während alle anderen https://http\_proxy Protokolle andere Protokolle verwenden \_ würden.

Standardmäßig geht die Funktion davon aus, dass der von *lpszProxyName angegebene* Proxy ein CERN-Proxy ist. Eine Anwendung kann mehrere Proxys angeben, einschließlich verschiedener Proxys für die verschiedenen Protokolle. Wenn Sie beispielsweise ""ftp=ftp://ftp-gw HTTP= proxy"" angeben, werden FTP-Anforderungen über den ftp-gw-Proxy gesendet, der an Port 21 lausst, und HTTP-Anforderungen werden über einen CERN-Proxy mit dem Namen jericho gesendet, der an Port https://jericho:99 99 lausiert. Andernfalls würden HTTP-Anforderungen über den CERN-Proxy mit dem Namen proxy gesendet, der an Port 80 laussiert. Wenn die Anwendung beispielsweise nur FTP verwendet, muss sie ""ftp=ftp://ftp-gw:21" nicht angeben. Es könnte nur ""ftp-gw"" angegeben werden. Eine Anwendung muss nur dann die Protokollnamen angeben, wenn sie mehr als ein Protokoll pro Handle verwendet, das von [**InternetOpen zurückgegeben wird.**](/windows/desktop/api/Wininet/nf-wininet-internetopena)

### <a name="listing-the-proxy-bypass"></a>Auflisten der Proxyumgehung

Hostnamen oder IP-Adressen, die nicht an den Proxy gesendet werden sollen, können in der Proxyumgehungsliste aufgeführt werden. Diese Liste kann Platzhalter " " enthalten, wodurch die Anwendung den Proxyserver für Adressen \* umgeht, die dem angegebenen Muster entsprechen. Um mehrere Adressen und Hostnamen auflisten zu können, trennen Sie sie durch Semikolons in der Proxyumgehungszeichenfolge. Wenn das Makro " " angegeben ist, umgeht die Funktion den Proxy für jeden <local> Hostnamen, der keinen Zeitraum enthält.

WinINet umgeht standardmäßig den Proxy für Anforderungen, die die Hostnamen "localhost", "loopback", "127.0.0.1" oder \[ "::1" \] verwenden. Dieses Verhalten tritt auf, da ein Remoteproxyserver diese Adressen in der Regel nicht ordnungsgemäß auflöset.

**Internet Explorer 9:** Sie können den lokalen Computer mithilfe des Makros "<-loopback>" aus der Proxyumgehungsliste entfernen.

Das folgende Beispiel zeigt Beispielaufrufe von [**InternetOpen mithilfe**](/windows/desktop/api/Wininet/nf-wininet-internetopena) verschiedener Proxyumgehungszeichenfolgen. In den Kommentaren über jedem Aufruf wird beschrieben, welche Auswirkungen die Umgehungszeichenfolge auf die Hostnamen hat, auf die über das [**von ihr erstellte HINTERNET-Handle**](appendix-a-hinternet-handles.md) zugegriffen wird.


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

Um eine Sitzung zu starten, muss die [**InternetConnect-Funktion**](/windows/desktop/api/Wininet/nf-wininet-internetconnecta) ein Handle aus dem stamm-Handle erstellen, das von der [**InternetOpen-Funktion zurückgegeben**](/windows/desktop/api/Wininet/nf-wininet-internetopena) wird. [**InternetConnect**](/windows/desktop/api/Wininet/nf-wininet-internetconnecta) legt die Serveradresse, Die Portnummer, den Benutzernamen, das Kennwort und den Diensttyp fest.

[**InternetConnect**](/windows/desktop/api/Wininet/nf-wininet-internetconnecta) verwendet das von [**InternetOpen**](/windows/desktop/api/Wininet/nf-wininet-internetopena) erstellte [**HINTERNET-Stammhand**](appendix-a-hinternet-handles.md) handle, um ein Sitzungshand handle zu erstellen. Wenn das [INTERNET \_ FLAG \_ ASYNC-Flag](api-flags.md) im Aufruf von [**InternetOpen**](/windows/desktop/api/Wininet/nf-wininet-internetopena)festgelegt wurde, sollte der Aufruf von [**InternetConnect**](/windows/desktop/api/Wininet/nf-wininet-internetconnecta) einen Kontextwert ungleich 0 (null) enthalten.

Der Servername kann entweder den Hostnamen (z. B. "www.servername.com") oder die IP-Nummer der Website im ASCII-Dezimalformat (z. B. "10.0.1.45") enthalten.

Der Serverport ist die TCP/IP-Portnummer (Transmission Control Protocol/Internet Protocol), mit der eine Verbindung auf dem Server hergestellt werden soll. [**InternetConnect**](/windows/desktop/api/Wininet/nf-wininet-internetconnecta) verwendet den Standardport für den ausgewählten Diensttyp, wenn der Wert INTERNET \_ INVALID PORT NUMBER verwendet \_ \_ wird. Die folgenden Tabellen enthalten die Serverport-Standardwerte für WinINet.



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
<td>Verwenden Sie den Standardport für Gopherserver (Port 70).
<blockquote>
[!Note]<br />
Windows Xp und Windows Server 2003 R2 und früher.
</blockquote>
<br/></td>
</tr>
<tr class="odd">
<td>INTERNET_DEFAULT_HTTP_PORT</td>
<td>Verwenden Sie den Standardport für HTTP-Server (Port 80).</td>
</tr>
<tr class="even">
<td>INTERNET_DEFAULT_HTTPS_PORT</td>
<td>Verwenden Sie den Standardport für HTTPS-Server (Port 443).</td>
</tr>
<tr class="odd">
<td>INTERNET_DEFAULT_SOCKS_PORT</td>
<td>Verwenden Sie den Standardport für SOCKS-Firewallserver (Port 1080).</td>
</tr>
</tbody>
</table>



 

### <a name="defining-the-user-name-and-password"></a>Definieren von Benutzername und Kennwort

Der Wert von *lpszUsername* ist die Adresse einer mit **NULL** beendeten Zeichenfolge, die den Namen des Benutzers enthält, der sich anmelden möchte. Wenn dieser Parameter **NULL ist,** verwendet die Funktion einen entsprechenden Standardwert, mit Ausnahme von HTTP. Ein **NULL-Parameter** in HTTP bewirkt, dass der Server einen Fehler zurückgibt. Für das FTP-Protokoll ist der Standardwert anonym.

Der Wert von *lpszPassword* ist die Adresse einer mit **NULL** beendeten Zeichenfolge, die das Anmeldekennwort enthält. Wenn sowohl *lpszUsername als* auch *lpszPassword* **NULL sind,** verwendet die Funktion das anonyme Standardkennwort. Bei FTP ist das anonyme Standardkennwort der E-Mail-Name des Benutzers. Wenn *lpszUsername nicht* **NULL und** *lpszPassword* **NULL** ist, verwendet die Funktion ein leeres Kennwort. Es gibt vier mögliche Einstellungen für *lpszUsername* und *lpszPassword,* die die in der folgenden Tabelle gezeigten Verhaltensweisen erzeugen.



| *lpszUsername*      | *lpszPassword*      | An FTP-Server gesendeter Benutzername | An FTP-Server gesendetes Kennwort |
|---------------------|---------------------|------------------------------|-----------------------------|
| **NULL**            | **NULL**            | "anonym"                  | E-Mail-Name des Benutzers           |
| Zeichenfolge ungleich **NULL** | **NULL**            | *lpszUsername*               | ""                          |
| **NULL**            | Zeichenfolge ungleich **NULL** | ERROR                        | ERROR                       |
| Zeichenfolge ungleich **NULL** | Zeichenfolge ungleich **NULL** | *lpszUsername*               | *lpszPassword*              |



 

Diese Informationen können mithilfe der Funktionen [**InternetSetOption**](/windows/desktop/api/Wininet/nf-wininet-internetsetoptiona) und [**InternetErrorDlg**](/windows/desktop/api/Wininet/nf-wininet-interneterrordlg) geändert werden. [**InternetSetOption**](/windows/desktop/api/Wininet/nf-wininet-internetsetoptiona) ändert die Werte für Benutzername und Kennwort, während [**InternetErrorDlg**](/windows/desktop/api/Wininet/nf-wininet-interneterrordlg) ein Dialogfeld anzeigt, in dem der richtige Benutzername und das richtige Kennwort angefordert werden.

### <a name="defining-the-session"></a>Definieren der Sitzung

Legen Sie zum Definieren der Sitzung, die eingerichtet wird, den Diensttyp, die Flags und den Kontextwert für [**InternetConnect**](/windows/desktop/api/Wininet/nf-wininet-internetconnecta)fest.

Für [**InternetConnect**](/windows/desktop/api/Wininet/nf-wininet-internetconnecta)stehen zwei Diensttypen zur Verfügung: INTERNET \_ SERVICE FTP und INTERNET SERVICE \_ \_ \_ HTTP. INTERNET \_ SERVICE HTTP wird sowohl für \_ HTTP- als auch für HTTPS-Sitzungen verwendet.

[INTERNET \_ FLAG \_ PASSIVE](api-flags.md) ist das einzige dienstspezifische Flag, das von den WinINet-Funktionen verwendet wird. Dieses Flag kann festgelegt werden, wenn der Diensttyp INTERNET \_ SERVICE \_ FTP ist, um passive FTP-Semantik zu verwenden.

Für alle synchronen Vorgänge sollte der Wert von *dwContext* auf 0 (null) festgelegt werden. Wenn asynchrone Vorgänge durch Festlegen des [INTERNET \_ FLAG \_ ASYNC-Flags](api-flags.md) im Aufruf von [**InternetOpen**](/windows/desktop/api/Wininet/nf-wininet-internetopena)eingerichtet wurden, sollte für *dwContext* ein Wert ungleich 0 (null) angegeben werden. Weitere Informationen zu asynchronen Vorgängen finden Sie unter [Einrichten von asynchronen Vorgängen.](common-functions.md)

Bei FTP-Sitzungen versucht [**InternetConnect,**](/windows/desktop/api/Wininet/nf-wininet-internetconnecta) eine Verbindung mit dem Server im Internet herzustellen. Bei HTTP-Sitzungen stellt [**InternetConnect**](/windows/desktop/api/Wininet/nf-wininet-internetconnecta) erst dann eine Verbindung her, wenn eine andere Funktion versucht, Informationen vom Server abzurufen.

> [!Note]  
> WinINet unterstützt keine Serverimplementierungen. Darüber hinaus sollte sie nicht von einem Dienst verwendet werden. Verwenden Sie für Serverimplementierungen oder -dienste [Microsoft Windows HTTP-Dienste (WinHTTP).](/windows/desktop/WinHttp/winhttp-start-page)

 

 

