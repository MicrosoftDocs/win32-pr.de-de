---
title: Ereignis Sperrung
description: Ereignis Sperrung
ms.assetid: 1e537503-f7e7-42f4-aa3c-3c71715b84fe
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2e403448d53949c263b8e146961690de1200436c
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "103856044"
---
# <a name="event-freezing"></a>Ereignis Sperrung

Ein Container kann ein Steuerelement benachrichtigen, dass er nicht bereit ist, auf Ereignisse zu reagieren, indem er [**IOleControl:: frezeevents**](/windows/desktop/api/OCIdl/nf-ocidl-iolecontrol-freezeevents) mit **true** aufruft. Das Einfrieren der Ereignisse kann durch Aufrufen von " **frezeevents** mit **false**" aufgehoben werden. Wenn ein Container Ereignisse friert, wird die Ereignisverarbeitung eingefroren, und es wird kein Ereignis empfangen. Das heißt, ein Container kann weiterhin Ereignisse empfangen, während Ereignisse eingefroren werden. Wenn ein Container eine Ereignis Benachrichtigung empfängt, während seine Ereignisse eingefroren sind, sollte der Container das Ereignis ignorieren. Es ist keine weitere Aktion erforderlich.

Ein Steuerelement sollte den Aufrufen von " [**frezeevents**](/windows/desktop/api/OCIdl/nf-ocidl-iolecontrol-freezeevents) " eines Containers mit " **true** " notieren, wenn es für das Steuerelement wichtig ist, dass ein Ereignis nicht übersehen wird. Während die Ereignisverarbeitung eines Containers eingefroren ist, sollte ein Steuerelement eine der folgenden Techniken implementieren:

-   Lösen Sie die Ereignisse in den vollständigen Kenntnissen aus, dass der Container keine Aktion durchführt.
-   Verwerfen Sie alle Ereignisse, die das Steuerelement ausgelöst hätte.
-   Richten Sie alle ausstehenden Ereignisse in die Warteschlange ein, und lösen Sie Sie aus, nachdem der Container " [**frezeevents**](/windows/desktop/api/OCIdl/nf-ocidl-iolecontrol-freezeevents) " mit **false**
-   Richten Sie nur relevante oder wichtige Ereignisse in die Warteschlange ein, und lösen Sie Sie aus, nachdem der Container " [**frezeevents**](/windows/desktop/api/OCIdl/nf-ocidl-iolecontrol-freezeevents) " mit **false**

Jede Technik ist akzeptabel und in unterschiedlichen Situationen angemessen. Der Entwickler des Steuer Elements ist verantwortlich für die Bestimmung und Implementierung der entsprechenden Technik für die Funktionalität des Steuer Elements.

 

 




