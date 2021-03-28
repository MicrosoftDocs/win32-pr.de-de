---
title: Processquadtess factorsavg-Funktion
description: Generiert die korrigierten Mosaik Faktoren für einen Quad-Patch. | Processquadtess factorsavg-Funktion
ms.assetid: 3af1dad3-1923-45f3-9908-ca403e7f0cfe
keywords:
- Processquadtess factorsavg-Funktion HLSL
topic_type:
- apiref
api_name:
- ProcessQuadTessFactorsAvg
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 36a50dd971161f3e03514947db447774da5b6a62
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/09/2021
ms.locfileid: "104995654"
---
# <a name="processquadtessfactorsavg-function"></a>Processquadtess factorsavg-Funktion

Generiert die korrigierten Mosaik Faktoren für einen Quad-Patch.

## <a name="syntax"></a>Syntax

``` syntax
void ProcessQuadTessFactorsAvg(
  in  float4 RawEdgeFactors,
  in  float InsideScale,
  out float4 RoundedEdgeTessFactors,
  out float2 RoundedInsideTessFactors,
  out float2 UnroundedInsideTessFactors
);
```

## <a name="parameters"></a>Parameter

<dl> <dt>

*Rawedgefactors* \[ in\]
</dt> <dd>

Typ: **float4**

Die Edge-Mosaik Faktoren, die an die Mosaik Phase übergebenen werden.

</dd> <dt>

*Insidescale* \[ in\]
</dt> <dd>

Typ: **float**

Der Skalierungsfaktor, der auf die von der Mosaik Phase berechneten UV-Mosaik Faktoren angewendet wird. Der zulässige Bereich für insidescale liegt zwischen 0,0 und 1,0.

</dd> <dt>

*Roundebug Factors* \[ vorgenommen\]
</dt> <dd>

Typ: **float4**

Die gerundeten Edge-Mosaik Faktoren, die von der Mosaik Phase berechnet werden.

</dd> <dt>

*Rounabdinsidetess Factors* \[ vorgenommen\]
</dt> <dd>

Typ: **float2**

Die gerundeten Mosaik Faktoren, die von der Mosaik Phase für innere Ränder berechnet werden.

</dd> <dt>

*Unroundecodinsidetess Factors* \[ vorgenommen\]
</dt> <dd>

Typ: **float2**

Die Mosaik Faktoren, die von der Mosaik Phase für innere Ränder berechnet werden.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Diese Funktion gibt keinen Wert zurück.

## <a name="remarks"></a>Bemerkungen

Generiert die korrigierten Mosaik Faktoren für einen Quad-Patch, wobei die in Mosaik Faktoren als Durchschnitt der Edge-Mosaik Faktoren berechnet werden. Die inneren Tess-Faktoren sind identische Werte, die durch den Durchschnitt aller vier von insidescale skalierten Kanten bestimmt werden. Das Ergebnis wird dann basierend auf dem Partitionierungs Modus abgerundet, aber die nicht gerundeten Ergebnisse sind mithilfe des Parameters unroundedinsidetess Factors verfügbar.

### <a name="minimum-shader-model"></a>Minimaler Shader-Modell

Diese Funktion wird in den folgenden shadermodellen unterstützt.



| Shadermodell                                                                | Unterstützt |
|-----------------------------------------------------------------------------|-----------|
| [Shader Model 5](d3d11-graphics-reference-sm5.md) und höhere shadermodelle | ja       |



 

Diese Funktion wird in den folgenden Typen von Shadern unterstützt:



| Scheitelpunkt | Hülle | Domain | Geometrie | Pixel | Compute |
|--------|------|--------|----------|-------|---------|
|        | x    |        |          |       |         |



 

## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[Intrinsische Funktionen](dx-graphics-hlsl-intrinsic-functions.md)
</dt> <dt>

[Shader-Modell 5](d3d11-graphics-reference-sm5.md)
</dt> </dl>

 

 




