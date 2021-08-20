---
description: Die Int64x32Div32-Funktion implementiert die Formel ((a \* b)+rnd)/c, wobei ein ein 64-Bit-Wert und b, c und rnd 32-Bit-Werte sind.
ms.assetid: 566ac194-5b15-43b7-aa7c-0c18c6f69691
title: Int64x32Div32-Funktion (Wxutil.h)
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
ms.openlocfilehash: a56425d1f07346f8e546940ff5880416e4e63efc692974c78f0e344b9ec01c5b
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "120051590"
---
# <a name="int64x32div32-function"></a>Int64x32Div32-Funktion

Die Funktion implementiert die Formel, wobei `Int64x32Div32` `((a*b)+rnd)/c` *ein* ein 64-Bit-Wert und *b,* *c* und *rnd* 32-Bit-Werte sind.

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

Zeitstempel und Suchzeiten sind 64-Bit-Werte, daher ist diese Funktion nützlich für Konvertierungen auf 32-Bit-Systemen. In MPEG-1 beträgt der Systemuhrverweis beispielsweise 90 kHz oder 90.000 Takte pro Sekunde. Die Formel zum Konvertieren dieser In bezugszeit (Einheiten von 100 Nanosekunden) ist


```C++
(timestamp * 1000) / 9
```



kann als berechnet `Int64x32Div32(timestamp, 1000, 9, 0)` werden. Verwenden Sie *den rnd-Parameter* als Rundungsfaktor.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>Wxutil.h (include Streams.h)</dt> </dl>                                                                                    |
| Bibliothek<br/> | <dl> <dt>Strmbase.lib (Einzelhandels-Builds); </dt> <dt>Strmbasd.lib (Debugbuilds)</dt> </dl> |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[Verschiedene Hilfsfunktionen](miscellaneous-helper-functions.md)
</dt> <dt>

[**llMulDiv**](llmuldiv.md)
</dt> </dl>

 

 




