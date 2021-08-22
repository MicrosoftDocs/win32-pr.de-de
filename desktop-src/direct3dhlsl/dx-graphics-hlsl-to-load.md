---
title: Laden (DirectX HLSL-Texturobjekt)
description: Liest Texeldaten ohne Filterung oder Sampling.
ms.assetid: a2fbda88-29c7-4d28-bd3e-df1d9aa36ee8
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- apiref
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: ba394fb13fd98793401b29e6343ef4fa9ff0194b7a86f22dda1e58439737b34b
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119119864"
---
# <a name="load-directx-hlsl-texture-object"></a>Laden (DirectX HLSL-Texturobjekt)

Liest Texeldaten ohne Filterung oder Sampling.



<table>
<tbody>
<tr class="odd">
<td>ret Object.Load(<dl> typeX Location,<br />
[typeX SampleIndex, ]<br />
[typeX Offset ]<br />
</dl>);</td>
</tr>
</tbody>
</table>

typeX gibt an, dass es vier mögliche Typen gibt: **int**, **int2**, **int3** oder **int4**.

 

## <a name="parameters"></a>Parameter

<dl> <dt>

<span id="Object"></span><span id="object"></span><span id="OBJECT"></span>*Objekt*
</dt> <dd>

Ein [Texturobjekttyp](dx-graphics-hlsl-to-type.md) (außer TextureCube oder TextureCubeArray).

</dd> <dt>

<span id="Location"></span><span id="location"></span><span id="LOCATION"></span>*Lage*
</dt> <dd>

\[in \] Die Texturkoordinaten; die letzte Komponente gibt die Mipmapebene an. Diese Methode verwendet ein 0-basiertes Koordinatensystem und kein UV-System von 0,0 bis 1,0. Der Argumenttyp ist vom Texturobjekttyp abhängig.



| Objekttyp                                  | Parametertyp |
|----------------------------------------------|----------------|
| Buffer                                       | INT            |
| Texture1D, Texture2DMS                       | int2           |
| Texture1DArray, Texture 2D, Texture2DMSArray | int3           |
| Texture2DArray, Texture3D                    | int4           |



 

Um beispielsweise auf eine 2D-Textur zu zugreifen, geben Sie UV-Koordinaten für die ersten beiden Komponenten und eine Mipmapebene für die dritte Komponente an.

> [!Note]  
> Wenn mindestens eine der Koordinaten in *Location* die mipmap-Leveldimensionen u, v oder w der Textur überschreitet, gibt **Load** in allen Komponenten 0 (null) zurück. Direct3D garantiert, dass 0 (null) für jede Ressource zurückgesetzt wird, auf die über grenzenlose Grenzen zugegriffen wird.

 

</dd> <dt>

<span id="SampleIndex"></span><span id="sampleindex"></span><span id="SAMPLEINDEX"></span>*SampleIndex*
</dt> <dd>

\[in \] Ein optionaler Samplingindex.



| Texturtyp                                                                                                   | Parametertyp |
|----------------------------------------------------------------------------------------------------------------|----------------|
| Texture1D, Texture1DArray, Texture2D, Texture2DArray, Texture3D, Texture2DArray, TextureCube, TextureCubeArray | Nicht unterstützt  |
| Texture2DMS, Texture2DMSArray                                                                                 | INT            |



 

> [!Note]  
> *SampleIndex* ist nur für Texturen mit mehreren Stichproben verfügbar.

 

</dd> <dt>

<span id="Offset"></span><span id="offset"></span><span id="OFFSET"></span>*Offset*
</dt> <dd>

\[in \] Ein optionaler Offset, der vor der Stichprobenentnahme auf die Texturkoordinaten angewendet wird. Der Offsettyp ist vom Texturobjekttyp abhängig und muss statisch sein.



| Texturtyp                                             | Parametertyp |
|----------------------------------------------------------|----------------|
| Texture1D, Texture1DArray                                | INT            |
| Texture2D, Texture2DArray, Texture2DMS, Texture2DMSArray | int2           |
| Texture3D, Texture2DArray                                | int3           |



 

> [!Note]  
> Wenn Sie *Offset mit* Texturen mit mehreren Stichproben verwenden, müssen Sie auch *SampleIndex angeben.*

 

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Der Rückgabetyp entspricht dem Typ in der *Object-Deklaration.* Beispielsweise verfügt ein Texture2D-Objekt, das als "Texture2d myTexture;" deklariert wurde, über einen Rückgabewert <uint4> vom Typ **uint4.**

## <a name="minimum-shader-model"></a>Minimales Shadermodell

Diese Funktion wird in den folgenden Shadermodellen unterstützt.



| vs \_ 4 \_ 0 | vs \_ 4 \_ 1 | ps \_ 4 \_ 0 | ps \_ 4 \_ 1 | gs \_ 4 \_ 0 | gs \_ 4 \_ 1 |
|----------|-----------|----------|-----------|----------|-----------|
| x        | x         | x        | x         | x        | x         |



 

-   ShaderModell 4.1 ist in Direct3D 10.1 oder höher verfügbar.

## <a name="example"></a>Beispiel

Dieses Teilcodebeispiel ist aus der Datei Paint.fx im [AdvancedParticles-Beispiel](https://msdn.microsoft.com/library/Ee416394(v=VS.85).aspx).


```
// Object Declarations
Buffer<float4> g_ParticleBuffer;

// Shader body calling the intrinsic function
float4 PSPaint(PSQuadIn input) : SV_Target
{       
    ... 
    for( int i=g_ParticleStart; i<g_NumParticles; i+=g_ParticleStep )
    {
        ... 
        // load the particle
        float4 particlePos = g_ParticleBuffer.Load( i*4 );
        float4 particleColor = g_ParticleBuffer.Load( (i*4) + 2 );
        ...     
    }
    ...
}   
```



## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Texture-Object](dx-graphics-hlsl-to-type.md)
</dt> </dl>

 

 




