---
title: Angeben von compilerzielen
description: Hier werden die Ziele für verschiedene Profile aufgelistet, die von den D3DCompile \-Funktionen und vom HLSL-Compiler unterstützt werden.
ms.assetid: 594E1C14-C1D4-4207-91A1-28892CE6D821
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d68fc6c5a202ad537b02a20846d36526533240f3
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "104390952"
---
# <a name="specifying-compiler-targets"></a>Angeben von compilerzielen

Sie müssen den Shader-Ziel – Satz von Shader-Funktionen – angeben, die beim Aufrufen der Funktion [**D3DCompile**](/windows/win32/api/d3dcompiler/nf-d3dcompiler-d3dcompile), [**D3DCompile2**](/windows/win32/api/d3dcompiler/nf-d3dcompiler-d3dcompile2)oder [**D3DCompileFromFile**](/windows/win32/api/d3dcompiler/nf-d3dcompiler-d3dcompilefromfile) kompiliert werden sollen. Hier werden die Ziele für verschiedene Profile aufgelistet, die von den **D3DCompile \*** -Funktionen und dem HLSL-Compiler unterstützt werden.

-   [Direct3D 11,0-und 11,1-Funktionsebenen](#direct3d-110-and-111-feature-levels)
-   [Direct3D 10,1-Funktionsebene](#direct3d-101-feature-level)
-   [Direct3D 10,0-Funktionsebene](#direct3d-100-feature-level)
-   [Direct3D-featureebenen der 9,1, 9,2 und 9,3](#direct3d-91-92-and-93-feature-levels)
-   [Legacy Direct3D 9-Shader-Modell 3,0](#legacy-direct3d-9-shader-model-30)
-   [Legacy Direct3D 9-Shader-Modell 2,0](#legacy-direct3d-9-shader-model-20)
-   [Legacy Direct3D 9-Shader-Modell 1. x](#legacy-direct3d-9-shader-model-1x)
-   [Ältere Effekte](#legacy-effects)
-   [Hinweise](#notes)
-   [Zugehörige Themen](#related-topics)

## <a name="direct3d-110-and-111-feature-levels"></a>Direct3D 11,0-und 11,1-Funktionsebenen

Im folgenden sind die Shader-Ziele aufgeführt, die von 11,1 11,0 [Direct3D unterstützt](/windows/desktop/direct3d11/overviews-direct3d-11-devices-downlevel-intro) werden.



| Target   | Beschreibung                                                                                                              |
|----------|--------------------------------------------------------------------------------------------------------------------------|
| CS \_ 5 \_ 0 | DirectCompute 5,0 ([Compute-Shader](/windows/desktop/direct3d11/direct3d-11-advanced-stages-compute-shader))                              |
| DS \_ 5 \_ 0 | [Domänen-Shader](/windows/desktop/direct3d11/direct3d-11-advanced-stages-tessellation)             |
| GS \_ 5 \_ 0 | [Geometry-Shader](/previous-versions//bb205146(v=vs.85)) |
| HS \_ 5 \_ 0 | [Rumpf-Shader](/windows/desktop/direct3d11/direct3d-11-advanced-stages-tessellation)                   |
| PS \_ 5 \_ 0 | [Pixel-Shader](/previous-versions//bb205146(v=vs.85))          |
| vs \_ 5 \_ 0 | [Vertex-Shader](/previous-versions//bb205146(v=vs.85))       |



 

## <a name="direct3d-101-feature-level"></a>Direct3D 10,1-Funktionsebene

Dies sind die shaderziele, die von der Direct3D 10,1- [Featureebene](/windows/desktop/direct3d11/overviews-direct3d-11-devices-downlevel-intro) unterstützt werden.



| Target   | Beschreibung                                                                                                              |
|----------|--------------------------------------------------------------------------------------------------------------------------|
| CS \_ 4 \_ 1 | DirectCompute 4,1 ([Compute-Shader](/windows/desktop/direct3d11/direct3d-11-advanced-stages-compute-shader)) ¹                             |
| GS \_ 4 \_ 1 | [Geometry-Shader](/previous-versions//bb205146(v=vs.85)) |
| PS \_ 4 \_ 1 | [Pixel-Shader](/previous-versions//bb205146(v=vs.85))          |
| vs \_ 4 \_ 1 | [Vertex-Shader](/previous-versions//bb205146(v=vs.85))       |



 

## <a name="direct3d-100-feature-level"></a>Direct3D 10,0-Funktionsebene

Dies sind die shaderziele, die von der Direct3D 10,0- [Featureebene](/windows/desktop/direct3d11/overviews-direct3d-11-devices-downlevel-intro) unterstützt werden.



| Target   | Beschreibung                                                                                                              |
|----------|--------------------------------------------------------------------------------------------------------------------------|
| CS \_ 4 \_ 0 | DirectCompute 4,0 ([Compute-Shader](/windows/desktop/direct3d11/direct3d-11-advanced-stages-compute-shader)) ¹                             |
| GS \_ 4 \_ 0 | [Geometry-Shader](/previous-versions//bb205146(v=vs.85)) |
| PS \_ 4 \_ 0 | [Pixel-Shader](/previous-versions//bb205146(v=vs.85))          |
| vs \_ 4 \_ 0 | [Vertex-Shader](/previous-versions//bb205146(v=vs.85))       |



 

## <a name="direct3d-91-92-and-93-feature-levels"></a>Direct3D-featureebenen der 9,1, 9,2 und 9,3

Im folgenden sind die Shader-Ziele aufgeführt, die die [Funktionsebenen](/windows/desktop/direct3d11/overviews-direct3d-11-devices-downlevel-intro) Direct3D 9,1, 9,2 und 9,3 unterstützen.

> [!Note]  
> Wenn Sie die \* \_ \_ HLSL-Shader-Profile der 4 0- \_ Ebene \_ 9 \_ x verwenden, verwenden Sie implizit die [Shader Model 2. x](dx-graphics-hlsl-sm2.md) -Profile zur Unterstützung von Direct3D 9-fähiger Hardware. Shader Model 2. x-Profile unterstützen ein eingeschränktes Verhalten der Fluss Steuerung als das [Shader-Modell 4. x](dx-graphics-hlsl-sm4.md) und spätere Profile.

 



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th>Target</th>
<th>Beschreibung</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>ps_4_0_level_9_1</td>
<td>[Pixelshader](/previous-versions//bb205146(v=vs.85)) für 9,1 und 9,2 (ähnliche Grenzwerte wie PS_2_0)
<ul>
<li>64 arithmetische und 32 Textur Anweisungen</li>
<li>12 temporäre Register</li>
<li>4 Ebenen von abhängigen Lesevorgängen</li>
</ul></td>
</tr>
<tr class="even">
<td>ps_4_0_level_9_3</td>
<td><a href="/previous-versions//bb205146(v=vs.85)">Pixel-Shader</a> für 9,3 (ähnliche Grenzwerte für ps_2_x ² mit zusätzlichen shaderfeatures)
<ul>
<li>512-Anweisungen</li>
<li>32 temporäre Register</li>
<li>Statische Fluss Steuerung (maximale Tiefe von 4)</li>
<li>Dynamische Fluss Steuerung (maximale Tiefe von 24)</li>
<li>D3DPS20CAPS_ARBITRARYSWIZZLE</li>
<li>D3DPS20CAPS_GRADIENTINSTRUCTIONS</li>
<li>D3DPS20CAPS_PREDICATION</li>
<li>D3DPS20CAPS_NODEPENDENTREADLIMIT</li>
<li>D3DPS20CAPS_NOTEXINSTRUCTIONLIMIT</li>
</ul></td>
</tr>
<tr class="odd">
<td>vs_4_0_level_9_1</td>
<td><a href="/previous-versions//bb205146(v=vs.85)">Vertex-Shader</a> für 9,1 und 9,2 (ähnlich wie VS_2_0)
<ul>
<li>256-Anweisungen</li>
<li>12 temporäre Register</li>
<li>Statische Fluss Steuerung (maximale Tiefe von 1)</li>
</ul></td>
</tr>
<tr class="even">
<td>vs_4_0_level_9_3</td>
<td><a href="/previous-versions//bb205146(v=vs.85)">Vertex-Shader</a> für 9,3 (ähnlich wie vs_2_a ² mit zusätzlichen shaderfeatures und Instanziierung)
<ul>
<li>256-Anweisungen</li>
<li>32 temporäre Register</li>
<li>Statische Fluss Steuerung (maximale Tiefe von 4)</li>
<li>D3DVS20CAPS_PREDICATION</li>
</ul></td>
</tr>
</tbody>
</table>



 

## <a name="legacy-direct3d-9-shader-model-30"></a>Legacy Direct3D 9-Shader-Modell 3,0

Im folgenden finden Sie die Shader-Ziele für das Legacy-Direct3D 9-Shader-Modell 3,0 ³.



| Target    | Beschreibung                                                                                                                       |
|-----------|-----------------------------------------------------------------------------------------------------------------------------------|
| PS \_ 3 \_ 0  | [Pixel-Shader](/previous-versions//bb205146(v=vs.85)) 3,0               |
| PS \_ 3 ( \_ SW) | [Pixelshader](/previous-versions//bb205146(v=vs.85)) 3,0 (Software)    |
| vs \_ 3 \_ 0  | [Vertex-Shader](/previous-versions//bb205146(v=vs.85)) 3,0            |
| vs \_ 3- \_ SW | [Vertex-Shader](/previous-versions//bb205146(v=vs.85)) 3,0 (Software) |



 

## <a name="legacy-direct3d-9-shader-model-20"></a>Legacy Direct3D 9-Shader-Modell 2,0

Im folgenden finden Sie die Shader-Ziele für das Legacy-Direct3D 9-Shader-Modell 2,0 ³.



| Target    | Beschreibung                                                                                                                     |
|-----------|---------------------------------------------------------------------------------------------------------------------------------|
| PS \_ 2 \_ 0  | [Pixel-Shader](/previous-versions//bb205146(v=vs.85)) 2,0             |
| PS \_ 2 \_ a  | [Pixel-Shader](/previous-versions//bb205146(v=vs.85)) 2a              |
| PS \_ 2 \_ b  | [Pixel-Shader](/previous-versions//bb205146(v=vs.85)) 2B              |
| PS \_ 2 \_ SW | [Pixel-Shader](/previous-versions//bb205146(v=vs.85)) 2,0-Software    |
| vs \_ 2 \_ 0  | [Vertex-Shader](/previous-versions//bb205146(v=vs.85)) 2,0          |
| vs \_ 2 \_ a  | [Vertex-Shader](/previous-versions//bb205146(v=vs.85)) 2a           |
| vs \_ 2 \_ SW | [Vertex-Shader](/previous-versions//bb205146(v=vs.85)) 2,0-Software |



 

## <a name="legacy-direct3d-9-shader-model-1x"></a>Legacy Direct3D 9-Shader-Modell 1. x

Im folgenden sind die Shader-Ziele für das Legacy Direct3D 9-Shader-Modell 1. x ⁴ aufgeführt.



| Target   | Beschreibung                                                                                                                                                                       |
|----------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| TX \_ 1 \_ 0 | Textur-Shader-Profil, das Legacy D3DX9 ⁵ Functions [**D3DXCreateTextureShader**](/windows/desktop/direct3d9/d3dxcreatetextureshader) und [**D3DXFillTextureTX**](/windows/desktop/direct3d9/d3dxfilltexturetx) verwenden |
| vs \_ 1 \_ 1 | [Vertex-Shader](/previous-versions//bb205146(v=vs.85)) 1,1                                                            |



 

## <a name="legacy-effects"></a>Ältere Effekte

Im folgenden finden Sie die Wirkungs Ziele für ältere Effekte.



| Target   | Beschreibung                               |
|----------|-------------------------------------------|
| FX \_ 2 \_ 0 | Effekte (FX) für Direct3D 9 in D3DX9 ⁵     |
| FX \_ 4 \_ 0 | Effekte (FX) für Direct3D 10,0 in d3dx10 ⁵ |
| FX \_ 4 \_ 1 | Effekte (FX) für Direct3D 10,1 in d3dx10 ⁵ |
| FX \_ 5 \_ 0 | Effekte (FX) für Direct3D 11 ⁵             |



 

## <a name="notes"></a>Notizen

Im folgenden finden Sie einige Hinweise, die in den vorherigen Abschnitten beschrieben werden:

1.  auf [Featureebene](/windows/desktop/direct3d11/overviews-direct3d-11-devices-downlevel-intro) 10,0-und 10,1-Geräten kann DirectCompute optional unterstützt werden. Um die Unterstützung zu überprüfen, verwenden Sie [**ID3D11Device:: checkfeaturesupport**](/windows/desktop/api/d3d11/nf-d3d11-id3d11device-checkfeaturesupport) mit [**D3D11 \_ Feature \_ d3d10 \_ X \_ Hardware \_ options**](/windows/desktop/api/d3d11/ne-d3d11-d3d11_feature).
2.  auf [Featureebene](/windows/desktop/direct3d11/overviews-direct3d-11-devices-downlevel-intro) 9,3 ist eine Hardware erforderlich, die den Anforderungen für das [Legacy-Direct3D 9-Shader-Modell 3,0](#legacy-direct3d-9-shader-model-30)entspricht. diese Featureebene verwendet jedoch keine vs \_ 3 0- \_ oder PS \_ 3 0- \_ Ziele.
3.  Verwenden Sie nur Legacy-Direct3D 9-Shader-Modelle mit der Direct3D 9-API. Verwenden Sie stattdessen die 9. x-Profile mit der API Direct3D 10. x und 11. x.
4.  Die aktuellen HLSL-Shader- **D3DCompile \*** -Funktionen unterstützen keine Legacy-1. x-Pixel-Shader. Die letzte Version von HLSL zur Unterstützung dieser Ziele war D3DX9 in der Version vom Oktober 2006 des DirectX SDK.
5.  Alle Versionen von D3DX und DirectX SDK sind veraltet. Weitere Informationen finden Sie unter [wo ist das DirectX SDK?](/windows/desktop/directx-sdk--august-2009-).

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Programmieranleitung für HLSL](dx-graphics-hlsl-pguide.md)
</dt> </dl>

 

 