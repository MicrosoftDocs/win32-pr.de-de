---
title: SampleLevel::SampleLevel(S,float,float,int,uint)-Funktion für Texture2D
description: Samples a Texture2D on the specified mipmap level and returns status about the operation.
ms.assetid: B021D42E-9F63-4CCE-939B-F93D91F7CB80
keywords:
- SampleLevel-Funktion HLSL
topic_type:
- apiref
api_name:
- SampleLevel
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 14e143405717730ce7d7460732941d05f72aa58e9169052a0bb1b5c705185c49
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118510289"
---
# <a name="samplelevelsamplelevelsfloatfloatintuint-function-for-texture2d"></a>SampleLevel::SampleLevel(S,float,float,int,uint)-Funktion für Texture2D

Samples a [**Texture2D**](sm5-object-texture2d.md) on the specified mipmap level and returns status about the operation.

## <a name="syntax"></a>Syntax


``` syntax
DXGI_FORMAT SampleLevel(
  in  SamplerState S,
  in  float        Location,
  in  float        LOD,
  in  int          Offset,
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



| Texture-Object Typ                    | Parametertyp |
|----------------------------------------|----------------|
| Texture1D                              | float          |
| Texture1DArray, Texture2D              | float2         |
| Texture2DArray, Texture3D, TextureCube | float3         |
| TextureCubeArray                       | float4         |



 

</dd> <dt>

*LOD* \[ In\]
</dt> <dd>

Typ: **float**

\[in \] Eine Zahl, die die Mipmapebene angibt. Wenn der Wert ≤ 0 ist, wird Mipmap-Ebene 0 (größte Karte) verwendet. Der Bruchwert (sofern angegeben) wird verwendet, um zwischen zwei Mipmapebenen zu interpolieren.

</dd> <dt>

*Offset* \[ In\]
</dt> <dd>

Typ: **int**

Ein optionaler Texturkoordinatenoffset, der für jeden Texturobjekttyp verwendet werden kann. Der Offset wird vor der Stichprobenentnahme auf die Position angewendet. Verwenden Sie einen Offset nur bei einer ganzzahligen MIP-Ebene. Andernfalls erhalten Sie möglicherweise Ergebnisse, die sich nicht gut in die Hardware übersetzen lassen. Der Argumenttyp ist vom Texturobjekttyp abhängig. Weitere Informationen finden Sie unter [Anwenden von ganzzahligen Offsets.](dx-graphics-hlsl-to-sample.md)



| Texture-Object Typ           | Parametertyp |
|-------------------------------|----------------|
| Texture1D, Texture1DArray     | INT            |
| Texture2D, Texture2DArray     | int2           |
| Texture3D                     | int3           |
| TextureCube, TextureCubeArray | Nicht unterstützt  |



 

</dd> <dt>

*Status* \[ out\]
</dt> <dd>

Typ: **uint**

Der Status des Vorgangs. Sie können nicht direkt auf den Status zugreifen. Übergeben Sie stattdessen den Status an die [**systeminterne CheckAccessFullyMapped-Funktion.**](checkaccessfullymapped.md) **CheckAccessFullyMapped** gibt **TRUE zurück,** wenn alle Werte aus dem entsprechenden **Beispiel-,** **Gather-** oder **Load-Vorgang** auf zugeordnete Kacheln in einer [gekachelten Ressource zugegriffen haben.](/windows/desktop/direct3d11/direct3d-11-2-features) Wenn Werte aus einer nicht zugeordneten Kachel übernommen wurden, gibt **CheckAccessFullyMapped** **FALSE zurück.**

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Typ: **[ **DXGI \_ FORMAT**](/windows/desktop/api/dxgiformat/ne-dxgiformat-dxgi_format)**

Das Texturformat, bei dem es sich um einen der typierten Werte handelt, die in [**DXGI \_ FORMAT aufgeführt sind.**](/windows/desktop/api/dxgiformat/ne-dxgiformat-dxgi_format)

## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[SampleLevel-Methoden](texture2d-samplelevel.md)
</dt> </dl>

 

 
