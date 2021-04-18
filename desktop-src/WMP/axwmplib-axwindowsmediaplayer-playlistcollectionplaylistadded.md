---
title: Playlistcollectionplaylistadded-Ereignis des AxWindowsMediaPlayer-Objekts
description: Das playlistcollectionplaylistadded-Ereignis tritt auf, wenn der Wiedergabelisten Auflistung eine Wiedergabeliste hinzugefügt wird. | Playlistcollectionplaylistadded-Ereignis des AxWindowsMediaPlayer-Objekts
ms.assetid: 13d3bc86-6655-4536-a58f-327eabb2b8f9
keywords:
- Playlistcollectionplaylistadded-Ereignis der AxWindowsMediaPlayer-Objekt Fenster Media Player
topic_type:
- apiref
api_name:
- PlaylistCollectionPlaylistAdded Event of the AxWindowsMediaPlayer Object
api_location:
- AxInterop.WMPLib.dll
api_type:
- Assembly
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b019e58ae8955f6df894101956e4776c2cd71626
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106352103"
---
# <a name="playlistcollectionplaylistadded-event-of-the-axwindowsmediaplayer-object"></a>Playlistcollectionplaylistadded-Ereignis des AxWindowsMediaPlayer-Objekts

Das playlistcollectionplaylistadded-Ereignis tritt auf, wenn der Wiedergabelisten Auflistung eine Wiedergabeliste hinzugefügt wird.

``` syntax
[C#]
private void player_PlaylistCollectionPlaylistAdded(
  object sender,
  _WMPOCXEvents_PlaylistCollectionPlaylistAddedEvent e
)

[Visual Basic]
Private Sub player_PlaylistCollectionPlaylistAdded(
  sender As Object,
  e As _WMPOCXEvents_PlaylistCollectionPlaylistAddedEvent
) Handles player.PlaylistCollectionPlaylistAdded
```

## <a name="event-data"></a>Ereignisdaten

Der diesem Ereignis zugeordnete Handler ist vom Typ **AxWMPLib. \_ Wmpocxevents \_ playlistcollectionplaylistaddedeventhandler**. Dieser Handler empfängt ein Argument vom Typ **AxWMPLib. \_ Wmpocxevents \_ playlistcollectionplaylistaddedevent**, das die folgende Eigenschaft enthält, die sich auf dieses Ereignis bezieht.



| Eigenschaft             | BESCHREIBUNG                                                                |
|----------------------|----------------------------------------------------------------------------|
| **bstrauplaylistname** | System. StringGibt den Namen der hinzugefügten Wiedergabeliste an.<br/> |



 

## <a name="remarks"></a>Bemerkungen

Der Name der hinzugefügten Wiedergabeliste kann verwendet werden, um die entsprechende Wiedergabeliste mithilfe von iwmpplaylistcollection abzurufen. **getByName** -Methode.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|----------------------|----------------------------------------------------------------------------------------------------------------------------|
| Version<br/>   | Windows Media Player 9-Serie oder höher<br/>                                                                          |
| Namespace<br/> | **AxWMPLib**<br/>                                                                                                    |
| Assembly<br/>  | <dl> <dt>AxInterop.WMPLib.dll (AxInterop.WMPLib.dll.dll)</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**AxWindowsMediaPlayer-Objekt (VB und c#)**](axwindowsmediaplayer-object--vb-and-c.md)
</dt> <dt>

[**Iwmpplaylistcollection. getByName (VB und c#)**](wmplibiwmpplaylistcollection-iwmpplaylistcollection-getbyname--vb-and-c.md)
</dt> </dl>

 

 





