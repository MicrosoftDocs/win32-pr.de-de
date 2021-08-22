---
title: EN_PARAGRAPHEXPANDED Benachrichtigungscode (Richedit.h)
description: Benachrichtigt das übergeordnete Element eines Rich-Edit-Steuerelements, dass eine Kontur erweitert wurde. Dieses Benachrichtigungscode wird von einem Rich-Edit-Steuerelement in Form einer WM \_ NOTIFY-Nachricht gesendet.
ms.assetid: D33EB118-FC79-4284-820B-3424F13722C4
keywords:
- EN_PARAGRAPHEXPANDED Benachrichtigungscode Windows Steuerelementen
topic_type:
- apiref
api_name:
- EN_PARAGRAPHEXPANDEDC
api_location:
- Richedit.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: eefff660e03afd38932b81c2852e999dd8d56196dafacd3afa5aa79076b51326
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119436660"
---
# <a name="en_paragraphexpanded-notification-code"></a>EN \_ PARAGRAPHEXPANDED-Benachrichtigungscode

Benachrichtigt das übergeordnete Element eines Rich-Edit-Steuerelements, dass eine Kontur erweitert wurde. Dieses Benachrichtigungscode wird von einem Rich-Edit-Steuerelement in Form einer [**WM \_ NOTIFY-Nachricht**](wm-notify.md) gesendet.


```C++
EN_PARAGRAPHEXPANDED

    lpnmhdr = (LPNMHDR) lParam;
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*lParam* 
</dt> <dd>

Eine [**NMHDR-Struktur.**](/windows/desktop/api/richedit/ns-richedit-nmhdr)

</dd> </dl>

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows Nur \[ Vista-Desktop-Apps\]<br/>                                        |
| Unterstützte Mindestversion (Server)<br/> | Windows Nur Server \[ 2003-Desktop-Apps\]<br/>                                  |
| Header<br/>                   | <dl> <dt>Richedit.h</dt> </dl> |



 

 





