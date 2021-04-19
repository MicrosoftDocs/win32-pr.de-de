---
description: Zum Vereinfachen der Konfiguration von Proxy Einstellungen implementiert WinHTTP 5,1 das WPAD-Protokoll (Web Proxy Auto-Discovery), das auch als AutoProxy bezeichnet wird.
ms.assetid: f766f37b-a1aa-420f-ac3b-d03485630d88
title: WinHTTP-AutoProxy-Unterstützung
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 26584bd0b1809f3866ed42adc7198275f40f991c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106357339"
---
# <a name="winhttp-autoproxy-support"></a>WinHTTP-AutoProxy-Unterstützung

Zum Vereinfachen der Konfiguration von Proxy Einstellungen implementiert WinHTTP 5,1 das WPAD-Protokoll (Web Proxy Auto-Discovery), das auch als AutoProxy bezeichnet wird.

## <a name="overview-of-autoproxy"></a>Übersicht über AutoProxy

Anwendungen und Komponenten, die WinHTTP zum Senden von HTTP-Anforderungen verwenden, sollten sicherstellen, dass die Proxykonfiguration ordnungsgemäß festgelegt ist. Wenn der Client nicht über eine direkte Internet Verbindung verfügt, sollte normalerweise eine HTTP-Anforderung über einen Webproxyserver gesendet werden, der das lokale Netzwerk des Clients mit dem Internet verbindet (z. b. Dies ist häufig der Fall bei Webclients in einem Unternehmens-LAN). Bei serverbasierten Anwendungen wird die Proxykonfiguration normalerweise vom Administrator des Servers mithilfe des Dienstprogramms WinHTTP ProxyCfg.exe verwaltet. Der Server Administrator kennt den Namen des Proxy Servers im voraus und verwendet ProxyCfg.exe, um diese Einstellung in der Registrierung aufzuzeichnen, in der WinHTTP nachschlagen kann. Es ist jedoch problematisch, dass Client Desktop-Endbenutzer die WinHTTP-Proxy Einstellungen manuell konfigurieren. Der Endbenutzer kennt den Namen des Proxy Servers möglicherweise nicht. die Notwendigkeit, dass der Endbenutzer das ProxyCfg.exe-Hilfsprogramm ausführen muss, kann eine Unterstützung für eine Organisation darstellen. Zur Unterstützung eines guten Benutzer Erlebnisses sollte eine webfähige Client Anwendung die Proxykonfiguration ohne Benutzereingriff ermitteln.

Zum Vereinfachen der Konfiguration der Proxy Einstellungen für WinHTTP-basierte Anwendungen implementiert WinHTTP jetzt das [WPAD-Protokoll (Web Proxy Auto-Discovery)](https://tools.ietf.org/html/draft-ietf-wrec-wpad-01), das häufig als *aktivierter automatischer Proxy* bezeichnet wird. Dabei handelt es sich um das Protokoll, das von Webbrowsern implementiert wird, um die Proxykonfiguration automatisch zu ermitteln, ohne dass ein Endbenutzer einen Proxy Server manuell angeben muss. Diese Funktion ist ab WinHTTP-Version 5,1 in Windows 2000 Service Pack 3, Windows XP Service Pack 1 und Windows Server 2003 verfügbar. Beachten Sie, dass zwar sowohl Microsoft Internet Explorer als auch Microsoft WinHTTP unterstützen, die Spezifikation jedoch nie über die "Internet Draft"-Phase hinausgeht und im Mai 2001 abgelaufen ist.

Das WPAD-Protokoll funktioniert wie folgt:

1.  Mithilfe der DHCP-und/oder DNS-Netzwerkprotokolle wird die URL einer Datei für die automatische Proxy Konfiguration erkannt. Die URL identifiziert eine PAC-Datei im lokalen Netzwerk des Clients. WinHTTP unterstützt nur die PAC-URLs "http:" und "https:". Es werden z. b. keine URLs für "file:" unterstützt.
2.  Die PAC-Datei wird heruntergeladen und optional auf dem Client Computer zwischengespeichert. Bei der PAC-Datei handelt es sich um ein ausführbares Skript, das eine Liste mit einem oder mehreren Proxy Servern mit einem Zielhostnamen und einer URL generiert. WinHTTP unterstützt nur ECMAScript-basierte PAC-Dateien.
3.  Für jede HTTP-Anforderung wird der PAC-Skriptcode ausgeführt, wobei der Hostname und die URL der HTTP-Anforderung als Parameter weitergegeben werden. WinHTTP erwartet, dass der PAC-Skriptcode eine Funktion mit dem Namen " **FindProxyForURL**" im folgenden Format enthält:
4.  ``` syntax
    FindProxyForURL( url, host );
    ```

    Diese Funktion berechnet eine Liste mit mindestens einem Proxy Server, der vom HTTP-Client verwendet werden kann, um die Anforderung zu übertragen. Wenn das PAC-Skript feststellt, dass der HTTP-Client den Zielserver direkt erreichen kann, ohne einen Proxy Server zu verwenden, bedeutet dies, dass dies mit einem speziellen Rückgabewert erreicht wird.

## <a name="autoproxy-topics"></a>Themen zu AutoProxy

-   [WinHTTP AutoProxy-Funktionen](winhttp-autoproxy-api.md)
-   [Ermittlung ohne automatische Konfigurationsdatei](discovery-without-an-auto-config-file.md)
-   [AutoProxy-Probleme in WinHTTP](autoproxy-issues-in-winhttp.md)
-   [Festlegen von WinInet-Proxy Konfigurationen in WinHTTP](setting-wininet-proxy-configurations-in-winhttp.md)
-   [AutoProxy-Cache](autoproxy-cache.md)
-   [IPv6-Erweiterungen für das Auto-config-Datei Format des Navigators](ipv6-extensions-to-navigator-auto-config-file-format.md)

 

 



