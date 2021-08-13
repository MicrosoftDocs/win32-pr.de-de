---
title: MediaCollection.getByAuthor-Methode
description: Die getByAuthor-Methode ruft eine Wiedergabeliste der Medienelemente vom angegebenen Autor ab.
ms.assetid: 8f9b3ee3-a809-4d24-81ce-adad63e5347c
keywords:
- getByAuthor-Windows Media Player
- getByAuthor-Methode Windows Media Player , MediaCollection-Klasse
- MediaCollection-Klasse Windows Media Player , getByAuthor-Methode
topic_type:
- apiref
api_name:
- MediaCollection.getByAuthor
api_location:
- wmp.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 87989d38d49ff87ce26b7394f4ee79ef4bd7197cd0e35dcd5316797df401ba49
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118574627"
---
# <a name="mediacollectiongetbyauthor-method"></a>MediaCollection.getByAuthor-Methode

Die **getByAuthor-Methode** ruft eine Wiedergabeliste der Medienelemente vom angegebenen Autor ab.

## <a name="syntax"></a>Syntax


```JScript
retVal = MediaCollection.getByAuthor(
  author
)
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*author* \[ In\]
</dt> <dd>

**Eine Zeichenfolge,** die den Namen des Autors enthält.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Diese Methode gibt ein **Playlist-Objekt** zurück.

## <a name="remarks"></a>Hinweise

Um diese Methode verwenden zu können, ist Lesezugriff auf die Bibliothek erforderlich. Weitere Informationen finden Sie unter [Bibliothekszugriff.](library-access.md)

## <a name="examples"></a>Beispiele

Im folgenden beispiel JScript *MediaCollection verwendet.* **getByAuthor zum** Abrufen einer Wiedergabeliste von Medienelementen. Die Wiedergabeliste enthält Elemente, die mit dem vom Benutzer angegebenen Autor in einem HTML-TEXT-Eingabeelement namens GetAuthor übereinstimmen. Das **Player-Objekt** wurde mit der ID = "Player" erstellt.


```JScript
<!-- Use an HTML BUTTON element to create the playlist and play the media items. -->
<INPUT TYPE = "BUTTON"  NAME = "PlayAuthor"  
       ID = "PlayAuthor"  
       VALUE = "Play Author"

onClick = "
    /* Retrieve the author name text from the user. */
    var author = GetAuthor.value;

    /* Create the playlist by using getByAuthor. */
    var pl = Player.mediaCollection.getByAuthor(Author);

    /* Make the new playlist the current playlist. */
    Player.currentPlaylist = pl;

    /* Play the media items in the new playlist. */
               Player.controls.play();
">

```



## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|------------------------------------------------------------------------------------|
| Version<br/> | Windows Media Player Version 7.0 oder höher.<br/>                              |
| DLL<br/>     | <dl> <dt>Wmp.dll</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**MediaCollection-Objekt**](mediacollection-object.md)
</dt> <dt>

[**Playlist-Objekt**](playlist-object.md)
</dt> <dt>

[**Einstellungen.mediaAccessRights**](settings-mediaaccessrights.md)
</dt> <dt>

[**Einstellungen.requestMediaAccessRights**](settings-requestmediaaccessrights.md)
</dt> </dl>

 

 





