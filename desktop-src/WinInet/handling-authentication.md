---
title: Behandeln der Authentifizierung
description: Einige Proxys und Server erfordern eine Authentifizierung, bevor Sie Zugriff auf Ressourcen im Internet gewähren.
ms.assetid: f3752031-30d3-4e35-8eae-1d4971b66bc2
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 36a8eaa38f61f0d97f1f543e0623313aa196aab7
ms.sourcegitcommit: 773fa6257ead6c74154ad3cf46d21e49adc900aa
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/09/2020
ms.locfileid: "104039772"
---
# <a name="handling-authentication"></a>Behandeln der Authentifizierung

Einige Proxys und Server erfordern eine Authentifizierung, bevor Sie Zugriff auf Ressourcen im Internet gewähren. Die WinInet-Funktionen unterstützen die Server-und Proxy Authentifizierung für HTTP-Sitzungen. Die Authentifizierung von FTP-Servern muss von der [**InternetConnect**](/windows/desktop/api/Wininet/nf-wininet-internetconnecta) -Funktion verarbeitet werden. Die FTP-Gatewayauthentifizierung wird derzeit nicht unterstützt.

## <a name="about-http-authentication"></a>Informationen zur HTTP-Authentifizierung

Wenn eine Authentifizierung erforderlich ist, empfängt die Client Anwendung den Statuscode 401, wenn der Server eine Authentifizierung erfordert, oder 407, wenn für den Proxy eine Authentifizierung erforderlich ist. Mit dem Statuscode sendet der Proxy oder Server mindestens einen authentifikatsantwortheader – Proxy-authentifizieren (für die Proxy Authentifizierung) oder WWW-Authenticate (für die Server Authentifizierung).

Jeder authentifizieren-Antwortheader enthält ein verfügbares Authentifizierungsschema und einen Bereich. Wenn mehrere Authentifizierungs Schemas unterstützt werden, gibt der Server mehrere authentifizieren-Antwortheader zurück. Beim Bereichs Wert wird die Groß-/Kleinschreibung beachtet, und es wird ein Schutzbereich auf dem Proxy oder Server definiert. Beispielsweise wäre der Header "www-Authenticate: Basic Realm =" example "" ein Beispiel für einen Header, der zurückgegeben wird, wenn eine Server Authentifizierung erforderlich ist.

Die Client Anwendung, die die Anforderung gesendet hat, kann sich selbst authentifizieren, indem Sie ein Autorisierungs Header Feld mit der Anforderung einschließt. Der Autorisierungs Header würde das Authentifizierungsschema und die entsprechende Antwort enthalten, die für dieses Schema erforderlich ist. Beispielsweise würde die Kopfzeile "Authorization: Basic <username: Password>" der Anforderung hinzugefügt und erneut an den Server gesendet, wenn der Client den authentifizieren-Antwortheader "www-authentifizieren: Basic Realm =" example "" empfangen hat.

Es gibt zwei allgemeine Arten von Authentifizierungs Schemas:

-   Standard Authentifizierungsschema, bei dem der Benutzername und das Kennwort in Klartext an den Server gesendet werden.
-   Challenge-Response-Schemas, die ein Challenge-Response-Format ermöglichen.

Das grundlegende Authentifizierungsschema basiert auf dem Modell, das ein Client selbst mit einem Benutzernamen und einem Kennwort für jeden Bereich authentifizieren muss. Der Server dient zum Verarbeiten der Anforderung, wenn Sie mit einem Autorisierungs Header mit einem gültigen Benutzernamen und Kennwort erneut gesendet wird.

Mit Challenge-Response-Schemas wird eine sicherere Authentifizierung ermöglicht. Wenn eine Anforderung eine Authentifizierung mit einem Challenge-Response-Schema erfordert, werden der entsprechende Statuscode und die Authenticate-Header an den Client zurückgegeben. Der Client muss dann die Anforderung mit einem Aushandlungs Vorgang erneut senden. Der Server gibt einen entsprechenden Statuscode mit einer Herausforderung zurück, und der Client müsste dann die Anforderung mit der richtigen Antwort erneut senden, um den angeforderten Dienst zu erhalten.

In der folgenden Tabelle sind die Authentifizierungs Schemas, der Authentifizierungstyp, die dll, die Sie unterstützt, und eine Beschreibung des Schemas aufgelistet.



| Schema                                    | type               | DLL                  | BESCHREIBUNG                                                                                                                                                                                                                                                                                                                                        |
|-------------------------------------------|--------------------|----------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Basic (cleartext)                         | basic              | Wininet.dll          | Verwendet eine Base64-codierte Zeichenfolge, die den Benutzernamen und das Kennwort enthält.                                                                                                                                                                                                                                                                             |
| Digest                                    | Challenge-Response | Digest.dll           | Ein Challenge-Response-Schema, das die Verwendung eines Nonce-Werts (eine vom Server angegebene Daten Zeichenfolge) herausstellt. Eine gültige Antwort enthält eine Prüfsumme aus dem Benutzernamen, dem Kennwort, dem angegebenen Nonce-Wert, der HTTP-Methode und dem angeforderten Uniform Resource Identifier (URI). Die Unterstützung für die Digest-Authentifizierung wurde in Microsoft Internet Explorer 5 eingeführt. |
| NT-LAN-Manager (NTLM)                     | Challenge-Response | Winsspi.dll          | Ein Challenge-Response-Schema, das die Herausforderung auf den Benutzernamen stützt.                                                                                                                                                                                                                                                                             |
| Microsoft-Netzwerk (MSN)                   | Challenge-Response | Msnsspc.dll          | Das Authentifizierungsschema the Microsoft Network.                                                                                                                                                                                                                                                                                                     |
| Authentifizierung verteilter Kenn Wörter (dpa) | Challenge-Response | Msapsspc.dll         | Ähnelt der MSN-Authentifizierung und wird auch vom Microsoft-Netzwerk verwendet.                                                                                                                                                                                                                                                                           |
| Remote Passphrase-Authentifizierung (RPA)    | CompuServe         | Rpawinet.dll da.dll | Compuservice-Authentifizierungsschema. Weitere Informationen finden Sie in den [Spezifikationen für den RPA-Mechanismus](https://www.compuserve.com/).                                                                                                                                                                                                    |



 

Für andere als die Standard Authentifizierung müssen die Registrierungsschlüssel zusätzlich zur Installation der entsprechenden DLL eingerichtet werden.

Wenn eine Authentifizierung erforderlich ist, sollte das [Internet \_ Flag \_ Keep \_ Connection](api-flags.md) -Flag im [**httpopanrequest**](/windows/desktop/api/Wininet/nf-wininet-httpopenrequesta)-Befehl verwendet werden. Das \_ \_ \_ kennflag für die Verbindungsart "Internet" ist für NTLM und andere Arten der Authentifizierung erforderlich, um die Verbindung während des Authentifizierungs Vorgangs aufrechtzuerhalten. Wenn die Verbindung nicht beibehalten wird, muss der Authentifizierungs Vorgang mit dem Proxy oder dem Server neu gestartet werden.

Die Funktionen [**InternetOpenUrl**](/windows/desktop/api/Wininet/nf-wininet-internetopenurla) und [**HttpSendRequest**](/windows/desktop/api/Wininet/nf-wininet-httpsendrequesta) werden erfolgreich abgeschlossen, auch wenn eine Authentifizierung erforderlich ist. Der Unterschied besteht darin, dass die in den Header Dateien und in der [**Datei "internetreadfile**](/windows/desktop/api/Wininet/nf-wininet-internetreadfile) " zurückgegebenen Daten eine HTML-Seite erhalten, in der der Benutzer über den Statuscode

### <a name="registering-authentication-keys"></a>Registrieren von authentifizierungsschlüsseln

Internet \_ Open \_ Type \_ preconfig prüft die Registrierungs Werte **ProxyEnable**, **Proxyserver** und **ProxyOverride**. Diese Werte befinden sich unter **HKEY \_ Current \_ User** \\ **Software** \\ **Microsoft** \\ **Windows** \\ **CurrentVersion** \\ **Internet Settings**.

Für andere Authentifizierungs Schemas als Basic muss der Registrierung unter **HKEY \_ local \_ Machine** \\ **Software** \\ **Microsoft** \\ **Internet Explorer** \\ **Security** ein Schlüssel hinzugefügt werden. Ein **DWORD** -Wert, **Flags**, sollte mit dem entsprechenden Wert festgelegt werden. In der folgenden Liste werden die möglichen Werte für den **Flags** -Wert angezeigt.

-   Eindeutiger \_ \_ \_ \_ Kontext \_ pro \_ tcpip (Wert = 0x01) für Plug-in-Authentifizierungsflags

    Jeder TCP/IP-Socket (Transmission Control Protocol/Internet Protocol) enthält einen anderen Kontext. Andernfalls wird für jede Bereichs-oder Block-URL-Vorlage ein neuer Kontext übermittelt.

-   Plug-in- \_ Authentifizierungsflags \_ können die \_ \_ \_ Benutzeroberfläche verarbeiten (Wert = 0x02)

    Diese DLL kann Ihre eigene Benutzereingaben verarbeiten.

-   Plug-in- \_ auth- \_ Flags \_ können \_ \_ keine \_ passwd verarbeiten (Wert = 0x04)

    Diese DLL kann eine Authentifizierung durchgeführt werden, ohne dass der Benutzer zur Eingabe eines Kennworts aufgefordert wird.

-   Plug-in für die Plug-in-Authentifizierung \_ \_ \_ ohne \_ Bereich (Wert = 0x08)

    Diese DLL verwendet keine Standard-HTTP-Bereichs Zeichenfolge. Alle Daten, die als Bereich angezeigt werden, sind Schema spezifische Daten.

-   Plug-in- \_ auth- \_ Flags \_ bleiben \_ \_ nicht \_ erforderlich (Wert = 0x10)

    Diese DLL erfordert keine permanente Verbindung für Ihre Challenge-Response-Sequenz.

Wenn Sie z. b. die NTLM-Authentifizierung hinzufügen möchten, muss der Schlüssel NTLM der **lokalen HKEY- \_ \_ Computer** \\ **Software** \\ **Microsoft** \\ **Internet Explorer** \\ **Security** hinzugefügt werden. Unter **HKEY \_ local \_ Machine** \\ **Software** \\ **Microsoft** \\ **Internet Explorer** \\ **Security** \\ **NTLM** müssen der Zeichen folgen Wert, der **dllfile**-Wert und der **DWORD** -Wert **Flags** hinzugefügt werden. **Dllfile** muss auf Winsspi.dll festgelegt werden, und **Flags** müssen auf 0x08 festgelegt werden.

### <a name="server-authentication"></a>Serverauthentifizierung

Wenn ein Server eine Anforderung empfängt, die eine Authentifizierung erfordert, gibt der Server eine 401-Statuscode Meldung zurück. In dieser Meldung sollte der Server mindestens einen WWW-Authenticate Antwortheader enthalten. Diese Header enthalten die Authentifizierungsmethoden, die der Server zur Verfügung gestellt hat. WinInet wählt die erste Methode aus, die er erkennt.

Die Standard Authentifizierung bietet eine schwache Sicherheit, es sei denn, der Channel ist erstmalig mit SSL oder PCT verschlüsselt.

Die [**internetterrordlg**](/windows/desktop/api/Wininet/nf-wininet-interneterrordlg) -Funktion kann verwendet werden, um die Benutzernamen-und Kenn Wort Daten vom Benutzer abzurufen, oder es kann eine angepasste Benutzeroberfläche entworfen werden, um die Daten zu erhalten.

Eine benutzerdefinierte Schnittstelle kann die [**internettoption**](/windows/desktop/api/Wininet/nf-wininet-internetsetoptiona) -Funktion verwenden, um die [Internet \_ Option \_ Password](option-flags.md) -und [Internet \_ Option \_ username](option-flags.md) -Werte festzulegen und die Anforderung dann erneut an den Server zu senden.

### <a name="proxy-authentication"></a>Proxyauthentifizierung

Wenn ein Client versucht, einen Proxy zu verwenden, der eine Authentifizierung erfordert, gibt der Proxy eine 407-Statuscode Meldung an den Client zurück. In dieser Meldung sollte der Proxy mindestens einen Proxy-Authenticate Antwortheader enthalten. Diese Header enthalten die vom Proxy verfügbaren Authentifizierungsmethoden. WinInet wählt die erste Methode aus, die er erkennt.

Die [**internetterrordlg**](/windows/desktop/api/Wininet/nf-wininet-interneterrordlg) -Funktion kann verwendet werden, um die Benutzernamen-und Kenn Wort Daten vom Benutzer zu erhalten, oder es kann eine angepasste Benutzeroberfläche entworfen werden.

Eine benutzerdefinierte Schnittstelle kann die [**internettoption**](/windows/desktop/api/Wininet/nf-wininet-internetsetoptiona) -Funktion verwenden, um die [Internet \_ Option \_ Proxy \_ Kennwort](option-flags.md) und [Internet \_ options \_ Proxy- \_ Benutzernamen](option-flags.md) Werte festzulegen und die Anforderung dann erneut an den Proxy zu senden.

Wenn kein Proxy Benutzername und kein Kennwort festgelegt sind, versucht WinInet, den Benutzernamen und das Kennwort für den Server zu verwenden. Dieses Verhalten ermöglicht es Clients, dieselbe angepasste Benutzeroberfläche zu implementieren, die zum Verarbeiten der Server Authentifizierung verwendet wird.

## <a name="handling-http-authentication"></a>Behandeln der HTTP-Authentifizierung

Die HTTP-Authentifizierung kann entweder mit " [**internetterrordlg**](/windows/desktop/api/Wininet/nf-wininet-interneterrordlg) " oder mit einer benutzerdefinierten Funktion durchgeführt werden, die " [**InternetSetOption**](/windows/desktop/api/Wininet/nf-wininet-internetsetoptiona) " verwendet oder eigene Authentifizierungs Header hinzufügt. [**Internetzterrordlg**](/windows/desktop/api/Wininet/nf-wininet-interneterrordlg) kann die mit einem [**hinternethandle**](appendix-a-hinternet-handles.md) verknüpften Header untersuchen, um verborgene Fehler, wie z. b. Statuscodes von einem Proxy oder Server, zu suchen. [**InternetSetOption**](/windows/desktop/api/Wininet/nf-wininet-internetsetoptiona) kann verwendet werden, um den Benutzernamen und das Kennwort für den Proxy und den Server festzulegen. Bei der MSN-und DPA-Authentifizierung muss [**internetterrordlg**](/windows/desktop/api/Wininet/nf-wininet-interneterrordlg) verwendet werden, um den Benutzernamen und das Kennwort festzulegen.

Für jede benutzerdefinierte Funktion, die eigene WWW-Authenticate oder Proxy-Authenticate Header hinzufügt, sollte das [Internet \_ Flag \_ No \_ auth](api-flags.md) -Flag festgelegt werden, um die Authentifizierung zu deaktivieren.

Im folgenden Beispiel wird gezeigt, wie mit [**internetterrordlg**](/windows/desktop/api/Wininet/nf-wininet-interneterrordlg) die HTTP-Authentifizierung behandelt werden kann.


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



Im Beispiel wird dwErrorCode verwendet, um alle Fehler zu speichern, die mit dem-Befehl von [**HttpSendRequest**](/windows/desktop/api/Wininet/nf-wininet-httpsendrequesta)verknüpft sind. [**HttpSendRequest**](/windows/desktop/api/Wininet/nf-wininet-httpsendrequesta) wird erfolgreich abgeschlossen, auch wenn für den Proxy oder Server eine Authentifizierung erforderlich ist. Wenn das \_ Flag Fehler UI-Filter für Fehler der Flags-Fehlermeldung \_ \_ \_ \_ an [**internetterrordlg**](/windows/desktop/api/Wininet/nf-wininet-interneterrordlg)übermittelt wird, prüft die Funktion die Header auf alle verdeckten Fehler. Diese ausgeblendeten Fehler würden alle Authentifizierungsanforderungen einschließen. [**Interneterrordlg**](/windows/desktop/api/Wininet/nf-wininet-interneterrordlg) zeigt das entsprechende Dialogfeld an, in dem der Benutzer zur Eingabe der erforderlichen Daten aufgefordert wird. Die Flags \_ \_ -Fehler \_ - \_ UI \_ -Flags Daten generieren Daten und Flags \_ Fehler \_ UI \_ Flags ändern-Flags \_ \_ müssen auch an [**interneterrordlg**](/windows/desktop/api/Wininet/nf-wininet-interneterrordlg)übermittelt werden, damit die Funktion die entsprechende Datenstruktur für den Fehler erstellt und die Ergebnisse des Dialog Felds im [**HINTERNET**](appendix-a-hinternet-handles.md) -handle speichert.

Der folgende Beispielcode zeigt, wie die Authentifizierung mithilfe von [**InternetSetOption**](/windows/desktop/api/Wininet/nf-wininet-internetsetoptiona)verarbeitet werden kann.


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
> WinInet unterstützt keine Server Implementierungen. Außerdem sollte Sie nicht von einem Dienst verwendet werden. Verwenden Sie für Server Implementierungen oder-Dienste [Microsoft Windows HTTP-Dienste (WinHTTP)](/windows/desktop/WinHttp/winhttp-start-page).

 

 

 