---
title: Texture2DArray::GatherCmp(S,float,float,int)-Funktion
description: Für vier Texelwerte, die in einem bilinealen Filtervorgang verwendet werden, gibt ihren Vergleich mit einem Vergleichswert zurück. | Texture2DArray::GatherCmp(S,float,float,int)-Funktion
ms.assetid: 7bb86448-cc73-4423-9ef4-149427cffc95
keywords:
- GatherCmp-Funktion HLSL
topic_type:
- apiref
api_name:
- GatherCmp
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 2753ac82ab653634a1c211f1eedde6b2867ade42f645d2f63d3cab41776ebb31
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "117724638"
---
# <a name="texture2darraygathercmpsfloatfloatint-function"></a>Texture2DArray::GatherCmp(S,float,float,int)-Funktion

Für vier Texelwerte, die in einem bilinealen Filtervorgang verwendet werden, gibt ihren Vergleich mit einem Vergleichswert zurück.

## <a name="syntax"></a>Syntax

``` syntax
float4 GatherCmp(
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

*location* \[ In\]
</dt> <dd>

Typ: **float3**

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

[GatherCmp-Methoden](texture2darray-gathercmp.md)
</dt> <dt>

[Shadermodell 5](d3d11-graphics-reference-sm5.md)
</dt> </dl>

 

 




