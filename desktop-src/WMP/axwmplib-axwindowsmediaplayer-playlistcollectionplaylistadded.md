---
title: PlaylistCollectionPlaylistAdded-Ereignis des AxWindowsMediaPlayer-Objekts
description: Das PlaylistCollectionPlaylistAdded-Ereignis tritt auf, wenn der Wiedergabelistensammlung eine Wiedergabeliste hinzugefügt wird. | PlaylistCollectionPlaylistAdded-Ereignis des AxWindowsMediaPlayer-Objekts
ms.assetid: 13d3bc86-6655-4536-a58f-327eabb2b8f9
keywords:
- PlaylistCollectionPlaylistAdded-Ereignis des AxWindowsMediaPlayer-Objekts Windows Media Player
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
ms.openlocfilehash: 4d5223d5864aa8be9019b2219ef09917a1c63cf16d87a48aef9543246d5197a8
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118581825"
---
# <a name="playlistcollectionplaylistadded-event-of-the-axwindowsmediaplayer-object"></a>PlaylistCollectionPlaylistAdded-Ereignis des AxWindowsMediaPlayer-Objekts

Das PlaylistCollectionPlaylistAdded-Ereignis tritt auf, wenn der Wiedergabelistensammlung eine Wiedergabeliste hinzugefügt wird.

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

Der diesem Ereignis zugeordnete Handler ist vom Typ **AxWMPLib. \_ WMPOCXEvents \_ PlaylistCollectionPlaylistAddedEventHandler**. Dieser Handler empfängt ein Argument vom Typ **AxWMPLib. \_ WMPOCXEvents \_ PlaylistCollectionPlaylistAddedEvent**, das die folgende Eigenschaft im Zusammenhang mit diesem Ereignis enthält.



| Eigenschaft             | Beschreibung                                                                |
|----------------------|----------------------------------------------------------------------------|
| **bstrPlaylistName** | System.String Gibt den Namen der hinzugefügten Wiedergabeliste an.<br/> |



 

## <a name="remarks"></a>Hinweise

Der Name der hinzugefügten Wiedergabeliste kann verwendet werden, um die entsprechende Wiedergabeliste mithilfe der IWMPPlaylistCollection abzurufen. **getByName-Methode.**

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|----------------------|----------------------------------------------------------------------------------------------------------------------------|
| Version<br/>   | Windows Media Player Serie 9 oder höher<br/>                                                                          |
| Namespace<br/> | **AxWMPLib**<br/>                                                                                                    |
| Assembly<br/>  | <dl> <dt>AxInterop.WMPLib.dll (AxInterop.WMPLib.dll.dll)</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**AxWindowsMediaPlayer-Objekt (VB und C#)**](axwindowsmediaplayer-object--vb-and-c.md)
</dt> <dt>

[**IWMPPlaylistCollection.getByName (VB und C#)**](wmplibiwmpplaylistcollection-iwmpplaylistcollection-getbyname--vb-and-c.md)
</dt> </dl>

 

 





