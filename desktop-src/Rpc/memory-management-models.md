---
title: Memory-Management-Modelle
description: Memory-Management-Modelle
ms.assetid: 1690901b-2a1e-455b-a440-2674f5e5dfa4
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a985158f54bf09d149e04c7eebc5853417e39191ca0bb854cb7d1ba5de1e5d86
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "120019980"
---
# <a name="memory-management-models"></a>Memory-Management-Modelle

Als Entwickler haben Sie mehrere Möglichkeiten, wie Arbeitsspeicher belegt und freigegeben wird. Betrachten Sie eine komplexe Datenstruktur, die aus Knoten besteht, die mit Zeigern verbunden sind, z. B. eine verknüpfte Liste oder eine Struktur. Sie können Attribute anwenden, die eines der folgenden Modelle auswählen:

-   [Knoten-nach-Knoten-Zuordnung und Zuordnungsaufbeendung.](node-by-node-allocation-and-deallocation.md)
-   [Ein einzelner linearer Puffer, der vom Stub für die gesamte Struktur zugeordnet wird.](stub-allocated-buffers.md)
-   [Verwaltung des Serverstubspeichers](server-stub-memory-management.md)
-   [Ein einzelner linearer Puffer, der von der Clientanwendung für die gesamte Struktur zugeordnet wird.](application-allocated-buffer.md)
-   [Persistenter Speicher auf dem Server.](persistent-storage-on-the-server.md)

 

 




