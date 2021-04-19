---
title: Playlistchange-Ereignis des AxWindowsMediaPlayer-Objekts
description: Das playlistchange-Ereignis tritt auf, wenn eine Wiedergabeliste geändert wird. | Playlistchange-Ereignis des AxWindowsMediaPlayer-Objekts
ms.assetid: e4166d81-a205-401a-94c4-a1619e764647
keywords:
- Playlistchange-Ereignis der AxWindowsMediaPlayer-Objekt Fenster Media Player
topic_type:
- apiref
api_name:
- PlaylistChange Event of the AxWindowsMediaPlayer Object
api_location:
- AxInterop.WMPLib.dll
api_type:
- Assembly
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9989b303d8e9077c158fd844c93431100205d9f6
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106356062"
---
# <a name="playlistchange-event-of-the-axwindowsmediaplayer-object"></a>Playlistchange-Ereignis des AxWindowsMediaPlayer-Objekts

Das playlistchange-Ereignis tritt auf, wenn eine Wiedergabeliste geändert wird.

``` syntax
[C#]
private void player_PlaylistChange(
  object sender,
  _WMPOCXEvents_PlaylistChangeEvent e
)

[Visual Basic]
Private Sub player_PlaylistChange(
  sender As Object,
  e As _WMPOCXEvents_PlaylistChangeEvent
) Handles player.PlaylistChange
```

## <a name="event-data"></a>Ereignisdaten

Der diesem Ereignis zugeordnete Handler ist vom Typ **AxWMPLib. \_ Wmpocxevents \_ playlistchangeeventhandler**. Dieser Handler empfängt ein Argument vom Typ **AxWMPLib. \_ Wmpocxevents \_ playlistchangeevent**, das die folgenden Eigenschaften enthält, die mit diesem Ereignis verknüpft sind.



| Eigenschaft     | BESCHREIBUNG                                                                                                                   |
|--------------|-------------------------------------------------------------------------------------------------------------------------------|
| **Abspielen** | System. objectdas Objekt, das sich geändert hat. Sie können dies in eine iwmpwiedergabe-Schnittstelle umwandeln, um darauf zuzugreifen.<br/>                |
| **change**   | WMPLib. wmpplaylistchangeeventtypea-Enumerationswert, der den Typ der Änderung angibt, die für die Wiedergabeliste aufgetreten ist.<br/> |



 

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

[**Iwmpwiedergabe-Schnittstelle (VB und c#)**](iwmpplaylist--vb-and-c.md)
</dt> </dl>

 

 





