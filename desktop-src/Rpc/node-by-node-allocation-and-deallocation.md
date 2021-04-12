---
title: Zuordnung und Aufhebung der Zuordnung von Knoten zu Knoten
description: Die Zuordnung von Knoten zu Knoten und die Aufhebung der Zuordnung von Datenstrukturen durch die stusb ist die Standardmethode der Speicherverwaltung für alle Parameter auf dem Client und dem Server.
ms.assetid: 04752fd9-438c-4b52-830b-ce136f83b3b8
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b6cc6b3ff61d4db3ba716664a2ff854e94cb28fc
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "104473637"
---
# <a name="node-by-node-allocation-and-deallocation"></a>Zuordnung und Aufhebung der Zuordnung von Knoten zu Knoten

Die Zuordnung von Knoten zu Knoten und die Aufhebung der Zuordnung von Datenstrukturen durch die stusb ist die Standardmethode der Speicherverwaltung für alle Parameter auf dem Client und dem Server. Auf der Clientseite ordnet der Stub jeden Knoten einem separaten aufrufszuordnungs- [ \_ Benutzer \_ ](/windows/desktop/Midl/midl-user-allocate-1)Namen zu. Auf der Serverseite wird anstelle des Aufrufs von " **Mittel l- \_ Benutzer \_**" der private Arbeitsspeicher verwendet, wann immer dies möglich ist. Wenn die **mittlere \_ Benutzer \_** Zuordnungen aufgerufen werden, ruft der serverstubvorgang die **\_ Benutzer \_ kostenlos** auf, um die Daten freizugeben. In den meisten Fällen führt die Verwendung der Zuordnung von Knoten zu Knoten und das Aufheben der Zuordnung anstelle der Verwendung von " **\[ zuordnen" (alle \_ Knoten) \]** zu einer verbesserten Leistung der serverseitigen Stubdaten.

 

 