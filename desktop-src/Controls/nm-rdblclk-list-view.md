---
title: NM_RDBLCLK (Listenansicht) Benachrichtigungscode (Commctrl.h)
description: Wird von einem Listenansicht-Steuerelement gesendet, wenn der Benutzer mit der rechten Maustaste auf ein Element doppelklickt. Dieser Benachrichtigungscode wird in Form einer WM \_ NOTIFY-Nachricht gesendet.
ms.assetid: ebbb127f-07bd-48e0-bf38-7bbda5802f70
keywords:
- NM_RDBLCLK -Benachrichtigungscode (Listenansicht) Windows Controls
topic_type:
- apiref
api_name:
- NM_RDBLCLK
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9c0197659f89392d352e2500d37cbda9dadee5487c5ee180123f502d127925a9
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118957989"
---
# <a name="nm_rdblclk-list-view-notification-code"></a>NM \_ RDBLCLK-Benachrichtigungscode (Listenansicht)

Wird von einem Listenansicht-Steuerelement gesendet, wenn der Benutzer mit der rechten Maustaste auf ein Element doppelklickt. Dieser Benachrichtigungscode wird in Form einer [**WM \_ NOTIFY-Nachricht**](wm-notify.md) gesendet.


```C++
NM_RDBLCLK

    lpnmitem = (LPNMITEMACTIVATE) lParam;
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*lParam* 
</dt> <dd>

[Version 4.71](common-control-versions.md). Zeiger auf eine [**NMITEMACTIVATE-Struktur,**](/windows/win32/api/commctrl/ns-commctrl-nmitemactivate) die zusätzliche Informationen zu dieser Benachrichtigung enthält. Die **Member iItem,** **iSubItem** und **ptAction** dieser Struktur enthalten Informationen zum Element.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Der Rückgabewert für diese Benachrichtigung wird nicht verwendet.

## <a name="remarks"></a>Hinweise

Das **iItem-Member** *von lParam* ist nur gültig, wenn auf das Symbol oder die Bezeichnung der ersten Spalte geklickt wurde. Um zu bestimmen, welches Element ausgewählt wird, wenn ein Klick an anderer Stelle in einer Zeile erfolgt, senden Sie eine [**LVM \_ SUBITEMHITTEST-Nachricht.**](lvm-subitemhittest.md)

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows Nur \[ Vista-Desktop-Apps\]<br/>                                        |
| Unterstützte Mindestversion (Server)<br/> | Windows Nur Server \[ 2003-Desktop-Apps\]<br/>                                  |
| Header<br/>                   | <dl> <dt>Commctrl.h</dt> </dl> |



 

 





