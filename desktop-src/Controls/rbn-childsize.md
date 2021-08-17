---
title: RBN_CHILDSIZE Benachrichtigungscode (Commctrl.h)
description: Wird von einem Rebar-Steuerelement gesendet, wenn die Größe des untergeordneten Fensters eines Bandes geändert wird. Dieser Benachrichtigungscode wird in Form einer WM \_ NOTIFY-Nachricht gesendet.
ms.assetid: ba64d21a-e568-4894-8007-be644ae4f54a
keywords:
- RBN_CHILDSIZE Benachrichtigungscode Windows Steuerelementen
topic_type:
- apiref
api_name:
- RBN_CHILDSIZE
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3450b0c94d4c625d866a25fb5d319b2f0957bef58c6e46296a498ecf3803f764
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119985280"
---
# <a name="rbn_childsize-notification-code"></a>RBN \_ CHILDSIZE-Benachrichtigungscode

Wird von einem Rebar-Steuerelement gesendet, wenn die Größe des untergeordneten Fensters eines Bandes geändert wird. Dieser Benachrichtigungscode wird in Form einer [**WM \_ NOTIFY-Nachricht**](wm-notify.md) gesendet.


```C++
RBN_CHILDSIZE

    lprbcs = (LPNMREBARCHILDSIZE) lParam;
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*lParam* 
</dt> <dd>

Zeiger auf eine [**NMREBARCHILDSIZE-Struktur,**](/windows/win32/api/commctrl/ns-commctrl-nmrebarchildsize) die Informationen zum Benachrichtigungscode enthält.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Der Rückgabewert für diese Benachrichtigung wird nicht verwendet.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows Nur \[ Vista-Desktop-Apps\]<br/>                                        |
| Unterstützte Mindestversion (Server)<br/> | Windows Nur Server \[ 2003-Desktop-Apps\]<br/>                                  |
| Header<br/>                   | <dl> <dt>Commctrl.h</dt> </dl> |



 

 





