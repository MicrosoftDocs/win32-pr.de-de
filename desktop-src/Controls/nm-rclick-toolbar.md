---
title: NM_RCLICK (Symbolleiste) Benachrichtigungscode (Commctrl.h)
description: Wird von einem Symbolleisten-Steuerelement gesendet, wenn der Benutzer mit der rechten Maustaste auf die Symbolleiste klickt. Dieser Benachrichtigungscode wird in Form einer WM \_ NOTIFY-Nachricht gesendet.
ms.assetid: e9d2d871-e922-444d-a76c-e73f249ed410
keywords:
- NM_RCLICK -Benachrichtigungscode (Symbolleiste) Windows Steuerelementen
topic_type:
- apiref
api_name:
- NM_RCLICK
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 52fde315a3c68712c58b7e9466c351c6ac9a9117710ee6f285bd9ba9521ba56f
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118958069"
---
# <a name="nm_rclick-toolbar-notification-code"></a>NM \_ RCLICK-Benachrichtigungscode (Symbolleiste)

Wird von einem Symbolleisten-Steuerelement gesendet, wenn der Benutzer mit der rechten Maustaste auf die Symbolleiste klickt. Dieser Benachrichtigungscode wird in Form einer [**WM \_ NOTIFY-Nachricht**](wm-notify.md) gesendet.


```C++
NM_RCLICK

    lpnmmouse = (LPNMMOUSE) lParam;
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*lParam* 
</dt> <dd>

Zeiger auf eine [**NMMOUSE-Struktur,**](/windows/win32/api/commctrl/ns-commctrl-nmmouse) die Informationen zu diesem Benachrichtigungscode enthält. Wenn mit der Maus auf ein Symbolleistenelement geklickt wurde, enthält das **dwItemSpec-Element** den Elementbezeichner und **das dwItemData-Element** die Elementdaten. Wenn mit der Maus auf ein Trennzeichen oder Leerzeichen in der Symbolleiste geklickt wurde, enthält **das dwItemSpec-Member** -1.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Gibt **FALSE zurück,** damit das Symbolleisten-Steuerelement die Standardverarbeitung des Ereignisses durchführen kann, oder **TRUE,** um zu verhindern, dass das Steuerelement das Ereignis verarbeitet.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows Nur \[ Vista-Desktop-Apps\]<br/>                                        |
| Unterstützte Mindestversion (Server)<br/> | Windows Nur Server \[ 2003-Desktop-Apps\]<br/>                                  |
| Header<br/>                   | <dl> <dt>Commctrl.h</dt> </dl> |



 

 





