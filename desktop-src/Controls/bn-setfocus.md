---
title: BN_SETFOCUS Benachrichtigungs Code (Winuser. h)
description: Wird gesendet, wenn eine Schaltfläche den Tastaturfokus erhält. Die Schaltfläche muss den Typ "b Benachrichtigen" aufweisen \_ , um diesen Benachrichtigungs Code zu senden. Das übergeordnete Fenster der Schaltfläche empfängt diesen Benachrichtigungs Code über die WM- \_ Befehls Meldung.
ms.assetid: 6b8d9bde-67f9-454f-ba2c-e5c8d9ff2709
keywords:
- Windows-Steuerelemente für BN_SETFOCUS Benachrichtigungs
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
ms.openlocfilehash: 3eb9204f5b23b62b6cee9fb2652a16d546f6ef62
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "106339944"
---
# <a name="bn_setfocus-notification-code"></a>BN- \_ SetFocus-Benachrichtigungs Code

Wird gesendet, wenn eine Schaltfläche den Tastaturfokus erhält. Die Schaltfläche muss den Typ " [**b \_ Benachrichtigen**](button-styles.md) " aufweisen, um diesen Benachrichtigungs Code zu senden.

Das übergeordnete Fenster der Schaltfläche empfängt diesen Benachrichtigungs Code über die [**WM- \_ Befehls**](/windows/desktop/menurc/wm-command) Meldung.


```C++
BN_SETFOCUS

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

[BN- \_ killfokus](bn-killfocus.md)
</dt> </dl>

 

