---
description: Das Name-Makro generiert eine reine debugzeichenfolge.
ms.assetid: 5cb9f803-dd2b-4055-bdcc-e754ef5fa505
title: Name (wxdebug. h)
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
ms.openlocfilehash: 0b698551789deb0c3775bd4ac722136e1abc9d38
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106373760"
---
# <a name="name"></a>NAME

Das **Name** -Makro generiert eine reine debugzeichenfolge.

``` syntax
NAME(strLiteral);
```

## <a name="parameters"></a>Parameter

<dl> <dt>

<span id="strLiteral"></span><span id="strliteral"></span><span id="STRLITERAL"></span>*"Straume"*
</dt> <dd>

Text Zeichenfolge.

</dd> </dl>

## <a name="remarks"></a>Bemerkungen

In Debugbuilds entspricht dieses Makro dem **Text** Makro. In Einzelhandels Builds wird Sie in (TCHAR \* ) **null** aufgelöst. Dieses Makro ist hilfreich beim Deklarieren des Namens eines Objekts, das von der [**cbaseobject**](cbaseobject.md) -Klasse abgeleitet wird.


```C++
pObject = new CBaseObject(NAME("My Object"));
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

 

 




