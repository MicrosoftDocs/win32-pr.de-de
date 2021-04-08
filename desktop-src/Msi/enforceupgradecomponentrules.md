---
description: Dies ist eine Computer spezifische System Richtlinie, mit der upgradekomponentenregeln bei kleinen Updates und geringfügigen Upgrades angewendet werden können.
ms.assetid: 0d39c059-d936-454c-aed8-efedd3da7473
title: Enforceupgradecomponentrules
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c5a2fc093c2f0beb4167374f93447d978bbca8eb
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "103959931"
---
# <a name="enforceupgradecomponentrules"></a>Enforceupgradecomponentrules

Dies ist eine Computer spezifische [System Richtlinie](system-policy.md) , mit der upgradekomponentenregeln bei [kleinen Updates](small-updates.md) und [geringfügigen Upgrades](minor-upgrades.md)angewendet werden können.

Legen Sie die enforceupgradecomponentrules-Richtlinie auf 1 fest, um upgradekomponentenregeln bei [kleinen Updates](small-updates.md) und [geringfügigen Upgrades](minor-upgrades.md) aller Produkte auf dem Computer anzuwenden. Legen Sie die Eigenschaft [**msienforceupgradecomponentrules**](msienforceupgradecomponentrules.md) in der Befehlszeile oder in der [Eigenschaften Tabelle](property-table.md)auf 1 fest, um die Regeln bei kleinen Updates und geringfügigen Upgrades eines bestimmten Produkts anzuwenden.

Wenn die Eigenschaft oder die Richtlinie auf 1 festgelegt wurde, können [kleine Updates](small-updates.md) und [kleinere Upgrades](minor-upgrades.md) fehlschlagen, da das Update versucht, Folgendes zu tun:

-   Fügen Sie am Anfang oder in der Mitte einer vorhandenen Funktionsstruktur ein neues Feature hinzu.

    Die neue Funktion muss als neue Blatt Funktion zu einer vorhandenen Funktionsstruktur hinzugefügt werden.

    In diesem Fall kann der [**ProductCode**](productcode.md) des Produkts geändert werden, und die Updates können als [großes Upgrade](major-upgrades.md)behandelt werden.

-   Entfernen einer Komponente aus einer Funktion.

    Dies kann auch vorkommen, wenn Sie die GUID einer Komponente ändern. Die von der ursprünglichen GUID identifizierte Komponente scheint entfernt zu werden, und die von der neuen GUID identifizierte Komponente wird als neue Komponente angezeigt.

    **Windows Installer 4,5 und höher:** Die Komponente kann mithilfe von Windows Installer 4,5 oder höher ordnungsgemäß entfernt werden, indem das **msidbcomponentattributesuninstallonabgelöst** -Attribut in der [Component-Tabelle](component-table.md) festgelegt oder die [**msiuninstallablösung dedcomponents**](msiuninstallsupersededcomponents.md) -Eigenschaft festgelegt wird.

    Alternativ kann der [**ProductCode**](productcode.md) des Produkts geändert werden, und die Updates können als [großes Upgrade](major-upgrades.md)behandelt werden.

## <a name="registry-key"></a>Registrierungsschlüssel

**HKEY \_ Software Richtlinien für lokale \_ Computer** \\  \\  \\ **Microsoft** \\ **Windows** \\ **Installer**

## <a name="data-type"></a>Datentyp

**REG \_ DWORD**

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Wird in Windows Installer 2,0 und früher nicht unterstützt.](not-supported-in-windows-installer-version-2-0.md)
</dt> </dl>

 

 



