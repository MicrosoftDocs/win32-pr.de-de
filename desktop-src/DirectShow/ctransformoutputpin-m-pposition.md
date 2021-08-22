---
description: 'CTransformOutputPin::m_pPosition Member : Hilfsobjekt zum Übergeben von Seek-Befehlen upstream.'
ms.assetid: 2ca9bae7-a133-4e09-8aa7-1c4601ec5db0
title: CTransformOutputPin::m_pPosition-Member (Transfrm.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- m_pPosition
api_type:
- LibDef
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: bfa565d38fa982ea457da13ee9cf08a1d0f2fe8d5ba52ef3c5b86379fc02b509
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119538160"
---
# <a name="ctransformoutputpinm_pposition-member"></a>CTransformOutputPin::m \_ pPosition-Member

Hilfsobjekt zum Übergeben von Suchbefehlen upstream.

## <a name="syntax"></a>Syntax


```C++
IUnknown *m_pPosition;
```



## <a name="remarks"></a>Hinweise

Wenn der Pin zum ersten Mal nach der [**IMediaPosition-**](/windows/desktop/api/Control/nn-control-imediaposition) oder [**IMediaSeeking-Schnittstelle**](/windows/desktop/api/Strmif/nn-strmif-imediaseeking) abgefragt wird, wird ein [**CPosPassThru-Hilfsobjekt**](cpospassthru.md) erstellt und aggregiert.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>Transfrm.h (include Streams.h)</dt> </dl>                                                                                  |
| Bibliothek<br/> | <dl> <dt>Strmbase.lib (Verkaufsbuilds); </dt> <dt>Strmbasd.lib (Debugbuilds)</dt> </dl> |



 

 




