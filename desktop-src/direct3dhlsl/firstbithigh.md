---
title: firstbithigh-Funktion
description: Ruft die Position des ersten festgelegten Bits ab dem bit mit der höchsten Reihenfolge ab und arbeitet nach unten pro Komponente.
ms.assetid: 0fa89a9e-1706-44f7-8dd3-c37af5c11ddc
keywords:
- firstbithigh-Funktion HLSL
topic_type:
- apiref
api_name:
- firstbithigh
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 1c62b6f090126887930415fc408da4f4a6c17bc4a99429db61fd298960c07e6b
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119949700"
---
# <a name="firstbithigh-function"></a>firstbithigh-Funktion

Ruft die Position des ersten festgelegten Bits ab dem bit mit der höchsten Reihenfolge ab und arbeitet nach unten pro Komponente.

## <a name="syntax"></a>Syntax

``` syntax
int firstbithigh(
  in int value
);
```

## <a name="parameters"></a>Parameter

<dl> <dt>

*wert* \[ In\]
</dt> <dd>

Typ: **[ **int**](/windows/desktop/WinProg/windows-data-types)**

Der Eingabewert.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Typ: **[ **int**](/windows/desktop/WinProg/windows-data-types)**

Die Position des ersten festgelegten Bits.

## <a name="remarks"></a>Hinweise

Für eine ganze Zahl mit Vorzeichen ist das erste signifikante Bit 0 (null) für eine negative Zahl.

Die folgenden überladenen Versionen sind ebenfalls verfügbar:

``` syntax
int2 firstbithigh(int2 value);
int3 firstbithigh(int3 value);
int4 firstbithigh(int4 value);
uint firstbithigh(uint value);
uint2 firstbithigh(uint2 value);
uint3 firstbithigh(uint3 value);
uint4 firstbithigh(uint4 value);
```

### <a name="minimum-shader-model"></a>Shader-Mindestmodell

Diese Funktion wird in den folgenden Shadermodellen unterstützt.



| Shadermodell                                                                | Unterstützt |
|-----------------------------------------------------------------------------|-----------|
| [Shadermodell 5](d3d11-graphics-reference-sm5.md) und höhere Shadermodelle | Ja       |



 

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

 

 