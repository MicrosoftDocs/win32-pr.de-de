---
title: SampleCmp::SampleCmp(S,float,float,int,float,uint)-Funktion für Texture1D
description: Die Funktion verwendet einen Vergleichswert, um Stichproben abzulehnen, mit einem optionalen Wert, an den Diebwerte der Detailebene (Sample Level-of-Detail, LOD) klammern. Für Texture1D.
ms.assetid: D2320225-4BC6-4229-A624-6D0F105DD788
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
ms.openlocfilehash: 9782d7196d740ddd0b93256182f16b57e0bdc81d18e7a0648bee5e4380edf373
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "117724304"
---
# <a name="samplecmpsamplecmpsfloatfloatintfloatuint-function-for-texture1d"></a>SampleCmp::SampleCmp(S,float,float,int,float,uint)-Funktion für Texture1D

Samples a texture, using a comparison value to reject samples, with an optional value to clamp sample level-of-detail (LOD) values to . Gibt den Status des Vorgangs zurück.

## <a name="syntax"></a>Syntax


``` syntax
DXGI_FORMAT SampleCmp(
  in  SamplerState S,
  in  float        Location,
  in  float        CompareValue,
  in  int          Offset,
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

*Klammer* \[ In\]
</dt> <dd>

Typ: **float**

Ein optionaler Wert, an den LoD-Beispielwerte klammern werden. Wenn Sie z. B. 2,0f für den Klammerwert übergeben, stellen Sie sicher, dass keine einzelne Stichprobe auf eine Mip-Ebene unter 2,0f zuf zutritt.

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

[SampleCmp-Methoden](texture1d-samplecmp.md)
</dt> </dl>

 

 
