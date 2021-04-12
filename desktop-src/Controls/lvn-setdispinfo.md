---
title: LVN_SETDISPINFO Benachrichtigungs Code (kommctrl. h)
description: Benachrichtigt das übergeordnete Fenster eines Listenansicht-Steuer Elements, dass die Informationen, die für ein Element verwaltet werden, aktualisiert werden müssen. Dieser Benachrichtigungs Code wird in Form einer WM-Benachrichtigungs \_ Meldung gesendet.
ms.assetid: 1ea51d50-4a57-4662-972e-89e916fa9b16
keywords:
- Windows-Steuerelemente für LVN_SETDISPINFO Benachrichtigungs
topic_type:
- apiref
api_name:
- LVN_SETDISPINFO
- LVN_SETDISPINFOA
- LVN_SETDISPINFOW
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 659623d892f0f5a556f4890703d4e0dd725536b5
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "103956820"
---
# <a name="lvn_setdispinfo-notification-code"></a>LVN \_ setdispinfo-Benachrichtigungs Code

Benachrichtigt das übergeordnete Fenster eines Listenansicht-Steuer Elements, dass die Informationen, die für ein Element verwaltet werden, aktualisiert werden müssen. Dieser Benachrichtigungs Code wird in Form einer WM- [**\_ Benachrichtigungs**](wm-notify.md) Meldung gesendet.


```C++
LVN_SETDISPINFO
        
    pdi = (NMLVDISPINFO*) lParam
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*lParam* 
</dt> <dd>

Ein Zeiger auf eine [**nmlvdispinfo**](/windows/win32/api/commctrl/ns-commctrl-nmlvdispinfoa) -Struktur, die Informationen für das geänderte Element angibt. Das **Element Element** dieser Struktur ist eine [**lvitem**](/windows/win32/api/commctrl/ns-commctrl-lvitema) -Struktur, die Informationen über das geänderte Element enthält. Der **pszText** -Member des **Elements** enthält einen gültigen Wert, unabhängig davon, ob das lvif- \_ textflag im **Mask** -Member dieser Struktur festgelegt ist.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Kein Rückgabewert.

## <a name="remarks"></a>Bemerkungen

Der Benachrichtigungs Empfänger wandelt *LPARAM* ein, um die [**nmlvdispinfo**](/windows/win32/api/commctrl/ns-commctrl-nmlvdispinfoa) -Struktur abzurufen. Der *wParam* -Parameter enthält den Nachrichten Code.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Nur Windows Vista \[ -Desktop-Apps\]<br/>                                        |
| Unterstützte Mindestversion (Server)<br/> | Nur Windows Server 2003 \[ -Desktop-Apps\]<br/>                                  |
| Header<br/>                   | <dl> <dt>Kommstrg. h</dt> </dl> |
| Unicode- und ANSI-Name<br/>   | **LVN \_ Setdispinfow** (Unicode) und **LVN \_ setdispinfoa** (ANSI)<br/>           |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[LVN \_ getdispinfo](lvn-getdispinfo.md)
</dt> </dl>

 

 





