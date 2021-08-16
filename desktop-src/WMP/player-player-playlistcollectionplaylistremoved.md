---
title: Player.PlaylistCollectionPlaylistRemoved-Ereignis
description: Das PlaylistCollectionPlaylistRemoved-Ereignis tritt auf, wenn eine Wiedergabeliste aus der Wiedergabelistensammlung entfernt wird. | Player.PlaylistCollectionPlaylistRemoved-Ereignis
ms.assetid: 2405be98-b4c2-4b4e-bea6-0c48a3e26f18
keywords:
- PlaylistCollectionPlaylistRemoved-Ereignis Windows Media Player
- PlaylistCollectionPlaylistRemoved-Ereignis Windows Media Player , Player-Klasse
- Playerklasse Windows Media Player , PlaylistCollectionPlaylistRemoved-Ereignis
topic_type:
- apiref
api_name:
- Player.PlaylistCollectionPlaylistRemoved
api_location:
- wmp.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 456f7598b9e1f1d2c2a6e76e58a0b06142980835c3c6d71d9ab10c2230ac386f
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118337974"
---
# <a name="playerplaylistcollectionplaylistremoved-event"></a>Player.PlaylistCollectionPlaylistRemoved-Ereignis

Das **PlaylistCollectionPlaylistRemoved-Ereignis** tritt auf, wenn eine Wiedergabeliste aus der Wiedergabelistensammlung entfernt wird.

## <a name="syntax"></a>Syntax


```JScript
Player.PlaylistCollectionPlaylistRemoved(
  bstrPlaylistName
)
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*bstrPlaylistName* 
</dt> <dd>

**Eine Zeichenfolge,** die den Namen der Wiedergabeliste angibt, die entfernt wurde.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Dieses Ereignis gibt keinen Wert zurück.

## <a name="remarks"></a>Hinweise

Der Wert von Ereignisparametern wird von Windows Media Player angegeben und kann mithilfe des angegebenen Parameternamens auf eine Methode in einer importierten JScript-Datei zugegriffen oder an diese übergeben werden. Dieser Parametername muss genau wie gezeigt typisieren, einschließlich Groß- und Groß-/Schreibanforderungen.

**Windows Media Player 10 Mobile:** Dieses Ereignis wird nicht unterstützt.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|------------------------------------------------------------------------------------|
| Version<br/> | Windows Media Player Version 7.0 oder höher.<br/>                              |
| DLL<br/>     | <dl> <dt>Wmp.dll</dt> </dl> |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[**Player-Objekt**](player-object.md)
</dt> <dt>

[**PlaylistCollection.getByName**](playlistcollection-getbyname.md)
</dt> </dl>

 

 





