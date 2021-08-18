---
title: Texture2D::GatherCmp(S,float,float,int)-Funktion
description: Für vier Texelwerte, die in einem bilinealen Filtervorgang verwendet werden, gibt ihren Vergleich mit einem Vergleichswert zurück. | Texture2D::GatherCmp(S,float,float,int)-Funktion
ms.assetid: 1084bcb3-2834-400a-98ff-4e3182f63f20
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
ms.openlocfilehash: ce62ebefdd23b914abbe38b84fe2e04db2200abdfb31a778e7cf8799eb8677b2
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119788330"
---
# <a name="texture2dgathercmpsfloatfloatint-function"></a>Texture2D::GatherCmp(S,float,float,int)-Funktion

Für vier Texelwerte, die in einem bilinealen Filtervorgang verwendet werden, gibt ihren Vergleich mit einem Vergleichswert zurück.

## <a name="syntax"></a>Syntax

``` syntax
float4 GatherCmp(
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

[GatherCmp-Methoden](texture2d-gathercmp.md)
</dt> <dt>

[Shadermodell 5](d3d11-graphics-reference-sm5.md)
</dt> </dl>

 

 




