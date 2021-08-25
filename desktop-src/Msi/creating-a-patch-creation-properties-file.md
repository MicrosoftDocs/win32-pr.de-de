---
description: Um das Beispielpatchpaket zu reproduzieren, benötigen Sie ein Softwaretool, das in der Lage ist, ein Windows Installer-Patchpaket zu erstellen und zu bearbeiten.
ms.assetid: 0653d8f6-89b0-4c56-ae51-3c7cb7df2909
title: Erstellen einer Eigenschaftendatei für die Patcherstellung
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 50873fd508aa9f31435bd401284d38d13310991e150b28f4e24e5ec27f505dc8
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118379405"
---
# <a name="creating-a-patch-creation-properties-file"></a>Erstellen einer Eigenschaftendatei für die Patcherstellung

Um das Beispielpatchpaket zu reproduzieren, benötigen Sie ein Softwaretool, das in der Lage ist, ein Windows Installer-Patchpaket zu erstellen und zu bearbeiten. Mehrere Tools zum Erstellen von Patchpaketen sind von unabhängigen Softwareherstellern verfügbar. Das in den folgenden Abschnitten erläuterte Beispiel verwendet einen Windows Installer-Datenbank-Editor namens Orca, um eine Eigenschaftendatei für die Patcherstellung (ERWEITERUNG PCP) zu erstellen. Die PCP-Datei kann mit [](msimsp-exe.md) den Hilfsprogrammen [](patchwiz-dll.md)Msimsp.exeundPatchwiz.dllverwendet werden, um ein Windows Installer-Patchpaket (MSP-Erweiterung) zu generieren. Orca, Msimsp.exe und Patchwiz.dll werden in den Windows SDK-Komponenten für Windows [Installer-Entwickler bereitgestellt.](platform-sdk-components-for-windows-installer-developers.md)

Eine leere Eigenschaftendatei für die Patcherstellung, template.pcp, wird ebenfalls mit dem SDK bereitgestellt. Erstellen Sie eine Kopie von template.pcp, und benennen Sie diese Kopie MNP2000.pcp um. Verwenden Sie Orca oder einen anderen Datenbank-Editor, um die folgenden Daten in die Properties-Tabelle von MNP2000.pcp ein. Die Tabelle Eigenschaften enthält globale Einstellungen für das Patchpaket.

[Eigenschaftentabelle](properties-table-patchwiz-dll-.md)



| Name                               | Wert                                  |
|------------------------------------|----------------------------------------|
| AllowProductCodeMismatches         | 1                                      |
| AllowProductVersionMajorMismatches | 1                                      |
| ApiPatchingSymbolFlags             | 0x00000000                             |
| DontRemoveTempFolderWhenFinished   | 1                                      |
| IncludeWholeFilesOnly              | 0                                      |
| ListOfPatchGUIDsToReplace          |                                        |
| ListOfTargetProductCodes           | \*                                     |
| PatchGUID                          | {5406B219-A1AC-4BC4-8695-72292C8195AC} |
| PatchOutputPath                    | c: \\ output.msp                         |
| PatchSourceList                    | PatchSourceList                        |



 

Geben Sie mithilfe des Datenbank-Editors die folgenden Daten in die ImageFamilies-Tabelle von MNP2000.pcp ein. Die Tabelle ImageFamilies enthält Informationen, die während des Patchens der [Media-Tabelle](media-table.md) hinzugefügt werden sollen.

[ImageFamilies-Tabelle](imagefamilies-table-patchwiz-dll-.md)



| Familie  | MediaSrcPropName | MediaDiskId | FileSequenceStart | DiskPrompt | VolumeLabel |
|---------|------------------|-------------|-------------------|------------|-------------|
| MNPapps | MNPSrcPropName   | 2           | 1000              |            |             |



 

Geben Sie die folgenden Daten in die Tabelle UpgradedImages von MNP2000.pcp ein. Die Tabelle UpgradedImages enthält Informationen zum aktualisierten Image, das Sie unter [Planning a Small Update Patch (Planen eines kleinen Updatepatches) erstellt haben.](planning-a-small-update-patch.md)

[Tabelle "UpgradedImages"](upgradedimages-table-patchwiz-dll-.md)



| Upgraded   | MsiPath                                           | PatchMsiPath | SymbolPaths | Familie  |
|------------|---------------------------------------------------|--------------|-------------|---------|
| MNP \_ behoben | C: \\ Hinweis: \_ Installer patch upgraded \\ \\ \\MNP2000.msi |              |             | MNPapps |



 

Geben Sie die folgenden Daten in die Tabelle TargetImages von MNP2000.pcp ein. Die Tabelle TargetImages enthält Informationen zum Zielimage.

[TargetImages-Tabelle](targetimages-table-patchwiz-dll-.md)



| Ziel     | MsiPath                                         | SymbolPaths | Upgraded   | Auftrag | ProductValidateFlags | IgnoreMissingSrcFiles |
|------------|-------------------------------------------------|-------------|------------|-------|----------------------|-----------------------|
| MNP-Fehler \_ | C: \\ Hinweis Installer Patch Target \_ \\ \\ \\MNP2000.msi |             | MNP \_ behoben | 1     |                      | 0                     |



 

Lassen Sie für das Beispielpatchpaket die folgenden Tabellen in MNP2000.pcp leer.

[UpgradedFiles \_ OptionalData Table](upgradedfiles-optionaldata-table-patchwiz-dll-.md)

[FamilyFileRanges-Tabelle](familyfileranges-table-patchwiz-dll-.md)

[TargetFiles \_ OptionalData-Tabelle](targetfiles-optionaldata-table-patchwiz-dll-.md)

[ExternalFiles-Tabelle](externalfiles-table-patchwiz-dll-.md)

[Tabelle "UpgradedFilesToIgnore"](upgradedfilestoignore-table-patchwiz-dll-.md)

[Fortsetzen](generating-a-patch-package.md)

 

 



