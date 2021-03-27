---
title: 'Texture2D:: gathercmpalpha (S, float, float, int)-Funktion'
description: 'Für vier textexwerte, die in einem bilinearen Filter Vorgang verwendet werden, wird ein Vergleich der Alpha Komponente mit einem Vergleichswert zurückgegeben. | Texture2D:: gathercmpalpha (S, float, float, int)-Funktion'
ms.assetid: 6fa60604-1eac-405d-bffa-3055569b7a09
keywords:
- Gathercmpalpha-Funktion HLSL
topic_type:
- apiref
api_name:
- GatherCmpAlpha
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 3a7f7fcdc6e24cac5c04068fda7f781d0bdd376a
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/09/2021
ms.locfileid: "104393910"
---
# <a name="texture2dgathercmpalphasfloatfloatint-function"></a>Texture2D:: gathercmpalpha (S, float, float, int)-Funktion

Für vier textexwerte, die in einem bilinearen Filter Vorgang verwendet werden, wird ein Vergleich der Alpha Komponente mit einem Vergleichswert zurückgegeben.

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

Typ: **samplercomparisonstate**

Der null basierte samplerindex.

</dd> <dt>

*Speicherort* \[ in\]
</dt> <dd>

Typ: **float2**

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

[Gathercmpalpha-Methoden](texture2d-gathercmpalpha.md)
</dt> <dt>

[Shader-Modell 5](d3d11-graphics-reference-sm5.md)
</dt> </dl>

 

 




