---
title: DTN_USERSTRING Benachrichtigungscode (Commctrl.h)
description: Wird von einem Datums- und Uhrzeitauswahl-Steuerelement (DTP) gesendet, wenn ein Benutzer die Bearbeitung einer Zeichenfolge im Steuerelement abgeschlossen hat.
ms.assetid: a5b13582-323b-4804-912c-a988d902547d
keywords:
- DTN_USERSTRING Benachrichtigungscode Windows Steuerelementen
topic_type:
- apiref
api_name:
- DTN_USERSTRING
- DTN_USERSTRINGA
- DTN_USERSTRINGW
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c6eabae4ed5a4fbe9ff0652b77fb7b6fbaf709b9030e3aa982af486ad6b7ed0d
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "120062920"
---
# <a name="dtn_userstring-notification-code"></a>DTN \_ USERSTRING-Benachrichtigungscode

Wird von einem Datums- und Uhrzeitauswahl-Steuerelement (DTP) gesendet, wenn ein Benutzer die Bearbeitung einer Zeichenfolge im Steuerelement abgeschlossen hat. Dieser Benachrichtigungscode wird nur von DTP-Steuerelementen gesendet, die auf den [**DTS \_ APPCANPARSE-Stil festgelegt**](date-and-time-picker-control-styles.md) sind. Dieser Benachrichtigungscode wird in Form einer [**WM \_ NOTIFY-Nachricht**](wm-notify.md) gesendet.


```C++
DTN_USERSTRING

    lpDTstring = (LPNMDATETIMESTRING) lParam;
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*lParam* 
</dt> <dd>

Ein Zeiger auf eine [**NMDATETIMESTRING-Struktur,**](/windows/win32/api/commctrl/ns-commctrl-nmdatetimestringa) die Informationen über die Instanz des Benachrichtigungscodes enthält.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Der Besitzer des Steuerelements muss 0 (null) zurückgeben.

## <a name="remarks"></a>Hinweise

Durch die Behandlung dieses Benachrichtigungscodes kann der Besitzer benutzerdefinierte Antworten auf Zeichenfolgen bereitstellen, die vom Benutzer in das Steuerelement eingegeben werden. Der Besitzer muss darauf vorbereitet sein, die Eingabezeichenfolge zu analysieren und bei Bedarf Maßnahmen zu ergreifen.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows Nur \[ Vista-Desktop-Apps\]<br/>                                        |
| Unterstützte Mindestversion (Server)<br/> | Windows Nur Server \[ 2003-Desktop-Apps\]<br/>                                  |
| Header<br/>                   | <dl> <dt>Commctrl.h</dt> </dl> |
| Unicode- und ANSI-Name<br/>   | **DTN \_ USERSTRINGW** (Unicode) und **DTN \_ USERSTRINGA** (ANSI)<br/>             |



 

 





