---
title: Durationunitchange-Ereignis des AxWindowsMediaPlayer-Objekts
description: Das durationunitchange-Ereignis ist für die zukünftige Verwendung reserviert.
ms.assetid: d8d7da21-bc61-49f8-91bd-4c232295c1ac
keywords:
- Das durationunitchange-Ereignis der AxWindowsMediaPlayer-Objekt Fenster Media Player
topic_type:
- apiref
api_name:
- DurationUnitChange Event of the AxWindowsMediaPlayer Object
api_location:
- AxInterop.WMPLib.dll
api_type:
- Assembly
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f90aa052c61893d83683d10f482cd05841a49fab
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106365175"
---
# <a name="durationunitchange-event-of-the-axwindowsmediaplayer-object"></a>Durationunitchange-Ereignis des AxWindowsMediaPlayer-Objekts

Das durationunitchange-Ereignis ist für die zukünftige Verwendung reserviert.

``` syntax
[C#]
private void player_DurationUnitChange(
  object sender,
  _WMPOCXEvents_DurationUnitChangeEvent e
)

[Visual Basic]
Private Sub player_DurationUnitChange(  
  sender As Object,  
  e As _WMPOCXEvents_DurationUnitChangeEvent
) Handles player.DurationUnitChange
```

## <a name="event-data"></a>Ereignisdaten

Der diesem Ereignis zugeordnete Handler ist vom Typ **AxWMPLib. \_ Wmpocxevents \_ durationunitchangeeventhandler**. Dieser Handler empfängt ein Argument vom Typ **AxWMPLib. \_ Wmpocxevents \_ durationunitchangeevent**, das die folgende Eigenschaft enthält, die sich auf dieses Ereignis bezieht.



| Eigenschaft        | BESCHREIBUNG                               |
|-----------------|-------------------------------------------|
| newdurationunit | **System. Int32** Nicht unterstützt.<br/> |



 

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

 

 





