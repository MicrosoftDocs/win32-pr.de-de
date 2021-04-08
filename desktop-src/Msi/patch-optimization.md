---
description: Windows Installer können das Patchen optimieren, um die für die Anwendung von Patches auf installierte Anwendungen erforderliche Zeit zu verkürzen.
ms.assetid: 2bb1c94a-55b6-4aee-b86d-ee9e1f8ed290
title: Patch-Optimierung
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 86215855bb02314d7eb54c774541b0a2086c7c99
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "103864079"
---
# <a name="patch-optimization"></a>Patch-Optimierung

Windows Installer können das Patchen optimieren, um die für die Anwendung von Patches auf installierte Anwendungen erforderliche Zeit zu verkürzen.

**Windows Installer 2,0:** Nicht unterstützt. Für Versionen von Windows Installer, die vor Windows Installer 3,0 veröffentlicht wurden, führt das Patchen eine komplette Reparatur Installation der Anwendung durch, die erheblich mehr Zeit in Anspruch nehmen kann.

**Windows Installer 3,0 und höher:** Beim Patchen werden nur die Teile einer Anwendung geändert, die durch einen Patch geändert werden.

**Windows Installer 3,1 und höher:** Ab Windows Installer 3,1 erfordert die patchoptimierung, dass für alle Patches in der Transaktion die OptimizedInstallMode-Eigenschaft in der [MsiPatchMetadata-Tabelle](msipatchmetadata-table.md)auf 1 (eins) festgelegt ist.

Wenn in einem Patch nur die folgenden Tabellen geändert werden, werden die mit allen anderen Tabellen verbundenen Aktionen von Windows Installer 3,0 oder höher überspringt, auch wenn diese Aktionen in den Sequenz Tabellen des ursprünglichen Anwendungsinstallations Pakets (MSI-Datei) aufgelistet sind.

-   ["AdminExecuteSequence"](adminexecutesequence-table.md)
-   [AdminUISequence](adminuisequence-table.md)
-   [Condition](condition-table.md)
-   [CustomAction](customaction-table.md)
-   [File](file-table.md)
-   [Filesfpcatalog](filesfpcatalog-table.md)
-   [InstallExecuteSequence](installexecutesequence-table.md)
-   [InstallUISequence](installuisequence-table.md)
-   [Medien](media-table.md)
-   [MoveFile](movefile-table.md)
-   [MsiAssembly](msiassembly-table.md)
-   [Msidigitalcertificate](msidigitalcertificate-table.md)
-   [Msidigitalsignature](msidigitalsignature-table.md)
-   [Msiflehash](msifilehash-table.md)
-   [Msipatchheader](msipatchheaders-table.md)
-   [Patch](patch-table.md)
-   [Patchpaket](patchpackage-table.md)
-   [Eigenschaft](property-table.md)
-   [Registrierung](registry-table.md)
-   [Sfpcatalog](sfpcatalog-table.md)
-   [Export der Typbibliothek](typelib-table.md)
-   [\_Spalten](-columns-table.md)
-   [\_Speicher](-storages-table.md)
-   [\_Datenströme](-streams-table.md)
-   [\_Tabellen](-tables-table.md)
-   [\_Transformview-Tabelle](-transformview-table.md)
-   [\_Überprüfen](-validation-table.md)

Verwenden Sie die Richtlinie [disableflyweightpatching](disableflyweightpatching.md) , um die patchoptimierungs Option zu deaktivieren.

 

 



