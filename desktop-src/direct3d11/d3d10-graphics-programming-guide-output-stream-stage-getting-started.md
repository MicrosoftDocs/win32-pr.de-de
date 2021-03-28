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
# <a name="getting-started-with-the-stream-output-stage"></a>Ersten Einstieg in die Stream-Output Phase

In diesem Abschnitt wird beschrieben, wie ein Geometry-Shader mit der Stream-Ausgabestufe verwendet wird.

## <a name="compile-a-geometry-shader"></a>Kompilieren eines Geometry-Shaders

Dieser Geometry-Shader (GS) berechnet eine Vorderseite für jedes Dreieck und gibt Positions-, normal-und Texturkoordinaten Daten aus.


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



Beachten Sie dabei, dass ein Geometry-Shader ähnlich wie ein Scheitelpunkt oder Pixel-Shader aussieht, aber mit den folgenden Ausnahmen: der von der Funktion zurückgegebene Typ, die Eingabeparameter Deklarationen und die intrinsische Funktion.



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th>Element</th>
<th>BESCHREIBUNG</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span id="Function_return_type"></span><span id="function_return_type"></span><span id="FUNCTION_RETURN_TYPE"></span>Funktions Rückgabetyp<br/></td>
<td>Der Funktions Rückgabetyp bewirkt, dass die maximale Anzahl der Scheitel Punkte deklariert, die vom Shader ausgegeben werden können. In diesem Fall <span data-codelanguage=""></span>
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

definiert die Ausgabe als maximal 12 Vertices.</td>
</tr>
<tr class="even">
<td><p><span id="Input_parameter_declarations"></span><span id="input_parameter_declarations"></span><span id="INPUT_PARAMETER_DECLARATIONS"></span>Eingabeparameter Deklarationen</p></td>
<td><p>Diese Funktion nimmt zwei Eingabeparameter an:</p>
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
<p>Der erste Parameter ist ein Array von Vertices (in diesem Fall 3), das durch eine GSPS_INPUT Struktur definiert wird (die pro-Vertex-Daten als eine Position, eine normale und eine Textur Koordinate definiert). Der erste Parameter verwendet auch das Dreiecks Schlüsselwort. Dies bedeutet, dass die Eingabe Assembler-Stufe Daten an den Geometry-Shader als einen der Grundtypen des Dreiecks (Dreiecks Liste oder Dreieck) ausgeben muss.</p>
<p>Der zweite Parameter ist ein vom Typ trianglestream definierter Dreiecks Datenstrom <GSPS_INPUT> . Dies bedeutet, dass es sich bei dem Parameter um ein Array von Dreiecken handelt, von denen jede aus drei Vertices besteht (die die Daten aus den Membern von GSPS_INPUT enthalten).</p>
<p>Verwenden Sie die Schlüsselwörter Dreieck und trianglestream, um einzelne Dreiecke oder einen Datenstrom von Dreiecken in einer GS zu identifizieren.</p></td>
</tr>
<tr class="odd">
<td><p><span id="Intrinsic_function"></span><span id="intrinsic_function"></span><span id="INTRINSIC_FUNCTION"></span>Intrinsische Funktion</p></td>
<td><p>In den Codezeilen in der Shader-Funktion werden intrinsische HLSL-Funktionen von Common-Shader-Core verwendet, mit Ausnahme der letzten beiden Zeilen, die "append" und "restartstrip" aufrufen. Diese Funktionen sind nur für einen Geometry-Shader verfügbar. Anfügen informiert den Geometry-Shader darüber, dass die Ausgabe an den aktuellen Strip angefügt werden soll. Restartstrip erstellt einen neuen primitiven Strip. Ein neuer Strip wird bei jedem Aufruf der GS-Phase implizit erstellt.</p></td>
</tr>
</tbody>
</table>



 

Der Rest des Shader ähnelt einem Scheitelpunkt oder einem Pixelshader. Der Geometry-Shader verwendet eine-Struktur, um Eingabeparameter zu deklarieren, und markiert das Positions Element mit der SV- \_ Positions Semantik, um der Hardware mitzuteilen, dass es sich um Positionsdaten handelt. Die Eingabe Struktur identifiziert die anderen beiden Eingabeparameter als Texturkoordinaten (auch wenn einer von Ihnen ein Gesicht normal enthält). Wenn Sie möchten, können Sie Ihre eigene benutzerdefinierte Semantik für die Vorderseite verwenden.

Nachdem Sie den Geometry-Shader entworfen haben, müssen Sie [**D3DCompile**](/windows/desktop/direct3dhlsl/d3dcompile) zum Kompilieren aufrufen, wie im folgenden Codebeispiel gezeigt.


```
DWORD dwShaderFlags = D3DCOMPILE_ENABLE_STRICTNESS;
ID3DBlob** ppShader;

D3DCompile( pSrcData, sizeof( pSrcData ), 
  "Tutorial13.fx", NULL, NULL, "GS", "gs_4_0", 
  dwShaderFlags, 0, &ppShader, NULL );
```



Genau wie Scheitelpunkt-und Pixel-Shader benötigen Sie ein Shader-Flag, um dem Compiler mitzuteilen, wie der Shader kompiliert werden soll (für das Debuggen, optimiert für Geschwindigkeit usw.), die Einstiegspunkt Funktion und das Shader-Modell, anhand dessen validiert werden soll. In diesem Beispiel wird ein Geometry-Shader erstellt, der aus der Datei Tutorial13. FX erstellt wurde, indem die GS-Funktion verwendet wird. Der Shader wird für das Shader-Modell 4,0 kompiliert.

## <a name="create-a-geometry-shader-object-with-stream-output"></a>Erstellen eines Geometry-Shader Objekts mit Datenstrom Ausgabe

Wenn Sie wissen, dass Sie die Daten aus der Geometrie streamen, und Sie den Shader erfolgreich kompiliert haben, besteht der nächste Schritt im Aufrufen von [**ID3D11Device:: kreategeometryshaderwithstreamoutput**](/windows/desktop/api/D3D11/nf-d3d11-id3d11device-creategeometryshaderwithstreamoutput) zum Erstellen des Geometry-Shader-Objekts.

Zuerst müssen Sie jedoch die Eingabe Signatur der Ausgabe der Ausgabe (also) deklarieren. Diese Signatur gleicht die GS-Ausgaben und die so-Eingaben zum Zeitpunkt der Objekt Erstellung ab oder überprüft sie. Der folgende Code ist ein Beispiel für die so-Deklaration.


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



Diese Funktion erfordert mehrere Parameter, einschließlich:

-   Ein Zeiger auf den kompilierten Geometry-Shader (oder Vertex-Shader, wenn kein Geometry-Shader vorhanden ist und die Daten direkt aus dem Vertexshader gestreamt werden). Weitere Informationen zum Aufrufen dieses Zeigers finden Sie unter "aufrufen [eines Zeigers auf einen kompilierten Shader](/windows/desktop/direct3dhlsl/dx-graphics-hlsl-using-shaders-10)".
-   Ein Zeiger auf ein Array von Deklarationen, die die Eingabedaten für die Stream-Ausgabe Phase beschreiben. (Siehe [**D3D11 \_ so- \_ Deklarations \_ Eintrag**](/windows/desktop/api/D3D11/ns-d3d11-d3d11_so_declaration_entry).) Sie können bis zu 64 Deklarationen angeben, eine für jeden Elementtyp, der aus der so-Phase ausgegeben werden soll. Das Array der Deklarations Einträge beschreibt das Datenlayout, unabhängig davon, ob nur ein einzelner Puffer oder mehrere Puffer an die Streamausgabe gebunden werden sollen.
-   Die Anzahl der Elemente, die von der so-Phase ausgeschrieben werden.
-   Ein Zeiger auf das Geometry-Shader-Objekt, das erstellt wird (siehe [**ID3D11GeometryShader**](/windows/win32/api/d3d11/nn-d3d11-id3d11geometryshader)).

In dieser Situation ist der Puffer Stride NULL. der Index des Datenstroms, der an den Raster gesendet werden soll, ist 0, und die Klassen Verknüpfungs Schnittstelle ist NULL.

Die Datenstrom-Ausgabe Deklaration definiert, wie Daten in eine Puffer Ressource geschrieben werden. Sie können der Ausgabe Deklaration beliebig viele Komponenten hinzufügen. Verwenden Sie die so-Phase, um in eine einzelne Puffer Ressource oder viele Puffer Ressourcen zu schreiben. Bei einem einzelnen Puffer kann die so-Phase viele verschiedene Elemente pro Scheitelpunkt schreiben. Für mehrere Puffer kann die so-Phase nur ein einzelnes Element von pro-Vertex-Daten in jeden Puffer schreiben.

Um die so-Phase ohne Verwendung eines Geometry-Shaders zu verwenden, müssen Sie [**ID3D11Device:: deategeometryshaderwithstreamoutput**](/windows/desktop/api/D3D11/nf-d3d11-id3d11device-creategeometryshaderwithstreamoutput) aufrufen und einen Zeiger auf einen Vertex-Shader an den *pshaderbytecode* -Parameter übergeben.

## <a name="set-the-output-targets"></a>Festlegen der Ausgabe Ziele

Der letzte Schritt besteht darin, die so-Phasen Puffer festzulegen. Daten können zur späteren Verwendung in einen oder mehrere Puffer im Arbeitsspeicher gestreamt werden. Der folgende Code zeigt, wie ein einzelner Puffer erstellt wird, der für Scheitelpunkt Daten verwendet werden kann, sowie für die so-Phase, um Daten in zu streamen.


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



Erstellen Sie einen Puffer durch Aufrufen von [**ID3D11Device:: createbuffer**](/windows/desktop/api/D3D11/nf-d3d11-id3d11device-createbuffer). Dieses Beispiel veranschaulicht die Standardverwendung, die typisch für eine Puffer Ressource ist, die relativ häufig von der CPU aktualisiert werden soll. Das Bindungsflag identifiziert die Pipeline Stufe, an die die Ressource gebunden werden kann. Alle Ressourcen, die von der so-Phase verwendet werden, müssen auch mit dem Bindungsflag d3d10 \_ Bind \_ Stream Output erstellt werden \_ .

Nachdem der Puffer erfolgreich erstellt wurde, legen Sie ihn auf das aktuelle Gerät durch Aufrufen von [**Verknüpfung id3d11devicecontext aus:: sosettargets**](/windows/desktop/api/D3D11/nf-d3d11-id3d11devicecontext-sosettargets)fest:


```
UINT offset[1] = 0;
D3D11Device->SOSetTargets( 1, &m_pBuffer, offset );
```



Dieser Befehl nimmt die Anzahl von Puffern, einen Zeiger auf die Puffer und ein Array von Offsets (ein Offset in jeden Puffer, der angibt, wohin mit dem Schreiben von Daten begonnen werden soll). Daten werden in diese streamingausgabepuffer geschrieben, wenn eine Draw-Funktion aufgerufen wird. Eine interne Variable verfolgt die Position, an der mit dem Schreiben von Daten in die streamingausgabepuffer begonnen werden soll, und gibt an, dass die Variablen weiterhin erhöht werden, bis [**sosettargets**](/windows/desktop/api/D3D11/nf-d3d11-id3d11devicecontext-sosettargets) erneut aufgerufen wird und ein neuer Offset Wert angegeben wird.

Alle Daten, die in die Ziel Puffer geschrieben werden, sind 32-Bit-Werte.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Stream-Ausgabe Phase](d3d10-graphics-programming-guide-output-stream-stage.md)
</dt> </dl>

 

