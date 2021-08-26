---
title: ProcessQuadTessFactorsMax-Funktion
description: Generiert die korrigierten Mosaikfaktoren für einen Quad patch. | ProcessQuadTessFactorsMax-Funktion
ms.assetid: a0c91430-db25-49c9-bcc8-d2be1d0e6f6c
keywords:
- ProcessQuadTessFactorsMax-Funktion HLSL
topic_type:
- apiref
api_name:
- ProcessQuadTessFactorsMax
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 58cfa3f9e6dd69210da18d672acd2b56ad73e34be9cf2c5d8b179181e636050f
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "120067780"
---
# <a name="processquadtessfactorsmax-function"></a>ProcessQuadTessFactorsMax-Funktion

Generiert die korrigierten Mosaikfaktoren für einen Quad patch.

## <a name="syntax"></a>Syntax

``` syntax
void ProcessQuadTessFactorsMax(
  in  float4 RawEdgeFactors,
  in  float InsideScale,
  out float4 RoundedEdgeTessFactors,
  out float2 RoundedInsideTessFactors,
  out float2 UnroundedInsideTessFactors
);
```

## <a name="parameters"></a>Parameter

<dl> <dt>

*RawEdgeFactors* \[ In\]
</dt> <dd>

Typ: **float4**

Die Mosaikfaktoren der Kante, die an die Mosaikphase übergeben werden.

</dd> <dt>

*InsideScale* \[ In\]
</dt> <dd>

Typ: **float**

Der Skalierungsfaktor, der auf die UV-Mosaikfaktoren angewendet wird, die von der Mosaikphase berechnet werden. Der zulässige Bereich für InsideScale liegt zwischen 0,0 und 1,0.

</dd> <dt>

*RoundedEdgeTessFactors* \[ out\]
</dt> <dd>

Typ: **float4**

Die gerundeten Edge-Mosaikfaktoren, die von der Mosaikphase berechnet werden.

</dd> <dt>

*RoundedInsideTessFactors* \[ out\]
</dt> <dd>

Typ: **float2**

Die gerundeten Mosaikfaktoren, die von der Mosaikstufe für innerhalb von Kanten berechnet werden.

</dd> <dt>

*UnroundedInsideTessFactors* \[ out\]
</dt> <dd>

Typ: **float2**

Die Mosaikfaktoren, die von der Mosaikphase für innerhalb von Kanten berechnet werden.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Diese Funktion gibt keinen Wert zurück.

## <a name="remarks"></a>Hinweise

Generiert die korrigierten Mosaikfaktoren für einen Quad-Patch und setzt die Mosaikfaktoren innerhalb des Mosaiks als Maximales der Mosaikfaktoren der Kante ab. Die Inside-Tess-Faktoren sind identische Werte, die durch das Maximum aller vier von InsideScale skalierten Kanten bestimmt werden. Das Ergebnis wird dann basierend auf dem Partitionierungsmodus gerundet, aber die ungerundeten Ergebnisse sind mithilfe des *UnroundedInsideTessFactors-Parameters* verfügbar.

### <a name="minimum-shader-model"></a>Minimales Shadermodell

Diese Funktion wird in den folgenden Shadermodellen unterstützt.



| Shadermodell                                                                | Unterstützt |
|-----------------------------------------------------------------------------|-----------|
| [Shadermodell 5](d3d11-graphics-reference-sm5.md) und höher– Shadermodelle | Ja       |



 

Diese Funktion wird in den folgenden Shadertypen unterstützt:



| Scheitelpunkt | Rumpf | Domain | Geometrie | Pixel | Compute |
|--------|------|--------|----------|-------|---------|
|        | x    |        |          |       |         |



 

## <a name="see-also"></a>Siehe auch

<dl> <dt>

[Systeminterne Funktionen](dx-graphics-hlsl-intrinsic-functions.md)
</dt> <dt>

[Shadermodell 5](d3d11-graphics-reference-sm5.md)
</dt> </dl>

 

 




