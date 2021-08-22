---
title: NM_CLICK -Benachrichtigungscode (Listenansicht) (Commctrl.h)
description: Wird von einem Listenansichtssteuerelement gesendet, wenn der Benutzer mit der linken Maustaste auf ein Element klickt. Dieser Benachrichtigungscode wird in Form einer WM \_ NOTIFY-Nachricht gesendet.
ms.assetid: 7921bc27-54ca-4bb2-ac88-8267776661ab
keywords:
- NM_CLICK -Benachrichtigungscode (Listenansicht) Windows-Steuerelemente
topic_type:
- apiref
api_name:
- NM_CLICK
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1e9189861db0ec956b549145584202e3b88978478a9dd8de4386785d46e0d160
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "120061760"
---
# <a name="nm_click-list-view-notification-code"></a>NM \_ CLICK-Benachrichtigungscode (Listenansicht)

Wird von einem Listenansichtssteuerelement gesendet, wenn der Benutzer mit der linken Maustaste auf ein Element klickt. Dieser Benachrichtigungscode wird in Form einer [**WM \_ NOTIFY-Nachricht**](wm-notify.md) gesendet.


```C++
NM_CLICK

    lpnmitem = (LPNMITEMACTIVATE) lParam;
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*lParam* 
</dt> <dd>

[Version 4.71.](common-control-versions.md) Zeiger auf eine [**NMITEMACTIVATE-Struktur,**](/windows/win32/api/commctrl/ns-commctrl-nmitemactivate) die zusätzliche Informationen zu dieser Benachrichtigung enthält. Die **Member iItem,** **iSubItem** und **ptAction** dieser Struktur enthalten Informationen über das Element.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Der Rückgabewert für diese Benachrichtigung wird nicht verwendet.

## <a name="remarks"></a>Hinweise

Das **iItem-Element** von *lParam* ist nur gültig, wenn auf das Symbol oder die Bezeichnung der ersten Spalte geklickt wurde. Um zu bestimmen, welches Element ausgewählt wird, wenn ein Klick an anderer Stelle in einer Zeile erfolgt, senden Sie eine [**LVM \_ SUBITEMHITTEST-Nachricht.**](lvm-subitemhittest.md)

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows \[Nur Vista-Desktop-Apps\]<br/>                                        |
| Unterstützte Mindestversion (Server)<br/> | Windows Nur Server \[ 2003-Desktop-Apps\]<br/>                                  |
| Header<br/>                   | <dl> <dt>Commctrl.h</dt> </dl> |



 

 





