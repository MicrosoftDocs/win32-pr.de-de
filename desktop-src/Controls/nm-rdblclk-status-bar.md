---
title: NM_RDBLCLK -Benachrichtigungscode (Statusleiste) (Commctrl.h)
description: Benachrichtigt die übergeordneten Fenster eines Statusleisten-Steuerelements, dass der Benutzer im Steuerelement mit der rechten Maustaste doppelklickt. Dieser Benachrichtigungscode wird in Form einer WM \_ NOTIFY-Nachricht gesendet.
ms.assetid: 57d8c5a7-e179-4b65-a3aa-5566d5780c18
keywords:
- NM_RDBLCLK -Benachrichtigungscode (Statusleiste) Windows-Steuerelemente
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
ms.openlocfilehash: d8aa5c754eed028d050f1f42ab6ab7ae652bfb3a3dc8bedb49df81357db6b5af
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118410681"
---
# <a name="nm_rdblclk-status-bar-notification-code"></a>NM \_ RDBLCLK-Benachrichtigungscode (Statusleiste)

Benachrichtigt die übergeordneten Fenster eines Statusleisten-Steuerelements, dass der Benutzer im Steuerelement mit der rechten Maustaste doppelklickt. Dieser Benachrichtigungscode wird in Form einer [**WM \_ NOTIFY-Nachricht**](wm-notify.md) gesendet.


```C++
NM_RDBLCLK

    lpnm = (LPNMMOUSE) lParam;
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*lParam* 
</dt> <dd>

Zeiger auf eine [**NMMOUSE-Struktur,**](/windows/win32/api/commctrl/ns-commctrl-nmmouse) die zusätzliche Informationen zu dieser Benachrichtigung enthält. Das **dwItemSpec-Element** enthält den Index des Abschnitts, auf den geklickt wurde.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Gibt **TRUE** zurück, um anzugeben, dass der Mausklick verarbeitet wurde, und unterdrückt die Standardverarbeitung durch das System. Gibt **FALSE** zurück, um die Standardverarbeitung des Klicks zuzulassen.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows \[Nur Vista-Desktop-Apps\]<br/>                                        |
| Unterstützte Mindestversion (Server)<br/> | Windows Nur Server \[ 2003-Desktop-Apps\]<br/>                                  |
| Header<br/>                   | <dl> <dt>Commctrl.h</dt> </dl> |



 

 





