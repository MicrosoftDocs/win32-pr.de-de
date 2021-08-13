---
title: HDN_FILTERBTNCLICK Benachrichtigungscode (Commctrl.h)
description: Benachrichtigt das übergeordnete Fenster des Headersteuerfelds, wenn auf die Filterschaltfläche oder als Reaktion auf eine HDM \_ SETITEM-Meldung geklickt wird. Dieser Benachrichtigungscode wird in Form einer WM \_ NOTIFY-Nachricht gesendet.
ms.assetid: 36b85cdc-1022-4568-8891-0c919c850fd4
keywords:
- HDN_FILTERBTNCLICK Benachrichtigungscode Windows Steuerelementen
topic_type:
- apiref
api_name:
- HDN_FILTERBTNCLICK
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 01ba216c9946854ccfc6a651db90ab1dd5ed106dfca6ddf568d485c33dae70ab
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119435510"
---
# <a name="hdn_filterbtnclick-notification-code"></a>\_HDN-FILTERBTNCLICK-Benachrichtigungscode

Benachrichtigt das übergeordnete Fenster des Headersteuerfelds, wenn auf die Filterschaltfläche oder als Reaktion auf eine [**HDM \_ SETITEM-Meldung geklickt**](hdm-setitem.md) wird. Dieser Benachrichtigungscode wird in Form einer [**WM \_ NOTIFY-Nachricht**](wm-notify.md) gesendet.


```C++
HDN_FILTERBTNCLICK

    pNMHDFilterBtnClk = (LPNMHDFILTERBTNCLICK) lParam;
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*lParam* 
</dt> <dd>

Ein Zeiger auf eine [**NMHDFILTERBTNCLICK-Struktur,**](/windows/win32/api/commctrl/ns-commctrl-nmhdfilterbtnclick) die Informationen über das Headersteuerfeld und die Headerfilterschaltfläche enthält.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Wenn Sie **TRUE zurückgeben,** wird ein [HDN \_ FILTERCHANGE-Benachrichtigungscode](hdn-filterchange.md) an das übergeordnete Fenster des Header-Steuerelements gesendet. Dieser Benachrichtigungscode gibt dem übergeordneten Fenster die Möglichkeit, seine Benutzeroberflächenelemente zu synchronisieren. Geben **Sie FALSE** zurück, wenn die Benachrichtigung nicht gesendet werden soll.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows Nur \[ Vista-Desktop-Apps\]<br/>                                        |
| Unterstützte Mindestversion (Server)<br/> | Windows Nur Server \[ 2003-Desktop-Apps\]<br/>                                  |
| Header<br/>                   | <dl> <dt>Commctrl.h</dt> </dl> |



## <a name="see-also"></a>Weitere Informationen:

<dl> <dt>

[**NMHDFILTERBTNCLICK**](/windows/win32/api/commctrl/ns-commctrl-nmhdfilterbtnclick)
</dt> </dl>

 

 





