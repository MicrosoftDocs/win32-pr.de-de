---
description: Das Note-Makro sendet eine Zeichenfolge an den debugausgabespeicherort. Wird in Einzelhandels Builds ignoriert.
ms.assetid: 8b85861a-b4d6-4cc6-9ac9-77d06f173869
title: Hinweis (wxdebug. h)
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
ms.openlocfilehash: 898d31c48807c3bf0826dc643d89126db36b0f0b
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106361480"
---
# <a name="note"></a>HINWEIS

Das- `NOTE` Makro sendet eine Zeichenfolge an den debugausgabeort. Wird in Einzelhandels Builds ignoriert.

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

<span id="pFormat"></span><span id="pformat"></span><span id="PFORMAT"></span>*pformat*
</dt> <dd>

Eine Format Zeichenfolge im printf-Format.

</dd> <dt>

<span id="arg1arg5"></span><span id="ARG1ARG5"></span>*arg1*–*arg5*
</dt> <dd>

Zusätzliche Argumente für die Format Zeichenfolge. Die Anzahl der Argumente muss mit dem Namen des Makros identisch sein. Beispielsweise übernimmt **NOTE1** ein Argument, und **NOTE5** übernimmt fünf Argumente.

</dd> </dl>

## <a name="remarks"></a>Bemerkungen

Diese Makros sind Varianten des [**dbglog**](dbglog.md) -Makros. Sie generieren Protokoll-Ablauf \_ Verfolgungs Meldungen der Ebene 5.

## <a name="example"></a>Beispiel


```C++
NOTE("Warning, failed to created graph.");
NOTE2("Width: %d, Height: %d", width, height);
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

 

 




