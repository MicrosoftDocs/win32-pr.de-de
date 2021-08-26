---
title: Schreiben von HLSL-Shadern in Direct3D 9
description: Schreiben von HLSL-Shadern in Direct3D 9
ms.assetid: 7db6b264-c96c-4298-9b8a-d0c488390e4e
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 67e6fec265682dcdbe8ffa967ba757382eda2e17d55aff8b8a1ae168a96df3c2
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119950110"
---
# <a name="writing-hlsl-shaders-in-direct3d-9"></a>Schreiben von HLSL-Shadern in Direct3D 9

-   [Grundlagen zu Vertex-Shader](#vertex-shader-basics)
-   [Grundlagen zu Pixel-Shader](#pixel-shader-basics)
    -   [Texturstufe und Samplerzustände](#texture-stage-and-sampler-states)
    -   [Pixel-Shadereingaben](#pixel-shader-inputs)
    -   [Pixel-Shader-Ausgaben](#pixel-shader-outputs)
-   [Shadereingaben und Shadervariablen](#shader-inputs-and-shader-variables)
    -   [Deklarieren von Shadervariablen](#declaring-shader-variables)
    -   [Uniform Shader Inputs](#uniform-shader-inputs)
    -   [Variierende Shadereingaben und Semantik](#varying-shader-inputs-and-semantics)
    -   [Sampler und Texturobjekte](#samplers-and-texture-objects)
-   [Schreiben von Funktionen](#writing-functions)
-   [Flow Steuerung](#flow-control)
-   [Zugehörige Themen](#related-topics)

## <a name="vertex-shader-basics"></a>Vertex-Shader Grundlagen

Im Betrieb ersetzt ein programmierbarer Vertex-Shader die Scheitelpunktverarbeitung, die von der Microsoft Direct3D-Grafikpipeline durchgeführt wird. Bei verwendung eines Vertex-Shaders werden Zustandsinformationen zu Transformations- und Beleuchtungsvorgängen von der festen Funktionspipeline ignoriert. Wenn der Vertex-Shader deaktiviert ist und die Verarbeitung fester Funktionen zurückgegeben wird, gelten alle aktuellen Zustandseinstellungen.

Das Mosaik von hohen Primitiven sollte vor der Ausführung des Vertex-Shaders erfolgen. Implementierungen, die Oberflächentessellation nach der Shaderverarbeitung ausführen, müssen dies auf eine Weise tun, die für die Anwendung und den Shadercode nicht offensichtlich ist.

Ein Vertex-Shader muss mindestens die Scheitelpunktposition im homogenen Clipraum aus geben. Optional kann der Vertex-Shader Texturkoordinaten, Scheitelpunktfarbe, Scheitelpunktbeleuchtung, Lichtfaktoren und so weiter aus geben.

## <a name="pixel-shader-basics"></a>Pixel-Shader Grundlagen

Die Pixelverarbeitung wird von Pixel-Shadern auf einzelnen Pixeln ausgeführt. Pixel-Shader arbeiten zusammen mit Vertex-Shadern. Die Ausgabe eines Vertex-Shaders stellt die Eingaben für einen Pixel-Shader zur Verwendung. Andere Pixeloperationen (Blending, Schablonenoperationen und Renderzielblending) erfolgen nach der Ausführung des Shaders.

### <a name="texture-stage-and-sampler-states"></a>Texturstufe und Samplerzustände

Ein Pixel-Shader ersetzt die vom Multitexturblender angegebene Pixelblendingfunktion vollständig, einschließlich vorgängen, die zuvor durch die Texturstufenzustände definiert wurden. Textursstichproben- und Filtervorgänge, die von den Standardtexturstufenzuständen für Minierung, Vergrößerung, MIP-Filterung und die Wrap-Adressierungsmodi gesteuert wurden, können in Shadern initialisiert werden. Die Anwendung kann diese Zustände ändern, ohne dass die Neuverstellung des derzeit gebundenen Shaders erforderlich ist. Das Festlegen des Zustands kann noch einfacher werden, wenn Ihre Shader innerhalb eines Effekts entworfen wurden.

### <a name="pixel-shader-inputs"></a>Pixel-Shadereingaben

Für die Pixel-Shaderversionen ps \_ 1 1 - ps 2 0 werden diffuse und specular-Farben im Bereich von 0 bis 1 überschniffen (klammert), bevor sie vom \_ \_ \_ Shader verwendet werden.

Für die Eingabe von Farbwerten für den Pixel-Shader wird angenommen, dass sie perspektivisch korrekt sind, aber dies ist (für alle Hardware) nicht garantiert. Farben, die aus Texturkoordinaten entnommen werden, werden perspektivisch korrekt durchgeitert und während der Iteration an den Bereich 0 bis 1 geklammert.

### <a name="pixel-shader-outputs"></a>Pixel-Shader-Ausgaben

Für die Pixel-Shaderversionen ps 1 1 - ps 1 4 ist das vom Pixel-Shader ausgegebene Ergebnis der Inhalt \_ \_ des \_ \_ Registers r0. Alles, was sie enthält, wenn der Shader die Verarbeitung abgeschlossen hat, wird an die Phase und den Renderzielblender gesendet.

Bei Pixel-Shaderversionen ps 2 0 und höher wird die Ausgabefarbe von \_ \_ oC0 - oC4 ausgegeben.

## <a name="shader-inputs-and-shader-variables"></a>Shadereingaben und Shadervariablen

-   [Deklarieren von Shadervariablen](#declaring-shader-variables)
-   [Uniform Shader Inputs](#uniform-shader-inputs)
-   [Variierende Shadereingaben und Semantik](#varying-shader-inputs-and-semantics)
-   [Sampler und Texturobjekte](#samplers-and-texture-objects)

### <a name="declaring-shader-variables"></a>Deklarieren von Shadervariablen

Die einfachste Variablendeklaration enthält einen Typ und einen Variablennamen, z. B. diese Gleitkommadeklaration:


```
float fVar;
```



Sie können eine Variable in derselben Anweisung initialisieren.


```
float fVar = 3.1f;
```



Ein Array von Variablen kann deklariert werden.


```
int iVar[3];
```



oder deklariert und in derselben Anweisung initialisiert.


```
int iVar[3] = {1,2,3};
```



Im Folgenden finden Sie einige Deklarationen, die viele der Merkmale von HLSL-Variablen (High-Level Shader Language) veranschaulichen:


```
float4 color;
uniform float4 position : POSITION; 
const float4 lightDirection = {0,0,1};
```



Datendeklarationen können jeden gültigen Typ verwenden, einschließlich:

-   [Datentypen (DirectX HLSL)](dx-graphics-hlsl-data-types.md)
-   [Vektortyp (DirectX HLSL)](dx-graphics-hlsl-vector.md)
-   [Matrixtyp (DirectX HLSL)](dx-graphics-hlsl-matrix.md)
-   [Shadertyp (DirectX HLSL)](dx-graphics-hlsl-shader.md)
-   [Samplertyp (DirectX HLSL)](dx-graphics-hlsl-sampler.md)
-   [Benutzerdefinierter Typ (DirectX HLSL)](dx-graphics-hlsl-user-defined.md)

Ein Shader kann Variablen, Argumente und Funktionen der obersten Ebene haben.


```
// top-level variable
float globalShaderVariable; 

// top-level function
void function(
in float4 position: POSITION0 // top-level argument
              )
{
  float localShaderVariable; // local variable
  function2(...)
}

void function2()
{
  ...
}
```



Variablen der obersten Ebene werden außerhalb aller Funktionen deklariert. Argumente der obersten Ebene sind Parameter für eine Funktion der obersten Ebene. Eine Funktion der obersten Ebene ist eine beliebige Funktion, die von der Anwendung aufgerufen wird (im Gegensatz zu einer Funktion, die von einer anderen Funktion aufgerufen wird).

### <a name="uniform-shader-inputs"></a>Uniform Shader Inputs

Vertex- und Pixel-Shader akzeptieren zwei Arten von Eingabedaten: variierend und einheitlich. Die variierende Eingabe sind die Daten, die für jede Ausführung des Shaders eindeutig sind. Bei einem Vertex-Shader stammen die unterschiedlichen Daten (z.B. Position, Normal usw.) aus den Scheitelpunktstreams. Die einheitlichen Daten (z. B. Materialfarbe, Welttransformation usw.) sind für mehrere Ausführungen eines Shaders konstant. Für Diejenigen, die mit den Shadermodellen der Assembly vertraut sind, werden einheitliche Daten durch konstante Register und unterschiedliche Daten durch die Register v und t angegeben.

Einheitliche Daten können mit zwei Methoden angegeben werden. Die gängigste Methode ist das Deklarieren globaler Variablen und deren Verwendung innerhalb eines Shaders. Jede Verwendung globaler Variablen innerhalb eines Shaders führt dazu, dass diese Variable der Liste der für diesen Shader erforderlichen einheitlichen Variablen hinzugefügt wird. Die zweite Methode besteht im Markieren eines Eingabeparameters der Shaderfunktion der obersten Ebene als einheitlich. Diese Kennzeichnung gibt an, dass die gegebene Variable der Liste der einheitlichen Variablen hinzugefügt werden soll.

Einheitliche Variablen, die von einem Shader verwendet werden, werden über die konstante Tabelle an die Anwendung zurück übermittelt. Die Konstantentabelle ist der Name der Symboltabelle, die definiert, wie die von einem Shader verwendeten einheitlichen Variablen in die Konstantenregister passen. Im Gegensatz zu den globalen Variablen werden die Parameter der einheitlichen Funktion in der Konstantentabelle mit einem Dollarzeichen ($) angezeigt. Das Dollarzeichen ist erforderlich, um Namenskollisionen zwischen lokalen einheitlichen Eingaben und globalen Variablen mit demselben Namen zu vermeiden.

Die Konstantentabelle enthält die konstanten Registerpositionen aller vom Shader verwendeten einheitlichen Variablen. Die Tabelle enthält auch die Typinformationen und den Standardwert, sofern angegeben.

### <a name="varying-shader-inputs-and-semantics"></a>Variierende Shadereingaben und Semantik

Unterschiedliche Eingabeparameter (einer Shaderfunktion der obersten Ebene) müssen entweder mit einem semantischen oder uniform-Schlüsselwort gekennzeichnet werden, das angibt, dass der Wert für die Ausführung des Shaders konstant ist. Wenn eine Shadereingabe der obersten Ebene nicht mit einem semantischen oder einheitlichen Schlüsselwort markiert ist, kann der Shader nicht kompiliert werden.

Die Eingabesemantik ist ein Name, der verwendet wird, um die gegebene Eingabe mit einer Ausgabe des vorherigen Teils der Grafikpipeline zu verknüpfen. Beispielsweise wird die eingabesemantische POSITION0 von den Vertex-Shadern verwendet, um anzugeben, wo die Positionsdaten aus dem Scheitelpunktpuffer verknüpft werden sollen.

Pixels- und Vertex-Shader verfügen aufgrund der verschiedenen Teile der Grafikpipeline, die in die einzelnen Shadereinheiten einfingen, über unterschiedliche Sätze von Eingabesemantik. Die Vertex-Shader-Eingabesemantik beschreibt die Pro-Scheitelpunkt-Informationen (z.B. Position, Normal, Texturkoordinaten, Farbe, Tangens, Binormal usw.), die aus einem Scheitelpunktpuffer in ein Formular geladen werden sollen, das vom Vertex-Shader genutzt werden kann. Die Eingabesemantik ist direkt der Verwendung der Scheitelpunktdeklaration und dem Verwendungsindex zu zuordnen.

Die Pixel-Shader-Eingabesemantik beschreibt die Informationen, die von der Rasterungseinheit pro Pixel bereitgestellt werden. Die Daten werden generiert, indem zwischen ausgaben des Vertex-Shaders für jeden Scheitelpunkt des aktuellen Primitiven interpoliert wird. Die grundlegende Pixel-Shader-Eingabesemantik verknüpfen die Ausgabefarbe und Texturkoordinateninformationen mit Eingabeparametern.

Die Eingabesemantik kann der Shadereingabe mit zwei Methoden zugewiesen werden:

-   Anfügen eines Doppelpunkts und des semantischen Namens an die Parameterdeklaration.
-   Definieren einer Eingabestruktur mit Eingabesemantik, die jedem Strukturmitglied zugewiesen ist.

Vertex- und Pixel-Shader stellen Ausgabedaten für die nachfolgende Grafikpipelinephase zur Verfügung. Ausgabesemantik wird verwendet, um anzugeben, wie vom Shader generierte Daten mit den Eingaben der nächsten Phase verknüpft werden sollen. Beispielsweise wird die Ausgabesemantik für einen Vertex-Shader verwendet, um die Ausgaben der Interpolatoren im Rasterizer zu verknüpfen, um die Eingabedaten für den Pixel-Shader zu generieren. Bei den Pixel-Shader-Ausgaben handelt es sich um die Werte, die der Alphablendingeinheit für jedes der Renderziele bereitgestellt werden, oder um den Tiefenwert, der in den Tiefenpuffer geschrieben wird.

Die Vertex-Shader-Ausgabesemantik wird verwendet, um den Shader sowohl mit dem Pixel-Shader als auch mit der Rasterizer-Stufe zu verknüpfen. Ein Vertex-Shader, der vom Rasterizer verwendet und nicht für den Pixel-Shader verfügbar gemacht wird, muss mindestens Positionsdaten generieren. Vertex-Shader, die Texturkoordinaten- und Farbdaten generieren, stellen diese Daten nach Abschluss der Interpolation an einen Pixel-Shader bereit.

Die Pixel-Shader-Ausgabesemantik bindet die Ausgabefarben eines Pixel-Shaders an das richtige Renderziel. Die Ausgabefarbe des Pixelshaders ist mit der Alphablendphase verknüpft, die bestimmt, wie die Zielrenderziele geändert werden. Die Pixel-Shader-Tiefenausgabe kann verwendet werden, um die Zieltiefewerte an der aktuellen Rasterposition zu ändern. Die Tiefenausgabe und mehrere Renderziele werden nur bei einigen Shadermodellen unterstützt.

Die Syntax für die Ausgabesemantik ist identisch mit der Syntax zum Angeben der Eingabesemantik. Die Semantik kann entweder direkt für Parameter angegeben werden, die als "out"-Parameter deklariert sind, oder während der Definition einer Struktur zugewiesen werden, die entweder als "out"-Parameter oder als Rückgabewert einer Funktion zurückgegeben wird.

Semantik identifiziert, woher Daten stammen. Semantik sind optionale Bezeichner, die Shadereingaben und -ausgaben identifizieren. Semantik wird an einer von drei Stellen angezeigt:

-   Nach einem Strukturmember.
-   Nach einem Argument in der Eingabeargumentliste einer Funktion.
-   Nach der Eingabeargumentliste der Funktion.

In diesem Beispiel wird eine -Struktur verwendet, um eine oder mehrere Vertex-Shadereingaben bereitzustellen, und eine andere -Struktur, um eine oder mehrere Vertex-Shaderausgaben bereitzustellen. Jeder der Strukturmember verwendet eine Semantik.


```
vector vClr;

struct VS_INPUT
{
    float4 vPosition : POSITION;
    float3 vNormal : NORMAL;
    float4 vBlendWeights : BLENDWEIGHT;
};

struct VS_OUTPUT
{
    float4  vPosition : POSITION;
    float4  vDiffuse : COLOR;

};

float4x4 mWld1;
float4x4 mWld2;
float4x4 mWld3;
float4x4 mWld4;

float Len;
float4 vLight;

float4x4 mTot;

VS_OUTPUT VS_Skinning_Example(const VS_INPUT v, uniform float len=100)
{
    VS_OUTPUT out;

    // Skin position (to world space)
    float3 vPosition = 
        mul(v.vPosition, (float4x3) mWld1) * v.vBlendWeights.x +
        mul(v.vPosition, (float4x3) mWld2) * v.vBlendWeights.y +
        mul(v.vPosition, (float4x3) mWld3) * v.vBlendWeights.z +
        mul(v.vPosition, (float4x3) mWld4) * v.vBlendWeights.w;
    // Skin normal (to world space)
    float3 vNormal =
        mul(v.vNormal, (float3x3) mWld1) * v.vBlendWeights.x + 
        mul(v.vNormal, (float3x3) mWld2) * v.vBlendWeights.y + 
        mul(v.vNormal, (float3x3) mWld3) * v.vBlendWeights.z + 
        mul(v.vNormal, (float3x3) mWld4) * v.vBlendWeights.w;
    
    // Output stuff
    out.vPosition    = mul(float4(vPosition + vNormal * Len, 1), mTot);
    out.vDiffuse  = dot(vLight,vNormal);

    return out;
}
```



Die Eingabestruktur identifiziert die Daten aus dem Scheitelpunktpuffer, der die Shadereingaben bereitstellt. Dieser Shader ordnet die Daten aus den Elementen position, normal und blendweight des Vertexpuffers in Vertex-Shaderregister zu. Der Eingabedatentyp muss nicht genau mit dem Datentyp der Scheitelpunktdeklaration übereinstimmen. Wenn sie nicht genau übereinstimmen, werden die Scheitelpunktdaten automatisch in den HLSL-Datentyp konvertiert, wenn sie in die Shaderregister geschrieben werden. Wenn die normalen Daten beispielsweise von der Anwendung als UINT-Typ definiert wurden, werden sie beim Lesen durch den Shader in float3 konvertiert.

Wenn die Daten im Scheitelpunktstream weniger Komponenten als der entsprechende Shaderdatentyp enthalten, werden die fehlenden Komponenten mit 0 initialisiert (mit Ausnahme von w, das mit 1 initialisiert wird).

Die Eingabesemantik ähnelt den Werten in [**D3DDECLUSAGE**](/windows/desktop/direct3d9/d3ddeclusage).

Die Ausgabestruktur identifiziert die Vertex-Shader-Ausgabeparameter von Position und Farbe. Diese Ausgaben werden von der Pipeline für die Dreiecksrasterung (bei der primitiven Verarbeitung) verwendet. Die als Positionsdaten markierte Ausgabe gibt die Position eines Scheitelpunkts im homogenen Raum an. Ein Scheitelpunkt-Shader muss mindestens Positionsdaten generieren. Die Bildschirmraumposition wird berechnet, nachdem der Vertex-Shader abgeschlossen ist, indem die Koordinate (x, y, z) durch w dividiert wird. Im Bildschirmbereich sind -1 und 1 die minimalen und maximalen x- und y-Werte der Grenzen des Viewports, während z für Z-Puffertests verwendet wird.

Die Ausgabesemantik ähnelt auch den Werten in [**D3DDECLUSAGE.**](/windows/desktop/direct3d9/d3ddeclusage) Im Allgemeinen kann eine Ausgabestruktur für einen Vertex-Shader auch als Eingabestruktur für einen Pixel-Shader verwendet werden, vorausgesetzt, der Pixel-Shader liest keine Variablen, die mit der Position, Punktgröße oder Semantik der Semantik des Gleitkommawerts gekennzeichnet sind. Diese Semantik wird Skalarwerten pro Scheitelpunkt zugeordnet, die nicht von einem Pixel-Shader verwendet werden. Wenn diese Werte für den Pixelshader benötigt werden, können sie in eine andere Ausgabevariable kopiert werden, die eine Pixelshadersemantik verwendet.

Globale Variablen werden registers automatisch vom Compiler zugewiesen. Globale Variablen werden auch als einheitliche Parameter bezeichnet, da der Inhalt der Variablen für alle Pixel identisch ist, die jedes Mal verarbeitet werden, wenn der Shader aufgerufen wird. Die Register sind in der konstanten Tabelle enthalten, die mithilfe der [**ID3DXConstantTable-Schnittstelle**](/windows/desktop/direct3d9/id3dxconstanttable) gelesen werden kann.

Die Eingabesemantik für Pixel-Shader ordnen Werte bestimmten Hardwareregistern für den Transport zwischen Vertex-Shadern und Pixel-Shadern zu. Jeder Registertyp verfügt über bestimmte Eigenschaften. Da derzeit nur zwei Semantiken für Farb- und Texturkoordinaten vorhanden sind, ist es üblich, dass die meisten Daten auch dann als Texturkoordinate markiert werden, wenn sie dies nicht ist.

Beachten Sie, dass die Vertex-Shader-Ausgabestruktur eine Eingabe mit Positionsdaten verwendet hat, die nicht vom Pixelshader verwendet wird. HLSL ermöglicht gültige Ausgabedaten eines Vertex-Shaders, die keine gültigen Eingabedaten für einen Pixel-Shader sind, vorausgesetzt, dass im Pixelshader nicht darauf verwiesen wird.

Eingabeargumente können auch Arrays sein. Semantik wird automatisch vom Compiler für jedes Element des Arrays erhöht. Betrachten Sie beispielsweise die folgende explizite Deklaration:


```
struct VS_OUTPUT
{
    float4 Position   : POSITION;
    float3 Diffuse    : COLOR0;
    float3 Specular   : COLOR1;               
    float3 HalfVector : TEXCOORD3;
    float3 Fresnel    : TEXCOORD2;               
    float3 Reflection : TEXCOORD0;               
    float3 NoiseCoord : TEXCOORD1;               
};

float4 Sparkle(VS_OUTPUT In) : COLOR
```



Die oben angegebene explizite Deklaration entspricht der folgenden Deklaration, bei der die Semantik automatisch vom Compiler erhöht wird:


```
float4 Sparkle(float4 Position : POSITION,
                 float3 Col[2] : COLOR0,
                 float3 Tex[4] : TEXCOORD0) : COLOR0
{
   // shader statements
   ...
```



Genau wie die Eingabesemantik identifiziert die Ausgabesemantik die Datenverwendung für Pixel-Shader-Ausgabedaten. Viele Pixelshader schreiben nur in eine Ausgabefarbe. Pixel-Shader können auch einen Tiefenwert gleichzeitig in ein oder mehrere Renderziele schreiben (bis zu vier). Wie Vertex-Shader verwenden Pixel-Shader eine -Struktur, um mehr als eine Ausgabe zurückzugeben. Dieser Shader schreibt 0 in die Farbkomponenten sowie in die Tiefenkomponente.


```
struct PS_OUTPUT
{
    float4 Color[4] : COLOR0;
    float  Depth  : DEPTH;
};

PS_OUTPUT main(void)
{
    PS_OUTPUT out;

   // Shader statements
   ...

  // Write up to four pixel shader output colors
  out.Color[0] =  ...
  out.Color[1] =  ...
  out.Color[2] =  ...
  out.Color[3] =  ...

  // Write pixel depth 
  out.Depth =  ...

    return out;
}
```



Die Pixel-Shader-Ausgabefarben müssen vom Typ float4 sein. Beim Schreiben mehrerer Farben müssen alle Ausgabefarben zusammenhängend verwendet werden. Anders ausgedrückt: [COLOR1](dx-graphics-hlsl-semantics.md) kann nur dann eine Ausgabe sein, wenn [COLOR0](dx-graphics-hlsl-semantics.md) bereits geschrieben wurde. Die Pixel-Shader-Tiefenausgabe muss vom Typ float1 sein.

### <a name="samplers-and-texture-objects"></a>Sampler und Texturobjekte

Ein Sampler enthält den Samplerzustand. Der Samplerzustand gibt die Textur an, die entnommen werden soll, und steuert die Filterung, die während der Stichprobenentnahme durchgeführt wird. Zum Sampling einer Textur sind drei Dinge erforderlich:

-   Eine Textur
-   Ein Sampler (mit Samplerzustand)
-   Eine Samplinganweisung

Sampler können mit Texturen und dem Samplerzustand initialisiert werden, wie hier gezeigt:


```
sampler s = sampler_state 
{ 
  texture = NULL; 
  mipfilter = LINEAR; 
};
```



Hier ist ein Beispiel für den Code zum Beispiel einer 2D-Textur:


```
texture tex0;
sampler2D s_2D;

float2 sample_2D(float2 tex : TEXCOORD0) : COLOR
{
  return tex2D(s_2D, tex);
}
```



Die Textur wird mit einer Texturvariablen tex0 deklariert.

In diesem Beispiel wird eine Samplervariable namens s \_ 2D deklariert. Der Sampler enthält den Samplerzustand in geschweiften Klammern. Dies schließt die Textur ein, die entnommen wird, und optional den Filterzustand (d. h. Umbruchmodi, Filtermodi usw.). Wenn der Samplerzustand ausgelassen wird, wird ein Standardzustand des Samplers angewendet, der die lineare Filterung und einen Umbruchmodus für die Texturkoordinaten angibt. Die Samplerfunktion nimmt eine Gleitkommatexturkoordinate mit zwei Komponenten an und gibt eine Farbe mit zwei Komponenten zurück. Dies wird mit dem Rückgabetyp float2 dargestellt und stellt Daten in den rot-grünen Komponenten dar.

Vier Arten von Samplern werden definiert (siehe [Schlüsselwörter](dx-graphics-hlsl-appendix.md)), und Texturs lookups werden von den systeminternen Funktionen ausgeführt: [**tex1D(s, t) (DirectX HLSL)**](dx-graphics-hlsl-tex1d.md), [**tex2D(s, t) (DirectX HLSL)**](dx-graphics-hlsl-tex2d.md), [**tex3D(s, t) (DirectX HLSL)**](dx-graphics-hlsl-tex3d.md), [**texCUBE(s, t) (DirectX HLSL).**](dx-graphics-hlsl-texcube.md) Hier sehen Sie ein Beispiel für die 3D-Stichprobenentnahme:


```
texture tex0;
sampler3D s_3D;

float3 sample_3D(float3 tex : TEXCOORD0) : COLOR
{
  return tex3D(s_3D, tex);
}
```



Diese Samplerdeklaration verwendet den Standard-Samplerzustand für die Filtereinstellungen und den Adressmodus.

Hier sehen Sie das entsprechende Beispiel für die Cubesampling:


```
texture tex0;
samplerCUBE s_CUBE;

float3 sample_CUBE(float3 tex : TEXCOORD0) : COLOR
{
  return texCUBE(s_CUBE, tex);
}
```



Und schließlich sehen Sie hier das Beispiel für die 1D-Stichprobenentnahme:


```
texture tex0;
sampler1D s_1D;

float sample_1D(float tex : TEXCOORD0) : COLOR
{
  return tex1D(s_1D, tex);
}
```



Da die Runtime keine 1D-Texturen unterstützt, verwendet der Compiler eine 2D-Textur mit dem Wissen, dass die y-Koordinate unwichtig ist. Da [**tex1D(s, t) (DirectX HLSL)**](dx-graphics-hlsl-tex1d.md) als 2D-Textursuche implementiert ist, kann der Compiler die y-Komponente effizient auswählen. In einigen seltenen Szenarien kann der Compiler keine effiziente y-Komponente auswählen. In diesem Fall gibt er eine Warnung aus.


```
texture tex0;
sampler s_1D_float;

float4 main(float texCoords : TEXCOORD) : COLOR
{
    return tex1D(s_1D_float, texCoords);
}
```



Dieses spezielle Beispiel ist ineffizient, da der Compiler die Eingabekoordinate in ein anderes Register verschieben muss (da eine 1D-Suche als 2D-Suche implementiert und die Texturkoordinate als float1 deklariert wird). Wenn der Code mithilfe einer float2-Eingabe anstelle von float1 umgeschrieben wird, kann der Compiler die Eingabetexturkoordinate verwenden, da er weiß, dass y mit etwas initialisiert wird.


```
texture tex0;
sampler s_1D_float2;

float4 main(float2 texCoords : TEXCOORD) : COLOR
{
    return tex1D(s_1D_float2, texCoords);
}
```



Alle Texturs lookups können mit "bias" oder "proj" (d.h. [**tex2Dbias (DirectX HLSL)**](dx-graphics-hlsl-tex2dbias.md), [**texCUBEproj (DirectX HLSL)**](dx-graphics-hlsl-texcubeproj.md)) angefügt werden. Mit dem Suffix "proj" wird die Texturkoordinate durch die w-Komponente geteilt. Mit "Bias" wird die Mip-Ebene von der w-Komponente verschoben. Daher nehmen alle Texturs lookups mit einem Suffix immer eine float4-Eingabe an. [**tex1D(s, t) (DirectX HLSL)**](dx-graphics-hlsl-tex1d.md) und [**tex2D(s, t) (DirectX HLSL)**](dx-graphics-hlsl-tex2d.md) ignorieren die yz- bzw. z-Komponenten.

Sampler können auch im Array verwendet werden, obwohl derzeit kein Back-End den dynamischen Arrayzugriff auf Sampler unterstützt. Daher ist Folgendes gültig, da es zur Kompilierzeit aufgelöst werden kann:


```
tex2D(s[0],tex)
```



Dieses Beispiel ist jedoch ungültig.


```
tex2D(s[a],tex)
```



Der dynamische Zugriff auf Sampler ist in erster Linie für das Schreiben von Programmen mit Literalschleifen nützlich. Der folgende Code veranschaulicht den Zugriff auf Samplerarrays:


```
sampler sm[4];

float4 main(float4 tex[4] : TEXCOORD) : COLOR
{
    float4 retColor = 1;

    for(int i = 0; i < 4;i++)
    {
        retColor *= tex2D(sm[i],tex[i]);
    }

    return retColor;
}
```



> [!Note]
>
> Mithilfe der Microsoft Direct3D-Debuglaufzeit können Sie Konflikte zwischen der Anzahl der Komponenten in einer Textur und einem Sampler abfangen.

 

## <a name="writing-functions"></a>Schreiben von Funktionen

Funktionen untergliedern große Aufgaben in kleinere Aufgaben. Kleine Aufgaben sind einfacher zu debuggen und können wiederverwendet werden, sobald sie sich bewährt haben. Funktionen können verwendet werden, um Details anderer Funktionen auszublenden, wodurch ein Programm, das aus Funktionen besteht, einfacher zu verfolgen ist.

HLSL-Funktionen ähneln C-Funktionen auf verschiedene Weise: Sie enthalten sowohl eine Definition als auch einen Funktionstext und deklarieren sowohl Rückgabetypen als auch Argumentlisten. Wie C-Funktionen führt die HLSL-Validierung typüberprüfungen für die Argumente, Argumenttypen und den Rückgabewert während der Shaderkompilierung durch.

Im Gegensatz zu C-Funktionen verwenden HLSL-Einstiegspunktfunktionen Semantik, um Funktionsargumente an Shadereingaben und -ausgaben zu binden (HLSL-Funktionen, die intern aufgerufen werden, ignorieren Semantik). Dies erleichtert das Binden von Pufferdaten an einen Shader und das Binden von Shaderausgaben an Shadereingaben.

Eine Funktion enthält eine Deklaration und einen Text, und die Deklaration muss dem Text vorangehen.


```
float4 VertexShader_Tutorial_1(float4 inPos : POSITION ) : POSITION
{
    return mul(inPos, WorldViewProj );
};
```



Die Funktionsdeklaration enthält alles vor den geschweiften Klammern:


```
float4 VertexShader_Tutorial_1(float4 inPos : POSITION ) : POSITION
```



Eine Funktionsdeklaration enthält Folgendes:

-   Ein Rückgabetyp
-   Ein Funktionsname
-   Eine Argumentliste (optional)
-   Eine Ausgabesemantik (optional)
-   Eine Anmerkung (optional)

Der Rückgabetyp kann jeder der grundlegenden HLSL-Datentypen sein, z. B. float4:


```
float4 VertexShader_Tutorial_1(float4 inPos : POSITION ) : POSITION
{
   ...
}
```



Der Rückgabetyp kann eine Struktur sein, die bereits definiert wurde:


```
struct VS_OUTPUT
{
    float4  vPosition        : POSITION;
    float4  vDiffuse         : COLOR;
}; 

VS_OUTPUT VertexShader_Tutorial_1(float4 inPos : POSITION )
{
   ...
}
```



Wenn die Funktion keinen Wert zurückgibt, kann void als Rückgabetyp verwendet werden.


```
void VertexShader_Tutorial_1(float4 inPos : POSITION )
{
   ...
}
```



Der Rückgabetyp wird immer zuerst in einer Funktionsdeklaration angezeigt.


```
float4 VertexShader_Tutorial_1(float4 inPos : POSITION ) : POSITION
```



Eine Argumentliste deklariert die Eingabeargumente für eine Funktion. Sie kann auch Werte deklarieren, die zurückgegeben werden. Einige Argumente sind sowohl Eingabe- als auch Ausgabeargumente. Hier sehen Sie ein Beispiel für einen Shader, der vier Eingabeargumente annimmt.


```
float4 Light(float3 LightDir : TEXCOORD1, 
             uniform float4 LightColor,  
             float2 texcrd : TEXCOORD0, 
             uniform sampler samp) : COLOR 
{
    float3 Normal = tex2D(samp,texcrd);

    return dot((Normal*2 - 1), LightDir)*LightColor;
}
```



Diese Funktion gibt eine endgültige Farbe zurück, die eine Mischung aus einem Texturbeispiel und der hellen Farbe ist. Die Funktion nimmt vier Eingaben entgegen. Zwei Eingaben haben Semantik: LightDir hat die [TEXCOORD1-Semantik](dx-graphics-hlsl-semantics.md) und texcrd die [TEXCOORD0-Semantik.](dx-graphics-hlsl-semantics.md) Die Semantik bedeutet, dass die Daten für diese Variablen aus dem Scheitelpunktpuffer stammen. Obwohl die LightDir-Variable über eine [TEXCOORD1-Semantik](dx-graphics-hlsl-semantics.md) verfügt, ist der Parameter wahrscheinlich keine Texturkoordinate. Der TEXCOORDn-Semantiktyp wird häufig verwendet, um eine Semantik für einen Typ zu liefern, der nicht vordefiniert ist (es gibt keine Vertex-Shader-Eingabesemantik für eine lichte Richtung).

Die beiden anderen Eingaben LightColor und samp sind mit dem [Schlüsselwort uniform](dx-graphics-hlsl-appendix.md) gekennzeichnet. Dies sind einheitliche Konstanten, die sich zwischen Draw-Aufrufen nicht ändern. Die Werte für diese Parameter stammen aus globalen Shadervariablen.

Argumente können als Eingaben mit dem Schlüsselwort in und Ausgabeargumente mit dem Schlüsselwort out bezeichnet werden. Argumente können nicht als Verweis übergeben werden. Ein Argument kann jedoch sowohl eine Eingabe als auch eine Ausgabe sein, wenn es mit dem Schlüsselwort inout deklariert wird. Argumente, die an eine Funktion übergeben werden, die mit dem Schlüsselwort inout markiert sind, werden als Kopien des Originals betrachtet, bis die Funktion zurückgegeben wird, und sie werden zurückkopiert. Hier sehen Sie ein Beispiel für die Verwendung von inout:


```
void Increment_ByVal(inout float A, inout float B) 
{ 
    A++; B++;
}
```



Diese Funktion erhöht die Werte in A und B und gibt sie zurück.

Der Funktionstext ist der gesamte Code nach der Funktionsdeklaration.


```
float4 VertexShader_Tutorial_1(float4 inPos : POSITION ) : POSITION
{
    return mul(inPos, WorldViewProj );
};
```



Der Text besteht aus Anweisungen, die von geschweiften Klammern umgeben sind. Der Funktionstext implementiert alle Funktionen mithilfe von Variablen, Literalen, Ausdrücken und Anweisungen.

Der Shadertext führt zwei Dinge aus: Er führt eine Matrixmultiplikation aus und gibt ein float4-Ergebnis zurück. Die Matrixmultiplikation wird mit der multiplizierenden [**DirectX-Funktion (DirectX HLSL)**](dx-graphics-hlsl-mul.md) durchgeführt, die eine Multiplikation der 4x4-Matrix ausführt. **mul (DirectX HLSL)** wird als systeminterne Funktion bezeichnet, da sie bereits in die HLSL-Funktionsbibliothek integriert ist. Systeminterne Funktionen werden im nächsten Abschnitt ausführlicher behandelt.

Die Matrixmultiplikation kombiniert einen Eingabevektor Pos und eine zusammengesetzte Matrix WorldViewProj. Das Ergebnis sind Positionsdaten, die in den Bildschirmbereich transformiert werden. Dies ist die minimale Vertex-Shaderverarbeitung, die wir durchführen können. Wenn wir die Feste Funktionspipeline anstelle eines Vertex-Shaders verwenden, könnten die Scheitelpunktdaten nach dieser Transformation gezeichnet werden.

Die letzte Anweisung in einem Funktionstext ist eine return-Anweisung. Genau wie C gibt diese Anweisung die Steuerung von der Funktion an die Anweisung zurück, die die Funktion aufgerufen hat.

Funktionsrückgabetypen können alle in HLSL definierten einfachen Datentypen sein, einschließlich bool, int half, float und double. Rückgabetypen können einer der komplexen Datentypen sein, z. B. Vektoren und Matrizen. HLSL-Typen, die auf Objekte verweisen, können nicht als Rückgabetypen verwendet werden. Dies schließt Pixelshader, Vertexshader, Textur und Sampler ein.

Hier ist ein Beispiel für eine Funktion, die eine -Struktur für einen Rückgabetyp verwendet.


```
float4x4 WorldViewProj : WORLDVIEWPROJ;

struct VS_OUTPUT
{
    float4 Pos  : POSITION;
};

VS_OUTPUT VS_HLL_Example(float4 inPos : POSITION )
{
    VS_OUTPUT Out;

    Out.Pos = mul(inPos,  WorldViewProj );

    return Out;
};
```



Der rückgabetyp float4 wurde durch die Struktur VS \_ OUTPUT ersetzt, die jetzt einen einzelnen float4-Member enthält.

Eine return-Anweisung signalisiert das Ende einer Funktion. Dies ist die einfachste return-Anweisung. Sie gibt die Steuerung von der Funktion an das aufrufende Programm zurück. Es wird kein Wert zurückgegeben.


```
void main()
{
    return ;
}
```



Eine return-Anweisung kann einen oder mehrere Werte zurückgeben. In diesem Beispiel wird ein Literalwert zurückgegeben:


```
float main( float input : COLOR0) : COLOR0
{
    return 0;
}
```



In diesem Beispiel wird das skalare Ergebnis eines Ausdrucks zurückgegeben:


```
return  light.enabled;
```



In diesem Beispiel wird ein float4-Wert zurückgegeben, der aus einer lokalen Variablen und einem Literal erstellt wurde:


```
return  float4(color.rgb, 1) ;
```



In diesem Beispiel wird ein float4-Wert zurückgegeben, der aus dem Von einer systeminternen Funktion zurückgegebenen Ergebnis und einigen Literalwerten erstellt wird:


```
float4 func(float2 a: POSITION): COLOR
{
    return float4(sin(length(a) * 100.0) * 0.5 + 0.5, sin(a.y * 50.0), 0, 1);
}
```



In diesem Beispiel wird eine -Struktur zurückgegeben, die einen oder mehrere Member enthält:


```
float4x4 WorldViewProj;

struct VS_OUTPUT
{
    float4 Pos  : POSITION;
};

VS_OUTPUT VertexShader_Tutorial_1(float4 inPos : POSITION )
{
    VS_OUTPUT out;
    out.Pos = mul(inPos, WorldViewProj );
    return out;
};
```



## <a name="flow-control"></a>Flusssteuerung

Die meisten aktuellen Scheitelpunkt- und Pixel-Shaderhardware ist so konzipiert, dass eine Shaderlinie zeilenweisend ausgeführt wird, wobei jede Anweisung einmal ausgeführt wird. HLSL unterstützt die Flusssteuerung, einschließlich statischer Verzweigung, prädikatierter Anweisungen, statischer Schleifen, dynamischer Verzweigung und dynamischer Schleife.

Zuvor führte die Verwendung einer if-Anweisung zu Assemblysprach-Shadercode, der sowohl die if-Seite als auch die andere Seite des Codeflows implementiert. Im Folgenden finden Sie ein Beispiel für den in HLSL-Code, der für \_ 1 1 kompiliert \_ wurde:


```
if (Value > 0)
    oPos = Value1; 
else
    oPos = Value2; 
```



Und hier ist der resultierende Assemblycode:


```
// Calculate linear interpolation value in r0.w
mov r1.w, c2.x               
slt r0.w, c3.x, r1.w         
// Linear interpolation between value1 and value2
mov r7, -c1                      
add r2, r7, c0                   
mad oPos, r0.w, r2, c1  
```



Einige Hardware ermöglicht entweder statisches oder dynamisches Schleifen, aber die meisten erfordern eine lineare Ausführung. Für die Modelle, die keine Schleifen unterstützen, muss die Registrierung aller Schleifen aufgehoben werden. Ein Beispiel hierfür ist das [Beispiel "DepthOfField Sample",](https://msdn.microsoft.com/library/Ee416592(v=VS.85).aspx) das unrollierte Schleifen auch für Ps \_ 1 \_ 1-Shader verwendet.

HLSL bietet jetzt Unterstützung für jede dieser Arten von Flusssteuerung:

-   statische Verzweigung
-   Prädikatanweisungen
-   statische Schleifen
-   Dynamische Verzweigung
-   Dynamisches Schleifening

Statische Verzweigung ermöglicht das Ein- oder Ausschalten von Shadercodeblöcken basierend auf einer booleschen Shaderkonstante. Dies ist eine praktische Methode zum Aktivieren oder Deaktivieren von Codepfaden basierend auf dem Typ des objekts, das gerade gerendert wird. Zwischen Draw-Aufrufen können Sie entscheiden, welche Features Sie mit dem aktuellen Shader unterstützen möchten, und dann die booleschen Flags festlegen, die zum Abrufen dieses Verhaltens erforderlich sind. Alle Anweisungen, die von einer booleschen Konstante deaktiviert werden, werden während der Shaderausführung übersprungen.

Die vertrauteste Verzweigungsunterstützung ist die dynamische Verzweigung. Bei der dynamischen Verzweigung befindet sich die Vergleichsbedingung in einer Variablen, was bedeutet, dass der Vergleich für jeden Scheitelpunkt oder jedes Pixel zur Laufzeit durchgeführt wird (im Gegensatz zum Vergleich zur Kompilierzeit oder zwischen zwei Zeichnen-Aufrufen). Die Leistungstreffer sind die Kosten für den Branch plus die Kosten für die Anweisungen auf der Seite des Branchs. Dynamische Verzweigung wird im Shadermodell 3 oder höher implementiert. Die Optimierung von Shadern, die mit diesen Modellen funktionieren, ähnelt der Optimierung von Code, der auf einer CPU ausgeführt wird.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Programmieranleitung für HLSL](dx-graphics-hlsl-pguide.md)
</dt> </dl>

 

 
