---
title: WM_NOTIFY Meldung (Winuser. h)
description: Wird von einem allgemeinen Steuerelement an das übergeordnete Fenster gesendet, wenn ein Ereignis aufgetreten ist oder das Steuerelement einige Informationen erfordert.
ms.assetid: vs|controls|~\controls\common\messages\wm_notify.htm
keywords:
- Windows-Steuerelemente für WM_NOTIFY Meldung
topic_type:
- apiref
api_name:
- WM_NOTIFY
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f1905954e7fb164f8436216fa918cc6f243f4b17
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "103956711"
---
# <a name="wm_notify-message"></a>WM- \_ Benachrichtigungs Meldung

Wird von einem allgemeinen Steuerelement an das übergeordnete Fenster gesendet, wenn ein Ereignis aufgetreten ist oder das Steuerelement einige Informationen erfordert.

## <a name="parameters"></a>Parameter

<dl> <dt>

*wParam* 
</dt> <dd>

Der Bezeichner des allgemeinen Steuer Elements, das die Nachricht sendet. Es ist nicht garantiert, dass dieser Bezeichner eindeutig ist. Eine Anwendung sollte das **hwndfrom** -oder **idfrom** -Member der [**NMHDR**](/windows/desktop/api/richedit/ns-richedit-nmhdr) -Struktur (übergeben als *LPARAM* -Parameter) verwenden, um das Steuerelement zu identifizieren.

</dd> <dt>

*lParam* 
</dt> <dd>

Ein Zeiger auf eine [**NMHDR**](/windows/desktop/api/richedit/ns-richedit-nmhdr) -Struktur, die den Benachrichtigungs Code und zusätzliche Informationen enthält. Bei einigen Benachrichtigungs Meldungen verweist dieser Parameter auf eine größere Struktur, die über die **NMHDR** -Struktur als erstes Element verfügt.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Der Rückgabewert wird ignoriert, außer bei Benachrichtigungs Meldungen, die andernfalls angeben.

## <a name="remarks"></a>Bemerkungen

Das Ziel der Nachricht muss das **HWND** des übergeordneten Elements des Steuer Elements sein. Dieser Wert kann mithilfe von [**GetParent**](/windows/desktop/api/winuser/nf-winuser-getparent)abgerufen werden, wie im folgenden Beispiel gezeigt, wobei *m \_ controlhwnd* das **HWND** des Steuer Elements selbst ist.


```
NMHDR nmh;
nmh.code = CUSTOM_SELCHANGE;    // Message type defined by control.
nmh.idFrom = GetDlgCtrlID(m_controlHwnd);
nmh.hwndFrom = m_controlHwnd;
SendMessage(GetParent(m_controlHwnd), 
    WM_NOTIFY, 
    nmh.idFrom, 
    (LPARAM)&nmh);
```



Anwendungen verarbeiten die Meldung in der Fenster Prozedur des übergeordneten Fensters, wie im folgenden Beispiel gezeigt, das die vom benutzerdefinierten Steuerelement im vorherigen Beispiel gesendete Benachrichtigungs Meldung behandelt.


```
INT_PTR CALLBACK DlgProc(HWND hDlg, UINT message, WPARAM wParam, LPARAM lParam)
{
    switch (message)
    {
    case WM_NOTIFY:
        switch (((LPNMHDR)lParam)->code)
        {
        case CUSTOM_SELCHANGE:
            if (((LPNMHDR)lParam)->idFrom == IDC_CUSTOMLISTBOX1)
            {
                ...   // Respond to message.
                return TRUE;
            }
            break; 
        ... // More cases on WM_NOTIFY switch.
        break;
        }
    ...  // More cases on message switch.
    }
    return FALSE;
}
```



Einige Benachrichtigungen, vor allem diejenigen, die für einen längeren Zeitraum in der API enthalten waren, werden als [**WM- \_ Befehls**](/windows/desktop/menurc/wm-command) Nachrichten gesendet. Weitere Informationen finden Sie unter [Control Messages](control-messages.md).

Wenn sich der Nachrichten Handler in einer Dialogfeld Prozedur befindet, müssen Sie die Funktion [**SetWindowLong**](/windows/desktop/api/winuser/nf-winuser-setwindowlonga) mit DWL \_ msgresult verwenden, um einen Rückgabewert festzulegen.

Für Windows Vista-Systeme und spätere Systeme kann die **WM- \_ Benachrichtigungs** Meldung nicht zwischen Prozessen gesendet werden.

Viele Benachrichtigungen sind sowohl im ANSI-als auch im Unicode-Format verfügbar. Das Fenster, das die **WM- \_ Benachrichtigungs** Meldung sendet, verwendet die [**WM \_ notifyformat**](wm-notifyformat.md) -Meldung, um zu bestimmen, welches Format verwendet werden soll Weitere Erläuterungen finden Sie unter **WM \_ notifyformat** .

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|--------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Nur Windows Vista \[ -Desktop-Apps\]<br/>                                       |
| Unterstützte Mindestversion (Server)<br/> | Nur Windows Server 2003 \[ -Desktop-Apps\]<br/>                                 |
| Header<br/>                   | <dl> <dt>Winuser. h</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**WM \_ notifyformat**](wm-notifyformat.md)
</dt> </dl>

 

