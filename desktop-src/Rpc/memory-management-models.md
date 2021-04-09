---
title: Memory-Management Modelle
description: Memory-Management Modelle
ms.assetid: 1690901b-2a1e-455b-a440-2674f5e5dfa4
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b8114f11755829be9d5f7b17b751e075701ac0aa
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "103948099"
---
# <a name="memory-management-models"></a>Memory-Management Modelle

Als Entwickler haben Sie mehrere Möglichkeiten, wie Arbeitsspeicher zugeordnet und freigegeben wird. Angenommen, eine komplexe Datenstruktur besteht aus Knoten, die mit Zeigern verbunden sind, z. b. eine verknüpfte Liste oder eine Struktur. Sie können Attribute anwenden, mit denen eines der folgenden Modelle ausgewählt wird:

-   [Zuordnung und Aufhebung der Zuordnung von Knoten zu Knoten](node-by-node-allocation-and-deallocation.md).
-   [Ein einzelner linearer Puffer, der vom Stub für die gesamte Struktur zugeordnet wird](stub-allocated-buffers.md).
-   [Server-Stub-Speicherverwaltung](server-stub-memory-management.md)
-   [Ein einzelner linearer Puffer, der von der Client Anwendung für die gesamte Struktur zugewiesen wird](application-allocated-buffer.md).
-   [Persistente Speicherung auf dem Server](persistent-storage-on-the-server.md).

 

 




