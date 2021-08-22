---
title: MouseUp-Ereignis des AxWindowsMediaPlayer-Objekts
description: Das MouseUp-Ereignis tritt auf, wenn der Benutzer eine Maustaste loslässt. | MouseUp-Ereignis des AxWindowsMediaPlayer-Objekts
ms.assetid: 26bb6e82-d744-4770-b4de-07c9f52b76ec
keywords:
- MouseUp-Ereignis des AxWindowsMediaPlayer-Windows Media Player
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
ms.openlocfilehash: 10adcb3705182be7543eb1a89ea82d50cac096f3200a6341e10156de9262fa0a
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119509440"
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

Der diesem Ereignis zugeordnete Handler ist vom Typ **AxWMPLib. \_ WMPOCXEvents \_ MouseUpEventHandler**. Dieser Handler empfängt ein Argument vom Typ **AxWMPLib. \_ WMPOCXEvents \_ MouseUpEvent**, das die folgenden Eigenschaften im Zusammenhang mit diesem Ereignis enthält.



| Eigenschaft    | Beschreibung                                                                                                                                                                                                                                                                                                                    |
|-------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| nButton     | System.Int16A-Bitfeld mit Bits, die der linken Schaltfläche (Bit 0), der rechten Schaltfläche (Bit 1) und der mittleren Schaltfläche (Bit 2) entspricht. Diese Bits entsprechen den Werten 1, 2 bzw. 4. Es wird nur eines der Bits festgelegt, was die Schaltfläche angibt, die das Ereignis verursacht hat.<br/>                                                |
| nShiftState | System.Int16A-Bitfeld mit den am wenigsten signifikanten Bits, die der UMSCHALTTASTE (Bit 0), der STRG-TASTE (Bit 1) und der ALT-Taste (Bit 2) entspricht. Diese Bits entsprechen den Werten 1, 2 bzw. 4. Einige, alle oder keine der Bits können festgelegt werden, was darauf hinweist, dass einige, alle oder keine der Tasten gedrückt werden.<br/> |
| Fx          | System.Int32Die x-Koordinate des Mauszeigers relativ zur oberen linken Ecke des Steuerelements.<br/>                                                                                                                                                                                                                 |
| Fy          | System.Int32Die y-Koordinate des Mauszeigers relativ zur oberen linken Ecke des Steuerelements.<br/>                                                                                                                                                                                                                 |



 

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

 

 





