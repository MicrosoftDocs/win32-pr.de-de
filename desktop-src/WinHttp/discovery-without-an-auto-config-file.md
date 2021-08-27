---
description: Wenn keine Proxy-Autokonfigurationsdatei im lokalen Netzwerk bereitgestellt wurde, kann WinHttpGetProxyForUrl keinen Proxyserver finden.
ms.assetid: a170e63a-8586-47df-af5e-4ee3621795b2
title: Ermittlung ohne automatische Konfigurationsdatei
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 553f4f798a821ff219b587c494d5dccfbba8c4b22efd0d1692ca2069f53041de
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "120097940"
---
# <a name="discovery-without-an-auto-config-file"></a>Ermittlung ohne automatische Konfigurationsdatei

Wenn keine Proxy-Autokonfigurationsdatei im lokalen Netzwerk bereitgestellt wurde, kann [**WinHttpGetProxyForUrl**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpgetproxyforurl) keinen Proxyserver finden. Wenn **WinHttpGetProxyForUrl** ausfällt, gibt es abhängig von der Laufzeitumgebung mehrere mögliche Fallbackstrategien zum Abrufen einer geeigneten Proxykonfiguration. Dazu gehören die Eingabeaufforderung für die Proxyeinstellung über eine Benutzeroberfläche, das Speichern der Proxykonfiguration in der Registrierung mithilfe des WinHTTP-Hilfsprogramms "ProxyCfg.exe" oder die Verwendung von [**WinHttpGetIEProxyConfigForCurrentUser,**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpgetieproxyconfigforcurrentuser) um zu überprüfen, ob ein Proxyserver in den Einstellungen Internet Explorer aufgeführt ist.

Es ist möglich, dass keine Automatische Proxykonfigurationsdatei vorhanden ist, da der Client über eine direkte Internetverbindung verfügt, z. B. über einen ISP, und keinen Proxyserver benötigt.

Ein Proxyserver ist dagegen möglicherweise erforderlich, aber das lokale Netzwerk unterstützt WPAD möglicherweise nicht. In diesem Fall muss die Proxykonfiguration vom Benutzer abgerufen oder auf dem Clientcomputer gefunden werden.

Eine WinHTTP-basierte Anwendung, die in einer Serverumgebung der mittleren Ebene ausgeführt wird, z. B. eine COM+- oder ASP-Anwendung, sollte sich darauf verlassen, dass ein Serveradministrator eine Standardproxykonfiguration in der Registrierung mithilfe des Hilfsprogramms "ProxyCfg.exe" festlegt. Diese Standardkonfigurationsinformationen können dann entweder mithilfe der [**WinHttpGetDefaultProxyConfiguration-Funktion**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpgetdefaultproxyconfiguration) oder einfach durch Angeben des **\_ \_ \_ PRECONFIG-Flags WINHTTP ACCESS TYPE** im [**WinHttpOpen-Aufruf**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpopen) abgerufen werden.

Andererseits kann eine WinHTTP-Anwendung, die auf einem Clientdesktopcomputer ausgeführt wird, versuchen, die Proxyeinstellungen Internet Explorer zu überprüfen. [**WinHttpGetIEProxyConfigForCurrentUser**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpgetieproxyconfigforcurrentuser) füllt eine vom Aufrufer bereitgestellte [**WINHTTP \_ CURRENT USER \_ \_ IE PROXY \_ \_ CONFIG-Struktur**](/windows/win32/api/winhttp/ns-winhttp-winhttp_current_user_ie_proxy_config) mit den Internet Explorer Proxyeinstellungen des aktuellen Benutzers für die aktuelle aktive Verbindung (DFÜ, VPN oder LAN) aus. Diese Konfiguration kann darauf hinweisen, dass die automatische Erkennung verwendet wird, oder sie kann eine URL für eine Proxy-Autokonfigurationsdatei angeben, oder sie kann einen tatsächlichen Proxyserver angeben, der verwendet werden soll, oder sie kann eine Kombination der drei angeben. Wenn diese Informationen eine PAC-URL oder einen Proxyserver enthalten, kann die WinHTTP-Anwendung versuchen, diese zu verwenden.

Ein Beispiel, das die Funktionen [**WinHttpGetProxyForUrl**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpgetproxyforurl) und [**WinHttpGetIEProxyConfigForCurrentUser**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpgetieproxyconfigforcurrentuser) verwendet, finden Sie in den WinHTTP-Beispielen des Platform Software Development Kit (SDK).

 

 



