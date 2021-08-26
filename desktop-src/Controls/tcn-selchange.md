---
title: TCN_SELCHANGE Benachrichtigungscode (Commctrl.h)
description: Benachrichtigt das übergeordnete Fenster eines Registerkartensteuerelements, dass sich die aktuell ausgewählte Registerkarte geändert hat. Dieser Benachrichtigungscode wird in Form einer WM \_ NOTIFY-Nachricht gesendet.
ms.assetid: f40e30f6-169b-4381-a300-12c3befb5fc5
keywords:
- TCN_SELCHANGE Benachrichtigungscode Windows-Steuerelemente
topic_type:
- apiref
api_name:
- TCN_SELCHANGE
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e54ad012e98005e8fbf5148af58aab10d90e3127afeab6311cc8b8f3f84e2988
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119876180"
---
# <a name="tcn_selchange-notification-code"></a>TCN \_ SELCHANGE-Benachrichtigungscode

Benachrichtigt das übergeordnete Fenster eines Registerkartensteuerelements, dass sich die aktuell ausgewählte Registerkarte geändert hat. Dieser Benachrichtigungscode wird in Form einer [**WM \_ NOTIFY-Nachricht**](wm-notify.md) gesendet.


```C++
TCN_SELCHANGE 

    lpnmhdr = (LPNMHDR) lParam; 
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*lParam* 
</dt> <dd>

Zeiger auf eine [**NMHDR-Struktur,**](/windows/desktop/api/richedit/ns-richedit-nmhdr) die zusätzliche Informationen zu dieser Benachrichtigung enthält.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Kein Rückgabewert.

## <a name="remarks"></a>Hinweise

Verwenden Sie das [**\_ GetCurSel-Makro TabCtrl,**](/windows/desktop/api/Commctrl/nf-commctrl-tabctrl_getcursel) um die aktuell ausgewählte Registerkarte zu bestimmen.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows \[Nur Vista-Desktop-Apps\]<br/>                                        |
| Unterstützte Mindestversion (Server)<br/> | Windows Nur Server \[ 2003-Desktop-Apps\]<br/>                                  |
| Header<br/>                   | <dl> <dt>Commctrl.h</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[TCN \_ SELCHANGING](tcn-selchanging.md)
</dt> </dl>

 

 





