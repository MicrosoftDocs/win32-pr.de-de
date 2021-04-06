---
title: Konsistenz-GUIDs
description: Konsistenz-GUIDs stellen eine Erkennungs Strategie dar, die es einer Anwendung ermöglicht, partielle Updates zu erkennen.
ms.assetid: 3418667f-4d5a-4a4b-b0f5-7744a21608f7
ms.tgt_platform: multiple
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8bcfb25d0f04a459217811a2ff0393fac47e3206
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "104036256"
---
# <a name="consistency-guids"></a>Konsistenz-GUIDs

Konsistenz-GUIDs stellen eine Erkennungs Strategie dar, die es einer Anwendung ermöglicht, partielle Updates zu erkennen. Eine Konsistenz-GUID (Global Unique Identifier) wird auf jedes Objekt in einem verknüpften Satz angewendet. In der Implementierung generiert eine Quell Anwendung eine neue GUID und wendet Sie auf jedes Objekt an, das Sie in der Gruppe verwandter Objekte aktualisiert. Anschließend wendet Sie die neue GUID auf die restlichen Objekte in der Menge an und wird beendet, indem die neue GUID auf das "Master"-Objekt angewendet wird. In der Regel handelt es sich bei dem "Master"-Objekt um einen Container, der das übergeordnete Element der anderen Objekte in der Menge ist.

Wichtige Hinweise:

-   Konsistenz-GUIDs, die mit Objekt Zählungen oder Prüfsummen kombiniert werden, sind effektiver als Konsistenz-GUIDs, da die Anwendung, die die Objekte liest, möglicherweise nicht weiß, wie viele Objekte mit der GUID vorhanden sein sollten.
-   Anwendungen müssen eigene GUIDs generieren (eine Microsoft Win32-API, uuidcreate, bietet diese Funktion) und nicht die vom System generierten GUIDs verwenden, die im **objectGUID** -Attribut eines Objekts gefunden werden. Dies liegt daran, dass eine Konsistenz-GUID bei jeder Aktualisierung des Satzes von Objekten geändert werden muss. Objektidentitäts-GUIDs, die in " **objectGUID** " gefunden werden, werden nach dem Erstellen des Objekts nie geändert.
-   Bei Konsistenz-GUIDs wird davon ausgegangen, dass kein Objekt von Mengen gemeinsam verwendet wird, sodass jede Menge eine eindeutige Konsistenz-GUID aufweisen kann.

 

 




