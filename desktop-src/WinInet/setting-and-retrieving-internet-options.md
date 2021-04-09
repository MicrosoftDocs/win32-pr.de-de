---
title: Festlegen und Abrufen von Internet Optionen
description: In diesem Thema wird beschrieben, wie Internet Optionen mithilfe der Funktionen InternetSetOption und InternetQueryOption festgelegt und abgerufen werden.
ms.assetid: b596a4a9-c34a-402a-af76-b930fe5f0901
keywords:
- Festlegen und Abrufen von Internet Optionen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 418bf21620cf7b7c4426844c95a39ef1fde04e11
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "103858409"
---
# <a name="setting-and-retrieving-internet-options"></a>Festlegen und Abrufen von Internet Optionen

In diesem Thema wird beschrieben, wie Internet Optionen mithilfe der Funktionen [**InternetSetOption**](/windows/desktop/api/Wininet/nf-wininet-internetsetoptiona) und [**InternetQueryOption**](/windows/desktop/api/Wininet/nf-wininet-internetqueryoptiona) festgelegt und abgerufen werden.

Internet Optionen können mit einem angegebenen [**hinternethandle**](appendix-a-hinternet-handles.md) oder den aktuellen Einstellungen in Microsoft Internet Explorer festgelegt oder abgerufen werden.

-   [Implementierungs Schritte](#implementation-steps)
    -   [Auswählen von Internet Optionen](#choosing-internet-options)
    -   [Auswählen des HINTERNET-Handles](#choosing-the-hinternet-handle)
    -   [Festlegen oder Abrufen der Optionen](#setting-or-retrieving-the-options)
-   [Bereich des hinternethandles](#scope-of-hinternet-handle)
-   [Festlegen einzelner Optionen](#setting-individual-options)
-   [Abrufen einzelner Optionen](#retrieving-individual-options)
    -   [Beispiel zum Vervollständigen](#complete-sample)
-   [Festlegen von Verbindungsoptionen](#setting-connection-options)
-   [Abrufen von Verbindungsoptionen](#retrieving-connection-options)
-   [Zugehörige Themen](#related-topics)

## <a name="implementation-steps"></a>Implementierungs Schritte

Um Internet Optionen festzulegen oder abzurufen, führen Sie die folgenden Schritte aus:

-   [Auswählen von Internet Optionen](#choosing-internet-options)
-   [Auswählen des HINTERNET-Handles](#choosing-the-hinternet-handle)
-   [Festlegen oder Abrufen der Optionen](#setting-or-retrieving-the-options)

### <a name="choosing-internet-options"></a>Auswählen von Internet Optionen

Da es so viele Internet Optionen gibt, ist es wichtig, die richtigen Optionen auszuwählen. Viele Internetoptionen wirken sich auf das Verhalten der WinInet-Funktionen und Internet Explorer aus:

Beispielsweise können Sie folgende Aktionen ausführen:

-   Behandeln Sie die grundlegende Server-und Proxy Authentifizierung durch Festlegen von Benutzernamen und Kenn Wörtern.
-   Legen Sie die Benutzer-Agent-Zeichenfolge fest, die von Servern verwendet wird, um die Funktionen der Client Anwendung oder des Browsers zu identifizieren.
-   Ruft den Handlertyp des angegebenen [**HINTERNET**](appendix-a-hinternet-handles.md) -Handles ab.

Weitere Informationen und eine Liste der Internet Optionen finden Sie unter [**Optionsflags**](option-flags.md).

In Internet Explorer 5 und höher können einige Optionen über eine bestimmte Internetverbindung festgelegt oder abgerufen werden, indem die options [**Liste "Internet \_ pro \_ conn \_ \_**](/windows/desktop/api/Wininet/ns-wininet-internet_per_conn_option_lista) " und die Optionen " [**Internet \_ pro \_ \_**](/windows/desktop/api/Wininet/ns-wininet-internet_per_conn_optiona) conn" verwendet werden. Weitere Informationen und eine Liste der Optionen, die von einer bestimmten Internet Verbindung festgelegt oder abgerufen werden können, finden Sie unter dem **dwOptions** -Member der [**Option "Internet \_ pro \_ conn \_**](/windows/desktop/api/Wininet/ns-wininet-internet_per_conn_optiona) ".

### <a name="choosing-the-hinternet-handle"></a>Auswählen des HINTERNET-Handles

Das [**HINTERNET**](appendix-a-hinternet-handles.md) -handle, das zum Festlegen oder Abrufen von Internet Optionen verwendet wird, bestimmt den Gültigkeitsbereich des Vorgangs. Alle Handles, die über diesen Handle erstellt werden, erben die für dieses Handle festgelegten Optionen.

Beispielsweise müssen Client Anwendungen, die einen Proxy mit Authentifizierung erfordern, wahrscheinlich nicht jedes Mal, wenn die Anwendung versucht, auf eine Internet Ressource zuzugreifen, den Proxy Benutzernamen und das Kennwort festlegen. Wenn alle Anforderungen für eine bestimmte Verbindung vom gleichen Proxy verarbeitet werden und der Proxy Benutzername und das Kennwort für einen Verbindungstyp des [**hinternethandles**](appendix-a-hinternet-handles.md) festgelegt werden, d. h. ein Handle, das durch einen Aufruf von [**InternetConnect**](/windows/desktop/api/Wininet/nf-wininet-internetconnecta)erstellt wurde, können alle Aufrufe, die von diesem **HINTERNET** handle abgeleitet sind, denselben Proxy Benutzernamen und dasselbe Kennwort verwenden. Wenn Sie den Proxy Benutzernamen und das Kennwort jedes Mal festlegen, wenn ein **hinternethandle** von [**HttpOpenRequest**](/windows/desktop/api/Wininet/nf-wininet-httpopenrequesta) erstellt wird, ist zusätzlicher und unnötiger Verwaltungsaufwand erforderlich. Beachten Sie, dass bei Verwendung eines Proxys, für den eine Authentifizierung erforderlich ist, die Proxy Anmelde Informationen für jede neue Verbindung festgelegt werden müssen.

### <a name="setting-or-retrieving-the-options"></a>Festlegen oder Abrufen der Optionen

Wenn Sie ermittelt haben, welche Internetoptionen und welches [**hinternethandle**](appendix-a-hinternet-handles.md) verwendet werden sollen, rufen Sie diese Internetoptionen ab. Um Optionen festzulegen oder abzurufen, rufen Sie entweder [**InternetQueryOption**](/windows/desktop/api/Wininet/nf-wininet-internetqueryoptiona) oder [**InternetSetOption**](/windows/desktop/api/Wininet/nf-wininet-internetsetoptiona)auf.

## <a name="scope-of-hinternet-handle"></a>Bereich des hinternethandles

Das [**hinternethandle**](appendix-a-hinternet-handles.md) , mit dem Internet Optionen festgelegt oder abgerufen werden, bestimmt die Aktionen, für die die Optionen gültig sind.

Diese Handles haben drei Ebenen:

-   Das [**HINTERNET**](appendix-a-hinternet-handles.md) -Stamm handle (das durch einen [**Internet Open**](/windows/desktop/api/Wininet/nf-wininet-internetopena)-Rückruf erstellt wurde) würde alle Internet Optionen enthalten, die diese Instanz von WinInet betreffen.
-   [**HINTERNET**](appendix-a-hinternet-handles.md) Handles, die eine Verbindung mit einem Server herstellen (durch einen [**Internet Verbindungs**](/windows/desktop/api/Wininet/nf-wininet-internetconnecta)Gespräch erstellt)
-   [**Hinternethandles**](appendix-a-hinternet-handles.md) , die einer Ressource oder einer Enumeration von Ressourcen auf einem bestimmten Server zugeordnet sind.

Zusätzlich zu den verschiedenen [**HINTERNET**](appendix-a-hinternet-handles.md) -Handles kann eine Anwendung auch **null** verwenden, um die Standardwerte der Internetoptionen, die von Internet Explorer und den WinInet-Funktionen verwendet werden, festzulegen oder abzurufen. Wenn Sie beim Verwenden von **null** als handle Internet Optionen festlegen, werden die Standardwerte der Optionen geändert, die derzeit in der Registrierung gespeichert sind. Client Anwendungen sollten keine Registrierungsfunktionen verwenden, um die Standardwerte der Internet Optionen zu ändern, da die Implementierung der gespeicherten Optionen in Zukunft geändert werden kann.

In der folgenden Tabelle sind die Typen der [**hinternethandles**](appendix-a-hinternet-handles.md) und der Bereich der Ihnen zugeordneten Internet Optionen aufgeführt.



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th>Handle-Typ</th>
<th>Bereich</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><strong>NULL</strong></td>
<td>Die Standard Options Einstellungen für Internet Explorer.</td>
</tr>
<tr class="even">
<td>INTERNET_HANDLE_TYPE_CONNECT_FTP</td>
<td>Die Options Einstellungen für diese Verbindung mit einem FTP-Server. Diese Optionen wirken sich auf alle von diesem <a href="appendix-a-hinternet-handles.md"><strong>hinternethandle</strong></a> initiierten Vorgänge aus, z. b. Dateidownloads.</td>
</tr>
<tr class="odd">
<td>INTERNET_HANDLE_TYPE_CONNECT_GOPHER</td>
<td>Die Options Einstellungen für diese Verbindung mit einem Gopher-Server. Diese Optionen wirken sich auf alle von diesem <a href="appendix-a-hinternet-handles.md"><strong>hinternethandle</strong></a> initiierten Vorgänge aus, z. b. Dateidownloads.
<blockquote>
[!Note]<br />
Nur Windows XP und Windows Server 2003 R2 und früher.
</blockquote>
<br/></td>
</tr>
<tr class="even">
<td>INTERNET_HANDLE_TYPE_CONNECT_HTTP</td>
<td>Die Options Einstellungen für diese Verbindung mit einem HTTP-Server. Diese Optionen wirken sich auf alle von diesem <a href="appendix-a-hinternet-handles.md"><strong>hinternethandle</strong></a> initiierten Vorgänge aus, z. b. Dateidownloads.</td>
</tr>
<tr class="odd">
<td>INTERNET_HANDLE_TYPE_FILE_REQUEST</td>
<td>Die Options Einstellungen, die dieser Datei Anforderung zugeordnet sind.</td>
</tr>
<tr class="even">
<td>INTERNET_HANDLE_TYPE_FTP_FILE</td>
<td>Die Options Einstellungen, die mit diesem FTP-Ressourcen Download verknüpft sind.</td>
</tr>
<tr class="odd">
<td>INTERNET_HANDLE_TYPE_FTP_FILE_HTML</td>
<td>Die Options Einstellungen, die diesem FTP-Ressourcen Download zugeordnet sind, sind in HTML formatiert.</td>
</tr>
<tr class="even">
<td>INTERNET_HANDLE_TYPE_FTP_FIND</td>
<td>Die Options Einstellungen, die dieser Suche nach Dateien auf einem FTP-Server zugeordnet sind.</td>
</tr>
<tr class="odd">
<td>INTERNET_HANDLE_TYPE_FTP_FIND_HTML</td>
<td>Die Options Einstellungen, die dieser Suche nach Dateien auf einem FTP-Server zugeordnet sind, die in HTML formatiert sind.</td>
</tr>
<tr class="even">
<td>INTERNET_HANDLE_TYPE_GOPHER_FILE</td>
<td>Die Options Einstellungen, die diesem Gopher-Ressourcen Download zugeordnet sind.
<blockquote>
[!Note]<br />
Nur Windows XP und Windows Server 2003 R2 und früher.
</blockquote>
<br/></td>
</tr>
<tr class="odd">
<td>INTERNET_HANDLE_TYPE_GOPHER_FILE_HTML</td>
<td>Die Options Einstellungen, die diesem Gopher-Ressourcen Download zugeordnet sind, sind in HTML formatiert.
<blockquote>
[!Note]<br />
Nur Windows XP und Windows Server 2003 R2 und früher.
</blockquote>
<br/></td>
</tr>
<tr class="even">
<td>INTERNET_HANDLE_TYPE_GOPHER_FIND</td>
<td>Die Options Einstellungen, die dieser Suche nach Dateien auf einem Gopher-Server zugeordnet sind.
<blockquote>
[!Note]<br />
Nur Windows XP und Windows Server 2003 R2 und früher.
</blockquote>
<br/></td>
</tr>
<tr class="odd">
<td>INTERNET_HANDLE_TYPE_GOPHER_FIND_HTML</td>
<td>Die Options Einstellungen, die dieser Suche nach Dateien auf einem Gopher-Server zugeordnet sind, der in HTML formatiert ist.
<blockquote>
[!Note]<br />
Nur Windows XP und Windows Server 2003 R2 und früher.
</blockquote>
<br/></td>
</tr>
<tr class="even">
<td>INTERNET_HANDLE_TYPE_HTTP_REQUEST</td>
<td>Die Options Einstellungen, die dieser HTTP-Anforderung zugeordnet sind.</td>
</tr>
<tr class="odd">
<td>INTERNET_HANDLE_TYPE_INTERNET</td>
<td>Die Options Einstellungen, die dieser Instanz der WinInet-Funktionen zugeordnet sind.</td>
</tr>
</tbody>
</table>



 

## <a name="setting-individual-options"></a>Festlegen einzelner Optionen

Nachdem Sie die Internetoptionen festgelegt haben, die Sie festlegen möchten, und den von diesen Optionen betroffenen Bereich festlegen, ist das Festlegen von Internetoptionen nicht kompliziert. Sie müssen lediglich die [**InternetSetOption**](/windows/desktop/api/Wininet/nf-wininet-internetsetoptiona) -Funktion mit dem gewünschten [**HINTERNET**](appendix-a-hinternet-handles.md) handle, dem Internet Optionsflag und einem Puffer, der die Informationen enthält, die Sie festlegen möchten, abrufen.

Im folgenden Beispiel wird gezeigt, wie der Proxy Benutzername und das Kennwort für ein angegebenes [**HINTERNET**](appendix-a-hinternet-handles.md) -handle festgelegt werden.


```C++
// strUsername is a string buffer of cchMax characters or less.
// It contains the proxy user name.
size_t cchMax = 80;
size_t cchUserLength, cchPasswordLength;
HRESULT hr = StringCchLength(strUsername, cchMax, &cchUserLength);

if (SUCCEEDED(hr))
{
   // hOpen is the HINTERNET handle created by InternetConnect.
   InternetSetOption(hConnect, INTERNET_OPTION_PROXY_USERNAME,
      strUsername, DWORD(cchUserLength)+1);
}
else
{
   // Insert error handling code here.
}

// strPassword is the string buffer that contains the proxy password.
hr = StringCchLength(strPassword, cchMax, &cchPasswordLength);

InternetSetOption(hOpen, INTERNET_OPTION_PROXY_PASSWORD,
    strPassword, DWORD(cchPasswordLength)+1);
```



## <a name="retrieving-individual-options"></a>Abrufen einzelner Optionen

Internet Optionen können mithilfe der [**InternetQueryOption**](/windows/desktop/api/Wininet/nf-wininet-internetqueryoptiona) -Funktion abgerufen werden. So rufen Sie Internet Optionen ab:

1.  Bestimmen Sie die Puffergröße, die zum Abrufen der Internet Options Informationen erforderlich ist.

    Die Puffergröße kann ermittelt werden, indem für die Adresse des Puffers **null** verwendet und eine Puffergröße von NULL übergeben wird.

    ```C++
    DWORD dwSize;
    InternetQueryOption(NULL, INTERNET_OPTION_USER_AGENT, NULL, &dwSize);
    ```

    

    Der von [**InternetQueryOption**](/windows/desktop/api/Wininet/nf-wininet-internetqueryoptiona) zurückgegebene Wert ist die Menge an Arbeitsspeicher, die zum Abrufen der Informationen benötigt wird (in Bytes).

2.  Zuordnen eines Speichers für den Puffer.
    ```C++
    char *lpszData;
    lpszData = new char[dwSize];
    ```

    

3.  Rufen Sie die Daten ab.
    ```C++
    InternetQueryOption( NULL, 
                         INTERNET_OPTION_USER_AGENT,
                         lpszData, &dwSize );
    ```

    

4.  Freigeben des Speichers.
    ```C++
    delete [] lpszData;
    ```

    

### <a name="complete-sample"></a>Beispiel zum Vervollständigen

Im folgenden finden Sie das gesamte Beispiel, das im vorherigen Abschnitt verwendet wurde. Dieses Beispiel zeigt, wie die standardmäßige Benutzer-Agent-Zeichenfolge abgerufen wird.


```C++
// This call determines the required buffer size.
DWORD dwSize;
InternetQueryOption(NULL, INTERNET_OPTION_USER_AGENT, NULL, &dwSize);

// Allocate the necessary memory.
char *lpszData;
lpszData = new char[dwSize];

// Call InternetQueryOption again with the provided buffer.
InternetQueryOption( NULL, 
                     INTERNET_OPTION_USER_AGENT,
                     lpszData, &dwSize );

// Insert code here to use the user agent string data.

// Free the allocated memory.
delete [] lpszData;
```



## <a name="setting-connection-options"></a>Festlegen von Verbindungsoptionen

In Internet Explorer 5 und höher können Internetoptionen für eine bestimmte Verbindung auf festgelegt werden. Zuvor wurden für alle Verbindungen dieselben Internet Options Einstellungen verwendet. So legen Sie Optionen für eine bestimmte Verbindung fest:

1.  Erstellen Sie [**eine \_ \_ \_ options \_ Listenstruktur für das Internet pro Conn**](/windows/desktop/api/Wininet/ns-wininet-internet_per_conn_option_lista) .
2.  Weisen Sie den Arbeitsspeicher für die einzelnen Internet Optionen zu, die Sie für die Verbindung festlegen möchten.
3.  Legen Sie die Optionen im [**Internet \_ pro Conn- \_ \_ options**](/windows/desktop/api/Wininet/ns-wininet-internet_per_conn_optiona) Strukturen fest.
4.  Legen Sie die Optionen mithilfe von [**internettoption**](/windows/desktop/api/Wininet/nf-wininet-internetsetoptiona)fest.

Im folgenden Codebeispiel wird gezeigt, wie Proxy Daten für eine LAN-Verbindung festgelegt werden.


```C++
BOOL SetConnectionOptions()
{
    INTERNET_PER_CONN_OPTION_LIST list;
    BOOL    bReturn;
    DWORD   dwBufSize = sizeof(list);

    // Fill the list structure.
    list.dwSize = sizeof(list);

    // NULL == LAN, otherwise connectoid name.
    list.pszConnection = NULL;

    // Set three options.
    list.dwOptionCount = 3;
    list.pOptions = new INTERNET_PER_CONN_OPTION[3];

    // Ensure that the memory was allocated.
    if(NULL == list.pOptions)
    {
        // Return FALSE if the memory wasn't allocated.
        return FALSE;
    }

    // Set flags.
    list.pOptions[0].dwOption = INTERNET_PER_CONN_FLAGS;
    list.pOptions[0].Value.dwValue = PROXY_TYPE_DIRECT |
        PROXY_TYPE_PROXY;

    // Set proxy name.
    list.pOptions[1].dwOption = INTERNET_PER_CONN_PROXY_SERVER;
    list.pOptions[1].Value.pszValue = TEXT("https://proxy:80");

    // Set proxy override.
    list.pOptions[2].dwOption = INTERNET_PER_CONN_PROXY_BYPASS;
    list.pOptions[2].Value.pszValue = TEXT("local");

    // Set the options on the connection.
    bReturn = InternetSetOption(NULL,
        INTERNET_OPTION_PER_CONNECTION_OPTION, &list, dwBufSize);

    // Free the allocated memory.
    delete [] list.pOptions;

    return bReturn;
}
```



## <a name="retrieving-connection-options"></a>Abrufen von Verbindungsoptionen

In Internet Explorer 5 und höher können Internetoptionen über eine bestimmte Verbindung abgerufen werden. So rufen Sie Optionen von einer bestimmten Verbindung ab

1.  Erstellen Sie [**eine \_ \_ \_ options \_ Listenstruktur für das Internet pro Conn**](/windows/desktop/api/Wininet/ns-wininet-internet_per_conn_option_lista) .
2.  Weisen Sie den Arbeitsspeicher für die einzelnen Internet Optionen zu, die von der Verbindung abgerufen werden sollen.
3.  Geben Sie die Optionen mithilfe der Optionen [**Internet \_ pro \_ conn- \_ Option**](/windows/desktop/api/Wininet/ns-wininet-internet_per_conn_optiona) an.
4.  Rufen Sie die Optionen mithilfe von [**InternetQueryOption**](/windows/desktop/api/Wininet/nf-wininet-internetqueryoptiona)ab.
5.  Verwenden Sie die Option Data.
6.  Verwenden Sie die [**GlobalFree**](/windows/desktop/api/winbase/nf-winbase-globalfree) -Funktion, um den Arbeitsspeicher freizugeben, der den Options Daten zugeordnet ist.

> [!Note]  
> WinInet unterstützt keine Server Implementierungen. Außerdem sollte Sie nicht von einem Dienst verwendet werden. Verwenden Sie für Server Implementierungen oder-Dienste [Microsoft Windows HTTP-Dienste (WinHTTP)](/windows/desktop/WinHttp/winhttp-start-page).

 

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Behandeln der Authentifizierung](handling-authentication.md)
</dt> <dt>

[HINTERNET-Handles](appendix-a-hinternet-handles.md)
</dt> </dl>

 

