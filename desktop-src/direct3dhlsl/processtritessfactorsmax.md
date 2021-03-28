---
title: Processtritess factorsmax-Funktion
description: Generiert die korrigierten Mosaik Faktoren für einen Tri-Patch. | Processtritess factorsmax-Funktion
ms.assetid: a24cc1a8-5e6e-4963-b36b-e2265475580e
keywords:
- Processtritesfactorsmax-Funktion HLSL
topic_type:
- apiref
api_name:
- ProcessTriTessFactorsMax
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: b5c17fe1dd9f3457a4104178e61af3589ba9f72d
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/09/2021
ms.locfileid: "104530653"
---
# <a name="processtritessfactorsmax-function"></a>Processtritess factorsmax-Funktion

Generiert die korrigierten Mosaik Faktoren für einen Tri-Patch.

## <a name="syntax"></a>Syntax

``` syntax
void ProcessTriTessFactorsMax(
  in  float3 RawEdgeFactors,
  in  float InsideScale,
  out float3 RoundedEdgeTessFactors,
  out float RoundedInsideTessFactor,
  out float UnroundedInsideTessFactor
);
```

## <a name="parameters"></a>Parameter

<dl> <dt>

*Rawedgefactors* \[ in\]
</dt> <dd>

Typ: **float3**

Die Edge-Mosaik Faktoren, die an die Mosaik Phase übergebenen werden.

</dd> <dt>

*Insidescale* \[ in\]
</dt> <dd>

Typ: **float**

Der Skalierungsfaktor, der auf die von der Mosaik Phase berechneten UV-Mosaik Faktoren angewendet wird. Der zulässige Bereich für insidescale liegt zwischen 0,0 und 1,0.

</dd> <dt>

*Roundebug Factors* \[ vorgenommen\]
</dt> <dd>

Typ: **float3**

Die gerundeten Edge-Mosaik Faktoren, die von der Mosaik Phase berechnet werden.

</dd> <dt>

*Rounabdinsidetess Factor* \[ vorgenommen\]
</dt> <dd>

Typ: **float**

Die Mosaik Faktoren, die von der Mosaik Stufe berechnet werden, und gerundet.

</dd> <dt>

*Unroundecodinsidetess Factor* \[ vorgenommen\]
</dt> <dd>

Typ: **float**

Die ursprünglichen, nicht abgerundeten, von der Mosaik Phase berechneten UV-Mosaik Faktoren.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Diese Funktion gibt keinen Wert zurück.

## <a name="remarks"></a>Bemerkungen

Generiert die korrigierten Mosaik Faktoren für einen Tri-Patch, der den inneren Mosaik Faktor als Maximum der Edge-Mosaik Faktoren berechnet, die dann von insidescale skaliert werden. Das Ergebnis wird dann basierend auf dem Partitionierungs Modus abgerundet, aber die nicht gerundeten Ergebnisse sind mit dem unroundedinsidetess Factor-Parameter verfügbar.

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

 

 




