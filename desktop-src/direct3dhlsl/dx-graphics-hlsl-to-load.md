---
title: Load (DirectX-HLSL-Textur Objekt)
description: Liest textandaten ohne Filterung oder Stichprobenentnahme.
ms.assetid: a2fbda88-29c7-4d28-bd3e-df1d9aa36ee8
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- apiref
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 08d3964788a238492ff7d5189544603b35808465
ms.sourcegitcommit: 4c00910ed754d7d0a68c9a833751d714c06e3b39
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/05/2021
ms.locfileid: "104123319"
---
# <a name="load-directx-hlsl-texture-object"></a>Load (DirectX-HLSL-Textur Objekt)

Liest textandaten ohne Filterung oder Stichprobenentnahme.



<table>
<tbody>
<tr class="odd">
<td>Ret Object. Load (<dl> TypeX-Speicherort,<br />
[TypeX sampleingedex,]<br />
[TypeX-Offset]<br />
</dl>);</td>
</tr>
</tbody>
</table>

TypeX gibt an, dass vier mögliche Typen vorhanden sind: **int**, **int2**, **int3** oder **INT4**.

 

## <a name="parameters"></a>Parameter

<dl> <dt>

<span id="Object"></span><span id="object"></span><span id="OBJECT"></span>*Objekt*
</dt> <dd>

Ein [Textur Objekttyp](dx-graphics-hlsl-to-type.md) (außer texturecube oder texturecubearray).

</dd> <dt>

<span id="Location"></span><span id="location"></span><span id="LOCATION"></span>*Hotels*
</dt> <dd>

\[in \] den Texturkoordinaten gibt die letzte Komponente die MipMap-Ebene an. Diese Methode verwendet ein 0-basiertes Koordinatensystem und kein 0,0-1.0-System. Der Argumenttyp ist vom Textur Objekttyp abhängig.



| Objekttyp                                  | Parametertyp |
|----------------------------------------------|----------------|
| Buffer                                       | INT            |
| Texture1D, Texture2DMS                       | int2           |
| Texture1DArray, Textur 2D, Texture2DMSArray | int3           |
| Texture2DArray, Texture3D                    | int4           |



 

Um z. b. auf eine 2D-Textur zuzugreifen, stellen Sie UV-Koordinaten für die ersten beiden Komponenten und eine MipMap-Ebene für die dritte Komponente bereit.

> [!Note]  
> Wenn eine oder mehrere der Koordinaten an der *Position* die u-, v-oder w-MipMap-ebenendimensionen der Textur überschreiten, gibt **Load** in allen Komponenten 0 (null) zurück. Direct3D garantiert, dass NULL für alle Ressourcen zurückgegeben wird, auf die außerhalb der Grenzen zugegriffen wird.

 

</dd> <dt>

<span id="SampleIndex"></span><span id="sampleindex"></span><span id="SAMPLEINDEX"></span>*Sample Index*
</dt> <dd>

\[in \] einem optionalen Stichproben Index.



| Textur-Typ                                                                                                   | Parametertyp |
|----------------------------------------------------------------------------------------------------------------|----------------|
| Texture1D, Texture1DArray, Texture2D, Texture2DArray, Texture3D, Texture2DArray, texturecube, texturecubearray | Nicht unterstützt  |
| Texture2DMS, Texture2DMSArray ¹                                                                                 | INT            |



 

> [!Note]  
> *Sampleindex* ist nur für Texturen mit mehreren Beispielen verfügbar.

 

</dd> <dt>

<span id="Offset"></span><span id="offset"></span><span id="OFFSET"></span>*Kompensieren*
</dt> <dd>

\[\]ein optionaler Offset, der vor der Stichprobenentnahme auf die Texturkoordinaten angewendet wird. Der offsettyp ist vom Textur Objekttyp abhängig und muss statisch sein.



| Textur-Typ                                             | Parametertyp |
|----------------------------------------------------------|----------------|
| Texture1D, Texture1DArray                                | INT            |
| Texture2D, Texture2DArray, Texture2DMS, Texture2DMSArray | int2           |
| Texture3D, Texture2DArray                                | int3           |



 

> [!Note]  
> Wenn Sie *Offset* mit Multi-Sample-Texturen verwenden, müssen Sie auch *sampleindex* angeben.

 

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Der Rückgabetyp entspricht dem Typ in der *Objekt* Deklaration. Ein Texture2D-Objekt, das als "Texture2D <uint4> MyTexture;" deklariert wurde, hat beispielsweise einen Rückgabewert vom Typ " **uint4**".

## <a name="minimum-shader-model"></a>Minimaler Shader-Modell

Diese Funktion wird in den folgenden shadermodellen unterstützt.



| vs \_ 4 \_ 0 | vs \_ 4 \_ ¹ | PS \_ 4 \_ 0 | PS \_ 4 \_ ¹ | GS \_ 4 \_ 0 | GS \_ 4 \_ 1 ¹ |
|----------|-----------|----------|-----------|----------|-----------|
| x        | x         | x        | x         | x        | x         |



 

-   Das Shader-Modell 4,1 ist in Direct3D 10,1 oder höher verfügbar.

## <a name="example"></a>Beispiel

Dieses partielle Codebeispiel wird aus der Paint. FX-Datei im [advancedpartikel](https://msdn.microsoft.com/library/Ee416394(v=VS.85).aspx)-Beispiel entnommen.


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

[Texture-Objekt](dx-graphics-hlsl-to-type.md)
</dt> </dl>

 

 




