---
title: Das Modell für verteilte Systeme
description: In der Herkömmlichen bedeutete ein monolithisches System, das auf mehreren Computern ausgeführt wurde, das System in separate Client- und Serverkomponenten zu unterteilen.
ms.assetid: 6055bcef-e34c-4f2d-92b9-9aec75cf3cec
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 859b2a0a83e7f12bd7caf372e60acf2736a114a0cdf46893830032a47a548019
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118924172"
---
# <a name="the-model-for-distributed-systems"></a>Das Modell für verteilte Systeme

In der Herkömmlichen bedeutete ein monolithisches System, das auf mehreren Computern ausgeführt wurde, das System in separate Client- und Serverkomponenten zu unterteilen. In solchen Systemen hat die Clientkomponente die Benutzeroberfläche verarbeitet, und der Server stellt Back-End-Verarbeitung bereit, z. B. Datenbankzugriff, Drucken und so weiter. Mit zunehmender Verbreitung, kostensenkungenden Kosten und immer höheren Bandbreitennetzwerken wurde das Aufteilen von Softwaresystemen in mehrere Komponenten praktischer, da jede Komponente auf einem anderen Computer ausgeführt wird und eine spezielle Funktion ausgeführt wird. Dieser Ansatz hat die Entwicklung, Verwaltung, Verwaltung und häufig verbesserte Leistung und Stabilität vereinfacht, da ein Ausfall auf einem Computer nicht notwendigerweise das gesamte System deaktiviert hat.

In vielen Fällen wird das System dem Client als nicht transparente Cloud angezeigt, die die erforderlichen Vorgänge ausführt, obwohl das verteilte System aus einzelnen Knoten besteht, wie in der folgenden Abbildung dargestellt.

![-Clients greifen auf Dienste in einem System von RPC-Servern zu, das als nicht transparente Cloud für externe Clients angezeigt wird.](images/indy-nodes.png)

Die Deckkraft der Cloud wird beibehalten, da Computingvorgänge im Auftrag des Clients aufgerufen werden. Daher können Clients einen Computer (einen Knoten *)* in der Cloud suchen und einen bestimmten Vorgang anfordern. beim Ausführen des Vorgangs kann dieser Computer Funktionen auf anderen Computern innerhalb der Cloud aufrufen, ohne die zusätzlichen Schritte oder den Computer, auf dem sie ausgeführt wurden, für den Client verfügbar zu machen.

Mit diesem Paradigma kann die Mechanismen eines verteilten, cloudbasierten Systems in viele einzelne Paketaustausche oder Konversationen zwischen einzelnen Knoten aufgeschlüsselt werden.

Herkömmliche Client-Server-Systeme verfügen über zwei Knoten mit festen Rollen und Zuständigkeiten. Moderne verteilte Systeme können über mehr als zwei Knoten verfügen, und ihre Rollen sind häufig dynamisch. In einer Konversation kann ein Knoten ein Client sein, während der Knoten in einer anderen Konversation der Server sein kann. In vielen Fällen ist der letztendliche Consumer der verfügbar gemachten Funktionalität ein Client, bei dem ein Benutzer auf der Tastatur die Ausgabe beobachtet. In anderen Fällen funktioniert das verteilte System unbeaufsichtigt, und es werden Hintergrundvorgänge ausgeführt.

Das verteilte System hat möglicherweise keine dedizierten Clients und Server für jeden bestimmten Paketaustausch, aber es ist wichtig zu beachten, dass es einen Aufrufer (oder Initiator) gibt, der häufig als Client bezeichnet wird. Es gibt auch den Empfänger des Anrufs (häufig als Server bezeichnet). Es ist nicht erforderlich, über einen zweigeteilten Paketaustausch im Anforderung-Antwort-Format eines verteilten Systems zu verfügen. Häufig werden Nachrichten nur auf eine Weise gesendet.

 

 




