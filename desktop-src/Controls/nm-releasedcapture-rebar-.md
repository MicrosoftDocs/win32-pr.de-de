---
title: NM_RELEASEDCAPTURE(Rebar)-Benachrichtigungscode (Commctrl.h)
description: Benachrichtigt das übergeordnete Fenster eines Rebar-Steuerelements, dass das Steuerelement die Mauserfassung freigibt. Dieser Benachrichtigungscode wird in Form einer WM \_ NOTIFY-Nachricht gesendet.
ms.assetid: 1196260f-b9ba-4a9e-80a7-e126196c3beb
keywords:
- NM_RELEASEDCAPTURE (Neuleisten)-Benachrichtigungscode Windows-Steuerelemente
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
ms.openlocfilehash: 0601a8daa581b9f3dea477c849d668e222308bdcb991fe4c107470c341ff5661
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119018778"
---
# <a name="nm_releasedcapture-rebar-notification-code"></a>NM \_ RELEASEDCAPTURE-Benachrichtigungscode (Rebar)

Benachrichtigt das übergeordnete Fenster eines Rebar-Steuerelements, dass das Steuerelement die Mauserfassung freigibt. Dieser Benachrichtigungscode wird in Form einer [**WM \_ NOTIFY-Nachricht**](wm-notify.md) gesendet.


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

Das Steuerelement ignoriert den Rückgabewert dieses Benachrichtigungscodes.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows \[Nur Vista-Desktop-Apps\]<br/>                                        |
| Unterstützte Mindestversion (Server)<br/> | Windows Nur Server \[ 2003-Desktop-Apps\]<br/>                                  |
| Header<br/>                   | <dl> <dt>Commctrl.h</dt> </dl> |



 

 





