---
title: LVN_BEGINSCROLL Benachrichtigungscode (Commctrl.h)
description: Benachrichtigt das übergeordnete Fenster eines Listenansichtssteuerelements, wenn ein Bildlaufvorgang gestartet wird. Dieser Benachrichtigungscode wird in Form einer WM \_ NOTIFY-Nachricht gesendet.
ms.assetid: 67123db1-118c-43d7-8511-12a3c4413958
keywords:
- LVN_BEGINSCROLL Benachrichtigungscode Windows-Steuerelemente
topic_type:
- apiref
api_name:
- LVN_BEGINSCROLL
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e416aee093ed6526d85d81361e2774b963572de73ce84c21105f19d1675968f4
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119915220"
---
# <a name="lvn_beginscroll-notification-code"></a>LVN \_ BEGINSCROLL-Benachrichtigungscode

Benachrichtigt das übergeordnete Fenster eines Listenansichtssteuerelements, wenn ein Bildlaufvorgang gestartet wird. Dieser Benachrichtigungscode wird in Form einer [**WM \_ NOTIFY-Nachricht**](wm-notify.md) gesendet.


```C++
LVN_BEGINSCROLL

    pnmLVScroll = (LPNMLVSCROLL) lParam;
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*lParam* 
</dt> <dd>

Zeiger auf eine [**NMLVSCROLL-Struktur,**](/windows/win32/api/commctrl/ns-commctrl-nmlvscroll) die die horizontale oder vertikale Position des Startorts des Bildlaufvorgangs enthält.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Rückgabewert nicht verwendet.

## <a name="remarks"></a>Hinweise

> [!Note]  
> Um diesen Benachrichtigungscode verwenden zu können, müssen Sie ein Manifest angeben, das Comclt32.dll Version 6.0 angibt. Weitere Informationen zu Manifesten finden Sie unter [Aktivieren von visuellen Stilen.](cookbook-overview.md)

 

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows \[Nur Vista-Desktop-Apps\]<br/>                                        |
| Unterstützte Mindestversion (Server)<br/> | Windows Nur Server \[ 2003-Desktop-Apps\]<br/>                                  |
| Header<br/>                   | <dl> <dt>Commctrl.h</dt> </dl> |



 

 





