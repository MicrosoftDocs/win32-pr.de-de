---
title: WM_NEXTDLGCTL Meldung (Winuser. h)
description: Wird an eine Dialogfeld Prozedur gesendet, um den Tastaturfokus auf ein anderes Steuerelement im Dialogfeld festzulegen.
ms.assetid: 63d9fac2-3057-4bfa-9960-911fd18877d4
keywords:
- Dialog Felder WM_NEXTDLGCTL Meldung
topic_type:
- apiref
api_name:
- WM_NEXTDLGCTL
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: fc6b70dbaf010b839a0069513f97de8fdab1c0a1
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104518344"
---
# <a name="wm_nextdlgctl-message"></a>WM- \_ nextdlgctl-Nachricht

Wird an eine Dialogfeld Prozedur gesendet, um den Tastaturfokus auf ein anderes Steuerelement im Dialogfeld festzulegen.


```C++
#define WM_NEXTDLGCTL                   0x0028
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*wParam* 
</dt> <dd>

Wenn *LPARAM* den Wert **true** hat, identifiziert dieser Parameter das Steuerelement, das den Fokus erhält. Wenn *LPARAM* auf **false** festgelegt ist, gibt dieser Parameter an, ob das nächste oder vorherige Steuerelement mit dem **WS \_ tabstoppstil** den Fokus erhält. Wenn *wParam* gleich 0 (null) ist, erhält das nächste Steuerelement den Fokus. Andernfalls erhält das vorherige Steuerelement mit dem **WS \_ tabstoppstil** den Fokus.

</dd> <dt>

*lParam* 
</dt> <dd>

Das nieder wertige Wort gibt an, wie das System *wParam* verwendet. Wenn das nieder wertige Wort **true** ist, ist *wParam* ein Handle, das dem Steuerelement zugeordnet ist, das den Fokus erhält. Andernfalls ist *wParam* ein Flag, das angibt, ob das nächste oder vorherige Steuerelement mit dem **WS \_ tabstoppstil** den Fokus erhält.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Eine Anwendung sollte NULL zurückgeben, wenn Sie diese Nachricht verarbeitet.

## <a name="remarks"></a>Bemerkungen

Diese Meldung führt zusätzliche Dialogfeld-Verwaltungsvorgänge aus, die über diejenigen hinausgehen, die von der [**SetFocus**](/windows/desktop/api/winuser/nf-winuser-setfocus) -Funktion **WM- \_ nextdlgctl** ausgeführt werden, aktualisiert den standardmäßigen PUSHBUTTON-Rahmen, legt den Standard Steuerelement Bezeichner fest und wählt automatisch den Text eines Bearbeitungs Steuer Elements aus

Verwenden Sie die [**SendMessage**](/windows/desktop/api/winuser/nf-winuser-sendmessage) -Funktion nicht, um eine **WM- \_ nextdlgctl** -Nachricht zu senden, wenn Ihre Anwendung andere Nachrichten, die den Fokus festlegen, gleichzeitig verarbeitet. Verwenden Sie stattdessen die [**PostMessage**](/windows/desktop/api/winuser/nf-winuser-postmessagea) -Funktion.

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

[**PostMessage**](/windows/desktop/api/winuser/nf-winuser-postmessagea)
</dt> <dt>

[**SendMessage**](/windows/desktop/api/winuser/nf-winuser-sendmessage)
</dt> <dt>

[**SetFocus**](/windows/desktop/api/winuser/nf-winuser-setfocus)
</dt> <dt>

**Licher**
</dt> <dt>

[Dialog Felder](dialog-boxes.md)
</dt> </dl>

 

