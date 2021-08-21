---
title: DTN_WMKEYDOWN Benachrichtigungscode (Commctrl.h)
description: Wird von einem DTP-Steuerelement (Date and Time Picker) gesendet, wenn der Benutzer ein Rückruffeld einwählt. Dieser Benachrichtigungscode wird in Form einer WM \_ NOTIFY-Nachricht gesendet.
ms.assetid: e67e222d-28a1-4d30-ae64-8ec9a62fa321
keywords:
- DTN_WMKEYDOWN Benachrichtigungscode Windows Steuerelementen
topic_type:
- apiref
api_name:
- DTN_WMKEYDOWN
- DTN_WMKEYDOWNA
- DTN_WMKEYDOWNW
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0eaf822cc5eb8d1d8bdeca6b0853766774105af07cda77f55743d60d0fb12cdd
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119019978"
---
# <a name="dtn_wmkeydown-notification-code"></a>DTN \_ WMKEYDOWN-Benachrichtigungscode

Wird von einem DTP-Steuerelement (Date and Time Picker) gesendet, wenn der Benutzer ein Rückruffeld einwählt. Dieser Benachrichtigungscode wird in Form einer [**WM \_ NOTIFY-Nachricht**](wm-notify.md) gesendet.


```C++
DTN_WMKEYDOWN

    lpDTKeystroke = (LPNMDATETIMEWMKEYDOWN)lParam;
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*lParam* 
</dt> <dd>

Ein Zeiger auf eine [**NMDATETIMEWMKEYDOWN-Struktur,**](/windows/win32/api/commctrl/ns-commctrl-nmdatetimewmkeydowna) die Informationen zu dieser Instanz des Benachrichtigungscodes enthält. Die -Struktur enthält Informationen über den Schlüssel, den der Benutzer typiert hat, die Teilzeichenfolge, die das Rückruffeld definiert, sowie das aktuelle Systemdatum und die aktuelle Systemzeit.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Der Besitzer des Steuerelements muss 0 (null) zurückgeben.

## <a name="remarks"></a>Hinweise

Durch die Behandlung dieses Benachrichtigungscodes kann der Besitzer des Steuerelements bestimmte Antworten auf Tastatureingaben innerhalb der Rückruffelder des Steuerelements bereitstellen.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows Nur \[ Vista-Desktop-Apps\]<br/>                                        |
| Unterstützte Mindestversion (Server)<br/> | Windows Nur Server \[ 2003-Desktop-Apps\]<br/>                                  |
| Header<br/>                   | <dl> <dt>Commctrl.h</dt> </dl> |
| Unicode- und ANSI-Name<br/>   | **DTN \_ WMKEYDOWNW** (Unicode) und **DTN \_ WMKEYDOWNA** (ANSI)<br/>               |



 

 





