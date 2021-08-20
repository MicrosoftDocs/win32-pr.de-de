---
description: Private Nachricht, die den Fensterstil auf WS \_ EX TOPMOST (WS EX \_ TOPMOST) setzt.
ms.assetid: 4934400e-4ca5-4ace-b9b9-3889f4cf610e
title: CBaseWindow::m_ShowStageTop-Member (Winutil.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- m_ShowStageTop
api_type:
- LibDef
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: dbd8943b297d6e33f3b86a62c7e67dd2039a6b99d316061be30a4c3016711c41
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119016518"
---
# <a name="cbasewindowm_showstagetop-member"></a>CBaseWindow::m \_ ShowStageTop-Member

Private Nachricht, die den Fensterstil auf WS \_ EX TOPMOST (WS EX \_ TOPMOST) setzt.

## <a name="syntax"></a>Syntax


```C++
UINT m_ShowStageTop;
```



## <a name="remarks"></a>Hinweise

Videorenderer sollten diese Nachricht an das Fenster senden, wenn sie in den Vollbildmodus wechseln.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>Winutil.h (include Streams.h)</dt> </dl>                                                                                   |
| Bibliothek<br/> | <dl> <dt>Strmbase.lib (Einzelhandels-Builds); </dt> <dt>Strmbasd.lib (Debugbuilds)</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**CBaseWindow-Klasse**](cbasewindow.md)
</dt> </dl>

 

 




