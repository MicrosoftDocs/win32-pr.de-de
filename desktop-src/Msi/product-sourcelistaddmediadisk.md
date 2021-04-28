---
description: 'Product.SourceListAddMediaDisk-Methode: Die SourceListAddMediaDisk-Methode fügt dem Satz registrierter Datenträger einen Datenträger hinzu. Akzeptiert Diskid, VolumeLabel und DiskPrompt als Parameter. Diese Methode ruft für MsiSourceListAddMediaDisk auf.'
ms.assetid: 19cb6884-2191-4da3-a6d2-8874564be67d
title: Product.SourceListAddMediaDisk-Methode
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
ms.openlocfilehash: 4cf5fac906b048930b47a07acb2c04c7243d5bbf
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2021
ms.locfileid: "108113578"
---
# <a name="productsourcelistaddmediadisk-method"></a>Product.SourceListAddMediaDisk-Methode

Die **SourceListAddMediaDisk-Methode** fügt dem Satz registrierter Datenträger einen Datenträger hinzu. Akzeptiert *Diskid,* *VolumeLabel* und *DiskPrompt* als Parameter. Diese Methode ruft [**für MsiSourceListAddMediaDisk**](/windows/desktop/api/Msi/nf-msi-msisourcelistaddmediadiska)auf.

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

*Diskid* 
</dt> <dd>

Dieser Parameter stellt die ID des Datenträgers bereit, der hinzugefügt oder aktualisiert wird.

</dd> <dt>

*VolumeLabel* 
</dt> <dd>

Dieser Parameter stellt die Bezeichnung des Datenträgers bereit, der hinzugefügt oder aktualisiert wird. Ein Update überschreibt die vorhandene Volumebezeichnung in der Registrierung. Um nur die Datenträgereingabeaufforderung zu ändern, erhalten Sie die vorhandene Bezeichnung für registrierte Volumes, und geben Sie sie zusammen mit der eingabeaufforderung für den neuen Datenträger an. Eine leere Zeichenfolge für diesen Parameter registriert eine leere Zeichenfolge (0 Byte lang) als Volumebezeichnung.

</dd> <dt>

*DiskPrompt* 
</dt> <dd>

Dieser Parameter stellt die Eingabeaufforderung des Datenträgers bereit, der hinzugefügt oder aktualisiert wird. Ein Update überschreibt die vorhandene Datenträgeraufforderung in der Registrierung. Um nur die Volumebezeichnung zu ändern, erhalten Sie die vorhandene Datenträgeraufforderung aus der Registrierung, und geben Sie die neue Volumebezeichnung an. Eine leere Zeichenfolge für diesen Parameter registriert eine leere Zeichenfolge (0 Byte lang) als Eingabeaufforderung für den Datenträger.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Diese Methode gibt keinen Wert zurück.

## <a name="requirements"></a>Anforderungen



| Anforderungen | Wert |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Version<br/> | Windows Installer 5.0 unter Windows Server 2012, Windows 8, Windows Server 2008 R2 oder Windows 7. Windows Installer 4.0 oder Windows Installer 4.5 unter Windows Server 2008 oder Windows Vista. Windows Installer 3.0 oder höher unter Windows Server 2003, Windows XP und Windows 2000<br/> |
| DLL<br/>     | <dl> <dt>Msi.dll</dt> </dl>                                                                                                                                                                                                   |
| IID<br/>     | IID IProduct ist als \_ 000C10A0-0000-0000-C000-00000000046 definiert.<br/>                                                                                                                                                                                                          |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[**Produkt**](product-object.md)
</dt> <dt>

[**MsiSourceListAddMediaDisk**](/windows/desktop/api/Msi/nf-msi-msisourcelistaddmediadiska)
</dt> <dt>

[In Version Windows Installer 2.0 und früher nicht unterstützt](not-supported-in-windows-installer-version-2-0.md)
</dt> </dl>

 

 




