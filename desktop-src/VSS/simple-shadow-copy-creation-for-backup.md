---
description: Es gibt eine Reihe verschiedener Typen von Schatten Kopien, die ein Anforderer erstellen kann.
ms.assetid: a20570ea-e3eb-4d65-b8fa-9a27ce1a3e74
title: Einfache Erstellung von Schatten Kopien für die Sicherung
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c11e030c0531c96eee40e9cd5bb7cc9366284985
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "103751032"
---
# <a name="simple-shadow-copy-creation-for-backup"></a>Einfache Erstellung von Schatten Kopien für die Sicherung

Es gibt eine Reihe verschiedener Typen von Schatten Kopien, die ein Anforderer erstellen kann. Bei den meisten Sicherungs Anwendungen würden Sie jedoch folgende Aktionen ausführen:

1.  Nennen Sie [**IVssBackupComponents:: SetContext**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-setcontext) mit einem Kontext der VSS \_ ctx- \_ Sicherung.
2.  Nennen Sie [**IVssBackupComponents:: gatherwritermetadata**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-gatherwritermetadata) , um die Kommunikation mit Writern zu initialisieren.
3.  Nennen Sie [**IVssBackupComponents:: addComponent**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-addcomponent) , um der Sicherung Datei-und Datenbankkomponenten hinzuzufügen.
4.  Nennen Sie [**IVssBackupComponents:: startnapshotset**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-startsnapshotset) , um den schattenkopiemechanismus zu initialisieren.
5.  Nennen Sie [**IVssBackupComponents:: adddesnapshotset**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-addtosnapshotset) , um Volumes in die Schatten Kopie einzubeziehen.
6.  Nennen Sie [**IVssBackupComponents::P Analyse forbackup**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-prepareforbackup) , um Writer über Sicherungs Vorgänge zu benachrichtigen.

 

 



