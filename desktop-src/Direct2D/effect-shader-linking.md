---
title: Effektshader-Verknüpfung
description: Direct2D verwendet eine Optimierung namens "Effect Shader Linking", die das Rendering mehrerer Effekte Diagramm Rendering in einem einzigen Durchlauf kombiniert.
ms.assetid: 431A5B39-6C84-442D-AC66-0F341E10DF2C
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d0a17691346649b2ddcde7ca4f3e343be6a35a90
ms.sourcegitcommit: b7a1da2711221fa99072079bf52399cbdfc6bd9d
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/05/2021
ms.locfileid: "104351749"
---
# <a name="effect-shader-linking"></a>Effektshader-Verknüpfung

Direct2D verwendet eine Optimierung namens "Effect Shader Linking", die das Rendering mehrerer Effekte Diagramm Rendering in einem einzigen Durchlauf kombiniert.

-   [Übersicht über die Auswirkung der Shader-Verknüpfung](#overview-of-effect-shader-linking)
-   [Verwenden von Effekt-Shader-Verknüpfung](#using-effect-shader-linking)
-   [Erstellen eines shaderverknüpfungs-kompatiblen benutzerdefinierten Effekts](#authoring-a-shader-linking-compatible-custom-effect)
-   [Beispiel-Shader mit Verknüpfungs kompatiblem Effekten](#example-linking-compatible-effect-shader)
-   [Kompilieren eines verknüpften kompatiblen Shaders](#compiling-a-linking-compatible-shader)
    -   [Schritt 1: Kompilieren der Exportfunktion](#step-1-compile-the-export-function)
    -   [Schritt 2: Kompilieren Sie den vollständigen Shader, und Betten Sie die Exportfunktion ein.](#step-2-compile-the-full-shader-and-embed-the-export-function)
-   [Funktions Spezifikationen exportieren](#export-function-specifications)
-   [Zugehörige Themen](#related-topics)

## <a name="overview-of-effect-shader-linking"></a>Übersicht über die Auswirkung der Shader-Verknüpfung

Die Effekt-Shader-Verknüpfungs Optimierungen bauen auf der HLSL-Shader-Verknüpfung auf, einem Direct3D 11,2-Feature, das das Generieren von Pixel-und Vertex-Shadern zur Laufzeit ermöglicht, indem vorkompilierte Shaderfunktionen verknüpft werden. Die folgenden Abbildungen veranschaulichen das Konzept des Effekts von Shader-Verknüpfungen in einem Effekt Diagramm. Die erste Abbildung zeigt ein typisches Direct2D Effect-Diagramm mit vier Renderingtransformationen. Ohne Shader-Verknüpfung nutzt jede Transformation einen Renderingdurchlauf und erfordert eine zwischen Oberfläche. in diesem Diagramm sind insgesamt 4 Pass-und 3-zwischenate erforderlich.



|                                                                                                             |
|-------------------------------------------------------------------------------------------------------------|
| ![Transformieren des Diagramms ohne shaderverknüpfung: 4 Pass-und 3-Intermediate.](images/shader-transform-graph.png) |



 

Die zweite Abbildung zeigt das gleiche Effekt Diagramm, in dem jede renderingtransformation durch eine Verknüpf bares-Funktions Version ersetzt wurde. Direct2D ist in der Lage, das gesamte Diagramm zu verknüpfen und in einem Durchlauf auszuführen, ohne dass ein Vermittler erforderlich ist. Dies kann zu einer deutlichen Verringerung der GPU-Ausführungszeit und zur Verringerung der GPU-Speicherauslastung in Spitzenzeiten.



|                                                                                                   |
|---------------------------------------------------------------------------------------------------|
| ![Transformieren des Diagramms mit shaderverknüpfung: 1 Durchlauf, 0 zwischen.](images/shader-linking-graph.png) |



 

Auswirkungen der Shader-Verknüpfung auf einzelne Transformationen innerhalb eines Effekts. Dies bedeutet, dass selbst ein Diagramm mit einem einzelnen Effekt von Shader-Verknüpfungen profitieren kann, wenn dieser Effekt über mehrere gültige Transformationen verfügt.

## <a name="using-effect-shader-linking"></a>Verwenden von Effekt-Shader-Verknüpfung

Wenn Sie eine Direct2D-Anwendung erstellen, die Effekte verwendet, müssen Sie nichts Unternehmen, um den Effekt von Shader-Verknüpfungen zu nutzen. Direct2D analysiert automatisch das Effekt Diagramm, um die optimale Methode zum Verknüpfen der einzelnen Transformationen zu ermitteln.

Autoren von Effekten sind dafür verantwortlich, ihre Wirkung auf eine Weise zu implementieren, die das Verknüpfen von shadereffekten unterstützt. Weitere Informationen finden Sie weiter unten im Abschnitt [Authoring a Shader Linking-Compatible Custom Effect](#authoring-a-shader-linking-compatible-custom-effect) . Alle integrierten Effekte unterstützen Shader-Verknüpfungen.

Direct2D verknüpft nur angrenzende Renderingtransformationen in Situationen, in denen es von Vorteil ist. Bei der Entscheidung, ob zwei Transformationen verknüpft werden sollen, werden mehrere Faktoren berücksichtigt. Beispielsweise wird die Shader-Verknüpfung nicht ausgeführt, wenn eine der Transformationen Scheitelpunkt-oder COMPUTE-Shader verwendet, da nur Pixel-Shader verknüpft werden können. Wenn ein Effekt nicht so erstellt wurde, dass er mit Shader-Verknüpfungen kompatibel ist, werden umgebende Transformationen nicht damit verknüpft.

Wenn eine solche Verknüpfungs Gefahr besteht, verknüpft Direct2D keine Transformationen neben der Gefahr, sondern versucht trotzdem, den Rest des Diagramms zu verknüpfen.



|                                                                                                             |
|-------------------------------------------------------------------------------------------------------------|
| ![Transformieren des Diagramms mit einer Verknüpfungs Gefahr: 2 Durchlauf, 1 zwischen.](images/shader-linking-graph-hazard.png) |



 

## <a name="authoring-a-shader-linking-compatible-custom-effect"></a>Erstellen eines shaderverknüpfungs-kompatiblen benutzerdefinierten Effekts

Wenn Sie einen eigenen benutzerdefinierten Direct2D-Effekt erstellen, müssen Sie sicherstellen, dass die zugehörigen Transformationen die Shader-Verknüpfung des Effekts unterstützen. Dies erfordert einige geringfügige Änderungen daran, wie vorherige benutzerdefinierte Effekte implementiert wurden. Wenn eine Transformation innerhalb des benutzerdefinierten Effekts keine shaderverknüpfung unterstützt, wird Sie von Direct2D nicht mit Transformationen verknüpft, die sich in der Ausgabe im Diagramm befinden.

Als Autor eines benutzerdefinierten Effekts sollten Sie verschiedene wichtige Konzepte und Anforderungen beachten:

-   **Keine Änderungen an den Effekten der Schnittstellen Implementierungen.**

    Sie müssen keinen Code ändern, der die verschiedenen Wirkungs Schnittstellen, wie z. b. [ID2D1DrawTransform](/windows/win32/api/d2d1effectauthor/nn-d2d1effectauthor-id2d1drawtransform), implementiert.

-   **Bereitstellen einer vollständigen und Export Funktions Version von Shadern**

    Sie müssen eine Export Funktions Version der Shader Ihres Effekts bereitstellen, die von Direct2D untersucht werden können. Außerdem müssen Sie auch weiterhin den ursprünglichen vollständigen Shader bereitstellen. Dies liegt daran, dass Direct2D zur Laufzeit die richtige shaderversion auswählt, je nachdem, ob die Shader-Verknüpfung auf einen bestimmten Link im Diagramm angewendet werden soll.

    Wenn eine Transformation nur das vollständige Pixel-Shader-BLOB (über [ID2D1EffectContext:: loadpixelshader](/windows/win32/api/d2d1effectauthor/nf-d2d1effectauthor-id2d1effectcontext-loadpixelshader)) bereitstellt, wird Sie nicht mit angrenzenden Transformationen verknüpft.

- **Hilfsfunktionen**

    Direct2D stellt [HLSL](hlsl-helpers.md) -Hilfsobjekte und-Makros bereit, mit denen automatisch sowohl die vollständigen als auch die Export Funktions Versionen eines Shaders generiert werden. Diese Hilfsprogramme finden Sie unter d2d1effecthelpers. hlsli. Außerdem können Sie mit dem HLSL-Compiler (FXC) den Export Funktions-Shader in ein privates Feld im vollständigen Shader einfügen. Auf diese Weise müssen Sie nur einmal einen Shader erstellen und beide Versionen gleichzeitig an Direct2D übergeben. Sowohl d2d1effecthelpers. hlsli als auch der FXC-Compiler sind als Teil des Windows SDK enthalten.

    Die Hilfsfunktionen:

  - [D2DGetInput](d2dgetinput.md)  
  - [D2DSampleInput](d2dsampleinput.md)  
  - [D2DSampleInputAtOffset](d2dsampleinputatoffset.md)  
  - [D2DSampleInputAtPosition](d2dsampleinputatposition.md)  
  - [D2DGetInputCoordinate](d2dgetinputcoordinate.md)  
  - [D2DGetScenePosition](d2dgetsceneposition.md)  
  - [D2D \_ PS- \_ Eintrag](d2d-ps-entry.md)  

  Sie können auch manuell zwei Versionen der einzelnen Shader erstellen und diese zweimal kompilieren, sofern die unten aufgeführten Spezifikationen in den [Export Funktions Spezifikationen](#export-function-specifications) erfüllt sind.

-   **Nur Pixel-Shader**

    Direct2D bietet keine Unterstützung für das Verknüpfen von COMPUTE-oder Vertex-Shadern. Wenn Ihre Wirkung jedoch sowohl einen Scheitelpunkt als auch einen PixelShader verwendet, kann die Ausgabe des Pixelshaders weiterhin verknüpft werden.

-   **Einfaches und komplexes Sampling**

    Die Verknüpfung der shaderfunktion funktioniert, indem die Ausgabe eines Pixelshaders mit der Eingabe eines nachfolgenden Pixelshader-Pass verbunden wird. Dies ist nur möglich, wenn der verarbeitende Pixelshader nur einen einzelnen Eingabe Wert erfordert, um seine Berechnung auszuführen. Dieser Wert würde normalerweise von der Stichprobenentnahme einer Eingabe Textur in der Textur Koordinate stammen, die vom Vertexshader ausgegeben wird. Ein solcher Pixel-Shader wird als einfache Stichprobenentnahme bezeichnet.

    

    |                                                                                                                                                                                            |
    |--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
    | ![die Graustufen Konvertierung ist ein Beispiel für eine einfache Stichprobenentnahme. der Wert eines bestimmten Ausgabe Pixels hängt nur vom Wert des entsprechenden Eingabe Pixels ab.](images/simple-sampling.png) |

    

     

    Einige Pixel-Shader, wie z. b. ein gauscher Weichzeichner, berechnen Ihre Ausgabe aus mehreren Eingabe Beispielen anstelle eines einzelnen Beispiels. Ein solcher Pixel-Shader wird als komplexe Stichprobenentnahme bezeichnet.

    

    |                                                                                                                                                           |
    |-----------------------------------------------------------------------------------------------------------------------------------------------------------|
    | ![gauscher Weichzeichner ist ein Beispiel für eine komplexe Stichprobenentnahme. der Wert des mittleren Ausgabe Pixels hängt von mehreren Eingabe Pixeln ab.](images/complex-sampling.png) |

    

     

    Nur Shaderfunktionen mit einfachen Eingaben können von einer anderen shaderfunktion bereitgestellt werden. Shader-Funktionen mit komplexen Eingaben müssen mit einer Eingabe Textur für Stichproben bereitgestellt werden. Dies bedeutet, dass Direct2D keinen Shader mit komplexen Eingaben mit seinem Vorgänger verknüpft.

    Wenn Sie die [Direct2D HLSL](hlsl-helpers.md)-Hilfsprogramme verwenden, müssen Sie im HLSL angeben, ob ein Shader komplexe oder einfache Eingaben verwendet.

## <a name="example-linking-compatible-effect-shader"></a>Beispiel-Shader mit Verknüpfungs kompatiblem Effekten

Der folgende Code Ausschnitt stellt mithilfe der D2D-Hilfsprogramme einen einfachen Verknüpfungs kompatiblen Effekt-Shader dar:

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

Beachten Sie in diesem kurzen Beispiel, dass keine Funktionsparameter deklariert werden, dass die Anzahl der Eingaben und der Typ der einzelnen Eingaben vor der Einstiegs Funktion deklariert wird. die Eingabe wird durch Aufrufen von [D2DGetInput](d2dgetinput.md)abgerufen, und die Präprozessordirektiven müssen vor dem einschließen der Hilfsdatei definiert werden.

Ein Verknüpfungs kompatibler Shader muss sowohl einen regulären Einzelpass-Pixel-Shader als auch eine Export-Shader-Funktion bereitstellen. Mit dem [D2D \_ PS- \_ Eintrags](d2d-ps-entry.md) Makro können alle diese aus demselben Code generiert werden, wenn Sie in Verbindung mit dem Shader-Kompilierungs Skript verwendet werden.

Beim Kompilieren eines vollständigen Shaders werden die Makros in den folgenden Code erweitert, der über eine D2D Effects-kompatible Eingabe Signatur verfügt.

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

Wenn eine Export Funktions Version desselben Codes kompiliert wird, wird der folgende Code generiert:

```syntax
// Shader function version
export float4 LinkingCompatiblePixelShader_Function(
    float4 input0 : INPUT0)
    {
        input.rgb *= input.a;
        return input;
    }      
```

Beachten Sie, dass die Textur Eingabe, die normalerweise durch Sampling eines Texture2D abgerufen wird, durch eine Funktions Eingabe (input0) ersetzt wurde.

Eine vollständige Beschreibung der Schritte, die Sie zum Schreiben eines Verknüpfungs kompatiblen Effekts ausführen müssen, finden Sie im [Tutorial zu benutzerdefinierten Effekten](custom-effects.md) und im [Beispiel Direct2D Custom Image Effects](https://github.com/microsoft/Windows-universal-samples/tree/master/Samples/D2DCustomEffects).

## <a name="compiling-a-linking-compatible-shader"></a>Kompilieren eines verknüpften kompatiblen Shaders

Damit Sie nicht erreichbar sind, muss das an D2D über gegebene Pixel-Shader-BLOB sowohl die vollständigen als auch die Export Funktions Versionen des Shaders enthalten. Dies wird erreicht, indem die kompilierte Exportfunktion in den \_ \_ privaten Datenbereich D3D BLOB eingebettet wird \_ .

Wenn die Shader mit den D2D Helper-Funktionen erstellt werden, muss zum Zeitpunkt der Kompilierung ein D2D-Kompilierungs Ziel definiert werden. Die Ziel Typen für die Kompilierung sind D2D \_ Full \_ Shader und D2D \_ Function.

Das Kompilieren eines Verknüpfungs kompatiblen Effekt-Shaders ist ein zweistufiger Prozess:

-   [Kompilieren der Export-Funktion](#step-1-compile-the-export-function)
-   [Kompilieren Sie den vollen Shader, und Betten Sie die Exportfunktion ein.](#step-2-compile-the-full-shader-and-embed-the-export-function)

> [!Note]  
> Wenn Sie einen Effekt mithilfe von Visual Studio kompilieren, sollten Sie eine Batchdatei erstellen, die beide FXC-Befehle ausführt, und diese Batchdatei als benutzerdefinierten Buildschritt ausführen, der vor dem Kompilierungs Schritt ausgeführt wird.

 

### <a name="step-1-compile-the-export-function"></a>Schritt 1: Kompilieren der Exportfunktion

```syntax
fxc /T <shadermodel> <MyShaderFile>.hlsl /D D2D_FUNCTION /D D2D_ENTRY=<entry> /Fl <MyShaderFile>.fxlib           
```

Um die Export Funktions Version Ihres Shaders zu kompilieren, müssen Sie die folgenden Flags an FXC übergeben.



|                                |                                                                                                                                                                                                                                                           |
|--------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **Flag**                       | **Beschreibung**                                                                                                                                                                                                                                           |
| /T <ShaderModel>         | Legen <ShaderModel> Sie auf das entsprechende Pixel-Shader-Profil fest, wie in der [FXC-Syntax](/windows/desktop/direct3dtools/dx-graphics-tools-fxc-syntax)definiert. Dabei muss es sich um eines der unter "HLSL Shader Linking" aufgeführten Profile handeln. |
| <MyShaderFile>. HLSL      | Legen <MyShaderFile> Sie auf den Namen der HLSL-Datei fest.                                                                                                                                                                                                    |
| /D D2D- \_ Funktion               | Diese Definition weist FXC an, die Export Funktions Version des Shaders zu kompilieren.                                                                                                                                                                       |
| /D D2D \_ Eintrag =<entry>    | Legen <entry> Sie auf den Namen des HLSL-Einstiegs Punkts fest, den Sie im [D2D \_ PS- \_ Eintrags](d2d-ps-entry.md) Makro definiert haben.                                                                                                                                    |
| /FL <MyShaderFile> . fxlib | Legen <MyShaderfile> Sie auf fest, wo Sie die Export Funktions Version des Shaders speichern möchten. Beachten Sie, dass die Erweiterung ". fxlib" lediglich zur Erleichterung der Identifikation dient.                                                                                              |



 

### <a name="step-2-compile-the-full-shader-and-embed-the-export-function"></a>Schritt 2: Kompilieren Sie den vollständigen Shader, und Betten Sie die Exportfunktion ein.

```syntax
fxc /T ps_<shadermodel> <MyShaderFile>.hlsl /D D2D_FULL_SHADER /D D2D_ENTRY=<entry> /E <entry> /setprivate <MyShaderFile>.fxlib /Fo <MyShader>.cso /Fh <MyShader>.h           
```

Um die vollständige Version Ihres Shaders mit der eingebetteten Exportversion zu kompilieren, müssen Sie die folgenden Flags an FXC übergeben.



|                                        |                                                                                                                                                                                                                                                                                      |
|----------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **Flag**                               | **Beschreibung**                                                                                                                                                                                                                                                                      |
| /T <ShaderModel>                 | Legen <ShaderModel> Sie auf das entsprechende Pixel-Shader-Profil fest, wie in der [FXC-Syntax](/windows/desktop/direct3dtools/dx-graphics-tools-fxc-syntax)definiert. Dabei muss es sich um das Pixel-Shader-Profil handeln, das dem in Schritt 1 angegebenen Verknüpfungs Profil entspricht. |
| <MyShaderFile>. HLSL              | Legen <MyShaderFile> Sie auf den Namen der HLSL-Datei fest.                                                                                                                                                                                                                               |
| /D D2D \_ Full- \_ Shader                   | Diese Definition weist FXC an, die vollständige Version des Shaders zu kompilieren.                                                                                                                                                                                                             |
| /D D2D \_ Eintrag =<entry>            | Legen <entry> Sie auf den Namen des HLSL-Einstiegs Punkts fest, den Sie im D2D \_ PS \_ Entry ()-Makro definiert haben.                                                                                                                                                                                 |
| /E <entry>                       | Legen <entry> Sie auf den Namen des HLSL-Einstiegs Punkts fest, den Sie im D2D \_ PS \_ Entry ()-Makro definiert haben.                                                                                                                                                                                 |
| /setprivate <MyShaderFile> . fxlib | Dieses Argument weist FXC an, den in Schritt 1 generierten Export Funktions-Shader in den \_ \_ privaten Datenbereich D3D BLOB einzubetten \_ .                                                                                                                                                          |
| /FO <MyShader> . CSO               | Legen <MyShader> Sie auf fest, wo Sie den abschließenden, kombinierten kompilierten Shader speichern möchten.                                                                                                                                                                                                 |
| /FH <MyShader> . h                 | Legen <MyShader> Sie auf fest, wo Sie den abschließenden kombinierten Header speichern möchten.                                                                                                                                                                                                          |



 

## <a name="export-function-specifications"></a>Funktions Spezifikationen exportieren

Es ist möglich – aber nicht empfehlenswert –, einen kompatiblen Effekt-Shader zu erstellen, ohne die von D2D bereitgestellten Hilfsprogramme zu verwenden. Es muss darauf geachtet werden, dass die Eingabe Signaturen der vollständigen Shader-und Exportfunktionen den D2D-Spezifikationen entsprechen.

Die Spezifikationen für vollständige Shader sind identisch mit früheren Windows-Versionen. Kurz gesagt, die Pixel-Shader-Eingabeparameter müssen SV \_ -Position, Szenen \_ Position und ein texkoord pro Effekt Eingabe sein.

Für die Export-Funktion muss die Funktion ein float4-Wert zurückgeben, und die Eingaben müssen einen der folgenden Typen aufweisen:

-   Einfache Eingabe

    ```syntax
    float4 d2d_inputN : INPUTN         
    ```

    Bei einfachen Eingaben fügt D2D entweder eine Beispiel Funktion zwischen der Eingabe Textur und der Shader-Funktion ein, oder die Eingabe wird von der Ausgabe einer anderen shaderfunktion bereitgestellt.

-   Komplexe Eingabe

    ```syntax
    float4 d2d_uvN  : TEXCOORDN                
    ```

    Bei komplexen Eingaben übergibt D2D nur eine Textur Koordinate, wie in der Dokumentation zu Windows 8 beschrieben.

-   Ausgabe Speicherort

    ```syntax
    float4 d2d_posScene : SCENE_POSITION                
    ```

    Es kann nur eine Szenen \_ Positions Eingabe definiert werden. Dieser Parameter sollte nur bei Bedarf eingeschlossen werden, da dieser Parameter nur von einer Funktion pro verknüpftem Shader verwendet werden kann.

Die Semantik muss wie oben beschrieben definiert werden, da D2D die Semantik prüft, um zu entscheiden, wie Funktionen miteinander verknüpft werden sollen. Wenn eine Funktions Eingabe nicht mit einem der oben genannten Typen identisch ist, wird die Funktion für Shader-Verknüpfungen abgelehnt.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[HLSL-Hilfsprogramme](hlsl-helpers.md)
</dt> <dt>

[ID3D11Linker-Schnittstelle](/windows/desktop/api/d3d11shader/nn-d3d11shader-id3d11linker)
</dt> <dt>

[ID3D11FunctionLinkingGraph-Schnittstelle](/windows/desktop/api/d3d11shader/nn-d3d11shader-id3d11functionlinkinggraph)
</dt> </dl>

 

 