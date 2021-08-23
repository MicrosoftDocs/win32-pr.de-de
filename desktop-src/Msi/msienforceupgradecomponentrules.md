---
description: Legen Sie die MSIENFORCEUPGRADECOMPONENTRULES-Eigenschaft in der Befehlszeile oder in der Tabelle Eigenschaft auf 1 fest, um die Upgradekomponentenregeln bei kleinen Updates und kleineren Upgrades eines bestimmten Produkts anzuwenden.
ms.assetid: 0c8424c7-ab9b-4a09-aaa8-6a3f44c2789f
title: MSIENFORCEUPGRADECOMPONENTRULES-Eigenschaft
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 11535beb45ac521e59ec31c5e5231b23549394b75e5df2372ba4295471ea8008
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118945044"
---
# <a name="msienforceupgradecomponentrules-property"></a>MSIENFORCEUPGRADECOMPONENTRULES-Eigenschaft

Legen Sie die **MSIENFORCEUPGRADECOMPONENTRULES-Eigenschaft** in der Befehlszeile oder in der Tabelle [](small-updates.md) [Eigenschaft](property-table.md) [](minor-upgrades.md) auf 1 fest, um die Upgradekomponentenregeln bei kleinen Updates und kleineren Upgrades eines bestimmten Produkts anzuwenden. Um die Regeln bei kleinen Updates und kleineren Upgrades aller Produkte auf dem Computer anzuwenden, legen Sie die [Richtlinie EnforceUpgradeComponentRules](enforceupgradecomponentrules.md) auf 1 fest.

Wenn die Eigenschaft oder Richtlinie auf 1 [](minor-upgrades.md) festgelegt [ist,](small-updates.md) können kleine Updates und kleinere Upgrades fehlschlagen, da das Update versucht, folgende Schritte durchzuführen, die gegen die Upgradekomponentenregeln verstoßen:

-   Fügen Sie oben oder in der Mitte einer vorhandenen Featurestruktur ein neues Feature hinzu.

    Das neue Feature muss einer vorhandenen Featurestruktur als neues Blattfeature hinzugefügt werden.

    In diesem Fall kann [**der ProductCode**](productcode.md) des Produkts geändert werden, und das Update kann als größeres [Upgrade behandelt werden.](major-upgrades.md)

-   Entfernen sie eine Komponente aus einem Feature.

    Dies kann auch auftreten, wenn Sie die GUID einer Komponente ändern. Die von der ursprünglichen GUID identifizierte Komponente scheint entfernt zu werden, und die Durch die neue GUID identifizierte Komponente wird als neue Komponente angezeigt.

    **Windows Installer 4.5 und höher:** Die Komponente kann mithilfe von Windows Installer 4.5 und höher ordnungsgemäß entfernt werden, indem das **Attribut msidbComponentAttributesUninstallOnSupersedence** in der Komponententabelle oder die [**MSIUNINSTALLSUPERSEDEDCOMPONENTS-Eigenschaft**](msiuninstallsupersededcomponents.md) festgelegt wird. [](component-table.md)

    Alternativ kann der [**ProductCode**](productcode.md) des Produkts geändert werden, und das Update kann als größeres [Upgrade behandelt werden.](major-upgrades.md)

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Version<br/> | Windows Installer 5.0 auf Windows Server 2012, Windows 8, Windows Server 2008 R2 oder Windows 7. Windows Installer 4.0 oder Windows Installer 4.5 auf Windows Server 2008 oder Windows Vista. Windows Installer 3.0 oder höher auf Windows Server 2003 oder Windows XP. Informationen zum [Windows Service](windows-installer-portal.md) Pack, das für eine Windows Installer-Version erforderlich ist, finden Sie unter Windows Installer Run-Time Anforderungen.<br/> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[Eigenschaften](properties.md)
</dt> <dt>

[Nicht unterstützt in Windows Installer 2.0 und früher](not-supported-in-windows-installer-version-2-0.md)
</dt> </dl>

 

 




