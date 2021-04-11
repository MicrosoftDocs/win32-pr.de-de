---
description: Eine Liste der Features, die in Direct3D 10 verfügbar sind, finden Sie hier. Auf dieser Seite werden die Direct3D 9-Funktionen aufgelistet, die in Direct3D 10 nicht mehr unterstützt werden.
ms.assetid: ad3eff8e-a225-47c0-a53f-b1a3c94bcaac
title: Veraltete Features (Direct3D 10)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a66b6fe5092427cd66876ab5f6e1d7aaf83f0880
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104126698"
---
# <a name="deprecated-features-direct3d-10"></a>Veraltete Features (Direct3D 10)

Eine Liste der Features, die in Direct3D 10 verfügbar sind, finden Sie [hier](d3d10-graphics-programming-guide-api-features.md). Auf dieser Seite werden die Direct3D 9-Funktionen aufgelistet, die in Direct3D 10 nicht mehr unterstützt werden.



|                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                       |
|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Die größten Funktionsänderungen in Direct3D 10 lauten:<br/> Direct3D 10 unterstützt die Transformations-und Beleuchtungs Pipeline mit fester Funktions Zeit nicht mehr.<br/> Direct3D 10 unterstützt nicht mehr die Textur Blender mit fester Funktion (manchmal auch als Pixel-Shader fester Funktion bezeichnet).<br/> Direct3D 10 implementiert neue rasterisierungsregeln, die einfacher und sauberer sind als die in Direct3D 9 implementierten Legacy-GDI-Regeln. Beispielsweise wird das Steuerelement für das letzte Pixel für Linien nicht mehr unterstützt.<br/> |



 

Hier finden Sie eine umfassende Liste der Features in Direct3D 9, die in Direct3D 10 als veraltet eingestuft wurden.

-   **Alpha Blend**. Alpha Blend ist nun unabhängig von Color Blend programmiert. Direct3D 10 fügt eine UMSCHALT Fläche "Alpha-Blend-enable" hinzu, die standardmäßig aktiviert ist. Weitere Informationen finden Sie unter [State Objects (Direct3D 10)](d3d10-graphics-programming-guide-api-features-state-objects.md) .
-   **Alpha-Test**. Der Alpha Test ist ein Pixel Verhalten mit fester Funktionsweise für Direct3D 9. Der Alpha Test wird in programmierbare Pixel-Shader für Direct3D 10 und höher verschoben. Informationen zum emuinieren der Direct3D 9-Alpha Testfunktion in Direct3D 10 und höher finden Sie im fixedfuncemu-Beispiel im [DirectX SDK für Juni 2010](https://www.microsoft.com/download/en/details.aspx?id=6812).
-   **Optionen** für den Blend-Modus. Bothsrcalpha wurde aus d3d10 Blend entfernt, \_ da es mit bothinvsrcalpha redundant ist. Weitere Informationen finden Sie unter [**d3d10 \_ Blend**](/windows/desktop/api/D3D10/ne-d3d10-d3d10_blend) .
-   **Block Komprimierungs Formate**. In Direct3D 10 gibt es keinen Unterschied zwischen vorab multipliziertem Alpha oder nicht-prämultipliziertem alpha. Diese Direct3D 9-Formate werden diesen Direct3D 10-Formaten zugeordnet: 

    | Direct3D 9 | Direct3D 10 |
    |------------|-------------|
    | DXT1       | BC1\*       |
    | DXT2,DXT3  | BU2\*       |
    | DXT4, DXT5  | BC3\*       |

    

     

    Weitere Informationen finden Sie unter [Block Komprimierung (Direct3D 10)](d3d10-graphics-programming-guide-resources-block-compression.md) .

-   Ausschneide **Flächen**. Anstelle der Verwendung von Clip-Ebenen implementiert Direct3D 10 Ausschneide Abstände und umschneide Abstände mit bis zu 8 Komponenten, die jeweils bis zu zwei Elemente von Vertex-Attributen bilden. Weitere Informationen finden Sie unter [Semantik (DirectX HLSL)](../direct3dhlsl/dx-graphics-hlsl-semantics.md) . Das [fixedfuncemu](https://msdn.microsoft.com/library/Ee416406(v=VS.85).aspx) -Beispiel enthält ein Beispiel für das emuinieren von Clip-Flächen in Direct3D 10.
-   **Dithering**. Direct3D 10 unterstützt das Schreiben von Daten in ein Renderziel nicht.
-   Die **Transformations-und Beleuchtungs Pipeline der Fixed-Funktion in ist nicht verfügbar**. Stattdessen müssen Sie Shaders verwenden. Weitere Informationen finden Sie unter [Shader-Phasen (Direct3D 10)](/previous-versions//bb205146(v=vs.85)) .
-   **Textur-Mixer mit fester Funktion (auch als fester funktionspixelshader bezeichnet)**. Stattdessen müssen Sie Shaders verwenden. Weitere Informationen finden Sie unter [Shader-Phasen (Direct3D 10)](/previous-versions//bb205146(v=vs.85)) .
-   Die **Füll Modi** wurden geändert. Direct3D 10 implementiert Solid-und Draht Modell-Füll Modi. Der D3DFILLMODE-Punkt wurde entfernt. verwenden Sie bei Bedarf einen Geometry-Shader, um den Punkt Modus zu emulieren. Das [fixedfuncemu](https://msdn.microsoft.com/library/Ee416406(v=VS.85).aspx) -Beispiel enthält ein Beispiel für das emuinieren von D3DFILLMODE Point in Direct3D 10. Weitere Informationen finden [**Sie unter d3d10 \_ Fill \_ Mode**](/windows/desktop/api/D3D10/ne-d3d10-d3d10_fill_mode) and [Shader Stages (Direct3D 10)](/previous-versions//bb205146(v=vs.85)) .
-   **Formatiert**. Hardware kann Formate verwenden, die von der API verfügbar gemacht werden. Die Formate der Leuchtkraft sind nicht mehr implementiert.
-   **Filterung von MipMap**. Die Option zum Auswählen des Modus "kein Filter" wurde entfernt. Verwenden Sie stattdessen eine Textur mit nur einer einzelnen MipMap, oder legen Sie den maxlod-samplerstatus auf 0 fest. Weitere Informationen finden Sie unter [State Objects (Direct3D 10)](d3d10-graphics-programming-guide-api-features-state-objects.md) .
-   **Paletten**. Anwendungen sollten stattdessen einen abhängigen Textur Lesevorgang verwenden.
-   **Pixel-und Vertex-Shader-Modelle**: 1 \_ x, 2 \_ x und 3 \_ 0. Direct3D 10 unterstützt Shader Model 4. Weitere Informationen finden Sie unter [Shader Model 4](../direct3dhlsl/dx-graphics-hlsl-sm4.md) .
-   **Punkt Sprite**. Verwenden Sie stattdessen einen Geometry-Shader. Weitere Informationen finden Sie unter [Shader-Phasen (Direct3D 10)](/previous-versions//bb205146(v=vs.85)) .
-   **Rasterisierungsregeln**. Ältere Regeln für GDI-Zeilen rasterisierung werden durch saubere, einfachere Regeln ersetzt. Das letzte Pixel-Steuerelement für Linien wird nicht mehr unterstützt. Weitere Informationen finden Sie unter [rasterization Rules (Direct3D 10)](../direct3d11/d3d10-graphics-programming-guide-rasterizer-stage-rules.md) .
-   **Schattierung**. D3DSHADEMODE (die flache/Gouraud/Phong-Schattierung unterstützen) wurde entfernt. Direct3D 10 implementiert stattdessen zwei Interpolationen Modifizierers für Vertex-Shader-Ausgaben. Unter [fixedfuncemu Sample](https://msdn.microsoft.com/library/Ee416406(v=VS.85).aspx) finden Sie ein Beispiel für das emuinieren von Direct3D 9-Modi "Gouraud" und "Flat Shade" in Direct3D 10.
-   **texldp** -Anweisung. Eine Anwendung muss einen projizierten Textur Ladevorgang mit zusätzlichen HLSL-Anweisungen implementieren. Weitere Informationen finden Sie unter [Referenz für HLSL](../direct3dhlsl/dx-graphics-hlsl-reference.md) . Das [fixedfuncemu](https://msdn.microsoft.com/library/Ee416406(v=VS.85).aspx) -Beispiel enthält ein Beispiel für das emuinieren von texldp in Direct3D 10.
-   Der Status der Textur **Koordinaten-Index** (TCI) Textur Stufen (D3DTSS \_ texcoordindex) wird nicht mehr unterstützt.
-   **Dreiecks Lüfter**. Eine Anwendung muss vorhandene Dreiecks-Fans in Dreiecks Listen oder Dreiecks Streifen konvertieren. Wenn Sie einige Verhaltensweisen mithilfe von drawprimitiver in älteren APIs emulieren möchten, verwenden Sie drawindebug in Direct3D 10. Weitere Informationen finden Sie unter [primitive Topologien (Direct3D 10)](../direct3d11/d3d10-graphics-programming-guide-primitive-topologies.md) .
-   **W-Pufferung**. Die Hardware Unterstützung ist nicht garantiert. Es wird empfohlen, dass eine Anwendung stattdessen tiefen Puffer mit hoher Genauigkeit verwendet. Weitere Informationen finden Sie unter [Konfigurieren von Depth-Stencil Funktionen (Direct3D 10)](../direct3d11/d3d10-graphics-programming-guide-depth-stencil.md) .
-   **Wrap-Modi** (umschließen von Texturkoordinaten). Die Textur Adress Umbrüche (z. b. Wrap, Spiegelung, Klammer usw.) sind immer noch vorhanden. Weitere Informationen finden Sie unter [**d3d10 \_ Sampler \_ DESC**](/windows/desktop/api/D3D10/ns-d3d10-d3d10_sampler_desc) and [**d3d10 \_ Texture \_ Address \_ Mode**](/windows/desktop/api/D3D10/ne-d3d10-d3d10_texture_address_mode).

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[API-Features (Direct3D 10)](d3d10-graphics-programming-guide-api-features.md)
</dt> </dl>

 

 
