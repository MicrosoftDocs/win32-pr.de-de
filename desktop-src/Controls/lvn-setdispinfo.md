---
title: LVN_SETDISPINFO Benachrichtigungscode (Commctrl.h)
description: Benachrichtigt das übergeordnete Fenster eines Listenansichtssteuerelements, dass es die für ein Element verwalteten Informationen aktualisieren muss. Dieser Benachrichtigungscode wird in Form einer WM \_ NOTIFY-Nachricht gesendet.
ms.assetid: 1ea51d50-4a57-4662-972e-89e916fa9b16
keywords:
- LVN_SETDISPINFO Benachrichtigungscode Windows Controls
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
ms.openlocfilehash: 6f4827d37a115f2bd1bb523f78bdb5975de4314056a174be4bfa886e1a076497
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119915060"
---
# <a name="lvn_setdispinfo-notification-code"></a>LVN \_ SETDISPINFO-Benachrichtigungscode

Benachrichtigt das übergeordnete Fenster eines Listenansichtssteuerelements, dass es die für ein Element verwalteten Informationen aktualisieren muss. Dieser Benachrichtigungscode wird in Form einer [**WM \_ NOTIFY-Nachricht**](wm-notify.md) gesendet.


```C++
LVN_SETDISPINFO
        
    pdi = (NMLVDISPINFO*) lParam
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*lParam* 
</dt> <dd>

Zeiger auf eine [**NMLVDISPINFO-Struktur,**](/windows/win32/api/commctrl/ns-commctrl-nmlvdispinfoa) die Informationen für das geänderte Element angibt. Der **Elementmember** dieser Struktur ist eine [**LVITEM-Struktur,**](/windows/win32/api/commctrl/ns-commctrl-lvitema) die Informationen über das geänderte Element enthält. Der **pszText-Member** des **Elements** enthält einen gültigen Wert, unabhängig davon, ob das LVIF \_ TEXT-Flag im **Maskenmember** dieser Struktur festgelegt ist.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Kein Rückgabewert.

## <a name="remarks"></a>Hinweise

Der Benachrichtigungsempfänger castt *lParam,* um die [**NMLVDISPINFO-Struktur**](/windows/win32/api/commctrl/ns-commctrl-nmlvdispinfoa) abzurufen. Der *wParam-Parameter* enthält den Nachrichtencode.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows \[Nur Vista-Desktop-Apps\]<br/>                                        |
| Unterstützte Mindestversion (Server)<br/> | Windows Nur Server \[ 2003-Desktop-Apps\]<br/>                                  |
| Header<br/>                   | <dl> <dt>Commctrl.h</dt> </dl> |
| Unicode- und ANSI-Name<br/>   | **LVN \_ SETDISPINFOW** (Unicode) und **LVN \_ SETDISPINFOA** (ANSI)<br/>           |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[LVN \_ GETDISPINFO](lvn-getdispinfo.md)
</dt> </dl>

 

 





