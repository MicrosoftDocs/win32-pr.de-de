---
title: Verwenden von Shadern in Direct3D 10
description: Verwenden von Shadern in Direct3D 10
ms.assetid: cff6f901-cb9b-44d5-a75b-9a4029a37215
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 0e19275532ce8fd034813d8574f6bdc04d72f966
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "104315182"
---
# <a name="using-shaders-in-direct3d-10"></a>Verwenden von Shadern in Direct3D 10

Die Pipeline verfügt über drei Shader-Stufen, die jeweils mit einem HLSL-Shader programmiert werden. Alle Direct3D 10-Shader werden in HLSL geschrieben und als Ziel für Shader Model 4 verwendet.



|                                                                                                                                                                                                                                                                                                                                                |
|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Unterschiede zwischen Direct3D 9 und Direct3D 10:<br/> Im Gegensatz zu Direct3D 9-shadermodellen, die in einer zwischen Assemblysprache erstellt werden können, werden Shader-Modell-4,0-Shader nur in HLSL erstellt. Die Offline Kompilierung von Shader in den Geräte nutzbaren Bytecode wird weiterhin unterstützt und wird für die meisten Szenarien empfohlen.<br/> |



 

In diesem Beispiel wird nur ein Scheitelpunkt-Shader verwendet. Da alle Shader aus dem gemeinsamen Shader-Kern erstellt werden, ist das Erlernen der Verwendung eines Vertex-Shader sehr ähnlich wie bei der Verwendung eines Geometry-oder Pixelshader.

Nachdem Sie einen HLSL-Shader verfasst haben (in diesem Beispiel wird der Vertex-Shader hlslwithoutfx. VSH verwendet), müssen Sie ihn für die jeweilige Pipeline Phase vorbereiten, in der er verwendet wird. Zu diesem Zweck müssen Sie folgende Schritte ausführen:

-   [Kompilieren eines Shaders](#compile-a-shader)
-   [Erstellen eines shaderobjekts](#create-a-shader-object)
-   [Festlegen des Shader-Objekts](#set-the-shader-object)
-   [Für alle 3 shaderphasen wiederholen](#repeat-for-all-3-shader-stages)

Diese Schritte müssen für jeden Shader in der Pipeline wiederholt werden.

## <a name="compile-a-shader"></a>Kompilieren eines Shaders

Der erste Schritt besteht darin, den Shader zu kompilieren, um zu überprüfen, ob Sie die HLSL-Anweisungen ordnungsgemäß codiert haben. Dies erfolgt durch Aufrufen von D3D10CompileShader und das Bereitstellen von mehreren Parametern, wie hier gezeigt:


```
    IPD3D10Blob * pBlob;
    
        
    // Compile the vertex shader from the file
    D3D10CompileShader( strPath, strlen( strPath ), "HLSLWithoutFX.vsh", 
        NULL, NULL, "Ripple", "vs_4_0", dwShaderFlags, &pBlob, NULL );
```



Diese Funktion übernimmt die folgenden Parameter:

-   Der Name der Datei (und Länge der namens Zeichenfolge in Bytes), die den Shader enthält. Dieses Beispiel verwendet nur einen Vertex-Shader (in der Datei "hlslwithoutfx. VSH", in der die Dateierweiterung ". VSH" eine Abkürzung für Vertex-Shader ist).
-   Der Shader-Funktionsname. In diesem Beispiel wird ein Vertex-Shader aus der Ripple-Funktion kompiliert, die eine einzelne Eingabe annimmt und eine Ausgabestruktur zurückgibt (die Funktion ist aus dem Beispiel hlslwithoutfx):
    ```
    VS_OUTPUT Ripple( in float2 vPosition : POSITION )
    ```

    

-   Ein Zeiger auf alle Makros, die vom Shader verwendet werden. Verwenden \_ Sie das d3d10-Shader \_ -Makro, um die Makros zu definieren. Erstellen Sie einfach eine namens Zeichenfolge, die alle Makronamen (wobei jeder Name durch ein Leerzeichen getrennt ist) und eine Definitions Zeichenfolge (bei jedem makrokörper durch ein Leerzeichen getrennt) enthält. Beide Zeichen folgen müssen Null enden.
-   Ein Zeiger auf alle anderen Dateien, die Sie einschließen müssen, damit die Shader kompiliert werden können. Dabei wird die ID3D10Include-Schnittstelle verwendet, die über zwei vom Benutzer implementierte Methoden verfügt: Öffnen und schließen. Um dies zu tun, müssen Sie den Text der Open-und Close-Methode implementieren. Fügen Sie in der Open-Methode den Code hinzu, den Sie zum Öffnen der gewünschten Includedateien verwenden möchten. Fügen Sie in der Close-Funktion den Code hinzu, um die Dateien zu schließen, wenn Sie damit abgeschlossen sind.
-   Der Name der zu kompilierenden Shader-Funktion. Dieser Shader kompiliert die Ripple-Funktion.
-   Das Shader-Profil, das beim Kompilieren als Ziel für das Ziel Da Sie eine Funktion in einem Scheitelpunkt, einer Geometrie oder einem Pixelshader kompilieren können, teilt das Profil dem Compiler mit, welcher Typ von Shader und welches Shader-Modell den Code vergleichen soll.
-   Shader-Compilerflags. Diese Flags teilen dem Compiler mit, welche Informationen in die kompilierte Ausgabe eingefügt werden sollen und wie der Ausgabecode optimiert werden soll: für Geschwindigkeit, Debuggen usw. Eine Auflistung der verfügbaren Flags finden Sie unter [Wirkungs Konstanten (Direct3D 10)](/windows/desktop/direct3d10/d3d10-graphics-reference-effect-constants) . Das Beispiel enthält Code, den Sie verwenden können, um die compilerflagwerte für das Projekt festzulegen. Dies ist hauptsächlich eine Frage, ob Sie Debuginformationen generieren möchten.
-   Ein Zeiger auf den Puffer, der den kompilierten Shader-Code enthält. Der Puffer enthält auch alle eingebetteten Debug-und Symboltabellen Informationen, die von den Compilerflags angefordert werden.
-   Ein Zeiger auf einen Puffer, der eine Auflistung von Fehlern und Warnungen enthält, die während der Kompilierung aufgetreten sind. Dies sind die gleichen Meldungen, die in der Debugausgabe angezeigt werden, wenn Sie den Debugger beim Kompilieren des Shader ausgeführt haben. **Null** ist ein akzeptabler Wert, wenn Sie nicht möchten, dass die Fehler an einen Puffer zurückgegeben werden.

Wenn der Shader erfolgreich kompiliert wird, wird ein Zeiger auf den Shader-Code als ID3D10Blob-Schnittstelle zurückgegeben. Sie wird als BLOB-Schnittstelle bezeichnet, da sich der Zeiger auf einen Speicherort im Arbeitsspeicher befindet, der aus einem Array von DWORD besteht. Die-Schnittstelle wird bereitgestellt, sodass Sie einen Zeiger auf den kompilierten Shader erhalten können, den Sie im nächsten Schritt benötigen.

Ab dem SDK vom Dezember 2006 ist der DirectX 10 HLSL-Compiler nun der Standard Compiler in DirectX 9 und DirectX 10. Ausführliche Informationen finden Sie unter [Effect-Compiler-Tool](/windows/desktop/direct3dtools/fxc) .

### <a name="get-a-pointer-to-a-compiled-shader"></a>Einen Zeiger auf einen kompilierten Shader erhalten

Mehrere API-Methoden erfordern einen Zeiger auf einen kompilierten Shader. Dieses Argument wird normalerweise als " *pshaderbytecode* " bezeichnet, da es auf einen kompilierten Shader zeigt, der als Sequenz von Byte Codes dargestellt wird. Zum Abrufen eines Zeigers auf einen kompilierten Shader kompilieren Sie zuerst den Shader, indem Sie [**D3D10CompileShader**](/windows/desktop/api/d3d10shader/nf-d3d10shader-d3d10compileshader) oder eine ähnliche Funktion aufrufen. Wenn die Kompilierung erfolgreich ist, wird der kompilierte Shader in einer [**ID3D10Blob**](/windows/desktop/api/d3dcommon/nn-d3dcommon-id3d10blob) -Schnittstelle zurückgegeben. Verwenden Sie abschließend die [**getbufferpointer**](/windows/desktop/api/d3dcommon/nf-d3dcommon-id3d10blob-getbufferpointer) -Methode, um den Zeiger zurückzugeben.

## <a name="create-a-shader-object"></a>Erstellen eines shaderobjekts

Nachdem der Shader kompiliert wurde, rufen Sie "kreatevertexshader" auf, um das Shader-Objekt zu erstellen:


```
    ID3D10VertexShader ** ppVertexShader
    ID3D10Blob pBlob;


    // Create the vertex shader
    hr = pd3dDevice->CreateVertexShader( (DWORD*)pBlob->GetBufferPointer(),
        pBlob->GetBufferSize(), &ppVertexShader );

    // Release the pointer to the compiled shader once you are done with it
    pBlob->Release();
```



Um das Shader-Objekt zu erstellen, übergeben Sie den Zeiger an den kompilierten Shader in "kreatevertexshader". Da der Shader zuerst erfolgreich kompiliert werden musste, wird dieser Vorgang fast sicher bestanden, es sei denn, es liegt ein Speicherproblem auf dem Computer vor.

Sie können beliebig viele Shader-Objekte erstellen und einfach Zeiger darauf halten. Derselbe Mechanismus funktioniert für geometry-und Pixel-Shader, wenn Sie den Shader-Profilen (wenn Sie die Compile-Methode aufrufen) den Schnittstellennamen entsprechen (wenn Sie die Create-Methode aufrufen).

## <a name="set-the-shader-object"></a>Festlegen des Shader-Objekts

Der letzte Schritt besteht darin, den Shader auf die Pipeline Stufe festzulegen. Da in der Pipeline drei Shader-Stufen vorhanden sind, müssen Sie drei API-Aufrufe erstellen, eine für jede Phase.


```
    // Set a vertex shader
    pd3dDevice->VSSetShader( g_pVS10 );
```



Der vssetshader-Befehl verwendet den Zeiger auf den Vertex-Shader, der in Schritt 1 erstellt wurde. Dadurch wird der Shader im Gerät festgelegt. Die Vertex-Shader-Stufe wird jetzt mit Ihrem Scheitelpunkt-Shader-Code initialisiert, und nur noch werden alle shadervariablen initialisiert.

## <a name="repeat-for-all-3-shader-stages"></a>Für alle 3 shaderphasen wiederholen

Wiederholen Sie dieselben Schritte, um einen beliebigen Scheitelpunkt oder Pixel-Shader oder sogar einen Geometry-Shader zu erstellen, der an den Pixelshader ausgibt.

## <a name="related-topics"></a>Verwandte Themen

[Kompilieren von Shadern](dx-graphics-hlsl-part1.md)


## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Programmieranleitung für HLSL](dx-graphics-hlsl-pguide.md)
</dt> </dl>

 

