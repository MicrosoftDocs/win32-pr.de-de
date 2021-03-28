---
title: 'Samplelevel:: samplelevel (S, float, float, uint)-Funktion'
description: 'Führt eine Stichprobe für eine Textur auf der angegebenen MipMap-Ebene aus und gibt den Status des Vorgangs zurück. | Samplelevel:: samplelevel (S, float, float, uint)-Funktion'
ms.assetid: 3794D17F-BC70-4D3A-9F2C-ADF900983D2C
keywords:
- Samplelevel-Funktion HLSL
topic_type:
- apiref
api_name:
- SampleLevel
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 356e2779d82e886946e93d2071ae693279c07eb8
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/09/2021
ms.locfileid: "104219266"
---
# <a name="samplelevelsamplelevelsfloatfloatuint-function"></a>Samplelevel:: samplelevel (S, float, float, uint)-Funktion

Führt eine Stichprobe für eine Textur auf der angegebenen MipMap-Ebene aus und gibt den Status des Vorgangs zurück.

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

*Lod* \[ in\]
</dt> <dd>

Typ: **float**

\[in \] einer Zahl, die die MipMap-Ebene angibt. Wenn der Wert 0 (null) ist, wird MipMap Level 0 (größte Zuordnung) verwendet. Der Bruch Wert (falls angegeben) wird verwendet, um zwischen zwei MipMap-Ebenen zu interpolieren.

</dd> <dt>

*Status* \[ vorgenommen\]
</dt> <dd>

Typ: **uint**

Der Status des Vorgangs. Sie können nicht direkt auf den Status zugreifen. übergeben Sie stattdessen den Status an die systeminterne [**checkaccessfullymapping**](checkaccessfullymapped.md) -Funktion. **Checkaccessfullymapping** gibt **true** zurück, wenn alle Werte aus dem entsprechenden **Sample**-, **Gather**-oder **Load** -Vorgang auf zugeordnete Kacheln in einer [gekachelten Ressource](/windows/desktop/direct3d11/direct3d-11-2-features)zugegriffen haben. Wenn Werte von einer nicht zugeordneten Kachel entnommen wurden, gibt **checkaccessfullymapping** den Wert **false** zurück.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Typ: **[ **DXGI- \_ Format**](/windows/desktop/api/dxgiformat/ne-dxgiformat-dxgi_format)**

Das Textur Format, bei dem es sich um einen der im [**DXGI- \_ Format**](/windows/desktop/api/dxgiformat/ne-dxgiformat-dxgi_format)aufgelisteten typisierten Werte handelt.

## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[Samplelevel-Methoden](texturecubearray-samplelevel.md)
</dt> <dt>

[**Texturecubearray**](texturecubearray.md)
</dt> </dl>

 

 
