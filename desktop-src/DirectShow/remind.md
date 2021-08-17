---
description: Das REMIND-Makro generiert zur Kompilierzeit eine Erinnerung. Dieses Makro generiert eine Zeichenfolge, die die Parameterzeichenfolge, den Namen der Quelldatei und die Zeilennummer enthält.
ms.assetid: 12043df5-ed68-4980-91aa-7598d8ab1951
title: REMIND (Wxdebug.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- REMIND
api_type:
- LibDef
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: c17ec8fac190cd98803a0dfa85acff015d0ac2c18ce712cc87316dd2dca181bb
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118952119"
---
# <a name="remind"></a>Erinnern

Das `REMIND` Makro generiert zur Kompilierzeit eine Erinnerung. Dieses Makro generiert eine Zeichenfolge, die die Parameterzeichenfolge, den Namen der Quelldatei und die Zeilennummer enthält.

``` syntax
REMIND(strLiteral);
```

## <a name="parameters"></a>Parameter

<dl> <dt>

<span id="strLiteral"></span><span id="strliteral"></span><span id="STRLITERAL"></span>*strLiteral*
</dt> <dd>

Textzeichenfolge.

</dd> </dl>

## <a name="remarks"></a>Hinweise

Dieses Makro ist nützlich, um Warnungen zur Kompilierzeit zu generieren:


```C++
#pragma message (REMIND("TO DO: Add support for IDispatch."))
```



## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>Wxdebug.h (include Streams.h)</dt> </dl>                                                                                   |
| Bibliothek<br/> | <dl> <dt>Strmbase.lib (Einzelhandels-Builds); </dt> <dt>Strmbasd.lib (Debugbuilds)</dt> </dl> |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[Debugausgabefunktionen](debug-output-functions.md)
</dt> </dl>

 

 




