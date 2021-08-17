---
title: PSN_KILLACTIVE Benachrichtigungscode (Prsht.h)
description: Benachrichtigt eine Seite, dass sie die Aktivierung verlieren wird, weil eine andere Seite aktiviert wird oder der Benutzer auf die Schaltfläche OK geklickt hat. Dieser Benachrichtigungscode wird in Form einer WM \_ NOTIFY-Nachricht gesendet.
ms.assetid: 470cd6ff-73ad-451a-a861-4d3324a8a8db
keywords:
- PSN_KILLACTIVE Benachrichtigungscode Windows Steuerelementen
topic_type:
- apiref
api_name:
- PSN_KILLACTIVE
api_location:
- Prsht.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5eaf1a5221e186ebe5f01f942ec99d82906ea87ef7f1b8f73860bade24ab1751
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118169650"
---
# <a name="psn_killactive-notification-code"></a>PSN \_ KILLACTIVE-Benachrichtigungscode

Benachrichtigt eine Seite, dass sie die Aktivierung verlieren wird, weil eine andere Seite aktiviert wird oder der Benutzer auf die Schaltfläche OK geklickt hat. Dieser Benachrichtigungscode wird in Form einer [**WM \_ NOTIFY-Nachricht**](wm-notify.md) gesendet.


```C++
PSN_KILLACTIVE 

    lppsn = (LPPSHNOTIFY) lParam; 
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*lParam* 
</dt> <dd>

Zeiger auf eine [**PSHNOTIFY-Struktur,**](/windows/desktop/api/Prsht/ns-prsht-pshnotify) die Informationen zum Benachrichtigungscode enthält. Diese Struktur enthält eine [**NMHDR-Struktur**](/windows/desktop/api/richedit/ns-richedit-nmhdr) als ersten Member, **hdr**. Der **hwndFrom-Member** dieser **NMHDR-Struktur** enthält das Handle für das Eigenschaftenblatt. Das **lParam-Member** der **PSHNOTIFY-Struktur** enthält keine Informationen.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Gibt **TRUE zurück,** um zu verhindern, dass die Seite die Aktivierung verliert, oder **FALSE,** um sie zu ermöglichen.

## <a name="remarks"></a>Hinweise

Eine Anwendung verarbeitet diesen Benachrichtigungscode, um die vom Benutzer eingegebenen Informationen zu überprüfen.

> [!Note]  
> Das Eigenschaftenblatt wird die Liste der Seiten bearbeiten, wenn der PSN \_ KILLACTIVE-Benachrichtigungscode gesendet wird. Versuchen Sie nicht, Seiten hinzuzufügen, zu entfernen oder hinzuzufügen, während Sie diesen Benachrichtigungscode behandeln. Dies führt zu unvorhersehbaren Ergebnissen.

 

Zum Festlegen eines Rückgabewerts muss die Dialogfeldprozedur für die Seite die [**SetWindowLong-Funktion**](/windows/desktop/api/winuser/nf-winuser-setwindowlonga) aufrufen, bei der ein DWL MSGRESULT-Wert auf den \_ Rückgabewert festgelegt ist. Die Dialogfeldprozedur muss **TRUE zurückgeben.**

Wenn in der Dialogfeldprozedur DWL MSGRESULT auf TRUE festgelegt wird, sollte ein Meldungsfeld angezeigt werden, in dem dem Benutzer das \_ Problem erklärt wird. 

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows Nur \[ Vista-Desktop-Apps\]<br/>                                     |
| Unterstützte Mindestversion (Server)<br/> | Windows Nur Server \[ 2003-Desktop-Apps\]<br/>                               |
| Header<br/>                   | <dl> <dt>Prsht.h</dt> </dl> |



 

