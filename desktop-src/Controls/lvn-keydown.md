---
title: LVN_KEYDOWN Benachrichtigungs Code (kommctrl. h)
description: Benachrichtigt das übergeordnete Fenster eines Listenansicht-Steuer Elements, dass eine Taste gedrückt wurde. Dieser Benachrichtigungs Code wird in Form einer WM-Benachrichtigungs \_ Meldung gesendet.
ms.assetid: 3aa3d165-7227-41c4-8bc2-3e51a0f52ee3
keywords:
- Windows-Steuerelemente für LVN_KEYDOWN Benachrichtigungs
topic_type:
- apiref
api_name:
- LVN_KEYDOWN
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 516c64e9050a6946d3a135ecc0d00d7e384e9844
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "103957259"
---
# <a name="lvn_keydown-notification-code"></a>LVN- \_ KeyDown-Benachrichtigungs Code

Benachrichtigt das übergeordnete Fenster eines Listenansicht-Steuer Elements, dass eine Taste gedrückt wurde. Dieser Benachrichtigungs Code wird in Form einer WM- [**\_ Benachrichtigungs**](wm-notify.md) Meldung gesendet.


```C++
LVN_KEYDOWN

    pnkd = (LPNMLVKEYDOWN) lParam; 
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*lParam* 
</dt> <dd>

Zeiger auf eine [**nmlvkeydown**](/windows/win32/api/commctrl/ns-commctrl-nmlvkeydown) -Struktur.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Kein Rückgabewert.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Nur Windows Vista \[ -Desktop-Apps\]<br/>                                        |
| Unterstützte Mindestversion (Server)<br/> | Nur Windows Server 2003 \[ -Desktop-Apps\]<br/>                                  |
| Header<br/>                   | <dl> <dt>Kommstrg. h</dt> </dl> |



 

 





