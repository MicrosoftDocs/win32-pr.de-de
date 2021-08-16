---
title: asdouble-Funktion
description: Interpretiert einen Umwandlungswert (zwei 32-Bit-Werte) in einen Double neu.
ms.assetid: 55e5276d-81e1-4e7e-8cb4-0beb57d2fb7f
keywords:
- asdouble-Funktion HLSL
topic_type:
- apiref
api_name:
- asdouble
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 0e191a2bf9ee7fb46337c3c7dfef7f8dea3525acf936ab745c07e7720f1ac509
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119626640"
---
# <a name="asdouble-function"></a>asdouble-Funktion

Interpretiert einen Umwandlungswert (zwei 32-Bit-Werte) in einen Double neu.

## <a name="syntax"></a>Syntax

``` syntax
double asdouble(
  in uint lowbits,
  in uint highbits
);
```

## <a name="parameters"></a>Parameter

<dl> <dt>

*lowbits* \[ In\]
</dt> <dd>

Typ: **uint**

Das niedrige 32-Bit-Muster des Eingabewerts.

</dd> <dt>

*Highbits* \[ In\]
</dt> <dd>

Typ: **uint**

Das hohe 32-Bit-Muster des Eingabewerts.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Typ: **double**

Die Eingabe (zwei 32-Bit-Werte) wird als Double-Wert umformiert.

## <a name="remarks"></a>Hinweise

Die folgende überladene Version ist ebenfalls verfügbar:

``` syntax
double2 asdouble(uint2 lowbits, uint2 highbits);
```

Wenn der Eingabewert zwei 32-Bit-Komponenten ist, enthält der Rückgabetyp ein Double. Wenn der Eingabewert vier 32-Bit-Komponenten ist, enthält der Rückgabetyp zwei Doubles. Wenn der Eingabewert ein 64-Bit-Typ ist, hat der zurückgegebene Wert die gleiche Anzahl von Komponenten wie der Eingabewert.

### <a name="minimum-shader-model"></a>Shader-Mindestmodell

Diese Funktion wird in den folgenden Shadermodellen unterstützt.



| Shadermodell                                                                | Unterstützt |
|-----------------------------------------------------------------------------|-----------|
| [Shadermodell 5](d3d11-graphics-reference-sm5.md) und höhere Shadermodelle | ja       |



 

Diese Funktion wird in den folgenden Shadertypen unterstützt:



| Scheitelpunkt | Rumpf | Domain | Geometrie | Pixel | Compute |
|--------|------|--------|----------|-------|---------|
| x      | x    | x      | x        | x     | x       |



 

## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[Systeminterne Funktionen](dx-graphics-hlsl-intrinsic-functions.md)
</dt> <dt>

[Shadermodell 5](d3d11-graphics-reference-sm5.md)
</dt> </dl>

 

 




