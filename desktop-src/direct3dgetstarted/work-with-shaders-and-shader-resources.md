---
title: Arbeiten mit Shadern und Shaderressourcen
description: Es ist an der Zeit zu erfahren, wie Sie mit Shadern und Shaderressourcen arbeiten, um Ihr Microsoft DirectX-Spiel für Windows 8 zu entwickeln.
ms.assetid: 25a11983-e3f6-4bd3-86f1-d660edc4cd4b
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bbf0152ba74dcc8dd1c602b69d854634502c928a0deefe5521bcab8999954049
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118288550"
---
# <a name="work-with-shaders-and-shader-resources"></a>Arbeiten mit Shadern und Shaderressourcen

Es ist an der Zeit zu erfahren, wie Sie mit Shadern und Shaderressourcen arbeiten, um Ihr Microsoft DirectX-Spiel für Windows 8 zu entwickeln. Wir haben erfahren, wie Sie das Grafikgerät und die Ressourcen einrichten, und vielleicht haben Sie sogar damit begonnen, die Pipeline zu ändern. Sehen wir uns nun pixel- und vertex-Shader an.

Wenn Sie nicht mit Shadersprachen vertraut sind, ist eine kurze Erläuterung in der gewünschten Reihenfolge. Shader sind kleine Programme auf niedriger Ebene, die in bestimmten Phasen in der Grafikpipeline kompiliert und ausgeführt werden. Ihre Spezielle sind sehr schnelle mathematische Gleitkommaoperationen. Die gängigsten Shaderprogramme sind:

-   **Vertex-Shader**: Wird für jeden Scheitelpunkt in einer Szene ausgeführt. Dieser Shader arbeitet mit Vertexpufferelementen, die ihm von der aufrufenden App bereitgestellt werden, und führt minimal zu einem Positionsvektor mit vier Komponenten, der in eine Pixelposition gerastet wird.
-   **Pixel-Shader**: Wird für jedes Pixel in einem Renderziel ausgeführt. Dieser Shader empfängt gerasterte Koordinaten aus vorherigen Shaderstufen (in den einfachsten Pipelines wäre dies der Scheitelpunkt-Shader) und gibt eine Farbe (oder einen anderen 4-Komponenten-Wert) für diese Pixelposition zurück, die dann in ein Renderziel geschrieben wird.

Dieses Beispiel enthält sehr einfache Vertex- und Pixel-Shader, die nur Geometrie zeichnen, sowie komplexere Shader, die grundlegende Beleuchtungsberechnungen hinzufügen.

Shaderprogramme sind in Der Microsoft High Level Shader Language (HLSL) geschrieben. Die HLSL-Syntax sieht ähnlich wie C aus, jedoch ohne die Zeiger. Shaderprogramme müssen sehr kompakt und effizient sein. Wenn Ihr Shader zu viele Anweisungen kompiliert, kann er nicht ausgeführt werden, und es wird ein Fehler zurückgegeben. (Beachten Sie, dass die genaue Zulässige Anzahl von Anweisungen Teil der [Direct3D-Featureebene](/windows/desktop/direct3d11/overviews-direct3d-11-devices-downlevel-intro)ist.)

In Direct3D werden Shader nicht zur Laufzeit kompiliert. Sie werden kompiliert, wenn der Rest des Programms kompiliert wird. Wenn Sie Ihre App mit Microsoft Visual Studio 2013 kompilieren, werden die HLSL-Dateien in CSO-Dateien (.cso) kompiliert, die Ihre App vor dem Zeichnen laden und im GPU-Speicher platzieren muss. Stellen Sie sicher, dass Sie diese CSO-Dateien in Ihre App einschließen, wenn Sie sie packen. sie sind Ressourcen wie Gitternetze und Texturen.

## <a name="understand-hlsl-semantics"></a>Grundlegendes zur HLSL-Semantik

Es ist wichtig, dass Sie sich einen Moment Zeit nehmen, um die HLSL-Semantik zu besprechen, bevor wir fortfahren, da sie für neue Direct3D-Entwickler oft verwirrend sind. HLSL-Semantik sind Zeichenfolgen, die einen Wert identifizieren, der zwischen der App und einem Shaderprogramm übergeben wird. Obwohl es sich um eine Vielzahl von möglichen Zeichenfolgen handeln kann, empfiehlt es sich, eine Zeichenfolge wie oder zu `POSITION` `COLOR` verwenden, die die Verwendung angibt. Sie weisen diese Semantik zu, wenn Sie einen konstanten Puffer oder ein Eingabelayout erstellen. Sie können auch eine Zahl zwischen 0 und 7 an die Semantik anfügen, wenn Sie separate Register für ähnliche Werte verwenden möchten. Beispiel: COLOR0, COLOR1, COLOR2...

Semantik mit dem Präfix \_ "SV" sind *Systemwertsemantik,* die von Ihrem Shaderprogramm in geschrieben werden. Ihr Spiel selbst (das auf der CPU ausgeführt wird) kann sie nicht ändern. In der Regel enthalten diese Semantik Werte, die Ein- oder Ausgaben aus einer anderen Shaderphase in der Grafikpipeline sind oder vollständig von der GPU generiert werden.

Darüber hinaus `SV_` weisen Semantik unterschiedliche Verhaltensweisen auf, wenn sie verwendet werden, um Eingaben in oder Ausgaben aus einer Shaderphase anzugeben. (Ausgabe) enthält beispielsweise `SV_POSITION` die Vertexdaten, die während der Vertex-Shaderphase transformiert wurden, und `SV_POSITION` (*eingabe*) enthält die Pixelpositionswerte, die von der GPU während der Rasterungsphase interpoliert wurden.

Hier sind einige allgemeine HLSL-Semantik:

-   `POSITION`(*n*) für Scheitelpunktpufferdaten. `SV_POSITION` stellt eine Pixelposition für den Pixelshader bereit und kann nicht von Ihrem Spiel geschrieben werden.
-   `NORMAL`(*n*) für normale Daten, die vom Scheitelpunktpuffer bereitgestellt werden.
-   `TEXCOORD`(*n*) für Textur-UV-Koordinatendaten, die für einen Shader bereitgestellt werden.
-   `COLOR`(n) für RGBA-Farbdaten, die für einen Shader bereitgestellt werden. Beachten Sie, dass sie identisch behandelt wird, um Daten zu koordinieren, einschließlich der Interpolation des Werts während der Rasterung. mithilfe der Semantik können Sie einfach erkennen, dass es sich um Farbdaten handelt.
-   `SV_Target`\[n \] zum Schreiben aus einem Pixel-Shader in eine Zieltextur oder einen anderen Pixelpuffer.

Wir sehen uns einige Beispiele für die HLSL-Semantik an, während wir das Beispiel betrachten.

## <a name="read-from-the-constant-buffers"></a>Lesen aus den Konstantenpuffern

Jeder Shader kann aus einem konstanten Puffer lesen, wenn dieser Puffer an seine Phase als Ressource angefügt ist. In diesem Beispiel wird nur dem Vertex-Shader ein konstanter Puffer zugewiesen.

Der Konstantenpuffer wird an zwei Stellen deklariert: im C++-Code und in den entsprechenden HLSL-Dateien, die darauf zugreifen.

So wird die konstante Pufferstruktur im C++-Code deklariert.


```C++
typedef struct _constantBufferStruct {
    DirectX::XMFLOAT4X4 world;
    DirectX::XMFLOAT4X4 view;
    DirectX::XMFLOAT4X4 projection;
} ConstantBufferStruct;
```



Stellen Sie beim Deklarieren der Struktur für den Konstantenpuffer in Ihrem C++-Code sicher, dass alle Daten ordnungsgemäß an 16-Byte-Grenzen ausgerichtet sind. Die einfachste Möglichkeit hierfür ist die Verwendung von [DirectXMath-Typen](/windows/desktop/dxmath/directxmath-portal) wie **XMFLOAT4** oder **XMFLOAT4X4,** wie im Beispielcode zu sehen. Sie können sich auch vor falsch ausgerichteten Puffern schützen, indem Sie eine statische Assertion deklarieren:


```C++
// Assert that the constant buffer remains 16-byte aligned.
static_assert((sizeof(ConstantBufferStruct) % 16) == 0, "Constant Buffer size must be 16-byte aligned");
```



Diese Codezeile verursacht zur Kompilierzeit einen Fehler, wenn **ConstantBufferStruct** nicht auf 16 Byte ausgerichtet ist. Weitere Informationen zur konstanten Pufferausrichtung und zum Packen finden Sie unter [Komprimierungsregeln für konstante Variablen.](/windows/desktop/direct3dhlsl/dx-graphics-hlsl-packing-rules)

Nun wird der Konstantenpuffer im Scheitelpunkt-Shader HLSL deklariert.


```C++
cbuffer ModelViewProjectionConstantBuffer : register(b0)
{
    matrix mWorld;      // world matrix for object
    matrix View;        // view matrix
    matrix Projection;  // projection matrix
};
```



Für alle Puffer – Konstante, Textur, Sampler oder andere – muss ein Register definiert sein, damit die GPU darauf zugreifen kann. Jede Shaderphase lässt bis zu 15 konstante Puffer zu, und jeder Puffer kann bis zu 4.096 konstante Variablen enthalten. Die Syntax der Registerverwendungsdeklaration lautet wie folgt:

-   **b** _\#_ : Ein Register für einen konstanten Puffer (**cbuffer**).
-   **t** _\#_ : Ein Register für einen Texturpuffer (**tbuffer**).
-   **s:** _\#_ Ein Register für einen Sampler. (Ein Sampler definiert das Suchverhalten für Texel in der Texturressource.)

Beispielsweise kann die HLSL für einen Pixel-Shader eine Textur und einen Sampler als Eingabe mit einer Deklaration wie dieser annehmen.

``` syntax
Texture2D simpleTexture : register(t0);
SamplerState simpleSampler : register(s0);
```

Es liegt an Ihnen, Konstantenpuffer zu Registern zuzuweisen. Wenn Sie die Pipeline einrichten, fügen Sie einen Konstantenpuffer an denselben Slot an, dem Sie ihn in der HLSL-Datei zugewiesen haben. Im vorherigen Thema gibt der Aufruf von [**VSSetConstantBuffers**](/windows/desktop/api/d3d11/nf-d3d11-id3d11devicecontext-vssetconstantbuffers) beispielsweise "0" für den ersten Parameter an. Dies weist Direct3D an, die konstante Pufferressource zum Registrieren von 0 anzufügen, was der Zuweisung des Puffers zu **register(b0)** in der HLSL-Datei entspricht.

## <a name="read-from-the-vertex-buffers"></a>Lesen aus den Scheitelpunktpuffern

Der Scheitelpunktpuffer stellt die Dreiecksdaten für die Szenenobjekte für die Vertex-Shader bereit. Wie beim konstanten Puffer wird die Vertexpufferstruktur im C++-Code mit ähnlichen Komprimierungsregeln deklariert.


```C++
typedef struct _vertexPositionColor
{
    DirectX::XMFLOAT3 pos;
    DirectX::XMFLOAT3 color;
} VertexPositionColor;
```



Es gibt kein Standardformat für Scheitelpunktdaten in Direct3D 11. Stattdessen definieren wir unser eigenes Vertexdatenlayout mithilfe eines Deskriptors. Die Datenfelder werden mithilfe eines Arrays von [**D3D11 \_ INPUT \_ ELEMENT \_ DESC-Strukturen**](/windows/desktop/api/d3d11/ns-d3d11-d3d11_input_element_desc) definiert. Hier zeigen wir ein einfaches Eingabelayout, das das gleiche Scheitelpunktformat wie die vorherige Struktur beschreibt:


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



Wenn Sie beim Ändern des Beispielcodes Daten zum Scheitelpunktformat hinzufügen, achten Sie darauf, auch das Eingabelayout zu aktualisieren, da der Shader es nicht interpretieren kann. Sie können das Scheitelpunktlayout wie folgt ändern:


```C++
typedef struct _vertexPositionColorTangent
{
    DirectX::XMFLOAT3 pos;
    DirectX::XMFLOAT3 normal;
    DirectX::XMFLOAT3 tangent;
} VertexPositionColorTangent;
```



In diesem Fall würden Sie die Definition des Eingabelayouts wie folgt ändern.


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



Jeder der Eingabelayoutelementdefinitionen wird eine Zeichenfolge vorangestellt, z. B. "POSITION" oder "NORMAL". Dies ist die Semantik, die wir weiter oben in diesem Thema erläutert haben. Dies ist wie ein Handle, mit dem die GPU dieses Element bei der Verarbeitung des Scheitelpunkts identifizieren kann. Wählen Sie allgemeine, aussagekräftige Namen für Ihre Scheitelpunktelemente aus.

Wie beim konstanten Puffer verfügt der Vertex-Shader über eine entsprechende Pufferdefinition für eingehende Scheitelpunktelemente. (Aus diesem Grund haben wir beim Erstellen des Eingabelayouts einen Verweis auf die Vertex-Shaderressource bereitgestellt: Direct3D überprüft das Datenlayout pro Scheitelpunkt mit der Eingabestruktur des Shaders.) Beachten Sie, wie die Semantik zwischen der Eingabelayoutdefinition und dieser HLSL-Pufferdeklaration übereinstimmt. Es wird jedoch `COLOR` ein "0" angefügt. Es ist nicht erforderlich, 0 hinzuzufügen, wenn Sie nur ein Element im Layout deklariert haben. Es ist `COLOR` jedoch eine bewährte Methode, es anzufügen, falls Sie in Zukunft weitere Farbelemente hinzufügen möchten.


```C++
struct VS_INPUT
{
    float3 vPos   : POSITION;
    float3 vColor : COLOR0;
};
```



## <a name="pass-data-between-shaders"></a>Übergeben von Daten zwischen Shadern

Shader nehmen Eingabetypen und geben ausgabetypen von ihren Hauptfunktionen bei der Ausführung zurück. Für den im vorherigen Abschnitt definierten Vertex-Shader war der Eingabetyp die VS \_ INPUT-Struktur, und wir haben ein übereinstimmendes Eingabelayout und eine C++-Struktur definiert. Ein Array dieser Struktur wird verwendet, um einen Scheitelpunktpuffer in der **CreateCube-Methode** zu erstellen.

Der Vertex-Shader gibt eine PS \_ INPUT-Struktur zurück, die minimal die letzte Scheitelpunktposition mit 4 Komponenten (float4) enthalten muss. Für diesen Positionswert muss die Systemwertsemantik ( ) deklariert sein, damit die GPU über die Daten verfügt, `SV_POSITION` die sie zum Ausführen des nächsten Zeichnungsschritts benötigt. Beachten Sie, dass es keine 1:1-Entsprechung zwischen der Vertex-Shaderausgabe und der Pixel-Shadereingabe gibt. Der Vertex-Shader gibt eine Struktur für jeden angegebenen Scheitelpunkt zurück, aber der Pixelshader wird einmal für jedes Pixel ausgeführt. Das liegt daran, dass die Pro-Scheitelpunkt-Daten zuerst die Rasterungsphase durchlaufen. Diese Phase entscheidet, welche Pixel die zu zeichnende Geometrie "abdecken", berechnet interpolierte Daten pro Scheitelpunkt für jedes Pixel und ruft dann den Pixelshader einmal für jedes dieser Pixel auf. Interpolation ist das Standardverhalten beim Rastern von Ausgabewerten und insbesondere für die korrekte Verarbeitung von Ausgabevektordaten (Lichtvektoren, Pro-Scheitelpunkt-Normalwerte und Tangenten usw.) von entscheidender Bedeutung.


```C++
struct PS_INPUT
{
    float4 Position : SV_POSITION;  // interpolated vertex position (system value)
    float4 Color    : COLOR0;       // interpolated diffuse color
};
```



## <a name="review-the-vertex-shader"></a>Überprüfen des Vertex-Shaders

Der Vertex-Shader ist sehr einfach: Nehmen Sie einen Scheitelpunkt (Position und Farbe) ein, transformieren Sie die Position von Modellkoordinaten in projizierte Perspektivenkoordinaten, und geben Sie sie (zusammen mit der Farbe) an den Rasterizer zurück. Beachten Sie, dass der Farbwert zusammen mit den Positionsdaten interpoliert wird und für jedes Pixel einen anderen Wert bereitstellt, obwohl der Vertex-Shader keine Berechnungen für den Farbwert durchgeführt hat.


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



Ein komplexerer Vertex-Shader, z. B. ein Shader, der die Scheitelpunkte eines Objekts für die Phong-Schattierung einrichten soll, könnte in etwa wie folgt aussehen. In diesem Fall nutzen wir die Tatsache, dass die Vektoren und Normalwerte interpoliert werden, um eine gleichmäßig aussehende Oberfläche anzunähern.

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

## <a name="review-the-pixel-shader"></a>Überprüfen des Pixelshader

Dieser Pixel-Shader in diesem Beispiel ist möglicherweise die absolute Mindestmenge an Code, die Sie in einem Pixel-Shader haben können. Sie übernimmt die interpolierten Pixelfarbdaten, die während der Rasterung generiert werden, und gibt sie als Ausgabe zurück, wo sie in ein Renderziel geschrieben werden. Wie fad!


```C++
PS_OUTPUT main(PS_INPUT In)
{
    PS_OUTPUT Output;

    Output.RGBColor = In.Color;

    return Output;
}
```



Der wichtige Teil ist die `SV_TARGET` Systemwertsemantik für den Rückgabewert. Sie gibt an, dass die Ausgabe in das primäre Renderziel geschrieben werden soll. Dabei handelt es sich um den Texturpuffer, der der Swapkette zur Anzeige bereitgestellt wird. Dies ist für Pixel-Shader erforderlich– ohne die Farbdaten aus dem Pixel-Shader müsste Direct3D nichts anzeigen!

Ein Beispiel für einen komplexeren Pixelshader zum Ausführen der Phong-Schattierung könnte wie folgt aussehen. Da die Vektoren und Normalitäten interpoliert wurden, müssen wir sie nicht pro Pixel berechnen. Sie müssen jedoch aufgrund der Funktionsweise der Interpolation erneut normalisiert werden. Konzeptionell müssen wir den Vektor nach und nach von Der Richtung an Scheitelpunkt A in Richtung bei Scheitelpunkt B "drehen" und dabei seine Länge beibehalten. Die Wheras-Interpolation schneidet stattdessen über eine gerade Linie zwischen den beiden Vektorendpunkten.

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

In einem anderen Beispiel nimmt der Pixel-Shader seine eigenen konstanten Puffer an, die Licht- und Materialinformationen enthalten. Das Eingabelayout im Vertex-Shader wird erweitert, um normale Daten einzuschließen, und es wird erwartet, dass die Ausgabe dieses Vertex-Shaders transformierte Vektoren für den Scheitelpunkt, das Licht und die Scheitelpunktnorm im Ansichtkoordinatensystem enthält.

Wenn Sie über Texturpuffer und Sampler mit zugewiesenen Registern **(t** bzw. **s)** verfügen, können Sie auch im Pixelshader darauf zugreifen.

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

Shader sind sehr leistungsstarke Tools, die verwendet werden können, um prozedurale Ressourcen wie Schattenkarten oder Rauschtexturen zu generieren. In der Tat erfordern erweiterte Techniken, dass Sie Texturen abstrakter betrachten, nicht als visuelle Elemente, sondern als Puffer. Sie enthalten Daten wie Höheninformationen oder andere Daten, die im letzten Pixel-Shaderdurchlauf oder in diesem bestimmten Frame als Teil eines mehrstufigen Effektdurchlaufs entnommen werden können. Multi-Sampling ist ein leistungsstarkes Tool und das Backbone vieler moderner visueller Effekte.

## <a name="next-steps"></a>Nächste Schritte

Wir hoffen, dass Sie an diesem Punkt mit DirectX 11 vertraut sind und bereit sind, mit der Arbeit an Ihrem Projekt zu beginnen. Hier finden Sie einige Links, mit denen Sie andere Fragen zur Entwicklung mit DirectX und C++ beantworten können:

-   [Entwickeln von Spielen](/previous-versions/windows/apps/hh452744(v=win.10))
-   [Verwenden Visual Studio Tools für die DirectX-Spieleprogrammierung](/previous-versions/windows/apps/dn166877(v=win.10))
-   [Exemplarische Vorgehensweisen zur Entwicklung von DirectX-Spielen und Beispielen](/previous-versions/windows/apps/hh465149(v=win.10))
-   [Zusätzliche Ressourcen für die Spieleprogrammierung](/previous-versions/windows/apps/dn194515(v=win.10))

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Arbeiten mit DirectX-Geräteressourcen](work-with-dxgi.md)
</dt> <dt>

[Grundlegendes zur Direct3D 11-Renderingpipeline](understand-the-directx-11-2-graphics-pipeline.md)
</dt> </dl>

 

 