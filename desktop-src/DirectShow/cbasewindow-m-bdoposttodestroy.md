---
description: Flag, das angibt, ob das Fenster seine Zerstörungsmeldung sendet oder sendet.
ms.assetid: 553a372e-1abe-4661-bfa5-b8a63be63c72
title: CBaseWindow::m_bDoPostToDestroy-Member (Winutil.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- m_bDoPostToDestroy
api_type:
- LibDef
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 070b94cc75fa3fb2d9b5983901abc2406b2e601ec3370323854905708ee681f2
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118954609"
---
# <a name="cbasewindowm_bdoposttodestroy-member"></a>CBaseWindow::m \_ bDoPostToDestroy-Member

Flag, das angibt, ob das Fenster seine Zerstörungsmeldung sendet oder sendet. True gibt an, dass die [**CBaseWindow::D oneWithWindow-Methode**](cbasewindow-donewithwindow.md) die **PostMessage-Funktion** verwendet, um sich selbst eine private Zerstörungsnachricht zu senden. **False** gibt an, dass **DoneWithWindow** die **SendMessage-Funktion** verwendet, um die Nachricht zu senden. Standardmäßig ist der Wert **FALSE.**

## <a name="syntax"></a>Syntax


```C++
BOOL m_bDoPostToDestroy;
```



## <a name="requirements"></a>Requirements (Anforderungen)



| Anforderung | Wert |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>Winutil.h (include Streams.h)</dt> </dl>                                                                                   |
| Bibliothek<br/> | <dl> <dt>Strmbase.lib (Verkaufsbuilds); </dt> <dt>Strmbasd.lib (Debugbuilds)</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**CBaseWindow-Klasse**](cbasewindow.md)
</dt> </dl>

 

 




