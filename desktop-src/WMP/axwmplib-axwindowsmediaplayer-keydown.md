---
title: KeyDown-Ereignis des AxWindowsMediaPlayer-Objekts
description: Das KeyDown-Ereignis tritt auf, wenn eine Taste gedrückt wird. | KeyDown-Ereignis des AxWindowsMediaPlayer-Objekts
ms.assetid: e67b9628-6c53-4893-921a-9487ebfc1cd5
keywords:
- KeyDown-Ereignis des AxWindowsMediaPlayer-Objekts Windows Media Player
topic_type:
- apiref
api_name:
- KeyDown Event of the AxWindowsMediaPlayer Object
api_location:
- AxInterop.WMPLib.dll
api_type:
- Assembly
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 054736007219021dbc0a4c1c968f61e1bbdb285fa416aae5f3c92c3880fb55de
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119469720"
---
# <a name="keydown-event-of-the-axwindowsmediaplayer-object"></a>KeyDown-Ereignis des AxWindowsMediaPlayer-Objekts

Das KeyDown-Ereignis tritt auf, wenn eine Taste gedrückt wird.

``` syntax
[C#]
private void player_KeyDownEvent(
  object sender,
  _WMPOCXEvents_KeyDownEvent e
)

[Visual Basic]
Private Sub player_KeyDownEvent(  
  sender As Object, 
  e As _WMPOCXEvents_KeyDownEvent
) Handles player.KeyDownEvent
```

## <a name="event-data"></a>Ereignisdaten

Der diesem Ereignis zugeordnete Handler ist vom Typ **AxWMPLib. \_ WMPOCXEvents \_ KeyDownEventHandler**. Dieser Handler empfängt ein Argument vom Typ **AxWMPLib. \_ WMPOCXEvents \_ KeyDownEvent**, das die folgenden Eigenschaften im Zusammenhang mit diesem Ereignis enthält.



| Eigenschaft    | BESCHREIBUNG                                                                                                                                                                                                                                                                                                                                                                          |
|-------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| nKeyCode    | System.Int16 Gibt an, welche physische Taste gedrückt wird. Mögliche Werte finden Sie unter Hinweise.<br/>                                                                                                                                                                                                                                                                                    |
| nShiftState | System.Int16A-Bitfeld mit den am wenigsten signifikanten Bits, die der UMSCHALTTASTE (Bit 0), der STRG-Taste (Bit 1) und der ALT-Taste (Bit 2) entsprechen. Diese Bits entsprechen den Werten 1, 2 bzw. 4. Das Shift-Argument gibt den Zustand dieser Schlüssel an. Einige, alle oder keine der Bits können festgelegt werden, was darauf hinweist, dass einige, alle oder keine der Tasten gedrückt werden.<br/> |



 

## <a name="remarks"></a>Hinweise

Die **nKeyCode-Eigenschaft** gibt einen physischen Schlüssel an. Die folgenden Tabellen zeigen die möglichen Werte für die Haupttasten auf einer Standardtastatur.

Werte für die Hauptschlüssel.



| Key                     | Wert   |
|-------------------------|---------|
| A-Z                     | 65-90   |
| 0-9                     | 48-56   |
| F1–F12                  | 112-123 |
| ESC                     | 27      |
| TAB                     | 9       |
| Feststelltaste               | 20      |
| UMSCHALT (links oder rechts)   | 16      |
| STRG (links oder rechts)    | 17      |
| ALT (links oder rechts)     | 18      |
| SPACE                   | 32      |
| RÜCKTASTE               | 8       |
| EINGABETASTE                   | 13      |
| Windows Logo-TASTE, links  | 91      |
| Windows Logo-Taste rechts | 92      |
| Anwendungsschlüssel         | 93      |



 

Werte für die Nummernpadtasten.



| Key               | Wert  |
|-------------------|--------|
| 0-9               | 96-105 |
| NUM-SPERRE          | 144    |
| DIVIDE (/)        | 111    |
| MULTIPLY ( \* )     | 106    |
| SUBTRACT (-)      | 109    |
| ADD (+)           | 107    |
| SEPARATOR (EINGABETASTE) | 108    |
| DECIMAL (.)       | 110    |



 

Werte für die Navigationsschlüssel.



| Key         | Wert |
|-------------|-------|
| INSERT      | 45    |
| Delete      | 46    |
| POS1        | 36    |
| ENDE         | 35    |
| BILD-AUF     | 33    |
| BILD-AB   | 34    |
| NACH-OBEN-TASTE    | 38    |
| NACH-UNTEN-TASTE  | 40    |
| NACH-LINKS-TASTE  | 37    |
| NACH-RECHTS-TASTE | 39    |



 

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

 

 





