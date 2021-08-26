---
title: NM_LDOWN -Benachrichtigungscode (Symbolleiste) (Commctrl.h)
description: Benachrichtigt das übergeordnete Fenster einer Symbolleiste, dass die linke Maustaste gedrückt wurde. Dieser Benachrichtigungscode wird in Form einer WM \_ NOTIFY-Nachricht gesendet.
ms.assetid: f5b356fb-265b-4eb0-a5a3-2a22d688f847
keywords:
- NM_LDOWN -Benachrichtigungscode (Symbolleiste) Windows-Steuerelemente
topic_type:
- apiref
api_name:
- NM_LDOWN
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6cf283e8b3e0d1ed780a80d5608849bc42f200b61a5a94692c0924cb2e6241a8
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119919650"
---
# <a name="nm_ldown-toolbar-notification-code"></a>NM \_ LDOWN-Benachrichtigungscode (Symbolleiste)

Benachrichtigt das übergeordnete Fenster einer Symbolleiste, dass die linke Maustaste gedrückt wurde. Dieser Benachrichtigungscode wird in Form einer [**WM \_ NOTIFY-Nachricht**](wm-notify.md) gesendet.


```C++
NM_LDOWN

    lpnmmouse = (LPNMMOUSE) lParam; 
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*lParam* 
</dt> <dd>

Zeiger auf eine [**NMMOUSE-Struktur,**](/windows/win32/api/commctrl/ns-commctrl-nmmouse) die Informationen zu diesem Benachrichtigungscode enthält. Wenn mit der Maus auf ein Symbolleistenelement geklickt wurde, enthält das **element dwItemSpec-Element** den Elementbezeichner und das **dwItemData-Element** die Elementdaten. Wenn auf der Symbolleiste auf ein Trennzeichen oder Leerzeichen geklickt wurde, enthält das **dwItemSpec-Element** -1.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Gibt **FALSE** zurück, damit das Symbolleistensteuerelement die Standardverarbeitung des Ereignisses ausführen kann, oder **TRUE,** um zu verhindern, dass das Steuerelement das Ereignis verarbeitet.

## <a name="remarks"></a>Hinweise

Diese Benachrichtigung wird gesendet, nachdem der [ \_ TBN-DROPDOWN-Benachrichtigungscode](tbn-dropdown.md) gesendet wurde.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows \[Nur Vista-Desktop-Apps\]<br/>                                        |
| Unterstützte Mindestversion (Server)<br/> | Windows Nur Server \[ 2003-Desktop-Apps\]<br/>                                  |
| Header<br/>                   | <dl> <dt>Commctrl.h</dt> </dl> |



 

 





