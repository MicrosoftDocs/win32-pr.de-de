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
# <a name="using-shaders-in-direct3d-10"></a><span data-ttu-id="9c25f-103">Verwenden von Shadern in Direct3D 10</span><span class="sxs-lookup"><span data-stu-id="9c25f-103">Using Shaders in Direct3D 10</span></span>

<span data-ttu-id="9c25f-104">Die Pipeline verfügt über drei Shaderstufen, die jeweils mit einem HLSL-Shader programmiert sind.</span><span class="sxs-lookup"><span data-stu-id="9c25f-104">The pipeline has three shader stages and each one is programmed with an HLSL shader.</span></span> <span data-ttu-id="9c25f-105">Alle Direct3D 10-Shader sind in HLSL geschrieben und richten sich an Shadermodell 4.</span><span class="sxs-lookup"><span data-stu-id="9c25f-105">All Direct3D 10 shaders are written in HLSL, targeting shader model 4.</span></span>


<span data-ttu-id="9c25f-106">Unterschiede zwischen Direct3D 9 und Direct3D 10:</span><span class="sxs-lookup"><span data-stu-id="9c25f-106">Differences between Direct3D 9 and Direct3D 10:</span></span>

- <span data-ttu-id="9c25f-107">Im Gegensatz zu Direct3D 9-Shadermodellen, die in einer Zwischenassemblysprache erstellt werden können, werden Shadermodell 4.0-Shader nur in HLSL erstellt.</span><span class="sxs-lookup"><span data-stu-id="9c25f-107">Unlike Direct3D 9 shader models which could be authored in an intermediate assembly language, shader model 4.0 shaders are only authored in HLSL.</span></span> <span data-ttu-id="9c25f-108">Die Offlinekompilierung von Shadern in vom Gerät nutzbaren Bytecode wird weiterhin unterstützt und für die meisten Szenarien empfohlen.</span><span class="sxs-lookup"><span data-stu-id="9c25f-108">Offline compilation of shaders into device-consumable bytecode is still supported, and recommended for most scenarios.</span></span>



 

<span data-ttu-id="9c25f-109">In diesem Beispiel wird nur ein Vertex-Shader verwendet.</span><span class="sxs-lookup"><span data-stu-id="9c25f-109">This example uses only a vertex shader.</span></span> <span data-ttu-id="9c25f-110">Da alle Shader aus dem allgemeinen Shaderkern erstellt werden, ähnelt das Erlernen der Verwendung eines Vertex-Shaders der Verwendung eines Geometrie- oder Pixel-Shaders.</span><span class="sxs-lookup"><span data-stu-id="9c25f-110">Because all shaders are built from the common shader core, learning how to use a vertex shader is very similar to using a geometry or pixel shader.</span></span>

<span data-ttu-id="9c25f-111">Nachdem Sie einen HLSL-Shader erstellt haben (in diesem Beispiel wird der Scheitelpunkt-Shader HLSLWithoutFX.vsh verwendet), müssen Sie ihn für die jeweilige Pipelinephase vorbereiten, die ihn verwendet.</span><span class="sxs-lookup"><span data-stu-id="9c25f-111">Once you have authored an HLSL shader (this example uses the vertex shader HLSLWithoutFX.vsh), you will need to prepare it for the particular pipeline stage that will use it.</span></span> <span data-ttu-id="9c25f-112">Dazu müssen Sie:</span><span class="sxs-lookup"><span data-stu-id="9c25f-112">To do this you need to:</span></span>

-   [<span data-ttu-id="9c25f-113">Kompilieren eines Shaders</span><span class="sxs-lookup"><span data-stu-id="9c25f-113">Compile a Shader</span></span>](#compile-a-shader)
-   [<span data-ttu-id="9c25f-114">Erstellen eines Shaderobjekts</span><span class="sxs-lookup"><span data-stu-id="9c25f-114">Create a Shader Object</span></span>](#create-a-shader-object)
-   [<span data-ttu-id="9c25f-115">Festlegen des Shaderobjekts</span><span class="sxs-lookup"><span data-stu-id="9c25f-115">Set the Shader Object</span></span>](#set-the-shader-object)
-   [<span data-ttu-id="9c25f-116">Wiederholen für alle drei Shaderstufen</span><span class="sxs-lookup"><span data-stu-id="9c25f-116">Repeat for all 3 Shader Stages</span></span>](#repeat-for-all-3-shader-stages)

<span data-ttu-id="9c25f-117">Diese Schritte müssen für jeden Shader in der Pipeline wiederholt werden.</span><span class="sxs-lookup"><span data-stu-id="9c25f-117">These steps need to be repeated for each shader in the pipeline.</span></span>

## <a name="compile-a-shader"></a><span data-ttu-id="9c25f-118">Kompilieren eines Shaders</span><span class="sxs-lookup"><span data-stu-id="9c25f-118">Compile a Shader</span></span>

<span data-ttu-id="9c25f-119">Der erste Schritt besteht darin, den Shader zu kompilieren, um zu überprüfen, ob Sie die HLSL-Anweisungen ordnungsgemäß codiert haben.</span><span class="sxs-lookup"><span data-stu-id="9c25f-119">The first step is to compile the shader, to check to see that you have coded the HLSL statements correctly.</span></span> <span data-ttu-id="9c25f-120">Dazu wird D3D10CompileShader aufgerufen und mit mehreren Parametern angegeben, wie hier gezeigt:</span><span class="sxs-lookup"><span data-stu-id="9c25f-120">This is done by calling D3D10CompileShader and supplying it with several parameters as shown here:</span></span>


```
    IPD3D10Blob * pBlob;
    
        
    // Compile the vertex shader from the file
    D3D10CompileShader( strPath, strlen( strPath ), "HLSLWithoutFX.vsh", 
        NULL, NULL, "Ripple", "vs_4_0", dwShaderFlags, &pBlob, NULL );
```



<span data-ttu-id="9c25f-121">Diese Funktion verwendet die folgenden Parameter:</span><span class="sxs-lookup"><span data-stu-id="9c25f-121">This function takes the following parameters:</span></span>

-   <span data-ttu-id="9c25f-122">Der Name der Datei ( und die Länge der Namenszeichenfolge in Bytes ), die den Shader enthält.</span><span class="sxs-lookup"><span data-stu-id="9c25f-122">The name of the file ( and length of the name string in bytes ) that contains the shader.</span></span> <span data-ttu-id="9c25f-123">In diesem Beispiel wird nur ein Vertex-Shader verwendet (in der Datei HLSLWithoutFX.vsh, wobei die Dateierweiterung .vsh eine Abkürzung für vertex shader ist).</span><span class="sxs-lookup"><span data-stu-id="9c25f-123">This example uses a vertex shader only (in the file HLSLWithoutFX.vsh file where the file extension .vsh is an abbreviation for vertex shader).</span></span>
-   <span data-ttu-id="9c25f-124">Der Name der Shaderfunktion.</span><span class="sxs-lookup"><span data-stu-id="9c25f-124">The shader function name.</span></span> <span data-ttu-id="9c25f-125">In diesem Beispiel wird ein Vertex-Shader aus der Funktion "Pixels" kompiliert, der eine einzelne Eingabe annimmt und eine Ausgabestruktur zurückgibt (die Funktion stammt aus dem HLSLWithoutFX-Beispiel):</span><span class="sxs-lookup"><span data-stu-id="9c25f-125">This example compiles a vertex shader from the Ripple function which takes a single input and returns an output struct (the function is from the HLSLWithoutFX sample):</span></span>
    ```
    VS_OUTPUT Ripple( in float2 vPosition : POSITION )
    ```

    

-   <span data-ttu-id="9c25f-126">Ein Zeiger auf alle makros, die vom Shader verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="9c25f-126">A pointer to all macros used by the shader.</span></span> <span data-ttu-id="9c25f-127">Verwenden Sie D3D10 \_ SHADER \_ MACRO, um Ihre Makros zu definieren. Erstellen Sie einfach eine Namenszeichenfolge, die alle Makronamen enthält (wobei jeder Name durch ein Leerzeichen getrennt ist) und eine Definitionszeichenfolge (wobei jeder Makrotext durch ein Leerzeichen getrennt ist).</span><span class="sxs-lookup"><span data-stu-id="9c25f-127">Use D3D10\_SHADER\_MACRO to help define your macros; simply create a name string that contains all the macro names (with each name separated by a space) and a definition string (with each macro body separated by a space).</span></span> <span data-ttu-id="9c25f-128">Beide Zeichenfolgen müssen NULL-terminiert sein.</span><span class="sxs-lookup"><span data-stu-id="9c25f-128">Both strings need to be NULL terminated.</span></span>
-   <span data-ttu-id="9c25f-129">Ein Zeiger auf alle anderen Dateien, die Sie enthalten müssen, um Ihre Shader zum Kompilieren zu erhalten.</span><span class="sxs-lookup"><span data-stu-id="9c25f-129">A pointer to any other files that you need included to get your shaders to compile.</span></span> <span data-ttu-id="9c25f-130">Hierbei wird die ID3D10Include-Schnittstelle verwendet, die über zwei benutzerimplementierte Methoden verfügt: Öffnen und Schließen.</span><span class="sxs-lookup"><span data-stu-id="9c25f-130">This uses the ID3D10Include interface which has two user-implemented methods: Open and Close.</span></span> <span data-ttu-id="9c25f-131">Damit dies funktioniert, müssen Sie den Text der Open- und Close-Methoden implementieren. Fügen Sie in der Open-Methode den Code hinzu, den Sie zum Öffnen beliebiger Includedateien verwenden möchten. Fügen Sie in der Close-Funktion den Code hinzu, um die Dateien zu schließen, wenn Sie damit fertig sind.</span><span class="sxs-lookup"><span data-stu-id="9c25f-131">To make this work, you will need to implement the body of the Open and Close methods; in the Open method add the code you would use to open whatever include files you want, in the Close function add the code to close the files when you are done with them.</span></span>
-   <span data-ttu-id="9c25f-132">Der Name der zu kompilierende Shaderfunktion.</span><span class="sxs-lookup"><span data-stu-id="9c25f-132">The name of the shader function to compile.</span></span> <span data-ttu-id="9c25f-133">Dieser Shader kompiliert die Funktion "Ethereum".</span><span class="sxs-lookup"><span data-stu-id="9c25f-133">This shader compiles the Ripple function.</span></span>
-   <span data-ttu-id="9c25f-134">Das Shaderprofil, auf das beim Kompilieren ausgerichtet werden soll.</span><span class="sxs-lookup"><span data-stu-id="9c25f-134">The shader profile to target when compiling.</span></span> <span data-ttu-id="9c25f-135">Da Sie eine Funktion in einen Scheitelpunkt, eine Geometrie oder einen Pixel-Shader kompilieren können, teilt das Profil dem Compiler mit, mit welchem Shadertyp und welchem Shadermodell der Code verglichen werden soll.</span><span class="sxs-lookup"><span data-stu-id="9c25f-135">Since you can compile a function into a vertex, geometry, or pixel shader, the profile tells the compiler which type of shader and which shader model to compare the code against.</span></span>
-   <span data-ttu-id="9c25f-136">Shadercompilerflags.</span><span class="sxs-lookup"><span data-stu-id="9c25f-136">Shader compiler flags.</span></span> <span data-ttu-id="9c25f-137">Diese Flags teilen dem Compiler mit, welche Informationen in die kompilierte Ausgabe aufgenommen werden sollen und wie der Ausgabecode optimiert werden soll: für Geschwindigkeit, debuggen usw. Eine Liste der verfügbaren Flags finden Sie unter [Effektkonstanten (Direct3D 10).](/windows/desktop/direct3d10/d3d10-graphics-reference-effect-constants)</span><span class="sxs-lookup"><span data-stu-id="9c25f-137">These flags tell the compiler what information to put into the compiled output and how you want the output code optimized: for speed, for debug, etc. See [Effect Constants (Direct3D 10)](/windows/desktop/direct3d10/d3d10-graphics-reference-effect-constants) for a listing of the available flags.</span></span> <span data-ttu-id="9c25f-138">Das Beispiel enthält Code, mit dem Sie die Compilerflagwerte für Ihr Projekt festlegen können. Dies ist hauptsächlich eine Frage, ob Sie Debuginformationen generieren möchten.</span><span class="sxs-lookup"><span data-stu-id="9c25f-138">The sample contains some code you can use to set the compiler flag values for your project - this is mainly a question of whether or not you want to generate debug information.</span></span>
-   <span data-ttu-id="9c25f-139">Ein Zeiger auf den Puffer, der den kompilierten Shadercode enthält.</span><span class="sxs-lookup"><span data-stu-id="9c25f-139">A pointer to the buffer that contains the compiled shader code.</span></span> <span data-ttu-id="9c25f-140">Der Puffer enthält auch alle eingebetteten Debug- und Symboltabelleninformationen, die von den Compilerflags angefordert werden.</span><span class="sxs-lookup"><span data-stu-id="9c25f-140">The buffer also contains any embedded debug and symbol table information requested by the compiler flags.</span></span>
-   <span data-ttu-id="9c25f-141">Ein Zeiger auf einen Puffer, der eine Liste von Fehlern und Warnungen enthält, die während der Kompilierung aufgetreten sind. Dies sind die gleichen Meldungen, die in der Debugausgabe angezeigt werden, wenn Sie den Debugger beim Kompilieren des Shaders ausführen.</span><span class="sxs-lookup"><span data-stu-id="9c25f-141">A pointer to a buffer that contains a listing of errors and warnings that were encountered during the compile, which are the same messages you would see in the debug output if you were running the debugger while compiling the shader.</span></span> <span data-ttu-id="9c25f-142">**NULL** ist ein akzeptabler Wert, wenn die Fehler nicht an einen Puffer zurückgegeben werden sollen.</span><span class="sxs-lookup"><span data-stu-id="9c25f-142">**NULL** is an acceptable value when you don't want the errors returned to a buffer.</span></span>

<span data-ttu-id="9c25f-143">Wenn der Shader erfolgreich kompiliert wird, wird ein Zeiger auf den Shadercode als ID3D10Blob-Schnittstelle zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="9c25f-143">If the shader compiles successfully, a pointer to the shader code is returned as a ID3D10Blob interface.</span></span> <span data-ttu-id="9c25f-144">Sie wird als Blob-Schnittstelle bezeichnet, da der Zeiger auf eine Position im Arbeitsspeicher zeigt, die aus einem Array von DWORD besteht.</span><span class="sxs-lookup"><span data-stu-id="9c25f-144">It is called the Blob interface because the pointer is to a location in memory that is made up of an array of DWORD's.</span></span> <span data-ttu-id="9c25f-145">Die -Schnittstelle wird bereitgestellt, damit Sie einen Zeiger auf den kompilierten Shader abrufen können, den Sie im nächsten Schritt benötigen.</span><span class="sxs-lookup"><span data-stu-id="9c25f-145">The interface is provided so that you can get a pointer to the compiled shader which you will need in the next step.</span></span>

<span data-ttu-id="9c25f-146">Ab dem SDK vom Dezember 2006 ist der DirectX 10 HLSL-Compiler jetzt sowohl in DirectX 9 als auch in DirectX 10 der Standardcompiler.</span><span class="sxs-lookup"><span data-stu-id="9c25f-146">Beginning with the December 2006 SDK, the DirectX 10 HLSL compiler is now the default compiler in both DirectX 9 and DirectX 10.</span></span> <span data-ttu-id="9c25f-147">Weitere Informationen finden Sie unter [Effektcompilertool.](/windows/desktop/direct3dtools/fxc)</span><span class="sxs-lookup"><span data-stu-id="9c25f-147">See [Effect-Compiler Tool](/windows/desktop/direct3dtools/fxc) for details.</span></span>

### <a name="get-a-pointer-to-a-compiled-shader"></a><span data-ttu-id="9c25f-148">Abrufen eines Zeigers auf einen kompilierten Shader</span><span class="sxs-lookup"><span data-stu-id="9c25f-148">Get a Pointer to a Compiled Shader</span></span>

<span data-ttu-id="9c25f-149">Mehrere API-Methoden erfordern einen Zeiger auf einen kompilierten Shader.</span><span class="sxs-lookup"><span data-stu-id="9c25f-149">Several API methods require a pointer to a compiled shader.</span></span> <span data-ttu-id="9c25f-150">Dieses Argument wird in der Regel als *pShaderBytecode* bezeichnet, da es auf einen kompilierten Shader verweist, der als Sequenz von Bytecodes dargestellt wird.</span><span class="sxs-lookup"><span data-stu-id="9c25f-150">This argument is usually called *pShaderBytecode* because it points to a compiled shader represented as a sequence of byte codes.</span></span> <span data-ttu-id="9c25f-151">Um einen Zeiger auf einen kompilierten Shader abzurufen, kompilieren Sie zuerst den Shader, indem Sie [**D3D10CompileShader**](/windows/desktop/api/d3d10shader/nf-d3d10shader-d3d10compileshader) oder eine ähnliche Funktion aufrufen.</span><span class="sxs-lookup"><span data-stu-id="9c25f-151">To get a pointer to a compiled shader, first compile the shader by calling [**D3D10CompileShader**](/windows/desktop/api/d3d10shader/nf-d3d10shader-d3d10compileshader) or a similar function.</span></span> <span data-ttu-id="9c25f-152">Wenn die Kompilierung erfolgreich ist, wird der kompilierte Shader in einer [**ID3D10Blob-Schnittstelle**](/windows/desktop/api/d3dcommon/nn-d3dcommon-id3d10blob) zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="9c25f-152">If compilation is successful, the compiled shader is returned in an [**ID3D10Blob**](/windows/desktop/api/d3dcommon/nn-d3dcommon-id3d10blob) interface.</span></span> <span data-ttu-id="9c25f-153">Verwenden Sie abschließend die [**GetBufferPointer-Methode,**](/windows/desktop/api/d3dcommon/nf-d3dcommon-id3d10blob-getbufferpointer) um den Zeiger zurückzugeben.</span><span class="sxs-lookup"><span data-stu-id="9c25f-153">Finally, use the [**GetBufferPointer**](/windows/desktop/api/d3dcommon/nf-d3dcommon-id3d10blob-getbufferpointer) method to return the pointer.</span></span>

## <a name="create-a-shader-object"></a><span data-ttu-id="9c25f-154">Erstellen eines Shaderobjekts</span><span class="sxs-lookup"><span data-stu-id="9c25f-154">Create a Shader Object</span></span>

<span data-ttu-id="9c25f-155">Nachdem der Shader kompiliert wurde, rufen Sie CreateVertexShader auf, um das Shaderobjekt zu erstellen:</span><span class="sxs-lookup"><span data-stu-id="9c25f-155">Once the shader is compiled, call CreateVertexShader to create the shader object:</span></span>


```
    ID3D10VertexShader ** ppVertexShader
    ID3D10Blob pBlob;


    // Create the vertex shader
    hr = pd3dDevice->CreateVertexShader( (DWORD*)pBlob->GetBufferPointer(),
        pBlob->GetBufferSize(), &ppVertexShader );

    // Release the pointer to the compiled shader once you are done with it
    pBlob->Release();
```



<span data-ttu-id="9c25f-156">Um das Shaderobjekt zu erstellen, übergeben Sie den Zeiger auf den kompilierten Shader an CreateVertexShader.</span><span class="sxs-lookup"><span data-stu-id="9c25f-156">To create the shader object, pass the pointer to the compiled shader into CreateVertexShader.</span></span> <span data-ttu-id="9c25f-157">Da Sie den Shader zuerst erfolgreich kompilieren mussten, wird dieser Aufruf mit ziemlicher Sicherheit erfolgreich ausgeführt, es sei denn, Sie haben ein Speicherproblem auf Ihrem Computer.</span><span class="sxs-lookup"><span data-stu-id="9c25f-157">Since you had to successfully compile the shader first, this call will almost certainly pass, unless you have a memory problem on your machine.</span></span>

<span data-ttu-id="9c25f-158">Sie können beliebig viele Shaderobjekte erstellen und einfach Zeiger darauf beibehalten.</span><span class="sxs-lookup"><span data-stu-id="9c25f-158">You can create as many shader objects as you like and simply keep pointers to them.</span></span> <span data-ttu-id="9c25f-159">Dieser Mechanismus funktioniert für Geometrie- und Pixel-Shader, vorausgesetzt, Sie stimmen mit den Shaderprofilen (wenn Sie die Kompilierungsmethode aufrufen) mit den Schnittstellennamen überein (wenn Sie die create-Methode aufrufen).</span><span class="sxs-lookup"><span data-stu-id="9c25f-159">This same mechanism works for geometry and pixel shaders assuming you match the shader profiles (when you call the compile method) to the interface names (when you call the create method).</span></span>

## <a name="set-the-shader-object"></a><span data-ttu-id="9c25f-160">Festlegen des Shaderobjekts</span><span class="sxs-lookup"><span data-stu-id="9c25f-160">Set the Shader Object</span></span>

<span data-ttu-id="9c25f-161">Im letzten Schritt wird der Shader auf die Pipelinephase festgelegt.</span><span class="sxs-lookup"><span data-stu-id="9c25f-161">The last step is set the shader to the pipeline stage.</span></span> <span data-ttu-id="9c25f-162">Da die Pipeline drei Shaderstufen umfasst, müssen Sie drei API-Aufrufe durchführen, einen für jede Phase.</span><span class="sxs-lookup"><span data-stu-id="9c25f-162">Since there are three shader stages in the pipeline, you will need to make three API calls, one for each stage.</span></span>


```
    // Set a vertex shader
    pd3dDevice->VSSetShader( g_pVS10 );
```



<span data-ttu-id="9c25f-163">Beim Aufruf von VSSetShader wird der Zeiger auf den in Schritt 1 erstellten Vertexshader verwendet.</span><span class="sxs-lookup"><span data-stu-id="9c25f-163">The call to VSSetShader takes the pointer to the vertex shader created in step 1.</span></span> <span data-ttu-id="9c25f-164">Dadurch wird der Shader auf dem Gerät festgelegt.</span><span class="sxs-lookup"><span data-stu-id="9c25f-164">This sets the shader in the device.</span></span> <span data-ttu-id="9c25f-165">Die Vertex-Shaderphase wird nun mit ihrem Vertex-Shadercode initialisiert. Alles, was übrig bleibt, ist das Initialisieren aller Shadervariablen.</span><span class="sxs-lookup"><span data-stu-id="9c25f-165">The vertex shader stage is now initialized with its vertex shader code, all that remains is initializing any shader variables.</span></span>

## <a name="repeat-for-all-3-shader-stages"></a><span data-ttu-id="9c25f-166">Wiederholen für alle drei Shaderstufen</span><span class="sxs-lookup"><span data-stu-id="9c25f-166">Repeat for all 3 Shader Stages</span></span>

<span data-ttu-id="9c25f-167">Wiederholen Sie diese Schritte, um einen Vertex- oder Pixel-Shader oder sogar einen Geometrie-Shader zu erstellen, der an den Pixelshader ausgegeben wird.</span><span class="sxs-lookup"><span data-stu-id="9c25f-167">Repeat these same set of steps to build any vertex or pixel shader or even a geometry shader that outputs to the pixel shader.</span></span>

## <a name="related-topics"></a><span data-ttu-id="9c25f-168">Verwandte Themen</span><span class="sxs-lookup"><span data-stu-id="9c25f-168">Related Topics</span></span>

[<span data-ttu-id="9c25f-169">Kompilieren von Shadern</span><span class="sxs-lookup"><span data-stu-id="9c25f-169">Compiling Shaders</span></span>](dx-graphics-hlsl-part1.md)


## <a name="related-topics"></a><span data-ttu-id="9c25f-170">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="9c25f-170">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="9c25f-171">Programmieranleitung für HLSL</span><span class="sxs-lookup"><span data-stu-id="9c25f-171">Programming Guide for HLSL</span></span>](dx-graphics-hlsl-pguide.md)
</dt> </dl>

 

