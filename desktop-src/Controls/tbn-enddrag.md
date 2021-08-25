---
title: TBN_ENDDRAG Benachrichtigungscode (Commctrl.h)
description: Benachrichtigt das übergeordnete Fenster der Symbolleiste, dass der Benutzer das Ziehen einer Schaltfläche auf einer Symbolleiste beendet hat. Dieser Benachrichtigungscode wird in Form einer WM \_ NOTIFY-Nachricht gesendet.
ms.assetid: 846ba42e-6e0d-45bb-88ce-7b4d2cb17e13
keywords:
- TBN_ENDDRAG Benachrichtigungscode Windows-Steuerelemente
topic_type:
- apiref
api_name:
- TBN_ENDDRAG
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: fff6cfff7448f452223681ef1ebf720e0330c1fee52ba48862411978d53a0616
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119876870"
---
# <a name="tbn_enddrag-notification-code"></a>TBN \_ ENDDRAG-Benachrichtigungscode

Benachrichtigt das übergeordnete Fenster der Symbolleiste, dass der Benutzer das Ziehen einer Schaltfläche auf einer Symbolleiste beendet hat. Dieser Benachrichtigungscode wird in Form einer [**WM \_ NOTIFY-Nachricht**](wm-notify.md) gesendet.


```C++
TBN_ENDDRAG 

    lpnmtb = (LPNMTOOLBAR) lParam; 
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*lParam* 
</dt> <dd>

Zeiger auf eine [**NMTOOLBAR-Struktur.**](/windows/win32/api/commctrl/ns-commctrl-nmtoolbara) Das **iItem-Element** enthält den Befehlsbezeichner der gezogenen Schaltfläche.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Kein Rückgabewert.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows \[Nur Vista-Desktop-Apps\]<br/>                                        |
| Unterstützte Mindestversion (Server)<br/> | Windows Nur Server \[ 2003-Desktop-Apps\]<br/>                                  |
| Header<br/>                   | <dl> <dt>Commctrl.h</dt> </dl> |



 

 





