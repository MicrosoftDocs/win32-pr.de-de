---
title: PSN_TRANSLATEACCELERATOR Benachrichtigungscode (Prsht.h)
description: Benachrichtigt ein Eigenschaftenblatt, dass eine Tastaturnachricht empfangen wurde. Sie bietet der Seite die Möglichkeit, eine private Tastaturbeschleunigungsübersetzung zu erstellen. Dieser Benachrichtigungscode wird in Form einer WM \_ NOTIFY-Nachricht gesendet.
ms.assetid: 04d67326-92f9-4b92-a27e-354815f3c1a8
keywords:
- PSN_TRANSLATEACCELERATOR Benachrichtigungscode Windows Steuerelementen
topic_type:
- apiref
api_name:
- PSN_TRANSLATEACCELERATOR
api_location:
- Prsht.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7ca25ed7dd2a2fa2b11e0854f7fe9e4bb4afb9aa47ec52c21bc1c6e346ebf16d
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119914490"
---
# <a name="psn_translateaccelerator-notification-code"></a>PSN \_ TRANSLATEACCELERATOR-Benachrichtigungscode

Benachrichtigt ein Eigenschaftenblatt, dass eine Tastaturnachricht empfangen wurde. Sie bietet der Seite die Möglichkeit, eine private Tastaturbeschleunigungsübersetzung zu erstellen. Dieser Benachrichtigungscode wird in Form einer [**WM \_ NOTIFY-Nachricht**](wm-notify.md) gesendet.


```C++
PSN_TRANSLATEACCELERATOR 

    lppsn = (LPPSHNOTIFY) lParam; 
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*lParam* 
</dt> <dd>

Ein Zeiger auf eine [**PSHNOTIFY-Struktur,**](/windows/desktop/api/Prsht/ns-prsht-pshnotify) die Informationen zum Benachrichtigungscode enthält. Diese Struktur enthält eine [**NMHDR-Struktur**](/windows/desktop/api/richedit/ns-richedit-nmhdr) als ersten Member, **hdr**. Der **hwndFrom-Member** der **NMHDR-Struktur** enthält das Handle für das Eigenschaftenblatt. Der **lParam-Member** der **PSHNOTIFY-Struktur** ist ein Zeiger auf das [**MSG**](/windows/win32/api/winuser/ns-winuser-msg)der Nachricht. Sie kann in einen **LPMSG-Typ** umge castiert werden, um Zugriff auf die Parameter der zu übersetzenden Nachricht zu erhalten.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Gibt PSNRET \_ MESSAGEHANDLED zurück, um anzugeben, dass keine weitere Verarbeitung erforderlich ist. Gibt PSNRET \_ NOERROR zurück, um die normale Verarbeitung an fordern.

## <a name="remarks"></a>Hinweise

Zum Festlegen des Rückgabewerts muss die Dialogfeldprozedur für die Seite die [**SetWindowLong-Funktion**](/windows/desktop/api/winuser/nf-winuser-setwindowlonga) mit dem DWL \_ MSGRESULT-Wert verwenden. Die Dialogfeldprozedur muss **TRUE zurückgeben.**

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows Nur \[ Vista-Desktop-Apps\]<br/>                                     |
| Unterstützte Mindestversion (Server)<br/> | Windows Nur Server \[ 2003-Desktop-Apps\]<br/>                               |
| Header<br/>                   | <dl> <dt>Prsht.h</dt> </dl> |



 

