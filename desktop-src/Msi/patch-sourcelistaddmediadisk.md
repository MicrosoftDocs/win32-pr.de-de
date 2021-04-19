---
description: Die sourcelistaddmediadisk-Methode fügt dem Satz registrierter Datenträger einen Datenträger hinzu. Akzeptiert DiskId, VolumeLabel und diskprompt als Parameter. Diese Methode ruft auf msisourcelistaddmediadisk auf.
ms.assetid: 6feaf2d3-7e39-4e22-9e74-9a2f98369eac
title: Patch. sourcelistaddmediadisk-Methode
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Patch.SourceListAddMediaDisk
api_type:
- COM
api_location:
- Msi.dll
ms.openlocfilehash: a7c74ccdfb90a0cb365e6110defc9b60dac1f471
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106366727"
---
# <a name="patchsourcelistaddmediadisk-method"></a>Patch. sourcelistaddmediadisk-Methode

Die **sourcelistaddmediadisk** -Methode fügt dem Satz registrierter Datenträger einen Datenträger hinzu. Akzeptiert *DiskId*, *VolumeLabel* und *diskprompt* als Parameter. Diese Methode ruft auf [**msisourcelistaddmediadisk**](/windows/desktop/api/Msi/nf-msi-msisourcelistaddmediadiska)auf.

## <a name="syntax"></a>Syntax


```JScript
Patch.SourceListAddMediaDisk(
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

Dieser Parameter gibt die Bezeichnung des Datenträgers an, der hinzugefügt oder aktualisiert wird. Ein Update überschreibt die vorhandene Volumebezeichnung in der Registrierung. Wenn Sie nur die Eingabeaufforderung für den Datenträger ändern möchten, können Sie die vorhandene registrierte Volumebezeichnung sowie die neue Eingabeaufforderung für den Datenträger angeben. Eine NULL-Zeichenfolge oder eine leere Zeichenfolge registriert eine leere Zeichenfolge (0 Byte Länge) als Volumebezeichnung.

</dd> <dt>

*Diskprompt* 
</dt> <dd>

Dieser Parameter gibt die Eingabeaufforderung des Datenträgers an, der hinzugefügt oder aktualisiert wird. Ein Update überschreibt die vorhandene Datenträger Aufforderung in der Registrierung. Um die Volumebezeichnung nur zu ändern, müssen Sie die vorhandene Datenträger Aufforderung aus der Registrierung erhalten und die neue Volumebezeichnung bereitstellen. Eine NULL-Zeichenfolge oder eine leere Zeichenfolge registriert eine leere Zeichenfolge (0 Byte Länge) als Eingabeaufforderung für den Datenträger.

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

[**Msisourcelistaddmediadisk**](/windows/desktop/api/Msi/nf-msi-msisourcelistaddmediadiska)
</dt> <dt>

[Wird in Windows Installer 2,0 und früher nicht unterstützt.](not-supported-in-windows-installer-version-2-0.md)
</dt> </dl>

 

 




