---
title: asuint-Funktion
description: Interpretiert das Bitmuster eines 64-Bit-Werts als zwei 32-Bit-Ganzzahlen ohne Vorzeichen neu.
ms.assetid: 29671661-4fec-46e5-9b6f-56fba8e1d756
keywords:
- asuint-Funktion HLSL
topic_type:
- apiref
api_name:
- asuint
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 02f0df4d31ca978b8b58b50cd0c91710056aa9ac0f3cac1ae370a4edba6a9edf
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119626590"
---
# <a name="asuint-function"></a>asuint-Funktion

Interpretiert das Bitmuster eines 64-Bit-Werts als zwei 32-Bit-Ganzzahlen ohne Vorzeichen neu.

## <a name="syntax"></a>Syntax

``` syntax
void asuint(
  in  double value,
  out uint lowbits,
  out uint highbits
);
```

## <a name="parameters"></a>Parameter

<dl> <dt>

*value* \[ In\]
</dt> <dd>

Typ: **double**

Der Eingabewert.

</dd> <dt>

*lowbits* \[ out\]
</dt> <dd>

Typ: **uint**

Das niedrige 32-Bit-Muster des *Werts*.

</dd> <dt>

*Highbits* \[ out\]
</dt> <dd>

Typ: **uint**

Das hohe 32-Bit-Muster des *Werts*.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Diese Funktion gibt keinen Wert zurück.

## <a name="remarks"></a>Hinweise

Diese Funktion ist eine alternative Version der [**systeminternen Asuint-Funktion,**](dx-graphics-hlsl-asuint.md) die in früheren Shadermodellen verfügbar war und für ShaderModell 5 eingeführt wurde. Die ursprüngliche Funktion (im HLSL-Compiler durch ihre unterschiedliche Signatur erkannt) bleibt für Shader Model 5 verfügbar.

### <a name="minimum-shader-model"></a>Minimales Shadermodell

Diese Funktion wird in den folgenden Shadermodellen unterstützt.



| Shadermodell                                                                | Unterstützt |
|-----------------------------------------------------------------------------|-----------|
| [Shadermodell 5](d3d11-graphics-reference-sm5.md) und höher– Shadermodelle | Ja       |



 

Diese Funktion wird in den folgenden Shadertypen unterstützt:



| Scheitelpunkt | Rumpf | Domain | Geometrie | Pixel | Compute |
|--------|------|--------|----------|-------|---------|
| x      | x    | x      | x        | x     | x       |



 

## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[Systeminterne Funktionen](dx-graphics-hlsl-intrinsic-functions.md)
</dt> <dt>

[**asuint (DirectX HLSL)**](dx-graphics-hlsl-asuint.md)
</dt> <dt>

[Shadermodell 5](d3d11-graphics-reference-sm5.md)
</dt> </dl>

 

 




