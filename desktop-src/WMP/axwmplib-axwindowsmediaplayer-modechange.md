---
title: Modechange-Ereignis des AxWindowsMediaPlayer-Objekts
description: Das modechange-Ereignis tritt auf, wenn ein Windows Media Player-Modus geändert wird. | Modechange-Ereignis des AxWindowsMediaPlayer-Objekts
ms.assetid: 56308425-dce5-4691-8970-c0807744abef
keywords:
- Modechange-Ereignis der AxWindowsMediaPlayer-Objekt Fenster Media Player
topic_type:
- apiref
api_name:
- ModeChange Event of the AxWindowsMediaPlayer Object
api_location:
- AxInterop.WMPLib.dll
api_type:
- Assembly
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c06575fc986f4223056244964c2d070874c890b2
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106358635"
---
# <a name="modechange-event-of-the-axwindowsmediaplayer-object"></a>Modechange-Ereignis des AxWindowsMediaPlayer-Objekts

Das modechange-Ereignis tritt auf, wenn ein Windows Media Player-Modus geändert wird.

``` syntax
[C#]
private void player_ModeChange(
  object sender,
  _WMPOCXEvents_ModeChangeEvent e
)

[Visual Basic]
Private Sub player_ModeChange( 
  sender As Object,
  e As _WMPOCXEvents_ModeChangeEvent
) Handles player.ModeChange
```

## <a name="event-data"></a>Ereignisdaten

Der diesem Ereignis zugeordnete Handler ist vom Typ **AxWMPLib. \_ Wmpocxevents \_ modechangeeventhandler**. Dieser Handler empfängt ein Argument vom Typ **AxWMPLib. \_ Wmpocxevents \_ modechangeevent**, das die folgenden Eigenschaften enthält, die mit diesem Ereignis verknüpft sind.



| Eigenschaft | BESCHREIBUNG                                                                                    |
|----------|------------------------------------------------------------------------------------------------|
| "Name" | System. stringindikiert den Modus, der geändert wurde. Mögliche Werte finden Sie unter "Hinweise".<br/> |
| newValue | System. booleangibt den neuen Zustand des angegebenen Modus an.<br/>                        |



 

## <a name="remarks"></a>Bemerkungen

In der folgenden Tabelle werden die möglichen Werte für die Eigenschaft "mudename" angezeigt.



| Zeichenfolge  | Beschreibung                                         |
|---------|-----------------------------------------------------|
| Shuffle | Spuren werden in zufälliger Reihenfolge wiedergegeben.                  |
| loop    | Die gesamte Sequenz von Spuren wird wiederholt wiedergegeben. |



 

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

[**Iwmpsettings. getMode (VB und c#)**](wmplibiwmpsettings-iwmpsettings-getmode--vb-and-c.md)
</dt> <dt>

[**Iwmpsettings. SetMode (VB und c#)**](wmplibiwmpsettings-iwmpsettings-setmode--vb-and-c.md)
</dt> </dl>

 

 





