---
description: 'Die Kombination aus Pfad, Datei Spezifikation und Rekursions Flag (wszpath, wszfilespec, und bRecursive müssen mit dem Wert eines der Datei Sätze, die einer der Writer-Komponenten hinzugefügt werden, mithilfe von ivsskreateschreitermetadata:: addfilestofilegroup, ivsskreateschreitermetadata:: adddatabasefiles oder ivsskreateschreitermetadata:: adddatabaselogfiles in folgenden Reihen entsprechen:'
ms.assetid: debf181a-1579-46f2-86ef-a1d2a850e99e
title: Semantik Änderungen an Windows Server 2003
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 53b9d2edc56f215f554b497eebff9f76a1da53dd
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104215542"
---
# <a name="semantic-changes-to-windows-server-2003"></a><span data-ttu-id="f8d13-103">Semantik Änderungen an Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="f8d13-103">Semantic Changes to Windows Server 2003</span></span>

<span data-ttu-id="f8d13-104">Die Kombination aus Pfad, Datei Spezifikation und Rekursions Flag (*wszpath*, *wszfilespec*, und *bRecursive* müssen mit dem Wert eines der Datei Sätze, die einer der Writer-Komponenten hinzugefügt werden, mithilfe von [**ivsskreateschreitermetadata:: addfilestofilegroup**](/windows/desktop/api/VsWriter/nf-vswriter-ivsscreatewritermetadata-addfilestofilegroup), [**ivsskreateschreitermetadata:: adddatabasefiles**](/windows/desktop/api/VsWriter/nf-vswriter-ivsscreatewritermetadata-adddatabasefiles)oder [**ivsskreateschreitermetadata:: adddatabaselogfiles**](/windows/desktop/api/VsWriter/nf-vswriter-ivsscreatewritermetadata-adddatabaselogfiles) in folgenden Reihen entsprechen:</span><span class="sxs-lookup"><span data-stu-id="f8d13-104">The combination of path, file specification, and recursion flag (*wszPath*, *wszFileSpec*, and *bRecursive*, respectively) must match that of one of the file sets added to one of the writer's components using [**IVssCreateWriterMetadata::AddFilesToFileGroup**](/windows/desktop/api/VsWriter/nf-vswriter-ivsscreatewritermetadata-addfilestofilegroup), [**IVssCreateWriterMetadata::AddDatabaseFiles**](/windows/desktop/api/VsWriter/nf-vswriter-ivsscreatewritermetadata-adddatabasefiles), or [**IVssCreateWriterMetadata::AddDatabaseLogFiles**](/windows/desktop/api/VsWriter/nf-vswriter-ivsscreatewritermetadata-adddatabaselogfiles) when:</span></span>

-   <span data-ttu-id="f8d13-105">Ein Anforderer fügt mithilfe von [**IVssBackupComponents:: addnewtarget**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-addnewtarget)ein neues Ziel hinzu.</span><span class="sxs-lookup"><span data-stu-id="f8d13-105">A requester adds a new target using [**IVssBackupComponents::AddNewTarget**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-addnewtarget).</span></span>
-   <span data-ttu-id="f8d13-106">Ein Writer fügt mithilfe von [**ivsskreateschreitermetadata:: addalternate elocationmapping**](/windows/desktop/api/VsWriter/nf-vswriter-ivsscreatewritermetadata-addalternatelocationmapping)eine Alternative Speicherort Zuordnung hinzu.</span><span class="sxs-lookup"><span data-stu-id="f8d13-106">A writer adds an alternate location mapping using [**IVssCreateWriterMetadata::AddAlternateLocationMapping**](/windows/desktop/api/VsWriter/nf-vswriter-ivsscreatewritermetadata-addalternatelocationmapping).</span></span>
-   <span data-ttu-id="f8d13-107">Vorhandene Dateien werden mithilfe von [**IVssComponent:: AddDifferencedFilesByLastModifyTime**](/windows/desktop/api/VsWriter/nf-vswriter-ivsscomponent-adddifferencedfilesbylastmodifytime)als differenzierte Dateien hinzugefügt.</span><span class="sxs-lookup"><span data-stu-id="f8d13-107">Existing files are added as differenced files using [**IVssComponent::AddDifferencedFilesByLastModifyTime**](/windows/desktop/api/VsWriter/nf-vswriter-ivsscomponent-adddifferencedfilesbylastmodifytime).</span></span>
-   <span data-ttu-id="f8d13-108">Ein Anforderer gibt an, dass eine Alternative Speicherort Zuordnung verwendet wurde, um einen Datei Satz mithilfe von [**IVssBackupComponents:: addalternativelocationmapping**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-addalternativelocationmapping)wiederherzustellen.</span><span class="sxs-lookup"><span data-stu-id="f8d13-108">A requester indicates that an alternate location mapping was used to restore a file set using [**IVssBackupComponents::AddAlternativeLocationMapping**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-addalternativelocationmapping).</span></span>

 

 



