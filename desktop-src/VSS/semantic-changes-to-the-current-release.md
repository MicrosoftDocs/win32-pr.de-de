---
description: 'Die Kombination aus Pfad, Dateispezifikation und Rekursionsflag (wszPath, wszFileSpec bzw. bRecursive) muss mit denen eines der Dateisätze übereinstimmen, die einer der Komponenten des Writers mithilfe von IVssCreateWriterMetadata::AddFilesToFileGroup, IVssCreateWriterMetadata::AddDatabaseFiles oder IVssCreateWriterMetadata::AddDatabaseLogFiles hinzugefügt wurden, wenn:'
ms.assetid: debf181a-1579-46f2-86ef-a1d2a850e99e
title: Semantische Änderungen Windows Server 2003
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8319259dc27c981822bb242d20243264ca9025d959693aafcb3836976fd7754d
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119866260"
---
# <a name="semantic-changes-to-windows-server-2003"></a>Semantische Änderungen Windows Server 2003

Die Kombination aus Pfad, Dateispezifikation und Rekursionsflag (*wszPath*, *wszFileSpec* und *bRecursive*) muss mit dem eines der Dateisätze übereinstimmen, die mithilfe von [**IVssCreateWriterMetadata::AddFilesToFileGroup,**](/windows/desktop/api/VsWriter/nf-vswriter-ivsscreatewritermetadata-addfilestofilegroup) [**IVssCreateWriterMetadata::AddDatabaseFiles**](/windows/desktop/api/VsWriter/nf-vswriter-ivsscreatewritermetadata-adddatabasefiles)oder [**IVssCreateWriterMetadata::AddDatabaseFiles oder IVssCreateWriterMetadata::AddDatabaseLogFiles**](/windows/desktop/api/VsWriter/nf-vswriter-ivsscreatewritermetadata-adddatabaselogfiles) hinzugefügt wurden, wenn:

-   Eine Anfordernde fügt mithilfe von [**IVssBackupComponents::AddNewTarget ein neues Ziel hinzu.**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-addnewtarget)
-   Ein Writer fügt mithilfe von [**IVssCreateWriterMetadata::AddAlternateLocationMapping**](/windows/desktop/api/VsWriter/nf-vswriter-ivsscreatewritermetadata-addalternatelocationmapping)eine alternative Speicherortzuordnung hinzu.
-   Vorhandene Dateien werden mithilfe von [**IVssComponent::AddDifferencedFilesByLastModifyTime**](/windows/desktop/api/VsWriter/nf-vswriter-ivsscomponent-adddifferencedfilesbylastmodifytime)als differenzierte Dateien hinzugefügt.
-   Eine Anfordernde gibt an, dass eine alternative Speicherortzuordnung verwendet wurde, um einen Dateisatz mithilfe von [**IVssBackupComponents::AddAlternativeLocationMapping wiederherzustellen.**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-addalternativelocationmapping)

 

 



