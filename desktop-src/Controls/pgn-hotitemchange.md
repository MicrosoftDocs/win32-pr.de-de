---
title: PGN_HOTITEMCHANGE (Commctrl.h)
description: Benachrichtigt das übergeordnete Fenster eines Pagersteuerelements, dass sich das heiße (hervorgehobene) Element geändert hat. Dieser Benachrichtigungscode wird in Form einer WM \_ NOTIFY-Nachricht gesendet.
ms.assetid: 0f59677c-0251-49f4-b909-6fac6d93f354
keywords:
- PGN_HOTITEMCHANGE message Windows Controls
topic_type:
- apiref
api_name:
- PGN_HOTITEMCHANGE
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a6510eeb648ad883d04ccc0baf916223bb5209d110c2237ef3bf618d241c2ede
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "117830134"
---
# <a name="pgn_hotitemchange-message"></a>PGN \_ HOTITEMCHANGE-Nachricht

Benachrichtigt das übergeordnete Fenster eines Pagersteuerelements, dass sich das heiße (hervorgehobene) Element geändert hat. Dieser Benachrichtigungscode wird in Form einer [**WM \_ NOTIFY-Nachricht**](wm-notify.md) gesendet.


```C++
PGN_HOTITEMCHANGE

    pnmPGHotItem = (LPNMPGHOTITEM) lParam;
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*lParam* 
</dt> <dd>

Zeiger auf eine [**NMPGHOTITEM-Struktur,**](/windows/win32/api/commctrl/ns-commctrl-nmpghotitem) die Informationen zu diesem Benachrichtigungscode enthält.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Geben Sie 0 (null) zurück, um das Element oder einen Wert ungleich 0 (null) zu markieren, um eine Hervorhebung zu verhindern.

## <a name="remarks"></a>Hinweise

> [!Note]  
> Um diesen Benachrichtigungscode verwenden zu können, müssen Sie ein Manifest angeben, das Comclt32.dll 6.0 an. Weitere Informationen zu Manifesten finden Sie unter [Aktivieren von visuellen Stilen.](cookbook-overview.md)

 

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows Nur \[ Vista-Desktop-Apps\]<br/>                                        |
| Unterstützte Mindestversion (Server)<br/> | Windows Nur Server \[ 2003-Desktop-Apps\]<br/>                                  |
| Header<br/>                   | <dl> <dt>Commctrl.h</dt> </dl> |



 

 





