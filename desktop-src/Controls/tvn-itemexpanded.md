---
title: TVN_ITEMEXPANDED Benachrichtigungscode (Commctrl.h)
description: Benachrichtigt das übergeordnete Fenster eines Strukturansicht-Steuerelements, dass die Liste der untergeordneten Elemente eines übergeordneten Elements erweitert oder reduziert wurde. Dieser Benachrichtigungscode wird in Form einer WM \_ NOTIFY-Nachricht gesendet.
ms.assetid: 18d9d61d-6ec5-4d3b-9c02-36d0e61ed232
keywords:
- TVN_ITEMEXPANDED Benachrichtigungscode Windows Steuerelementen
topic_type:
- apiref
api_name:
- TVN_ITEMEXPANDED
- TVN_ITEMEXPANDEDA
- TVN_ITEMEXPANDEDW
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 18af761c7580707bfd0926874e25069ca15b564bf6ef205cd6dc7aaaecb6a772
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119018628"
---
# <a name="tvn_itemexpanded-notification-code"></a>TVN \_ ITEMEXPANDED-Benachrichtigungscode

Benachrichtigt das übergeordnete Fenster eines Strukturansicht-Steuerelements, dass die Liste der untergeordneten Elemente eines übergeordneten Elements erweitert oder reduziert wurde. Dieser Benachrichtigungscode wird in Form einer [**WM \_ NOTIFY-Nachricht**](wm-notify.md) gesendet.


```C++
TVN_ITEMEXPANDED 

    pnmtv = (LPNMTREEVIEW) lParam 
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*lParam* 
</dt> <dd>

Zeiger auf eine [**NMTREEVIEW-Struktur.**](/windows/win32/api/commctrl/ns-commctrl-nmtreeviewa) Das **itemNew-Element** ist eine [**TVITEM-Struktur,**](/windows/win32/api/commctrl/ns-commctrl-tvitema) die gültige Informationen über das übergeordnete Element in den **Membern hItem**, **state** und **lParam** enthält. Das **Aktionsmitglied** gibt an, ob die Liste erweitert oder reduziert wurde. Eine Liste der möglichen Werte finden Sie in der Beschreibung der [**MELDUNG TVM \_ EXPAND.**](tvm-expand.md)

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Der Rückgabewert wird ignoriert.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows Nur \[ Vista-Desktop-Apps\]<br/>                                        |
| Unterstützte Mindestversion (Server)<br/> | Windows Nur Server \[ 2003-Desktop-Apps\]<br/>                                  |
| Header<br/>                   | <dl> <dt>Commctrl.h</dt> </dl> |
| Unicode- und ANSI-Name<br/>   | **TVN \_ ITEMEXPANDEDW** (Unicode) und **TVN \_ ITEMEXPANDEDA** (ANSI)<br/>         |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[TVN \_ ITEMEXPANDING](tvn-itemexpanding.md)
</dt> </dl>

 

 





