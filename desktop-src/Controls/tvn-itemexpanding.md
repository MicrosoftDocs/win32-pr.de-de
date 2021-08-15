---
title: TVN_ITEMEXPANDING Benachrichtigungscode (Commctrl.h)
description: Benachrichtigt das übergeordnete Fenster eines Strukturansicht-Steuerelements, dass die Liste der untergeordneten Elemente eines übergeordneten Elements erweitert oder reduziert werden soll. Dieser Benachrichtigungscode wird in Form einer WM \_ NOTIFY-Nachricht gesendet.
ms.assetid: 5ce256df-49e5-4fbf-9cdc-79dd2edbd8ec
keywords:
- TVN_ITEMEXPANDING Benachrichtigungscode Windows Steuerelementen
topic_type:
- apiref
api_name:
- TVN_ITEMEXPANDING
- TVN_ITEMEXPANDINGA
- TVN_ITEMEXPANDINGW
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7f4403b41682590d305b527d6445c208011b368b2d2474d66720ed32d29c80ca
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118957789"
---
# <a name="tvn_itemexpanding-notification-code"></a>TVN \_ ITEMEXPANDING-Benachrichtigungscode

Benachrichtigt das übergeordnete Fenster eines Strukturansicht-Steuerelements, dass die Liste der untergeordneten Elemente eines übergeordneten Elements erweitert oder reduziert werden soll. Dieser Benachrichtigungscode wird in Form einer [**WM \_ NOTIFY-Nachricht**](wm-notify.md) gesendet.


```C++
TVN_ITEMEXPANDING 

    pnmtv = (LPNMTREEVIEW) lParam 
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*lParam* 
</dt> <dd>

Zeiger auf eine [**NMTREEVIEW-Struktur.**](/windows/win32/api/commctrl/ns-commctrl-nmtreeviewa) Das **itemNew-Element** ist eine [**TVITEM-Struktur,**](/windows/win32/api/commctrl/ns-commctrl-tvitema) die gültige Informationen über das übergeordnete Element in den **Membern hItem**, **state** und **lParam** enthält. Das **Aktionsmitglied** gibt an, ob die Liste erweitert oder reduziert werden soll. Eine Liste der möglichen Werte finden Sie in der Beschreibung der [**MELDUNG TVM \_ EXPAND.**](tvm-expand.md)

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Gibt **TRUE zurück,** um zu verhindern, dass die Liste erweitert oder verklappt wird.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows Nur \[ Vista-Desktop-Apps\]<br/>                                        |
| Unterstützte Mindestversion (Server)<br/> | Windows Nur Server \[ 2003-Desktop-Apps\]<br/>                                  |
| Header<br/>                   | <dl> <dt>Commctrl.h</dt> </dl> |
| Unicode- und ANSI-Name<br/>   | **TVN \_ ITEMEXPANDINGW** (Unicode) und **TVN \_ ITEMEXPANDINGA** (ANSI)<br/>       |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[TVN \_ ITEMEXPANDED](tvn-itemexpanded.md)
</dt> </dl>

 

 





