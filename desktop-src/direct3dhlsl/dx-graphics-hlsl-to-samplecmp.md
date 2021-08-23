---
title: SampleCmp (DirectX HLSL-Texturobjekt)
description: Samples a texture and compares a single component against the specified comparison value. (Stichprobenentnahme für eine Textur und Vergleich einer einzelnen Komponente mit dem angegebenen Vergleichswert.
ms.assetid: e21894c4-e8c5-4c3d-92c1-727964f8fd94
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- apiref
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: a606ad9081f1ca1fdc4261d862ea6edfef4460989bb6d51d839d85f5797c1466
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119854640"
---
# <a name="samplecmp-directx-hlsl-texture-object"></a>SampleCmp (DirectX HLSL-Texturobjekt)

Samples a texture and compares a single component against the specified comparison value. (Stichprobenentnahme für eine Textur und Vergleich einer einzelnen Komponente mit dem angegebenen Vergleichswert.

<table>
<tbody>
<tr class="odd">
<td>float Object.SampleCmp( <dl> SamplerComparisonState S,<br />
float Location,<br />
float CompareValue,<br />
[int Offset]<br />
</dl>);</td>
</tr>
</tbody>
</table>
 

Der Vergleich ist ein Einzelkomponentenvergleich zwischen der ersten in der Textur gespeicherten Komponente und dem an die -Methode übergebenen Vergleichswert.

Diese Methode kann nur über einen Pixel-Shader aufgerufen werden. Wird in einem Scheitelpunkt- oder Geometrie-Shader nicht unterstützt.

## <a name="parameters"></a>Parameter

<dl> <dt>

<span id="Object"></span><span id="object"></span><span id="OBJECT"></span>*Objekt*
</dt> <dd>

Beliebiger [Texturobjekttyp](dx-graphics-hlsl-to-type.md) (außer Texture2DMS, Texture2DMSArray oder Texture3D).

</dd> <dt>

<span id="S"></span><span id="s"></span>*S*
</dt> <dd>

\[in einem Samplervergleichszustand, bei dem es sich um den Samplerzustand plus einen Vergleichszustand \] (eine Vergleichsfunktion und einen Vergleichsfilter) handelt. Details und ein Beispiel finden Sie unter [Samplertyp.](dx-graphics-hlsl-sampler.md)

</dd> <dt>

<span id="Location"></span><span id="location"></span><span id="LOCATION"></span>*Lage*
</dt> <dd>

\[in \] Die Texturkoordinaten. Der Argumenttyp ist vom Texturobjekttyp abhängig.

| Texture-Object Typ          | Parametertyp |
|------------------------------|----------------|
| Texture1D                    | float          |
| Texture1DArray, Texture2D    | float2         |
| Texture2DArray, TextureCube | float3         |
| TextureCubeArray            | float4         |

</dd> <dt>

<span id="CompareValue"></span><span id="comparevalue"></span><span id="COMPAREVALUE"></span>*CompareValue*
</dt> <dd>

Ein Gleitkommawert, der als Vergleichswert verwendet werden soll.

</dd> <dt>

<span id="Offset"></span><span id="offset"></span><span id="OFFSET"></span>*Offset*
</dt> <dd>

\[in \] Ein optionaler Texturkoordinatenoffset, der für jeden Texturobjekttyp verwendet werden kann. Der Offset wird vor der Stichprobenentnahme auf die Position angewendet. Die Texturoffsets müssen statisch sein. Der Argumenttyp ist vom Texturobjekttyp abhängig. Weitere Informationen finden Sie unter [Anwenden von Texturkoordinatenoffsets.](dx-graphics-hlsl-to-sample.md)

| Texture-Object Typ            | Parametertyp |
|--------------------------------|----------------|
| Texture1D, Texture1DArray      | INT            |
| Texture2D, Texture2DArray     | int2           |
| TextureCube, TextureCubeArray | Nicht unterstützt  |

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Gibt einen Gleitkommawert im Bereich \[ 0..1 \] zurück.

Für jedes abgerufene Texel (basierend auf der Samplerkonfiguration des Filtermodus) führt **SampleCmp** einen Vergleich des z-Werts (3. Komponente der Eingabe) aus dem Shader mit dem Texelwert durch (1, wenn der Vergleich besteht, andernfalls 0). **SampleCmp** kombiniert dann diese 0- und 1-Ergebnisse für jedes Texel wie bei der normalen Texturfilterung (kein Durchschnitt) und gibt den resultierenden \[ 0,1-Wert an den \] Shader zurück.

## <a name="remarks"></a>Hinweise

Die Vergleichsfilterung bietet einen grundlegenden Filtervorgang, der für die Filterung mit geringerer Tiefe in Prozent nützlich ist.

Bei Verwendung dieser Methode für eine Gleitkommaressource (anstelle eines mit Vorzeichen normalisierten oder unsignierten normalisierten Formats) wird der Vergleichswert nicht automatisch zwischen 0,0 und 1,0 geklammert. Daher kann eine manuelle Klammer des Vergleichswerts für gängige Schattentechniken erforderlich sein.

Verwenden Sie einen Offset nur bei einer ganzzahligen MIP-Ebene. Andernfalls erhalten Sie je nach Hardwareimplementierung oder Treibereinstellungen möglicherweise unterschiedliche Ergebnisse.

## <a name="minimum-shader-model"></a>Minimales Shadermodell

Diese Funktion wird in den folgenden Shadermodellen unterstützt.

| vs \_ 4 \_ 0 | vs \_ 4 \_ 1% | ps \_ 4 \_ 0 | ps \_ 4 \_ 1). | gs \_ 4 \_ 0 | gs \_ 4 \_ 1² |
|----------|-----------|----------|-----------|----------|-----------|
|          |           | x.       | x         |          |           |

1.  Texture2DArray und TextureCubeArray sind in Shader Model 4.1 oder höher verfügbar.
2.  ShaderModell 4.1 ist in Direct3D 10.1 oder höher verfügbar.

> [!NOTE]  
> **SampleCmp** ist auch in ps 4 \_ 0 \_ Level 9 1 und \_ \_ 4 0 level 9 3 verfügbar, wenn Sie die Techniken verwenden, die unter Implementieren von Schattenpuffern für \_ \_ \_ \_ [Direct3D-Featureebene 9](/previous-versions/windows/apps/jj262110(v=win.10))beschrieben sind.

## <a name="related-topics"></a>Zugehörige Themen

[Texture-Object](dx-graphics-hlsl-to-type.md)
