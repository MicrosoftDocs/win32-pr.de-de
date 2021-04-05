---
title: LBN_SETFOCUS Benachrichtigungs Code (Winuser. h)
description: Benachrichtigt die Anwendung, dass das Listenfeld den Tastaturfokus erhalten hat. Das übergeordnete Fenster des Listen Felds empfängt diesen Benachrichtigungs Code über die WM- \_ Befehls Meldung.
ms.assetid: d9e5e035-98a5-4ece-ba40-6d341c101859
keywords:
- Windows-Steuerelemente für LBN_SETFOCUS Benachrichtigungs
topic_type:
- apiref
api_name:
- LBN_SETFOCUS
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 88e56043982cec6606f7c78d3469ab2583951f88
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "103858913"
---
# <a name="lbn_setfocus-notification-code"></a>LBN- \_ SetFocus-Benachrichtigungs Code

Benachrichtigt die Anwendung, dass das Listenfeld den Tastaturfokus erhalten hat. Das übergeordnete Fenster des Listen Felds empfängt diesen Benachrichtigungs Code über die [**WM- \_ Befehls**](/windows/desktop/menurc/wm-command) Meldung.


```C++
LBN_SETFOCUS

    WPARAM wParam;
    LPARAM lParam; 
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*wParam* 
</dt> <dd>

Das [**LoWord**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85)) enthält den Bezeichner des Listen Felds. Das [**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85)) gibt den Benachrichtigungs Code an.

</dd> <dt>

*lParam* 
</dt> <dd>

Handle für das Listenfeld.

</dd> </dl>

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Nur Windows Vista \[ -Desktop-Apps\]<br/>                                                           |
| Unterstützte Mindestversion (Server)<br/> | Nur Windows Server 2003 \[ -Desktop-Apps\]<br/>                                                     |
| Header<br/>                   | <dl> <dt>Winuser. h (Windows. h einschließen)</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

**Verweis**
</dt> <dt>

[LBN- \_ killfokus](lbn-killfocus.md)
</dt> <dt>

**Andere Ressourcen**
</dt> <dt>

[**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85))
</dt> <dt>

[**LOWORD**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85))
</dt> <dt>

[**WM- \_ Befehl**](/windows/desktop/menurc/wm-command)
</dt> </dl>

 

