---
title: Kompilieren von Shadern
description: Sehen wir uns nun verschiedene Möglichkeiten zum Kompilieren Ihres shadercodes und Konventionen für Dateierweiterungen für Shader-Code an.
ms.assetid: a4e6b7cd-c5cc-4165-ba73-205155e449c9
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 3ea71da99dd68769324b07d3fc76a0c5ca00009d
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "104315525"
---
# <a name="compiling-shaders"></a><span data-ttu-id="41f85-103">Kompilieren von Shadern</span><span class="sxs-lookup"><span data-stu-id="41f85-103">Compiling shaders</span></span>

> [!NOTE]
> <span data-ttu-id="41f85-104">In diesem Thema wird der Compiler behandelt, der `FXC.EXE` für Shader-Modelle 2 bis 5,1 verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="41f85-104">This topic covers the `FXC.EXE` compiler used for Shader Models 2 through 5.1.</span></span> <span data-ttu-id="41f85-105">Für Shader Model 6 verwenden Sie `DXC.EXE` stattdessen, das unter [Verwenden von dxc.exe und dxcompiler.dll](https://github.com/microsoft/DirectXShaderCompiler/wiki/Using-dxc.exe-and-dxcompiler.dll)dokumentiert ist.</span><span class="sxs-lookup"><span data-stu-id="41f85-105">For Shader Model 6, you use `DXC.EXE` instead, which is documented in [Using dxc.exe and dxcompiler.dll](https://github.com/microsoft/DirectXShaderCompiler/wiki/Using-dxc.exe-and-dxcompiler.dll).</span></span>

<span data-ttu-id="41f85-106">Microsoft Visual Studio 2012 kann nun Shader-Code aus \* . HLSL-Dateien kompilieren, die Sie in das C++-Projekt einschließen.</span><span class="sxs-lookup"><span data-stu-id="41f85-106">Microsoft Visual Studio 2012 can now compile shader code from \*.hlsl files that you include in your C++ project.</span></span>

<span data-ttu-id="41f85-107">Im Rahmen des Buildprozesses verwendet Visual Studio 2012 den [fxc.exe](/windows/desktop/direct3dtools/fxc) HLSL-Code Compiler zum Kompilieren der HLSL-Dateien in binäre shaderobjektdateien oder in Byte Arrays, die in Header Dateien definiert sind.</span><span class="sxs-lookup"><span data-stu-id="41f85-107">As part of the build process, Visual Studio 2012 uses the [fxc.exe](/windows/desktop/direct3dtools/fxc) HLSL code compiler to compile the .hlsl files into binary shader object files or into byte arrays that are defined in header files.</span></span> <span data-ttu-id="41f85-108">Wie der HLSL-Code Compiler jede HLSL-Datei in Ihrem Projekt kompiliert, hängt davon ab, wie Sie die **Ouput files** -Eigenschaft für diese Datei angeben.</span><span class="sxs-lookup"><span data-stu-id="41f85-108">How the HLSL code compiler compiles each .hlsl file in your project depends on how you specify the **Ouput Files** property for that file.</span></span> <span data-ttu-id="41f85-109">Weitere Informationen zu Eigenschaften Seiten von HLSL finden Sie unter [HLSL-Eigenschaften Seiten](/previous-versions/visualstudio/visual-studio-2012/jj620902(v=vs.110)).</span><span class="sxs-lookup"><span data-stu-id="41f85-109">For more info about HLSL property pages, see [HLSL Property Pages](/previous-versions/visualstudio/visual-studio-2012/jj620902(v=vs.110)).</span></span>

<span data-ttu-id="41f85-110">Die Kompilierungs Methode, die Sie verwenden, hängt in der Regel von der Größe Ihrer \* HLSL-Datei ab.</span><span class="sxs-lookup"><span data-stu-id="41f85-110">The compile method that you use typically depends on the size of your \*.hlsl file.</span></span> <span data-ttu-id="41f85-111">Wenn Sie eine große Menge an Bytecode in einen Header einschließen, erhöhen Sie die Größe und die anfängliche Ladezeit Ihrer APP.</span><span class="sxs-lookup"><span data-stu-id="41f85-111">If you include a large amount of byte code in a header, you increase the size and the initial load time of your app.</span></span> <span data-ttu-id="41f85-112">Außerdem erzwingen Sie, dass sämtlicher Bytecode auch nach der Erstellung des Shaders im Speicher gespeichert wird, wodurch Ressourcen verschwendet werden.</span><span class="sxs-lookup"><span data-stu-id="41f85-112">You also force all byte code to reside in memory even after the shader is created, which wastes resources.</span></span> <span data-ttu-id="41f85-113">Wenn Sie jedoch Bytecode in einen Header einschließen, können Sie die Codekomplexität verringern und die Shader-Erstellung vereinfachen.</span><span class="sxs-lookup"><span data-stu-id="41f85-113">But when you include byte code in a header, you can reduce code complexity and simplify shader creation.</span></span>

<span data-ttu-id="41f85-114">Sehen wir uns nun verschiedene Möglichkeiten zum Kompilieren Ihres shadercodes und Konventionen für Dateierweiterungen für Shader-Code an.</span><span class="sxs-lookup"><span data-stu-id="41f85-114">Let's now look at various ways to compile your shader code and conventions for file extensions for shader code.</span></span>

-   [<span data-ttu-id="41f85-115">Verwenden von Shader-Code Dateierweiterungen</span><span class="sxs-lookup"><span data-stu-id="41f85-115">Using shader code file extensions</span></span>](#using-shader-code-file-extensions)
-   [<span data-ttu-id="41f85-116">Kompilieren bei Buildzeit in Objektdateien</span><span class="sxs-lookup"><span data-stu-id="41f85-116">Compiling at build time to object files</span></span>](#compiling-at-build-time-to-object-files)
-   [<span data-ttu-id="41f85-117">Kompilieren bei Buildzeit in Header Dateien</span><span class="sxs-lookup"><span data-stu-id="41f85-117">Compiling at build time to header files</span></span>](#compiling-at-build-time-to-header-files)
-   [<span data-ttu-id="41f85-118">Kompilieren mit D3DCompileFromFile</span><span class="sxs-lookup"><span data-stu-id="41f85-118">Compiling with D3DCompileFromFile</span></span>](#compiling-with-d3dcompilefromfile)
-   [<span data-ttu-id="41f85-119">Verwandte Themen</span><span class="sxs-lookup"><span data-stu-id="41f85-119">Related Topics</span></span>](#related-topics)
-   [<span data-ttu-id="41f85-120">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="41f85-120">Related topics</span></span>](#related-topics)

## <a name="using-shader-code-file-extensions"></a><span data-ttu-id="41f85-121">Verwenden von Shader-Code Dateierweiterungen</span><span class="sxs-lookup"><span data-stu-id="41f85-121">Using shader code file extensions</span></span>

<span data-ttu-id="41f85-122">Um die Microsoft-Konvention einzuhalten, verwenden Sie diese Dateierweiterungen für den Shader-Code:</span><span class="sxs-lookup"><span data-stu-id="41f85-122">To conform to Microsoft convention, use these file extensions for your shader code:</span></span>

-   <span data-ttu-id="41f85-123">Eine Datei mit der Erweiterung. HLSL enthält einen[HLSL](dx-graphics-hlsl-reference.md)-Quellcode (High Level Shading Language).</span><span class="sxs-lookup"><span data-stu-id="41f85-123">A file with the .hlsl extension holds High Level Shading Language ([HLSL](dx-graphics-hlsl-reference.md)) source code.</span></span>
-   <span data-ttu-id="41f85-124">Eine Datei mit der Erweiterung. CSO enthält ein kompiliertes Shader-Objekt.</span><span class="sxs-lookup"><span data-stu-id="41f85-124">A file with the .cso extension holds a compiled shader object.</span></span>
-   <span data-ttu-id="41f85-125">Eine Datei mit der Erweiterung ". h" ist eine Header Datei, aber in einem Shader-Code Kontext definiert diese Header Datei ein Bytearray, das Shader-Daten enthält.</span><span class="sxs-lookup"><span data-stu-id="41f85-125">A file with the .h extension is a header file, but in a shader code context, this header file defines a byte array that holds shader data.</span></span>

## <a name="compiling-at-build-time-to-object-files"></a><span data-ttu-id="41f85-126">Kompilieren bei Buildzeit in Objektdateien</span><span class="sxs-lookup"><span data-stu-id="41f85-126">Compiling at build time to object files</span></span>

<span data-ttu-id="41f85-127">Wenn Sie die HLSL-Dateien in binäre shaderobjektdateien kompilieren, muss Ihre APP die Daten aus diesen Objektdateien lesen (. CSO ist die Standard Erweiterung für diese Objektdateien), die Daten Byte Arrays zuweisen und aus diesen Byte Arrays Shader-Objekte erstellen.</span><span class="sxs-lookup"><span data-stu-id="41f85-127">If you compile your .hlsl files into binary shader object files, your app needs to read the data from those object files (.cso is the default extension for these object files), assign the data to byte arrays, and create shader objects from those byte arrays.</span></span> <span data-ttu-id="41f85-128">Um z. b. einen Vertex-Shader ([**ID3D11VertexShader**](/windows/desktop/api/d3d11/nn-d3d11-id3d11vertexshader)) zu erstellen \* \* , rufen Sie die [**ID3D11Device:: kreatevertexshader**](/windows/desktop/api/d3d11/nf-d3d11-id3d11device-createvertexshader) -Methode mit einem Bytearray auf, das kompilierten Vertex-Shader-Bytecode enthält.</span><span class="sxs-lookup"><span data-stu-id="41f85-128">For example, to create a vertex shader ([**ID3D11VertexShader**](/windows/desktop/api/d3d11/nn-d3d11-id3d11vertexshader)\*\*), call the [**ID3D11Device::CreateVertexShader**](/windows/desktop/api/d3d11/nf-d3d11-id3d11device-createvertexshader) method with a byte array that contains compiled vertex shader byte code.</span></span> <span data-ttu-id="41f85-129">Das [Direct3D Tutorial-Beispiel](https://github.com/microsoftarchive/msdn-code-gallery-microsoft/tree/master/Official%20Windows%20Platform%20Sample/Direct3D%20tutorial%20sample) veranschaulicht, wie shaderobjekte aus Byte Arrays erstellt werden, die von CSO-Binär-shaderobjektdateien abgerufen wurden.</span><span class="sxs-lookup"><span data-stu-id="41f85-129">The [Direct3D tutorial sample](https://github.com/microsoftarchive/msdn-code-gallery-microsoft/tree/master/Official%20Windows%20Platform%20Sample/Direct3D%20tutorial%20sample) shows how to create shader objects from byte arrays that it obtained from .cso binary shader object files.</span></span> <span data-ttu-id="41f85-130">In diesem Beispielcode aus dem [Direct3D-tutorialbeispiel](https://github.com/microsoftarchive/msdn-code-gallery-microsoft/tree/master/Official%20Windows%20Platform%20Sample/Direct3D%20tutorial%20sample)gibt die **Ouput files** -Eigenschaft für die simplevertexshader. HLSL-Datei an, dass in die simplevertexshader. CSO-Objektdatei kompiliert werden soll.</span><span class="sxs-lookup"><span data-stu-id="41f85-130">In this example code from the [Direct3D tutorial sample](https://github.com/microsoftarchive/msdn-code-gallery-microsoft/tree/master/Official%20Windows%20Platform%20Sample/Direct3D%20tutorial%20sample), the **Ouput Files** property for the SimpleVertexShader.hlsl file specifies to compile into the SimpleVertexShader.cso object file.</span></span>

```cpp
        auto vertexShaderBytecode = reader->ReadData("SimpleVertexShader.cso");
        ComPtr<ID3D11VertexShader> vertexShader;
        DX::ThrowIfFailed(
            m_d3dDevice->CreateVertexShader(
                vertexShaderBytecode->Data,
                vertexShaderBytecode->Length,
                nullptr,
                &vertexShader
                )
```

## <a name="compiling-at-build-time-to-header-files"></a><span data-ttu-id="41f85-131">Kompilieren bei Buildzeit in Header Dateien</span><span class="sxs-lookup"><span data-stu-id="41f85-131">Compiling at build time to header files</span></span>

<span data-ttu-id="41f85-132">Wenn Sie die HLSL-Dateien in Byte Arrays kompilieren, die in Header Dateien definiert sind, müssen Sie diese Header Dateien in Ihren Code einschließen.</span><span class="sxs-lookup"><span data-stu-id="41f85-132">If you compile your .hlsl files into byte arrays that are defined in header files, you need to include those header files in your code.</span></span> <span data-ttu-id="41f85-133">Das [Beispiel für Medien Erweiterungen](https://github.com/microsoftarchive/msdn-code-gallery-microsoft/tree/master/Official%20Windows%20Platform%20Sample/Media%20extensions%20sample) veranschaulicht das Erstellen von shaderobjekten aus Byte Arrays, die in Header Dateien definiert sind und die Sie zum Zeitpunkt der Kompilierung in das Projekt einschließen.</span><span class="sxs-lookup"><span data-stu-id="41f85-133">The [Media extensions sample](https://github.com/microsoftarchive/msdn-code-gallery-microsoft/tree/master/Official%20Windows%20Platform%20Sample/Media%20extensions%20sample) shows how to create shader objects from byte arrays that are defined in header files and that you include in your project at compile time.</span></span> <span data-ttu-id="41f85-134">In diesem Beispielcode aus dem Beispiel für [Medien Erweiterungen](https://github.com/microsoftarchive/msdn-code-gallery-microsoft/tree/master/Official%20Windows%20Platform%20Sample/Media%20extensions%20sample)gibt die **Ouput files** -Eigenschaft für die PixelShader. HLSL-Datei an, dass die Kompilierung in das *g \_ psshader* -Bytearray erfolgt, das in der Header Datei "Pixelshader. h" definiert ist.</span><span class="sxs-lookup"><span data-stu-id="41f85-134">In this example code from the [Media extensions sample](https://github.com/microsoftarchive/msdn-code-gallery-microsoft/tree/master/Official%20Windows%20Platform%20Sample/Media%20extensions%20sample), the **Ouput Files** property for the PixelShader.hlsl file specifies to compile into the *g\_psshader* byte array that is defined in the PixelShader.h header file.</span></span>


```C++
#       include "PixelShader.h"
        ComPtr<ID3D11PixelShader> m_pPixelShader;
        hr = pDevice->CreatePixelShader(g_psshader, sizeof(g_psshader), nullptr, &m_pPixelShader);
```



## <a name="compiling-with-d3dcompilefromfile"></a><span data-ttu-id="41f85-135">Kompilieren mit D3DCompileFromFile</span><span class="sxs-lookup"><span data-stu-id="41f85-135">Compiling with D3DCompileFromFile</span></span>

<span data-ttu-id="41f85-136">Sie können auch die [**D3DCompileFromFile**](/windows/win32/api/d3dcompiler/nf-d3dcompiler-d3dcompilefromfile) -Funktion zur Laufzeit verwenden, um Shader-Code zu kompilieren.</span><span class="sxs-lookup"><span data-stu-id="41f85-136">You can also use the [**D3DCompileFromFile**](/windows/win32/api/d3dcompiler/nf-d3dcompiler-d3dcompilefromfile) function at run time to compile shader code.</span></span> <span data-ttu-id="41f85-137">Weitere Informationen hierzu finden Sie unter Gewusst [wie: Kompilieren eines Shaders](/windows/desktop/direct3d11/how-to--compile-a-shader).</span><span class="sxs-lookup"><span data-stu-id="41f85-137">For more info about how to do this, see [How To: Compile a Shader](/windows/desktop/direct3d11/how-to--compile-a-shader).</span></span>

> [!Note]  
> <span data-ttu-id="41f85-138">Windows Store-Apps unterstützen [**D3DCompileFromFile**](/windows/win32/api/d3dcompiler/nf-d3dcompiler-d3dcompilefromfile) für die Entwicklung, aber nicht für die Bereitstellung.</span><span class="sxs-lookup"><span data-stu-id="41f85-138">Windows Store apps support using [**D3DCompileFromFile**](/windows/win32/api/d3dcompiler/nf-d3dcompiler-d3dcompilefromfile) for development but not for deployment.</span></span>

 

## <a name="related-topics"></a><span data-ttu-id="41f85-139">Verwandte Themen</span><span class="sxs-lookup"><span data-stu-id="41f85-139">Related Topics</span></span>

[<span data-ttu-id="41f85-140">Programmieranleitung für HLSL</span><span class="sxs-lookup"><span data-stu-id="41f85-140">Programming Guide for HLSL</span></span>](dx-graphics-hlsl-pguide.md)


## <a name="related-topics"></a><span data-ttu-id="41f85-141">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="41f85-141">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="41f85-142">Programmieranleitung für HLSL</span><span class="sxs-lookup"><span data-stu-id="41f85-142">Programming Guide for HLSL</span></span>](dx-graphics-hlsl-pguide.md)
</dt> </dl>

 

 