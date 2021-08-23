---
title: Verwalten von Netzwerkverbindungssätzen (Zuordnungen)
description: Ab Windows 2000 kann die RPC-Laufzeit mehr als eine Verbindung zwischen client und server aufrechterhalten.
ms.assetid: 9b9c42e9-8ed5-46a6-b6ec-4093ce0128bb
keywords:
- Verwalten von Netzwerkverbindungssätzen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: def88053639c2911dca26d57a080c7fbcbd71728000bee2f12ca7440cb56320b
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118928386"
---
# <a name="managing-network-connection-sets-associations"></a>Verwalten von Netzwerkverbindungssätzen (Zuordnungen)

Ab Windows 2000 kann die RPC-Laufzeit mehr als eine Verbindung zwischen client und server aufrechterhalten. Dies erleichtert den Vorgang für Transporte, die das Ändern der Clientidentität nicht unterstützen, ohne die Verbindung, Multithreadclients und asynchrone Clients wiederherzustellen. Der Satz von Verbindungen zwischen einem Clientprozess und einem Serverendpunkt wird in der RPC-Terminologie als *Zuordnung* bezeichnet. Das Verstehen von Zuordnungen kann die Implementierung von RPC verbessern.

In einem Singlethread-Szenario mit einzelner Clientidentität öffnet RPC eine Verbindung zwischen einem Clientprozess und einem Serverendpunkt, um RPC-Aufrufe vorzunehmen. Wenn ein synchroner RPC-Aufruf erfolgt, sendet der Client die Anforderung über diese Verbindung an den Server und empfängt auch die Antwort darauf. Wenn die Anzahl der Threads, die RPC-Aufrufe im Clientprozess senden, zunimmt, kann sich die Sicherheitsidentität des Clients ändern. Wenn asynchrone/Pipeaufrufe mit synchronen Aufrufen auf dem Client kombiniert werden, benötigt RPC möglicherweise mehr als eine Netzwerkverbindung. Alle Verbindungen in der Gruppe werden in einem Verbindungspool zusammengefasst, der als Zuordnung bezeichnet wird.

Ein synchroner Remoteprozeduraufruf verwendet ausschließlich eine bestimmte Verbindung, um RPC-Standards zu entsprechen. Eine verbindung, die von einem synchronen RPC-Aufruf verwendet wird, gilt als ausgelastet, wenn eine Anforderung gesendet wurde, aber keine Antwort empfangen wurde. Für diese Verbindung ist kein anderer Datenverkehr zulässig, bis die Antwort empfangen wird. Die RPC-Laufzeit versucht, asynchrone Multiplexaufrufe durchzuführen und RPC-Aufrufe über die gleiche Verbindung zu leiten. Synchrone und asynchrone/Pipeaufrufe können nicht mit derselben Verbindung gemischt werden. Dies bedeutet, dass eine bestimmte Verbindung entweder für synchrone RPC-Aufrufe oder für asynchrone/Pipe-RPC-Aufrufe verwendet werden kann.

RPC versucht aggressiv, Verbindungen aus dem Pool wiederzuverwenden. Wenn ein neuer RPC-Aufruf erfolgt, versucht RPC, eine geeignete Verbindung aus dem Pool zu finden, und erstellt nur dann eine neue Verbindung, wenn keine geeignete Verbindung gefunden werden kann. Damit eine Verbindung als geeignet angesehen wird, muss sie:

-   Der entsprechende Typ (synchron oder asynchron/pipe).
-   Sie können kostenlos sein.
-   Sie verfügen über die gleiche Sicherheitsidentität wie das Bindungshandle, für das der Aufruf erfolgt. Wenn die dynamische Identitätsnachverfolgung verwendet wird, wird die Identität des Bindungshandle am Anfang des Aufrufs aus dem Threadtoken aktualisiert. Wenn die statische Identitätsnachverfolgung verwendet wird, wird die Clientidentität verwendet, die auf dem Bindungshandle gestempelt ist.

Wenn der Aufruf abgeschlossen ist, wird die Verbindung nach dem Empfang der Antwort als frei markiert und kann für andere RPC-Aufrufe verwendet werden.

Die Sicherheitsidentität für eine Verbindung kann nicht geändert werden. Wenn beispielsweise eine große Anzahl von Aufrufen an denselben Server unter verschiedenen Sicherheitsidentitäten erfolgt, wächst die Anzahl der Verbindungen im Threadpool. Die Zuordnung selbst wird als Verweis gezählt, und wenn alle Verweise nicht mehr enthalten sind, werden alle Verbindungen beendet und geschlossen. Jedes Bindungshandle und jedes Kontexthandle enthalten einen Verweis auf die Zuordnung. Wenn alle geschlossen sind, verschwindet die Zuordnung. Auf Windows XP werden Zuordnungen nicht notwendigerweise sofort ausgeblendet. sie bleiben möglicherweise für einen kurzen Zeitraum erhalten (der Zielzeitraum beträgt 20 Sekunden, aber die RPC-Laufzeit kann die Zerstörung der Zuordnung verzögern, wenn keine Threads zum Ausführen der Aufgabe verfügbar sind). Wenn die Zuordnung nicht aktiv bleiben soll, nachdem das letzte Kontexthandle/Bindungshandle geschlossen wurde, verwenden Sie die OPTION RPC \_ C \_ OPT \_ DONT \_ LINGER, um die RPC-Runtime zu zwingen, die Verbindung sofort zu schließen.

 

 




