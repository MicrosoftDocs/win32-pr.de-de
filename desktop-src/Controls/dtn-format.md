---
title: DTN_FORMAT Benachrichtigungscode (Commctrl.h)
description: Wird von einem Datums- und Uhrzeitauswahl-Steuerelement (DTP) gesendet, um an anforderungsgemäßen Text zu senden, der in einem Rückruffeld angezeigt werden soll. Dieser Benachrichtigungscode wird in Form einer WM \_ NOTIFY-Nachricht gesendet.
ms.assetid: ce0ee230-638e-425f-9f34-c379342cea93
keywords:
- DTN_FORMAT Benachrichtigungscode Windows Steuerelementen
topic_type:
- apiref
api_name:
- DTN_FORMAT
- DTN_FORMATA
- DTN_FORMATW
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 75fb4279f6ec6b95ded673083a024d32785dd5156588852663e6c307f8351dc4
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119916270"
---
# <a name="dtn_format-notification-code"></a>DTN \_ FORMAT-Benachrichtigungscode

Wird von einem Datums- und Uhrzeitauswahl-Steuerelement (DTP) gesendet, um an anforderungsgemäßen Text zu senden, der in einem Rückruffeld angezeigt werden soll. Dieser Benachrichtigungscode wird in Form einer [**WM \_ NOTIFY-Nachricht**](wm-notify.md) gesendet.


```C++
DTN_FORMAT

    lpNMFormat = (LPNMDATETIMEFORMAT) lParam;
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*lParam* 
</dt> <dd>

Ein Zeiger auf eine [**NMDATETIMEFORMAT-Struktur,**](/windows/win32/api/commctrl/ns-commctrl-nmdatetimeformata) die Informationen zu dieser Instanz des Benachrichtigungscodes enthält. Die -Struktur enthält die Teilzeichenfolge, die das Rückruffeld definiert und die formatierte Zeichenfolge empfängt, die vom Steuerelement angezeigt wird.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Der Besitzer des Steuerelements muss 0 (null) zurückgeben.

## <a name="remarks"></a>Hinweise

Durch die Behandlung dieses Benachrichtigungscodes kann der Besitzer des Steuerelements eine benutzerdefinierte Zeichenfolge bereitstellen, die vom Steuerelement angezeigt wird. (Weitere Informationen zu Rückruffeldern finden Sie unter [Rückruffelder.)](date-and-time-picker-controls.md)

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows Nur \[ Vista-Desktop-Apps\]<br/>                                        |
| Unterstützte Mindestversion (Server)<br/> | Windows Nur Server \[ 2003-Desktop-Apps\]<br/>                                  |
| Header<br/>                   | <dl> <dt>Commctrl.h</dt> </dl> |
| Unicode- und ANSI-Name<br/>   | **DTN \_ FORMATW** (Unicode) und **DTN \_ FORMATA** (ANSI)<br/>                     |



 

 





