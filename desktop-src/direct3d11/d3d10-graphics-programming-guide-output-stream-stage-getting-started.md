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
# <a name="getting-started-with-the-stream-output-stage"></a>Erste Schritte mit der Stream-Output Stage

In diesem Abschnitt wird beschrieben, wie Sie einen Geometrie-Shader mit der Streamausgabephase verwenden.

## <a name="compile-a-geometry-shader"></a>Kompilieren eines Geometrie-Shaders

Dieser Geometrie-Shader (GS) berechnet eine Gesichtsnormal für jedes Dreieck und gibt Position, Normal- und Texturkoordinatendaten aus.


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



Beachten Sie unter Berücksichtigung dieses Codes, dass ein Geometrie-Shader ähnlich wie ein Vertex- oder Pixel-Shader aussieht, jedoch mit den folgenden Ausnahmen: dem von der Funktion zurückgegebenen Typ, den Eingabeparameterdeklarationen und der systeminternen Funktion.



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th>Element</th>
<th>Beschreibung</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span id="Function_return_type"></span><span id="function_return_type"></span><span id="FUNCTION_RETURN_TYPE"></span>Funktions-Rückgabetyp<br/></td>
<td>Der Rückgabetyp der Funktion führt eine Aufgabe aus und deklariert die maximale Anzahl von Scheitelzeichen, die vom Shader ausgegeben werden können. In diesem Fall <span data-codelanguage=""></span>
<table>
<colgroup>
<col style="width: 100%" />
</colgroup>
<tbody>
<tr class="odd">
<td><pre><code>maxvertexcount(12)</code></pre></td>
</tr>
</tbody>
</table>

definiert die Ausgabe als maximal 12 Scheiteltices.</td>
</tr>
<tr class="even">
<td><p><span id="Input_parameter_declarations"></span><span id="input_parameter_declarations"></span><span id="INPUT_PARAMETER_DECLARATIONS"></span>Eingabeparameterdeklarationen</p></td>
<td><p>Diese Funktion verwendet zwei Eingabeparameter:</p>
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
<p>Der erste Parameter ist ein Array von Scheitelpunkt (in diesem Fall 3), das durch eine GSPS_INPUT-Struktur definiert wird (die Pro-Scheitelpunkt-Daten als Position, normal und Texturkoordinate definiert). Der erste Parameter verwendet auch das Schlüsselwort triangle. Das bedeutet, dass die Stufe des Eingabe-Assemblers Daten an den Geometrie-Shader als einen der primitiven Dreieckstypen (Dreiecksliste oder Dreiecksstreifen) ausgibt.</p>
<p>Der zweite Parameter ist ein Dreiecksstream, der durch den Typ TriangleStream &lt; &gt; GSPS_INPUTT. Dies bedeutet, dass der -Parameter ein Array von Dreiecken ist, von denen jedes aus drei Scheitelstellen besteht (die die Daten aus den Membern der GSPS_INPUT).</p>
<p>Verwenden Sie die Schlüsselwörter triangle und trianglestream, um einzelne Dreiecke oder einen Stream von Dreiecken in einem GS zu identifizieren.</p></td>
</tr>
<tr class="odd">
<td><p><span id="Intrinsic_function"></span><span id="intrinsic_function"></span><span id="INTRINSIC_FUNCTION"></span>Systeminterne Funktion</p></td>
<td><p>Die Codezeilen in der Shaderfunktion verwenden intrinsische HLSL-Funktionen mit allgemeinem Shaderkern, mit Ausnahme der letzten beiden Zeilen, die Append und RestartStrip aufrufen. Diese Funktionen sind nur für einen Geometrie-Shader verfügbar. Append informiert den Geometrie-Shader darüber, die Ausgabe an den aktuellen Strip anfügen. RestartStrip erstellt einen neuen primitiven Strip. Bei jedem Aufruf der GS-Phase wird implizit ein neuer Strip erstellt.</p></td>
</tr>
</tbody>
</table>



 

Der Rest des Shaders sieht einem Scheitelpunkt- oder Pixel-Shader sehr ähnlich. Der Geometrie-Shader verwendet eine -Struktur, um Eingabeparameter zu deklarieren, und markiert den Position member mit der SV POSITION-Semantik, um die Hardware darüber zu informieren, dass es sich um \_ Positionsdaten handelt. Die Eingabestruktur identifiziert die anderen beiden Eingabeparameter als Texturkoordinaten (obwohl einer davon eine Gesichtsnormnorm enthält). Wenn Sie möchten, können Sie ihre eigene benutzerdefinierte Semantik für die Gesichtsnorm verwenden.

Nachdem Sie den Geometrie-Shader entworfen haben, rufen [**Sie D3DCompile**](/windows/desktop/direct3dhlsl/d3dcompile) auf, um zu kompilieren, wie im folgenden Codebeispiel gezeigt.


```
DWORD dwShaderFlags = D3DCOMPILE_ENABLE_STRICTNESS;
ID3DBlob** ppShader;

D3DCompile( pSrcData, sizeof( pSrcData ), 
  "Tutorial13.fx", NULL, NULL, "GS", "gs_4_0", 
  dwShaderFlags, 0, &ppShader, NULL );
```



Genau wie Vertex- und Pixel-Shader benötigen Sie ein Shaderflag, um dem Compiler mitteilen zu können, wie der Shader kompiliert werden soll (für das Debuggen, für geschwindigkeitsoptimiert und so weiter), für die Einstiegspunktfunktion und für das Shadermodell, anhand derer überprüft werden soll. In diesem Beispiel wird mithilfe der GS-Funktion ein Geometrie-Shader erstellt, der aus der Datei Tutorial13.fx erstellt wurde. Der Shader wird für Shadermodell 4.0 kompiliert.

## <a name="create-a-geometry-shader-object-with-stream-output"></a>Erstellen eines Geometry-Shader Objekts mit Streamausgabe

Wenn Sie wissen, dass Sie die Daten aus der Geometrie streamen und den Shader erfolgreich kompiliert haben, besteht der nächste Schritt im Aufrufen von [**ID3D11Device::CreateGeometryShaderWithStreamOutput,**](/windows/desktop/api/D3D11/nf-d3d11-id3d11device-creategeometryshaderwithstreamoutput) um das Geometrieshaderobjekt zu erstellen.

Zunächst müssen Sie jedoch die Eingangssignatur der Phase "Output(SO)" deklarieren. Diese Signatur stimmt mit den GS-Ausgaben und den SO-Eingaben zum Zeitpunkt der Objekterstellung ab oder überprüft sie. Der folgende Code ist ein Beispiel für die SO-Deklaration.


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



Diese Funktion verwendet mehrere Parameter, darunter:

-   Ein Zeiger auf den kompilierten Geometrie-Shader (oder vertex shader, wenn kein Geometrie-Shader vorhanden ist und Daten direkt aus dem Vertex-Shader gestreamt werden). Informationen zum Abrufen dieses Zeigers finden Sie unter [Getting a Pointer to a Compiled Shader](/windows/desktop/direct3dhlsl/dx-graphics-hlsl-using-shaders-10).
-   Ein Zeiger auf ein Array von Deklarationen, die die Eingabedaten für die Streamausgabephase beschreiben. (Siehe [**D3D11 \_ SO DECLARATION \_ \_ ENTRY**](/windows/desktop/api/D3D11/ns-d3d11-d3d11_so_declaration_entry).) Sie können bis zu 64 Deklarationen, eine für jeden unterschiedlichen Elementtyp, der aus der SO-Phase ausgegeben werden soll, liefern. Das Array von Deklarationseinträgen beschreibt das Datenlayout, unabhängig davon, ob nur ein einzelner oder mehrere Puffer für die Streamausgabe gebunden werden sollen.
-   Die Anzahl der Elemente, die von der SO-Phase geschrieben werden.
-   Ein Zeiger auf das erstellte Geometrieshaderobjekt (siehe [**ID3D11GeometryShader**](/windows/win32/api/d3d11/nn-d3d11-id3d11geometryshader)).

In diesem Fall ist der Pufferschritt NULL, der Index des Streams, der an den Rasterizer gesendet werden soll, ist 0, und die Klassenverknüpfungsschnittstelle ist NULL.

Die Streamausgabedeklaration definiert, wie Daten in eine Pufferressource geschrieben werden. Sie können der Ausgabedeklaration so viele Komponenten hinzufügen, wie Sie möchten. Verwenden Sie die So-Phase, um in eine einzelne Pufferressource oder viele Pufferressourcen zu schreiben. Für einen einzelnen Puffer kann die SO-Phase viele verschiedene Elemente pro Scheitelpunkt schreiben. Bei mehreren Puffern kann die SO-Phase nur ein einzelnes Element von Pro-Scheitelpunkt-Daten in jeden Puffer schreiben.

Um die SO-Phase ohne einen Geometrieshader zu verwenden, rufen Sie [**ID3D11Device::CreateGeometryShaderWithStreamOutput**](/windows/desktop/api/D3D11/nf-d3d11-id3d11device-creategeometryshaderwithstreamoutput) auf, und übergeben Sie einen Zeiger auf einen Vertexshader an den *pShaderBytecode-Parameter.*

## <a name="set-the-output-targets"></a>Festlegen der Ausgabeziele

Der letzte Schritt besteht im Festlegen der So-Phasenpuffer. Daten können zur späteren Verwendung in einen oder mehrere Puffer im Arbeitsspeicher gestreamt werden. Der folgende Code zeigt, wie Sie einen einzelnen Puffer erstellen, der für Scheitelpunktdaten sowie für die SO-Phase zum Streamen von Daten verwendet werden kann.


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



Erstellen Sie einen Puffer, indem Sie [**ID3D11Device::CreateBuffer aufrufen.**](/windows/desktop/api/D3D11/nf-d3d11-id3d11device-createbuffer) In diesem Beispiel wird die Standardverwendung veranschaulicht. Dies ist typisch für eine Pufferressource, die voraussichtlich relativ häufig von der CPU aktualisiert wird. Das Bindungsflag identifiziert die Pipelinephase, an die die Ressource gebunden werden kann. Jede ressource, die von der SO-Phase verwendet wird, muss auch mit dem Bindungsflag D3D10 \_ BIND STREAM OUTPUT erstellt \_ \_ werden.

Nachdem der Puffer erfolgreich erstellt wurde, legen Sie ihn auf das aktuelle Gerät fest, indem Sie [**ID3D11DeviceContext::SOSetTargets aufrufen:**](/windows/desktop/api/D3D11/nf-d3d11-id3d11devicecontext-sosettargets)


```
UINT offset[1] = 0;
D3D11Device->SOSetTargets( 1, &m_pBuffer, offset );
```



Dieser Aufruf nimmt die Anzahl der Puffer, einen Zeiger auf die Puffer und ein Array von Offsets an (ein Offset in jeden der Puffer, der angibt, wo mit dem Schreiben von Daten begonnen werden soll). Daten werden in diese Streamingausgabepuffer geschrieben, wenn eine draw-Funktion aufgerufen wird. Eine interne Variable verfolgt die Position, an der mit dem Schreiben von Daten in die Streamingausgabepuffer begonnen werden soll, und diese Variablen werden weiter erhöht, bis [**SOSetTargets**](/windows/desktop/api/D3D11/nf-d3d11-id3d11devicecontext-sosettargets) erneut aufgerufen wird und ein neuer Offsetwert angegeben wird.

Alle Daten, die in die Zielpuffer geschrieben werden, sind 32-Bit-Werte.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Streamausgabephase](d3d10-graphics-programming-guide-output-stream-stage.md)
</dt> </dl>

 

