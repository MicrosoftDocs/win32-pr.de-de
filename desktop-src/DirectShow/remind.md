---
description: Das Erinnerungs Makro generiert zum Zeitpunkt der Kompilierung eine Erinnerung. Dieses Makro generiert eine Zeichenfolge, die die Parameter Zeichenfolge, den Namen der Quelldatei und die Zeilennummer enthält.
ms.assetid: 12043df5-ed68-4980-91aa-7598d8ab1951
title: Erinnerung (wxdebug. h)
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
ms.openlocfilehash: 305e5df628244293b643da8882f57dd83041c4c6
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106372074"
---
# <a name="remind"></a>Erinnern

Das `REMIND` Makro generiert zum Zeitpunkt der Kompilierung eine Erinnerung. Dieses Makro generiert eine Zeichenfolge, die die Parameter Zeichenfolge, den Namen der Quelldatei und die Zeilennummer enthält.

``` syntax
REMIND(strLiteral);
```

## <a name="parameters"></a>Parameter

<dl> <dt>

<span id="strLiteral"></span><span id="strliteral"></span><span id="STRLITERAL"></span>*"Straume"*
</dt> <dd>

Text Zeichenfolge.

</dd> </dl>

## <a name="remarks"></a>Bemerkungen

Dieses Makro ist nützlich zum Erzeugen von Warnungen zur Kompilierzeit:


```C++
#pragma message (REMIND("TO DO: Add support for IDispatch."))
```



## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>Wxdebug. h (Include Streams. h)</dt> </dl>                                                                                   |
| Bibliothek<br/> | <dl> " <dt>Straumbase. lib" (Einzelhandels Builds);</dt> " <dt>Straumbasd. lib" (Debugbuilds)</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[Debug-Ausgabefunktionen](debug-output-functions.md)
</dt> </dl>

 

 




