---
description: Die folgenden Begriffe werden verwendet, um das Debuggen zu beschreiben.
ms.assetid: 580f2787-d944-4350-a2c2-c00816b3f515
title: Debug-Terminologie
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ffa12e24a6c763f9cda983ad961ba85a41c63cec
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "103958137"
---
# <a name="debugging-terminology"></a><span data-ttu-id="7b01d-103">Debug-Terminologie</span><span class="sxs-lookup"><span data-stu-id="7b01d-103">Debugging Terminology</span></span>

<span data-ttu-id="7b01d-104">Die folgenden Begriffe werden verwendet, um das Debuggen zu beschreiben.</span><span class="sxs-lookup"><span data-stu-id="7b01d-104">The following terms are used when describing debugging.</span></span>

<dl> <dt>

<span data-ttu-id="7b01d-105"><span id="Blue_screen"></span><span id="blue_screen"></span><span id="BLUE_SCREEN"></span>Blauer Bildschirm</span><span class="sxs-lookup"><span data-stu-id="7b01d-105"><span id="Blue_screen"></span><span id="blue_screen"></span><span id="BLUE_SCREEN"></span>Blue screen</span></span>
</dt> <dd>

<span data-ttu-id="7b01d-106">Wenn das System ein Hardwareproblem, Daten Inkonsistenz oder einen ähnlichen Fehler feststellt, wird möglicherweise ein blauer Bildschirm mit Informationen angezeigt, mit denen die Ursache des Fehlers bestimmt werden kann.</span><span class="sxs-lookup"><span data-stu-id="7b01d-106">When the system encounters a hardware problem, data inconsistency, or similar error, it may display a blue screen containing information that can be used to determine the cause of the error.</span></span> <span data-ttu-id="7b01d-107">Diese Informationen umfassen den Endzeitpunkt und ob eine Absturz Abbild Datei erstellt wurde.</span><span class="sxs-lookup"><span data-stu-id="7b01d-107">This information includes the STOP code and whether a crash dump file was created.</span></span> <span data-ttu-id="7b01d-108">Sie kann auch eine Liste geladener Treiber und eine Stapel Überwachung enthalten.</span><span class="sxs-lookup"><span data-stu-id="7b01d-108">It may also include a list of loaded drivers and a stack trace.</span></span>

</dd> <dt>

<span data-ttu-id="7b01d-109"><span id="Crash_dump_file"></span><span id="crash_dump_file"></span><span id="CRASH_DUMP_FILE"></span>Absturz Abbild Datei</span><span class="sxs-lookup"><span data-stu-id="7b01d-109"><span id="Crash_dump_file"></span><span id="crash_dump_file"></span><span id="CRASH_DUMP_FILE"></span>Crash dump file</span></span>
</dt> <dd>

<span data-ttu-id="7b01d-110">Sie können das System so konfigurieren, dass Informationen in eine Absturz Abbild Datei auf der Festplatte geschrieben werden, wenn ein Stoppcode generiert wird.</span><span class="sxs-lookup"><span data-stu-id="7b01d-110">You can configure the system to write information to a crash dump file on your hard disk whenever a STOP code is generated.</span></span> <span data-ttu-id="7b01d-111">Die Datei enthält Informationen, die der Debugger verwenden kann, um den Fehler zu analysieren.</span><span class="sxs-lookup"><span data-stu-id="7b01d-111">The file contains information the debugger can use to analyze the error.</span></span> <span data-ttu-id="7b01d-112">Diese Datei kann so groß wie der physische Arbeitsspeicher auf dem Computer sein.</span><span class="sxs-lookup"><span data-stu-id="7b01d-112">This file can be as big as the physical memory contained in the computer.</span></span>

</dd> <dt>

<span data-ttu-id="7b01d-113"><span id="Debugger"></span><span id="debugger"></span><span id="DEBUGGER"></span>Debugger</span><span class="sxs-lookup"><span data-stu-id="7b01d-113"><span id="Debugger"></span><span id="debugger"></span><span id="DEBUGGER"></span>Debugger</span></span>
</dt> <dd>

<span data-ttu-id="7b01d-114">Ein Programm, das entwickelt wurde, um Fehler in einem anderen Programm zu erkennen, zu finden und zu korrigieren.</span><span class="sxs-lookup"><span data-stu-id="7b01d-114">A program designed to help detect, locate, and correct errors in another program.</span></span> <span data-ttu-id="7b01d-115">Sie ermöglicht es dem Entwickler, die Ausführung des Prozesses und der zugehörigen Threads zu durchlaufen, Arbeitsspeicher, Variablen und andere Elemente von Prozess-und Thread Kontext zu überwachen.</span><span class="sxs-lookup"><span data-stu-id="7b01d-115">It allows the developer to step through the execution of the process and its threads, monitoring memory, variables, and other elements of process and thread context.</span></span>

</dd> <dt>

<span data-ttu-id="7b01d-116"><span id="Kernel_mode"></span><span id="kernel_mode"></span><span id="KERNEL_MODE"></span>Kernel Modus</span><span class="sxs-lookup"><span data-stu-id="7b01d-116"><span id="Kernel_mode"></span><span id="kernel_mode"></span><span id="KERNEL_MODE"></span>Kernel mode</span></span>
</dt> <dd>

<span data-ttu-id="7b01d-117">Der Prozessor Modus, in dem Systemdienste und Gerätetreiber ausgeführt werden.</span><span class="sxs-lookup"><span data-stu-id="7b01d-117">The processor mode in which system services and device drivers run.</span></span> <span data-ttu-id="7b01d-118">Alle Schnittstellen und CPU-Anweisungen sind verfügbar, und der Zugriff auf den gesamten Speicher ist möglich.</span><span class="sxs-lookup"><span data-stu-id="7b01d-118">All interfaces and CPU instructions are available, and all memory is accessible.</span></span>

</dd> <dt>

<span data-ttu-id="7b01d-119"><span id="Minidump_file"></span><span id="minidump_file"></span><span id="MINIDUMP_FILE"></span>Minidumpdatei</span><span class="sxs-lookup"><span data-stu-id="7b01d-119"><span id="Minidump_file"></span><span id="minidump_file"></span><span id="MINIDUMP_FILE"></span>Minidump file</span></span>
</dt> <dd>

<span data-ttu-id="7b01d-120">Anwendungen können Minidump-Dateien im Benutzermodus entwickeln, die eine nützliche Teilmenge der in einer Absturz Abbild Datei enthaltenen Informationen enthalten.</span><span class="sxs-lookup"><span data-stu-id="7b01d-120">Applications can produce user-mode minidump files, which contain a useful subset of the information contained in a crash dump file.</span></span> <span data-ttu-id="7b01d-121">Weitere Informationen finden Sie unter [Minidump files](minidump-files.md).</span><span class="sxs-lookup"><span data-stu-id="7b01d-121">For more information, see [Minidump Files](minidump-files.md).</span></span>

</dd> <dt>

<span data-ttu-id="7b01d-122"><span id="STOP_code"></span><span id="stop_code"></span><span id="STOP_CODE"></span>Code Abbrechen</span><span class="sxs-lookup"><span data-stu-id="7b01d-122"><span id="STOP_code"></span><span id="stop_code"></span><span id="STOP_CODE"></span>STOP code</span></span>
</dt> <dd>

<span data-ttu-id="7b01d-123">Der Fehlercode, der den Fehler angibt, mit dem der Systemkernel nicht mehr ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="7b01d-123">The error code that identifies the error that stopped the system kernel from continuing to run.</span></span>

</dd> <dt>

<span data-ttu-id="7b01d-124"><span id="Symbol_files"></span><span id="symbol_files"></span><span id="SYMBOL_FILES"></span>Symbol Dateien</span><span class="sxs-lookup"><span data-stu-id="7b01d-124"><span id="Symbol_files"></span><span id="symbol_files"></span><span id="SYMBOL_FILES"></span>Symbol files</span></span>
</dt> <dd>

<span data-ttu-id="7b01d-125">Alle Systemanwendungen, Treiber und DLLs werden so erstellt, dass Ihre Debuginformationen in separaten Dateien gespeichert werden, die als Symbol Dateien bezeichnet werden.</span><span class="sxs-lookup"><span data-stu-id="7b01d-125">All system applications, drivers, and DLLs are built such that their debugging information resides in separate files known as symbol files.</span></span> <span data-ttu-id="7b01d-126">Daher ist das System kleiner und schneller, aber es kann dennoch debuggten werden, wenn die Symbol Dateien installiert sind.</span><span class="sxs-lookup"><span data-stu-id="7b01d-126">Therefore, the system is smaller and faster, yet it can still be debugged if the symbol files are installed.</span></span> <span data-ttu-id="7b01d-127">Weitere Informationen finden Sie unter [Symbol Dateien](symbol-files.md).</span><span class="sxs-lookup"><span data-stu-id="7b01d-127">For more information, see [Symbol Files](symbol-files.md).</span></span>

</dd> <dt>

<span data-ttu-id="7b01d-128"><span id="User_mode"></span><span id="user_mode"></span><span id="USER_MODE"></span>Benutzermodus</span><span class="sxs-lookup"><span data-stu-id="7b01d-128"><span id="User_mode"></span><span id="user_mode"></span><span id="USER_MODE"></span>User mode</span></span>
</dt> <dd>

<span data-ttu-id="7b01d-129">Der Prozessor Modus, in dem Anwendungen ausgeführt werden.</span><span class="sxs-lookup"><span data-stu-id="7b01d-129">The processor mode in which applications run.</span></span> <span data-ttu-id="7b01d-130">Ein eingeschränkter Satz von Schnittstellen ist in diesem Modus verfügbar, und der Zugriff auf Systemdaten ist begrenzt.</span><span class="sxs-lookup"><span data-stu-id="7b01d-130">A limited set of interfaces are available in this mode, and access to system data is limited.</span></span>

</dd> </dl>

## <a name="related-topics"></a><span data-ttu-id="7b01d-131">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="7b01d-131">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="7b01d-132">Konfigurieren von automatischem Debugging</span><span class="sxs-lookup"><span data-stu-id="7b01d-132">Configuring Automatic Debugging</span></span>](configuring-automatic-debugging.md)
</dt> </dl>

 

 



