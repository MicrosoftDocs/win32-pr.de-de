---
description: Flag, das angibt, ob sich die Qualität geändert hat.
ms.assetid: 9084ab1d-b6a0-4e87-a653-86e64c74b07f
title: CTransformFilter::m_bQualityChanged-Member (Transfrm.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- m_bQualityChanged
api_type:
- LibDef
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 454d8bad4ced2291b061b09992ad450d9e483f269e3fd72b192adbbacb077d7c
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118953609"
---
# <a name="ctransformfilterm_bqualitychanged-member"></a>CTransformFilter::m \_ bQualityChanged-Member

Flag, das angibt, ob sich die Qualität geändert hat. Wenn der Filter ein Beispiel zum ersten Mal löscht, sendet er ein [**EC \_ QUALITY \_ CHANGE-Ereignis**](ec-quality-change.md) an den Filterdiagramm-Manager und legt dieses Flag auf **TRUE fest.** Dieses Ereignis wird erst dann erneut gesendet, wenn der Filter beendet und neu gestartet wird, auch wenn er in der Zwischenzeit weiterhin Stichproben abbricht.

## <a name="syntax"></a>Syntax


```C++
BOOL m_bQualityChanged;
```



## <a name="requirements"></a>Requirements (Anforderungen)



| Anforderung | Wert |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>Transfrm.h (include Streams.h)</dt> </dl>                                                                                  |
| Bibliothek<br/> | <dl> <dt>Strmbase.lib (Einzelhandels-Builds); </dt> <dt>Strmbasd.lib (Debugbuilds)</dt> </dl> |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[**CTransformFilter-Klasse**](ctransformfilter.md)
</dt> </dl>

 

 




