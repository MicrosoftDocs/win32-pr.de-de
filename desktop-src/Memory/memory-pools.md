---
description: 'Der Speicher-Manager erstellt die folgenden Speicherpools, die das System verwendet, um Speicher zuzuweisen: nicht Auslagerungs Pool und Auslagerungs Pool.'
ms.assetid: 68ee9c72-f3a3-4f1f-a827-ed4210a665e4
title: Speicher Pools
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 60987b43347e55d8ee2d01672dbb8173ffc8dd5d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106357096"
---
# <a name="memory-pools"></a><span data-ttu-id="20a66-103">Speicher Pools</span><span class="sxs-lookup"><span data-stu-id="20a66-103">Memory Pools</span></span>

<span data-ttu-id="20a66-104">Der Speicher-Manager erstellt die folgenden Speicherpools, die das System verwendet, um Speicher zuzuweisen: nicht Auslagerungs Pool und Auslagerungs Pool.</span><span class="sxs-lookup"><span data-stu-id="20a66-104">The memory manager creates the following memory pools that the system uses to allocate memory: nonpaged pool and paged pool.</span></span> <span data-ttu-id="20a66-105">Beide Speicherpools befinden sich in der Region des Adressraums, der für das System reserviert ist und dem virtuellen Adressraum der einzelnen Prozesse zugeordnet ist.</span><span class="sxs-lookup"><span data-stu-id="20a66-105">Both memory pools are located in the region of the address space that is reserved for the system and mapped into the virtual address space of each process.</span></span> <span data-ttu-id="20a66-106">Der nicht-Auslagerungs Pool besteht aus virtuellen Speicheradressen, die sich garantiert im physischen Speicher befinden, solange die entsprechenden Kernel Objekte zugewiesen werden.</span><span class="sxs-lookup"><span data-stu-id="20a66-106">The nonpaged pool consists of virtual memory addresses that are guaranteed to reside in physical memory as long as the corresponding kernel objects are allocated.</span></span> <span data-ttu-id="20a66-107">Der Auslagerungs Pool besteht aus virtuellem Arbeitsspeicher, der ein-und auslagern aus dem System möglich ist.</span><span class="sxs-lookup"><span data-stu-id="20a66-107">The paged pool consists of virtual memory that can be paged in and out of the system.</span></span> <span data-ttu-id="20a66-108">Um die Leistung zu verbessern, verfügen Systeme mit einem einzelnen Prozessor über drei auslagerbare Pools, und Multiprozessorsysteme verfügen über fünf auslagerbare Pools.</span><span class="sxs-lookup"><span data-stu-id="20a66-108">To improve performance, systems with a single processor have three paged pools, and multiprocessor systems have five paged pools.</span></span>

<span data-ttu-id="20a66-109">Die Handles für [Kernel Objekte](../sysinfo/kernel-objects.md) werden im ausgelagerten Pool gespeichert, sodass die Anzahl der Handles, die Sie erstellen können, auf dem verfügbaren Arbeitsspeicher basiert.</span><span class="sxs-lookup"><span data-stu-id="20a66-109">The handles for [kernel objects](../sysinfo/kernel-objects.md) are stored in the paged pool, so the number of handles you can create is based on available memory.</span></span>

<span data-ttu-id="20a66-110">Das System zeichnet die Limits und die aktuellen Werte für den nicht auslagerten Pool, den Auslagerungs Pool und die Auslagerungs Datei Verwendung auf.</span><span class="sxs-lookup"><span data-stu-id="20a66-110">The system records the limits and current values for its nonpaged pool, paged pool, and page file usage.</span></span> <span data-ttu-id="20a66-111">Weitere Informationen finden Sie unter [Informationen zur Speicherleistung](memory-performance-information.md).</span><span class="sxs-lookup"><span data-stu-id="20a66-111">For more information, see [Memory Performance Information](memory-performance-information.md).</span></span>

 

 
