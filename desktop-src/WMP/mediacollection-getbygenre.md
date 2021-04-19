---
title: Mediacollection. getbygenre-Methode
description: Die getbygenre-Methode ruft eine Wiedergabeliste der Medienelemente mit dem angegebenen Genre ab.
ms.assetid: 022a0c52-93e1-4ab4-90a7-632bcd6fc004
keywords:
- getbygenre-Methode, Windows-Media Player
- getbygenre-Methode Windows Media Player, mediacollection-Klasse
- Mediacollection-Klasse, Windows Media Player, getbygenre-Methode
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
ms.openlocfilehash: 4b73cd7fe9bb3efa9115e2ba5d01b6d12c89898d
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106354127"
---
# <a name="mediacollectiongetbygenre-method"></a>Mediacollection. getbygenre-Methode

Die **getbygenre** -Methode ruft eine Wiedergabeliste der Medienelemente mit dem angegebenen Genre ab.

## <a name="syntax"></a>Syntax


```JScript
retVal = MediaCollection.getByGenre(
  genre
)
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*Genre* \[ in\]
</dt> <dd>

**Zeichenfolge** , die den Namen des Genres enthält.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Diese Methode gibt ein **Wiedergabe** Listen Objekt zurück.

## <a name="remarks"></a>Bemerkungen

Um diese Methode verwenden zu können, ist Lesezugriff auf die Bibliothek erforderlich. Weitere Informationen finden Sie unter [Bibliotheks Zugriff](library-access.md).

## <a name="examples"></a>Beispiele

Im folgenden JScript-Beispiel wird *mediacollection* verwendet. **getbygenre** zum Abrufen einer Wiedergabeliste von Medien Elementen. Die Wiedergabeliste enthält Elemente mit dem vom Benutzer angegebenen Genre in einem HTML-Text Eingabe Element mit dem Namen getgenre. Das **Player** -Objekt wurde mit ID = "Player" erstellt.


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

 

 





