---
title: RBN_ENDDRAG Benachrichtigungscode (Commctrl.h)
description: Wird von einem Rebar-Steuerelement gesendet, wenn der Benutzer das Ziehen eines Bands beendet. Dieser Benachrichtigungscode wird in Form einer WM \_ NOTIFY-Nachricht gesendet.
ms.assetid: 24b06144-6a4c-46a4-bef1-d6592f72a2c0
keywords:
- RBN_ENDDRAG Benachrichtigungscode Windows-Steuerelemente
topic_type:
- apiref
api_name:
- RBN_ENDDRAG
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5c09831672d61c824a1c8cea30b3ba3731d4ad589cc98c88ce3830586cb342cd
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119985060"
---
# <a name="rbn_enddrag-notification-code"></a>RBN \_ ENDDRAG-Benachrichtigungscode

Wird von einem Rebar-Steuerelement gesendet, wenn der Benutzer das Ziehen eines Bands beendet. Dieser Benachrichtigungscode wird in Form einer [**WM \_ NOTIFY-Nachricht**](wm-notify.md) gesendet.


```C++
RBN_ENDDRAG

    lpnmrb = (LPNMREBAR) lParam;
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*lParam* 
</dt> <dd>

Zeiger auf eine [**NMREBAR-Struktur,**](/windows/win32/api/commctrl/ns-commctrl-nmrebar) die Informationen zum Benachrichtigungscode enthält.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Der Rückgabewert für diesen Benachrichtigungscode wird nicht verwendet.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows \[Nur Vista-Desktop-Apps\]<br/>                                        |
| Unterstützte Mindestversion (Server)<br/> | Windows Nur Server \[ 2003-Desktop-Apps\]<br/>                                  |
| Header<br/>                   | <dl> <dt>Commctrl.h</dt> </dl> |



 

 





