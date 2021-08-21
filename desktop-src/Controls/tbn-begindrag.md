---
title: TBN_BEGINDRAG Benachrichtigungscode (Commctrl.h)
description: Benachrichtigt das übergeordnete Fenster einer Symbolleiste, dass der Benutzer damit begonnen hat, eine Schaltfläche in eine Symbolleiste zu ziehen. Dieser Benachrichtigungscode wird in Form einer WM \_ NOTIFY-Nachricht gesendet.
ms.assetid: 244406e5-e13d-4c80-81fa-81b018b29ec1
keywords:
- TBN_BEGINDRAG Benachrichtigungscode Windows Steuerelementen
topic_type:
- apiref
api_name:
- TBN_BEGINDRAG
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5283b2853709742713f79afb761cc39739f6df7467a1de869c545c705c8488ca
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119077974"
---
# <a name="tbn_begindrag-notification-code"></a>TBN \_ BEGINDRAG-Benachrichtigungscode

Benachrichtigt das übergeordnete Fenster einer Symbolleiste, dass der Benutzer damit begonnen hat, eine Schaltfläche in eine Symbolleiste zu ziehen. Dieser Benachrichtigungscode wird in Form einer [**WM \_ NOTIFY-Nachricht**](wm-notify.md) gesendet.


```C++
TBN_BEGINDRAG 

    lpnmtb = (LPNMTOOLBAR) lParam; 
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*lParam* 
</dt> <dd>

Zeiger auf eine [**NMTOOLBAR-Struktur.**](/windows/win32/api/commctrl/ns-commctrl-nmtoolbara) Das **iItem-Member** enthält den Befehlsbezeichner der zu ziehenden Schaltfläche.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Kein Rückgabewert.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows Nur \[ Vista-Desktop-Apps\]<br/>                                        |
| Unterstützte Mindestversion (Server)<br/> | Windows Nur Server \[ 2003-Desktop-Apps\]<br/>                                  |
| Header<br/>                   | <dl> <dt>Commctrl.h</dt> </dl> |



 

 





