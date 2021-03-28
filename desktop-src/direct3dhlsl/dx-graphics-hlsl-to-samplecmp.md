---
title: Samplecmp (DirectX HLSL-Textur Objekt)
description: Vergleicht eine Textur und vergleicht eine einzelne Komponente mit dem angegebenen Vergleichswert.
ms.assetid: e21894c4-e8c5-4c3d-92c1-727964f8fd94
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- apiref
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 6991bead4bfc42451c26fe5476b4c114626eb7e8
ms.sourcegitcommit: 0d6365d4e852b09a9100d9cfb9a5334922ebf478
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 11/17/2020
ms.locfileid: "104993654"
---
# <a name="samplecmp-directx-hlsl-texture-object"></a>Samplecmp (DirectX HLSL-Textur Objekt)

Vergleicht eine Textur und vergleicht eine einzelne Komponente mit dem angegebenen Vergleichswert.

<table>
<tbody>
<tr class="odd">
<td>float-Objekt. samplecmp ( <dl> Samplercomparisonstate S,<br />
float-Speicherort<br />
float-CompareValue,<br />
[int Offset]<br />
</dl>);</td>
</tr>
</tbody>
</table>
 

Der Vergleich ist ein Einzelkomponenten Vergleich zwischen der ersten in der Textur gespeicherten Komponente und dem in der Methode übergebenen Vergleichswert.

Diese Methode kann nur von einem Pixelshader aufgerufen werden. Sie wird in einem Scheitelpunkt oder Geometry-Shader nicht unterstützt.

## <a name="parameters"></a>Parameter

<dl> <dt>

<span id="Object"></span><span id="object"></span><span id="OBJECT"></span>*Objekt*
</dt> <dd>

Ein beliebiger [Textur Objekttyp](dx-graphics-hlsl-to-type.md) (mit Ausnahme von Texture2DMS, Texture2DMSArray oder Texture3D).

</dd> <dt>

<span id="S"></span><span id="s"></span>*Hymnen*
</dt> <dd>

\[in \] einem Sampler-Vergleichs Zustand, bei dem es sich um den samplerzustand plus einen Vergleichs Zustand handelt (eine Vergleichsfunktion und ein Vergleichs Filter). Weitere Informationen und ein Beispiel finden Sie unter dem [Samplingtyp](dx-graphics-hlsl-sampler.md) .

</dd> <dt>

<span id="Location"></span><span id="location"></span><span id="LOCATION"></span>*Hotels*
</dt> <dd>

\[in \] den Texturkoordinaten. Der Argumenttyp ist vom Textur Objekttyp abhängig.

| Texture-Object-Typ          | Parametertyp |
|------------------------------|----------------|
| Texture1D                    | float          |
| Texture1DArray, Texture2D    | float2         |
| Texture2DArray ¹, texturecube | float3         |
| Texturecubearray ¹            | float4         |

</dd> <dt>

<span id="CompareValue"></span><span id="comparevalue"></span><span id="COMPAREVALUE"></span>*CompareValue*
</dt> <dd>

Ein Gleit Komma Wert, der als Vergleichswert verwendet werden soll.

</dd> <dt>

<span id="Offset"></span><span id="offset"></span><span id="OFFSET"></span>*Kompensieren*
</dt> <dd>

\[in \] einem optionalen Text der Textur Koordinate, der für jeden Textur Objekttyp verwendet werden kann. der Offset wird vor der Stichprobenentnahme auf den Speicherort angewendet. Die Textur Offsets müssen statisch sein. Der Argumenttyp ist vom Textur Objekttyp abhängig. Weitere Informationen finden Sie unter [Anwenden von Texturkoordinaten Offsets](dx-graphics-hlsl-to-sample.md).

| Texture-Object-Typ            | Parametertyp |
|--------------------------------|----------------|
| Texture1D, Texture1DArray      | INT            |
| Texture2D, Texture2DArray ¹     | int2           |
| Texturecube, texturecubearray ¹ | Nicht unterstützt  |

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Gibt einen Gleit Komma Wert im Bereich von \[ 0.. 1 zurück \] .

Bei jedem abgerufenen Texttyp (basierend auf der samplingkonfiguration des Filter Modus) führt **samplecmp** einen Vergleich des z-Werts (3rd-Komponente der Eingabe) vom Shader mit dem textexwert aus (1, wenn der Vergleich durchlaufen wird; andernfalls 0). **Samplecmp** kombiniert dann diese 0-und 1-Ergebnisse für alle Texttypen wie bei normaler Textur Filterung (kein Durchschnitt) und gibt den resultierenden \[ Wert 0.. 1 \] an den Shader zurück.

## <a name="remarks"></a>Bemerkungen

Durch die Vergleichs Filterung wird ein grundlegender Filter Vorgang bereitstellt, der für eine genauere (prozentuale) Filterung nützlich ist.

Wenn diese Methode für eine Gleit Komma Ressource verwendet wird (anstelle eines signierten oder nicht signierten normalisierten Formats), wird der Vergleichswert nicht automatisch zwischen 0,0 und 1,0 gebunden. Daher kann eine manuelle Klammer des Vergleichs Werts für gängige shadoingtechniken erforderlich sein.

Verwenden Sie einen Offset nur bei einer ganzzahligen miplevel. Andernfalls erhalten Sie abhängig von der Hardware Implementierung oder den Treibereinstellungen möglicherweise unterschiedliche Ergebnisse.

## <a name="minimum-shader-model"></a>Minimaler Shader-Modell

Diese Funktion wird in den folgenden shadermodellen unterstützt.

| vs \_ 4 \_ 0 | vs \_ 4 \_ 1 ² | PS \_ 4 \_ 0 | PS \_ 4 \_ 1 ² | GS \_ 4 \_ 0 | GS \_ 4 \_ 1 ² |
|----------|-----------|----------|-----------|----------|-----------|
|          |           | x ¹       | x         |          |           |

1.  Texture2DArray und texturecubearray sind im Shader-Modell 4,1 oder höher verfügbar.
2.  Das Shader-Modell 4,1 ist in Direct3D 10,1 oder höher verfügbar.

> [!NOTE]  
> **Samplecmp** ist auch in der PS 4 \_ 0 \_ \_ -Ebene 9 \_ 1 und 4 \_ 0 \_ Stufe \_ 9 3 verfügbar \_ , wenn Sie die Verfahren verwenden, die unter [Implementieren von Schatten Puffern für Direct3D Feature Level 9](/previous-versions/windows/apps/jj262110(v=win.10))beschrieben werden.

## <a name="related-topics"></a>Zugehörige Themen

[Texture-Objekt](dx-graphics-hlsl-to-type.md)
