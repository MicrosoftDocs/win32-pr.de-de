---
title: PSN_QUERYCANCEL Benachrichtigungscode (Prsht.h)
description: Gibt an, dass der Benutzer das Eigenschaftenblatt abgebrochen hat. Dieser Benachrichtigungscode wird in Form einer WM \_ NOTIFY-Nachricht gesendet.
ms.assetid: 4a789e08-065a-485c-87e3-f7958e2dc544
keywords:
- PSN_QUERYCANCEL Benachrichtigungscode Windows-Steuerelemente
topic_type:
- apiref
api_name:
- PSN_QUERYCANCEL
api_location:
- Prsht.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: bff5ed6203d255a18c40044febb2f7afd9ab42e15c5a9d8ae9fa1a1a56518693
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119798620"
---
# <a name="psn_querycancel-notification-code"></a>PSN \_ QUERYCANCEL-Benachrichtigungscode

Gibt an, dass der Benutzer das Eigenschaftenblatt abgebrochen hat. Dieser Benachrichtigungscode wird in Form einer [**WM \_ NOTIFY-Nachricht**](wm-notify.md) gesendet.


```C++
PSN_QUERYCANCEL 

    lppsn = (LPPSHNOTIFY) lParam;  
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*lParam* 
</dt> <dd>

Zeiger auf eine [**PSHNOTIFY-Struktur,**](/windows/desktop/api/Prsht/ns-prsht-pshnotify) die Informationen zum Benachrichtigungscode enthält. Diese Struktur enthält eine [**NMHDR-Struktur**](/windows/desktop/api/richedit/ns-richedit-nmhdr) als erstes Element, **hdr.** Der **hwndFrom-Member** dieser **NMHDR-Struktur** enthält das Handle für das Eigenschaftenblatt. Der **lParam-Member** der **PSHNOTIFY-Struktur** enthält keine Informationen.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Gibt **TRUE** zurück, um den Abbruchvorgang zu verhindern, oder **FALSE,** um dies zuzulassen.

## <a name="remarks"></a>Hinweise

Dieser Benachrichtigungscode wird in der Regel gesendet, wenn ein Benutzer auf die Schaltfläche **Abbrechen** klickt. Sie wird auch gesendet, wenn ein Benutzer auf die **X-Schaltfläche** in der oberen rechten Ecke des Eigenschaftenblatts klickt oder die ESCAPE-Taste drückt. Eine Eigenschaftenblattseite kann diesen Benachrichtigungscode verarbeiten, um den Benutzer aufzufordern, den Abbruchvorgang zu überprüfen.

Um einen Rückgabewert festzulegen, muss die Dialogfeldprozedur für die Seite die [**SetWindowLong-Funktion**](/windows/desktop/api/winuser/nf-winuser-setwindowlonga) aufrufen, wobei DWL \_ MSGRESULT auf den Rückgabewert festgelegt ist. Die Dialogfeldprozedur muss **TRUE** zurückgeben.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows \[Nur Vista-Desktop-Apps\]<br/>                                     |
| Unterstützte Mindestversion (Server)<br/> | Windows Nur Server \[ 2003-Desktop-Apps\]<br/>                               |
| Header<br/>                   | <dl> <dt>Prsht.h</dt> </dl> |



 

