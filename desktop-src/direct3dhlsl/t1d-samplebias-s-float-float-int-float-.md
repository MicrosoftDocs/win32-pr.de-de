---
title: SampleBias::SampleBias(S,float,float,int,float)-Funktion für Texture1D
description: Die SampleBias::SampleBias(S,float,float,int,float)-Funktion samplingt eine Textur, nachdem der Biaswert auf die Mipmapebene angewendet wurde.
ms.assetid: 88BC4E99-B33D-4DAA-9A77-849B2F5FE6A7
keywords:
- SampleBias-Funktion HLSL
topic_type:
- apiref
api_name:
- SampleBias
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 120eb2f4f6b092b29e6dc5bd763152a2336e1d87a1ec5f15f2570587632f6dd3
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118285308"
---
# <a name="samplebiassamplebiassfloatfloatintfloat-function-for-texture1d"></a>SampleBias::SampleBias(S,float,float,int,float)-Funktion für Texture1D

Stichproben einer Textur, nachdem der Biaswert auf die Mipmapebene angewendet wurde, mit einem optionalen Wert zum Zusammenbinden von LOD-Werten (Sample Sample Level of Detail).

## <a name="syntax"></a>Syntax


``` syntax
DXGI_FORMAT SampleBias(
  in SamplerState S,
  in float        Location,
  in float        Bias,
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

*Voreingenommenheit* \[ In\]
</dt> <dd>

Typ: **float**

Der Biaswert, bei dem es sich um eine Gleitkommazahl zwischen 0,0 und einschließlich 1,0 handelt, wird vor der Stichprobenentnahme auf eine Mip-Ebene angewendet.

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

## <a name="see-also"></a>Siehe auch

<dl> <dt>

[SampleBias-Methoden](texture1d-samplebias.md)
</dt> </dl>

 

 
