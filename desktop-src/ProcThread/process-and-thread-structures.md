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
# <a name="process-and-thread-structures"></a>Prozess-und Thread Strukturen

In diesem Thema werden die Strukturen aufgelistet, die mit Prozessen, Threads, Prozessoren, Auftrags Objekten und Benutzermodus-Zeitplanung (ums) verwendet werden.

## <a name="process-and-thread-structures"></a>Prozess-und Thread Strukturen

Die folgenden Strukturen werden für Prozesse und Threads verwendet:

-   [**APP- \_ Speicher \_ Informationen**](/windows/win32/api/processthreadsapi/ns-processthreadsapi-app_memory_information)
-   [**AR- \_ Status**](/windows/win32/api/winuser/ne-winuser-ar_state)
-   [**Cache \_ Deskriptor**](/windows/desktop/api/WinNT/ns-winnt-cache_descriptor)
-   [**IO-Leistungsindikatoren \_**](/windows/desktop/api/WinNT/ns-winnt-io_counters)
-   [**Ausrichtung \_**](/windows/desktop/api/WinUser/ne-winuser-orientation_preference)
-   [**Peer**](/windows/desktop/api/Winternl/ns-winternl-peb)
-   [**\_lb-LDR- \_ Daten**](/windows/desktop/api/Winternl/ns-winternl-peb_ldr_data)
-   [**Prozess \_ Informationen**](/windows/win32/api/processthreadsapi/ns-processthreadsapi-process_information)
-   [**Informationen zum Prozess \_ Speicher \_ Erschöpfung \_**](/windows/win32/api/processthreadsapi/ns-processthreadsapi-process_memory_exhaustion_info)
-   [**\_ \_ ASLR- \_ Richtlinie zur Prozess Minderung**](/windows/desktop/api/WinNT/ns-winnt-process_mitigation_aslr_policy)
-   [**\_ \_ binäre \_ Signatur \_ Richtlinie für die Prozess Minderung**](/windows/desktop/api/WinNT/ns-winnt-process_mitigation_binary_signature_policy)
-   [**\_ \_ \_ \_ \_ Richtlinie zum Schutz der Ablauf Steuerung für Prozesse**](/windows/desktop/api/WinNT/ns-winnt-process_mitigation_control_flow_guard_policy)
-   [**\_DEP- \_ \_ Richtlinie zur Prozess Minderung**](/windows/desktop/api/WinNT/ns-winnt-process_mitigation_dep_policy)
-   [**\_ \_ dynamische \_ Code \_ Richtlinie für die Prozess Minderung**](/windows/desktop/api/WinNT/ns-winnt-process_mitigation_dynamic_code_policy)
-   [**\_ \_ \_ \_ Richtlinie zum Deaktivieren des Erweiterungs Punkts zum Prozess \_**](/windows/desktop/api/winnt/ns-winnt-process_mitigation_extension_point_disable_policy)
-   [**\_ \_ \_ Richtlinie zum Deaktivieren der Schriftart \_ zur Verarbeitung**](/windows/desktop/api/WinNT/ns-winnt-process_mitigation_font_disable_policy)
-   [**\_Abbild \_ \_ Lade \_ Richtlinie für Prozess Minderung**](/windows/desktop/api/WinNT/ns-winnt-process_mitigation_image_load_policy)
-   [**Richtlinie zur Vermeidung von \_ \_ strengen \_ Handles \_ \_ der Prozess Minderung**](/windows/desktop/api/WinNT/ns-winnt-process_mitigation_strict_handle_check_policy)
-   [**\_ \_ \_ \_ Richtlinie zum Deaktivieren des System aufrubungs Systems \_**](/windows/desktop/api/WinNT/ns-winnt-process_mitigation_system_call_disable_policy)
-   [**\_Benutzer \_ Prozess \_ Parameter von RTL**](/windows/desktop/api/Winternl/ns-winternl-rtl_user_process_parameters)
-   [**STARTUPINFO**](/windows/win32/api/processthreadsapi/ns-processthreadsapi-startupinfoa)
-   [**Startupinfoex**](/windows/desktop/api/WinBase/ns-winbase-startupinfoexa)
-   [**TEB**](/windows/desktop/api/Winternl/ns-winternl-teb)

## <a name="processor-structures"></a>Prozessor Strukturen

Die folgenden Strukturen werden mit Prozessoren und Prozessor Gruppen verwendet:

-   [**Cache \_ Beziehung**](/windows/desktop/api/WinNT/ns-winnt-cache_relationship)
-   [**Gruppen \_ Affinität**](/windows/desktop/api/WinNT/ns-winnt-group_affinity)
-   [**Gruppen \_ Beziehung**](/windows/desktop/api/WinNT/ns-winnt-group_relationship)
-   [**NUMA- \_ Knoten \_ Beziehung**](/windows/desktop/api/WinNT/ns-winnt-numa_node_relationship)
-   [**Informationen zur Prozessor \_ Gruppe \_**](/windows/desktop/api/WinNT/ns-winnt-processor_group_info)
-   [**Prozessor \_ Nummer**](/windows/desktop/api/WinNT/ns-winnt-processor_number)
-   [**Prozessor \_ Beziehung**](/windows/desktop/api/WinNT/ne-winnt-logical_processor_relationship)
-   [**Informationen zum System- \_ CPU- \_ Satz \_**](/windows/desktop/api/winnt/ns-winnt-system_cpu_set_information)
-   [**\_Informationen zum logischen System \_ Prozessor \_**](/windows/desktop/api/WinNT/ns-winnt-system_logical_processor_information)
-   [**\_Informationen zum logischen System Prozessor ( \_ \_ \_ Ex)**](/windows/desktop/api/WinNT/ns-winnt-system_logical_processor_information_ex)

## <a name="dispatcher-queue-structure"></a>Struktur der Dispatcher-Warteschlange

Die folgende Struktur wird verwendet, um einen [dispatcherqueuecontroller](/uwp/api/windows.system.dispatcherqueuecontroller)zu erstellen.

-   [**Dispatcherqueueoptions**](/windows/desktop/api/DispatcherQueue/ns-dispatcherqueue-dispatcherqueueoptions)

## <a name="job-object-structures"></a>Auftrags Objektstrukturen

Die folgenden Strukturen werden mit Auftrags Objekten verwendet:

-   [**JobObject \_ - \_ Abschluss \_ Anschluss zuordnen**](/windows/desktop/api/WinNT/ns-winnt-jobobject_associate_completion_port)
-   [**\_grundlegende Informationen zur \_ Buchhaltung von JobObject \_**](/windows/desktop/api/WinNT/ns-winnt-jobobject_basic_accounting_information)
-   [**\_grundlegende Informationen und e/a \_ - \_ \_ Buchhaltungs \_ Informationen**](/windows/desktop/api/WinNT/ns-winnt-jobobject_basic_and_io_accounting_information)
-   [**\_Informationen zu grundlegenden \_ \_ Informationen zu JobObject**](/windows/desktop/api/WinNT/ns-winnt-jobobject_basic_limit_information)
-   [**\_Liste der grundlegenden \_ Prozess- \_ IDs \_ in JobObject**](/windows/desktop/api/WinNT/ns-winnt-jobobject_basic_process_id_list)
-   [**\_grundlegende Einschränkungen der \_ Benutzeroberfläche von JobObject \_**](/windows/desktop/api/WinNT/ns-winnt-jobobject_basic_ui_restrictions)
-   [**JobObject- \_ Ende \_ der \_ Auftrags \_ Zeit \_ Informationen**](/windows/desktop/api/WinNT/ns-winnt-jobobject_end_of_job_time_information)
-   [**\_Informationen zu erweiterten \_ \_ Informationen zu JobObject**](/windows/desktop/api/WinNT/ns-winnt-jobobject_extended_limit_information)
-   [**\_Informationen zum Sicherheits \_ Limit \_ für JobObject**](/windows/desktop/api/WinNT/ns-winnt-jobobject_security_limit_information)

## <a name="user-mode-scheduling-structures"></a>Planen von User-Mode Planung

Die folgenden Strukturen werden mit ums verwendet:

-   [**UMS \_ Create \_ Thread- \_ Attribute**](/windows/desktop/api/WinNT/ns-winnt-ums_create_thread_attributes)
-   [**UMS- \_ Scheduler- \_ Start \_ Informationen**](/windows/desktop/api/WinBase/ns-winbase-ums_scheduler_startup_info)
-   [**UMS- \_ System \_ Thread \_ Informationen**](/windows/desktop/api/WinBase/ns-winbase-ums_system_thread_information)

 

 
