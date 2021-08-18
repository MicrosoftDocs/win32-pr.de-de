---
description: Übersicht über Ereignisbenachrichtigungen
ms.assetid: c8b960db-fb8b-4c32-99c3-9d83432574cc
title: Übersicht über Ereignisbenachrichtigungen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 90ca5e6ffb4737054f773fc5be35d56939e711442a3b31761cd23c144ed00ac1
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119148533"
---
# <a name="overview-of-event-notification"></a>Übersicht über Ereignisbenachrichtigungen

Ein Filter benachrichtigt den Filter Graph Manager über ein Ereignis, indem eine Ereignisbenachrichtigung veröffentlicht wird. Das Ereignis kann ein erwartetes Ereignis sein, z. B. das Ende eines Streams, oder es kann einen Fehler darstellen, z. B. ein Fehler beim Rendern eines Streams. Der Filter Graph-Manager verarbeitet einige Filterereignisse selbst und überlässt anderen die Anwendung. Wenn der Filter Graph-Manager kein Filterereignis behandelt, wird die Ereignisbenachrichtigung in eine Warteschlange eingereiht. Das Filterdiagramm kann auch eigene Ereignisbenachrichtigungen für die Anwendung in die Warteschlange stellen.

Eine Anwendung ruft Ereignisse aus der Warteschlange ab und antwortet basierend auf dem Ereignistyp darauf. Die Ereignisbenachrichtigung in DirectShow ähnelt daher dem Microsoft Windows Message Queuing-Schema. Eine Anwendung kann auch das Standardverhalten des Graph-Managers für einen bestimmten Ereignistyp abbrechen. Der Filter Graph Manager versetzt diese Ereignisse dann direkt in die Warteschlange, damit die Anwendung sie verarbeiten kann.

Dieser Mechanismus ermöglicht

-   Der Filter Graph Manager für die Kommunikation mit der Anwendung.
-   Filter für die Kommunikation mit der Anwendung und dem Filter Graph Manager.
-   Die Anwendung, um ihren Grad an Beteiligung an der Behandlung von Ereignissen zu bestimmen.

 

 



