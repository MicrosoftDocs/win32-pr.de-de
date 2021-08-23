---
description: Ein Schattenkopieanbieter muss richtlinienkonform sein, um die Kompatibilität des Anfordernden sicherzustellen.
ms.assetid: 49baeb89-1dc9-45c2-a532-071085a8e52f
title: Erforderliches Verhalten für Schattenkopieanbieter
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 97153d3780701fce6edcde4a4a7740ae1d296b58b2bb44ea38c51f3ab1204499
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119056388"
---
# <a name="required-behaviors-for-shadow-copy-providers"></a>Erforderliches Verhalten für Schattenkopieanbieter

Ein Schattenkopieanbieter muss richtlinienkonform sein, um die Kompatibilität des Anfordernden sicherzustellen. Zur Laufzeit muss eine Sicherungsanwendung oder eine andere Anfordernde, die Schattenkopien verwendet, ordnungsgemäß funktionieren, ohne dass sie über details zur Implementierung eines bestimmten Anbieters wissen muss.

## <a name="automagic-resource-management"></a>Automatische Ressourcenverwaltung

Der Anfordernde muss einem Schattenkopiesatz einfach ein Volume hinzufügen können. Der Anfordernde kann Schattenkopieattribute wie **VSS \_ VOLSNAP \_ ATTR \_ TRANSPORTABLE,** **VSS \_ VOLSNAP \_ ATTR \_ DIFFERENTIAL** und/oder **VSS \_ VOLSNAP \_ ATTR \_ PLEX** im [**\_ VSS \_ SNAPSHOT \_ CONTEXT**](/windows/desktop/api/Vss/ne-vss-vss_snapshot_context)angeben. Der Anbieter muss diese Attribute verwenden. Wenn diese Attribute nicht unterstützt werden, sollte dies darauf hinweisen, dass der Schattenkopiesatz nicht unterstützt wird, indem \* *pbIsSupported* in [**IVssHardwareSnapshotProvider::AreLunsSupported**](/windows/desktop/api/VsProv/nf-vsprov-ivsshardwaresnapshotprovider-arelunssupported) auf FALSE festgelegt **wird.**

Der Anbieter darf niemals zustimmen, eine Schattenkopie zu unterstützen, die er nicht erstellen kann. Wenn der Anfordernde kein Plex- oder differenzielles Attribut anberaumt, muss der Anbieter die automatische Logik für die Zuweisung von Subsystemspeicherplatz für die Schattenkopie enthalten und die Schattenkopie mit der am besten geeigneten Methode erstellen. Der Hardwareanbieter darf keine anbieterspezifische API zum Verwalten der erforderlichen Schattenkopieeigenschaften enthalten.

## <a name="created-shadow-copy-volumes-are-read-only-and-hidden"></a>Erstellte Schattenkopievolumes werden Read-Only ausgeblendet.

VSS legt Flags für jede betroffene LUN so fest, dass die resultierenden Schattenkopievolumes ausgeblendet und schreibgeschützt sind, wenn sie von einem Computer erkannt werden, auf dem Windows Server 2003 ausgeführt wird. Laufwerkbuchstaben und bereitgestellte Ordner werden nicht automatisch zugewiesen. VSS verwaltet diese Flags während des gesamten Lebenszyklus einer Schattenkopie.

## <a name="hardware-shadow-copy-luns-must-be-readwrite"></a>Hardwareschattenkopie-LUNs müssen gelesen/geschrieben werden

VSS unterstützt Hardwareschattenkopien nur, wenn die zugrunde liegende LUN als Lese-/Schreibzugriff zugeordnet ist. Dies muss vor dem Erstellen der Schattenkopie erfolgen. dies ist nach der Tatsache nicht mehr möglich. Hardwareanbieter sollten diese Flags nicht ändern. Weitere Informationen zur Verwendung dieser Flags durch VSS finden Sie unter [Der Erstellungsprozess für Schattenkopien.](the-shadow-copy-creation-process.md)

## <a name="auto-import-hardware-shadow-copies-are-not-supported-on-windows-cluster-service"></a>Der automatische Import von Hardwareschattenkopien wird für Windows Clusterdienst nicht unterstützt.

Windows Clusterdienst können LUNs mit doppelten Signaturen und Partitionslayout nicht aufnehmen. Die Schattenkopie-LUNs müssen auf einen Host außerhalb des Clusters transportiert werden. Weitere Informationen finden Sie unter [Schnelle Wiederherstellung mit transportierbaren Schattenkopievolumes.](fast-recovery-using-transportable-shadow-copied-volumes.md)

## <a name="shadow-copies-that-contain-dynamic-disks-must-be-transported-to-a-different-host"></a>Schattenkopien, die dynamische Datenträger enthalten, müssen auf einen anderen Host transportiert werden.

**Vor Windows Server 2008:** Die native Unterstützung für dynamische Datenträger kann LUNs mit doppelten Signaturen und Konfigurationsdatenbankinhalten nicht unterstützen. Die Schattenkopie-LUNs müssen auf einen anderen Host transportiert werden. VSS erzwingt dies, indem automatischer Import von Schattenkopien von dynamischen Datenträgern nicht erlaubt wird. Eine anfordernde Person sollte keine transportierbare Schattenkopie zurück auf denselben Host importieren.

**Ab Windows Server 2008:** Diese Einschränkung wurde entfernt.

## <a name="providers-are-out-of-process"></a>Anbieter sind out-of-Process

Alle Anbieter müssen als Out-of-Process-COM-Komponenten implementiert werden.

## <a name="time-critical-operations"></a>Time-Critical Vorgänge

Lange Vorgänge wie das Synchronisieren von Plexes sollten in [**IVssHardwareSnapshotProvider::BeginPrepareSnapshot initiiert werden.**](/windows/desktop/api/VsProv/nf-vsprov-ivsshardwaresnapshotprovider-beginpreparesnapshot) Diese Funktion sollte die asynchrone Vorbereitung starten und schnell zurückkehren. [**IVssProviderCreateSnapshotSet::EndPrepareSnapshots**](/windows/desktop/api/VsProv/nf-vsprov-ivssprovidercreatesnapshotset-endpreparesnapshots) dient als "Rendezvous"-Funktion. Der Anbieter kann synchron in dieser Methode auf den Abschluss der Vorbereitungsarbeit warten, die von **BeginPrepareSnapshot gestartet wurde.**

Anbieter dürfen keine Verzögerungen in [**IVssProviderCreateSnapshotSet::P reCommitSnapshots,**](/windows/desktop/api/VsProv/nf-vsprov-ivssprovidercreatesnapshotset-precommitsnapshots) [**IVssProviderCreateSnapshotSet::CommitSnapshots**](/windows/desktop/api/VsProv/nf-vsprov-ivssprovidercreatesnapshotset-commitsnapshots)oder [**IVssProviderCreateSnapshotSet::P ostCommitSnapshots**](/windows/desktop/api/VsProv/nf-vsprov-ivssprovidercreatesnapshotset-postcommitsnapshots) hinzufügen, da Anwendungen während dieser Aufrufe eingefroren werden. **CommitSnapshots** sollten innerhalb von Sekunden zurückgeben, da dies während des Leerens und Haltens aufgerufen wird, und vsS Kernel Support cancels the Flush and Hold if the release is not received within 10 seconds, which would VSS to fail the shadow copy creation process. Wenn der Anbieter mehr als einige Sekunden benötigt, um diesen Aufruf zu schließen, ist die Wahrscheinlichkeit hoch, dass die Erstellung der Schattenkopie fehlschlägt.

## <a name="careful-io-during-commitsnapshots"></a>Sorgfältige E/A während CommitSnapshots

Hardwareanbieter sollten während [**CommitSnapshots**](/windows/desktop/api/VsProv/nf-vsprov-ivssprovidercreatesnapshotset-commitsnapshots)keine E/A-Bzw. E/A-Dienstleistungen für die volumes, die an der Schattenkopie beteiligt sind, machen müssen. Wenn E/A erforderlich sind, dürfen Anbieter keine E/A-Schritte für ein ursprüngliches Volume initiieren, während sie die **CommitSnapshots-Methode** behandeln.

Während [**CommitSnapshots**](/windows/desktop/api/VsProv/nf-vsprov-ivssprovidercreatesnapshotset-commitsnapshots)blockieren VSS Kernel Support-Treiber E/A auf den ursprünglichen Volumes, die schattenkopiert werden. Wenn der Anbieter synchrone E/A für ein Volume verwendet, das sich im Schattenkopiesatz befindet, wird diese E/A blockiert, und der Schattenkopie-Commitprozess wird deadlocked. Der Anbieter sollte keine Win32-APIs während **CommitSnapshots** aufrufen, da er eine hohe Wahrscheinlichkeit hat, E/A und einen Deadlock zu verursachen. Das VsS-Kernelunterstützungs-Timeout unterbricht diesen Deadlock nach 10 Sekunden, aber dies verursacht einen Fehler bei der Erstellung der Schattenkopie.

Wenn E/A-Vorgänge versucht werden müssen, muss dies asynchron erfolgen. Die E/A wird erst abgeschlossen, nachdem alle Anbieter von ihren [**CommitSnapshots-Methoden zurückgegeben**](/windows/desktop/api/VsProv/nf-vsprov-ivssprovidercreatesnapshotset-commitsnapshots) wurden. Im Allgemeinen ist es besser, solche Vorgänge im [**PostCommitSnapshots-Aufruf**](/windows/desktop/api/VsProv/nf-vsprov-ivssprovidercreatesnapshotset-postcommitsnapshots) durchzuführen.

## <a name="readwrite-shadow-copy-luns"></a>Lese-/Schreibschattenkopie-LUNs

In dieser Version unterstützt VSS nur Lese-/Schreib-Schattenkopie-LUNs, auch wenn die Volumes als schreibgeschützt verfügbar gemacht werden. Der Grund dafür ist, dass das System Datenstrukturen auf dem Datenträger ändern muss, z. B.:

-   Datenträgersignatur, die sich während des Schattenkopieprozesses ändert
-   Partitionsbezogene Datenstrukturen, einschließlich derer, die angeben, dass die Partition schreibgeschützt, ausgeblendet, eine Schattenkopie ist und keinen Laufwerkbuchstaben zugewiesen werden sollte.

## <a name="unique-page-83-information"></a>Eindeutige Informationen zu Seite 83

Sowohl die ursprüngliche LUN als auch die neu erstellte Schattenkopie-LUN müssen mindestens einen eindeutigen Speicherbezeichner in den Seiten 83-Daten enthalten. Mindestens ein SPEICHERBEzeichner mit dem Typ 1, 2, 3 oder 8 und einer Zuordnung von 0 muss für die ursprüngliche LUN und die neu erstellte Schattenkopie-LUN eindeutig \_ sein.

 

 



