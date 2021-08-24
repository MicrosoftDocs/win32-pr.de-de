---
title: TBN_RESTORE Benachrichtigungscode (Commctrl.h)
description: Benachrichtigt das übergeordnete Fenster einer Symbolleiste, dass gerade eine Symbolleiste wiederhergestellt wird. Dieser Benachrichtigungscode wird in Form einer WM \_ NOTIFY-Nachricht gesendet.
ms.assetid: b1f0c801-d56b-4e93-b9ba-b572aaa38647
keywords:
- TBN_RESTORE Benachrichtigungscode Windows Steuerelementen
topic_type:
- apiref
api_name:
- TBN_RESTORE
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4f267e5cff52eb1a6011b16aa02d63870503478051e72d574da05467c8329f91
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119543499"
---
# <a name="tbn_restore-notification-code"></a>TBN \_ RESTORE-Benachrichtigungscode

Benachrichtigt das übergeordnete Fenster einer Symbolleiste, dass gerade eine Symbolleiste wiederhergestellt wird. Dieser Benachrichtigungscode wird in Form einer [**WM \_ NOTIFY-Nachricht**](wm-notify.md) gesendet.


```C++
TBN_RESTORE 

    lpnmtb = (LPNMTBRESTORE) lParam; 
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*lParam* 
</dt> <dd>

Zeiger auf eine [**NMTBRESTORE-Struktur.**](/windows/win32/api/commctrl/ns-commctrl-nmtbrestore)

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Die Anwendung sollte null als Antwort auf den ersten **TBN \_ RESTORE-Benachrichtigungscode** zurückgeben, der zu Beginn des Wiederherstellungsprozesses empfangen wurde, um die Wiederherstellung der Schaltflächeninformationen fortzufahren. Wenn die Anwendung einen Wert ungleich 0 (null) zurückgibt, wird der Wiederherstellungsvorgang abgebrochen.

## <a name="remarks"></a>Hinweise

Die Anwendung erhält diesen Benachrichtigungscode einmal zu Beginn des Wiederherstellungsprozesses und einmal für jede Schaltfläche. Dieser Benachrichtigungscode bietet Ihnen die Möglichkeit, die Informationen aus dem zuvor gespeicherten Datenstrom zu extrahieren. Wenn Sie keine Informationen gespeichert haben, ignorieren Sie den Benachrichtigungscode. Eine [ausführlichere Erläuterung der](toolbar-controls-overview.md) Behandlung von TBN RESTORE finden Sie unter Anpassung der **\_ Symbolleiste.**

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows Nur \[ Vista-Desktop-Apps\]<br/>                                        |
| Unterstützte Mindestversion (Server)<br/> | Windows Nur Server \[ 2003-Desktop-Apps\]<br/>                                  |
| Header<br/>                   | <dl> <dt>Commctrl.h</dt> </dl> |



 

 





