---
title: Tool Hilfefunktionen
description: Listet die Funktionen der Tool Hilfe Bibliothek auf.
ms.assetid: 83732bd6-f4cf-409d-ad17-86503d408dc3
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 54f9d95598f9b48343ea9731e1a826fb147a73a8
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "104037467"
---
# <a name="tool-help-functions"></a><span data-ttu-id="da0f8-103">Tool Hilfefunktionen</span><span class="sxs-lookup"><span data-stu-id="da0f8-103">Tool Help Functions</span></span>

<span data-ttu-id="da0f8-104">Die folgenden Funktionen sind Teil der Tool Hilfe Bibliothek.</span><span class="sxs-lookup"><span data-stu-id="da0f8-104">The following functions are part of the tool help library.</span></span>



| <span data-ttu-id="da0f8-105">Funktion</span><span class="sxs-lookup"><span data-stu-id="da0f8-105">Function</span></span>                                                           | <span data-ttu-id="da0f8-106">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="da0f8-106">Description</span></span>                                                                                                      |
|--------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="da0f8-107">**CreateToolhelp32Snapshot**</span><span class="sxs-lookup"><span data-stu-id="da0f8-107">**CreateToolhelp32Snapshot**</span></span>](/windows/desktop/api/TlHelp32/nf-tlhelp32-createtoolhelp32snapshot)       | <span data-ttu-id="da0f8-108">Erstellt eine Momentaufnahme der angegebenen Prozesse sowie die Heaps, Module und Threads, die von diesen Prozessen verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="da0f8-108">Takes a snapshot of the specified processes, as well as the heaps, modules, and threads used by these processes.</span></span> |
| [<span data-ttu-id="da0f8-109">**Heap32First**</span><span class="sxs-lookup"><span data-stu-id="da0f8-109">**Heap32First**</span></span>](/windows/desktop/api/TlHelp32/nf-tlhelp32-heap32first)                                 | <span data-ttu-id="da0f8-110">Ruft Informationen zum ersten Block eines Heaps ab, der von einem Prozess zugeordnet wurde.</span><span class="sxs-lookup"><span data-stu-id="da0f8-110">Retrieves information about the first block of a heap that has been allocated by a process.</span></span>                      |
| [<span data-ttu-id="da0f8-111">**Heap32ListFirst**</span><span class="sxs-lookup"><span data-stu-id="da0f8-111">**Heap32ListFirst**</span></span>](/windows/desktop/api/TlHelp32/nf-tlhelp32-heap32listfirst)                         | <span data-ttu-id="da0f8-112">Ruft Informationen zum ersten Heap ab, der durch einen angegebenen Prozess zugeordnet wurde.</span><span class="sxs-lookup"><span data-stu-id="da0f8-112">Retrieves information about the first heap that has been allocated by a specified process.</span></span>                       |
| [<span data-ttu-id="da0f8-113">**Heap32ListNext**</span><span class="sxs-lookup"><span data-stu-id="da0f8-113">**Heap32ListNext**</span></span>](/windows/desktop/api/TlHelp32/nf-tlhelp32-heap32listnext)                           | <span data-ttu-id="da0f8-114">Ruft Informationen über den nächsten Heap ab, der von einem Prozess zugeordnet wurde.</span><span class="sxs-lookup"><span data-stu-id="da0f8-114">Retrieves information about the next heap that has been allocated by a process.</span></span>                                  |
| [<span data-ttu-id="da0f8-115">**Heap32Next**</span><span class="sxs-lookup"><span data-stu-id="da0f8-115">**Heap32Next**</span></span>](/windows/desktop/api/TlHelp32/nf-tlhelp32-heap32next)                                   | <span data-ttu-id="da0f8-116">Ruft Informationen über den nächsten Block eines Heaps ab, der von einem Prozess zugeordnet wurde.</span><span class="sxs-lookup"><span data-stu-id="da0f8-116">Retrieves information about the next block of a heap that has been allocated by a process.</span></span>                       |
| [<span data-ttu-id="da0f8-117">**Module32First**</span><span class="sxs-lookup"><span data-stu-id="da0f8-117">**Module32First**</span></span>](/windows/desktop/api/TlHelp32/nf-tlhelp32-module32first)                             | <span data-ttu-id="da0f8-118">Ruft Informationen zum ersten Modul ab, das einem Prozess zugeordnet ist.</span><span class="sxs-lookup"><span data-stu-id="da0f8-118">Retrieves information about the first module associated with a process.</span></span>                                          |
| [<span data-ttu-id="da0f8-119">**Module32Next**</span><span class="sxs-lookup"><span data-stu-id="da0f8-119">**Module32Next**</span></span>](/windows/desktop/api/TlHelp32/nf-tlhelp32-module32next)                               | <span data-ttu-id="da0f8-120">Ruft Informationen zum nächsten Modul ab, das einem Prozess oder Thread zugeordnet ist.</span><span class="sxs-lookup"><span data-stu-id="da0f8-120">Retrieves information about the next module associated with a process or thread.</span></span>                                 |
| [<span data-ttu-id="da0f8-121">**Process32First**</span><span class="sxs-lookup"><span data-stu-id="da0f8-121">**Process32First**</span></span>](/windows/desktop/api/TlHelp32/nf-tlhelp32-process32first)                           | <span data-ttu-id="da0f8-122">Ruft Informationen zum ersten Prozess ab, der in einer System Momentaufnahme aufgetreten ist.</span><span class="sxs-lookup"><span data-stu-id="da0f8-122">Retrieves information about the first process encountered in a system snapshot.</span></span>                                  |
| [<span data-ttu-id="da0f8-123">**Process32Next**</span><span class="sxs-lookup"><span data-stu-id="da0f8-123">**Process32Next**</span></span>](/windows/desktop/api/TlHelp32/nf-tlhelp32-process32next)                             | <span data-ttu-id="da0f8-124">Ruft Informationen zum nächsten Prozess ab, der in einer System Momentaufnahme aufgezeichnet wurde.</span><span class="sxs-lookup"><span data-stu-id="da0f8-124">Retrieves information about the next process recorded in a system snapshot.</span></span>                                      |
| [<span data-ttu-id="da0f8-125">**Thread32First**</span><span class="sxs-lookup"><span data-stu-id="da0f8-125">**Thread32First**</span></span>](/windows/desktop/api/TlHelp32/nf-tlhelp32-thread32first)                             | <span data-ttu-id="da0f8-126">Ruft Informationen über den ersten Thread eines Prozesses ab, der in einer System Momentaufnahme aufgetreten ist.</span><span class="sxs-lookup"><span data-stu-id="da0f8-126">Retrieves information about the first thread of any process encountered in a system snapshot.</span></span>                    |
| [<span data-ttu-id="da0f8-127">**Thread32Next**</span><span class="sxs-lookup"><span data-stu-id="da0f8-127">**Thread32Next**</span></span>](/windows/desktop/api/TlHelp32/nf-tlhelp32-thread32next)                               | <span data-ttu-id="da0f8-128">Ruft Informationen über den nächsten Thread eines Prozesses ab, der in der Momentaufnahme des System Speichers aufgetreten ist.</span><span class="sxs-lookup"><span data-stu-id="da0f8-128">Retrieves information about the next thread of any process encountered in the system memory snapshot.</span></span>            |
| [<span data-ttu-id="da0f8-129">**Toolhelp32ReadProcessMemory**</span><span class="sxs-lookup"><span data-stu-id="da0f8-129">**Toolhelp32ReadProcessMemory**</span></span>](/windows/desktop/api/TlHelp32/nf-tlhelp32-toolhelp32readprocessmemory) | <span data-ttu-id="da0f8-130">Kopiert Speicher, der einem anderen Prozess zugeordnet ist, in einen von der Anwendung bereitgestellten Puffer.</span><span class="sxs-lookup"><span data-stu-id="da0f8-130">Copies memory allocated to another process into an application-supplied buffer.</span></span>                                  |



 

 

 




