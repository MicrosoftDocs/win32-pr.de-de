---
title: Knoten-nach-Knoten-Zuordnung und Zuordnungsaufbelegung
description: Die Knoten-nach-Knoten-Zuordnung und -Freigabe von Datenstrukturen durch die Stubs ist die Standardmethode der Speicherverwaltung für alle Parameter sowohl auf dem Client als auch auf dem Server.
ms.assetid: 04752fd9-438c-4b52-830b-ce136f83b3b8
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 52aea7c2e95615af8549c1f66476e1a105b91abd68dd31089db9cf23d8ec2af3
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118927839"
---
# <a name="node-by-node-allocation-and-deallocation"></a>Knoten-nach-Knoten-Zuordnung und Zuordnungsaufbelegung

Die Knoten-nach-Knoten-Zuordnung und -Freigabe von Datenstrukturen durch die Stubs ist die Standardmethode der Speicherverwaltung für alle Parameter sowohl auf dem Client als auch auf dem Server. Auf clientseitiger Seite ordnet der Stub jedem Knoten einen separaten Aufruf von [midl \_ user \_ zu.](/windows/desktop/Midl/midl-user-allocate-1) Auf serverseitiger Seite wird nach Möglichkeit privater Arbeitsspeicher verwendet, anstatt **midl \_ user \_ zuzuweisen.** Wenn **midl \_ user \_ allocate** aufgerufen wird, rufen die Serverstubs **midl user \_ \_ free** auf, um die Daten frei zu geben. In den meisten Fällen führt die Verwendung von Knoten-zu-Knoten-Zuordnung und -Zuordnung anstelle von **\[ "allocate" (alle \_ Knoten) \]** zu einer höheren Leistung der serverseitigen Stubs.

 

 