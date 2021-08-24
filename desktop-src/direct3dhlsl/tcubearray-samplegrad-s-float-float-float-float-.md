---
title: SampleGrad::SampleGrad(S,float,float,float,float)-Funktion für TextureCubeArray
description: Erfahren Sie, wie diese Funktion eine Textur mithilfe eines Farbverlaufs abtast, um die Art und Weise zu beeinflussen, wie die Stichprobenposition berechnet wird. Für TextureCubeArray.
ms.assetid: 0C7DC9AA-3F0A-47E4-852F-7AE25CF67EA3
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
ms.openlocfilehash: f49ca0673d0796fc960b9a955381ad359cb291171be2106ec11fe690cabecb52
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119892580"
---
# <a name="samplegradsamplegradsfloatfloatfloatfloat-function-for-texturecubearray"></a>SampleGrad::SampleGrad(S,float,float,float,float)-Funktion für TextureCubeArray

Stichproben einer Textur, wobei ein Farbverlauf verwendet wird, um die Berechnung der Stichprobenposition zu beeinflussen, mit einem optionalen Wert zum Zusammenbinden von LOD-Werten (Sample Level of Detail).

## <a name="syntax"></a>Syntax


``` syntax
DXGI_FORMAT SampleGrad(
  in SamplerState S,
  in float        Location,
  in float        DDX,
  in float        DDY,
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

*Klammer* \[ In\]
</dt> <dd>

Typ: **float**

Ein optionaler Wert zum Klammern von LOD-Beispielwerten. Wenn Sie beispielsweise 2,0f für den Klammerwert übergeben, stellen Sie sicher, dass keine einzelne Stichprobe auf eine Mip-Ebene kleiner als 2,0f zugreift.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Typ: **[ **DXGI \_ FORMAT**](/windows/desktop/api/dxgiformat/ne-dxgiformat-dxgi_format)**

Das Texturformat, bei dem es sich um einen der typisierten Werte handelt, die in [**DXGI \_ FORMAT**](/windows/desktop/api/dxgiformat/ne-dxgiformat-dxgi_format)aufgeführt sind.

## <a name="see-also"></a>Siehe auch

<dl> <dt>

[SampleGrad-Methoden](texturecubearray-samplegrad.md)
</dt> <dt>

[**TextureCubeArray**](texturecubearray.md)
</dt> </dl>

 

 
