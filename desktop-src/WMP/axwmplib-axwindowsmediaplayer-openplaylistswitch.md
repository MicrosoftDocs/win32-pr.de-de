---
title: Openplaylistswitch-Ereignis des AxWindowsMediaPlayer-Objekts
description: Das openplaylistswitch-Ereignis tritt auf, wenn die Wiedergabe eines Titels auf einer DVD beginnt. | Openplaylistswitch-Ereignis des AxWindowsMediaPlayer-Objekts
ms.assetid: 0b9c37a3-1349-48bd-8e1a-aba286c82abf
keywords:
- Openplaylistswitch-Ereignis der AxWindowsMediaPlayer-Objekt Fenster Media Player
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
ms.openlocfilehash: 338d360944b46555be53d5e212561cf906dd33c9
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106367589"
---
# <a name="openplaylistswitch-event-of-the-axwindowsmediaplayer-object"></a>Openplaylistswitch-Ereignis des AxWindowsMediaPlayer-Objekts

Das openplaylistswitch-Ereignis tritt auf, wenn die Wiedergabe eines Titels auf einer DVD beginnt.

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

Der diesem Ereignis zugeordnete Handler ist vom Typ **AxWMPLib. \_ Wmpocxevents \_ openplaylistswitcheventhandler**. Dieser Handler empfängt ein Argument vom Typ **AxWMPLib. \_ Wmpocxevents \_ openplaylistswitchevent**, das die folgende Eigenschaft enthält, die sich auf dieses Ereignis bezieht.



| Eigenschaft  | BESCHREIBUNG                                                                                                         |
|-----------|---------------------------------------------------------------------------------------------------------------------|
| **pitem** | System. objectobject, das den Titel darstellt. Sie können dies in eine iwmpwiedergabe-Schnittstelle umwandeln, um darauf zuzugreifen.<br/> |



 

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

 

 





