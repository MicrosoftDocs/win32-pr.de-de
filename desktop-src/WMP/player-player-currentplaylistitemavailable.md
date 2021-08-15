---
title: Player.CurrentPlaylistItemAvailable-Ereignis
description: Das CurrentPlaylistItemAvailable-Ereignis tritt auf, wenn die aktuelle Wiedergabeliste verfügbar wird. | Player.CurrentPlaylistItemAvailable-Ereignis
ms.assetid: 4894e2fc-3464-413f-8abf-8b5e91899946
keywords:
- CurrentPlaylistItemAvailable-Ereignis Windows Media Player
- CurrentPlaylistItemAvailable-Ereignis Windows Media Player , Player-Klasse
- Player-Klasse Windows Media Player , CurrentPlaylistItemAvailable-Ereignis
topic_type:
- apiref
api_name:
- Player.CurrentPlaylistItemAvailable
api_location:
- wmp.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1c4c2543f99d9bc645fa021d7dc5c94f66369b3c3151647dc4d575aab0a32f62
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118338136"
---
# <a name="playercurrentplaylistitemavailable-event"></a>Player.CurrentPlaylistItemAvailable-Ereignis

Das **CurrentPlaylistItemAvailable-Ereignis** tritt auf, wenn die aktuelle Wiedergabeliste verfügbar wird.

## <a name="syntax"></a>Syntax


```JScript
Player.CurrentPlaylistItemAvailable(
  bstrItemName
)
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*bstrItemName* 
</dt> <dd>

**Eine Zeichenfolge,** die den Namen des aktuellen Wiedergabelistenelements enthält.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Dieses Ereignis gibt keinen Wert zurück.

## <a name="remarks"></a>Hinweise

Der Name der aktuellen Wiedergabeliste kann verwendet werden, um das entsprechende **Playlist-Objekt** mithilfe der *PlaylistCollection abzurufen.* **getByName-Methode.**

Der Wert von Ereignisparametern wird von Windows Media Player angegeben und kann mithilfe des angegebenen Parameternamens auf eine Methode in einer importierten JScript datei zugegriffen oder an diese übergeben werden. Dieser Parametername muss genau wie gezeigt typisieren, einschließlich Groß- und Groß-/Schreibanforderungen.

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

[**Wiedergabelistenobjekt**](playlist-object.md)
</dt> <dt>

[**PlaylistCollection.getByName**](playlistcollection-getbyname.md)
</dt> </dl>

 

 





