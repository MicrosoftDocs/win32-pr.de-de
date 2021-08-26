---
description: In diesem Thema wird die Verwendung des WinHTTP-Proxykonfigurationstools (Microsoft Windows HTTP Services) &\# 0034;ProxyCfg.exe&\# 0034; erläutert.
ms.assetid: f96adf59-59be-414e-ad6f-9eac05f4b975
title: Netsh.exe und ProxyCfg.exe Proxy Konfigurationstools
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ef64c952db59fb4709614c498b4d9c732403798e
ms.sourcegitcommit: 61a4c522182aa1cacbf5669683d9570a3bf043b2
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/26/2021
ms.locfileid: "122885824"
---
# <a name="netshexe-and-proxycfgexe-proxy-configuration-tools"></a>Netsh.exe und ProxyCfg.exe Proxy Konfigurationstools

**Windows Vista und Windows Server 2008: **

ProxyCfg.exe ist veraltet. Sie wird durch die [ winhttpNetsh.exe befehle](/previous-versions/windows/it-pro/windows-server-2008-R2-and-2008/cc731131(v=ws.10)) ersetzt.

In diesem Thema wird die Verwendung des WinHTTP-Proxykonfigurationstools [(Microsoft Windows HTTP Services)](about-winhttp.md) "ProxyCfg.exe" erläutert.

Es gibt zwei Möglichkeiten, über einen Proxy mithilfe von Microsoft Windows HTTP Services (WinHTTP) auf HTTP- und HTTPS-Server (Secure Hypertext Transfer Protocol) zu zugreifen. Zunächst können Sie Proxyeinstellungen in Ihrer WinHTTP-Anwendung angeben. Zweitens können Sie mithilfe des Proxykonfigurations-Hilfsprogramms, das sich im Verzeichnis %windir% system32 befindet, Standardproxyeinstellungen von außerhalb \\ Ihrer Anwendung angeben.

Sie können die Proxydaten programmgesteuert innerhalb Ihrer Anwendung oder Ihres Skripts festlegen. Wenn Sie eine Anwendung mithilfe der WinHTTP-API schreiben, verwenden Sie eine der beiden folgenden Verfahren, um die Proxyeinstellungen zu ändern.

-   Verwenden Sie die [**WinHttpOpen-Funktion.**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpopen) Geben Sie den Zugriffstyp im zweiten Parameter, den Namen des Proxys im dritten Parameter und eine Umgehungsliste im vierten Parameter an. Das folgende Beispiel zeigt, wie die [**WinHttpOpen-Funktion**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpopen) zum Festlegen von Proxydaten verwendet werden kann.

    ``` syntax
    hSession = WinHttpOpen( L"WinHTTP Example/1.0",  
                            WINHTTP_ACCESS_TYPE_NAMED_PROXY,
                            L"proxy_name", 
                            L"<local>", 
                            0);
    ```

-   Verwenden Sie die [**WinHttpSetOption-Funktion.**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpsetoption) Mit [**dem WINHTTP \_ OPTION \_ PROXY-Flag**](option-flags.md) können Sie Proxyeinstellungen mit einer [**WINHTTP PROXY \_ \_ INFO-Struktur**](/windows/win32/api/winhttp/ns-winhttp-winhttp_proxy_info) angeben. Der folgende Beispielcode zeigt, wie die [**WinHttpSetOption-Funktion**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpsetoption) zum Festlegen von Proxydaten verwendet werden kann.

    ``` syntax
    WINHTTP_PROXY_INFO proxyInfo;
    proxyInfo.dwAccessType = WINHTTP_ACCESS_TYPE_NAMED_PROXY;
    proxyInfo.lpszProxy = L"proxy_name";
    proxyInfo.lpszProxyBypass = L"<local>";
        
    // Set the proxy information for this session.
    WinHttpSetOption( hSession, 
                      WINHTTP_OPTION_PROXY, 
                      &proxyInfo, 
                      sizeof(proxyInfo));
    ```

Wenn Sie ein Skript oder eine Anwendung mithilfe des [**WinHttpRequest-Objekts**](winhttprequest.md) schreiben, verwenden Sie das folgende Verfahren, um die Proxyeinstellungen zu ändern.

-   Verwenden Sie die [**SetProxy-Methode.**](iwinhttprequest-setproxy.md) Geben Sie den Zugriffstyp im ersten Parameter, den Namen des Proxys im zweiten Parameter und eine Umgehungsliste im dritten Parameter an. Das folgende Beispiel zeigt, wie die [**SetProxy-Methode**](iwinhttprequest-setproxy.md) im Skript zum Festlegen von Proxydaten verwendet werden kann.

    ``` syntax
    WinHttpReq.SetProxy( HTTPREQUEST_PROXYSETTING_PROXY, 
                         "proxy_server:80", 
                         "*.microsoft.com");
    ```

Verwenden Sie das Proxykonfigurations-Hilfsprogramm, um Standardeinstellungen anzugeben und die Verwendung der [**SetProxy-Methode**](iwinhttprequest-setproxy.md) oder [**der WinHttpSetOption-Funktion**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpsetoption) zu vermeiden. Mit diesem Hilfsprogramm können Sie angeben, dass Ihre Anwendung entweder direkt, über einen Proxy oder über eine Kombination aus direktem und Proxyzugriff auf ein Netzwerk zutritt, indem Sie eine Umgehungsliste angeben. Wenn Sie die WinHTTP-API verwenden, bestimmt das Proxykonfigurationstool die Einstellungen nur, wenn Sie das **WINHTTP \_ ACCESS TYPE \_ \_ DEFAULT-Flag** an die [**WinHttpOpen-API**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpopen) übergeben. Das [**WinHttpRequest-Objekt**](winhttprequest.md) verwendet standardmäßig die Einstellungen des Proxykonfigurationstools.

Die Proxyeinstellungen für WinHTTP sind nicht die Proxyeinstellungen für Microsoft Internet Explorer. Sie können die Proxyeinstellungen für WinHTTP im Microsoft-Portal nicht Windows Systemsteuerung. Die Verwendung des WinHTTP-Proxykonfigurations-Hilfsprogramms ändert nicht die Einstellungen, die Sie für Internet Explorer.

> [!Note]  
> Wenn Sie versuchen, eine HTTP-Anforderung mit WinHTTP zu öffnen und zu senden, und die Proxyeinstellungen falsch sind, tritt ein Fehler auf.

 

## <a name="command-line-parameters"></a>Befehlszeilenparameter

In der folgenden Tabelle sind die Befehlszeilenparameter aufgeführt, die für die Verwendung mit dem ProxyCfg.exe sind.



| Parameter | Beschreibung                                                                                                                                                                                                                                                                                                                                                                                                                       |
|-----------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Keine      | Wenn keine Parameter angegeben werden, werden die aktuellen WinHTTP-Proxyeinstellungen angezeigt.                                                                                                                                                                                                                                                                                                                                               |
| ?         | Hilfeinformationen werden angezeigt.                                                                                                                                                                                                                                                                                                                                                                                                    |
| T         | Gibt an, dass WinHTTP-Anwendungen ohne Proxy direkt auf das Netzwerk zugreifen.                                                                                                                                                                                                                                                                                                                                                 |
| p         | Gibt den Proxyserver an. Sie können auch eine optionale Liste von Servern angeben, auf die ohne Proxy zugegriffen wird.                                                                                                                                                                                                                                                                                                                   |
| u         | Gibt an, dass WinHTTP-Anwendungen die Proxyeinstellungen des aktuellen Benutzers für Internet Explorer. Dieser Parameter funktioniert nicht, wenn Internet Explorer Proxyeinstellungen automatisch erkennt oder eine automatische Konfigurations-URL zum Festlegen der Proxyinformationen verwendet.                                                                                                                                                      |
| i         | Gibt an, dass WinHTTP-Anwendungen die Proxyeinstellungen des aktuellen Benutzers für Internet Explorer. Dies funktioniert nur, ProxyCfg.exe zuvor nicht verwendet wurde. Wenn ProxyCfg.exe installiert ist, geben Sie an, dass der Befehlszeilenparameter "u" die manuellen Einstellungen verwendet. Dieser Parameter funktioniert nicht, wenn Internet Explorer Proxyeinstellungen automatisch erkennt oder eine automatische Konfigurations-URL zum Festlegen der Proxyinformationen verwendet. |



 

Sie können Proxys in einer durch Leerzeichen getrennten Zeichenfolge angeben. Die Proxyauflistungen können die Portnummer enthalten, die für den Zugriff auf den Proxy verwendet wird. Um einen Proxy für ein bestimmtes Protokoll auflisten zu können, muss die Zeichenfolge das Format &lt; protokoll &gt; =https://<\_ Proxyname>. Die gültigen Protokolle sind HTTP und HTTPS. Um beispielsweise einen HTTP-Proxy auflisten zu können, ist eine gültige Zeichenfolge http= , wobei http proxy name der Name des Proxyservers und 80 die Portnummer ist, die Sie für den Zugriff auf den Proxy verwenden https://http\_proxy\_name:80 \_ \_ müssen. Wenn der Proxy die Standardportnummer für dieses Protokoll verwendet, können Sie die Portnummer weglassen. Wenn ein Proxyname selbst aufgeführt wird, können Sie ihn als Standardproxy für alle Protokolle verwenden, die keinen angegebenen Proxy haben. Beispielsweise verwendet http= anderer Proxy http proxy für alle https://http\_proxy \_ HTTP-Vorgänge, während das HTTPS-Protokoll den Proxy mit dem \_ Namen other \_ proxy verwendet.

Sie können lokal bekannte Hostnamen oder IP-Adressen in der Proxyumgehungsliste auflisten. Diese Liste kann Platzhalter wie " " enthalten, die dazu führen, dass die Anwendung den Proxyserver für Adressen umgeht, die dem angegebenen Muster entsprechen, z. B. \* \* ".microsoft.com" oder \* ".org". Platzhalterzeichen müssen die linkssten Zeichen in der Liste sein. Beispiel: \* "aaa." wird nicht unterstützt. Um mehrere Adressen und Hostnamen auflisten zu können, trennen Sie sie durch Leerzeichen oder Semikolons in der Proxyumgehungszeichenfolge. Wenn Sie das lokale Makro angeben, umgeht die Funktion alle &lt; &gt; Hostnamen, die keinen Zeitraum enthalten.

> [!WARNING]
> Nachdem Proxycfg.exe ausgeführt wurde, können Sie die vorherigen Proxyeinstellungen nicht wiederherstellen. Sie können die Proxyeinstellungen jedoch vollständig entfernen.

 

## <a name="usage"></a>Verwendung

Um das Proxykonfigurationstool zu verwenden, öffnen Sie ein Eingabeaufforderungsfenster, und führen Sie das Hilfsprogramm für die Proxykonfiguration mit den entsprechenden Befehlszeilenparametern aus. Der folgende Abschnitt enthält Syntaxbeispiele.

## <a name="example-syntax"></a>Beispielsyntax

### <a name="example-1-use-a-proxy-only-for-external-resources"></a>Beispiel 1: Verwenden eines Proxys nur für externe Ressourcen

Im Folgenden finden Sie die gängigste Verwendung für Proxycfg.exe. Dieser Befehl gibt an, dass sowohl auf HTTP- als auch auf HTTPS-Server über den Proxyserver mit dem Namen "Proxyserver" zugegriffen wird, mit Ausnahme von Hostnamen, die \_ keinen Zeitraum enthalten.

**proxycfg -p proxy \_ server " &lt; local &gt; "**

### <a name="example-2-use-a-proxy-for-all-resources"></a>Beispiel 2: Verwenden eines Proxys für alle Ressourcen

Im folgenden Beispiel wird angegeben, dass sowohl auf HTTP- als auch auf HTTPS-Server über den Proxyserver mit dem Namen \_ "Proxyserver" zugegriffen wird. Es ist keine Umgehungsliste angegeben.

**proxycfg -p proxy \_ server**

### <a name="example-3-use-a-different-proxy-for-secure-resources"></a>Beispiel 3: Verwenden eines anderen Proxys für sichere Ressourcen

Im folgenden Beispiel wird angegeben, dass auf HTTP-Server über den HTTP-Proxy und auf HTTPS-Server über den \_ HTTPS-Proxy zugegriffen \_ wird. Lokale Intranetstandorte und alle Standorte in der \* .microsoft.com-Domäne umgehen den Proxy.

**proxycfg -p "http=http \_ proxy https=https \_ proxy" " &lt; local ; &gt; \* . microsoft.com"**

## <a name="removing-proxycfgexe"></a>Entfernen ProxyCfg.exe

Nachdem Sie das Proxykonfigurationstool verwendet haben, können Sie ihre ursprünglichen Proxyeinstellungen nicht wiederherstellen. Bei Bedarf können Sie jedoch die Registrierungseinstellungen entfernen, die das Hilfsprogramm erstellt. Um die registrierungseinträge zu entfernen, ProxyCfg.exe erstellt werden, müssen Sie den **WinHttpSettings-Wert** aus dem folgenden Registrierungsschlüssel löschen.

**HKEY \_ LOCAL \_ MACHINE** \\ **SOFTWARE** \\ **Microsoft** \\ **Windows** \\ **CurrentVersion** \\ **Internet Einstellungen** \\ **Connections** \\ **WinHttpSettings**

Durch das Löschen *des WinHttpSettings-Werts* werden alle Proxykonfigurationen entfernt.

## <a name="proxycfgexe-and-authentication"></a>ProxyCfg.exe und Authentifizierung

Das Proxykonfigurations-Hilfsprogramm legt die Standardauthentifizierungsrichtlinie fest. Da Sie keine NTLM-Authentifizierung mit nicht vertrauenswürdigen Hosts durchführen sollten, erfolgt die NTLM-Authentifizierung standardmäßig nur automatisch bei Hosts in der Proxyumgehungsliste. Wenn kein Proxy verfügbar ist, können Sie ProxyCfg.exe verwenden, um eine Umgehungsliste von Hosts anzugeben, denen Sie vertrauen, um die NTLM-Authentifizierung durchzuführen. Ein Proxyname ist erforderlich, wenn ProxyCfg.exe für diesen Zweck verwendet wird. Sie können jedoch eine beliebige gültige Zeichenfolge statt eines echten Proxynamens verwenden.

Weitere Informationen zur Richtlinie für die automatische Anmeldung finden Sie unter [Richtlinie für die automatische Anmeldung.](authentication-in-winhttp.md)

 

 
