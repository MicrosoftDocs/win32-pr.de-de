---
description: Übersicht über die Ereignis Benachrichtigung
ms.assetid: c8b960db-fb8b-4c32-99c3-9d83432574cc
title: Übersicht über die Ereignis Benachrichtigung
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4c60c3251a74606f07f25ab6870cfd1f333ecbbd
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/06/2021
ms.locfileid: "103746568"
---
# <a name="overview-of-event-notification"></a>Übersicht über die Ereignis Benachrichtigung

Ein Filter benachrichtigt den Filter-Graph-Manager über ein Ereignis, indem er eine Ereignis Benachrichtigung bereitstellt. Das Ereignis ist möglicherweise erwartungsgemäß, wie z. b. das Ende eines Streams, oder es könnte einen Fehler darstellen, z. b. einen Fehler beim Rendering eines Streams. Der Filter Graph-Manager verarbeitet einige Filter Ereignisse allein und lässt andere von der Anwendung verarbeiten. Wenn der Filter Graph-Manager kein Filter Ereignis behandelt, wird die Ereignis Benachrichtigung in eine Warteschlange eingefügt. Das Filter Diagramm kann auch seine eigenen Ereignis Benachrichtigungen für die Anwendung in die Warteschlange stellen.

Eine Anwendung ruft Ereignisse aus der Warteschlange ab und antwortet Ihnen basierend auf dem Ereignistyp. Die Ereignis Benachrichtigung in DirectShow ähnelt daher dem Microsoft Windows Message queuingschema. Eine Anwendung kann auch das Standardverhalten des Filter Graph-Managers für einen bestimmten Ereignistyp abbrechen. Der Filter Graph-Manager fügt diese Ereignisse dann direkt in die Warteschlange ein, damit Sie von der Anwendung behandelt wird.

Dieser Mechanismus ermöglicht

-   Der Filter-Graph-Manager für die Kommunikation mit der Anwendung.
-   Filter für die Kommunikation mit der Anwendung und dem Filter-Graph-Manager.
-   Die Anwendung, um den Grad der Beteiligung an der Behandlung von Ereignissen zu ermitteln.

 

 



