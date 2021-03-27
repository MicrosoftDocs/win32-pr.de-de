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
# <a name="constructing-a-function-linking-graph-and-linking-it-to-compiled-code"></a><span data-ttu-id="5e98b-103">Erstellen eines funktionsverknüpfungs Diagramms und Verknüpfen dieses Diagramms mit kompiliertem Code</span><span class="sxs-lookup"><span data-stu-id="5e98b-103">Constructing a function-linking-graph and linking it to compiled code</span></span>

<span data-ttu-id="5e98b-104">Hier erfahren Sie, wie Sie Funktions Verknüpfungs Diagramme (FLGS) für Shader erstellen und diese Shader mit einer shaderbibliothek verknüpfen, um shaderblobfunktionen zu erzeugen, die von der Direct3D-Laufzeit verwendet werden können.</span><span class="sxs-lookup"><span data-stu-id="5e98b-104">Here we show you how to construct function-linking-graphs (FLGs) for shaders and how to link those shaders with a shader library to produce shader blobs that the Direct3D runtime can use.</span></span>

<span data-ttu-id="5e98b-105">**Ziel:** Zum Erstellen eines funktionsverknüpfungs Diagramms und Verknüpfen dieses Diagramms mit kompiliertem Code.</span><span class="sxs-lookup"><span data-stu-id="5e98b-105">**Objective:** To construct a function-linking-graph and link it to compiled code.</span></span>

## <a name="prerequisites"></a><span data-ttu-id="5e98b-106">Voraussetzungen</span><span class="sxs-lookup"><span data-stu-id="5e98b-106">Prerequisites</span></span>

<span data-ttu-id="5e98b-107">Es wird davon ausgegangen, dass Sie mit C+ vertraut sind.</span><span class="sxs-lookup"><span data-stu-id="5e98b-107">We assume that you are familiar with C++.</span></span> <span data-ttu-id="5e98b-108">Sie müssen außerdem mit den grundlegenden Konzepten der Grafikprogrammierung vertraut sein.</span><span class="sxs-lookup"><span data-stu-id="5e98b-108">You also need basic experience with graphics programming concepts.</span></span>

<span data-ttu-id="5e98b-109">Außerdem wird davon ausgegangen, dass Sie das [Packen einer shaderbibliothek](pachaging-a-shader-library.md)durchlaufen haben.</span><span class="sxs-lookup"><span data-stu-id="5e98b-109">We also assume that you went through [Packaging a shader library](pachaging-a-shader-library.md).</span></span>

<span data-ttu-id="5e98b-110">**Zeit bis zum Abschluss:** 30 Minuten.</span><span class="sxs-lookup"><span data-stu-id="5e98b-110">**Time to complete:** 30 minutes.</span></span>

## <a name="instructions"></a><span data-ttu-id="5e98b-111">Instructions</span><span class="sxs-lookup"><span data-stu-id="5e98b-111">Instructions</span></span>

### <a name="1-construct-a-function-linking-graph-for-the-vertex-shader"></a><span data-ttu-id="5e98b-112">1. Erstellen eines funktionsverknüpfungs Diagramms für den Vertex-Shader.</span><span class="sxs-lookup"><span data-stu-id="5e98b-112">1. Construct a function-linking-graph for the vertex shader.</span></span>

<span data-ttu-id="5e98b-113">Rufen Sie die [**D3DCreateFunctionLinkingGraph**](/windows/desktop/api/D3Dcompiler/nf-d3dcompiler-d3dcreatefunctionlinkinggraph) -Funktion auf, um ein Funktions Verknüpfungs Diagramm ([**ID3D11FunctionLinkingGraph**](/windows/desktop/api/d3d11shader/nn-d3d11shader-id3d11functionlinkinggraph)) zu erstellen, das den Scheitelpunkt Shader darstellt.</span><span class="sxs-lookup"><span data-stu-id="5e98b-113">Call the [**D3DCreateFunctionLinkingGraph**](/windows/desktop/api/D3Dcompiler/nf-d3dcompiler-d3dcreatefunctionlinkinggraph) function to create a function-linking-graph ([**ID3D11FunctionLinkingGraph**](/windows/desktop/api/d3d11shader/nn-d3d11shader-id3d11functionlinkinggraph)) to represent the vertex shader.</span></span>

<span data-ttu-id="5e98b-114">Verwenden Sie ein Array von [**D3D11- \_ Parameter- \_ DESC**](/windows/desktop/api/d3d11shader/ns-d3d11shader-d3d11_parameter_desc) -Strukturen, um die Eingabeparameter für den Vertex-Shader zu definieren.</span><span class="sxs-lookup"><span data-stu-id="5e98b-114">Use an array of [**D3D11\_PARAMETER\_DESC**](/windows/desktop/api/d3d11shader/ns-d3d11shader-d3d11_parameter_desc) structures to define the input parameters for the vertex shader.</span></span> <span data-ttu-id="5e98b-115">Die [Eingabe-Assembler-Phase](/windows/desktop/direct3d11/d3d10-graphics-programming-guide-input-assembler-stage) fügt die Eingabeparameter in den Vertexshader ein.</span><span class="sxs-lookup"><span data-stu-id="5e98b-115">The [Input-Assembler Stage](/windows/desktop/direct3d11/d3d10-graphics-programming-guide-input-assembler-stage) feeds the input parameters to the vertex shader.</span></span> <span data-ttu-id="5e98b-116">Das Layout der Eingabeparameter des Vertex-Shaders entspricht dem Layout des Vertexshaders im kompilierten Code.</span><span class="sxs-lookup"><span data-stu-id="5e98b-116">The layout of the vertex shader’s input parameters matches the layout of the vertex shader in the compiled code.</span></span> <span data-ttu-id="5e98b-117">Nachdem Sie die Eingabeparameter definiert haben, müssen Sie die [**ID3D11FunctionLinkingGraph:: abtinputsignature**](/windows/desktop/api/d3d11shader/nf-d3d11shader-id3d11functionlinkinggraph-setinputsignature) -Methode aufrufen, um den Eingabe Knoten ([**ID3D11LinkingNode**](/windows/desktop/api/d3d11shader/nn-d3d11shader-id3d11linkingnode)) für den Vertexshader zu definieren.</span><span class="sxs-lookup"><span data-stu-id="5e98b-117">After you define the input parameters, call the [**ID3D11FunctionLinkingGraph::SetInputSignature**](/windows/desktop/api/d3d11shader/nf-d3d11shader-id3d11functionlinkinggraph-setinputsignature) method to define the input node ([**ID3D11LinkingNode**](/windows/desktop/api/d3d11shader/nn-d3d11shader-id3d11linkingnode)) for the vertex shader.</span></span>


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



<span data-ttu-id="5e98b-118">Rufen Sie die [**ID3D11FunctionLinkingGraph:: CallFunction**](/windows/desktop/api/d3d11shader/nf-d3d11shader-id3d11functionlinkinggraph-callfunction) -Methode auf, um einen Knoten für die Haupt-Vertex-Shader-Funktion zu erstellen und Aufrufe an [**ID3D11FunctionLinkingGraph::P assvalue**](/windows/desktop/api/d3d11shader/nf-d3d11shader-id3d11functionlinkinggraph-passvalue) vorzunehmen, um Werte vom Eingabe Knoten an den Knoten für die Haupt-Vertex-Shader-Funktion zu übergeben.</span><span class="sxs-lookup"><span data-stu-id="5e98b-118">Call the [**ID3D11FunctionLinkingGraph::CallFunction**](/windows/desktop/api/d3d11shader/nf-d3d11shader-id3d11functionlinkinggraph-callfunction) method to create a node for the main vertex shader function and make calls to [**ID3D11FunctionLinkingGraph::PassValue**](/windows/desktop/api/d3d11shader/nf-d3d11shader-id3d11functionlinkinggraph-passvalue) to pass values from the input node to the node for the main vertex shader function.</span></span>


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



<span data-ttu-id="5e98b-119">Verwenden Sie ein Array von [**D3D11- \_ Parameter- \_ DESC**](/windows/desktop/api/d3d11shader/ns-d3d11shader-d3d11_parameter_desc) -Strukturen, um die Ausgabeparameter für den Vertex-Shader zu definieren.</span><span class="sxs-lookup"><span data-stu-id="5e98b-119">Use an array of [**D3D11\_PARAMETER\_DESC**](/windows/desktop/api/d3d11shader/ns-d3d11shader-d3d11_parameter_desc) structures to define the output parameters for the vertex shader.</span></span> <span data-ttu-id="5e98b-120">Der Vertex-Shader fügt seine Ausgabeparameter in den Pixelshader ein.</span><span class="sxs-lookup"><span data-stu-id="5e98b-120">The vertex shader feeds its output parameters to the pixel shader.</span></span> <span data-ttu-id="5e98b-121">Das Layout der Ausgabeparameter des Vertex-Shader entspricht dem Layout des Pixelshaders im kompilierten Code.</span><span class="sxs-lookup"><span data-stu-id="5e98b-121">The layout of the vertex shader’s output parameters matches the layout of the pixel shader in the compiled code.</span></span> <span data-ttu-id="5e98b-122">Nachdem Sie die Ausgabeparameter definiert haben, können Sie die [**ID3D11FunctionLinkingGraph:: setoutputsignature**](/windows/desktop/api/d3d11shader/nf-d3d11shader-id3d11functionlinkinggraph-setoutputsignature) -Methode aufrufen, um den Ausgabe Knoten ([**ID3D11LinkingNode**](/windows/desktop/api/d3d11shader/nn-d3d11shader-id3d11linkingnode)) für den Vertex-Shader zu definieren.</span><span class="sxs-lookup"><span data-stu-id="5e98b-122">After you define the output parameters, call the [**ID3D11FunctionLinkingGraph::SetOutputSignature**](/windows/desktop/api/d3d11shader/nf-d3d11shader-id3d11functionlinkinggraph-setoutputsignature) method to define the output node ([**ID3D11LinkingNode**](/windows/desktop/api/d3d11shader/nn-d3d11shader-id3d11linkingnode)) for the vertex shader.</span></span>


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



<span data-ttu-id="5e98b-123">Nehmen Sie Aufrufe an [**ID3D11FunctionLinkingGraph::P assvalue**](/windows/desktop/api/d3d11shader/nf-d3d11shader-id3d11functionlinkinggraph-passvalue) an, um Werte vom Knoten für die Haupt-Vertex-Shader-Funktion an den Ausgabe Knoten zu übergeben.</span><span class="sxs-lookup"><span data-stu-id="5e98b-123">Make calls to [**ID3D11FunctionLinkingGraph::PassValue**](/windows/desktop/api/d3d11shader/nf-d3d11shader-id3d11functionlinkinggraph-passvalue) to pass values from the node for the main vertex shader function to the output node.</span></span>


```C++
            LinkingThrowIfFailed(vertexShaderGraph->PassValue(vertexFunctionCallNode.Get(), 0, vertexShaderOutputNode.Get(), 2), 
                vertexShaderGraph.Get());
            LinkingThrowIfFailed(vertexShaderGraph->PassValue(vertexFunctionCallNode.Get(), 1, vertexShaderOutputNode.Get(), 0), 
                vertexShaderGraph.Get());
            LinkingThrowIfFailed(vertexShaderGraph->PassValue(vertexFunctionCallNode.Get(), 2, vertexShaderOutputNode.Get(), 1), 
                vertexShaderGraph.Get());
```



<span data-ttu-id="5e98b-124">Aufrufen der [**ID3D11FunctionLinkingGraph:: kreatemoduleinstance**](/windows/desktop/api/d3d11shader/nf-d3d11shader-id3d11functionlinkinggraph-createmoduleinstance) -Methode zum Abschließen des Vertex-Shader-Diagramms.</span><span class="sxs-lookup"><span data-stu-id="5e98b-124">Call the [**ID3D11FunctionLinkingGraph::CreateModuleInstance**](/windows/desktop/api/d3d11shader/nf-d3d11shader-id3d11functionlinkinggraph-createmoduleinstance) method to finalize the vertex shader graph.</span></span>


```C++
            // Finalize the vertex shader graph.
            ComPtr<ID3D11ModuleInstance> vertexShaderGraphInstance;
            LinkingThrowIfFailed(vertexShaderGraph->CreateModuleInstance(&vertexShaderGraphInstance, nullptr), vertexShaderGraph.Get());
```



### <a name="2-link-the-vertex-shader"></a><span data-ttu-id="5e98b-125">2. verknüpfen Sie den Vertexshader.</span><span class="sxs-lookup"><span data-stu-id="5e98b-125">2. Link the vertex shader</span></span>

<span data-ttu-id="5e98b-126">Rufen Sie die [**D3DCreateLinker**](/windows/desktop/api/D3Dcompiler/nf-d3dcompiler-d3dcreatelinker) -Funktion auf, um einen Linker ([**ID3D11Linker**](/windows/desktop/api/d3d11shader/nn-d3d11shader-id3d11linker)) zu erstellen, den Sie verwenden können, um die Instanz der shaderbibliothek zu verknüpfen, die Sie beim [Verpacken einer shaderbibliothek](pachaging-a-shader-library.md) mit der Instanz des Vertex-shaderdiagramms erstellt haben, die Sie im vorherigen Schritt erstellt haben.</span><span class="sxs-lookup"><span data-stu-id="5e98b-126">Call the [**D3DCreateLinker**](/windows/desktop/api/D3Dcompiler/nf-d3dcompiler-d3dcreatelinker) function to create a linker ([**ID3D11Linker**](/windows/desktop/api/d3d11shader/nn-d3d11shader-id3d11linker)) that you can use to link the instance of the shader library that you created in [Packaging a shader library](pachaging-a-shader-library.md) with the instance of the vertex shader graph that you created in the preceding step.</span></span> <span data-ttu-id="5e98b-127">Aufrufen der [**ID3D11Linker:: uselibrary**](/windows/desktop/api/d3d11shader/nf-d3d11shader-id3d11linker-uselibrary) -Methode, um die Shader-Bibliothek anzugeben, die für die Verknüpfung verwendet werden soll.</span><span class="sxs-lookup"><span data-stu-id="5e98b-127">Call the [**ID3D11Linker::UseLibrary**](/windows/desktop/api/d3d11shader/nf-d3d11shader-id3d11linker-uselibrary) method to specify the shader library to use for linking.</span></span> <span data-ttu-id="5e98b-128">Rufen Sie die [**ID3D11Linker:: Link**](/windows/desktop/api/d3d11shader/nf-d3d11shader-id3d11linker-link) -Methode auf, um die Shader-Bibliothek mit dem Vertexshader-Diagramm zu verknüpfen und einen Zeiger auf die [**ID3DBlob**](/previous-versions/windows/desktop/legacy/ff728743(v=vs.85)) -Schnittstelle zu erstellen, mit der Sie auf den kompilierten Scheitelpunkt-Shader-Code zugreifen können</span><span class="sxs-lookup"><span data-stu-id="5e98b-128">Call the [**ID3D11Linker::Link**](/windows/desktop/api/d3d11shader/nf-d3d11shader-id3d11linker-link) method to link the shader library with the vertex shader graph and to produce a pointer to the [**ID3DBlob**](/previous-versions/windows/desktop/legacy/ff728743(v=vs.85)) interface that you can use to access the compiled vertex shader code.</span></span> <span data-ttu-id="5e98b-129">Sie können dann den kompilierten Scheitelpunkt-Shader-Code an die [**ID3D11Device:: anatevertexshader**](/windows/desktop/api/d3d11/nf-d3d11-id3d11device-createvertexshader) -Methode übergeben, um das Vertex-Shader-Objekt und die [**ID3D11Device:: kreateinputlayout**](/windows/desktop/api/d3d11/nf-d3d11-id3d11device-createinputlayout) -Methode zum Erstellen des Eingabe Layout-Objekts zu erstellen.</span><span class="sxs-lookup"><span data-stu-id="5e98b-129">You can then pass this compiled vertex shader code to the [**ID3D11Device::CreateVertexShader**](/windows/desktop/api/d3d11/nf-d3d11-id3d11device-createvertexshader) method to create the vertex shader object and to the [**ID3D11Device::CreateInputLayout**](/windows/desktop/api/d3d11/nf-d3d11-id3d11device-createinputlayout) method to create the input-layout object.</span></span>


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



### <a name="3-construct-a-function-linking-graph-for-the-pixel-shader"></a><span data-ttu-id="5e98b-130">3. Erstellen eines funktionsverknüpfungs Diagramms für den Pixelshader.</span><span class="sxs-lookup"><span data-stu-id="5e98b-130">3. Construct a function-linking-graph for the pixel shader.</span></span>

<span data-ttu-id="5e98b-131">Rufen Sie die [**D3DCreateFunctionLinkingGraph**](/windows/desktop/api/D3Dcompiler/nf-d3dcompiler-d3dcreatefunctionlinkinggraph) -Funktion auf, um ein funktionsverknüpfungs Diagramm ([**ID3D11FunctionLinkingGraph**](/windows/desktop/api/d3d11shader/nn-d3d11shader-id3d11functionlinkinggraph)) zu erstellen, das den Pixelshader darstellt.</span><span class="sxs-lookup"><span data-stu-id="5e98b-131">Call the [**D3DCreateFunctionLinkingGraph**](/windows/desktop/api/D3Dcompiler/nf-d3dcompiler-d3dcreatefunctionlinkinggraph) function to create a function-linking-graph ([**ID3D11FunctionLinkingGraph**](/windows/desktop/api/d3d11shader/nn-d3d11shader-id3d11functionlinkinggraph)) to represent the pixel shader.</span></span>

<span data-ttu-id="5e98b-132">Verwenden Sie ein Array von [**D3D11- \_ Parameter- \_ DESC**](/windows/desktop/api/d3d11shader/ns-d3d11shader-d3d11_parameter_desc) -Strukturen, um die Eingabeparameter für den Pixelshader zu definieren.</span><span class="sxs-lookup"><span data-stu-id="5e98b-132">Use an array of [**D3D11\_PARAMETER\_DESC**](/windows/desktop/api/d3d11shader/ns-d3d11shader-d3d11_parameter_desc) structures to define the input parameters for the pixel shader.</span></span> <span data-ttu-id="5e98b-133">Die Vertex-Shader-Stufe fügt die Eingabeparameter in den Pixelshader ein.</span><span class="sxs-lookup"><span data-stu-id="5e98b-133">The vertex shader stage feeds the input parameters to the pixel shader.</span></span> <span data-ttu-id="5e98b-134">Das Layout der Eingabeparameter des Pixel-Shaders entspricht dem Layout des Pixel-Shaders im kompilierten Code.</span><span class="sxs-lookup"><span data-stu-id="5e98b-134">The layout of the pixel shader’s input parameters matches the layout of the pixel shader in the compiled code.</span></span> <span data-ttu-id="5e98b-135">Nachdem Sie die Eingabeparameter definiert haben, müssen Sie die [**ID3D11FunctionLinkingGraph:: abtinputsignature**](/windows/desktop/api/d3d11shader/nf-d3d11shader-id3d11functionlinkinggraph-setinputsignature) -Methode aufrufen, um den Eingabe Knoten ([**ID3D11LinkingNode**](/windows/desktop/api/d3d11shader/nn-d3d11shader-id3d11linkingnode)) für den Pixelshader zu definieren.</span><span class="sxs-lookup"><span data-stu-id="5e98b-135">After you define the input parameters, call the [**ID3D11FunctionLinkingGraph::SetInputSignature**](/windows/desktop/api/d3d11shader/nf-d3d11shader-id3d11functionlinkinggraph-setinputsignature) method to define the input node ([**ID3D11LinkingNode**](/windows/desktop/api/d3d11shader/nn-d3d11shader-id3d11linkingnode)) for the pixel shader.</span></span>


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



<span data-ttu-id="5e98b-136">Rufen Sie die [**ID3D11FunctionLinkingGraph:: CallFunction**](/windows/desktop/api/d3d11shader/nf-d3d11shader-id3d11functionlinkinggraph-callfunction) -Methode auf, um einen Knoten für die Haupt-Pixelshader-Funktion zu erstellen, und führen Sie Aufrufe an [**ID3D11FunctionLinkingGraph::P assvalue**](/windows/desktop/api/d3d11shader/nf-d3d11shader-id3d11functionlinkinggraph-passvalue) aus, um Werte vom Eingabe Knoten an den Knoten für die Haupt Pixel-Shader-Funktion zu übergeben.</span><span class="sxs-lookup"><span data-stu-id="5e98b-136">Call the [**ID3D11FunctionLinkingGraph::CallFunction**](/windows/desktop/api/d3d11shader/nf-d3d11shader-id3d11functionlinkinggraph-callfunction) method to create a node for the main pixel shader function and make calls to [**ID3D11FunctionLinkingGraph::PassValue**](/windows/desktop/api/d3d11shader/nf-d3d11shader-id3d11functionlinkinggraph-passvalue) to pass values from the input node to the node for the main pixel shader function.</span></span>


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



<span data-ttu-id="5e98b-137">Verwenden Sie ein Array von [**D3D11- \_ Parameter- \_ DESC**](/windows/desktop/api/d3d11shader/ns-d3d11shader-d3d11_parameter_desc) -Strukturen, um die Ausgabeparameter für den Pixelshader zu definieren.</span><span class="sxs-lookup"><span data-stu-id="5e98b-137">Use an array of [**D3D11\_PARAMETER\_DESC**](/windows/desktop/api/d3d11shader/ns-d3d11shader-d3d11_parameter_desc) structures to define the output parameters for the pixel shader.</span></span> <span data-ttu-id="5e98b-138">Der Pixelshader fügt seine Ausgabeparameter in die [Ausgabe-Fusion-Phase](/windows/desktop/direct3d11/d3d10-graphics-programming-guide-output-merger-stage)ein.</span><span class="sxs-lookup"><span data-stu-id="5e98b-138">The pixel shader feeds its output parameters to the [Output-Merger Stage](/windows/desktop/direct3d11/d3d10-graphics-programming-guide-output-merger-stage).</span></span> <span data-ttu-id="5e98b-139">Nachdem Sie die Ausgabeparameter definiert haben, rufen Sie die [**ID3D11FunctionLinkingGraph:: setoutputsignature**](/windows/desktop/api/d3d11shader/nf-d3d11shader-id3d11functionlinkinggraph-setoutputsignature) -Methode auf, um den Ausgabe Knoten ([**ID3D11LinkingNode**](/windows/desktop/api/d3d11shader/nn-d3d11shader-id3d11linkingnode)) für den Pixelshader zu definieren und Aufrufe an [**ID3D11FunctionLinkingGraph::P assvalue**](/windows/desktop/api/d3d11shader/nf-d3d11shader-id3d11functionlinkinggraph-passvalue) vorzunehmen, um Werte von einem Pixelshader-Funktions Knoten an den Ausgabe Knoten zu übergeben.</span><span class="sxs-lookup"><span data-stu-id="5e98b-139">After you define the output parameters, call the [**ID3D11FunctionLinkingGraph::SetOutputSignature**](/windows/desktop/api/d3d11shader/nf-d3d11shader-id3d11functionlinkinggraph-setoutputsignature) method to define the output node ([**ID3D11LinkingNode**](/windows/desktop/api/d3d11shader/nn-d3d11shader-id3d11linkingnode)) for the pixel shader and make calls to [**ID3D11FunctionLinkingGraph::PassValue**](/windows/desktop/api/d3d11shader/nf-d3d11shader-id3d11functionlinkinggraph-passvalue) to pass values from a pixel shader function node to the output node.</span></span>


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



<span data-ttu-id="5e98b-140">Aufrufen der [**ID3D11FunctionLinkingGraph:: up-ModuleInstance**](/windows/desktop/api/d3d11shader/nf-d3d11shader-id3d11functionlinkinggraph-createmoduleinstance) -Methode zum Abschließen des Pixel-shaderdiagramms.</span><span class="sxs-lookup"><span data-stu-id="5e98b-140">Call the [**ID3D11FunctionLinkingGraph::CreateModuleInstance**](/windows/desktop/api/d3d11shader/nf-d3d11shader-id3d11functionlinkinggraph-createmoduleinstance) method to finalize the pixel shader graph.</span></span>


```C++
            // Finalize the pixel shader graph.
            ComPtr<ID3D11ModuleInstance> pixelShaderGraphInstance;
            LinkingThrowIfFailed(pixelShaderGraph->CreateModuleInstance(&pixelShaderGraphInstance, nullptr), pixelShaderGraph.Get());
```



### <a name="4-link-the-pixel-shader"></a><span data-ttu-id="5e98b-141">4. verknüpfen Sie den Pixelshader.</span><span class="sxs-lookup"><span data-stu-id="5e98b-141">4. Link the pixel shader</span></span>

<span data-ttu-id="5e98b-142">Rufen Sie die [**D3DCreateLinker**](/windows/desktop/api/D3Dcompiler/nf-d3dcompiler-d3dcreatelinker) -Funktion auf, um einen Linker ([**ID3D11Linker**](/windows/desktop/api/d3d11shader/nn-d3d11shader-id3d11linker)) zu erstellen, den Sie verwenden können, um die Instanz der shaderbibliothek zu verknüpfen, die Sie beim [Verpacken einer shaderbibliothek](pachaging-a-shader-library.md) mit der Instanz des pixelshaderdiagramms erstellt haben, die Sie im vorherigen Schritt erstellt haben.</span><span class="sxs-lookup"><span data-stu-id="5e98b-142">Call the [**D3DCreateLinker**](/windows/desktop/api/D3Dcompiler/nf-d3dcompiler-d3dcreatelinker) function to create a linker ([**ID3D11Linker**](/windows/desktop/api/d3d11shader/nn-d3d11shader-id3d11linker)) that you can use to link the instance of the shader library that you created in [Packaging a shader library](pachaging-a-shader-library.md) with the instance of the pixel shader graph that you created in the preceding step.</span></span> <span data-ttu-id="5e98b-143">Aufrufen der [**ID3D11Linker:: uselibrary**](/windows/desktop/api/d3d11shader/nf-d3d11shader-id3d11linker-uselibrary) -Methode, um die Shader-Bibliothek anzugeben, die für die Verknüpfung verwendet werden soll.</span><span class="sxs-lookup"><span data-stu-id="5e98b-143">Call the [**ID3D11Linker::UseLibrary**](/windows/desktop/api/d3d11shader/nf-d3d11shader-id3d11linker-uselibrary) method to specify the shader library to use for linking.</span></span> <span data-ttu-id="5e98b-144">Rufen Sie die [**ID3D11Linker:: Link**](/windows/desktop/api/d3d11shader/nf-d3d11shader-id3d11linker-link) -Methode auf, um die Shader-Bibliothek mit dem Pixel-Shader-Diagramm zu verknüpfen und einen Zeiger auf die [**ID3DBlob**](/previous-versions/windows/desktop/legacy/ff728743(v=vs.85)) -Schnittstelle zu erstellen, mit der Sie auf den kompilierten Pixel-Shader-Code zugreifen können</span><span class="sxs-lookup"><span data-stu-id="5e98b-144">Call the [**ID3D11Linker::Link**](/windows/desktop/api/d3d11shader/nf-d3d11shader-id3d11linker-link) method to link the shader library with the pixel shader graph and to produce a pointer to the [**ID3DBlob**](/previous-versions/windows/desktop/legacy/ff728743(v=vs.85)) interface that you can use to access the compiled pixel shader code.</span></span> <span data-ttu-id="5e98b-145">Sie können dann den kompilierten Pixel-Shader-Code an die [**ID3D11Device:: anatepixelshader**](/windows/desktop/api/d3d11/nf-d3d11-id3d11device-createpixelshader) -Methode übergeben, um das Pixel-Shader-Objekt zu erstellen.</span><span class="sxs-lookup"><span data-stu-id="5e98b-145">You can then pass this compiled pixel shader code to the [**ID3D11Device::CreatePixelShader**](/windows/desktop/api/d3d11/nf-d3d11-id3d11device-createpixelshader) method to create the pixel shader object.</span></span>


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



## <a name="summary"></a><span data-ttu-id="5e98b-146">Zusammenfassung</span><span class="sxs-lookup"><span data-stu-id="5e98b-146">Summary</span></span>

<span data-ttu-id="5e98b-147">Wir haben die [**ID3D11FunctionLinkingGraph**](/windows/desktop/api/d3d11shader/nn-d3d11shader-id3d11functionlinkinggraph) -Methoden verwendet, um die Vertex-und Pixel-Shader-Diagramme zu erstellen und die Shader-Strukturprogramm gesteuert anzugeben.</span><span class="sxs-lookup"><span data-stu-id="5e98b-147">We used the [**ID3D11FunctionLinkingGraph**](/windows/desktop/api/d3d11shader/nn-d3d11shader-id3d11functionlinkinggraph) methods to construct the vertex and pixel shader graphs and to specify the shader structure programmatically.</span></span>

<span data-ttu-id="5e98b-148">Diese Diagramm Konstruktionen bestehen aus Sequenzen von vorkompilierten Funktionsaufrufen, die Werte an einander übergeben.</span><span class="sxs-lookup"><span data-stu-id="5e98b-148">These graph constructions consist of sequences of precompiled function calls that pass values to each other.</span></span> <span data-ttu-id="5e98b-149">FLG-Knoten ([**ID3D11LinkingNode**](/windows/desktop/api/d3d11shader/nn-d3d11shader-id3d11linkingnode)) stellen Eingabe-und Ausgabe-Shader-Knoten und Aufrufe von vorkompilierten Bibliotheksfunktionen dar.</span><span class="sxs-lookup"><span data-stu-id="5e98b-149">FLG nodes ([**ID3D11LinkingNode**](/windows/desktop/api/d3d11shader/nn-d3d11shader-id3d11linkingnode)) represent input and output shader nodes and invocations of precompiled library functions.</span></span> <span data-ttu-id="5e98b-150">Die Reihenfolge, in der Sie die Funktionsaufruf Knoten registrieren, definiert die Abfolge der Aufrufe.</span><span class="sxs-lookup"><span data-stu-id="5e98b-150">The order in which you register the function-call nodes defines the sequence of invocations.</span></span> <span data-ttu-id="5e98b-151">Sie müssen zuerst den Eingabe Knoten ([**ID3D11FunctionLinkingGraph:: setinputsignature**](/windows/desktop/api/d3d11shader/nf-d3d11shader-id3d11functionlinkinggraph-setinputsignature)) und den Ausgabe Knoten ([**ID3D11FunctionLinkingGraph:: setoutputsignature**](/windows/desktop/api/d3d11shader/nf-d3d11shader-id3d11functionlinkinggraph-setoutputsignature)) angeben.</span><span class="sxs-lookup"><span data-stu-id="5e98b-151">You must specify the input node ([**ID3D11FunctionLinkingGraph::SetInputSignature**](/windows/desktop/api/d3d11shader/nf-d3d11shader-id3d11functionlinkinggraph-setinputsignature)) first and the output node last ([**ID3D11FunctionLinkingGraph::SetOutputSignature**](/windows/desktop/api/d3d11shader/nf-d3d11shader-id3d11functionlinkinggraph-setoutputsignature)).</span></span> <span data-ttu-id="5e98b-152">FLG-Kanten definieren, wie Werte von einem Knoten an einen anderen übermittelt werden.</span><span class="sxs-lookup"><span data-stu-id="5e98b-152">FLG edges define how values are passed from one node to another.</span></span> <span data-ttu-id="5e98b-153">Die Datentypen der bestandenen Werte müssen identisch sein. Es gibt keine implizite Typkonvertierung.</span><span class="sxs-lookup"><span data-stu-id="5e98b-153">The data types of passed values must be the same; there is no implicit type conversion.</span></span> <span data-ttu-id="5e98b-154">Shape-und swishingregeln folgen dem HLSL-Verhalten.</span><span class="sxs-lookup"><span data-stu-id="5e98b-154">Shape and swizzling rules follow the HLSL behavior.</span></span> <span data-ttu-id="5e98b-155">Werte können nur in dieser Reihenfolge weitergegeben werden.</span><span class="sxs-lookup"><span data-stu-id="5e98b-155">Values can only be passed forward in this sequence.</span></span>

<span data-ttu-id="5e98b-156">Wir haben auch [**ID3D11Linker**](/windows/desktop/api/d3d11shader/nn-d3d11shader-id3d11linker) -Methoden verwendet, um die Shader-Bibliothek mit den shaderdiagrammen zu verknüpfen und Shader-blobtypen für die zu verwendende Direct3D-Laufzeit zu erzeugen.</span><span class="sxs-lookup"><span data-stu-id="5e98b-156">We also used [**ID3D11Linker**](/windows/desktop/api/d3d11shader/nn-d3d11shader-id3d11linker) methods to link the shader library with the shader graphs and to produce shader blobs for the Direct3D runtime to use.</span></span>

<span data-ttu-id="5e98b-157">Herzlichen Glückwunsch!</span><span class="sxs-lookup"><span data-stu-id="5e98b-157">Congratulations!</span></span> <span data-ttu-id="5e98b-158">Sie sind jetzt bereit, die Shader-Verknüpfung in ihren eigenen apps zu verwenden.</span><span class="sxs-lookup"><span data-stu-id="5e98b-158">You are now ready to use shader linking in your own apps.</span></span>

## <a name="related-topics"></a><span data-ttu-id="5e98b-159">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="5e98b-159">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="5e98b-160">Verwenden der Shader-Verknüpfung</span><span class="sxs-lookup"><span data-stu-id="5e98b-160">Using shader linking</span></span>](using-shader-linking.md)
</dt> </dl>

 

 