---
title: TBN_WRAPHOTITEM Benachrichtigungscode (Commctrl.h)
description: Benachrichtigt eine Anwendung mit zwei oder mehr Symbolleisten, dass sich das heiße Element ändern wird. Dieser Benachrichtigungscode wird in Form einer WM \_ NOTIFY-Nachricht gesendet.
ms.assetid: 169309ec-68dd-4cbb-8963-f842cf75b4fc
keywords:
- TBN_WRAPHOTITEM Benachrichtigungscode Windows Steuerelementen
topic_type:
- apiref
api_name:
- TBN_WRAPHOTITEM
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 33c6bd1f2e750a2fd71dc053d31ca452fa581891037db73d356e5405476b28de
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119293361"
---
# <a name="tbn_wraphotitem-notification-code"></a>TBN \_ WRAPHOTITEM-Benachrichtigungscode

Benachrichtigt eine Anwendung mit zwei oder mehr Symbolleisten, dass sich das heiße Element ändern wird. Dieser Benachrichtigungscode wird in Form einer [**WM \_ NOTIFY-Nachricht**](wm-notify.md) gesendet.


```C++
TBN_WRAPHOTITEM

    lpnmtb = (NMTBWRAPHOTITEM) lParam; 
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*lParam* 
</dt> <dd>

Ein Zeiger auf eine -Struktur, die das alte heiße Element (**iStart**) enthält und ob sich das neue heiße Element vor ihm befindet (**iDir** = -1) oder danach (**iDir** = 1), sowie ein Grund, warum sich das heiße Element ändert.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

**TRUE,** wenn die Anwendung die Änderung des heißen Elements selbst umwandelt; **andernfalls FALSE**.

## <a name="remarks"></a>Hinweise

Die **NMTBWRAPHOTITEM-Struktur** muss von der Anwendung wie folgt definiert werden:

``` syntax
typedef struct tagNMTBWRAPHOTITEM {
    NMHDR hdr;
    int iStart;
    int iDir;
    UINT nReason;       // HICF_* flags
} NMTBWRAPHOTITEM, *LPNMTBWRAPHOTITEM;
```

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows Nur \[ Vista-Desktop-Apps\]<br/>                                        |
| Unterstützte Mindestversion (Server)<br/> | Windows Nur Server \[ 2003-Desktop-Apps\]<br/>                                  |
| Header<br/>                   | <dl> <dt>Commctrl.h</dt> </dl> |



 

 





