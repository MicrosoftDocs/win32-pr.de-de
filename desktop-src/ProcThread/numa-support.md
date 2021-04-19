---
description: Das herkömmliche Modell für Multiprozessorunterstützung ist symmetrischer Multiprozessor (SMP). In diesem Modell hat jeder Prozessor gleichen Zugriff auf den Arbeitsspeicher und die e/a-Vorgänge. Wenn weitere Prozessoren hinzugefügt werden, wird der Prozessorbus zu einer Einschränkung der Systemleistung.
ms.assetid: a1263968-2b26-45cc-bdd7-6aa354821a5a
title: NUMA-Unterstützung
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 559df7d4e13571953f2826188bd80ccbc472b2ca
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106349409"
---
# <a name="numa-support"></a>NUMA-Unterstützung

Das herkömmliche Modell für Multiprozessorunterstützung ist symmetrischer Multiprozessor (SMP). In diesem Modell hat jeder Prozessor gleichen Zugriff auf den Arbeitsspeicher und die e/a-Vorgänge. Wenn weitere Prozessoren hinzugefügt werden, wird der Prozessorbus zu einer Einschränkung der Systemleistung.

System-Designer verwenden NUMA (Non-Uniform Memory Access), um die Prozessorgeschwindigkeit zu erhöhen, ohne die Last des Prozessorbus zu erhöhen. Die Architektur ist nicht einheitlich, da jeder Prozessor in der Nähe einiger Speicher Teile und weiter von anderen Teilen des Arbeitsspeichers ist. Der Prozessor erhält schnell Zugriff auf den Arbeitsspeicher, in dem er sich befindet, und es kann länger dauern, bis der Zugriff auf den Arbeitsspeicher, der weiter entfernt ist, möglich ist.

In einem NUMA-System werden CPUs in kleineren Systemen angeordnet, die als *Knoten* bezeichnet werden. Jeder Knoten verfügt über eigene Prozessoren und Arbeitsspeicher und ist über einen Cache übergreifenden Interconnect-Bus mit dem größeren System verbunden.

Das System versucht, die Leistung zu verbessern, indem Threads auf Prozessoren geplant werden, die sich im gleichen Knoten wie der verwendete Arbeitsspeicher befinden. Es wird versucht, Speicher Belegungs Anforderungen innerhalb des Knotens zu erfüllen, bei Bedarf jedoch Arbeitsspeicher von anderen Knoten zuweisen. Außerdem wird eine API bereitgestellt, mit der die Topologie des Systems für Anwendungen zur Verfügung gestellt wird. Sie können die Leistung Ihrer Anwendungen verbessern, indem Sie die NUMA-Funktionen verwenden, um die Zeitplanung und die Speicherauslastung zu optimieren.

Zunächst müssen Sie das Layout der Knoten im System bestimmen. Um den höchsten nummerierten Knoten im System abzurufen, verwenden Sie die Funktion [**getnumahighestnodenumschlag**](/windows/win32/api/systemtopologyapi/nf-systemtopologyapi-getnumahighestnodenumber) . Beachten Sie, dass diese Anzahl nicht garantiert der Gesamtzahl der Knoten im System entspricht. Außerdem ist es nicht garantiert, dass Knoten mit sequenziellen Zahlen geschlossen werden. Um die Liste der Prozessoren im System abzurufen, verwenden Sie die [**getprocessaffinitymask**](/windows/desktop/api/WinBase/nf-winbase-getprocessaffinitymask) -Funktion. Sie können den Knoten für jeden Prozessor in der Liste ermitteln, indem Sie die [**getnumaprocessornode**](/windows/desktop/api/WinBase/nf-winbase-getnumaprocessornode) -Funktion verwenden. Alternativ dazu können Sie die [**getnumanodeprocessormask**](/windows/desktop/api/WinBase/nf-winbase-getnumanodeprocessormask) -Funktion verwenden, um eine Liste aller Prozessoren eines Knotens abzurufen.

Nachdem Sie ermittelt haben, welche Prozessoren zu welchen Knoten gehören, können Sie die Leistung Ihrer Anwendung optimieren. Um sicherzustellen, dass alle Threads für den Prozess auf demselben Knoten ausgeführt werden, verwenden Sie die Funktion [**setprocessaffinitymask**](/windows/desktop/api/WinBase/nf-winbase-setprocessaffinitymask) mit einer Prozess Affinitäts Maske, die Prozessoren im gleichen Knoten angibt. Dies erhöht die Effizienz von Anwendungen, deren Threads auf denselben Speicher zugreifen müssen. Alternativ dazu können Sie die Funktion [**SetThreadAffinityMask**](/windows/desktop/api/WinBase/nf-winbase-setthreadaffinitymask) verwenden, um die Anzahl der Threads auf den einzelnen Knoten einzuschränken.

Speicherintensive Anwendungen müssen die Speicherauslastung optimieren. Verwenden Sie die [**getnumaavailablememorynode**](/windows/desktop/api/WinBase/nf-winbase-getnumaavailablememorynode) -Funktion, um die Menge des für einen Knoten verfügbaren freien Speichers abzurufen. Die [**virtualallocexnuma**](/windows/win32/api/memoryapi/nf-memoryapi-virtualallocexnuma) -Funktion ermöglicht es der Anwendung, einen bevorzugten Knoten für die Speicher Belegung anzugeben. **Virtualallocexnuma** weist keine physischen Seiten zu, sodass es erfolgreich ist, ob die Seiten auf diesem Knoten oder an anderer Stelle im System verfügbar sind. Die physischen Seiten werden bei Bedarf zugewiesen. Wenn der bevorzugte Knoten nicht mehr auf den Seiten ausgeführt wird, verwendet der Speicher-Manager Seiten von anderen Knoten. Wenn der Arbeitsspeicher ausgelagert wird, wird derselbe Prozess verwendet, wenn er wieder zurückgegeben wird.

### <a name="numa-support-on-systems-with-more-than-64-logical-processors"></a>NUMA-Unterstützung für Systeme mit mehr als 64 logischen Prozessoren

Auf Systemen mit mehr als 64 logischen Prozessoren werden Knoten den [Prozessor Gruppen](processor-groups.md) entsprechend der Kapazität der Knoten zugewiesen. Die Kapazität eines Knotens ist die Anzahl der Prozessoren, die beim Starten des Systems mit weiteren logischen Prozessoren vorhanden sind, die hinzugefügt werden können, während das System ausgeführt wird.

**Windows Server 2008, Windows Vista, Windows Server 2003 und Windows XP:** Prozessor Gruppen werden nicht unterstützt.

Jeder Knoten muss vollständig in einer Gruppe enthalten sein. Wenn die Kapazitäten der Knoten relativ klein sind, weist das System der gleichen Gruppe mehr als einen Knoten zu und wählt Knoten aus, die sich physisch in der Nähe zueinander befinden, um die Leistung zu verbessern. Wenn die Kapazität eines Knotens die maximale Anzahl von Prozessoren in einer Gruppe überschreitet, teilt das System den Knoten in mehrere kleinere Knoten auf, die jeweils klein genug sind, um in eine Gruppe zu passen.

Ein idealer NUMA-Knoten für einen neuen Prozess kann mithilfe des erweiterten Attributs " [**proc \_ Thread \_ Attribut \_ bevorzugte \_ Knoten**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-updateprocthreadattribute) " angefordert werden, wenn der Prozess erstellt wird. Wie bei einem Thread idealen Prozessor ist der ideale Knoten ein Hinweis für den Scheduler, der den neuen Prozess der Gruppe zuweist, die den angeforderten Knoten enthält, wenn dies möglich ist.

Die erweiterten NUMA-Funktionen [**getnumaavailablememorynodeex**](/windows/desktop/api/WinBase/nf-winbase-getnumaavailablememorynodeex), " [**getnumanodeprocessormaskex**](/windows/win32/api/systemtopologyapi/nf-systemtopologyapi-getnumanodeprocessormaskex)", " [**getnumaprocessornode Ex**](/windows/desktop/api/WinBase/nf-winbase-getnumaprocessornodeex)" und " [**getnumaproximitynode Ex**](/windows/win32/api/systemtopologyapi/nf-systemtopologyapi-getnumaproximitynodeex) " unterscheiden sich von ihren nicht erweiterten Entsprechungen insofern, als die Knotennummer ein **UShort** -Wert und kein **UCHAR** ist, um die potenziell größere Anzahl von Knoten in einem System mit mehr als 64 logischen Prozessoren zu integrieren. Außerdem enthält der mit den erweiterten Funktionen angegebene Prozessor die Prozessor Gruppe; der mit den nicht erweiterten Funktionen angegebene Prozessor ist Gruppen bezogen. Weitere Informationen finden Sie in den Referenz Themen zu den einzelnen Funktionen.

Eine Gruppen abhängige Anwendung kann mithilfe der entsprechenden erweiterten NUMA-Funktionen alle Threads einem bestimmten Knoten ähnlich wie weiter oben in diesem Thema zuweisen. Die Anwendung verwendet [**getlogicalprocessorinformationex**](/windows/win32/api/sysinfoapi/nf-sysinfoapi-getlogicalprocessorinformationex) , um die Liste aller Prozessoren im System zu erhalten. Beachten Sie, dass die Anwendung die Prozess Affinitäts Maske nicht festlegen kann, es sei denn, der Prozess wird einer einzelnen Gruppe zugewiesen, und der beabsichtigte Knoten befindet sich in dieser Gruppe. In der Regel muss die Anwendung [**setthreadgroupaffität**](/windows/win32/api/processtopologyapi/nf-processtopologyapi-setthreadgroupaffinity) aufrufen, um die zugehörigen Threads auf den vorgesehenen Knoten zu beschränken.

## <a name="numa-api"></a>NUMA-API

In der folgenden Tabelle wird die NUMA-API beschrieben.



| Funktion                                                                     | BESCHREIBUNG                                                                                                                                                                                                                     |
|------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**Zuordnung von "Zuweisung"**](/windows/win32/api/memoryapi/nf-memoryapi-allocateuserphysicalpagesnuma)      | Ordnet physische Speicherseiten zu, die in den AWE-Bereichen eines [](../memory/address-windowing-extensions.md) angegebenen Prozesses zugeordnet und deren Zuordnung aufgehoben werden soll, und gibt den NUMA-Knoten für den physischen Speicher an. |
| [**"Kreatefilemappingnuma"**](/windows/win32/api/memoryapi/nf-memoryapi-createfilemappingnumaw)                      | Erstellt oder öffnet ein benanntes oder unbenanntes Datei Zuordnung-Objekt für eine angegebene Datei und gibt den NUMA-Knoten für den physischen Speicher an.                                                                                              |
| [**GetLogicalProcessorInformation**](/windows/win32/api/sysinfoapi/nf-sysinfoapi-getlogicalprocessorinformation)     | Ruft Informationen über logische Prozessoren und zugehörige Hardware ab.                                                                                                                                                            |
| [**Getlogicalprocessorinformationex**](/windows/win32/api/sysinfoapi/nf-sysinfoapi-getlogicalprocessorinformationex) | Ruft Informationen über die Beziehungen von logischen Prozessoren und zugehöriger Hardware ab.                                                                                                                                       |
| [**Getnumaavailablememorynode**](/windows/desktop/api/WinBase/nf-winbase-getnumaavailablememorynode)             | Ruft die Menge des Arbeitsspeichers ab, der im angegebenen Knoten verfügbar ist.                                                                                                                                                                 |
| [**Getnumaavailablememorynode Ex**](/windows/desktop/api/WinBase/nf-winbase-getnumaavailablememorynodeex)         | Ruft die Menge des Arbeitsspeichers ab, der in einem als **UShort** angegebenen Knoten verfügbar ist.                                                                                                                                             |
| [**Getnumahighestnodenzuber**](/windows/win32/api/systemtopologyapi/nf-systemtopologyapi-getnumahighestnodenumber)                 | Ruft den Knoten ab, der derzeit die höchste Anzahl aufweist.                                                                                                                                                                       |
| [**Getnumanodeprocessormask**](/windows/desktop/api/WinBase/nf-winbase-getnumanodeprocessormask)                 | Ruft die Prozessor Maske für den angegebenen Knoten ab.                                                                                                                                                                            |
| [**Getnumanodeprocessormaskex**](/windows/win32/api/systemtopologyapi/nf-systemtopologyapi-getnumanodeprocessormaskex)             | Ruft die Prozessor Maske für einen Knoten ab, der als **UShort** -Wert angegeben ist.                                                                                                                                                        |
| [**Getnumaprocessornode**](/windows/desktop/api/WinBase/nf-winbase-getnumaprocessornode)                         | Ruft die Knotennummer für den angegebenen Prozessor ab.                                                                                                                                                                          |
| [**Getnumaprocessornode Ex**](/windows/desktop/api/WinBase/nf-winbase-getnumaprocessornodeex)                     | Ruft die Knotennummer als **UShort** -Wert für den angegebenen Prozessor ab.                                                                                                                                                    |
| [**Getnumaproximitynode**](/windows/desktop/api/WinBase/nf-winbase-getnumaproximitynode)                         | Ruft die Knotennummer für den angegebenen Näherungs Bezeichner ab.                                                                                                                                                               |
| [**Getnumaproximitynode Ex**](/windows/win32/api/systemtopologyapi/nf-systemtopologyapi-getnumaproximitynodeex)                     | Ruft die Knotennummer als **UShort** -Wert für den angegebenen Näherungs Bezeichner ab.                                                                                                                                         |
| [**Mapviewoffileexnuma**](/windows/win32/api/winbase/nf-winbase-mapviewoffileexnuma)                          | Ordnet eine Ansicht einer Datei Zuordnung dem Adressraum eines aufrufenden Prozesses zu und gibt den NUMA-Knoten für den physischen Speicher an.                                                                                                 |
| [**Virtualzuweisung-exnuma**](/windows/win32/api/memoryapi/nf-memoryapi-virtualallocexnuma)                            | Reserviert einen Arbeitsspeicher Bereich innerhalb des virtuellen Adressraums des angegebenen Prozesses oder führt einen Commit aus und gibt den NUMA-Knoten für den physischen Speicher an.                                                                          |



 

Die [**queryworkingsettex**](/windows/win32/api/psapi/nf-psapi-queryworkingsetex) -Funktion kann verwendet werden, um den NUMA-Knoten abzurufen, dem eine Seite zugeordnet ist. Ein Beispiel finden Sie unter [Zuordnen von Arbeitsspeicher aus einem NUMA-Knoten](../memory/allocating-memory-from-a-numa-node.md).

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Belegen von Speicher aus einem NUMA-Knoten](../memory/allocating-memory-from-a-numa-node.md)
</dt> <dt>

[Mehrere Prozessoren](multiple-processors.md)
</dt> <dt>

[Prozessorgruppen](processor-groups.md)
</dt> </dl>

 

 
