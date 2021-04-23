---
title: countbits-Funktion
description: Zählt die Anzahl der Bits (pro Komponente), die in der Eingabe-Ganzzahl festgelegt sind.
ms.assetid: c4fafbc8-e21c-48cb-b433-8241a989ec85
keywords:
- countbits-Funktion HLSL
topic_type:
- apiref
api_name:
- countbits
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 357aceca6e2aea261a9e94212b58ff6308c99560
ms.sourcegitcommit: 435ea8f5bf06808ffa7dce39afb0ee6de842ba2f
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2021
ms.locfileid: "107925623"
---
# <a name="countbits-function"></a>countbits-Funktion

Zählt die Anzahl der Bits (pro Komponente), die in der Eingabe-Ganzzahl festgelegt sind.

## <a name="syntax"></a>Syntax

``` syntax
uint countbits(
  in uint value
);
```

## <a name="parameters"></a>Parameter

<dl> <dt>

*value* \[ In\]
</dt> <dd>

Typ: **uint**

Der Eingabewert.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Typ: **uint**

Die Anzahl der Bits.

## <a name="remarks"></a>Bemerkungen

Die folgenden überladenen Versionen sind ebenfalls verfügbar:

``` syntax
uint count_bits(uint value);
uint2 count_bits(uint2 value);
uint3 count_bits(uint3 value);
uint4 count_bits(uint4 value);
```

### <a name="minimum-shader-model"></a>Minimales Shadermodell

Diese Funktion wird in den folgenden Shadermodellen unterstützt.



| Shadermodell                                                                | Unterstützt |
|-----------------------------------------------------------------------------|-----------|
| [Shadermodell 5](d3d11-graphics-reference-sm5.md) und höher– Shadermodelle | ja       |



 

Diese Funktion wird in den folgenden Shadertypen unterstützt:



| Scheitelpunkt | Rumpf | Domain | Geometrie | Pixel | Compute |
|--------|------|--------|----------|-------|---------|
| x      | x    | x      | x        | x     | x       |



 

## <a name="see-also"></a>Siehe auch

<dl> <dt>

[Systeminterne Funktionen](dx-graphics-hlsl-intrinsic-functions.md)
</dt> <dt>

[Shadermodell 5](d3d11-graphics-reference-sm5.md)
</dt> </dl>

 

 




