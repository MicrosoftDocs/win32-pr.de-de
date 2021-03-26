---
title: Verpacken einer shaderbibliothek
description: Hier erfahren Sie, wie Sie den Shader-Code kompilieren, den kompilierten Code in eine shaderbibliothek laden und Ressourcen von Quell Slots an Ziel Slots binden.
ms.assetid: ED2EB1DE-3C25-4633-BFA7-C535ABBBAD28
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 90124ca9753a390b924d5ba702e1986e32eee9e5
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "104993558"
---
# <a name="packaging-a-shader-library"></a><span data-ttu-id="08d1b-103">Verpacken einer shaderbibliothek</span><span class="sxs-lookup"><span data-stu-id="08d1b-103">Packaging a shader library</span></span>

<span data-ttu-id="08d1b-104">Hier erfahren Sie, wie Sie den Shader-Code kompilieren, den kompilierten Code in eine shaderbibliothek laden und Ressourcen von Quell Slots an Ziel Slots binden.</span><span class="sxs-lookup"><span data-stu-id="08d1b-104">Here we show you how to compile your shader code, load the compiled code into a shader library, and bind resources from source slots to destination slots.</span></span>

<span data-ttu-id="08d1b-105">**Ziel:** Zum Verpacken einer shaderbibliothek, die für die Shader-Verknüpfung verwendet werden soll.</span><span class="sxs-lookup"><span data-stu-id="08d1b-105">**Objective:** To package a shader library to use for shader linking.</span></span>

## <a name="prerequisites"></a><span data-ttu-id="08d1b-106">Voraussetzungen</span><span class="sxs-lookup"><span data-stu-id="08d1b-106">Prerequisites</span></span>

<span data-ttu-id="08d1b-107">Es wird davon ausgegangen, dass Sie mit C+ vertraut sind.</span><span class="sxs-lookup"><span data-stu-id="08d1b-107">We assume that you are familiar with C++.</span></span> <span data-ttu-id="08d1b-108">Sie müssen außerdem mit den grundlegenden Konzepten der Grafikprogrammierung vertraut sein.</span><span class="sxs-lookup"><span data-stu-id="08d1b-108">You also need basic experience with graphics programming concepts.</span></span>

<span data-ttu-id="08d1b-109">**Zeit bis zum Abschluss:** 30 Minuten.</span><span class="sxs-lookup"><span data-stu-id="08d1b-109">**Time to complete:** 30 minutes.</span></span>

## <a name="instructions"></a><span data-ttu-id="08d1b-110">Instructions</span><span class="sxs-lookup"><span data-stu-id="08d1b-110">Instructions</span></span>

### <a name="1-compiling-your-shader-code"></a><span data-ttu-id="08d1b-111">1. Kompilieren des Shader-Codes</span><span class="sxs-lookup"><span data-stu-id="08d1b-111">1. Compiling your shader code</span></span>

<span data-ttu-id="08d1b-112">Kompilieren Sie den Shader-Code mit einer der Kompilierungs Funktionen.</span><span class="sxs-lookup"><span data-stu-id="08d1b-112">Compile your shader code with one of the compile functions.</span></span> <span data-ttu-id="08d1b-113">Dieser Code Ausschnitt verwendet beispielsweise [**D3DCompile**](/windows/win32/api/d3dcompiler/nf-d3dcompiler-d3dcompile).</span><span class="sxs-lookup"><span data-stu-id="08d1b-113">For example, this code snippet uses [**D3DCompile**](/windows/win32/api/d3dcompiler/nf-d3dcompiler-d3dcompile).</span></span>

```cpp
    string source;
 
    ComPtr<ID3DBlob> codeBlob;
    ComPtr<ID3DBlob> errorBlob;
    HRESULT hr = D3DCompile(
        source.c_str(),
        source.size(),
        "ShaderModule",
        NULL,
        NULL,
        NULL,
        ("lib" + m_shaderModelSuffix).c_str(),
        D3DCOMPILE_OPTIMIZATION_LEVEL3,
        0,
        &codeBlob,
        &errorBlob
        );
```

<span data-ttu-id="08d1b-114">Die Quell Zeichenfolge enthält den nicht kompilierten ASCII-HLSL-Code.</span><span class="sxs-lookup"><span data-stu-id="08d1b-114">The source string contains the uncompiled ASCII HLSL code.</span></span>

### <a name="2-load-the-compiled-code-into-a-shader-library"></a><span data-ttu-id="08d1b-115">2. Laden Sie den kompilierten Code in eine Shader-Bibliothek.</span><span class="sxs-lookup"><span data-stu-id="08d1b-115">2. Load the compiled code into a shader library.</span></span>

<span data-ttu-id="08d1b-116">Aufrufen der [**D3DLoadModule**](/windows/desktop/api/D3Dcompiler/nf-d3dcompiler-d3dloadmodule) -Funktion, um den kompilierten Code ([**ID3DBlob**](/previous-versions/windows/desktop/legacy/ff728743(v=vs.85))) in ein Modul ([**ID3D11Module**](/windows/desktop/api/d3d11shader/nn-d3d11shader-id3d11module)) zu laden, das eine Shader-Bibliothek darstellt.</span><span class="sxs-lookup"><span data-stu-id="08d1b-116">Call the [**D3DLoadModule**](/windows/desktop/api/D3Dcompiler/nf-d3dcompiler-d3dloadmodule) function to load the compiled code ([**ID3DBlob**](/previous-versions/windows/desktop/legacy/ff728743(v=vs.85))) into a module ([**ID3D11Module**](/windows/desktop/api/d3d11shader/nn-d3d11shader-id3d11module)) that represents a shader library.</span></span>


```C++
    // Load the compiled library code into a module object.
    ComPtr<ID3D11Module> shaderLibrary;
    DX::ThrowIfFailed(D3DLoadModule(codeBlob->GetBufferPointer(), codeBlob->GetBufferSize(), &shaderLibrary));
```



### <a name="3-bind-resources-from-source-slots-to-destination-slots"></a><span data-ttu-id="08d1b-117">3. binden Sie Ressourcen von Quell Slots an Ziel Slots.</span><span class="sxs-lookup"><span data-stu-id="08d1b-117">3. Bind resources from source slots to destination slots.</span></span>

<span data-ttu-id="08d1b-118">Rufen Sie die [**ID3D11Module:: kreateinstance**](/windows/desktop/api/d3d11shader/nf-d3d11shader-id3d11module-createinstance) -Methode auf, um eine Instanz ([**ID3D11ModuleInstance**](/windows/desktop/api/d3d11shader/nn-d3d11shader-id3d11moduleinstance)) der Bibliothek zu erstellen, damit Sie dann Ressourcen Bindungen für die Instanz definieren können.</span><span class="sxs-lookup"><span data-stu-id="08d1b-118">Call the [**ID3D11Module::CreateInstance**](/windows/desktop/api/d3d11shader/nf-d3d11shader-id3d11module-createinstance) method to create an instance ([**ID3D11ModuleInstance**](/windows/desktop/api/d3d11shader/nn-d3d11shader-id3d11moduleinstance)) of the library so you can then define resource bindings for the instance.</span></span>

<span data-ttu-id="08d1b-119">Wenden Sie die Bind-Methoden von [**ID3D11ModuleInstance**](/windows/desktop/api/d3d11shader/nn-d3d11shader-id3d11moduleinstance) an, um die benötigten Ressourcen aus den Quell Slots an Ziel Slots zu binden.</span><span class="sxs-lookup"><span data-stu-id="08d1b-119">Call the bind methods of [**ID3D11ModuleInstance**](/windows/desktop/api/d3d11shader/nn-d3d11shader-id3d11moduleinstance) to bind the resources you need from source slots to destination slots.</span></span> <span data-ttu-id="08d1b-120">Die Ressourcen können Texturen, Puffer, Samplern, Konstante Puffer oder UAVs sein.</span><span class="sxs-lookup"><span data-stu-id="08d1b-120">The resources can be textures, buffers, samplers, constant buffers, or UAVs.</span></span> <span data-ttu-id="08d1b-121">In der Regel verwenden Sie die gleichen Slots wie die Quell Bibliothek.</span><span class="sxs-lookup"><span data-stu-id="08d1b-121">Typically, you will use the same slots as the source library.</span></span>


```C++
    // Create an instance of the library and define resource bindings for it.
    // In this sample we use the same slots as the source library however this is not required.
    ComPtr<ID3D11ModuleInstance> shaderLibraryInstance;
    DX::ThrowIfFailed(shaderLibrary->CreateInstance("", &shaderLibraryInstance));
    // HRESULTs for Bind methods are intentionally ignored as compiler optimizations may eliminate the source
    // bindings. In these cases, the Bind operation will fail, but the final shader will function normally.
    shaderLibraryInstance->BindResource(0, 0, 1);
    shaderLibraryInstance->BindSampler(0, 0, 1);
    shaderLibraryInstance->BindConstantBuffer(0, 0, 0);
    shaderLibraryInstance->BindConstantBuffer(1, 1, 0);
    shaderLibraryInstance->BindConstantBuffer(2, 2, 0);
```



<span data-ttu-id="08d1b-122">Dieser HLSL-Code zeigt, dass die Quell Bibliothek die gleichen Slots (T0, S0, B0, B1 und B2) wie die Slots verwendet, die in den vorhergehenden Bind-Methoden von [**ID3D11ModuleInstance**](/windows/desktop/api/d3d11shader/nn-d3d11shader-id3d11moduleinstance)verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="08d1b-122">This HLSL code shows that the source library uses the same slots (t0, s0, b0, b1, and b2) as the slots used in the preceding bind methods of [**ID3D11ModuleInstance**](/windows/desktop/api/d3d11shader/nn-d3d11shader-id3d11moduleinstance).</span></span>

``` syntax
// This is the default code in the fixed header section.
Texture2D<float3> Texture : register(t0);
SamplerState Anisotropic : register(s0);
cbuffer CameraData : register(b0)
{
    float4x4 Model;
    float4x4 View;
    float4x4 Projection;
};
cbuffer TimeVariantSignals : register(b1)
{
    float SineWave;
    float SquareWave;
    float TriangleWave;
    float SawtoothWave;
};

// This code is not displayed, but is used as part of the linking process.
cbuffer HiddenBuffer : register(b2)
{
    float3 LightDirection;
};
```

## <a name="summary-and-next-steps"></a><span data-ttu-id="08d1b-123">Zusammenfassung und nächste Schritte</span><span class="sxs-lookup"><span data-stu-id="08d1b-123">Summary and next steps</span></span>

<span data-ttu-id="08d1b-124">Wir haben Shader-Code kompiliert, den kompilierten Code in eine shaderbibliothek geladen und Ressourcen von Quell Slots an Ziel Slots gebunden.</span><span class="sxs-lookup"><span data-stu-id="08d1b-124">We compiled shader code, loaded the compiled code into a shader library, and bound resources from source slots to destination slots.</span></span>

<span data-ttu-id="08d1b-125">Im nächsten Schritt erstellen wir funktionsverknüpfungs Diagramme (FLGS) für Shader, verknüpfen Sie mit kompiliertem Code und erzeugen Shader-blobdateien, die von der Direct3D-Laufzeit verwendet werden können.</span><span class="sxs-lookup"><span data-stu-id="08d1b-125">Next we construct function-linking-graphs (FLGs) for shaders, link them to compiled code, and produce shader blobs that the Direct3D runtime can use.</span></span>

[<span data-ttu-id="08d1b-126">Erstellen eines funktionsverknüpfungs Diagramms und Verknüpfen dieses Diagramms mit kompiliertem Code</span><span class="sxs-lookup"><span data-stu-id="08d1b-126">Constructing a function-linking-graph and linking it to compiled code</span></span>](constructing-a-function-linking-graph.md)

## <a name="related-topics"></a><span data-ttu-id="08d1b-127">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="08d1b-127">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="08d1b-128">Verwenden der Shader-Verknüpfung</span><span class="sxs-lookup"><span data-stu-id="08d1b-128">Using shader linking</span></span>](using-shader-linking.md)
</dt> </dl>

 

 