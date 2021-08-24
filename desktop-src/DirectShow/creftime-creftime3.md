---
description: 'CRefTime.CRefTime-Konstruktor (Reftime.h): Konstruktormethode.'
ms.assetid: c1282676-6f2b-438a-850e-17bb6d7a2c68
title: CRefTime.CRefTime-Konstruktor (Reftime.h) – rt-Parameter
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CRefTime.CRefTime
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 0ab8d2124e63be2c85f5a056e2f546f70c5441a24f427594bb775e14e4788490
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119073404"
---
# <a name="creftimecreftime-constructor-reftimeh"></a>CRefTime.CRefTime-Konstruktor (Reftime.h)

Konstruktormethode.

## <a name="syntax"></a>Syntax


```C++
CRefTime(
   REFERENCE_TIME rt
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*Rt* 
</dt> <dd>

Zeit in Einheiten von 100 Nanosekunden.

</dd> </dl>

## <a name="remarks"></a>Hinweise

Die Verweiszeit ist standardmäßig auf 0 (null) festgelegt.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>Reftime.h (include Streams.h)</dt> </dl>                                                                                   |
| Bibliothek<br/> | <dl> <dt>Strmbase.lib (Verkaufsbuilds); </dt> <dt>Strmbasd.lib (Debugbuilds)</dt> </dl> |



 

 




