---
description: Transport fähige Schatten Kopien können verwendet werden, um eine schnelle Wiederherstellung zu ermöglichen.
ms.assetid: 2eaffcf7-01b2-44ce-8bc4-fd9fa42c8a8c
title: Schnelle Wiederherstellung mithilfe von transportable schattenkopierten Volumes
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a588395de36b0e6773eacf7f46a45452a69c13c2
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106363400"
---
# <a name="fast-recovery-using-transportable-shadow-copied-volumes"></a>Schnelle Wiederherstellung mithilfe von transportable schattenkopierten Volumes

[*Transport fähige Schatten Kopien*](vssgloss-t.md) können verwendet werden, um eine *schnelle Wiederherstellung* zu ermöglichen.

Die schnelle Wiederherstellung kann verwendet werden, um schnell zu einer früheren Schatten Kopie zurückzukehren. Hierzu sind folgende Schritte erforderlich:

1.  Erstellen Sie die austauschen-Schatten Kopie der entsprechenden LUNs. Die Schatten Kopie kann entweder [*persistent*](vssgloss-p.md) oder nicht persistent sein.
2.  Entfernen der ursprünglichen LUNs
    1.  Wenn sich der Computer in einem Cluster befindet, markieren Sie die betroffenen Datenträger Ressourcen als offline, oder aktivieren Sie den [Wartungsmodus](/previous-versions/windows/desktop/mscs/maintaining-physical-disk-resources) für diese Datenträger Ressourcen.
    2.  Maskieren Sie die betroffenen LUNs von diesem Computer (und allen anderen Knoten, wenn sich der Computer in einem Cluster befindet).
3.  Importieren Sie die Schatten Kopie mithilfe der [**IVssBackupComponents:: importshots**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-importsnapshots) -Methode.
4.  Unterbrechen Sie die Schatten Kopie mithilfe der [**IVssBackupComponents:: breaksnapshotset**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-breaksnapshotset) -Methode.
5.  Markieren Sie die neuen Schattenkopievolumes als Lese-/Schreib.
6.  Wenn sich der Computer in einem Cluster befindet, machen Sie die neuen schattenkopieluns als ursprüngliche LUNs verfügbar.
    1.  Aufheben der Maskierung der schattenkopieluns auf den anderen Knoten im Cluster.
    2.  Markieren Sie die Ressourcen, die zuvor als offline markiert waren, oder deaktivieren Sie den Wartungsmodus für diese Datenträger Ressourcen.

> [!Note]  
> Transport fähige Schatten Kopien in einem Cluster werden vor Windows Server 2003 mit Service Pack 1 (SP1) nicht unterstützt. Dies wird nur mit kompatiblen LUNs unterstützt, die mindestens eine SCSI-VPD (Vital Product Data)-Seite 0x83 \_ -Speicher Bezeichner vom Typ 1, 2 oder 8 und Association 0 aufweisen, und die LUNs müssen einen Basis Datenträger mit MBR-Partitionierung verwalten.

 

 

 
