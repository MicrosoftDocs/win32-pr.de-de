---
title: Systemanbieter
description: Aktivieren Sie die Ereignisse des Systemablaufverfolgungsanbieters mit EnableTraceEx2.
ms.topic: article
ms.date: 06/02/2021
ms.openlocfilehash: 48a93ab94b87a43e0eb8a292320536a04ef43477
ms.sourcegitcommit: cb87082135319cbdc5df541e3071eebb83a58972
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/04/2021
ms.locfileid: "111387799"
---
# <a name="system-providers"></a>Systemanbieter
 
Ab Windows 10 SDK-Build 20348 können die Ereignisse des Systemablaufverfolgungsanbieters auf die gleiche Weise aktiviert werden wie andere ETW-Anbieter mit [EnableTraceEx2.](/windows/win32/api/evntrace/nf-evntrace-enabletraceex2)  Die verschiedenen Flags und [Gruppenmasken,](/windows/win32/api/evntrace/ns-evntrace-event_trace_properties) die dem Systemablaufverfolgungsanbieter zugeordnet sind, wurden neuen Ablaufverfolgungsanbietern zugeordnet, die als Systemanbieter bezeichnet werden, und übereinstimmenden Schlüsselwörtern.  
 
Wie beim direkten Aktivieren des Systemablaufverfolgungsanbieters können die Systemanbieter nur durch eine Sitzung aktiviert werden, für die [der EVENT_TRACE_SYSTEM_LOGGER_MODE](/windows/win32/etw/logging-mode-constants) festgelegt ist.

## <a name="system-provider-reference"></a>Systemanbieterreferenz

* [System-ALPC-Anbieter](#system-alpc-provider)
* [Systemkonfigurationsanbieter](#system-config-provider)
* [System-CPU-Anbieter](#system-cpu-provider)
* [System Hypervisor Provider](#system-hypervisor-provider)
* [Systemunterbrechungsanbieter](#system-interrupt-provider)
* [System-E/A-Anbieter](#system-io-provider)
* [System-E/A-Filteranbieter](#system-io-filter-provider)
* [Systemsperranbieter](#system-lock-provider)
* [Systemspeicheranbieter](#system-memory-provider)
* [Systemobjektanbieter](#system-object-provider)
* [System Power Provider](#system-power-provider)
* [Systemprozessanbieter](#system-process-provider)
* [Systemprofilanbieter](#system-profile-provider)
* [Systemregistrierungsanbieter](#system-registry-provider)
* [Systemplaneranbieter](#system-scheduler-provider)
* [System Syscall Provider](#system-syscall-provider)
* [System Timer Provider](#system-timer-provider)
 
### <a name="system-alpc-provider"></a>System-ALPC-Anbieter

Stellt Ereignisse im Zusammenhang mit dem ALPC-System bereit.

GUID: SystemAlpcProviderGuid {fcb9baaf-e529-4980-92e9-ced1a6aadfdf}

| Schlüsselwort | Entsprechende Legacyflags und -gruppen |
| ------- | ------------------------------------- |
| SYSTEM_ALPC_KW_GENERAL | PERF_ALPC, EVENT_TRACE_FLAG_ALPC |
 
### <a name="system-config-provider"></a>Systemkonfigurationsanbieter 

Stellt Systemkonfigurationsereignisse bereit.

GUID: SystemConfigProviderGuid {fef3a8b6-318d-4b67-a96a-3b0f6b8f18fe}

| Schlüsselwort | Entsprechende Legacyflags und -gruppen |
| ------- | ------------------------------------- |
| SYSTEM_CONFIG_KW_SYSTEM | PERF_SYSCFG_SYSTEM |
| SYSTEM_CONFIG_KW_GRAPHICS | PERF_SYSCFG_GRAPHICS |
| SYSTEM_CONFIG_KW_STORAGE | PERF_SYSCFG_STORAGE |
| SYSTEM_CONFIG_KW_NETWORK | PERF_SYSCFG_NETWORK |
| SYSTEM_CONFIG_KW_SERVICES | PERF_SYSCFG_SERVICES |
| SYSTEM_CONFIG_KW_PNP | PERF_SYSCFG_PNP |
| SYSTEM_CONFIG_KW_OPTICAL | PERF_SYSCFG_OPTICAL |
 
### <a name="system-cpu-provider"></a>System-CPU-Anbieter 

Stellt Ereignisse bereit, die sich auf die CPU beziehen.

GUID: SystemCpuProviderGuid {c6c5265f-eae8-4650-aae4-9d48603d8510}

| Schlüsselwort | Entsprechende Legacyflags und -gruppen |
| ------- | ------------------------------------- |
| SYSTEM_CPU_KW_CONFIG | PERF_CPU_CONFIG |
| SYSTEM_CPU_KW_CACHE_FLUSH | PERF_CACHE_FLUSH |
| SYSTEM_CPU_KW_SPEC_CONTROL | PERF_SPEC_CONTROL |
 
### <a name="system-hypervisor-provider"></a>System Hypervisor Provider 

Stellt Ereignisse bereit, die sich auf den Hypervisor beziehen.

GUID: SystemHypervisorProviderGuid {bafa072a-918a-4bed-b622-bc152097098f}

| Schlüsselwort | Entsprechende Legacyflags und -gruppen |
| ------- | ------------------------------------- |
| SYSTEM_HYPERVISOR_KW_PROFILE | PERF_HV_PROFILE |
| SYSTEM_HYPERVISOR_KW_CALLOUTS | PERF_HV_CALLOUTS |
| SYSTEM_HYPERVISOR_KW_VTL_CHANGE | PERF_VTL_CHANGE |
 
### <a name="system-interrupt-provider"></a>Systemunterbrechungsanbieter 

Stellt Ereignisse im Zusammenhang mit DPCs und Interrupts bereit.

GUID: SystemInterruptProviderGuid {d4bbee17-b545-4888-858b-744169015b25}

| Schlüsselwort | Entsprechende Legacyflags und -gruppen |
| ------- | ------------------------------------- |
| SYSTEM_INTERRUPT_KW_GENERAL | PERF_INTERRUPT, EVENT_TRACE_FLAG_INTERRUPT |
| SYSTEM_INTERRUPT_KW_CLOCK_INTERRUPT | PERF_CLOCK_INTERRUPT |
| SYSTEM_INTERRUPT_KW_DPC | PERF_DPC, EVENT_TRACE_FLAG_DPC |
| SYSTEM_INTERRUPT_KW_DPC_QUEUE | PERF_DPC_QUEUE |
| SYSTEM_INTERRUPT_KW_WDF_DPC | PERF_WDF_DPC |
| SYSTEM_INTERRUPT_KW_WDF_INTERRUPT | PERF_WDF_INTERRUPT |
| SYSTEM_INTERRUPT_KW_IPI | PERF_IPI |
 
 
### <a name="system-io-provider"></a>System-E/A-Anbieter 

Stellt Ereignisse im Zusammenhang mit mehreren Arten von E/A bereit, einschließlich Datenträger, Cache und Netzwerk.

GUID: SystemIoProviderGuid {3d5c43e3-0f1c-4202-b817-174c0070dc79}

| Schlüsselwort | Entsprechende Legacyflags und -gruppen |
| ------- | ------------------------------------- |
| SYSTEM_IO_KW_DISK | EVENT_TRACE_FLAG_DISK_IO |
| SYSTEM_IO_KW_DISK_INIT | PERF_DISK_IO_INIT, EVENT_TRACE_FLAG_DISK_IO_INIT |
| SYSTEM_IO_KW_FILENAME | PERF_FILENAME, EVENT_TRACE_FLAG_DISK_FILE_IO |
| SYSTEM_IO_KW_SPLIT | PERF_SPLIT_IO, EVENT_TRACE_FLAG_SPLIT_IO |
| SYSTEM_IO_KW_FILE | PERF_FILE_IO, EVENT_TRACE_FLAG_FILE_IO |
| SYSTEM_IO_KW_OPTICAL | PERF_OPTICAL_IO, EVENT_TRACE_FLAG_FILE_IO_INIT |
| SYSTEM_IO_KW_OPTICAL_INIT | PERF_OPTICAL_IO_INIT |
| SYSTEM_IO_KW_DRIVERS | PERF_DRIVERS, EVENT_TRACE_FLAG_DRIVER |
| SYSTEM_IO_KW_CC | PERF_CC |
| SYSTEM_IO_KW_NETWORK | PERF_NETWORK, EVENT_TRACE_FLAG_NETWORK_TCPIP |

Hinweis: Wenn Sie das Schlüsselwort SYSTEM_IO_KW_DRIVERS aktivieren, werden auch SYSTEM_IO_KW_FILENAME automatisch aktiviert.  Die SYSTEM_IO_KW_FILENAME wird auch automatisch aktiviert, wenn der Systemspeicheranbieter mit dem Schlüsselwort SYSTEM_MEMORY_KW_MEMORY aktiviert ist.
 
### <a name="system-io-filter-provider"></a>System-E/A-Filteranbieter 

Stellt Ereignisse im Zusammenhang mit der E/A-Filterung bereit, einschließlich Zeitsteuerung und Fehlern.

GUID: SystemIoFilterProviderGuid {fbd09363-9e22-4661-b8bf-e7a34b535b8c}

| Schlüsselwort | Entsprechende Legacyflags und -gruppen |
| ------- | ------------------------------------- |
| SYSTEM_IOFILTER_KW_GENERAL | PERF_FLT_IO |
| SYSTEM_IOFILTER_KW_INIT | PERF_FLT_IO_INIT |
| SYSTEM_IOFILTER_KW_FASTIO | PERF_FLT_FASTIO |
| SYSTEM_IOFILTER_KW_FAILURE | PERF_FLT_IO_FAILURE |
 
### <a name="system-lock-provider"></a>Systemsperranbieter 

Stellt Ereignisse im Zusammenhang mit Kernelsperrmechanismen bereit.

GUID: SystemLockProviderGuid {721ddfd3-dacc-4e1e-b26a-a2cb31d4705a}

| Schlüsselwort | Entsprechende Legacyflags und -gruppen |
| ------- | ------------------------------------- |
| SYSTEM_LOCK_KW_SPINLOCK | PERF_SPINLOCK |
| SYSTEM_LOCK_KW_SPINLOCK_COUNTERS | PERF_SPINLOCK_CNTRS |
| SYSTEM_LOCK_KW_SYNC_OBJECTS | PERF_SYNC_OBJECTS |
 
### <a name="system-memory-provider"></a>Systemspeicheranbieter 

Stellt Ereignisse bereit, die sich auf den Speicher-Manager beziehen.

GUID: SystemMemoryProviderGuid {82958ca9-b6cd-47f8-a3a8-03ae85a4bc24}

| Schlüsselwort | Entsprechende Legacyflags und -gruppen |
| ------- | ------------------------------------- |
| SYSTEM_MEMORY_KW_GENERAL | PERF_MEMORY |
| SYSTEM_MEMORY_KW_HARD_FAULTS | PERF_HARD_FAULTS, EVENT_TRACE_FLAG_MEMORY_HARD_FAULTS |
| SYSTEM_MEMORY_KW_ALL_FAULTS | PERF_ALL_FAULTS, EVENT_TRACE_FLAG_MEMORY_PAGE_FAULTS |
| SYSTEM_MEMORY_KW_POOL | PERF_POOL |
| SYSTEM_MEMORY_KW_MEMINFO | PERF_MEMINFO |
| SYSTEM_MEMORY_KW_PFSECTION | PERF_PFSECTION |
| SYSTEM_MEMORY_KW_MEMINFO_WS | PERF_MEMINFO_WS |
| SYSTEM_MEMORY_KW_HEAP | PERF_HEAP |
| SYSTEM_MEMORY_KW_WS | PERF_WS |
| SYSTEM_MEMORY_KW_CONTMEM_GEN | PERF_CONTMEM_GEN |
| SYSTEM_MEMORY_KW_VIRTUAL_ALLOC | PERF_VIRTUAL_ALLOC, EVENT_TRACE_FLAG_VIRTUAL_ALLOC |
| SYSTEM_MEMORY_KW_FOOTPRINT | PERF_FOOTPRINT |
| SYSTEM_MEMORY_KW_SESSION | PERF_SESSION |
| SYSTEM_MEMORY_KW_REFSET | PERF_REFSET |
| SYSTEM_MEMORY_KW_VAMAP | PERF_VAMAP, EVENT_TRACE_FLAG_VAMAP |

Hinweise: 
* Wenn Sie das Schlüsselwort SYSTEM_MEMORY_KW_MEMORY aktivieren, wird SYSTEM_IO_KW_FILENAME automatisch auch auf dem System-E/A-Anbieter aktiviert.
* Die vom SYSTEM_MEMORY_KW_POOL aktivierten Ereignisse unterstützen einen Pooltagfilter, um Ereignisse selektiv nur für bestimmte Pooltags zu schreiben.  Dies wird als [schematisierter Filter](/windows/win32/api/evntprov/ns-evntprov-event_filter_descriptor) für den Systemspeicheranbieter konfiguriert.  Der PoolTag-Filter wird wie folgt erstellt:

    ```cpp
    {
    EVENT_FILTER_HEADER Header; 
    ULONG PoolTags[ETW_MAX_POOLTAG_FILTER];
    }
    ```

* Die [EVENT_FILTER_HEADER](/windows/win32/api/evntprov/ns-evntprov-event_filter_header) sollte initialisiert werden, wobei id auf SYSTEM_MEMORY_POOL_FILTER_ID und das Größenfeld auf die Größe von Header plus den verwendeten Teil des PoolTags-Arrays festgelegt ist.  

* Jedes Pooltag ist eine 4-stellige Zeichenfolge, die als ULONG im Filter gespeichert wird.  
 
 
### <a name="system-object-provider"></a>Systemobjektanbieter 

Stellt Ereignisse bereit, die sich auf den Objekt-Manager beziehen.

GUID: SystemObjectProviderGuid {febd7460-3d1d-47eb-af49-c9eeb1e146f2}

| Schlüsselwort | Entsprechende Legacyflags und -gruppen |
| ------- | ------------------------------------- |
| SYSTEM_OBJECT_KW_HANDLE | PERF_OB_HANDLE |
| SYSTEM_OBJECT_KW_OBJECT | PERF_OB_OBJECT |
 
### <a name="system-power-provider"></a>System Power Provider 

Stellt Ereignisse bereit, die sich auf den Energiezustand des Systems beziehen.

GUID: SystemPowerProviderGuid {c134884a-32d5-4488-80e5-14ed7abb8269}

| Schlüsselwort | Entsprechende Legacyflags und -gruppen |
| ------- | ------------------------------------- |
| SYSTEM_POWER_KW_GENERAL | PERF_POWER |
| SYSTEM_POWER_KW_HIBER_RUNDOWN | PERF_HIBER_RUNDOWN |
| SYSTEM_POWER_KW_PROCESSOR_IDLE | PERF_PROCESSOR_IDLE |
| SYSTEM_POWER_KW_IDLE_SELECTION | PERF_IDLE_SELECTION |
| SYSTEM_POWER_KW_PPM_EXIT_LATENCY | PERF_PPM_EXIT_LATENCY |
 
### <a name="system-process-provider"></a>Systemprozessanbieter 

Stellt Ereignisse im Zusammenhang mit dem Prozess einschließlich Lebensdauerinformationen, Bildladeereignissen und threadbezogenen Ereignissen zur Verfügung.

GUID: SystemProcessProviderGuid {151f55dc-467d-471f-83b5-5f889d46ff66}

| Schlüsselwort | Entsprechende Legacyflags und -gruppen |
| ------- | ------------------------------------- |
| SYSTEM_PROCESS_KW_GENERAL | PERF_PROCESS, EVENT_TRACE_FLAG_PROCESS |
| SYSTEM_PROCESS_KW_INSWAP | PERF_PROCESS_INSWAP |
| SYSTEM_PROCESS_KW_FREEZE | PERF_PROCESS_FREEZE |
| SYSTEM_PROCESS_KW_PERF_COUNTER | PERF_PERF_COUNTER, EVENT_TRACE_FLAG_PROCESS_COUNTERS |
| SYSTEM_PROCESS_KW_WAKE_COUNTER | PERF_WAKE_COUNTER |
| SYSTEM_PROCESS_KW_WAKE_DROP | PERF_WAKE_DROP |
| SYSTEM_PROCESS_KW_WAKE_EVENT | PERF_WAKE_EVENT |
| SYSTEM_PROCESS_KW_DEBUG_EVENTS | PERF_DEBUG_EVENTS, EVENT_TRACE_FLAG_DEBUG_EVENTS |
| SYSTEM_PROCESS_KW_DBGPRINT | PERF_DBGPRINT, EVENT_TRACE_FLAG_DBGPRINT |
| SYSTEM_PROCESS_KW_JOB | PERF_JOB, EVENT_TRACE_FLAG_JOB |
| SYSTEM_PROCESS_KW_WORKER_THREAD | PERF_WORKER_THREAD |
| SYSTEM_PROCESS_KW_THREAD | PERF_THREAD, EVENT_TRACE_FLAG_THREAD |
| SYSTEM_PROCESS_KW_LOADER | PERF_LOADER, EVENT_TRACE_FLAG_IMAGE_LOAD |
 
### <a name="system-profile-provider"></a>Systemprofilanbieter 

Stellt Profilerstellungsereignisse zur Verfügung.

GUID: SystemProfileProviderGuid {bfeb0324-1cee-496f-a409-2ac2b48a6322}

| Schlüsselwort | Entsprechende Legacyflags und -gruppen |
| ------- | ------------------------------------- |
| SYSTEM_PROFILE_KW_GENERAL | PERF_PROFILE, EVENT_TRACE_FLAG_PROFILE |
| SYSTEM_PROFILE_KW_PMC_PROFILE | PERF_PMC_PROFILE |
 
### <a name="system-registry-provider"></a>Systemregistrierungsanbieter 

Stellt Ereignisse im Zusammenhang mit der Registrierung zur Verfügung.

GUID: SystemRegistryProviderGuid {16156bd9-fab4-4cfa-a232-89d1099058e3}

| Schlüsselwort | Entsprechende Legacyflags und -gruppen |
| ------- | ------------------------------------- |
| SYSTEM_REGISTRY_KW_GENERAL | PERF_REGISTRY, EVENT_TRACE_FLAG_REGISTRY |
| SYSTEM_REGISTRY_KW_HIVE | PERF_REG_HIVE |
| SYSTEM_REGISTRY_KW_NOTIFICATION | PERF_REG_NOTIF |
 
### <a name="system-scheduler-provider"></a>Systemplaneranbieter 

Stellt Ereignisse im Zusammenhang mit dem Planer zur Verfügung.

GUID: SystemSchedulerProviderGuid {599a2a76-4d91-4910-9ac7-7d33f2e97a6c}

| Schlüsselwort | Entsprechende Legacyflags und -gruppen |
| ------- | ------------------------------------- |
| SYSTEM_SCHEDULER_KW_XSCHEDULER | PERF_XSCHEDULER |
| SYSTEM_SCHEDULER_KW_DISPATCHER | PERF_DISPATCHER, EVENT_TRACE_FLAG_DISPATCHER |
| SYSTEM_SCHEDULER_KW_KERNEL_QUEUE | PERF_KERNEL_QUEUE |
| SYSTEM_SCHEDULER_KW_SHOULD_YIELD | PERF_SHOULD_YIELD |
| SYSTEM_SCHEDULER_KW_ANTI_STARVATION | PERF_ANTI_STARVATION |
| SYSTEM_SCHEDULER_KW_LOAD_BALANCER | PERF_LOAD_BALANCER |
| SYSTEM_SCHEDULER_KW_AFFINITY | PERF_AFFINITY |
| SYSTEM_SCHEDULER_KW_PRIORITY | PERF_PRIORITY |
| SYSTEM_SCHEDULER_KW_IDEAL_PROCESSOR | PERF_IDEAL_PROCESSOR |
| SYSTEM_SCHEDULER_KW_CONTEXT_SWITCH | PERF_CONTEXT_SWITCH, EVENT_TRACE_FLAG_CSWITCH |
 
### <a name="system-syscall-provider"></a>System Syscall Provider 

Stellt Ereignisse mit Informationen zu Systemaufrufen zur Verfügung.

GUID: SystemSyscallProviderGuid {434286f7-6f1b-45bb-b37e-95f623046c7c}

| Schlüsselwort | Entsprechende Legacyflags und -gruppen |
| ------- | ------------------------------------- |
| SYSTEM_SYSCALL_KW_GENERAL | PERF_SYSCALL, EVENT_TRACE_FLAG_SYSTEMCALL |
 
### <a name="system-timer-provider"></a>Systemzeitgeberanbieter 

Stellt Ereignisse im Zusammenhang mit Timern im Kernel zur Verfügung.

GUID: SystemTimerProviderGuid {4f061568-e215-499f-ab2e-eda0ae890a5b}

| Schlüsselwort | Entsprechende Legacyflags und -gruppen |
| ------- | ------------------------------------- |
| SYSTEM_TIMER_KW_GENERAL | PERF_TIMER |
| SYSTEM_TIMER_KW_CLOCK_TIMER | PERF_CLOCK_TIMER |
 
## <a name="remarks"></a>Hinweise

Dieser neue Aktivierungsmechanismus ist zusätzlich zu den bereits vorhandenen Methoden zum Aktivieren dieser Ereignisse vorhanden.  Jeglicher Code, der zuvor funktioniert hat, wird weiterhin verwendet.
 
Die vom Systemablaufverfolgungsanbieter generierten Ereignisse ändern sich aufgrund dieser neuen Funktion nicht.  Dies bedeutet, dass die ausgegebenen Ereignisse nicht als von den einzelnen Systemanbietern ausgegeben markiert sind.
 
Weitere Informationen zur Anbieter-GUID und Schlüsselwortdefinitionen finden Sie unter [evntrace.h](/windows/win32/api/evntrace/).

## <a name="see-also"></a>Weitere Informationen

[Konfigurieren und Starten einer SystemTraceProvider-Sitzung](configuring-and-starting-a-systemtraceprovider-session.md)

[evntrace.h-Header](/windows/win32/api/evntrace/)