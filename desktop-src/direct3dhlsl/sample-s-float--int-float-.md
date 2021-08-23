---
title: Sample(S,float,int,float)-Funktion (HLSL-Referenz)
description: Probieren Sie eine Texture2D mit einem optionalen Wert aus, um LoD-Werte (Sample Level of Detail) zu klammern.
ms.assetid: 899FACB6-40BB-471B-82A7-BDBBC63B206E
keywords:
- HLSL-Beispielfunktion
topic_type:
- apiref
api_name:
- Sample
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: d22cf5fa8a8fe03a62b554def7caf28b4c4e8ab9065446bab9281e4e791e5d3c
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118986220"
---
# <a name="samplesfloatintfloat-function-hlsl-reference"></a>Sample(S,float,int,float)-Funktion (HLSL-Referenz)

Probieren Sie eine [**Texture2D**](sm5-object-texture2d.md) mit einem optionalen Wert aus, um LoD-Werte (Sample Level of Detail) zu klammern.

> [!Note]  
> Erfordert [Shadermodell 5](d3d11-graphics-reference-sm5.md) oder höher.

 

## <a name="syntax"></a>Syntax

``` syntax
DXGI_FORMAT Sample(
  in SamplerState S,
  in float Location,
  in int Offset,
  in float Clamp
);
```

## <a name="parameters"></a>Parameter

<dl> <dt>

*S* \[ in\]
</dt> <dd>

Ein [Samplerzustand.](dx-graphics-hlsl-sampler.md) Dies ist ein Objekt, das in einer Effektdatei deklariert ist, die Zustandszuweisungen enthält.

</dd> <dt>

*Standort* \[ In\]
</dt> <dd>

Texturkoordinaten Der Argumenttyp ist vom Texturobjekttyp abhängig.



| Texture-Object-Typ                    | Parametertyp |
|----------------------------------------|----------------|
| Texture1D                              | float          |
| Texture1DArray, Texture2D              | float2         |
| Texture2DArray, Texture3D, TextureCube | float3         |
| TextureCubeArray                       | float4         |



 

</dd> <dt>

*Offset* \[ In\]
</dt> <dd>

Ein optionaler Texturkoordinatenoffset, der für jeden Texturobjekttyp verwendet werden kann. Der Offset wird vor der Stichprobenentnahme auf den Speicherort angewendet. Die Texturoffsets müssen statisch sein. Der Argumenttyp ist vom Texturobjekttyp abhängig. Weitere Informationen finden Sie unter [Anwenden von Texturkoordinatenoffsets.](dx-graphics-hlsl-to-sample.md)



| Texture-Object-Typ           | Parametertyp |
|-------------------------------|----------------|
| Texture1D, Texture1DArray     | INT            |
| Texture2D, Texture2DArray     | int2           |
| Texture3D                     | int3           |
| TextureCube, TextureCubeArray | Nicht unterstützt  |



 

</dd> <dt>

*Klammer* \[ In\]
</dt> <dd>

Ein optionaler Wert zum Klammern von LOD-Beispielwerten. Wenn Sie beispielsweise 2,0f für den Klammerwert übergeben, stellen Sie sicher, dass keine einzelne Stichprobe auf eine Mip-Ebene kleiner als 2,0f zugreift.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Das Texturformat, bei dem es sich um einen der typisierten Werte handelt, die in [**DXGI \_ FORMAT**](/windows/desktop/api/dxgiformat/ne-dxgiformat-dxgi_format)aufgeführt sind.

## <a name="remarks"></a>Hinweise

Textursampling verwendet die Texelposition, um einen Texelwert zu suchen. Vor der Suche kann ein Offset auf die Position angewendet werden. Der Zustand des Samplers enthält die Sampling- und Filteroptionen. Diese Methode kann innerhalb eines Pixel-Shaders aufgerufen werden, wird jedoch in einem Scheitelpunkt-Shader oder einem Geometrie-Shader nicht unterstützt.

Verwenden Sie einen Offset nur auf einem ganzzahligen Miplevel. Andernfalls erhalten Sie je nach Hardwareimplementierungen oder Treibereinstellungen möglicherweise unterschiedliche Ergebnisse.

### <a name="calculating-texel-positions"></a>Berechnen von Texelpositionen

Texturkoordinaten sind Gleitkommawerte, die auf Texturdaten verweisen, die auch als normalisierter Texturraum bezeichnet werden. Adressumbruchmodi werden in dieser Reihenfolge angewendet (Texturkoordinaten + Offsets + Umbruchmodus), um Texturkoordinaten außerhalb des \[ Bereichs 0...1 zu \] ändern.

Bei Texturarrays gibt ein zusätzlicher Wert im location-Parameter einen Index in einem Texturarray an. Dieser Index wird als skalierter float-Wert behandelt (anstelle des normalisierten Raums für Standardtexturkoordinaten). Die Konvertierung in einen ganzzahligen Index erfolgt in der folgenden Reihenfolge (float + round-to-nearest-even integer + Klammer an den Arraybereich).

### <a name="applying-texture-coordinate-offsets"></a>Anwenden von Texturkoordinatenoffsets

Der offset-Parameter ändert die Texturkoordinaten im Texelraum. Obwohl Texturkoordinaten gleitkommazahlen normalisiert sind, wendet der Offset einen ganzzahligen Offset an. Beachten Sie auch, dass die Texturoffsets statisch sein müssen.

Das zurückgegebene Datenformat wird durch das Texturformat bestimmt. Wenn die Texturressource z. B. mit dem \_ DXGI FORMAT \_ A8B8G8R8 \_ UNORM \_ SRGB-Format definiert wurde, konvertiert der Samplingvorgang die stichprobenierten Texel von Gamma 2.0 in 1.0, filtert und schreibt das Ergebnis als Gleitkommawert im Bereich \[ 0..1. \]

Verwenden Sie einen Offset nur auf einem ganzzahligen Miplevel. Andernfalls erhalten Sie möglicherweise Ergebnisse, die sich nicht gut in die Hardware übersetzen lassen.

## <a name="see-also"></a>Siehe auch

<dl> <dt>

[Beispielmethoden](texture-sample-overload.md)
</dt> <dt>

[Texturobjekt](dx-graphics-hlsl-to-type.md)
</dt> </dl>

 

 
