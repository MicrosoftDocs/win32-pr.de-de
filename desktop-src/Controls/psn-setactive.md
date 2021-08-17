---
title: PSN_SETACTIVE Benachrichtigungscode (Prsht.h)
description: Benachrichtigt eine Seite, dass sie aktiviert werden soll. Dieser Benachrichtigungscode wird in Form einer WM \_ NOTIFY-Nachricht gesendet.
ms.assetid: 0cf918b7-9f0d-4dec-8df1-a1d2d8ac6463
keywords:
- PSN_SETACTIVE Benachrichtigungscode Windows Steuerelementen
topic_type:
- apiref
api_name:
- PSN_SETACTIVE
api_location:
- Prsht.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 16e7b656f5497065378af87408fa87fc16cf9ca2cef3cc710f52a1cd643c2927
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118409732"
---
# <a name="psn_setactive-notification-code"></a>PSN \_ SETACTIVE-Benachrichtigungscode

Benachrichtigt eine Seite, dass sie aktiviert werden soll. Dieser Benachrichtigungscode wird in Form einer [**WM \_ NOTIFY-Nachricht**](wm-notify.md) gesendet.


```C++
PSN_SETACTIVE 

    lppsn = (LPPSHNOTIFY) lParam; 
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*lParam* 
</dt> <dd>

Zeiger auf eine [**PSHNOTIFY-Struktur,**](/windows/desktop/api/Prsht/ns-prsht-pshnotify) die Informationen zum Benachrichtigungscode enthält. Diese Struktur enthält eine [**NMHDR-Struktur**](/windows/desktop/api/richedit/ns-richedit-nmhdr) als ersten Member, **hdr**. Der **hwndFrom-Member** dieser **NMHDR-Struktur** enthält das Handle für das Eigenschaftenblatt. Das **lParam-Member** der **PSHNOTIFY-Struktur** enthält keine Informationen.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Gibt null zurück, um die Aktivierung zu akzeptieren, oder -1, um die nächste oder vorherige Seite zu aktivieren (je nachdem, ob der Benutzer auf die Schaltfläche Weiter **oder** **Zurück geklickt** hat). Um die Aktivierung auf eine bestimmte Seite zu setzen, geben Sie den Ressourcenbezeichner der Seite zurück.

## <a name="remarks"></a>Hinweise

Der PSN \_ SETACTIVE-Benachrichtigungscode wird gesendet, bevor die Seite sichtbar ist. Eine Anwendung kann diesen Benachrichtigungscode verwenden, um Daten auf der Seite zu initialisieren.

> [!Note]  
> Das Eigenschaftenblatt wird die Liste der Seiten bearbeiten, wenn der PSN \_ SETACTIVE-Benachrichtigungscode gesendet wird. Versuchen Sie nicht, Seiten hinzuzufügen, zu entfernen oder hinzuzufügen, während Sie diesen Benachrichtigungscode behandeln. Dies führt zu unvorhersehbaren Ergebnissen.

 

Zum Festlegen des Rückgabewerts muss die Dialogfeldprozedur für die Seite die [**SetWindowLong-Funktion**](/windows/desktop/api/winuser/nf-winuser-setwindowlonga) mit dem DWL MSGRESULT-Wert verwenden, und die Dialogfeldprozedur muss \_ **TRUE zurückgeben.**

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows Nur \[ Vista-Desktop-Apps\]<br/>                                     |
| Unterstützte Mindestversion (Server)<br/> | Windows Nur Server \[ 2003-Desktop-Apps\]<br/>                               |
| Header<br/>                   | <dl> <dt>Prsht.h</dt> </dl> |



 

