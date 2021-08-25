---
title: ComeCollection.getByDriveSpecifier-Methode
description: Die getByDriveSpecifier-Methode ruft das einem bestimmten Laufwerkbuchstaben zugeordnete Cull-Objekt ab.
ms.assetid: 60626ffc-3d10-435b-8827-c5d7b6e02607
keywords:
- getByDriveSpecifier-Windows Media Player
- getByDriveSpecifier-Methode Windows Media Player , ComeCollection-Klasse
- Ccollection-Klasse Windows Media Player , getByDriveSpecifier-Methode
topic_type:
- apiref
api_name:
- CdromCollection.getByDriveSpecifier
api_location:
- wmp.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: fa5487b3a57fb1e7e4167561fcca08e10d6472182881fa221bd8e671bc814cc0
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119864090"
---
# <a name="cdromcollectiongetbydrivespecifier-method"></a>ComeCollection.getByDriveSpecifier-Methode

Die **getByDriveSpecifier-Methode** ruft das einem bestimmten Laufwerkbuchstaben zugeordnete **Cull-Objekt** ab.

## <a name="syntax"></a>Syntax


```JScript
retVal = CdromCollection.getByDriveSpecifier(
  driveSpecifier
)
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*driveSpecifier* \[ In\]
</dt> <dd>

**Eine Zeichenfolge,** die den Laufwerkbuchstaben gefolgt von einem Doppelpunkt (":") enthält.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Diese Methode gibt ein **Ckrony-Objekt** zurück.

## <a name="remarks"></a>Hinweise

Laufwerkbuchstaben müssen in der Form *X*: angegeben werden, wobei *X* den Laufwerkbuchstaben darstellt.

Um diese Methode verwenden zu können, ist Lesezugriff auf die Bibliothek erforderlich. Weitere Informationen finden Sie unter [Bibliothekszugriff.](library-access.md)

**Windows Media Player 10 Mobile:** Diese Methode wird nicht unterstützt.

## <a name="examples"></a>Beispiele

Im folgenden beispiel JScript *Ccollection verwendet.* **getByDriveSpecifier** zum Abrufen des **Czeichnerobjekts,** das einem vom Benutzer bereitgestellten Laufwerkbuchstaben entspricht. Für die Benutzereingabe wurde ein HTML-Textelement mit NAME = "MyText" erstellt. Das **Player-Objekt** wurde mit der ID = "Player" erstellt.


```JScript
// Store the drive letter provided by the user.
var DriveLetter = MyText.value;

// Append a colon to the drive letter to create a valid drive specifier.
DriveLetter += ":";

// Get the Cdrom object using the drive specifier.
var Drive = Player.cdRomCollection.getByDriveSpecifier(DriveLetter);

// Use the Cdrom object to open the drive door.
Drive.eject();
```



## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|------------------------------------------------------------------------------------|
| Version<br/> | Windows Media Player Version 7.0 oder höher.<br/>                              |
| DLL<br/>     | <dl> <dt>Wmp.dll</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**Come-Objekt**](cdrom-object.md)
</dt> <dt>

[**Ctive.eject**](cdrom-eject.md)
</dt> <dt>

[**Ccollection-Objekt**](cdromcollection-object.md)
</dt> <dt>

[**Einstellungen.mediaAccessRights**](settings-mediaaccessrights.md)
</dt> <dt>

[**Einstellungen.requestMediaAccessRights**](settings-requestmediaaccessrights.md)
</dt> </dl>

 

 





