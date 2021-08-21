---
title: HDN_BEGINTRACK Benachrichtigungscode (Commctrl.h)
description: Benachrichtigt das übergeordnete Fenster eines Headersteuerfelds, dass der Benutzer mit dem Ziehen eines Unterteilers im Steuerelement begonnen hat (d. h., der Benutzer hat die linke Maustaste gedrückt, während sich der Mauszeiger auf einem Unterteiler im Headersteuerfeld befindet).
ms.assetid: 363b14bc-2b7e-4c37-9caf-7671fcc3cfa5
keywords:
- HDN_BEGINTRACK Benachrichtigungscode Windows Steuerelementen
topic_type:
- apiref
api_name:
- HDN_BEGINTRACK
- HDN_BEGINTRACKA
- HDN_BEGINTRACKW
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4250f178c4e1e2322e1609159eabd2fbd99611c10420bb90ce7bd287c44a5d88
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118170940"
---
# <a name="hdn_begintrack-notification-code"></a>HDN \_ BEGINTRACK-Benachrichtigungscode

Benachrichtigt das übergeordnete Fenster eines Headersteuerfelds, dass der Benutzer mit dem Ziehen eines Unterteilers im Steuerelement begonnen hat (d. h., der Benutzer hat die linke Maustaste gedrückt, während sich der Mauszeiger auf einem Unterteiler im Headersteuerfeld befindet). Dieser Benachrichtigungscode wird in Form einer [**WM \_ NOTIFY-Nachricht**](wm-notify.md) gesendet.


```C++
HDN_BEGINTRACK

    pNMHeader = (LPNMHEADER) lParam; 
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*lParam* 
</dt> <dd>

Ein Zeiger auf eine [**NMHEADER-Struktur,**](/windows/win32/api/commctrl/ns-commctrl-nmheadera) die Informationen über das Headersteuerelement und das Element enthält, dessen Unterteiler gezogen werden soll.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Gibt **FALSE zurück,** um die Nachverfolgung des Unterteilers zu ermöglichen, oder **TRUE,** um die Nachverfolgung zu verhindern.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows Nur \[ Vista-Desktop-Apps\]<br/>                                        |
| Unterstützte Mindestversion (Server)<br/> | Windows Nur Server \[ 2003-Desktop-Apps\]<br/>                                  |
| Header<br/>                   | <dl> <dt>Commctrl.h</dt> </dl> |
| Unicode- und ANSI-Name<br/>   | **HDN \_ BEGINTRACKW** (Unicode) und **HDN \_ BEGINTRACKA** (ANSI)<br/>             |



 

 





