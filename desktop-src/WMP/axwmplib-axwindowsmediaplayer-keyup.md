---
title: KeyUp-Ereignis des AxWindowsMediaPlayer-Objekts
description: Das KeyUp-Ereignis tritt auf, wenn eine Taste losgelassen wird. | KeyUp-Ereignis des AxWindowsMediaPlayer-Objekts
ms.assetid: db814481-6099-4dbd-8ab1-808e1875ae35
keywords:
- Das KeyUp-Ereignis der AxWindowsMediaPlayer-Objekt Fenster Media Player
topic_type:
- apiref
api_name:
- KeyUp Event of the AxWindowsMediaPlayer Object
api_location:
- AxInterop.WMPLib.dll
api_type:
- Assembly
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 509f520ff7624b0b29302d7bf5cd825cd45b4254
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106370207"
---
# <a name="keyup-event-of-the-axwindowsmediaplayer-object"></a>KeyUp-Ereignis des AxWindowsMediaPlayer-Objekts

Das KeyUp-Ereignis tritt auf, wenn eine Taste losgelassen wird.

``` syntax
[C#]
private void player_KeyUpEvent(
  object sender,
  _WMPOCXEvents_KeyUpEvent e
)

[Visual Basic]
Private Sub player_KeyUpEvent(
    sender As Object,
    e As _WMPOCXEvents_KeyUpEvent
) Handles player.KeyUpEvent
```

## <a name="event-data"></a>Ereignisdaten

Der diesem Ereignis zugeordnete Handler ist vom Typ **AxWMPLib. \_ Wmpocxevents \_ keyugventhandler**. Dieser Handler empfängt ein Argument vom Typ **AxWMPLib. \_ Wmpocxevents \_ keyupeer Vent**, das die folgenden Eigenschaften enthält, die mit diesem Ereignis verknüpft sind.



| Eigenschaft    | BESCHREIBUNG                                                                                                                                                                                                                                                                                                                                                                          |
|-------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| nKeyCode    | System. Int16Specifies der physische Schlüssel, auf den geklickt wird. Mögliche Werte finden Sie im Abschnitt "Hinweise" des KeyDown-Ereignisses.<br/>                                                                                                                                                                                                                                                   |
| nshiftstate | System. Int16A Bitfeld mit den geringsten signifikanten Bits, die der Umschalttaste (Bit 0), der STRG-Taste (Bit 1) und der Alt-Taste (Bit 2) entsprechen. Diese Bits entsprechen den Werten 1, 2 und 4. Das Shift-Argument gibt den Zustand dieser Schlüssel an. Einige, alle oder keine der Bits können festgelegt werden. Dies deutet darauf hin, dass einige, alle oder keine der Schlüssel gedrückt werden.<br/> |



 

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

 

 





