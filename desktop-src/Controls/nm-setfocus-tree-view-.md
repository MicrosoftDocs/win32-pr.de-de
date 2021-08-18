---
title: NM_SETFOCUS (Strukturansicht) Benachrichtigungscode (Commctrl.h)
description: Benachrichtigt das übergeordnete Fenster eines Strukturansicht-Steuerelements, dass das Steuerelement den Eingabefokus erhalten hat. Dieser Benachrichtigungscode wird in Form einer WM \_ NOTIFY-Nachricht gesendet.
ms.assetid: 4bdd6cd2-afd3-4c0b-914b-8fff55e474a9
keywords:
- NM_SETFOCUS -Benachrichtigungscode (Strukturansicht) Windows Steuerelementen
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
ms.openlocfilehash: 5c7aab780dec67e82e19716bc15a6c65d37894bb9d3bbe9b6bb58c227283be76
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119919550"
---
# <a name="nm_setfocus-tree-view-notification-code"></a>NM \_ SETFOCUS-Benachrichtigungscode (Strukturansicht)

Benachrichtigt das übergeordnete Fenster eines Strukturansicht-Steuerelements, dass das Steuerelement den Eingabefokus erhalten hat. Dieser Benachrichtigungscode wird in Form einer [**WM \_ NOTIFY-Nachricht**](wm-notify.md) gesendet.


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

Der Rückgabewert wird ignoriert.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows Nur \[ Vista-Desktop-Apps\]<br/>                                        |
| Unterstützte Mindestversion (Server)<br/> | Windows Nur Server \[ 2003-Desktop-Apps\]<br/>                                  |
| Header<br/>                   | <dl> <dt>Commctrl.h</dt> </dl> |



 

 





