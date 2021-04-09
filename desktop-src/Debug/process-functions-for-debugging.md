---
description: Die Funktion "deateprocess" ermöglicht einem Debugger, einen Prozess zu starten und zu debuggen.
ms.assetid: 7056e181-9bc5-4530-a7b8-d5ff1e345eef
title: Verarbeitungsfunktionen für das Debuggen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d31378a4115acfdd5a4a1836199b7387adeb6e3f
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "103958300"
---
# <a name="process-functions-for-debugging"></a><span data-ttu-id="b578a-103">Verarbeitungsfunktionen für das Debuggen</span><span class="sxs-lookup"><span data-stu-id="b578a-103">Process Functions for Debugging</span></span>

<span data-ttu-id="b578a-104">Die Funktion " [**deateprocess**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-createprocessa) " ermöglicht einem Debugger, einen Prozess zu starten und zu debuggen.</span><span class="sxs-lookup"><span data-stu-id="b578a-104">The [**CreateProcess**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-createprocessa) function enables a debugger to start a process and debug it.</span></span> <span data-ttu-id="b578a-105">Der *fdwcreate* -Parameter von " **kreateprocess** " wird verwendet, um den Typ des Debugvorgangs anzugeben.</span><span class="sxs-lookup"><span data-stu-id="b578a-105">The *fdwCreate* parameter of **CreateProcess** is used to specify the type of debugging operation.</span></span> <span data-ttu-id="b578a-106">Wenn das \_ debugprozessflag für den-Parameter angegeben wird, debuggt ein Debugger den neuen Prozess und alle Nachfolger des Prozesses, vorausgesetzt, dass die Nachfolger ohne das \_ debugprozessflag erstellt werden.</span><span class="sxs-lookup"><span data-stu-id="b578a-106">If the DEBUG\_PROCESS flag is specified for the parameter, a debugger debugs the new process and all of the process's descendants, provided that the descendants are created without the DEBUG\_PROCESS flag.</span></span>

<span data-ttu-id="b578a-107">Wenn der \_ Debugprozess und das Debuggen \_ nur \_ diese \_ prozessflags für " *f" erstellt* werden, debuggt der Debugger den neuen Prozess, aber keinen seiner Nachfolger.</span><span class="sxs-lookup"><span data-stu-id="b578a-107">If the DEBUG\_PROCESS and DEBUG\_ONLY\_THIS\_PROCESS flags are specified for *fdwCreate*, a debugger debugs the new process but none of its descendants.</span></span>

<span data-ttu-id="b578a-108">Ein Debugger kann eine andere Debuggen, indem er einen Prozess mit dem \_ debugprozessflag erstellt.</span><span class="sxs-lookup"><span data-stu-id="b578a-108">One debugger can debug another by creating a process with the DEBUG\_PROCESS flag.</span></span> <span data-ttu-id="b578a-109">Der neue Prozess (der Debugger, der debuggt wird) muss dann einen Prozess mit dem \_ debugprozessflag erstellen.</span><span class="sxs-lookup"><span data-stu-id="b578a-109">The new process (the debugger being debugged) must then create a process with the DEBUG\_PROCESS flag.</span></span>

<span data-ttu-id="b578a-110">Die [**OpenProcess**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-openprocess) -Funktion ermöglicht einem Debugger das Abrufen des Bezeichners eines vorhandenen Prozesses.</span><span class="sxs-lookup"><span data-stu-id="b578a-110">The [**OpenProcess**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-openprocess) function enables a debugger to obtain the identifier of an existing process.</span></span> <span data-ttu-id="b578a-111">(Die [**DebugActiveProcess**](/windows/win32/api/debugapi/nf-debugapi-debugactiveprocess) -Funktion verwendet diesen Bezeichner, um den Debugger an den Prozess anzufügen.) In der Regel öffnen debuggger einen Prozess mit den \_ \_ Schreib-und Prozess-VM-Schreib Flags der Prozess-VM \_ \_ .</span><span class="sxs-lookup"><span data-stu-id="b578a-111">(The [**DebugActiveProcess**](/windows/win32/api/debugapi/nf-debugapi-debugactiveprocess) function uses this identifier to attach the debugger to the process.) Typically, debuggers open a process with the PROCESS\_VM\_READ and PROCESS\_VM\_WRITE flags.</span></span> <span data-ttu-id="b578a-112">Die Verwendung dieser Flags ermöglicht dem Debugger das Lesen und Schreiben in den virtuellen Arbeitsspeicher des Prozesses mithilfe der Funktionen " [**leseprocessmemory**](/windows/win32/api/memoryapi/nf-memoryapi-readprocessmemory) " und " [**schreiteprocessmemory**](/windows/win32/api/memoryapi/nf-memoryapi-writeprocessmemory) ".</span><span class="sxs-lookup"><span data-stu-id="b578a-112">Using these flags enables the debugger to read from and write to the virtual memory of the process by using the [**ReadProcessMemory**](/windows/win32/api/memoryapi/nf-memoryapi-readprocessmemory) and [**WriteProcessMemory**](/windows/win32/api/memoryapi/nf-memoryapi-writeprocessmemory) functions.</span></span> <span data-ttu-id="b578a-113">Weitere Informationen finden Sie unter [**Prozesse und Threads**](../procthread/processes-and-threads.md).</span><span class="sxs-lookup"><span data-stu-id="b578a-113">For more information, see [**Processes and Threads**](../procthread/processes-and-threads.md).</span></span>

 

 
