---
title: TBN_DRAGOVER Benachrichtigungscode (Commctrl.h)
description: Ermittelt, ob eine TB MARKBUTTON-Nachricht für eine Schaltfläche gesendet werden \_ soll, die gezogen wird. Dieser Benachrichtigungscode wird in Form einer WM \_ NOTIFY-Nachricht gesendet.
ms.assetid: 2bb5c52e-0c90-4662-8ffd-045ecc7ed7e5
keywords:
- TBN_DRAGOVER Benachrichtigungscode Windows Steuerelementen
topic_type:
- apiref
api_name:
- TBN_DRAGOVER
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 718a51f14f096edbd8df72b0c5fc33ca65ec0c303a095f108981482c9fb3cda5
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "117829344"
---
# <a name="tbn_dragover-notification-code"></a>TBN \_ DRAGOVER-Benachrichtigungscode

Ermittelt, ob eine [**TB \_ MARKBUTTON-Nachricht**](tb-markbutton.md) für eine Schaltfläche gesendet werden soll, die gezogen wird. Dieser Benachrichtigungscode wird in Form einer [**WM \_ NOTIFY-Nachricht**](wm-notify.md) gesendet.


```C++
TBN_DRAGOVER

    lpnmtb = (NMTBHOTITEM*) lParam; 
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*lParam* 
</dt> <dd>

Ein Zeiger auf eine [**NMTBHOTITEM-Struktur,**](/windows/win32/api/commctrl/ns-commctrl-nmtbhotitem) der angibt, welches Element gezogen wird.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

**FALSE,** wenn die Symbolleiste eine TB \_ MARKBUTTON-Nachricht senden soll, **andernfalls TRUE**.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows Nur \[ Vista-Desktop-Apps\]<br/>                                        |
| Unterstützte Mindestversion (Server)<br/> | Windows Nur Server \[ 2003-Desktop-Apps\]<br/>                                  |
| Header<br/>                   | <dl> <dt>Commctrl.h</dt> </dl> |



 

 





