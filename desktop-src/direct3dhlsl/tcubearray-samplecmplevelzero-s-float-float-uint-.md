---
title: SampleCmpLevelZero::SampleCmpLevelZero(S,float,float,uint)-Funktion für TextureCubeArray
description: Stichproben einer Textur nur auf mipmap-Ebene 0, vergleicht das Ergebnis mit einem Vergleichswert und gibt dann den Status des Vorgangs zurück. Für TextureCubeArray.
ms.assetid: D73447C6-E77C-4027-B265-24F96C679357
keywords:
- SampleCmpLevelZero-Funktion HLSL
topic_type:
- apiref
api_name:
- SampleCmpLevelZero
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 446db99336e07a526b73b4bbcb743b13107f8427958c19bcbd091f41350b6f77
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "120023090"
---
# <a name="samplecmplevelzerosamplecmplevelzerosfloatfloatuint-function-for-texturecubearray"></a>SampleCmpLevelZero::SampleCmpLevelZero(S,float,float,uint)-Funktion für TextureCubeArray

Samples a texture on mipmap level 0 only and compares the result to a comparison value. (Stichprobenentnahme einer Textur nur auf Mipmap-Ebene 0 und Vergleich des Ergebnisses mit einem Vergleichswert. Gibt den Status des Vorgangs zurück.

## <a name="syntax"></a>Syntax


``` syntax
DXGI_FORMAT SampleCmpLevelZero(
  in  SamplerState S,
  in  float        Location,
  in  float        CompareValue,
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

*Status* \[ out\]
</dt> <dd>

Typ: **uint**

Der Status des Vorgangs. Sie können nicht direkt auf den Status zugreifen. Übergeben Sie stattdessen den Status an die [**systeminterne CheckAccessFullyMapped-Funktion.**](checkaccessfullymapped.md) **CheckAccessFullyMapped** gibt **TRUE zurück,** wenn alle Werte aus dem entsprechenden **Beispiel-,** **Gather-** oder **Load-Vorgang** auf zugeordnete Kacheln in einer [gekachelten Ressource zugegriffen haben.](/windows/desktop/direct3d11/direct3d-11-2-features) Wenn Werte aus einer nicht zugeordneten Kachel übernommen wurden, gibt **CheckAccessFullyMapped** **FALSE zurück.**

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Typ: **[ **DXGI \_ FORMAT**](/windows/desktop/api/dxgiformat/ne-dxgiformat-dxgi_format)**

Das Texturformat, bei dem es sich um einen der typierten Werte handelt, die in [**DXGI \_ FORMAT aufgeführt sind.**](/windows/desktop/api/dxgiformat/ne-dxgiformat-dxgi_format)

## <a name="see-also"></a>Siehe auch

<dl> <dt>

[SampleCmpLevelZero-Methoden](texturecubearray-samplecmplevelzero.md)
</dt> <dt>

[**TextureCubeArray**](texturecubearray.md)
</dt> </dl>

 

 
