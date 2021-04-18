---
description: Die sourcelistclearall-Methode des Patch-Objekts löscht die vollständige Quell Liste aller Quellen des angegebenen Typs für einen Patch. Akzeptiert den Typ als Parameter. Diese Methode ruft msisourcelistclearallex auf.
ms.assetid: 9458a3db-8eaa-4067-875f-8fac68bdf1f8
title: Patch. sourcelistclearall-Methode
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Patch.SourceListClearAll
api_type:
- COM
api_location:
- Msi.dll
ms.openlocfilehash: 31d7bceac706715099778cf84af2c3b2ec323880
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106351385"
---
# <a name="patchsourcelistclearall-method"></a>Patch. sourcelistclearall-Methode

Die **sourcelistclearall** -Methode des [**Patch**](patch-object.md) -Objekts löscht die vollständige Quell Liste aller Quellen des angegebenen Typs für einen Patch. Akzeptiert den *Typ* als Parameter. Diese Methode ruft [**msisourcelistclearallex**](/windows/desktop/api/Msi/nf-msi-msisourcelistclearallexa)auf.

## <a name="syntax"></a>Syntax


```JScript
Patch.SourceListClearAll(
  Type
)
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*Type* 
</dt> <dd>

Der Typ des Quell Typs, z. b. Netzwerk, URL oder Medien.

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

[**Msisourcelistclearallex**](/windows/desktop/api/Msi/nf-msi-msisourcelistclearallexa)
</dt> <dt>

[Wird in Windows Installer 2,0 und früher nicht unterstützt.](not-supported-in-windows-installer-version-2-0.md)
</dt> </dl>

 

 




