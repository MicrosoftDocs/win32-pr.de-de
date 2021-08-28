---
description: Das NAME-Makro generiert eine nur debugbasierte Zeichenfolge.
ms.assetid: 5cb9f803-dd2b-4055-bdcc-e754ef5fa505
title: NAME (Wxdebug.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- NAME
api_type:
- LibDef
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 9fa3d9c7e343dcbc8c6959a1ead025cafb3e4722382d7fd61c085bcff05347ec
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "120107680"
---
# <a name="name"></a>NAME

Das **NAME-Makro** generiert eine nur debugbasierte Zeichenfolge.

``` syntax
NAME(strLiteral);
```

## <a name="parameters"></a>Parameter

<dl> <dt>

<span id="strLiteral"></span><span id="strliteral"></span><span id="STRLITERAL"></span>*strLiteral*
</dt> <dd>

Textzeichenfolge.

</dd> </dl>

## <a name="remarks"></a>Hinweise

In Debugbuilds entspricht dieses Makro dem **TEXT-Makro.** In Einzelhandels-Builds wird in (TCHAR \* ) **NULL auflöset.** Dieses Makro ist nützlich, wenn der Name eines Objekts deklariert wird, das von der [**CBaseObject-Klasse abgeleitet**](cbaseobject.md) wird.


```C++
pObject = new CBaseObject(NAME("My Object"));
```



## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>Wxdebug.h (include Streams.h)</dt> </dl>                                                                                   |
| Bibliothek<br/> | <dl> <dt>Strmbase.lib (Einzelhandels-Builds); </dt> <dt>Strmbasd.lib (Debugbuilds)</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[Debugausgabefunktionen](debug-output-functions.md)
</dt> </dl>

 

 




