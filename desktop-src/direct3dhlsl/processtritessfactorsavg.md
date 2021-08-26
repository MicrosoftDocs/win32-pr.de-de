---
title: ProcessTriTessFactorsAvg-Funktion
description: Generiert die korrigierten Mosaikfaktoren für einen Tripatch. | ProcessTriTessFactorsAvg-Funktion
ms.assetid: 005a63b6-f35d-42d6-bb29-f4ebb374080e
keywords:
- ProcessTriTessFactorsAvg-Funktion HLSL
topic_type:
- apiref
api_name:
- ProcessTriTessFactorsAvg
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 2d119ee7011bbd4a03a2a2c8247b9df9e95f983e07ffd3ab3e4603a3a3eaa7de
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "120067770"
---
# <a name="processtritessfactorsavg-function"></a>ProcessTriTessFactorsAvg-Funktion

Generiert die korrigierten Mosaikfaktoren für einen Tripatch.

## <a name="syntax"></a>Syntax

``` syntax
void ProcessTriTessFactorsAvg(
  in  float3 RawEdgeFactors,
  in  float InsideScale,
  out float3 RoundedEdgeTessFactors,
  out float RoundedInsideTessFactor,
  out float UnroundedInsideTessFactor
);
```

## <a name="parameters"></a>Parameter

<dl> <dt>

*RawEdgeFactors* \[ In\]
</dt> <dd>

Typ: **float3**

Die Edge-Mosaikfaktoren, die an die Mosaikstufe übergeben werden.

</dd> <dt>

*InsideScale* \[ In\]
</dt> <dd>

Typ: **float**

Der Skalierungsfaktor, der auf die UV-Mosaikfaktoren angewendet wird, die von der Mosaikstufe berechnet werden. Der zulässige Bereich für InsideScale ist 0,0 bis 1,0.

</dd> <dt>

*RoundedEdgeTessFactors* \[ out\]
</dt> <dd>

Typ: **float3**

Die gerundeten Edge-Mosaikfaktoren, die von der Mosaikstufe berechnet werden.

</dd> <dt>

*RoundedInsideTessFactor* \[ out\]
</dt> <dd>

Typ: **float**

Die Mosaikfaktoren, die von der Mosaikstufe berechnet und gerundet werden.

</dd> <dt>

*UnroundedInsideTessFactor* \[ out\]
</dt> <dd>

Typ: **float**

Die ursprünglichen, nicht umschwenkten UV-Mosaikfaktoren, die von der Mosaikphase berechnet werden.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Diese Funktion gibt keinen Wert zurück.

## <a name="remarks"></a>Hinweise

Generiert die korrigierten Mosaikfaktoren für ein Tripatch und berechnet den Faktor für das Mosaik innerhalb des Mosaiks als Durchschnitt der Edge-Mosaikfaktoren, die dann von InsideScale skaliert werden. Das Ergebnis wird dann basierend auf dem Partitionierungsmodus gerundet, aber die nichtroundierten Ergebnisse sind mit dem Parameter UnroundedInsideTessFactor verfügbar.

### <a name="minimum-shader-model"></a>Shader-Mindestmodell

Diese Funktion wird in den folgenden Shadermodellen unterstützt.



| Shadermodell                                                                | Unterstützt |
|-----------------------------------------------------------------------------|-----------|
| [Shadermodell 5](d3d11-graphics-reference-sm5.md) und höhere Shadermodelle | Ja       |



 

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

 

 




