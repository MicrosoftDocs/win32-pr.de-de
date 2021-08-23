---
title: NM_RDBLCLK (Strukturansicht) Benachrichtigungscode (Commctrl.h)
description: Benachrichtigt das übergeordnete Element eines Strukturansicht-Steuerelements, dass der Benutzer im Steuerelement auf die rechte Maustaste doppelklickt. Diese Benachrichtigung wird in Form einer WM \_ NOTIFY-Nachricht gesendet.
ms.assetid: eb1ae167-32cb-45d6-92e6-7bf5f7e46c2a
keywords:
- NM_RDBLCLK -Benachrichtigungscode (Strukturansicht) Windows Steuerelemente
topic_type:
- apiref
api_name:
- NM_RDBLCLK
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4da45d7ac3363a5dc362ef6d34255531f71ce780075e8106fb9579126298a1e5
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119826070"
---
# <a name="nm_rdblclk-tree-view-notification-code"></a>NM \_ RDBLCLK-Benachrichtigungscode (Strukturansicht)

Benachrichtigt das übergeordnete Element eines Strukturansicht-Steuerelements, dass der Benutzer im Steuerelement auf die rechte Maustaste doppelklickt. Diese Benachrichtigung wird in Form einer [**WM \_ NOTIFY-Nachricht**](wm-notify.md) gesendet.


```C++
NM_RDBLCLK

    lpnmh = (LPNMHDR) lParam;
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*lParam* 
</dt> <dd>

Zeiger auf eine [**NMHDR-Struktur,**](/windows/desktop/api/richedit/ns-richedit-nmhdr) die zusätzliche Informationen zu dieser Benachrichtigung enthält.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Geben Sie einen Wert ungleich 0 (null) zurück, um die Standardverarbeitung zu verhindern, oder 0 (null), um die Standardverarbeitung zu ermöglichen.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows Nur \[ Vista-Desktop-Apps\]<br/>                                        |
| Unterstützte Mindestversion (Server)<br/> | Windows Nur Server \[ 2003-Desktop-Apps\]<br/>                                  |
| Header<br/>                   | <dl> <dt>Commctrl.h</dt> </dl> |



 

 





