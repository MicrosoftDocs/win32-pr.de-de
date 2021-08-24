---
title: LVN_COLUMNCLICK Benachrichtigungscode (Commctrl.h)
description: Benachrichtigt das übergeordnete Fenster eines Listenansicht-Steuerelements, dass auf eine Spaltenüberschrift geklickt wurde, während sich das Listenansicht-Steuerelement im Berichtsmodus befindet. Dieser Benachrichtigungscode wird in Form einer WM \_ NOTIFY-Nachricht gesendet.
ms.assetid: a6bfbd6c-4778-47a7-92e9-9140d46d89cc
keywords:
- LVN_COLUMNCLICK Benachrichtigungscode Windows Steuerelementen
topic_type:
- apiref
api_name:
- LVN_COLUMNCLICK
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 74cd88674b10a799f58fd0549a6711f3d00934f7b1baaf892cff86c6ef223d19
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119319810"
---
# <a name="lvn_columnclick-notification-code"></a>LVN \_ COLUMNCLICK-Benachrichtigungscode

Benachrichtigt das übergeordnete Fenster eines Listenansicht-Steuerelements, dass auf eine Spaltenüberschrift geklickt wurde, während sich das Listenansicht-Steuerelement im Berichtsmodus befindet. Dieser Benachrichtigungscode wird in Form einer [**WM \_ NOTIFY-Nachricht**](wm-notify.md) gesendet.


```C++
LVN_COLUMNCLICK

    pnmv = (LPNMLISTVIEW) lParam; 
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*lParam* 
</dt> <dd>

Zeiger auf eine [**NMLISTVIEW-Struktur.**](/windows/win32/api/commctrl/ns-commctrl-nmlistview) Das **iItem-Member** ist -1, und das **iSubItem-Member** identifiziert die Spalte. Alle anderen Member sind 0 (null).

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Kein Rückgabewert.

## <a name="remarks"></a>Hinweise

Die Verwendung von Headersteuerelementformaten wie HDF CHECKBOX zum Ändern des Formats von Spaltenüberschriften in einem Listenansichtssteuerelement bewirkt, dass das Steuerelement den \_ [HDN \_ ITEMSTATEICONCLICK-Benachrichtigungscode](hdn-itemstateiconclick.md) anstelle von LVN COLUMNCLICK sendet, wenn auf ein Headerelement geklickt \_ wird.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows Nur \[ Vista-Desktop-Apps\]<br/>                                        |
| Unterstützte Mindestversion (Server)<br/> | Windows Nur Server \[ 2003-Desktop-Apps\]<br/>                                  |
| Header<br/>                   | <dl> <dt>Commctrl.h</dt> </dl> |



 

 





