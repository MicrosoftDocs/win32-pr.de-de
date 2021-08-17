---
title: Ereignis einfrieren
description: Ereignis einfrieren
ms.assetid: 1e537503-f7e7-42f4-aa3c-3c71715b84fe
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ba439ebce12a48d78e1eb1d2daa31990c02f4a42082d3425e9b6ef2f842b3ba1
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "117736800"
---
# <a name="event-freezing"></a>Ereignis einfrieren

Ein Container kann ein Steuerelement benachrichtigen, dass es nicht bereit ist, auf Ereignisse zu reagieren, indem [**er IOleControl::FreezeEvents**](/windows/desktop/api/OCIdl/nf-ocidl-iolecontrol-freezeevents) mit **TRUE** aufruft. Sie kann die Fixierung der Ereignisse aufheben, indem **FreezeEvents** mit **FALSE** aufgerufen wird. Wenn ein Container Ereignisse einfriert, wird die Ereignisverarbeitung und nicht der Ereignisempfang blockiert. Das heißt, ein Container kann weiterhin Ereignisse empfangen, während Ereignisse fixiert sind. Wenn ein Container eine Ereignisbenachrichtigung empfängt, während seine Ereignisse fixiert sind, sollte der Container das Ereignis ignorieren. Es ist keine andere Aktion geeignet.

Ein Steuerelement sollte den Aufruf eines Containers an [**FreezeEvents**](/windows/desktop/api/OCIdl/nf-ocidl-iolecontrol-freezeevents) mit **TRUE** notieren, wenn es für das Steuerelement wichtig ist, dass ein Ereignis nicht verpasst wird. Während die Ereignisverarbeitung eines Containers eingefroren ist, sollte ein Steuerelement eine der folgenden Verfahren implementieren:

-   Löst die Ereignisse in dem vollständigen Wissen aus, dass der Container keine Aktion vornimmt.
-   Verwerfen Sie alle Ereignisse, die das Steuerelement ausgelöst hätte.
-   Stellen Sie alle ausstehenden Ereignisse in die Warteschlange, und werden sie ausgelöst, nachdem der Container [**FreezeEvents**](/windows/desktop/api/OCIdl/nf-ocidl-iolecontrol-freezeevents) mit **FALSE** aufgerufen hat.
-   Stellen Sie nur relevante oder wichtige Ereignisse in die Warteschlange, und setzen Sie sie aus, nachdem der Container [**FreezeEvents**](/windows/desktop/api/OCIdl/nf-ocidl-iolecontrol-freezeevents) mit **FALSE** aufgerufen hat.

Jede Technik ist unter verschiedenen Umständen akzeptabel und geeignet. Der Steuerelemententwickler ist für die Bestimmung und Implementierung der geeigneten Technik für die Funktionalität des Steuerelements verantwortlich.

 

 




