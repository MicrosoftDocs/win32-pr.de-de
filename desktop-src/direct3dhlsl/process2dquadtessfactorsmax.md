---
title: Process2DQuadTessFactorsMax-Funktion
description: Generiert die korrigierten Mosaikfaktoren für einen Quad patch. | Process2DQuadTessFactorsMax-Funktion
ms.assetid: 1de95946-d82d-42ba-93d7-ab8383fd5018
keywords:
- Process2DQuadTessFactorsMax-Funktion HLSL
topic_type:
- apiref
api_name:
- Process2DQuadTessFactorsMax
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: f3325f08d1457230f52a539eaa9a7694d56266b7f2fd8cfd921c7a70e61ab568
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118510945"
---
# <a name="process2dquadtessfactorsmax-function"></a>Process2DQuadTessFactorsMax-Funktion

Generiert die korrigierten Mosaikfaktoren für einen Quad patch.

## <a name="syntax"></a>Syntax

``` syntax
void Process2DQuadTessFactorsMax(
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

Generiert die korrigierten Mosaikfaktoren für einen Quad-Patch und setzt die Mosaikfaktoren innerhalb des Mosaiks als Maximales der Mosaikfaktoren der Kante ab. Die Mosaikfaktoren "you" und "V" werden unabhängig voneinander mithilfe der Höchstwerte der gegensätzlichen Seiten der Domäne berechnet und dann von InsideScale skaliert. Das Ergebnis wird dann basierend auf dem Partitionierungsmodus gerundet, aber die ungerundeten Ergebnisse sind mithilfe des UnroundedInsideTessFactors-Parameters verfügbar.

### <a name="minimum-shader-model"></a>Minimales Shadermodell

Diese Funktion wird in den folgenden Shadermodellen unterstützt.



| Shadermodell                                                                | Unterstützt |
|-----------------------------------------------------------------------------|-----------|
| [Shadermodell 5](d3d11-graphics-reference-sm5.md) und höher– Shadermodelle | ja       |



 

Diese Funktion wird in den folgenden Shadertypen unterstützt:



| Scheitelpunkt | Rumpf | Domain | Geometrie | Pixel | Compute |
|--------|------|--------|----------|-------|---------|
|        | x    |        |          |       |         |



 

## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[Systeminterne Funktionen](dx-graphics-hlsl-intrinsic-functions.md)
</dt> <dt>

[Shadermodell 5](d3d11-graphics-reference-sm5.md)
</dt> </dl>

 

 




