---
title: PlaylistCollectionPlaylistRemoved-Ereignis des AxWindowsMediaPlayer-Objekts
description: Das PlaylistCollectionPlaylistRemoved-Ereignis tritt auf, wenn eine Wiedergabeliste aus der Wiedergabelistensammlung entfernt wird. | PlaylistCollectionPlaylistRemoved-Ereignis des AxWindowsMediaPlayer-Objekts
ms.assetid: 96935a9e-4c08-42e9-a63f-7b6cda41b243
keywords:
- PlaylistCollectionPlaylistRemoved-Ereignis des AxWindowsMediaPlayer-Objekts Windows Media Player
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
ms.openlocfilehash: 170dd4291c1c60f0e20c548c611485cddd50f5ec51d3f244d21f3e046e5c0d4c
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119864571"
---
# <a name="playlistcollectionplaylistremoved-event-of-the-axwindowsmediaplayer-object"></a>PlaylistCollectionPlaylistRemoved-Ereignis des AxWindowsMediaPlayer-Objekts

Das PlaylistCollectionPlaylistRemoved-Ereignis tritt auf, wenn eine Wiedergabeliste aus der Wiedergabelistensammlung entfernt wird.

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

Der diesem Ereignis zugeordnete Handler ist vom Typ **AxWMPLib. \_ WMPOCXEvents \_ PlaylistCollectionPlaylistRemovedEventHandler**. Dieser Handler empfängt ein Argument vom Typ **AxWMPLib. \_ WMPOCXEvents \_ PlaylistCollectionPlaylistRemovedEvent**, das die folgende Eigenschaft im Zusammenhang mit diesem Ereignis enthält.



| Eigenschaft             | BESCHREIBUNG                                                                  |
|----------------------|------------------------------------------------------------------------------|
| **bstrPlaylistName** | System.String Gibt den Namen der entfernten Wiedergabeliste an.<br/> |



 

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|----------------------|----------------------------------------------------------------------------------------------------------------------------|
| Version<br/>   | Windows Media Player 9er Serie oder höher<br/>                                                                          |
| Namespace<br/> | **AxWMPLib**<br/>                                                                                                    |
| Assembly<br/>  | <dl> <dt>AxInterop.WMPLib.dll (AxInterop.WMPLib.dll.dll)</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**AxWindowsMediaPlayer-Objekt (VB und C#)**](axwindowsmediaplayer-object--vb-and-c.md)
</dt> <dt>

[**IWMPPlaylistCollection.getByName (VB und C#)**](wmplibiwmpplaylistcollection-iwmpplaylistcollection-getbyname--vb-and-c.md)
</dt> </dl>

 

 





