---
title: MouseUp-Ereignis des AxWindowsMediaPlayer-Objekts
description: Das MouseUp-Ereignis tritt auf, wenn der Benutzer eine Maustaste loslässt. | MouseUp-Ereignis des AxWindowsMediaPlayer-Objekts
ms.assetid: 26bb6e82-d744-4770-b4de-07c9f52b76ec
keywords:
- Das MouseUp-Ereignis der AxWindowsMediaPlayer-Objekt Fenster Media Player
topic_type:
- apiref
api_name:
- MouseUp Event of the AxWindowsMediaPlayer Object
api_location:
- AxInterop.WMPLib.dll
api_type:
- Assembly
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a2bf9c209b4fa263eb0a6cbcba2a32b0b1c46fa9
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106361555"
---
# <a name="mouseup-event-of-the-axwindowsmediaplayer-object"></a>MouseUp-Ereignis des AxWindowsMediaPlayer-Objekts

Das MouseUp-Ereignis tritt auf, wenn der Benutzer eine Maustaste loslässt.

``` syntax
[C#]
private void player_MouseUpEvent(
  object sender,
  _WMPOCXEvents_MouseUpEvent e
)

[Visual Basic]
Private Sub player_MouseUpEvent(  
  sender As Object,
  e As _WMPOCXEvents_MouseUpEvent
) Handles player.MouseUpEvent
```

## <a name="event-data"></a>Ereignisdaten

Der diesem Ereignis zugeordnete Handler ist vom Typ **AxWMPLib. \_ Wmpocxevents \_ mouseupeer-thandler**. Dieser Handler empfängt ein Argument vom Typ **AxWMPLib. \_ Wmpocxevents \_ mouseupeer Vent**, das die folgenden Eigenschaften enthält, die mit diesem Ereignis verknüpft sind.



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

 

 





