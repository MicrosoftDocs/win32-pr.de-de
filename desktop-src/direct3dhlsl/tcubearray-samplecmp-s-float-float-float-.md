---
title: SampleCmp::SampleCmp(S,float,float,float)-Funktion für TextureCubeArray
description: Samples a texture, using a comparison value to reject samples, with an optional value to clamp sample level-of-detail (LOD) values to . | SampleCmp::SampleCmp(S,float,float,float)-Funktion für TextureCubeArray
ms.assetid: A8824A82-A3FD-4FEE-BC10-56843997BBCE
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
ms.openlocfilehash: c5d5e8945dc04f11e62cf668cfdd81fc2f8f616bce00482cadad4a7e1cde398f
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "117723298"
---
# <a name="samplecmpsamplecmpsfloatfloatfloat-function-for-texturecubearray"></a>SampleCmp::SampleCmp(S,float,float,float)-Funktion für TextureCubeArray

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

Ein optionaler Wert, an den LoD-Beispielwerte klammern werden. Wenn Sie z. B. 2,0f für den Klammerwert übergeben, stellen Sie sicher, dass keine einzelne Stichprobe auf eine Mip-Ebene unter 2,0f zuf zutritt.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Typ: **[ **DXGI \_ FORMAT**](/windows/desktop/api/dxgiformat/ne-dxgiformat-dxgi_format)**

Das Texturformat, bei dem es sich um einen der typierten Werte handelt, die in [**DXGI \_ FORMAT aufgeführt sind.**](/windows/desktop/api/dxgiformat/ne-dxgiformat-dxgi_format)

## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[SampleCmp-Methoden](texturecubearray-samplecmp.md)
</dt> <dt>

[**TextureCubeArray**](texturecubearray.md)
</dt> </dl>

 

 
