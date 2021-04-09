---
description: Die 64-Bit-Versionen von Windows 7 und Windows Server 2008 R2 und höhere Versionen von Windows unterstützen mehr als 64 logische Prozessoren auf einem einzelnen Computer. Diese Funktionalität ist in 32-Bit-Versionen von Windows nicht verfügbar.
ms.assetid: c627ac0f-96e8-48b5-9103-4316f487e173
title: Prozessorgruppen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: cebc5b9ab1b386847b6561a9f6322c2fca0e2ae5
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104042258"
---
# <a name="processor-groups"></a>Prozessorgruppen

Die 64-Bit-Versionen von Windows 7 und Windows Server 2008 R2 und höhere Versionen von Windows unterstützen mehr als 64 logische Prozessoren auf einem einzelnen Computer. Diese Funktionalität ist in 32-Bit-Versionen von Windows nicht verfügbar.

Systeme mit mehr als einem physischen Prozessor oder Systemen mit physischen Prozessoren, die mehrere Kerne aufweisen, bieten dem Betriebssystem mehrere logische Prozessoren. Ein *logischer Prozessor* ist eine logische Computer-Engine aus der Sicht des Betriebssystems, der Anwendung oder des Treibers. Ein *Kern* ist eine Prozessoreinheit, die aus einem oder mehreren logischen Prozessoren bestehen kann. Ein *physischer Prozessor* kann aus einem oder mehreren Kernen bestehen. Ein physischer Prozessor ist das gleiche wie ein Prozessor Paket, ein Socket oder eine CPU.

Die Unterstützung für Systeme, die mehr als 64 logische Prozessoren aufweisen, basiert auf dem Konzept einer *Prozessor Gruppe*, bei der es sich um einen statischen Satz von bis zu 64 logischen Prozessoren handelt, die als einzelne Zeit Planungs Entität behandelt werden. Prozessor Gruppen werden beginnend mit 0 nummeriert. Systeme mit weniger als 64 logischen Prozessoren verfügen immer über eine einzelne Gruppe, Gruppe 0.

**Windows Server 2008, Windows Vista, Windows Server 2003 und Windows XP:** Prozessor Gruppen werden nicht unterstützt.

Beim Starten des Systems erstellt das Betriebssystem Prozessor Gruppen und weist den Gruppen logische Prozessoren zu. Wenn das System in der Lage ist, Prozessoren hinzuzufügen, lässt das Betriebssystem Speicherplatz in Gruppen für Prozessoren zu, die möglicherweise während der Ausführung des Systems eintreffen. Das Betriebssystem minimiert die Anzahl der Gruppen in einem System. Beispielsweise verfügt ein System mit 128 logischen Prozessoren über zwei Prozessor Gruppen mit 64 Prozessoren in jeder Gruppe, nicht vier Gruppen mit 32 logischen Prozessoren in jeder Gruppe.

Um eine bessere Leistung zu erzielen, übernimmt das Betriebssystem die physische Lokalität beim Zuweisen von logischen Prozessoren zu Gruppen. Alle logischen Prozessoren in einem Kern und alle Kerne in einem physischen Prozessor werden, sofern möglich, derselben Gruppe zugewiesen. Physische Prozessoren, die sich physisch in der Nähe zueinander befinden, werden derselben Gruppe zugewiesen. Ein NUMA-Knoten wird einer einzelnen Gruppe zugewiesen, es sei denn, die Kapazität des Knotens überschreitet die maximale Gruppengröße. Weitere Informationen finden Sie [unter NUMA-Unterstützung](numa-support.md).

Auf Systemen mit 64 oder weniger Prozessoren funktionieren vorhandene Anwendungen ohne Änderungen ordnungsgemäß. Anwendungen, die keine Funktionen mit Prozessor Affinitäts Masken oder Prozessornummern aufzurufen, werden unabhängig von der Anzahl der Prozessoren auf allen Systemen ordnungsgemäß ausgeführt. Um auf Systemen mit mehr als 64 logischen Prozessoren ordnungsgemäß arbeiten zu können, sind für die folgenden Arten von Anwendungen möglicherweise Änderungen erforderlich:

-   Anwendungen, die pro-Prozessor-Informationen für das gesamte System verwalten, warten oder anzeigen, müssen geändert werden, um mehr als 64 logische Prozessoren zu unterstützen. Ein Beispiel für eine solche Anwendung ist der Windows Task-Manager, in dem die Arbeitsauslastung der einzelnen Prozessoren im System angezeigt wird.
-   Anwendungen, deren Leistung kritisch ist und die effizient über 64 logische Prozessoren hinaus skaliert werden können, müssen so geändert werden, dass Sie auf solchen Systemen ausgeführt werden. Datenbankanwendungen können z. b. von Änderungen profitieren.
-   Wenn eine Anwendung eine DLL verwendet, die Prozessor übergreifende Datenstrukturen aufweist, und die dll nicht geändert wurde, um mehr als 64 logische Prozessoren zu unterstützen, müssen alle Threads in der Anwendung, die von der dll exportierte Funktionen aufzurufen, derselben Gruppe zugewiesen werden.

Standardmäßig ist eine Anwendung auf eine einzelne Gruppe beschränkt, die eine umfangreiche Verarbeitungskapazität für die typische Anwendung bereitstellen sollte. Das Betriebssystem weist den einzelnen Prozess anfänglich einer einzelnen Gruppe in den Gruppen im System zu. Ein Prozess beginnt seine Ausführung, die einer Gruppe zugewiesen ist. Der erste Thread eines Prozesses wird anfänglich in der Gruppe ausgeführt, der der Prozess zugewiesen ist. Jeder neu erstellte Thread wird derselben Gruppe wie der Thread zugewiesen, der ihn erstellt hat.

Eine Anwendung, die die Verwendung mehrerer Gruppen erfordert, damit Sie auf mehr als 64 Prozessoren ausgeführt werden kann, muss explizit ermitteln, wo die Threads ausgeführt werden müssen, und Sie ist dafür verantwortlich, die Prozessor Affinitäten der Threads auf die gewünschten Gruppen festzulegen. Das Flag über [ \_ geordnetes \_ Affinitäts Vererbung](process-creation-flags.md) kann verwendet werden, um einen übergeordneten Prozess (der sich vom aktuellen Prozess unterscheiden kann) anzugeben, von dem die Affinität für einen neuen Prozess generiert wird. Wenn der Prozess in einer einzelnen Gruppe ausgeführt wird, kann er seine Affinität mithilfe von " [**getprocessaffinitymask**](/windows/desktop/api/WinBase/nf-winbase-getprocessaffinitymask) " und " [**setprocessaffinitymask**](/windows/desktop/api/WinBase/nf-winbase-setprocessaffinitymask) " lesen und ändern, während Sie in derselben Gruppe verbleiben. Wenn die Prozess Affinität geändert wird, wird die neue Affinität auf Ihre Threads angewendet.

Die Affinität eines Threads kann bei der Erstellung mithilfe des erweiterten Attributs für die [**\_ \_ Attribut \_ Gruppen \_ Affinität "proc Thread Attribute**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-updateprocthreadattribute) " und [**der Funktion "**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-createremotethreadex) " der Funktion "" in der Funktion "-Funktion" Nachdem der Thread erstellt wurde, kann seine Affinität durch Aufrufen von [**SetThreadAffinityMask**](/windows/desktop/api/WinBase/nf-winbase-setthreadaffinitymask) oder [**setthreadgroupaffative**](/windows/win32/api/processtopologyapi/nf-processtopologyapi-setthreadgroupaffinity)geändert werden. Wenn ein Thread einer anderen Gruppe als der Prozess zugewiesen ist, wird die Affinität des Prozesses so aktualisiert, dass die Thread Affinität enthalten ist, und der Prozess wird zu einem Prozess mit mehreren Gruppen. Für einzelne Threads müssen weitere Affinitäts Änderungen vorgenommen werden. die Affinität eines Prozesses mit mehreren Gruppen kann nicht mithilfe von [**setprocessaffinitymask**](/windows/desktop/api/WinBase/nf-winbase-setprocessaffinitymask)geändert werden. Die [**getprocessgroupaff-**](/windows/win32/api/processtopologyapi/nf-processtopologyapi-getprocessgroupaffinity) Funktion Ruft den Satz von Gruppen ab, denen ein Prozess und seine Threads zugewiesen sind.

Um die Affinität für alle einem Auftrags Objekt zugeordneten Prozesse anzugeben, verwenden Sie die [**SetInformationJobObject**](/windows/win32/api/jobapi2/nf-jobapi2-setinformationjobobject) -Funktion mit der " **jobobjectgroupinformation** "-oder " **jobobjectgroupinformationex** "-Informations Klasse.

Ein logischer Prozessor wird durch seine Gruppennummer und deren Gruppen relative Prozessornummer identifiziert. Dies wird durch eine [**Prozessor \_ Zahlen**](/windows/desktop/api/WinNT/ns-winnt-processor_number) Struktur dargestellt. Numerische Prozessor Zahlen, die von Legacy Funktionen verwendet werden, sind Gruppen bezogen.

Eine Erörterung der Änderungen an der Betriebssystemarchitektur zur Unterstützung von mehr als 64 Prozessoren finden Sie im Whitepaper [unterstützende Systeme mit mehr als 64 Prozessoren](https://www.microsoft.com/whdc/system/Sysinternals/MoreThan64proc.mspx).

Eine Liste der neuen Funktionen und Strukturen, die Prozessor Gruppen unterstützen, finden Sie unter [Neues in Prozessen und Threads](what-s-new-in-processes-and-threads.md).

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Mehrere Prozessoren](multiple-processors.md)
</dt> <dt>

[NUMA-Unterstützung](numa-support.md)
</dt> </dl>

 

 
