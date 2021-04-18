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
# <a name="semantic-changes-to-windows-server-2003"></a>Semantik Änderungen an Windows Server 2003

Die Kombination aus Pfad, Datei Spezifikation und Rekursions Flag (*wszpath*, *wszfilespec*, und *bRecursive* müssen mit dem Wert eines der Datei Sätze, die einer der Writer-Komponenten hinzugefügt werden, mithilfe von [**ivsskreateschreitermetadata:: addfilestofilegroup**](/windows/desktop/api/VsWriter/nf-vswriter-ivsscreatewritermetadata-addfilestofilegroup), [**ivsskreateschreitermetadata:: adddatabasefiles**](/windows/desktop/api/VsWriter/nf-vswriter-ivsscreatewritermetadata-adddatabasefiles)oder [**ivsskreateschreitermetadata:: adddatabaselogfiles**](/windows/desktop/api/VsWriter/nf-vswriter-ivsscreatewritermetadata-adddatabaselogfiles) in folgenden Reihen entsprechen:

-   Ein Anforderer fügt mithilfe von [**IVssBackupComponents:: addnewtarget**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-addnewtarget)ein neues Ziel hinzu.
-   Ein Writer fügt mithilfe von [**ivsskreateschreitermetadata:: addalternate elocationmapping**](/windows/desktop/api/VsWriter/nf-vswriter-ivsscreatewritermetadata-addalternatelocationmapping)eine Alternative Speicherort Zuordnung hinzu.
-   Vorhandene Dateien werden mithilfe von [**IVssComponent:: AddDifferencedFilesByLastModifyTime**](/windows/desktop/api/VsWriter/nf-vswriter-ivsscomponent-adddifferencedfilesbylastmodifytime)als differenzierte Dateien hinzugefügt.
-   Ein Anforderer gibt an, dass eine Alternative Speicherort Zuordnung verwendet wurde, um einen Datei Satz mithilfe von [**IVssBackupComponents:: addalternativelocationmapping**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-addalternativelocationmapping)wiederherzustellen.

 

 



