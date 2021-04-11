---
title: Verwalten von Netzwerk Verbindungs Sätzen (Zuordnungen)
description: Ab Windows 2000 kann für die RPC-Laufzeit mehr als eine Verbindung zwischen dem Client und dem Server beibehalten werden.
ms.assetid: 9b9c42e9-8ed5-46a6-b6ec-4093ce0128bb
keywords:
- Verwalten von Netzwerk Verbindungs Sätzen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 81e99afe23d90e44d85dc7a2ec9301b45e1f20b1
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "104207114"
---
# <a name="managing-network-connection-sets-associations"></a>Verwalten von Netzwerk Verbindungs Sätzen (Zuordnungen)

Ab Windows 2000 kann für die RPC-Laufzeit mehr als eine Verbindung zwischen dem Client und dem Server beibehalten werden. Dies erleichtert den Betrieb für Transporte, die das Ändern der Client Identität nicht unterstützen, ohne dass die Verbindung, Multithread-Clients und asynchrone Clients wieder hergestellt werden müssen. Der Satz von Verbindungen zwischen einem Client Prozess und einem Server Endpunkt wird in der RPC-Terminologie als " *Association* " bezeichnet. Das Verständnis von Zuordnungen kann die Implementierung von RPC verbessern.

In einem Szenario mit einem Single-Client-Identitäts Szenario öffnet RPC eine Verbindung zwischen einem Client Prozess und einem Server Endpunkt, um RPC-Aufrufe durchführen zu können. Wenn ein synchroner RPC-Aufruf durchgeführt wird, sendet der Client die Anforderung an den Server über diese Verbindung und erhält auch die Antwort darauf. Wenn die Anzahl der Threads, die RPC-Aufrufe im Client Prozess bewirken, zunimmt, kann sich die Sicherheitsidentität des Clients ändern. Wenn asynchrone/Pipe-Aufrufe mit synchronen Aufrufen auf dem Client gemischt werden, benötigt RPC möglicherweise mehr als eine Netzwerkverbindung. Alle Verbindungen im Satz werden in einen Verbindungspool eingefügt, der als Zuordnung bezeichnet wird.

Ein synchroner Remote Prozedur Aufruf verwendet exklusiv eine angegebene Verbindung, um die RPC-Standards einzuhalten. Eine Verbindung, die von einem synchronen RPC-Aufruf verwendet wird, wird als ausgelastet betrachtet, wenn eine Anforderung gesendet wurde, aber keine Antwort empfangen wurde. Es ist kein anderer Datenverkehr für diese Verbindung zulässig, bis die Antwort empfangen wurde. Die RPC-Laufzeit versucht, asynchrone und Weiterleiten von RPC-Aufrufen über dieselbe Verbindung auszuführen. Synchrone und asynchrone/Pipe-Aufrufe können nicht mit derselben Verbindung gemischt werden, d. h., eine gegebene Verbindung kann für synchrone RPC-Aufrufe oder für asynchrone/Pipe-RPC-Aufrufe verwendet werden.

RPC versucht aggressiv, Verbindungen aus dem Pool wiederzuverwenden. Wenn ein neuer RPC-Aufruf erfolgt, versucht RPC, eine geeignete Verbindung aus dem Pool zu finden, und erstellt nur dann eine neue Verbindung, wenn eine geeignete Verbindung nicht gefunden werden kann. Damit eine Verbindung als geeignet eingestuft wird, muss Sie folgende Schritte ausführen:

-   Der geeignete Typ (synchron oder asynchron/Pipe).
-   Kostenlos.
-   Sie haben dieselbe Sicherheitsidentität wie das Bindungs handle, für das der-Befehl durchgeführt wird. Wenn die dynamische Identitäts Verfolgung verwendet wird, wird die Identität des Bindungs Handles am Anfang des Aufrufes aus dem Thread Token aktualisiert. Wenn die statische Identitäts Nachverfolgung verwendet wird, wird die Client Identität verwendet, die für das Bindungs handle gestempelt wird.

Wenn der Aufruf beendet ist, wird die Verbindung nach dem Empfang der Antwort als frei markiert und kann für andere RPC-Aufrufe verwendet werden.

Die Sicherheitsidentität für eine Verbindung kann nicht geändert werden. Wenn z. b. eine große Anzahl von Aufrufen desselben Servers unter verschiedenen Sicherheits Identitäten durchgeführt wird, wächst die Anzahl der Verbindungen im Thread Pool. Die Zuordnung selbst ist Verweis Zählung, und wenn alle Verweise nicht mehr vorhanden sind, werden alle Verbindungen angehalten und geschlossen. Jedes Bindungs Handle und jedes Kontext Handle enthalten einen Verweis auf die Zuordnung. Wenn alle geschlossen sind, verschwindet die Zuordnung. Unter Windows XP verschwinden Zuordnungen nicht notwendigerweise sofort. Sie bleiben möglicherweise für einen kurzen Zeitraum erhalten (der zielzeitraum beträgt 20 Sekunden, aber die RPC-Laufzeit kann das zerstören der Zuordnung verzögern, wenn keine Threads zum Ausführen der Aufgabe verfügbar sind). Wenn Sie nicht möchten, dass die Zuordnung aktiv bleibt, nachdem das letzte Kontext Handle/Bindungs Handle geschlossen wurde, verwenden Sie \_ die \_ Option RPC C opt dont LINGER, um zu erzwingen, dass die RPC- \_ \_ Laufzeit die Verbindung sofort schließt.

 

 




