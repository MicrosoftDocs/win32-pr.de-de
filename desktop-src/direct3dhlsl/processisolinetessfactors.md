---
title: ProcessIsolineTessFactors-Funktion
description: Generiert die gerundeten Mosaikfaktoren für eine Isolinie.
ms.assetid: 0816b3e0-cb03-4a7a-9732-e84c637b3d48
keywords:
- ProcessIsolineTessFactors-Funktion HLSL
topic_type:
- apiref
api_name:
- ProcessIsolineTessFactors
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 34c6f4d579ee7fbaee9416d7a607e3856a7793021cca7149723d3d6e5a2b4a49
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118986290"
---
# <a name="processisolinetessfactors-function"></a>ProcessIsolineTessFactors-Funktion

Generiert die gerundeten Mosaikfaktoren für eine Isolinie.

## <a name="syntax"></a>Syntax

``` syntax
void ProcessIsolineTessFactors(
  in  float RawDetailFactor,
  in  float RawDensityFactor,
  out float RoundedDetailFactor,
  out float RoundedDensityFactor
);
```

## <a name="parameters"></a>Parameter

<dl> <dt>

*RawDetailFactor* \[ In\]
</dt> <dd>

Typ: **float**

Der gewünschte Detailfaktor.

</dd> <dt>

*RawDensityFactor* \[ In\]
</dt> <dd>

Typ: **float**

Der gewünschte Dichtefaktor.

</dd> <dt>

*RoundedDetailFactor* \[ out\]
</dt> <dd>

Typ: **float**

Der gerundete Detailfaktor, der an einen Bereich gebunden ist, der vom Mosaikator verwendet werden kann.

</dd> <dt>

*RoundedDensityFactor* \[ out\]
</dt> <dd>

Typ: **float**

Der gerundete Dichtefaktor, der an einen Bereich gebunden ist, kann vom Mosaikator verwendet werden.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Diese Funktion gibt keinen Wert zurück.

## <a name="remarks"></a>Hinweise

### <a name="minimum-shader-model"></a>Shader-Mindestmodell

Diese Funktion wird in den folgenden Shadermodellen unterstützt.



| Shadermodell                                                                | Unterstützt |
|-----------------------------------------------------------------------------|-----------|
| [Shadermodell 5](d3d11-graphics-reference-sm5.md) und höhere Shadermodelle | Ja       |



 

Diese Funktion wird in den folgenden Shadertypen unterstützt:



| Scheitelpunkt | Rumpf | Domain | Geometrie | Pixel | Compute |
|--------|------|--------|----------|-------|---------|
|        | x    |        |          |       |         |



 

## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[Systeminterne Funktionen](dx-graphics-hlsl-intrinsic-functions.md)
</dt> <dt>

[Shadermodell 5](d3d11-graphics-reference-sm5.md)
</dt> </dl>

 

 




