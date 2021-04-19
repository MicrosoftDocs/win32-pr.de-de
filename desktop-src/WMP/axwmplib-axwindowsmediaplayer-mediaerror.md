---
title: MediaError-Ereignis des AxWindowsMediaPlayer-Objekts
description: Das MediaError-Ereignis tritt auf, wenn ein Medienobjekt einen Fehlerzustand aufweist.
ms.assetid: a1fb3422-85c4-4856-951a-332517599984
keywords:
- MediaError-Ereignis der AxWindowsMediaPlayer-Objekt Fenster Media Player
topic_type:
- apiref
api_name:
- MediaError Event of the AxWindowsMediaPlayer Object
api_location:
- AxInterop.WMPLib.dll
api_type:
- Assembly
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 874b9297846a8f25f25c68545df234aa1be70594
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106361660"
---
# <a name="mediaerror-event-of-the-axwindowsmediaplayer-object"></a>MediaError-Ereignis des AxWindowsMediaPlayer-Objekts

Das MediaError-Ereignis tritt auf, wenn ein Medienobjekt einen Fehlerzustand aufweist.

``` syntax
[C#]
private void player_MediaError(
  object sender,
  _WMPOCXEvents_MediaErrorEvent e
)

[Visual Basic]
Private Sub player_MediaError(
  sender As Object,
  e As _WMPOCXEvents_MediaErrorEvent
) Handles player.MediaError
```

## <a name="event-data"></a>Ereignisdaten

Der diesem Ereignis zugeordnete Handler ist vom Typ **AxWMPLib. \_ Wmpocxevents \_ mediaerroreventhandler**. Dieser Handler empfängt ein Argument vom Typ **AxWMPLib. \_ Wmpocxevents \_ mediaerrorevent**, das die folgende Eigenschaft enthält, die sich auf dieses Ereignis bezieht.



| Eigenschaft     | BESCHREIBUNG                                                                                                           |
|--------------|-----------------------------------------------------------------------------------------------------------------------|
| pmediaobject | System. objectobject mit einem Fehlerzustand. Sie können dies in eine iwmpmedia-Schnittstelle umwandeln, um darauf zuzugreifen.<br/> |



 

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

[**Iwmpmedia-Schnittstelle (VB und c#)**](iwmpmedia--vb-and-c.md)
</dt> </dl>

 

 





