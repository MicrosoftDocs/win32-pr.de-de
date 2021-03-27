---
title: 'Samplecmp:: samplecmp (S, float, float, int, float, uint)-Funktion für Texture2DArray'
description: Diese Funktion prüft eine Textur mithilfe eines Vergleichs Werts, um Beispiele abzulehnen, mit einem optionalen Wert, mit dem Samplingrate-Werte (LOD-Werte) an eine Klammer mit einem optionalen Wert überstehen. Für Texture2DArray.
ms.assetid: 847A6B79-3A66-4209-AB01-7C1FDA8A433A
keywords:
- Samplecmp-Funktion HLSL
topic_type:
- apiref
api_name:
- SampleCmp
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: cc8957ca2f6c1eb3e4a665b5d6df134c854ccc3c
ms.sourcegitcommit: 168d11879cb9fd89d26f826482725c0a626be00f
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/16/2021
ms.locfileid: "104219735"
---
# <a name="samplecmpsamplecmpsfloatfloatintfloatuint-function-for-texture2darray"></a>Samplecmp:: samplecmp (S, float, float, int, float, uint)-Funktion für Texture2DArray

Verwendet einen Vergleichswert zum ablehnen von Beispielen, wobei ein optionaler Wert zum Einspannen von Samplingrate-Werten (LOD) an verwendet wird. Gibt den Status des Vorgangs zurück.

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

*CompareValue* \[ in\]
</dt> <dd>

Typ: **float**

Ein Gleit Komma Wert, der als Vergleichswert verwendet werden soll.

</dd> <dt>

*Offset* \[ in\]
</dt> <dd>

Typ: **int**

Ein optionaler Offset der Textur Koordinate, der für jeden Textur Objekttyp verwendet werden kann. der Offset wird vor der Stichprobenentnahme auf den Speicherort angewendet. Verwenden Sie einen Offset nur bei einer ganzzahligen miplevel. Andernfalls erhalten Sie möglicherweise Ergebnisse, die nicht gut in Hardware übersetzt werden. Der Argumenttyp ist vom Textur Objekttyp abhängig. Weitere Informationen finden Sie unter [Anwenden von ganzzahligen Offsets](dx-graphics-hlsl-to-sample.md).



| Texture-Object-Typ           | Parametertyp |
|-------------------------------|----------------|
| Texture1D, Texture1DArray     | INT            |
| Texture2D, Texture2DArray     | int2           |
| Texture3D                     | int3           |
| Texturecube, texturecubearray | Nicht unterstützt  |



 

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

[Samplecmp-Methoden](texture2darray-samplecmp.md)
</dt> <dt>

[**Texture2DArray**](sm5-object-texture2darray.md)
</dt> </dl>

 

 
