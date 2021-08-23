---
description: Die llMulDiv-Funktion implementiert die Formel ((a \* b)+rnd)/c, wobei jeder Begriff ein 64-Bit-Wert ist.
ms.assetid: cd5073b9-27c7-42ee-8487-2d4ea29f77d4
title: llMulDiv-Funktion (Wxutil.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Int64x32Div32
api_type:
- LibDef
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: df58175955106906027a6d2d10c465b82ad6313cd493e3ef9ef3ba279cd0115f
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118952349"
---
# <a name="llmuldiv-function"></a>llMulDiv-Funktion

Die `llMulDiv` Funktion implementiert die Formel, wobei jeder Begriff ein `((a*b)+rnd)/c` 64-Bit-Wert ist.

Zeitstempel und Suchzeiten sind 64-Bit-Werte, daher ist diese Funktion nützlich für Konvertierungen auf 32-Bit-Systemen. Die Formel für Bytes pro Sekunde ist z. B.


```C++
(Number of Bytes * Reference Time) / 10,000,000
```



kann als berechnet `llMulDiv(nBytes, rtTime, 10000000, 0)` werden. Verwenden Sie *den rnd-Parameter* als Rundungsfaktor.

## <a name="syntax"></a>Syntax


```C++
LONGLONG WINAPI Int64x32Div32(
   LONGLONG a,
   LONGLONG b,
   LONGLONG c,
   LONGLONG rnd
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*Eine* 
</dt> <dd>

Multiplikation.

</dd> <dt>

*b* 
</dt> <dd>

Multiplikator.

</dd> <dt>

*c* 
</dt> <dd>

Divisor.

</dd> <dt>

*Rnd* 
</dt> <dd>

Rundungsfaktor.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Gibt entweder die `(a * b + rnd)/c` Berechnung oder einen der folgenden Werte zurück.



| Rückgabecode                                                                                       | Beschreibung                                                              |
|---------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------|
| <dl> <dt>**0x7FFFFFFFFFFFFFFF**</dt> </dl> | Überlauf aufgetreten, weil das Ergebnis zu groß (positiv) ist.<br/> |
| <dl> <dt>**0x8000000000000000**</dt> </dl> | Ein Überlauf ist aufgetreten, weil das Ergebnis zu groß (negativ) ist.<br/> |



 

## <a name="remarks"></a>Hinweise

Die Rundung für die Division ist in Richtung 0 (null) ausgerichtet. Division durch 0 (null) wird als Überlaufbedingung gezählt.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>Wxutil.h (include Streams.h)</dt> </dl>                                                                                    |
| Bibliothek<br/> | <dl> <dt>Strmbase.lib (Einzelhandels-Builds); </dt> <dt>Strmbasd.lib (Debugbuilds)</dt> </dl> |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[Verschiedene Hilfsfunktionen](miscellaneous-helper-functions.md)
</dt> <dt>

[**Int64x32Div32**](int64x32div32.md)
</dt> </dl>

 

 




