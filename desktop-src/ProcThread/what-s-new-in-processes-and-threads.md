---
description: Windows 7 und Windows Server 2008 R2 enthalten die folgenden neuen Programmier Elemente für Prozesse und Threads.
ms.assetid: 69cd8713-b40c-4fec-a256-9c2ee3d73da5
title: Neues bei Prozessen und Threads
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ee7dfb708a2890bab1fcd3fd66385f74bd8513b1
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "103865044"
---
# <a name="whats-new-in-processes-and-threads"></a>Neues bei Prozessen und Threads

Windows 7 und Windows Server 2008 R2 enthalten die folgenden neuen Programmier Elemente für Prozesse und Threads.

## <a name="new-capabilities"></a>Neue Funktionen

Die 64-Bit-Versionen von Windows 7 und Windows Server 2008 R2 unterstützen mehr als 64 logische Prozessoren auf einem einzelnen Computer. Weitere Informationen finden Sie unter [Prozessor Gruppen](processor-groups.md).

Die benutzermodusplanung (ums) ist ein schlanker Mechanismus, mit dem Anwendungen ihre eigenen Threads planen können. Weitere Informationen finden Sie unter [User-Mode Scheduling](user-mode-scheduling.md).

## <a name="new-functions"></a>Neue Funktionen

Die folgenden neuen Funktionen werden mit Prozessoren und Prozessor Gruppen verwendet.



| Funktion                                                                                | BESCHREIBUNG                                                                                                                                                          |
|-----------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**"Kreateremotethreadex"**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-createremotethreadex)<br/>                         | Erstellt einen Thread, der im virtuellen Adressraum eines anderen Prozesses ausgeführt wird, und gibt optional Erweiterte Attribute an, wie z. b. Prozessor Gruppen Affinität.<br/> |
| [**Getactiveprocessorcount**](/windows/desktop/api/WinBase/nf-winbase-getactiveprocessorcount)<br/>                   | Gibt die Anzahl aktiver Prozessoren in einer Prozessor Gruppe oder im System zurück.<br/>                                                                            |
| [**Getactiveprocessorgroupcount**](/windows/desktop/api/WinBase/nf-winbase-getactiveprocessorgroupcount)<br/>         | Gibt die Anzahl aktiver Prozessor Gruppen im System zurück.<br/>                                                                                              |
| [**Getcurrentprocessornumex**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-getcurrentprocessornumberex)<br/>           | Ruft die Prozessor Gruppe und die Anzahl der logischen Prozessoren ab, in denen der aufrufenden Thread ausgeführt wird.<br/>                                                 |
| [**Getlogicalprocessorinformationex**](/windows/win32/api/sysinfoapi/nf-sysinfoapi-getlogicalprocessorinformationex)<br/> | Ruft Informationen über die Beziehungen von logischen Prozessoren und zugehöriger Hardware ab.<br/>                                                                 |
| [**Getmaximumprocessorcount**](/windows/desktop/api/WinBase/nf-winbase-getmaximumprocessorcount)<br/>                 | Gibt die maximale Anzahl logischer Prozessoren zurück, die eine Prozessor Gruppe oder das System aufweisen kann.<br/>                                                           |
| [**Getmaximumprocessorgroupcount**](/windows/desktop/api/WinBase/nf-winbase-getmaximumprocessorgroupcount)<br/>       | Gibt die maximale Anzahl von Prozessor Gruppen zurück, die das System aufweisen kann. <br/>                                                                                 |
| [**Getnumaavailablememorynode Ex**](/windows/desktop/api/WinBase/nf-winbase-getnumaavailablememorynodeex)<br/>         | Ruft die Menge des Arbeitsspeichers ab, der im angegebenen Knoten als ushort-Wert verfügbar ist.<br/>                                                                 |
| [**Getnumanodenumschlag**](/windows/desktop/api/WinBase/nf-winbase-getnumanodenumberfromhandle)<br/>           | Ruft den NUMA-Knoten ab, der dem zugrunde liegenden Gerät für ein Datei Handle zugeordnet ist.<br/>                                                                          |
| [**Getnumanodeprocessormaskex**](/windows/win32/api/systemtopologyapi/nf-systemtopologyapi-getnumanodeprocessormaskex)<br/>             | Ruft die Prozessor Maske für den angegebenen NUMA-Knoten als ushort-Wert ab.<br/>                                                                               |
| [**Getnumaprocessornode Ex**](/windows/desktop/api/WinBase/nf-winbase-getnumaprocessornodeex)<br/>                     | Ruft die Knotennummer des angegebenen logischen Prozessors als ushort-Wert ab.<br/>                                                                           |
| [**Getnumaproximitynode Ex**](/windows/win32/api/systemtopologyapi/nf-systemtopologyapi-getnumaproximitynodeex)<br/>                     | Ruft die Knotennummer als ushort-Wert für den angegebenen Näherungs Bezeichner ab.<br/>                                                                       |
| [**Getprocessgroupaffität**](/windows/win32/api/processtopologyapi/nf-processtopologyapi-getprocessgroupaffinity)<br/>                   | Ruft die Prozessor Gruppen Affinität des angegebenen Prozesses ab.<br/>                                                                                          |
| [**Getprocessorsystemcycletime**](/windows/win32/api/sysinfoapi/nf-sysinfoapi-getprocessorsystemcycletime)<br/>           | Ruft die Schleifen Zeit ab, die jeder Prozessor in der angegebenen Gruppe für das Ausführen von verzögerten Prozedur aufrufen (DPCs) und Interrupt-Dienst Routinen (ISRs) aufgewendet hat.<br/>     |
| [**Getthreadgroupaffität**](/windows/win32/api/processtopologyapi/nf-processtopologyapi-getthreadgroupaffinity)<br/>                     | Ruft die Prozessor Gruppen Affinität des angegebenen Threads ab.<br/>                                                                                           |
| [**Getthreadidealprocessorex**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-getthreadidealprocessorex)<br/>               | Ruft die Prozessornummer des idealen Prozessors für den angegebenen Thread ab.<br/>                                                                           |
| [**Queryidleprocessorcycletimeex**](/windows/win32/api/realtimeapiset/nf-realtimeapiset-queryidleprocessorcycletimeex)<br/>       | Ruft die akkumulierte Zeit für den Leerlauf Thread für jeden logischen Prozessor in der angegebenen Prozessor Gruppe ab. <br/>                                     |
| [**Setthreadgroupaffität**](/windows/win32/api/processtopologyapi/nf-processtopologyapi-setthreadgroupaffinity)<br/>                     | Legt die Prozessor Gruppen Affinität für den angegebenen Thread fest.<br/>                                                                                               |
| [**SetThreadIdealProcessorEx**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-setthreadidealprocessorex)<br/>               | Legt den idealen Prozessor für den angegebenen Thread fest und ruft optional den vorherigen idealen Prozessor ab.<br/>                                                  |



 

Die folgenden neuen Funktionen werden mit Thread Pools verwendet.



| Funktion                                                                              | BESCHREIBUNG                                                                                                    |
|---------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------|
| [**Querythreadpoolstackinformation**](/windows/win32/api/threadpoolapiset/nf-threadpoolapiset-querythreadpoolstackinformation)<br/> | Ruft die Stapel Reserve-und-Commit-Größen für Threads im angegebenen Thread Pool ab.<br/>              |
| [**Setthreadpoolcallbackpersistent**](/windows/desktop/api/WinBase/nf-winbase-setthreadpoolcallbackpersistent)<br/> | Gibt an, dass der Rückruf in einem permanenten Thread ausgeführt werden soll.<br/>                                      |
| [**Setthreadpoolcallbackpriority**](/windows/desktop/api/WinBase/nf-winbase-setthreadpoolcallbackpriority)<br/>     | Gibt die Priorität einer Rückruffunktion in Relation zu anderen Arbeits Elementen im gleichen Thread Pool an.<br/> |
| [**Setthreadpoolstackinformation**](/windows/win32/api/threadpoolapiset/nf-threadpoolapiset-setthreadpoolstackinformation)<br/>     | Legt die Stapel Reserve-und-Commit-Größen für neue Threads im angegebenen Thread Pool fest. <br/>              |



 

Die folgenden neuen Funktionen werden mit ums verwendet.



| Funktion                                                                          | BESCHREIBUNG                                                                                                   |
|-----------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------|
| [**"Kreateumscompletionlist"**](/windows/desktop/api/WinBase/nf-winbase-createumscompletionlist)<br/>             | Erstellt eine ums-Vervollständigungsliste.<br/>                                                                     |
| [**"Kreateumsthread Context"**](/windows/desktop/api/WinBase/nf-winbase-createumsthreadcontext)<br/>               | Erstellt einen ums-Thread Kontext zur Darstellung eines ums-Arbeitsthreads.<br/>                                     |
| [**Deleteumscompletionlist**](/windows/desktop/api/WinBase/nf-winbase-deleteumscompletionlist)<br/>             | Löscht die angegebene ums-Vervollständigungsliste. Die Liste muss leer sein.<br/>                                 |
| [**Deleteumsthread Context**](/windows/desktop/api/WinBase/nf-winbase-deleteumsthreadcontext)<br/>               | Löscht den angegebenen ums-Thread Kontext. Der Thread muss beendet werden.<br/>                           |
| [**"Abqueueumscompletionlistitems"**](/windows/desktop/api/WinBase/nf-winbase-dequeueumscompletionlistitems)<br/> | Ruft ums-Arbeitsthreads aus der angegebenen ums-Vervollständigungsliste ab.<br/>                               |
| [**Enterumsschedulingmode**](/windows/desktop/api/WinBase/nf-winbase-enterumsschedulingmode)<br/>               | Konvertiert den aufrufenden Thread in einen ums-Scheduler-Thread.<br/>                                           |
| [**Executeumsthread**](/windows/desktop/api/WinBase/nf-winbase-executeumsthread)<br/>                           | Führt den angegebenen ums-Workerthread aus.<br/>                                                              |
| [**Getcurrentumsthread**](/windows/desktop/api/WinBase/nf-winbase-getcurrentumsthread)<br/>                     | Gibt den ums-Thread Kontext des aufrufenden UMS-Threads zurück.<br/>                                          |
| [**Getnextumslistitem**](/windows/desktop/api/WinBase/nf-winbase-getnextumslistitem)<br/>                       | Gibt den nächsten ums-Thread Kontext in einer Liste von ums-Thread Kontexten zurück.<br/>                              |
| [**Getumscompletionlistevent**](/windows/desktop/api/WinBase/nf-winbase-getumscompletionlistevent)<br/>         | Ruft ein Handle für das-Ereignis ab, das der angegebenen ums-Vervollständigungsliste zugeordnet ist.<br/>                 |
| [**Queryumsthumeinformationen**](/windows/desktop/api/WinBase/nf-winbase-queryumsthreadinformation)<br/>         | Ruft Informationen über den angegebenen ums-Arbeitsthreads ab.<br/>                                       |
| [**Informationen zu "abtumsthinfo"**](/windows/desktop/api/WinBase/nf-winbase-setumsthreadinformation)<br/>             | Legt anwendungsspezifische Kontextinformationen für den angegebenen ums-Arbeits Thread fest.<br/>                 |
| [*Umsschedulerproc*](/windows/desktop/api/WinNT/nc-winnt-rtl_ums_scheduler_entry_point)<br/>                             | Die Anwendungs definierte ums-Scheduler-Einstiegspunkt Funktion, die mit einer ums-Vervollständigungsliste verknüpft ist. <br/> |
| [**Umsthumyield**](/windows/desktop/api/WinBase/nf-winbase-umsthreadyield)<br/>                               | Übergibt die Steuerung an den ums-planerthread, in dem der aufrufenden ums-Arbeits Thread ausgeführt wird.<br/>      |



 

## <a name="new-structures"></a>Neue Strukturen



| Struktur                                                                                                 | BESCHREIBUNG                                                                                         |
|-----------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------|
| [**Cache \_ Beziehung**](/windows/desktop/api/WinNT/ns-winnt-cache_relationship)<br/>                                              | Beschreibt Cache Attribute. <br/>                                                             |
| [**Gruppen \_ Affinität**](/windows/desktop/api/WinNT/ns-winnt-group_affinity)<br/>                                                      | Enthält eine Prozessor gruppenspezifische Affinität, z. b. die Affinität eines Threads.<br/>          |
| [**Gruppen \_ Beziehung**](/windows/desktop/api/WinNT/ns-winnt-group_relationship)<br/>                                              | Enthält Informationen zu Prozessor Gruppen. <br/>                                            |
| [**NUMA- \_ Knoten \_ Beziehung**](/windows/desktop/api/WinNT/ns-winnt-numa_node_relationship)<br/>                                     | Enthält Informationen über einen NUMA-Knoten in einer Prozessor Gruppe. <br/>                            |
| [**Informationen zur Prozessor \_ Gruppe \_**](/windows/desktop/api/WinNT/ns-winnt-processor_group_info)<br/>                                         | Enthält die Anzahl und die Affinität von Prozessoren in einer Prozessor Gruppe.<br/>                     |
| [**Prozessor \_ Nummer**](/windows/desktop/api/WinNT/ns-winnt-processor_number)<br/>                                                  | Stellt einen logischen Prozessor in einer Prozessor Gruppe dar.<br/>                                     |
| [**Prozessor \_ Beziehung**](/windows/desktop/api/WinNT/ns-winnt-processor_relationship)<br/>                                      | Enthält Informationen über die Affinität innerhalb einer Prozessor Gruppe.<br/>                            |
| [**\_Informationen zum logischen System Prozessor ( \_ \_ \_ Ex)**](/windows/desktop/api/WinNT/ns-winnt-system_logical_processor_information_ex)<br/> | Enthält Informationen über die Beziehungen von logischen Prozessoren und zugehöriger Hardware.<br/> |
| [**UMS \_ Create \_ Thread- \_ Attribute**](/windows/desktop/api/WinNT/ns-winnt-ums_create_thread_attributes)<br/>                        | Gibt Attribute für einen ums-Arbeitsthreads an. <br/>                                           |
| [**UMS- \_ Scheduler- \_ Start \_ Informationen**](/windows/desktop/api/WinBase/ns-winbase-ums_scheduler_startup_info)<br/>                            | Gibt Attribute für einen ums-Scheduler-Thread an.<br/>                                          |



 

 

 
