---
title: BN_HILITE Benachrichtigungscode (Winuser.h)
description: Wird gesendet, wenn der Benutzer eine Schaltfläche auswählt.
ms.assetid: f20ba77e-257c-44ec-a2dd-dbf23cd78d07
keywords:
- BN_HILITE Benachrichtigungscode Windows Steuerelementen
topic_type:
- apiref
api_name:
- BN_HILITE
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e864fff01fcce9c7856ab040f66d12e08524c731b43d343a2e878e15e41e801f
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119827620"
---
# <a name="bn_hilite-notification-code"></a>\_BN-HILITE-Benachrichtigungscode

Wird gesendet, wenn der Benutzer eine Schaltfläche auswählt.

> [!Note]  
> Dieser Benachrichtigungscode wird nur zur Kompatibilität mit 16-Bit-Versionen von Windows 3.0 bereitgestellt. Anwendungen sollten den [**BS \_ OWNERDRAW-Schaltflächenstil**](button-styles.md) und die [**DRAWITEMSTRUCT-Struktur**](/windows/win32/api/winuser/ns-winuser-drawitemstruct) für diese Aufgabe verwenden.

 

Das übergeordnete Fenster der Schaltfläche empfängt diesen Benachrichtigungscode über die [**WM \_ COMMAND-Meldung.**](/windows/desktop/menurc/wm-command)


```C++
BN_HILITE

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

Handle für die Schaltfläche.

</dd> </dl>

## <a name="remarks"></a>Hinweise

BN \_ HILITE ist mit dem [BN \_ PUSHED-Benachrichtigungscode](bn-pushed.md) identisch.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows Nur \[ Vista-Desktop-Apps\]<br/>                                                           |
| Unterstützte Mindestversion (Server)<br/> | Windows Nur Server \[ 2003-Desktop-Apps\]<br/>                                                     |
| Header<br/>                   | <dl> <dt>Winuser.h (include Windows.h)</dt> </dl> |



 

