---
description: In diesem Thema werden Strukturen aufgeführt, die mit Prozessen, Threads, Prozessoren, Auftragsobjekten und der Benutzermodusplanung (UMS) verwendet werden.
ms.assetid: dbb50193-4c67-494e-9c46-2ac3106fac9a
title: Prozess- und Threadstrukturen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2b5893340c72ee46eff43b16db936025fbb5463fbe0cc10e2eba1829962269d1
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "120081380"
---
# <a name="process-and-thread-structures"></a>Prozess- und Threadstrukturen

In diesem Thema werden Strukturen aufgeführt, die mit Prozessen, Threads, Prozessoren, Auftragsobjekten und der Benutzermodusplanung (UMS) verwendet werden.

## <a name="process-and-thread-structures"></a>Prozess- und Threadstrukturen

Die folgenden Strukturen werden mit Prozessen und Threads verwendet:

-   [**INFORMATIONEN ZUM \_ \_ APP-ARBEITSSPEICHER**](/windows/win32/api/processthreadsapi/ns-processthreadsapi-app_memory_information)
-   [**AR \_ STATE**](/windows/win32/api/winuser/ne-winuser-ar_state)
-   [**\_CACHE-DESKRIPTOR**](/windows/desktop/api/WinNT/ns-winnt-cache_descriptor)
-   [**\_E/A-LEISTUNGSINDIKATOREN**](/windows/desktop/api/WinNT/ns-winnt-io_counters)
-   [**\_AUSRICHTUNGSPRÄFERENZ**](/windows/desktop/api/WinUser/ne-winuser-orientation_preference)
-   [**Peb**](/windows/desktop/api/Winternl/ns-winternl-peb)
-   [**PEB \_ LDR \_ DATA**](/windows/desktop/api/Winternl/ns-winternl-peb_ldr_data)
-   [**\_PROZESSINFORMATIONEN**](/windows/win32/api/processthreadsapi/ns-processthreadsapi-process_information)
-   [**INFORMATIONEN ZUR \_ \_ PROZESSSPEICHERERSCHÖPFUNG \_**](/windows/win32/api/processthreadsapi/ns-processthreadsapi-process_memory_exhaustion_info)
-   [**\_ \_ PROZESSMINDERUNGS-ASLR-RICHTLINIE \_**](/windows/desktop/api/WinNT/ns-winnt-process_mitigation_aslr_policy)
-   [**PROCESS \_ MITIGATION \_ BINARY \_ SIGNATURE \_ POLICY**](/windows/desktop/api/WinNT/ns-winnt-process_mitigation_binary_signature_policy)
-   [**PROCESS \_ MITIGATION CONTROL FLOW \_ \_ \_ \_ GUARD-RICHTLINIE**](/windows/desktop/api/WinNT/ns-winnt-process_mitigation_control_flow_guard_policy)
-   [**\_ \_ PROZESSMINDERUNGS-DEP-RICHTLINIE \_**](/windows/desktop/api/WinNT/ns-winnt-process_mitigation_dep_policy)
-   [**RICHTLINIE FÜR \_ DYNAMISCHEN \_ CODE ZUR \_ \_ PROZESSMINDERUNG**](/windows/desktop/api/WinNT/ns-winnt-process_mitigation_dynamic_code_policy)
-   [**RICHTLINIE DEAKTIVIEREN \_ DES \_ \_ PROZESSMINDERUNGSPUNKTS \_ \_**](/windows/desktop/api/winnt/ns-winnt-process_mitigation_extension_point_disable_policy)
-   [**PROCESS \_ MITIGATION \_ FONT \_ DISABLE \_ POLICY**](/windows/desktop/api/WinNT/ns-winnt-process_mitigation_font_disable_policy)
-   [**\_PROZESSMINDERUNGSRICHTLINIE ZUM LADEN VON \_ \_ \_ IMAGES**](/windows/desktop/api/WinNT/ns-winnt-process_mitigation_image_load_policy)
-   [**PROCESS \_ MITIGATION \_ STRICT \_ HANDLE \_ CHECK \_ POLICY**](/windows/desktop/api/WinNT/ns-winnt-process_mitigation_strict_handle_check_policy)
-   [**PROCESS \_ MITIGATION SYSTEM CALL DISABLE POLICY (PROZESSMINDERUNGSSYSTEMAUFRUF: \_ RICHTLINIE \_ \_ \_ DEAKTIVIEREN)**](/windows/desktop/api/WinNT/ns-winnt-process_mitigation_system_call_disable_policy)
-   [**\_ \_ RTL-BENUTZERPROZESSPARAMETER \_**](/windows/desktop/api/Winternl/ns-winternl-rtl_user_process_parameters)
-   [**STARTUPINFO**](/windows/win32/api/processthreadsapi/ns-processthreadsapi-startupinfoa)
-   [**STARTUPINFOEX**](/windows/desktop/api/WinBase/ns-winbase-startupinfoexa)
-   [**TEB**](/windows/desktop/api/Winternl/ns-winternl-teb)

## <a name="processor-structures"></a>Prozessorstrukturen

Die folgenden Strukturen werden mit Prozessoren und Prozessorgruppen verwendet:

-   [**\_CACHEBEZIEHUNG**](/windows/desktop/api/WinNT/ns-winnt-cache_relationship)
-   [**\_GRUPPENAFFINITÄT**](/windows/desktop/api/WinNT/ns-winnt-group_affinity)
-   [**GROUP \_ RELATIONSHIP**](/windows/desktop/api/WinNT/ns-winnt-group_relationship)
-   [**\_NUMA-KNOTENBEZIEHUNG \_**](/windows/desktop/api/WinNT/ns-winnt-numa_node_relationship)
-   [**\_ \_ PROZESSORGRUPPENINFORMATIONEN**](/windows/desktop/api/WinNT/ns-winnt-processor_group_info)
-   [**\_PROZESSORNUMMER**](/windows/desktop/api/WinNT/ns-winnt-processor_number)
-   [**\_PROZESSORBEZIEHUNG**](/windows/desktop/api/WinNT/ne-winnt-logical_processor_relationship)
-   [**INFORMATIONEN \_ ZUM SYSTEM-CPU-SATZ \_ \_**](/windows/desktop/api/winnt/ns-winnt-system_cpu_set_information)
-   [**SYSTEMINFORMATIONEN \_ \_ ZUM LOGISCHEN \_ PROZESSOR**](/windows/desktop/api/WinNT/ns-winnt-system_logical_processor_information)
-   [**SYSTEM \_ LOGICAL \_ PROCESSOR \_ INFORMATION \_ EX**](/windows/desktop/api/WinNT/ns-winnt-system_logical_processor_information_ex)

## <a name="dispatcher-queue-structure"></a>Warteschlangenstruktur des Verteilers

Die folgende -Struktur wird verwendet, um einen [DispatcherQueueController zu erstellen.](/uwp/api/windows.system.dispatcherqueuecontroller)

-   [**DispatcherQueueOptions**](/windows/desktop/api/DispatcherQueue/ns-dispatcherqueue-dispatcherqueueoptions)

## <a name="job-object-structures"></a>Auftragsobjektstrukturen

Die folgenden Strukturen werden mit Auftragsobjekten verwendet:

-   [**JOBOBJECT \_ ASSOCIATE \_ COMPLETION \_ PORT**](/windows/desktop/api/WinNT/ns-winnt-jobobject_associate_completion_port)
-   [**GRUNDLEGENDE INFORMATIONEN ZUR \_ \_ \_ AUFTRAGSOBJEKTBUCHHALTUNG**](/windows/desktop/api/WinNT/ns-winnt-jobobject_basic_accounting_information)
-   [**GRUNDLEGENDE UND \_ \_ E/A-KONTOFÜHRUNGSINFORMATIONEN \_ \_ FÜR \_ JOBOBJECT**](/windows/desktop/api/WinNT/ns-winnt-jobobject_basic_and_io_accounting_information)
-   [**GRUNDLEGENDE INFORMATIONEN \_ ZUM JOBOBJECT-GRENZWERT \_ \_**](/windows/desktop/api/WinNT/ns-winnt-jobobject_basic_limit_information)
-   [**JOBOBJECT \_ BASIC \_ PROCESS \_ ID \_ LIST**](/windows/desktop/api/WinNT/ns-winnt-jobobject_basic_process_id_list)
-   [**GRUNDLEGENDE EINSCHRÄNKUNGEN \_ DER JOBOBJECT-BENUTZEROBERFLÄCHE \_ \_**](/windows/desktop/api/WinNT/ns-winnt-jobobject_basic_ui_restrictions)
-   [**INFORMATIONEN ZUM \_ \_ JOBOBJECT-ENDE \_ \_ DER \_ AUFTRAGSZEIT**](/windows/desktop/api/WinNT/ns-winnt-jobobject_end_of_job_time_information)
-   [**INFORMATIONEN ZUM \_ ERWEITERTEN \_ GRENZWERT FÜR JOBOBJECT \_**](/windows/desktop/api/WinNT/ns-winnt-jobobject_extended_limit_information)
-   [**INFORMATIONEN ZUM \_ \_ JOBOBJECT-SICHERHEITSLIMIT \_**](/windows/desktop/api/WinNT/ns-winnt-jobobject_security_limit_information)

## <a name="user-mode-scheduling-structures"></a>User-Mode Planungsstrukturen

Die folgenden Strukturen werden mit UMS verwendet:

-   [**UMS \_ CREATE \_ THREAD \_ ATTRIBUTES**](/windows/desktop/api/WinNT/ns-winnt-ums_create_thread_attributes)
-   [**STARTINFORMATIONEN ZUM UMS \_ SCHEDULER \_ \_**](/windows/desktop/api/WinBase/ns-winbase-ums_scheduler_startup_info)
-   [**INFORMATIONEN ZUM \_ \_ UMS-SYSTEMTHREAD \_**](/windows/desktop/api/WinBase/ns-winbase-ums_system_thread_information)

 

 
