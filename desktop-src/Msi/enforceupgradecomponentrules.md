---
description: Dies ist eine Systemrichtlinie pro Computer, die verwendet werden kann, um Upgradekomponentenregeln bei kleinen Updates und kleineren Upgrades anzuwenden.
ms.assetid: 0d39c059-d936-454c-aed8-efedd3da7473
title: EnforceUpgradeComponentRules
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 882d7df0e794dfb89ab2211db1fada576bd6e056972810d582385c1404e625a8
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "120086070"
---
# <a name="enforceupgradecomponentrules"></a>EnforceUpgradeComponentRules

Dies ist eine computerspezifische [Systemrichtlinie,](system-policy.md) die verwendet [](small-updates.md) werden kann, um Upgradekomponentenregeln bei kleinen Updates und kleineren [Upgrades anzuwenden.](minor-upgrades.md)

Legen Sie die Richtlinie EnforceUpgradeComponentRules auf 1 fest, um Upgradekomponentenregeln bei kleinen Updates und kleineren Upgrades aller Produkte auf dem Computer anzuwenden. [](small-updates.md) [](minor-upgrades.md) Um die Regeln bei kleinen Updates und kleineren Upgrades eines bestimmten Produkts anzuwenden, legen Sie die [**MSIENFORCEUPGRADECOMPONENTRULES-Eigenschaft**](msienforceupgradecomponentrules.md) in der Befehlszeile oder in der Tabelle Eigenschaft auf 1 [fest.](property-table.md)

Wenn die Eigenschaft oder Richtlinie auf 1 [](minor-upgrades.md) festgelegt [wurde,](small-updates.md) können kleine Updates und kleinere Upgrades fehlschlagen, da das Update folgende Schritte versucht:

-   Fügen Sie oben oder in der Mitte einer vorhandenen Featurestruktur ein neues Feature hinzu.

    Das neue Feature muss einer vorhandenen Featurestruktur als neues Blattfeature hinzugefügt werden.

    In diesem Fall kann [**der ProductCode**](productcode.md) des Produkts geändert werden, und die Updates können als größeres [Upgrade behandelt werden.](major-upgrades.md)

-   Entfernen sie eine Komponente aus einem Feature.

    Dies kann auch auftreten, wenn Sie die GUID einer Komponente ändern. Die von der ursprünglichen GUID identifizierte Komponente scheint entfernt zu werden, und die Durch die neue GUID identifizierte Komponente wird als neue Komponente angezeigt.

    **Windows Installer 4.5 und höher:** Die Komponente kann mithilfe von Windows Installer 4.5 oder höher ordnungsgemäß entfernt werden, indem das **Attribut msidbComponentAttributesUninstallOnSupersedence** in der Component-Tabelle oder die [**MSIUNINSTALLSUPERSEDEDCOMPONENTS-Eigenschaft**](msiuninstallsupersededcomponents.md) festgelegt wird. [](component-table.md)

    Alternativ kann der [**ProductCode**](productcode.md) des Produkts geändert werden, und die Updates können als größeres [Upgrade behandelt werden.](major-upgrades.md)

## <a name="registry-key"></a>Registrierungsschlüssel

**HKEY \_ LOCAL \_** \\ **MACHINE-Softwarerichtlinien** \\  \\ **Microsoft** \\ **Windows** \\ **Installer**

## <a name="data-type"></a>Datentyp

**REG \_ DWORD**

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Nicht unterstützt in Windows Installer 2.0 und früher](not-supported-in-windows-installer-version-2-0.md)
</dt> </dl>

 

 



