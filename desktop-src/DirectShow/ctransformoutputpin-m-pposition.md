---
description: 'CTransformOutputPin::m_pPosition Member : Hilfsobjekt zum Übergeben von Seek-Befehlen im Upstream.'
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
ms.openlocfilehash: b9c5a1b5d5ced7a9f3985ceebdd2bdcb8e491d2e
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2021
ms.locfileid: "108084858"
---
# <a name="ctransformoutputpinm_pposition-member"></a>CTransformOutputPin::m \_ pPosition-Member

Hilfsobjekt zum Übergeben von Suchbefehlen im Upstream.

## <a name="syntax"></a>Syntax


```C++
IUnknown *m_pPosition;
```



## <a name="remarks"></a>Bemerkungen

Wenn der Pin zum ersten Mal nach der [**IMediaPosition-**](/windows/desktop/api/Control/nn-control-imediaposition) oder [**IMediaSeeking-Schnittstelle**](/windows/desktop/api/Strmif/nn-strmif-imediaseeking) abgefragt wird, wird ein [**CPosPassThru-Hilfsobjekt**](cpospassthru.md) erstellt und aggregiert.

## <a name="requirements"></a>Anforderungen



| Anforderungen | Wert |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>Transfrm.h (include Streams.h)</dt> </dl>                                                                                  |
| Bibliothek<br/> | <dl> <dt>Strmbase.lib (Verkaufsbuilds); </dt> <dt>Strmbasd.lib (Debugbuilds)</dt> </dl> |



 

 




