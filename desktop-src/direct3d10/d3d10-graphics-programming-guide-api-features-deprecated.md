---
description: Eine Liste der in Direct3D 10 verfügbaren Features finden Sie hier. Auf dieser Seite werden die Direct3D 9-Features aufgeführt, die in Direct3D 10 nicht mehr unterstützt werden.
ms.assetid: ad3eff8e-a225-47c0-a53f-b1a3c94bcaac
title: Veraltete Features (Direct3D 10)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 50ce1750e6d8f98785bf87fb92169e56f0b4ca4e8a6dfdd34c6174a8c3087eb3
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119852770"
---
# <a name="deprecated-features-direct3d-10"></a>Veraltete Features (Direct3D 10)

Eine Liste der in Direct3D 10 verfügbaren Features finden Sie [hier.](d3d10-graphics-programming-guide-api-features.md) Auf dieser Seite werden die Direct3D 9-Features aufgeführt, die in Direct3D 10 nicht mehr unterstützt werden.

Die größten Featureänderungen in Direct3D 10 sind:

- Direct3D 10 unterstützt die Transformations- und Beleuchtungspipeline fester Funktionen nicht mehr.
- Direct3D 10 unterstützt nicht mehr den Texturblender mit fester Funktion (manchmal auch als Pixel-Shader mit fester Funktion bezeichnet).
- Direct3D 10 implementiert neue Rasterregeln, die einfacher und einfacher als die älteren GDI-Regeln sind, die in Direct3D 9 implementiert sind. Beispielsweise wird das Letzte-Pixel-Steuerelement für Zeilen nicht mehr unterstützt.

Im Folgenden finden Sie eine vollständige Liste der Features in Direct3D 9, die in Direct3D 10 veraltet sind.

- **Alphablending**. Alphablending ist jetzt unabhängig von der Farbmischung programmiert. Direct3D 10 fügt einen Alphablend-Enable-Umschalter hinzu, der standardmäßig aktiviert ist. Weitere [Informationen finden Sie unter Zustandsobjekte (Direct3D 10).](d3d10-graphics-programming-guide-api-features-state-objects.md)
- **Alphatest**. Der Alphatest ist ein Pixelverhalten mit fester Funktion für Direct3D 9. Der Alphatest wird in programmierbare Pixel-Shader für Direct3D 10 und höher verschoben. Informationen zum Emulieren der Direct3D 9 Alpha-Testfunktion in Direct3D 10 und höher finden Sie im Beispiel FixedFuncEMU im DirectX SDK für Juni [2010.](https://www.microsoft.com/download/en/details.aspx?id=6812)
- **Optionen für den Blend-Modus**. BOTHSRCALPHA wurde aus D3D10 BLEND entfernt, da \_ es mit BOTHINVSRCALPHA redundant ist. Weitere Informationen finden Sie unter [**D3D10 \_ BLEND.**](/windows/desktop/api/D3D10/ne-d3d10-d3d10_blend)
- **Blockkomprimierungsformate**. In Direct3D 10 gibt es keinen Unterschied zwischen vorab multipliziertem alpha und nicht prämultipliziertem Alpha. Diese Direct3D 9-Formate sind diesen Direct3D 10-Formaten zuordnen: 

    | Direct3D 9 | Direct3D 10 |
    |------------|-------------|
    | DXT1       | BC1\*       |
    | DXT2,DXT3  | BU2\*       |
    | DXT4,DXT5  | BC3\*       |

    

     

    Weitere [Informationen finden Sie unter Blockkomprimierung (Direct3D 10).](d3d10-graphics-programming-guide-resources-block-compression.md)

-   **Clipebenen**. Anstatt Clipebenen zu verwenden, implementiert Direct3D 10 Clipentfernungen und CULL-Abstände mit bis zu 8 Komponenten in bis zu 2 Elementen von Scheitelpunktattributen. Weitere [Informationen finden Sie unter Semantik (DirectX HLSL).](../direct3dhlsl/dx-graphics-hlsl-semantics.md) [Das FixedFuncEMU-Beispiel](https://msdn.microsoft.com/library/Ee416406(v=VS.85).aspx) enthält ein Beispiel für das Emulieren von Clipebenen in Direct3D 10.
-   **Dithering von**. Direct3D 10 unterstützt nicht das Schreiben geerbter Daten in ein Renderziel.
-   **Transformations- und Beleuchtungspipeline für feste Funktionen in nicht verfügbar.** Stattdessen müssen Sie Shader verwenden. Weitere [Informationen finden Sie unter Shaderstufen (Direct3D 10).](/previous-versions//bb205146(v=vs.85))
-   **Texturblender mit fester Funktion (auch als Pixel-Shader für feste Funktionen bezeichnet)**. Stattdessen müssen Sie Shader verwenden. Weitere [Informationen finden Sie unter Shaderstufen (Direct3D 10).](/previous-versions//bb205146(v=vs.85))
-   **Die Füllmodi** haben sich geändert. Direct3D 10 implementiert die Füllmodi "Solid" und "Wireframe". D3DFILLMODE-Punkt wurde entfernt. Verwenden Sie bei Bedarf einen Geometrie-Shader, um den Punktmodus zu emulieren. [Das FixedFuncEMU-Beispiel](https://msdn.microsoft.com/library/Ee416406(v=VS.85).aspx) enthält ein Beispiel für das Emulieren eines D3DFILLMODE-Punkts in Direct3D 10. Weitere Informationen finden Sie unter D3D10 FILL MODE and [Shader Stages (Direct3D 10) (D3D10 FILL MODE und Shader Stages (Direct3D 10)).](/previous-versions//bb205146(v=vs.85)) [**\_ \_**](/windows/desktop/api/D3D10/ne-d3d10-d3d10_fill_mode)
-   **Formatiert**. Hardware kann Formate verwenden, die von der API verfügbar gemacht werden. Leuchtdichteformate werden nicht mehr implementiert.
-   **Mipmap-Filterung**. Die Option zum Auswählen des Modus ohne Filter wurde entfernt. Verwenden Sie stattdessen eine Textur mit nur einer einzelnen Mipmap, oder legen Sie den MaxLOD-Samplerzustand auf 0 fest. Weitere [Informationen finden Sie unter Zustandsobjekte (Direct3D 10).](d3d10-graphics-programming-guide-api-features-state-objects.md)
-   **Paletten**. Anwendungen sollten stattdessen eine abhängige Textur lesen.
-   **Pixels- und Vertex-Shadermodelle:** 1 \_ x, 2 \_ x und 3 \_ 0. Direct3D 10 unterstützt Shadermodell 4. Weitere [Informationen finden Sie unter ShaderModell 4.](../direct3dhlsl/dx-graphics-hlsl-sm4.md)
-   **Punkt-Sprites**. Verwenden Sie stattdessen einen Geometrie-Shader. Weitere [Informationen finden Sie unter Shaderstufen (Direct3D 10).](/previous-versions//bb205146(v=vs.85))
-   **Rasterregeln**. Ältere GDI-Zeilenrasterregeln werden durch klarere, einfachere Regeln ersetzt. Das Steuerelement für das letzte Pixel für Zeilen wird nicht mehr unterstützt. Weitere [Informationen finden Sie unter Rasterregeln (Direct3D 10).](../direct3d11/d3d10-graphics-programming-guide-rasterizer-stage-rules.md)
-   **Schattierungsmodi**. D3DSHADEMODE (die flat/gouraud/phong shading unterstützen) wurde entfernt. Direct3D 10 implementiert stattdessen zwei Interpolationsmodifizierer für Vertex-Shader-Ausgaben. Unter [FixedFuncEMU-Beispiel](https://msdn.microsoft.com/library/Ee416406(v=VS.85).aspx) finden Sie ein Beispiel für das Emulieren von Direct3D 9 Gouraud- und Flat shade-Modi in Direct3D 10.
-   **texldp-Anweisung.** Eine Anwendung muss eine projizierte Texturlast mit zusätzlichen HLSL-Anweisungen implementieren. Weitere [Informationen finden Sie unter Referenz für HLSL.](../direct3dhlsl/dx-graphics-hlsl-reference.md) [Das FixedFuncEMU-Beispiel](https://msdn.microsoft.com/library/Ee416406(v=VS.85).aspx) enthält ein Beispiel für die Emulation von texldp in Direct3D 10.
-   **Texturphasenzustand** des Texturkoordinatenindexes (Texture Coordinate Index, TCI) (D3DTSS \_ TEXCOORDINDEX) wird nicht mehr unterstützt.
-   **Dreiecks-Lüfter**. Eine Anwendung muss vorhandene Dreiecks-Lüfter in Dreieckslisten oder Dreiecksstreifen konvertieren. Um einige Verhaltensweisen mit DrawPrimitive in älteren APIs zu emulieren, versuchen Sie, DrawIndexed in Direct3D 10 zu verwenden. Weitere [Informationen finden Sie unter Primitive Topologien (Direct3D 10).](../direct3d11/d3d10-graphics-programming-guide-primitive-topologies.md)
-   **W puffert**. Hardwareunterstützung ist nicht garantiert. Es wird empfohlen, dass eine Anwendung stattdessen Tiefenpuffer mit hoher Genauigkeit verwendet. Weitere Informationen finden Depth-Stencil Konfigurieren der Funktionalität [(Direct3D 10).](../direct3d11/d3d10-graphics-programming-guide-depth-stencil.md)
-   **Umbruchmodi** (Texturkoordinatenumbruch). Texturadressenumbruch (z. B. Wrap, Spiegelung, Klammer usw.) ist weiterhin vorhanden. Weitere Informationen [**finden Sie unter D3D10 \_ SAMPLER \_ DESC**](/windows/desktop/api/D3D10/ns-d3d10-d3d10_sampler_desc) und [**D3D10 \_ TEXTURE ADDRESS \_ \_ MODE**](/windows/desktop/api/D3D10/ne-d3d10-d3d10_texture_address_mode).

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[API-Features (Direct3D 10)](d3d10-graphics-programming-guide-api-features.md)
</dt> </dl>

 

 
