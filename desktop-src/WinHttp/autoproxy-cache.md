---
description: AutoProxy Cache
ms.assetid: 087104e8-ab38-4ba4-be70-23a5ea2bb130
title: AutoProxy Cache
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 45d494f1491dd52484a893dbab601ed4870f03badf5f849dca413f9554a8493e
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119614180"
---
# <a name="autoproxy-cache"></a>AutoProxy Cache

Die [**WinHttpGetProxyForUrl-Funktion**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpgetproxyforurl) führt eine automatische Proxysuche pro Anforderung für die angegebene URL durch. Wenn mehrere Proxys zurückgegeben werden, sollten Clientanwendungen jeden Proxy vor dem Senden der Anforderung testen (weitere Informationen finden Sie im Abschnitt Only One Proxy Server is Currently Supported (Nur ein [Proxyserver](autoproxy-issues-in-winhttp.md) wird derzeit unterstützt) unter AutoProxy Issues in WinHTTP (Probleme mit autoproxy in WinHTTP). Die Informationen in diesem Thema gelten für Aufrufe von **WinHttpGetProxyForUrl,** wenn der Client die automatische Proxyermittlung angibt.

[**WinHttpGetProxyForUrl**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpgetproxyforurl) sucht optional die AUTOPROXY-URL und lädt das Autoproxyskript von dieser Website herunter. WinHttp verwendet das Autoproxyskript, um die Proxyserver zu suchen. Sowohl die AUTOPROXY-URL als auch das Autoproxyskript werden für die angegebene Sitzung zwischengespeichert. Für jede Sitzung werden nur eine AUTOPROXY-URL und ein Skript zwischengespeichert. In der Regel werden das Autoproxyskript und die URL zwischengespeichert, bis sich die dem Computer zugeordnete IP-Adresse ändert. Wenn während eines Aufrufs von **WinHttpGetProxyForUrl** eine neue IP-Adresse erkannt wird, versucht der Aufruf, eine neue AUTOPROXY-URL und ein Neues Skript zu suchen und die Ergebnisse zwischenzuspeichern. Pro Sitzung sollte nur ein Benutzer zugelassen werden, damit die zwischengespeicherten Daten nicht für andere Benutzer auf dem Computer freigegeben werden. Weitere Informationen finden Sie unter [Übersicht über WinHTTP-Sitzungen.](winhttp-sessions-overview.md)

Wenn der Out-of-Process-Dienst aktiv ist, wenn [**WinHttpGetProxyForUrl**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpgetproxyforurl) aufgerufen wird, sind die zwischengespeicherte AUTOPROXY-URL und das Skript für den gesamten Computer verfügbar. Wenn jedoch der Out-of-Process-Dienst verwendet wird und das **Flag fAutoLogonIfCklavged** in der *pAutoProxyOptions-Struktur* true ist, werden die URL und das Skript des automatischen Proxys nicht zwischengespeichert. Daher führt der Aufruf **von WinHttpGetProxyForUrl,** bei dem **das fAutoLogonIfC nach** wie vor auf **TRUE** festgelegt ist, zu zusätzlichen Mehraufwandsvorgängen, die sich auf die Leistung auswirken können. Die folgenden Schritte können verwendet werden, um die Leistung zu verbessern.

**So verbessern Sie die Leistung**

1.  Rufen [**Sie WinHttpGetProxyForUrl auf,**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpgetproxyforurl) und legen Sie dabei den Parameter fAutoLogonIfChallenged auf **false fest.** Die AUTOPROXY-URL und das Skript werden für zukünftige Aufrufe von **WinHttpGetProxyForUrl zwischengespeichert.**
2.  Wenn Schritt 1 mit FEHLER **\_ WINHTTP \_ LOGIN \_ FAILURE** fehlschlägt, rufen Sie [**WinHttpGetProxyForUrl**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpgetproxyforurl) auf, und legen Sie dabei **den Member fAutoLogonIfC zu** TRUE **fest.**

 

 



