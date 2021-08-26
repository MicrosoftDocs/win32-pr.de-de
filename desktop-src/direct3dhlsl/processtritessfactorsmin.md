---
title: ProcessTriTessFactorsMin-Funktion
description: Generiert die korrigierten Mosaikfaktoren für einen tri-Patch. | ProcessTriTessFactorsMin-Funktion
ms.assetid: fa1e19c2-fadf-42d4-9574-834eaf871393
keywords:
- ProcessTriTessFactorsMin-Funktion HLSL
topic_type:
- apiref
api_name:
- ProcessTriTessFactorsMin
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 09cb10f8adac68511a5b4bb5b469ab3e4f630aab0b9a58b539100914f0668114
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "120023740"
---
# <a name="processtritessfactorsmin-function"></a>ProcessTriTessFactorsMin-Funktion

Generiert die korrigierten Mosaikfaktoren für einen tri-Patch.

## <a name="syntax"></a>Syntax

``` syntax
void ProcessTriTessFactorsMin(
  in  float3 RawEdgeFactors,
  in  float InsideScale,
  out float3 RoundedEdgeTessFactors,
  out float RoundedInsideTessFactors,
  out float UnroundedInsideTessFactors
);
```

## <a name="parameters"></a>Parameter

<dl> <dt>

*RawEdgeFactors* \[ In\]
</dt> <dd>

Typ: **float3**

Die Mosaikfaktoren der Kante, die an die Mosaikphase übergeben werden.

</dd> <dt>

*InsideScale* \[ In\]
</dt> <dd>

Typ: **float**

Der Skalierungsfaktor, der auf die UV-Mosaikfaktoren angewendet wird, die von der Mosaikphase berechnet werden. Der zulässige Bereich für InsideScale liegt zwischen 0,0 und 1,0.

</dd> <dt>

*RoundedEdgeTessFactors* \[ out\]
</dt> <dd>

Typ: **float3**

Die gerundeten Edge-Mosaikfaktoren, die von der Mosaikphase berechnet werden.

</dd> <dt>

*RoundedInsideTessFactors* \[ out\]
</dt> <dd>

Typ: **float**

Die gerundeten Mosaikfaktoren, die von der Mosaikstufe für innerhalb von Kanten berechnet werden.

</dd> <dt>

*UnroundedInsideTessFactors* \[ out\]
</dt> <dd>

Typ: **float**

Die Mosaikfaktoren, die von der Mosaikphase für innerhalb von Kanten berechnet werden.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Diese Funktion gibt keinen Wert zurück.

## <a name="remarks"></a>Hinweise

Generiert die korrigierten Mosaikfaktoren für einen Tripatch und setzt den Mosaikfaktor innerhalb des Rahmens als Mindestwert der Mosaikfaktoren des Edges, die dann von InsideScale skaliert werden. Das Ergebnis wird dann basierend auf dem Partitionierungsmodus gerundet, aber die ungerundeten Ergebnisse sind mithilfe des UnroundedInsideTessFactor-Parameters verfügbar.

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

 

 




