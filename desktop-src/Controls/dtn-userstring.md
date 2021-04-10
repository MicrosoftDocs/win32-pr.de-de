---
title: DTN_USERSTRING Benachrichtigungs Code (kommctrl. h)
description: Wird von einem DTP-Steuerelement (Datums-und Zeitauswahl) gesendet, wenn ein Benutzer das Bearbeiten einer Zeichenfolge im-Steuerelement beendet.
ms.assetid: a5b13582-323b-4804-912c-a988d902547d
keywords:
- Windows-Steuerelemente für DTN_USERSTRING Benachrichtigungs
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
ms.openlocfilehash: 4878875d23a0a5fce95aa4cc9ebfedfbdf24cb93
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "103858712"
---
# <a name="dtn_userstring-notification-code"></a>DTN \_ UserString-Benachrichtigungs Code

Wird von einem DTP-Steuerelement (Datums-und Zeitauswahl) gesendet, wenn ein Benutzer das Bearbeiten einer Zeichenfolge im-Steuerelement beendet. Dieser Benachrichtigungs Code wird nur von DTP-Steuerelementen gesendet, die auf den [**DTS \_ appcananalyse**](date-and-time-picker-control-styles.md) -Stil festgelegt sind. Dieser Benachrichtigungs Code wird in Form einer WM- [**\_ Benachrichtigungs**](wm-notify.md) Meldung gesendet.


```C++
DTN_USERSTRING

    lpDTstring = (LPNMDATETIMESTRING) lParam;
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*lParam* 
</dt> <dd>

Ein Zeiger auf eine [**nmdatetimestring**](/windows/win32/api/commctrl/ns-commctrl-nmdatetimestringa) -Struktur, die Informationen über die Instanz des Benachrichtigungs Codes enthält.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Der Besitzer des Steuer Elements muss 0 (null) zurückgeben.

## <a name="remarks"></a>Bemerkungen

Durch die Behandlung dieses Benachrichtigungs Codes kann der Besitzer benutzerdefinierte Antworten auf Zeichen folgen bereitstellen, die vom Benutzer in das Steuerelement eingegeben werden. Der Besitzer muss darauf vorbereitet sein, die Eingabe Zeichenfolge zu analysieren und ggf. Aktionen auszuführen.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Nur Windows Vista \[ -Desktop-Apps\]<br/>                                        |
| Unterstützte Mindestversion (Server)<br/> | Nur Windows Server 2003 \[ -Desktop-Apps\]<br/>                                  |
| Header<br/>                   | <dl> <dt>Kommstrg. h</dt> </dl> |
| Unicode- und ANSI-Name<br/>   | **Dtn \_ Userstringw** (Unicode) und **Dtn \_ userstrauch** (ANSI)<br/>             |



 

 





