---
title: Texture2DArray::GatherCmpBlue(S,float,float,int)-Funktion
description: Für vier Texelwerte, die in einem bilinearen Filtervorgang verwendet werden, gibt einen Vergleich ihrer blauen Komponente mit einem Vergleichswert zurück. | Texture2DArray::GatherCmpBlue(S,float,float,int)-Funktion
ms.assetid: 5fa23e27-368a-4c55-b6d6-33506c932a43
keywords:
- GatherCmpBlue-Funktion HLSL
topic_type:
- apiref
api_name:
- GatherCmpBlue
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 8b8783bf9c8fcb628d6d67a2e099877d67de7c84229d8f8f8e48769386b12e6e
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118985891"
---
# <a name="texture2darraygathercmpbluesfloatfloatint-function"></a>Texture2DArray::GatherCmpBlue(S,float,float,int)-Funktion

Für vier Texelwerte, die in einem bilinearen Filtervorgang verwendet werden, gibt einen Vergleich ihrer blauen Komponente mit einem Vergleichswert zurück.

## <a name="syntax"></a>Syntax

``` syntax
float4 GatherCmpBlue(
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



 

## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[GatherCmpBlue-Methoden](texture2darray-gathercmpblue.md)
</dt> <dt>

[Shadermodell 5](d3d11-graphics-reference-sm5.md)
</dt> </dl>

 

 




