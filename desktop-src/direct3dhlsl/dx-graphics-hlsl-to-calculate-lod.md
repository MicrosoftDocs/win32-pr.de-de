---
title: Calculatelevelof Detail (DirectX HLSL Texture-Objekt)
description: Berechnet den Detailgrad.
ms.assetid: 7c7c3754-45a9-49c6-8420-aac22f776b15
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- apiref
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: c59b8da97ff1cbe0bd88d6a49120a0a040cf3c30
ms.sourcegitcommit: ae73f4dd3cf5a3c6a1ea7d191ca32a5b01f6686b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/08/2020
ms.locfileid: "104976864"
---
# <a name="calculatelevelofdetail-directx-hlsl-texture-object"></a>Calculatelevelof Detail (DirectX HLSL Texture-Objekt)

Berechnet den Detailgrad.



|                                                                 |
|-----------------------------------------------------------------|
| Ret Object. calculatelevelof Detail (Sampler \_ State S, float x); |



 

## <a name="parameters"></a>Parameter



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th>Element</th>
<th>BESCHREIBUNG</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span id="Object"></span><span id="object"></span><span id="OBJECT"></span><em>Objekt</em><br/></td>
<td>Ein beliebiger <a href="dx-graphics-hlsl-to-type.md">Textur Objekttyp</a> (mit Ausnahme von Texture2DMS und Texture2DMSArray).<br/></td>
</tr>
<tr class="even">
<td><span id="S"></span><span id="s"></span><em>Hymnen</em><br/></td>
<td>in Ein <a href="/windows/desktop/direct3d10/d3d10-effect-sampler-syntax">samplerzustand</a>. Dies ist ein Objekt, das in einer Effekt Datei deklariert wurde, die Zustands Zuweisungen enthält.<br/></td>
</tr>
<tr class="odd">
<td><span id="x"></span><span id="X"></span><em>Stuben</em><br/></td>
<td>in Der lineare Interpolations Wert oder die Werte, bei dem es sich um eine Gleit Komma Zahl zwischen 0,0 und 1,0 handelt. Die Anzahl der Komponenten ist vom Textur Objekttyp abhängig. <br/> 
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
<td>Texture3D, texturecube, texturecubearray </td>
<td>float3</td>
</tr>
</tbody>
</table>

<p> </p></td>
</tr>
</tbody>
</table>



 

## <a name="return-value"></a>Rückgabewert

Gibt die berechnete Lod zurück, einen einzelnen Gleit Komma Wert.

## <a name="minimum-shader-model"></a>Minimaler Shader-Modell

Diese Funktion wird in den folgenden shadermodellen unterstützt.



| vs \_ 4 \_ 0 | vs \_ 4 \_ 1  | PS \_ 4 \_ 0 | PS \_ 4 \_ 1  | GS \_ 4 \_ 0 | GS \_ 4 \_ 1  |
|----------|-----------|----------|-----------|----------|-----------|
|          |           |          | x         |          |           |



 

1.  Texturecubearray ist im Shader-Modell 4,1 oder höher verfügbar.
2.  Das Shader-Modell 4,1 ist in Direct3D 10,1 oder höher verfügbar.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Texture-Objekt](dx-graphics-hlsl-to-type.md)
</dt> </dl>

 

