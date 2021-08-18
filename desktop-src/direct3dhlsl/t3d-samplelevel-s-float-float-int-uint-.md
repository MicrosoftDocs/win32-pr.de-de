---
title: SampleLevel::SampleLevel(S,float,float,int,uint)-Funktion für Texture3D
description: Samples a texture on the specified mipmap level and returns status about the operation. (Stichprobenentnahme einer Textur auf der angegebenen Mipmapebene und Rückgabe des Status des Vorgangs. Für Texture3D. | SampleLevel::SampleLevel(S,float,float,int,uint)-Funktion
ms.assetid: D79247AC-A922-49C7-BAC6-807C31F279B1
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
ms.openlocfilehash: 3492684d6a3fb017776a2c5946da859cc8c74418660d60c3c9622915aee20dce
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119043458"
---
# <a name="samplelevelsamplelevelsfloatfloatintuint-function-for-texture3d"></a>SampleLevel::SampleLevel(S,float,float,int,uint)-Funktion für Texture3D

Samples a texture on the specified mipmap level and returns status about the operation. (Stichprobenentnahme einer Textur auf der angegebenen Mipmapebene und Rückgabe des Status des Vorgangs.

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

[SampleLevel-Methoden](texture3d-samplelevel.md)
</dt> <dt>

[**Texture3D**](sm5-object-texture3d.md)
</dt> </dl>

 

 
