---
title: PSN_WIZFINISH Benachrichtigungscode (Prsht.h)
description: Benachrichtigt eine Seite, dass der Benutzer in einem Assistenten auf die Schaltfläche Fertig stellen geklickt hat. Dieser Benachrichtigungscode wird in Form einer WM \_ NOTIFY-Nachricht gesendet.
ms.assetid: 8ef0a8a7-2d25-4969-9b8f-e42dcc1c8fb5
keywords:
- PSN_WIZFINISH Benachrichtigungscode Windows Steuerelementen
topic_type:
- apiref
api_name:
- PSN_WIZFINISH
api_location:
- Prsht.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b9a11b018a57126c0882862271fa209fcd507224a46180ebb5fbaed4355fc040
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119588180"
---
# <a name="psn_wizfinish-notification-code"></a>PSN \_ WIZFINISH-Benachrichtigungscode

Benachrichtigt eine Seite, dass der Benutzer in einem Assistenten auf **die** Schaltfläche Fertig stellen geklickt hat. Dieser Benachrichtigungscode wird in Form einer [**WM \_ NOTIFY-Nachricht**](wm-notify.md) gesendet.


```C++
PSN_WIZFINISH 

    lppsn = (LPPSHNOTIFY) lParam; 
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*lParam* 
</dt> <dd>

Zeiger auf eine [**PSHNOTIFY-Struktur,**](/windows/desktop/api/Prsht/ns-prsht-pshnotify) die Informationen zum Benachrichtigungscode enthält. Diese Struktur enthält eine [**NMHDR-Struktur**](/windows/desktop/api/richedit/ns-richedit-nmhdr) als ersten Member, **hdr**. Der **hwndFrom-Member** dieser **NMHDR-Struktur** enthält das Handle für das Eigenschaftenblatt. Das **lParam-Member** der **PSHNOTIFY-Struktur** enthält keine Informationen.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

-   Gibt **TRUE zurück,** um zu verhindern, dass der Assistent beendet wird.
-   [Version 5.80.](common-control-versions.md) und höher. Gibt ein Fensterhand handle zurück, um zu verhindern, dass der Assistent beendet wird. Der Assistent setzt den Fokus auf dieses Fenster. Das Fenster muss im Besitz der Assistentenseite sein.
-   Gibt **FALSE zurück,** damit der Assistent abgeschlossen werden kann.

## <a name="remarks"></a>Hinweise

Zum Festlegen des Rückgabewerts muss die Dialogfeldprozedur für die Seite die [**SetWindowLong-Funktion**](/windows/desktop/api/winuser/nf-winuser-setwindowlonga) mit dem DWL MSGRESULT-Wert verwenden, und die Dialogfeldprozedur muss \_ **TRUE zurückgeben.**

[Version 5.80.](common-control-versions.md) Wenn Ihre Anwendung **TRUE zurückgibt,** um zu verhindern, dass ein Assistent beendet wird, hat sie keine Kontrolle darüber, welches Fenster auf der Seite den Fokus erhält. Anwendungen, die das Beenden eines Assistenten beenden müssen, sollten dies normalerweise tun, indem sie das Handle des Fensters auf der Assistentenseite zurückgeben, das den Fokus erhalten soll.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows Nur \[ Vista-Desktop-Apps\]<br/>                                     |
| Unterstützte Mindestversion (Server)<br/> | Windows Nur Server \[ 2003-Desktop-Apps\]<br/>                               |
| Header<br/>                   | <dl> <dt>Prsht.h</dt> </dl> |



 

