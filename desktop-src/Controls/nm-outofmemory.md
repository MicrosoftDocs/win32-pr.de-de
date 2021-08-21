---
title: NM_OUTOFMEMORY Benachrichtigungscode (Commctrl.h)
description: Benachrichtigt das übergeordnete Fenster eines Steuerelements, dass das Steuerelement einen Vorgang nicht abschließen konnte, da nicht genügend Arbeitsspeicher verfügbar war. Dieser Benachrichtigungscode wird in Form einer WM \_ NOTIFY-Nachricht gesendet.
ms.assetid: d7d80515-ae6c-4817-a698-d486a9d86c4a
keywords:
- NM_OUTOFMEMORY Benachrichtigungscode Windows-Steuerelemente
topic_type:
- apiref
api_name:
- NM_OUTOFMEMORY
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c8a2efdd0048006b86d97964dc953d2dbd7c4ecb2687b3c0fb67a5effc63fea0
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118958109"
---
# <a name="nm_outofmemory-notification-code"></a>NM \_ OUTOFMEMORY-Benachrichtigungscode

Benachrichtigt das übergeordnete Fenster eines Steuerelements, dass das Steuerelement einen Vorgang nicht abschließen konnte, da nicht genügend Arbeitsspeicher verfügbar war. Dieser Benachrichtigungscode wird in Form einer [**WM \_ NOTIFY-Nachricht**](wm-notify.md) gesendet.


```C++
NM_OUTOFMEMORY

    lpnmh = (LPNMHDR) lParam; 
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*lParam* 
</dt> <dd>

Ein Zeiger auf eine [**NMHDR-Struktur,**](/windows/desktop/api/richedit/ns-richedit-nmhdr) die zusätzliche Informationen zu dieser Benachrichtigung enthält.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Der Rückgabewert wird vom -Steuerelement ignoriert.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows \[Nur Vista-Desktop-Apps\]<br/>                                        |
| Unterstützte Mindestversion (Server)<br/> | Windows Nur Server \[ 2003-Desktop-Apps\]<br/>                                  |
| Header<br/>                   | <dl> <dt>Commctrl.h</dt> </dl> |



 

 





