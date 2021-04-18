---
description: Die Int64x32Div32-Funktion implementiert die Formel ((a \* b) + Rnd)/c wobei a ein 64-Bit-Wert ist und b, c und Rnd 32-Bit-Werte sind.
ms.assetid: 566ac194-5b15-43b7-aa7c-0c18c6f69691
title: Int64x32Div32-Funktion (wxutil. h)
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
ms.openlocfilehash: de60ca08b262dbf97aa118bd115bd6dc58576a1d
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106361671"
---
# <a name="int64x32div32-function"></a>Int64x32Div32-Funktion

Die `Int64x32Div32` -Funktion implementiert die Formel, `((a*b)+rnd)/c` bei der *ein* 64-Bit-Wert ist und *b*, *c* und *Rnd* 32-Bit-Werte sind.

## <a name="syntax"></a>Syntax


```C++
LONGLONG WINAPI Int64x32Div32(
   LONGLONG a,
   LONG     b,
   LONG     c,
   LONG     rnd
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*ein* 
</dt> <dd>

Multiplikand.

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

Rundungs Faktor.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Gibt entweder die `(a * b + rnd)/c` Berechnung oder einen der folgenden Werte zurück.



| Rückgabecode                                                                                       | Beschreibung                                                              |
|---------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------|
| <dl> <dt>**0x7FFFFFFFFFFFFFFF**</dt> </dl> | Ein Überlauf ist aufgetreten, da das Ergebnis zu groß ist (positiv).<br/> |
| <dl> <dt>**0x8000000000000000**</dt> </dl> | Ein Überlauf ist aufgetreten, da das Ergebnis zu groß (negativ) ist.<br/> |



 

## <a name="remarks"></a>Bemerkungen

Rundung für die Division liegt in Richtung NULL. Die Division durch 0 (null) wird als Überlauf Bedingung gezählt.

Zeitstempel und Suchzeiten sind 64-Bit-Werte, sodass diese Funktion zum Ausführen von Konvertierungen auf 32-Bit-Systemen nützlich ist. In MPEG-1 beträgt die Systemuhr beispielsweise 90-kHz oder 90.000 Ticks pro Sekunde. Die Formel zum Konvertieren dieses in eine Verweis Zeit (100-Nanosecond-Einheiten) ist


```C++
(timestamp * 1000) / 9
```



, die als berechnet werden können `Int64x32Div32(timestamp, 1000, 9, 0)` . Verwenden Sie den *Rnd* -Parameter als Rundungs Faktor.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>Wxutil. h (Include Streams. h)</dt> </dl>                                                                                    |
| Bibliothek<br/> | <dl> " <dt>Straumbase. lib" (Einzelhandels Builds);</dt> " <dt>Straumbasd. lib" (Debugbuilds)</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[Diverse Hilfsfunktionen](miscellaneous-helper-functions.md)
</dt> <dt>

[**llmuldiv**](llmuldiv.md)
</dt> </dl>

 

 




