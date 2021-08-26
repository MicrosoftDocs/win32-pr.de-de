---
title: Process2DQuadTessFactorsMin-Funktion
description: Generiert die korrigierten Mosaikfaktoren für einen Quad patch. | Process2DQuadTessFactorsMin-Funktion
ms.assetid: 45adf78a-9386-4460-97df-59d7739a1eee
keywords:
- Process2DQuadTessFactorsMin-Funktion HLSL
topic_type:
- apiref
api_name:
- Process2DQuadTessFactorsMin
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 77f62ff1b55b9c0c36a70bd64f2b0d5ad95be747d5fd11cae33e82eb896d21d2
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "120067900"
---
# <a name="process2dquadtessfactorsmin-function"></a>Process2DQuadTessFactorsMin-Funktion

Generiert die korrigierten Mosaikfaktoren für einen Quad patch.

## <a name="syntax"></a>Syntax

``` syntax
void Process2DQuadTessFactorsMin(
  in  float4 RawEdgeFactors,
  in  float2 InsideScale,
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

Typ: **float2**

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

Generiert die korrigierten Mosaikfaktoren für einen Quad-Patch und setzt die Mosaikfaktoren innerhalb des Mosaiks als Mindestwert der Edge-Mosaikfaktoren ab. Die Mosaikfaktoren "you" und "V" werden unabhängig voneinander berechnet, indem die mindesten der gegensätzlichen Seiten der Domäne verwendet werden. Anschließend werden sie von InsideScale skaliert. Das Ergebnis wird dann basierend auf dem Partitionierungsmodus gerundet, aber die ungerundeten Ergebnisse sind mithilfe des UnroundedInsideTessFactors-Parameters verfügbar.

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

 

 




