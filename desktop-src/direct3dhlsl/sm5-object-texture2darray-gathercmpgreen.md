---
title: Texture2DArray::GatherCmpGreen(S,float,float,int)-Funktion
description: Für vier Texelwerte, die in einem bilinearen Filtervorgang verwendet werden, gibt einen Vergleich ihrer grünen Komponente mit einem Vergleichswert zurück. | Texture2DArray::GatherCmpGreen(S,float,float,int)-Funktion
ms.assetid: baf14de9-5237-42a5-bffc-848e55cbc28f
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
ms.openlocfilehash: 50251f83a0aae7e066ae1e586aa31eb74a002ad20c2843e2a0e22168ccf8e8c5
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "120067580"
---
# <a name="texture2darraygathercmpgreensfloatfloatint-function"></a>Texture2DArray::GatherCmpGreen(S,float,float,int)-Funktion

Für vier Texelwerte, die in einem bilinearen Filtervorgang verwendet werden, gibt einen Vergleich ihrer grünen Komponente mit einem Vergleichswert zurück.

## <a name="syntax"></a>Syntax

``` syntax
float4 GatherCmpGreen(
  in SamplerComparisonState s,
  in float3 location,
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

Typ: **float3**

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



 

## <a name="see-also"></a>Siehe auch

<dl> <dt>

[GatherCmpGreen-Methoden](texture2darray-gathercmpgreen.md)
</dt> <dt>

[Shadermodell 5](d3d11-graphics-reference-sm5.md)
</dt> </dl>

 

 




