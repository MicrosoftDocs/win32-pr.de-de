---
title: Debuggen WOW64
description: Anwendungen, die unter WOW64 ausgeführt werden, können entweder mit einem x86-gehosteten Debugger oder einem nativen Debugger Debuggen.
ms.assetid: e0945bdd-998d-4531-869f-21c505cb2135
keywords:
- WOW64 64-Bit-Windows-Programmierung, Debuggen
- Debuggen WOW64 64-Bit-Windows-Programmierung
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: dcc7590b0b4f44f9e1a48a204723fb0652b9c2e4
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "104390877"
---
# <a name="debugging-wow64"></a><span data-ttu-id="4b845-105">Debuggen WOW64</span><span class="sxs-lookup"><span data-stu-id="4b845-105">Debugging WOW64</span></span>

<span data-ttu-id="4b845-106">Anwendungen, die unter WOW64 ausgeführt werden, können auf zwei Arten deentschlbelt werden</span><span class="sxs-lookup"><span data-stu-id="4b845-106">Applications running under WOW64 can be debugged two ways:</span></span>

-   <span data-ttu-id="4b845-107">Verwenden Sie einen x86-gehosteten Debugger wie z. b. ntiond, WinDbg oder Visual Studio.</span><span class="sxs-lookup"><span data-stu-id="4b845-107">Use an x86-hosted debugger such as NTSD, WinDbg, or Visual Studio.</span></span> <span data-ttu-id="4b845-108">Die 32-Bit-NTSD wird in "% SystemRoot% \\ syswow64" in Einzelhandels Installationen installiert.</span><span class="sxs-lookup"><span data-stu-id="4b845-108">The 32-bit NTSD is installed to %systemroot%\\syswow64 on retail installations.</span></span> <span data-ttu-id="4b845-109">Beachten Sie, dass x86-Debugger zum Debuggen von x86-Code verwendet werden können. er kann jedoch nicht verwendet werden, um Breakpoints innerhalb der WOW64-Thunk-Ebene zu disassemblieren oder festzulegen, da es 64 sich um einen</span><span class="sxs-lookup"><span data-stu-id="4b845-109">Note that x86 debuggers can be used to debug x86 code, but cannot be used to disassemble or set breakpoints within the WOW64 thunk layer because it is 64-bit native code.</span></span>
-   <span data-ttu-id="4b845-110">Verwenden Sie einen systemeigenen Debugger wie CDB, NZD oder WinDbg und die WOW64-Debugger-Erweiterung, Wow64exts.dll.</span><span class="sxs-lookup"><span data-stu-id="4b845-110">Use a native debugger such as CDB, NTSD, or WinDbg and the WOW64 debugger extension, Wow64exts.dll.</span></span> <span data-ttu-id="4b845-111">Wenn der Native Debugger unterbrochen wird, während sich der Prozessor im x86-Modus befindet, stellt der Debugger den Prozess als x86-Prozess dar.</span><span class="sxs-lookup"><span data-stu-id="4b845-111">If the native debugger breaks while the processor is in x86 mode, the debugger presents the process as an x86 process.</span></span> <span data-ttu-id="4b845-112">Wenn sich der Prozessor im einheitlichen Modus befindet, zeigt der Debugger den Prozess als Native an.</span><span class="sxs-lookup"><span data-stu-id="4b845-112">If the processor is in native mode, the debugger presents the process as native.</span></span>

<span data-ttu-id="4b845-113">CDB, NZD und WinDbg sind in Debuggingtools für Windows enthalten.</span><span class="sxs-lookup"><span data-stu-id="4b845-113">CDB, NTSD, and WinDbg are included in Debugging Tools for Windows.</span></span> <span data-ttu-id="4b845-114">Weitere Informationen finden Sie in der Dokumentation [zu Debuggingtools für Windows](/windows-hardware/drivers/debugger/) .</span><span class="sxs-lookup"><span data-stu-id="4b845-114">For more information, see the [Debugging Tools for Windows](/windows-hardware/drivers/debugger/) documentation.</span></span>

<span data-ttu-id="4b845-115">Die Wow64exts-Debugger-Erweiterung wird mit WinDbg installiert.</span><span class="sxs-lookup"><span data-stu-id="4b845-115">The Wow64exts debugger extension is installed with WinDbg.</span></span> <span data-ttu-id="4b845-116">Verwenden Sie den Befehl! Load wow64exts, um die Debugger-Erweiterung zu laden.</span><span class="sxs-lookup"><span data-stu-id="4b845-116">Use the !load wow64exts command to load the debugger extension.</span></span> <span data-ttu-id="4b845-117">In der folgenden Tabelle sind die wow64exts-Debugger-Erweiterungs Befehle aufgeführt.</span><span class="sxs-lookup"><span data-stu-id="4b845-117">The following table lists the !wow64exts debugger extension commands.</span></span>



| <span data-ttu-id="4b845-118">Get-Help</span><span class="sxs-lookup"><span data-stu-id="4b845-118">Command</span></span>                | <span data-ttu-id="4b845-119">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="4b845-119">Description</span></span>                                                                                                                              |
|------------------------|------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="4b845-120">! wow64exts. SW</span><span class="sxs-lookup"><span data-stu-id="4b845-120">!wow64exts.sw</span></span>          | <span data-ttu-id="4b845-121">Wechselt zwischen x86-und einheitlichen Modus.</span><span class="sxs-lookup"><span data-stu-id="4b845-121">Switches between x86 and native mode.</span></span>                                                                                                    |
| <span data-ttu-id="4b845-122">! wow64exts. k- *Anzahl*</span><span class="sxs-lookup"><span data-stu-id="4b845-122">!wow64exts.k *count*</span></span>   | <span data-ttu-id="4b845-123">Sichert eine kombinierte 32-Bit/64-Bit-Stapel Überwachung.</span><span class="sxs-lookup"><span data-stu-id="4b845-123">Dumps a combined 32-bit/64-bit stack trace.</span></span> <span data-ttu-id="4b845-124">Wenn *count* angegeben wird, sichert der Befehl die ersten *Anzahl* Adressen in jeder Stapel Überwachung.</span><span class="sxs-lookup"><span data-stu-id="4b845-124">If *count* is specified, the command dumps the first *count* addresses in each stack trace.</span></span>  |
| <span data-ttu-id="4b845-125">! wow64exts.info</span><span class="sxs-lookup"><span data-stu-id="4b845-125">!wow64exts.info</span></span>        | <span data-ttu-id="4b845-126">Sichert grundlegende Informationen über den Peer des Prozesses, den TEB des aktuellen Threads und die von WOW64 verwendeten TLS-Slots (Thread Local Storage).</span><span class="sxs-lookup"><span data-stu-id="4b845-126">Dumps basic information about the PEB of the process, the TEB of the current thread, and thread local storage (TLS) slots used by WOW64.</span></span> |
| <span data-ttu-id="4b845-127">! wow64exts. r- *Adresse*</span><span class="sxs-lookup"><span data-stu-id="4b845-127">!wow64exts.r *address*</span></span> | <span data-ttu-id="4b845-128">Sichert den Kontext für die angegebene Adresse.</span><span class="sxs-lookup"><span data-stu-id="4b845-128">Dumps context for the specified address.</span></span> <span data-ttu-id="4b845-129">Wenn *Address* nicht angegeben wird, gibt der Befehl den Kontext für den Prozessor aus.</span><span class="sxs-lookup"><span data-stu-id="4b845-129">If *address* is not specified, the command dumps context for the processor.</span></span>                     |



 

 

 