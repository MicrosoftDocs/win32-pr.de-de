---
title: Das Modell für verteilte Systeme
description: Normalerweise führte das System auf mehreren Computern dazu, das System in separate Client-und Serverkomponenten aufzuteilen.
ms.assetid: 6055bcef-e34c-4f2d-92b9-9aec75cf3cec
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 82cd1ea3301d68e77562a63c542bc075692e5192
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "103947544"
---
# <a name="the-model-for-distributed-systems"></a>Das Modell für verteilte Systeme

Normalerweise führte das System auf mehreren Computern dazu, das System in separate Client-und Serverkomponenten aufzuteilen. In solchen Systemen hat die Client Komponente die Benutzeroberfläche verarbeitet, und der Server hat die Back-End-Verarbeitung bereitgestellt, wie z. b. Datenbankzugriff, Drucken usw. Wenn sich die Computer weiter verbreiten, Kosten gesenkt und durch immer höhere Bandbreiten Netzwerke verbunden wurden, wurde das Aufteilen von Softwaresystemen in mehrere Komponenten bequemer, wobei jede Komponente auf einem anderen Computer ausgeführt und eine spezialisierte Funktion durchgeführt wurde. Dieser Ansatz vereinfacht die Entwicklung, Verwaltung, Verwaltung und häufig verbesserte Leistung und Stabilität, da das gesamte System aufgrund eines Fehlers auf einem Computer nicht zwangsläufig deaktiviert wurde.

In vielen Fällen wird dem Client das System als nicht transparente Cloud angezeigt, die die erforderlichen Vorgänge ausführt, auch wenn das verteilte System aus einzelnen Knoten besteht, wie in der folgenden Abbildung dargestellt.

![Clients greifen auf Dienste in einem System von RPC-Servern zu, das als nicht transparente Cloud für externe Clients angezeigt wird](images/indy-nodes.png)

Die Deckkraft der Cloud wird aufrechterhalten, da Computer Vorgänge im Auftrag des Clients aufgerufen werden. Daher können Clients einen Computer (einen *Knoten*) in der Cloud suchen und einen bestimmten Vorgang anfordern. bei der Durchführung des Vorgangs kann dieser Computerfunktionen auf anderen Computern in der Cloud aufrufen, ohne die zusätzlichen Schritte oder den Computer, auf dem Sie ausgeführt wurden, auf dem Client verfügbar zu machen.

Bei diesem Paradigma kann die Mechanik eines verteilten cloudähnlichen Systems in viele einzelne Paket Austausch Vorgänge oder Konversationen zwischen einzelnen Knoten aufgeteilt werden.

Herkömmliche Client/Server-Systeme verfügen über zwei Knoten mit fester Rolle und Zuständigkeiten. Moderne verteilte Systeme können über mehr als zwei Knoten verfügen, und ihre Rollen sind häufig dynamisch. In einer Konversation kann ein Knoten ein Client sein, während in einer anderen Konversation der Knoten der Server sein kann. In vielen Fällen ist der ultimative Consumer der verfügbar gemachten Funktionalität ein Client, bei dem sich ein Benutzer auf der Tastatur befindet und die Ausgabe überwacht. In anderen Fällen funktioniert das verteilte System unbeaufsichtigt und führt Hintergrund Vorgänge aus.

Das verteilte System verfügt möglicherweise nicht über dedizierte Clients und Server für jeden bestimmten Paket Austausch, aber es ist wichtig, sich daran zu erinnern, dass es einen Aufrufer gibt (oder einen Initiator, der häufig als Client bezeichnet wird). Es gibt auch den Empfänger des Aufrufes (wird häufig als Server bezeichnet). Es ist nicht erforderlich, einen bidirektionalen Paket Austausch im Anforderungs-Antwort-Format eines verteilten Systems zu haben. Häufig werden Nachrichten nur eine Möglichkeit gesendet.

 

 




