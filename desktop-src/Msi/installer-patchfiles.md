---
description: Die PATCHFILES-Eigenschaft gibt ein stringlist-Objekt zurück, das eine Liste von Dateien enthält, die durch die bereitgestellte Liste der Patches aktualisiert werden können.
ms.assetid: 14549847-8558-4a9a-9ad5-3575c3f4391e
title: Installer. PATCHFILES (Eigenschaft)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Installer.PatchFiles
api_type:
- COM
api_location:
- Msi.dll
ms.openlocfilehash: 43491bb384e6f95b31b4e7ae12e5fd32f4fbe8b6
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106358774"
---
# <a name="installerpatchfiles-property"></a>Installer. PATCHFILES (Eigenschaft)

Die **PATCHFILES** -Eigenschaft gibt ein [**stringlist**](stringlist-object.md) -Objekt zurück, das eine Liste von Dateien enthält, die durch die bereitgestellte Liste der Patches aktualisiert werden können. Diese Eigenschaft ruft [**msigetpatchfilelist**](/windows/desktop/api/Msi/nf-msi-msigetpatchfilelista)auf. Weitere Informationen zum Verwenden der **PATCHFILES** -Eigenschaft finden Sie [unter Auflisten der Dateien, die aktualisiert werden können](listing-the-files-that-can-be-updated.md).

Diese Eigenschaft ist schreibgeschützt.

## <a name="syntax"></a>Syntax


```JScript
propVal = Installer.PatchFiles
```



## <a name="property-value"></a>Eigenschaftswert

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Version<br/> | Windows Installer 5,0 unter Windows Server 2012, Windows 8, Windows Server 2008 R2 oder Windows 7. Windows Installer 4,0 oder Windows Installer 4,5 unter Windows Server 2008 oder Windows Vista. Windows Installer 4,5 unter Windows Server 2003 und Windows XP<br/> |
| DLL<br/>     | <dl> <dt>Msi.dll</dt> </dl>                                                                                                                                                                           |
| IID<br/>     | IID \_ iinstaller ist definiert als 000c1090-0000-0000-C000-000000000046<br/>                                                                                                                                                                                |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**Installer-Objekt**](installer-object.md)
</dt> <dt>

[Wird in Windows Installer 3,1 und früheren Versionen nicht unterstützt.](not-supported-in-windows-installer-version-3-1.md)
</dt> </dl>

 

 




