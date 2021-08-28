---
title: NM_DBLCLK (Symbolleiste) Benachrichtigungscode (Commctrl.h)
description: Benachrichtigt das übergeordnete Fenster eines Symbolleisten-Steuerelements, dass der Benutzer im Steuerelement auf die linke Maustaste doppelklickt. Dieser Benachrichtigungscode wird in Form einer WM \_ NOTIFY-Nachricht gesendet.
ms.assetid: c6198245-cfd4-4e1f-877d-94c1d47e09d2
keywords:
- NM_DBLCLK -Benachrichtigungscode (Symbolleiste) Windows Steuerelementen
topic_type:
- apiref
api_name:
- NM_DBLCLK
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 75abaf61938fbf377dbe8b6c5eaca99ff5ab027abe08c670de72a218dd51f1b1
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119919660"
---
# <a name="nm_dblclk-toolbar-notification-code"></a>NM \_ DBLCLK-Benachrichtigungscode (Symbolleiste)

Benachrichtigt das übergeordnete Fenster eines Symbolleisten-Steuerelements, dass der Benutzer im Steuerelement auf die linke Maustaste doppelklickt. Dieser Benachrichtigungscode wird in Form einer [**WM \_ NOTIFY-Nachricht**](wm-notify.md) gesendet.


```C++
NM_DBLCLK

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



 

 





