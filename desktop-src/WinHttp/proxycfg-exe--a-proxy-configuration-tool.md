---
description: In diesem Thema wird die Verwendung des Microsoft Windows HTTP-Dienste (WinHTTP)-proxykonfigurationstools &\# 0034; ProxyCfg.exe&\# 0034; erläutert.
ms.assetid: f96adf59-59be-414e-ad6f-9eac05f4b975
title: Netsh.exe und ProxyCfg.exe Proxy Konfigurationstools
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 96a33e832d324a5863652673b8e25725fba72e88
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104524827"
---
# <a name="netshexe-and-proxycfgexe-proxy-configuration-tools"></a>Netsh.exe und ProxyCfg.exe Proxy Konfigurationstools

* * Windows Vista und Windows Server 2008: * *

ProxyCfg.exe ist veraltet. Sie wird durch die [Netsh.exe WinHTTP](/previous-versions/windows/it-pro/windows-server-2008-R2-and-2008/cc731131(v=ws.10)) -Befehle ersetzt.

In diesem Thema wird die Verwendung des [Microsoft Windows HTTP-Dienste (WinHTTP)](about-winhttp.md) -proxykonfigurationstools "ProxyCfg.exe" erläutert.

Es gibt zwei Möglichkeiten für den Zugriff auf http-und Secure Hypertext Transfer Protocol (HTTPS)-Server über einen Proxy mithilfe der Microsoft Windows HTTP-Dienste (WinHTTP). Zuerst können Sie Proxy Einstellungen in der WinHTTP-Anwendung angeben. Zweitens können Sie die Standard Proxy Einstellungen von außerhalb der Anwendung angeben, indem Sie das Proxy Konfigurations Hilfsprogramm im Verzeichnis% windir% \\ system32 verwenden.

Sie können die Proxy Daten in der Anwendung oder im Skript Programm gesteuert festlegen. Wenn Sie eine Anwendung mit der WinHTTP-API schreiben, verwenden Sie eine der beiden folgenden Verfahren, um die Proxy Einstellungen zu ändern.

-   Verwenden Sie die [**WinHttpOpen**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpopen) -Funktion. Legen Sie den Zugriffstyp im zweiten Parameter, den Namen des Proxys im dritten Parameter und eine Umgehungs Liste im vierten Parameter fest. Im folgenden Beispiel wird gezeigt, wie die [**WinHttpOpen**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpopen) -Funktion zum Festlegen von Proxy Daten verwendet werden kann.

    ``` syntax
    hSession = WinHttpOpen( L"WinHTTP Example/1.0",  
                            WINHTTP_ACCESS_TYPE_NAMED_PROXY,
                            L"proxy_name", 
                            L"<local>", 
                            0);
    ```

-   Verwenden Sie die [**WinHttpSetOption**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpsetoption) -Funktion. Das [**WinHTTP \_ - \_ optionsproxyflag**](option-flags.md) ermöglicht Ihnen das Angeben von Proxy Einstellungen mit einer [**WinHTTP- \_ Proxy \_ Informations**](/windows/win32/api/winhttp/ns-winhttp-winhttp_proxy_info) Struktur. Der folgende Beispielcode zeigt, wie die [**WinHttpSetOption**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpsetoption) -Funktion zum Festlegen von Proxy Daten verwendet werden kann.

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

Wenn Sie ein Skript oder eine Anwendung mit dem [**WinHttpRequest**](winhttprequest.md) -Objekt schreiben, verwenden Sie das folgende Verfahren, um die Proxy Einstellungen zu ändern.

-   Verwenden Sie die [**SetProxy**](iwinhttprequest-setproxy.md) -Methode. Geben Sie den Zugriffstyp im ersten Parameter, den Namen des Proxys im zweiten Parameter und eine Umgehungs Liste im dritten Parameter an. Im folgenden Beispiel wird gezeigt, wie die [**SetProxy**](iwinhttprequest-setproxy.md) -Methode im Skript zum Festlegen von Proxy Daten verwendet werden kann.

    ``` syntax
    WinHttpReq.SetProxy( HTTPREQUEST_PROXYSETTING_PROXY, 
                         "proxy_server:80", 
                         "*.microsoft.com");
    ```

Um die Standardeinstellungen anzugeben und die Verwendung der [**SetProxy**](iwinhttprequest-setproxy.md) -Methode oder der [**WinHttpSetOption**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpsetoption) -Funktion zu vermeiden, verwenden Sie das Proxy Konfigurations Hilfsprogramm. Mit diesem Hilfsprogramm können Sie angeben, dass Ihre Anwendung entweder direkt, über einen Proxy oder durch eine Kombination aus direktem und Proxy Zugriff auf ein Netzwerk zugreifen soll, indem Sie eine Umgehungs Liste angeben. Wenn Sie die WinHTTP-API verwenden, bestimmt das Proxy Konfigurationstool nur die Einstellungen, wenn Sie das **Standardflag WinHTTP- \_ \_ Zugriffstyp \_** an die [**WinHttpOpen**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpopen) -API übergeben. Das [**WinHttpRequest**](winhttprequest.md) -Objekt verwendet standardmäßig die Einstellungen für das Proxy Konfigurationstool.

Die Proxy Einstellungen für WinHTTP sind nicht die Proxy Einstellungen für Microsoft Internet Explorer. In der Microsoft Windows-Systemsteuerung können Sie die Proxy Einstellungen für WinHTTP nicht konfigurieren. Die Verwendung des Konfigurations Hilfsprogramms WinHTTP-Proxy ändert nicht die Einstellungen, die Sie für Internet Explorer verwenden.

> [!Note]  
> Wenn Sie versuchen, eine HTTP-Anforderung mit WinHTTP zu öffnen und zu senden, und die Proxy Einstellungen falsch sind, tritt ein Fehler auf.

 

## <a name="command-line-parameters"></a>Befehlszeilenparameter

In der folgenden Tabelle sind die Befehlszeilenparameter aufgeführt, die für die Verwendung mit dem ProxyCfg.exe Tool verfügbar sind.



| Parameter | BESCHREIBUNG                                                                                                                                                                                                                                                                                                                                                                                                                       |
|-----------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| none      | Wenn keine Parameter angegeben werden, werden die aktuellen WinHTTP-Proxy Einstellungen angezeigt.                                                                                                                                                                                                                                                                                                                                               |
| ?         | Hilfe Informationen werden angezeigt.                                                                                                                                                                                                                                                                                                                                                                                                    |
| d         | Gibt an, dass WinHTTP-Anwendungen direkt und ohne Proxy auf das Netzwerk zugreifen.                                                                                                                                                                                                                                                                                                                                                 |
| p         | Gibt den Proxy Server an. Sie können auch eine optionale Liste der Server angeben, auf die ohne Proxy zugegriffen werden soll.                                                                                                                                                                                                                                                                                                                   |
| u         | Gibt an, dass WinHTTP-Anwendungen die Proxy Einstellungen des aktuellen Benutzers für Internet Explorer verwenden. Dieser Parameter funktioniert nicht, wenn Internet Explorer Proxy Einstellungen automatisch erkennt, oder wenn er eine automatische Konfigurations-URL verwendet, um die Proxy Informationen festzulegen.                                                                                                                                                      |
| i         | Gibt an, dass WinHTTP-Anwendungen die Proxy Einstellungen des aktuellen Benutzers für Internet Explorer verwenden. Dies funktioniert nur, wenn ProxyCfg.exe zuvor nicht verwendet wurde. Wenn ProxyCfg.exe installiert ist, geben Sie an, dass für den Befehlszeilenparameter "u" die manuellen Einstellungen verwendet werden. Dieser Parameter funktioniert nicht, wenn Internet Explorer Proxy Einstellungen automatisch erkennt, oder wenn er eine automatische Konfigurations-URL verwendet, um die Proxy Informationen festzulegen. |



 

Sie können Proxys in einer durch Leerzeichen getrennten Zeichenfolge angeben. Die Proxy Listen können die Portnummer enthalten, die für den Zugriff auf den Proxy verwendet wird. Zum Auflisten eines Proxys für ein bestimmtes Protokoll muss die Zeichenfolge dem folgenden Format entsprechen: <protocol> = https://<Proxy \_ Name>. Gültige Protokolle sind http und HTTPS. Um beispielsweise einen HTTP-Proxy aufzulisten, ist eine gültige Zeichenfolge http = https://http\_proxy\_name:80 , wobei \_ http \_ -Proxy Name der Name des Proxy Servers und 80 die Portnummer ist, die Sie für den Zugriff auf den Proxy verwenden müssen. Wenn der Proxy die Standard Portnummer für dieses Protokoll verwendet, können Sie die Portnummer weglassen. Wenn ein Proxy Name allein aufgeführt wird, können Sie ihn als Standard Proxy für alle Protokolle verwenden, die nicht über einen bestimmten Proxy verfügen. Http = https://http\_proxy anderer \_ Proxy verwendet beispielsweise http- \_ Proxy für http-Vorgänge, während das HTTPS-Protokoll den Proxy namens anderer \_ Proxy verwendet.

Sie können lokale bekannte Hostnamen oder IP-Adressen in der Proxy Umgehungs Liste auflisten. Diese Liste kann Platzhalter enthalten, wie z. b. " \* ", die bewirken, dass die Anwendung den Proxy Server für Adressen umgeht, die dem angegebenen Muster entsprechen, z. b. " \* . Microsoft.com" oder " \* . org". Platzhalter Zeichen müssen die äußersten linken Zeichen in der Liste sein. Beispiel: "AAA". \* wird nicht unterstützt. Wenn Sie mehrere Adressen und Hostnamen auflisten möchten, trennen Sie diese durch Leerzeichen oder Semikolons in der Proxy Umgehungs Zeichenfolge. Wenn Sie das- <local> Makro angeben, umgeht die Funktion jeden Hostnamen, der keinen-Zeitraum enthält.

> [!WARNING]
> Nachdem Proxycfg.exe ausgeführt wurde, können Sie die vorherigen Proxy Einstellungen nicht wiederherstellen. Allerdings können Sie die Proxy Einstellungen vollständig entfernen.

 

## <a name="usage"></a>Verbrauch

Um das Proxy Konfigurationstool zu verwenden, öffnen Sie ein Eingabe Aufforderungs Fenster, und führen Sie das Proxy Konfigurations Hilfsprogramm mit den entsprechenden Befehlszeilen Parametern aus. Der folgende Abschnitt enthält Beispiele für die Syntax.

## <a name="example-syntax"></a>Beispiel Syntax

### <a name="example-1-use-a-proxy-only-for-external-resources"></a>Beispiel 1: Verwenden eines Proxys nur für externe Ressourcen

Im folgenden finden Sie die gängigste Verwendung von Proxycfg.exe. Dieser Befehl gibt an, dass auf http-und HTTPS-Server über den Proxy Server mit dem Namen "Proxy \_ Server" zugegriffen wird, mit Ausnahme von Hostnamen, die keinen Punkt enthalten.

**proxycfg-p-Proxy \_ Server " <local> "**

### <a name="example-2-use-a-proxy-for-all-resources"></a>Beispiel 2: Verwenden eines Proxys für alle Ressourcen

Im folgenden Beispiel wird angegeben, dass auf http-und HTTPS-Server über den Proxy Server mit dem Namen "Proxy \_ Server" zugegriffen wird. Es wurde keine Umgehungs Liste angegeben.

**proxycfg-p-Proxy \_ Server**

### <a name="example-3-use-a-different-proxy-for-secure-resources"></a>Beispiel 3: Verwenden eines anderen Proxys für sichere Ressourcen

Im folgenden Beispiel wird angegeben, dass der Zugriff auf http-Server über den HTTP \_ -Proxy Proxy und auf HTTPS-Server über den HTTPS- \_ Proxy erfolgt. Lokale Intranetsites und eine beliebige Site in der \* . Microsoft.com-Domäne umgehen den Proxy.

**proxycfg-p "http = http- \_ Proxy HTTPS = HTTPS- \_ Proxy" " <local> ; \* . Microsoft.com "**

## <a name="removing-proxycfgexe"></a>Entfernen von ProxyCfg.exe

Nachdem Sie das Proxy Konfigurationstool verwendet haben, können Sie die ursprünglichen Proxy Einstellungen nicht wiederherstellen. Falls erforderlich, können Sie jedoch die Registrierungs Einstellungen entfernen, die vom-Hilfsprogramm erstellt werden. Um die von ProxyCfg.exe erstellten Registrierungseinträge zu entfernen, müssen Sie den **WinHttpSettings** -Wert aus dem folgenden Registrierungsschlüssel löschen.

**HKEY \_ Lokale \_ Computer** \\ **Software** \\ **Microsoft** \\ **Windows** \\ **CurrentVersion** \\ **Internet Settings** \\ **Connections** \\ **WinHttpSettings**

Wenn Sie den *WinHttpSettings* -Wert löschen, werden alle Proxy Konfigurationen entfernt.

## <a name="proxycfgexe-and-authentication"></a>ProxyCfg.exe und Authentifizierung

Das Proxy Konfigurations Hilfsprogramm legt die Standard Authentifizierungs Richtlinie fest. Da Sie die NTLM-Authentifizierung nicht bei nicht vertrauenswürdigen Hosts ausführen sollten, erfolgt die NTLM-Authentifizierung standardmäßig nur automatisch mit Hosts in der Proxy Umgehungs Liste. Wenn kein Proxy vorhanden ist, können Sie weiterhin ProxyCfg.exe verwenden, um eine Umgehungs Liste der Hosts anzugeben, denen Sie Vertrauen, um die NTLM-Authentifizierung auszuführen. Ein Proxy Name ist erforderlich, wenn ProxyCfg.exe zu diesem Zweck verwendet wird. Sie können jedoch eine beliebige gültige Zeichenfolge anstelle eines echten Proxy namens verwenden.

Weitere Informationen zur Richtlinie für die automatische Anmeldung finden Sie unter [Richtlinie](authentication-in-winhttp.md)für die automatische Anmeldung.

 

 
