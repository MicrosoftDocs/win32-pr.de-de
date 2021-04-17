---
title: Arbeiten mit Shader und Shaderressourcen
description: Es ist an der Zeit, sich mit Shader und Shaderressourcen bei der Entwicklung Ihres Microsoft DirectX-Spiels für Windows 8 zu informieren.
ms.assetid: 25a11983-e3f6-4bd3-86f1-d660edc4cd4b
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 26ac147971221b04b02f2a45af8e8d4f6855a5e3
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "104390515"
---
# <a name="work-with-shaders-and-shader-resources"></a><span data-ttu-id="8ae76-103">Arbeiten mit Shader und Shaderressourcen</span><span class="sxs-lookup"><span data-stu-id="8ae76-103">Work with shaders and shader resources</span></span>

<span data-ttu-id="8ae76-104">Es ist an der Zeit, sich mit Shader und Shaderressourcen bei der Entwicklung Ihres Microsoft DirectX-Spiels für Windows 8 zu informieren.</span><span class="sxs-lookup"><span data-stu-id="8ae76-104">It's time to learn how to work with shaders and shader resources in developing your Microsoft DirectX game for Windows 8.</span></span> <span data-ttu-id="8ae76-105">Wir haben gesehen, wie das Grafikgerät und die Ressourcen eingerichtet werden, und vielleicht haben Sie sogar damit begonnen, seine Pipeline zu ändern.</span><span class="sxs-lookup"><span data-stu-id="8ae76-105">We've seen how to set up the graphics device and resources, and perhaps you've even started modifying its pipeline.</span></span> <span data-ttu-id="8ae76-106">Sehen wir uns nun die Pixel-und Vertex-Shader an.</span><span class="sxs-lookup"><span data-stu-id="8ae76-106">So now let's look at pixel and vertex shaders.</span></span>

<span data-ttu-id="8ae76-107">Wenn Sie mit Shader-Sprachen nicht vertraut sind, finden Sie in der richtigen Reihenfolge eine kurze Erörterung.</span><span class="sxs-lookup"><span data-stu-id="8ae76-107">If you aren't familiar with shader languages, a quick discussion is in order.</span></span> <span data-ttu-id="8ae76-108">Shader sind kleine, Low-Level-Programme, die in bestimmten Phasen der Grafik Pipeline kompiliert und ausgeführt werden.</span><span class="sxs-lookup"><span data-stu-id="8ae76-108">Shaders are small, low-level programs that are compiled and run at specific stages in the graphics pipeline.</span></span> <span data-ttu-id="8ae76-109">Ihre Spezialität sind sehr schnelle Gleit Komma Operationen mit Gleit Komma Zahlen.</span><span class="sxs-lookup"><span data-stu-id="8ae76-109">Their specialty is very fast floating-point mathematical operations.</span></span> <span data-ttu-id="8ae76-110">Die häufigsten Shader-Programme sind:</span><span class="sxs-lookup"><span data-stu-id="8ae76-110">The most common shader programs are:</span></span>

-   <span data-ttu-id="8ae76-111">**Vertex-Shader**– wird für jeden Scheitelpunkt in einer Szene ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="8ae76-111">**Vertex shader**—Executed for each vertex in a scene.</span></span> <span data-ttu-id="8ae76-112">Dieser Shader verarbeitet Vertex-Puffer Elemente, die von der aufrufenden App bereitgestellt werden, und führt minimal zu einem Positions Vektor mit vier Komponenten, der in eine Pixelposition gerengt wird.</span><span class="sxs-lookup"><span data-stu-id="8ae76-112">This shader operates on vertex buffer elements provided to it by the calling app, and minimally results in a 4-component position vector that will be rasterized into a pixel position.</span></span>
-   <span data-ttu-id="8ae76-113">**Pixel-Shader**– wird für jedes Pixel in einem Renderziel ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="8ae76-113">**Pixel shader**—Executed for each pixel in a render target.</span></span> <span data-ttu-id="8ae76-114">Dieser Shader empfängt rasterisierte Koordinaten aus früheren shaderphasen (in den einfachsten Pipelines, dies wäre der Vertexshader) und gibt eine Farbe (oder einen anderen 4-komponentenwert) für die Pixelposition zurück, die dann in ein Renderziel geschrieben wird.</span><span class="sxs-lookup"><span data-stu-id="8ae76-114">This shader receives rasterized coordinates from previous shader stages (in the simplest pipelines, this would be the vertex shader) and returns a color (or other 4-component value) for that pixel position, which is then written into a render target.</span></span>

<span data-ttu-id="8ae76-115">Dieses Beispiel enthält sehr einfache Scheitelpunkt-und Pixel-Shader, die nur Geometrie zeichnen, und komplexere Shader, die grundlegende Beleuchtungsberechnungen hinzufügen.</span><span class="sxs-lookup"><span data-stu-id="8ae76-115">This example includes very basic vertex and pixel shaders that only draw geometry, and more complex shaders that add basic lighting calculations.</span></span>

<span data-ttu-id="8ae76-116">Shader-Programme sind in Microsoft High Level Shader Language (HLSL) geschrieben.</span><span class="sxs-lookup"><span data-stu-id="8ae76-116">Shader programs are written in Microsoft High Level Shader Language (HLSL).</span></span> <span data-ttu-id="8ae76-117">Die HLSL-Syntax sieht ähnlich aus wie C, aber ohne die Zeiger.</span><span class="sxs-lookup"><span data-stu-id="8ae76-117">HLSL syntax looks a lot like C, but without the pointers.</span></span> <span data-ttu-id="8ae76-118">Shader-Programme müssen sehr kompakt und effizient sein.</span><span class="sxs-lookup"><span data-stu-id="8ae76-118">Shader programs must be very compact and efficient.</span></span> <span data-ttu-id="8ae76-119">Wenn Ihr Shader zu viele Anweisungen kompiliert, kann er nicht ausgeführt werden, und es wird ein Fehler zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="8ae76-119">If your shader compiles to too many instructions, it cannot be run and an error is returned.</span></span> <span data-ttu-id="8ae76-120">(Beachten Sie, dass die genaue Anzahl zulässiger Anweisungen Teil der [Direct3D-Funktionsebene](/windows/desktop/direct3d11/overviews-direct3d-11-devices-downlevel-intro)ist.)</span><span class="sxs-lookup"><span data-stu-id="8ae76-120">(Note that the exact number of instructions allowed is part of the [Direct3D feature level](/windows/desktop/direct3d11/overviews-direct3d-11-devices-downlevel-intro).)</span></span>

<span data-ttu-id="8ae76-121">In Direct3D werden Shader zur Laufzeit nicht kompiliert. Sie werden kompiliert, wenn der Rest des Programms kompiliert wird.</span><span class="sxs-lookup"><span data-stu-id="8ae76-121">In Direct3D, shaders are not compiled at run time; they are compiled when the rest of the program is compiled.</span></span> <span data-ttu-id="8ae76-122">Wenn Sie die APP mit Microsoft Visual Studio 2013 kompilieren, werden die HLSL-Dateien in CSO-Dateien (. CSO) kompiliert, die ihre App laden und vor dem Zeichnen in den GPU-Speicher platzieren muss.</span><span class="sxs-lookup"><span data-stu-id="8ae76-122">When you compile your app with Microsoft Visual Studio 2013, the HLSL files are compiled to CSO (.cso) files that your app must load and place in GPU memory prior to drawing.</span></span> <span data-ttu-id="8ae76-123">Stellen Sie sicher, dass Sie diese CSO-Dateien bei der Paket Erstellung in Ihre APP einschließen. Dabei handelt es sich um Ressourcen wie Netzen und Texturen.</span><span class="sxs-lookup"><span data-stu-id="8ae76-123">Make sure you include these CSO files with your app when you package it; they are assets just like meshes and textures.</span></span>

## <a name="understand-hlsl-semantics"></a><span data-ttu-id="8ae76-124">Grundlegendes zur HLSL-Semantik</span><span class="sxs-lookup"><span data-stu-id="8ae76-124">Understand HLSL semantics</span></span>

<span data-ttu-id="8ae76-125">Es ist wichtig, dass Sie sich einen Moment Zeit nehmen, um die HLSL-Semantik zu erörtern, bevor Sie fortfahren, denn Sie sind häufig eine Verwechslung für neue Direct3D-Entwickler.</span><span class="sxs-lookup"><span data-stu-id="8ae76-125">It's important to take a moment to discuss HLSL semantics before we continue, because they are often a point of confusion for new Direct3D developers.</span></span> <span data-ttu-id="8ae76-126">HLSL-Semantik sind Zeichen folgen, die einen Wert angeben, der zwischen der APP und einem Shader-Programm übermittelt wird.</span><span class="sxs-lookup"><span data-stu-id="8ae76-126">HLSL semantics are strings that identify a value passed between the app and a shader program.</span></span> <span data-ttu-id="8ae76-127">Obwohl es sich um eine beliebige Vielzahl möglicher Zeichen folgen handeln kann, empfiehlt es sich, eine Zeichenfolge wie `POSITION` oder zu verwenden `COLOR` , die die Verwendung angibt.</span><span class="sxs-lookup"><span data-stu-id="8ae76-127">Although they can be any of a variety of possible strings, the best practice is to use a string like `POSITION` or `COLOR` that indicates the usage.</span></span> <span data-ttu-id="8ae76-128">Diese Semantik weisen Sie zu, wenn Sie einen konstanten Puffer oder ein Eingabe Layout erstellen.</span><span class="sxs-lookup"><span data-stu-id="8ae76-128">You assign these semantics when you are constructing a constant buffer or input layout.</span></span> <span data-ttu-id="8ae76-129">Sie können auch eine Zahl zwischen 0 und 7 an die Semantik anfügen, wenn Sie separate Register für ähnliche Werte verwenden möchten.</span><span class="sxs-lookup"><span data-stu-id="8ae76-129">You can also append a number between 0 and 7 to the semantic so that you use separate registers for similar values.</span></span> <span data-ttu-id="8ae76-130">Beispiel: COLOR0, COLOR1, COLOR2...</span><span class="sxs-lookup"><span data-stu-id="8ae76-130">For example: COLOR0, COLOR1, COLOR2...</span></span>

<span data-ttu-id="8ae76-131">Bei der Semantik mit dem Präfix "SV \_ " handelt es sich um eine *System Wert* Semantik, die von Ihrem Shader-Programm geschrieben wird. Ihr Spiel selbst (auf der CPU ausgeführt) kann Sie nicht ändern.</span><span class="sxs-lookup"><span data-stu-id="8ae76-131">Semantics that are prefixed with "SV\_" are *system value* semantics that are written to by your shader program; your game itself (running on the CPU) cannot modify them.</span></span> <span data-ttu-id="8ae76-132">In der Regel enthalten diese Semantik Werte, bei denen es sich um Eingaben oder Ausgaben aus einer anderen Shader-Stufe in der Grafik Pipeline handelt oder die vollständig von der GPU generiert werden.</span><span class="sxs-lookup"><span data-stu-id="8ae76-132">Typically, these semantics contain values that are inputs or outputs from another shader stage in the graphics pipeline, or that are generated entirely by the GPU.</span></span>

<span data-ttu-id="8ae76-133">Außerdem `SV_` hat die Semantik ein anderes Verhalten, wenn Sie verwendet werden, um Eingaben für eine Shader-Stufe anzugeben oder diese auszugeben.</span><span class="sxs-lookup"><span data-stu-id="8ae76-133">Additionally, `SV_` semantics have different behaviors when they are used to specify input to or output from a shader stage.</span></span> <span data-ttu-id="8ae76-134">`SV_POSITION`(Output) enthält z. b. die Vertexdaten, die während der Vertex-Shader-Stufe transformiert werden, und `SV_POSITION` (*Input*) enthält die Pixel Positionswerte, die während der rasterisierungsphase von der GPU interpoliert wurden.</span><span class="sxs-lookup"><span data-stu-id="8ae76-134">For example, `SV_POSITION` (output) contains the vertex data transformed during the vertex shader stage, and `SV_POSITION` (*input*) contains the pixel position values that were interpolated by the GPU during the rasterization stage.</span></span>

<span data-ttu-id="8ae76-135">Im folgenden finden Sie einige allgemeine HLSL-Semantik:</span><span class="sxs-lookup"><span data-stu-id="8ae76-135">Here are a few common HLSL semantics:</span></span>

-   <span data-ttu-id="8ae76-136">`POSITION`(*n*) für Vertex-Puffer Daten.</span><span class="sxs-lookup"><span data-stu-id="8ae76-136">`POSITION`(*n*) for vertex buffer data.</span></span> <span data-ttu-id="8ae76-137">`SV_POSITION` stellt eine Pixelposition für den Pixelshader bereit und kann nicht von Ihrem Spiel geschrieben werden.</span><span class="sxs-lookup"><span data-stu-id="8ae76-137">`SV_POSITION` provides a pixel position to the pixel shader and cannot be written by your game.</span></span>
-   <span data-ttu-id="8ae76-138">`NORMAL`(*n*) für normale Daten, die vom Vertex-Puffer bereitgestellt werden.</span><span class="sxs-lookup"><span data-stu-id="8ae76-138">`NORMAL`(*n*) for normal data provided by the vertex buffer.</span></span>
-   <span data-ttu-id="8ae76-139">`TEXCOORD`(*n*) für Textur-UV-Koordinatendaten, die an einen Shader übergeben werden.</span><span class="sxs-lookup"><span data-stu-id="8ae76-139">`TEXCOORD`(*n*) for texture UV coordinate data supplied to a shader.</span></span>
-   <span data-ttu-id="8ae76-140">`COLOR`(n) für RGBA-Farbdaten, die an einen Shader übergeben werden.</span><span class="sxs-lookup"><span data-stu-id="8ae76-140">`COLOR`(n) for RGBA color data supplied to a shader.</span></span> <span data-ttu-id="8ae76-141">Beachten Sie, dass Sie identisch mit der Koordinierung von Daten behandelt wird, einschließlich der Interpolation des Werts während der rasterisierung. mithilfe der Semantik können Sie einfach erkennen, dass es sich um Farbdaten handelt.</span><span class="sxs-lookup"><span data-stu-id="8ae76-141">Note that it is treated identically to coordinate data, including interpolating the value during rasterization; the semantic simply helps you identify that it is color data.</span></span>
-   <span data-ttu-id="8ae76-142">`SV_Target`\[n \] zum Schreiben von einem Pixelshader in eine Ziel Textur oder einen anderen Pixel Puffer.</span><span class="sxs-lookup"><span data-stu-id="8ae76-142">`SV_Target`\[n\] for writing from a pixel shader to a target texture or other pixel buffer.</span></span>

<span data-ttu-id="8ae76-143">Einige Beispiele für die HLSL-Semantik finden Sie im Beispiel.</span><span class="sxs-lookup"><span data-stu-id="8ae76-143">We'll see some examples of HLSL semantics as we review the example.</span></span>

## <a name="read-from-the-constant-buffers"></a><span data-ttu-id="8ae76-144">Aus konstantenpuffern lesen</span><span class="sxs-lookup"><span data-stu-id="8ae76-144">Read from the constant buffers</span></span>

<span data-ttu-id="8ae76-145">Jeder Shader kann aus einem konstanten Puffer lesen, wenn dieser Puffer an seine Stufe als Ressource angefügt wird.</span><span class="sxs-lookup"><span data-stu-id="8ae76-145">Any shader can read from a constant buffer if that buffer is attached to its stage as a resource.</span></span> <span data-ttu-id="8ae76-146">In diesem Beispiel wird nur dem Vertex-Shader ein konstanter Puffer zugewiesen.</span><span class="sxs-lookup"><span data-stu-id="8ae76-146">In this example, only the vertex shader is assigned a constant buffer.</span></span>

<span data-ttu-id="8ae76-147">Der Konstante Puffer wird an zwei Stellen deklariert: im C++-Code und in den entsprechenden HLSL-Dateien, die darauf zugreifen.</span><span class="sxs-lookup"><span data-stu-id="8ae76-147">The constant buffer is declared in two places: in the C++ code, and in the corresponding HLSL files that will access it.</span></span>

<span data-ttu-id="8ae76-148">Im folgenden wird erläutert, wie die Konstante Puffer Struktur im C++-Code deklariert wird.</span><span class="sxs-lookup"><span data-stu-id="8ae76-148">Here's how the constant buffer struct is declared in the C++ code.</span></span>


```C++
typedef struct _constantBufferStruct {
    DirectX::XMFLOAT4X4 world;
    DirectX::XMFLOAT4X4 view;
    DirectX::XMFLOAT4X4 projection;
} ConstantBufferStruct;
```



<span data-ttu-id="8ae76-149">Wenn Sie die Struktur für den Konstantenpuffer in Ihrem C++-Code deklarieren, stellen Sie sicher, dass alle Daten ordnungsgemäß an 16-Byte-Grenzen ausgerichtet sind.</span><span class="sxs-lookup"><span data-stu-id="8ae76-149">When declaring the structure for the constant buffer in your C++ code, ensure that all of the data is correctly aligned along 16-byte boundaries.</span></span> <span data-ttu-id="8ae76-150">Die einfachste Möglichkeit hierfür ist die Verwendung von [directxmath](/windows/desktop/dxmath/directxmath-portal) -Typen, wie z. b. **XMFLOAT4** oder **XMFLOAT4X4**, wie im Beispielcode gezeigt.</span><span class="sxs-lookup"><span data-stu-id="8ae76-150">The easiest way to do this is to use [DirectXMath](/windows/desktop/dxmath/directxmath-portal) types, like **XMFLOAT4** or **XMFLOAT4X4**, as seen in the example code.</span></span> <span data-ttu-id="8ae76-151">Sie können auch Schutz vor falsch ausgerichteten Puffern haben, indem Sie eine statische Assert deklarieren:</span><span class="sxs-lookup"><span data-stu-id="8ae76-151">You can also guard against misaligned buffers by declaring a static assert:</span></span>


```C++
// Assert that the constant buffer remains 16-byte aligned.
static_assert((sizeof(ConstantBufferStruct) % 16) == 0, "Constant Buffer size must be 16-byte aligned");
```



<span data-ttu-id="8ae76-152">Diese Codezeile führt zum Zeitpunkt der Kompilierung zu einem Fehler, wenn **constantbufferstruct** nicht mit 16 Byte ausgerichtet ist.</span><span class="sxs-lookup"><span data-stu-id="8ae76-152">This line of code will cause an error at compile time if **ConstantBufferStruct** is not 16-byte aligned.</span></span> <span data-ttu-id="8ae76-153">Weitere Informationen zur konstanten Puffer Ausrichtung und-Verpackung finden Sie unter [Packen von Regeln für konstante Variablen](/windows/desktop/direct3dhlsl/dx-graphics-hlsl-packing-rules).</span><span class="sxs-lookup"><span data-stu-id="8ae76-153">For more information about constant buffer alignment and packing, see [Packing Rules for Constant Variables](/windows/desktop/direct3dhlsl/dx-graphics-hlsl-packing-rules).</span></span>

<span data-ttu-id="8ae76-154">Hier sehen Sie, wie der Konstante Puffer im Vertex-Shader HLSL deklariert wird.</span><span class="sxs-lookup"><span data-stu-id="8ae76-154">Now, here's how the constant buffer is declared in the vertex shader HLSL.</span></span>


```C++
cbuffer ModelViewProjectionConstantBuffer : register(b0)
{
    matrix mWorld;      // world matrix for object
    matrix View;        // view matrix
    matrix Projection;  // projection matrix
};
```



<span data-ttu-id="8ae76-155">Alle Puffer – für Konstante, Textur, Sampler oder andere – muss ein Register definiert sein, damit die GPU darauf zugreifen kann.</span><span class="sxs-lookup"><span data-stu-id="8ae76-155">All buffers—constant, texture, sampler, or other—must have a register defined so the GPU can access them.</span></span> <span data-ttu-id="8ae76-156">Jede Shader-Stufe ermöglicht bis zu 15 Konstante Puffer, und jeder Puffer kann bis zu 4.096 Konstante Variablen enthalten.</span><span class="sxs-lookup"><span data-stu-id="8ae76-156">Each shader stage allows up to 15 constant buffers, and each buffer can hold up to 4,096 constant variables.</span></span> <span data-ttu-id="8ae76-157">Die Syntax der Register Verwendungs Deklaration lautet wie folgt:</span><span class="sxs-lookup"><span data-stu-id="8ae76-157">The register-usage declaration syntax is as follows:</span></span>

-   <span data-ttu-id="8ae76-158">**b \* \* *\#* : ein Register für einen konstanten Puffer (** cBuffer \* \*).</span><span class="sxs-lookup"><span data-stu-id="8ae76-158">**b\*\**\#*: A register for a constant buffer (** cbuffer\*\*).</span></span>
-   <span data-ttu-id="8ae76-159">**t \* \* *\#* : ein Register für einen Textur Puffer (** tBuffer \* \*).</span><span class="sxs-lookup"><span data-stu-id="8ae76-159">**t\*\**\#*: A register for a texture buffer (** tbuffer\*\*).</span></span>
-   <span data-ttu-id="8ae76-160">**s \* \* \#**: ein Register für einen Sampler.</span><span class="sxs-lookup"><span data-stu-id="8ae76-160">\**s\*\*\*\#*: A register for a sampler.</span></span> <span data-ttu-id="8ae76-161">(Ein Sampler definiert das Suchverhalten für texeln in der Textur Ressource.)</span><span class="sxs-lookup"><span data-stu-id="8ae76-161">(A sampler defines the lookup behavior for texels in the texture resource.)</span></span>

<span data-ttu-id="8ae76-162">Beispielsweise kann das HLSL für einen PixelShader eine Textur und einen Sampler als Eingabe mit einer Deklaration wie diesem annehmen.</span><span class="sxs-lookup"><span data-stu-id="8ae76-162">For example, the HLSL for a pixel shader might take a texture and a sampler as input with a declaration like this.</span></span>

``` syntax
Texture2D simpleTexture : register(t0);
SamplerState simpleSampler : register(s0);
```

<span data-ttu-id="8ae76-163">Es liegt an Ihnen, den Registern Konstante Puffer zuzuweisen – beim Einrichten der Pipeline fügen Sie einen konstanten Puffer an denselben Slot an, den Sie in der HLSL-Datei zugewiesen haben.</span><span class="sxs-lookup"><span data-stu-id="8ae76-163">It's up to you to assign constant buffers to registers—when you set up the pipeline, you attach a constant buffer to the same slot you assigned it to in the HLSL file.</span></span> <span data-ttu-id="8ae76-164">Im vorherigen Thema zeigt der [**vssetconstantbuffers**](/windows/desktop/api/d3d11/nf-d3d11-id3d11devicecontext-vssetconstantbuffers) -Aufrufe z. b. für den ersten Parameter "0" an.</span><span class="sxs-lookup"><span data-stu-id="8ae76-164">For example, in the previous topic the call to [**VSSetConstantBuffers**](/windows/desktop/api/d3d11/nf-d3d11-id3d11devicecontext-vssetconstantbuffers) indicates '0' for the first parameter.</span></span> <span data-ttu-id="8ae76-165">Dies weist Direct3D an, die Konstante Puffer Ressource an Register 0 anzufügen, was der Zuordnung des Puffers zur **Registrierung (B0)** in der HLSL-Datei entspricht.</span><span class="sxs-lookup"><span data-stu-id="8ae76-165">That tells Direct3D to attach the constant buffer resource to register 0, which matches the buffer's assignment to **register(b0)** in the HLSL file.</span></span>

## <a name="read-from-the-vertex-buffers"></a><span data-ttu-id="8ae76-166">Lesen aus den Scheitel Punkten</span><span class="sxs-lookup"><span data-stu-id="8ae76-166">Read from the vertex buffers</span></span>

<span data-ttu-id="8ae76-167">Der Vertex-Puffer stellt den Vertexshader die Dreiecks Daten für die Szene Objekte zur Verfügung.</span><span class="sxs-lookup"><span data-stu-id="8ae76-167">The vertex buffer supplies the triangle data for the scene objects to the vertex shader(s).</span></span> <span data-ttu-id="8ae76-168">Wie beim Konstanten Puffer wird die Vertex-Puffer Struktur im C++-Code mit ähnlichen Verpackungs Regeln deklariert.</span><span class="sxs-lookup"><span data-stu-id="8ae76-168">As with the constant buffer, the vertex buffer struct is declared in the C++ code, using similar packing rules.</span></span>


```C++
typedef struct _vertexPositionColor
{
    DirectX::XMFLOAT3 pos;
    DirectX::XMFLOAT3 color;
} VertexPositionColor;
```



<span data-ttu-id="8ae76-169">Es gibt kein Standardformat für Scheitelpunkt Daten in Direct3D 11.</span><span class="sxs-lookup"><span data-stu-id="8ae76-169">There is no standard format for vertex data in Direct3D 11.</span></span> <span data-ttu-id="8ae76-170">Stattdessen definieren wir unser eigenes Vertex-Datenlayout mithilfe eines Deskriptors. die Datenfelder werden mithilfe eines Arrays aus [**D3D11- \_ Eingabe \_ Element \_**](/windows/desktop/api/d3d11/ns-d3d11-d3d11_input_element_desc) -Erstellungs Strukturen definiert.</span><span class="sxs-lookup"><span data-stu-id="8ae76-170">Instead, we define our own vertex data layout using a descriptor; the data fields are defined using an array of [**D3D11\_INPUT\_ELEMENT\_DESC**](/windows/desktop/api/d3d11/ns-d3d11-d3d11_input_element_desc) structures.</span></span> <span data-ttu-id="8ae76-171">Hier sehen Sie ein einfaches Eingabe Layout, das das gleiche Scheitelpunkt Format wie die vorherige Struktur beschreibt:</span><span class="sxs-lookup"><span data-stu-id="8ae76-171">Here, we show a simple input layout that describes the same vertex format as the preceding struct:</span></span>


```C++
D3D11_INPUT_ELEMENT_DESC iaDesc [] =
{
    { "POSITION", 0, DXGI_FORMAT_R32G32B32_FLOAT,
    0, 0, D3D11_INPUT_PER_VERTEX_DATA, 0 },

    { "COLOR", 0, DXGI_FORMAT_R32G32B32_FLOAT,
    0, 12, D3D11_INPUT_PER_VERTEX_DATA, 0 },
};

hr = device->CreateInputLayout(
    iaDesc,
    ARRAYSIZE(iaDesc),
    bytes,
    bytesRead,
    &m_pInputLayout
    );
```



<span data-ttu-id="8ae76-172">Wenn Sie beim Ändern des Beispielcodes dem Vertex-Format Daten hinzufügen, achten Sie darauf, dass Sie auch das Eingabe Layout aktualisieren, oder der Shader kann es nicht interpretieren.</span><span class="sxs-lookup"><span data-stu-id="8ae76-172">If you add data to the vertex format when modifying the example code, be sure to update the input layout as well, or the shader will not be able to interpret it.</span></span> <span data-ttu-id="8ae76-173">Sie können das Scheitelpunkt Layout wie folgt ändern:</span><span class="sxs-lookup"><span data-stu-id="8ae76-173">You might modify the vertex layout like this:</span></span>


```C++
typedef struct _vertexPositionColorTangent
{
    DirectX::XMFLOAT3 pos;
    DirectX::XMFLOAT3 normal;
    DirectX::XMFLOAT3 tangent;
} VertexPositionColorTangent;
```



<span data-ttu-id="8ae76-174">In diesem Fall würden Sie die Eingabe Layout-Definition wie folgt ändern.</span><span class="sxs-lookup"><span data-stu-id="8ae76-174">In that case, you'd modify the input-layout definition as follows.</span></span>


```C++
D3D11_INPUT_ELEMENT_DESC iaDescExtended[] =
{
    { "POSITION", 0, DXGI_FORMAT_R32G32B32_FLOAT,
    0, 0, D3D11_INPUT_PER_VERTEX_DATA, 0 },

    { "NORMAL", 0, DXGI_FORMAT_R32G32B32_FLOAT,
    0, 12, D3D11_INPUT_PER_VERTEX_DATA, 0 },

    { "TANGENT", 0, DXGI_FORMAT_R32G32B32_FLOAT,
    0, 12, D3D11_INPUT_PER_VERTEX_DATA, 0 },
};

hr = device->CreateInputLayout(
    iaDesc,
    ARRAYSIZE(iaDesc),
    bytes,
    bytesRead,
    &m_pInputLayoutExtended
    );
```



<span data-ttu-id="8ae76-175">Jeder Eingabe Layout-Element Definition wird eine Zeichenfolge vorangestellt, wie z. b. "Position" oder "Normal" – Dies ist die Semantik, die wir zuvor in diesem Thema besprochen haben.</span><span class="sxs-lookup"><span data-stu-id="8ae76-175">Each of the input-layout element definitions is prefixed with a string, like "POSITION" or "NORMAL"—that is the semantic we discussed earlier in this topic.</span></span> <span data-ttu-id="8ae76-176">Es ähnelt einem Handle, das der GPU bei der Verarbeitung des Scheitel Punkts dabei hilft, dieses Element zu identifizieren.</span><span class="sxs-lookup"><span data-stu-id="8ae76-176">It's like a handle that helps the GPU identify that element when processing the vertex.</span></span> <span data-ttu-id="8ae76-177">Wählen Sie allgemeine, aussagekräftige Namen für die Vertex-Elemente aus.</span><span class="sxs-lookup"><span data-stu-id="8ae76-177">Choose common, meaningful names for your vertex elements.</span></span>

<span data-ttu-id="8ae76-178">Ebenso wie beim Konstanten Puffer verfügt der Vertex-Shader über eine entsprechende Puffer Definition für eingehende Vertex-Elemente.</span><span class="sxs-lookup"><span data-stu-id="8ae76-178">Just as with the constant buffer, the vertex shader has a corresponding buffer definition for incoming vertex elements.</span></span> <span data-ttu-id="8ae76-179">(Aus diesem Grund haben wir beim Erstellen des Eingabe Layouts einen Verweis auf die Vertex-Shader-Ressource bereitgestellt Direct3D die Überprüfung des pro-Vertex-Daten Layouts mit der Eingabe Struktur des Shader.) Beachten Sie, dass die Semantik zwischen der Eingabe Layout-Definition und dieser HLSL-Puffer Deklaration entspricht.</span><span class="sxs-lookup"><span data-stu-id="8ae76-179">(That's why we provided a reference to the vertex shader resource when creating the input layout - Direct3D validates the per-vertex data layout with the shader's input struct.) Note how the semantics match between the input layout definition and this HLSL buffer declaration.</span></span> <span data-ttu-id="8ae76-180">Es wird jedoch `COLOR` ein "0" angefügt.</span><span class="sxs-lookup"><span data-stu-id="8ae76-180">However, `COLOR` has a "0" appended to it.</span></span> <span data-ttu-id="8ae76-181">Es ist nicht erforderlich, den Wert 0 hinzuzufügen, wenn Sie nur ein `COLOR` Element im Layout deklariert haben. es wird jedoch empfohlen, es anzufügen, falls Sie in Zukunft weitere Farbelemente hinzufügen.</span><span class="sxs-lookup"><span data-stu-id="8ae76-181">It isn't necessary to add the 0 if you have only one `COLOR` element declared in the layout, but it's a good practice to append it in case you you choose to add more color elements in the future.</span></span>


```C++
struct VS_INPUT
{
    float3 vPos   : POSITION;
    float3 vColor : COLOR0;
};
```



## <a name="pass-data-between-shaders"></a><span data-ttu-id="8ae76-182">Übergeben von Daten zwischen Shadern</span><span class="sxs-lookup"><span data-stu-id="8ae76-182">Pass data between shaders</span></span>

<span data-ttu-id="8ae76-183">Shader nehmen bei der Ausführung Eingabetypen an und geben Ausgabetypen von ihren Hauptfunktionen zurück.</span><span class="sxs-lookup"><span data-stu-id="8ae76-183">Shaders take input types and return output types from their main functions upon execution.</span></span> <span data-ttu-id="8ae76-184">Für den Vertex-Shader, der im vorherigen Abschnitt definiert wurde, war der Eingabetyp die vs \_ -Eingabe Struktur, und wir haben ein entsprechendes Eingabe Layout und eine C++-Struktur definiert.</span><span class="sxs-lookup"><span data-stu-id="8ae76-184">For the vertex shader defined in the previous section, the input type was the VS\_INPUT structure, and we defined a matching input layout and C++ struct.</span></span> <span data-ttu-id="8ae76-185">Ein Array dieser Struktur wird verwendet, um einen Vertex-Puffer in der Methode " **kreatecube** " zu erstellen.</span><span class="sxs-lookup"><span data-stu-id="8ae76-185">An array of this struct is used to create a vertex buffer in the **CreateCube** method.</span></span>

<span data-ttu-id="8ae76-186">Der Vertex-Shader gibt eine PS \_ -Eingabe Struktur zurück, die die endgültige Scheitelpunkt Position von 4 Komponenten (float4) minimal enthalten muss.</span><span class="sxs-lookup"><span data-stu-id="8ae76-186">The vertex shader returns a PS\_INPUT structure, which must minimally contain the 4-component (float4) final vertex position.</span></span> <span data-ttu-id="8ae76-187">Für diesen Positionswert muss der System Wert Semantic, `SV_POSITION` , deklariert werden, damit die GPU über die Daten verfügt, die Sie zum Ausführen des nächsten Zeichnungs Schritts benötigt.</span><span class="sxs-lookup"><span data-stu-id="8ae76-187">This position value must have the system value semantic, `SV_POSITION`, declared for it so the GPU has the data it needs to perform the next drawing step.</span></span> <span data-ttu-id="8ae76-188">Beachten Sie, dass es keine 1:1-Entsprechung zwischen der Vertex-Shader-Ausgabe und der Pixel-Shadereingabe gibt. der Vertex-Shader gibt eine Struktur für jeden angegebenen Scheitelpunkt zurück, der Pixelshader wird jedoch für jedes Pixel einmal ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="8ae76-188">Notice that there is not a 1:1 correspondence between vertex shader output and pixel shader input; the vertex shader returns one structure for each vertex it is given, but the pixel shader runs once for each pixel.</span></span> <span data-ttu-id="8ae76-189">Das liegt daran, dass die pro-Vertex-Daten zuerst die rasterisierungsphase passieren.</span><span class="sxs-lookup"><span data-stu-id="8ae76-189">That's because the per-vertex data first passes through the rasterization stage.</span></span> <span data-ttu-id="8ae76-190">Diese Stufe bestimmt, welche Pixel die Geometrie "abdecken", die Sie zeichnen, berechnet interpoliert pro-Vertex-Daten für jedes Pixel und ruft dann den Pixelshader für jede dieser Pixel einmal auf.</span><span class="sxs-lookup"><span data-stu-id="8ae76-190">This stage decides which pixels "cover" the geometry you're drawing, computes interpolated per-vertex data for each pixel, and then calls the pixel shader once for each of those pixels.</span></span> <span data-ttu-id="8ae76-191">Die Interpolation ist das Standardverhalten beim rasterieren von Ausgabe Werten. Sie ist insbesondere für die korrekte Verarbeitung von Ausgabe Vektordaten (helle Vektoren, pro-Vertex-Normale und-Tangents usw.) entscheidend.</span><span class="sxs-lookup"><span data-stu-id="8ae76-191">Interpolation is the default behavior when rasterizing output values, and is essential in particular for the correct processing of output vector data (light vectors, per-vertex normals and tangents, and others).</span></span>


```C++
struct PS_INPUT
{
    float4 Position : SV_POSITION;  // interpolated vertex position (system value)
    float4 Color    : COLOR0;       // interpolated diffuse color
};
```



## <a name="review-the-vertex-shader"></a><span data-ttu-id="8ae76-192">Überprüfen Sie den Vertexshader.</span><span class="sxs-lookup"><span data-stu-id="8ae76-192">Review the vertex shader</span></span>

<span data-ttu-id="8ae76-193">Der Vertex-Beispiel Shader ist sehr einfach: nehmen Sie einen Scheitelpunkt (Position und Farbe), transformieren Sie die Position von Modell Koordinaten in Perspektiven projizierte Koordinaten, und geben Sie diese (zusammen mit der Farbe) an den Rasterizer zurück.</span><span class="sxs-lookup"><span data-stu-id="8ae76-193">The example vertex shader is very simple: take in a vertex (position and color), transform the position from model coordinates into perspective projected coordinates, and return it (along with the color) to the rasterizer.</span></span> <span data-ttu-id="8ae76-194">Beachten Sie, dass der Farbwert direkt zusammen mit den Positionsdaten interpoliert wird, wobei für jedes Pixel ein anderer Wert bereitgestellt wird, auch wenn der Vertexshader keine Berechnungen für den Farbwert durchgeführt hat.</span><span class="sxs-lookup"><span data-stu-id="8ae76-194">Notice that the color value is interpolated right along with the position data, providing a different value for each pixel even though the vertex shader didn't perform any calculations on the color value.</span></span>


```C++
VS_OUTPUT main(VS_INPUT input) // main is the default function name
{
    VS_OUTPUT Output;

    float4 pos = float4(input.vPos, 1.0f);

    // Transform the position from object space to homogeneous projection space
    pos = mul(pos, mWorld);
    pos = mul(pos, View);
    pos = mul(pos, Projection);
    Output.Position = pos;

    // Just pass through the color data
    Output.Color = float4(input.vColor, 1.0f);

    return Output;
}
```



<span data-ttu-id="8ae76-195">Ein komplexerer Vertexshader, wie z. b. ein Objekt, das die Scheitel Punkte eines Objekts für die Phong-Schattierung festlegt, könnte wie folgt aussehen.</span><span class="sxs-lookup"><span data-stu-id="8ae76-195">A more complex vertex shader, such as one that sets up an object's vertices for Phong shading, might look more like this.</span></span> <span data-ttu-id="8ae76-196">In diesem Fall nutzen wir die Tatsache, dass die Vektoren und normale interpoliert werden, um eine nahtlose Oberfläche zu finden.</span><span class="sxs-lookup"><span data-stu-id="8ae76-196">In this case, we're taking advantage of the fact that the vectors and normals are interpolated to approximate a smooth-looking surface.</span></span>

``` syntax
// A constant buffer that stores the three basic column-major matrices for composing geometry.
cbuffer ModelViewProjectionConstantBuffer : register(b0)
{
    matrix model;
    matrix view;
    matrix projection;
};

cbuffer LightConstantBuffer : register(b1)
{
    float4 lightPos;
};

struct VertexShaderInput
{
    float3 pos : POSITION;
    float3 normal : NORMAL;
};

// Per-pixel color data passed through the pixel shader.

struct PixelShaderInput
{
    float4 position : SV_POSITION; 
    float3 outVec : POSITION0;
    float3 outNormal : NORMAL0;
    float3 outLightVec : POSITION1;
};

PixelShaderInput main(VertexShaderInput input)
{
    // Inefficient -- doing this only for instruction. Normally, you would
 // premultiply them on the CPU and place them in the cbuffer.
    matrix mvMatrix = mul(model, view);
    matrix mvpMatrix = mul(mvMatrix, projection);

    PixelShaderInput output;

    float4 pos = float4(input.pos, 1.0f);
    float4 normal = float4(input.normal, 1.0f);
    float4 light = float4(lightPos.xyz, 1.0f);

    // 
    float4 eye = float4(0.0f, 0.0f, -2.0f, 1.0f);

    // Transform the vertex position into projected space.
    output.gl_Position = mul(pos, mvpMatrix);
    output.outNormal = mul(normal, mvMatrix).xyz;
    output.outVec = -(eye - mul(pos, mvMatrix)).xyz;
    output.outLightVec = mul(light, mvMatrix).xyz;

    return output;
}
```

## <a name="review-the-pixel-shader"></a><span data-ttu-id="8ae76-197">Überprüfen Sie den Pixelshader.</span><span class="sxs-lookup"><span data-stu-id="8ae76-197">Review the pixel shader</span></span>

<span data-ttu-id="8ae76-198">Dieser Pixelshader in diesem Beispiel ist möglicherweise die absolute Mindestmenge an Code, den Sie in einem Pixelshader haben können.</span><span class="sxs-lookup"><span data-stu-id="8ae76-198">This pixel shader in this example is quite possibly the absolute minimum amount of code you can have in a pixel shader.</span></span> <span data-ttu-id="8ae76-199">Dabei werden die während der rasterisierung generierten interinterpolierten Pixel Farbdaten verwendet und als Ausgabe zurückgegeben, wo Sie in ein Renderziel geschrieben werden.</span><span class="sxs-lookup"><span data-stu-id="8ae76-199">It takes the interpolated pixel color data generated during rasterization and returns it as output, where it will be written to a render target.</span></span> <span data-ttu-id="8ae76-200">Wie langweilig!</span><span class="sxs-lookup"><span data-stu-id="8ae76-200">How boring!</span></span>


```C++
PS_OUTPUT main(PS_INPUT In)
{
    PS_OUTPUT Output;

    Output.RGBColor = In.Color;

    return Output;
}
```



<span data-ttu-id="8ae76-201">Der wichtige Teil ist die `SV_TARGET` System-Wert-Semantik für den Rückgabewert.</span><span class="sxs-lookup"><span data-stu-id="8ae76-201">The important part is the `SV_TARGET` system-value semantic on the return value.</span></span> <span data-ttu-id="8ae76-202">Gibt an, dass die Ausgabe in das primäre Renderziel geschrieben werden soll. Dies ist der Textur Puffer, der für die Anzeige Kette bereitgestellt wird.</span><span class="sxs-lookup"><span data-stu-id="8ae76-202">It indicates that the output is to be written to the primary render target, which is the texture buffer supplied to the swap chain for display.</span></span> <span data-ttu-id="8ae76-203">Dies ist für Pixel-Shader erforderlich. ohne die Farbdaten aus dem Pixelshader wäre Direct3D nicht zum Anzeigen vorhanden.</span><span class="sxs-lookup"><span data-stu-id="8ae76-203">This is required for pixel shaders - without the color data from the pixel shader, Direct3D wouldn't have anything to display!</span></span>

<span data-ttu-id="8ae76-204">Ein Beispiel für einen komplexeren Pixelshader, um die Phong-Schattierung auszuführen, könnte wie folgt aussehen.</span><span class="sxs-lookup"><span data-stu-id="8ae76-204">An example of a more complex pixel shader to perform Phong shading might look like this.</span></span> <span data-ttu-id="8ae76-205">Da die Vektoren und normale interpoliert wurden, müssen wir Sie nicht pro Pixel berechnen.</span><span class="sxs-lookup"><span data-stu-id="8ae76-205">Since the vectors and normals were interpolated, we don't have to compute them on a per-pixel basis.</span></span> <span data-ttu-id="8ae76-206">Wir müssen Sie jedoch aufgrund der Funktionsweise der Interpolationen erneut normalisieren. konzeptionell müssen wir den Vektor schrittweise von der Richtung in Scheitelpunkt a in Richtung in Vertex B "drehen", wobei seine Länge beibehalten wird. – wheras Interpolation wird stattdessen über eine gerade Linie zwischen den beiden Vektor Endpunkten gekürzt.</span><span class="sxs-lookup"><span data-stu-id="8ae76-206">However, we do have to re-normalize them because of how interpolation works; conceptually, we need to gradually "spin" the vector from direction at vertex A to direction at vertex B, maintaining its length—wheras interpolation instead cuts across a straight line between the two vector endpoints.</span></span>

``` syntax
cbuffer MaterialConstantBuffer : register(b2)
{
    float4 lightColor;
    float4 Ka;
    float4 Kd;
    float4 Ks;
    float4 shininess;
};

struct PixelShaderInput
{
    float4 position : SV_POSITION;
    float3 outVec : POSITION0;
    float3 normal : NORMAL0;
    float3 light : POSITION1;
};

float4 main(PixelShaderInput input) : SV_TARGET
{
    float3 L = normalize(input.light);
    float3 V = normalize(input.outVec);
    float3 R = normalize(reflect(L, input.normal));

    float4 diffuse = Ka + (lightColor * Kd * max(dot(input.normal, L), 0.0f));
    diffuse = saturate(diffuse);

    float4 specular = Ks * pow(max(dot(R, V), 0.0f), shininess.x - 50.0f);
    specular = saturate(specular);

    float4 finalColor = diffuse + specular;

    return finalColor;
}
```

<span data-ttu-id="8ae76-207">In einem anderen Beispiel nimmt der Pixelshader seine eigenen Konstanten Puffer an, die helle und Material Informationen enthalten.</span><span class="sxs-lookup"><span data-stu-id="8ae76-207">In another example, the pixel shader takes its own constant buffers that contain light and material information.</span></span> <span data-ttu-id="8ae76-208">Das Eingabe Layout im Vertexshader würde so erweitert werden, dass es normale Daten enthält, und die Ausgabe dieses Vertexshaders soll die transformierten Vektoren für den Scheitelpunkt, das Licht und den Scheitelpunkt im Ansichts Koordinatensystem einschließen.</span><span class="sxs-lookup"><span data-stu-id="8ae76-208">The input layout in the vertex shader would be expanded to include normal data, and the output from that vertex shader is expected to include transformed vectors for the vertex, the light, and the vertex normal in the view coordinate system.</span></span>

<span data-ttu-id="8ae76-209">Wenn Sie Textur Puffer und Samplern mit zugewiesenen Registern (**t** bzw. **s**) haben, können Sie auch im Pixelshader darauf zugreifen.</span><span class="sxs-lookup"><span data-stu-id="8ae76-209">If you have texture buffers and samplers with assigned registers (**t** and **s**, respectively), you can access them in the pixel shader also.</span></span>

``` syntax
Texture2D simpleTexture : register(t0);
SamplerState simpleSampler : register(s0);

struct PixelShaderInput
{
    float4 pos : SV_POSITION;
    float3 norm : NORMAL;
    float2 tex : TEXCOORD0;
};

float4 SimplePixelShader(PixelShaderInput input) : SV_TARGET
{
    float3 lightDirection = normalize(float3(1, -1, 0));
    float4 texelColor = simpleTexture.Sample(simpleSampler, input.tex);
    float lightMagnitude = 0.8f * saturate(dot(input.norm, -lightDirection)) + 0.2f;
    return texelColor * lightMagnitude;
}
```

<span data-ttu-id="8ae76-210">Shader sind sehr leistungsfähige Tools, die verwendet werden können, um prozedurale Ressourcen wie Schatten Zuordnungen oder Rausch Texturen zu generieren.</span><span class="sxs-lookup"><span data-stu-id="8ae76-210">Shaders are very powerful tools that can be used to generate procedural resources like shadow maps or noise textures.</span></span> <span data-ttu-id="8ae76-211">In der Tat erfordern erweiterte Techniken, dass Sie Texturen abstrakter betrachten, nicht als visuelle Elemente, sondern als Puffer.</span><span class="sxs-lookup"><span data-stu-id="8ae76-211">In fact, advanced techniques require that you think of textures more abstractly, not as visual elements but as buffers.</span></span> <span data-ttu-id="8ae76-212">Sie enthalten Daten wie z. b. Höheninformationen oder andere Daten, die im letzten Pixel-Shader-Durchlauf oder in diesem bestimmten Frame als Teil einer mehrstufigen Auswirkung durchlaufen werden können.</span><span class="sxs-lookup"><span data-stu-id="8ae76-212">They hold data like height information, or other data that can be sampled in the final pixel shader pass or in that particular frame as part of a multi-stage effects pass.</span></span> <span data-ttu-id="8ae76-213">Multisampling ist ein leistungsfähiges Tool und das Backbone aus vielen modernen visuellen Effekten.</span><span class="sxs-lookup"><span data-stu-id="8ae76-213">Multi-sampling is a powerful tool and the backbone of many modern visual effects.</span></span>

## <a name="next-steps"></a><span data-ttu-id="8ae76-214">Nächste Schritte</span><span class="sxs-lookup"><span data-stu-id="8ae76-214">Next steps</span></span>

<span data-ttu-id="8ae76-215">Ich hoffe, dass Sie an diesem Punkt mit DirectX 11vertraut sind und bereit sind, mit der Arbeit an Ihrem Projekt zu beginnen.</span><span class="sxs-lookup"><span data-stu-id="8ae76-215">Hopefully, you're comfortable with DirectX 11at this point and are ready to start working on your project.</span></span> <span data-ttu-id="8ae76-216">Hier finden Sie einige Links, die Ihnen helfen, andere Fragen zu beantworten, die Sie möglicherweise zur Entwicklung mit DirectX und C++ haben:</span><span class="sxs-lookup"><span data-stu-id="8ae76-216">Here are some links to help answer other questions you may have about development with DirectX and C++:</span></span>

-   <span data-ttu-id="8ae76-217">[Entwickeln von Spielen](/previous-versions/windows/apps/hh452744(v=win.10))</span><span class="sxs-lookup"><span data-stu-id="8ae76-217">[Developing games](/previous-versions/windows/apps/hh452744(v=win.10))</span></span>
-   <span data-ttu-id="8ae76-218">[Verwenden von Visual Studio-Tools für die DirectX-Spielprogrammierung](/previous-versions/windows/apps/dn166877(v=win.10))</span><span class="sxs-lookup"><span data-stu-id="8ae76-218">[Use Visual Studio tools for DirectX game programming](/previous-versions/windows/apps/dn166877(v=win.10))</span></span>
-   <span data-ttu-id="8ae76-219">[DirectX-Spieleentwicklung und Exemplarische Vorgehensweisen für Beispiele](/previous-versions/windows/apps/hh465149(v=win.10))</span><span class="sxs-lookup"><span data-stu-id="8ae76-219">[DirectX game development and sample walkthroughs](/previous-versions/windows/apps/hh465149(v=win.10))</span></span>
-   <span data-ttu-id="8ae76-220">[Zusätzliche Programmier Ressourcen für Spiele](/previous-versions/windows/apps/dn194515(v=win.10))</span><span class="sxs-lookup"><span data-stu-id="8ae76-220">[Additional game programming resources](/previous-versions/windows/apps/dn194515(v=win.10))</span></span>

## <a name="related-topics"></a><span data-ttu-id="8ae76-221">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="8ae76-221">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="8ae76-222">Arbeiten mit DirectX-Geräte Ressourcen</span><span class="sxs-lookup"><span data-stu-id="8ae76-222">Work with DirectX device resources</span></span>](work-with-dxgi.md)
</dt> <dt>

[<span data-ttu-id="8ae76-223">Grundlegendes zur Direct3D 11-Renderingpipeline</span><span class="sxs-lookup"><span data-stu-id="8ae76-223">Understand the Direct3D 11 rendering pipeline</span></span>](understand-the-directx-11-2-graphics-pipeline.md)
</dt> </dl>

 

 