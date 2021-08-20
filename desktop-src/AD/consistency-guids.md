---
title: Konsistenz-GUIDs
description: Konsistenz-GUIDs sind eine Erkennungsstrategie, mit der eine Anwendung Teilupdates erkennen kann.
ms.assetid: 3418667f-4d5a-4a4b-b0f5-7744a21608f7
ms.tgt_platform: multiple
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: aa0a6f0105ebc7732303f74afdebba33883a9d8bc915ef36cbb314858c56e5ef
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118021994"
---
# <a name="consistency-guids"></a>Konsistenz-GUIDs

Konsistenz-GUIDs sind eine Erkennungsstrategie, mit der eine Anwendung Teilupdates erkennen kann. Eine Konsistenz-GUID (Globally Unique IDentifier) wird auf jedes Objekt in einem verknüpften Satz angewendet. In der Implementierung generiert eine Quellanwendung eine neue GUID und wendet sie auf jedes Objekt an, das sie im Satz verwandter Objekte aktualisiert. Anschließend wird die neue GUID auf die restlichen Objekte in der Menge angewendet, und die neue GUID wird auf das Masterobjekt angewendet. In der Regel ist das Masterobjekt ein Container, der das übergeordnete Element der anderen Objekte in der Menge ist.

Wichtige Hinweise:

-   Konsistenz-GUIDs in Kombination mit Objektanzahlen oder Prüfsummen sind effektiver als Konsistenz-GUIDs allein, da die Anwendung, die die Objekte liest, möglicherweise nicht weiß, wie viele Objekte mit der GUID vorhanden sein sollen.
-   Anwendungen müssen ihre eigenen GUIDs generieren (eine Microsoft Win32-API, UuidCreate, stellt diese Funktion bereit) und dürfen nicht die vom System generierten GUIDs im **objectGUID-Attribut** eines Objekts verwenden. Dies liegt daran, dass eine Konsistenz-GUID jedes Mal geändert werden muss, wenn der Satz von Objekten aktualisiert wird. Die in **objectGUID** gefundenen Objektidentitäts-GUIDs ändern sich nach dem Erstellen des Objekts nie.
-   Konsistenz-GUIDs gehen davon aus, dass kein Objekt von mehreren Sätzen gemeinsam genutzt wird, sodass jede Gruppe über eine eindeutige Konsistenz-GUID verfügen kann.

 

 




