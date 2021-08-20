---
title: RBN_AUTOBREAK (Commctrl.h)
description: Benachrichtigt das übergeordnete Element einer Rebar, dass eine Unterbrechung in der Leiste angezeigt wird. Das übergeordnete Element bestimmt, ob die Unterbrechung festgelegt werden soll. Dieser Benachrichtigungscode wird in Form einer WM \_ NOTIFY-Nachricht gesendet.
ms.assetid: b7a63027-6cfa-4d5a-9ea6-fdd8b4fb6864
keywords:
- RBN_AUTOBREAK von Windows-Steuerelementen
topic_type:
- apiref
api_name:
- RBN_AUTOBREAK
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e63a6b0279199bc0c1d96f0d31884b85e13b9c42036bf0e0f98404825eb66e5b
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118169232"
---
# <a name="rbn_autobreak-message"></a>RBN \_ AUTOBREAK-Meldung

Benachrichtigt das übergeordnete Element [einer Rebar,](rebar-controls.md) dass eine Unterbrechung in der Leiste angezeigt wird. Das übergeordnete Element bestimmt, ob die Unterbrechung festgelegt werden soll. Dieser Benachrichtigungscode wird in Form einer [**WM \_ NOTIFY-Nachricht**](wm-notify.md) gesendet.


```C++
RBN_AUTOBREAK

    pnmRebarAutoBreak = (LPNMREBARAUTOBREAK) lParam;
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*lParam* 
</dt> <dd>

Zeiger auf eine [**NMREBARAUTOBREAK-Struktur,**](/windows/win32/api/commctrl/ns-commctrl-nmrebarautobreak) die Informationen zum Benachrichtigungscode enthält.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Der Rückgabewert für diese Benachrichtigung wird nicht verwendet.

## <a name="remarks"></a>Hinweise

Der Wert im **fAutoBreak-Member** der [**NMREBARAUTOBREAK-Struktur**](/windows/win32/api/commctrl/ns-commctrl-nmrebarautobreak) gibt an, ob in der Leiste ein Break auftreten soll.

Um diesen Benachrichtigungscode zu verwenden, geben Comctl32.dll 6 im Manifest an. Weitere Informationen zu Manifesten finden Sie unter [Aktivieren von visuellen Stilen.](cookbook-overview.md)

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows Nur \[ Vista-Desktop-Apps\]<br/>                                        |
| Unterstützte Mindestversion (Server)<br/> | Windows Nur Server \[ 2003-Desktop-Apps\]<br/>                                  |
| Header<br/>                   | <dl> <dt>Commctrl.h</dt> </dl> |



 

 





