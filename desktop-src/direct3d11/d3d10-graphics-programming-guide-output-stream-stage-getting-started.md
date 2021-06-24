---
title: Erste Schritte mit der Stream-Output Stage
description: In diesem Abschnitt wird beschrieben, wie Sie einen Geometrie-Shader mit der Streamausgabephase verwenden.
ms.assetid: 37146486-5922-4833-850c-cc4a51de0957
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ae2e72d25177926c948f43996b6c57d42a7c557b
ms.sourcegitcommit: 749dea42142dec076d41a8f26cb57ae8db46e848
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/24/2021
ms.locfileid: "112587877"
---
# <a name="getting-started-with-the-stream-output-stage"></a><span data-ttu-id="ce8a2-103">Erste Schritte mit der Stream-Output Stage</span><span class="sxs-lookup"><span data-stu-id="ce8a2-103">Getting Started with the Stream-Output Stage</span></span>

<span data-ttu-id="ce8a2-104">In diesem Abschnitt wird beschrieben, wie Sie einen Geometrie-Shader mit der Streamausgabephase verwenden.</span><span class="sxs-lookup"><span data-stu-id="ce8a2-104">This section describes how to use a geometry shader with the stream output stage.</span></span>

## <a name="compile-a-geometry-shader"></a><span data-ttu-id="ce8a2-105">Kompilieren eines Geometrie-Shaders</span><span class="sxs-lookup"><span data-stu-id="ce8a2-105">Compile a Geometry Shader</span></span>

<span data-ttu-id="ce8a2-106">Dieser Geometrie-Shader (GS) berechnet eine Gesichtsnormal für jedes Dreieck und gibt Position, Normal- und Texturkoordinatendaten aus.</span><span class="sxs-lookup"><span data-stu-id="ce8a2-106">This geometry shader (GS) calculates a face normal for each triangle, and outputs position, normal and texture coordinate data.</span></span>


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



<span data-ttu-id="ce8a2-107">Beachten Sie unter Berücksichtigung dieses Codes, dass ein Geometrie-Shader ähnlich wie ein Vertex- oder Pixel-Shader aussieht, jedoch mit den folgenden Ausnahmen: dem von der Funktion zurückgegebenen Typ, den Eingabeparameterdeklarationen und der systeminternen Funktion.</span><span class="sxs-lookup"><span data-stu-id="ce8a2-107">Keeping that code in mind, consider that a geometry shader looks much like a vertex or pixel shader, but with the following exceptions: the type returned by the function, the input parameter declarations, and the intrinsic function.</span></span>



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="ce8a2-108">Element</span><span class="sxs-lookup"><span data-stu-id="ce8a2-108">Item</span></span></th>
<th><span data-ttu-id="ce8a2-109">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="ce8a2-109">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="ce8a2-110"><span id="Function_return_type"></span><span id="function_return_type"></span><span id="FUNCTION_RETURN_TYPE"></span>Funktions-Rückgabetyp</span><span class="sxs-lookup"><span data-stu-id="ce8a2-110"><span id="Function_return_type"></span><span id="function_return_type"></span><span id="FUNCTION_RETURN_TYPE"></span>Function return type</span></span><br/></td>
<td><span data-ttu-id="ce8a2-111">Der Rückgabetyp der Funktion führt eine Aufgabe aus und deklariert die maximale Anzahl von Scheitelzeichen, die vom Shader ausgegeben werden können.</span><span class="sxs-lookup"><span data-stu-id="ce8a2-111">The function return type does one thing, declares the maximum number of vertices that can be output by the shader.</span></span> <span data-ttu-id="ce8a2-112">In diesem Fall <span data-codelanguage=""></span>
</span><span class="sxs-lookup"><span data-stu-id="ce8a2-112">In this case, <span data-codelanguage=""></span>
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

<span data-ttu-id="ce8a2-113">definiert die Ausgabe als maximal 12 Scheiteltices.</span><span class="sxs-lookup"><span data-stu-id="ce8a2-113">defines the output to be a maximum of 12 vertices.</span></span></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="ce8a2-114"><span id="Input_parameter_declarations"></span><span id="input_parameter_declarations"></span><span id="INPUT_PARAMETER_DECLARATIONS"></span>Eingabeparameterdeklarationen</span><span class="sxs-lookup"><span data-stu-id="ce8a2-114"><span id="Input_parameter_declarations"></span><span id="input_parameter_declarations"></span><span id="INPUT_PARAMETER_DECLARATIONS"></span>Input parameter declarations</span></span></p></td>
<td><p><span data-ttu-id="ce8a2-115">Diese Funktion verwendet zwei Eingabeparameter:</span><span class="sxs-lookup"><span data-stu-id="ce8a2-115">This function takes two input parameters:</span></span></p>
<div class="code">
<span data-codelanguage=""></span>
<table>
<colgroup>
<col style="width: 100%" />
</colgroup>
<tbody>
<tr class="odd">
<td><pre><code>triangle GSPS_INPUT input[3] , inout TriangleStream&lt;GSPS_INPUTT&gt; TriStream</code></pre></td>
</tr>
</tbody>
</table>

</div>
<p><span data-ttu-id="ce8a2-116">Der erste Parameter ist ein Array von Scheitelpunkt (in diesem Fall 3), das durch eine GSPS_INPUT-Struktur definiert wird (die Pro-Scheitelpunkt-Daten als Position, normal und Texturkoordinate definiert).</span><span class="sxs-lookup"><span data-stu-id="ce8a2-116">The first parameter is an array of vertices (3 in this case) defined by a GSPS_INPUT structure (which defines per-vertex data as a position, a normal and a texture coordinate).</span></span> <span data-ttu-id="ce8a2-117">Der erste Parameter verwendet auch das Schlüsselwort triangle. Das bedeutet, dass die Stufe des Eingabe-Assemblers Daten an den Geometrie-Shader als einen der primitiven Dreieckstypen (Dreiecksliste oder Dreiecksstreifen) ausgibt.</span><span class="sxs-lookup"><span data-stu-id="ce8a2-117">The first parameter also uses the triangle keyword, which means the input assembler stage must output data to the geometry shader as one of the triangle primitive types (triangle list or triangle strip).</span></span></p>
<p><span data-ttu-id="ce8a2-118">Der zweite Parameter ist ein Dreiecksstream, der durch den Typ TriangleStream &lt; &gt; GSPS_INPUTT.</span><span class="sxs-lookup"><span data-stu-id="ce8a2-118">The second parameter is a triangle stream defined by the type TriangleStream&lt;GSPS_INPUTT&gt;.</span></span> <span data-ttu-id="ce8a2-119">Dies bedeutet, dass der -Parameter ein Array von Dreiecken ist, von denen jedes aus drei Scheitelstellen besteht (die die Daten aus den Membern der GSPS_INPUT).</span><span class="sxs-lookup"><span data-stu-id="ce8a2-119">This means the parameter is an array of triangles, each of which is made up of three vertices (that contain the data from the members of GSPS_INPUT).</span></span></p>
<p><span data-ttu-id="ce8a2-120">Verwenden Sie die Schlüsselwörter triangle und trianglestream, um einzelne Dreiecke oder einen Stream von Dreiecken in einem GS zu identifizieren.</span><span class="sxs-lookup"><span data-stu-id="ce8a2-120">Use the triangle and trianglestream keywords to identify individual triangles or a stream of triangles in a GS.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="ce8a2-121"><span id="Intrinsic_function"></span><span id="intrinsic_function"></span><span id="INTRINSIC_FUNCTION"></span>Systeminterne Funktion</span><span class="sxs-lookup"><span data-stu-id="ce8a2-121"><span id="Intrinsic_function"></span><span id="intrinsic_function"></span><span id="INTRINSIC_FUNCTION"></span>Intrinsic function</span></span></p></td>
<td><p><span data-ttu-id="ce8a2-122">Die Codezeilen in der Shaderfunktion verwenden intrinsische HLSL-Funktionen mit allgemeinem Shaderkern, mit Ausnahme der letzten beiden Zeilen, die Append und RestartStrip aufrufen.</span><span class="sxs-lookup"><span data-stu-id="ce8a2-122">The lines of code in the shader function use common-shader-core HLSL intrinsic functions except the last two lines, which call Append and RestartStrip.</span></span> <span data-ttu-id="ce8a2-123">Diese Funktionen sind nur für einen Geometrie-Shader verfügbar.</span><span class="sxs-lookup"><span data-stu-id="ce8a2-123">These functions are only available to a geometry shader.</span></span> <span data-ttu-id="ce8a2-124">Append informiert den Geometrie-Shader darüber, die Ausgabe an den aktuellen Strip anfügen. RestartStrip erstellt einen neuen primitiven Strip.</span><span class="sxs-lookup"><span data-stu-id="ce8a2-124">Append informs the geometry shader to append the output to the current strip; RestartStrip creates a new primitive strip.</span></span> <span data-ttu-id="ce8a2-125">Bei jedem Aufruf der GS-Phase wird implizit ein neuer Strip erstellt.</span><span class="sxs-lookup"><span data-stu-id="ce8a2-125">A new strip is implicitly created in every invocation of the GS stage.</span></span></p></td>
</tr>
</tbody>
</table>



 

<span data-ttu-id="ce8a2-126">Der Rest des Shaders sieht einem Scheitelpunkt- oder Pixel-Shader sehr ähnlich.</span><span class="sxs-lookup"><span data-stu-id="ce8a2-126">The rest of the shader looks very similar to a vertex or pixel shader.</span></span> <span data-ttu-id="ce8a2-127">Der Geometrie-Shader verwendet eine -Struktur, um Eingabeparameter zu deklarieren, und markiert den Position member mit der SV POSITION-Semantik, um die Hardware darüber zu informieren, dass es sich um \_ Positionsdaten handelt.</span><span class="sxs-lookup"><span data-stu-id="ce8a2-127">The geometry shader uses a structure to declare input parameters and marks the position member with the SV\_POSITION semantic to tell the hardware that this is positional data.</span></span> <span data-ttu-id="ce8a2-128">Die Eingabestruktur identifiziert die anderen beiden Eingabeparameter als Texturkoordinaten (obwohl einer davon eine Gesichtsnormnorm enthält).</span><span class="sxs-lookup"><span data-stu-id="ce8a2-128">The input structure identifies the other two input parameters as texture coordinates (even though one of them will contain a face normal).</span></span> <span data-ttu-id="ce8a2-129">Wenn Sie möchten, können Sie ihre eigene benutzerdefinierte Semantik für die Gesichtsnorm verwenden.</span><span class="sxs-lookup"><span data-stu-id="ce8a2-129">You could use your own custom semantic for the face normal if you prefer.</span></span>

<span data-ttu-id="ce8a2-130">Nachdem Sie den Geometrie-Shader entworfen haben, rufen [**Sie D3DCompile**](/windows/desktop/direct3dhlsl/d3dcompile) auf, um zu kompilieren, wie im folgenden Codebeispiel gezeigt.</span><span class="sxs-lookup"><span data-stu-id="ce8a2-130">Having designed the geometry shader, call [**D3DCompile**](/windows/desktop/direct3dhlsl/d3dcompile) to compile as shown in the following code example.</span></span>


```
DWORD dwShaderFlags = D3DCOMPILE_ENABLE_STRICTNESS;
ID3DBlob** ppShader;

D3DCompile( pSrcData, sizeof( pSrcData ), 
  "Tutorial13.fx", NULL, NULL, "GS", "gs_4_0", 
  dwShaderFlags, 0, &ppShader, NULL );
```



<span data-ttu-id="ce8a2-131">Genau wie Vertex- und Pixel-Shader benötigen Sie ein Shaderflag, um dem Compiler mitteilen zu können, wie der Shader kompiliert werden soll (für das Debuggen, für geschwindigkeitsoptimiert und so weiter), für die Einstiegspunktfunktion und für das Shadermodell, anhand derer überprüft werden soll.</span><span class="sxs-lookup"><span data-stu-id="ce8a2-131">Just like vertex and pixel shaders, you need a shader flag to tell the compiler how you want the shader compiled (for debugging, optimized for speed, and so on), the entry point function, and the shader model to validate against.</span></span> <span data-ttu-id="ce8a2-132">In diesem Beispiel wird mithilfe der GS-Funktion ein Geometrie-Shader erstellt, der aus der Datei Tutorial13.fx erstellt wurde.</span><span class="sxs-lookup"><span data-stu-id="ce8a2-132">This example creates a geometry shader built from the Tutorial13.fx file, by using the GS function.</span></span> <span data-ttu-id="ce8a2-133">Der Shader wird für Shadermodell 4.0 kompiliert.</span><span class="sxs-lookup"><span data-stu-id="ce8a2-133">The shader is compiled for shader model 4.0.</span></span>

## <a name="create-a-geometry-shader-object-with-stream-output"></a><span data-ttu-id="ce8a2-134">Erstellen eines Geometry-Shader Objekts mit Streamausgabe</span><span class="sxs-lookup"><span data-stu-id="ce8a2-134">Create a Geometry-Shader Object with Stream Output</span></span>

<span data-ttu-id="ce8a2-135">Wenn Sie wissen, dass Sie die Daten aus der Geometrie streamen und den Shader erfolgreich kompiliert haben, besteht der nächste Schritt im Aufrufen von [**ID3D11Device::CreateGeometryShaderWithStreamOutput,**](/windows/desktop/api/D3D11/nf-d3d11-id3d11device-creategeometryshaderwithstreamoutput) um das Geometrieshaderobjekt zu erstellen.</span><span class="sxs-lookup"><span data-stu-id="ce8a2-135">Once you know that you will be streaming the data from the geometry, and you have successfully compiled the shader, the next step is to call [**ID3D11Device::CreateGeometryShaderWithStreamOutput**](/windows/desktop/api/D3D11/nf-d3d11-id3d11device-creategeometryshaderwithstreamoutput) to create the geometry shader object.</span></span>

<span data-ttu-id="ce8a2-136">Zunächst müssen Sie jedoch die Eingangssignatur der Phase "Output(SO)" deklarieren.</span><span class="sxs-lookup"><span data-stu-id="ce8a2-136">But first, you need to declare the steam output (SO) stage input signature.</span></span> <span data-ttu-id="ce8a2-137">Diese Signatur stimmt mit den GS-Ausgaben und den SO-Eingaben zum Zeitpunkt der Objekterstellung ab oder überprüft sie.</span><span class="sxs-lookup"><span data-stu-id="ce8a2-137">This signature matches or validates the GS outputs and the SO inputs at the time of object creation.</span></span> <span data-ttu-id="ce8a2-138">Der folgende Code ist ein Beispiel für die SO-Deklaration.</span><span class="sxs-lookup"><span data-stu-id="ce8a2-138">The following code is an example of the SO declaration.</span></span>


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



<span data-ttu-id="ce8a2-139">Diese Funktion verwendet mehrere Parameter, darunter:</span><span class="sxs-lookup"><span data-stu-id="ce8a2-139">This function takes several parameters including:</span></span>

-   <span data-ttu-id="ce8a2-140">Ein Zeiger auf den kompilierten Geometrie-Shader (oder vertex shader, wenn kein Geometrie-Shader vorhanden ist und Daten direkt aus dem Vertex-Shader gestreamt werden).</span><span class="sxs-lookup"><span data-stu-id="ce8a2-140">A pointer to the compiled geometry shader (or vertex shader if no geometry shader will be present and data will be streamed out directly from the vertex shader).</span></span> <span data-ttu-id="ce8a2-141">Informationen zum Abrufen dieses Zeigers finden Sie unter [Getting a Pointer to a Compiled Shader](/windows/desktop/direct3dhlsl/dx-graphics-hlsl-using-shaders-10).</span><span class="sxs-lookup"><span data-stu-id="ce8a2-141">For information about how to get this pointer, see [Getting a Pointer to a Compiled Shader](/windows/desktop/direct3dhlsl/dx-graphics-hlsl-using-shaders-10).</span></span>
-   <span data-ttu-id="ce8a2-142">Ein Zeiger auf ein Array von Deklarationen, die die Eingabedaten für die Streamausgabephase beschreiben.</span><span class="sxs-lookup"><span data-stu-id="ce8a2-142">A pointer to an array of declarations that describe the input data for the stream output stage.</span></span> <span data-ttu-id="ce8a2-143">(Siehe [**D3D11 \_ SO DECLARATION \_ \_ ENTRY**](/windows/desktop/api/D3D11/ns-d3d11-d3d11_so_declaration_entry).) Sie können bis zu 64 Deklarationen, eine für jeden unterschiedlichen Elementtyp, der aus der SO-Phase ausgegeben werden soll, liefern.</span><span class="sxs-lookup"><span data-stu-id="ce8a2-143">(See [**D3D11\_SO\_DECLARATION\_ENTRY**](/windows/desktop/api/D3D11/ns-d3d11-d3d11_so_declaration_entry).) You can supply up to 64 declarations, one for each different type of element to be output from the SO stage.</span></span> <span data-ttu-id="ce8a2-144">Das Array von Deklarationseinträgen beschreibt das Datenlayout, unabhängig davon, ob nur ein einzelner oder mehrere Puffer für die Streamausgabe gebunden werden sollen.</span><span class="sxs-lookup"><span data-stu-id="ce8a2-144">The array of declaration entries describes the data layout regardless of whether only a single buffer or multiple buffers are to be bound for stream output.</span></span>
-   <span data-ttu-id="ce8a2-145">Die Anzahl der Elemente, die von der SO-Phase geschrieben werden.</span><span class="sxs-lookup"><span data-stu-id="ce8a2-145">The number of elements that are written out by the SO stage.</span></span>
-   <span data-ttu-id="ce8a2-146">Ein Zeiger auf das erstellte Geometrieshaderobjekt (siehe [**ID3D11GeometryShader**](/windows/win32/api/d3d11/nn-d3d11-id3d11geometryshader)).</span><span class="sxs-lookup"><span data-stu-id="ce8a2-146">A pointer to the geometry shader object that is created (see [**ID3D11GeometryShader**](/windows/win32/api/d3d11/nn-d3d11-id3d11geometryshader)).</span></span>

<span data-ttu-id="ce8a2-147">In diesem Fall ist der Pufferschritt NULL, der Index des Streams, der an den Rasterizer gesendet werden soll, ist 0, und die Klassenverknüpfungsschnittstelle ist NULL.</span><span class="sxs-lookup"><span data-stu-id="ce8a2-147">In this situation, the buffer stride is NULL, the index of the stream to be sent to the rasterizer is 0, and the class linkage interface is NULL.</span></span>

<span data-ttu-id="ce8a2-148">Die Streamausgabedeklaration definiert, wie Daten in eine Pufferressource geschrieben werden.</span><span class="sxs-lookup"><span data-stu-id="ce8a2-148">The stream output declaration defines the way that data is written to a buffer resource.</span></span> <span data-ttu-id="ce8a2-149">Sie können der Ausgabedeklaration so viele Komponenten hinzufügen, wie Sie möchten.</span><span class="sxs-lookup"><span data-stu-id="ce8a2-149">You can add as many components as you want to the output declaration.</span></span> <span data-ttu-id="ce8a2-150">Verwenden Sie die So-Phase, um in eine einzelne Pufferressource oder viele Pufferressourcen zu schreiben.</span><span class="sxs-lookup"><span data-stu-id="ce8a2-150">Use the SO stage to write to a single buffer resource or many buffer resources.</span></span> <span data-ttu-id="ce8a2-151">Für einen einzelnen Puffer kann die SO-Phase viele verschiedene Elemente pro Scheitelpunkt schreiben.</span><span class="sxs-lookup"><span data-stu-id="ce8a2-151">For a single buffer, the SO stage can write many different elements per-vertex.</span></span> <span data-ttu-id="ce8a2-152">Bei mehreren Puffern kann die SO-Phase nur ein einzelnes Element von Pro-Scheitelpunkt-Daten in jeden Puffer schreiben.</span><span class="sxs-lookup"><span data-stu-id="ce8a2-152">For multiple buffers, the SO stage can only write a single element of per-vertex data to each buffer.</span></span>

<span data-ttu-id="ce8a2-153">Um die SO-Phase ohne einen Geometrieshader zu verwenden, rufen Sie [**ID3D11Device::CreateGeometryShaderWithStreamOutput**](/windows/desktop/api/D3D11/nf-d3d11-id3d11device-creategeometryshaderwithstreamoutput) auf, und übergeben Sie einen Zeiger auf einen Vertexshader an den *pShaderBytecode-Parameter.*</span><span class="sxs-lookup"><span data-stu-id="ce8a2-153">To use the SO stage without using a geometry shader, call [**ID3D11Device::CreateGeometryShaderWithStreamOutput**](/windows/desktop/api/D3D11/nf-d3d11-id3d11device-creategeometryshaderwithstreamoutput) and pass a pointer to a vertex shader to the *pShaderBytecode* parameter.</span></span>

## <a name="set-the-output-targets"></a><span data-ttu-id="ce8a2-154">Festlegen der Ausgabeziele</span><span class="sxs-lookup"><span data-stu-id="ce8a2-154">Set the Output Targets</span></span>

<span data-ttu-id="ce8a2-155">Der letzte Schritt besteht im Festlegen der So-Phasenpuffer.</span><span class="sxs-lookup"><span data-stu-id="ce8a2-155">The last step is to set the SO stage buffers.</span></span> <span data-ttu-id="ce8a2-156">Daten können zur späteren Verwendung in einen oder mehrere Puffer im Arbeitsspeicher gestreamt werden.</span><span class="sxs-lookup"><span data-stu-id="ce8a2-156">Data can be streamed into one or more buffers in memory for use later.</span></span> <span data-ttu-id="ce8a2-157">Der folgende Code zeigt, wie Sie einen einzelnen Puffer erstellen, der für Scheitelpunktdaten sowie für die SO-Phase zum Streamen von Daten verwendet werden kann.</span><span class="sxs-lookup"><span data-stu-id="ce8a2-157">The following code shows how to create a single buffer that can be used for vertex data, as well as for the SO stage to stream data into.</span></span>


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



<span data-ttu-id="ce8a2-158">Erstellen Sie einen Puffer, indem Sie [**ID3D11Device::CreateBuffer aufrufen.**](/windows/desktop/api/D3D11/nf-d3d11-id3d11device-createbuffer)</span><span class="sxs-lookup"><span data-stu-id="ce8a2-158">Create a buffer by calling [**ID3D11Device::CreateBuffer**](/windows/desktop/api/D3D11/nf-d3d11-id3d11device-createbuffer).</span></span> <span data-ttu-id="ce8a2-159">In diesem Beispiel wird die Standardverwendung veranschaulicht. Dies ist typisch für eine Pufferressource, die voraussichtlich relativ häufig von der CPU aktualisiert wird.</span><span class="sxs-lookup"><span data-stu-id="ce8a2-159">This example illustrates default usage, which is typical for a buffer resource that is expected to be updated fairly frequently by the CPU.</span></span> <span data-ttu-id="ce8a2-160">Das Bindungsflag identifiziert die Pipelinephase, an die die Ressource gebunden werden kann.</span><span class="sxs-lookup"><span data-stu-id="ce8a2-160">The binding flag identifies the pipeline stage that the resource can be bound to.</span></span> <span data-ttu-id="ce8a2-161">Jede ressource, die von der SO-Phase verwendet wird, muss auch mit dem Bindungsflag D3D10 \_ BIND STREAM OUTPUT erstellt \_ \_ werden.</span><span class="sxs-lookup"><span data-stu-id="ce8a2-161">Any resource used by the SO stage must also be created with the bind flag D3D10\_BIND\_STREAM\_OUTPUT.</span></span>

<span data-ttu-id="ce8a2-162">Nachdem der Puffer erfolgreich erstellt wurde, legen Sie ihn auf das aktuelle Gerät fest, indem Sie [**ID3D11DeviceContext::SOSetTargets aufrufen:**](/windows/desktop/api/D3D11/nf-d3d11-id3d11devicecontext-sosettargets)</span><span class="sxs-lookup"><span data-stu-id="ce8a2-162">Once the buffer is successfully created, set it to the current device by calling [**ID3D11DeviceContext::SOSetTargets**](/windows/desktop/api/D3D11/nf-d3d11-id3d11devicecontext-sosettargets):</span></span>


```
UINT offset[1] = 0;
D3D11Device->SOSetTargets( 1, &m_pBuffer, offset );
```



<span data-ttu-id="ce8a2-163">Dieser Aufruf nimmt die Anzahl der Puffer, einen Zeiger auf die Puffer und ein Array von Offsets an (ein Offset in jeden der Puffer, der angibt, wo mit dem Schreiben von Daten begonnen werden soll).</span><span class="sxs-lookup"><span data-stu-id="ce8a2-163">This call takes the number of buffers, a pointer to the buffers, and an array of offsets (one offset into each of the buffers that indicates where to begin writing data).</span></span> <span data-ttu-id="ce8a2-164">Daten werden in diese Streamingausgabepuffer geschrieben, wenn eine draw-Funktion aufgerufen wird.</span><span class="sxs-lookup"><span data-stu-id="ce8a2-164">Data will be written to these streaming-output buffers when a draw function is called.</span></span> <span data-ttu-id="ce8a2-165">Eine interne Variable verfolgt die Position, an der mit dem Schreiben von Daten in die Streamingausgabepuffer begonnen werden soll, und diese Variablen werden weiter erhöht, bis [**SOSetTargets**](/windows/desktop/api/D3D11/nf-d3d11-id3d11devicecontext-sosettargets) erneut aufgerufen wird und ein neuer Offsetwert angegeben wird.</span><span class="sxs-lookup"><span data-stu-id="ce8a2-165">An internal variable keeps track of the position for where to begin writing data to the streaming-output buffers, and that variables will continue to increment until [**SOSetTargets**](/windows/desktop/api/D3D11/nf-d3d11-id3d11devicecontext-sosettargets) is called again and a new offset value is specified.</span></span>

<span data-ttu-id="ce8a2-166">Alle Daten, die in die Zielpuffer geschrieben werden, sind 32-Bit-Werte.</span><span class="sxs-lookup"><span data-stu-id="ce8a2-166">All data written out to the target buffers will be 32-bit values.</span></span>

## <a name="related-topics"></a><span data-ttu-id="ce8a2-167">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="ce8a2-167">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="ce8a2-168">Streamausgabephase</span><span class="sxs-lookup"><span data-stu-id="ce8a2-168">Stream-Output Stage</span></span>](d3d10-graphics-programming-guide-output-stream-stage.md)
</dt> </dl>

 

