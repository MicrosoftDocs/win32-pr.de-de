---
description: Wenn ein Experte während der Laufzeit einen Fehler verursacht, wird der zugewiesene Arbeitsspeicher von Netzwerkmonitor freigegeben, wenn Sie Netzwerkmonitor Funktionen für die Speicherverwaltung verwenden.
ms.assetid: b6f5749b-161e-47a7-82cf-d85ad3703ecd
title: Verwalten des Arbeitsspeichers
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8e2e2a6cca89a095c03c5c0cad25642b87d2c252
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "103959021"
---
# <a name="managing-memory"></a><span data-ttu-id="535f6-103">Verwalten des Arbeitsspeichers</span><span class="sxs-lookup"><span data-stu-id="535f6-103">Managing Memory</span></span>

<span data-ttu-id="535f6-104">Wenn ein Experte während der Laufzeit einen Fehler verursacht, wird der zugewiesene Arbeitsspeicher von Netzwerkmonitor freigegeben, wenn Sie Netzwerkmonitor Funktionen für die Speicherverwaltung verwenden.</span><span class="sxs-lookup"><span data-stu-id="535f6-104">Should an expert fail during run time, if you use Network Monitor functions for memory management, Network Monitor will free allocated memory.</span></span> <span data-ttu-id="535f6-105">Wenn Sie jedoch einen Experten schreiben, ist es möglicherweise erforderlich, Systemressourcen und Datenstruktur Informationen abzurufen.</span><span class="sxs-lookup"><span data-stu-id="535f6-105">However, when you write an expert, it might be necessary to acquire system resources and data structure information.</span></span> <span data-ttu-id="535f6-106">Der Netzwerkmonitor Protokoll-COALESCE-Experte erhält z. b. ein Datei Handle zum Erstellen einer neuen Erfassung.</span><span class="sxs-lookup"><span data-stu-id="535f6-106">For example, the Network Monitor Protocol Coalesce Expert acquires a file handle to build a new capture.</span></span> <span data-ttu-id="535f6-107">Jeder Experte muss eine eigene **try/catch-** Behandlung erstellen, damit der Experte Ressourcen freigeben kann, die er erworben hat.</span><span class="sxs-lookup"><span data-stu-id="535f6-107">Each expert must build its own **try/catch** handling so that the expert can free resources it acquired.</span></span>

<span data-ttu-id="535f6-108">Wenn Arbeitsspeicher zugewiesen ist, verwenden Sie die folgenden vorhandenen Speicherfunktionen:</span><span class="sxs-lookup"><span data-stu-id="535f6-108">When memory is allocated, use the following existing memory functions:</span></span>

-   [<span data-ttu-id="535f6-109">**"Expertenlocmemory"**</span><span class="sxs-lookup"><span data-stu-id="535f6-109">**ExpertAllocMemory**</span></span>](expertallocmemory.md)
-   [<span data-ttu-id="535f6-110">**Expertrebelegcmemory**</span><span class="sxs-lookup"><span data-stu-id="535f6-110">**ExpertReallocMemory**</span></span>](expertreallocmemory.md)

 

 



