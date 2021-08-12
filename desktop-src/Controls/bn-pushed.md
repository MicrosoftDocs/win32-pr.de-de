---
title: BN_PUSHED Benachrichtigungscode (Winuser.h)
description: Wird gesendet, wenn der Pushzustand einer Schaltfläche auf pushed festgelegt ist.
ms.assetid: 34000def-189c-4a37-bcef-4ca09a67df00
keywords:
- BN_PUSHED Benachrichtigungscode Windows Steuerelementen
topic_type:
- apiref
api_name:
- BN_PUSHED
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3d95210ebe5abaddabcc33b908baf1cb2c1498af7446f32d7ebcfa9500ebd329
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118674134"
---
# <a name="bn_pushed-notification-code"></a>BN \_ PUSHED-Benachrichtigungscode

Wird gesendet, wenn der Pushzustand einer Schaltfläche auf pushed festgelegt ist.

> [!Note]  
> Dieser Benachrichtigungscode wird nur zur Kompatibilität mit 16-Bit-Versionen von Windows 3.0 bereitgestellt. Anwendungen sollten den [**BS \_ OWNERDRAW-Schaltflächenstil**](button-styles.md) und die [**DRAWITEMSTRUCT-Struktur**](/windows/win32/api/winuser/ns-winuser-drawitemstruct) für diese Aufgabe verwenden.

 

Das übergeordnete Fenster der Schaltfläche empfängt diesen Benachrichtigungscode über die [**WM \_ COMMAND-Meldung.**](/windows/desktop/menurc/wm-command)


```C++
BN_PUSHED

    WPARAM wParam;
    LPARAM lParam; 
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*wParam* 
</dt> <dd>

Das [**LOWORD enthält**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85)) den Steuerelementbezeichner der Schaltfläche. Das [**HIWORD gibt**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85)) den Benachrichtigungscode an.

</dd> <dt>

*lParam* 
</dt> <dd>

Ein Handle für die Schaltfläche.

</dd> </dl>

## <a name="remarks"></a>Hinweise

BN \_ PUSHED ist mit dem [ \_ BN-HILITE-Benachrichtigungscode](bn-hilite.md) identisch.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows Nur \[ Vista-Desktop-Apps\]<br/>                                                           |
| Unterstützte Mindestversion (Server)<br/> | Windows Nur Server \[ 2003-Desktop-Apps\]<br/>                                                     |
| Header<br/>                   | <dl> <dt>Winuser.h (include Windows.h)</dt> </dl> |



## <a name="see-also"></a>Weitere Informationen:

<dl> <dt>

[**BN \_ UNPUSHED**](bn-unpushed.md)
</dt> </dl>

 

