---
description: Das Zustandsübergangsmodell in einem Schattenkopieanbieter wird durch die Serialisierung der Erstellung von Schattenkopien ab dem Zeitpunkt des Aufrufs von IVssBackupComponents::StartSnapshotSet bis zum Aufruf von IVssBackupComponents::D oSnapshotSet vereinfacht.
ms.assetid: 5dbf0fb3-53cb-4532-9a8f-bd955afe16c4
title: Zustandsübergänge in Schattenkopieanbietern
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ad6141b9b8f221a1e67e95fde1e6b33ad819c0cbdead57eeb676164e89acc392
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118121600"
---
# <a name="state-transitions-in-shadow-copy-providers"></a>Zustandsübergänge in Schattenkopieanbietern

Das Zustandsübergangsmodell in einem Schattenkopieanbieter wird durch die Serialisierung der Erstellung von Schattenkopien von dem Zeitpunkt, zu dem [**IVssBackupComponents::StartSnapshotSet**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-startsnapshotset) aufgerufen wird, bis zum Aufruf von [**IVssBackupComponents::D oSnapshotSet**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-dosnapshotset) vereinfacht. Wenn eine andere Anfordernde während dieser Zeit versucht, eine Schattenkopie zu erstellen, tritt beim Aufruf von **StartSnapshotSet** der Fehler **VSS \_ E SNAPSHOT SET \_ IN \_ \_ \_ PROGRESS** auf, der angibt, dass die zweite Anfordernde warten und es erneut versuchen soll.

VSS wird [**IVssProviderCreateSnapshotSet::AbortSnapshots**](/windows/desktop/api/VsProv/nf-vsprov-ivssprovidercreatesnapshotset-abortsnapshots) nur aufrufen, nachdem der Anfordernde [**DoSnapshotSet**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-dosnapshotset)aufgerufen hat, auch wenn die Schattenkopie fehlschlägt oder vor diesem Punkt abgebrochen wird. Dies bedeutet, dass ein Anbieter erst dann einen Aufruf von **AbortSnapshots** erhält, nachdem [**IVssProviderCreateSnapshotSet::EndPrepareSnapshots**](/windows/desktop/api/VsProv/nf-vsprov-ivssprovidercreatesnapshotset-endpreparesnapshots) aufgerufen wurde. Wenn eine Schattenkopie abgebrochen wird oder vor diesem Punkt fehlschlägt, erhält der Anbieter erst dann einen Hinweis, wenn eine neue Schattenkopie gestartet wird. Aus diesem Grund muss der Anbieter darauf vorbereitet sein, einen out-of-sequence-Aufruf von [**IVssHardwareSnapshotProvider::BeginPrepareSnapshot**](/windows/desktop/api/VsProv/nf-vsprov-ivsshardwaresnapshotprovider-beginpreparesnapshot) zu einem beliebigen Zeitpunkt zu verarbeiten. Dieser Out-of-Sequence-Aufruf stellt den Anfang einer neuen Schattenkopiesequenz dar und hat eine neue Schattenkopiesatz-ID.

 

 



