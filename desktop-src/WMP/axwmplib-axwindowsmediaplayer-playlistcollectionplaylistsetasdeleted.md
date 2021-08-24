---
title: PlaylistCollectionPlaylistSetAsDeleted-Ereignis des AxWindowsMediaPlayer-Objekts
description: Das PlaylistCollectionPlaylistSetAsDeleted-Ereignis ist für die zukünftige Verwendung reserviert.
ms.assetid: 6c0a4d2c-e965-4a88-acd4-2a2a12265e36
keywords:
- PlaylistCollectionPlaylistSetAsDeleted-Ereignis des AxWindowsMediaPlayer-Objekts Windows Media Player
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
ms.openlocfilehash: b11187ffaf6e16612ba7edb573e0b0bc71e9d2abf44ee509db2404026e3ed570
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119864579"
---
# <a name="playlistcollectionplaylistsetasdeleted-event-of-the-axwindowsmediaplayer-object"></a>PlaylistCollectionPlaylistSetAsDeleted-Ereignis des AxWindowsMediaPlayer-Objekts

Das PlaylistCollectionPlaylistSetAsDeleted-Ereignis ist für die zukünftige Verwendung reserviert.

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

Der diesem Ereignis zugeordnete Handler ist vom Typ **AxWMPLib. \_ WMPOCXEvents \_ PlaylistCollectionPlaylistSetAsDeletedEventHandler**. Dieser Handler empfängt ein Argument vom Typ **AxWMPLib. \_ WMPOCXEvents \_ PlaylistCollectionPlaylistSetAsDeletedEvent**, das die folgenden Eigenschaften im Zusammenhang mit diesem Ereignis enthält.



| Eigenschaft         | BESCHREIBUNG                                 |
|------------------|---------------------------------------------|
| bstrPlaylistName | **System.String** Wird nicht unterstützt.<br/>  |
| varfIsDeleted    | **System.Boolean** Wird nicht unterstützt.<br/> |



 

## <a name="remarks"></a>Hinweise

Dieses Ereignis ist für die zukünftige Verwendung reserviert.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|----------------------|----------------------------------------------------------------------------------------------------------------------------|
| Version<br/>   | Windows Media Player 9er Serie oder höher<br/>                                                                          |
| Namespace<br/> | **AxWMPLib**<br/>                                                                                                    |
| Assembly<br/>  | <dl> <dt>AxInterop.WMPLib.dll (AxInterop.WMPLib.dll.dll)</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**AxWindowsMediaPlayer-Objekt (VB und C#)**](axwindowsmediaplayer-object--vb-and-c.md)
</dt> </dl>

 

 





