---
title: BN_SETFOCUS Benachrichtigungscode (Winuser.h)
description: Wird gesendet, wenn eine Schaltfläche den Tastaturfokus erhält. Die Schaltfläche muss den Stil BS \_ NOTIFY haben, um diesen Benachrichtigungscode zu senden. Das übergeordnete Fenster der Schaltfläche empfängt diesen Benachrichtigungscode über die WM \_ COMMAND-Meldung.
ms.assetid: 6b8d9bde-67f9-454f-ba2c-e5c8d9ff2709
keywords:
- BN_SETFOCUS Benachrichtigungscode Windows Steuerelementen
topic_type:
- apiref
api_name:
- BN_SETFOCUS
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2a10cb9b728d6f98f984ff6b70fb76c42102d8414d486cdba3db27b3ac6fbe99
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119827590"
---
# <a name="bn_setfocus-notification-code"></a>BN \_ SETFOCUS-Benachrichtigungscode

Wird gesendet, wenn eine Schaltfläche den Tastaturfokus erhält. Die Schaltfläche muss den [**Stil BS \_ NOTIFY**](button-styles.md) haben, um diesen Benachrichtigungscode zu senden.

Das übergeordnete Fenster der Schaltfläche empfängt diesen Benachrichtigungscode über die [**WM \_ COMMAND-Meldung.**](/windows/desktop/menurc/wm-command)


```C++
BN_SETFOCUS

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

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows Nur \[ Vista-Desktop-Apps\]<br/>                                                           |
| Unterstützte Mindestversion (Server)<br/> | Windows Nur Server \[ 2003-Desktop-Apps\]<br/>                                                     |
| Header<br/>                   | <dl> <dt>Winuser.h (include Windows.h)</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[BN \_ KILLFOCUS](bn-killfocus.md)
</dt> </dl>

 

