---
title: WM_VKEYTOITEM Meldung (Winuser. h)
description: Wird von einem Listenfeld mit dem lbs- \_ wantkeyboardinput-Stil an seinen Besitzer als Antwort auf eine WM- \_ KeyDown-Nachricht gesendet.
ms.assetid: 2eab922f-7298-436f-bd94-0eefae7284d5
keywords:
- Windows-Steuerelemente für WM_VKEYTOITEM Meldung
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
ms.openlocfilehash: 7d1685682d8305fff5d9d93ef59d8859e099e6ce
ms.sourcegitcommit: 3d9dce1bd6c84e2b51759e940aa95aa9b459cd20
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/04/2021
ms.locfileid: "104351729"
---
# <a name="wm_vkeytoitem-message"></a>WM- \_ vkeytoitem-Meldung

Wird von einem Listenfeld mit dem [**lbs- \_ wantkeyboardinput**](list-box-styles.md) -Stil an seinen Besitzer als Antwort auf eine [**WM- \_ KeyDown**](/windows/desktop/inputdev/wm-keydown) -Nachricht gesendet.


```C++
WM_VKEYTOITEM

    WPARAM wParam;
    LPARAM lParam; 
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*wParam* 
</dt> <dd>

Das [**LoWord**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85)) gibt den Code des virtuellen Schlüssels der vom Benutzer gedrückten Taste an. Das [**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85)) -Element gibt die aktuelle Position der Einfügemarke an.

</dd> <dt>

*lParam* 
</dt> <dd>

Handle für das Listenfeld.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Der Rückgabewert gibt die Aktion an, die die Anwendung als Antwort auf die Nachricht ausgeführt hat. Der Rückgabewert-2 gibt an, dass die Anwendung alle Aspekte der Elementauswahl behandelt hat und keine weitere Aktion im Listenfeld erfordert. (Siehe Hinweise.) Der Rückgabewert-1 gibt an, dass das Listenfeld die Standardaktion als Reaktion auf den Tastatur Strich ausführen soll. Ein Rückgabewert von 0 (null) oder größer gibt den Index eines Elements im Listenfeld an und gibt an, dass im Listenfeld die Standardaktion für den Tastatur Strich für das angegebene Element ausgeführt werden soll.

## <a name="remarks"></a>Bemerkungen

Der Rückgabewert-2 ist nur für Schlüssel gültig, die vom Listenfeld-Steuerelement nicht in Zeichen übersetzt werden. Wenn die [**WM- \_ keydownnachricht**](/windows/desktop/inputdev/wm-keydown) in eine [**WM \_ char**](/windows/desktop/inputdev/wm-char) -Nachricht übersetzt wird und die Anwendung die als Ergebnis des Tastendruck generierte **WM \_ vkeytoitem** -Nachricht verarbeitet, ignoriert das Listenfeld den Rückgabewert und übernimmt die Standard Verarbeitung für das Zeichen. **WM \_ KeyDown** -Nachrichten, die von Schlüsseln wie "VK \_ up", "VK \_ down", "VK Next" und " \_ VK Previous" generiert werden, \_ werden nicht in " **WM \_ char** In solchen Fällen wird durch das Abfangen der **WM \_ vkeytoitem** -Nachricht und die Rückgabe von-2 verhindert, dass das Listenfeld die Standard Verarbeitung für diesen Schlüssel vornimmt.

Zum Abfangen von Schlüsseln, die eine char-Nachricht generieren und eine spezielle Verarbeitung durchführen, muss die Anwendung das Listenfeld unterteilen, sowohl die [**WM- \_ KeyDown**](/windows/desktop/inputdev/wm-keydown) -als auch die [**WM- \_ char**](/windows/desktop/inputdev/wm-char) -Nachricht abfangen und die Nachrichten entsprechend in der Unterklassen Prozedur verarbeiten.

Die vorangehenden Hinweise gelten für reguläre Listenfelder, die mit dem [**lbs- \_ wantkeyboardinput**](list-box-styles.md) -Stil erstellt werden. Wenn das Listenfeld vom Besitzer gezeichnet wird, muss die Anwendung die " [**WM \_ chartoitem**](wm-chartoitem.md) "-Nachricht verarbeiten.

Die [**defwindowproc**](/windows/desktop/api/winuser/nf-winuser-defwindowproca) -Funktion gibt-1 zurück.

Wenn eine Dialogfeld Prozedur diese Nachricht behandelt, sollte Sie den gewünschten Rückgabewert in einen **booleschen** Wert umwandeln und den Wert direkt zurückgeben. Der \_ von der [**SetWindowLong**](/windows/desktop/api/winuser/nf-winuser-setwindowlonga) -Funktion festgelegte DWL-msgresult-Wert wird ignoriert.

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

[**WM- \_ Diagramm**](wm-chartoitem.md)
</dt> <dt>

**Andere Ressourcen**
</dt> <dt>

[**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85))
</dt> <dt>

[**LOWORD**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85))
</dt> <dt>

[**WM- \_ KeyDown**](/windows/desktop/inputdev/wm-keydown)
</dt> </dl>

 

