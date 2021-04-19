---
description: Die sourcelistclearmediadisk-Methode des Product-Objekts entfernt einen angegebenen Datenträger aus der Gruppe der registrierten Datenträger für ein Produkt. Akzeptiert DiskId als Parameter. Diese Methode ruft msisourcelistclearmediadisk auf.
ms.assetid: 7eec644e-5127-4c17-a8bd-6b0eb091c8aa
title: Product. sourcelistclearmediadisk-Methode
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Product.SourceListClearMediaDisk
api_type:
- COM
api_location:
- Msi.dll
ms.openlocfilehash: a607591f45208854118b0f97849cd7072e484bee
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106366933"
---
# <a name="productsourcelistclearmediadisk-method"></a>Product. sourcelistclearmediadisk-Methode

Die **sourcelistclearmediadisk** -Methode des [**Product**](product-object.md) -Objekts entfernt einen angegebenen Datenträger aus der Gruppe der registrierten Datenträger für ein Produkt. Akzeptiert *DiskId* als Parameter. Diese Methode ruft [**msisourcelistclearmediadisk**](/windows/desktop/api/Msi/nf-msi-msisourcelistclearmediadiska)auf.

## <a name="syntax"></a>Syntax


```JScript
Product.SourceListClearMediaDisk(
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
| IID<br/>     | IID \_ iproduct ist definiert als 000c10a0-0000-0000-C000-000000000046<br/>                                                                                                                                                                                                          |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**Product**](product-object.md)
</dt> <dt>

[**Msisourcelistclearmediadisk**](/windows/desktop/api/Msi/nf-msi-msisourcelistclearmediadiska)
</dt> <dt>

[Wird in Windows Installer 2,0 und früher nicht unterstützt.](not-supported-in-windows-installer-version-2-0.md)
</dt> </dl>

 

 




