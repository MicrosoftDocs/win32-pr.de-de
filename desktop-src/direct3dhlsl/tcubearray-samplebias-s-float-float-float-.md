---
title: SampleBias::SampleBias(S,float,float,float)-Funktion für TextureCubeArray
description: Die SampleBias::SampleBias(S,float,float,float)-Funktion für TextureCubeArray samplingt eine Textur, nachdem der Biaswert auf die Mipmapebene angewendet wurde.
ms.assetid: 6683F115-4F81-4C24-B735-67DB4B52455B
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
ms.openlocfilehash: ea7c030ca1a99e9d9169ac4e20c26fbb352d199f471be2f926f758c87374b092
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119043134"
---
# <a name="samplebiassamplebiassfloatfloatfloat-function-for-texturecubearray"></a>SampleBias::SampleBias(S,float,float,float)-Funktion für TextureCubeArray

Stichproben einer Textur, nachdem der Biaswert auf die Mipmapebene angewendet wurde, mit einem optionalen Wert zum Zusammenbinden von LOD-Werten (Sample Sample Level of Detail).

## <a name="syntax"></a>Syntax


``` syntax
DXGI_FORMAT SampleBias(
  in SamplerState S,
  in float        Location,
  in float        Bias,
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

[SampleBias-Methoden](texturecubearray-samplebias.md)
</dt> <dt>

[**TextureCubeArray**](texturecubearray.md)
</dt> </dl>

 

 
