---
title: HDN_ITEMKEYDOWN Benachrichtigungscode (Commctrl.h)
description: Benachrichtigt das übergeordnete Fenster eines Headersteuerelements, dass eine Taste gedrückt und ein Element ausgewählt wurde. Dieser Benachrichtigungscode wird in Form einer WM \_ NOTIFY-Nachricht gesendet.
ms.assetid: ab6922ab-907d-44fc-8606-28f395118405
keywords:
- HDN_ITEMKEYDOWN Benachrichtigungscode Windows Controls
topic_type:
- apiref
api_name:
- HDN_ITEMKEYDOWN
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 473222e6cd0da7fd886571db045ee91ea6d8c46ce6bcc20e141af837d5aa92e8
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119435430"
---
# <a name="hdn_itemkeydown-notification-code"></a>HDN \_ ITEMKEYDOWN-Benachrichtigungscode

Benachrichtigt das übergeordnete Fenster eines Headersteuerelements, dass eine Taste gedrückt und ein Element ausgewählt wurde. Dieser Benachrichtigungscode wird in Form einer [**WM \_ NOTIFY-Nachricht**](wm-notify.md) gesendet.


```C++
HDN_ITEMKEYDOWN

   pNMHeader = (LPNMHEADER) lParam;
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*lParam* 
</dt> <dd>

Ein Zeiger auf eine [**NMHEADER-Struktur,**](/windows/win32/api/commctrl/ns-commctrl-nmheadera) die zusätzliche Informationen über den gedrückten Schlüssel enthält.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Kein Rückgabewert.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows \[Nur Vista-Desktop-Apps\]<br/>                                        |
| Unterstützte Mindestversion (Server)<br/> | Windows Nur Server \[ 2008-Desktop-Apps\]<br/>                                  |
| Header<br/>                   | <dl> <dt>Commctrl.h</dt> </dl> |



 

 





