---
title: PlaylistCollection.getByName-Methode
description: Die getByName-Methode ruft ein PlaylistArray-Objekt ab, das Wiedergabelisten mit dem angegebenen Namen enthält, sofern vorhanden.
ms.assetid: 0308a98d-1149-4367-b602-33fa54c1760f
keywords:
- getByName-Methode Windows Media Player
- getByName-Methode Windows Media Player , PlaylistCollection-Klasse
- PlaylistCollection-Klasse Windows Media Player , getByName-Methode
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
ms.openlocfilehash: 300307ff011abf8b28c645901422291ccab4cf7c66a7a3ba81121ffe1c22e573
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118334641"
---
# <a name="playlistcollectiongetbyname-method"></a>PlaylistCollection.getByName-Methode

Die **getByName-Methode** ruft ein **PlaylistArray-Objekt** ab, das Wiedergabelisten mit dem angegebenen Namen enthält, sofern vorhanden.

## <a name="syntax"></a>Syntax


```JScript
retVal = PlaylistCollection.getByName(
  name
)
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*name* \[ In\]
</dt> <dd>

**Zeichenfolge,** die den Namen der abzurufenden Wiedergabelisten enthält.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Diese Methode gibt ein **PlaylistArray-Objekt** zurück.

## <a name="remarks"></a>Hinweise

Verwenden Sie *PlaylistArray.* **count,** um zu bestimmen, ob eine Wiedergabeliste vorhanden ist. Wenn **count** 0 (null) ist, ist keine Wiedergabeliste vorhanden.

Um diese Methode zu verwenden, ist Lesezugriff auf die Bibliothek erforderlich. Weitere Informationen finden Sie unter [Bibliothekszugriff.](library-access.md)

## <a name="examples"></a>Beispiele

Im folgenden JScript Beispiel wird *playlistCollection* verwendet. **getByName,** um das **playlistCollection-Objekt** auf eine Wiedergabeliste mit dem Namen "ThreeList" zu überprüfen. Wenn die Wiedergabeliste "Threelist" vorhanden ist, legt **getByName** "ThreeList" als aktuelle Wiedergabeliste fest. Das **Player-Objekt** wurde mit der ID = "Player" erstellt.


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
| Version<br/> | Windows Media Player Version 7.0 oder höher.<br/>                              |
| DLL<br/>     | <dl> <dt>Wmp.dll</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**PlaylistArray-Objekt**](playlistarray-object.md)
</dt> <dt>

[**PlaylistArray.count**](playlistarray-count.md)
</dt> <dt>

[**PlaylistCollection-Objekt**](playlistcollection-object.md)
</dt> <dt>

[**Einstellungen.mediaAccessRights**](settings-mediaaccessrights.md)
</dt> <dt>

[**Einstellungen.requestMediaAccessRights**](settings-requestmediaaccessrights.md)
</dt> </dl>

 

 





