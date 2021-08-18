---
title: TVN_SELCHANGING Benachrichtigungscode (Commctrl.h)
description: Benachrichtigt das übergeordnete Fenster eines Strukturansichtssteuerelements, dass die Auswahl von einem Element in ein anderes geändert werden soll. Dieser Benachrichtigungscode wird in Form einer WM \_ NOTIFY-Nachricht gesendet.
ms.assetid: 53f24ee0-433c-4680-9075-5e2b21117ed9
keywords:
- TVN_SELCHANGING Benachrichtigungscode Windows-Steuerelemente
topic_type:
- apiref
api_name:
- TVN_SELCHANGING
- TVN_SELCHANGINGA
- TVN_SELCHANGINGW
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4b09933e1e4c7393521f298c60435efde76fbea23ef703f536fb241cc9f78610
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119433480"
---
# <a name="tvn_selchanging-notification-code"></a>TVN \_ SELCHANGING-Benachrichtigungscode

Benachrichtigt das übergeordnete Fenster eines Strukturansichtssteuerelements, dass die Auswahl von einem Element in ein anderes geändert werden soll. Dieser Benachrichtigungscode wird in Form einer [**WM \_ NOTIFY-Nachricht**](wm-notify.md) gesendet.


```C++
TVN_SELCHANGING 

    pnmtv = (LPNMTREEVIEW) lParam 
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*lParam* 
</dt> <dd>

Zeiger auf eine [**NMTREEVIEW-Struktur.**](/windows/win32/api/commctrl/ns-commctrl-nmtreeviewa) Die Elemente **itemOld** und **itemNew** enthalten gültige Informationen über das aktuell ausgewählte Element und das neu ausgewählte Element. Der **Aktionsmember** gibt an, ob sich die Auswahl durch eine Maus- oder Tastaturaktion ändert. Eine Liste der möglichen Werte finden Sie in der Beschreibung des [TVN SELCHANGED-Benachrichtigungscodes. \_ ](tvn-selchanged.md)

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Gibt **TRUE** zurück, um zu verhindern, dass sich die Auswahl ändert.

## <a name="remarks"></a>Hinweise

Wenn Anwendungen auf diesen Benachrichtigungscode reagieren, sollten sie die Elemente, die die Auswahl erhalten oder verlieren, nicht löschen.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows \[Nur Vista-Desktop-Apps\]<br/>                                        |
| Unterstützte Mindestversion (Server)<br/> | Windows Nur Server \[ 2003-Desktop-Apps\]<br/>                                  |
| Header<br/>                   | <dl> <dt>Commctrl.h</dt> </dl> |
| Unicode- und ANSI-Name<br/>   | **TVN \_ SELCHANGINGW** (Unicode) und **TVN \_ SELCHANGINGA** (ANSI)<br/>           |



 

 





