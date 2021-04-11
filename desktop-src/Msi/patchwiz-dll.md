---
description: Zum Generieren eines Patchpakets empfiehlt es sich, ein patcherstellungs Tool wie Msimsp.exe und Patchwiz.dll zu verwenden.
ms.assetid: aca3bbd2-440a-405f-bddc-5f9cc831b811
title: Patchwiz.dll
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c6dc1135a9e2c09bb8a96e041f77bae39f0057ea
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "104218521"
---
# <a name="patchwizdll"></a>Patchwiz.dll

Zum Generieren eines Patchpakets empfiehlt es sich, ein patcherstellungs Tool wie [Msimsp.exe](msimsp-exe.md) und Patchwiz.dll zu verwenden. Patchwiz.dll Version 4,0 ist kompatibel mit Paketen und Patches, die mit früheren Versionen der Patchwiz.dll erstellt wurden. Das Patchwiz.dll Tool ist nur in den [Windows SDK Komponenten für Windows Installer Entwickler](platform-sdk-components-for-windows-installer-developers.md)verfügbar.

Patchwiz.dll Version 4,0 verfügt über eine neue Funktion, [uikreatepatchpackageex (Patchwiz.dll)](uicreatepatchpackageex--patchwiz-dll-.md), die die Funktionalität von [uikreatepatchpackage (Patchwiz.dll)](uicreatepatchpackage-patchwiz-dll-.md)erweitert. Diese Funktionen nehmen eine patcherstellungs-Eigenschaften Datei (PCP-Datei) an und generieren ein Installer- [Patchpaket](patch-packages.md).

Bei der PCP-Datei handelt es sich um eine binäre Datenbankdatei mit demselben Format wie eine Windows Installer Datenbank (MSI-Datei), jedoch mit einem anderen Datenbankschema. Daher kann eine PCP-Datei mit denselben Tools erstellt werden, die für eine Installerdatenbank verwendet werden.

Sie können eine PCP-Datei erstellen, indem Sie einen Tabellen-Editor wie [Orca.exe](orca-exe.md) zum Eingeben von Informationen in die leere PCP-Datenbank verwenden, die mit dem Windows Installer SDK (Template. PCP) bereitgestellt wird. Weitere Informationen finden Sie unter [Beispiel für ein kleines Update-Patching](a-small-update-patching-example.md).

Die folgenden Datenbanktabellen sind in jeder PCP-Datei erforderlich:

-   [Properties-Tabelle (Patchwiz.dll)](properties-table-patchwiz-dll-.md)
-   [Tabelle "ImageFamilies" (Patchwiz.dll)](imagefamilies-table-patchwiz-dll-.md)
-   [UpgradedImages-Tabelle (Patchwiz.dll)](upgradedimages-table-patchwiz-dll-.md)
-   [TargetImages-Tabelle (Patchwiz.dll)](targetimages-table-patchwiz-dll-.md)

Die folgenden Datenbanktabellen sind optional:

-   [Tabelle "upgradedfiles" \_ (OptionalData) (Patchwiz.dll)](upgradedfiles-optionaldata-table-patchwiz-dll-.md)
-   [Familyfileranges-Tabelle (Patchwiz.dll)](familyfileranges-table-patchwiz-dll-.md)
-   [Targetfiles \_ (OptionalData-Tabelle) (Patchwiz.dll)](targetfiles-optionaldata-table-patchwiz-dll-.md)
-   [Externalfiles-Tabelle (Patchwiz.dll)](externalfiles-table-patchwiz-dll-.md)
-   [Tabelle "Upgrade dfilestoignore" (Patchwiz.dll)](upgradedfilestoignore-table-patchwiz-dll-.md)

Die folgende Tabelle ist in PCP-Dateien erforderlich, deren minimumrequirements dmsiversion 300 in der [Properties](properties-table-patchwiz-dll-.md) -Tabelle entspricht.

-   [Patchmetadata-Tabelle (Patchwiz.dll)](patchmetadata-table--patchwiz-dll-.md)

> [!Note]  
> Die Tabelle ist optional, wenn minimumrequirements dmsiversion nicht gleich 300 ist.

 

Die mit Windows Installer 3,0 veröffentlichte Version von Patchwiz.dll kann automatisch Informationen zur Patchsequenzierung generieren und Sie der [msipatchsequence-Tabelle](msipatchsequence-table.md) eines neuen Patches hinzufügen. Die [Tabelle "patchsequence](patchsequence-table--patchwiz-dll-.md) " kann verwendet werden, um patchsequenzierungs Informationen manuell der Tabelle "msipatchsequence" hinzuzufügen. Weitere Informationen finden Sie unter [Erstellen von Patchsequenzinformationen](generating-patch-sequence-information---patchwiz-dll-.md).

Ab Patchwiz.dll Version 2,0 können Sie die Geschwindigkeit der nachfolgenden Patcherstellung mithilfe von [patchinformations Caching (Patchwiz.dll)](patch-information-caching-patchwiz-dll-.md)erhöhen.

Wenn Sie öffentliche Symbole für die Ziel-und upgradeabbild-Binärdateien verwenden, können binäre patchgrößen um ungefähr eine Hälfte reduziert werden. Weitere Informationen finden Sie unter [Verwenden von Symbolen, um die binäre Patchgröße zu verringern](using-symbols-to-reduce-binary-patch-size.md).

Sie können angeben, dass bestimmte Bereiche der Zieldatei beim Patchen nicht überschrieben werden sollen und dass die Informationen in diesen Regionen beibehalten werden. Weitere Informationen finden Sie unter [Patchen ausgewählter Bereiche einer Datei](patching-selected-regions-of-a-file.md).

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Veröffentlichte Versionen, Tools und verteilbare Dateien](released-versions-tools-and-redistributables.md)
</dt> </dl>

 

 



