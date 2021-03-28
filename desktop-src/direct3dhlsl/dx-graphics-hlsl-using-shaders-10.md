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
# <a name="using-shaders-in-direct3d-10"></a><span data-ttu-id="f2123-103">Verwenden von Shadern in Direct3D 10</span><span class="sxs-lookup"><span data-stu-id="f2123-103">Using Shaders in Direct3D 10</span></span>

<span data-ttu-id="f2123-104">Die Pipeline verfügt über drei Shader-Stufen, die jeweils mit einem HLSL-Shader programmiert werden.</span><span class="sxs-lookup"><span data-stu-id="f2123-104">The pipeline has three shader stages and each one is programmed with an HLSL shader.</span></span> <span data-ttu-id="f2123-105">Alle Direct3D 10-Shader werden in HLSL geschrieben und als Ziel für Shader Model 4 verwendet.</span><span class="sxs-lookup"><span data-stu-id="f2123-105">All Direct3D 10 shaders are written in HLSL, targeting shader model 4.</span></span>



|                                                                                                                                                                                                                                                                                                                                                |
|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="f2123-106">Unterschiede zwischen Direct3D 9 und Direct3D 10:</span><span class="sxs-lookup"><span data-stu-id="f2123-106">Differences between Direct3D 9 and Direct3D 10:</span></span><br/> <span data-ttu-id="f2123-107">Im Gegensatz zu Direct3D 9-shadermodellen, die in einer zwischen Assemblysprache erstellt werden können, werden Shader-Modell-4,0-Shader nur in HLSL erstellt.</span><span class="sxs-lookup"><span data-stu-id="f2123-107">Unlike Direct3D 9 shader models which could be authored in an intermediate assembly language, shader model 4.0 shaders are only authored in HLSL.</span></span> <span data-ttu-id="f2123-108">Die Offline Kompilierung von Shader in den Geräte nutzbaren Bytecode wird weiterhin unterstützt und wird für die meisten Szenarien empfohlen.</span><span class="sxs-lookup"><span data-stu-id="f2123-108">Offline compilation of shaders into device-consumable bytecode is still supported, and recommended for most scenarios.</span></span><br/> |



 

<span data-ttu-id="f2123-109">In diesem Beispiel wird nur ein Scheitelpunkt-Shader verwendet.</span><span class="sxs-lookup"><span data-stu-id="f2123-109">This example uses only a vertex shader.</span></span> <span data-ttu-id="f2123-110">Da alle Shader aus dem gemeinsamen Shader-Kern erstellt werden, ist das Erlernen der Verwendung eines Vertex-Shader sehr ähnlich wie bei der Verwendung eines Geometry-oder Pixelshader.</span><span class="sxs-lookup"><span data-stu-id="f2123-110">Because all shaders are built from the common shader core, learning how to use a vertex shader is very similar to using a geometry or pixel shader.</span></span>

<span data-ttu-id="f2123-111">Nachdem Sie einen HLSL-Shader verfasst haben (in diesem Beispiel wird der Vertex-Shader hlslwithoutfx. VSH verwendet), müssen Sie ihn für die jeweilige Pipeline Phase vorbereiten, in der er verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="f2123-111">Once you have authored an HLSL shader (this example uses the vertex shader HLSLWithoutFX.vsh), you will need to prepare it for the particular pipeline stage that will use it.</span></span> <span data-ttu-id="f2123-112">Zu diesem Zweck müssen Sie folgende Schritte ausführen:</span><span class="sxs-lookup"><span data-stu-id="f2123-112">To do this you need to:</span></span>

-   [<span data-ttu-id="f2123-113">Kompilieren eines Shaders</span><span class="sxs-lookup"><span data-stu-id="f2123-113">Compile a Shader</span></span>](#compile-a-shader)
-   [<span data-ttu-id="f2123-114">Erstellen eines shaderobjekts</span><span class="sxs-lookup"><span data-stu-id="f2123-114">Create a Shader Object</span></span>](#create-a-shader-object)
-   [<span data-ttu-id="f2123-115">Festlegen des Shader-Objekts</span><span class="sxs-lookup"><span data-stu-id="f2123-115">Set the Shader Object</span></span>](#set-the-shader-object)
-   [<span data-ttu-id="f2123-116">Für alle 3 shaderphasen wiederholen</span><span class="sxs-lookup"><span data-stu-id="f2123-116">Repeat for all 3 Shader Stages</span></span>](#repeat-for-all-3-shader-stages)

<span data-ttu-id="f2123-117">Diese Schritte müssen für jeden Shader in der Pipeline wiederholt werden.</span><span class="sxs-lookup"><span data-stu-id="f2123-117">These steps need to be repeated for each shader in the pipeline.</span></span>

## <a name="compile-a-shader"></a><span data-ttu-id="f2123-118">Kompilieren eines Shaders</span><span class="sxs-lookup"><span data-stu-id="f2123-118">Compile a Shader</span></span>

<span data-ttu-id="f2123-119">Der erste Schritt besteht darin, den Shader zu kompilieren, um zu überprüfen, ob Sie die HLSL-Anweisungen ordnungsgemäß codiert haben.</span><span class="sxs-lookup"><span data-stu-id="f2123-119">The first step is to compile the shader, to check to see that you have coded the HLSL statements correctly.</span></span> <span data-ttu-id="f2123-120">Dies erfolgt durch Aufrufen von D3D10CompileShader und das Bereitstellen von mehreren Parametern, wie hier gezeigt:</span><span class="sxs-lookup"><span data-stu-id="f2123-120">This is done by calling D3D10CompileShader and supplying it with several parameters as shown here:</span></span>


```
    IPD3D10Blob * pBlob;
    
        
    // Compile the vertex shader from the file
    D3D10CompileShader( strPath, strlen( strPath ), "HLSLWithoutFX.vsh", 
        NULL, NULL, "Ripple", "vs_4_0", dwShaderFlags, &pBlob, NULL );
```



<span data-ttu-id="f2123-121">Diese Funktion übernimmt die folgenden Parameter:</span><span class="sxs-lookup"><span data-stu-id="f2123-121">This function takes the following parameters:</span></span>

-   <span data-ttu-id="f2123-122">Der Name der Datei (und Länge der namens Zeichenfolge in Bytes), die den Shader enthält.</span><span class="sxs-lookup"><span data-stu-id="f2123-122">The name of the file ( and length of the name string in bytes ) that contains the shader.</span></span> <span data-ttu-id="f2123-123">Dieses Beispiel verwendet nur einen Vertex-Shader (in der Datei "hlslwithoutfx. VSH", in der die Dateierweiterung ". VSH" eine Abkürzung für Vertex-Shader ist).</span><span class="sxs-lookup"><span data-stu-id="f2123-123">This example uses a vertex shader only (in the file HLSLWithoutFX.vsh file where the file extension .vsh is an abbreviation for vertex shader).</span></span>
-   <span data-ttu-id="f2123-124">Der Shader-Funktionsname.</span><span class="sxs-lookup"><span data-stu-id="f2123-124">The shader function name.</span></span> <span data-ttu-id="f2123-125">In diesem Beispiel wird ein Vertex-Shader aus der Ripple-Funktion kompiliert, die eine einzelne Eingabe annimmt und eine Ausgabestruktur zurückgibt (die Funktion ist aus dem Beispiel hlslwithoutfx):</span><span class="sxs-lookup"><span data-stu-id="f2123-125">This example compiles a vertex shader from the Ripple function which takes a single input and returns an output struct (the function is from the HLSLWithoutFX sample):</span></span>
    ```
    VS_OUTPUT Ripple( in float2 vPosition : POSITION )
    ```

    

-   <span data-ttu-id="f2123-126">Ein Zeiger auf alle Makros, die vom Shader verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="f2123-126">A pointer to all macros used by the shader.</span></span> <span data-ttu-id="f2123-127">Verwenden \_ Sie das d3d10-Shader \_ -Makro, um die Makros zu definieren. Erstellen Sie einfach eine namens Zeichenfolge, die alle Makronamen (wobei jeder Name durch ein Leerzeichen getrennt ist) und eine Definitions Zeichenfolge (bei jedem makrokörper durch ein Leerzeichen getrennt) enthält.</span><span class="sxs-lookup"><span data-stu-id="f2123-127">Use D3D10\_SHADER\_MACRO to help define your macros; simply create a name string that contains all the macro names (with each name separated by a space) and a definition string (with each macro body separated by a space).</span></span> <span data-ttu-id="f2123-128">Beide Zeichen folgen müssen Null enden.</span><span class="sxs-lookup"><span data-stu-id="f2123-128">Both strings need to be NULL terminated.</span></span>
-   <span data-ttu-id="f2123-129">Ein Zeiger auf alle anderen Dateien, die Sie einschließen müssen, damit die Shader kompiliert werden können.</span><span class="sxs-lookup"><span data-stu-id="f2123-129">A pointer to any other files that you need included to get your shaders to compile.</span></span> <span data-ttu-id="f2123-130">Dabei wird die ID3D10Include-Schnittstelle verwendet, die über zwei vom Benutzer implementierte Methoden verfügt: Öffnen und schließen.</span><span class="sxs-lookup"><span data-stu-id="f2123-130">This uses the ID3D10Include interface which has two user-implemented methods: Open and Close.</span></span> <span data-ttu-id="f2123-131">Um dies zu tun, müssen Sie den Text der Open-und Close-Methode implementieren. Fügen Sie in der Open-Methode den Code hinzu, den Sie zum Öffnen der gewünschten Includedateien verwenden möchten. Fügen Sie in der Close-Funktion den Code hinzu, um die Dateien zu schließen, wenn Sie damit abgeschlossen sind.</span><span class="sxs-lookup"><span data-stu-id="f2123-131">To make this work, you will need to implement the body of the Open and Close methods; in the Open method add the code you would use to open whatever include files you want, in the Close function add the code to close the files when you are done with them.</span></span>
-   <span data-ttu-id="f2123-132">Der Name der zu kompilierenden Shader-Funktion.</span><span class="sxs-lookup"><span data-stu-id="f2123-132">The name of the shader function to compile.</span></span> <span data-ttu-id="f2123-133">Dieser Shader kompiliert die Ripple-Funktion.</span><span class="sxs-lookup"><span data-stu-id="f2123-133">This shader compiles the Ripple function.</span></span>
-   <span data-ttu-id="f2123-134">Das Shader-Profil, das beim Kompilieren als Ziel für das Ziel</span><span class="sxs-lookup"><span data-stu-id="f2123-134">The shader profile to target when compiling.</span></span> <span data-ttu-id="f2123-135">Da Sie eine Funktion in einem Scheitelpunkt, einer Geometrie oder einem Pixelshader kompilieren können, teilt das Profil dem Compiler mit, welcher Typ von Shader und welches Shader-Modell den Code vergleichen soll.</span><span class="sxs-lookup"><span data-stu-id="f2123-135">Since you can compile a function into a vertex, geometry, or pixel shader, the profile tells the compiler which type of shader and which shader model to compare the code against.</span></span>
-   <span data-ttu-id="f2123-136">Shader-Compilerflags.</span><span class="sxs-lookup"><span data-stu-id="f2123-136">Shader compiler flags.</span></span> <span data-ttu-id="f2123-137">Diese Flags teilen dem Compiler mit, welche Informationen in die kompilierte Ausgabe eingefügt werden sollen und wie der Ausgabecode optimiert werden soll: für Geschwindigkeit, Debuggen usw. Eine Auflistung der verfügbaren Flags finden Sie unter [Wirkungs Konstanten (Direct3D 10)](/windows/desktop/direct3d10/d3d10-graphics-reference-effect-constants) .</span><span class="sxs-lookup"><span data-stu-id="f2123-137">These flags tell the compiler what information to put into the compiled output and how you want the output code optimized: for speed, for debug, etc. See [Effect Constants (Direct3D 10)](/windows/desktop/direct3d10/d3d10-graphics-reference-effect-constants) for a listing of the available flags.</span></span> <span data-ttu-id="f2123-138">Das Beispiel enthält Code, den Sie verwenden können, um die compilerflagwerte für das Projekt festzulegen. Dies ist hauptsächlich eine Frage, ob Sie Debuginformationen generieren möchten.</span><span class="sxs-lookup"><span data-stu-id="f2123-138">The sample contains some code you can use to set the compiler flag values for your project - this is mainly a question of whether or not you want to generate debug information.</span></span>
-   <span data-ttu-id="f2123-139">Ein Zeiger auf den Puffer, der den kompilierten Shader-Code enthält.</span><span class="sxs-lookup"><span data-stu-id="f2123-139">A pointer to the buffer that contains the compiled shader code.</span></span> <span data-ttu-id="f2123-140">Der Puffer enthält auch alle eingebetteten Debug-und Symboltabellen Informationen, die von den Compilerflags angefordert werden.</span><span class="sxs-lookup"><span data-stu-id="f2123-140">The buffer also contains any embedded debug and symbol table information requested by the compiler flags.</span></span>
-   <span data-ttu-id="f2123-141">Ein Zeiger auf einen Puffer, der eine Auflistung von Fehlern und Warnungen enthält, die während der Kompilierung aufgetreten sind. Dies sind die gleichen Meldungen, die in der Debugausgabe angezeigt werden, wenn Sie den Debugger beim Kompilieren des Shader ausgeführt haben.</span><span class="sxs-lookup"><span data-stu-id="f2123-141">A pointer to a buffer that contains a listing of errors and warnings that were encountered during the compile, which are the same messages you would see in the debug output if you were running the debugger while compiling the shader.</span></span> <span data-ttu-id="f2123-142">**Null** ist ein akzeptabler Wert, wenn Sie nicht möchten, dass die Fehler an einen Puffer zurückgegeben werden.</span><span class="sxs-lookup"><span data-stu-id="f2123-142">**NULL** is an acceptable value when you don't want the errors returned to a buffer.</span></span>

<span data-ttu-id="f2123-143">Wenn der Shader erfolgreich kompiliert wird, wird ein Zeiger auf den Shader-Code als ID3D10Blob-Schnittstelle zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="f2123-143">If the shader compiles successfully, a pointer to the shader code is returned as a ID3D10Blob interface.</span></span> <span data-ttu-id="f2123-144">Sie wird als BLOB-Schnittstelle bezeichnet, da sich der Zeiger auf einen Speicherort im Arbeitsspeicher befindet, der aus einem Array von DWORD besteht.</span><span class="sxs-lookup"><span data-stu-id="f2123-144">It is called the Blob interface because the pointer is to a location in memory that is made up of an array of DWORD's.</span></span> <span data-ttu-id="f2123-145">Die-Schnittstelle wird bereitgestellt, sodass Sie einen Zeiger auf den kompilierten Shader erhalten können, den Sie im nächsten Schritt benötigen.</span><span class="sxs-lookup"><span data-stu-id="f2123-145">The interface is provided so that you can get a pointer to the compiled shader which you will need in the next step.</span></span>

<span data-ttu-id="f2123-146">Ab dem SDK vom Dezember 2006 ist der DirectX 10 HLSL-Compiler nun der Standard Compiler in DirectX 9 und DirectX 10.</span><span class="sxs-lookup"><span data-stu-id="f2123-146">Beginning with the December 2006 SDK, the DirectX 10 HLSL compiler is now the default compiler in both DirectX 9 and DirectX 10.</span></span> <span data-ttu-id="f2123-147">Ausführliche Informationen finden Sie unter [Effect-Compiler-Tool](/windows/desktop/direct3dtools/fxc) .</span><span class="sxs-lookup"><span data-stu-id="f2123-147">See [Effect-Compiler Tool](/windows/desktop/direct3dtools/fxc) for details.</span></span>

### <a name="get-a-pointer-to-a-compiled-shader"></a><span data-ttu-id="f2123-148">Einen Zeiger auf einen kompilierten Shader erhalten</span><span class="sxs-lookup"><span data-stu-id="f2123-148">Get a Pointer to a Compiled Shader</span></span>

<span data-ttu-id="f2123-149">Mehrere API-Methoden erfordern einen Zeiger auf einen kompilierten Shader.</span><span class="sxs-lookup"><span data-stu-id="f2123-149">Several API methods require a pointer to a compiled shader.</span></span> <span data-ttu-id="f2123-150">Dieses Argument wird normalerweise als " *pshaderbytecode* " bezeichnet, da es auf einen kompilierten Shader zeigt, der als Sequenz von Byte Codes dargestellt wird.</span><span class="sxs-lookup"><span data-stu-id="f2123-150">This argument is usually called *pShaderBytecode* because it points to a compiled shader represented as a sequence of byte codes.</span></span> <span data-ttu-id="f2123-151">Zum Abrufen eines Zeigers auf einen kompilierten Shader kompilieren Sie zuerst den Shader, indem Sie [**D3D10CompileShader**](/windows/desktop/api/d3d10shader/nf-d3d10shader-d3d10compileshader) oder eine ähnliche Funktion aufrufen.</span><span class="sxs-lookup"><span data-stu-id="f2123-151">To get a pointer to a compiled shader, first compile the shader by calling [**D3D10CompileShader**](/windows/desktop/api/d3d10shader/nf-d3d10shader-d3d10compileshader) or a similar function.</span></span> <span data-ttu-id="f2123-152">Wenn die Kompilierung erfolgreich ist, wird der kompilierte Shader in einer [**ID3D10Blob**](/windows/desktop/api/d3dcommon/nn-d3dcommon-id3d10blob) -Schnittstelle zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="f2123-152">If compilation is successful, the compiled shader is returned in an [**ID3D10Blob**](/windows/desktop/api/d3dcommon/nn-d3dcommon-id3d10blob) interface.</span></span> <span data-ttu-id="f2123-153">Verwenden Sie abschließend die [**getbufferpointer**](/windows/desktop/api/d3dcommon/nf-d3dcommon-id3d10blob-getbufferpointer) -Methode, um den Zeiger zurückzugeben.</span><span class="sxs-lookup"><span data-stu-id="f2123-153">Finally, use the [**GetBufferPointer**](/windows/desktop/api/d3dcommon/nf-d3dcommon-id3d10blob-getbufferpointer) method to return the pointer.</span></span>

## <a name="create-a-shader-object"></a><span data-ttu-id="f2123-154">Erstellen eines shaderobjekts</span><span class="sxs-lookup"><span data-stu-id="f2123-154">Create a Shader Object</span></span>

<span data-ttu-id="f2123-155">Nachdem der Shader kompiliert wurde, rufen Sie "kreatevertexshader" auf, um das Shader-Objekt zu erstellen:</span><span class="sxs-lookup"><span data-stu-id="f2123-155">Once the shader is compiled, call CreateVertexShader to create the shader object:</span></span>


```
    ID3D10VertexShader ** ppVertexShader
    ID3D10Blob pBlob;


    // Create the vertex shader
    hr = pd3dDevice->CreateVertexShader( (DWORD*)pBlob->GetBufferPointer(),
        pBlob->GetBufferSize(), &ppVertexShader );

    // Release the pointer to the compiled shader once you are done with it
    pBlob->Release();
```



<span data-ttu-id="f2123-156">Um das Shader-Objekt zu erstellen, übergeben Sie den Zeiger an den kompilierten Shader in "kreatevertexshader".</span><span class="sxs-lookup"><span data-stu-id="f2123-156">To create the shader object, pass the pointer to the compiled shader into CreateVertexShader.</span></span> <span data-ttu-id="f2123-157">Da der Shader zuerst erfolgreich kompiliert werden musste, wird dieser Vorgang fast sicher bestanden, es sei denn, es liegt ein Speicherproblem auf dem Computer vor.</span><span class="sxs-lookup"><span data-stu-id="f2123-157">Since you had to successfully compile the shader first, this call will almost certainly pass, unless you have a memory problem on your machine.</span></span>

<span data-ttu-id="f2123-158">Sie können beliebig viele Shader-Objekte erstellen und einfach Zeiger darauf halten.</span><span class="sxs-lookup"><span data-stu-id="f2123-158">You can create as many shader objects as you like and simply keep pointers to them.</span></span> <span data-ttu-id="f2123-159">Derselbe Mechanismus funktioniert für geometry-und Pixel-Shader, wenn Sie den Shader-Profilen (wenn Sie die Compile-Methode aufrufen) den Schnittstellennamen entsprechen (wenn Sie die Create-Methode aufrufen).</span><span class="sxs-lookup"><span data-stu-id="f2123-159">This same mechanism works for geometry and pixel shaders assuming you match the shader profiles (when you call the compile method) to the interface names (when you call the create method).</span></span>

## <a name="set-the-shader-object"></a><span data-ttu-id="f2123-160">Festlegen des Shader-Objekts</span><span class="sxs-lookup"><span data-stu-id="f2123-160">Set the Shader Object</span></span>

<span data-ttu-id="f2123-161">Der letzte Schritt besteht darin, den Shader auf die Pipeline Stufe festzulegen.</span><span class="sxs-lookup"><span data-stu-id="f2123-161">The last step is set the shader to the pipeline stage.</span></span> <span data-ttu-id="f2123-162">Da in der Pipeline drei Shader-Stufen vorhanden sind, müssen Sie drei API-Aufrufe erstellen, eine für jede Phase.</span><span class="sxs-lookup"><span data-stu-id="f2123-162">Since there are three shader stages in the pipeline, you will need to make three API calls, one for each stage.</span></span>


```
    // Set a vertex shader
    pd3dDevice->VSSetShader( g_pVS10 );
```



<span data-ttu-id="f2123-163">Der vssetshader-Befehl verwendet den Zeiger auf den Vertex-Shader, der in Schritt 1 erstellt wurde.</span><span class="sxs-lookup"><span data-stu-id="f2123-163">The call to VSSetShader takes the pointer to the vertex shader created in step 1.</span></span> <span data-ttu-id="f2123-164">Dadurch wird der Shader im Gerät festgelegt.</span><span class="sxs-lookup"><span data-stu-id="f2123-164">This sets the shader in the device.</span></span> <span data-ttu-id="f2123-165">Die Vertex-Shader-Stufe wird jetzt mit Ihrem Scheitelpunkt-Shader-Code initialisiert, und nur noch werden alle shadervariablen initialisiert.</span><span class="sxs-lookup"><span data-stu-id="f2123-165">The vertex shader stage is now initialized with its vertex shader code, all that remains is initializing any shader variables.</span></span>

## <a name="repeat-for-all-3-shader-stages"></a><span data-ttu-id="f2123-166">Für alle 3 shaderphasen wiederholen</span><span class="sxs-lookup"><span data-stu-id="f2123-166">Repeat for all 3 Shader Stages</span></span>

<span data-ttu-id="f2123-167">Wiederholen Sie dieselben Schritte, um einen beliebigen Scheitelpunkt oder Pixel-Shader oder sogar einen Geometry-Shader zu erstellen, der an den Pixelshader ausgibt.</span><span class="sxs-lookup"><span data-stu-id="f2123-167">Repeat these same set of steps to build any vertex or pixel shader or even a geometry shader that outputs to the pixel shader.</span></span>

## <a name="related-topics"></a><span data-ttu-id="f2123-168">Verwandte Themen</span><span class="sxs-lookup"><span data-stu-id="f2123-168">Related Topics</span></span>

[<span data-ttu-id="f2123-169">Kompilieren von Shadern</span><span class="sxs-lookup"><span data-stu-id="f2123-169">Compiling Shaders</span></span>](dx-graphics-hlsl-part1.md)


## <a name="related-topics"></a><span data-ttu-id="f2123-170">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="f2123-170">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="f2123-171">Programmieranleitung für HLSL</span><span class="sxs-lookup"><span data-stu-id="f2123-171">Programming Guide for HLSL</span></span>](dx-graphics-hlsl-pguide.md)
</dt> </dl>

 

