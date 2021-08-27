---
title: CalculateLevelOfDetail (DirectX HLSL-Texturobjekt)
description: Berechnet die Detailebene.
ms.assetid: 7c7c3754-45a9-49c6-8420-aac22f776b15
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- apiref
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 44d71469cf5fd3246a0bb038cf369227cb3a3017
ms.sourcegitcommit: c276a8912787b2cda74dcf54eb96df961bb1188b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2021
ms.locfileid: "122625826"
---
# <a name="calculatelevelofdetail-directx-hlsl-texture-object"></a>CalculateLevelOfDetail (DirectX HLSL-Texturobjekt)

Berechnet die Detailebene.

ret Object.CalculateLevelOfDetail( sampler \_ state S, float x );



 

## <a name="parameters"></a>Parameter



<table>
<colgroup>
<col  />
<col  />
</colgroup>
<thead>
<tr class="header">
<th>Element</th>
<th>Beschreibung</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span id="Object"></span><span id="object"></span><span id="OBJECT"></span><em>Objekt</em><br/></td>
<td>Jeder <a href="dx-graphics-hlsl-to-type.md">Texturobjekttyp</a> (mit Ausnahme von Texture2DMS und Texture2DMSArray).<br/></td>
</tr>
<tr class="even">
<td><span id="S"></span><span id="s"></span><em>S</em><br/></td>
<td>[in] Ein <a href="/windows/desktop/direct3d10/d3d10-effect-sampler-syntax">Samplerzustand.</a> Dies ist ein Objekt, das in einer Effektdatei deklariert ist, die Zustandszuweisungen enthält.<br/></td>
</tr>
<tr class="odd">
<td><span id="x"></span><span id="X"></span><em>X</em><br/></td>
<td>[in] Der lineare Interpolationswert oder -werte, bei dem es sich um eine Gleitkommazahl zwischen 0,0 und einschließlich 1,0 handelt. Die Anzahl der Komponenten hängt vom Texturobjekttyp ab. <br/> 
<table>
<thead>
<tr class="header">
<th>Texture-Object-Typ</th>
<th>Parametertyp</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>Texture1D, Texture1DArray</td>
<td>float1</td>
</tr>
<tr class="even">
<td>Texture2D, Texture2DArray</td>
<td>float2</td>
</tr>
<tr class="odd">
<td>Texture3D, TextureCube, TextureCubeArray </td>
<td>float3</td>
</tr>
</tbody>
</table>

<p> </p></td>
</tr>
</tbody>
</table>



 

## <a name="return-value"></a>Rückgabewert

Gibt die berechnete LOD zurück, einen einzelnen Gleitkommawert.

## <a name="minimum-shader-model"></a>Shader-Mindestmodell

Diese Funktion wird in den folgenden Shadermodellen unterstützt.



| Vs \_ 4 \_ 0 | Vs \_ 4 \_ 1  | ps \_ 4 \_ 0 | ps \_ 4 \_ 1  | gs \_ 4 \_ 0 | gs \_ 4 \_ 1  |
|----------|-----------|----------|-----------|----------|-----------|
|          |           |          | x         |          |           |



 

1.  TextureCubeArray ist im Shadermodell 4.1 oder höher verfügbar.
2.  Shadermodell 4.1 ist in Direct3D 10.1 oder höher verfügbar.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Texturobjekt](dx-graphics-hlsl-to-type.md)
</dt> </dl>

 

