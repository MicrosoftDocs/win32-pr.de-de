---
title: NM_SETFOCUS (Listenansicht) Benachrichtigungscode (Commctrl.h)
description: Benachrichtigt das übergeordnete Fenster eines Listenansicht-Steuerelements, dass das Steuerelement den Eingabefokus erhalten hat. Dieser Benachrichtigungscode wird in Form einer WM \_ NOTIFY-Nachricht gesendet.
ms.assetid: 43d3b09a-f095-4f30-87a8-2f2e782d6720
keywords:
- NM_SETFOCUS -Benachrichtigungscode (Listenansicht) Windows Controls
topic_type:
- apiref
api_name:
- NM_SETFOCUS
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 312382eb81694bc49a121cd336e76c361a3519222f63723bb8d5203201c996f2
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118410303"
---
# <a name="nm_setfocus-list-view-notification-code"></a>NM \_ SETFOCUS-Benachrichtigungscode (Listenansicht)

Benachrichtigt das übergeordnete Fenster eines Listenansicht-Steuerelements, dass das Steuerelement den Eingabefokus erhalten hat. Dieser Benachrichtigungscode wird in Form einer [**WM \_ NOTIFY-Nachricht**](wm-notify.md) gesendet.


```C++
NM_SETFOCUS 

    lpnmh = (LPNMHDR) lParam; 
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*lParam* 
</dt> <dd>

Zeiger auf eine [**NMHDR-Struktur,**](/windows/desktop/api/richedit/ns-richedit-nmhdr) die zusätzliche Informationen zu dieser Benachrichtigung enthält.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Der Rückgabewert für diese Benachrichtigung wird nicht verwendet.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows Nur \[ Vista-Desktop-Apps\]<br/>                                        |
| Unterstützte Mindestversion (Server)<br/> | Windows Nur Server \[ 2003-Desktop-Apps\]<br/>                                  |
| Header<br/>                   | <dl> <dt>Commctrl.h</dt> </dl> |



 

 





