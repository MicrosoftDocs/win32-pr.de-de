---
title: LBN_SELCHANGE Benachrichtigungscode (Winuser.h)
description: Benachrichtigt die Anwendung, dass sich die Auswahl in einem Listenfeld aufgrund der Benutzereingabe geändert hat. Das übergeordnete Fenster des Listenfelds empfängt diesen Benachrichtigungscode über die WM \_ COMMAND-Meldung.
ms.assetid: 126d2c47-816e-4179-a870-f5c5a34c5513
keywords:
- LBN_SELCHANGE Benachrichtigungscode Windows Controls
topic_type:
- apiref
api_name:
- LBN_SELCHANGE
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3ef87aebcf2ce804a10b4682bfaf2cba900bd227a06671959d11babce5f46774
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "120085180"
---
# <a name="lbn_selchange-notification-code"></a>LBN \_ SELCHANGE-Benachrichtigungscode

Benachrichtigt die Anwendung, dass sich die Auswahl in einem Listenfeld aufgrund der Benutzereingabe geändert hat. Das übergeordnete Fenster des Listenfelds empfängt diesen Benachrichtigungscode über die [**WM \_ COMMAND-Meldung.**](/windows/desktop/menurc/wm-command)


```C++
LBN_SELCHANGE

    WPARAM wParam;
    LPARAM lParam; 
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*wParam* 
</dt> <dd>

[**LOWORD**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85)) enthält den Bezeichner des Listenfelds. [**Hiword**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85)) gibt den Benachrichtigungscode an.

</dd> <dt>

*lParam* 
</dt> <dd>

Handle für das Listenfeld.

</dd> </dl>

## <a name="remarks"></a>Hinweise

Dieser Benachrichtigungscode wird nur von einem Listenfeld mit dem [**LBS \_ NOTIFY-Format**](list-box-styles.md) gesendet.

Dieser Benachrichtigungscode wird nicht gesendet, wenn die Meldung [**LB \_ SETSEL**](lb-setsel.md), [**LB \_ SETCURSEL**](lb-setcursel.md), [**LB \_ SELECTSTRING**](lb-selectstring.md), [**LB \_ SELITEMRANGE**](lb-selitemrange.md) oder [**LB \_ SELITEMRANGEEX**](lb-selitemrangeex.md) die Auswahl ändert.

Bei einem Listenfeld mit mehrfacher Auswahl wird der LBN \_ SELCHANGE-Benachrichtigungscode gesendet, wenn der Benutzer eine Pfeiltaste drückt, auch wenn sich die Auswahl nicht ändert.

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

[**LB \_ SETCURSEL**](lb-setcursel.md)
</dt> <dt>

[LBN \_ DBLCLK](lbn-dblclk.md)
</dt> <dt>

[LBN \_ SELCANCEL](lbn-selcancel.md)
</dt> <dt>

**Andere Ressourcen**
</dt> <dt>

[**\_WM-BEFEHL**](/windows/desktop/menurc/wm-command)
</dt> </dl>

 

