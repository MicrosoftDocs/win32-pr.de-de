---
title: LVN_DELETEALLITEMS Benachrichtigungscode (Commctrl.h)
description: Benachrichtigt das übergeordnete Fenster eines Listenansicht-Steuerelements, dass alle Elemente im Steuerelement gelöscht werden. Dieser Benachrichtigungscode wird in Form einer WM \_ NOTIFY-Nachricht gesendet.
ms.assetid: e4a219cf-4af9-4d02-8810-f576ba658177
keywords:
- LVN_DELETEALLITEMS Benachrichtigungscode Windows Steuerelementen
topic_type:
- apiref
api_name:
- LVN_DELETEALLITEMS
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 06f76ec4deaf67c1448fab5054c05ea8ede79c0972061c8be8e4f36b2e40ef54
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119019128"
---
# <a name="lvn_deleteallitems-notification-code"></a>LVN \_ DELETEALLITEMS-Benachrichtigungscode

Benachrichtigt das übergeordnete Fenster eines Listenansicht-Steuerelements, dass alle Elemente im Steuerelement gelöscht werden. Dieser Benachrichtigungscode wird in Form einer [**WM \_ NOTIFY-Nachricht**](wm-notify.md) gesendet.


```C++
LVN_DELETEALLITEMS

    pnmv = (LPNMLISTVIEW) lParam; 
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*lParam* 
</dt> <dd>

Zeiger auf eine [**NMLISTVIEW-Struktur.**](/windows/win32/api/commctrl/ns-commctrl-nmlistview) Das **iItem-Member** ist -1, und die anderen Member sind 0 (null).

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Um nachfolgende [LVN \_ DELETEITEM-Benachrichtigungscodes](lvn-deleteitem.md) zu unterdrücken, geben Sie **TRUE zurück.**

Um nachfolgende [LVN \_ DELETEITEM-Benachrichtigungscodes](lvn-deleteitem.md) zu erhalten, geben Sie **FALSE zurück.**

## <a name="remarks"></a>Hinweise

Ein Listenansicht-Steuerelement sendet den [**LVM \_ DELETEALLITEMS-Benachrichtigungscode,**](lvm-deleteallitems.md) wenn es zerstört wird oder wenn es die **LVM \_ DELETEALLITEMS-Nachricht empfängt.** Wenn **LVM \_ DELETEALLITEMS** nicht **TRUE** zurück gibt, sendet das Steuerelement auch einen [LVN DELETEITEM-Benachrichtigungscode, \_](lvn-deleteitem.md) wenn jedes Element gelöscht wird.

Wenn sich der [**LVM \_ DELETEALLITEMS-Meldungshandler**](lvm-deleteallitems.md) in einer Dialogfeldprozedur befindet, geben Sie **TRUE** aus der Dialogfeldprozedur zurück, und verwenden Sie die [**SetWindowLong-Funktion**](/windows/desktop/api/winuser/nf-winuser-setwindowlonga) mit DWL MSGRESULT, um den Rückgabewert der Nachricht zu \_ setzen.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows Nur \[ Vista-Desktop-Apps\]<br/>                                        |
| Unterstützte Mindestversion (Server)<br/> | Windows Nur Server \[ 2003-Desktop-Apps\]<br/>                                  |
| Header<br/>                   | <dl> <dt>Commctrl.h</dt> </dl> |



 

