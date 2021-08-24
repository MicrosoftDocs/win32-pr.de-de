---
description: Um die Konfiguration von Proxyeinstellungen zu vereinfachen, implementiert WinHTTP 5.1 das WPAD-Protokoll (Web Proxy Auto-Discovery), das auch als Autoproxy bezeichnet wird.
ms.assetid: f766f37b-a1aa-420f-ac3b-d03485630d88
title: WinHTTP AutoProxy-Unterstützung
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b0f6a07645fd7d8bcd401bf399d2a9f525499c4d3a725e49b9d170c067092f70
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119614080"
---
# <a name="winhttp-autoproxy-support"></a>WinHTTP AutoProxy-Unterstützung

Um die Konfiguration von Proxyeinstellungen zu vereinfachen, implementiert WinHTTP 5.1 das WPAD-Protokoll (Web Proxy Auto-Discovery), das auch als Autoproxy bezeichnet wird.

## <a name="overview-of-autoproxy"></a>Übersicht über AutoProxy

Anwendungen und Komponenten, die WinHTTP zum Senden von HTTP-Anforderungen verwenden, sollten sicherstellen, dass die Proxykonfiguration ordnungsgemäß festgelegt ist. Sofern der Client keine direkte Internetverbindung hat, sollte eine HTTP-Anforderung normalerweise über einen Webproxyserver gesendet werden, der das lokale Netzwerk des Clients mit dem Internet verbindet (dies ist z. B. häufig bei Webclients in einem Unternehmens-LAN der Fall). Bei serverbasierten Anwendungen wird die Proxykonfiguration normalerweise vom Administrator des Servers mithilfe des WinHTTP-hilfsprogramms ProxyCfg.exe verwaltet. Der Serveradministrator kennt den Namen des Proxyservers im Voraus und verwendet ProxyCfg.exe, um diese Einstellung in der Registrierung aufzuzeichnen, in der WinHTTP ihn suchen kann. Es ist jedoch problematisch, dass Clientdesktop-Endbenutzer WinHTTP-Proxyeinstellungen manuell konfigurieren müssen. Der Endbenutzer kennt den Namen des Proxyservers möglicherweise nicht. Die Anforderung, dass der Endbenutzer das hilfsprogramm ProxyCfg.exe ausführen muss, kann eine Supportlast für eine Organisation darstellen. Um eine gute Benutzererfahrung zu unterstützen, sollte eine webfähige Clientanwendung die Proxykonfiguration ohne Benutzereingriff bestimmen.

Um die Konfiguration der Proxyeinstellungen für WinHTTP-basierte Anwendungen zu vereinfachen, implementiert WinHTTP jetzt das [WPAD-Protokoll (Web Proxy Auto-Discovery),](https://tools.ietf.org/html/draft-ietf-wrec-wpad-01)das häufig als *autoproxy* bezeichnet wird. Dies ist dasselbe Protokoll, das Webbrowser implementieren, um die Proxykonfiguration automatisch zu ermitteln, ohne dass ein Endbenutzer einen Proxyserver manuell angeben muss. Dieses Feature ist ab WinHTTP Version 5.1 in Windows 2000 Service Pack 3, Windows XP Service Pack 1 und Windows Server 2003 verfügbar. Beachten Sie, dass zwar sowohl Microsoft Internet Explorer als auch Microsoft WinHTTP WPAD unterstützen, die Spezifikation jedoch nie über die Phase "Internet-Draft" hinausgeht und im Mai 2001 abgelaufen ist.

Das WPAD-Protokoll funktioniert wie folgt:

1.  Mithilfe der DHCP- und/oder DNS-Netzwerkprotokolle wird die URL einer PAC-Datei (Proxy Auto-Configuration) ermittelt. Die URL identifiziert eine PAC-Datei im lokalen Netzwerk des Clients. WinHTTP unterstützt nur DIE PAC-URLs "http:" und "https:". sie unterstützt z. B. keine "file:"-URLs.
2.  Die PAC-Datei wird heruntergeladen und optional auf dem Clientcomputer zwischengespeichert. Die PAC-Datei ist ein ausführbares Skript, das eine Liste von einem oder mehreren Proxyservern generiert, wenn ein Zielhostname und eine URL angegeben werden. WinHTTP unterstützt nur ECMAScript-basierte PAC-Dateien.
3.  Bei jeder HTTP-Anforderung wird der PAC-Skriptcode ausgeführt, wobei der Hostname und die URL der HTTP-Anforderung als Parameter übergeben werden. WinHTTP erwartet, dass der PAC-Skriptcode eine Funktion namens **FindProxyForURL** im Format enthält:
4.  ``` syntax
    FindProxyForURL( url, host );
    ```

    Diese Funktion berechnet eine Liste von einem oder mehreren Proxyservern, die vom HTTP-Client verwendet werden können, um die Anforderung zu übertragen. Wenn das PAC-Skript feststellt, dass der HTTP-Client den Zielserver direkt erreichen kann, ohne überhaupt einen Proxyserver zu durchlaufen, wird dies mit einem speziellen Rückgabewert angegeben.

## <a name="autoproxy-topics"></a>AutoProxy-Themen

-   [WinHTTP AutoProxy-Funktionen](winhttp-autoproxy-api.md)
-   [Ermittlung ohne automatische Konfigurationsdatei](discovery-without-an-auto-config-file.md)
-   [AutoProxy-Probleme in WinHTTP](autoproxy-issues-in-winhttp.md)
-   [Festlegen von WinInet-Proxykonfigurationen in WinHTTP](setting-wininet-proxy-configurations-in-winhttp.md)
-   [AutoProxy Cache](autoproxy-cache.md)
-   [IPv6-Erweiterungen für das Navigator-Dateiformat für die automatische Konfiguration](ipv6-extensions-to-navigator-auto-config-file-format.md)

 

 



