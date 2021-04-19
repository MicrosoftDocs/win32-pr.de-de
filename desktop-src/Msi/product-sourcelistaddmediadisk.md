---
description: Die sourcelistaddmediadisk-Methode fügt dem Satz registrierter Datenträger einen Datenträger hinzu. Akzeptiert DiskId, VolumeLabel und diskprompt als Parameter. Diese Methode ruft auf msisourcelistaddmediadisk auf.
ms.assetid: 19cb6884-2191-4da3-a6d2-8874564be67d
title: Product. sourcelistaddmediadisk-Methode
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Product.SourceListAddMediaDisk
api_type:
- COM
api_location:
- Msi.dll
ms.openlocfilehash: d2f81b21570d708f361e45be7f6f42a93fd0d335
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106369597"
---
# <a name="productsourcelistaddmediadisk-method"></a>Product. sourcelistaddmediadisk-Methode

Die **sourcelistaddmediadisk** -Methode fügt dem Satz registrierter Datenträger einen Datenträger hinzu. Akzeptiert *DiskId*, *VolumeLabel* und *diskprompt* als Parameter. Diese Methode ruft auf [**msisourcelistaddmediadisk**](/windows/desktop/api/Msi/nf-msi-msisourcelistaddmediadiska)auf.

## <a name="syntax"></a>Syntax


```JScript
Product.SourceListAddMediaDisk(
  Diskid,
  VolumeLabel,
  DiskPrompt
)
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*DiskId* 
</dt> <dd>

Dieser Parameter gibt die ID des Datenträgers an, der hinzugefügt oder aktualisiert wird.

</dd> <dt>

*VolumeLabel* 
</dt> <dd>

Dieser Parameter gibt die Bezeichnung des Datenträgers an, der hinzugefügt oder aktualisiert wird. Ein Update überschreibt die vorhandene Volumebezeichnung in der Registrierung. Wenn Sie nur die Eingabeaufforderung für den Datenträger ändern möchten, können Sie die vorhandene registrierte Volumebezeichnung sowie die neue Eingabeaufforderung für den Datenträger angeben. Eine leere Zeichenfolge für diesen Parameter registriert eine leere Zeichenfolge (0 Byte Länge) als Volumebezeichnung.

</dd> <dt>

*Diskprompt* 
</dt> <dd>

Dieser Parameter gibt die Eingabeaufforderung des Datenträgers an, der hinzugefügt oder aktualisiert wird. Ein Update überschreibt die vorhandene Datenträger Aufforderung in der Registrierung. Um die Volumebezeichnung nur zu ändern, müssen Sie die vorhandene Datenträger Aufforderung aus der Registrierung erhalten und die neue Volumebezeichnung bereitstellen. Eine leere Zeichenfolge für diesen Parameter registriert eine leere Zeichenfolge (0 Byte Länge) als Eingabeaufforderung für den Datenträger.

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

[**Msisourcelistaddmediadisk**](/windows/desktop/api/Msi/nf-msi-msisourcelistaddmediadiska)
</dt> <dt>

[Wird in Windows Installer 2,0 und früher nicht unterstützt.](not-supported-in-windows-installer-version-2-0.md)
</dt> </dl>

 

 




