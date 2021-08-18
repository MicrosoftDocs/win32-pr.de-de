---
title: DoubleClick-Ereignis des AxWindowsMediaPlayer-Objekts
description: Das DoubleClick-Ereignis tritt auf, wenn der Benutzer auf eine Maustaste auf einem Windows Media Player-Steuerelement doppelklickt.
ms.assetid: 4f116d8a-1ad5-443a-9c91-66214bbdebcf
keywords:
- DoubleClick-Ereignis des AxWindowsMediaPlayer-Objekts Windows Media Player
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
ms.openlocfilehash: cb01a5d0d5b9dd750c1232badb913000218a088d1ba6b41bc22e4e5dd49a6230
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119136103"
---
# <a name="doubleclick-event-of-the-axwindowsmediaplayer-object"></a>DoubleClick-Ereignis des AxWindowsMediaPlayer-Objekts

Das DoubleClick-Ereignis tritt auf, wenn der Benutzer auf eine Maustaste auf einem Windows Media Player-Steuerelement doppelklickt.

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

Der diesem Ereignis zugeordnete Handler ist vom Typ **AxWMPLib. \_ WMPOCXEvents \_ DoubleClickEventHandler**. Dieser Handler empfängt ein Argument vom Typ **AxWMPLib. \_ WMPOCXEvents \_ DoubleClickEvent**, das die folgenden Eigenschaften im Zusammenhang mit diesem Ereignis enthält.



| Eigenschaft    | Beschreibung                                                                                                                                                                                                                                                                                                                    |
|-------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| nButton     | System.Int16A-Bitfeld mit Bits, die der linken Schaltfläche (Bit 0), der rechten Schaltfläche (Bit 1) und der mittleren Schaltfläche (Bit 2) entsprechen. Diese Bits entsprechen den Werten 1, 2 bzw. 4. Es wird nur eines der Bits festgelegt, das die Schaltfläche angibt, die das Ereignis verursacht hat.<br/>                                                |
| nShiftState | System.Int16A-Bitfeld mit den am wenigsten signifikanten Bits, die der UMSCHALTTASTE (Bit 0), der STRG-Taste (Bit 1) und der ALT-Taste (Bit 2) entsprechen. Diese Bits entsprechen den Werten 1, 2 bzw. 4. Einige, alle oder keine der Bits können festgelegt werden, was darauf hinweist, dass einige, alle oder keine der Tasten gedrückt werden.<br/> |
| Fx          | System.Int32Die x-Koordinate des Mauszeigers relativ zur linken oberen Ecke des Steuerelements.<br/>                                                                                                                                                                                                                 |
| Fy          | System.Int32Die y-Koordinate des Mauszeigers relativ zur linken oberen Ecke des Steuerelements.<br/>                                                                                                                                                                                                                 |



 

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|----------------------|----------------------------------------------------------------------------------------------------------------------------|
| Version<br/>   | Windows Media Player 9er Serie oder höher<br/>                                                                          |
| Namespace<br/> | **AxWMPLib**<br/>                                                                                                    |
| Assembly<br/>  | <dl> <dt>AxInterop.WMPLib.dll (AxInterop.WMPLib.dll.dll)</dt> </dl> |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[**AxWindowsMediaPlayer-Objekt (VB und C#)**](axwindowsmediaplayer-object--vb-and-c.md)
</dt> </dl>

 

 





