---
title: SampleGrad::SampleGrad(S,float,float,float,int,float)-Funktion für Texture1D
description: Die Funktion erfasst eine Textur mithilfe eines Farbverlaufs, um die Art und Weise zu beeinflussen, wie die Stichprobenposition berechnet wird, mit einem optionalen Wert zum Zusammenbinden von LOD-Werten (Sample Level of Detail).
ms.assetid: 34A79CB6-0C45-40ED-845C-77C08F1DEC57
keywords:
- SampleGrad-Funktion HLSL
topic_type:
- apiref
api_name:
- SampleGrad
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 3c9f750f386ffb4fd3c13af717b173f752b7f515003cf16f9d2df4b37385dda9
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "117724274"
---
# <a name="samplegradsamplegradsfloatfloatfloatintfloat-function-for-texture1d"></a>SampleGrad::SampleGrad(S,float,float,float,int,float)-Funktion für Texture1D

Stichproben einer Textur, wobei ein Farbverlauf verwendet wird, um die Berechnung der Stichprobenposition zu beeinflussen, mit einem optionalen Wert zum Zusammenbinden von LOD-Werten (Sample Level of Detail).

## <a name="syntax"></a>Syntax


``` syntax
DXGI_FORMAT SampleGrad(
  in SamplerState S,
  in float        Location,
  in float        DDX,
  in float        DDY,
  in int          Offset,
  in float        Clamp
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*S* \[ in\]
</dt> <dd>

Typ: **SamplerState**

Ein [Samplerzustand.](dx-graphics-hlsl-sampler.md) Dies ist ein Objekt, das in einer Effektdatei deklariert ist, die Zustandszuweisungen enthält.

</dd> <dt>

*Standort* \[ In\]
</dt> <dd>

Typ: **float**

Texturkoordinaten Der Argumenttyp ist vom Texturobjekttyp abhängig.



| Texture-Object-Typ                    | Parametertyp |
|----------------------------------------|----------------|
| Texture1D                              | float          |
| Texture1DArray, Texture2D              | float2         |
| Texture2DArray, Texture3D, TextureCube | float3         |
| TextureCubeArray                       | float4         |



 

</dd> <dt>

*DDX* \[ in\]
</dt> <dd>

Typ: **float**

Die Änderungsrate der Oberflächengeometrie in x Richtung. Der Argumenttyp ist vom Texturobjekttyp abhängig.



| Texture-Object-Typ                      | Parametertyp |
|------------------------------------------|----------------|
| Texture1D, Texture1DArray                | float          |
| Texture2D, Texture2DArray                | float2         |
| Texture3D, TextureCube, TextureCubeArray | float3         |
| Texture2DMS, Texture2DMSArray            | Nicht unterstützt  |



 

</dd> <dt>

*DDY* \[ In\]
</dt> <dd>

Typ: **float**

Die Änderungsrate der Oberflächengeometrie in y-Richtung. Der Argumenttyp ist vom Texturobjekttyp abhängig.



| Texture-Object-Typ                      | Parametertyp |
|------------------------------------------|----------------|
| Texture1D, Texture1DArray                | float          |
| Texture2D, Texture2DArray                | float2         |
| Texture3D, TextureCube, TextureCubeArray | float3         |
| Texture2DMS, Texture2DMSArray            | Nicht unterstützt  |



 

</dd> <dt>

*Offset* \[ In\]
</dt> <dd>

Typ: **int**

Ein optionaler Texturkoordinatenoffset, der für jeden Texturobjekttyp verwendet werden kann. Der Offset wird vor der Stichprobenentnahme auf den Speicherort angewendet. Verwenden Sie einen Offset nur auf einem ganzzahligen Miplevel. Andernfalls erhalten Sie möglicherweise Ergebnisse, die sich nicht gut in die Hardware übersetzen lassen. Der Argumenttyp ist vom Texturobjekttyp abhängig. Weitere Informationen finden Sie unter [Anwenden von ganzzahligen Offsets.](dx-graphics-hlsl-to-sample.md)



| Texture-Object-Typ           | Parametertyp |
|-------------------------------|----------------|
| Texture1D, Texture1DArray     | INT            |
| Texture2D, Texture2DArray     | int2           |
| Texture3D                     | int3           |
| TextureCube, TextureCubeArray | Nicht unterstützt  |



 

</dd> <dt>

*Klammer* \[ In\]
</dt> <dd>

Typ: **float**

Ein optionaler Wert zum Klammern von LOD-Beispielwerten. Wenn Sie beispielsweise 2,0f für den Klammerwert übergeben, stellen Sie sicher, dass keine einzelne Stichprobe auf eine Mip-Ebene kleiner als 2,0f zugreift.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Typ: **[ **DXGI \_ FORMAT**](/windows/desktop/api/dxgiformat/ne-dxgiformat-dxgi_format)**

Das Texturformat, bei dem es sich um einen der typisierten Werte handelt, die in [**DXGI \_ FORMAT**](/windows/desktop/api/dxgiformat/ne-dxgiformat-dxgi_format)aufgeführt sind.

## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[SampleGrad-Methoden](texture1d-samplegrad.md)
</dt> </dl>

 

 
