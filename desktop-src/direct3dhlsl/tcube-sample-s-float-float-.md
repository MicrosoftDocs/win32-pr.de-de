---
title: TextureCube::Sample(S,float,float)-Funktion
description: Samples a texture with an optional value to clamp sample level-of-detail (LOD) values to . | TextureCube::Sample(S,float,float)-Funktion
ms.assetid: 7DB25135-46B5-48E2-91D0-A45D355179D6
keywords:
- Beispielfunktion HLSL
topic_type:
- apiref
api_name:
- Sample
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 08613bb9b9465f1908828025316018d1747b1b0f7805478ce535457e45a2be18
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118788172"
---
# <a name="texturecubesamplesfloatfloat-function"></a>TextureCube::Sample(S,float,float)-Funktion

Samples a texture with an optional value to clamp sample level-of-detail (LOD) values to .

## <a name="syntax"></a>Syntax


``` syntax
DXGI_FORMAT Sample(
  in SamplerState S,
  in float        Location,
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

[Beispielmethoden](texturecube-sample.md)
</dt> <dt>

[**TextureCube**](texturecube.md)
</dt> </dl>

 

 
