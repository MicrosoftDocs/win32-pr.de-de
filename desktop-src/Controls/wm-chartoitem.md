---
title: WM_CHARTOITEM (Winuser.h)
description: Wird von einem Listenfeld mit dem LBS WANTKEYBOARDINPUT-Stil als Reaktion auf eine WM CHAR-Nachricht an den \_ \_ Besitzer gesendet.
ms.assetid: f941c00b-b836-4f1b-b8cf-8ac2b0704af3
keywords:
- WM_CHARTOITEM meldungssteuerelemente Windows
topic_type:
- apiref
api_name:
- WM_CHARTOITEM
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4f3809ae800cfc753925e7c27d87f970ce56c10d90ace7c23e87b46f3e0067fb
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118957529"
---
# <a name="wm_chartoitem-message"></a>WM \_ CHARTOITEM-Meldung

Wird von einem Listenfeld mit dem [**LBS \_ WANTKEYBOARDINPUT-Stil**](list-box-styles.md) als Reaktion auf eine [**WM \_ CHAR-Nachricht**](/windows/desktop/inputdev/wm-char) an den Besitzer gesendet.


```C++
WM_CHARTOITEM

    WPARAM wParam;
    LPARAM lParam; 
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*wParam* 
</dt> <dd>

Das [**LOWORD gibt**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85)) den Zeichencode der Taste an, die der Benutzer gedrückt hat. Das [**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85)) gibt die aktuelle Position des Caretworts an.

</dd> <dt>

*lParam* 
</dt> <dd>

Handle für das Listenfeld.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Der Rückgabewert gibt die Aktion an, die die Anwendung als Reaktion auf die Nachricht ausgeführt hat. Der Rückgabewert -1 oder -2 gibt an, dass die Anwendung alle Aspekte der Elementauswahl verarbeitet hat und keine weitere Aktion durch das Listenfeld erfordert. Ein Rückgabewert von 0 oder höher gibt den nullbasierten Index eines Elements im Listenfeld an und gibt an, dass das Listenfeld die Standardaktion für die Tastatureingabe für das angegebene Element ausführen soll.

## <a name="remarks"></a>Hinweise

Die [**DefWindowProc-Funktion**](/windows/desktop/api/winuser/nf-winuser-defwindowproca) gibt -1 zurück.

Nur vom Besitzer gezeichnete Listenfelder ohne [**LBS \_ HASSTRINGS-Format**](list-box-styles.md) können diese Meldung empfangen.

Wenn eine Dialogfeldprozedur diese Meldung verarbeitet, sollte sie den gewünschten Rückgabewert in einen **BOOL-Wert** umkehren und den Wert direkt zurückgeben. Der von der [**SetWindowLong-Funktion festgelegte**](/windows/desktop/api/winuser/nf-winuser-setwindowlonga) *\_ MSGRESULT-DWL-Wert* wird ignoriert.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows Nur \[ Vista-Desktop-Apps\]<br/>                                                           |
| Unterstützte Mindestversion (Server)<br/> | Windows Nur Server \[ 2003-Desktop-Apps\]<br/>                                                     |
| Header<br/>                   | <dl> <dt>Winuser.h (include Windows.h)</dt> </dl> |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

**Referenz**
</dt> <dt>

[**WM \_ VKEYTOITEM**](wm-vkeytoitem.md)
</dt> <dt>

**Andere Ressourcen**
</dt> <dt>

[**DefWindowProc**](/windows/desktop/api/winuser/nf-winuser-defwindowproca)
</dt> <dt>

[**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85))
</dt> <dt>

[**LOWORD**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85))
</dt> <dt>

[**WM \_ CHAR**](/windows/desktop/inputdev/wm-char)
</dt> </dl>

 

