---
title: Player.PlaylistCollectionPlaylistAdded-Ereignis
description: Das PlaylistCollectionPlaylistAdded-Ereignis tritt auf, wenn der Wiedergabelistensammlung eine Wiedergabeliste hinzugefügt wird. | Player.PlaylistCollectionPlaylistAdded-Ereignis
ms.assetid: 07acb5e6-d832-4f0b-a6bb-2b7ba27c368d
keywords:
- PlaylistCollectionPlaylistAdded-Ereignis Windows Media Player
- PlaylistCollectionPlaylistAdded-Ereignis Windows Media Player , Player-Klasse
- Player-Klasse Windows Media Player , PlaylistCollectionPlaylistAdded-Ereignis
topic_type:
- apiref
api_name:
- Player.PlaylistCollectionPlaylistAdded
api_location:
- wmp.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1e72dcacbb60c141348a295fe086957b1404475e9e3be90433f8bdbe816fc834
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118572589"
---
# <a name="playerplaylistcollectionplaylistadded-event"></a>Player.PlaylistCollectionPlaylistAdded-Ereignis

Das **PlaylistCollectionPlaylistAdded-Ereignis** tritt auf, wenn der Wiedergabelistensammlung eine Wiedergabeliste hinzugefügt wird.

## <a name="syntax"></a>Syntax


```JScript
Player.PlaylistCollectionPlaylistAdded(
  bstrPlaylistName
)
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*bstrPlaylistName* 
</dt> <dd>

**Zeichenfolge,** die den Namen der hinzugefügten Wiedergabeliste angibt.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Dieses Ereignis gibt keinen Wert zurück.

## <a name="remarks"></a>Hinweise

Der Name der hinzugefügten Wiedergabeliste kann verwendet werden, um das entsprechende **Wiedergabelistenobjekt** mithilfe der *PlaylistCollection* abzurufen. **getByName-Methode.**

Der Wert von Ereignisparametern wird von Windows Media Player angegeben und kann mithilfe des angegebenen Parameternamens in einer importierten JScript-Datei auf eine Methode zugegriffen oder an diese übergeben werden. Dieser Parametername muss genau wie gezeigt eingegeben werden, einschließlich Der Groß-/Großschreibung.

**Windows Media Player 10 Mobile:** Dieses Ereignis wird nicht unterstützt.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|------------------------------------------------------------------------------------|
| Version<br/> | Windows Media Player Version 7.0 oder höher.<br/>                              |
| DLL<br/>     | <dl> <dt>Wmp.dll</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**Player-Objekt**](player-object.md)
</dt> <dt>

[**PlaylistCollection.getByName**](playlistcollection-getbyname.md)
</dt> </dl>

 

 





