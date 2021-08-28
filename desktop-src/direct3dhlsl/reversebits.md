---
title: reversebits-Funktion
description: Kehrt die Reihenfolge der Bits pro Komponente um.
ms.assetid: dad46e25-9980-4645-98eb-d834db704fc8
keywords:
- reversebits-Funktion HLSL
topic_type:
- apiref
api_name:
- reversebits
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: b9f055764c04f552fe9d7afda2adf1e401352cf3fc3dd3ead16c4ca6377bd4fe
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119853720"
---
# <a name="reversebits-function"></a>reversebits-Funktion

Kehrt die Reihenfolge der Bits pro Komponente um.

## <a name="syntax"></a>Syntax

``` syntax
uint reversebits(
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

Der Eingabewert mit umgekehrter Bit reihenfolge.

## <a name="remarks"></a>Hinweise

Die folgenden überladenen Versionen sind ebenfalls verfügbar:

``` syntax
uint2 reversebits(uint2 value);
uint3 reversebits(uint3 value);
uint4 reversebits(uint4 value);
```

### <a name="minimum-shader-model"></a>Minimales Shadermodell

Diese Funktion wird in den folgenden Shadermodellen unterstützt.



| Shadermodell                                                                | Unterstützt |
|-----------------------------------------------------------------------------|-----------|
| [Shadermodell 5](d3d11-graphics-reference-sm5.md) und höher– Shadermodelle | Ja       |



 

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

 

 




