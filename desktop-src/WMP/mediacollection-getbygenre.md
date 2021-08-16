---
title: MediaCollection.getByGenre-Methode
description: Die getByGenre-Methode ruft eine Wiedergabeliste der Medienelemente mit dem angegebenen Genre ab.
ms.assetid: 022a0c52-93e1-4ab4-90a7-632bcd6fc004
keywords:
- getByGenre-Methode Windows Media Player
- getByGenre-Methode Windows Media Player , MediaCollection-Klasse
- MediaCollection-Klasse Windows Media Player , getByGenre-Methode
topic_type:
- apiref
api_name:
- MediaCollection.getByGenre
api_location:
- wmp.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 06df514e7ed399e73f6778912df32a4ed0be57a90039fe867c75cf31a3eec807
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119135013"
---
# <a name="mediacollectiongetbygenre-method"></a>MediaCollection.getByGenre-Methode

Die **getByGenre-Methode** ruft eine Wiedergabeliste der Medienelemente mit dem angegebenen Genre ab.

## <a name="syntax"></a>Syntax


```JScript
retVal = MediaCollection.getByGenre(
  genre
)
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*Genre* \[ In\]
</dt> <dd>

**Zeichenfolge,** die den Namen des Genres enthält.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Diese Methode gibt ein **Playlist-Objekt** zurück.

## <a name="remarks"></a>Hinweise

Um diese Methode zu verwenden, ist Lesezugriff auf die Bibliothek erforderlich. Weitere Informationen finden Sie unter [Bibliothekszugriff.](library-access.md)

## <a name="examples"></a>Beispiele

Im folgenden JScript Beispiel wird *MediaCollection* verwendet. **getByGenre,** um eine Wiedergabeliste von Medienelementen abzurufen. Die Wiedergabeliste enthält Elemente mit dem Genre, das vom Benutzer in einem HTML TEXT-Eingabeelement mit dem Namen GetGenre angegeben wird. Das **Player-Objekt** wurde mit der ID = "Player" erstellt.


```JScript
<!-- Use an HTML BUTTON element to create the playlist and play 
the media items. -->
<INPUT TYPE = "BUTTON"  
       NAME = "PlayGenre"  
       ID = "PlayGenre"  
       VALUE = "Play Genre"

onClick = "
    /* Retrieve the genre text from the user. */
    var genre = GetGenre.value;

    /* Create the playlist using getByGenre. */
    var pl = Player.mediaCollection.getByGenre(genre);

    /* Make the new playlist the current playlist. */
    Player.currentPlaylist = pl;

    /* Play the digital media item in the new playlist. */
    Player.controls.play();
">

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

 

 





