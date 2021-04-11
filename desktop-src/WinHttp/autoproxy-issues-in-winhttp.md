---
description: Beachten Sie die folgenden wichtigen Probleme bei der Verwendung der Funktion "WinHTTP aktivierter automatischer Proxy".
ms.assetid: 9bae89b7-8f54-42ec-a240-998c97e26d25
title: AutoProxy-Probleme in WinHTTP
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 22c6edbf56ec1ffc4dfac930a5d4858429cc6447
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "104217614"
---
# <a name="autoproxy-issues-in-winhttp"></a>AutoProxy-Probleme in WinHTTP

Beachten Sie die folgenden wichtigen Probleme bei der Verwendung der Funktion "WinHTTP aktivierter automatischer Proxy".

## <a name="only-one-proxy-server-is-currently-supported"></a>Zurzeit wird nur ein Proxy Server unterstützt.

Von WinHTTP werden derzeit keine Proxy Konfigurationen unterstützt, die mehr als einen Proxy Server angeben. Wenn [**WinHttpGetProxyForUrl**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpgetproxyforurl) eine [**WinHTTP- \_ Proxy \_ Informations**](/windows/win32/api/winhttp/ns-winhttp-winhttp_proxy_info) Struktur zurückgibt, die eine Liste von Proxy Servern enthält, die von der Anwendung dann auf dem Anforderungs Handle mithilfe der **WinHTTP- \_ Option \_ Proxy** -Option festgelegt wird, verwendet WinHTTP nur den ersten Proxy Server in der Liste. Wenn auf diesen Proxy Server nicht zugegriffen werden kann, führt WinHTTP kein Failover auf einen der anderen Proxy Server in der Liste aus. Es ist für die Anwendung von der Anwendung, diesen Fall zu behandeln, indem die **\_ Option \_ Proxy Option WinHTTP** erneut mit dem nächsten Proxy Server in der Liste festgelegt und die Anforderung erneut gesendet wird.

## <a name="security-risk-mitigation"></a>Minderung von Sicherheitsrisiken

Zum Verarbeiten der automatischen Proxy Konfigurationsdatei muss der heruntergeladene Skriptcode ausgeführt werden. Zu berücksichtigende Sicherheitsbedenken: Wenn der Server, auf dem sich die PAC-Datei befindet, kompromittiert wurde, ist der PAC-Skriptcode möglicherweise bösartig. Daher verwendet WinHTTP die folgenden Vorsichtsmaßnahmen zum Schutz des Clients:

1.  Der Skriptcode wird daran gehindert, ActiveX-Objekte zu instanziieren. Dies blockiert viele potenziell gefährliche Funktionen, wie z. b. die Fähigkeit, auf Dateien zuzugreifen und Netzwerk-e/a auszuführen.
2.  * * Windows Server 2003: * *[**WinHttpGetProxyForUrl**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpgetproxyforurl) delegiert die gesamte WPAD-Verarbeitung an einen externen Prozess externen Dienst, den Dienst für die automatische Ermittlung von WinHTTP-Webproxys, der unter dem integrierten Benutzerkonto des lokalen Diensts mit geringen Berechtigungen ausgeführt wird.

3.  **Windows XP mit SP2 und Windows Server 2003:** Ein PAC-Skript kann nicht länger als 60 Sekunden ausgeführt werden, nachdem die Skriptausführung beendet wurde.

4.  **Windows XP mit SP2 und Windows Server 2003:** WinHTTP lehnt PAC-Dateien ab, die größer als 1 MB sind. Eine typische PAC-Datei ist in der Regel nicht mehr als ein paar Kilobyte groß.

Beachten Sie, dass die Verarbeitung des PAC-Skriptcodes die Verwendung von com erfordert, da WinHTTP die Microsoft JScript-Komponente zum Ausführen des Skripts verwendet. Wenn die WPAD-Protokoll Verarbeitung von WinHTTP nicht an einen externen, Prozess externen WebProxy-Dienst für die automatische Ermittlung delegiert werden kann, lädt [**WinHttpGetProxyForUrl**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpgetproxyforurl) die com-Laufzeit innerhalb des Anwendungsprozesses für die Dauer des Aufrufes. Wenn die Anwendung selbst bereits com verwendet, sollte dies kein Problem sein.

## <a name="performance-considerations"></a>Überlegungen zur Leistung

Der Prozess für die automatische Erkennung kann langsam sein, möglicherweise so lange wie mehrere Sekunden. Die Funktionen " [**WinHttpGetProxyForUrl**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpgetproxyforurl) " und " [winhttpdetectautoproxyconfigurl](/windows/desktop/api/Winhttp/nf-winhttp-winhttpdetectautoproxyconfigurl) " blockieren synchrone Funktionen. Es kann sein, dass ein bestimmter Mechanismus zur automatischen Erkennung (z. b. DHCP) wesentlich langsamer ist als der andere (z. b. DNS). Wenn sowohl der **\_ \_ \_ \_ DHCP** -als auch der automatische Erkennungs- **\_ \_ \_ \_ DNS \_ -Typ** für die automatische Erkennung von WinHTTP automatisch erkannt werden, verwendet WinHTTP DHCP zuerst in Übereinstimmung mit der WPAD-Spezifikation. Wenn keine PAC-URL erkannt wird, indem eine DHCP-Anforderung ausgegeben wird, versucht WinHTTP, die PAC-Datei unter einer bekannten DNS-Adresse zu finden.

[**WinHttpGetProxyForUrl**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpgetproxyforurl) verwendet den WinHTTP-Sitzungshandle-Parameter zum Zwischenspeichern der PAC-Datei und die Ergebnisse der automatischen Erkennung. Es empfiehlt sich, nach Möglichkeit dasselbe Sitzungs Handle für mehrere **WinHttpGetProxyForUrl** -Aufrufe zu verwenden, um eine wiederholte PAC-URL-Erkennung und das Herunterladen von Dateien zu vermeiden. Die PAC-Datei wird nur im Arbeitsspeicher zwischengespeichert und wird verworfen, wenn die Anwendung das Sitzungs handle schließt.

Aufgrund der Auswirkungen auf die Leistung von AutoProxy wird empfohlen, dass die Funktion nur von Desktop Client Anwendungen oder-Diensten verwendet wird. serverbasierte Anwendungen sollten sich auf den Server Administrator mit dem Hilfsprogramm "ProxyCfg.exe" stützen.

 

 



