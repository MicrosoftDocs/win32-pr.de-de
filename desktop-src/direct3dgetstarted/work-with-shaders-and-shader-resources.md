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
# <a name="work-with-shaders-and-shader-resources"></a>Arbeiten mit Shader und Shaderressourcen

Es ist an der Zeit, sich mit Shader und Shaderressourcen bei der Entwicklung Ihres Microsoft DirectX-Spiels für Windows 8 zu informieren. Wir haben gesehen, wie das Grafikgerät und die Ressourcen eingerichtet werden, und vielleicht haben Sie sogar damit begonnen, seine Pipeline zu ändern. Sehen wir uns nun die Pixel-und Vertex-Shader an.

Wenn Sie mit Shader-Sprachen nicht vertraut sind, finden Sie in der richtigen Reihenfolge eine kurze Erörterung. Shader sind kleine, Low-Level-Programme, die in bestimmten Phasen der Grafik Pipeline kompiliert und ausgeführt werden. Ihre Spezialität sind sehr schnelle Gleit Komma Operationen mit Gleit Komma Zahlen. Die häufigsten Shader-Programme sind:

-   **Vertex-Shader**– wird für jeden Scheitelpunkt in einer Szene ausgeführt. Dieser Shader verarbeitet Vertex-Puffer Elemente, die von der aufrufenden App bereitgestellt werden, und führt minimal zu einem Positions Vektor mit vier Komponenten, der in eine Pixelposition gerengt wird.
-   **Pixel-Shader**– wird für jedes Pixel in einem Renderziel ausgeführt. Dieser Shader empfängt rasterisierte Koordinaten aus früheren shaderphasen (in den einfachsten Pipelines, dies wäre der Vertexshader) und gibt eine Farbe (oder einen anderen 4-komponentenwert) für die Pixelposition zurück, die dann in ein Renderziel geschrieben wird.

Dieses Beispiel enthält sehr einfache Scheitelpunkt-und Pixel-Shader, die nur Geometrie zeichnen, und komplexere Shader, die grundlegende Beleuchtungsberechnungen hinzufügen.

Shader-Programme sind in Microsoft High Level Shader Language (HLSL) geschrieben. Die HLSL-Syntax sieht ähnlich aus wie C, aber ohne die Zeiger. Shader-Programme müssen sehr kompakt und effizient sein. Wenn Ihr Shader zu viele Anweisungen kompiliert, kann er nicht ausgeführt werden, und es wird ein Fehler zurückgegeben. (Beachten Sie, dass die genaue Anzahl zulässiger Anweisungen Teil der [Direct3D-Funktionsebene](/windows/desktop/direct3d11/overviews-direct3d-11-devices-downlevel-intro)ist.)

In Direct3D werden Shader zur Laufzeit nicht kompiliert. Sie werden kompiliert, wenn der Rest des Programms kompiliert wird. Wenn Sie die APP mit Microsoft Visual Studio 2013 kompilieren, werden die HLSL-Dateien in CSO-Dateien (. CSO) kompiliert, die ihre App laden und vor dem Zeichnen in den GPU-Speicher platzieren muss. Stellen Sie sicher, dass Sie diese CSO-Dateien bei der Paket Erstellung in Ihre APP einschließen. Dabei handelt es sich um Ressourcen wie Netzen und Texturen.

## <a name="understand-hlsl-semantics"></a>Grundlegendes zur HLSL-Semantik

Es ist wichtig, dass Sie sich einen Moment Zeit nehmen, um die HLSL-Semantik zu erörtern, bevor Sie fortfahren, denn Sie sind häufig eine Verwechslung für neue Direct3D-Entwickler. HLSL-Semantik sind Zeichen folgen, die einen Wert angeben, der zwischen der APP und einem Shader-Programm übermittelt wird. Obwohl es sich um eine beliebige Vielzahl möglicher Zeichen folgen handeln kann, empfiehlt es sich, eine Zeichenfolge wie `POSITION` oder zu verwenden `COLOR` , die die Verwendung angibt. Diese Semantik weisen Sie zu, wenn Sie einen konstanten Puffer oder ein Eingabe Layout erstellen. Sie können auch eine Zahl zwischen 0 und 7 an die Semantik anfügen, wenn Sie separate Register für ähnliche Werte verwenden möchten. Beispiel: COLOR0, COLOR1, COLOR2...

Bei der Semantik mit dem Präfix "SV \_ " handelt es sich um eine *System Wert* Semantik, die von Ihrem Shader-Programm geschrieben wird. Ihr Spiel selbst (auf der CPU ausgeführt) kann Sie nicht ändern. In der Regel enthalten diese Semantik Werte, bei denen es sich um Eingaben oder Ausgaben aus einer anderen Shader-Stufe in der Grafik Pipeline handelt oder die vollständig von der GPU generiert werden.

Außerdem `SV_` hat die Semantik ein anderes Verhalten, wenn Sie verwendet werden, um Eingaben für eine Shader-Stufe anzugeben oder diese auszugeben. `SV_POSITION`(Output) enthält z. b. die Vertexdaten, die während der Vertex-Shader-Stufe transformiert werden, und `SV_POSITION` (*Input*) enthält die Pixel Positionswerte, die während der rasterisierungsphase von der GPU interpoliert wurden.

Im folgenden finden Sie einige allgemeine HLSL-Semantik:

-   `POSITION`(*n*) für Vertex-Puffer Daten. `SV_POSITION` stellt eine Pixelposition für den Pixelshader bereit und kann nicht von Ihrem Spiel geschrieben werden.
-   `NORMAL`(*n*) für normale Daten, die vom Vertex-Puffer bereitgestellt werden.
-   `TEXCOORD`(*n*) für Textur-UV-Koordinatendaten, die an einen Shader übergeben werden.
-   `COLOR`(n) für RGBA-Farbdaten, die an einen Shader übergeben werden. Beachten Sie, dass Sie identisch mit der Koordinierung von Daten behandelt wird, einschließlich der Interpolation des Werts während der rasterisierung. mithilfe der Semantik können Sie einfach erkennen, dass es sich um Farbdaten handelt.
-   `SV_Target`\[n \] zum Schreiben von einem Pixelshader in eine Ziel Textur oder einen anderen Pixel Puffer.

Einige Beispiele für die HLSL-Semantik finden Sie im Beispiel.

## <a name="read-from-the-constant-buffers"></a>Aus konstantenpuffern lesen

Jeder Shader kann aus einem konstanten Puffer lesen, wenn dieser Puffer an seine Stufe als Ressource angefügt wird. In diesem Beispiel wird nur dem Vertex-Shader ein konstanter Puffer zugewiesen.

Der Konstante Puffer wird an zwei Stellen deklariert: im C++-Code und in den entsprechenden HLSL-Dateien, die darauf zugreifen.

Im folgenden wird erläutert, wie die Konstante Puffer Struktur im C++-Code deklariert wird.


```C++
typedef struct _constantBufferStruct {
    DirectX::XMFLOAT4X4 world;
    DirectX::XMFLOAT4X4 view;
    DirectX::XMFLOAT4X4 projection;
} ConstantBufferStruct;
```



Wenn Sie die Struktur für den Konstantenpuffer in Ihrem C++-Code deklarieren, stellen Sie sicher, dass alle Daten ordnungsgemäß an 16-Byte-Grenzen ausgerichtet sind. Die einfachste Möglichkeit hierfür ist die Verwendung von [directxmath](/windows/desktop/dxmath/directxmath-portal) -Typen, wie z. b. **XMFLOAT4** oder **XMFLOAT4X4**, wie im Beispielcode gezeigt. Sie können auch Schutz vor falsch ausgerichteten Puffern haben, indem Sie eine statische Assert deklarieren:


```C++
// Assert that the constant buffer remains 16-byte aligned.
static_assert((sizeof(ConstantBufferStruct) % 16) == 0, "Constant Buffer size must be 16-byte aligned");
```



Diese Codezeile führt zum Zeitpunkt der Kompilierung zu einem Fehler, wenn **constantbufferstruct** nicht mit 16 Byte ausgerichtet ist. Weitere Informationen zur konstanten Puffer Ausrichtung und-Verpackung finden Sie unter [Packen von Regeln für konstante Variablen](/windows/desktop/direct3dhlsl/dx-graphics-hlsl-packing-rules).

Hier sehen Sie, wie der Konstante Puffer im Vertex-Shader HLSL deklariert wird.


```C++
cbuffer ModelViewProjectionConstantBuffer : register(b0)
{
    matrix mWorld;      // world matrix for object
    matrix View;        // view matrix
    matrix Projection;  // projection matrix
};
```



Alle Puffer – für Konstante, Textur, Sampler oder andere – muss ein Register definiert sein, damit die GPU darauf zugreifen kann. Jede Shader-Stufe ermöglicht bis zu 15 Konstante Puffer, und jeder Puffer kann bis zu 4.096 Konstante Variablen enthalten. Die Syntax der Register Verwendungs Deklaration lautet wie folgt:

-   **b * * *\#* : ein Register für einen konstanten Puffer (** cBuffer * *).
-   **t * * *\#* : ein Register für einen Textur Puffer (** tBuffer * *).
-   **s * * \#**: ein Register für einen Sampler. (Ein Sampler definiert das Suchverhalten für texeln in der Textur Ressource.)

Beispielsweise kann das HLSL für einen PixelShader eine Textur und einen Sampler als Eingabe mit einer Deklaration wie diesem annehmen.

``` syntax
Texture2D simpleTexture : register(t0);
SamplerState simpleSampler : register(s0);
```

Es liegt an Ihnen, den Registern Konstante Puffer zuzuweisen – beim Einrichten der Pipeline fügen Sie einen konstanten Puffer an denselben Slot an, den Sie in der HLSL-Datei zugewiesen haben. Im vorherigen Thema zeigt der [**vssetconstantbuffers**](/windows/desktop/api/d3d11/nf-d3d11-id3d11devicecontext-vssetconstantbuffers) -Aufrufe z. b. für den ersten Parameter "0" an. Dies weist Direct3D an, die Konstante Puffer Ressource an Register 0 anzufügen, was der Zuordnung des Puffers zur **Registrierung (B0)** in der HLSL-Datei entspricht.

## <a name="read-from-the-vertex-buffers"></a>Lesen aus den Scheitel Punkten

Der Vertex-Puffer stellt den Vertexshader die Dreiecks Daten für die Szene Objekte zur Verfügung. Wie beim Konstanten Puffer wird die Vertex-Puffer Struktur im C++-Code mit ähnlichen Verpackungs Regeln deklariert.


```C++
typedef struct _vertexPositionColor
{
    DirectX::XMFLOAT3 pos;
    DirectX::XMFLOAT3 color;
} VertexPositionColor;
```



Es gibt kein Standardformat für Scheitelpunkt Daten in Direct3D 11. Stattdessen definieren wir unser eigenes Vertex-Datenlayout mithilfe eines Deskriptors. die Datenfelder werden mithilfe eines Arrays aus [**D3D11- \_ Eingabe \_ Element \_**](/windows/desktop/api/d3d11/ns-d3d11-d3d11_input_element_desc) -Erstellungs Strukturen definiert. Hier sehen Sie ein einfaches Eingabe Layout, das das gleiche Scheitelpunkt Format wie die vorherige Struktur beschreibt:


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



Wenn Sie beim Ändern des Beispielcodes dem Vertex-Format Daten hinzufügen, achten Sie darauf, dass Sie auch das Eingabe Layout aktualisieren, oder der Shader kann es nicht interpretieren. Sie können das Scheitelpunkt Layout wie folgt ändern:


```C++
typedef struct _vertexPositionColorTangent
{
    DirectX::XMFLOAT3 pos;
    DirectX::XMFLOAT3 normal;
    DirectX::XMFLOAT3 tangent;
} VertexPositionColorTangent;
```



In diesem Fall würden Sie die Eingabe Layout-Definition wie folgt ändern.


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



Jeder Eingabe Layout-Element Definition wird eine Zeichenfolge vorangestellt, wie z. b. "Position" oder "Normal" – Dies ist die Semantik, die wir zuvor in diesem Thema besprochen haben. Es ähnelt einem Handle, das der GPU bei der Verarbeitung des Scheitel Punkts dabei hilft, dieses Element zu identifizieren. Wählen Sie allgemeine, aussagekräftige Namen für die Vertex-Elemente aus.

Ebenso wie beim Konstanten Puffer verfügt der Vertex-Shader über eine entsprechende Puffer Definition für eingehende Vertex-Elemente. (Aus diesem Grund haben wir beim Erstellen des Eingabe Layouts einen Verweis auf die Vertex-Shader-Ressource bereitgestellt Direct3D die Überprüfung des pro-Vertex-Daten Layouts mit der Eingabe Struktur des Shader.) Beachten Sie, dass die Semantik zwischen der Eingabe Layout-Definition und dieser HLSL-Puffer Deklaration entspricht. Es wird jedoch `COLOR` ein "0" angefügt. Es ist nicht erforderlich, den Wert 0 hinzuzufügen, wenn Sie nur ein `COLOR` Element im Layout deklariert haben. es wird jedoch empfohlen, es anzufügen, falls Sie in Zukunft weitere Farbelemente hinzufügen.


```C++
struct VS_INPUT
{
    float3 vPos   : POSITION;
    float3 vColor : COLOR0;
};
```



## <a name="pass-data-between-shaders"></a>Übergeben von Daten zwischen Shadern

Shader nehmen bei der Ausführung Eingabetypen an und geben Ausgabetypen von ihren Hauptfunktionen zurück. Für den Vertex-Shader, der im vorherigen Abschnitt definiert wurde, war der Eingabetyp die vs \_ -Eingabe Struktur, und wir haben ein entsprechendes Eingabe Layout und eine C++-Struktur definiert. Ein Array dieser Struktur wird verwendet, um einen Vertex-Puffer in der Methode " **kreatecube** " zu erstellen.

Der Vertex-Shader gibt eine PS \_ -Eingabe Struktur zurück, die die endgültige Scheitelpunkt Position von 4 Komponenten (float4) minimal enthalten muss. Für diesen Positionswert muss der System Wert Semantic, `SV_POSITION` , deklariert werden, damit die GPU über die Daten verfügt, die Sie zum Ausführen des nächsten Zeichnungs Schritts benötigt. Beachten Sie, dass es keine 1:1-Entsprechung zwischen der Vertex-Shader-Ausgabe und der Pixel-Shadereingabe gibt. der Vertex-Shader gibt eine Struktur für jeden angegebenen Scheitelpunkt zurück, der Pixelshader wird jedoch für jedes Pixel einmal ausgeführt. Das liegt daran, dass die pro-Vertex-Daten zuerst die rasterisierungsphase passieren. Diese Stufe bestimmt, welche Pixel die Geometrie "abdecken", die Sie zeichnen, berechnet interpoliert pro-Vertex-Daten für jedes Pixel und ruft dann den Pixelshader für jede dieser Pixel einmal auf. Die Interpolation ist das Standardverhalten beim rasterieren von Ausgabe Werten. Sie ist insbesondere für die korrekte Verarbeitung von Ausgabe Vektordaten (helle Vektoren, pro-Vertex-Normale und-Tangents usw.) entscheidend.


```C++
struct PS_INPUT
{
    float4 Position : SV_POSITION;  // interpolated vertex position (system value)
    float4 Color    : COLOR0;       // interpolated diffuse color
};
```



## <a name="review-the-vertex-shader"></a>Überprüfen Sie den Vertexshader.

Der Vertex-Beispiel Shader ist sehr einfach: nehmen Sie einen Scheitelpunkt (Position und Farbe), transformieren Sie die Position von Modell Koordinaten in Perspektiven projizierte Koordinaten, und geben Sie diese (zusammen mit der Farbe) an den Rasterizer zurück. Beachten Sie, dass der Farbwert direkt zusammen mit den Positionsdaten interpoliert wird, wobei für jedes Pixel ein anderer Wert bereitgestellt wird, auch wenn der Vertexshader keine Berechnungen für den Farbwert durchgeführt hat.


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



Ein komplexerer Vertexshader, wie z. b. ein Objekt, das die Scheitel Punkte eines Objekts für die Phong-Schattierung festlegt, könnte wie folgt aussehen. In diesem Fall nutzen wir die Tatsache, dass die Vektoren und normale interpoliert werden, um eine nahtlose Oberfläche zu finden.

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

## <a name="review-the-pixel-shader"></a>Überprüfen Sie den Pixelshader.

Dieser Pixelshader in diesem Beispiel ist möglicherweise die absolute Mindestmenge an Code, den Sie in einem Pixelshader haben können. Dabei werden die während der rasterisierung generierten interinterpolierten Pixel Farbdaten verwendet und als Ausgabe zurückgegeben, wo Sie in ein Renderziel geschrieben werden. Wie langweilig!


```C++
PS_OUTPUT main(PS_INPUT In)
{
    PS_OUTPUT Output;

    Output.RGBColor = In.Color;

    return Output;
}
```



Der wichtige Teil ist die `SV_TARGET` System-Wert-Semantik für den Rückgabewert. Gibt an, dass die Ausgabe in das primäre Renderziel geschrieben werden soll. Dies ist der Textur Puffer, der für die Anzeige Kette bereitgestellt wird. Dies ist für Pixel-Shader erforderlich. ohne die Farbdaten aus dem Pixelshader wäre Direct3D nicht zum Anzeigen vorhanden.

Ein Beispiel für einen komplexeren Pixelshader, um die Phong-Schattierung auszuführen, könnte wie folgt aussehen. Da die Vektoren und normale interpoliert wurden, müssen wir Sie nicht pro Pixel berechnen. Wir müssen Sie jedoch aufgrund der Funktionsweise der Interpolationen erneut normalisieren. konzeptionell müssen wir den Vektor schrittweise von der Richtung in Scheitelpunkt a in Richtung in Vertex B "drehen", wobei seine Länge beibehalten wird. – wheras Interpolation wird stattdessen über eine gerade Linie zwischen den beiden Vektor Endpunkten gekürzt.

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

In einem anderen Beispiel nimmt der Pixelshader seine eigenen Konstanten Puffer an, die helle und Material Informationen enthalten. Das Eingabe Layout im Vertexshader würde so erweitert werden, dass es normale Daten enthält, und die Ausgabe dieses Vertexshaders soll die transformierten Vektoren für den Scheitelpunkt, das Licht und den Scheitelpunkt im Ansichts Koordinatensystem einschließen.

Wenn Sie Textur Puffer und Samplern mit zugewiesenen Registern (**t** bzw. **s**) haben, können Sie auch im Pixelshader darauf zugreifen.

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

Shader sind sehr leistungsfähige Tools, die verwendet werden können, um prozedurale Ressourcen wie Schatten Zuordnungen oder Rausch Texturen zu generieren. In der Tat erfordern erweiterte Techniken, dass Sie Texturen abstrakter betrachten, nicht als visuelle Elemente, sondern als Puffer. Sie enthalten Daten wie z. b. Höheninformationen oder andere Daten, die im letzten Pixel-Shader-Durchlauf oder in diesem bestimmten Frame als Teil einer mehrstufigen Auswirkung durchlaufen werden können. Multisampling ist ein leistungsfähiges Tool und das Backbone aus vielen modernen visuellen Effekten.

## <a name="next-steps"></a>Nächste Schritte

Ich hoffe, dass Sie an diesem Punkt mit DirectX 11vertraut sind und bereit sind, mit der Arbeit an Ihrem Projekt zu beginnen. Hier finden Sie einige Links, die Ihnen helfen, andere Fragen zu beantworten, die Sie möglicherweise zur Entwicklung mit DirectX und C++ haben:

-   [Entwickeln von Spielen](/previous-versions/windows/apps/hh452744(v=win.10))
-   [Verwenden von Visual Studio-Tools für die DirectX-Spielprogrammierung](/previous-versions/windows/apps/dn166877(v=win.10))
-   [DirectX-Spieleentwicklung und Exemplarische Vorgehensweisen für Beispiele](/previous-versions/windows/apps/hh465149(v=win.10))
-   [Zusätzliche Programmier Ressourcen für Spiele](/previous-versions/windows/apps/dn194515(v=win.10))

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Arbeiten mit DirectX-Geräte Ressourcen](work-with-dxgi.md)
</dt> <dt>

[Grundlegendes zur Direct3D 11-Renderingpipeline](understand-the-directx-11-2-graphics-pipeline.md)
</dt> </dl>

 

 