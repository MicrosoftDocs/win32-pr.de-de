---
title: NM_RELEASEDCAPTURE (Symbolleiste) Benachrichtigungscode (Commctrl.h)
description: Benachrichtigt das übergeordnete Fenster eines Symbolleisten-Steuerelements, dass das Steuerelement die Mausaufnahme frei gibt. Dieser Benachrichtigungscode wird in Form einer WM \_ NOTIFY-Nachricht gesendet.
ms.assetid: 8d9b637c-710e-4337-9466-8616a93d1c44
keywords:
- NM_RELEASEDCAPTURE -Benachrichtigungscode (Symbolleiste) Windows Steuerelementen
topic_type:
- apiref
api_name:
- NM_RELEASEDCAPTURE
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5df364d5a303ca5b62a435710c32cee5aa1e7bae7dc5c0f800c23c058b4dcfb7
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118957969"
---
# <a name="nm_releasedcapture-toolbar-notification-code"></a>NM \_ RELEASEDCAPTURE-Benachrichtigungscode (Symbolleiste)

Benachrichtigt das übergeordnete Fenster eines Symbolleisten-Steuerelements, dass das Steuerelement die Mausaufnahme frei gibt. Dieser Benachrichtigungscode wird in Form einer [**WM \_ NOTIFY-Nachricht**](wm-notify.md) gesendet.


```C++
NM_RELEASEDCAPTURE

    lpnmh = (LPNMHDR) lParam; 
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*lParam* 
</dt> <dd>

Zeiger auf eine [**NMHDR-Struktur,**](/windows/desktop/api/richedit/ns-richedit-nmhdr) die zusätzliche Informationen zu dieser Benachrichtigung enthält.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Das -Steuerelement ignoriert den Rückgabewert aus diesem Benachrichtigungscode.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows Nur \[ Vista-Desktop-Apps\]<br/>                                        |
| Unterstützte Mindestversion (Server)<br/> | Windows Nur Server \[ 2003-Desktop-Apps\]<br/>                                  |
| Header<br/>                   | <dl> <dt>Commctrl.h</dt> </dl> |



 

 





