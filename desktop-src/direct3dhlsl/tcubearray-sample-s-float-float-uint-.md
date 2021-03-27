---
title: 'Texturecubearray:: Sample (S, float, float, uint)-Funktion'
description: 'Führt eine Stichprobe für eine Textur mit einem optionalen Wert aus, um die Samplingrate-Werte (LOD) zu binden, und gibt den Status des Vorgangs zurück. | Texturecubearray:: Sample (S, float, float, uint)-Funktion'
ms.assetid: 5645841D-A32E-452E-873C-E070CF6A4C00
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
ms.openlocfilehash: 24e6d77698507f0d1673b66954db8e78466ac728
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/09/2021
ms.locfileid: "103761703"
---
# <a name="texturecubearraysamplesfloatfloatuint-function"></a>Texturecubearray:: Sample (S, float, float, uint)-Funktion

Führt eine Stichprobe für eine Textur mit einem optionalen Wert aus, um die Samplingrate-Werte (LOD) zu binden, und gibt den Status des Vorgangs zurück.

## <a name="syntax"></a>Syntax


``` syntax
DXGI_FORMAT Sample(
  in  SamplerState S,
  in  float        Location,
  in  float        Clamp,
  out uint         Status
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*S* \[ in\]
</dt> <dd>

Ein [samplerzustand](dx-graphics-hlsl-sampler.md). Dies ist ein Objekt, das in einer Effekt Datei deklariert wurde, die Zustands Zuweisungen enthält.

</dd> <dt>

*Speicherort* \[ in\]
</dt> <dd>

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

Ein optionaler Wert zum Einspannen von Sample-Lod-Werten. Wenn Sie beispielsweise 2.0 f als Klammer Wert übergeben, stellen Sie sicher, dass kein einzelnes Beispiel auf eine MIP-Ebene kleiner als 2.0 f zugreift.

</dd> <dt>

*Status* \[ vorgenommen\]
</dt> <dd>

Der Status des Vorgangs. Sie können nicht direkt auf den Status zugreifen. übergeben Sie stattdessen den Status an die systeminterne [**checkaccessfullymapping**](checkaccessfullymapped.md) -Funktion. **Checkaccessfullymapping** gibt **true** zurück, wenn alle Werte aus dem entsprechenden **Sample**-, **Gather**-oder **Load** -Vorgang auf zugeordnete Kacheln in einer [gekachelten Ressource](/windows/desktop/direct3d11/direct3d-11-2-features)zugegriffen haben. Wenn Werte von einer nicht zugeordneten Kachel entnommen wurden, gibt **checkaccessfullymapping** den Wert **false** zurück.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Das Textur Format, bei dem es sich um einen der im [**DXGI- \_ Format**](/windows/desktop/api/dxgiformat/ne-dxgiformat-dxgi_format)aufgelisteten typisierten Werte handelt.

## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[Beispiel Methoden](texturecubearray-sample.md)
</dt> <dt>

[**Texturecubearray**](texturecubearray.md)
</dt> </dl>

 

 
