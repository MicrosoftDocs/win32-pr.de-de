---
title: BN_KILLFOCUS Benachrichtigungs Code (Winuser. h)
description: Wird gesendet, wenn eine Schaltfläche den Tastaturfokus verliert. Die Schaltfläche muss den Typ "b Benachrichtigen" aufweisen \_ , um diesen Benachrichtigungs Code zu senden. Das übergeordnete Fenster der Schaltfläche empfängt diesen Benachrichtigungs Code über die WM- \_ Befehls Meldung.
ms.assetid: 740154ba-47fd-4084-8b86-6166f1e1b39f
keywords:
- Windows-Steuerelemente für BN_KILLFOCUS Benachrichtigungs
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
ms.openlocfilehash: c3fb6737d88ccddedbba6db58ffd0f713da7a8a2
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104475753"
---
# <a name="bn_killfocus-notification-code"></a>BN- \_ killfokus-Benachrichtigungs Code

Wird gesendet, wenn eine Schaltfläche den Tastaturfokus verliert. Die Schaltfläche muss den Typ " [**b \_ Benachrichtigen**](button-styles.md) " aufweisen, um diesen Benachrichtigungs Code zu senden.

Das übergeordnete Fenster der Schaltfläche empfängt diesen Benachrichtigungs Code über die [**WM- \_ Befehls**](/windows/desktop/menurc/wm-command) Meldung.


```C++
BN_KILLFOCUS

    WPARAM wParam;
    LPARAM lParam; 
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*wParam* 
</dt> <dd>

Das [**LoWord**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85)) enthält den Steuerelement Bezeichner der Schaltfläche. Das [**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85)) gibt den Benachrichtigungs Code an.

</dd> <dt>

*lParam* 
</dt> <dd>

Ein Handle für die Schaltfläche.

</dd> </dl>

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Nur Windows Vista \[ -Desktop-Apps\]<br/>                                                           |
| Unterstützte Mindestversion (Server)<br/> | Nur Windows Server 2003 \[ -Desktop-Apps\]<br/>                                                     |
| Header<br/>                   | <dl> <dt>Winuser. h (Windows. h einschließen)</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[BN- \_ SetFocus](bn-setfocus.md)
</dt> </dl>

 

