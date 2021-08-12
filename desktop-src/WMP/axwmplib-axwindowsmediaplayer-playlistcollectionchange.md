---
title: PlaylistCollectionChange-Ereignis des AxWindowsMediaPlayer-Objekts
description: Das PlaylistCollectionChange-Ereignis tritt auf, wenn sich etwas in der Wiedergabelistensammlung ändert. | PlaylistCollectionChange-Ereignis des AxWindowsMediaPlayer-Objekts
ms.assetid: 868ee1c6-b740-4614-90ac-961c59091f0f
keywords:
- PlaylistCollectionChange-Ereignis des AxWindowsMediaPlayer-Objekts Windows Media Player
topic_type:
- apiref
api_name:
- PlaylistCollectionChange Event of the AxWindowsMediaPlayer Object
api_location:
- AxInterop.WMPLib.dll
api_type:
- Assembly
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 15bf5b60fe1e2c0d6bf8a08555048122993b11b900530af400966a9736bf5b00
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118581863"
---
# <a name="playlistcollectionchange-event-of-the-axwindowsmediaplayer-object"></a>PlaylistCollectionChange-Ereignis des AxWindowsMediaPlayer-Objekts

Das PlaylistCollectionChange-Ereignis tritt auf, wenn sich etwas in der Wiedergabelistensammlung ändert.

``` syntax
[C#]
private void player_PlaylistCollectionChange(
  object sender,
  System.EventArgs e
)

[Visual Basic]
Private Sub player_PlaylistCollectionChange(
  sender As Object,
  e As System.EventArgs
) Handles player.PlaylistCollectionChange
```

## <a name="event-data"></a>Ereignisdaten

Dieses Ereignis enthält keine Daten.

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

 

 





