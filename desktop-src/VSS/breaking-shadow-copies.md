---
description: 'Ein Anforderer kann einen Schattenkopiesatz mithilfe der IVssBackupComponents:: breaksnapshotset-Methode oder der IVssBackupComponentsEx2:: breaksnapshotsetex-Methode unterbrechen.'
ms.assetid: fb796b2f-b6fb-48ee-8d42-36f88cb165aa
title: Unterbrechen von Schatten Kopien
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7dac84c9f45d16d8a88f9d61ad6e4c277dfad3ae
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106350949"
---
# <a name="breaking-shadow-copies"></a>Unterbrechen von Schatten Kopien

Ein Anforderer kann einen Schattenkopiesatz mithilfe der [**IVssBackupComponents:: breaksnapshotset**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-breaksnapshotset) -Methode oder der [**IVssBackupComponentsEx2:: breaksnapshotsetex**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponentsex2-breaksnapshotsetex) -Methode unterbrechen.

Eine beschädigte Schatten Kopie ist ein Volume, das eine Schatten Kopie enthält, die nicht mehr von VSS verwaltet wird. Das Unterbrechen einer Schatten Kopie hat nur den Sinn, dass der [*Anbieter*](vssgloss-p.md) der Schatten Kopie ein [*Hardware Anbieter*](vssgloss-h.md)ist. Dies liegt daran, dass nur Hardware Anbieter eine Schatten Kopie als tatsächliches Volume mit einem Lebenszyklus unabhängig von VSS implementieren können. Wenn VSS dieses Volume nicht verwaltet, ist es weiterhin verfügbar.

Software Anbieter behalten nur Schatten Kopien bei, wenn Sie an VSS-Vorgängen beteiligt sind. Aus diesem Grund hat das Unterbrechen einer Schatten Kopie keine Bedeutung für Softwareanbieter.

Wenn die Schatten Kopie von einem Hardware Anbieter verwaltet wurde, muss der Anforderer die Schatten Kopie importieren, bevor [**breaksnapshotset**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-breaksnapshotset) oder [**breaksnapshotsetex**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponentsex2-breaksnapshotsetex)aufgerufen wird. Bei nicht transportable (von einem Hardware Anbieter erstellten) Schatten Kopien werden diese implizit als Teil des [**IVssBackupComponents::D osnapshotset**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-dosnapshotset) -Aufrufes importiert.

Nachdem der Anforderer [**breaksnapshotset**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-breaksnapshotset) oder [**breaksnapshotsetex**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponentsex2-breaksnapshotsetex)aufgerufen hat, kann der Schattenkopiesatz weiterhin über seine Geräte Objekte oder andere Zugriffs Pfade aufgerufen werden. er ist jedoch nicht mehr als Schatten Kopie festgelegt. Sie kann mithilfe der VDS-com-Schnittstellen (Virtual Disk Service) als ein oder mehrere LUNs verwaltet werden. Mithilfe von VDS kann ein Anforderer die LUNs in Lese-/Schreibzugriff konvertieren, Sie mit Laufwerk Buchstaben einbinden oder Sie auf anderen Computern maskieren bzw. die Maskierung aufheben. Weitere Informationen finden Sie in der [VDS-API-Dokumentation](../vds/virtual-disk-service-portal.md) .

 

 
