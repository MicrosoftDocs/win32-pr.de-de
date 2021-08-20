---
title: KeyPress-Ereignis des AxWindowsMediaPlayer-Objekts
description: Das KeyPress-Ereignis tritt auf, wenn eine Taste gedrückt und losgelassen wird. | KeyPress-Ereignis des AxWindowsMediaPlayer-Objekts
ms.assetid: 73ecd6f9-1b58-4e28-ad1b-2d930a235e1d
keywords:
- KeyPress-Ereignis des AxWindowsMediaPlayer-Objekts Windows Media Player
topic_type:
- apiref
api_name:
- KeyPress Event of the AxWindowsMediaPlayer Object
api_location:
- AxInterop.WMPLib.dll
api_type:
- Assembly
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 45b8022feacda910b28d68636c1abdcb2f6c1c9d3c2e799f762f25f5060b2b82
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119618790"
---
# <a name="keypress-event-of-the-axwindowsmediaplayer-object"></a>KeyPress-Ereignis des AxWindowsMediaPlayer-Objekts

Das KeyPress-Ereignis tritt auf, wenn eine Taste gedrückt und losgelassen wird.

``` syntax
[C#]
private void player_KeyPressEvent(
  object sender,
  _WMPOCXEvents_KeyPressEvent e
)

[Visual Basic]
Private Sub player_KeyPressEvent(  
  sender As Object,  
  e As _WMPOCXEvents_KeyPressEvent
) Handles player.KeyPressEvent
```

## <a name="event-data"></a>Ereignisdaten

Der diesem Ereignis zugeordnete Handler ist vom Typ **AxWMPLib. \_ WMPOCXEvents \_ KeyPressEventHandler**. Dieser Handler empfängt ein Argument vom Typ **AxWMPLib. \_ WMPOCXEvents \_ KeyPressEvent**, das die folgende Eigenschaft im Zusammenhang mit diesem Ereignis enthält.



| Eigenschaft      | Beschreibung                                                                        |
|---------------|------------------------------------------------------------------------------------|
| **nKeyAscii** | System.Int16 Gibt den numerischen STANDARD-ANSI-Code für das Zeichen an.<br/> |



 

## <a name="remarks"></a>Hinweise

Dieses Ereignis tritt auf, wenn die Tastatureingabe zu einem druckbaren Tastaturzeichen führt, die STRG-TASTE in Kombination mit einem Zeichen aus dem Standardal alphabet oder einem von einigen sonderzeichen sowie die EINGABETASTE oder DIE RÜCKTASTE verwendet wird.

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

 

 





