---
title: SampleCmp::SampleCmp(S,float,float,float)-Funktion für TextureCube
description: Samples a texture, using a comparison value to reject samples, with an optional value to clamp sample level-of-detail (LOD) values to . | SampleCmp::SampleCmp(S,float,float,float)-Funktion für TextureCube
ms.assetid: FCCF12CF-3F0A-4468-9FC4-27CAAF0BEEE3
keywords:
- SampleCmp-Funktion HLSL
topic_type:
- apiref
api_name:
- SampleCmp
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: d46ab1adc7e5ce84d1cc8e8673babd5f24fb2afe33a620162fa757d5650053e5
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118506555"
---
# <a name="samplecmpsamplecmpsfloatfloatfloat-function-for-texturecube"></a>SampleCmp::SampleCmp(S,float,float,float)-Funktion für TextureCube

Samples a texture, using a comparison value to reject samples, with an optional value to clamp sample level-of-detail (LOD) values to .

## <a name="syntax"></a>Syntax


``` syntax
DXGI_FORMAT SampleCmp(
  in SamplerState S,
  in float        Location,
  in float        CompareValue,
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



| Texture-Object Typ                    | Parametertyp |
|----------------------------------------|----------------|
| Texture1D                              | float          |
| Texture1DArray, Texture2D              | float2         |
| Texture2DArray, Texture3D, TextureCube | float3         |
| TextureCubeArray                       | float4         |



 

</dd> <dt>

*CompareValue* \[ In\]
</dt> <dd>

Typ: **float**

Ein Gleitkommawert, der als Vergleichswert verwendet werden soll.

</dd> <dt>

*Klammer* \[ In\]
</dt> <dd>

Typ: **float**

Ein optionaler Wert, an den LoD-Beispielwerte klammern werden. Wenn Sie z. B. 2,0f für den Klammerwert übergeben, stellen Sie sicher, dass keine einzelne Stichprobe auf eine MIP-Ebene unter 2,0f zuf zutritt.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Typ: **[ **DXGI \_ FORMAT**](/windows/desktop/api/dxgiformat/ne-dxgiformat-dxgi_format)**

Das Texturformat, bei dem es sich um einen der typierten Werte handelt, die in [**DXGI \_ FORMAT aufgeführt sind.**](/windows/desktop/api/dxgiformat/ne-dxgiformat-dxgi_format)

## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[SampleCmp-Methoden](texturecube-samplecmp.md)
</dt> <dt>

[**TextureCube**](texturecube.md)
</dt> </dl>

 

 
