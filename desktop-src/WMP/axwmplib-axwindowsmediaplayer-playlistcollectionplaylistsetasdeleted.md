---
title: Playlistcollectionplaylistsetasdeleted-Ereignis des AxWindowsMediaPlayer-Objekts
description: Das playlistcollectionplaylisteintasdeleted-Ereignis ist für die zukünftige Verwendung reserviert.
ms.assetid: 6c0a4d2c-e965-4a88-acd4-2a2a12265e36
keywords:
- Playlistcollectionplaylistsetasdeleted-Ereignis der AxWindowsMediaPlayer-Objekt Fenster Media Player
topic_type:
- apiref
api_name:
- PlaylistCollectionPlaylistSetAsDeleted Event of the AxWindowsMediaPlayer Object
api_location:
- AxInterop.WMPLib.dll
api_type:
- Assembly
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: bf432ede40298abed98cdf0c5b02b0a192f7b3a9
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106358741"
---
# <a name="playlistcollectionplaylistsetasdeleted-event-of-the-axwindowsmediaplayer-object"></a>Playlistcollectionplaylistsetasdeleted-Ereignis des AxWindowsMediaPlayer-Objekts

Das playlistcollectionplaylisteintasdeleted-Ereignis ist für die zukünftige Verwendung reserviert.

``` syntax
[C#]
private void player_PlaylistCollectionPlaylistSetAsDeleted(
  object sender,
  _WMPOCXEvents_PlaylistCollectionPlaylistSetAsDeletedEvent e
)

[Visual Basic]
Private Sub player_PlaylistCollectionPlaylistSetAsDeleted(
  sender As Object,
  e As _WMPOCXEvents_PlaylistCollectionPlaylistSetAsDeletedEvent
) Handles player.PlaylistCollectionPlaylistSetAsDeleted
```

## <a name="event-data"></a>Ereignisdaten

Der diesem Ereignis zugeordnete Handler ist vom Typ **AxWMPLib. \_ Wmpocxevents \_ playlistcollectionplaylistentasdeletedeventhandler**. Dieser Handler empfängt ein Argument vom Typ **AxWMPLib. \_ Wmpocxevents \_ playlistcollectionplaylistentasdeletedevent**, das die folgenden Eigenschaften enthält, die mit diesem Ereignis verknüpft sind.



| Eigenschaft         | BESCHREIBUNG                                 |
|------------------|---------------------------------------------|
| bstrauplaylistname | **System. String** Nicht unterstützt.<br/>  |
| varfisdeleted    | **System. Boolean** Nicht unterstützt.<br/> |



 

## <a name="remarks"></a>Bemerkungen

Dieses Ereignis ist für die zukünftige Verwendung reserviert.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|----------------------|----------------------------------------------------------------------------------------------------------------------------|
| Version<br/>   | Windows Media Player 9-Serie oder höher<br/>                                                                          |
| Namespace<br/> | **AxWMPLib**<br/>                                                                                                    |
| Assembly<br/>  | <dl> <dt>AxInterop.WMPLib.dll (AxInterop.WMPLib.dll.dll)</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**AxWindowsMediaPlayer-Objekt (VB und c#)**](axwindowsmediaplayer-object--vb-and-c.md)
</dt> </dl>

 

 





