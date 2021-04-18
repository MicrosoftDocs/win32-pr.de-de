---
title: Ausrichtungsfehler
description: Ausrichtungsfehler
ms.assetid: 16e69aec-3aec-4684-bf37-b3e5db6e4f87
keywords:
- Ausrichtungsfehler 64-Bit-Windows-Programmierung
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 318a7a55010ac148354d000ece32c91a8652f821
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "106338485"
---
# <a name="alignment-faults"></a><span data-ttu-id="560d7-104">Ausrichtungsfehler</span><span class="sxs-lookup"><span data-stu-id="560d7-104">Alignment Faults</span></span>

<span data-ttu-id="560d7-105">Der System Ausrichtungsfehler Handler ist auf Itanium-basierten Systemen standardmäßig deaktiviert.</span><span class="sxs-lookup"><span data-stu-id="560d7-105">The system alignment-fault handler is turned off by default on Itanium-based systems.</span></span> <span data-ttu-id="560d7-106">Daher wird durch den nicht ausgerichteten Datenzugriff eine Ausnahme generiert, die nicht automatisch vom System korrigiert wird, es sei denn, die Anwendung fängt die Ausnahme in einem [Frame basierten Ausnahmehandler](/windows/desktop/Debug/frame-based-exception-handling)ab.</span><span class="sxs-lookup"><span data-stu-id="560d7-106">Therefore, any unaligned data access generates an exception that will not automatically be fixed by the system unless the application catches the exception in a [frame-based exception handler](/windows/desktop/Debug/frame-based-exception-handling).</span></span> <span data-ttu-id="560d7-107">Um den systemausrichtungs-Fault-Handler zu aktivieren, müssen Sie [**die Funktion "**](/windows/desktop/api/errhandlingapi/nf-errhandlingapi-seterrormode) \*" mit " **SEM \_ noalignmentfaultexcept**" aufrufen.</span><span class="sxs-lookup"><span data-stu-id="560d7-107">To enable the system alignment-fault hander, call the [**SetErrorMode**](/windows/desktop/api/errhandlingapi/nf-errhandlingapi-seterrormode) function with **SEM\_NOALIGNMENTFAULTEXCEPT**.</span></span> <span data-ttu-id="560d7-108">Beachten Sie jedoch, dass es bei Prozessen zu schwerwiegenden Leistungseinbußen kommen kann, wenn der System Ausrichtungsfehler Handler aktiviert ist und der Prozess Ausrichtungsfehler generiert.</span><span class="sxs-lookup"><span data-stu-id="560d7-108">However, note that processes may experience severe performance degradation if the system alignment-fault handler is enabled and the process generates alignment faults.</span></span>

<span data-ttu-id="560d7-109">Wenn der WinDbg-Debugger als System Debugger installiert wurde, wird WinDBG automatisch gestartet, wenn ein Prozess im System eine nicht behandelte Ausnahme generiert.</span><span class="sxs-lookup"><span data-stu-id="560d7-109">If the WinDbg debugger has been installed as the system debugger, WinDbg will automatically be launched if any process on the system generates an unhandled exception.</span></span> <span data-ttu-id="560d7-110">Wenn Sie keinen Debugger als System Debugger installiert haben, zeigt das System ein Dialogfeld an, in dem Sie darauf hingewiesen werden, dass die Anwendung einen Fehler festgestellt hat und die Gelegenheit bietet, das Problem an Microsoft zu melden.</span><span class="sxs-lookup"><span data-stu-id="560d7-110">If you do not have a debugger installed as your system debugger, the system displays a dialog box stating that your application has encountered an error and providing the opportunity to report the problem to Microsoft.</span></span>

<span data-ttu-id="560d7-111">Auf x64-und ARM64-Systemen werden alle Ausrichtungsfehler durch eine Kombination aus Hardware und Software behandelt.</span><span class="sxs-lookup"><span data-stu-id="560d7-111">On x64 and ARM64 systems, any alignment faults are handled by a combination of hardware and software.</span></span> <span data-ttu-id="560d7-112">Für eine optimale Leistung sollte der gesamte Zugriff auf den Arbeitsspeicher ordnungsgemäß ausgerichtet werden.</span><span class="sxs-lookup"><span data-stu-id="560d7-112">For best performance, all access to memory should be properly aligned.</span></span> <span data-ttu-id="560d7-113">Außerdem sollte der nicht ausgerichtete [Zugriff auf Interlocked-Variablen](/windows/desktop/Sync/interlocked-variable-access) auf ARM64 vermieden werden, da diese Vorgänge nicht atomarisch sind.</span><span class="sxs-lookup"><span data-stu-id="560d7-113">In addition, unaligned [interlocked variable access](/windows/desktop/Sync/interlocked-variable-access) should be avoided on ARM64, as these operations are not atomic-safe.</span></span>

 

 