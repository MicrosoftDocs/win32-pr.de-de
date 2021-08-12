---
title: BN_UNPUSHED Benachrichtigungscode (Winuser.h)
description: Wird gesendet, wenn der Pushzustand einer Schaltfläche auf "nicht gesendet" festgelegt ist.
ms.assetid: 1ae7311d-f067-41fe-a117-e0c70d239e9d
keywords:
- BN_UNPUSHED Benachrichtigungscode Windows Controls
topic_type:
- apiref
api_name:
- BN_UNPUSHED
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 418cb2cacc872fd1e1dfcd86778fddf35939c8e022510a4e0df7e00cf7718bc0
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118674114"
---
# <a name="bn_unpushed-notification-code"></a>\_BN-UNPUSHED-Benachrichtigungscode

Wird gesendet, wenn der Pushzustand einer Schaltfläche auf "nicht gesendet" festgelegt ist.

> [!Note]  
> Dieser Benachrichtigungscode wird nur zur Kompatibilität mit 16-Bit-Versionen von Windows vor Version 3.0 bereitgestellt. Anwendungen sollten den [**BS \_ OWNERDRAW-Schaltflächenstil**](button-styles.md) und die [**DRAWITEMSTRUCT-Struktur**](/windows/win32/api/winuser/ns-winuser-drawitemstruct) für diese Aufgabe verwenden.

 

Das übergeordnete Fenster der Schaltfläche empfängt diesen Benachrichtigungscode über die [**WM \_ COMMAND-Meldung.**](/windows/desktop/menurc/wm-command)


```C++
BN_UNPUSHED

    WPARAM wParam;
    LPARAM lParam; 
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*wParam* 
</dt> <dd>

[**LowORD**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85)) enthält den Steuerelementbezeichner der Schaltfläche. [**Hiword**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85)) gibt den Benachrichtigungscode an.

</dd> <dt>

*lParam* 
</dt> <dd>

Ein Handle für die Schaltfläche.

</dd> </dl>

## <a name="remarks"></a>Hinweise

BN \_ UNPUSHED entspricht dem [BN UNHILITE-Benachrichtigungscode. \_ ](bn-unhilite.md)

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows \[Nur Vista-Desktop-Apps\]<br/>                                                           |
| Unterstützte Mindestversion (Server)<br/> | Windows Nur Server \[ 2003-Desktop-Apps\]<br/>                                                     |
| Header<br/>                   | <dl> <dt>Winuser.h (include Windows.h)</dt> </dl> |



## <a name="see-also"></a>Weitere Informationen:

<dl> <dt>

[BN \_ PER PUSH ÜBERTRAGEN](bn-pushed.md)
</dt> </dl>

 

