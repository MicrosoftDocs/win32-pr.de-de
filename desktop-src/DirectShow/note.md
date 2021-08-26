---
description: Das NOTE-Makro sendet eine Zeichenfolge an den Debugausgabespeicherort. Wird in Einzelhandelsbuilds ignoriert.
ms.assetid: 8b85861a-b4d6-4cc6-9ac9-77d06f173869
title: HINWEIS (Wxdebug.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- NOTE
api_type:
- LibDef
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 0becacba37f3f474577c36a694539de77795f1c19ccf3b1655cb80370be9e297
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "120050920"
---
# <a name="note"></a>HINWEIS

Das `NOTE` Makro sendet eine Zeichenfolge an den Debugausgabespeicherort. Wird in Einzelhandelsbuilds ignoriert.

``` syntax
NOTE(
    pFormat
);

NOTEn(
    pFormat,
    arg1 ... arg5
);
```

## <a name="parameters"></a>Parameter

<dl> <dt>

<span id="pFormat"></span><span id="pformat"></span><span id="PFORMAT"></span>*pFormat*
</dt> <dd>

Eine Formatzeichenfolge im printf-Format.

</dd> <dt>

<span id="arg1arg5"></span><span id="ARG1ARG5"></span>*arg1*–*arg5*
</dt> <dd>

Zusätzliche Argumente für die Formatzeichenfolge. Die Anzahl der Argumente muss mit dem Makronamen übereinstimmen. Note1  verwendet beispielsweise ein Argument, **NOTE5** fünf Argumente.

</dd> </dl>

## <a name="remarks"></a>Hinweise

Diese Makros sind Varianten des [**DbgLog-Makros.**](dbglog.md) Sie generieren LOG TRACE-Meldungen der Ebene \_ 5.

## <a name="example"></a>Beispiel


```C++
NOTE("Warning, failed to created graph.");
NOTE2("Width: %d, Height: %d", width, height);
```



## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>Wxdebug.h (include Streams.h)</dt> </dl>                                                                                   |
| Bibliothek<br/> | <dl> <dt>Strmbase.lib (Verkaufsbuilds); </dt> <dt>Strmbasd.lib (Debugbuilds)</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[Debuggen von Ausgabefunktionen](debug-output-functions.md)
</dt> </dl>

 

 




