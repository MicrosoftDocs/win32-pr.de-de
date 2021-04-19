---
description: Legen Sie die Eigenschaft msienforceupgradecomponentrules in der Befehlszeile oder in der Eigenschaften Tabelle auf 1 fest, um die upgradekomponentenregeln bei kleinen Updates und geringfügigen Upgrades eines bestimmten Produkts anzuwenden.
ms.assetid: 0c8424c7-ab9b-4a09-aaa8-6a3f44c2789f
title: Msienforceupgradecomponentrules (Eigenschaft)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 85d5946ba3a0001c988ddfe76eeaf95c008205b7
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106368575"
---
# <a name="msienforceupgradecomponentrules-property"></a>Msienforceupgradecomponentrules (Eigenschaft)

Legen Sie die Eigenschaft **msienforceupgradecomponentrules** in der Befehlszeile oder in der [Eigenschaften Tabelle](property-table.md) auf 1 fest, um die upgradekomponentenregeln bei [kleinen Updates](small-updates.md) und [geringfügigen Upgrades](minor-upgrades.md) eines bestimmten Produkts anzuwenden. Wenn Sie die Regeln bei kleinen Updates und geringfügigen Upgrades aller Produkte auf dem Computer anwenden möchten, legen Sie die [enforceupgradecomponentrules](enforceupgradecomponentrules.md) -Richtlinie auf 1 fest.

Wenn die Eigenschaft oder die Richtlinie auf 1 festgelegt ist, können [kleine Updates](small-updates.md) und [kleinere Upgrades](minor-upgrades.md) fehlschlagen, da das Update versucht, Folgendes auszuführen, das gegen die Regeln der upgradekomponente verstößt:

-   Fügen Sie am Anfang oder in der Mitte einer vorhandenen Funktionsstruktur ein neues Feature hinzu.

    Die neue Funktion muss als neue Blatt Funktion zu einer vorhandenen Funktionsstruktur hinzugefügt werden.

    In diesem Fall kann der [**ProductCode**](productcode.md) des Produkts geändert werden, und das Update kann als [großes Upgrade](major-upgrades.md)behandelt werden.

-   Entfernen einer Komponente aus einer Funktion.

    Dies kann auch vorkommen, wenn Sie die GUID einer Komponente ändern. Die von der ursprünglichen GUID identifizierte Komponente scheint entfernt zu werden, und die von der neuen GUID identifizierte Komponente wird als neue Komponente angezeigt.

    **Windows Installer 4,5 und höher:** Die Komponente kann mithilfe von Windows Installer 4,5 und höher ordnungsgemäß entfernt werden, indem das **msidbcomponentattributesuninstallonabgelöst** -Attribut in der [Component-Tabelle](component-table.md) festgelegt oder die [**msiuninstallablösung dedcomponents**](msiuninstallsupersededcomponents.md) -Eigenschaft festgelegt wird.

    Alternativ kann der [**ProductCode**](productcode.md) des Produkts geändert werden, und das Update kann als [großes Upgrade](major-upgrades.md)behandelt werden.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Version<br/> | Windows Installer 5,0 unter Windows Server 2012, Windows 8, Windows Server 2008 R2 oder Windows 7. Windows Installer 4,0 oder Windows Installer 4,5 unter Windows Server 2008 oder Windows Vista. Windows Installer 3,0 oder höher unter Windows Server 2003 oder Windows XP. Informationen zu den minimalen Windows-Service Pack, die für eine Windows Installer Version erforderlich sind, finden Sie in den [Windows Installer Run-Time Anforderungen](windows-installer-portal.md) .<br/> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[Eigenschaften](properties.md)
</dt> <dt>

[Wird in Windows Installer 2,0 und früher nicht unterstützt.](not-supported-in-windows-installer-version-2-0.md)
</dt> </dl>

 

 




