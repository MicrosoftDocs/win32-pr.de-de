---
description: Die patchesex-Eigenschaft gibt ein RecordList-Objekt zurück, das die Liste der Patches auflistet.
ms.assetid: 14fa0a1b-325c-42b7-b023-cd168e0615cc
title: Installer. patchesex-Eigenschaft
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Installer.PatchesEx
api_type:
- COM
api_location:
- Msi.dll
ms.openlocfilehash: e615a9d17dbf1a40332afc5b49b3c0c5446963ee
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106368308"
---
# <a name="installerpatchesex-property"></a>Installer. patchesex-Eigenschaft

Die **patchesex** -Eigenschaft gibt ein [**RecordList**](recordlist-object.md) -Objekt zurück, das die Liste der Patches auflistet. Diese Eigenschaft ruft [**msienumschlag Patch esex**](/windows/desktop/api/Msi/nf-msi-msienumpatchesexa)auf.

Diese Eigenschaft ist schreibgeschützt.

## <a name="syntax"></a>Syntax


```JScript
propVal = Installer.PatchesEx
```



## <a name="property-value"></a>Eigenschaftswert

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Version<br/> | Windows Installer 5,0 unter Windows Server 2012, Windows 8, Windows Server 2008 R2 oder Windows 7. Windows Installer 4,0 oder Windows Installer 4,5 unter Windows Server 2008 oder Windows Vista. Windows Installer 3,0 oder höher unter Windows Server 2003 oder Windows XP.<br/> |
| DLL<br/>     | <dl> <dt>Msi.dll</dt> </dl>                                                                                                                                                                                    |
| IID<br/>     | IID \_ iinstaller ist definiert als 000c1090-0000-0000-C000-000000000046<br/>                                                                                                                                                                                         |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**Installationsprogramm**](installer-object.md)
</dt> <dt>

[**Msienum patchesex**](/windows/desktop/api/Msi/nf-msi-msienumpatchesexa)
</dt> <dt>

[**Patch**](patch-object.md)
</dt> <dt>

[Wird in Windows Installer 2,0 und früher nicht unterstützt.](not-supported-in-windows-installer-version-2-0.md)
</dt> </dl>

 

 




