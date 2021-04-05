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
# <a name="simple-shadow-copy-creation-for-backup"></a><span data-ttu-id="564b1-103">Einfache Erstellung von Schatten Kopien für die Sicherung</span><span class="sxs-lookup"><span data-stu-id="564b1-103">Simple Shadow Copy Creation for Backup</span></span>

<span data-ttu-id="564b1-104">Es gibt eine Reihe verschiedener Typen von Schatten Kopien, die ein Anforderer erstellen kann.</span><span class="sxs-lookup"><span data-stu-id="564b1-104">There are a number of different types of shadow copy a requester can create.</span></span> <span data-ttu-id="564b1-105">Bei den meisten Sicherungs Anwendungen würden Sie jedoch folgende Aktionen ausführen:</span><span class="sxs-lookup"><span data-stu-id="564b1-105">However, for most backup applications, you would do the following:</span></span>

1.  <span data-ttu-id="564b1-106">Nennen Sie [**IVssBackupComponents:: SetContext**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-setcontext) mit einem Kontext der VSS \_ ctx- \_ Sicherung.</span><span class="sxs-lookup"><span data-stu-id="564b1-106">Call [**IVssBackupComponents::SetContext**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-setcontext) with a context of VSS\_CTX\_BACKUP.</span></span>
2.  <span data-ttu-id="564b1-107">Nennen Sie [**IVssBackupComponents:: gatherwritermetadata**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-gatherwritermetadata) , um die Kommunikation mit Writern zu initialisieren.</span><span class="sxs-lookup"><span data-stu-id="564b1-107">Call [**IVssBackupComponents::GatherWriterMetadata**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-gatherwritermetadata) to initialize communication with writers.</span></span>
3.  <span data-ttu-id="564b1-108">Nennen Sie [**IVssBackupComponents:: addComponent**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-addcomponent) , um der Sicherung Datei-und Datenbankkomponenten hinzuzufügen.</span><span class="sxs-lookup"><span data-stu-id="564b1-108">Call [**IVssBackupComponents::AddComponent**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-addcomponent) to add file and database components to the backup.</span></span>
4.  <span data-ttu-id="564b1-109">Nennen Sie [**IVssBackupComponents:: startnapshotset**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-startsnapshotset) , um den schattenkopiemechanismus zu initialisieren.</span><span class="sxs-lookup"><span data-stu-id="564b1-109">Call [**IVssBackupComponents::StartSnapshotSet**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-startsnapshotset) to initialize the shadow copy mechanism.</span></span>
5.  <span data-ttu-id="564b1-110">Nennen Sie [**IVssBackupComponents:: adddesnapshotset**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-addtosnapshotset) , um Volumes in die Schatten Kopie einzubeziehen.</span><span class="sxs-lookup"><span data-stu-id="564b1-110">Call [**IVssBackupComponents::AddToSnapshotSet**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-addtosnapshotset) to include volumes in the shadow copy.</span></span>
6.  <span data-ttu-id="564b1-111">Nennen Sie [**IVssBackupComponents::P Analyse forbackup**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-prepareforbackup) , um Writer über Sicherungs Vorgänge zu benachrichtigen.</span><span class="sxs-lookup"><span data-stu-id="564b1-111">Call [**IVssBackupComponents::PrepareForBackup**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-prepareforbackup) to notify writers of backup operations.</span></span>

 

 



