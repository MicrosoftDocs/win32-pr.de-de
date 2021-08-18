---
title: KeyUp-Ereignis des AxWindowsMediaPlayer-Objekts
description: Das KeyUp-Ereignis tritt auf, wenn ein Schlüssel freigegeben wird. | KeyUp-Ereignis des AxWindowsMediaPlayer-Objekts
ms.assetid: db814481-6099-4dbd-8ab1-808e1875ae35
keywords:
- KeyUp-Ereignis des AxWindowsMediaPlayer-Objekts Windows Media Player
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
ms.openlocfilehash: 6c3a2666268e2c12e74c6498446ff49bde69dd30cf9819a7899e88a8b8ee4466
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119136013"
---
# <a name="keyup-event-of-the-axwindowsmediaplayer-object"></a>KeyUp-Ereignis des AxWindowsMediaPlayer-Objekts

Das KeyUp-Ereignis tritt auf, wenn ein Schlüssel freigegeben wird.

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

Der diesem Ereignis zugeordnete Handler ist vom Typ **AxWMPLib. \_ WMPOCXEvents \_ KeyUpEventHandler**. Dieser Handler empfängt ein Argument vom Typ **AxWMPLib. \_ WMPOCXEvents \_ KeyUpEvent**, das die folgenden Eigenschaften im Zusammenhang mit diesem Ereignis enthält.



| Eigenschaft    | Beschreibung                                                                                                                                                                                                                                                                                                                                                                          |
|-------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| nKeyCode    | System.Int16 Gibt an, welche physische Taste gedrückt wird. Mögliche Werte finden Sie im Abschnitt Hinweise des KeyDown-Ereignisses.<br/>                                                                                                                                                                                                                                                   |
| nShiftState | System.Int16A-Bitfeld mit den am wenigsten signifikanten Bits, die der UMSCHALTTASTE (Bit 0), der STRG-Taste (Bit 1) und der ALT-Taste (Bit 2) entsprechen. Diese Bits entsprechen den Werten 1, 2 bzw. 4. Das Shift-Argument gibt den Zustand dieser Schlüssel an. Einige, alle oder keine der Bits können festgelegt werden, was darauf hinweist, dass einige, alle oder keine der Tasten gedrückt werden.<br/> |



 

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

 

 





