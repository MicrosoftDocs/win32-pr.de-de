---
title: Ersten Einstieg in die Stream-Output Phase
description: In diesem Abschnitt wird beschrieben, wie ein Geometry-Shader mit der Stream-Ausgabestufe verwendet wird.
ms.assetid: 37146486-5922-4833-850c-cc4a51de0957
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 909b3ba37e8b80201a4afc3e5bf18f016fed38a0
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "104976737"
---
# <a name="getting-started-with-the-stream-output-stage"></a><span data-ttu-id="9c0af-103">Ersten Einstieg in die Stream-Output Phase</span><span class="sxs-lookup"><span data-stu-id="9c0af-103">Getting Started with the Stream-Output Stage</span></span>

<span data-ttu-id="9c0af-104">In diesem Abschnitt wird beschrieben, wie ein Geometry-Shader mit der Stream-Ausgabestufe verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="9c0af-104">This section describes how to use a geometry shader with the stream output stage.</span></span>

## <a name="compile-a-geometry-shader"></a><span data-ttu-id="9c0af-105">Kompilieren eines Geometry-Shaders</span><span class="sxs-lookup"><span data-stu-id="9c0af-105">Compile a Geometry Shader</span></span>

<span data-ttu-id="9c0af-106">Dieser Geometry-Shader (GS) berechnet eine Vorderseite für jedes Dreieck und gibt Positions-, normal-und Texturkoordinaten Daten aus.</span><span class="sxs-lookup"><span data-stu-id="9c0af-106">This geometry shader (GS) calculates a face normal for each triangle, and outputs position, normal and texture coordinate data.</span></span>


```
struct GSPS_INPUT
{
    float4 Pos : SV_POSITION;
    float3 Norm : TEXCOORD0;
    float2 Tex : TEXCOORD1;
};

[maxvertexcount(12)]
void GS( triangle GSPS_INPUT input[3], inout TriangleStream<GSPS_INPUT> TriStream )
{
    GSPS_INPUT output;
    
    //
    // Calculate the face normal
    //
    float3 faceEdgeA = input[1].Pos - input[0].Pos;
    float3 faceEdgeB = input[2].Pos - input[0].Pos;
    float3 faceNormal = normalize( cross(faceEdgeA, faceEdgeB) );
    float3 ExplodeAmt = faceNormal*Explode;
    
    //
    // Calculate the face center
    //
    float3 centerPos = (input[0].Pos.xyz + input[1].Pos.xyz + input[2].Pos.xyz)/3.0;
    float2 centerTex = (input[0].Tex + input[1].Tex + input[2].Tex)/3.0;
    centerPos += faceNormal*Explode;
    
    //
    // Output the pyramid
    //
    for( int i=0; i<3; i++ )
    {
        output.Pos = input[i].Pos + float4(ExplodeAmt,0);
        output.Pos = mul( output.Pos, View );
        output.Pos = mul( output.Pos, Projection );
        output.Norm = input[i].Norm;
        output.Tex = input[i].Tex;
        TriStream.Append( output );
        
        int iNext = (i+1)%3;
        output.Pos = input[iNext].Pos + float4(ExplodeAmt,0);
        output.Pos = mul( output.Pos, View );
        output.Pos = mul( output.Pos, Projection );
        output.Norm = input[iNext].Norm;
        output.Tex = input[iNext].Tex;
        TriStream.Append( output );
        
        output.Pos = float4(centerPos,1) + float4(ExplodeAmt,0);
        output.Pos = mul( output.Pos, View );
        output.Pos = mul( output.Pos, Projection );
        output.Norm = faceNormal;
        output.Tex = centerTex;
        TriStream.Append( output );
        
        TriStream.RestartStrip();
    }
    
    for( int i=2; i>=0; i-- )
    {
        output.Pos = input[i].Pos + float4(ExplodeAmt,0);
        output.Pos = mul( output.Pos, View );
        output.Pos = mul( output.Pos, Projection );
        output.Norm = -input[i].Norm;
        output.Tex = input[i].Tex;
        TriStream.Append( output );
    }
    TriStream.RestartStrip();
}
```



<span data-ttu-id="9c0af-107">Beachten Sie dabei, dass ein Geometry-Shader ähnlich wie ein Scheitelpunkt oder Pixel-Shader aussieht, aber mit den folgenden Ausnahmen: der von der Funktion zurückgegebene Typ, die Eingabeparameter Deklarationen und die intrinsische Funktion.</span><span class="sxs-lookup"><span data-stu-id="9c0af-107">Keeping that code in mind, consider that a geometry shader looks much like a vertex or pixel shader, but with the following exceptions: the type returned by the function, the input parameter declarations, and the intrinsic function.</span></span>



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="9c0af-108">Element</span><span class="sxs-lookup"><span data-stu-id="9c0af-108">Item</span></span></th>
<th><span data-ttu-id="9c0af-109">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="9c0af-109">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="9c0af-110"><span id="Function_return_type"></span><span id="function_return_type"></span><span id="FUNCTION_RETURN_TYPE"></span>Funktions Rückgabetyp</span><span class="sxs-lookup"><span data-stu-id="9c0af-110"><span id="Function_return_type"></span><span id="function_return_type"></span><span id="FUNCTION_RETURN_TYPE"></span>Function return type</span></span><br/></td>
<td><span data-ttu-id="9c0af-111">Der Funktions Rückgabetyp bewirkt, dass die maximale Anzahl der Scheitel Punkte deklariert, die vom Shader ausgegeben werden können.</span><span class="sxs-lookup"><span data-stu-id="9c0af-111">The function return type does one thing, declares the maximum number of vertices that can be output by the shader.</span></span> <span data-ttu-id="9c0af-112">In diesem Fall <span data-codelanguage=""></span>
</span><span class="sxs-lookup"><span data-stu-id="9c0af-112">In this case, <span data-codelanguage=""></span>
</span></span><table>
<colgroup>
<col style="width: 100%" />
</colgroup>
<tbody>
<tr class="odd">
<td><pre><code>maxvertexcount(12)</code></pre></td>
</tr>
</tbody>
</table>

<span data-ttu-id="9c0af-113">definiert die Ausgabe als maximal 12 Vertices.</span><span class="sxs-lookup"><span data-stu-id="9c0af-113">defines the output to be a maximum of 12 vertices.</span></span></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="9c0af-114"><span id="Input_parameter_declarations"></span><span id="input_parameter_declarations"></span><span id="INPUT_PARAMETER_DECLARATIONS"></span>Eingabeparameter Deklarationen</span><span class="sxs-lookup"><span data-stu-id="9c0af-114"><span id="Input_parameter_declarations"></span><span id="input_parameter_declarations"></span><span id="INPUT_PARAMETER_DECLARATIONS"></span>Input parameter declarations</span></span></p></td>
<td><p><span data-ttu-id="9c0af-115">Diese Funktion nimmt zwei Eingabeparameter an:</span><span class="sxs-lookup"><span data-stu-id="9c0af-115">This function takes two input parameters:</span></span></p>
<div class="code">
<span data-codelanguage=""></span>
<table>
<colgroup>
<col style="width: 100%" />
</colgroup>
<tbody>
<tr class="odd">
<td><pre><code>triangle GSPS_INPUT input[3] , inout TriangleStream<GSPS_INPUT> TriStream</code></pre></td>
</tr>
</tbody>
</table>

</div>
<p><span data-ttu-id="9c0af-116">Der erste Parameter ist ein Array von Vertices (in diesem Fall 3), das durch eine GSPS_INPUT Struktur definiert wird (die pro-Vertex-Daten als eine Position, eine normale und eine Textur Koordinate definiert).</span><span class="sxs-lookup"><span data-stu-id="9c0af-116">The first parameter is an array of vertices (3 in this case) defined by a GSPS_INPUT structure (which defines per-vertex data as a position, a normal and a texture coordinate).</span></span> <span data-ttu-id="9c0af-117">Der erste Parameter verwendet auch das Dreiecks Schlüsselwort. Dies bedeutet, dass die Eingabe Assembler-Stufe Daten an den Geometry-Shader als einen der Grundtypen des Dreiecks (Dreiecks Liste oder Dreieck) ausgeben muss.</span><span class="sxs-lookup"><span data-stu-id="9c0af-117">The first parameter also uses the triangle keyword, which means the input assembler stage must output data to the geometry shader as one of the triangle primitive types (triangle list or triangle strip).</span></span></p>
<p><span data-ttu-id="9c0af-118">Der zweite Parameter ist ein vom Typ trianglestream definierter Dreiecks Datenstrom <GSPS_INPUT> .</span><span class="sxs-lookup"><span data-stu-id="9c0af-118">The second parameter is a triangle stream defined by the type TriangleStream<GSPS_INPUT>.</span></span> <span data-ttu-id="9c0af-119">Dies bedeutet, dass es sich bei dem Parameter um ein Array von Dreiecken handelt, von denen jede aus drei Vertices besteht (die die Daten aus den Membern von GSPS_INPUT enthalten).</span><span class="sxs-lookup"><span data-stu-id="9c0af-119">This means the parameter is an array of triangles, each of which is made up of three vertices (that contain the data from the members of GSPS_INPUT).</span></span></p>
<p><span data-ttu-id="9c0af-120">Verwenden Sie die Schlüsselwörter Dreieck und trianglestream, um einzelne Dreiecke oder einen Datenstrom von Dreiecken in einer GS zu identifizieren.</span><span class="sxs-lookup"><span data-stu-id="9c0af-120">Use the triangle and trianglestream keywords to identify individual triangles or a stream of triangles in a GS.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="9c0af-121"><span id="Intrinsic_function"></span><span id="intrinsic_function"></span><span id="INTRINSIC_FUNCTION"></span>Intrinsische Funktion</span><span class="sxs-lookup"><span data-stu-id="9c0af-121"><span id="Intrinsic_function"></span><span id="intrinsic_function"></span><span id="INTRINSIC_FUNCTION"></span>Intrinsic function</span></span></p></td>
<td><p><span data-ttu-id="9c0af-122">In den Codezeilen in der Shader-Funktion werden intrinsische HLSL-Funktionen von Common-Shader-Core verwendet, mit Ausnahme der letzten beiden Zeilen, die "append" und "restartstrip" aufrufen.</span><span class="sxs-lookup"><span data-stu-id="9c0af-122">The lines of code in the shader function use common-shader-core HLSL intrinsic functions except the last two lines, which call Append and RestartStrip.</span></span> <span data-ttu-id="9c0af-123">Diese Funktionen sind nur für einen Geometry-Shader verfügbar.</span><span class="sxs-lookup"><span data-stu-id="9c0af-123">These functions are only available to a geometry shader.</span></span> <span data-ttu-id="9c0af-124">Anfügen informiert den Geometry-Shader darüber, dass die Ausgabe an den aktuellen Strip angefügt werden soll. Restartstrip erstellt einen neuen primitiven Strip.</span><span class="sxs-lookup"><span data-stu-id="9c0af-124">Append informs the geometry shader to append the output to the current strip; RestartStrip creates a new primitive strip.</span></span> <span data-ttu-id="9c0af-125">Ein neuer Strip wird bei jedem Aufruf der GS-Phase implizit erstellt.</span><span class="sxs-lookup"><span data-stu-id="9c0af-125">A new strip is implicitly created in every invocation of the GS stage.</span></span></p></td>
</tr>
</tbody>
</table>



 

<span data-ttu-id="9c0af-126">Der Rest des Shader ähnelt einem Scheitelpunkt oder einem Pixelshader.</span><span class="sxs-lookup"><span data-stu-id="9c0af-126">The rest of the shader looks very similar to a vertex or pixel shader.</span></span> <span data-ttu-id="9c0af-127">Der Geometry-Shader verwendet eine-Struktur, um Eingabeparameter zu deklarieren, und markiert das Positions Element mit der SV- \_ Positions Semantik, um der Hardware mitzuteilen, dass es sich um Positionsdaten handelt.</span><span class="sxs-lookup"><span data-stu-id="9c0af-127">The geometry shader uses a structure to declare input parameters and marks the position member with the SV\_POSITION semantic to tell the hardware that this is positional data.</span></span> <span data-ttu-id="9c0af-128">Die Eingabe Struktur identifiziert die anderen beiden Eingabeparameter als Texturkoordinaten (auch wenn einer von Ihnen ein Gesicht normal enthält).</span><span class="sxs-lookup"><span data-stu-id="9c0af-128">The input structure identifies the other two input parameters as texture coordinates (even though one of them will contain a face normal).</span></span> <span data-ttu-id="9c0af-129">Wenn Sie möchten, können Sie Ihre eigene benutzerdefinierte Semantik für die Vorderseite verwenden.</span><span class="sxs-lookup"><span data-stu-id="9c0af-129">You could use your own custom semantic for the face normal if you prefer.</span></span>

<span data-ttu-id="9c0af-130">Nachdem Sie den Geometry-Shader entworfen haben, müssen Sie [**D3DCompile**](/windows/desktop/direct3dhlsl/d3dcompile) zum Kompilieren aufrufen, wie im folgenden Codebeispiel gezeigt.</span><span class="sxs-lookup"><span data-stu-id="9c0af-130">Having designed the geometry shader, call [**D3DCompile**](/windows/desktop/direct3dhlsl/d3dcompile) to compile as shown in the following code example.</span></span>


```
DWORD dwShaderFlags = D3DCOMPILE_ENABLE_STRICTNESS;
ID3DBlob** ppShader;

D3DCompile( pSrcData, sizeof( pSrcData ), 
  "Tutorial13.fx", NULL, NULL, "GS", "gs_4_0", 
  dwShaderFlags, 0, &ppShader, NULL );
```



<span data-ttu-id="9c0af-131">Genau wie Scheitelpunkt-und Pixel-Shader benötigen Sie ein Shader-Flag, um dem Compiler mitzuteilen, wie der Shader kompiliert werden soll (für das Debuggen, optimiert für Geschwindigkeit usw.), die Einstiegspunkt Funktion und das Shader-Modell, anhand dessen validiert werden soll.</span><span class="sxs-lookup"><span data-stu-id="9c0af-131">Just like vertex and pixel shaders, you need a shader flag to tell the compiler how you want the shader compiled (for debugging, optimized for speed, and so on), the entry point function, and the shader model to validate against.</span></span> <span data-ttu-id="9c0af-132">In diesem Beispiel wird ein Geometry-Shader erstellt, der aus der Datei Tutorial13. FX erstellt wurde, indem die GS-Funktion verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="9c0af-132">This example creates a geometry shader built from the Tutorial13.fx file, by using the GS function.</span></span> <span data-ttu-id="9c0af-133">Der Shader wird für das Shader-Modell 4,0 kompiliert.</span><span class="sxs-lookup"><span data-stu-id="9c0af-133">The shader is compiled for shader model 4.0.</span></span>

## <a name="create-a-geometry-shader-object-with-stream-output"></a><span data-ttu-id="9c0af-134">Erstellen eines Geometry-Shader Objekts mit Datenstrom Ausgabe</span><span class="sxs-lookup"><span data-stu-id="9c0af-134">Create a Geometry-Shader Object with Stream Output</span></span>

<span data-ttu-id="9c0af-135">Wenn Sie wissen, dass Sie die Daten aus der Geometrie streamen, und Sie den Shader erfolgreich kompiliert haben, besteht der nächste Schritt im Aufrufen von [**ID3D11Device:: kreategeometryshaderwithstreamoutput**](/windows/desktop/api/D3D11/nf-d3d11-id3d11device-creategeometryshaderwithstreamoutput) zum Erstellen des Geometry-Shader-Objekts.</span><span class="sxs-lookup"><span data-stu-id="9c0af-135">Once you know that you will be streaming the data from the geometry, and you have successfully compiled the shader, the next step is to call [**ID3D11Device::CreateGeometryShaderWithStreamOutput**](/windows/desktop/api/D3D11/nf-d3d11-id3d11device-creategeometryshaderwithstreamoutput) to create the geometry shader object.</span></span>

<span data-ttu-id="9c0af-136">Zuerst müssen Sie jedoch die Eingabe Signatur der Ausgabe der Ausgabe (also) deklarieren.</span><span class="sxs-lookup"><span data-stu-id="9c0af-136">But first, you need to declare the steam output (SO) stage input signature.</span></span> <span data-ttu-id="9c0af-137">Diese Signatur gleicht die GS-Ausgaben und die so-Eingaben zum Zeitpunkt der Objekt Erstellung ab oder überprüft sie.</span><span class="sxs-lookup"><span data-stu-id="9c0af-137">This signature matches or validates the GS outputs and the SO inputs at the time of object creation.</span></span> <span data-ttu-id="9c0af-138">Der folgende Code ist ein Beispiel für die so-Deklaration.</span><span class="sxs-lookup"><span data-stu-id="9c0af-138">The following code is an example of the SO declaration.</span></span>


```
D3D11_SO_DECLARATION_ENTRY pDecl[] =
{
    // semantic name, semantic index, start component, component count, output slot
    { "SV_POSITION", 0, 0, 4, 0 },   // output all components of position
    { "TEXCOORD0", 0, 0, 3, 0 },     // output the first 3 of the normal
    { "TEXCOORD1", 0, 0, 2, 0 },     // output the first 2 texture coordinates
};

D3D11Device->CreateGeometryShaderWithStreamOut( pShaderBytecode, ShaderBytecodesize, pDecl, 
    sizeof(pDecl), NULL, 0, 0, NULL, &pStreamOutGS );
```



<span data-ttu-id="9c0af-139">Diese Funktion erfordert mehrere Parameter, einschließlich:</span><span class="sxs-lookup"><span data-stu-id="9c0af-139">This function takes several parameters including:</span></span>

-   <span data-ttu-id="9c0af-140">Ein Zeiger auf den kompilierten Geometry-Shader (oder Vertex-Shader, wenn kein Geometry-Shader vorhanden ist und die Daten direkt aus dem Vertexshader gestreamt werden).</span><span class="sxs-lookup"><span data-stu-id="9c0af-140">A pointer to the compiled geometry shader (or vertex shader if no geometry shader will be present and data will be streamed out directly from the vertex shader).</span></span> <span data-ttu-id="9c0af-141">Weitere Informationen zum Aufrufen dieses Zeigers finden Sie unter "aufrufen [eines Zeigers auf einen kompilierten Shader](/windows/desktop/direct3dhlsl/dx-graphics-hlsl-using-shaders-10)".</span><span class="sxs-lookup"><span data-stu-id="9c0af-141">For information about how to get this pointer, see [Getting a Pointer to a Compiled Shader](/windows/desktop/direct3dhlsl/dx-graphics-hlsl-using-shaders-10).</span></span>
-   <span data-ttu-id="9c0af-142">Ein Zeiger auf ein Array von Deklarationen, die die Eingabedaten für die Stream-Ausgabe Phase beschreiben.</span><span class="sxs-lookup"><span data-stu-id="9c0af-142">A pointer to an array of declarations that describe the input data for the stream output stage.</span></span> <span data-ttu-id="9c0af-143">(Siehe [**D3D11 \_ so- \_ Deklarations \_ Eintrag**](/windows/desktop/api/D3D11/ns-d3d11-d3d11_so_declaration_entry).) Sie können bis zu 64 Deklarationen angeben, eine für jeden Elementtyp, der aus der so-Phase ausgegeben werden soll.</span><span class="sxs-lookup"><span data-stu-id="9c0af-143">(See [**D3D11\_SO\_DECLARATION\_ENTRY**](/windows/desktop/api/D3D11/ns-d3d11-d3d11_so_declaration_entry).) You can supply up to 64 declarations, one for each different type of element to be output from the SO stage.</span></span> <span data-ttu-id="9c0af-144">Das Array der Deklarations Einträge beschreibt das Datenlayout, unabhängig davon, ob nur ein einzelner Puffer oder mehrere Puffer an die Streamausgabe gebunden werden sollen.</span><span class="sxs-lookup"><span data-stu-id="9c0af-144">The array of declaration entries describes the data layout regardless of whether only a single buffer or multiple buffers are to be bound for stream output.</span></span>
-   <span data-ttu-id="9c0af-145">Die Anzahl der Elemente, die von der so-Phase ausgeschrieben werden.</span><span class="sxs-lookup"><span data-stu-id="9c0af-145">The number of elements that are written out by the SO stage.</span></span>
-   <span data-ttu-id="9c0af-146">Ein Zeiger auf das Geometry-Shader-Objekt, das erstellt wird (siehe [**ID3D11GeometryShader**](/windows/win32/api/d3d11/nn-d3d11-id3d11geometryshader)).</span><span class="sxs-lookup"><span data-stu-id="9c0af-146">A pointer to the geometry shader object that is created (see [**ID3D11GeometryShader**](/windows/win32/api/d3d11/nn-d3d11-id3d11geometryshader)).</span></span>

<span data-ttu-id="9c0af-147">In dieser Situation ist der Puffer Stride NULL. der Index des Datenstroms, der an den Raster gesendet werden soll, ist 0, und die Klassen Verknüpfungs Schnittstelle ist NULL.</span><span class="sxs-lookup"><span data-stu-id="9c0af-147">In this situation, the buffer stride is NULL, the index of the stream to be sent to the rasterizer is 0, and the class linkage interface is NULL.</span></span>

<span data-ttu-id="9c0af-148">Die Datenstrom-Ausgabe Deklaration definiert, wie Daten in eine Puffer Ressource geschrieben werden.</span><span class="sxs-lookup"><span data-stu-id="9c0af-148">The stream output declaration defines the way that data is written to a buffer resource.</span></span> <span data-ttu-id="9c0af-149">Sie können der Ausgabe Deklaration beliebig viele Komponenten hinzufügen.</span><span class="sxs-lookup"><span data-stu-id="9c0af-149">You can add as many components as you want to the output declaration.</span></span> <span data-ttu-id="9c0af-150">Verwenden Sie die so-Phase, um in eine einzelne Puffer Ressource oder viele Puffer Ressourcen zu schreiben.</span><span class="sxs-lookup"><span data-stu-id="9c0af-150">Use the SO stage to write to a single buffer resource or many buffer resources.</span></span> <span data-ttu-id="9c0af-151">Bei einem einzelnen Puffer kann die so-Phase viele verschiedene Elemente pro Scheitelpunkt schreiben.</span><span class="sxs-lookup"><span data-stu-id="9c0af-151">For a single buffer, the SO stage can write many different elements per-vertex.</span></span> <span data-ttu-id="9c0af-152">Für mehrere Puffer kann die so-Phase nur ein einzelnes Element von pro-Vertex-Daten in jeden Puffer schreiben.</span><span class="sxs-lookup"><span data-stu-id="9c0af-152">For multiple buffers, the SO stage can only write a single element of per-vertex data to each buffer.</span></span>

<span data-ttu-id="9c0af-153">Um die so-Phase ohne Verwendung eines Geometry-Shaders zu verwenden, müssen Sie [**ID3D11Device:: deategeometryshaderwithstreamoutput**](/windows/desktop/api/D3D11/nf-d3d11-id3d11device-creategeometryshaderwithstreamoutput) aufrufen und einen Zeiger auf einen Vertex-Shader an den *pshaderbytecode* -Parameter übergeben.</span><span class="sxs-lookup"><span data-stu-id="9c0af-153">To use the SO stage without using a geometry shader, call [**ID3D11Device::CreateGeometryShaderWithStreamOutput**](/windows/desktop/api/D3D11/nf-d3d11-id3d11device-creategeometryshaderwithstreamoutput) and pass a pointer to a vertex shader to the *pShaderBytecode* parameter.</span></span>

## <a name="set-the-output-targets"></a><span data-ttu-id="9c0af-154">Festlegen der Ausgabe Ziele</span><span class="sxs-lookup"><span data-stu-id="9c0af-154">Set the Output Targets</span></span>

<span data-ttu-id="9c0af-155">Der letzte Schritt besteht darin, die so-Phasen Puffer festzulegen.</span><span class="sxs-lookup"><span data-stu-id="9c0af-155">The last step is to set the SO stage buffers.</span></span> <span data-ttu-id="9c0af-156">Daten können zur späteren Verwendung in einen oder mehrere Puffer im Arbeitsspeicher gestreamt werden.</span><span class="sxs-lookup"><span data-stu-id="9c0af-156">Data can be streamed into one or more buffers in memory for use later.</span></span> <span data-ttu-id="9c0af-157">Der folgende Code zeigt, wie ein einzelner Puffer erstellt wird, der für Scheitelpunkt Daten verwendet werden kann, sowie für die so-Phase, um Daten in zu streamen.</span><span class="sxs-lookup"><span data-stu-id="9c0af-157">The following code shows how to create a single buffer that can be used for vertex data, as well as for the SO stage to stream data into.</span></span>


```
ID3D11Buffer *m_pBuffer;
int m_nBufferSize = 1000000;

D3D11_BUFFER_DESC bufferDesc =
{
    m_nBufferSize,
    D3D11_USAGE_DEFAULT,
    D3D11_BIND_STREAM_OUTPUT,
    0,
    0,
    0
};
D3D11Device->CreateBuffer( &bufferDesc, NULL, &m_pBuffer );
```



<span data-ttu-id="9c0af-158">Erstellen Sie einen Puffer durch Aufrufen von [**ID3D11Device:: createbuffer**](/windows/desktop/api/D3D11/nf-d3d11-id3d11device-createbuffer).</span><span class="sxs-lookup"><span data-stu-id="9c0af-158">Create a buffer by calling [**ID3D11Device::CreateBuffer**](/windows/desktop/api/D3D11/nf-d3d11-id3d11device-createbuffer).</span></span> <span data-ttu-id="9c0af-159">Dieses Beispiel veranschaulicht die Standardverwendung, die typisch für eine Puffer Ressource ist, die relativ häufig von der CPU aktualisiert werden soll.</span><span class="sxs-lookup"><span data-stu-id="9c0af-159">This example illustrates default usage, which is typical for a buffer resource that is expected to be updated fairly frequently by the CPU.</span></span> <span data-ttu-id="9c0af-160">Das Bindungsflag identifiziert die Pipeline Stufe, an die die Ressource gebunden werden kann.</span><span class="sxs-lookup"><span data-stu-id="9c0af-160">The binding flag identifies the pipeline stage that the resource can be bound to.</span></span> <span data-ttu-id="9c0af-161">Alle Ressourcen, die von der so-Phase verwendet werden, müssen auch mit dem Bindungsflag d3d10 \_ Bind \_ Stream Output erstellt werden \_ .</span><span class="sxs-lookup"><span data-stu-id="9c0af-161">Any resource used by the SO stage must also be created with the bind flag D3D10\_BIND\_STREAM\_OUTPUT.</span></span>

<span data-ttu-id="9c0af-162">Nachdem der Puffer erfolgreich erstellt wurde, legen Sie ihn auf das aktuelle Gerät durch Aufrufen von [**Verknüpfung id3d11devicecontext aus:: sosettargets**](/windows/desktop/api/D3D11/nf-d3d11-id3d11devicecontext-sosettargets)fest:</span><span class="sxs-lookup"><span data-stu-id="9c0af-162">Once the buffer is successfully created, set it to the current device by calling [**ID3D11DeviceContext::SOSetTargets**](/windows/desktop/api/D3D11/nf-d3d11-id3d11devicecontext-sosettargets):</span></span>


```
UINT offset[1] = 0;
D3D11Device->SOSetTargets( 1, &m_pBuffer, offset );
```



<span data-ttu-id="9c0af-163">Dieser Befehl nimmt die Anzahl von Puffern, einen Zeiger auf die Puffer und ein Array von Offsets (ein Offset in jeden Puffer, der angibt, wohin mit dem Schreiben von Daten begonnen werden soll).</span><span class="sxs-lookup"><span data-stu-id="9c0af-163">This call takes the number of buffers, a pointer to the buffers, and an array of offsets (one offset into each of the buffers that indicates where to begin writing data).</span></span> <span data-ttu-id="9c0af-164">Daten werden in diese streamingausgabepuffer geschrieben, wenn eine Draw-Funktion aufgerufen wird.</span><span class="sxs-lookup"><span data-stu-id="9c0af-164">Data will be written to these streaming-output buffers when a draw function is called.</span></span> <span data-ttu-id="9c0af-165">Eine interne Variable verfolgt die Position, an der mit dem Schreiben von Daten in die streamingausgabepuffer begonnen werden soll, und gibt an, dass die Variablen weiterhin erhöht werden, bis [**sosettargets**](/windows/desktop/api/D3D11/nf-d3d11-id3d11devicecontext-sosettargets) erneut aufgerufen wird und ein neuer Offset Wert angegeben wird.</span><span class="sxs-lookup"><span data-stu-id="9c0af-165">An internal variable keeps track of the position for where to begin writing data to the streaming-output buffers, and that variables will continue to increment until [**SOSetTargets**](/windows/desktop/api/D3D11/nf-d3d11-id3d11devicecontext-sosettargets) is called again and a new offset value is specified.</span></span>

<span data-ttu-id="9c0af-166">Alle Daten, die in die Ziel Puffer geschrieben werden, sind 32-Bit-Werte.</span><span class="sxs-lookup"><span data-stu-id="9c0af-166">All data written out to the target buffers will be 32-bit values.</span></span>

## <a name="related-topics"></a><span data-ttu-id="9c0af-167">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="9c0af-167">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="9c0af-168">Stream-Ausgabe Phase</span><span class="sxs-lookup"><span data-stu-id="9c0af-168">Stream-Output Stage</span></span>](d3d10-graphics-programming-guide-output-stream-stage.md)
</dt> </dl>

 

