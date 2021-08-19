---
description: Beachten Sie die folgenden wichtigen Probleme bei der Verwendung des WinHTTP-Autoproxyfeatures.
ms.assetid: 9bae89b7-8f54-42ec-a240-998c97e26d25
title: AutoProxy-Probleme in WinHTTP
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: cc07ca7320fee028431ff0d89be78ee0b2dc4bb63e8191386808f0936c8a1518
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119052088"
---
# <a name="autoproxy-issues-in-winhttp"></a>AutoProxy-Probleme in WinHTTP

Beachten Sie die folgenden wichtigen Probleme bei der Verwendung des WinHTTP-Autoproxyfeatures.

## <a name="only-one-proxy-server-is-currently-supported"></a>Derzeit wird nur ein Proxyserver unterstützt.

WinHTTP unterstützt derzeit keine Proxykonfigurationen, die mehr als einen Proxyserver angeben. Wenn [**WinHttpGetProxyForUrl**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpgetproxyforurl) eine [**WINHTTP \_ PROXY \_ INFO-Struktur**](/windows/win32/api/winhttp/ns-winhttp-winhttp_proxy_info) zurückgibt, die eine Liste von Proxyservern enthält, die die Anwendung dann mithilfe der **WINHTTP OPTION \_ \_ PROXY-Option** für das Anforderungshandle festlegt, verwendet WinHTTP nur den ersten Proxyserver in der Liste. Wenn auf diesen Proxyserver nicht zugegriffen werden kann, führt WinHTTP kein Failover auf einen der anderen Proxyserver in der Liste aus. Es liegt an der Anwendung, diesen Fall zu behandeln, indem die **WINHTTP \_ OPTION \_ PROXY-Option** erneut mit dem nächsten Proxyserver in der Liste festgelegt und die Anforderung erneut gesendet wird.

## <a name="security-risk-mitigation"></a>Entschärfung von Sicherheitsrisiken

Zum Verarbeiten der automatischen Proxykonfigurationsdatei muss der heruntergeladene Skriptcode ausgeführt werden. Einige zu berücksichtigende Sicherheitsrisiken: Wenn der Server, auf dem sich die PAC-Datei befindet, kompromittiert wurde, ist es möglich, dass der PAC-Skriptcode schädlich ist. Aus diesem Grund verwendet WinHTTP die folgenden Vorsichtsmaßnahmen, um den Client zu schützen:

1.  Der Skriptcode kann keine ActiveX Objekte instanziieren. Dadurch werden viele potenziell gefährlichen Funktionen blockiert, z. B. die Möglichkeit, auf Dateien zuzugreifen und Netzwerk-E/A durchzuführen.
2.  **Windows Server 2003: **[**WinHttpGetProxyForUrl**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpgetproxyforurl) delegiert die gesamte WPAD-Verarbeitung an einen externen Out-of-Process-Dienst, den automatischen WinHTTP-Webproxyermittlungsdienst, der unter dem integrierten Benutzerkonto des lokalen Diensts mit geringen Berechtigungen ausgeführt wird.

3.  **Windows XP mit SP2 und Windows Server 2003:** Ein PAC-Skript darf nicht länger als 60 Sekunden ausgeführt werden, danach wird die Skriptausführung beendet.

4.  **Windows XP mit SP2 und Windows Server 2003:** WinHTTP lehnt PAC-Dateien ab, die größer als 1 MB sind. Eine typische PAC-Datei ist in der Regel nicht mehr als einige Kilobyte groß.

Beachten Sie, dass die Verarbeitung des PAC-Skriptcodes die Verwendung von COM erfordert, da WinHTTP Microsoft JScript Komponente verwendet, um das Skript auszuführen. Wenn WinHTTP die WPAD-Protokollverarbeitung nicht an einen externen, out-of-process-Webproxy-Dienst für die automatische Ermittlung delegieren kann, lädt [**WinHttpGetProxyForUrl**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpgetproxyforurl) die COM-Runtime innerhalb des Anwendungsprozesses für die Dauer des Aufrufs. Wenn die Anwendung selbst bereits COM verwendet, sollte dies kein Problem sein.

## <a name="performance-considerations"></a>Überlegungen zur Leistung

Der Prozess der automatischen Erkennung kann langsam sein, möglicherweise bis zu mehrere Sekunden. Die Funktionen [**WinHttpGetProxyForUrl**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpgetproxyforurl) und [WinHttpDetectAutoProxyConfigUrl](/windows/desktop/api/Winhttp/nf-winhttp-winhttpdetectautoproxyconfigurl) sind blockierende, synchrone Funktionen. Es kann sein, dass ein bestimmter Mechanismus für die automatische Erkennung (z. B. DHCP) viel langsamer ist als der andere (z. B. DNS). Wenn sowohl die **\_ \_ \_ \_ DHCP-Flags WINHTTP AUTO DETECT TYPE** und **WINHTTP AUTO DETECT TYPE \_ \_ DNS \_ \_ \_ A** auto-detection angegeben sind, verwendet WinHTTP zuerst DHCP gemäß der WPAD-Spezifikation. Wenn keine PAC-URL ermittelt wird, indem eine DHCP-Anforderung ausgegeben wird, versucht WinHTTP, die PAC-Datei an einer bekannten DNS-Adresse zu finden.

[**WinHttpGetProxyForUrl**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpgetproxyforurl) verwendet den WinHTTP-Sitzungshandleparameter zum Zwischenspeichern der PAC-Datei und der Ergebnisse der automatischen Erkennung. Es empfiehlt sich, nach Möglichkeit das gleiche Sitzungshandle für mehrere **WinHttpGetProxyForUrl-Aufrufe** zu verwenden, um eine wiederholte PAC-URL-Erkennung und das Herunterladen von Dateien zu vermeiden. Die PAC-Datei wird nur im Arbeitsspeicher zwischengespeichert und verworfen, wenn die Anwendung das Sitzungshandle schließt.

Aufgrund der Auswirkungen von Autoproxy auf die Leistung wird empfohlen, dass nur Desktopclientanwendungen oder -dienste das Feature verwenden. Serverbasierte Anwendungen sollten sich auf den Serveradministrator verlassen, der das Hilfsprogramm "ProxyCfg.exe" verwendet.

 

 



