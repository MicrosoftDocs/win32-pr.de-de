---
description: Die m \_ EndSample-Membervariable gibt die Endzeit des letzten Beispiels an.
ms.assetid: 694815b6-8da5-4174-b2c7-7d686a557c6c
title: CDrawImage::m_EndSample-Member (Winutil.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- m_EndSample
api_type:
- LibDef
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 2877e709cb7d0d8a259dfa91e1ebe3b723771493e012bf29eef0fffe1c7eaeaa
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118656983"
---
# <a name="cdrawimagem_endsample-member"></a>CDrawImage::m \_ EndSample-Member

Die `m_EndSample` Membervariable gibt die Stoppzeit des letzten Beispiels an.

## <a name="syntax"></a>Syntax


```C++
CRefTime m_EndSample;
```



## <a name="remarks"></a>Hinweise

Der Wert ist nur innerhalb der [**CDrawImage::D isplaySampleTimes-Methode**](cdrawimage-displaysampletimes.md) gültig.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>Winutil.h (include Streams.h)</dt> </dl>                                                                                   |
| Bibliothek<br/> | <dl> <dt>Strmbase.lib (Einzelhandels-Builds); </dt> <dt>Strmbasd.lib (Debugbuilds)</dt> </dl> |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[**CDrawImage-Klasse**](cdrawimage.md)
</dt> </dl>

 

 




