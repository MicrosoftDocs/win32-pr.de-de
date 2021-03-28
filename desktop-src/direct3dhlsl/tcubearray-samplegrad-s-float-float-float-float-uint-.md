---
title: 'Samplegrad:: samplegrad (S, float, float, float, float, uint)-Funktion für texturecubearray'
description: Erfahren Sie, wie diese Funktion eine Textur Abtast, wobei ein Farbverlauf verwendet wird, um die Art und Weise zu beeinflussen, in der der Beispiel Speicherort berechnet wird Für texturecubearray.
ms.assetid: 849FAF04-A133-4E5B-967E-0679AE335CCC
keywords:
- Samplegrad-Funktion HLSL
topic_type:
- apiref
api_name:
- SampleGrad
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 00adfb5c7a1a95e5462b1bc524a6c7d86f71c2e8
ms.sourcegitcommit: 168d11879cb9fd89d26f826482725c0a626be00f
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/16/2021
ms.locfileid: "104982645"
---
# <a name="samplegradsamplegradsfloatfloatfloatfloatuint-function-for-texturecubearray"></a>Samplegrad:: samplegrad (S, float, float, float, float, uint)-Funktion für texturecubearray

Verwendet einen Farbverlauf, um die Art und Weise zu beeinflussen, wie der Beispiel Speicherort berechnet wird, mit einem optionalen Wert, mit dem Samplingrate-Werte (LOD-Werte) fixiert werden. Gibt den Status des Vorgangs zurück.

## <a name="syntax"></a>Syntax


``` syntax
DXGI_FORMAT SampleGrad(
  in  SamplerState S,
  in  float        Location,
  in  float        DDX,
  in  float        DDY,
  in  float        Clamp,
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

*DDX* \[ in\]
</dt> <dd>

Typ: **float**

Die Änderungs Rate der Oberflächengeometrie in der x-Richtung. Der Argumenttyp ist vom Textur Objekttyp abhängig.



| Texture-Object-Typ                      | Parametertyp |
|------------------------------------------|----------------|
| Texture1D, Texture1DArray                | float          |
| Texture2D, Texture2DArray                | float2         |
| Texture3D, texturecube, texturecubearray | float3         |
| Texture2DMS, Texture2DMSArray            | Nicht unterstützt  |



 

</dd> <dt>

Nicht mehr  \[ in\]
</dt> <dd>

Typ: **float**

Die Änderungs Rate der Oberflächengeometrie in der y-Richtung. Der Argumenttyp ist vom Textur Objekttyp abhängig.



| Texture-Object-Typ                      | Parametertyp |
|------------------------------------------|----------------|
| Texture1D, Texture1DArray                | float          |
| Texture2D, Texture2DArray                | float2         |
| Texture3D, texturecube, texturecubearray | float3         |
| Texture2DMS, Texture2DMSArray            | Nicht unterstützt  |



 

</dd> <dt>

*Klammer* \[ in\]
</dt> <dd>

Typ: **float**

Ein optionaler Wert zum Einspannen von Sample-Lod-Werten. Wenn Sie beispielsweise 2.0 f als Klammer Wert übergeben, stellen Sie sicher, dass kein einzelnes Beispiel auf eine MIP-Ebene kleiner als 2.0 f zugreift.

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

[Samplegrad-Methoden](texturecubearray-samplegrad.md)
</dt> <dt>

[**Texturecubearray**](texturecubearray.md)
</dt> </dl>

 

 
