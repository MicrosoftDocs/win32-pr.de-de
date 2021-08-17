---
description: Die 64-Bit-Versionen von Windows 7 und Windows Server 2008 R2 und höhere Versionen von Windows unterstützen mehr als 64 logische Prozessoren auf einem einzelnen Computer. Diese Funktionalität ist in 32-Bit-Versionen von Windows nicht verfügbar.
ms.assetid: c627ac0f-96e8-48b5-9103-4316f487e173
title: Prozessorgruppen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: fc5916faf3cf90bce7f8549834fe130f299f782d6b2534969c89d74df454ae9d
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119418670"
---
# <a name="processor-groups"></a>Prozessorgruppen

Die 64-Bit-Versionen von Windows 7 und Windows Server 2008 R2 und höhere Versionen von Windows unterstützen mehr als 64 logische Prozessoren auf einem einzelnen Computer. Diese Funktionalität ist in 32-Bit-Versionen von Windows nicht verfügbar.

Systeme mit mehr als einem physischen Prozessor oder Systeme mit physischen Prozessoren mit mehreren Kernen stellen das Betriebssystem mit mehreren logischen Prozessoren bereit. Ein *logischer Prozessor* ist eine logische Computing-Engine aus der Perspektive des Betriebssystems, der Anwendung oder des Treibers. Ein *Kern* ist eine Prozessoreinheit, die aus einem oder mehreren logischen Prozessoren bestehen kann. Ein *physischer Prozessor* kann aus einem oder mehreren Kernen bestehen. Ein physischer Prozessor entspricht einem Prozessorpaket, einem Socket oder einer CPU.

Die Unterstützung für Systeme mit mehr als 64 logischen Prozessoren basiert auf dem Konzept einer *Prozessorgruppe,* bei der es sich um eine statische Gruppe von bis zu 64 logischen Prozessoren handelt, die als einzelne Planungsentität behandelt wird. Prozessorgruppen werden beginnend mit 0 nummeriert. Systeme mit weniger als 64 logischen Prozessoren verfügen immer über eine einzelne Gruppe, Gruppe 0.

**Windows Server 2008, Windows Vista, Windows Server 2003 und Windows XP:** Prozessorgruppen werden nicht unterstützt.

Wenn das System gestartet wird, erstellt das Betriebssystem Prozessorgruppen und weist den Gruppen logische Prozessoren zu. Wenn das System Prozessoren hinzufügen kann, lässt das Betriebssystem Speicherplatz in Gruppen für Prozessoren zu, die möglicherweise während der Ausführung des Systems eingehen. Das Betriebssystem minimiert die Anzahl der Gruppen in einem System. Ein System mit 128 logischen Prozessoren verfügt beispielsweise über zwei Prozessorgruppen mit 64 Prozessoren in jeder Gruppe, nicht über vier Gruppen mit 32 logischen Prozessoren in jeder Gruppe.

Zur Verbesserung der Leistung berücksichtigt das Betriebssystem die physische Lokalität beim Zuweisen logischer Prozessoren zu Gruppen. Alle logischen Prozessoren in einem Kern und alle Kerne in einem physischen Prozessor werden nach Möglichkeit derselben Gruppe zugewiesen. Physische Prozessoren, die physisch nah beieinander liegen, werden derselben Gruppe zugewiesen. Ein NUMA-Knoten wird einer einzelnen Gruppe zugewiesen, es sei denn, die Kapazität des Knotens überschreitet die maximale Gruppengröße. Weitere Informationen finden Sie unter [NUMA-Unterstützung.](numa-support.md)

Auf Systemen mit 64 oder weniger Prozessoren funktionieren vorhandene Anwendungen ohne Änderungen ordnungsgemäß. Anwendungen, die keine Funktionen aufrufen, die Prozessoraffinitätsmasken oder Prozessornummern verwenden, funktionieren unabhängig von der Anzahl der Prozessoren auf allen Systemen ordnungsgemäß. Um ordnungsgemäß auf Systemen mit mehr als 64 logischen Prozessoren zu arbeiten, müssen die folgenden Arten von Anwendungen möglicherweise geändert werden:

-   Anwendungen, die Prozessorinformationen für das gesamte System verwalten, verwalten oder anzeigen, müssen geändert werden, um mehr als 64 logische Prozessoren zu unterstützen. Ein Beispiel für eine solche Anwendung ist Windows Task-Manager, die die Workload jedes Prozessors im System anzeigt.
-   Anwendungen, für die die Leistung entscheidend ist und die effizient über 64 logische Prozessoren skaliert werden können, müssen geändert werden, um auf solchen Systemen ausgeführt zu werden. Beispielsweise können Datenbankanwendungen von Änderungen profitieren.
-   Wenn eine Anwendung eine DLL mit prozessorbezogenen Datenstrukturen verwendet und die DLL nicht so geändert wurde, dass mehr als 64 logische Prozessoren unterstützt werden, müssen alle Threads in der Anwendung, die von der DLL exportierte Funktionen aufrufen, derselben Gruppe zugewiesen werden.

Standardmäßig ist eine Anwendung auf eine einzelne Gruppe beschränkt, die eine ausreichende Verarbeitungsfunktion für die typische Anwendung bereitstellen sollte. Das Betriebssystem weist zunächst jeden Prozess einer einzelnen Gruppe auf Roundrobin-Weise über die Gruppen im System hinweg zu. Ein Prozess beginnt mit der Ausführung, die einer Gruppe zugewiesen ist. Der erste Thread eines Prozesses wird anfänglich in der Gruppe ausgeführt, der der Prozess zugewiesen ist. Jeder neu erstellte Thread wird derselben Gruppe zugewiesen wie der Thread, der ihn erstellt hat.

Eine Anwendung, die die Verwendung mehrerer Gruppen erfordert, damit sie auf mehr als 64 Prozessoren ausgeführt werden kann, muss explizit bestimmen, wo ihre Threads ausgeführt werden sollen, und ist dafür verantwortlich, die Prozessoraffinitäten der Threads für die gewünschten Gruppen festzulegen. Das [INHERIT \_ PARENT \_ AFFINITY-Flag](process-creation-flags.md) kann verwendet werden, um einen übergeordneten Prozess anzugeben (der sich vom aktuellen Prozess unterscheiden kann), aus dem die Affinität für einen neuen Prozess generiert werden soll. Wenn der Prozess in einer einzelnen Gruppe ausgeführt wird, kann er seine Affinität mit [**GetProcessAffinityMask**](/windows/desktop/api/WinBase/nf-winbase-getprocessaffinitymask) und [**SetProcessAffinityMask**](/windows/desktop/api/WinBase/nf-winbase-setprocessaffinitymask) lesen und ändern, während er in derselben Gruppe verbleibt. Wenn die Prozessaffinität geändert wird, wird die neue Affinität auf ihre Threads angewendet.

Die Affinität eines Threads kann bei der Erstellung mithilfe des erweiterten Attributs [**PROC THREAD ATTRIBUTE GROUP \_ \_ \_ \_ AFFINITY**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-updateprocthreadattribute) mit der [**CreateRemoteThreadEx-Funktion**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-createremotethreadex) angegeben werden. Nachdem der Thread erstellt wurde, kann seine Affinität durch Aufrufen von [**SetThreadAffinityMask**](/windows/desktop/api/WinBase/nf-winbase-setthreadaffinitymask) oder [**SetThreadGroupAffinity**](/windows/win32/api/processtopologyapi/nf-processtopologyapi-setthreadgroupaffinity)geändert werden. Wenn ein Thread einer anderen Gruppe als dem Prozess zugewiesen ist, wird die Affinität des Prozesses aktualisiert, um die Affinität des Threads einzuschließt, und der Prozess wird zu einem Prozess mit mehreren Gruppen. Weitere Affinitätsänderungen müssen für einzelne Threads vorgenommen werden. Die Affinität eines Prozesses mit mehreren Gruppen kann nicht mit [**SetProcessAffinityMask**](/windows/desktop/api/WinBase/nf-winbase-setprocessaffinitymask)geändert werden. Die [**GetProcessGroupAffinity-Funktion**](/windows/win32/api/processtopologyapi/nf-processtopologyapi-getprocessgroupaffinity) ruft die Gruppen ab, denen ein Prozess und seine Threads zugewiesen sind.

Um Affinität für alle Einem Auftragsobjekt zugeordneten Prozesse anzugeben, verwenden Sie die [**SetInformationJobObject-Funktion**](/windows/win32/api/jobapi2/nf-jobapi2-setinformationjobobject) mit der **JobObjectGroupInformation-** oder **JobObjectGroupInformationEx-Informationsklasse.**

Ein logischer Prozessor wird anhand seiner Gruppennummer und seiner gruppenbezogenen Prozessornummer identifiziert. Dies wird durch eine [**PROCESSOR \_ NUMBER-Struktur**](/windows/desktop/api/WinNT/ns-winnt-processor_number) dargestellt. Numerische Prozessornummern, die von Legacyfunktionen verwendet werden, sind gruppenbezogen.

Eine Erläuterung der Änderungen an der Betriebssystemarchitektur zur Unterstützung von mehr als 64 Prozessoren finden Sie im Whitepaper [Unterstützen von Systemen mit mehr als 64 Prozessoren.](https://www.microsoft.com/whdc/system/Sysinternals/MoreThan64proc.mspx)

Eine Liste der neuen Funktionen und Strukturen, die Prozessorgruppen unterstützen, finden Sie unter [Neues in Prozessen und Threads.](what-s-new-in-processes-and-threads.md)

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Mehrere Prozessoren](multiple-processors.md)
</dt> <dt>

[NUMA-Unterstützung](numa-support.md)
</dt> </dl>

 

 
