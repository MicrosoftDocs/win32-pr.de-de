---
title: Mediacollection. getbyattribute-Methode
description: Die getbyattribute-Methode ruft eine Wiedergabeliste von Medien Elementen ab, die einen angegebenen Wert für ein angegebenes Attribut enthalten.
ms.assetid: a89f9c52-c655-4420-858e-c0eed661856f
keywords:
- getbyattribute-Methode, Windows-Media Player
- getbyattribute-Methode, Windows Media Player, mediacollection-Klasse
- Mediacollection-Klasse, Windows Media Player, getbyattribute-Methode
topic_type:
- apiref
api_name:
- MediaCollection.getByAttribute
api_location:
- wmp.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 533823127364416f8f4492c82381e682173c5c78
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106370226"
---
# <a name="mediacollectiongetbyattribute-method"></a>Mediacollection. getbyattribute-Methode

Die **getbyattribute** -Methode ruft eine Wiedergabeliste von Medien Elementen ab, die einen angegebenen Wert für ein angegebenes Attribut enthalten.

## <a name="syntax"></a>Syntax


```JScript
retVal = MediaCollection.getByAttribute(
  attribute,
  value
)
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*Attribut* \[ in\]
</dt> <dd>

**Zeichenfolge** , die den Namen des zu durchsuchenden Attributs angibt. Informationen zu den Attributen, die von Windows Media Player unterstützt werden, finden Sie in der [Referenz](attribute-reference.md)zu Windows Media Player-Attributen.

</dd> <dt>

*Wert* \[ in\]
</dt> <dd>

Eine **Zeichenfolge** , die den Wert angibt, den das Attribut aufweisen sollte.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Diese Methode gibt ein **Wiedergabe** Listen Objekt zurück.

## <a name="remarks"></a>Bemerkungen

Diese Methode kann verwendet werden, um eine generische Abfrage für Medienelemente zu erstellen, die einem Wert für ein Attribut in der Datenbank entsprechen. Dies ist nützlich für benutzerdefinierte Attribute. Wenn das Attribut nicht vorhanden ist, führt dies zu einem Fehler.

Mit dieser Methode können Sie alle Medienelemente eines bestimmten Typs abrufen. Verwenden Sie den Attributnamen "MediaType" und einen der folgenden Werte:



| Wert    | BESCHREIBUNG                                                |
|----------|------------------------------------------------------------|
| Audio    | Musik und andere reine Audioelemente.                          |
| Abspielen | Wiedergabelisten, die als **Medien** Objekte dargestellt werden.                |
| radio    | Radio Station-Elemente. Wird nicht von Windows Media Player 10 verwendet.  |
| video    | Video Elemente.                                               |
| Foto    | Foto Elemente. Erfordert Windows Media Player 10.             |
| andere    | Andere Elemente, wie z. b. ASF-Dateien oder URLs für Streaming-Medien. |



 

Um diese Methode verwenden zu können, ist Lesezugriff auf die Bibliothek erforderlich. Weitere Informationen finden Sie unter [Bibliotheks Zugriff](library-access.md).

## <a name="examples"></a>Beispiele

Im folgenden JScript-Beispiel wird *mediacollection* verwendet. " **getbyattribute** ", um den gesamten Inhalt der Bibliothek von der Künstlerin mit dem Namen "48 drei Das **Player** -Objekt wurde mit ID = "Player" erstellt.


```JScript
// Get a playlist object filled with media items by a 
// particular artist.
var pl = Player.mediaCollection.getByAttribute("Artist", "Triode 48");

// Make the new playlist the current one.
Player.currentPlaylist = pl;

// Start Windows Media Player.
Player.controls.play();

```



## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|------------------------------------------------------------------------------------|
| Version<br/> | Windows Media Player Version 7,0 oder höher.<br/>                              |
| DLL<br/>     | <dl> <dt>Wmp.dll</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**Mediacollection-Objekt**](mediacollection-object.md)
</dt> <dt>

[**Wiedergabelisten Objekt**](playlist-object.md)
</dt> <dt>

[**Settings. mediaaccessrights**](settings-mediaaccessrights.md)
</dt> <dt>

[**Settings. requestmediaaccessrights**](settings-requestmediaaccessrights.md)
</dt> </dl>

 

 





