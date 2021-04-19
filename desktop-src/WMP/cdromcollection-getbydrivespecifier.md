---
title: Cdromcollection. getbydrivespecifier-Methode
description: Die getbydrivespecifier-Methode ruft das CDROM-Objekt ab, das einem bestimmten Laufwerk Buchstaben zugeordnet ist.
ms.assetid: 60626ffc-3d10-435b-8827-c5d7b6e02607
keywords:
- getbydrivespecifier-Methode, Windows Media Player
- getbydrivespecifier-Methode, Windows Media Player, cdromcollection-Klasse
- Cdromcollection-Klasse, Windows Media Player, getbydrivespecifier-Methode
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
ms.openlocfilehash: 807b44a7be97ac93b5b0f270c2d1723404887c9d
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106370916"
---
# <a name="cdromcollectiongetbydrivespecifier-method"></a>Cdromcollection. getbydrivespecifier-Methode

Die **getbydrivespecifier** -Methode ruft das **CDROM** -Objekt ab, das einem bestimmten Laufwerk Buchstaben zugeordnet ist.

## <a name="syntax"></a>Syntax


```JScript
retVal = CdromCollection.getByDriveSpecifier(
  driveSpecifier
)
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*drivespecifier* \[ in\]
</dt> <dd>

**Zeichenfolge** , die den Laufwerk Buchstaben enthält, gefolgt von einem Doppelpunkt (":").

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Diese Methode gibt ein **CDROM** -Objekt zurück.

## <a name="remarks"></a>Bemerkungen

Laufwerk Buchstaben müssen in der Form *x*: angegeben werden, wobei *x* den Laufwerk Buchstaben darstellt.

Um diese Methode verwenden zu können, ist Lesezugriff auf die Bibliothek erforderlich. Weitere Informationen finden Sie unter [Bibliotheks Zugriff](library-access.md).

**Windows Media Player 10 Mobile:** Diese Methode wird nicht unterstützt.

## <a name="examples"></a>Beispiele

Im folgenden JScript-Beispiel wird *cdromcollection* verwendet. **getbydrivespecifier** zum Abrufen des **CDROM** -Objekts, das einem vom Benutzer bereitgestellten Laufwerk Buchstaben entspricht. Für die Benutzereingabe wurde ein HTML-Textelement mit dem Namen "MyText" erstellt. Das **Player** -Objekt wurde mit ID = "Player" erstellt.


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
| Version<br/> | Windows Media Player Version 7,0 oder höher.<br/>                              |
| DLL<br/>     | <dl> <dt>Wmp.dll</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**Cdrom-Objekt**](cdrom-object.md)
</dt> <dt>

[**Cdrom. eject**](cdrom-eject.md)
</dt> <dt>

[**Cdromcollection-Objekt**](cdromcollection-object.md)
</dt> <dt>

[**Settings. mediaaccessrights**](settings-mediaaccessrights.md)
</dt> <dt>

[**Settings. requestmediaaccessrights**](settings-requestmediaaccessrights.md)
</dt> </dl>

 

 





