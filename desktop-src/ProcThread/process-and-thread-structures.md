---
description: In diesem Thema werden die Strukturen aufgelistet, die mit Prozessen, Threads, Prozessoren, Auftrags Objekten und Benutzermodus-Zeitplanung (ums) verwendet werden.
ms.assetid: dbb50193-4c67-494e-9c46-2ac3106fac9a
title: Prozess-und Thread Strukturen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 59b2b4a8209c3f1f9fb3163c849fa2c229d2bdf5
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106356157"
---
# <a name="process-and-thread-structures"></a><span data-ttu-id="346dc-103">Prozess-und Thread Strukturen</span><span class="sxs-lookup"><span data-stu-id="346dc-103">Process and Thread Structures</span></span>

<span data-ttu-id="346dc-104">In diesem Thema werden die Strukturen aufgelistet, die mit Prozessen, Threads, Prozessoren, Auftrags Objekten und Benutzermodus-Zeitplanung (ums) verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="346dc-104">This topic lists structures that are used with processes, threads, processors, job objects, and user-mode scheduling (UMS).</span></span>

## <a name="process-and-thread-structures"></a><span data-ttu-id="346dc-105">Prozess-und Thread Strukturen</span><span class="sxs-lookup"><span data-stu-id="346dc-105">Process and Thread Structures</span></span>

<span data-ttu-id="346dc-106">Die folgenden Strukturen werden für Prozesse und Threads verwendet:</span><span class="sxs-lookup"><span data-stu-id="346dc-106">The following structures are used with processes and threads:</span></span>

-   [<span data-ttu-id="346dc-107">**APP- \_ Speicher \_ Informationen**</span><span class="sxs-lookup"><span data-stu-id="346dc-107">**APP\_MEMORY\_INFORMATION**</span></span>](/windows/win32/api/processthreadsapi/ns-processthreadsapi-app_memory_information)
-   [<span data-ttu-id="346dc-108">**AR- \_ Status**</span><span class="sxs-lookup"><span data-stu-id="346dc-108">**AR\_STATE**</span></span>](/windows/win32/api/winuser/ne-winuser-ar_state)
-   [<span data-ttu-id="346dc-109">**Cache \_ Deskriptor**</span><span class="sxs-lookup"><span data-stu-id="346dc-109">**CACHE\_DESCRIPTOR**</span></span>](/windows/desktop/api/WinNT/ns-winnt-cache_descriptor)
-   [<span data-ttu-id="346dc-110">**IO-Leistungsindikatoren \_**</span><span class="sxs-lookup"><span data-stu-id="346dc-110">**IO\_COUNTERS**</span></span>](/windows/desktop/api/WinNT/ns-winnt-io_counters)
-   [<span data-ttu-id="346dc-111">**Ausrichtung \_**</span><span class="sxs-lookup"><span data-stu-id="346dc-111">**ORIENTATION\_PREFERENCE**</span></span>](/windows/desktop/api/WinUser/ne-winuser-orientation_preference)
-   [<span data-ttu-id="346dc-112">**Peer**</span><span class="sxs-lookup"><span data-stu-id="346dc-112">**PEB**</span></span>](/windows/desktop/api/Winternl/ns-winternl-peb)
-   [<span data-ttu-id="346dc-113">**\_lb-LDR- \_ Daten**</span><span class="sxs-lookup"><span data-stu-id="346dc-113">**PEB\_LDR\_DATA**</span></span>](/windows/desktop/api/Winternl/ns-winternl-peb_ldr_data)
-   [<span data-ttu-id="346dc-114">**Prozess \_ Informationen**</span><span class="sxs-lookup"><span data-stu-id="346dc-114">**PROCESS\_INFORMATION**</span></span>](/windows/win32/api/processthreadsapi/ns-processthreadsapi-process_information)
-   [<span data-ttu-id="346dc-115">**Informationen zum Prozess \_ Speicher \_ Erschöpfung \_**</span><span class="sxs-lookup"><span data-stu-id="346dc-115">**PROCESS\_MEMORY\_EXHAUSTION\_INFO**</span></span>](/windows/win32/api/processthreadsapi/ns-processthreadsapi-process_memory_exhaustion_info)
-   [<span data-ttu-id="346dc-116">**\_ \_ ASLR- \_ Richtlinie zur Prozess Minderung**</span><span class="sxs-lookup"><span data-stu-id="346dc-116">**PROCESS\_MITIGATION\_ASLR\_POLICY**</span></span>](/windows/desktop/api/WinNT/ns-winnt-process_mitigation_aslr_policy)
-   [<span data-ttu-id="346dc-117">**\_ \_ binäre \_ Signatur \_ Richtlinie für die Prozess Minderung**</span><span class="sxs-lookup"><span data-stu-id="346dc-117">**PROCESS\_MITIGATION\_BINARY\_SIGNATURE\_POLICY**</span></span>](/windows/desktop/api/WinNT/ns-winnt-process_mitigation_binary_signature_policy)
-   [<span data-ttu-id="346dc-118">**\_ \_ \_ \_ \_ Richtlinie zum Schutz der Ablauf Steuerung für Prozesse**</span><span class="sxs-lookup"><span data-stu-id="346dc-118">**PROCESS\_MITIGATION\_CONTROL\_FLOW\_GUARD\_POLICY**</span></span>](/windows/desktop/api/WinNT/ns-winnt-process_mitigation_control_flow_guard_policy)
-   [<span data-ttu-id="346dc-119">**\_DEP- \_ \_ Richtlinie zur Prozess Minderung**</span><span class="sxs-lookup"><span data-stu-id="346dc-119">**PROCESS\_MITIGATION\_DEP\_POLICY**</span></span>](/windows/desktop/api/WinNT/ns-winnt-process_mitigation_dep_policy)
-   [<span data-ttu-id="346dc-120">**\_ \_ dynamische \_ Code \_ Richtlinie für die Prozess Minderung**</span><span class="sxs-lookup"><span data-stu-id="346dc-120">**PROCESS\_MITIGATION\_DYNAMIC\_CODE\_POLICY**</span></span>](/windows/desktop/api/WinNT/ns-winnt-process_mitigation_dynamic_code_policy)
-   [<span data-ttu-id="346dc-121">**\_ \_ \_ \_ Richtlinie zum Deaktivieren des Erweiterungs Punkts zum Prozess \_**</span><span class="sxs-lookup"><span data-stu-id="346dc-121">**PROCESS\_MITIGATION\_EXTENSION\_POINT\_DISABLE\_POLICY**</span></span>](/windows/desktop/api/winnt/ns-winnt-process_mitigation_extension_point_disable_policy)
-   [<span data-ttu-id="346dc-122">**\_ \_ \_ Richtlinie zum Deaktivieren der Schriftart \_ zur Verarbeitung**</span><span class="sxs-lookup"><span data-stu-id="346dc-122">**PROCESS\_MITIGATION\_FONT\_DISABLE\_POLICY**</span></span>](/windows/desktop/api/WinNT/ns-winnt-process_mitigation_font_disable_policy)
-   [<span data-ttu-id="346dc-123">**\_Abbild \_ \_ Lade \_ Richtlinie für Prozess Minderung**</span><span class="sxs-lookup"><span data-stu-id="346dc-123">**PROCESS\_MITIGATION\_IMAGE\_LOAD\_POLICY**</span></span>](/windows/desktop/api/WinNT/ns-winnt-process_mitigation_image_load_policy)
-   [<span data-ttu-id="346dc-124">**Richtlinie zur Vermeidung von \_ \_ strengen \_ Handles \_ \_ der Prozess Minderung**</span><span class="sxs-lookup"><span data-stu-id="346dc-124">**PROCESS\_MITIGATION\_STRICT\_HANDLE\_CHECK\_POLICY**</span></span>](/windows/desktop/api/WinNT/ns-winnt-process_mitigation_strict_handle_check_policy)
-   [<span data-ttu-id="346dc-125">**\_ \_ \_ \_ Richtlinie zum Deaktivieren des System aufrubungs Systems \_**</span><span class="sxs-lookup"><span data-stu-id="346dc-125">**PROCESS\_MITIGATION\_SYSTEM\_CALL\_DISABLE\_POLICY**</span></span>](/windows/desktop/api/WinNT/ns-winnt-process_mitigation_system_call_disable_policy)
-   [<span data-ttu-id="346dc-126">**\_Benutzer \_ Prozess \_ Parameter von RTL**</span><span class="sxs-lookup"><span data-stu-id="346dc-126">**RTL\_USER\_PROCESS\_PARAMETERS**</span></span>](/windows/desktop/api/Winternl/ns-winternl-rtl_user_process_parameters)
-   [<span data-ttu-id="346dc-127">**STARTUPINFO**</span><span class="sxs-lookup"><span data-stu-id="346dc-127">**STARTUPINFO**</span></span>](/windows/win32/api/processthreadsapi/ns-processthreadsapi-startupinfoa)
-   [<span data-ttu-id="346dc-128">**Startupinfoex**</span><span class="sxs-lookup"><span data-stu-id="346dc-128">**STARTUPINFOEX**</span></span>](/windows/desktop/api/WinBase/ns-winbase-startupinfoexa)
-   [<span data-ttu-id="346dc-129">**TEB**</span><span class="sxs-lookup"><span data-stu-id="346dc-129">**TEB**</span></span>](/windows/desktop/api/Winternl/ns-winternl-teb)

## <a name="processor-structures"></a><span data-ttu-id="346dc-130">Prozessor Strukturen</span><span class="sxs-lookup"><span data-stu-id="346dc-130">Processor Structures</span></span>

<span data-ttu-id="346dc-131">Die folgenden Strukturen werden mit Prozessoren und Prozessor Gruppen verwendet:</span><span class="sxs-lookup"><span data-stu-id="346dc-131">The following structures are used with processors and processor groups:</span></span>

-   [<span data-ttu-id="346dc-132">**Cache \_ Beziehung**</span><span class="sxs-lookup"><span data-stu-id="346dc-132">**CACHE\_RELATIONSHIP**</span></span>](/windows/desktop/api/WinNT/ns-winnt-cache_relationship)
-   [<span data-ttu-id="346dc-133">**Gruppen \_ Affinität**</span><span class="sxs-lookup"><span data-stu-id="346dc-133">**GROUP\_AFFINITY**</span></span>](/windows/desktop/api/WinNT/ns-winnt-group_affinity)
-   [<span data-ttu-id="346dc-134">**Gruppen \_ Beziehung**</span><span class="sxs-lookup"><span data-stu-id="346dc-134">**GROUP\_RELATIONSHIP**</span></span>](/windows/desktop/api/WinNT/ns-winnt-group_relationship)
-   [<span data-ttu-id="346dc-135">**NUMA- \_ Knoten \_ Beziehung**</span><span class="sxs-lookup"><span data-stu-id="346dc-135">**NUMA\_NODE\_RELATIONSHIP**</span></span>](/windows/desktop/api/WinNT/ns-winnt-numa_node_relationship)
-   [<span data-ttu-id="346dc-136">**Informationen zur Prozessor \_ Gruppe \_**</span><span class="sxs-lookup"><span data-stu-id="346dc-136">**PROCESSOR\_GROUP\_INFO**</span></span>](/windows/desktop/api/WinNT/ns-winnt-processor_group_info)
-   [<span data-ttu-id="346dc-137">**Prozessor \_ Nummer**</span><span class="sxs-lookup"><span data-stu-id="346dc-137">**PROCESSOR\_NUMBER**</span></span>](/windows/desktop/api/WinNT/ns-winnt-processor_number)
-   [<span data-ttu-id="346dc-138">**Prozessor \_ Beziehung**</span><span class="sxs-lookup"><span data-stu-id="346dc-138">**PROCESSOR\_RELATIONSHIP**</span></span>](/windows/desktop/api/WinNT/ne-winnt-logical_processor_relationship)
-   [<span data-ttu-id="346dc-139">**Informationen zum System- \_ CPU- \_ Satz \_**</span><span class="sxs-lookup"><span data-stu-id="346dc-139">**SYSTEM\_CPU\_SET\_INFORMATION**</span></span>](/windows/desktop/api/winnt/ns-winnt-system_cpu_set_information)
-   [<span data-ttu-id="346dc-140">**\_Informationen zum logischen System \_ Prozessor \_**</span><span class="sxs-lookup"><span data-stu-id="346dc-140">**SYSTEM\_LOGICAL\_PROCESSOR\_INFORMATION**</span></span>](/windows/desktop/api/WinNT/ns-winnt-system_logical_processor_information)
-   [<span data-ttu-id="346dc-141">**\_Informationen zum logischen System Prozessor ( \_ \_ \_ Ex)**</span><span class="sxs-lookup"><span data-stu-id="346dc-141">**SYSTEM\_LOGICAL\_PROCESSOR\_INFORMATION\_EX**</span></span>](/windows/desktop/api/WinNT/ns-winnt-system_logical_processor_information_ex)

## <a name="dispatcher-queue-structure"></a><span data-ttu-id="346dc-142">Struktur der Dispatcher-Warteschlange</span><span class="sxs-lookup"><span data-stu-id="346dc-142">Dispatcher Queue Structure</span></span>

<span data-ttu-id="346dc-143">Die folgende Struktur wird verwendet, um einen [dispatcherqueuecontroller](/uwp/api/windows.system.dispatcherqueuecontroller)zu erstellen.</span><span class="sxs-lookup"><span data-stu-id="346dc-143">The following structure is used to create a [DispatcherQueueController](/uwp/api/windows.system.dispatcherqueuecontroller).</span></span>

-   [<span data-ttu-id="346dc-144">**Dispatcherqueueoptions**</span><span class="sxs-lookup"><span data-stu-id="346dc-144">**DispatcherQueueOptions**</span></span>](/windows/desktop/api/DispatcherQueue/ns-dispatcherqueue-dispatcherqueueoptions)

## <a name="job-object-structures"></a><span data-ttu-id="346dc-145">Auftrags Objektstrukturen</span><span class="sxs-lookup"><span data-stu-id="346dc-145">Job Object Structures</span></span>

<span data-ttu-id="346dc-146">Die folgenden Strukturen werden mit Auftrags Objekten verwendet:</span><span class="sxs-lookup"><span data-stu-id="346dc-146">The following structures are used with job objects:</span></span>

-   [<span data-ttu-id="346dc-147">**JobObject \_ - \_ Abschluss \_ Anschluss zuordnen**</span><span class="sxs-lookup"><span data-stu-id="346dc-147">**JOBOBJECT\_ASSOCIATE\_COMPLETION\_PORT**</span></span>](/windows/desktop/api/WinNT/ns-winnt-jobobject_associate_completion_port)
-   [<span data-ttu-id="346dc-148">**\_grundlegende Informationen zur \_ Buchhaltung von JobObject \_**</span><span class="sxs-lookup"><span data-stu-id="346dc-148">**JOBOBJECT\_BASIC\_ACCOUNTING\_INFORMATION**</span></span>](/windows/desktop/api/WinNT/ns-winnt-jobobject_basic_accounting_information)
-   [<span data-ttu-id="346dc-149">**\_grundlegende Informationen und e/a \_ - \_ \_ Buchhaltungs \_ Informationen**</span><span class="sxs-lookup"><span data-stu-id="346dc-149">**JOBOBJECT\_BASIC\_AND\_IO\_ACCOUNTING\_INFORMATION**</span></span>](/windows/desktop/api/WinNT/ns-winnt-jobobject_basic_and_io_accounting_information)
-   [<span data-ttu-id="346dc-150">**\_Informationen zu grundlegenden \_ \_ Informationen zu JobObject**</span><span class="sxs-lookup"><span data-stu-id="346dc-150">**JOBOBJECT\_BASIC\_LIMIT\_INFORMATION**</span></span>](/windows/desktop/api/WinNT/ns-winnt-jobobject_basic_limit_information)
-   [<span data-ttu-id="346dc-151">**\_Liste der grundlegenden \_ Prozess- \_ IDs \_ in JobObject**</span><span class="sxs-lookup"><span data-stu-id="346dc-151">**JOBOBJECT\_BASIC\_PROCESS\_ID\_LIST**</span></span>](/windows/desktop/api/WinNT/ns-winnt-jobobject_basic_process_id_list)
-   [<span data-ttu-id="346dc-152">**\_grundlegende Einschränkungen der \_ Benutzeroberfläche von JobObject \_**</span><span class="sxs-lookup"><span data-stu-id="346dc-152">**JOBOBJECT\_BASIC\_UI\_RESTRICTIONS**</span></span>](/windows/desktop/api/WinNT/ns-winnt-jobobject_basic_ui_restrictions)
-   [<span data-ttu-id="346dc-153">**JobObject- \_ Ende \_ der \_ Auftrags \_ Zeit \_ Informationen**</span><span class="sxs-lookup"><span data-stu-id="346dc-153">**JOBOBJECT\_END\_OF\_JOB\_TIME\_INFORMATION**</span></span>](/windows/desktop/api/WinNT/ns-winnt-jobobject_end_of_job_time_information)
-   [<span data-ttu-id="346dc-154">**\_Informationen zu erweiterten \_ \_ Informationen zu JobObject**</span><span class="sxs-lookup"><span data-stu-id="346dc-154">**JOBOBJECT\_EXTENDED\_LIMIT\_INFORMATION**</span></span>](/windows/desktop/api/WinNT/ns-winnt-jobobject_extended_limit_information)
-   [<span data-ttu-id="346dc-155">**\_Informationen zum Sicherheits \_ Limit \_ für JobObject**</span><span class="sxs-lookup"><span data-stu-id="346dc-155">**JOBOBJECT\_SECURITY\_LIMIT\_INFORMATION**</span></span>](/windows/desktop/api/WinNT/ns-winnt-jobobject_security_limit_information)

## <a name="user-mode-scheduling-structures"></a><span data-ttu-id="346dc-156">Planen von User-Mode Planung</span><span class="sxs-lookup"><span data-stu-id="346dc-156">User-Mode Scheduling Structures</span></span>

<span data-ttu-id="346dc-157">Die folgenden Strukturen werden mit ums verwendet:</span><span class="sxs-lookup"><span data-stu-id="346dc-157">The following structures are used with UMS:</span></span>

-   [<span data-ttu-id="346dc-158">**UMS \_ Create \_ Thread- \_ Attribute**</span><span class="sxs-lookup"><span data-stu-id="346dc-158">**UMS\_CREATE\_THREAD\_ATTRIBUTES**</span></span>](/windows/desktop/api/WinNT/ns-winnt-ums_create_thread_attributes)
-   [<span data-ttu-id="346dc-159">**UMS- \_ Scheduler- \_ Start \_ Informationen**</span><span class="sxs-lookup"><span data-stu-id="346dc-159">**UMS\_SCHEDULER\_STARTUP\_INFO**</span></span>](/windows/desktop/api/WinBase/ns-winbase-ums_scheduler_startup_info)
-   [<span data-ttu-id="346dc-160">**UMS- \_ System \_ Thread \_ Informationen**</span><span class="sxs-lookup"><span data-stu-id="346dc-160">**UMS\_SYSTEM\_THREAD\_INFORMATION**</span></span>](/windows/desktop/api/WinBase/ns-winbase-ums_system_thread_information)

 

 
