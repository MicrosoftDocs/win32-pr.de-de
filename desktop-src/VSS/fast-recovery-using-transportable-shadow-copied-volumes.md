---
description: Transportierbare Schattenkopien können verwendet werden, um eine schnelle Wiederherstellung zu ermöglichen.
ms.assetid: 2eaffcf7-01b2-44ce-8bc4-fd9fa42c8a8c
title: Schnelle Wiederherstellung mit transportierbaren Schattenkopievolumes
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4fb5ddd7604b1463def4ceaa6cd474487255682cf4489b13c5da520128c06811
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "120006400"
---
# <a name="fast-recovery-using-transportable-shadow-copied-volumes"></a>Schnelle Wiederherstellung mit transportierbaren Schattenkopievolumes

[*Transportierbare Schattenkopien*](vssgloss-t.md) können verwendet werden, um eine *schnelle Wiederherstellung* zu ermöglichen.

Die schnelle Wiederherstellung kann verwendet werden, um schnell zu einer früheren Schattenkopie zurückzukehren. Hierzu sind folgende Schritte erforderlich:

1.  Erstellen Sie die transportierbare Schattenkopie der entsprechenden LUNs. Die Schattenkopie kann entweder [*persistent*](vssgloss-p.md) oder nicht beständig sein.
2.  Entfernen der ursprünglichen LUNs
    1.  Wenn sich der Computer in einem Cluster befindet, markieren Sie die betroffenen Datenträgerressourcen als offline, oder aktivieren Sie den [Wartungsmodus](/previous-versions/windows/desktop/mscs/maintaining-physical-disk-resources) für diese Datenträgerressourcen.
    2.  Maskieren Sie die betroffenen LUNs von diesem Computer (und alle anderen Knoten, wenn sich der Computer in einem Cluster befindet).
3.  Importieren Sie die Schattenkopie mithilfe der [**IVssBackupComponents::ImportSnapshots-Methode.**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-importsnapshots)
4.  Unterbrechen Sie die Schattenkopie mithilfe der [**IVssBackupComponents::BreakSnapshotSet-Methode.**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-breaksnapshotset)
5.  Markieren Sie die neuen Schattenkopievolumes als Lese-/Schreibzugriff.
6.  Wenn sich der Computer in einem Cluster befindet, machen Sie die neuen Schattenkopie-LUNs als ursprüngliche LUNs verfügbar.
    1.  Entpacken Sie die Schattenkopie-LUNs für die anderen Knoten im Cluster.
    2.  Markieren Sie die Zuvor als offline markierten Ressourcen als online, oder deaktivieren Sie den Wartungsmodus für diese Datenträgerressourcen.

> [!Note]  
> Transportierbare Schattenkopien in einem Cluster werden vor Windows Server 2003 mit Service Pack 1 (SP1) nicht unterstützt. Dies wird nur bei kompatiblen LUNs unterstützt, die mindestens eine SCSI-Seite für wichtige Produktdaten (SCSI Vital Product Data, VPD) 0x83 STORAGE \_ IDENTIFIER vom Typ 1,2 oder 8 und Zuordnung 0 aufweisen, und die LUNs müssen einen Basisdatenträger mit MBR-Partitionierung beibehalten.

 

 

 
