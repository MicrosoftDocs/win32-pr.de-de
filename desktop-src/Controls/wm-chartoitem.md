---
title: WM_CHARTOITEM Meldung (Winuser. h)
description: Wird von einem Listenfeld mit dem lbs- \_ wantkeyboardinput-Stil als Reaktion auf eine WM-char-Nachricht an seinen Besitzer gesendet \_ .
ms.assetid: f941c00b-b836-4f1b-b8cf-8ac2b0704af3
keywords:
- Windows-Steuerelemente für WM_CHARTOITEM Meldung
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
ms.openlocfilehash: 2dc9df55dcf9f507cb57e91fe0214eab94c53f22
ms.sourcegitcommit: ac62be2f60f757f61ea647a95c168c9841ffabac
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/10/2021
ms.locfileid: "104353918"
---
# <a name="wm_chartoitem-message"></a>WM- \_ chartoitem-Meldung

Wird von einem Listenfeld mit dem [**lbs- \_ wantkeyboardinput**](list-box-styles.md) -Stil als Reaktion auf eine [**WM- \_ char**](/windows/desktop/inputdev/wm-char) -Nachricht an seinen Besitzer gesendet.


```C++
WM_CHARTOITEM

    WPARAM wParam;
    LPARAM lParam; 
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*wParam* 
</dt> <dd>

Das [**LoWord**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85)) gibt den Zeichencode des Schlüssels an, den der Benutzer gedrückt hat. Das [**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85)) -Element gibt die aktuelle Position der Einfügemarke an.

</dd> <dt>

*lParam* 
</dt> <dd>

Handle für das Listenfeld.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Der Rückgabewert gibt die Aktion an, die die Anwendung als Antwort auf die Nachricht ausgeführt hat. Der Rückgabewert-1 oder-2 gibt an, dass die Anwendung alle Aspekte der Elementauswahl behandelt hat und keine weitere Aktion im Listenfeld erfordert. Ein Rückgabewert von 0 (null) oder größer gibt den NULL basierten Index eines Elements im Listenfeld an und gibt an, dass im Listenfeld die Standardaktion für den Tastatur Strich für das angegebene Element ausgeführt werden soll.

## <a name="remarks"></a>Bemerkungen

Die [**defwindowproc**](/windows/desktop/api/winuser/nf-winuser-defwindowproca) -Funktion gibt-1 zurück.

Nur vom Besitzer gezeichnete Listenfelder, die nicht den [**lbs \_ hasstrings**](list-box-styles.md) -Stil aufweisen, können diese Nachricht empfangen.

Wenn eine Dialogfeld Prozedur diese Nachricht behandelt, sollte Sie den gewünschten Rückgabewert in einen **booleschen** Wert umwandeln und den Wert direkt zurückgeben. Der von der [**SetWindowLong**](/windows/desktop/api/winuser/nf-winuser-setwindowlonga) -Funktion festgelegte *DWL- \_ msgresult* -Wert wird ignoriert.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Nur Windows Vista \[ -Desktop-Apps\]<br/>                                                           |
| Unterstützte Mindestversion (Server)<br/> | Nur Windows Server 2003 \[ -Desktop-Apps\]<br/>                                                     |
| Header<br/>                   | <dl> <dt>Winuser. h (Windows. h einschließen)</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

**Verweis**
</dt> <dt>

[**WM \_ vkeytoitem**](wm-vkeytoitem.md)
</dt> <dt>

**Andere Ressourcen**
</dt> <dt>

[**DefWindowProc**](/windows/desktop/api/winuser/nf-winuser-defwindowproca)
</dt> <dt>

[**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85))
</dt> <dt>

[**LOWORD**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85))
</dt> <dt>

[**WM \_ -Zeichen**](/windows/desktop/inputdev/wm-char)
</dt> </dl>

 

