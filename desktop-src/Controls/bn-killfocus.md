---
title: BN_KILLFOCUS Benachrichtigungscode (Winuser.h)
description: Wird gesendet, wenn eine Schaltfläche den Tastaturfokus verliert. Die Schaltfläche muss das Format BS \_ NOTIFY aufweisen, um diesen Benachrichtigungscode zu senden. Das übergeordnete Fenster der Schaltfläche empfängt diesen Benachrichtigungscode über die WM \_ COMMAND-Meldung.
ms.assetid: 740154ba-47fd-4084-8b86-6166f1e1b39f
keywords:
- BN_KILLFOCUS Benachrichtigungscode Windows-Steuerelemente
topic_type:
- apiref
api_name:
- BN_KILLFOCUS
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8f312ba2282c72b7db30c170b44528bd469591bbb0a4b4a2e14bb797d2be67f4
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118674086"
---
# <a name="bn_killfocus-notification-code"></a>BN \_ KILLFOCUS-Benachrichtigungscode

Wird gesendet, wenn eine Schaltfläche den Tastaturfokus verliert. Die Schaltfläche muss das [**Format BS \_ NOTIFY**](button-styles.md) aufweisen, um diesen Benachrichtigungscode zu senden.

Das übergeordnete Fenster der Schaltfläche empfängt diesen Benachrichtigungscode über die [**WM \_ COMMAND-Meldung.**](/windows/desktop/menurc/wm-command)


```C++
BN_KILLFOCUS

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

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows \[Nur Vista-Desktop-Apps\]<br/>                                                           |
| Unterstützte Mindestversion (Server)<br/> | Windows Nur Server \[ 2003-Desktop-Apps\]<br/>                                                     |
| Header<br/>                   | <dl> <dt>Winuser.h (include Windows.h)</dt> </dl> |



## <a name="see-also"></a>Weitere Informationen:

<dl> <dt>

[BN \_ SETFOCUS](bn-setfocus.md)
</dt> </dl>

 

