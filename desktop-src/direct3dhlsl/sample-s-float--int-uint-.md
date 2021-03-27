---
title: Sample (S, float, int, float, uint)-Funktion (HLSL-Referenz)
description: Führt eine Stichprobe für ein Texture2D-Element mit einem optionalen Wert aus, um die Samplingrate-Werte (LOD) zu binden, und gibt den Status des Vorgangs zurück.
ms.assetid: 1B9F48C4-DDB9-4547-B4AF-81A3ADA44C3F
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
ms.openlocfilehash: 9b378cb4031acecb8e0018053c7547e1948cc3e6
ms.sourcegitcommit: 0d6365d4e852b09a9100d9cfb9a5334922ebf478
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 11/17/2020
ms.locfileid: "103735217"
---
# <a name="samplesfloatintfloatuint-function-hlsl-reference"></a>Sample (S, float, int, float, uint)-Funktion (HLSL-Referenz)

Führt eine Stichprobe für ein [**Texture2D**](sm5-object-texture2d.md) -Element mit einem optionalen Wert aus, um die Samplingrate-Werte (LOD) zu binden, und gibt den Status des Vorgangs zurück.

> [!Note]  
> Erfordert [Shader-Modell 5](d3d11-graphics-reference-sm5.md) oder höher.

 

## <a name="syntax"></a>Syntax

``` syntax
DXGI_FORMAT Sample(
  in  SamplerState S,
  in  float Location,
  in  int Offset,
  in  float Clamp,
  out uint Status
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

*Offset* \[ in\]
</dt> <dd>

Ein optionaler Offset der Textur Koordinate, der für jeden Textur Objekttyp verwendet werden kann. der Offset wird vor der Stichprobenentnahme auf den Speicherort angewendet. Die Textur Offsets müssen statisch sein. Der Argumenttyp ist vom Textur Objekttyp abhängig. Weitere Informationen finden Sie unter [Anwenden von Texturkoordinaten Offsets](dx-graphics-hlsl-to-sample.md).



| Texture-Object-Typ           | Parametertyp |
|-------------------------------|----------------|
| Texture1D, Texture1DArray     | INT            |
| Texture2D, Texture2DArray     | int2           |
| Texture3D                     | int3           |
| Texturecube, texturecubearray | Nicht unterstützt  |



 

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

## <a name="remarks"></a>Bemerkungen

Bei der Textur Stichprobe wird die texusposition verwendet, um einen Texttyp zu suchen Ein Offset kann vor der Suche auf die Position angewendet werden. Der samplerstatus enthält die Optionen für Sampling und Filterung. Diese Methode kann in einem Pixelshader aufgerufen werden, wird jedoch in einem Vertexshader oder einem Geometry-Shader nicht unterstützt.

Verwenden Sie einen Offset nur bei einer ganzzahligen miplevel. Andernfalls erhalten Sie abhängig von der Hardware Implementierung oder den Treibereinstellungen möglicherweise unterschiedliche Ergebnisse.

### <a name="calculating-texel-positions"></a>Berechnen von textabpositionen

Texturkoordinaten sind Gleit Komma Werte, die auf Textur Daten verweisen, die auch als normalisierter Textur Raum bezeichnet werden. Adress Umbruch Modi werden in dieser Reihenfolge (Texturkoordinaten + Offsets + Wrap-Modus) angewendet, um die Texturkoordinaten außerhalb des \[ Bereichs 0... 1 zu ändern \] .

Bei Textur Arrays gibt ein zusätzlicher Wert im Location-Parameter einen Index in ein Textur Array an. Dieser Index wird als skalierter float-Wert (anstelle des normalisierten Raums für standardmäßige Texturkoordinaten) behandelt. Die Konvertierung in einen ganzzahligen Index erfolgt in der folgenden Reihenfolge (float + Round-to-Next-even Integer + Klammer zum Array Bereich).

### <a name="applying-texture-coordinate-offsets"></a>Anwenden von Texturkoordinaten Offsets

Der Offset-Parameter ändert die Texturkoordinaten in texesbereich. Obwohl Texturkoordinaten normalisierte Gleit Komma Zahlen sind, wendet der Offset einen ganzzahligen Offset an. Beachten Sie auch, dass die Textur Offsets statisch sein müssen.

Das zurückgegebene Datenformat wird durch das Textur Format bestimmt. Wenn die Textur Ressource z. b. mit dem DXGI- \_ Format \_ A8B8G8R8 \_ unorm \_ sRGB-Format definiert wurde, konvertiert der Samplingvorgang Sampling-texeln von Gamma 2,0 in 1,0, filtert und schreibt das Ergebnis als Gleit Komma Wert im Bereich \[ 0.. 1 \] .

## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[Beispiel Methoden](texture-sample-overload.md)
</dt> <dt>

[Texture-Objekt](dx-graphics-hlsl-to-type.md)
</dt> </dl>

 

 
