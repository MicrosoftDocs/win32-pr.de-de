---
title: WM_PASTE Meldung (Winuser. h)
description: Eine Anwendung sendet eine WM- \_ einfügenachricht an ein Bearbeitungs Steuerelement oder Kombinations Feld, um den aktuellen Inhalt der Zwischenablage an der aktuellen Position der Einfügemarke in das Bearbeitungs Steuerelement zu kopieren. Daten werden nur eingefügt, wenn die Zwischenablage Daten im CF- \_ Text Format enthält.
ms.assetid: 6830b511-986f-46ef-a977-7adedffe86ea
keywords:
- WM_PASTE Nachrichten Datenaustausch
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
ms.openlocfilehash: 86b723830ecdd0f8b7e3faa9da9adcb51161b297
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104392130"
---
# <a name="wm_paste-message"></a>WM- \_ Einfüge Nachricht

Eine Anwendung sendet eine **WM \_** -einfügenachricht an ein Bearbeitungs Steuerelement oder Kombinations Feld, um den aktuellen Inhalt der Zwischenablage an der aktuellen Position der Einfügemarke in das Bearbeitungs Steuerelement zu kopieren. Daten werden nur eingefügt, wenn die Zwischenablage Daten im [**CF- \_ Text**](standard-clipboard-formats.md) Format enthält.


```C++
#define WM_PASTE                        0x0302
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*wParam* 
</dt> <dd>

Dieser Parameter wird nicht verwendet und muss NULL sein.

</dd> <dt>

*lParam* 
</dt> <dd>

Dieser Parameter wird nicht verwendet und muss NULL sein.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Diese Meldung gibt keinen Wert zurück.

## <a name="remarks"></a>Bemerkungen

Beim Senden an ein Kombinations Feld wird die **WM- \_ Einfüge** Nachricht durch das Bearbeitungs Steuerelement behandelt. Diese Meldung hat keine Auswirkung, wenn Sie mit dem " [**CBS \_ DropDownList**](../controls/combo-box-styles.md) "-Stil an ein Kombinations Feld gesendet wird.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows 2000 Professional \[nur Desktop-Apps\]<br/>                                               |
| Unterstützte Mindestversion (Server)<br/> | Windows 2000 Server \[nur Desktop-Apps\]<br/>                                                     |
| Header<br/>                   | <dl> <dt>Winuser. h (Windows. h einschließen)</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

**Verweis**
</dt> <dt>

[**WM \_ Clear**](wm-clear.md)
</dt> <dt>

[**WM- \_ Kopie**](wm-copy.md)
</dt> <dt>

[**WM \_ Ausschneiden**](wm-cut.md)
</dt> <dt>

[**WM \_ rückgängig machen**](/windows/desktop/Controls/wm-undo)
</dt> <dt>

**Licher**
</dt> <dt>

[Zwischenablage](clipboard.md)
</dt> </dl>

 

