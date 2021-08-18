---
title: NM_CLICK -Benachrichtigungscode (Strukturansicht) (Commctrl.h)
description: Benachrichtigt das übergeordnete Fenster eines Strukturansichtssteuerelements, dass der Benutzer im Steuerelement auf die linke Maustaste geklickt hat. Dieser Benachrichtigungscode wird in Form einer WM \_ NOTIFY-Nachricht gesendet.
ms.assetid: 39b5716d-cae7-4dc4-b257-0118f4f432c6
keywords:
- NM_CLICK -Benachrichtigungscode (Strukturansicht) Windows-Steuerelemente
topic_type:
- apiref
api_name:
- NM_CLICK
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d9d942504afd13359f38fa62c4f6a283367288873f89922311242516b9063990
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119018888"
---
# <a name="nm_click-tree-view-notification-code"></a>NM \_ CLICK-Benachrichtigungscode (Strukturansicht)

Benachrichtigt das übergeordnete Fenster eines Strukturansichtssteuerelements, dass der Benutzer im Steuerelement auf die linke Maustaste geklickt hat. Dieser Benachrichtigungscode wird in Form einer [**WM \_ NOTIFY-Nachricht**](wm-notify.md) gesendet.


```C++
NM_CLICK
        
    lpnmh = (LPNMHDR) lParam;
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*lParam* 
</dt> <dd>

Zeiger auf eine [**NMHDR-Struktur,**](/windows/desktop/api/richedit/ns-richedit-nmhdr) die zusätzliche Informationen zu dieser Benachrichtigung enthält.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Gibt einen Wert ungleich 0 (null) zurück, um die Standardverarbeitung zu verhindern, oder 0 (null), um die Standardverarbeitung zuzulassen.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows \[Nur Vista-Desktop-Apps\]<br/>                                        |
| Unterstützte Mindestversion (Server)<br/> | Windows Nur Server \[ 2003-Desktop-Apps\]<br/>                                  |
| Header<br/>                   | <dl> <dt>Commctrl.h</dt> </dl> |



 

 





