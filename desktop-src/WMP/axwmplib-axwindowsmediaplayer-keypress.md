---
title: KeyPress-Ereignis des AxWindowsMediaPlayer-Objekts
description: Das KeyPress-Ereignis tritt auf, wenn eine Taste gedrückt und freigegeben wird. | KeyPress-Ereignis des AxWindowsMediaPlayer-Objekts
ms.assetid: 73ecd6f9-1b58-4e28-ad1b-2d930a235e1d
keywords:
- Das KeyPress-Ereignis der AxWindowsMediaPlayer-Objekt Fenster Media Player
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
ms.openlocfilehash: c4a01e84b8f765d024c753d08211f3bb84e7f011
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106352082"
---
# <a name="keypress-event-of-the-axwindowsmediaplayer-object"></a>KeyPress-Ereignis des AxWindowsMediaPlayer-Objekts

Das KeyPress-Ereignis tritt auf, wenn eine Taste gedrückt und freigegeben wird.

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

Der diesem Ereignis zugeordnete Handler ist vom Typ **AxWMPLib. \_ Wmpocxevents \_ KeyPressEventHandler**. Dieser Handler empfängt ein Argument vom Typ **AxWMPLib. \_ Wmpocxevents \_ KeyPressEvent**, das die folgende Eigenschaft enthält, die sich auf dieses Ereignis bezieht.



| Eigenschaft      | BESCHREIBUNG                                                                        |
|---------------|------------------------------------------------------------------------------------|
| **nkeyascii** | System. Int16Specifies der numerische Standard-ANSI-Code für das Zeichen.<br/> |



 

## <a name="remarks"></a>Bemerkungen

Dieses Ereignis tritt auf, wenn die Tastatureingabe ein beliebiges druckbares Tastatur Zeichen ergibt, die STRG-Taste mit einem Zeichen aus dem Standard Alphabet oder einem von einigen Sonderzeichen und der Eingabe-oder RÜCKTASTE gedrückt wird.

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

 

 





