---
title: DoubleClick-Ereignis des AxWindowsMediaPlayer-Objekts
description: Das Double Click-Ereignis tritt auf, wenn der Benutzer auf eine Maustaste in einem Windows Media Player-Steuerelement doppelklickt.
ms.assetid: 4f116d8a-1ad5-443a-9c91-66214bbdebcf
keywords:
- Das Double Click-Ereignis der AxWindowsMediaPlayer-Objekt Fenster Media Player
topic_type:
- apiref
api_name:
- DoubleClick Event of the AxWindowsMediaPlayer Object
api_location:
- AxInterop.WMPLib.dll
api_type:
- Assembly
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1ac809e8ea61b3abbbc964f6dc9ee2976442fc31
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106358388"
---
# <a name="doubleclick-event-of-the-axwindowsmediaplayer-object"></a>DoubleClick-Ereignis des AxWindowsMediaPlayer-Objekts

Das Double Click-Ereignis tritt auf, wenn der Benutzer auf eine Maustaste in einem Windows Media Player-Steuerelement doppelklickt.

``` syntax
[C#]
private void player_DoubleClickEvent(
  object sender,
  _WMPOCXEvents_DoubleClickEvent e
)

[Visual Basic]
Private Sub player_DoubleClickEvent(  
  sender As Object,  
  e As _WMPOCXEvents_DoubleClickEvent
) Handles player.DoubleClickEvent
```

## <a name="event-data"></a>Ereignisdaten

Der diesem Ereignis zugeordnete Handler ist vom Typ **AxWMPLib. \_ Wmpocxevents \_ doubleclickeventhandler**. Dieser Handler empfängt ein Argument vom Typ **AxWMPLib. \_ Wmpocxevents \_ doubleclickevent**, das die folgenden Eigenschaften enthält, die mit diesem Ereignis verknüpft sind.



| Eigenschaft    | BESCHREIBUNG                                                                                                                                                                                                                                                                                                                    |
|-------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| nschaltfläche     | System. Int16A Bitfeld mit Bits, die der linken Schaltfläche (Bit 0), der rechten Schaltfläche (Bit 1) und der mittleren Schaltfläche (Bit 2) entsprechen. Diese Bits entsprechen den Werten 1, 2 und 4. Es wird nur einer der Bits festgelegt, der die Schaltfläche angibt, die das Ereignis verursacht hat.<br/>                                                |
| nshiftstate | System. Int16A Bitfeld mit den geringsten signifikanten Bits, die der Umschalttaste (Bit 0), der STRG-Taste (Bit 1) und der Alt-Taste (Bit 2) entsprechen. Diese Bits entsprechen den Werten 1, 2 und 4. Einige, alle oder keine der Bits können festgelegt werden. Dies deutet darauf hin, dass einige, alle oder keine der Schlüssel gedrückt werden.<br/> |
| Designer          | System. Int32The x-Koordinate des Mauszeigers relativ zur linken oberen Ecke des Steuer Elements.<br/>                                                                                                                                                                                                                 |
| herrlichen          | System. Int32The y-Koordinate des Mauszeigers relativ zur linken oberen Ecke des Steuer Elements.<br/>                                                                                                                                                                                                                 |



 

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

 

 





