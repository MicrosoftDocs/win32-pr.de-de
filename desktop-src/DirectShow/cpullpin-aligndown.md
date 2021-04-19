---
description: Die aligndown-Methode verkürzt einen Wert auf eine angegebene Ausrichtungs Grenze.
ms.assetid: f0efdedb-67ec-49d6-92a8-54485aa04e15
title: Cpullpin. aligndown-Methode (pullpin. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CPullPin.AlignDown
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 1383517f4931fa153fd141878475cc8775a61045
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106359392"
---
# <a name="cpullpinaligndown-method"></a>Cpullpin. aligndown-Methode

Die- `AlignDown` Methode verkürzt einen Wert auf eine angegebene Ausrichtungs Grenze.

## <a name="syntax"></a>Syntax


```C++
LONGLONG AlignDown(
   LONGLONG ll,
   LONG     lAlign
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*ll* 
</dt> <dd>

Gibt die Zahl an, die ausgerichtet werden soll.

</dd> <dt>

*lalign* 
</dt> <dd>

Gibt die Ausrichtungs Grenze an.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Gibt das ausgerichtete Ergebnis zurück.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>Pullpin. h</dt> </dl>                                                                                                       |
| Bibliothek<br/> | <dl> " <dt>Straumbase. lib" (Einzelhandels Builds);</dt> " <dt>Straumbasd. lib" (Debugbuilds)</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**Cpullpin-Klasse**](cpullpin.md)
</dt> </dl>

 

 




