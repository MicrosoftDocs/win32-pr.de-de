---
title: KeyDown-Ereignis des AxWindowsMediaPlayer-Objekts
description: Das KeyDown-Ereignis tritt auf, wenn eine Taste gedrückt wird. | KeyDown-Ereignis des AxWindowsMediaPlayer-Objekts
ms.assetid: e67b9628-6c53-4893-921a-9487ebfc1cd5
keywords:
- Das KeyDown-Ereignis der AxWindowsMediaPlayer-Objekt Fenster Media Player
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
ms.openlocfilehash: fc89814063e1a43badd22e658b5f19ece7abb074
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106359747"
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

Der diesem Ereignis zugeordnete Handler ist vom Typ **AxWMPLib. \_ Wmpocxevents \_ keydownetventhandler**. Dieser Handler empfängt ein Argument vom Typ **AxWMPLib. \_ Wmpocxevents \_ keydownvent**, das die folgenden Eigenschaften enthält, die mit diesem Ereignis verknüpft sind.



| Eigenschaft    | BESCHREIBUNG                                                                                                                                                                                                                                                                                                                                                                          |
|-------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| nKeyCode    | System. Int16Specifies der physische Schlüssel, auf den geklickt wird. Mögliche Werte finden Sie unter "Hinweise".<br/>                                                                                                                                                                                                                                                                                    |
| nshiftstate | System. Int16A Bitfeld mit den geringsten signifikanten Bits, die der Umschalttaste (Bit 0), der STRG-Taste (Bit 1) und der Alt-Taste (Bit 2) entsprechen. Diese Bits entsprechen den Werten 1, 2 und 4. Das Shift-Argument gibt den Zustand dieser Schlüssel an. Einige, alle oder keine der Bits können festgelegt werden. Dies deutet darauf hin, dass einige, alle oder keine der Schlüssel gedrückt werden.<br/> |



 

## <a name="remarks"></a>Bemerkungen

Die **nKeyCode** -Eigenschaft gibt einen physischen Schlüssel an. In den folgenden Tabellen sind die möglichen Werte für die Hauptschlüssel auf einer Standardtastatur aufgeführt.

Werte für die Hauptschlüssel.



| Schlüssel                     | Wert   |
|-------------------------|---------|
| A-Z                     | 65-90   |
| 0-9                     | 48-56   |
| F1-F12                  | 112-123 |
| ESC                     | 27      |
| TAB                     | 9       |
| Feststelltaste               | 20      |
| Shift (links oder rechts)   | 16      |
| STRG (links oder rechts)    | 17      |
| ALT (links oder rechts)     | 18      |
| SPACE                   | 32      |
| RÜCKTASTE               | 8       |
| EINGABETASTE                   | 13      |
| Windows-Taste, Links  | 91      |
| Windows-Taste, rechts | 92      |
| Anwendungsschlüssel         | 93      |



 

Werte für die Zahlen Füll Tasten.



| Schlüssel               | Wert  |
|-------------------|--------|
| 0-9               | 96-105 |
| NUM-Sperre          | 144    |
| Dividieren (/)        | 111    |
| Multiplizieren ( \* )     | 106    |
| Subtraktion (-)      | 109    |
| Hinzufügen (+)           | 107    |
| Trennzeichen (EINGABETASTE) | 108    |
| Dezimalzahl (.)       | 110    |



 

Werte für die Navigationstasten.



| Schlüssel         | Wert |
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
| Version<br/>   | Windows Media Player 9-Serie oder höher<br/>                                                                          |
| Namespace<br/> | **AxWMPLib**<br/>                                                                                                    |
| Assembly<br/>  | <dl> <dt>AxInterop.WMPLib.dll (AxInterop.WMPLib.dll.dll)</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**AxWindowsMediaPlayer-Objekt (VB und c#)**](axwindowsmediaplayer-object--vb-and-c.md)
</dt> </dl>

 

 





