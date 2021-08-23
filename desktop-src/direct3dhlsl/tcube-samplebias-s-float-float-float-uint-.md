---
title: SampleBias::SampleBias(S,float,float,float,uint)-Funktion für TextureCube
description: Die SampleBias::SampleBias(S,float,float,float,uint)-Funktion für TextureCube samplingt eine Textur, nachdem der Biaswert auf die Mipmapebene angewendet wurde.
ms.assetid: A2F10B9B-5DF2-4389-83A9-F6A29781BF0A
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
ms.openlocfilehash: 45640d01b744ea6d2f930a67362e323a61fc1e2f1a87417f707289d7a337090d
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119043318"
---
# <a name="samplebiassamplebiassfloatfloatfloatuint-function-for-texturecube"></a>SampleBias::SampleBias(S,float,float,float,uint)-Funktion für TextureCube

Stichproben einer Textur, nachdem der Biaswert auf die Mipmapebene angewendet wurde, mit einem optionalen Wert zum Zusammenbinden von LOD-Werten (Sample Sample Level of Detail). Gibt den Status des Vorgangs zurück.

## <a name="syntax"></a>Syntax


``` syntax
DXGI_FORMAT SampleBias(
  in  SamplerState S,
  in  float        Location,
  in  float        Bias,
  in  float        Clamp,
  out uint         Status
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

</dd> <dt>

*Status* \[ out\]
</dt> <dd>

Typ: **uint**

Der Status des Vorgangs. Sie können nicht direkt auf den Status zugreifen. Übergeben Sie stattdessen den Status an die systeminterne [**CheckAccessFullyMapped-Funktion.**](checkaccessfullymapped.md) **CheckAccessFullyMapped** gibt **TRUE** zurück, wenn alle Werte aus dem entsprechenden **Beispiel-,** **Gather-** oder **Load-Vorgang** auf zugeordnete Kacheln in einer [gekachelten Ressource](/windows/desktop/direct3d11/direct3d-11-2-features)zugegriffen haben. Wenn Werte aus einer nicht zugeordneten Kachel stammen, gibt **CheckAccessFullyMapped** **FALSE** zurück.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Typ: **[ **DXGI \_ FORMAT**](/windows/desktop/api/dxgiformat/ne-dxgiformat-dxgi_format)**

Das Texturformat, bei dem es sich um einen der typisierten Werte handelt, die in [**DXGI \_ FORMAT**](/windows/desktop/api/dxgiformat/ne-dxgiformat-dxgi_format)aufgeführt sind.

## <a name="see-also"></a>Siehe auch

<dl> <dt>

[SampleBias-Methoden](texturecube-samplebias.md)
</dt> <dt>

[**TextureCube**](texturecube.md)
</dt> </dl>

 

 
