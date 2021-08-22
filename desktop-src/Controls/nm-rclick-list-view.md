---
title: NM_RCLICK (Listenansicht) Benachrichtigungscode (Commctrl.h)
description: Wird von einem Listenansicht-Steuerelement gesendet, wenn der Benutzer mit der rechten Maustaste auf ein Element klickt. Dieser Benachrichtigungscode wird in Form einer WM \_ NOTIFY-Nachricht gesendet.
ms.assetid: dc7f97b3-4aec-4a8f-a87c-62cef5ba4c40
keywords:
- NM_RCLICK -Benachrichtigungscode (Listenansicht) Windows Steuerelemente
topic_type:
- apiref
api_name:
- NM_RCLICK
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f58ab6b2496c35bb4b95a3808afb7e58b961584b8b72d086933ad2c3281e6f29
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119018808"
---
# <a name="nm_rclick-list-view-notification-code"></a>NM \_ RCLICK-Benachrichtigungscode (Listenansicht)

Wird von einem Listenansicht-Steuerelement gesendet, wenn der Benutzer mit der rechten Maustaste auf ein Element klickt. Dieser Benachrichtigungscode wird in Form einer [**WM \_ NOTIFY-Nachricht**](wm-notify.md) gesendet.


```C++
NM_RCLICK

    lpnmitem = (LPNMITEMACTIVATE) lParam;
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*lParam* 
</dt> <dd>

[Version 4.71](common-control-versions.md). Zeiger auf eine [**NMITEMACTIVATE-Struktur,**](/windows/win32/api/commctrl/ns-commctrl-nmitemactivate) die zusätzliche Informationen zu dieser Benachrichtigung enthält. Die **Member iItem,** **iSubItem** und **ptAction** dieser Struktur enthalten Informationen zum Element.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Geben Sie einen Wert ungleich 0 (null) zurück, um die Standardverarbeitung nicht zu erlauben, oder 0 (null), um die Standardverarbeitung zu ermöglichen.

## <a name="remarks"></a>Hinweise

Das **iItem-Member** *von lParam* ist nur gültig, wenn auf das Symbol oder die Bezeichnung der ersten Spalte geklickt wurde. Um zu bestimmen, welches Element ausgewählt wird, wenn ein Klick an anderer Stelle in einer Zeile erfolgt, senden Sie eine [**LVM \_ SUBITEMHITTEST-Nachricht.**](lvm-subitemhittest.md)

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows Nur \[ Vista-Desktop-Apps\]<br/>                                        |
| Unterstützte Mindestversion (Server)<br/> | Windows Nur Server \[ 2003-Desktop-Apps\]<br/>                                  |
| Header<br/>                   | <dl> <dt>Commctrl.h</dt> </dl> |



 

 





