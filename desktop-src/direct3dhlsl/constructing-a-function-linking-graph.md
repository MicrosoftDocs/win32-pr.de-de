---
title: Erstellen eines funktionsverknüpfungs Diagramms und Verknüpfen dieses Diagramms mit kompiliertem Code
description: Hier erfahren Sie, wie Sie Funktions Verknüpfungs Diagramme (FLGS) für Shader erstellen und diese Shader mit einer shaderbibliothek verknüpfen, um shaderblobfunktionen zu erzeugen, die von der Direct3D-Laufzeit verwendet werden können.
ms.assetid: 82C3109E-8571-49D2-A8BF-298E30E1281B
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c037e7ea111d11d24df173ffba7e56c8f486af82
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "103858389"
---
# <a name="constructing-a-function-linking-graph-and-linking-it-to-compiled-code"></a>Erstellen eines funktionsverknüpfungs Diagramms und Verknüpfen dieses Diagramms mit kompiliertem Code

Hier erfahren Sie, wie Sie Funktions Verknüpfungs Diagramme (FLGS) für Shader erstellen und diese Shader mit einer shaderbibliothek verknüpfen, um shaderblobfunktionen zu erzeugen, die von der Direct3D-Laufzeit verwendet werden können.

**Ziel:** Zum Erstellen eines funktionsverknüpfungs Diagramms und Verknüpfen dieses Diagramms mit kompiliertem Code.

## <a name="prerequisites"></a>Voraussetzungen

Es wird davon ausgegangen, dass Sie mit C+ vertraut sind. Sie müssen außerdem mit den grundlegenden Konzepten der Grafikprogrammierung vertraut sein.

Außerdem wird davon ausgegangen, dass Sie das [Packen einer shaderbibliothek](pachaging-a-shader-library.md)durchlaufen haben.

**Zeit bis zum Abschluss:** 30 Minuten.

## <a name="instructions"></a>Instructions

### <a name="1-construct-a-function-linking-graph-for-the-vertex-shader"></a>1. Erstellen eines funktionsverknüpfungs Diagramms für den Vertex-Shader.

Rufen Sie die [**D3DCreateFunctionLinkingGraph**](/windows/desktop/api/D3Dcompiler/nf-d3dcompiler-d3dcreatefunctionlinkinggraph) -Funktion auf, um ein Funktions Verknüpfungs Diagramm ([**ID3D11FunctionLinkingGraph**](/windows/desktop/api/d3d11shader/nn-d3d11shader-id3d11functionlinkinggraph)) zu erstellen, das den Scheitelpunkt Shader darstellt.

Verwenden Sie ein Array von [**D3D11- \_ Parameter- \_ DESC**](/windows/desktop/api/d3d11shader/ns-d3d11shader-d3d11_parameter_desc) -Strukturen, um die Eingabeparameter für den Vertex-Shader zu definieren. Die [Eingabe-Assembler-Phase](/windows/desktop/direct3d11/d3d10-graphics-programming-guide-input-assembler-stage) fügt die Eingabeparameter in den Vertexshader ein. Das Layout der Eingabeparameter des Vertex-Shaders entspricht dem Layout des Vertexshaders im kompilierten Code. Nachdem Sie die Eingabeparameter definiert haben, müssen Sie die [**ID3D11FunctionLinkingGraph:: abtinputsignature**](/windows/desktop/api/d3d11shader/nf-d3d11shader-id3d11functionlinkinggraph-setinputsignature) -Methode aufrufen, um den Eingabe Knoten ([**ID3D11LinkingNode**](/windows/desktop/api/d3d11shader/nn-d3d11shader-id3d11linkingnode)) für den Vertexshader zu definieren.


```C++
            ComPtr<ID3D11FunctionLinkingGraph> vertexShaderGraph;
            DX::ThrowIfFailed(D3DCreateFunctionLinkingGraph(0, &vertexShaderGraph));

            // Define the main input node which will be fed by the Input Assembler pipeline stage.
            static const D3D11_PARAMETER_DESC vertexShaderInputParameters[] =
            {
                {"inputPos",  "POSITION0", D3D_SVT_FLOAT, D3D_SVC_VECTOR, 1, 3, D3D_INTERPOLATION_LINEAR, D3D_PF_IN, 0, 0, 0, 0},
                {"inputTex",  "TEXCOORD0", D3D_SVT_FLOAT, D3D_SVC_VECTOR, 1, 2, D3D_INTERPOLATION_LINEAR, D3D_PF_IN, 0, 0, 0, 0},
                {"inputNorm", "NORMAL0",   D3D_SVT_FLOAT, D3D_SVC_VECTOR, 1, 3, D3D_INTERPOLATION_LINEAR, D3D_PF_IN, 0, 0, 0, 0}
            };
            ComPtr<ID3D11LinkingNode> vertexShaderInputNode;
            LinkingThrowIfFailed(vertexShaderGraph->SetInputSignature(vertexShaderInputParameters, ARRAYSIZE(vertexShaderInputParameters), 
                &vertexShaderInputNode), vertexShaderGraph.Get());
```



Rufen Sie die [**ID3D11FunctionLinkingGraph:: CallFunction**](/windows/desktop/api/d3d11shader/nf-d3d11shader-id3d11functionlinkinggraph-callfunction) -Methode auf, um einen Knoten für die Haupt-Vertex-Shader-Funktion zu erstellen und Aufrufe an [**ID3D11FunctionLinkingGraph::P assvalue**](/windows/desktop/api/d3d11shader/nf-d3d11shader-id3d11functionlinkinggraph-passvalue) vorzunehmen, um Werte vom Eingabe Knoten an den Knoten für die Haupt-Vertex-Shader-Funktion zu übergeben.


```C++
            // Create a node for the main VertexFunction call using the output of the helper functions.
            ComPtr<ID3D11LinkingNode> vertexFunctionCallNode;
            LinkingThrowIfFailed(vertexShaderGraph->CallFunction("", shaderLibrary.Get(), "VertexFunction", &vertexFunctionCallNode), 
                vertexShaderGraph.Get());

            // Define the graph edges from the input node and helper function nodes.
            LinkingThrowIfFailed(vertexShaderGraph->PassValue(homogenizeCallNodeForPos.Get(), D3D_RETURN_PARAMETER_INDEX, 
                vertexFunctionCallNode.Get(), 0), vertexShaderGraph.Get());
            LinkingThrowIfFailed(vertexShaderGraph->PassValue(vertexShaderInputNode.Get(), 1, vertexFunctionCallNode.Get(), 1), 
                vertexShaderGraph.Get());
            LinkingThrowIfFailed(vertexShaderGraph->PassValue(homogenizeCallNodeForNorm.Get(), D3D_RETURN_PARAMETER_INDEX, 
                vertexFunctionCallNode.Get(), 2), vertexShaderGraph.Get());
```



Verwenden Sie ein Array von [**D3D11- \_ Parameter- \_ DESC**](/windows/desktop/api/d3d11shader/ns-d3d11shader-d3d11_parameter_desc) -Strukturen, um die Ausgabeparameter für den Vertex-Shader zu definieren. Der Vertex-Shader fügt seine Ausgabeparameter in den Pixelshader ein. Das Layout der Ausgabeparameter des Vertex-Shader entspricht dem Layout des Pixelshaders im kompilierten Code. Nachdem Sie die Ausgabeparameter definiert haben, können Sie die [**ID3D11FunctionLinkingGraph:: setoutputsignature**](/windows/desktop/api/d3d11shader/nf-d3d11shader-id3d11functionlinkinggraph-setoutputsignature) -Methode aufrufen, um den Ausgabe Knoten ([**ID3D11LinkingNode**](/windows/desktop/api/d3d11shader/nn-d3d11shader-id3d11linkingnode)) für den Vertex-Shader zu definieren.


```C++
            // Define the main output node which will feed the Pixel Shader pipeline stage.
            static const D3D11_PARAMETER_DESC vertexShaderOutputParameters[] =
            {
                {"outputTex",  "TEXCOORD0",   D3D_SVT_FLOAT, D3D_SVC_VECTOR, 1, 2, D3D_INTERPOLATION_UNDEFINED, D3D_PF_OUT, 0, 0, 0, 0},
                {"outputNorm", "NORMAL0",     D3D_SVT_FLOAT, D3D_SVC_VECTOR, 1, 3, D3D_INTERPOLATION_UNDEFINED, D3D_PF_OUT, 0, 0, 0, 0},
                {"outputPos",  "SV_POSITION", D3D_SVT_FLOAT, D3D_SVC_VECTOR, 1, 4, D3D_INTERPOLATION_UNDEFINED, D3D_PF_OUT, 0, 0, 0, 0}
            };
            ComPtr<ID3D11LinkingNode> vertexShaderOutputNode;
            LinkingThrowIfFailed(vertexShaderGraph->SetOutputSignature(vertexShaderOutputParameters, ARRAYSIZE(vertexShaderOutputParameters), 
                &vertexShaderOutputNode), vertexShaderGraph.Get());
```



Nehmen Sie Aufrufe an [**ID3D11FunctionLinkingGraph::P assvalue**](/windows/desktop/api/d3d11shader/nf-d3d11shader-id3d11functionlinkinggraph-passvalue) an, um Werte vom Knoten für die Haupt-Vertex-Shader-Funktion an den Ausgabe Knoten zu übergeben.


```C++
            LinkingThrowIfFailed(vertexShaderGraph->PassValue(vertexFunctionCallNode.Get(), 0, vertexShaderOutputNode.Get(), 2), 
                vertexShaderGraph.Get());
            LinkingThrowIfFailed(vertexShaderGraph->PassValue(vertexFunctionCallNode.Get(), 1, vertexShaderOutputNode.Get(), 0), 
                vertexShaderGraph.Get());
            LinkingThrowIfFailed(vertexShaderGraph->PassValue(vertexFunctionCallNode.Get(), 2, vertexShaderOutputNode.Get(), 1), 
                vertexShaderGraph.Get());
```



Aufrufen der [**ID3D11FunctionLinkingGraph:: kreatemoduleinstance**](/windows/desktop/api/d3d11shader/nf-d3d11shader-id3d11functionlinkinggraph-createmoduleinstance) -Methode zum Abschließen des Vertex-Shader-Diagramms.


```C++
            // Finalize the vertex shader graph.
            ComPtr<ID3D11ModuleInstance> vertexShaderGraphInstance;
            LinkingThrowIfFailed(vertexShaderGraph->CreateModuleInstance(&vertexShaderGraphInstance, nullptr), vertexShaderGraph.Get());
```



### <a name="2-link-the-vertex-shader"></a>2. verknüpfen Sie den Vertexshader.

Rufen Sie die [**D3DCreateLinker**](/windows/desktop/api/D3Dcompiler/nf-d3dcompiler-d3dcreatelinker) -Funktion auf, um einen Linker ([**ID3D11Linker**](/windows/desktop/api/d3d11shader/nn-d3d11shader-id3d11linker)) zu erstellen, den Sie verwenden können, um die Instanz der shaderbibliothek zu verknüpfen, die Sie beim [Verpacken einer shaderbibliothek](pachaging-a-shader-library.md) mit der Instanz des Vertex-shaderdiagramms erstellt haben, die Sie im vorherigen Schritt erstellt haben. Aufrufen der [**ID3D11Linker:: uselibrary**](/windows/desktop/api/d3d11shader/nf-d3d11shader-id3d11linker-uselibrary) -Methode, um die Shader-Bibliothek anzugeben, die für die Verknüpfung verwendet werden soll. Rufen Sie die [**ID3D11Linker:: Link**](/windows/desktop/api/d3d11shader/nf-d3d11shader-id3d11linker-link) -Methode auf, um die Shader-Bibliothek mit dem Vertexshader-Diagramm zu verknüpfen und einen Zeiger auf die [**ID3DBlob**](/previous-versions/windows/desktop/legacy/ff728743(v=vs.85)) -Schnittstelle zu erstellen, mit der Sie auf den kompilierten Scheitelpunkt-Shader-Code zugreifen können Sie können dann den kompilierten Scheitelpunkt-Shader-Code an die [**ID3D11Device:: anatevertexshader**](/windows/desktop/api/d3d11/nf-d3d11-id3d11device-createvertexshader) -Methode übergeben, um das Vertex-Shader-Objekt und die [**ID3D11Device:: kreateinputlayout**](/windows/desktop/api/d3d11/nf-d3d11-id3d11device-createinputlayout) -Methode zum Erstellen des Eingabe Layout-Objekts zu erstellen.


```C++
            // Create a linker and hook up the module instance.
            ComPtr<ID3D11Linker> linker;
            DX::ThrowIfFailed(D3DCreateLinker(&linker));
            DX::ThrowIfFailed(linker->UseLibrary(shaderLibraryInstance.Get()));

            // Link the vertex shader.
            ComPtr<ID3DBlob> errorBlob;
            if (FAILED(linker->Link(vertexShaderGraphInstance.Get(), "main", ("vs" + m_shaderModelSuffix).c_str(), 0, &vertexShaderBlob, 
                &errorBlob)))
            {
                throw errorBlob;
            }


    ComPtr<ID3D11VertexShader> vertexShader;
    DX::ThrowIfFailed(
        device->CreateVertexShader(
            vertexShaderBlob->GetBufferPointer(),
            vertexShaderBlob->GetBufferSize(),
            nullptr,
            &vertexShader
            )
        );
    context->VSSetShader(vertexShader.Get(), nullptr, 0);
    D3D11_INPUT_ELEMENT_DESC inputLayoutDesc[] =
    {
        { "POSITION", 0, DXGI_FORMAT_R32G32B32_FLOAT, 0, 0,  D3D11_INPUT_PER_VERTEX_DATA, 0 },
        { "TEXCOORD", 0, DXGI_FORMAT_R32G32_FLOAT,    0, 12, D3D11_INPUT_PER_VERTEX_DATA, 0 },
        { "NORMAL",   0, DXGI_FORMAT_R32G32B32_FLOAT, 0, 20, D3D11_INPUT_PER_VERTEX_DATA, 0 }
    };
    ComPtr<ID3D11InputLayout> inputLayout;
    DX::ThrowIfFailed(device->CreateInputLayout(inputLayoutDesc, ARRAYSIZE(inputLayoutDesc), vertexShaderBlob->GetBufferPointer(), vertexShaderBlob->GetBufferSize(), &inputLayout));
    context->IASetInputLayout(inputLayout.Get());
```



### <a name="3-construct-a-function-linking-graph-for-the-pixel-shader"></a>3. Erstellen eines funktionsverknüpfungs Diagramms für den Pixelshader.

Rufen Sie die [**D3DCreateFunctionLinkingGraph**](/windows/desktop/api/D3Dcompiler/nf-d3dcompiler-d3dcreatefunctionlinkinggraph) -Funktion auf, um ein funktionsverknüpfungs Diagramm ([**ID3D11FunctionLinkingGraph**](/windows/desktop/api/d3d11shader/nn-d3d11shader-id3d11functionlinkinggraph)) zu erstellen, das den Pixelshader darstellt.

Verwenden Sie ein Array von [**D3D11- \_ Parameter- \_ DESC**](/windows/desktop/api/d3d11shader/ns-d3d11shader-d3d11_parameter_desc) -Strukturen, um die Eingabeparameter für den Pixelshader zu definieren. Die Vertex-Shader-Stufe fügt die Eingabeparameter in den Pixelshader ein. Das Layout der Eingabeparameter des Pixel-Shaders entspricht dem Layout des Pixel-Shaders im kompilierten Code. Nachdem Sie die Eingabeparameter definiert haben, müssen Sie die [**ID3D11FunctionLinkingGraph:: abtinputsignature**](/windows/desktop/api/d3d11shader/nf-d3d11shader-id3d11functionlinkinggraph-setinputsignature) -Methode aufrufen, um den Eingabe Knoten ([**ID3D11LinkingNode**](/windows/desktop/api/d3d11shader/nn-d3d11shader-id3d11linkingnode)) für den Pixelshader zu definieren.


```C++
            ComPtr<ID3D11FunctionLinkingGraph> pixelShaderGraph;
            DX::ThrowIfFailed(D3DCreateFunctionLinkingGraph(0, &pixelShaderGraph));

            // Define the main input node which will be fed by the vertex shader pipeline stage.
            static const D3D11_PARAMETER_DESC pixelShaderInputParameters[] =
            {
                {"inputTex",  "TEXCOORD0",   D3D_SVT_FLOAT, D3D_SVC_VECTOR, 1, 2, D3D_INTERPOLATION_UNDEFINED, D3D_PF_IN, 0, 0, 0, 0},
                {"inputNorm", "NORMAL0",     D3D_SVT_FLOAT, D3D_SVC_VECTOR, 1, 3, D3D_INTERPOLATION_UNDEFINED, D3D_PF_IN, 0, 0, 0, 0},
                {"inputPos",  "SV_POSITION", D3D_SVT_FLOAT, D3D_SVC_VECTOR, 1, 4, D3D_INTERPOLATION_UNDEFINED, D3D_PF_IN, 0, 0, 0, 0}
            };
            ComPtr<ID3D11LinkingNode> pixelShaderInputNode;
            LinkingThrowIfFailed(pixelShaderGraph->SetInputSignature(pixelShaderInputParameters, ARRAYSIZE(pixelShaderInputParameters), 
                &pixelShaderInputNode), pixelShaderGraph.Get());
```



Rufen Sie die [**ID3D11FunctionLinkingGraph:: CallFunction**](/windows/desktop/api/d3d11shader/nf-d3d11shader-id3d11functionlinkinggraph-callfunction) -Methode auf, um einen Knoten für die Haupt-Pixelshader-Funktion zu erstellen, und führen Sie Aufrufe an [**ID3D11FunctionLinkingGraph::P assvalue**](/windows/desktop/api/d3d11shader/nf-d3d11shader-id3d11functionlinkinggraph-passvalue) aus, um Werte vom Eingabe Knoten an den Knoten für die Haupt Pixel-Shader-Funktion zu übergeben.


```C++
            // Create a node for the main ColorFunction call and connect it to the pixel shader inputs.
            ComPtr<ID3D11LinkingNode> colorValueNode;
            LinkingThrowIfFailed(pixelShaderGraph->CallFunction("", shaderLibrary.Get(), "ColorFunction", &colorValueNode), 
                pixelShaderGraph.Get());

            // Define the graph edges from the input node.
            LinkingThrowIfFailed(pixelShaderGraph->PassValue(pixelShaderInputNode.Get(), 0, colorValueNode.Get(), 0), 
                pixelShaderGraph.Get());
            LinkingThrowIfFailed(pixelShaderGraph->PassValue(pixelShaderInputNode.Get(), 1, colorValueNode.Get(), 1), 
                pixelShaderGraph.Get());
```



Verwenden Sie ein Array von [**D3D11- \_ Parameter- \_ DESC**](/windows/desktop/api/d3d11shader/ns-d3d11shader-d3d11_parameter_desc) -Strukturen, um die Ausgabeparameter für den Pixelshader zu definieren. Der Pixelshader fügt seine Ausgabeparameter in die [Ausgabe-Fusion-Phase](/windows/desktop/direct3d11/d3d10-graphics-programming-guide-output-merger-stage)ein. Nachdem Sie die Ausgabeparameter definiert haben, rufen Sie die [**ID3D11FunctionLinkingGraph:: setoutputsignature**](/windows/desktop/api/d3d11shader/nf-d3d11shader-id3d11functionlinkinggraph-setoutputsignature) -Methode auf, um den Ausgabe Knoten ([**ID3D11LinkingNode**](/windows/desktop/api/d3d11shader/nn-d3d11shader-id3d11linkingnode)) für den Pixelshader zu definieren und Aufrufe an [**ID3D11FunctionLinkingGraph::P assvalue**](/windows/desktop/api/d3d11shader/nf-d3d11shader-id3d11functionlinkinggraph-passvalue) vorzunehmen, um Werte von einem Pixelshader-Funktions Knoten an den Ausgabe Knoten zu übergeben.


```C++
            // Define the main output node which will feed the Output Merger pipeline stage.
            D3D11_PARAMETER_DESC pixelShaderOutputParameters[] =
            {
                {"outputColor", "SV_TARGET", D3D_SVT_FLOAT, D3D_SVC_VECTOR, 1, 4, D3D_INTERPOLATION_UNDEFINED, D3D_PF_OUT, 0, 0, 0, 0}
            };
            ComPtr<ID3D11LinkingNode> pixelShaderOutputNode;
            LinkingThrowIfFailed(pixelShaderGraph->SetOutputSignature(pixelShaderOutputParameters, ARRAYSIZE(pixelShaderOutputParameters), 
                &pixelShaderOutputNode), pixelShaderGraph.Get());
            LinkingThrowIfFailed(pixelShaderGraph->PassValue(fillAlphaCallNode.Get(), D3D_RETURN_PARAMETER_INDEX, pixelShaderOutputNode.Get(), 0), 
                pixelShaderGraph.Get());
```



Aufrufen der [**ID3D11FunctionLinkingGraph:: up-ModuleInstance**](/windows/desktop/api/d3d11shader/nf-d3d11shader-id3d11functionlinkinggraph-createmoduleinstance) -Methode zum Abschließen des Pixel-shaderdiagramms.


```C++
            // Finalize the pixel shader graph.
            ComPtr<ID3D11ModuleInstance> pixelShaderGraphInstance;
            LinkingThrowIfFailed(pixelShaderGraph->CreateModuleInstance(&pixelShaderGraphInstance, nullptr), pixelShaderGraph.Get());
```



### <a name="4-link-the-pixel-shader"></a>4. verknüpfen Sie den Pixelshader.

Rufen Sie die [**D3DCreateLinker**](/windows/desktop/api/D3Dcompiler/nf-d3dcompiler-d3dcreatelinker) -Funktion auf, um einen Linker ([**ID3D11Linker**](/windows/desktop/api/d3d11shader/nn-d3d11shader-id3d11linker)) zu erstellen, den Sie verwenden können, um die Instanz der shaderbibliothek zu verknüpfen, die Sie beim [Verpacken einer shaderbibliothek](pachaging-a-shader-library.md) mit der Instanz des pixelshaderdiagramms erstellt haben, die Sie im vorherigen Schritt erstellt haben. Aufrufen der [**ID3D11Linker:: uselibrary**](/windows/desktop/api/d3d11shader/nf-d3d11shader-id3d11linker-uselibrary) -Methode, um die Shader-Bibliothek anzugeben, die für die Verknüpfung verwendet werden soll. Rufen Sie die [**ID3D11Linker:: Link**](/windows/desktop/api/d3d11shader/nf-d3d11shader-id3d11linker-link) -Methode auf, um die Shader-Bibliothek mit dem Pixel-Shader-Diagramm zu verknüpfen und einen Zeiger auf die [**ID3DBlob**](/previous-versions/windows/desktop/legacy/ff728743(v=vs.85)) -Schnittstelle zu erstellen, mit der Sie auf den kompilierten Pixel-Shader-Code zugreifen können Sie können dann den kompilierten Pixel-Shader-Code an die [**ID3D11Device:: anatepixelshader**](/windows/desktop/api/d3d11/nf-d3d11-id3d11device-createpixelshader) -Methode übergeben, um das Pixel-Shader-Objekt zu erstellen.


```C++
            // Create a linker and hook up the module instance.
            ComPtr<ID3D11Linker> linker;
            DX::ThrowIfFailed(D3DCreateLinker(&linker));
            DX::ThrowIfFailed(linker->UseLibrary(shaderLibraryInstance.Get()));

            // Link the pixel shader.
            ComPtr<ID3DBlob> errorBlob;
            if (FAILED(linker->Link(pixelShaderGraphInstance.Get(), "main", ("ps" + m_shaderModelSuffix).c_str(), 0, &pixelShaderBlob, &errorBlob)))
            {
                throw errorBlob;
            }


    ComPtr<ID3D11PixelShader> pixelShader;
    DX::ThrowIfFailed(
        device->CreatePixelShader(
            pixelShaderBlob->GetBufferPointer(),
            pixelShaderBlob->GetBufferSize(),
            nullptr,
            &pixelShader
            )
        );
    context->PSSetShader(pixelShader.Get(), nullptr, 0);
```



## <a name="summary"></a>Zusammenfassung

Wir haben die [**ID3D11FunctionLinkingGraph**](/windows/desktop/api/d3d11shader/nn-d3d11shader-id3d11functionlinkinggraph) -Methoden verwendet, um die Vertex-und Pixel-Shader-Diagramme zu erstellen und die Shader-Strukturprogramm gesteuert anzugeben.

Diese Diagramm Konstruktionen bestehen aus Sequenzen von vorkompilierten Funktionsaufrufen, die Werte an einander übergeben. FLG-Knoten ([**ID3D11LinkingNode**](/windows/desktop/api/d3d11shader/nn-d3d11shader-id3d11linkingnode)) stellen Eingabe-und Ausgabe-Shader-Knoten und Aufrufe von vorkompilierten Bibliotheksfunktionen dar. Die Reihenfolge, in der Sie die Funktionsaufruf Knoten registrieren, definiert die Abfolge der Aufrufe. Sie müssen zuerst den Eingabe Knoten ([**ID3D11FunctionLinkingGraph:: setinputsignature**](/windows/desktop/api/d3d11shader/nf-d3d11shader-id3d11functionlinkinggraph-setinputsignature)) und den Ausgabe Knoten ([**ID3D11FunctionLinkingGraph:: setoutputsignature**](/windows/desktop/api/d3d11shader/nf-d3d11shader-id3d11functionlinkinggraph-setoutputsignature)) angeben. FLG-Kanten definieren, wie Werte von einem Knoten an einen anderen übermittelt werden. Die Datentypen der bestandenen Werte müssen identisch sein. Es gibt keine implizite Typkonvertierung. Shape-und swishingregeln folgen dem HLSL-Verhalten. Werte können nur in dieser Reihenfolge weitergegeben werden.

Wir haben auch [**ID3D11Linker**](/windows/desktop/api/d3d11shader/nn-d3d11shader-id3d11linker) -Methoden verwendet, um die Shader-Bibliothek mit den shaderdiagrammen zu verknüpfen und Shader-blobtypen für die zu verwendende Direct3D-Laufzeit zu erzeugen.

Herzlichen Glückwunsch! Sie sind jetzt bereit, die Shader-Verknüpfung in ihren eigenen apps zu verwenden.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Verwenden der Shader-Verknüpfung](using-shader-linking.md)
</dt> </dl>

 

 