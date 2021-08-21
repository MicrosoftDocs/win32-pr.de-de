---
title: NM_RCLICK (Header) Benachrichtigungscode (Commctrl.h)
description: Benachrichtigt das übergeordnete Fenster eines Strukturansicht-Steuerelements, dass der Benutzer im Steuerelement auf die rechte Maustaste geklickt hat. Dieser Benachrichtigungscode wird in Form einer WM \_ NOTIFY-Nachricht gesendet.
ms.assetid: b453db51-9c41-4a85-8bc0-72bec10f8646
keywords:
- NM_RCLICK -Benachrichtigungscode (Header) Windows-Steuerelemente
topic_type:
- apiref
api_name:
- NM_RCLICK
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: eb3c5ff6a6e8bd86c2f5a69fdd6f7337178b12e68c8c0c9f12c945b27cfb13b0
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118958119"
---
# <a name="nm_rclick-header-notification-code"></a>NM \_ RCLICK-Benachrichtigungscode (Header)

Benachrichtigt das übergeordnete Fenster eines Strukturansicht-Steuerelements, dass der Benutzer im Steuerelement auf die rechte Maustaste geklickt hat. Dieser Benachrichtigungscode wird in Form einer [**WM \_ NOTIFY-Nachricht**](wm-notify.md) gesendet.


```C++
NM_RCLICK

    lpnmh = (LPNMHDR) lParam; 
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*lParam* 
</dt> <dd>

Ein Zeiger auf eine [**NMHDR-Struktur,**](/windows/desktop/api/richedit/ns-richedit-nmhdr) die zusätzliche Informationen zu dieser Benachrichtigung enthält.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Geben Sie einen Wert ungleich 0 (null) zurück, um die Standardverarbeitung nicht zu erlauben, oder 0 (null), um die Standardverarbeitung zu ermöglichen.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows Nur \[ Vista-Desktop-Apps\]<br/>                                        |
| Unterstützte Mindestversion (Server)<br/> | Windows Nur Server \[ 2003-Desktop-Apps\]<br/>                                  |
| Header<br/>                   | <dl> <dt>Commctrl.h</dt> </dl> |



 

 





