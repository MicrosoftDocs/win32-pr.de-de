---
title: 'Texturecubearray:: Sample (S, float, float)-Funktion'
description: 'Gibt eine Textur mit einem optionalen Wert aus, mit dem die Werte der Sample-Ebene (LOD) an eine Klammer angezeigt werden. | Texturecubearray:: Sample (S, float, float)-Funktion'
ms.assetid: E3BACA5E-18FC-4BD7-A8D8-C2808BDF1517
keywords:
- Beispiel Funktion HLSL
topic_type:
- apiref
api_name:
- Sample
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 0f3f822ee334262dc50950064c6b4257aca3dd1f
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/09/2021
ms.locfileid: "104981481"
---
# <a name="texturecubearraysamplesfloatfloat-function"></a>Texturecubearray:: Sample (S, float, float)-Funktion

Gibt eine Textur mit einem optionalen Wert aus, mit dem die Werte der Sample-Ebene (LOD) an eine Klammer angezeigt werden.

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

Typ: **samplerstate**

Ein [samplerzustand](dx-graphics-hlsl-sampler.md). Dies ist ein Objekt, das in einer Effekt Datei deklariert wurde, die Zustands Zuweisungen enthält.

</dd> <dt>

*Speicherort* \[ in\]
</dt> <dd>

Typ: **float**

Texturkoordinaten Der Argumenttyp ist vom Textur Objekttyp abhängig.



| Texture-Object-Typ                    | Parametertyp |
|----------------------------------------|----------------|
| Texture1D                              | float          |
| Texture1DArray, Texture2D              | float2         |
| Texture2DArray, Texture3D, texturecube | float3         |
| Texturecubearray                       | float4         |



 

</dd> <dt>

*Klammer* \[ in\]
</dt> <dd>

Typ: **float**

Ein optionaler Wert zum Einspannen von Sample-Lod-Werten. Wenn Sie beispielsweise 2.0 f als Klammer Wert übergeben, stellen Sie sicher, dass kein einzelnes Beispiel auf eine MIP-Ebene kleiner als 2.0 f zugreift.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Typ: **[ **DXGI- \_ Format**](/windows/desktop/api/dxgiformat/ne-dxgiformat-dxgi_format)**

Das Textur Format, bei dem es sich um einen der im [**DXGI- \_ Format**](/windows/desktop/api/dxgiformat/ne-dxgiformat-dxgi_format)aufgelisteten typisierten Werte handelt.

## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[Beispiel Methoden](texturecubearray-sample.md)
</dt> <dt>

[**Texturecubearray**](texturecubearray.md)
</dt> </dl>

 

 
