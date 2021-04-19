---
description: Die sourcelistclearmediadisk-Methode des Patch-Objekts entfernt einen angegebenen Datenträger aus der Gruppe der registrierten Datenträger für einen Patch. Akzeptiert DiskId als Parameter. Diese Methode ruft msisourcelistclearmediadisk auf.
ms.assetid: fc52ecb9-2c79-497b-b551-0d3c4f584e86
title: Patch. sourcelistclearmediadisk-Methode
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Patch.SourceListClearMediaDisk
api_type:
- COM
api_location:
- Msi.dll
ms.openlocfilehash: 722b4573d89214312e77e4fde78e1905aefa885f
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106354071"
---
# <a name="patchsourcelistclearmediadisk-method"></a>Patch. sourcelistclearmediadisk-Methode

Die **sourcelistclearmediadisk** -Methode des [**Patch**](patch-object.md) -Objekts entfernt einen angegebenen Datenträger aus der Gruppe der registrierten Datenträger für einen Patch. Akzeptiert *DiskId* als Parameter. Diese Methode ruft [**msisourcelistclearmediadisk**](/windows/desktop/api/Msi/nf-msi-msisourcelistclearmediadiska)auf.

## <a name="syntax"></a>Syntax


```JScript
Patch.SourceListClearMediaDisk(
  Diskid
)
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*DiskId* 
</dt> <dd>

Dieser Parameter gibt die ID des zu entfernenden Datenträgers an.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Diese Methode gibt keinen Wert zurück.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Version<br/> | Windows Installer 5,0 unter Windows Server 2012, Windows 8, Windows Server 2008 R2 oder Windows 7. Windows Installer 4,0 oder Windows Installer 4,5 unter Windows Server 2008 oder Windows Vista. Windows Installer 3,0 oder höher unter Windows Server 2003, Windows XP und Windows 2000<br/> |
| DLL<br/>     | <dl> <dt>Msi.dll</dt> </dl>                                                                                                                                                                                                   |
| IID<br/>     | IID \_ iPatch ist definiert als 000c10a1-0000-0000-C000-000000000046<br/>                                                                                                                                                                                                            |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**Patch**](patch-object.md)
</dt> <dt>

[**Msisourcelistclearmediadisk**](/windows/desktop/api/Msi/nf-msi-msisourcelistclearmediadiska)
</dt> <dt>

[Wird in Windows Installer 2,0 und früher nicht unterstützt.](not-supported-in-windows-installer-version-2-0.md)
</dt> </dl>

 

 




