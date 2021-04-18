---
description: Die msipatchremove-Eigenschaft gibt die Liste der Patches an, die während einer Installation entfernt werden sollen.
ms.assetid: 76f8daa9-d32c-4845-85bc-52b728f53d1f
title: Msipatchremove (Eigenschaft)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ebf83583c5b15311e175e67a867ff5aca71394b7
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106352904"
---
# <a name="msipatchremove-property"></a>Msipatchremove (Eigenschaft)

Die **msipatchremove** -Eigenschaft gibt die Liste der Patches an, die während einer Installation entfernt werden sollen. Einzelne Patches in der Liste werden durch Semikolons getrennt und können durch die Patchcode-GUID oder den vollständigen Pfad zum Patch dargestellt werden. Die [**msiremovepatches**](/windows/desktop/api/Msi/nf-msi-msiremovepatchesa) -Funktion und die [**removepatches**](installer-removepatches.md) -Methode des [Installer](installer-object.md) -Objekts legen die **msipatchremove** -Eigenschaft fest.

Die **msipatchremove** -Eigenschaft kann wie folgt in der Befehlszeile festgelegt werden, um einen Patch zu entfernen.

**msiexec/i A: \\Example.msi msipatchremove = c: \\ Patches \\ qfe1. msp; { 0bbb87f1-3186-409c-8cdd-c88aa2a4a7e0}; {A86B443B-E3BF-4009-ADED-F716FC735858}/QB**

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

 

 




