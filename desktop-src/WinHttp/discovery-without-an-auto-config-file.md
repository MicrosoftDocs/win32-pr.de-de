---
description: Wenn eine Datei für die automatische Proxykonfiguration nicht im lokalen Netzwerk bereitgestellt wurde, kann WinHttpGetProxyForUrl keinen Proxy Server finden.
ms.assetid: a170e63a-8586-47df-af5e-4ee3621795b2
title: Ermittlung ohne automatische Konfigurationsdatei
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b6a5ec281c2ef74e2a377cecbd30f16cbc49bd79
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106353222"
---
# <a name="discovery-without-an-auto-config-file"></a>Ermittlung ohne automatische Konfigurationsdatei

Wenn eine Datei für die automatische Proxykonfiguration nicht im lokalen Netzwerk bereitgestellt wurde, kann [**WinHttpGetProxyForUrl**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpgetproxyforurl) keinen Proxy Server finden. Wenn **WinHttpGetProxyForUrl** fehlschlägt, gibt es mehrere mögliche Fall Back Strategien, um eine geeignete Proxykonfiguration zu erhalten, abhängig von ihrer Laufzeitumgebung. Dazu gehört die Aufforderung zur Proxy Einstellung über eine Benutzeroberfläche, die das Speichern der Proxykonfiguration in der Registrierung mit dem WinHTTP-Hilfsprogramm "ProxyCfg.exe" oder das Verwenden von [**WinHttpGetIEProxyConfigForCurrentUser**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpgetieproxyconfigforcurrentuser) erfordert, um zu überprüfen, ob ein Proxy Server in den Einstellungen von Internet Explorer aufgeführt ist.

Es ist möglich, dass keine automatische Proxy Konfigurationsdatei vorhanden ist, da der Client über eine direkte Internet Verbindung verfügt, z. b. über einen ISP und keinen Proxy Server benötigt.

Möglicherweise ist auch ein Proxy Server erforderlich, aber das lokale Netzwerk unterstützt WPAD möglicherweise nicht. In diesem Fall muss die Proxykonfiguration vom Benutzer abgerufen oder irgendwo auf dem Client Computer gefunden werden.

Eine auf WinHTTP basierende Anwendung, die in einer Serverumgebung der mittleren Ebene ausgeführt wird, z. b. eine com+-oder ASP-Anwendung, sollte sich darauf verlassen, dass ein Server Administrator eine Standard Proxykonfiguration in der Registrierung unter Verwendung des Hilfsprogramms "ProxyCfg.exe" festlegt. Diese Standard Konfigurationsinformationen können dann entweder mithilfe der [**WinHttpGetDefaultProxyConfiguration**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpgetdefaultproxyconfiguration) -Funktion oder einfach durch Angeben des **WinHTTP- \_ \_ Zugriffstyp- \_ preconfig** -Flags im [**WinHttpOpen**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpopen) -Befehl abgerufen werden.

Auf der anderen Seite kann eine WinHTTP-Anwendung, die auf einem Client Desktop Computer ausgeführt wird, versuchen, die Proxy Einstellungen von Internet Explorer zu untersuchen. [**WinHttpGetIEProxyConfigForCurrentUser**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpgetieproxyconfigforcurrentuser) füllt eine vom Aufrufer angegebene WinHTTP-Vorlage für den [**\_ aktuellen \_ Benutzer- \_ \_ /proxykonfigurationsstruktur \_**](/windows/win32/api/winhttp/ns-winhttp-winhttp_current_user_ie_proxy_config) mit den Internet Explorer-Proxy Einstellungen des aktuellen Benutzers für die aktuelle aktive Verbindung (DFÜ, VPN oder LAN). Diese Konfiguration kann darauf hindeuten, dass die automatische Erkennung verwendet wird, oder es kann eine URL für eine automatische Proxy Konfigurationsdatei angegeben werden, oder es kann ein tatsächlicher Proxy Server angegeben werden, der verwendet werden soll, oder es kann eine Kombination der drei Werte angegeben werden. Wenn diese Informationen eine PAC-URL oder einen Proxy Server enthalten, kann Sie von der WinHTTP-Anwendung verwendet werden.

Ein Beispiel, in dem die Funktionen [**WinHttpGetProxyForUrl**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpgetproxyforurl) und [**WinHttpGetIEProxyConfigForCurrentUser**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpgetieproxyconfigforcurrentuser) verwendet werden, finden Sie unter WinHTTP-Beispiele für das Platform Software Development Kit (SDK).

 

 



