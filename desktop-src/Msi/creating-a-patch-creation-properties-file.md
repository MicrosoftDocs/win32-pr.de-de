---
description: Um das Beispiel-Patchpaket zu reproduzieren, benötigen Sie ein Software Tool, mit dem ein Windows Installer Patch-Paket erstellt und bearbeitet werden kann.
ms.assetid: 0653d8f6-89b0-4c56-ae51-3c7cb7df2909
title: Erstellen einer Eigenschaften Datei für die Patcherstellung
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2775f8521731b43264df315ae05a874e37dd3ffc
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106351588"
---
# <a name="creating-a-patch-creation-properties-file"></a>Erstellen einer Eigenschaften Datei für die Patcherstellung

Um das Beispiel-Patchpaket zu reproduzieren, benötigen Sie ein Software Tool, mit dem ein Windows Installer Patch-Paket erstellt und bearbeitet werden kann. Mehrere Tools zum Erstellen von patchpaketen sind von unabhängigen Softwareanbietern verfügbar. Im Beispiel, das in den folgenden Abschnitten erläutert wird, wird ein Windows Installer Datenbank-Editor namens Orca verwendet, um eine Eigenschaften Datei für die Patcherstellung (PCP-Erweiterung) zu erstellen. Die PCP-Datei kann mit den Dienstprogrammen [Msimsp.exe](msimsp-exe.md) und [Patchwiz.dll](patchwiz-dll.md) verwendet werden, um ein Windows Installer Patchpaket (MSP-Erweiterung) zu generieren. Orca, Msimsp.exe und Patchwiz.dll werden in den [Windows SDK Komponenten für Windows Installer Entwickler](platform-sdk-components-for-windows-installer-developers.md)bereitgestellt.

Mit dem SDK wird auch eine leere patcherstellungs-Eigenschaften Datei (Template. PCP) bereitgestellt. Erstellen Sie eine Kopie von Template. PCP, und benennen Sie diese Kopie MNP2000. PCP um. Verwenden Sie den Orca oder einen anderen Daten Bank Editor, um die folgenden Daten in die Properties-Tabelle von MNP2000. PCP einzugeben. Die Properties-Tabelle enthält globale Einstellungen für das Patchpaket.

[Eigenschaftentabelle](properties-table-patchwiz-dll-.md)



| Name                               | Wert                                  |
|------------------------------------|----------------------------------------|
| Allowproductcodemismatches         | 1                                      |
| Allowproductversionmajormismatches | 1                                      |
| Apipatchingsymbolflags             | 0x00000000                             |
| Dontremuvetempfolder. beendet   | 1                                      |
| Incluentwholefilesonly              | 0                                      |
| ListOf patchguidstoreplace          |                                        |
| Listoftargetproductcodes           | \*                                     |
| Patchguid                          | {5406b219-A1ac-4bc4-8695-72292c8195ac} |
| Patchoutputpath                    | c: \\ Output. msp                         |
| Patchsourcelist                    | Patchsourcelist                        |



 

Verwenden Sie den Datenbank-Editor, um die folgenden Daten in die Tabelle ImageFamilies von MNP2000. PCP einzugeben. Die Tabelle "ImageFamilies" enthält Informationen, die der [Medien Tabelle](media-table.md) beim Patchen hinzugefügt werden sollen.

[Tabelle "ImageFamilies"](imagefamilies-table-patchwiz-dll-.md)



| Familie  | Mediasrcpropname | Mediadiskid | Filesequencestart | Diskprompt | VolumeLabel |
|---------|------------------|-------------|-------------------|------------|-------------|
| Mnpapps | Mnpsrcpropname   | 2           | 1000              |            |             |



 

Geben Sie die folgenden Daten in die Tabelle "UpgradedImages" von MNP2000. PCP ein. Die Tabelle UpgradedImages enthält Informationen zu dem aktualisierten Image, das Sie in [Planen eines kleinen Update Patches](planning-a-small-update-patch.md)erstellt haben.

[UpgradedImages-Tabelle](upgradedimages-table-patchwiz-dll-.md)



| Upgraded   | Msipath                                           | Patchmsipath | SymbolPath | Familie  |
|------------|---------------------------------------------------|--------------|-------------|---------|
| MNP \_ korrigiert | C: \\ Hinweis zum \_ Aktualisieren des Installer- \\ Patches \\ \\MNP2000.msi |              |             | Mnpapps |



 

Geben Sie die folgenden Daten in die Tabelle TargetImages von MNP2000. PCP ein. Die Tabelle TargetImages enthält Informationen zum Zielimage.

[TargetImages-Tabelle](targetimages-table-patchwiz-dll-.md)



| Ziel     | Msipath                                         | SymbolPath | Upgraded   | Auftrag | Productvalidateflags | Ignoremissingsrcfiles |
|------------|-------------------------------------------------|-------------|------------|-------|----------------------|-----------------------|
| MNP- \_ Fehler | C: \\ Hinweis \_ zur \\MNP2000.msi des installerpatchziels \\ \\ |             | MNP \_ korrigiert | 1     |                      | 0                     |



 

Belassen Sie für das Beispiel Patch-Paket die folgenden Tabellen in MNP2000. PCP leer.

[Tabelle "upgradedfiles" ( \_ OptionalData)](upgradedfiles-optionaldata-table-patchwiz-dll-.md)

[Familyfileranges-Tabelle](familyfileranges-table-patchwiz-dll-.md)

[Targetfiles ( \_ OptionalData-Tabelle)](targetfiles-optionaldata-table-patchwiz-dll-.md)

[Externalfiles-Tabelle](externalfiles-table-patchwiz-dll-.md)

[Tabelle "Upgrade dfilestoignore"](upgradedfilestoignore-table-patchwiz-dll-.md)

[Fortsetzen](generating-a-patch-package.md)

 

 



