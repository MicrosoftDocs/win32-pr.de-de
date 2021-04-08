---
title: NM_SETCURSOR (ComboBoxEx)-Benachrichtigungs Code (kommctrl. h)
description: Benachrichtigt das übergeordnete Fenster eines ComboBoxEx-Steuer Elements, dass das-Steuerelement den Cursor als Antwort auf eine WM- \_ SetCursor-Nachricht festlegt. Dieser Benachrichtigungs Code wird in Form einer WM-Benachrichtigungs \_ Meldung gesendet.
ms.assetid: a1c617fa-8eb2-444f-88d1-9913de7a42d1
keywords:
- NM_SETCURSOR (ComboBoxEx)-Benachrichtigungs Code Windows-Steuerelemente
topic_type:
- apiref
api_name:
- NM_SETCURSOR
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5fbd5e10f06e74af0778521d31c69e63586a6476
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "103742665"
---
# <a name="nm_setcursor-comboboxex-notification-code"></a>NM \_ setcursor (ComboBoxEx)-Benachrichtigungs Code

Benachrichtigt das übergeordnete Fenster eines ComboBoxEx-Steuer Elements, dass das-Steuerelement den Cursor als Antwort auf eine [**WM- \_ SetCursor**](/windows/desktop/menurc/wm-setcursor) -Nachricht festlegt. Dieser Benachrichtigungs Code wird in Form einer WM- [**\_ Benachrichtigungs**](wm-notify.md) Meldung gesendet.


```C++
NM_SETCURSOR

    lpnmm = (LPNMMOUSE) lParam; 
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*lParam* 
</dt> <dd>

Ein Zeiger auf eine [**nmmouse**](/windows/win32/api/commctrl/ns-commctrl-nmmouse) -Struktur, die zusätzliche Informationen zu dieser Benachrichtigung enthält.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Gibt 0 (null) zurück, damit das Steuerelement den Cursor festlegen kann, um zu verhindern, dass das Steuerelement den Cursor festlegt.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Nur Windows Vista \[ -Desktop-Apps\]<br/>                                        |
| Unterstützte Mindestversion (Server)<br/> | Nur Windows Server 2003 \[ -Desktop-Apps\]<br/>                                  |
| Header<br/>                   | <dl> <dt>Kommstrg. h</dt> </dl> |



 

