---
title: Playlistcollectionplaylistrebewegungs-Ereignis des AxWindowsMediaPlayer-Objekts
description: Das playlistcollectionplaylistrebewegungs-Ereignis tritt auf, wenn eine Wiedergabeliste aus der Wiedergabelisten Auflistung entfernt wird. | Playlistcollectionplaylistrebewegungs-Ereignis des AxWindowsMediaPlayer-Objekts
ms.assetid: 96935a9e-4c08-42e9-a63f-7b6cda41b243
keywords:
- Playlistcollectionplaylistrebewegungsereignis der AxWindowsMediaPlayer-Objekt Fenster Media Player
topic_type:
- apiref
api_name:
- PlaylistCollectionPlaylistRemoved Event of the AxWindowsMediaPlayer Object
api_location:
- AxInterop.WMPLib.dll
api_type:
- Assembly
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6b982ff566380a7aa5bf4d0b1a1219739b52dd35
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106361686"
---
# <a name="playlistcollectionplaylistremoved-event-of-the-axwindowsmediaplayer-object"></a>Playlistcollectionplaylistrebewegungs-Ereignis des AxWindowsMediaPlayer-Objekts

Das playlistcollectionplaylistrebewegungs-Ereignis tritt auf, wenn eine Wiedergabeliste aus der Wiedergabelisten Auflistung entfernt wird.

``` syntax
[C#]
private void player_PlaylistCollectionPlaylistRemoved(
  object sender,
  _WMPOCXEvents_PlaylistCollectionPlaylistRemovedEvent e
)

[Visual Basic]
Private Sub player_PlaylistCollectionPlaylistRemoved(  
  sender As Object,
  e As _WMPOCXEvents_PlaylistCollectionPlaylistRemovedEvent
) Handles player.PlaylistCollectionPlaylistRemoved
```

## <a name="event-data"></a>Ereignisdaten

Der diesem Ereignis zugeordnete Handler ist vom Typ **AxWMPLib. \_ Wmpocxevents \_ playlistcollectionplaylistremuvedeventhandler**. Dieser Handler empfängt ein Argument vom Typ **AxWMPLib. \_ Wmpocxevents \_ playlistcollectionplaylistremuvedevent**, das die folgende Eigenschaft enthält, die sich auf dieses Ereignis bezieht.



| Eigenschaft             | BESCHREIBUNG                                                                  |
|----------------------|------------------------------------------------------------------------------|
| **bstrauplaylistname** | System. StringGibt den Namen der Wiedergabeliste an, die entfernt wurde.<br/> |



 

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

 

 





