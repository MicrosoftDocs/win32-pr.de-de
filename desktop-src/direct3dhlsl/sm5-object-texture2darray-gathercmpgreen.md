---
title: 'Texture2DArray:: gathercmpgreen (S, float, float, int)-Funktion'
description: 'Für vier textexwerte, die in einem bilinearen Filterungs Vorgang verwendet werden, wird ein Vergleich der grünen Komponente mit einem Vergleichswert zurückgegeben. | Texture2DArray:: gathercmpgreen (S, float, float, int)-Funktion'
ms.assetid: baf14de9-5237-42a5-bffc-848e55cbc28f
keywords:
- Gathercmpgreen-Funktion HLSL
topic_type:
- apiref
api_name:
- GatherCmpGreen
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 4f29da331d71c1fa8a2ceff783e4daec4a886d06
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/09/2021
ms.locfileid: "104995715"
---
# <a name="texture2darraygathercmpgreensfloatfloatint-function"></a>Texture2DArray:: gathercmpgreen (S, float, float, int)-Funktion

Für vier textexwerte, die in einem bilinearen Filterungs Vorgang verwendet werden, wird ein Vergleich der grünen Komponente mit einem Vergleichswert zurückgegeben.

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

Typ: **samplercomparisonstate**

Der null basierte samplerindex.

</dd> <dt>

*Speicherort* \[ in\]
</dt> <dd>

Typ: **float3**

Die Beispiel Koordinaten (u, v).

</dd> <dt>

*\_ Wert vergleichen* \[ in\]
</dt> <dd>

Typ: **float**

Ein Wert, der jeweils mit jedem Stichproben Wert verglichen werden soll.

</dd> <dt>

*Offset* \[ in\]
</dt> <dd>

Typ: **int2**

Ein Offset, der vor der Stichprobenentnahme auf die Textur Koordinate angewendet wird.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Typ: **float4**

Ein vier komponentenwert, wobei jede Komponente das Ergebnis eines Vergleichs pro Komponente ist.

## <a name="remarks"></a>Bemerkungen

Die Textur Beispiele können für bilineare Interpolationen verwendet werden.

Diese Funktion wird für die folgenden Typen von Shadern unterstützt:



| Scheitelpunkt | Hülle | Domain | Geometrie | Pixel | Compute |
|--------|------|--------|----------|-------|---------|
| x      | x    | x      | x        | x     | x       |



 

## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[Gathercmpgreen-Methoden](texture2darray-gathercmpgreen.md)
</dt> <dt>

[Shader-Modell 5](d3d11-graphics-reference-sm5.md)
</dt> </dl>

 

 




