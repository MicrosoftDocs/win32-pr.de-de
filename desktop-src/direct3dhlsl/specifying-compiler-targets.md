---
title: Angeben von Compilerzielen
description: Hier werden die Ziele für verschiedene Profile aufgeführt, die die D3DCompile\-Funktion und der HLSL-Compiler unterstützen.
ms.assetid: 594E1C14-C1D4-4207-91A1-28892CE6D821
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b84d020edaabf4c618b1fa911a91bc4cc0e8b37e
ms.sourcegitcommit: 9b5faa61c38b2d0c432b7f2dbee8c127b0e28a7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/19/2021
ms.locfileid: "122481836"
---
# <a name="specifying-compiler-targets"></a>Angeben von Compilerzielen

Sie müssen das Shaderziel angeben – eine Reihe von Shaderfeatures – für die Kompilierung, wenn Sie die [**D3DCompile-,**](/windows/win32/api/d3dcompiler/nf-d3dcompiler-d3dcompile) [**D3DCompile2-**](/windows/win32/api/d3dcompiler/nf-d3dcompiler-d3dcompile2)oder [**D3DCompileFromFile-Funktion**](/windows/win32/api/d3dcompiler/nf-d3dcompiler-d3dcompilefromfile) aufrufen. Hier werden die Ziele für verschiedene Profile aufgeführt, die von den **\* D3DCompile-Funktionen** und dem HLSL-Compiler unterstützt werden.

-   [Direct3D 11.0- und 11.1-Featureebenen](#direct3d-110-and-111-feature-levels)
-   [Direct3D 10.1-Featureebene](#direct3d-101-feature-level)
-   [Direct3D 10.0-Featureebene](#direct3d-100-feature-level)
-   [Direct3D-Featureebenen 9.1, 9.2 und 9.3](#direct3d-91-92-and-93-feature-levels)
-   [Legacy Direct3D 9 Shader Model 3.0](#legacy-direct3d-9-shader-model-30)
-   [Legacy Direct3D 9 Shader Model 2.0](#legacy-direct3d-9-shader-model-20)
-   [Legacy Direct3D 9 Shader Model 1.x](#legacy-direct3d-9-shader-model-1x)
-   [Legacyeffekte](#legacy-effects)
-   [Notizen](#notes)
-   [Zugehörige Themen](#related-topics)

## <a name="direct3d-110-and-111-feature-levels"></a>Direct3D 11.0- und 11.1-Featureebenen

Hier sind die Shaderziele, die die [Featureebenen](/windows/desktop/direct3d11/overviews-direct3d-11-devices-downlevel-intro) Direct3D 11.0 und 11.1 unterstützen.



| Target   | Beschreibung                                                                                                              |
|----------|--------------------------------------------------------------------------------------------------------------------------|
| CS \_ 5 \_ 0 | DirectCompute 5.0 ([Compute-Shader](/windows/desktop/direct3d11/direct3d-11-advanced-stages-compute-shader))                              |
| ds \_ 5 \_ 0 | [Domänen-Shader](/windows/desktop/direct3d11/direct3d-11-advanced-stages-tessellation)             |
| gs \_ 5 \_ 0 | [Geometry-Shader](/previous-versions//bb205146(v=vs.85)) |
| hs \_ 5 \_ 0 | [Hüllen-Shader](/windows/desktop/direct3d11/direct3d-11-advanced-stages-tessellation)                   |
| ps \_ 5 \_ 0 | [Pixel-Shader](/previous-versions//bb205146(v=vs.85))          |
| Vs \_ 5 \_ 0 | [Vertex-Shader](/previous-versions//bb205146(v=vs.85))       |



 

## <a name="direct3d-101-feature-level"></a>Direct3D 10.1-Featureebene

Hier sind die Shaderziele, die die Direct3D 10.1-Featureebene unterstützt. [](/windows/desktop/direct3d11/overviews-direct3d-11-devices-downlevel-intro)



| Target   | Beschreibung                                                                                                              |
|----------|--------------------------------------------------------------------------------------------------------------------------|
| CS \_ 4 \_ 1 | DirectCompute 4.1 ([Compute-Shader](/windows/desktop/direct3d11/direct3d-11-advanced-stages-compute-shader))¹                             |
| gs \_ 4 \_ 1 | [Geometry-Shader](/previous-versions//bb205146(v=vs.85)) |
| ps \_ 4 \_ 1 | [Pixel-Shader](/previous-versions//bb205146(v=vs.85))          |
| Vs \_ 4 \_ 1 | [Vertex-Shader](/previous-versions//bb205146(v=vs.85))       |



 

## <a name="direct3d-100-feature-level"></a>Direct3D 10.0-Featureebene

Hier sind die Shaderziele, die die Direct3D 10.0-Featureebene unterstützt. [](/windows/desktop/direct3d11/overviews-direct3d-11-devices-downlevel-intro)



| Target   | Beschreibung                                                                                                              |
|----------|--------------------------------------------------------------------------------------------------------------------------|
| cs \_ 4 \_ 0 | DirectCompute 4.0 ([Compute-Shader](/windows/desktop/direct3d11/direct3d-11-advanced-stages-compute-shader))¹                             |
| gs \_ 4 \_ 0 | [Geometry-Shader](/previous-versions//bb205146(v=vs.85)) |
| ps \_ 4 \_ 0 | [Pixel-Shader](/previous-versions//bb205146(v=vs.85))          |
| Vs \_ 4 \_ 0 | [Vertex-Shader](/previous-versions//bb205146(v=vs.85))       |



 

## <a name="direct3d-91-92-and-93-feature-levels"></a>Direct3D-Featureebenen 9.1, 9.2 und 9.3

Hier sind die Shaderziele, die die [Featureebenen](/windows/desktop/direct3d11/overviews-direct3d-11-devices-downlevel-intro) Direct3D 9.1, 9.2 und 9.3 unterstützen.

> [!Note]  
> Wenn Sie die \* \_ \_ 4 0 \_ Level \_ 9 \_ x HLSL-Shaderprofile verwenden, verwenden Sie implizit die [Shadermodell 2.x-Profile,](dx-graphics-hlsl-sm2.md) um Direct3D 9-fähige Hardware zu unterstützen. Shadermodell 2.x-Profile unterstützen ein eingeschränkteres Flusssteuerungsverhalten als die Profile des [Shadermodells 4.x](dx-graphics-hlsl-sm4.md) und höher.

 




| Target | Beschreibung | 
|--------|-------------|
| ps_4_0_level_9_1 | [Pixelshader](/previous-versions//bb205146(v=vs.85)) für 9.1 und 9.2 (ähnliche Grenzwerte wie ps_2_0)<ul><li>64 arithmetische und 32 Texturanweisungen</li><li>12 temporäre Register</li><li>4 Ebenen abhängiger Lesefunktionen</li></ul> | 
| ps_4_0_level_9_3 | <a href="/previous-versions//bb205146(v=vs.85)">Pixel-Shader</a> für 9.3 (ähnliche Grenzwerte wie ps_2_x limits mit zusätzlichen Shaderfeatures)<ul><li>512 Anweisungen</li><li>32 temporäre Register</li><li>Statische Flusssteuerung (maximale Tiefe von 4)</li><li>Dynamische Flusssteuerung (maximale Tiefe von 24)</li><li>D3DPS20CAPS_ARBITRARYSWIZZLE</li><li>D3DPS20CAPS_GRADIENTINSTRUCTIONS</li><li>D3DPS20CAPS_PREDICATION</li><li>D3DPS20CAPS_NODEPENDENTREADLIMIT</li><li>D3DPS20CAPS_NOTEXINSTRUCTIONLIMIT</li></ul> | 
| vs_4_0_level_9_1 | <a href="/previous-versions//bb205146(v=vs.85)">Vertex-Shader</a> für 9.1 und 9.2 (ähnlich wie vs_2_0)<ul><li>256 Anweisungen</li><li>12 temporäre Register</li><li>Statische Flusssteuerung (maximale Tiefe von 1)</li></ul> | 
| vs_4_0_level_9_3 | <a href="/previous-versions//bb205146(v=vs.85)">Vertex-Shader</a> für 9.3 (ähnlich wie vs_2_a² mit zusätzlichen Shaderfunktionen und Instanziierung)<ul><li>256 Anweisungen</li><li>32 temporäre Register</li><li>Statische Flusssteuerung (maximale Tiefe von 4)</li><li>D3DVS20CAPS_PREDICATION</li></ul> | 




 

## <a name="legacy-direct3d-9-shader-model-30"></a>Legacy Direct3D 9 Shader Model 3.0

Hier sind die Shaderziele für das Legacy-Direct3D 9-Shadermodell 3.0werte.



| Target    | Beschreibung                                                                                                                       |
|-----------|-----------------------------------------------------------------------------------------------------------------------------------|
| ps \_ 3 \_ 0  | [Pixelshader](/previous-versions//bb205146(v=vs.85)) 3.0               |
| ps \_ 3 \_ sw | [Pixelshader](/previous-versions//bb205146(v=vs.85)) 3.0 (Software)    |
| Vs \_ 3 \_ 0  | [Vertex-Shader](/previous-versions//bb205146(v=vs.85)) 3.0            |
| vs \_ 3 \_ sw | [Vertex-Shader](/previous-versions//bb205146(v=vs.85)) 3.0 (Software) |



 

## <a name="legacy-direct3d-9-shader-model-20"></a>Legacy Direct3D 9 Shader Model 2.0

Hier sind die Shaderziele für das Legacy-Direct3D 9-Shadermodell 2.0werte.



| Target    | Beschreibung                                                                                                                     |
|-----------|---------------------------------------------------------------------------------------------------------------------------------|
| ps \_ 2 \_ 0  | [Pixelshader](/previous-versions//bb205146(v=vs.85)) 2.0             |
| ps \_ 2 \_ a  | [Pixelshader](/previous-versions//bb205146(v=vs.85)) 2a              |
| ps \_ 2 \_ b  | [Pixelshader](/previous-versions//bb205146(v=vs.85)) 2b              |
| ps \_ 2 \_ sw | [Pixelshader](/previous-versions//bb205146(v=vs.85)) 2.0-Software    |
| Vs \_ 2 \_ 0  | [Vertex-Shader](/previous-versions//bb205146(v=vs.85)) 2.0          |
| vs \_ 2 \_ a  | [Vertex-Shader](/previous-versions//bb205146(v=vs.85)) 2a           |
| vs \_ 2 \_ sw | [Vertex-Shader](/previous-versions//bb205146(v=vs.85)) 2.0-Software |



 

## <a name="legacy-direct3d-9-shader-model-1x"></a>Legacy Direct3D 9 Shader Model 1.x

Hier sind die Shaderziele für das Legacy-Direct3D 9-Shadermodell 1.x⁴.



| Target   | Beschreibung                                                                                                                                                                       |
|----------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| tx \_ 1 \_ 0 | Texturshaderprofil, das von den Legacyfunktionen D3DX9⁵ [**D3DXCreateTextureShader**](/windows/desktop/direct3d9/d3dxcreatetextureshader) und [**D3DXFillTextureTX**](/windows/desktop/direct3d9/d3dxfilltexturetx) verwendet wird |
| Vs \_ 1 \_ 1 | [Vertex-Shader](/previous-versions//bb205146(v=vs.85)) 1.1                                                            |



 

## <a name="legacy-effects"></a>Legacyeffekte

Hier sind die Auswirkungsziele für Legacyeffekte.



| Target   | Beschreibung                               |
|----------|-------------------------------------------|
| fx \_ 2 \_ 0 | Effekte (FX) für Direct3D 9 in D3DX9⁵     |
| fx \_ 4 \_ 0 | Effekte (FX) für Direct3D 10.0 in D3DX10⁵ |
| fx \_ 4 \_ 1 | Effekte (FX) für Direct3D 10.1 in D3DX10⁵ |
| fx \_ 5 \_ 0 | Effekte (FX) für Direct3D 11⁵             |



 

## <a name="notes"></a>Hinweise

Im Folgenden finden Sie einige Hinweise, auf die sich die vorherigen Abschnitte beziehen:

1.  [Geräte der Featureebene](/windows/desktop/direct3d11/overviews-direct3d-11-devices-downlevel-intro) 10.0 und 10.1 können DirectCompute optional unterstützen. Um die Unterstützung zu überprüfen, verwenden Sie [**ID3D11Device::CheckFeatureSupport**](/windows/desktop/api/d3d11/nf-d3d11-id3d11device-checkfeaturesupport) with [**D3D11 \_ FEATURE \_ D3D10 \_ X HARDWARE \_ \_ OPTIONS**](/windows/desktop/api/d3d11/ne-d3d11-d3d11_feature).
2.  [Featureebene](/windows/desktop/direct3d11/overviews-direct3d-11-devices-downlevel-intro) 9.3 erfordert effektiv Hardware, die den Anforderungen für das [Ältere Direct3D 9-Shadermodell 3.0](#legacy-direct3d-9-shader-model-30)entspricht, aber diese Featureebene nutzt keine Ziele von \_ 3 \_ 0 oder PS \_ 3 \_ 0.
3.  Verwenden Sie nur ältere Direct3D 9-Shadermodelle mit der Direct3D 9-API. Verwenden Sie stattdessen die 9.x-Profile mit der Direct3D 10.x- und 11.x-API.
4.  Die aktuellen **D3DCompile-Funktionen \*** des HLSL-Shaders unterstützen keine Legacy-1.x-Pixelshader. Die letzte Version von HLSL zur Unterstützung dieser Ziele war D3DX9 in der Oktober 2006-Version des DirectX SDK.
5.  Alle Versionen von D3DX und des DirectX SDK sind veraltet. Weitere Informationen finden Sie unter [Wo befindet sich das DirectX SDK?](/windows/desktop/directx-sdk--august-2009-).

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Programmieranleitung für HLSL](dx-graphics-hlsl-pguide.md)
</dt> </dl>

 

 
