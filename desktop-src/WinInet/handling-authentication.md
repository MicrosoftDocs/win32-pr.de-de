---
title: Behandeln der Authentifizierung
description: Einige Proxys und Server erfordern eine Authentifizierung, bevor sie Zugriff auf Ressourcen im Internet gewähren.
ms.assetid: f3752031-30d3-4e35-8eae-1d4971b66bc2
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1797f34eb4f25f8d5e345b6790489acd5fad7e2bc21e6457642a1b4ffa022f9b
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118113829"
---
# <a name="handling-authentication"></a>Behandeln der Authentifizierung

Einige Proxys und Server erfordern eine Authentifizierung, bevor sie Zugriff auf Ressourcen im Internet gewähren. Die WinINet-Funktionen unterstützen die Server- und Proxyauthentifizierung für HTTP-Sitzungen. Die Authentifizierung von FTP-Servern muss von der [**InternetConnect-Funktion**](/windows/desktop/api/Wininet/nf-wininet-internetconnecta) durchgeführt werden. Derzeit wird die FTP-Gatewayauthentifizierung nicht unterstützt.

## <a name="about-http-authentication"></a>Informationen zur HTTP-Authentifizierung

Wenn eine Authentifizierung erforderlich ist, erhält die Clientanwendung den Statuscode 401, wenn der Server eine Authentifizierung erfordert, oder 407, wenn der Proxy eine Authentifizierung erfordert. Mit dem Statuscode sendet der Proxy oder Server mindestens einen Antwortheader: Proxyauthentifizierung (für Proxyauthentifizierung) oder WWW-Authenticate (für Serverauthentifizierung).

Jeder Authentifizierungsantwortheader enthält ein verfügbares Authentifizierungsschema und einen Bereich. Wenn mehrere Authentifizierungsschemas unterstützt werden, gibt der Server mehrere Authentifizierungsantwortheader zurück. Beim Bereichswert wird die Groß-/Kleinschreibung beachtet, und es wird ein Schutzbereich auf dem Proxy oder Server definiert. Beispielsweise wäre der Header "WWW-Authenticate: Basic Realm="example" ein Beispiel für einen Header, der zurückgegeben wird, wenn eine Serverauthentifizierung erforderlich ist.

Die Clientanwendung, die die Anforderung gesendet hat, kann sich authentifizieren, indem sie ein Autorisierungsheaderfeld in die Anforderung einschließt. Der Autorisierungsheader würde das Authentifizierungsschema und die entsprechende Antwort enthalten, die für dieses Schema erforderlich ist. Beispielsweise würde der Header "Authorization: Basic \<username:password> " der Anforderung hinzugefügt und erneut an den Server gesendet, wenn der Client den Authentifizierungsantwortheader "WWW-Authenticate: Basic Realm="example" erhalten hat.

Es gibt zwei allgemeine Arten von Authentifizierungsschemas:

-   Standardauthentifizierungsschema, bei dem Benutzername und Kennwort als Klartext an den Server gesendet werden.
-   Abfrage-/Antwortschemas, die ein Abfrage-Antwort-Format ermöglichen.

Das Standardauthentifizierungsschema basiert auf dem Modell, das ein Client sich mit einem Benutzernamen und kennwort für jeden Bereich authentifizieren muss. Der Server wartet die Anforderung, wenn sie erneut mit einem Autorisierungsheader gesendet wird, der einen gültigen Benutzernamen und ein gültiges Kennwort enthält.

Abfrage-/Antwortschemas ermöglichen eine sicherere Authentifizierung. Wenn eine Anforderung eine Authentifizierung mithilfe eines Abfrage-/Antwortschemas erfordert, werden der entsprechende Statuscode und die Authenticate-Header an den Client zurückgegeben. Der Client muss dann die Anforderung mit einer Aushandlung erneut senden. Der Server gibt einen entsprechenden Statuscode mit einer Abfrage zurück, und der Client müsste die Anforderung dann mit der richtigen Antwort erneut senden, um den angeforderten Dienst abzurufen.

In der folgenden Tabelle sind die Authentifizierungsschemas, der Authentifizierungstyp, die DLL, die sie unterstützt, und eine Beschreibung des Schemas aufgeführt.



| Schema                                    | Typ               | DLL                  | Beschreibung                                                                                                                                                                                                                                                                                                                                        |
|-------------------------------------------|--------------------|----------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Basic (Klartext)                         | basic              | Wininet.dll          | Verwendet eine Base64-codierte Zeichenfolge, die den Benutzernamen und das Kennwort enthält.                                                                                                                                                                                                                                                                             |
| Digest                                    | Challenge-Response | Digest.dll           | Ein Abfrage-Antwort-Schema, das die Verwendung eines Nonce-Werts (einer vom Server angegebenen Datenzeichenfolge) in Frage stellt. Eine gültige Antwort enthält eine Prüfsumme des Benutzernamens, des Kennworts, des angegebenen Nonce-Werts, der HTTP-Methode und des angeforderten Uniform Resource Identifier (URI). Die Unterstützung der Digestauthentifizierung wurde in Microsoft Internet Explorer 5 eingeführt. |
| NT LAN-Manager (NTLM)                     | Challenge-Response | Winsspi.dll          | Ein Abfrage-Antwort-Schema, das die Abfrage auf dem Benutzernamen basiert.                                                                                                                                                                                                                                                                             |
| Microsoft Network (MSN)                   | Challenge-Response | Msnsspc.dll          | das Authentifizierungsschema The Microsoft Network.                                                                                                                                                                                                                                                                                                     |
| Verteilte Kennwortauthentifizierung (Distributed Password Authentication, DPA) | Challenge-Response | Msapsspc.dll         | Ähnlich wie die MSN-Authentifizierung und wird auch vom Microsoft-Netzwerk verwendet.                                                                                                                                                                                                                                                                           |
| Remotepassphrase-Authentifizierung (RPA)    | Compuserve         | Rpawinet.dll, da.dll | CompuServe-Authentifizierungsschema. Weitere Informationen finden Sie in den [RPA-Mechanismusspezifikationen.](https://www.compuserve.com/)                                                                                                                                                                                                    |



 

Für andere Zwecke als die Standardauthentifizierung müssen die Registrierungsschlüssel zusätzlich zur Installation der entsprechenden DLL eingerichtet werden.

Wenn eine Authentifizierung erforderlich ist, sollte das [INTERNET \_ FLAG KEEP \_ \_ CONNECTION-Flag](api-flags.md) beim Aufruf von [**HttpOpenRequest**](/windows/desktop/api/Wininet/nf-wininet-httpopenrequesta)verwendet werden. Das FLAG INTERNET \_ FLAG KEEP CONNECTION ist für \_ \_ NTLM und andere Authentifizierungstypen erforderlich, um die Verbindung beim Abschließen des Authentifizierungsprozesses beizubehalten. Wenn die Verbindung nicht beibehalten wird, muss der Authentifizierungsprozess mit dem Proxy oder Server neu gestartet werden.

Die Funktionen [**InternetOpenUrl**](/windows/desktop/api/Wininet/nf-wininet-internetopenurla) und [**HttpSendRequest**](/windows/desktop/api/Wininet/nf-wininet-httpsendrequesta) werden auch dann erfolgreich abgeschlossen, wenn eine Authentifizierung erforderlich ist. Der Unterschied besteht darin, dass die in den Headerdateien und [**InternetReadFile**](/windows/desktop/api/Wininet/nf-wininet-internetreadfile) zurückgegebenen Daten eine HTML-Seite erhalten, die den Benutzer über den Statuscode informiert.

### <a name="registering-authentication-keys"></a>Registrieren von Authentifizierungsschlüsseln

INTERNET \_ OPEN \_ TYPE \_ PRECONFIG untersucht die Registrierungswerte **ProxyEnable**, **ProxyServer** und **ProxyOverride**. Diese Werte befinden sich unter **HKEY \_ CURRENT \_ USER** \\ **Software** \\ **Microsoft** \\ **Windows** \\ **CurrentVersion** Internet \\ **Einstellungen**.

Für andere Authentifizierungsschemas als Basic muss der Registrierung unter **HKEY \_ LOCAL \_ MACHINE** SOFTWARE Microsoft Internet Explorer Security ein Schlüssel hinzugefügt \\  \\  \\  \\ werden. Der **DWORD-Wert** **Flags** sollte mit dem entsprechenden Wert festgelegt werden. Die folgende Liste zeigt die möglichen Werte für den **Flags-Wert.**

-   PLUGIN \_ AUTH \_ FLAGS \_ UNIQUE CONTEXT PER \_ \_ \_ TCPIP (value=0x01)

    Jeder TCP/IP-Socket (Transmission Control Protocol/Internet Protocol) enthält einen anderen Kontext. Andernfalls wird ein neuer Kontext für jede Bereichs- oder Block-URL-Vorlage übergeben.

-   PLUGIN \_ AUTH \_ FLAGS \_ CAN HANDLE UI \_ \_ (value=0x02)

    Diese DLL kann ihre eigenen Benutzereingaben verarbeiten.

-   PLUGIN \_ AUTH \_ FLAGS \_ CAN HANDLE \_ \_ NO \_ PASSWD (value=0x04) (PLUG-IN-AUTHENTIFIZIERUNGSFLAGS KÖNNEN KEIN PASSWD VERARBEITEN (value=0x04)

    Diese DLL kann eine Authentifizierung durchführen, ohne den Benutzer zur Eingabe eines Kennworts aufzufordern.

-   PLUGIN \_ AUTH \_ FLAGS \_ NO REALM \_ (value=0x08)

    Diese DLL verwendet keine standardmäßige HTTP-Bereichszeichenfolge. Alle Daten, die ein Bereich zu sein scheinen, sind schemaspezifische Daten.

-   \_PLUG-IN-AUTHENTIFIZIERUNGSFLAGS \_ KEEP ALIVE NOT REQUIRED \_ \_ \_ \_ (value=0x10)

    Diese DLL erfordert keine permanente Verbindung für ihre Abfrage-/Antwortsequenz.

Um z. B. die NTLM-Authentifizierung hinzuzufügen, muss der Schlüssel NTLM **HKEY \_ LOCAL \_ MACHINE** SOFTWARE Microsoft Internet Explorer Security hinzugefügt \\  \\  \\  \\ werden. Unter **HKEY \_ LOCAL \_ MACHINE** \\ **SOFTWARE** \\ **Microsoft** \\ **Internet Explorer** \\ **Security** \\ **NTLM** müssen der Zeichenfolgenwert **DLLFile** und der **DWORD-Wert** **Flags** hinzugefügt werden. **DLLFile** muss auf Winsspi.dll und **Flags** auf 0x08 festgelegt werden.

### <a name="server-authentication"></a>Serverauthentifizierung

Wenn ein Server eine Anforderung empfängt, die eine Authentifizierung erfordert, gibt der Server die Statuscodemeldung 401 zurück. In dieser Meldung sollte der Server mindestens einen WWW-Authenticate Antwortheader enthalten. Diese Header enthalten die Authentifizierungsmethoden, die der Server zur Verfügung hat. WinINet wählt die erste Methode aus, die es erkennt.

Die Standardauthentifizierung bietet schwache Sicherheit, es sei denn, der Kanal ist zuerst mit SSL oder PCT verknüpft.

Die [**InternetErrorDlg-Funktion**](/windows/desktop/api/Wininet/nf-wininet-interneterrordlg) kann verwendet werden, um die Benutzernamen- und Kennwortdaten vom Benutzer abzurufen, oder eine benutzerdefinierte Benutzeroberfläche kann zum Abrufen der Daten entworfen werden.

Eine benutzerdefinierte Schnittstelle kann die [**InternetSetOption-Funktion**](/windows/desktop/api/Wininet/nf-wininet-internetsetoptiona) verwenden, um die Werte [INTERNET OPTION \_ \_ PASSWORD](option-flags.md) und [INTERNET OPTION \_ \_ USERNAME](option-flags.md) festzulegen und die Anforderung dann erneut an den Server zu senden.

### <a name="proxy-authentication"></a>Proxyauthentifizierung

Wenn ein Client versucht, einen Proxy zu verwenden, der eine Authentifizierung erfordert, gibt der Proxy eine 407-Statuscodemeldung an den Client zurück. In dieser Nachricht sollte der Proxy mindestens einen Proxy-Authenticate Antwortheader enthalten. Diese Header enthalten die Authentifizierungsmethoden, die über den Proxy verfügbar sind. WinINet wählt die erste Methode aus, die es erkennt.

Die [**InternetErrorDlg-Funktion**](/windows/desktop/api/Wininet/nf-wininet-interneterrordlg) kann verwendet werden, um die Benutzernamen- und Kennwortdaten vom Benutzer abzurufen, oder eine benutzerdefinierte Benutzeroberfläche kann entworfen werden.

Eine benutzerdefinierte Schnittstelle kann die [**InternetSetOption-Funktion**](/windows/desktop/api/Wininet/nf-wininet-internetsetoptiona) verwenden, um die Werte [INTERNET OPTION PROXY \_ \_ \_ PASSWORD](option-flags.md) und [INTERNET OPTION PROXY \_ \_ \_ USERNAME](option-flags.md) festzulegen und dann die Anforderung erneut an den Proxy zu senden.

Wenn kein Proxybenutzername und kein Kennwort festgelegt sind, versucht WinINet, den Benutzernamen und das Kennwort für den Server zu verwenden. Durch dieses Verhalten können Clients dieselbe benutzerdefinierte Benutzeroberfläche implementieren, die auch für die Serverauthentifizierung verwendet wird.

## <a name="handling-http-authentication"></a>Behandeln der HTTP-Authentifizierung

Die HTTP-Authentifizierung kann entweder mit [**InternetErrorDlg**](/windows/desktop/api/Wininet/nf-wininet-interneterrordlg) oder einer benutzerdefinierten Funktion verarbeitet werden, die [**InternetSetOption**](/windows/desktop/api/Wininet/nf-wininet-internetsetoptiona) verwendet oder eigene Authentifizierungsheader hinzufügt. [**InternetErrorDlg kann**](/windows/desktop/api/Wininet/nf-wininet-interneterrordlg) die einem [**HINTERNET-Handle**](appendix-a-hinternet-handles.md) zugeordneten Header untersuchen, um ausgeblendete Fehler zu finden, z. B. Statuscodes von einem Proxy oder Server. [**InternetSetOption**](/windows/desktop/api/Wininet/nf-wininet-internetsetoptiona) kann verwendet werden, um den Benutzernamen und das Kennwort für den Proxy und den Server festzusetzen. Für die MSN- und DPA-Authentifizierung [**muss InternetErrorDlg**](/windows/desktop/api/Wininet/nf-wininet-interneterrordlg) zum Festlegen des Benutzernamens und Kennworts verwendet werden.

Für jede benutzerdefinierte Funktion, die eigene WWW-Authenticate- oder Proxy-Authenticate-Header hinzufügt, sollte das [FLAG INTERNET FLAG NO \_ \_ \_ AUTH](api-flags.md) festgelegt werden, um die Authentifizierung zu deaktivieren.

Das folgende Beispiel zeigt, wie [**InternetErrorDlg**](/windows/desktop/api/Wininet/nf-wininet-interneterrordlg) zur Behandlung der HTTP-Authentifizierung verwendet werden kann.


```C++
HINTERNET hOpenHandle,  hConnectHandle, hResourceHandle;
DWORD dwError, dwErrorCode;
HWND hwnd = GetConsoleWindow();

hOpenHandle = InternetOpen(TEXT("Example"),
                           INTERNET_OPEN_TYPE_PRECONFIG, 
                           NULL, NULL, 0);

hConnectHandle = InternetConnect(hOpenHandle,
                                 TEXT("www.server.com"), 
                                 INTERNET_INVALID_PORT_NUMBER,
                                 NULL,
                                 NULL, 
                                 INTERNET_SERVICE_HTTP,
                                 0,0);

hResourceHandle = HttpOpenRequest(hConnectHandle, TEXT("GET"),
                                  TEXT("/premium/default.htm"),
                                  NULL, NULL, NULL, 
                                  INTERNET_FLAG_KEEP_CONNECTION, 0);

resend:

HttpSendRequest(hResourceHandle, NULL, 0, NULL, 0);

// dwErrorCode stores the error code associated with the call to
// HttpSendRequest.  

dwErrorCode = hResourceHandle ? ERROR_SUCCESS : GetLastError();

dwError = InternetErrorDlg(hwnd, hResourceHandle, dwErrorCode, 
                           FLAGS_ERROR_UI_FILTER_FOR_ERRORS | 
                           FLAGS_ERROR_UI_FLAGS_CHANGE_OPTIONS |
                           FLAGS_ERROR_UI_FLAGS_GENERATE_DATA,
                           NULL);

if (dwError == ERROR_INTERNET_FORCE_RETRY)
    goto resend;

// Insert code to read the data from the hResourceHandle
// at this point.

```



Im Beispiel wird dwErrorCode verwendet, um fehler zu speichern, die dem Aufruf von [**HttpSendRequest zugeordnet sind.**](/windows/desktop/api/Wininet/nf-wininet-httpsendrequesta) [**HttpSendRequest**](/windows/desktop/api/Wininet/nf-wininet-httpsendrequesta) wird erfolgreich abgeschlossen, auch wenn der Proxy oder Server eine Authentifizierung erfordert. Wenn das FLAG FLAGS ERROR UI FILTER FOR ERRORS an \_ \_ \_ \_ \_ [**InternetErrorDlg**](/windows/desktop/api/Wininet/nf-wininet-interneterrordlg)übergeben wird, überprüft die Funktion die Header auf ausgeblendete Fehler. Diese ausgeblendeten Fehler umfassen alle Anforderungen für die Authentifizierung. [**InternetErrorDlg zeigt**](/windows/desktop/api/Wininet/nf-wininet-interneterrordlg) das entsprechende Dialogfeld an, in dem der Benutzer zur Eingabe der erforderlichen Daten aufgefordert wird. Die FLAGS ERROR UI FLAGS GENERATE DATA und FLAGS ERROR UI FLAGS CHANGE OPTIONS flags sollten ebenfalls an \_ \_ \_ \_ \_ \_ \_ \_ \_ \_ [**InternetErrorDlg**](/windows/desktop/api/Wininet/nf-wininet-interneterrordlg)übergeben werden, [](appendix-a-hinternet-handles.md) damit die Funktion die entsprechende Datenstruktur für den Fehler erstellt und die Ergebnisse des Dialogfelds im HINTERNET-Handle speichert.

Der folgende Beispielcode zeigt, wie die Authentifizierung mithilfe von [**InternetSetOption behandelt werden kann.**](/windows/desktop/api/Wininet/nf-wininet-internetsetoptiona)


```C++
HINTERNET hOpenHandle,  hResourceHandle, hConnectHandle;
DWORD dwStatus;
DWORD dwStatusSize = sizeof(dwStatus);
char strUsername[64], strPassword[64];

// Normally, hOpenHandle, hResourceHandle,
// and hConnectHandle need to be properly assigned.

hOpenHandle = InternetOpen(TEXT("Example"),
                           INTERNET_OPEN_TYPE_PRECONFIG,
                           NULL, NULL, 0);
hConnectHandle = InternetConnect(hOpenHandle,
                                 TEXT("www.server.com"),
                                 INTERNET_INVALID_PORT_NUMBER,
                                 NULL,
                                 NULL,
                                 INTERNET_SERVICE_HTTP,
                                 0,0);

hResourceHandle = HttpOpenRequest(hConnectHandle, TEXT("GET"),
                                  TEXT("/premium/default.htm"),
                                  NULL, NULL, NULL,
                                  INTERNET_FLAG_KEEP_CONNECTION,
                                  0);

resend:

HttpSendRequest(hResourceHandle, NULL, 0, NULL, 0);

HttpQueryInfo(hResourceHandle, HTTP_QUERY_FLAG_NUMBER |
              HTTP_QUERY_STATUS_CODE, &dwStatus, &dwStatusSize, NULL);

switch (dwStatus)
{
    // cchUserLength is the length of strUsername and
    // cchPasswordLength is the length of strPassword.
    DWORD cchUserLength, cchPasswordLength;

    case HTTP_STATUS_PROXY_AUTH_REQ: // Proxy Authentication Required
        // Insert code to set strUsername and strPassword.

        // Insert code to safely determine cchUserLength and
        // cchPasswordLength. Insert appropriate error handling code.
        InternetSetOption(hResourceHandle,
                          INTERNET_OPTION_PROXY_USERNAME,
                          strUsername,
                          cchUserLength+1);

        InternetSetOption(hResourceHandle,
                          INTERNET_OPTION_PROXY_PASSWORD,
                          strPassword,
                          cchPasswordLength+1);
        goto resend;
        break;

    case HTTP_STATUS_DENIED:     // Server Authentication Required.
        // Insert code to set strUsername and strPassword.

        // Insert code to safely determine cchUserLength and
        // cchPasswordLength. Insert error handling code as
        // appropriate.
        InternetSetOption(hResourceHandle, INTERNET_OPTION_USERNAME,
                          strUsername, cchUserLength+1);
        InternetSetOption(hResourceHandle, INTERNET_OPTION_PASSWORD,
                          strPassword, cchPasswordLength+1);
        goto resend;
        break;
}

// Insert code to read the data from the hResourceHandle
// at this point.

```



> [!Note]  
> WinINet unterstützt keine Serverimplementierung. Darüber hinaus sollte sie nicht von einem Dienst verwendet werden. Verwenden Sie für Serverimplementierungen oder -dienste [Microsoft Windows HTTP Services (WinHTTP).](/windows/desktop/WinHttp/winhttp-start-page)

 

 

 