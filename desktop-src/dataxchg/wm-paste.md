---
title: WM_PASTE (Winuser.h)
description: Eine Anwendung sendet eine WM PASTE-Nachricht an ein Bearbeitungssteuerfeld oder Kombinationsfeld, um den aktuellen Inhalt der Zwischenablage in das Bearbeitungssteuerfeld an der aktuellen Einfügeposition \_ zu kopieren. Daten werden nur eingefügt, wenn die Zwischenablage Daten im CF \_ TEXT-Format enthält.
ms.assetid: 6830b511-986f-46ef-a977-7adedffe86ea
keywords:
- WM_PASTE der Exchange
topic_type:
- apiref
api_name:
- WM_PASTE
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1a3cc1815349a2194d5dd7e2a65eb1c9ae77a2947f41361a90e92bae73357f81
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119499120"
---
# <a name="wm_paste-message"></a>WM \_ PASTE-Nachricht

Eine Anwendung sendet eine **WM \_ PASTE-Nachricht** an ein Bearbeitungssteuerfeld oder Kombinationsfeld, um den aktuellen Inhalt der Zwischenablage in das Bearbeitungssteuerfeld an der aktuellen Einfügeposition zu kopieren. Daten werden nur eingefügt, wenn die Zwischenablage Daten im [**CF \_ TEXT-Format**](standard-clipboard-formats.md) enthält.


```C++
#define WM_PASTE                        0x0302
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

Diese Meldung gibt keinen Wert zurück.

## <a name="remarks"></a>Hinweise

Wenn die WM-PASTE-Nachricht an ein Kombinationsfeld gesendet wird, wird sie vom Bearbeitungssteuerfeld verarbeitet. **\_** Diese Meldung hat keine Auswirkungen, wenn sie an ein Kombinationsfeld mit dem [**CBS \_ DROPDOWNLIST-Format gesendet**](../controls/combo-box-styles.md) wird.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows 2000 Professional \[nur Desktop-Apps\]<br/>                                               |
| Unterstützte Mindestversion (Server)<br/> | Windows 2000 Server \[nur Desktop-Apps\]<br/>                                                     |
| Header<br/>                   | <dl> <dt>Winuser.h (include Windows.h)</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

**Referenz**
</dt> <dt>

[**WM \_ CLEAR**](wm-clear.md)
</dt> <dt>

[**WM \_ COPY**](wm-copy.md)
</dt> <dt>

[**WM \_ CUT**](wm-cut.md)
</dt> <dt>

[**WM \_ UNDO**](/windows/desktop/Controls/wm-undo)
</dt> <dt>

**Konzeptionellen**
</dt> <dt>

[Zwischenablage](clipboard.md)
</dt> </dl>

 

