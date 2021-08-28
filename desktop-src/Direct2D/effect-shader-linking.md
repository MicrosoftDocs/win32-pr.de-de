---
title: Effektshader-Verknüpfung
description: Direct2D verwendet eine Optimierung namens Effekt-Shaderverknüpfung, die mehrere Effektdiagrammrenderingdurchläufe in einem einzelnen Durchlauf kombiniert.
ms.assetid: 431A5B39-6C84-442D-AC66-0F341E10DF2C
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e22d9ae245b5bbaa0c13dd7d5296dc419f740404
ms.sourcegitcommit: 61a4c522182aa1cacbf5669683d9570a3bf043b2
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/26/2021
ms.locfileid: "122881825"
---
# <a name="effect-shader-linking"></a>Effektshader-Verknüpfung

Direct2D verwendet eine Optimierung namens Effekt-Shaderverknüpfung, die mehrere Effektdiagrammrenderingdurchläufe in einem einzelnen Durchlauf kombiniert.

-   [Übersicht über die Verknüpfung von Effekt-Shadern](#overview-of-effect-shader-linking)
-   [Verwenden von Effekt-Shaderverknüpfungen](#using-effect-shader-linking)
-   [Erstellen eines mit Shaderverknüpfung kompatiblen benutzerdefinierten Effekts](#authoring-a-shader-linking-compatible-custom-effect)
-   [Beispiel für einen verknüpfungskompatiblen Effekt-Shader](#example-linking-compatible-effect-shader)
-   [Kompilieren eines verknüpfungskompatiblen Shaders](#compiling-a-linking-compatible-shader)
    -   [Schritt 1: Kompilieren der Exportfunktion](#step-1-compile-the-export-function)
    -   [Schritt 2: Kompilieren des vollständigen Shaders und Einbetten der Exportfunktion](#step-2-compile-the-full-shader-and-embed-the-export-function)
-   [Exportieren von Funktionsspezifikationen](#export-function-specifications)
-   [Zugehörige Themen](#related-topics)

## <a name="overview-of-effect-shader-linking"></a>Übersicht über die Verknüpfung von Effekt-Shadern

Die Effekt-Shaderverknüpfungsoptimierungen bauen auf der HLSL-Shaderverknüpfung auf, einem Direct3D 11.2-Feature, mit dem Pixel- und Vertex-Shader zur Laufzeit generiert werden können, indem vorkompilierte Shaderfunktionen verknüpft werden. Die folgenden Abbildungen veranschaulichen das Konzept der Effekt-Shaderverknüpfung in einem Effektdiagramm. Die erste Abbildung zeigt ein typisches Direct2D-Effektdiagramm mit vier Renderingtransformationen. Ohne Shaderverknüpfung nutzt jede Transformation einen Renderingdurchlauf und erfordert eine Zwischenoberfläche. Insgesamt sind für dieses Diagramm vier Durchläufe und drei Zwischenschritte erforderlich.

![Transformieren eines Diagramms ohne Shaderverknüpfung: 4 Durchläufe und 3 Zwischenstufen.](images/shader-transform-graph.png)

Die zweite Abbildung zeigt das gleiche Effektdiagramm, in dem jede Renderingtransformation durch eine verlinkbare Funktionsversion ersetzt wurde. Direct2D kann das gesamte Diagramm verknüpfen und in einem Durchlauf ausführen, ohne zwischengeschaltet zu werden. Dies kann zu einer erheblichen Verringerung der GPU-Ausführungszeit und einer Verringerung der GPU-Spitzenspeicherauslastung sorgen.

![Transformationsdiagramm mit Shaderverknüpfung: 1 Durchlauf, 0 Zwischenstufen.](images/shader-linking-graph.png)



 

Die Effekt-Shaderverknüpfung arbeitet mit einzelnen Transformationen innerhalb eines Effekts. Dies bedeutet, dass auch ein Graph mit einem einzigen Effekt von der Shaderverknüpfung profitieren kann, wenn dieser Effekt mehrere gültige Transformationen hat.

## <a name="using-effect-shader-linking"></a>Verwenden von Effekt-Shaderverknüpfungen

Wenn Sie eine Direct2D-Anwendung erstellen, die Effekte verwendet, müssen Sie nichts unternehmen, um die Effekt-Shaderverknüpfung zu nutzen. Direct2D analysiert automatisch das Effektdiagramm, um die optimale Methode zum Verknüpfen der einzelnen Transformationen zu ermitteln.

Effektautoren sind dafür verantwortlich, ihre Effekte auf eine Weise zu implementieren, die das Verknüpfen von Effekt-Shadern unterstützt. Weitere Informationen finden Sie weiter unten im Abschnitt [Erstellen eines shaderverknüpfungskompatiblen benutzerdefinierten Effekts.](#authoring-a-shader-linking-compatible-custom-effect) Alle integrierten Effekte unterstützen die Shaderverknüpfung.

Direct2D verknüpft nur benachbarte Renderingtransformationen in Situationen, in denen dies vorteilhaft ist. Bei der Entscheidung, ob zwei Transformationen verknüpft werden sollen, werden mehrere Faktoren berücksichtigt. Beispielsweise wird die Shaderverknüpfung nicht ausgeführt, wenn eine der Transformationen Scheitelpunkt- oder Compute-Shader verwendet, da nur Pixel-Shader verknüpft werden können. Wenn ein Effekt nicht so erstellt wurde, dass er mit der Shaderverknüpfung kompatibel ist, werden umgebende Transformationen nicht damit verknüpft.

Falls eine solche Verknüpfungsgefahr vorliegt, verknüpft Direct2D keine Transformationen neben der Gefahr, sondern versucht weiterhin, den Rest des Diagramms zu verknüpfen.

![Transformieren eines Diagramms mit einer Verknüpfungsgefahr: 2 Durchläufe, 1 Zwischendiagramm.](images/shader-linking-graph-hazard.png)

## <a name="authoring-a-shader-linking-compatible-custom-effect"></a>Erstellen eines mit Shaderverknüpfung kompatiblen benutzerdefinierten Effekts

Wenn Sie Einen eigenen benutzerdefinierten Direct2D-Effekt erstellen, müssen Sie sicherstellen, dass die Transformationen das Verknüpfen von Effekt-Shadern unterstützen. Dies erfordert einige geringfügige Änderungen an der Implementierung vorheriger benutzerdefinierter Effekte. Wenn eine Transformation innerhalb Ihres benutzerdefinierten Effekts keine Shaderverknüpfung unterstützt, verknüpft Direct2D sie nicht mit transformationsgrenzend im Effektdiagramm.

Als Benutzerdefinierter Effektautor sollten Sie sich mehrerer wichtiger Konzepte und Anforderungen bewusst sein:

-   **Keine Änderungen an Schnittstellenimplementierungen**

    Sie müssen keinen Code ändern, der die verschiedenen Effektschnittstellen implementiert, z. B. [ID2D1DrawTransform.](/windows/win32/api/d2d1effectauthor/nn-d2d1effectauthor-id2d1drawtransform)

-   **Bereitstellen einer vollständigen und einer Exportfunktionsversion von Shadern**

    Sie müssen eine Exportfunktionsversion der Shader Ihres Effekts angeben, die von Direct2D verknüpft werden können. Darüber hinaus müssen Sie weiterhin den ursprünglichen, vollständigen Shader bereitstellen. Dies liegt daran, dass Direct2D zur Laufzeit die richtige Shaderversion auswählt, je nachdem, ob die Shaderverknüpfung auf einen bestimmten Link im Diagramm angewendet werden soll.

    Wenn eine Transformation nur das vollständige Pixelshaderblob (über [ID2D1EffectContext::LoadPixelShader)](/windows/win32/api/d2d1effectauthor/nf-d2d1effectauthor-id2d1effectcontext-loadpixelshader)bereitstellt, wird sie nicht mit angrenzenden Transformationen verknüpft.

- **Hilfsfunktionen**

    Direct2D stellt [HLSL-Hilfsfunktionen](hlsl-helpers.md) und -Makros bereit, die automatisch sowohl die vollständige als auch die Exportfunktionsversion eines Shaders generieren. Diese Hilfshilfen finden Sie unter d2d1effecthelpers.hlsli. Darüber hinaus können Sie mit dem HLSL-Compiler (FXC) den Exportfunktions-Shader in ein privates Feld im vollständigen Shader einfügen. Auf diese Weise müssen Sie nur einmal einen Shader erstellen und beide Versionen gleichzeitig an Direct2D übergeben. Sowohl d2d1effecthelpers.hlsli als auch der FXC-Compiler sind im Windows SDK enthalten.

    Die Hilfsfunktionen:

  - [D2DGetInput](d2dgetinput.md)  
  - [D2DSampleInput](d2dsampleinput.md)  
  - [D2DSampleInputAtOffset](d2dsampleinputatoffset.md)  
  - [D2DSampleInputAtPosition](d2dsampleinputatposition.md)  
  - [D2DGetInputCoordinate](d2dgetinputcoordinate.md)  
  - [D2DGetScenePosition](d2dgetsceneposition.md)  
  - [D2D \_ PS \_ ENTRY](d2d-ps-entry.md)  

  Sie können auch zwei Versionen jedes Shaders manuell erstellen und zweimal kompilieren, solange die unten unter Exportieren von [Funktionsspezifikationen beschriebenen Spezifikationen](#export-function-specifications) erfüllt sind.

-   **Nur Pixel-Shader**

    Direct2D unterstützt keine Verknüpfung von Compute- oder Vertex-Shadern. Wenn Ihr Effekt jedoch sowohl einen Scheitelpunkt- als auch einen Pixel-Shader verwendet, kann die Ausgabe des Pixel-Shaders weiterhin verknüpft werden.

-   **Einfache und komplexe Stichprobenentnahme**

    Die Shaderfunktionsverknüpfung funktioniert, indem die Ausgabe eines Pixelshaderdurchlaufs mit der Eingabe eines nachfolgenden Pixelshaderdurchlaufs verbunden wird. Dies ist nur möglich, wenn der verbrauchende Pixel-Shader nur einen einzelnen Eingabewert für die Berechnung benötigt. Dieser Wert stammt normalerweise aus der Stichprobenentnahme einer Eingabetextur an der Texturkoordinate, die vom Vertex-Shader ausgegeben wird. Ein solcher Pixelshader wird als einfache Stichprobenentnahme bezeichnet.

    ![Die Graustufenkonvertierung ist ein Beispiel für eine einfache Stichprobenentnahme. Der Wert eines bestimmten Ausgabepixels hängt nur vom Wert des entsprechenden Eingabepixels ab.](images/simple-sampling.png)

    Einige Pixel-Shader, z. B. ein Gaußsches Weichzeichner, berechnen ihre Ausgabe aus mehreren Eingabebeispielen und nicht nur aus einer einzelnen Stichprobe. Ein solcher Pixelshader wird als komplexe Stichprobenentnahme bezeichnet.

    

    ![der weichzeichnerische Weichzeichner ist ein Beispiel für eine komplexe Stichprobenentnahme. Der Wert des mittleren Ausgabepixels hängt von mehreren Eingabepixeln ab.](images/complex-sampling.png)

    
    Nur Shaderfunktionen mit einfachen Eingaben können ihre Eingaben von einer anderen Shaderfunktion erhalten. Shaderfunktionen mit komplexen Eingaben müssen mit einer Eingabetextur für die Stichprobenentnahme bereitgestellt werden. Dies bedeutet, dass Direct2D einen Shader nicht mit komplexen Eingaben mit seinem Vorgänger verknüpft.

    Wenn Sie die [Direct2D HLSL-Hilfatoren](hlsl-helpers.md)verwenden, müssen Sie in der HLSL angeben, ob ein Shader komplexe oder einfache Eingaben verwendet.

## <a name="example-linking-compatible-effect-shader"></a>Beispiel für einen verknüpfungskompatiblen Effekt-Shader

Mithilfe der D2D-Hilfatoren stellt der folgende Codeausschnitt einen einfachen verknüpfungskompatiblen Effekt-Shader dar:

```syntax
#define D2D_INPUT_COUNT 1
#define D2D_INPUT0_SIMPLE
#include “d2d1effecthelpers.hlsli”

D2D_PS_ENTRY(LinkingCompatiblePixelShader)
{
    float4 input = D2DGetInput(0);
    input.rgb *= input.a;
    return input;
}          
```

Beachten Sie in diesem kurzen Beispiel, dass keine Funktionsparameter deklariert werden, dass die Anzahl der Eingaben und der Typ jeder Eingabe vor der Eingabefunktion deklariert wird, die Eingabe durch Aufrufen von [D2DGetInput](d2dgetinput.md)abgerufen wird und dass Präprozessordirektiven definiert werden müssen, bevor die Hilfsdatei eingeschlossen wird.

Ein verknüpfungskompatibler Shader muss sowohl einen regulären Single-Pass-Pixelshader als auch eine Export-Shaderfunktion bereitstellen. Das [D2D \_ PS \_ ENTRY-Makro](d2d-ps-entry.md) ermöglicht, dass jedes dieser Makros aus dem gleichen Code generiert wird, wenn es in Verbindung mit dem Shaderkompilierungsskript verwendet wird.

Beim Kompilieren eines vollständigen Shaders werden die Makros in den folgenden Code erweitert, der über eine D2D Effects-kompatible Eingabesignatur verfügt.

```syntax
Texture2D<float4> InputTexture0;
SamplerState InputSampler0;

float4 LinkingCompatiblePixelShader(
    float4 pos   : SV_POSITION,
    float4 posScene : SCENE_POSITION,
    float4 uv0  : TEXCOORD0
    ) : SV_Target
    {
        float4 input = InputTexture0.Sample(InputSampler0, uv0.xy);
        input.rgb *= input.a;
        return input;
    }    
```

Beim Kompilieren einer Exportfunktionsversion desselben Codes wird der folgende Code generiert:

```syntax
// Shader function version
export float4 LinkingCompatiblePixelShader_Function(
    float4 input0 : INPUT0)
    {
        input.rgb *= input.a;
        return input;
    }      
```

Beachten Sie, dass die Textureingabe, die normalerweise durch Sampling einer Texture2D abgerufen wird, durch eine Funktionseingabe (input0) ersetzt wurde.

Eine vollständige Schritt-für-Schritt-Beschreibung der Schritte zum Schreiben eines verknüpfungskompatiblen Effekts finden Sie im Tutorial zu [benutzerdefinierten Effekten](custom-effects.md) und im Beispiel für [benutzerdefinierte Direct2D-Bildeffekte.](https://github.com/microsoft/Windows-universal-samples/tree/master/Samples/D2DCustomEffects)

## <a name="compiling-a-linking-compatible-shader"></a>Kompilieren eines verknüpfungskompatiblen Shaders

Um verknüpft werden zu können, muss das an D2D übergebene Pixel-Shaderblob sowohl die vollständige als auch die Exportfunktionsversion des Shaders enthalten. Dies wird erreicht, indem die kompilierte Exportfunktion in den \_ D3D BLOB \_ PRIVATE \_ DATA-Bereich eingebettet wird.

Wenn die Shader mit den D2D-Hilfsfunktionen erstellt werden, muss zur Kompilierungszeit ein D2D-Kompilierungsziel definiert werden. Die Kompilierungszieltypen sind D2D \_ FULL \_ SHADER und D2D \_ FUNCTION.

Das Kompilieren eines verknüpfungskompatiblen Effekt-Shaders ist ein zweistufiger Prozess:

-   [Kompilieren der Exportfunktion](#step-1-compile-the-export-function)
-   [Kompilieren des vollständigen Shaders und Einbetten der Exportfunktion](#step-2-compile-the-full-shader-and-embed-the-export-function)

> [!Note]  
> Beim Kompilieren eines Effekts mit Visual Studio sollten Sie eine Batchdatei erstellen, die beide FXC-Befehle ausführt, und diese Batchdatei als benutzerdefinierten Buildschritt ausführen, der vor dem Kompilierungsschritt ausgeführt wird.

 

### <a name="step-1-compile-the-export-function"></a>Schritt 1: Kompilieren der Exportfunktion

```syntax
fxc /T <shadermodel> <MyShaderFile>.hlsl /D D2D_FUNCTION /D D2D_ENTRY=<entry> /Fl <MyShaderFile>.fxlib           
```

Um die Exportfunktionsversion Ihres Shaders zu kompilieren, müssen Sie die folgenden Flags an FXC übergeben.



|    Flag                            |    Beschreibung                       |
|--------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| /T &lt; ShaderModel&gt;         | Legen Sie &lt; ShaderModel &gt; auf das entsprechende Pixel-Shaderprofil fest, wie in [FXC-Syntax](/windows/desktop/direct3dtools/dx-graphics-tools-fxc-syntax)definiert. Dies muss eines der Profile sein, die unter "HLSL-Shaderverknüpfung" aufgeführt sind. |
| &lt;MyShaderFile &gt; .hlsl      | Legen Sie &lt; MyShaderFile &gt; auf den Namen der HLSL-Datei fest.                                                                                                                                                                                                    |
| /D \_ D2D-FUNKTION               | Diese Definition weist FXC an, die Exportfunktionsversion des Shaders zu kompilieren.                                                                                                                                                                       |
| /D D2D \_ &lt; ENTRY=-Eintrag&gt;    | Legen Sie &lt; entry auf den Namen des &gt; HLSL-Einstiegspunkts fest, den Sie im [D2D \_ PS \_ ENTRY-Makro](d2d-ps-entry.md) definiert haben.                                                                                                                                    |
| /Fl &lt; MyShaderFile &gt; .fxlib | Legen &lt; Sie MyShaderfile &gt; auf fest, in dem Sie die Version der Exportfunktion des Shaders speichern möchten. Beachten Sie, dass die Erweiterung .fxlib nur zur einfacheren Identifizierung dient.                                                                                              |

### <a name="step-2-compile-the-full-shader-and-embed-the-export-function"></a>Schritt 2: Kompilieren des vollständigen Shaders und Einbetten der Exportfunktion

```syntax
fxc /T ps_<shadermodel> <MyShaderFile>.hlsl /D D2D_FULL_SHADER /D D2D_ENTRY=<entry> /E <entry> /setprivate <MyShaderFile>.fxlib /Fo <MyShader>.cso /Fh <MyShader>.h           
```

Um die Vollversion Ihres Shaders mit eingebetteter Exportversion zu kompilieren, müssen Sie die folgenden Flags an FXC übergeben.



|    Flag                                    |    Beschreibung                     |
|----------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| /T &lt; ShaderModel&gt;                 | Legen Sie &lt; ShaderModel &gt; auf das entsprechende Pixel-Shaderprofil fest, wie in [FXC-Syntax](/windows/desktop/direct3dtools/dx-graphics-tools-fxc-syntax)definiert. Dies muss das Pixel-Shaderprofil sein, das dem in Schritt 1 angegebenen Verknüpfungsprofil entspricht. |
| &lt;MyShaderFile &gt; .hlsl              | Legen Sie &lt; MyShaderFile &gt; auf den Namen der HLSL-Datei fest.                                                                                                                                                                                                                               |
| /D D2D \_ FULL \_ SHADER                   | Diese Definition weist FXC an, die Vollversion des Shaders zu kompilieren.                                                                                                                                                                                                             |
| /D D2D \_ &lt; ENTRY=-Eintrag&gt;            | Legen Sie &lt; entry auf den Namen des &gt; HLSL-Einstiegspunkts fest, den Sie im \_ D2D PS \_ ENTRY()-Makro definiert haben.                                                                                                                                                                                 |
| &lt;/E-Eintrag&gt;                       | Legen Sie &lt; entry auf den Namen des &gt; HLSL-Einstiegspunkts fest, den Sie im \_ D2D PS \_ ENTRY()-Makro definiert haben.                                                                                                                                                                                 |
| /setprivate &lt; MyShaderFile &gt; .fxlib | Dieses Argument weist FXC an, den in Schritt 1 generierten Exportfunktions-Shader in den \_ D3D BLOB \_ PRIVATE \_ DATA-Bereich einzubetten.                                                                                                                                                          |
| /Fo &lt; MyShader &gt; .cso               | Legen &lt; Sie MyShader &gt; auf den Ort fest, an dem Sie den endgültigen, kombinierten kompilierten Shader speichern möchten.                                                                                                                                                                                                 |
| /Ung &lt; MyShader &gt; .h                 | Legen &lt; Sie MyShader &gt; auf den Ort fest, an dem Sie den letzten kombinierten Header speichern möchten.                                                                                                                                                                                                          |

## <a name="export-function-specifications"></a>Exportieren von Funktionsspezifikationen

Es ist möglich , einen kompatiblen Effekt-Shader zu erstellen , obwohl dies nicht empfohlen wird, ohne die von D2D bereitgestellten Hilfsmöglichkeiten zu verwenden. Achten Sie darauf, dass sowohl der vollständige Shader als auch die Eingabesignaturen der Exportfunktion den D2D-Spezifikationen entsprechen.

Die Spezifikationen für vollständige Shader sind identisch mit früheren Windows Versionen. Kurz gesagt: Die Eingabeparameter des Pixelshaders müssen SV \_ POSITION, SCENE \_ POSITION und eine TEXCOORD-Eingabe pro Effekt sein.

Für die Exportfunktion muss die Funktion float4 zurückgeben, und ihre Eingaben müssen einen der folgenden Typen aufweisen:

-   Einfache Eingabe

    ```syntax
    float4 d2d_inputN : INPUTN         
    ```

    Bei einfachen Eingaben fügt D2D entweder eine Sample-Funktion zwischen der Eingabetextur und der Shaderfunktion ein, oder die Eingabe wird durch die Ausgabe einer anderen Shaderfunktion bereitgestellt.

-   Komplexe Eingabe

    ```syntax
    float4 d2d_uvN  : TEXCOORDN                
    ```

    Bei komplexen Eingaben übergibt D2D nur eine Texturkoordinate, wie in Windows 8 Dokumentation beschrieben.

-   Ausgabespeicherort

    ```syntax
    float4 d2d_posScene : SCENE_POSITION                
    ```

    Es kann nur eine SCENE \_ POSITION-Eingabe definiert werden. Dieser Parameter sollte nur bei Bedarf eingeschlossen werden, da nur eine Funktion pro verknüpften Shader diesen Parameter verwenden kann.

Die Semantik muss wie oben definiert werden, da D2D die Semantik untersucht, um zu entscheiden, wie Funktionen miteinander verknüpft werden sollen. Wenn eine Funktionseingabe nicht mit einem der oben genannten Typen übereinstimmt, wird die Funktion für die Shaderverknüpfung abgelehnt.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[HLSL-Hilfshilfen](hlsl-helpers.md)
</dt> <dt>

[ID3D11Linker-Schnittstelle](/windows/desktop/api/d3d11shader/nn-d3d11shader-id3d11linker)
</dt> <dt>

[ID3D11FunctionLinkingGraph-Schnittstelle](/windows/desktop/api/d3d11shader/nn-d3d11shader-id3d11functionlinkinggraph)
</dt> </dl>

 

 
