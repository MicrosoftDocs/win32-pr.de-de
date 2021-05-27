---
description: Das herkömmliche Modell für die Multiprozessorunterstützung ist symmetrischer Multiprozessor (SMP). In diesem Modell hat jeder Prozessor gleichen Zugriff auf Arbeitsspeicher und E/A. Wenn weitere Prozessoren hinzugefügt werden, wird der Prozessorbus zu einer Einschränkung der Systemleistung.
ms.assetid: a1263968-2b26-45cc-bdd7-6aa354821a5a
title: NUMA-Unterstützung
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 178f53c6b55b6ae291cd5cdcf99386515a441094
ms.sourcegitcommit: f848119a8faa29b27585f4df53f6e50ee9666684
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 05/27/2021
ms.locfileid: "110549805"
---
# <a name="numa-support"></a>NUMA-Unterstützung

Das herkömmliche Modell für die Multiprozessorunterstützung ist symmetrischer Multiprozessor (SMP). In diesem Modell hat jeder Prozessor gleichen Zugriff auf Arbeitsspeicher und E/A. Wenn weitere Prozessoren hinzugefügt werden, wird der Prozessorbus zu einer Einschränkung der Systemleistung.

System-Designer verwenden numa (Non-Uniform Memory Access), um die Prozessorgeschwindigkeit zu erhöhen, ohne die Auslastung des Prozessorbus zu erhöhen. Die Architektur ist nicht einheitlich, da sich jeder Prozessor in der Nähe einiger Teile des Arbeitsspeichers und weiter von anderen Teilen des Arbeitsspeichers befindet. Der Prozessor erhält schnell Zugriff auf den Arbeitsspeicher, dem er sich nähert, während es länger dauern kann, bis er auf den weiter entfernten Arbeitsspeicher zugreifen kann.

In einem NUMA-System werden CPUs in kleineren Systemen angeordnet, die als *Knoten* bezeichnet werden. Jeder Knoten verfügt über eigene Prozessoren und Arbeitsspeicher und ist über einen cachekonsektiven Interconnectbus mit dem größeren System verbunden.

Das System versucht, die Leistung zu verbessern, indem Threads auf Prozessoren geplant werden, die sich auf demselben Knoten wie der verwendete Arbeitsspeicher befinden. Es wird versucht, Speicherbelegungsanforderungen innerhalb des Knotens zu erfüllen, belegt aber bei Bedarf Arbeitsspeicher von anderen Knoten. Außerdem wird eine API bereitgestellt, um die Topologie des Systems für Anwendungen verfügbar zu machen. Sie können die Leistung Ihrer Anwendungen verbessern, indem Sie die NUMA-Funktionen verwenden, um die Zeitplanung und Speicherauslastung zu optimieren.

Zunächst müssen Sie das Layout der Knoten im System bestimmen. Um den höchsten nummerierten Knoten im System abzurufen, verwenden Sie die [**GetNumaHighestNodeNumber-Funktion.**](/windows/win32/api/systemtopologyapi/nf-systemtopologyapi-getnumahighestnodenumber) Beachten Sie, dass diese Anzahl nicht garantiert der Gesamtzahl der Knoten im System entspricht. Außerdem ist es nicht garantiert, dass Knoten mit sequenziellen Zahlen nah beieinander liegen. Um die Liste der Prozessoren auf dem System abzurufen, verwenden Sie die [**GetProcessAffinityMask-Funktion.**](/windows/desktop/api/WinBase/nf-winbase-getprocessaffinitymask) Sie können den Knoten für jeden Prozessor in der Liste mithilfe der [**GetNumaProcessorNode-Funktion**](/windows/desktop/api/WinBase/nf-winbase-getnumaprocessornode) bestimmen. Verwenden Sie alternativ die [**GetNumaNodeProcessorMask-Funktion,**](/windows/desktop/api/WinBase/nf-winbase-getnumanodeprocessormask) um eine Liste aller Prozessoren in einem Knoten abzurufen.

Nachdem Sie ermittelt haben, welche Prozessoren zu welchen Knoten gehören, können Sie die Leistung Ihrer Anwendung optimieren. Um sicherzustellen, dass alle Threads für den Prozess auf demselben Knoten ausgeführt werden, verwenden Sie die [**Funktion SetProcessAffinityMask**](/windows/desktop/api/WinBase/nf-winbase-setprocessaffinitymask) mit einer Prozessaffinitätsmaske, die Prozessoren im gleichen Knoten angibt. Dies erhöht die Effizienz von Anwendungen, deren Threads auf denselben Arbeitsspeicher zugreifen müssen. Alternativ können Sie die [**SetThreadAffinityMask-Funktion**](/windows/desktop/api/WinBase/nf-winbase-setthreadaffinitymask) verwenden, um die Anzahl der Threads auf jedem Knoten zu begrenzen.

Speicherintensive Anwendungen müssen ihre Speicherauslastung optimieren. Verwenden Sie die [**GetNumaAvailableMemoryNode-Funktion,**](/windows/desktop/api/WinBase/nf-winbase-getnumaavailablememorynode) um die Menge an freiem Arbeitsspeicher abzurufen, die für einen Knoten verfügbar ist. Mit [**der VirtualAllocExNuma-Funktion**](/windows/win32/api/memoryapi/nf-memoryapi-virtualallocexnuma) kann die Anwendung einen bevorzugten Knoten für die Speicherzuweisung angeben. **VirtualAllocExNuma** weist keine physischen Seiten zu, sodass dies erfolgreich ist, unabhängig davon, ob die Seiten auf diesem Knoten oder an anderer Stelle im System verfügbar sind. Die physischen Seiten werden bei Bedarf zugeordnet. Wenn die Seiten des bevorzugten Knotens nicht mehr verfügbar sind, verwendet der Arbeitsspeicher-Manager Seiten von anderen Knoten. Wenn der Arbeitsspeicher auspaget, wird der gleiche Prozess verwendet, wenn er wieder in den Speicher geladen wird.

### <a name="numa-support-on-systems-with-more-than-64-logical-processors"></a>NUMA-Unterstützung auf Systemen mit mehr als 64 logischen Prozessoren

Auf Systemen mit mehr als 64 logischen [](processor-groups.md) Prozessoren werden Knoten Prozessorgruppen entsprechend der Kapazität der Knoten zugewiesen. Die Kapazität eines Knotens ist die Anzahl der Prozessoren, die vorhanden sind, wenn das System zusammen mit zusätzlichen logischen Prozessoren gestartet wird, die hinzugefügt werden können, während das System ausgeführt wird.

**Windows Server 2008, Windows Vista, Windows Server 2003 und Windows XP:** Prozessorgruppen werden nicht unterstützt.

Jeder Knoten muss vollständig in einer Gruppe enthalten sein. Wenn die Kapazitäten der Knoten relativ klein sind, weist das System mehr als einen Knoten derselben Gruppe zu und wählt knoten, die sich physisch nah beieinander befinden, um eine bessere Leistung zu erzielen. Wenn die Kapazität eines Knotens die maximale Anzahl von Prozessoren in einer Gruppe überschreitet, teilt das System den Knoten in mehrere kleinere Knoten auf, die jeweils klein genug sind, um in eine Gruppe zu passen.

Ein idealer NUMA-Knoten für einen neuen Prozess kann mit dem erweiterten ATTRIBUT [**\_ PROC THREAD ATTRIBUTE \_ \_ PREFERRED \_ NODE**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-updateprocthreadattribute) angefordert werden, wenn der Prozess erstellt wird. Wie ein idealer Threadprozessor ist der ideale Knoten ein Hinweis für den Planer, der den neuen Prozess nach Möglichkeit der Gruppe zuweist, die den angeforderten Knoten enthält.

Die erweiterten NUMA-Funktionen [**GetNumaAvailableMemoryNodeEx,**](/windows/desktop/api/WinBase/nf-winbase-getnumaavailablememorynodeex) [**GetNumaNodeProcessorMaskEx,**](/windows/win32/api/systemtopologyapi/nf-systemtopologyapi-getnumanodeprocessormaskex) [**GetNumaProcessorNodeEx**](/windows/desktop/api/WinBase/nf-winbase-getnumaprocessornodeex)und [**GetNumaProximityNodeEx**](/windows/win32/api/systemtopologyapi/nf-systemtopologyapi-getnumaproximitynodeex) unterscheiden sich von ihren unbeaufsichtigten Entsprechungen darin, dass die Knotennummer ein **USHORT-Wert** anstelle eines **UCHAR-Werts** ist, um die potenziell größere Anzahl von Knoten in einem System mit mehr als 64 logischen Prozessoren aufzunehmen. Außerdem schließt der Prozessor, der mit den erweiterten Funktionen angegeben oder von den erweiterten Funktionen abgerufen wird, die Prozessorgruppe ein. Der Prozessor, der mit den unbeaufsichtigten Funktionen angegeben oder von diesem abgerufen wird, ist gruppenrelermaßen. Weitere Informationen finden Sie in den Referenzthemen zu einzelnen Funktionen.

Eine gruppenfähige Anwendung kann mithilfe der entsprechenden erweiterten NUMA-Funktionen alle threads einem bestimmten Knoten auf ähnliche Weise wie zuvor in diesem Thema beschrieben zuweisen. Die Anwendung verwendet [**GetLogicalProcessorInformationEx,**](/windows/win32/api/sysinfoapi/nf-sysinfoapi-getlogicalprocessorinformationex) um die Liste aller Prozessoren im System abzurufen. Beachten Sie, dass die Anwendung die Prozessaffinitätsmaske nur festlegen kann, wenn der Prozess einer einzelnen Gruppe zugewiesen ist und sich der vorgesehene Knoten in dieser Gruppe befindet. Normalerweise muss die Anwendung [**SetThreadGroupAffinity**](/windows/win32/api/processtopologyapi/nf-processtopologyapi-setthreadgroupaffinity) aufrufen, um ihre Threads auf den vorgesehenen Knoten zu beschränken.


### <a name="behavior-starting-with-windows-10-build-20348"></a>Verhalten ab Windows 10 Build 20348 

> [!NOTE]
> Ab Windows 10 Build 20348 wurde das Verhalten dieser und anderer NUMA-Funktionen geändert, um Systeme mit Knoten mit mehr als 64 Prozessoren besser zu unterstützen.

Das Erstellen von "falschen" Knoten zur Aufnahme einer 1:1-Zuordnung zwischen Gruppen und Knoten hat zu verwirrenden Verhaltensweisen bei einer unerwarteten Anzahl von NUMA-Knoten führen können. Ab Windows 10 Build 20348 hat sich das Betriebssystem geändert, sodass mehrere Gruppen einem Knoten zugeordnet werden können. Daher kann nun die echte NUMA-Topologie des Systems gemeldet werden.  

Im Rahmen dieser Änderungen am Betriebssystem wurde eine Reihe von NUMA-APIs geändert, um die Berichterstellung für mehrere Gruppen zu unterstützen, die jetzt einem einzelnen NUMA-Knoten zugeordnet werden können. Aktualisierte und neue APIs werden in der Tabelle unten im **Abschnitt NUMA-API** bezeichnet.

Da sich das Entfernen der Knotenteilung möglicherweise auf vorhandene Anwendungen auswirken kann, steht ein Registrierungswert zur Verfügung, um die Zurücksetzung auf das Legacyverhalten der Knotenteilung zu ermöglichen. Die Knotenteilung kann erneut aktiviert  werden, indem ein REG_DWORD namens "SplitLargeNodes" mit dem Wert 1 unterhalb HKEY_LOCAL_MACHINE\System\CurrentControlSet\Control\NUMA. Änderungen an dieser Einstellung erfordern einen Neustart, um wirksam zu werden.

```powershell
reg add "HKEY_LOCAL_MACHINE\SYSTEM\CurrentControlSet\Control\NUMA" /v SplitLargeNumaNodes /t REG_DWORD /v 1
```

> [!NOTE]
> Anwendungen, die aktualisiert werden, um die neue API-Funktionalität zu verwenden, die die echte NUMA-Topologie meldet, funktionieren weiterhin ordnungsgemäß auf Systemen, in denen die große Knotenteilung mit diesem Registrierungsschlüssel erneut verfügbar gemacht wurde.

Im folgenden Beispiel werden zunächst potenzielle Probleme bei der Zuordnung von Prozessoren zu NUMA-Knoten durch Builds von Tabellen mithilfe der Legacyaffinitäts-APIs veranschaulicht, die keine vollständige Abdeckung aller Prozessoren im System mehr bieten, was zu einer unvollständigen Tabelle führen kann. Die Auswirkungen einer solchen Vollständigkeit hängen vom Inhalt der Tabelle ab. Wenn in der Tabelle einfach die entsprechende Knotennummer gespeichert wird, ist dies wahrscheinlich nur ein Leistungsproblem, bei dem die nicht entdeckten Prozessoren als Teil von Knoten 0 übrig bleiben. Wenn die Tabelle jedoch Zeiger auf eine Kontextstruktur pro Knoten enthält, kann dies zur Laufzeit zu NULL-Dereferenzen führen.

Als Nächstes veranschaulicht das Codebeispiel zwei Problemumgehungen. Die erste besteht in der Migration zu den Multigruppen-Knotenaffinitäts-APIs (Benutzermodus und Kernelmodus). Die zweite besteht darin, **KeQueryLogicalProcessorRelationship** zu verwenden, um den NUMA-Knoten, der einer bestimmten Prozessornummer zugeordnet ist, direkt abfragt.

```cpp

//
// Problematic implementation using KeQueryNodeActiveAffinity.
//

USHORT CurrentNode;
USHORT HighestNodeNumber;
GROUP_AFFINITY NodeAffinity;
ULONG ProcessorIndex;
PROCESSOR_NUMBER ProcessorNumber;

HighestNodeNumber = KeQueryHighestNodeNumber();
for (CurrentNode = 0; CurrentNode <= HighestNodeNumber; CurrentNode += 1) {

    KeQueryNodeActiveAffinity(CurrentNode, &NodeAffinity, NULL);
    while (NodeAffinity.Mask != 0) {

        ProcessorNumber.Group = NodeAffinity.Group;
        BitScanForward(&ProcessorNumber.Number, NodeAffinity.Mask);

        ProcessorIndex = KeGetProcessorIndexFromNumber(&ProcessorNumber);

        ProcessorNodeContexts[ProcessorIndex] = NodeContexts[CurrentNode;]

        NodeAffinity.Mask &= ~((KAFFINITY)1 << ProcessorNumber.Number);
    }
}

//
// Resolution using KeQueryNodeActiveAffinity2.
//

USHORT CurrentIndex;
USHORT CurrentNode;
USHORT CurrentNodeAffinityCount;
USHORT HighestNodeNumber;
ULONG MaximumGroupCount;
PGROUP_AFFINITY NodeAffinityMasks;
ULONG ProcessorIndex;
PROCESSOR_NUMBER ProcessorNumber;
NTSTATUS Status;

MaximumGroupCount = KeQueryMaximumGroupCount();
NodeAffinityMasks = ExAllocatePool2(POOL_FLAG_PAGED,
                                    sizeof(GROUP_AFFINITY) * MaximumGroupCount,
                                    'tseT');

if (NodeAffinityMasks == NULL) {
    return STATUS_NO_MEMORY;
}

HighestNodeNumber = KeQueryHighestNodeNumber();
for (CurrentNode = 0; CurrentNode <= HighestNodeNumber; CurrentNode += 1) {

    Status = KeQueryNodeActiveAffinity2(CurrentNode,
                                        NodeAffinityMasks,
                                        MaximumGroupCount,
                                        &CurrentNodeAffinityCount);
    NT_ASSERT(NT_SUCCESS(Status));

    for (CurrentIndex = 0; CurrentIndex < CurrentNodeAffinityCount; CurrentIndex += 1) {

        CurrentAffinity = &NodeAffinityMasks[CurrentIndex];

        while (CurrentAffinity->Mask != 0) {

            ProcessorNumber.Group = CurrentAffinity.Group;
            BitScanForward(&ProcessorNumber.Number, CurrentAffinity->Mask);

            ProcessorIndex = KeGetProcessorIndexFromNumber(&ProcessorNumber);

            ProcessorNodeContexts[ProcessorIndex] = NodeContexts[CurrentNode];

            CurrentAffinity->Mask &= ~((KAFFINITY)1 << ProcessorNumber.Number);
        }
    }
}

//
// Resolution using KeQueryLogicalProcessorRelationship.
//

ULONG ProcessorCount;
ULONG ProcessorIndex;
SYSTEM_LOGICAL_PROCESSOR_INFORMATION_EX ProcessorInformation;
ULONG ProcessorInformationSize;
PROCESSOR_NUMBER ProcessorNumber;
NTSTATUS Status;

ProcessorCount = KeQueryActiveProcessorCountEx(ALL_PROCESSOR_GROUPS);

for (ProcessorIndex = 0; ProcessorIndex < ProcessorCount; ProcessorIndex += 1) {

    Status = KeGetProcessorNumberFromIndex(ProcessorIndex, &ProcessorNumber);
    NT_ASSERT(NT_SUCCESS(Status));

    ProcessorInformationSize = sizeof(ProcessorInformation);
    Status = KeQueryLogicalProcessorRelationship(&ProcessorNumber,
                                                    RelationNumaNode,
                                                    &ProcessorInformation,
                                                    &ProcesorInformationSize);
    NT_ASSERT(NT_SUCCESS(Status));

    NodeNumber = ProcessorInformation.NumaNode.NodeNumber;

    ProcessorNodeContexts[ProcessorIndex] = NodeContexts[NodeNumber];
}
```

## <a name="numa-api"></a>NUMA-API

In der folgenden Tabelle wird die NUMA-API beschrieben.



| Funktion                                                                     | Beschreibung                                                                                                                                                                                                                     |
|------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**AllocateUserPhysicalPagesNuma**](/windows/win32/api/memoryapi/nf-memoryapi-allocateuserphysicalpagesnuma)      | Ordnet physische Speicherseiten zu, die innerhalb eines beliebigen Adressfenstererweiterungsbereichs (Address [Windowing Extensions,](../memory/address-windowing-extensions.md) AWE) eines angegebenen Prozesses zugeordnet und nicht zugeordnet werden sollen, und gibt den NUMA-Knoten für den physischen Speicher an. |
| [**CreateFileMappingNuma**](/windows/win32/api/memoryapi/nf-memoryapi-createfilemappingnumaw)                      | Erstellt oder öffnet ein benanntes oder unbenannte Dateizuordnungsobjekt für eine angegebene Datei und gibt den NUMA-Knoten für den physischen Speicher an.                                                                                              |
| [**GetLogicalProcessorInformation**](/windows/win32/api/sysinfoapi/nf-sysinfoapi-getlogicalprocessorinformation)     | Aktualisiert im Windows 10 Build 20348. Ruft Informationen zu logischen Prozessoren und zugehöriger Hardware ab.                                                                                                                                                            |
| [**GetLogicalProcessorInformationEx**](/windows/win32/api/sysinfoapi/nf-sysinfoapi-getlogicalprocessorinformationex) | Aktualisiert im Windows 10 Build 20348. Ruft Informationen über die Beziehungen von logischen Prozessoren und zugehöriger Hardware ab.                                                                                                                                       |
| [**GetNumaAvailableMemoryNode**](/windows/desktop/api/WinBase/nf-winbase-getnumaavailablememorynode)             | Ruft die im angegebenen Knoten verfügbare Arbeitsspeichermenge ab.                                                                                                                                                                 |
| [**GetNumaAvailableMemoryNodeEx**](/windows/desktop/api/WinBase/nf-winbase-getnumaavailablememorynodeex)         | Ruft die Arbeitsspeichermenge ab, die in einem Knoten verfügbar ist, der als **USHORT-Wert** angegeben ist.                                                                                                                                             |
| [**GetNumaHighestNodeNumber**](/windows/win32/api/systemtopologyapi/nf-systemtopologyapi-getnumahighestnodenumber)                 | Ruft den Knoten ab, der derzeit über die höchste Zahl verfügt.                                                                                                                                                                       |
| [**GetNumaNodeProcessorMask**](/windows/desktop/api/WinBase/nf-winbase-getnumanodeprocessormask)                 | Aktualisiert in Windows 10 Build 20348. Ruft die Prozessormaske für den angegebenen Knoten ab.                                                                                                                                                                            |
| [**GetNumaNodeProcessorMask2**](/windows/win32/api/systemtopologyapi/nf-systemtopologyapi-getnumanodeprocessormask2)                         | Neu in Windows 10 Build 20348. Ruft die Prozessormaske mit mehreren Gruppen des angegebenen Knotens ab.                                                                                                                                                                          |
| [**GetNumaNodeProcessorMaskEx**](/windows/win32/api/systemtopologyapi/nf-systemtopologyapi-getnumanodeprocessormaskex)             | Aktualisiert in Windows 10 Build 20348. Ruft die Prozessormaske für einen Knoten ab, der als **USHORT-Wert** angegeben ist.                                                                                                                                                        |
| [**GetNumaProcessorNode**](/windows/desktop/api/WinBase/nf-winbase-getnumaprocessornode)                         | Ruft die Knotennummer für den angegebenen Prozessor ab.                                                                                                                                                                          |
| [**GetNumaProcessorNodeEx**](/windows/desktop/api/WinBase/nf-winbase-getnumaprocessornodeex)                     | Ruft die Knotennummer als **USHORT-Wert** für den angegebenen Prozessor ab.                                                                                                                                                    |
| [**GetNumaProximityNode**](/windows/desktop/api/WinBase/nf-winbase-getnumaproximitynode)                         | Ruft die Knotennummer für den angegebenen Näherungsbezeichner ab.                                                                                                                                                               |
| [**GetNumaProximityNodeEx**](/windows/win32/api/systemtopologyapi/nf-systemtopologyapi-getnumaproximitynodeex)                     | Ruft die Knotennummer als **USHORT-Wert** für den angegebenen Näherungsbezeichner ab.                                                                                                                                         |
| [**GetProcessDefaultCpuSetMasks**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-getprocessdefaultcpusetmasks)                     | Neu in Windows 10 Build 20348. Ruft die Liste der CPU-Sätze im Prozessstandardsatz ab, der von SetProcessDefaultCpuSetMasks oder SetProcessDefaultCpuSets festgelegt wurde.                                                                                                                                         |
| [**GetThreadSelectedCpuSetMasks**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-getthreadselectedcpusetmasks)                     | Neu in Windows 10 Build 20348. Legt die ausgewählte CPU-Mengenzuweisung für den angegebenen Thread fest. Diese Zuweisung überschreibt die Standardzuweisung des Prozesses, sofern festgelegt.                                                                                                                                          |
| [**MapViewOfFileExNuma**](/windows/win32/api/winbase/nf-winbase-mapviewoffileexnuma)                          | Ordnet eine Ansicht einer Dateizuordnung dem Adressraum eines aufrufenden Prozesses zu und gibt den NUMA-Knoten für den physischen Speicher an.                                                                                                 |
| [**SetProcessDefaultCpuSetMasks**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-setprocessdefaultcpusetmasks)                     | Neu in Windows 10 Build 20348. Legt die STANDARDMÄßIGE CPU Sets-Zuweisung für Threads im angegebenen Prozess fest.                                                                                                                                          |
| [**SetThreadSelectedCpuSetMasks**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-setthreadselectedcpusetmasks)                     | Neu in Windows 10 Build 20348. Legt die ausgewählte CPU-Mengenzuweisung für den angegebenen Thread fest. Diese Zuweisung überschreibt die Standardzuweisung des Prozesses, sofern festgelegt.                                                                                                                                          |
| [**VirtualAllocExNuma**](/windows/win32/api/memoryapi/nf-memoryapi-virtualallocexnuma)                            | Reserviert einen Speicherbereich innerhalb des virtuellen Adressraums des angegebenen Prozesses oder führt einen Commit aus und gibt den NUMA-Knoten für den physischen Speicher an.                                                                          |



 

Die [**QueryWorkingSetEx-Funktion**](/windows/win32/api/psapi/nf-psapi-queryworkingsetex) kann verwendet werden, um den NUMA-Knoten abzurufen, auf dem eine Seite zugeordnet ist. Ein Beispiel finden Sie unter [Zuordnen von Arbeitsspeicher aus einem NUMA-Knoten.](../memory/allocating-memory-from-a-numa-node.md)

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Zuordnen von Arbeitsspeicher aus einem NUMA-Knoten](../memory/allocating-memory-from-a-numa-node.md)
</dt> <dt>

[Mehrere Prozessoren](multiple-processors.md)
</dt> <dt>

[Prozessorgruppen](processor-groups.md)
</dt> </dl>

 

 
