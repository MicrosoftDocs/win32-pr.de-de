---
description: Die llmuldiv-Funktion implementiert die Formel ((a \* b) + Rnd)/c wobei jeder Begriff ein 64-Bit-Wert ist.
ms.assetid: cd5073b9-27c7-42ee-8487-2d4ea29f77d4
title: llmuldiv-Funktion (wxutil. h)
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
ms.openlocfilehash: e45d22eec1536517bd2b57d875dd596e4a1e28db
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106354141"
---
# <a name="llmuldiv-function"></a>llmuldiv-Funktion

Die `llMulDiv` -Funktion implementiert die Formel, `((a*b)+rnd)/c` bei der jeder Begriff ein 64-Bit-Wert ist.

Zeitstempel und Suchzeiten sind 64-Bit-Werte, sodass diese Funktion zum Ausführen von Konvertierungen auf 32-Bit-Systemen nützlich ist. Die Formel für Bytes pro Sekunde lautet z. b..


```C++
(Number of Bytes * Reference Time) / 10,000,000
```



, die als berechnet werden können `llMulDiv(nBytes, rtTime, 10000000, 0)` . Verwenden Sie den *Rnd* -Parameter als Rundungs Faktor.

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

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>Wxutil. h (Include Streams. h)</dt> </dl>                                                                                    |
| Bibliothek<br/> | <dl> " <dt>Straumbase. lib" (Einzelhandels Builds);</dt> " <dt>Straumbasd. lib" (Debugbuilds)</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[Diverse Hilfsfunktionen](miscellaneous-helper-functions.md)
</dt> <dt>

[**Int64x32Div32**](int64x32div32.md)
</dt> </dl>

 

 




