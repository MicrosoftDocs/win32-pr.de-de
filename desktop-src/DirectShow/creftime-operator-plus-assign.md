---
description: Der Operator += fügt zwei Verweiszeiten hinzu.
ms.assetid: 016d3dac-4d7c-490a-83aa-1d88a2080748
title: CRefTime.operator+=-Methode (Reftime.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CRefTime.operator+=
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 2280eca51cef8c84cb51f806a0c95748070459bf0a48670ca6144b2d499fd337
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "120108050"
---
# <a name="creftimeoperator-method"></a>CRefTime.operator+=-Methode

Der Operator += fügt zwei Verweiszeiten hinzu.

## <a name="syntax"></a>Syntax


```C++
CRefTime& operator+=(
  [ref] const CRefTime &rt
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*rt* \[ Ref\]
</dt> <dd>

Verweis auf ein **CRefTime-Objekt.**

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Gibt einen Verweis auf das -Objekt zurück.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>Reftime.h (include Streams.h)</dt> </dl>                                                                                   |
| Bibliothek<br/> | <dl> <dt>Strmbase.lib (Verkaufsbuilds); </dt> <dt>Strmbasd.lib (Debugbuilds)</dt> </dl> |



 

 




