---
description: Jeder Prozess auf 32-Bit-Microsoft Windows verfügt über einen eigenen virtuellen Adressraum, der die Adressierung von bis zu 4 Gigabyte Arbeitsspeicher ermöglicht.
ms.assetid: f259f3cb-81c0-4b5f-b6fa-9681a278019a
title: Informationen zur Speicherverwaltung
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4110bf1d0768f1321fd89ddd1d5a985e3e54aa75
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106346952"
---
# <a name="about-memory-management"></a><span data-ttu-id="88aa4-103">Informationen zur Speicherverwaltung</span><span class="sxs-lookup"><span data-stu-id="88aa4-103">About Memory Management</span></span>

<span data-ttu-id="88aa4-104">Jeder Prozess auf 32-Bit-Microsoft Windows verfügt über einen eigenen virtuellen Adressraum, der die Adressierung von bis zu 4 Gigabyte Arbeitsspeicher ermöglicht.</span><span class="sxs-lookup"><span data-stu-id="88aa4-104">Each process on 32-bit Microsoft Windows has its own virtual address space that enables addressing up to 4 gigabytes of memory.</span></span> <span data-ttu-id="88aa4-105">Jeder Prozess auf 64-Bit-Windows verfügt über einen virtuellen Adressraum von 8 Terabyte.</span><span class="sxs-lookup"><span data-stu-id="88aa4-105">Each process on 64-bit Windows has a virtual address space of 8 terabytes.</span></span> <span data-ttu-id="88aa4-106">Alle Threads eines Prozesses können auf den virtuellen Adressraum zugreifen.</span><span class="sxs-lookup"><span data-stu-id="88aa4-106">All threads of a process can access its virtual address space.</span></span> <span data-ttu-id="88aa4-107">Threads können jedoch nicht auf den Arbeitsspeicher zugreifen, der zu einem anderen Prozess gehört, wodurch verhindert wird, dass ein Prozess von einem anderen Prozess beschädigt wird.</span><span class="sxs-lookup"><span data-stu-id="88aa4-107">However, threads cannot access memory that belongs to another process, which protects a process from being corrupted by another process.</span></span>

<span data-ttu-id="88aa4-108">Informationen zum virtuellen Adressraum und den Speicherverwaltungsfunktionen finden Sie in den folgenden Themen.</span><span class="sxs-lookup"><span data-stu-id="88aa4-108">For information on the virtual address space and the memory management functions, see the following topics.</span></span>

-   [<span data-ttu-id="88aa4-109">Virtueller Adressraum</span><span class="sxs-lookup"><span data-stu-id="88aa4-109">Virtual Address Space</span></span>](virtual-address-space.md)
-   [<span data-ttu-id="88aa4-110">Speicher Pools</span><span class="sxs-lookup"><span data-stu-id="88aa4-110">Memory Pools</span></span>](memory-pools.md)
-   [<span data-ttu-id="88aa4-111">Informationen zur Speicherleistung</span><span class="sxs-lookup"><span data-stu-id="88aa4-111">Memory Performance Information</span></span>](memory-performance-information.md)
-   [<span data-ttu-id="88aa4-112">Funktionen des virtuellen Arbeitsspeichers</span><span class="sxs-lookup"><span data-stu-id="88aa4-112">Virtual Memory Functions</span></span>](virtual-memory-functions.md)
-   [<span data-ttu-id="88aa4-113">Heap Funktionen</span><span class="sxs-lookup"><span data-stu-id="88aa4-113">Heap Functions</span></span>](heap-functions.md)
-   [<span data-ttu-id="88aa4-114">Datei Zuordnung</span><span class="sxs-lookup"><span data-stu-id="88aa4-114">File Mapping</span></span>](file-mapping.md)
-   [<span data-ttu-id="88aa4-115">Unterstützung großer Arbeitsspeicher</span><span class="sxs-lookup"><span data-stu-id="88aa4-115">Large Memory Support</span></span>](large-memory-support.md)
-   [<span data-ttu-id="88aa4-116">Globale und lokale Funktionen</span><span class="sxs-lookup"><span data-stu-id="88aa4-116">Global and Local Functions</span></span>](global-and-local-functions.md)
-   [<span data-ttu-id="88aa4-117">Standard-C-Bibliotheksfunktionen</span><span class="sxs-lookup"><span data-stu-id="88aa4-117">Standard C Library Functions</span></span>](standard-c-library-functions.md)
-   [<span data-ttu-id="88aa4-118">Vergleichen von Speicher Belegungs Methoden</span><span class="sxs-lookup"><span data-stu-id="88aa4-118">Comparing Memory Allocation Methods</span></span>](comparing-memory-allocation-methods.md)

 

 



