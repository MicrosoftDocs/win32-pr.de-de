---
description: Legen Sie die MSIUNINSTALLSUPERSEDEDCOMPONENTS-Eigenschaft in der Property-Tabelle oder in einer Befehlszeile auf 1 fest.
ms.assetid: ba9b1b2d-1667-48c8-8f1a-9958a1d170da
title: MSIUNINSTALLSUPERSEDEDCOMPONENTS (Eigenschaft)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ae30e142167e2d080fa4c74c046625338fbf92fd4476b0339d60f77e321ab54a
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118943941"
---
# <a name="msiuninstallsupersededcomponents-property"></a>MSIUNINSTALLSUPERSEDEDCOMPONENTS (Eigenschaft)

Legen Sie **die MSIUNINSTALLSUPERSEDEDCOMPONENTS-Eigenschaft** in der [Property-Tabelle](property-table.md) oder in einer Befehlszeile auf 1 fest. Wenn diese Eigenschaft auf 1 festgelegt wurde, bestimmt das Installationsprogramm, ob die Komponenten in ersetzten Patches redundant werden. Das Installationsprogramm kann die Registrierung redundanter Komponenten aufheben und deinstallieren, um zu verhindern, dass verwaiste Komponenten auf dem Computer zurückgelassen werden.

Das Festlegen dieser Eigenschaft wirkt sich auf die Komponenten in allen Patches aus, die ersetzt werden. Um diese Funktionalität für einzelne Komponenten zu aktivieren, verwenden Sie das **attribut msidbComponentAttributesUninstallOnSupersedence** in der [Component -Tabelle.](component-table.md)

**[Windows Installer 4.0 und früher:](not-supported-in-windows-installer-4-0.md)** Nicht unterstützt. Versionen vor Windows Installer 4.5 ignorieren die **MSIUNINSTALLSUPERSEDEDCOMPONENTS-Eigenschaft.**

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Version<br/> | Windows Installer 5.0 auf Windows Server 2012, Windows 8, Windows Server 2008 R2 oder Windows 7. Windows Installer 4.5 oder Windows Installer 4.5 unter Windows Vista, Windows XP, Windows Server 2003 und Windows Server 2008. Informationen zum [Windows Service](windows-installer-portal.md) Pack, das für eine Windows Installer-Version erforderlich ist, finden Sie unter Windows Installer Run-Time Anforderungen.<br/> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[Eigenschaften](properties.md)
</dt> </dl>

 

 




