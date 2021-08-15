---
title: WM_COPY (Winuser.h)
description: Eine Anwendung sendet die WM COPY-Nachricht an ein Bearbeitungssteuerfeld oder Kombinationsfeld, um die aktuelle Auswahl im \_ \_ CF-TEXT-Format in die Zwischenablage zu kopieren.
ms.assetid: dcac3ad3-1e70-4b71-accd-261587224e60
keywords:
- WM_COPY der Exchange
topic_type:
- apiref
api_name:
- WM_COPY
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2d7774b1e2d52cbe21b8636bcaa1c695f9f49b319280ebc89c74fd652533066b
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "120096750"
---
# <a name="wm_copy-message"></a>WM \_ COPY-Nachricht

Eine Anwendung sendet die **WM \_ COPY-Nachricht** an ein Bearbeitungssteuerfeld oder Kombinationsfeld, um die aktuelle Auswahl im [**\_ CF-TEXT-Format**](standard-clipboard-formats.md) in die Zwischenablage zu kopieren.


```C++
#define WM_COPY                         0x0301
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*wParam* 
</dt> <dd>

Dieser Parameter wird nicht verwendet und muss 0 (null) sein.

</dd> <dt>

*lParam* 
</dt> <dd>

Dieser Parameter wird nicht verwendet und muss 0 (null) sein.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Gibt bei Erfolg einen Wert ungleich 0 (null) zurück, sonst 0 (null).

## <a name="remarks"></a>Hinweise

Wenn die WM COPY-Nachricht an ein Kombinationsfeld gesendet wird, wird sie vom Bearbeitungssteuerfeld verarbeitet. **\_** Diese Meldung hat keine Auswirkungen, wenn sie an ein Kombinationsfeld mit dem [**CBS \_ DROPDOWNLIST-Format gesendet**](../controls/combo-box-styles.md) wird.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows 2000 Professional \[nur Desktop-Apps\]<br/>                                               |
| Unterstützte Mindestversion (Server)<br/> | Windows 2000 Server \[nur Desktop-Apps\]<br/>                                                     |
| Header<br/>                   | <dl> <dt>Winuser.h (include Windows.h)</dt> </dl> |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

**Referenz**
</dt> <dt>

[**WM \_ CLEAR**](wm-clear.md)
</dt> <dt>

[**WM \_ CUT**](wm-cut.md)
</dt> <dt>

[**WM \_ PASTE**](wm-paste.md)
</dt> <dt>

[**WM \_ UNDO**](/windows/desktop/Controls/wm-undo)
</dt> <dt>

**Konzeptionellen**
</dt> <dt>

[Zwischenablage](clipboard.md)
</dt> </dl>

 

