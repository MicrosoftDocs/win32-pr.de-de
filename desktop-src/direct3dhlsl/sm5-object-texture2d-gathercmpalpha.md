---
title: Texture2D::GatherCmpAlpha(S,float,float,int)-Funktion
description: Gibt für vier Texelwerte, die in einem bilinearen Filtervorgang verwendet werden, einen Vergleich ihrer Alphakomponente mit einem Vergleichswert zurück. | Texture2D::GatherCmpAlpha(S,float,float,int)-Funktion
ms.assetid: 6fa60604-1eac-405d-bffa-3055569b7a09
keywords:
- GatherCmpAlpha-Funktion HLSL
topic_type:
- apiref
api_name:
- GatherCmpAlpha
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: f6e350ed14482646562121d910a8bd35f30403acf8dbde7df249ee1bc6ca800a
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118789603"
---
# <a name="texture2dgathercmpalphasfloatfloatint-function"></a>Texture2D::GatherCmpAlpha(S,float,float,int)-Funktion

Gibt für vier Texelwerte, die in einem bilinearen Filtervorgang verwendet werden, einen Vergleich ihrer Alphakomponente mit einem Vergleichswert zurück.

## <a name="syntax"></a>Syntax

``` syntax
float4 GatherCmpAlpha(
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

*Standort* \[ In\]
</dt> <dd>

Typ: **float2**

Die Beispielkoordinaten (u,v).

</dd> <dt>

*\_ Vergleichswert* \[ in\]
</dt> <dd>

Typ: **float**

Ein -Wert, der mit jedem Stichprobenwert verglichen werden soll.

</dd> <dt>

*Offset* \[ In\]
</dt> <dd>

Typ: **int2**

Ein Offset, der vor der Stichprobenentnahme auf die Texturkoordinate angewendet wird.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Typ: **float4**

Ein Wert mit vier Komponenten, jede Komponente ist das Ergebnis eines Komponentenvergleichs.

## <a name="remarks"></a>Hinweise

Die Texturbeispiele können für die bilineare Interpolation verwendet werden.

Diese Funktion wird für die folgenden Shadertypen unterstützt:



| Scheitelpunkt | Rumpf | Domain | Geometrie | Pixel | Compute |
|--------|------|--------|----------|-------|---------|
| x      | x    | x      | x        | x     | x       |



 

## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[GatherCmpAlpha-Methoden](texture2d-gathercmpalpha.md)
</dt> <dt>

[Shadermodell 5](d3d11-graphics-reference-sm5.md)
</dt> </dl>

 

 




