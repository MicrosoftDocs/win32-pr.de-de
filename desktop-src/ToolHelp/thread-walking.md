---
title: Thread-Walking
description: Eine Momentaufnahme, die die Thread Liste enthält, enthält Informationen zu jedem Thread jedes aktuell ausgeführten Prozesses.
ms.assetid: 2440b781-652d-4d73-b173-87504e7b49b5
keywords:
- Auflisten
- auflisten, Threads
- Threads
- Threads, Enumerieren von Threads
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 32eff584aedaa3f6124cc358a4ee9d2a94962843
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "106341735"
---
# <a name="thread-walking"></a><span data-ttu-id="e3c44-107">Thread-Walking</span><span class="sxs-lookup"><span data-stu-id="e3c44-107">Thread Walking</span></span>

<span data-ttu-id="e3c44-108">Eine Momentaufnahme, die die Thread Liste enthält, enthält Informationen zu jedem Thread jedes aktuell ausgeführten Prozesses.</span><span class="sxs-lookup"><span data-stu-id="e3c44-108">A snapshot that includes the thread list contains information about each thread of each currently executing process.</span></span> <span data-ttu-id="e3c44-109">Mit der [**Thread32First**](/windows/desktop/api/TlHelp32/nf-tlhelp32-thread32first) -Funktion können Sie Informationen für den ersten Thread in der Liste abrufen.</span><span class="sxs-lookup"><span data-stu-id="e3c44-109">You can retrieve information for the first thread in the list by using the [**Thread32First**](/windows/desktop/api/TlHelp32/nf-tlhelp32-thread32first) function.</span></span> <span data-ttu-id="e3c44-110">Nachdem Sie den ersten Thread in der Liste abgerufen haben, können Sie mithilfe der [**Thread32Next**](/windows/desktop/api/TlHelp32/nf-tlhelp32-thread32next) -Funktion Informationen für nachfolgende Threads abrufen.</span><span class="sxs-lookup"><span data-stu-id="e3c44-110">After retrieving the first thread in the list, you can retrieve information for subsequent threads by using the [**Thread32Next**](/windows/desktop/api/TlHelp32/nf-tlhelp32-thread32next) function.</span></span> <span data-ttu-id="e3c44-111">**Thread32First** und **Thread32Next** füllen eine [**THREADENTRY32**](/windows/win32/api/tlhelp32/ns-tlhelp32-threadentry32) -Struktur mit Informationen zu einzelnen Threads in der Momentaufnahme.</span><span class="sxs-lookup"><span data-stu-id="e3c44-111">**Thread32First** and **Thread32Next** fill a [**THREADENTRY32**](/windows/win32/api/tlhelp32/ns-tlhelp32-threadentry32) structure with information about individual threads in the snapshot.</span></span>

<span data-ttu-id="e3c44-112">Sie können die Threads eines bestimmten Prozesses auflisten, indem Sie eine Momentaufnahme erstellen, die die Threads einschließt, und dann durch Durchlaufen der Thread Liste die Informationen zu den Threads, die dieselbe Prozess-ID wie der angegebene Prozess aufweisen, beibehalten.</span><span class="sxs-lookup"><span data-stu-id="e3c44-112">You can enumerate the threads of a specific process by taking a snapshot that includes the threads and then by traversing the thread list, keeping information about the threads that have the same process identifier as the specified process.</span></span>

<span data-ttu-id="e3c44-113">Mit der [**GetLastError**](/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror) -Funktion können Sie einen erweiterten Fehlerstatus Code für [**Thread32First**](/windows/desktop/api/TlHelp32/nf-tlhelp32-thread32first) und [**Thread32Next**](/windows/desktop/api/TlHelp32/nf-tlhelp32-thread32next) abrufen.</span><span class="sxs-lookup"><span data-stu-id="e3c44-113">You can retrieve an extended error status code for [**Thread32First**](/windows/desktop/api/TlHelp32/nf-tlhelp32-thread32first) and [**Thread32Next**](/windows/desktop/api/TlHelp32/nf-tlhelp32-thread32next) by using the [**GetLastError**](/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror) function.</span></span>

> [!Note]  
> <span data-ttu-id="e3c44-114">Der Inhalt des **th32ThreadID** -Members von [**THREADENTRY32**](/windows/win32/api/tlhelp32/ns-tlhelp32-threadentry32) ist ein Thread Bezeichner, der von allen Funktionen verwendet werden kann, die einen Thread Bezeichner erfordern.</span><span class="sxs-lookup"><span data-stu-id="e3c44-114">The contents of the **th32ThreadID** member of [**THREADENTRY32**](/windows/win32/api/tlhelp32/ns-tlhelp32-threadentry32) is a thread identifier and can be used by any functions that require a thread identifier.</span></span>

 

## <a name="related-topics"></a><span data-ttu-id="e3c44-115">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="e3c44-115">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="e3c44-116">Durchlaufen der Thread Liste</span><span class="sxs-lookup"><span data-stu-id="e3c44-116">Traversing the Thread List</span></span>](traversing-the-thread-list.md)
</dt> </dl>

 

 