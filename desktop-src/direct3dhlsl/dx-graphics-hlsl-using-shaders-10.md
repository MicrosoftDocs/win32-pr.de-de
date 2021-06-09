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
ms.openlocfilehash: c0d6212851e4603aac4db7ec85dd20714dc87774
ms.sourcegitcommit: adba238660d8a5f4fe98fc6f5d105d56aac3a400
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/09/2021
ms.locfileid: "111826288"
---
# <a name="using-shaders-in-direct3d-10"></a>Verwenden von Shadern in Direct3D 10

Die Pipeline verfügt über drei Shaderstufen, die jeweils mit einem HLSL-Shader programmiert sind. Alle Direct3D 10-Shader sind in HLSL geschrieben und richten sich an Shadermodell 4.


Unterschiede zwischen Direct3D 9 und Direct3D 10:

- Im Gegensatz zu Direct3D 9-Shadermodellen, die in einer Zwischenassemblysprache erstellt werden können, werden Shadermodell 4.0-Shader nur in HLSL erstellt. Die Offlinekompilierung von Shadern in vom Gerät nutzbaren Bytecode wird weiterhin unterstützt und für die meisten Szenarien empfohlen.



 

In diesem Beispiel wird nur ein Vertex-Shader verwendet. Da alle Shader aus dem allgemeinen Shaderkern erstellt werden, ähnelt das Erlernen der Verwendung eines Vertex-Shaders der Verwendung eines Geometrie- oder Pixel-Shaders.

Nachdem Sie einen HLSL-Shader erstellt haben (in diesem Beispiel wird der Scheitelpunkt-Shader HLSLWithoutFX.vsh verwendet), müssen Sie ihn für die jeweilige Pipelinephase vorbereiten, die ihn verwendet. Dazu müssen Sie:

-   [Kompilieren eines Shaders](#compile-a-shader)
-   [Erstellen eines Shaderobjekts](#create-a-shader-object)
-   [Festlegen des Shaderobjekts](#set-the-shader-object)
-   [Wiederholen für alle drei Shaderstufen](#repeat-for-all-3-shader-stages)

Diese Schritte müssen für jeden Shader in der Pipeline wiederholt werden.

## <a name="compile-a-shader"></a>Kompilieren eines Shaders

Der erste Schritt besteht darin, den Shader zu kompilieren, um zu überprüfen, ob Sie die HLSL-Anweisungen ordnungsgemäß codiert haben. Dazu wird D3D10CompileShader aufgerufen und mit mehreren Parametern angegeben, wie hier gezeigt:


```
    IPD3D10Blob * pBlob;
    
        
    // Compile the vertex shader from the file
    D3D10CompileShader( strPath, strlen( strPath ), "HLSLWithoutFX.vsh", 
        NULL, NULL, "Ripple", "vs_4_0", dwShaderFlags, &pBlob, NULL );
```



Diese Funktion verwendet die folgenden Parameter:

-   Der Name der Datei ( und die Länge der Namenszeichenfolge in Bytes ), die den Shader enthält. In diesem Beispiel wird nur ein Vertex-Shader verwendet (in der Datei HLSLWithoutFX.vsh, wobei die Dateierweiterung .vsh eine Abkürzung für vertex shader ist).
-   Der Name der Shaderfunktion. In diesem Beispiel wird ein Vertex-Shader aus der Funktion "Pixels" kompiliert, der eine einzelne Eingabe annimmt und eine Ausgabestruktur zurückgibt (die Funktion stammt aus dem HLSLWithoutFX-Beispiel):
    ```
    VS_OUTPUT Ripple( in float2 vPosition : POSITION )
    ```

    

-   Ein Zeiger auf alle makros, die vom Shader verwendet werden. Verwenden Sie D3D10 \_ SHADER \_ MACRO, um Ihre Makros zu definieren. Erstellen Sie einfach eine Namenszeichenfolge, die alle Makronamen enthält (wobei jeder Name durch ein Leerzeichen getrennt ist) und eine Definitionszeichenfolge (wobei jeder Makrotext durch ein Leerzeichen getrennt ist). Beide Zeichenfolgen müssen NULL-terminiert sein.
-   Ein Zeiger auf alle anderen Dateien, die Sie enthalten müssen, um Ihre Shader zum Kompilieren zu erhalten. Hierbei wird die ID3D10Include-Schnittstelle verwendet, die über zwei benutzerimplementierte Methoden verfügt: Öffnen und Schließen. Damit dies funktioniert, müssen Sie den Text der Open- und Close-Methoden implementieren. Fügen Sie in der Open-Methode den Code hinzu, den Sie zum Öffnen beliebiger Includedateien verwenden möchten. Fügen Sie in der Close-Funktion den Code hinzu, um die Dateien zu schließen, wenn Sie damit fertig sind.
-   Der Name der zu kompilierende Shaderfunktion. Dieser Shader kompiliert die Funktion "Ethereum".
-   Das Shaderprofil, auf das beim Kompilieren ausgerichtet werden soll. Da Sie eine Funktion in einen Scheitelpunkt, eine Geometrie oder einen Pixel-Shader kompilieren können, teilt das Profil dem Compiler mit, mit welchem Shadertyp und welchem Shadermodell der Code verglichen werden soll.
-   Shadercompilerflags. Diese Flags teilen dem Compiler mit, welche Informationen in die kompilierte Ausgabe aufgenommen werden sollen und wie der Ausgabecode optimiert werden soll: für Geschwindigkeit, debuggen usw. Eine Liste der verfügbaren Flags finden Sie unter [Effektkonstanten (Direct3D 10).](/windows/desktop/direct3d10/d3d10-graphics-reference-effect-constants) Das Beispiel enthält Code, mit dem Sie die Compilerflagwerte für Ihr Projekt festlegen können. Dies ist hauptsächlich eine Frage, ob Sie Debuginformationen generieren möchten.
-   Ein Zeiger auf den Puffer, der den kompilierten Shadercode enthält. Der Puffer enthält auch alle eingebetteten Debug- und Symboltabelleninformationen, die von den Compilerflags angefordert werden.
-   Ein Zeiger auf einen Puffer, der eine Liste von Fehlern und Warnungen enthält, die während der Kompilierung aufgetreten sind. Dies sind die gleichen Meldungen, die in der Debugausgabe angezeigt werden, wenn Sie den Debugger beim Kompilieren des Shaders ausführen. **NULL** ist ein akzeptabler Wert, wenn die Fehler nicht an einen Puffer zurückgegeben werden sollen.

Wenn der Shader erfolgreich kompiliert wird, wird ein Zeiger auf den Shadercode als ID3D10Blob-Schnittstelle zurückgegeben. Sie wird als Blob-Schnittstelle bezeichnet, da der Zeiger auf eine Position im Arbeitsspeicher zeigt, die aus einem Array von DWORD besteht. Die -Schnittstelle wird bereitgestellt, damit Sie einen Zeiger auf den kompilierten Shader abrufen können, den Sie im nächsten Schritt benötigen.

Ab dem SDK vom Dezember 2006 ist der DirectX 10 HLSL-Compiler jetzt sowohl in DirectX 9 als auch in DirectX 10 der Standardcompiler. Weitere Informationen finden Sie unter [Effektcompilertool.](/windows/desktop/direct3dtools/fxc)

### <a name="get-a-pointer-to-a-compiled-shader"></a>Abrufen eines Zeigers auf einen kompilierten Shader

Mehrere API-Methoden erfordern einen Zeiger auf einen kompilierten Shader. Dieses Argument wird in der Regel als *pShaderBytecode* bezeichnet, da es auf einen kompilierten Shader verweist, der als Sequenz von Bytecodes dargestellt wird. Um einen Zeiger auf einen kompilierten Shader abzurufen, kompilieren Sie zuerst den Shader, indem Sie [**D3D10CompileShader**](/windows/desktop/api/d3d10shader/nf-d3d10shader-d3d10compileshader) oder eine ähnliche Funktion aufrufen. Wenn die Kompilierung erfolgreich ist, wird der kompilierte Shader in einer [**ID3D10Blob-Schnittstelle**](/windows/desktop/api/d3dcommon/nn-d3dcommon-id3d10blob) zurückgegeben. Verwenden Sie abschließend die [**GetBufferPointer-Methode,**](/windows/desktop/api/d3dcommon/nf-d3dcommon-id3d10blob-getbufferpointer) um den Zeiger zurückzugeben.

## <a name="create-a-shader-object"></a>Erstellen eines Shaderobjekts

Nachdem der Shader kompiliert wurde, rufen Sie CreateVertexShader auf, um das Shaderobjekt zu erstellen:


```
    ID3D10VertexShader ** ppVertexShader
    ID3D10Blob pBlob;


    // Create the vertex shader
    hr = pd3dDevice->CreateVertexShader( (DWORD*)pBlob->GetBufferPointer(),
        pBlob->GetBufferSize(), &ppVertexShader );

    // Release the pointer to the compiled shader once you are done with it
    pBlob->Release();
```



Um das Shaderobjekt zu erstellen, übergeben Sie den Zeiger auf den kompilierten Shader an CreateVertexShader. Da Sie den Shader zuerst erfolgreich kompilieren mussten, wird dieser Aufruf mit ziemlicher Sicherheit erfolgreich ausgeführt, es sei denn, Sie haben ein Speicherproblem auf Ihrem Computer.

Sie können beliebig viele Shaderobjekte erstellen und einfach Zeiger darauf beibehalten. Dieser Mechanismus funktioniert für Geometrie- und Pixel-Shader, vorausgesetzt, Sie stimmen mit den Shaderprofilen (wenn Sie die Kompilierungsmethode aufrufen) mit den Schnittstellennamen überein (wenn Sie die create-Methode aufrufen).

## <a name="set-the-shader-object"></a>Festlegen des Shaderobjekts

Im letzten Schritt wird der Shader auf die Pipelinephase festgelegt. Da die Pipeline drei Shaderstufen umfasst, müssen Sie drei API-Aufrufe durchführen, einen für jede Phase.


```
    // Set a vertex shader
    pd3dDevice->VSSetShader( g_pVS10 );
```



Beim Aufruf von VSSetShader wird der Zeiger auf den in Schritt 1 erstellten Vertexshader verwendet. Dadurch wird der Shader auf dem Gerät festgelegt. Die Vertex-Shaderphase wird nun mit ihrem Vertex-Shadercode initialisiert. Alles, was übrig bleibt, ist das Initialisieren aller Shadervariablen.

## <a name="repeat-for-all-3-shader-stages"></a>Wiederholen für alle drei Shaderstufen

Wiederholen Sie diese Schritte, um einen Vertex- oder Pixel-Shader oder sogar einen Geometrie-Shader zu erstellen, der an den Pixelshader ausgegeben wird.

## <a name="related-topics"></a>Verwandte Themen

[Kompilieren von Shadern](dx-graphics-hlsl-part1.md)


## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Programmieranleitung für HLSL](dx-graphics-hlsl-pguide.md)
</dt> </dl>

 

