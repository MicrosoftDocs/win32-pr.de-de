---
description: Ein Anforderer kann einen Schattenkopiesatz mithilfe der IVssBackupComponents::BreakSnapshotSet- oder IVssBackupComponentsEx2::BreakSnapshotSetEx-Methode unterbrechen.
ms.assetid: fb796b2f-b6fb-48ee-8d42-36f88cb165aa
title: Breaking Shadow Copies
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0fee7a17a77bb806bc6e3713c00c9a01b9bc583f56822b9940b0fe2afebb4e7f
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "120032900"
---
# <a name="breaking-shadow-copies"></a>Breaking Shadow Copies

Ein Anforderer kann einen Schattenkopiesatz mithilfe der [**IVssBackupComponents::BreakSnapshotSet-**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-breaksnapshotset) oder [**IVssBackupComponentsEx2::BreakSnapshotSetEx-Methode**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponentsex2-breaksnapshotsetex) unterbrechen.

Eine fehlerhafte Schattenkopie ist ein Volume, das eine Schattenkopie enthält, die nicht mehr von VSS verwaltet wird. Das Abbrechen einer Schattenkopie hat nur dann eine Bedeutung, wenn der [*Anbieter*](vssgloss-p.md) der Schattenkopie ein [*Hardwareanbieter*](vssgloss-h.md)ist. Dies liegt daran, dass nur Hardwareanbieter eine Schattenkopie als tatsächliches Volume mit einem von VSS unabhängigen Lebenszyklus implementieren können. Wenn VSS ein solches Volume nicht verwaltet, ist es weiterhin verfügbar.

Softwareanbieter verwalten Schattenkopien nur, wenn sie an VSS-Vorgängen beteiligt sind. Aus diesem Grund hat das Abbrechen einer Schattenkopie für Softwareanbieter keine Bedeutung.

Wenn die Schattenkopie von einem Hardwareanbieter verwaltet wurde, muss der Anforderer die Schattenkopie importieren, bevor [**er BreakSnapshotSet**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-breaksnapshotset) oder [**BreakSnapshotSetEx**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponentsex2-breaksnapshotsetex)aufruft. Bei nicht transportierbaren (von einem Hardwareanbieter erstellten) Schattenkopien werden diese implizit als Teil des [**IVssBackupComponents::D oSnapshotSet-Aufrufs**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-dosnapshotset) importiert.

Nachdem der Anforderer [**BreakSnapshotSet**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-breaksnapshotset) oder [**BreakSnapshotSetEx**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponentsex2-breaksnapshotsetex)aufgerufen hat, kann auf das Schattenkopieset weiterhin über seine Geräteobjekte oder andere Zugriffspfade zugegriffen werden, es handelt sich jedoch nicht mehr um einen Schattenkopiesatz. Sie kann als eine oder mehrere LUNs mithilfe der COM-Schnittstellen des Virtual Disk Service (VDS) verwaltet werden. Mit vds kann ein Anforderer die LUNs in Lese-/Schreibzugriff konvertieren, sie mit Laufwerkbuchstaben einbinden oder sie auf anderen Computern maskieren/maskieren. Weitere Informationen finden Sie in der [VDS-API-Dokumentation.](../vds/virtual-disk-service-portal.md)

 

 
