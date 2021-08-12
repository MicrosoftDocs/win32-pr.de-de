---
title: MediaCollection.getBy Auflistung-Methode
description: Die GetBy -Methode ruft eine Wiedergabeliste ab, die die Medienelemente aus dem angegebenen Album enthält.
ms.assetid: e7e72f0e-e0ae-4bbd-a8b7-966f0fc50059
keywords:
- getBy-Methode Windows Media Player
- getBy Auflistungsmethode Windows Media Player , MediaCollection-Klasse
- MediaCollection-Klasse Windows Media Player , getBy Auflistungsmethode
topic_type:
- apiref
api_name:
- MediaCollection.getByAlbum
api_location:
- wmp.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7c17b7113b66f49822bad5586033312c9ec50711e6290c3f655a0a1b75adc54c
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118574673"
---
# <a name="mediacollectiongetbyalbum-method"></a>MediaCollection.getBy Auflistung-Methode

Die **GetByPlay-Methode** ruft eine Wiedergabeliste ab, die die Medienelemente aus dem angegebenen Album enthält.

## <a name="syntax"></a>Syntax


```JScript
retVal = MediaCollection.getByAlbum(
  album
)
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*Album* \[ In\]
</dt> <dd>

**Eine Zeichenfolge,** die den Namen des Albums enthält.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Diese Methode gibt ein **Playlist-Objekt** zurück.

## <a name="remarks"></a>Hinweise

Um diese Methode zu verwenden, ist Lesezugriff auf die Bibliothek erforderlich. Weitere Informationen finden Sie unter [Bibliothekszugriff.](library-access.md)

## <a name="examples"></a>Beispiele

Im folgenden Beispiel wird *MediaCollection verwendet.* **getByList,** um eine Wiedergabeliste von Medienelementen abzurufen. Die Wiedergabeliste enthält Elemente mit dem vom Benutzer angegebenen Album in einem HTML-TEXT-Eingabeelement mit dem Namen GetSignal. Das **Player-Objekt** wurde mit der ID = "Player" erstellt.


```JScript
<!-- Use an HTML BUTTON element to create the playlist and 
then play the digital media items. -->
<INPUT TYPE = "BUTTON"
       NAME = "PlayAlbum" 
       ID = "PlayAlbum"  
       VALUE = "Play Album"

onClick = "
    /* Retrieve the album title text from the user. */
    var album = GetAlbum.value;

    /* Create the playlist using getByAlbum. */
    var pl = Player.mediaCollection.getByAlbum(album);

    /* Make the new playlist the current playlist. */
    Player.currentPlaylist = pl;

    /* Play the media in the new playlist. */
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

[**Wiedergabelistenobjekt**](playlist-object.md)
</dt> <dt>

[**Einstellungen.mediaAccessRights**](settings-mediaaccessrights.md)
</dt> <dt>

[**Einstellungen.requestMediaAccessRights**](settings-requestmediaaccessrights.md)
</dt> </dl>

 

 





