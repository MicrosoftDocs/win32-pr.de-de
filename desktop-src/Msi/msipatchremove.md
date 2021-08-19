---
description: Die MSIPATCHREMOVE-Eigenschaft gibt die Liste der Patches an, die während einer Installation entfernt werden.
ms.assetid: 76f8daa9-d32c-4845-85bc-52b728f53d1f
title: MSIPATCHREMOVE-Eigenschaft
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1259e42bebdbf44473fb92c666cdb764580c2f54321e7f14d0293b1fa9928103
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118944508"
---
# <a name="msipatchremove-property"></a>MSIPATCHREMOVE-Eigenschaft

Die **MSIPATCHREMOVE-Eigenschaft** gibt die Liste der Patches an, die während einer Installation entfernt werden. Einzelne Patches in der Liste werden durch Semikolons getrennt und können durch die Patchcode-GUID oder den vollständigen Pfad zum Patch dargestellt werden. Die [**MsiRemovePatches-Funktion**](/windows/desktop/api/Msi/nf-msi-msiremovepatchesa) und die [**RemovePatches-Methode**](installer-removepatches.md) des [Installer-Objekts](installer-object.md) legen die **MSIPATCHREMOVE-Eigenschaft** fest.

Die **MSIPATCHREMOVE-Eigenschaft** kann in der Befehlszeile wie folgt festgelegt werden, um einen Patch zu entfernen.

**msiexec /i A: \\Example.msi MSIPATCHREMOVE=c: \\ patches \\ qfe1.msp;{ 0BBB87F1-3186-409C-8CDD-C88AA2A4A7E0}; {A86B443B-E3BF-4009-ADED-F716FC735858}/qb**

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

 

 




