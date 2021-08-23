---
title: WM_VKEYTOITEM Meldung (Winuser.h)
description: Wird von einem Listenfeld mit dem \_ LBS-Format WANTKEYBOARDINPUT als Antwort auf eine WM KEYDOWN-Nachricht an den Besitzer \_ gesendet.
ms.assetid: 2eab922f-7298-436f-bd94-0eefae7284d5
keywords:
- WM_VKEYTOITEM Windows-Steuerelemente für Nachrichten
topic_type:
- apiref
api_name:
- WM_VKEYTOITEM
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 47c054952c74b8e66bb109b925cfbdc353ec97f7bebfb5b5cafaedf8857ccb5f
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118957469"
---
# <a name="wm_vkeytoitem-message"></a>WM \_ VKEYTOITEM-Meldung

Wird von einem Listenfeld mit dem [**\_ LBS-Format WANTKEYBOARDINPUT**](list-box-styles.md) als Antwort auf eine [**WM \_ KEYDOWN-Nachricht**](/windows/desktop/inputdev/wm-keydown) an den Besitzer gesendet.


```C++
WM_VKEYTOITEM

    WPARAM wParam;
    LPARAM lParam; 
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*wParam* 
</dt> <dd>

[**LOWORD**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85)) gibt den Code der virtuellen Taste an, die der Benutzer gedrückt hat. [**Hiword**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85)) gibt die aktuelle Position des Carets an.

</dd> <dt>

*lParam* 
</dt> <dd>

Handle für das Listenfeld.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Der Rückgabewert gibt die Aktion an, die die Anwendung als Antwort auf die Meldung ausgeführt hat. Der Rückgabewert -2 gibt an, dass die Anwendung alle Aspekte der Elementauswahl verarbeitet hat und keine weitere Aktion durch das Listenfeld erfordert. (Siehe Hinweise.) Der Rückgabewert -1 gibt an, dass das Listenfeld die Standardaktion als Reaktion auf die Tastatureingabe ausführen soll. Der Rückgabewert 0 oder höher gibt den Index eines Elements im Listenfeld an und gibt an, dass das Listenfeld die Standardaktion für die Tastatureingabe für das angegebene Element ausführen soll.

## <a name="remarks"></a>Hinweise

Der Rückgabewert -2 ist nur für Schlüssel gültig, die vom Listenfeld-Steuerelement nicht in Zeichen übersetzt werden. Wenn die [**WM \_ KEYDOWN-Nachricht**](/windows/desktop/inputdev/wm-keydown) in eine [**WM \_ CHAR-Nachricht**](/windows/desktop/inputdev/wm-char) übersetzt wird und die Anwendung die **WM \_ VKEYTOITEM-Nachricht** verarbeitet, die durch Drücken der TASTE generiert wurde, ignoriert das Listenfeld den Rückgabewert und führt die Standardverarbeitung für dieses Zeichen aus. **WM \_ KEYDOWN-Nachrichten,** die von Schlüsseln wie VK \_ UP, VK \_ DOWN, VK NEXT und VK PREVIOUS generiert \_ \_ werden, werden nicht in **WM \_ CHAR-Nachrichten** übersetzt. In solchen Fällen verhindert das Abfangen der **\_ WM-VKEYTOITEM-Nachricht** und das Zurückgeben von -2, dass das Listenfeld die Standardverarbeitung für diesen Schlüssel vornimmt.

Um Schlüssel abzufangen, die eine char-Nachricht generieren und eine spezielle Verarbeitung durchführen, muss die Anwendung die Unterklasse des Listenfelds erstellen, die [**WM \_ KEYDOWN-**](/windows/desktop/inputdev/wm-keydown) und [**WM \_ CHAR-Nachrichten**](/windows/desktop/inputdev/wm-char) abfangen und die Nachrichten entsprechend in der Unterklassenprozedur verarbeiten.

Die obigen Hinweise gelten für reguläre Listenfelder, die mit dem [**LBS \_ WANTKEYBOARDINPUT-Stil**](list-box-styles.md) erstellt werden. Wenn das Listenfeld vom Besitzer gezeichnet wird, muss die Anwendung die [**WM \_ CHARTOITEM-Nachricht**](wm-chartoitem.md) verarbeiten.

Die [**DefWindowProc-Funktion**](/windows/desktop/api/winuser/nf-winuser-defwindowproca) gibt -1 zurück.

Wenn eine Dialogfeldprozedur diese Meldung verarbeitet, sollte sie den gewünschten Rückgabewert in eine **BOOL-Datei** konvertieren und den Wert direkt zurückgeben. Der \_ von der [**SetWindowLong-Funktion**](/windows/desktop/api/winuser/nf-winuser-setwindowlonga) festgelegte DWL-MSGRESULT-Wert wird ignoriert.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows \[Nur Vista-Desktop-Apps\]<br/>                                                           |
| Unterstützte Mindestversion (Server)<br/> | Windows Nur Server \[ 2003-Desktop-Apps\]<br/>                                                     |
| Header<br/>                   | <dl> <dt>Winuser.h (include Windows.h)</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

**Referenz**
</dt> <dt>

[**\_WM-DIAGRAMMOITEM**](wm-chartoitem.md)
</dt> <dt>

**Andere Ressourcen**
</dt> <dt>

[**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85))
</dt> <dt>

[**LOWORD**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85))
</dt> <dt>

[**WM \_ KEYDOWN**](/windows/desktop/inputdev/wm-keydown)
</dt> </dl>

 

