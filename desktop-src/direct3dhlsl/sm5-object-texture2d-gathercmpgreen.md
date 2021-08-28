---
title: Texture2D::GatherCmpGreen(S,float,float,int)-Funktion
description: Für vier Texelwerte, die in einem bilinealen Filtervorgang verwendet werden, gibt einen Vergleich ihrer grünen Komponente mit einem Vergleichswert zurück. | Texture2D::GatherCmpGreen(S,float,float,int)-Funktion
ms.assetid: 5a11ce0c-56b2-460a-95d7-15688dd158ff
keywords:
- GatherCmpGreen-Funktion HLSL
topic_type:
- apiref
api_name:
- GatherCmpGreen
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 44ebf3590a756ea0bb78e6cc9c636523cb584cdd862059418f7b7c9508bfecfa
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "120095120"
---
# <a name="texture2dgathercmpgreensfloatfloatint-function"></a>Texture2D::GatherCmpGreen(S,float,float,int)-Funktion

Für vier Texelwerte, die in einem bilinealen Filtervorgang verwendet werden, gibt einen Vergleich ihrer grünen Komponente mit einem Vergleichswert zurück.

## <a name="syntax"></a>Syntax

``` syntax
float4 GatherCmpGreen(
  in SamplerComparisonState s,
  in float2 location,
  in float compare_value,
  in int2 offset
);
```

## <a name="parameters"></a>Parameter

<dl> <dt>

*s* \[ in\]
</dt> <dd>

Typ: **SamplerComparisonState**

Der nullbasierte Samplerindex.

</dd> <dt>

*location* \[ In\]
</dt> <dd>

Typ: **float2**

Die Beispielkoordinaten (u,v).

</dd> <dt>

*Vergleichen \_ des Werts* \[ in\]
</dt> <dd>

Typ: **float**

Ein -Wert, der jeweils mit jedem stichprobenentnahmen Wert verglichen werden soll.

</dd> <dt>

*offset* \[ In\]
</dt> <dd>

Typ: **int2**

Ein Offset, der vor der Stichprobenentnahme auf die Texturkoordinate angewendet wird.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Typ: **float4**

Ein Wert mit vier Komponenten, bei dem jede Komponente das Ergebnis eines Komponentenvergleichs ist.

## <a name="remarks"></a>Hinweise

Die Texturbeispiele können für die bilineare Interpolation verwendet werden.

Diese Funktion wird für die folgenden Shadertypen unterstützt:



| Scheitelpunkt | Rumpf | Domain | Geometrie | Pixel | Compute |
|--------|------|--------|----------|-------|---------|
| x      | x    | x      | x        | x     | x       |



 

## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[GatherCmpGreen-Methoden](texture2d-gathercmpgreen.md)
</dt> <dt>

[Shadermodell 5](d3d11-graphics-reference-sm5.md)
</dt> </dl>

 

 




