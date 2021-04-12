---
title: Prozess läuft
description: Eine Momentaufnahme, die die Prozessliste enthält, enthält Informationen zu jedem aktuell ausgeführten Prozess.
ms.assetid: 4fb55763-2206-48ad-8b1f-ed2c33b6f56b
keywords:
- Auflisten
- auflisten, Prozesse
- Prozesse
- Prozesse, Auflisten von Prozessen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: dbc95f0de4021ce3c355286376decbdecef2c883
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "104473549"
---
# <a name="process-walking"></a><span data-ttu-id="00874-107">Prozess läuft</span><span class="sxs-lookup"><span data-stu-id="00874-107">Process Walking</span></span>

<span data-ttu-id="00874-108">Eine Momentaufnahme, die die Prozessliste enthält, enthält Informationen zu jedem aktuell ausgeführten Prozess.</span><span class="sxs-lookup"><span data-stu-id="00874-108">A snapshot that includes the process list contains information about each currently executing process.</span></span> <span data-ttu-id="00874-109">Sie können Informationen für den ersten Prozess in der Liste abrufen, indem Sie die [**Process32First**](/windows/desktop/api/TlHelp32/nf-tlhelp32-process32first) -Funktion verwenden.</span><span class="sxs-lookup"><span data-stu-id="00874-109">You can retrieve information for the first process in the list by using the [**Process32First**](/windows/desktop/api/TlHelp32/nf-tlhelp32-process32first) function.</span></span> <span data-ttu-id="00874-110">Nachdem Sie den ersten Prozess in der Liste abgerufen haben, können Sie die Prozessliste für nachfolgende Einträge durchlaufen, indem Sie die [**Process32Next**](/windows/desktop/api/TlHelp32/nf-tlhelp32-process32next) -Funktion verwenden.</span><span class="sxs-lookup"><span data-stu-id="00874-110">After retrieving the first process in the list, you can traverse the process list for subsequent entries by using the [**Process32Next**](/windows/desktop/api/TlHelp32/nf-tlhelp32-process32next) function.</span></span> <span data-ttu-id="00874-111">**Process32First** und **Process32Next** füllen eine [**PROCESSENTRY32**](/windows/win32/api/tlhelp32/ns-tlhelp32-processentry32) -Struktur mit Informationen über einen Prozess in der Momentaufnahme.</span><span class="sxs-lookup"><span data-stu-id="00874-111">**Process32First** and **Process32Next** fill a [**PROCESSENTRY32**](/windows/win32/api/tlhelp32/ns-tlhelp32-processentry32) structure with information about a process in the snapshot.</span></span> <span data-ttu-id="00874-112">Ein Beispiel finden [Sie unter Erstellen einer Momentaufnahme und Anzeigen von Prozessen](taking-a-snapshot-and-viewing-processes.md).</span><span class="sxs-lookup"><span data-stu-id="00874-112">For an example, see [Taking a Snapshot and Viewing Processes](taking-a-snapshot-and-viewing-processes.md).</span></span>

<span data-ttu-id="00874-113">Mit der [**GetLastError**](/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror) -Funktion können Sie einen erweiterten Fehlerstatus Code für [**Process32First**](/windows/desktop/api/TlHelp32/nf-tlhelp32-process32first) und [**Process32Next**](/windows/desktop/api/TlHelp32/nf-tlhelp32-process32next) abrufen.</span><span class="sxs-lookup"><span data-stu-id="00874-113">You can retrieve an extended error status code for [**Process32First**](/windows/desktop/api/TlHelp32/nf-tlhelp32-process32first) and [**Process32Next**](/windows/desktop/api/TlHelp32/nf-tlhelp32-process32next) by using the [**GetLastError**](/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror) function.</span></span>

<span data-ttu-id="00874-114">Sie können den Arbeitsspeicher in einem bestimmten Prozess mithilfe der [**Toolhelp32ReadProcessMemory**](/windows/desktop/api/TlHelp32/nf-tlhelp32-toolhelp32readprocessmemory) -Funktion (oder der [**virtualqueryex**](/windows/desktop/api/memoryapi/nf-memoryapi-virtualqueryex) -Funktion) in einen Puffer einlesen.</span><span class="sxs-lookup"><span data-stu-id="00874-114">You can read the memory in a specific process into a buffer by using the [**Toolhelp32ReadProcessMemory**](/windows/desktop/api/TlHelp32/nf-tlhelp32-toolhelp32readprocessmemory) function (or the [**VirtualQueryEx**](/windows/desktop/api/memoryapi/nf-memoryapi-virtualqueryex) function).</span></span>

> [!Note]  
> <span data-ttu-id="00874-115">Die Inhalte der **th32ProcessID** -und **th32ParentProcessID** -Member von [**PROCESSENTRY32**](/windows/win32/api/tlhelp32/ns-tlhelp32-processentry32) sind Prozess Bezeichner und können von allen Funktionen verwendet werden, die eine Prozess-ID erfordern.</span><span class="sxs-lookup"><span data-stu-id="00874-115">The contents of the **th32ProcessID** and **th32ParentProcessID** members of [**PROCESSENTRY32**](/windows/win32/api/tlhelp32/ns-tlhelp32-processentry32) are process identifiers and can be used by any functions that require a process identifier.</span></span>

 

 

 