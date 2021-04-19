---
title: WM_COPY Meldung (Winuser. h)
description: Eine Anwendung sendet die WM- \_ Kopier Nachricht an ein Bearbeitungs Steuerelement oder ein Kombinations Feld, um die aktuelle Auswahl im CF-Text Format in die Zwischenablage zu kopieren \_ .
ms.assetid: dcac3ad3-1e70-4b71-accd-261587224e60
keywords:
- WM_COPY Nachrichten Datenaustausch
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
ms.openlocfilehash: b298248d75b1d25d1bfef8347347fe2f1a6c7916
ms.sourcegitcommit: 3d9dce1bd6c84e2b51759e940aa95aa9b459cd20
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/04/2021
ms.locfileid: "106363895"
---
# <a name="wm_copy-message"></a>WM- \_ Kopier Nachricht

Eine Anwendung sendet die **WM- \_ Kopier** Nachricht an ein Bearbeitungs Steuerelement oder ein Kombinations Feld, um die aktuelle Auswahl im [**CF- \_ Text**](standard-clipboard-formats.md) Format in die Zwischenablage zu kopieren.


```C++
#define WM_COPY                         0x0301
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

Gibt bei Erfolg einen Wert ungleich 0 (null) zurück, andernfalls NULL.

## <a name="remarks"></a>Bemerkungen

Beim Senden an ein Kombinations Feld wird die **WM- \_ Kopier** Nachricht durch das Bearbeitungs Steuerelement behandelt. Diese Meldung hat keine Auswirkung, wenn Sie mit dem " [**CBS \_ DropDownList**](../controls/combo-box-styles.md) "-Stil an ein Kombinations Feld gesendet wird.

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

[**WM \_ Ausschneiden**](wm-cut.md)
</dt> <dt>

[**WM \_ Einfügen**](wm-paste.md)
</dt> <dt>

[**WM \_ rückgängig machen**](/windows/desktop/Controls/wm-undo)
</dt> <dt>

**Licher**
</dt> <dt>

[Zwischenablage](clipboard.md)
</dt> </dl>

 

