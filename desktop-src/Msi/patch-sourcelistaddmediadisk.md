---
description: 'Patch.SourceListAddMediaDisk-Methode: Die SourceListAddMediaDisk-Methode fügt dem Satz registrierter Datenträger einen Datenträger hinzu. Akzeptiert Diskid, VolumeLabel und DiskPrompt als Parameter. Diese Methode ruft für MsiSourceListAddMediaDisk auf.'
ms.assetid: 6feaf2d3-7e39-4e22-9e74-9a2f98369eac
title: Patch.SourceListAddMediaDisk-Methode
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
ms.openlocfilehash: 052831befb95976358b53d989db36d5b2fa43efe
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2021
ms.locfileid: "108084371"
---
# <a name="patchsourcelistaddmediadisk-method"></a>Patch.SourceListAddMediaDisk-Methode

Die **SourceListAddMediaDisk-Methode** fügt dem Satz registrierter Datenträger einen Datenträger hinzu. Akzeptiert *Diskid,* *VolumeLabel* und *DiskPrompt* als Parameter. Diese Methode ruft für [**MsiSourceListAddMediaDisk auf.**](/windows/desktop/api/Msi/nf-msi-msisourcelistaddmediadiska)

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

*Diskid* 
</dt> <dd>

Dieser Parameter gibt die ID des Datenträgers an, der hinzugefügt oder aktualisiert wird.

</dd> <dt>

*VolumeLabel* 
</dt> <dd>

Dieser Parameter gibt die Bezeichnung des Datenträgers an, der hinzugefügt oder aktualisiert wird. Ein Update überschreibt die vorhandene Volumebezeichnung in der Registrierung. Um nur die Datenträgeraufforderung zu ändern, erhalten Sie die vorhandene registrierte Volumebezeichnung, und geben Sie sie zusammen mit der eingabeaufforderung für den neuen Datenträger an. Eine NULL- oder leere Zeichenfolge registriert eine leere Zeichenfolge (0 Byte länge) als Volumebezeichnung.

</dd> <dt>

*DiskPrompt* 
</dt> <dd>

Dieser Parameter stellt die Datenträgeraufforderung des Datenträgers zur Eingabe, der hinzugefügt oder aktualisiert wird. Ein Update überschreibt die vorhandene Datenträgeraufforderung in der Registrierung. Um nur die Volumebezeichnung zu ändern, erhalten Sie die vorhandene Datenträgeraufforderung aus der Registrierung, und geben Sie die neue Volumebezeichnung an. Eine NULL- oder leere Zeichenfolge registriert eine leere Zeichenfolge (0 Byte lang) als Datenträgeraufforderung.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Diese Methode gibt keinen Wert zurück.

## <a name="requirements"></a>Anforderungen



| Anforderungen | Wert |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Version<br/> | Windows Installer 5.0 unter Windows Server 2012, Windows 8, Windows Server 2008 R2 oder Windows 7. Windows Installer 4.0 oder Windows Installer 4.5 unter Windows Server 2008 oder Windows Vista. Windows Installer 3.0 oder höher unter Windows Server 2003, Windows XP und Windows 2000<br/> |
| DLL<br/>     | <dl> <dt>Msi.dll</dt> </dl>                                                                                                                                                                                                   |
| IID<br/>     | IID \_ IPatch ist als 000C10A1-0000-0000-C000-000000000046 definiert.<br/>                                                                                                                                                                                                            |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[**Patch**](patch-object.md)
</dt> <dt>

[**MsiSourceListAddMediaDisk**](/windows/desktop/api/Msi/nf-msi-msisourcelistaddmediadiska)
</dt> <dt>

[In Windows Installer 2.0 und früher nicht unterstützt](not-supported-in-windows-installer-version-2-0.md)
</dt> </dl>

 

 




