---
title: countbits-Funktion
description: Zählt die Anzahl der Bits (pro Komponente) in der Eingabe Ganzzahl.
ms.assetid: c4fafbc8-e21c-48cb-b433-8241a989ec85
keywords:
- count-Bits-Funktion HLSL
topic_type:
- apiref
api_name:
- countbits
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 60d3cd63502c6217e6fb0b0ff17685b2d2b5bf25
ms.sourcegitcommit: 57758ecb246c84d65e6e0e4bd5570d9176fa39cd
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/25/2019
ms.locfileid: "104038124"
---
# <a name="countbits-function"></a>countbits-Funktion

Zählt die Anzahl der Bits (pro Komponente) in der Eingabe Ganzzahl.

## <a name="syntax"></a>Syntax

``` syntax
uint countbits(
  in uint value
);
```

## <a name="parameters"></a>Parameter

<dl> <dt>

*Wert* \[ in\]
</dt> <dd>

Typ: **uint**

Der Eingabewert.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Typ: **uint**

Die Anzahl der Bits.

## <a name="remarks"></a>Bemerkungen

Außerdem sind die folgenden überladenen Versionen verfügbar:

``` syntax
uint count_bits(uint value);
uint2 count_bits(uint2 value);
uint3 count_bits(uint3 value);
uint4 count_bits(uint4 value);
```

### <a name="minimum-shader-model"></a>Minimaler Shader-Modell

Diese Funktion wird in den folgenden shadermodellen unterstützt.



| Shadermodell                                                                | Unterstützt |
|-----------------------------------------------------------------------------|-----------|
| [Shader Model 5](d3d11-graphics-reference-sm5.md) und höhere shadermodelle | ja       |



 

Diese Funktion wird in den folgenden Typen von Shadern unterstützt:



| Scheitelpunkt | Hülle | Domain | Geometrie | Pixel | Compute |
|--------|------|--------|----------|-------|---------|
| x      | x    | x      | x        | x     | x       |



 

## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[Intrinsische Funktionen](dx-graphics-hlsl-intrinsic-functions.md)
</dt> <dt>

[Shader-Modell 5](d3d11-graphics-reference-sm5.md)
</dt> </dl>

 

 




