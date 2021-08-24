---
title: ModeChange-Ereignis des AxWindowsMediaPlayer-Objekts
description: Das ModeChange-Ereignis tritt auf, wenn ein Modus von Windows Media Player geändert wird. | ModeChange-Ereignis des AxWindowsMediaPlayer-Objekts
ms.assetid: 56308425-dce5-4691-8970-c0807744abef
keywords:
- ModeChange-Ereignis des AxWindowsMediaPlayer-Objekts Windows Media Player
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
ms.openlocfilehash: aa3b81ce7c48fd34f03131c7ed3f6cafed1029b103f218842a70ecaade08f1af
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119764840"
---
# <a name="modechange-event-of-the-axwindowsmediaplayer-object"></a>ModeChange-Ereignis des AxWindowsMediaPlayer-Objekts

Das ModeChange-Ereignis tritt auf, wenn ein Modus von Windows Media Player geändert wird.

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

Der diesem Ereignis zugeordnete Handler ist vom Typ **AxWMPLib. \_ WMPOCXEvents \_ ModeChangeEventHandler**. Dieser Handler empfängt ein Argument vom Typ **AxWMPLib. \_ WMPOCXEvents \_ ModeChangeEvent**, das die folgenden Eigenschaften im Zusammenhang mit diesem Ereignis enthält.



| Eigenschaft | Beschreibung                                                                                    |
|----------|------------------------------------------------------------------------------------------------|
| modeName | System.StringIndicates the mode that was changed. Mögliche Werte finden Sie unter Hinweise.<br/> |
| newValue | System.BooleanIndicates den neuen Zustand des angegebenen Modus.<br/>                        |



 

## <a name="remarks"></a>Hinweise

Die folgende Tabelle zeigt die möglichen Werte für die modeName-Eigenschaft.



| Zeichenfolge  | Beschreibung                                         |
|---------|-----------------------------------------------------|
| Shuffle | Spuren werden in zufälliger Reihenfolge wiedergegeben.                  |
| loop    | Die gesamte Sequenz von Spuren wird wiederholt wiedergegeben. |



 

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|----------------------|----------------------------------------------------------------------------------------------------------------------------|
| Version<br/>   | Windows Media Player 9er Serie oder höher<br/>                                                                          |
| Namespace<br/> | **AxWMPLib**<br/>                                                                                                    |
| Assembly<br/>  | <dl> <dt>AxInterop.WMPLib.dll (AxInterop.WMPLib.dll.dll)</dt> </dl> |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[**AxWindowsMediaPlayer-Objekt (VB und C#)**](axwindowsmediaplayer-object--vb-and-c.md)
</dt> <dt>

[**IWMPSettings.getMode (VB und C#)**](wmplibiwmpsettings-iwmpsettings-getmode--vb-and-c.md)
</dt> <dt>

[**IWMPSettings.setMode (VB und C#)**](wmplibiwmpsettings-iwmpsettings-setmode--vb-and-c.md)
</dt> </dl>

 

 





