---
title: Übersetzung von Ereigniskoordinaten
description: Übersetzung von Ereigniskoordinaten
ms.assetid: e7de8af1-a409-4140-9e85-e035bd583912
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 843c2e5a3f978f405a3c126ef6a246024b55ccd2f73fbf86a8eed285b6181169
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119993140"
---
# <a name="event-coordinate-translation"></a>Übersetzung von Ereigniskoordinaten

Die 96-Spezifikation für Steuerelemente erfordert, dass Koordinaten, die für ereignisse übergeben werden, die vom Steuerelement ausgelöst werden, sich von HIMETRIC in punktbasiert ändern. Diese Änderung bringt die Ereignisübergabe von Koordinaten in Einklang mit Eigenschaften und Methoden, und daher liegt die Koordinatenübersetzung nicht mehr in der Verantwortung des Containers. Dies führt zu bestimmten Kompatibilitätsproblemen, bei denen ein Steuerelement Ereignisse mit einer nicht erwarteten Koordinatenbasis auslöst. Dies sollte nur ein Problem sein, bei dem ein 96-Steuerelementcontainer wie folgt ein älteres Steuerelement vor 96 hostet:

-   Wenn ein älterer Container vor 96 ein 96-Steuerelement hostet, zeigt das Steuerelement die Ereigniskoordinaten als Punkte an. Dies sollte dem Container keine Probleme verursachen, da der Container den Parametertyp erkennen sollte.
-   Wenn ein 96-Container ein Steuerelement vor 96 hostet, stellt das Steuerelement den Container mit Koordinaten bereit und erwartet, dass der Container eine erforderliche Übersetzung erhält. Der 96-Container erwartet jedoch, dass ein Steuerelement der Spezifikation für 96 Steuerelemente entspricht und seine Koordinaten als Punkte darstellt. Das Steuerelement verwendet die [**TransformCoords-Methode**](/windows/desktop/api/OCIdl/nf-ocidl-iolecontrolsite-transformcoords) auf der [**IOleControlSite-Schnittstelle,**](/windows/desktop/api/OCIdl/nn-ocidl-iolecontrolsite) die vom Container bereitgestellt wird, auf die gleiche Weise wie Eigenschaften und Methoden, um dies zu erreichen.

Daher muss der Benutzer eines 96-Containers, der Steuerelemente vor 96 hostet, beachten, dass eine weitere Übersetzung von Koordinaten erforderlich sein kann, wenn Ereignisse ausgelöst werden.

 

 




