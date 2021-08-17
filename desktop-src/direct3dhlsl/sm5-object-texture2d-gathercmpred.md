---
title: Texture2D::GatherCmpRed(S,float,float,int)-Funktion
description: Für vier Texelwerte, die in einem bilinealen Filtervorgang verwendet werden, gibt einen Vergleich ihrer roten Komponente mit einem Vergleichswert zurück. | Texture2D::GatherCmpRed(S,float,float,int)-Funktion
ms.assetid: bd5fdd3b-c1b0-4cb0-aec5-9fe020420e6c
keywords:
- GatherCmpRed-Funktion HLSL
topic_type:
- apiref
api_name:
- GatherCmpRed
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 07786eb41dfd45ce911717ee17b14c4694ab1972115b92a79076aef358ab0ad6
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "120095090"
---
# <a name="texture2dgathercmpredsfloatfloatint-function"></a>Texture2D::GatherCmpRed(S,float,float,int)-Funktion

Für vier Texelwerte, die in einem bilinealen Filtervorgang verwendet werden, gibt einen Vergleich ihrer roten Komponente mit einem Vergleichswert zurück.

## <a name="syntax"></a>Syntax

``` syntax
float4 GatherCmpRed(
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

[GatherCmpRed-Methoden](texture2d-gathercmpred.md)
</dt> <dt>

[Shadermodell 5](d3d11-graphics-reference-sm5.md)
</dt> </dl>

 

 




