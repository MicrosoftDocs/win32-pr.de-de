---
title: LVN_HOTTRACK Benachrichtigungscode (Commctrl.h)
description: Wird von einem Listenansichtssteuerelement gesendet, wenn der Benutzer den Mauszeiger über ein Element bewegt. Dieser Benachrichtigungscode wird nur von Listenansichtssteuerelementen gesendet, die den \_ erweiterten Listenansichtsstil LVS EX \_ TRACKSELECT aufweisen. Sie wird in Form einer WM \_ NOTIFY-Nachricht gesendet.
ms.assetid: 6bbfe6b8-9b67-49e4-9481-65abe98608bb
keywords:
- LVN_HOTTRACK Benachrichtigungscode Windows Controls
topic_type:
- apiref
api_name:
- LVN_HOTTRACK
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8ab311b17f287b695a6b21d333f7183fdda272029e2c57dfe468527d765d1602
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "117830431"
---
# <a name="lvn_hottrack-notification-code"></a>LVN \_ HOTTRACK-Benachrichtigungscode

Wird von einem Listenansichtssteuerelement gesendet, wenn der Benutzer den Mauszeiger über ein Element bewegt. Dieser Benachrichtigungscode wird nur von Listenansichtssteuerelementen gesendet, die den erweiterten [**Listenansichtsstil LVS \_ EX \_ TRACKSELECT**](extended-list-view-styles.md) aufweisen. Sie wird in Form einer [**WM \_ NOTIFY-Nachricht**](wm-notify.md) gesendet.


```C++
LVN_HOTTRACK

    lpnmlv = (LPNMLISTVIEW) lParam;
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*lParam* 
</dt> <dd>

Zeiger auf eine [**NMLISTVIEW-Struktur,**](/windows/win32/api/commctrl/ns-commctrl-nmlistview) die Informationen zu diesem Benachrichtigungscode enthält. Die **Member iItem,** **iSubItem** und **ptAction** dieser Struktur enthalten Informationen über das Element. Die empfangende Anwendung kann das **iItem-Element** ändern, um das element anzugeben, das ausgewählt wird. Wenn **iItem** auf -1 festgelegt ist, wird kein Element ausgewählt.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Geben Sie 0 (null) zurück, damit die Listenansicht die normale Verarbeitung der Trackauswahl ausführen kann. Wenn die Anwendung einen Wert ungleich 0 (null) zurückgibt, wird das Element nicht ausgewählt.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows \[Nur Vista-Desktop-Apps\]<br/>                                        |
| Unterstützte Mindestversion (Server)<br/> | Windows Nur Server \[ 2003-Desktop-Apps\]<br/>                                  |
| Header<br/>                   | <dl> <dt>Commctrl.h</dt> </dl> |



 

 





