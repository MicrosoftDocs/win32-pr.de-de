---
title: MediaCollection.getByAttribute-Methode
description: Die getByAttribute-Methode ruft eine Wiedergabeliste von Medienelementen ab, die einen angegebenen Wert für ein angegebenes Attribut enthalten.
ms.assetid: a89f9c52-c655-4420-858e-c0eed661856f
keywords:
- getByAttribute-Windows Media Player
- getByAttribute-Methode Windows Media Player , MediaCollection-Klasse
- MediaCollection-Klasse Windows Media Player , getByAttribute-Methode
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
ms.openlocfilehash: f942f0718202d6c3e509b177c34c4c4be20c058b1e74991fa0ae89955d7711d8
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118996309"
---
# <a name="mediacollectiongetbyattribute-method"></a>MediaCollection.getByAttribute-Methode

Die **getByAttribute-Methode** ruft eine Wiedergabeliste von Medienelementen ab, die einen angegebenen Wert für ein angegebenes Attribut enthalten.

## <a name="syntax"></a>Syntax


```JScript
retVal = MediaCollection.getByAttribute(
  attribute,
  value
)
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*Attribut* \[ In\]
</dt> <dd>

**Eine Zeichenfolge,** die den Namen des zu durchsuchenden Attributs angibt. Informationen zu den attributes, die von Windows Media Player unterstützt werden, finden Sie in der Windows Media Player [Attribute Reference](attribute-reference.md).

</dd> <dt>

*value* \[ In\]
</dt> <dd>

**Eine Zeichenfolge,** die den Wert angibt, über den das Attribut verfügen soll.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Diese Methode gibt ein **Playlist-Objekt** zurück.

## <a name="remarks"></a>Hinweise

Diese Methode kann verwendet werden, um eine generische Abfrage für Medienelemente zu erstellen, die mit einem Wert für ein Attribut in der Datenbank übereinstimmen. Dies ist bei benutzerdefinierten Attributen nützlich. Wenn das Attribut nicht vorhanden ist, tritt ein Fehler auf.

Sie können diese Methode verwenden, um alle Medienelemente eines bestimmten Typs abzurufen. Verwenden Sie den Attributnamen "MediaType" und einen der folgenden Werte:



| Wert    | Beschreibung                                                |
|----------|------------------------------------------------------------|
| Audio    | Musik und andere Nur-Audio-Elemente.                          |
| Playlist | Wiedergabelisten, die als **Medienobjekte dargestellt** werden.                |
| radio    | Radiostationselemente. Wird von Windows Media Player 10 nicht verwendet.  |
| video    | Videoelemente.                                               |
| Foto    | Fotoelemente. Erfordert Windows Media Player 10.             |
| Sonstige    | Andere Elemente, z. B. ASF-Dateien oder URLs für Streamingmedien. |



 

Um diese Methode zu verwenden, ist Lesezugriff auf die Bibliothek erforderlich. Weitere Informationen finden Sie unter [Bibliothekszugriff.](library-access.md)

## <a name="examples"></a>Beispiele

Im folgenden beispiel JScript *MediaCollection verwendet.* **getByAttribute** zum Wiederspielen aller Inhalte aus der Bibliothek durch den Interpreten namens Attributde 48. Das **Player-Objekt** wurde mit der ID = "Player" erstellt.


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
| Version<br/> | Windows Media Player Version 7.0 oder höher.<br/>                              |
| DLL<br/>     | <dl> <dt>Wmp.dll</dt> </dl> |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[**MediaCollection-Objekt**](mediacollection-object.md)
</dt> <dt>

[**Wiedergabelistenobjekt**](playlist-object.md)
</dt> <dt>

[**Einstellungen.mediaAccessRights**](settings-mediaaccessrights.md)
</dt> <dt>

[**Einstellungen.requestMediaAccessRights**](settings-requestmediaaccessrights.md)
</dt> </dl>

 

 





