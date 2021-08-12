---
title: SampleLevel::SampleLevel(S,float,float,uint)-Funktion
description: Probieren Sie eine Textur auf der angegebenen Mipmapebene aus und gibt den Status des Vorgangs zurück. | SampleLevel::SampleLevel(S,float,float,uint)-Funktion
ms.assetid: 3794D17F-BC70-4D3A-9F2C-ADF900983D2C
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
ms.openlocfilehash: 6eb4e4f6d3320bcac06c973ef28e8af0934f3a55da9045f01141157240434fbb
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118284298"
---
# <a name="samplelevelsamplelevelsfloatfloatuint-function"></a>SampleLevel::SampleLevel(S,float,float,uint)-Funktion

Probieren Sie eine Textur auf der angegebenen Mipmapebene aus und gibt den Status des Vorgangs zurück.

## <a name="syntax"></a>Syntax


``` syntax
DXGI_FORMAT SampleLevel(
  in  SamplerState S,
  in  float        Location,
  in  float        LOD,
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

*LOD* \[ In\]
</dt> <dd>

Typ: **float**

\[in \] Eine Zahl, die die Mipmapebene angibt. Wenn der Wert ≤ 0 ist, wird mipmap level 0 (größte Karte) verwendet. Der Bruchwert (sofern angegeben) wird verwendet, um zwischen zwei Mipmapebenen zu interpolieren.

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

[SampleLevel-Methoden](texturecubearray-samplelevel.md)
</dt> <dt>

[**TextureCubeArray**](texturecubearray.md)
</dt> </dl>

 

 
