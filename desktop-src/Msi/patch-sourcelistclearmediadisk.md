---
description: Die SourceListClearMediaDisk-Methode des Patch-Objekts entfernt einen angegebenen Datenträger aus dem Satz registrierter Datenträger für einen Patch. Akzeptiert Diskid als Parameter. Diese Methode ruft MsiSourceListClearMediaDisk auf.
ms.assetid: fc52ecb9-2c79-497b-b551-0d3c4f584e86
title: Patch.SourceListClearMediaDisk-Methode
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
ms.openlocfilehash: 73f3303ae8521dd5fb87f17a685189770d17de2d0289f0801b81fef5332b5076
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119558540"
---
# <a name="patchsourcelistclearmediadisk-method"></a>Patch.SourceListClearMediaDisk-Methode

Die **SourceListClearMediaDisk-Methode** des [**Patch-Objekts**](patch-object.md) entfernt einen angegebenen Datenträger aus dem Satz registrierter Datenträger für einen Patch. Akzeptiert *Diskid* als Parameter. Diese Methode ruft [**MsiSourceListClearMediaDisk auf.**](/windows/desktop/api/Msi/nf-msi-msisourcelistclearmediadiska)

## <a name="syntax"></a>Syntax


```JScript
Patch.SourceListClearMediaDisk(
  Diskid
)
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*Diskid* 
</dt> <dd>

Dieser Parameter gibt die ID des zu entfernenden Datenträgers an.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Diese Methode gibt keinen Wert zurück.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Version<br/> | Windows Installer 5.0 auf Windows Server 2012, Windows 8, Windows Server 2008 R2 oder Windows 7. Windows Installer 4.0 oder Windows Installer 4.5 auf Windows Server 2008 oder Windows Vista. Windows Installer 3.0 oder höher auf Windows Server 2003, Windows XP und Windows 2000<br/> |
| DLL<br/>     | <dl> <dt>Msi.dll</dt> </dl>                                                                                                                                                                                                   |
| IID<br/>     | IID IPatch ist als \_ 000C10A1-0000-0000-C000-00000000046 definiert.<br/>                                                                                                                                                                                                            |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**Patch**](patch-object.md)
</dt> <dt>

[**MsiSourceListClearMediaDisk**](/windows/desktop/api/Msi/nf-msi-msisourcelistclearmediadiska)
</dt> <dt>

[Nicht unterstützt in Windows Installer 2.0 und früher](not-supported-in-windows-installer-version-2-0.md)
</dt> </dl>

 

 




