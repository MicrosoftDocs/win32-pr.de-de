---
description: Legt den FOURCC-Teil des FOURCCMap-Objekts fest.
ms.assetid: cc821e39-e565-4255-a289-2c9507d43433
title: FOURCCMap::SetFOURCC-Methode (Fourcc.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- FOURCCMap.SetFOURCC
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 03ac14c7174fde7184bfdbfbb5d82d3fc1288d46ff37158bbbab146c34db5ed9
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119536830"
---
# <a name="fourccmapsetfourcc-method"></a>FOURCCMap::SetFOURCC-Methode

Legt den **FOURCC-Teil** des [**FOURCCMap-Objekts**](fourccmap.md) fest.

## <a name="syntax"></a>Syntax


```C++
void SetFOURCC(
   const GUID *pguid
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*pguid* 
</dt> <dd>

Zeiger auf den zurückgegebenen global eindeutigen Bezeichner **(GUID)** des **FOURCCMap-Objekts.**

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Kein Rückgabewert.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>Fourcc.h (include Streams.h)</dt> </dl>                                                                                    |
| Bibliothek<br/> | <dl> <dt>Strmbase.lib (Verkaufsbuilds); </dt> <dt>Strmbasd.lib (Debugbuilds)</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**FOURCCMap-Klasse**](fourccmap.md)
</dt> </dl>

 

 




