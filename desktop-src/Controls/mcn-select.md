---
title: MCN_SELECT Benachrichtigungscode (Commctrl.h)
description: Wird von einem Monatskalender-Steuerelement gesendet, wenn der Benutzer eine explizite Datumsauswahl innerhalb eines Monatskalender-Steuerelements vornimmt. Dieser Benachrichtigungscode wird in Form einer WM \_ NOTIFY-Nachricht gesendet.
ms.assetid: 3cabb4b2-9422-4190-85d3-ab6593891e3d
keywords:
- MCN_SELECT Benachrichtigungscode Windows Controls
topic_type:
- apiref
api_name:
- MCN_SELECT
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3e71674ebccd9a896a92f701e65c7767866b64edac25208248f4683792b5261c
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119018968"
---
# <a name="mcn_select-notification-code"></a>MCN \_ SELECT-Benachrichtigungscode

Wird von einem Monatskalender-Steuerelement gesendet, wenn der Benutzer eine explizite Datumsauswahl innerhalb eines Monatskalender-Steuerelements vornimmt. Dieser Benachrichtigungscode wird in Form einer [**WM \_ NOTIFY-Nachricht**](wm-notify.md) gesendet.


```C++
MCN_SELECT

    lpNMSelChange = (LPNMSELCHANGE) lParam;
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*lParam* 
</dt> <dd>

Zeiger auf eine [**NMSELCHANGE-Struktur,**](/windows/win32/api/commctrl/ns-commctrl-nmselchange) die Informationen zum aktuell ausgewählten Datumsbereich enthält.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Kein Rückgabewert.

## <a name="remarks"></a>Hinweise

Der **MCN \_ SELECT-Benachrichtigungscode** ähnelt [**MCN \_ SELCHANGE**](mcn-selchange.md), **mcn \_ select** wird jedoch nur als Reaktion auf die explizite Datumsauswahl eines Benutzers gesendet. **MCN \_ SELCHANGE** gilt für alle Auswahländerungen.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows \[Nur Vista-Desktop-Apps\]<br/>                                        |
| Unterstützte Mindestversion (Server)<br/> | Windows Nur Server \[ 2003-Desktop-Apps\]<br/>                                  |
| Header<br/>                   | <dl> <dt>Commctrl.h</dt> </dl> |



 

 





