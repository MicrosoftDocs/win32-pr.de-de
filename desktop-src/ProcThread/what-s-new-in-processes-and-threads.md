---
description: Windows 7 und Windows Server 2008 R2 enthalten die folgenden neuen Programmierelemente für Prozesse und Threads.
ms.assetid: 69cd8713-b40c-4fec-a256-9c2ee3d73da5
title: Neues in Prozessen und Threads
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: efe8b53349f5c6f19dd9beda1ffe6b933fbff63533988a40937453194df57295
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "117792958"
---
# <a name="whats-new-in-processes-and-threads"></a>Neues in Prozessen und Threads

Windows 7 und Windows Server 2008 R2 enthalten die folgenden neuen Programmierelemente für Prozesse und Threads.

## <a name="new-capabilities"></a>Neue Funktionen

Die 64-Bit-Versionen von Windows 7 und Windows Server 2008 R2 unterstützen mehr als 64 logische Prozessoren auf einem einzelnen Computer. Weitere Informationen finden Sie unter [Prozessorgruppen.](processor-groups.md)

Die Benutzermodusplanung (UMS) ist ein schlanker Mechanismus, mit dem Anwendungen ihre eigenen Threads planen können. Weitere Informationen finden Sie unter [Planen des Benutzermodus.](user-mode-scheduling.md)

## <a name="new-functions"></a>Neue Funktionen

Die folgenden neuen Funktionen werden mit Prozessoren und Prozessorgruppen verwendet.



| Funktion                                                                                | Beschreibung                                                                                                                                                          |
|-----------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**CreateRemoteThreadEx**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-createremotethreadex)<br/>                         | Erstellt einen Thread, der im virtuellen Adressraum eines anderen Prozesses ausgeführt wird und optional erweiterte Attribute wie Prozessorgruppenaffinität angibt.<br/> |
| [**GetActiveProcessorCount**](/windows/desktop/api/WinBase/nf-winbase-getactiveprocessorcount)<br/>                   | Gibt die Anzahl der aktiven Prozessoren in einer Prozessorgruppe oder im System zurück.<br/>                                                                            |
| [**GetActiveProcessorGroupCount**](/windows/desktop/api/WinBase/nf-winbase-getactiveprocessorgroupcount)<br/>         | Gibt die Anzahl der aktiven Prozessorgruppen im System zurück.<br/>                                                                                              |
| [**GetCurrentProcessorNumberEx**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-getcurrentprocessornumberex)<br/>           | Ruft die Prozessorgruppe und die Nummer des logischen Prozessors ab, in dem der aufrufende Thread ausgeführt wird.<br/>                                                 |
| [**GetLogicalProcessorInformationEx**](/windows/win32/api/sysinfoapi/nf-sysinfoapi-getlogicalprocessorinformationex)<br/> | Ruft Informationen über die Beziehungen von logischen Prozessoren und zugehöriger Hardware ab.<br/>                                                                 |
| [**GetMaximumProcessorCount**](/windows/desktop/api/WinBase/nf-winbase-getmaximumprocessorcount)<br/>                 | Gibt die maximale Anzahl logischer Prozessoren zurück, über die eine Prozessorgruppe oder das System verfügen kann.<br/>                                                           |
| [**GetMaximumProcessorGroupCount**](/windows/desktop/api/WinBase/nf-winbase-getmaximumprocessorgroupcount)<br/>       | Gibt die maximale Anzahl von Prozessorgruppen zurück, über die das System verfügen kann. <br/>                                                                                 |
| [**GetNumaAvailableMemoryNodeEx**](/windows/desktop/api/WinBase/nf-winbase-getnumaavailablememorynodeex)<br/>         | Ruft die Arbeitsspeichermenge ab, die im angegebenen Knoten als USHORT-Wert verfügbar ist.<br/>                                                                 |
| [**GetNumaNodeNumberFromHandle**](/windows/desktop/api/WinBase/nf-winbase-getnumanodenumberfromhandle)<br/>           | Ruft den NUMA-Knoten ab, der dem zugrunde liegenden Gerät für ein Dateihand handle zugeordnet ist.<br/>                                                                          |
| [**GetNumaNodeProcessorMaskEx**](/windows/win32/api/systemtopologyapi/nf-systemtopologyapi-getnumanodeprocessormaskex)<br/>             | Ruft die Prozessormaske für den angegebenen NUMA-Knoten als USHORT-Wert ab.<br/>                                                                               |
| [**GetNumaProcessorNodeEx**](/windows/desktop/api/WinBase/nf-winbase-getnumaprocessornodeex)<br/>                     | Ruft die Knotennummer des angegebenen logischen Prozessors als USHORT-Wert ab.<br/>                                                                           |
| [**GetNumaProximityNodeEx**](/windows/win32/api/systemtopologyapi/nf-systemtopologyapi-getnumaproximitynodeex)<br/>                     | Ruft die Knotennummer als USHORT-Wert für den angegebenen Näherungsbezeichner ab.<br/>                                                                       |
| [**GetProcessGroupAffinity**](/windows/win32/api/processtopologyapi/nf-processtopologyapi-getprocessgroupaffinity)<br/>                   | Ruft die Prozessorgruppenaffinität des angegebenen Prozesses ab.<br/>                                                                                          |
| [**GetProcessorSystemCycleTime**](/windows/win32/api/sysinfoapi/nf-sysinfoapi-getprocessorsystemcycletime)<br/>           | Ruft die Zykluszeit ab, die jeder Prozessor in der angegebenen Gruppe für die Ausführung von verzögerten Prozeduraufrufen (DEFERRED Procedure Calls, DPCs) und Interruptdienstroutinen (ISRs) verwendet hat.<br/>     |
| [**GetThreadGroupAffinity**](/windows/win32/api/processtopologyapi/nf-processtopologyapi-getthreadgroupaffinity)<br/>                     | Ruft die Prozessorgruppenaffinität des angegebenen Threads ab.<br/>                                                                                           |
| [**GetThreadIdealProcessorEx**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-getthreadidealprocessorex)<br/>               | Ruft die Prozessornummer des idealen Prozessors für den angegebenen Thread ab.<br/>                                                                           |
| [**QueryIdleProcessorCycleTimeEx**](/windows/win32/api/realtimeapiset/nf-realtimeapiset-queryidleprocessorcycletimeex)<br/>       | Ruft die akkumulierte Zykluszeit für den Leerlaufthread auf jedem logischen Prozessor in der angegebenen Prozessorgruppe ab. <br/>                                     |
| [**SetThreadGroupAffinity**](/windows/win32/api/processtopologyapi/nf-processtopologyapi-setthreadgroupaffinity)<br/>                     | Legt die Prozessorgruppenaffinität für den angegebenen Thread fest.<br/>                                                                                               |
| [**SetThreadIdealProcessorEx**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-setthreadidealprocessorex)<br/>               | Legt den idealen Prozessor für den angegebenen Thread fest und ruft optional den vorherigen idealen Prozessor ab.<br/>                                                  |



 

Die folgenden neuen Funktionen werden mit Threadpools verwendet.



| Funktion                                                                              | Beschreibung                                                                                                    |
|---------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------|
| [**QueryThreadpoolStackInformation**](/windows/win32/api/threadpoolapiset/nf-threadpoolapiset-querythreadpoolstackinformation)<br/> | Ruft die Stapelreserve- und Commitgrößen für Threads im angegebenen Threadpool ab.<br/>              |
| [**SetThreadpoolCallbackPersistent**](/windows/desktop/api/WinBase/nf-winbase-setthreadpoolcallbackpersistent)<br/> | Gibt an, dass der Rückruf in einem persistenten Thread ausgeführt werden soll.<br/>                                      |
| [**SetThreadpoolCallbackPriority**](/windows/desktop/api/WinBase/nf-winbase-setthreadpoolcallbackpriority)<br/>     | Gibt die Priorität einer Rückruffunktion relativ zu anderen Arbeitselementen im selben Threadpool an.<br/> |
| [**SetThreadpoolStackInformation**](/windows/win32/api/threadpoolapiset/nf-threadpoolapiset-setthreadpoolstackinformation)<br/>     | Legt die Stapelreserve- und Commitgrößen für neue Threads im angegebenen Threadpool fest. <br/>              |



 

Die folgenden neuen Funktionen werden mit UMS verwendet.



| Funktion                                                                          | Beschreibung                                                                                                   |
|-----------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------|
| [**CreateUmsCompletionList**](/windows/desktop/api/WinBase/nf-winbase-createumscompletionlist)<br/>             | Erstellt eine UMS-Vervollständigungsliste.<br/>                                                                     |
| [**CreateUmsThreadContext**](/windows/desktop/api/WinBase/nf-winbase-createumsthreadcontext)<br/>               | Erstellt einen UMS-Threadkontext zur Darstellung eines UMS-Arbeitsthreads.<br/>                                     |
| [**DeleteUmsCompletionList**](/windows/desktop/api/WinBase/nf-winbase-deleteumscompletionlist)<br/>             | Löscht die angegebene UMS-Vervollständigungsliste. Die Liste muss leer sein.<br/>                                 |
| [**DeleteUmsThreadContext**](/windows/desktop/api/WinBase/nf-winbase-deleteumsthreadcontext)<br/>               | Löscht den angegebenen UMS-Threadkontext. Der Thread muss beendet werden.<br/>                           |
| [**DequeueUmsCompletionListItems**](/windows/desktop/api/WinBase/nf-winbase-dequeueumscompletionlistitems)<br/> | Ruft UMS-Arbeitsthreads aus der angegebenen UMS-Vervollständigungsliste ab.<br/>                               |
| [**EnterUmsSchedulingMode**](/windows/desktop/api/WinBase/nf-winbase-enterumsschedulingmode)<br/>               | Konvertiert den aufrufenden Thread in einen UMS-Planerthread.<br/>                                           |
| [**ExecuteUmsThread**](/windows/desktop/api/WinBase/nf-winbase-executeumsthread)<br/>                           | Führt den angegebenen UMS-Arbeitsthread aus.<br/>                                                              |
| [**GetCurrentUmsThread**](/windows/desktop/api/WinBase/nf-winbase-getcurrentumsthread)<br/>                     | Gibt den UMS-Threadkontext des aufrufenden UMS-Threads zurück.<br/>                                          |
| [**GetNextUmsListItem**](/windows/desktop/api/WinBase/nf-winbase-getnextumslistitem)<br/>                       | Gibt den nächsten UMS-Threadkontext in einer Liste von UMS-Threadkontexten zurück.<br/>                              |
| [**GetUmsCompletionListEvent**](/windows/desktop/api/WinBase/nf-winbase-getumscompletionlistevent)<br/>         | Ruft ein Handle für das Ereignis ab, das der angegebenen UMS-Vervollständigungsliste zugeordnet ist.<br/>                 |
| [**QueryUmsThreadInformation**](/windows/desktop/api/WinBase/nf-winbase-queryumsthreadinformation)<br/>         | Ruft Informationen zum angegebenen UMS-Arbeitsthread ab.<br/>                                       |
| [**SetUmsThreadInformation**](/windows/desktop/api/WinBase/nf-winbase-setumsthreadinformation)<br/>             | Legt anwendungsspezifische Kontextinformationen für den angegebenen UMS-Arbeitsthread fest.<br/>                 |
| [*UmsSchedulerProc*](/windows/desktop/api/WinNT/nc-winnt-rtl_ums_scheduler_entry_point)<br/>                             | Die anwendungsdefinierte UMS-Planereinstiegspunktfunktion, die einer UMS-Vervollständigungsliste zugeordnet ist. <br/> |
| [**UmsThreadYield**](/windows/desktop/api/WinBase/nf-winbase-umsthreadyield)<br/>                               | Gibt die Steuerung an den UMS-Planerthread zurück, in dem der aufrufende UMS-Arbeitsthread ausgeführt wird.<br/>      |



 

## <a name="new-structures"></a>Neue Strukturen



| Struktur                                                                                                 | Beschreibung                                                                                         |
|-----------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------|
| [**\_CACHEBEZIEHUNG**](/windows/desktop/api/WinNT/ns-winnt-cache_relationship)<br/>                                              | Beschreibt Cacheattribute. <br/>                                                             |
| [**\_GRUPPENAFFINITÄT**](/windows/desktop/api/WinNT/ns-winnt-group_affinity)<br/>                                                      | Enthält eine prozessorgruppenspezifische Affinität, z. B. die Affinität eines Threads.<br/>          |
| [**GROUP \_ RELATIONSHIP**](/windows/desktop/api/WinNT/ns-winnt-group_relationship)<br/>                                              | Enthält Informationen zu Prozessorgruppen. <br/>                                            |
| [**\_NUMA-KNOTENBEZIEHUNG \_**](/windows/desktop/api/WinNT/ns-winnt-numa_node_relationship)<br/>                                     | Enthält Informationen zu einem NUMA-Knoten in einer Prozessorgruppe. <br/>                            |
| [**\_ \_ PROZESSORGRUPPENINFORMATIONEN**](/windows/desktop/api/WinNT/ns-winnt-processor_group_info)<br/>                                         | Enthält die Anzahl und Affinität der Prozessoren in einer Prozessorgruppe.<br/>                     |
| [**\_PROZESSORNUMMER**](/windows/desktop/api/WinNT/ns-winnt-processor_number)<br/>                                                  | Stellt einen logischen Prozessor in einer Prozessorgruppe dar.<br/>                                     |
| [**\_PROZESSORBEZIEHUNG**](/windows/desktop/api/WinNT/ns-winnt-processor_relationship)<br/>                                      | Enthält Informationen zur Affinität innerhalb einer Prozessorgruppe.<br/>                            |
| [**SYSTEM \_ LOGICAL \_ PROCESSOR \_ INFORMATION \_ EX**](/windows/desktop/api/WinNT/ns-winnt-system_logical_processor_information_ex)<br/> | Enthält Informationen über die Beziehungen von logischen Prozessoren und zugehöriger Hardware.<br/> |
| [**UMS \_ CREATE \_ THREAD \_ ATTRIBUTES**](/windows/desktop/api/WinNT/ns-winnt-ums_create_thread_attributes)<br/>                        | Gibt Attribute für einen UMS-Arbeitsthread an. <br/>                                           |
| [**STARTINFORMATIONEN ZUM UMS \_ SCHEDULER \_ \_**](/windows/desktop/api/WinBase/ns-winbase-ums_scheduler_startup_info)<br/>                            | Gibt Attribute für einen UMS-Planerthread an<br/>                                          |



 

 

 
