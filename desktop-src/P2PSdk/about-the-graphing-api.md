---
description: Die Peer-graphingapi ermöglicht es Anwendungen, Daten zwischen Peers effizient und zuverlässig zu übergeben. Die wichtigsten Konzepte der Peer Graph-Technologie sind die Knoten eines Peer Diagramms und Ereignis Hinweise.
ms.assetid: c3530134-bde3-4a9a-b433-4f198430a607
title: Informationen zur graphende-API
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c1b08e320f1c8d176d0bd34cc7a9a9422c6cfadc
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106349233"
---
# <a name="about-the-graphing-api"></a>Informationen zur graphende-API

Die Peer-graphingapi ermöglicht es Anwendungen, Daten zwischen Peers effizient und zuverlässig zu übergeben. Die wichtigsten Konzepte der Peer Graph-Technologie sind die **Knoten** eines Peer Diagramms und Ereignis Hinweise.

## <a name="nodes"></a>Nodes

Ein Knoten stellt eine bestimmte Instanz eines Peers in einem Netzwerk dar. Die Peer Graph-API-Infrastruktur stellt sicher, dass jeder Knoten über eine konsistente Sicht der Daten in einem Diagramm verfügt. Ein Knoten verfügt über die folgenden Features:

-   Kann eine Verbindung mit einem anderen Knoten herstellen und ein verbundener Netzwerk, das als Peer Diagramm bezeichnet wird, bilden.
-   Kann Daten für andere Knoten in einem Diagramm in Form eines [Datensatzes](records.md)freigeben.
-   Direkt von den Peer Diagrammen, die mithilfe der Peer [Gruppierungs-API](about-the-grouping-api.md)hergestellt wurden, können direkte Verbindungen erstellt werden.
    > [!Note]  
    > Direkte Verbindungen ermöglichen es Knoten, private Daten an einander zu senden.

     

## <a name="event-notices"></a>Ereignis Hinweise

Die Peer-graphingapi verfügt über eine Ereignis Infrastruktur, die es einer Anwendung ermöglicht, ein Peer Ereignis innerhalb der Peer graphat-API-Infrastruktur zu registrieren und zu erhalten. Wenn sich etwas innerhalb eines Peer Diagramms ändert, sendet eine Anwendung eine Ereignis Benachrichtigung, um zu ermitteln, ob eine Änderung aufgetreten ist.

 

 



