---
description: AutoProxy-Cache
ms.assetid: 087104e8-ab38-4ba4-be70-23a5ea2bb130
title: AutoProxy-Cache
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6d0492bec116bad8a82da0e961cf6d851d27c787
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106362954"
---
# <a name="autoproxy-cache"></a>AutoProxy-Cache

Die [**WinHttpGetProxyForUrl**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpgetproxyforurl) -Funktion führt die aktivierter automatischer Proxy-Suche pro Anforderung für die angegebene URL aus. Wenn mehrere Proxys zurückgegeben werden, sollten Client Anwendungen jeden Proxy vor dem Senden der Anforderung testen (Weitere Informationen finden Sie im Abschnitt [nur ein Proxy Server wird zurzeit unterstützt](autoproxy-issues-in-winhttp.md) in AutoProxy-Problemen in WinHTTP). Die Informationen in diesem Thema gelten für Aufrufe von **WinHttpGetProxyForUrl** , wenn der Client die automatische Proxy Ermittlung angibt.

[**WinHttpGetProxyForUrl**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpgetproxyforurl) gibt optional die aktivierter automatischer Proxy-URL an und lädt das aktivierter automatischer Proxy-Skript von dieser Website herunter. WinHTTP verwendet das aktivierter automatischer Proxy-Skript, um die Proxy Server zu suchen. Sowohl die aktivierter automatischer Proxy-URL als auch das aktivierter automatischer Proxy-Skript werden für die angegebene Sitzung zwischengespeichert. Es werden nur eine aktivierter automatischer Proxy-URL und ein Skript für jede Sitzung zwischengespeichert. Normalerweise werden das aktivierter automatischer Proxy-Skript und die URL zwischengespeichert, bis sich die IP-Adresse ändert, die dem Computer zugeordnet ist. Wenn während eines Aufrufens von **WinHttpGetProxyForUrl** eine neue IP-Adresse erkannt wird, versucht der-Befehl, eine neue aktivierter automatischer Proxy-URL zu suchen und die Ergebnisse zwischenzuspeichern. Pro Sitzung darf nur ein Benutzer zugelassen werden, damit die zwischengespeicherten Daten nicht für andere Benutzer auf dem Computer freigegeben werden. Weitere Informationen finden Sie unter [Übersicht über WinHTTP-Sitzungen](winhttp-sessions-overview.md).

Wenn der Out-of-Process-Dienst aktiv ist, wenn [**WinHttpGetProxyForUrl**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpgetproxyforurl) aufgerufen wird, sind die zwischengespeicherten aktivierter automatischer Proxy-URL und das Skript für den gesamten Computer verfügbar. Wenn der Out-of-Process-Dienst verwendet wird und das Flag " **fautologonif** " in der " *pautoproxyoptions* "-Struktur "true" ist, werden die aktivierter automatischer Proxy-URL und das Skript nicht zwischengespeichert. Daher führt das Aufrufen von **WinHttpGetProxyForUrl** mit dem auf **true** festgelegten Element **fautologonifforderer** zu zusätzlichen Verarbeitungsvorgängen, die sich auf die Leistung auswirken können. Die folgenden Schritte können verwendet werden, um die Leistung zu verbessern.

**Verbessern der Leistung**

1.  Aufrufen von [**WinHttpGetProxyForUrl**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpgetproxyforurl) , wobei der Parameter "fautologonifforce" auf " **false**" festgelegt ist. Die aktivierter automatischer Proxy-URL und das Skript werden für zukünftige Aufrufe von **WinHttpGetProxyForUrl** zwischengespeichert.
2.  Wenn Schritt 1 fehlschlägt, **bei \_ WinHTTP- \_ Anmelde \_ Fehler ein Fehler** auftritt, müssen Sie [**WinHttpGetProxyForUrl**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpgetproxyforurl) aufrufen, wobei das Element **fautologonifforderer** auf **true** festgelegt ist.

 

 



