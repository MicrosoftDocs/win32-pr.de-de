---
description: 'Das Zustands Übergangsmodell in einem Schattenkopieanbieter wird durch die Serialisierung der Erstellung von Schatten Kopien von dem Zeitpunkt, an dem IVssBackupComponents:: startnapshotset aufgerufen wird, vereinfacht, bis der Aufruf von IVssBackupComponents::D osnapshotset zurückgibt.'
ms.assetid: 5dbf0fb3-53cb-4532-9a8f-bd955afe16c4
title: Zustandsübergänge in schattenkopieanbietern
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0d628d11419158f947225b2e4cabd7f93975f421
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106358439"
---
# <a name="state-transitions-in-shadow-copy-providers"></a>Zustandsübergänge in schattenkopieanbietern

Das Zustands Übergangsmodell in einem Schattenkopieanbieter wird durch die Serialisierung der Erstellung von Schatten Kopien von dem Zeitpunkt, an dem [**IVssBackupComponents:: startnapshotset**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-startsnapshotset) aufgerufen wird, vereinfacht, bis der Aufruf von [**IVssBackupComponents::D osnapshotset**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-dosnapshotset) zurückgibt. Wenn ein anderer Anforderer versucht, während dieses Zeitraums eine Schatten Kopie zu erstellen, schlägt der Aufruf von **startnapshotset** mit dem in Bearbeitung befindlichen Fehler **VSS \_ E \_ Snapshot \_ \_ \_** fehl. Dies deutet darauf hin, dass der zweite Anforderer warten sollte, und wiederholen Sie den Vorgang.

VSS ruft nur [**ivssproviderkreatesnapshotset:: abortnapshots**](/windows/desktop/api/VsProv/nf-vsprov-ivssprovidercreatesnapshotset-abortsnapshots) auf, wenn die anfordernde Person " [**DoSnapshotSet**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-dosnapshotset)" aufgerufen hat, auch wenn die Schatten Kopie fehlschlägt oder vor diesem Zeitpunkt abgebrochen wird. Dies bedeutet, dass ein Anbieter einen Aufruf von **aborungnapshots** erst empfängt, nachdem [**ivssproviderkreatesnapshotset:: EndPrepareSnapshots**](/windows/desktop/api/VsProv/nf-vsprov-ivssprovidercreatesnapshotset-endpreparesnapshots) aufgerufen wurde. Wenn eine Schatten Kopie vor diesem Zeitpunkt abgebrochen wird oder fehlschlägt, erhält der Anbieter keine Angabe, bis eine neue Schatten Kopie gestartet wird. Aus diesem Grund muss der Anbieter darauf vorbereitet sein, einen Out-of-Sequence-Aufrufen von [**ivsshardwaresnapshotprovider:: beginpreparesnapshot**](/windows/desktop/api/VsProv/nf-vsprov-ivsshardwaresnapshotprovider-beginpreparesnapshot) zu einem beliebigen Zeitpunkt zu verarbeiten. Dieser out-of-Sequence-Befehl stellt den Anfang einer neuen schattenkopiesequenz dar und hat eine neue Schattenkopiesatz-ID.

 

 



