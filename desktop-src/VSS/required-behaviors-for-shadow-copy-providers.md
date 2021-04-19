---
description: Ein Schattenkopieanbieter muss den Richtlinien entsprechen, um die Kompatibilität von Anforderungen sicherzustellen.
ms.assetid: 49baeb89-1dc9-45c2-a532-071085a8e52f
title: Erforderliches Verhalten für Schattenkopieanbieter
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f451dea7154a313cd64a3a46fbcc3b5fe663ec12
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106360199"
---
# <a name="required-behaviors-for-shadow-copy-providers"></a>Erforderliches Verhalten für Schattenkopieanbieter

Ein Schattenkopieanbieter muss den Richtlinien entsprechen, um die Kompatibilität von Anforderungen sicherzustellen. Zur Laufzeit muss eine Sicherungs Anwendung oder ein beliebiger anderer Anforderer, der Schatten Kopien verwendet, ordnungsgemäß funktionieren, ohne dass spezifische Details der Anbieter Implementierung vorhanden sind.

## <a name="automagic-resource-management"></a>Automatisierung der Ressourcenverwaltung

Es muss möglich sein, dass der Anforderer einem Schattenkopiesatz einfach ein Volume hinzufügt. Der Anforderer kann schattenkopieattribute wie **VSS \_ Volsnap \_ attr \_ transportable**, **VSS \_ Volsnap \_ attr \_ Differential** und/oder **VSS \_ Volsnap \_ attr \_ Plex** im [**\_ VSS- \_ Momentaufnahme \_ Kontext**](/windows/desktop/api/Vss/ne-vss-vss_snapshot_context)angeben. Der Anbieter muss diese Attribute berücksichtigen. Wenn diese Attribute nicht berücksichtigt werden können, sollte Sie angeben, dass der Schattenkopiesatz nicht unterstützt wird, indem \* *pbissupported* in [**ivsshardwaresnapshotprovider:: arelunssupported**](/windows/desktop/api/VsProv/nf-vsprov-ivsshardwaresnapshotprovider-arelunssupported) auf **false** festgelegt wird.

Der Anbieter darf nicht die Unterstützung einer Schatten Kopie akzeptieren, die nicht erstellt werden kann. Wenn die anfordernde Person kein Plex-oder differenzielle Attribut angibt, muss der Anbieter automaginglogik zum Zuordnen des subsystemraums für die Schatten Kopie einschließen und die Schatten Kopie mithilfe der am besten geeigneten Methode erstellen. Der Hardware Anbieter darf keine anbieterspezifische API zum Verwalten der erforderlichen schattenkopieeigenschaften enthalten.

## <a name="created-shadow-copy-volumes-are-read-only-and-hidden"></a>Erstellte Schattenkopievolumes werden Read-Only und ausgeblendet.

VSS legt Flags für jede betroffene LUN fest, sodass die resultierenden Schattenkopievolumes ausgeblendet und schreibgeschützt werden, wenn Sie von einem Computer mit Windows Server 2003 erkannt werden. Laufwerk Buchstaben und eingebundene Ordner werden nicht automatisch zugewiesen. VSS verwaltet diese Flags während des Lebenszyklus einer Schatten Kopie.

## <a name="hardware-shadow-copy-luns-must-be-readwrite"></a>Hardware Schatten Kopie-LUNs müssen Lese-/Schreibzugriff aufweisen.

VSS unterstützt Hardware Schatten Kopien nur dann, wenn die zugrunde liegende LUN als Lese-/Schreibzugriff zugeordnet ist. Dies muss erfolgen, bevor die Schatten Kopie erstellt wird. Dies kann nicht nach dem Fakt erfolgen. Diese Flags dürfen von Hardware Anbietern nicht geändert werden. Weitere Informationen darüber, wie VSS diese Flags verwendet, finden Sie [unter Erstellen von Schatten Kopien](the-shadow-copy-creation-process.md).

## <a name="auto-import-hardware-shadow-copies-are-not-supported-on-windows-cluster-service"></a>Hardware Schatten Kopien automatisch importieren werden im Windows-Cluster Dienst nicht unterstützt.

Windows Clusterdienst kann keine LUNs mit doppelten Signaturen und Partitionslayout aufnehmen. Die schattenkopieluns müssen auf einen Host außerhalb des Clusters übertragen werden. Weitere Informationen finden Sie unter [schnelle Wiederherstellung mithilfe von transportable-Schattenkopievolumes](fast-recovery-using-transportable-shadow-copied-volumes.md).

## <a name="shadow-copies-that-contain-dynamic-disks-must-be-transported-to-a-different-host"></a>Schatten Kopien, die dynamische Datenträger enthalten, müssen zu einem anderen Host transportiert werden.

**Vor Windows Server 2008:** Die native Unterstützung für dynamische Datenträger kann keine LUNs mit doppelten Signaturen und Konfigurationsdaten Bank Inhalten aufnehmen. Die schattenkopieluns müssen auf einen anderen Host übertragen werden. VSS erzwingt dies, indem Schatten Kopien dynamischer Datenträger nicht automatisch importiert werden. Ein Anforderer sollte eine austauschen-Schatten Kopie nicht zurück auf denselben Host importieren.

**Ab Windows Server 2008:** Diese Einschränkung wird entfernt.

## <a name="providers-are-out-of-process"></a>Anbieter sind außerhalb des Prozesses

Alle Anbieter müssen als Prozess interne com-Komponenten implementiert werden.

## <a name="time-critical-operations"></a>Time-Critical Vorgänge

Lange Vorgänge, wie z. b. das Synchronisieren von plexes, sollten in [**ivsshardwaresnapshotprovider:: beginpreparesnapshot**](/windows/desktop/api/VsProv/nf-vsprov-ivsshardwaresnapshotprovider-beginpreparesnapshot)initiiert werden. Diese Funktion sollte die asynchrone Vorbereitungsarbeit starten und schnell zurückgeben. [**Ivssproviderkreatesnapshotset:: EndPrepareSnapshots**](/windows/desktop/api/VsProv/nf-vsprov-ivssprovidercreatesnapshotset-endpreparesnapshots) fungiert als "Rendezvous"-Funktion – der Anbieter kann synchron in dieser Methode warten, bis die Vorbereitungsarbeit abgeschlossen ist, die von **beginpreparesnapshot** gestartet wurde.

Anbieter dürfen in [**ivssproviderkreatesnapshotset keine Verzögerungen hinzufügen::P recommitsnapshot**](/windows/desktop/api/VsProv/nf-vsprov-ivssprovidercreatesnapshotset-precommitsnapshots), [**ivssproviderfroatesnapshotset:: commitsnapshot**](/windows/desktop/api/VsProv/nf-vsprov-ivssprovidercreatesnapshotset-commitsnapshots)oder [**ivssproviderkreatesnapshotset::P ostcommitsnapshot**](/windows/desktop/api/VsProv/nf-vsprov-ivssprovidercreatesnapshotset-postcommitsnapshots) , wenn Anwendungen während dieser Aufrufe eingefroren sind. **Commitmomentaufnahmen** sollten innerhalb von Sekunden zurückgegeben werden, da diese während des Fensters "leeren" und "Speichern" aufgerufen werden und die VSS-Kernel Unterstützung den Löschvorgang abbricht und hält, wenn das Release nicht innerhalb von 10 Sekunden empfangen wird. Dies würde dazu führen, dass VSS den Vorgang zum Erstellen von Schatten Kopien Wenn der Anbieter mehr als einige Sekunden Zeit benötigt, um diesen Vorgang abzuschließen, besteht eine hohe Wahrscheinlichkeit, dass die Erstellung von Schatten Kopien fehlschlägt.

## <a name="careful-io-during-commitsnapshots"></a>Sorgfältige e/a-Vorgänge während commitmomentaufnahmen

Hardware Anbieter sollten keine e/a-Vorgänge für die Volumes ausführen müssen, die während der [**commitmomentaufnahmen**](/windows/desktop/api/VsProv/nf-vsprov-ivssprovidercreatesnapshotset-commitsnapshots)an der Schatten Kopie beteiligt sind. Wenn e/a-Vorgänge erforderlich sind, dürfen Anbieter keine e/a-Vorgänge für ein ursprüngliches Volume initiieren, während die **commitshots** -Methode verarbeitet wird.

Während [**commitmomentaufnahmen**](/windows/desktop/api/VsProv/nf-vsprov-ivssprovidercreatesnapshotset-commitsnapshots)blockieren VSS-Kernel-Unterstützungs Treiber e/a-Vorgänge für die ursprünglichen Volumes, die Schatten Kopien kopiert werden. Wenn der Anbieter synchrone e/a-Vorgänge für ein Volume verwendet, das sich im Schattenkopiesatz befindet, wird der e/a-Vorgang blockiert, und der schattenkopiercommit-Prozess wird blockiert. Der Anbieter sollte während der **commitmomentaufnahmen** keine Win32-APIs aufzurufen, da diese eine hohe Wahrscheinlichkeit haben, dass e/a-Vorgänge und Deadlocks verursacht werden. Der Timeout Wert für die VSS-Kernel-Unterstützung unterbricht den Deadlock nach 10 Sekunden. Dies führt jedoch zu einem Fehler bei der Erstellung der Schatten Kopie.

Wenn ein e/a-Vorgang versucht werden muss, muss Sie asynchron ausgeführt werden. Die e/a-Vorgänge werden erst ausgeführt, nachdem alle Anbieter von Ihren [**commitmomentaufnahmen**](/windows/desktop/api/VsProv/nf-vsprov-ivssprovidercreatesnapshotset-commitsnapshots) -Methoden zurückgegeben haben. Im Allgemeinen ist es besser, solche Vorgänge im [**postcommitshots**](/windows/desktop/api/VsProv/nf-vsprov-ivssprovidercreatesnapshotset-postcommitsnapshots) -Befehl auszuführen.

## <a name="readwrite-shadow-copy-luns"></a>Lese-/schreibschattenkopie-LUNs

In dieser Version unterstützt VSS nur Lese-/schreibschattenkopie-LUNs, auch wenn die Volumes schreibgeschützt sind. Der Grund hierfür ist, dass das System die Datenstrukturen auf dem Datenträger ändern muss, z. b.:

-   Datenträger Signatur, die während des schattenkopiervorgangs geändert wird
-   Partitions bezogene Datenstrukturen, einschließlich derjenigen, die angeben, dass die Partition schreibgeschützt, ausgeblendet, eine Schatten Kopie ist und keinem Laufwerk Buchstaben zugewiesen werden soll.

## <a name="unique-page-83-information"></a>Eindeutige Seite 83-Informationen

Sowohl die ursprüngliche LUN als auch die neu erstellte Schatten Kopie-LUN müssen mindestens einen eindeutigen Speicher Bezeichner in den Daten der Seite 83 aufweisen. Mindestens ein Speicher \_ Bezeichner mit einem Typ von 1, 2, 3 oder 8 und eine Zuordnung von 0 muss in der ursprünglichen LUN und der neu erstellten schattenkopielun eindeutig sein.

 

 



