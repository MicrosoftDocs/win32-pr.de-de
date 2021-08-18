---
description: Mit der Peer Graphing-API können Anwendungen Daten effizient und zuverlässig zwischen Peers übergeben. Die Kernkonzepte der Peer graph-Technologie sind die Knoten eines Peerdiagramms und Ereignishinweise.
ms.assetid: c3530134-bde3-4a9a-b433-4f198430a607
title: Informationen zur Graphing-API
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 735bf7993744aa8d1e76b8c5d98e8d6856bb4e1757224cd0c98f2e7b1b6f710b
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119011788"
---
# <a name="about-the-graphing-api"></a>Informationen zur Graphing-API

Mit der Peer Graphing-API können Anwendungen Daten effizient und zuverlässig zwischen Peers übergeben. Die Kernkonzepte der Peer graph-Technologie sind **die Knoten** eines Peerdiagramms und Ereignishinweise.

## <a name="nodes"></a>Knoten

Ein Knoten stellt eine bestimmte Instanz eines Peers in einem Netzwerk dar. Die Peer Graphing-API-Infrastruktur stellt sicher, dass jeder Knoten über eine konsistente Ansicht der Daten in einem Diagramm verfügt. Ein Knoten verfügt über die folgenden Features:

-   Kann eine Verbindung mit einem anderen Knoten herstellen und ein miteinander verknüpftes Netzwerk bilden, das als Peerdiagramm bezeichnet wird.
-   Kann Daten für andere Knoten in einem Diagramm in Form eines Datensatzes [freigeben.](records.md)
-   Kann direkte Verbindungen getrennt von den Peerdiagrammen erstellen, die mithilfe der Peer [grouping-API eingerichtet wurden.](about-the-grouping-api.md)
    > [!Note]  
    > Direkte Verbindungen ermöglichen Es Knoten, private Daten aneinander zu senden.

     

## <a name="event-notices"></a>Ereignishinweise

Die Peer Graphing-API verfügt über eine Ereignisinfrastruktur, mit der eine Anwendung ein Peerereignis innerhalb der Peer Graphing-API-Infrastruktur registrieren und erhalten kann. Wenn sich etwas in einem Peerdiagramm ändert, sendet eine Anwendung eine Ereignisbenachrichtigung, um zu identifizieren, dass eine Änderung aufgetreten ist.

 

 



