---
title: OpenPlaylistSwitch-Ereignis des AxWindowsMediaPlayer-Objekts
description: Das OpenPlaylistSwitch-Ereignis tritt auf, wenn die Wiedergabe eines Titels auf einer DVD beginnt. | OpenPlaylistSwitch-Ereignis des AxWindowsMediaPlayer-Objekts
ms.assetid: 0b9c37a3-1349-48bd-8e1a-aba286c82abf
keywords:
- OpenPlaylistSwitch-Ereignis des AxWindowsMediaPlayer-Objekts Windows Media Player
topic_type:
- apiref
api_name:
- OpenPlaylistSwitch Event of the AxWindowsMediaPlayer Object
api_location:
- AxInterop.WMPLib.dll
api_type:
- Assembly
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c57341488c385b159ce294626a79b7e22287bff83864f7273b0f4432c1db95ae
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119764700"
---
# <a name="openplaylistswitch-event-of-the-axwindowsmediaplayer-object"></a>OpenPlaylistSwitch-Ereignis des AxWindowsMediaPlayer-Objekts

Das OpenPlaylistSwitch-Ereignis tritt auf, wenn die Wiedergabe eines Titels auf einer DVD beginnt.

``` syntax
[C#]
private void player_OpenPlaylistSwitch(
  object sender,
  _WMPOCXEvents_OpenPlaylistSwitchEvent e
)

[Visual Basic]
Private Sub player_OpenPlaylistSwitch(
  sender As Object,
  e As _WMPOCXEvents_OpenPlaylistSwitchEvent
) Handles player.OpenPlaylistSwitch
```

## <a name="event-data"></a>Ereignisdaten

Der diesem Ereignis zugeordnete Handler ist vom Typ **AxWMPLib. \_ WMPOCXEvents \_ OpenPlaylistSwitchEventHandler**. Dieser Handler empfängt ein Argument vom Typ **AxWMPLib. \_ WMPOCXEvents \_ OpenPlaylistSwitchEvent**, das die folgende Eigenschaft im Zusammenhang mit diesem Ereignis enthält.



| Eigenschaft  | Beschreibung                                                                                                         |
|-----------|---------------------------------------------------------------------------------------------------------------------|
| **pItem** | System.ObjectObject, das den Titel darstellt. Sie können diese in eine IWMPPlaylist-Schnittstelle umstellen, um darauf zuzugreifen.<br/> |



 

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|----------------------|----------------------------------------------------------------------------------------------------------------------------|
| Version<br/>   | Windows Media Player 9er Serie oder höher<br/>                                                                          |
| Namespace<br/> | **AxWMPLib**<br/>                                                                                                    |
| Assembly<br/>  | <dl> <dt>AxInterop.WMPLib.dll (AxInterop.WMPLib.dll.dll)</dt> </dl> |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[**AxWindowsMediaPlayer-Objekt (VB und C#)**](axwindowsmediaplayer-object--vb-and-c.md)
</dt> <dt>

[**IWMPPlaylist-Schnittstelle (VB und C#)**](iwmpplaylist--vb-and-c.md)
</dt> </dl>

 

 





