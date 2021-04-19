---
description: Legen Sie in der Eigenschaften Tabelle oder in einer Befehlszeile die msiuninstallablösung dedcomponents-Eigenschaft auf 1 fest.
ms.assetid: ba9b1b2d-1667-48c8-8f1a-9958a1d170da
title: Msiuninstallablösung dedcomponents (Eigenschaft)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: fcc930a258d8faebe71480f466f2b097fe1eda68
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106370252"
---
# <a name="msiuninstallsupersededcomponents-property"></a>Msiuninstallablösung dedcomponents (Eigenschaft)

Legen Sie in der [Eigenschaften Tabelle](property-table.md) oder in einer Befehlszeile die **msiuninstallablösung dedcomponents** -Eigenschaft auf 1 fest. Wenn diese Eigenschaft auf 1 festgelegt wurde, ermittelt das Installationsprogramm, ob die Komponenten in abgelösten Patches zu redundant werden. Das Installationsprogramm kann die Registrierung von redundanten Komponenten aufheben und deinstallieren, um zu verhindern, dass verwaiste Komponenten auf dem Computer bleiben

Das Festlegen dieser Eigenschaft wirkt sich auf die Komponenten in allen Patches aus, die abgelöst werden. Um diese Funktionalität für einzelne Komponenten zu aktivieren, verwenden Sie das **msidbcomponentattributesuninstallonabgelöst** -Attribut in der [Component-Tabelle](component-table.md).

**[Windows Installer 4,0 und früher](not-supported-in-windows-installer-4-0.md):** Nicht unterstützt. In früheren Versionen als Windows Installer 4,5 wird die **msiuninstallablösen** -Eigenschaft ignoriert.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Version<br/> | Windows Installer 5,0 unter Windows Server 2012, Windows 8, Windows Server 2008 R2 oder Windows 7. Windows Installer 4,5 oder Windows Installer 4,5 unter Windows Vista, Windows XP, Windows Server 2003 und Windows Server 2008. Informationen zu den minimalen Windows-Service Pack, die für eine Windows Installer Version erforderlich sind, finden Sie in den [Windows Installer Run-Time Anforderungen](windows-installer-portal.md) .<br/> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[Eigenschaften](properties.md)
</dt> </dl>

 

 




