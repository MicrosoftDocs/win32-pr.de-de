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
ms.openlocfilehash: 504a1d9ff5a2aa2b37227f0016cdc97d28d967fe
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "104039378"
---
# <a name="writing-hlsl-shaders-in-direct3d-9"></a>Schreiben von HLSL-Shadern in Direct3D 9

-   [Vertex-Shader-Grundlagen](#vertex-shader-basics)
-   [Grundlagen des Pixel-Shaders](#pixel-shader-basics)
    -   [Textur Stufen und samplerzustände](#texture-stage-and-sampler-states)
    -   [Pixel-shadereingaben](#pixel-shader-inputs)
    -   [Pixel-Shader-Ausgaben](#pixel-shader-outputs)
-   [Shadereingaben und shadervariablen](#shader-inputs-and-shader-variables)
    -   [Deklarieren von shadervariablen](#declaring-shader-variables)
    -   [Einheitliche shadereingaben](#uniform-shader-inputs)
    -   [Variierende shadereingaben und-Semantik](#varying-shader-inputs-and-semantics)
    -   [Samplers und Textur Objekte](#samplers-and-texture-objects)
-   [Schreiben von Funktionen](#writing-functions)
-   [Fluss Steuerung](#flow-control)
-   [Zugehörige Themen](#related-topics)

## <a name="vertex-shader-basics"></a>Grundlagen zu Vertex-Shader

Bei einem Vorgang ersetzt ein programmierbarer Vertexshader die Scheitelpunkt Verarbeitung, die durch die Microsoft Direct3D-Grafik Pipeline durchgeführt wird. Bei der Verwendung eines Scheitelpunkt-Shaders werden Zustandsinformationen zu Transformations-und Beleuchtungs Vorgängen von der Fixed-Funktions Pipeline ignoriert. Wenn der Vertex-Shader deaktiviert ist und die Verarbeitung fester Funktionen zurückgegeben wird, gelten alle aktuellen Zustands Einstellungen.

Vor der Ausführung des Vertexshaders sollte vor der Ausführung des Scheitelpunkt-Shaders ein Mosaik Prozess erstellt werden. Implementierungen, die nach der shaderverarbeitung das Oberflächen Mosaik ausführen, müssen dies auf eine Weise tun, die für die Anwendung und den Shader-Code nicht offensichtlich ist.

Ein Vertex-Shader muss mindestens eine Scheitelpunkt Position im homogenen Clip Bereich ausgeben. Optional kann der Vertex-Shader Texturkoordinaten, Scheitelpunkt Farben, Scheitelpunkt Beleuchtung, Nebel Faktoren usw. ausgeben.

## <a name="pixel-shader-basics"></a>Grundlagen zu Pixel-Shader

Die Pixel Verarbeitung erfolgt durch Pixel-Shader in einzelnen Pixeln. Pixel-Shader arbeiten mit Vertex-Shadern. die Ausgabe eines Vertex-Shaders stellt die Eingaben für einen PixelShader bereit. Andere Pixel Vorgänge (Nebel-Blending, Schablone-Vorgänge und renderzielmischung) treten nach der Ausführung des Shaders auf.

### <a name="texture-stage-and-sampler-states"></a>Textur Stufen und samplerzustände

Ein Pixelshader ersetzt vollständig die Pixel Mischungs Funktionen, die durch den Multitexture-Blender angegeben werden, einschließlich Vorgängen, die zuvor durch den Text der Textur Stufe definiert wurden. Textur Sampling-und Filter Vorgänge, die von den standardmäßigen Textur Phasen für Minimierung, Vergrößerung, MIP-Filterung und Umbruch Adressierungs Modi gesteuert wurden, können in Shadern initialisiert werden. Die Anwendung kann diese Zustände ändern, ohne dass der derzeit gebundene Shader neu generiert werden muss. Das Festlegen des Zustands kann sogar noch einfacher gemacht werden, wenn die Shader innerhalb eines Effekts entworfen wurden.

### <a name="pixel-shader-inputs"></a>Pixel-shadereingaben

Bei Pixel-Shader-Versionen PS \_ 1 \_ 1-PS \_ 2 \_ 0 sind diffuse und Glanz Farben im Bereich von 0 bis 1 erschöpft (geklammert), bevor Sie vom Shader verwendet werden.

Die Eingabe von Farbwerten für den Pixelshader wird als Perspektive angesehen, aber dies ist nicht garantiert (für alle Hardware). Farben, die aus Texturkoordinaten entnommen werden, werden in einer Perspektive ordnungsgemäß durchlaufen und während der Iterationen an den Bereich von 0 bis 1 gebunden.

### <a name="pixel-shader-outputs"></a>Pixel-Shader-Ausgaben

Bei Pixel-Shader-Versionen PS \_ 1 \_ 1-PS \_ 1 \_ 4 ist das vom Pixelshader ausgegebene Ergebnis der Inhalt von Register R0. Alles, was es enthält, wenn der Shader die Verarbeitung abschließt, wird an die Nebel-und Renderziel-Blender gesendet.

Bei Pixel-Shader-Versionen PS \_ 2 \_ 0 und höher wird die Ausgabe Farbe von oC0-oC4 ausgegeben.

## <a name="shader-inputs-and-shader-variables"></a>Shadereingaben und shadervariablen

-   [Deklarieren von shadervariablen](#declaring-shader-variables)
-   [Einheitliche shadereingaben](#uniform-shader-inputs)
-   [Variierende shadereingaben und-Semantik](#varying-shader-inputs-and-semantics)
-   [Samplers und Textur Objekte](#samplers-and-texture-objects)

### <a name="declaring-shader-variables"></a>Deklarieren von shadervariablen

Die einfachste Variablen Deklaration enthält einen Typ und einen Variablennamen, wie z. b. diese Gleit Komma Deklaration:


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



oder in derselben Anweisung deklariert und initialisiert.


```
int iVar[3] = {1,2,3};
```



Im folgenden finden Sie einige Deklarationen, die viele der Merkmale von HLSL-Variablen (High-Level Shader Language) veranschaulichen:


```
float4 color;
uniform float4 position : POSITION; 
const float4 lightDirection = {0,0,1};
```



Datendeklarationen können einen beliebigen gültigen Typ verwenden, einschließlich:

-   [Datentypen (DirectX HLSL)](dx-graphics-hlsl-data-types.md)
-   [Vector Type (DirectX HLSL)](dx-graphics-hlsl-vector.md)
-   [Matrixtyp (DirectX HLSL)](dx-graphics-hlsl-matrix.md)
-   [Shadertyp (DirectX HLSL)](dx-graphics-hlsl-shader.md)
-   [Sampltyp (DirectX HLSL)](dx-graphics-hlsl-sampler.md)
-   [Benutzerdefinierter Typ (DirectX HLSL)](dx-graphics-hlsl-user-defined.md)

Ein Shader kann Variablen, Argumente und Funktionen der obersten Ebene aufweisen.


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



Variablen der obersten Ebene werden außerhalb aller Funktionen deklariert. Argumente der obersten Ebene sind Parameter für eine Funktion der obersten Ebene. Eine Funktion der obersten Ebene ist jede Funktion, die von der Anwendung aufgerufen wird (im Gegensatz zu einer Funktion, die von einer anderen Funktion aufgerufen wird).

### <a name="uniform-shader-inputs"></a>Einheitliche shadereingaben

Scheitelpunkt-und Pixel-Shader akzeptieren zwei Arten von Eingabedaten: unterschiedlich und einheitlich. Die unterschiedliche Eingabe sind die Daten, die für jede Ausführung des Shaders eindeutig sind. Bei einem Vertex-Shader stammen die unterschiedlichen Daten (z. b. Position, normal usw.) aus den vertexstreams. Die einheitlichen Daten (z. b. Material Color, World Transform usw.) sind für mehrere Ausführungen eines Shaders konstant. Für diejenigen, die mit den assemblyshader-Modellen vertraut sind, werden einheitliche Daten durch konstante Register und abweichende Daten durch die v-und t-Register angegeben.

Einheitliche Daten können durch zwei Methoden angegeben werden. Die gängigste Methode besteht darin, globale Variablen zu deklarieren und in einem Shader zu verwenden. Jede Verwendung von globalen Variablen in einem Shader führt dazu, dass diese Variable der Liste der für diesen Shader erforderlichen, einheitlichen Variablen hinzugefügt wird. Die zweite Methode besteht darin, einen Eingabeparameter der Shader-Funktion der obersten Ebene als einheitlich zu markieren. Diese Markierung gibt an, dass die angegebene Variable der Liste der einheitlichen Variablen hinzugefügt werden soll.

Von einem Shader verwendete einheitliche Variablen werden über die Konstante Tabelle an die Anwendung übermittelt. Die Konstante Tabelle ist der Name für die Symboltabelle, der definiert, wie die von einem Shader verwendeten einheitlichen Variablen in die Konstanten Register passen. Die Parameter der einheitlichen Funktion erscheinen in der Konstanten Tabelle, der ein Dollarzeichen ($) vorangestellt ist, im Gegensatz zu den globalen Variablen. Das Dollarzeichen ist erforderlich, um Namenskollisionen zwischen lokalen, einheitlichen Eingaben und globalen Variablen mit demselben Namen zu vermeiden.

Die Konstante Tabelle enthält die Konstanten Register Speicherorte aller vom Shader verwendeten einheitlichen Variablen. Die Tabelle enthält auch die Typinformationen und den Standardwert, falls angegeben.

### <a name="varying-shader-inputs-and-semantics"></a>Variierende shadereingaben und-Semantik

Abweichende Eingabeparameter (einer shaderfunktion der obersten Ebene) müssen entweder mit einem Semantic-oder Uniform-Schlüsselwort markiert werden, das angibt, dass der Wert für die Ausführung des Shaders konstant ist. Wenn eine Shader-Eingabe der obersten Ebene nicht mit einem Semantic-oder Uniform-Schlüsselwort gekennzeichnet ist, kann der Shader nicht kompiliert werden.

Die Eingabe Semantik ist ein Name, der verwendet wird, um die angegebene Eingabe mit einer Ausgabe des vorherigen Teils der Grafik Pipeline zu verknüpfen. Beispielsweise wird die Eingabe Semantik POSITION0 von den Vertexshadern verwendet, um anzugeben, wo die Positionsdaten aus dem Vertex-Puffer verknüpft werden sollen.

Pixel-und Vertex-Shader haben unterschiedliche Sätze der Eingabe Semantik, da die verschiedenen Teile der Grafik Pipeline in jede shadereinheit eingecheckt werden. Die Vertex-Shader-Eingabe Semantik beschreibt die pro-Vertex-Informationen (z. b. Position, normal, Texturkoordinaten, Farbe, Tangens, Binormal usw.), die aus einem Vertex-Puffer in ein Formular geladen werden sollen, das vom Vertexshader verwendet werden kann. Die Eingabe Semantik wird direkt der Vertex-Deklarations Verwendung und dem Verwendungs Index zugeordnet.

Die Pixel-Shader-Eingabe Semantik beschreibt die Informationen, die pro Pixel von der rasterisierungseinheit bereitgestellt werden. Die Daten werden durch Interpolation zwischen Ausgaben des Vertex-Shaders für jeden Scheitelpunkt des aktuellen primitiven generiert. Die grundlegende Pixel-Shader-Eingabe Semantik verknüpft die Ausgabe Farbe und die Texturkoordinaten Informationen mit den Eingabe Parametern.

Die Eingabe Semantik kann Shader-Eingaben mit zwei Methoden zugewiesen werden:

-   Anhängen eines Doppelpunkts und des semantischen namens an die Parameter Deklaration.
-   Definieren einer Eingabe Struktur mit der Eingabe Semantik, die jedem Strukturmember zugewiesen ist.

Vertex-und Pixel-Shader stellen Ausgabedaten für die nachfolgende Grafik Pipeline Phase bereit. Die Ausgabe Semantik wird verwendet, um anzugeben, wie Daten, die vom Shader generiert werden, mit den Eingaben der nächsten Stufe verknüpft werden sollen. Beispielsweise wird die Ausgabe Semantik für einen Vertex-Shader verwendet, um die Ausgaben der Interpolatoren im Raster zu verknüpfen, um die Eingabedaten für den Pixelshader zu generieren. Die Pixel-Shader-Ausgaben sind die Werte, die für die Alpha Mischungs Einheit für jedes der Renderziele bereitgestellt werden, oder der in den tiefen Puffer geschriebene tiefen Wert.

Die Vertex-Shader-Ausgabe Semantik wird verwendet, um den Shader sowohl mit dem Pixelshader als auch mit der Raster-Stufe zu verknüpfen. Ein Vertexshader, der vom Raster genutzt wird und nicht für den Pixelshader verfügbar gemacht wird, muss die Positionsdaten als minimal generieren. Vertexshader, die Texturkoordinaten und Farbdaten generieren, stellen diese Daten einem Pixelshader nach dem Durchführen der Interpolation zur Verfügung.

Die Pixel-Shader-Ausgabe Semantik bindet die Ausgabe Farben eines Pixelshaders mit dem richtigen Renderziel. Die Pixel-Shader-Ausgabe Farbe ist mit der Alpha Blend-Phase verknüpft, die bestimmt, wie die zielrenderziele geändert werden. Die Ausgabe der Pixel-Shader-Tiefe kann verwendet werden, um die Ziel tiefen Werte an der aktuellen Raster Position zu ändern. Die tiefen Ausgabe und mehrere Renderingziele werden nur mit einigen shadermodellen unterstützt.

Die Syntax für die Ausgabe Semantik ist mit der Syntax zum Angeben der Eingabe Semantik identisch. Die Semantik kann entweder direkt für Parameter angegeben werden, die als "out"-Parameter deklariert oder während der Definition einer Struktur zugewiesen werden, die entweder als "out"-Parameter oder als Rückgabewert einer Funktion zurückgegeben wurde.

Die Semantik identifiziert, woher die Daten stammen. Semantik sind optionale Bezeichner zur Identifizierung von shadereingaben und-Ausgaben. Die Semantik wird an einem von drei Stellen angezeigt:

-   Nach einem Strukturmember.
-   Nach einem Argument in der Eingabe Argumentliste einer Funktion.
-   Nach der Eingabe Argumentliste der Funktion.

In diesem Beispiel wird eine-Struktur verwendet, um eine oder mehrere vertexshadereingaben bereitzustellen, und eine weitere-Struktur, um eine oder mehrere vertexshaderausgaben bereitzustellen. Jedes der Strukturmember verwendet eine Semantik.


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



Die Eingabe Struktur identifiziert die Daten aus dem Vertex-Puffer, der die shadereingaben bereitstellt. Dieser Shader ordnet die Daten aus den Positionen "Position", "Normal" und "blendweight" des Vertexpuffers den Vertex-Shader-Registern zu. Der Eingabe Datentyp muss nicht exakt mit dem Datentyp der Vertex-Deklaration übereinstimmen. Wenn Sie nicht genau übereinstimmt, werden die Scheitelpunkt Daten automatisch in den Datentyp von HLSL konvertiert, wenn Sie in die Shader-Register geschrieben werden. Wenn beispielsweise die normalen Daten vom Typ uint von der Anwendung definiert wurden, werden Sie beim Lesen durch den Shader in eine float3 konvertiert.

Wenn die Daten im vertexstream weniger Komponenten als der entsprechende shaderdatentyp enthalten, werden die fehlenden Komponenten mit 0 initialisiert (mit Ausnahme von w, die auf 1 initialisiert wird).

Die Eingabe Semantik ähnelt den Werten in [**D3DDECLUSAGE**](/windows/desktop/direct3d9/d3ddeclusage).

Die Ausgabestruktur identifiziert die Scheitelpunkt-Shader-Ausgabeparameter von Position und Farbe. Diese Ausgaben werden von der Pipeline für die Dreiecks rasterisierung (in primitiver Verarbeitung) verwendet. Die als Positionsdaten markierte Ausgabe bezeichnet die Position eines Scheitel Punkts in homogenem Raum. Ein Vertex-Shader muss mindestens Positionsdaten generieren. Die Position des Bildschirm Raums wird berechnet, nachdem der Vertexshader abgeschlossen ist, indem die (x, y, z)-Koordinate durch w dividiert wird. Im Bildschirmbereich sind-1 und 1 die minimalen und maximalen x-und y-Werte der Grenzen des Viewports, während z zum Testen von z-Puffern verwendet wird.

Die Ausgabe Semantik ähnelt auch den Werten in [**D3DDECLUSAGE**](/windows/desktop/direct3d9/d3ddeclusage). Im Allgemeinen kann eine Ausgabestruktur für einen Vertex-Shader auch als Eingabe Struktur für einen PixelShader verwendet werden, vorausgesetzt, der Pixelshader liest nicht aus einer Variablen, die mit der Position, der Punktgröße oder der Semantik des Diagramms gekennzeichnet ist. Diese Semantik wird mit pro-Vertex-Skalarwerten verknüpft, die nicht von einem Pixelshader verwendet werden. Wenn diese Werte für den Pixelshader erforderlich sind, können Sie in eine andere Ausgabevariable kopiert werden, die eine Pixel-Shader-Semantik verwendet.

Globale Variablen werden vom Compiler automatisch registriert. Globale Variablen werden auch als einheitliche Parameter bezeichnet, da der Inhalt der Variablen bei jedem Aufruf des Shaders identisch für alle Pixel ist, die verarbeitet werden. Die Register sind in der Konstanten Tabelle enthalten, die mit der [**ID3DXConstantTable**](/windows/desktop/direct3d9/id3dxconstanttable) -Schnittstelle gelesen werden kann.

Die Eingabe Semantik für Pixel-Shader ordnet Werte bestimmten Hardware Registern für den Transport zwischen Scheitelpunkt-Shadern und Pixel-Shadern zu. Jeder registriungstyp verfügt über bestimmte Eigenschaften. Da zurzeit nur zwei Semantik für Farb-und Texturkoordinaten vorhanden ist, werden die meisten Daten häufig als Texturkoordinaten gekennzeichnet, auch wenn dies nicht der Fall ist.

Beachten Sie, dass die Vertex-Shader-Ausgabestruktur eine Eingabe mit Positionsdaten verwendet hat, die nicht vom Pixelshader verwendet wird. HLSL ermöglicht gültige Ausgabedaten eines Vertexshaders, bei dem es sich nicht um gültige Eingabedaten für einen PixelShader handelt, vorausgesetzt, dass im Pixelshader nicht auf Sie verwiesen wird.

Eingabeargumente können auch Arrays sein. Die Semantik wird automatisch vom Compiler für jedes Element des Arrays inkrementiert. Beachten Sie beispielsweise die folgende explizite Deklaration:


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



Die oben angegebene explizite Deklaration entspricht der folgenden Deklaration, deren Semantik vom Compiler automatisch inkrementiert wird:


```
float4 Sparkle(float4 Position : POSITION,
                 float3 Col[2] : COLOR0,
                 float3 Tex[4] : TEXCOORD0) : COLOR0
{
   // shader statements
   ...
```



Ebenso wie die Eingabe Semantik identifiziert die Ausgabe Semantik die Datenverwendung für die Pixel-Shader-Ausgabedaten. Viele Pixel-Shader schreiben nur in eine Ausgabe Farbe. Pixel-Shader können auch gleichzeitig einen tiefen Wert in ein oder mehrere Renderingziele schreiben (bis zu vier). Wie Vertex-Shader verwenden Pixel-Shader eine-Struktur, um mehr als eine Ausgabe zurückzugeben. Dieser Shader schreibt 0 sowohl in die Farbkomponenten als auch in die tiefen Komponente.


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



Die Pixel-Shader-Ausgabe Farben müssen den Typ "float4" aufweisen. Wenn Sie mehrere Farben schreiben, müssen alle Ausgabe Farben zusammenhängend verwendet werden. Anders ausgedrückt kann [COLOR1](dx-graphics-hlsl-semantics.md) keine Ausgabe sein, es sei denn, [COLOR0](dx-graphics-hlsl-semantics.md) wurde bereits geschrieben. Die Ausgabe der Pixel-Shader-Tiefe muss vom Typ float1 sein.

### <a name="samplers-and-texture-objects"></a>Samplers und Textur Objekte

Ein Sampler enthält den samplerzustand. Der samplerstatus gibt die zu sammelnde Textur an und steuert die Filterung, die während des Samplings durchgeführt wird. Zum Beispiel für eine Textur sind drei Schritte erforderlich:

-   Eine Textur
-   Ein Sampler (mit dem samplerzustand)
-   Eine Samplings-Anweisung

Samplers können mit Texturen und dem samplerzustand initialisiert werden, wie hier gezeigt:


```
sampler s = sampler_state 
{ 
  texture = NULL; 
  mipfilter = LINEAR; 
};
```



Im folgenden finden Sie ein Beispiel für den Code für die Stichprobenentnahme einer 2D-Textur:


```
texture tex0;
sampler2D s_2D;

float2 sample_2D(float2 tex : TEXCOORD0) : COLOR
{
  return tex2D(s_2D, tex);
}
```



Die Textur wird mit einer Textur Variablen tex0 deklariert.

In diesem Beispiel wird eine samplervariable mit dem Namen s \_ 2D deklariert. Der Sampler enthält den samplerstatus in geschweiften Klammern. Dies schließt die Textur ein, die als Stichprobe verwendet wird, und optional den Filter Zustand (d. h. Umbruch Modi, Filtermodi usw.). Wenn der samplerzustand weggelassen wird, wird ein Standard-samplerstatus angewendet, der lineare Filterung und einen Umbruch Modus für die Texturkoordinaten angibt. Die samplingfunktion nimmt eine Gleit Komma-Textur Koordinate mit zwei Komponenten an und gibt eine Farbe mit zwei Komponenten zurück. Dies wird durch den float2-Rückgabetyp dargestellt und stellt Daten in den roten und grünen Komponenten dar.

Es sind vier Typen von Samplern definiert (siehe [Schlüsselwörter](dx-graphics-hlsl-appendix.md)), und Textur Suchvorgänge werden von den intrinsischen Funktionen durchgeführt: [**tex1D (s, t) (DirectX HLSL)**](dx-graphics-hlsl-tex1d.md), [**tex2D (s, t) (DirectX HLSL)**](dx-graphics-hlsl-tex2d.md), [**tex3D (s, t) (DirectX HLSL**](dx-graphics-hlsl-tex3d.md)), [**Texcube (s, t) (DirectX HLSL)**](dx-graphics-hlsl-texcube.md). Hier ist ein Beispiel für die 3D-Stichprobenentnahme:


```
texture tex0;
sampler3D s_3D;

float3 sample_3D(float3 tex : TEXCOORD0) : COLOR
{
  return tex3D(s_3D, tex);
}
```



Diese samplerdeklaration verwendet den Standard samplerstatus für die Filtereinstellungen und den Adress Modus.

Hier sehen Sie das entsprechende Beispiel für eine Beispiel-Stichprobe


```
texture tex0;
samplerCUBE s_CUBE;

float3 sample_CUBE(float3 tex : TEXCOORD0) : COLOR
{
  return texCUBE(s_CUBE, tex);
}
```



Und zum Schluss ist das Beispiel für die 1D-Stichprobenentnahme:


```
texture tex0;
sampler1D s_1D;

float sample_1D(float tex : TEXCOORD0) : COLOR
{
  return tex1D(s_1D, tex);
}
```



Da die Common Language Runtime keine 1D-Texturen unterstützt, verwendet der Compiler eine 2D-Textur mit dem wissen, dass die y-Koordinate unwichtig ist. Da [**tex1D (s, t) (DirectX HLSL)**](dx-graphics-hlsl-tex1d.md) als 2D-Textur Suche implementiert ist, kann der Compiler die y-Komponente auf effiziente Weise auswählen. In einigen seltenen Szenarios kann der Compiler keine effiziente y-Komponente auswählen. in diesem Fall wird eine Warnung ausgegeben.


```
texture tex0;
sampler s_1D_float;

float4 main(float texCoords : TEXCOORD) : COLOR
{
    return tex1D(s_1D_float, texCoords);
}
```



Dieses spezielle Beispiel ist ineffizient, da der Compiler die eingabekoordinate in ein anderes Register verschieben muss (da eine 1D-Suche als 2D-Suche implementiert wird und die Textur Koordinate als float1 deklariert wird). Wenn der Code mit einer float2-Eingabe anstelle eines float1 umgeschrieben wird, kann der Compiler die Eingabe Textur Koordinate verwenden, da er weiß, dass y für etwas initialisiert wird.


```
texture tex0;
sampler s_1D_float2;

float4 main(float2 texCoords : TEXCOORD) : COLOR
{
    return tex1D(s_1D_float2, texCoords);
}
```



Alle Textur Suchvorgänge können mit "Bias" oder "proj" angehängt werden (d. h. [**tex2Dbias (DirectX HLSL)**](dx-graphics-hlsl-tex2dbias.md), [**texcubeproj (DirectX HLSL)**](dx-graphics-hlsl-texcubeproj.md)). Mit dem Suffix "proj" wird die Textur Koordinate durch die w-Komponente dividiert. Bei "Bias" wird die MIP-Ebene von der w-Komponente verlagert. Folglich nehmen alle Textur Suchvorgänge mit einem Suffix immer eine float4-Eingabe an. [**tex1D (s, t) (DirectX HLSL)**](dx-graphics-hlsl-tex1d.md) und [**tex2D (s, t) (DirectX HLSL)**](dx-graphics-hlsl-tex2d.md) ignorieren die YZ-und z-Komponenten.

Samplers können auch im Array verwendet werden, obwohl das Back-End derzeit keinen Zugriff auf das dynamische Array von Samplern unterstützt. Daher ist Folgendes gültig, da es zum Zeitpunkt der Kompilierung aufgelöst werden kann:


```
tex2D(s[0],tex)
```



Dieses Beispiel ist jedoch nicht gültig.


```
tex2D(s[a],tex)
```



Der dynamische Zugriff von Samplern ist hauptsächlich zum Schreiben von Programmen mit literalschleifen nützlich. Der folgende Code veranschaulicht den Zugriff auf samplerarrays:


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
> Die Verwendung der Microsoft Direct3D Debug-Laufzeit kann Ihnen helfen, Konflikte zwischen der Anzahl der Komponenten in einer Textur und einem Sampler abzufangen.

 

## <a name="writing-functions"></a>Schreiben von Funktionen

Funktionen unterbrechen große Aufgaben in kleinere. Kleine Aufgaben sind einfacher zu Debuggen und können wieder verwendet werden, sobald Sie sich bewährt haben. Funktionen können verwendet werden, um Details anderer Funktionen auszublenden, wodurch ein Programm, das aus Funktionen besteht, einfacher zu befolgen ist.

HLSL-Funktionen ähneln C-Funktionen auf verschiedene Weise: beide enthalten eine Definition und einen Funktions Text und deklarieren sowohl Rückgabe Typen als auch Argumentlisten. Wie bei C-Funktionen führt die HLSL-Validierung bei der Shader-Kompilierung eine Typüberprüfung für die Argumente, die Argument Typen und den Rückgabewert durch.

Im Gegensatz zu C-Funktionen verwenden HLSL-Einstiegspunkt Funktionen Semantik, um Funktionsargumente an Shader-Eingaben und-Ausgaben zu binden (HLSL-Funktionen, die intern die Semantik ignorieren). Dies vereinfacht das Binden von Puffer Daten an einen Shader und das Binden von shaderausgaben an shadereingaben.

Eine Funktion enthält eine Deklaration und einen Text, und die Deklaration muss dem Text vorangestellt sein.


```
float4 VertexShader_Tutorial_1(float4 inPos : POSITION ) : POSITION
{
    return mul(inPos, WorldViewProj );
};
```



Die Funktionsdeklaration enthält alles, was vor den geschweiften Klammern liegt:


```
float4 VertexShader_Tutorial_1(float4 inPos : POSITION ) : POSITION
```



Eine Funktionsdeklaration enthält Folgendes:

-   Ein Rückgabetyp
-   Ein Funktionsname
-   Eine Argumentliste (optional)
-   Eine Ausgabe Semantik (optional)
-   Eine Anmerkung (optional)

Der Rückgabetyp kann jeder der HLSL-Grund Datentypen sein, z. b. ein float4:


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



Eine Argumentliste deklariert die Eingabeargumente für eine Funktion. Es können auch Werte deklariert werden, die zurückgegeben werden. Einige Argumente sind Eingabe-und Ausgabe Argumente. Im folgenden finden Sie ein Beispiel für einen Shader, der vier Eingabeargumente annimmt.


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



Diese Funktion gibt eine endgültige Farbe zurück, bei der es sich um eine Mischung aus einem Textur Beispiel und der hellen Farbe handelt. Die Funktion nimmt vier Eingaben an. Zwei Eingaben haben eine Semantik: lightdir weist die [TEXCOORD1](dx-graphics-hlsl-semantics.md) -Semantik auf, und texcrd hat die [TEXCOORD0](dx-graphics-hlsl-semantics.md) -Semantik. Die Semantik bedeutet, dass die Daten für diese Variablen aus dem Vertex-Puffer stammen. Obwohl die lightdir-Variable über eine [TEXCOORD1](dx-graphics-hlsl-semantics.md) -Semantik verfügt, ist der-Parameter wahrscheinlich keine Textur Koordinate. Der semantische Typ texcoordn wird häufig zum Bereitstellen einer Semantik für einen Typ verwendet, der nicht vordefiniert ist (es gibt keine Vertex-Shader-Eingabe Semantik für eine leichte Richtung).

Die anderen beiden Eingaben LightColor und SAMP werden mit dem Schlüsselwort [Uniform](dx-graphics-hlsl-appendix.md) bezeichnet. Dabei handelt es sich um einheitliche Konstanten, die sich nicht zwischen zeichnen-aufrufen ändern. Die Werte für diese Parameter stammen aus globalen Shader-Variablen.

Argumente können mit dem in-Schlüsselwort als Eingaben gekennzeichnet werden, und es werden Ausgabe Argumente mit dem out-Schlüsselwort ausgegeben. Argumente können nicht als Verweis übermittelt werden. ein Argument kann jedoch sowohl eine Eingabe als auch eine Ausgabe sein, wenn es mit dem INOUT-Schlüsselwort deklariert wird. Argumente, die an eine Funktion übergebenen werden, die mit dem INOUT-Schlüsselwort gekennzeichnet sind, werden bis zur Rückgabe der Funktion als Kopien des Originals angesehen und zurückkopiert. Hier ist ein Beispiel für die Verwendung von INOUT:


```
void Increment_ByVal(inout float A, inout float B) 
{ 
    A++; B++;
}
```



Diese Funktion erhöht die Werte in A und B und gibt Sie zurück.

Der Funktions Rumpf ist der gesamte Code nach der Funktionsdeklaration.


```
float4 VertexShader_Tutorial_1(float4 inPos : POSITION ) : POSITION
{
    return mul(inPos, WorldViewProj );
};
```



Der Text besteht aus Anweisungen, die von geschweiften Klammern eingeschlossen werden. Der Funktions Rumpf implementiert die gesamte Funktionalität mithilfe von Variablen, Literalen, Ausdrücken und Anweisungen.

Der Shader-Text hat zwei Dinge: er führt eine Matrix Multiplikation aus und gibt ein float4-Ergebnis zurück. Die Matrix Multiplikation erfolgt mit der [**mul-Funktion (DirectX HLSL)**](dx-graphics-hlsl-mul.md) , die eine 4 x 4-Matrix Multiplikation durchführt. **mul (DirectX HLSL)** wird als intrinsische Funktion bezeichnet, da Sie bereits in die HLSL-Bibliotheks Bibliothek integriert ist. Intrinsische Funktionen werden im nächsten Abschnitt ausführlicher behandelt.

Die Matrix Multiplikation kombiniert eine Eingabe Vektor-POS und eine zusammengesetzte Matrix worldviewproj. Das Ergebnis sind Positionsdaten, die in den Bildschirmbereich transformiert werden. Dies ist die minimale Vertex-Shader-Verarbeitung, die wir durchführen können. Wenn wir anstelle eines Scheitelpunkt-Shaders die Pipeline mit fester Funktionsweise verwenden, können die Scheitelpunkt Daten nach dieser Transformation gezeichnet werden.

Die letzte Anweisung in einem Funktions Text ist eine Return-Anweisung. Genau wie bei C gibt diese Anweisung die Steuerung von der-Funktion an die-Anweisung zurück, die die Funktion aufgerufen hat.

Funktions Rückgabe Typen können beliebige einfache Datentypen sein, die in HLSL definiert sind, einschließlich bool, int half, float und Double. Rückgabe Typen können einer der komplexen Datentypen sein, z. b. Vektoren und Matrizen. HLSL-Typen, die auf-Objekte verweisen, können nicht als Rückgabe Typen verwendet werden. Dies schließt Pixelshader, Vertexshader, Texture und Sampler ein.

Im folgenden finden Sie ein Beispiel für eine Funktion, die eine-Struktur für einen Rückgabetyp verwendet.


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



Der float4-Rückgabetyp wurde durch die Struktur vs \_ Output ersetzt, die jetzt einen einzelnen float4-Member enthält.

Eine Return-Anweisung signalisiert das Ende einer Funktion. Dies ist die einfachste Return-Anweisung. Sie gibt die Steuerung von der Funktion an das aufrufenden Programm zurück. Es wird kein Wert zurückgegeben.


```
void main()
{
    return ;
}
```



Eine Return-Anweisung kann einen oder mehrere Werte zurückgeben. In diesem Beispiel wird ein Literalwert zurückgegeben:


```
float main( float input : COLOR0) : COLOR0
{
    return 0;
}
```



In diesem Beispiel wird das skalare Ergebnis eines Ausdrucks zurückgegeben:


```
return  light.enabled = true ;
```



Dieses Beispiel gibt eine float4 zurück, die aus einer lokalen Variablen und einem Literalwert erstellt wurde:


```
return  float4(color.rgb, 1) ;
```



In diesem Beispiel wird ein float4-Wert zurückgegeben, der aus dem von einer intrinsischen Funktion zurückgegebenen Ergebnis und einigen Literalwerten erstellt wird:


```
float4 func(float2 a: POSITION): COLOR
{
    return float4(sin(length(a) * 100.0) * 0.5 + 0.5, sin(a.y * 50.0), 0, 1);
}
```



Dieses Beispiel gibt eine-Struktur zurück, die mindestens ein-Element enthält:


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

Die meisten aktuellen Scheitelpunkt-und Pixel-Shader-Hardware ist darauf ausgelegt, einen Shader zeilenweise auszuführen und jede Anweisung einmal auszuführen. HLSL unterstützt die Fluss Steuerung, einschließlich statischer Verzweigung, Prädikat Anweisungen, statischer Schleifen, dynamischer Verzweigungen und dynamischer Schleifen.

Früher führte die Verwendung einer if-Anweisung zu einem assemblysprachshader-Code, der sowohl die if-Seite als auch die else-Seite des Code Flusses implementiert. Im folgenden finden Sie ein Beispiel für den in HLSL-Code, der für vs \_ 1 1 kompiliert wurde \_ :


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



Einige Hardware ermöglicht entweder statische oder dynamische Schleifen, aber die meisten erfordern eine lineare Ausführung. Bei den Modellen, die keine Schleifen unterstützen, muss für alle Schleifen ein Rollback ausgeführt werden. Ein Beispiel hierfür ist das Beispiel " [DepthOfField Sample](https://msdn.microsoft.com/library/Ee416592(v=VS.85).aspx) ", in dem auch für PS \_ 1 1-Shader nicht rollende Schleifen verwendet werden \_ .

HLSL bietet jetzt Unterstützung für die einzelnen Arten der Fluss Steuerung:

-   statische Verzweigung
-   Prädikat Anweisungen
-   statische Schleifen
-   dynamische Verzweigungen
-   dynamische Schleifen

Bei der statischen Verzweigung können Blöcke von shadercode basierend auf einer booleschen Shader-Konstante ein-oder ausgeschaltet werden. Dies ist eine bequeme Methode zum Aktivieren oder Deaktivieren von Codepfade basierend auf dem Typ des Objekts, das gerade gerendert wird. Zwischen zeichnen-aufrufen können Sie entscheiden, welche Features Sie mit dem aktuellen Shader unterstützen möchten, und dann die booleschen Flags festlegen, die zum Erreichen dieses Verhaltens erforderlich sind. Alle-Anweisungen, die von einer booleschen Konstante deaktiviert werden, werden während der shaderausführung übersprungen.

Die vertraulichste Verzweigungs Unterstützung ist die dynamische Verzweigung. Bei der dynamischen Verzweigung befindet sich die Vergleichs Bedingung in einer Variablen. Dies bedeutet, dass der Vergleich für jeden Scheitelpunkt oder jedes Pixel zur Laufzeit erfolgt (im Gegensatz zum Vergleich, der zur Kompilierzeit oder zwischen zwei zeichnen-aufrufen auftritt). Die Leistungseinbußen sind die Kosten der Verzweigung zuzüglich der Kosten für die Anweisungen auf der Seite der Verzweigung. Dynamische Verzweigungen werden in Shader-Modell 3 oder höher implementiert. Die Optimierung von Shadern, die mit diesen Modellen funktionieren, ähnelt der Optimierung von Code, der auf einer CPU ausgeführt wird.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Programmieranleitung für HLSL](dx-graphics-hlsl-pguide.md)
</dt> </dl>

 

 