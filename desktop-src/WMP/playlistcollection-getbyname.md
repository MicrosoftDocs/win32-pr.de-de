---
title: Playlistcollection. getByName-Methode
description: Die getByName-Methode ruft ein playlistarray-Objekt ab, das Wiedergabelisten mit dem angegebenen Namen enthält (sofern vorhanden).
ms.assetid: 0308a98d-1149-4367-b602-33fa54c1760f
keywords:
- getByName-Methode, Windows-Media Player
- getByName-Methode, Windows Media Player, playlistcollection-Klasse
- Playlistcollection-Klasse, Windows Media Player, getByName-Methode
topic_type:
- apiref
api_name:
- PlaylistCollection.getByName
api_location:
- wmp.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7954df8e0ccc487df77ea31b3a26dce9eea6d2e0
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106366793"
---
# <a name="playlistcollectiongetbyname-method"></a>Playlistcollection. getByName-Methode

Die **getByName** -Methode ruft ein **playlistarray** -Objekt ab, das Wiedergabelisten mit dem angegebenen Namen enthält (sofern vorhanden).

## <a name="syntax"></a>Syntax


```JScript
retVal = PlaylistCollection.getByName(
  name
)
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*Name* \[ in\]
</dt> <dd>

**Zeichenfolge** , die den Namen der abzurufenden Wiedergabelisten enthält.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Diese Methode gibt ein **playlistarray** -Objekt zurück.

## <a name="remarks"></a>Bemerkungen

Verwenden Sie *playlistarray*. **Anzahl** , um zu bestimmen, ob eine Wiedergabeliste vorhanden ist Wenn **count** 0 (null) ist, ist keine Wiedergabeliste vorhanden.

Um diese Methode verwenden zu können, ist Lesezugriff auf die Bibliothek erforderlich. Weitere Informationen finden Sie unter [Bibliotheks Zugriff](library-access.md).

## <a name="examples"></a>Beispiele

Im folgenden JScript-Beispiel wird *playlistcollection* verwendet. **getByName** zum Überprüfen des **playlistcollection** -Objekts auf eine Wiedergabeliste mit dem Namen "threelist". Wenn die Wiedergabeliste "threelist" vorhanden ist, legt **getByName** "threelist" als aktuelle Wiedergabeliste fest. Das **Player** -Objekt wurde mit der ID = "Player" erstellt.


```JScript
//Retrieve the count of the playlists named "ThreeList".
var Checkit = Player.playlistCollection.getByName("ThreeList").count;

//Since duplicate playlist names are allowed, the count returned
//will be either zero (no playlist) or greater than zero 
//(playlist exists).
if (Checkit > 0){ 
    
   //Retrieve a playlistArray object containing "ThreeList". Assume that
   //there is only one playlist with that name, and assign it to the 
   //current playlist.
   Player.currentPlaylist = Player.playlistCollection.getByName("ThreeList").item(0);
}

```



## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|------------------------------------------------------------------------------------|
| Version<br/> | Windows Media Player Version 7,0 oder höher.<br/>                              |
| DLL<br/>     | <dl> <dt>Wmp.dll</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**Playlistarray-Objekt**](playlistarray-object.md)
</dt> <dt>

[**Playlistarray. Count**](playlistarray-count.md)
</dt> <dt>

[**Playlistcollection-Objekt**](playlistcollection-object.md)
</dt> <dt>

[**Settings. mediaaccessrights**](settings-mediaaccessrights.md)
</dt> <dt>

[**Settings. requestmediaaccessrights**](settings-requestmediaaccessrights.md)
</dt> </dl>

 

 





