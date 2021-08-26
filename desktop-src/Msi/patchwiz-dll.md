---
description: Es wird empfohlen, ein Patcherstellungstool wie Msimsp.exe und Patchwiz.dll zu verwenden, um ein Patchpaket zu generieren.
ms.assetid: aca3bbd2-440a-405f-bddc-5f9cc831b811
title: Patchwiz.dll
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0de7a099a95eb6b42341b7f440f15fadb42e6a5ea8bbf69ff4d61b1fcaa28d21
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "120129170"
---
# <a name="patchwizdll"></a>Patchwiz.dll

Es wird empfohlen, ein Patcherstellungstool wieMsimsp.exeund [ Patchwiz.dll ](msimsp-exe.md) zu verwenden, um ein Patchpaket zu generieren. Patchwiz.dll Version 4.0 ist mit Paketen und Patches kompatibel, die mit früheren Versionen der Patchwiz.dll erstellt wurden. Das Patchwiz.dll-Tool ist nur in den [Windows SDK-Komponenten für Windows Installer-Entwickler](platform-sdk-components-for-windows-installer-developers.md)verfügbar.

Patchwiz.dll Version 4.0 verfügt über eine neue Funktion, [UiCreatePatchPackageEx (Patchwiz.dll),](uicreatepatchpackageex--patchwiz-dll-.md)die die Funktionalität von [UiCreatePatchPackage (Patchwiz.dll)](uicreatepatchpackage-patchwiz-dll-.md)erweitert. Diese Funktionen verwenden eine Patcherstellungs-Eigenschaftendatei (PCP-Datei) und generieren ein [Patchpaket für das](patch-packages.md)Installationsprogramm.

Die PCP-Datei ist eine binäre Datenbankdatei mit dem gleichen Format wie eine Windows Installer-Datenbank (.msi-Datei), jedoch mit einem anderen Datenbankschema. Aus diesem Grund kann eine PCP-Datei mit den gleichen Tools erstellt werden, die für eine Installationsdatenbank verwendet werden.

Sie können eine PCP-Datei erstellen, indem Sie einen Tabellen-Editor wie [Orca.exe](orca-exe.md) verwenden, um Informationen in die leere PCP-Datenbank einzugeben, die mit dem Windows Installer SDK, Template.pcp, bereitgestellt wird. Weitere Informationen finden Sie unter Beispiel für [ein kleines Updatepatching.](a-small-update-patching-example.md)

Die folgenden Datenbanktabellen sind in jeder PCP-Datei erforderlich:

-   [Properties-Tabelle (Patchwiz.dll)](properties-table-patchwiz-dll-.md)
-   [ImageFamilies-Tabelle (Patchwiz.dll)](imagefamilies-table-patchwiz-dll-.md)
-   [Tabelle "UpgradedImages" (Patchwiz.dll)](upgradedimages-table-patchwiz-dll-.md)
-   [TargetImages-Tabelle (Patchwiz.dll)](targetimages-table-patchwiz-dll-.md)

Die folgenden Datenbanktabellen sind optional:

-   [UpgradedFiles \_ OptionalData Table (Patchwiz.dll)](upgradedfiles-optionaldata-table-patchwiz-dll-.md)
-   [FamilyFileRanges-Tabelle (Patchwiz.dll)](familyfileranges-table-patchwiz-dll-.md)
-   [TargetFiles \_ OptionalData Table (Patchwiz.dll)](targetfiles-optionaldata-table-patchwiz-dll-.md)
-   [ExternalFiles-Tabelle (Patchwiz.dll)](externalfiles-table-patchwiz-dll-.md)
-   [UpgradedFilesToIgnore-Tabelle (Patchwiz.dll)](upgradedfilestoignore-table-patchwiz-dll-.md)

Die folgende Tabelle ist in PCP-Dateien erforderlich, deren MinimumRequiredMsiVersion in der [Tabelle Eigenschaften](properties-table-patchwiz-dll-.md) gleich 300 ist.

-   [PatchMetadata-Tabelle (Patchwiz.dll)](patchmetadata-table--patchwiz-dll-.md)

> [!Note]  
> Die Tabelle ist optional, wenn MinimumRequiredMsiVersion ungleich 300 ist.

 

Die mit Windows Installer 3.0 veröffentlichte Version von Patchwiz.dll kann automatisch Patchsequenzierungsinformationen generieren und der [MsiPatchSequence-Tabelle](msipatchsequence-table.md) eines neuen Patches hinzufügen. Die [PatchSequence-Tabelle](patchsequence-table--patchwiz-dll-.md) kann verwendet werden, um der MsiPatchSequence-Tabelle manuell Patchsequenzierungsinformationen hinzuzufügen. Weitere Informationen finden Sie unter [Generieren von Patchsequenzinformationen.](generating-patch-sequence-information---patchwiz-dll-.md)

Ab Patchwiz.dll Version 2.0 können Sie die Geschwindigkeit der nachfolgenden Patcherstellung erhöhen, indem Sie [die Zwischenspeicherung von Patchinformationen (Patchwiz.dll)](patch-information-caching-patchwiz-dll-.md)verwenden.

Die Verwendung von öffentlichen Symbolen für Ihre Ziel- und Upgradeimagebinärdateien kann binäre Patchgrößen um etwa die Hälfte reduzieren. Weitere Informationen finden Sie unter [Verwenden von Symbolen zum Reduzieren der binären Patchgröße.](using-symbols-to-reduce-binary-patch-size.md)

Sie können angeben, dass bestimmte Bereiche der Zieldatei während des Patchens nicht überschrieben werden und dass die Informationen in diesen Regionen beibehalten werden. Weitere Informationen finden Sie unter [Patchen ausgewählter Bereiche einer Datei.](patching-selected-regions-of-a-file.md)

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Veröffentlichte Versionen, Tools und Redistributables](released-versions-tools-and-redistributables.md)
</dt> </dl>

 

 



