---
description: Windows Das Installationsprogramm kann das Patchen optimieren, um die Zeit zu reduzieren, die zum Anwenden von Patches auf installierte Anwendungen erforderlich ist.
ms.assetid: 2bb1c94a-55b6-4aee-b86d-ee9e1f8ed290
title: Patchoptimierung
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: fee37ba48764f6249410a6dfc2512245aa6ca6dfca68cff09ec15e06a42f9156
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118627643"
---
# <a name="patch-optimization"></a>Patchoptimierung

Windows Das Installationsprogramm kann das Patchen optimieren, um die Zeit zu reduzieren, die zum Anwenden von Patches auf installierte Anwendungen erforderlich ist.

**Windows Installer 2.0:** Nicht unterstützt. Für Versionen des Windows Installers, die vor Windows Installer 3.0 veröffentlicht wurden, wird beim Patchen eine vollständige Reparaturinstallation der Anwendung ausgeführt, die erheblich mehr Zeit in Dauern kann.

**Windows Installer 3.0 und höher:** Der Patchprozess ändert nur die Teile einer Anwendung, die durch einen Patch geändert werden.

**Windows Installer 3.1 und höher:** Ab Windows Installer 3.1 erfordert die Patchoptimierung, dass für alle Patches in der Transaktion die OptimizedInstallMode-Eigenschaft in der [MsiPatchMetadata-Tabelle](msipatchmetadata-table.md)auf 1 (eins) festgelegt ist.

Wenn ein Patch nur die folgenden Tabellen ändert, überspringt Windows Installer 3.0 oder höher die Aktionen, die allen anderen Tabellen zugeordnet sind, auch wenn diese Aktionen in den Sequenztabellen des ursprünglichen Anwendungsinstallationspakets (.msi-Datei) aufgeführt sind.

-   [AdminExecuteSequence](adminexecutesequence-table.md)
-   [AdminUISequence](adminuisequence-table.md)
-   [Condition](condition-table.md)
-   [CustomAction](customaction-table.md)
-   [File](file-table.md)
-   [FileSFPCatalog](filesfpcatalog-table.md)
-   [InstallExecuteSequence](installexecutesequence-table.md)
-   [InstallUISequence](installuisequence-table.md)
-   [Medien](media-table.md)
-   [MoveFile](movefile-table.md)
-   [MsiAssembly](msiassembly-table.md)
-   [MsiDigitalCertificate](msidigitalcertificate-table.md)
-   [MsiDigitalSignature](msidigitalsignature-table.md)
-   [MsiFileHash](msifilehash-table.md)
-   [MsiPatchHeaders](msipatchheaders-table.md)
-   [Patch](patch-table.md)
-   [PatchPackage](patchpackage-table.md)
-   [Eigenschaft](property-table.md)
-   [Registrierung](registry-table.md)
-   [SFPCatalog](sfpcatalog-table.md)
-   [Typelib](typelib-table.md)
-   [\_Spalten](-columns-table.md)
-   [\_Speicher](-storages-table.md)
-   [\_Datenströme](-streams-table.md)
-   [\_Tabellen](-tables-table.md)
-   [\_TransformView-Tabelle](-transformview-table.md)
-   [\_Überprüfung](-validation-table.md)

Verwenden Sie die [DisableFlyWeightPatching-Richtlinie,](disableflyweightpatching.md) um die Patchoptimierungsoption zu deaktivieren.

 

 



