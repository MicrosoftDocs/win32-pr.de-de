---
title: Shadermodell 3 (HLSL-Referenz)
description: Vertex-Shader und Pixel-Shader werden gegenüber früheren Shaderversionen erheblich vereinfacht.
ms.assetid: 01ac85cb-b309-4169-acc2-320a929b65cb
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: c277723628d5337e41e5fbf83baa9fda8af16adf
ms.sourcegitcommit: b6fe9acffad983c14864b8fe0296f6025cb1f961
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/26/2021
ms.locfileid: "107993867"
---
# <a name="shader-model-3-hlsl-reference"></a>Shadermodell 3 (HLSL-Referenz)

Vertex-Shader und Pixel-Shader werden gegenüber früheren Shaderversionen erheblich vereinfacht. Wenn Sie Shader in Hardware implementieren, dürfen Sie nicht vs \_ 3 \_ 0 oder ps \_ 3 \_ 0 mit anderen Shaderversionen verwenden, und Sie dürfen keinen shader-Typ mit der festen Funktionspipeline verwenden. Diese Änderungen ermöglichen es, Treiber und die Runtime zu vereinfachen. Die einzige Ausnahme besteht darin, dass softwarebasierte Shader im Vergleich zu \_ \_ 3 0 Shadern mit einer beliebigen Pixelshaderversion verwendet werden können. Darüber hinaus kann der \_ \_ Vertex-Shader nur Ausgabesemantik verwenden, die mit FVF-Codes (Flexible Vertex Format) kompatibel ist, wenn Sie einen reinen Software- oder 3 0-Shader mit einer früheren Pixelshaderversion verwenden.

Die Semantik, die für Vertex-Shaderausgaben verwendet wird, muss für Pixel-Shadereingaben verwendet werden. Die Semantik wird verwendet, um die Vertex-Shaderausgaben den Pixel-Shadereingaben zuzuordnen, ähnlich wie die Vertexdeklaration den Vertex-Shader-Eingaberegistern und vorherigen Shadermodellen zugeordnet wird. Weitere Informationen finden Sie unter Match Semantics on vs 3.0 and ps 3.0 Shaders (Übereinstimmungssemantik für Shader der 3.0- und ps 3.0-Shader).

Es wurden zusätzliche Renderzustände im Umbruchmodus hinzugefügt, um die Möglichkeit zusätzlicher Texturkoordinaten in diesem neuen Schema abzudecken. Attribute mit D3DDECLUSAGE \_ TEXCOORD und Verwendungsindex von 0 bis 15 werden im Umbruchmodus interpoliert, wenn der entsprechende [**D3DRS \_ WRAP \***](/windows/desktop/direct3d9/d3drenderstatetype) festgelegt ist.

-   [Features von Vertex-Shadermodell 3](#vertex-shader-model-3-features)
-   [Features des Pixelshadermodells 3](#pixel-shader-model-3-features)
-   [Match Semantics on vs \_ 3 \_ 0 and ps \_ 3 \_ 0 Shader](/windows)
-   [Änderungen am Modus "Verzweigungs-, Tiefen- und Schattierungsmodus"](#fog-depth-and-shading-mode-changes)
-   [Gleitkomma- und Ganzzahlkonvertierungen](#floating-point-and-integer-conversions)
-   [Angeben der vollständigen oder teilweisen Genauigkeit](#specifying-full-or-partial-precision)
-   [Softwarevertex- und Pixel-Shader](#software-vertex-and-pixel-shaders)

## <a name="vertex-shader-model-3-features"></a>Vertex-Shadermodell 3-Features

Die Ausgaberegistertypen des Vertex-Shaders wurden in zwölf Register reduziert (siehe [Ausgaberegister](dx9-graphics-reference-asm-vs-registers-output.md)). Jedes verwendete Register muss mithilfe der [dcl-Anweisung](dcl-usage---ps.md) und einer Semantik deklariert werden (z. B. dcl \_ color0 o0.xyzw).

Das 3 \_ 0-Vertex-Shadermodell (im Vergleich zu 3 0) erweitert die Features von vs. 2 0 mit einer leistungsfähigeren Registerindizierung, einer Reihe vereinfachter Ausgaberegister, der Möglichkeit, eine Textur in einem \_ \_ \_ Vertex-Shader zu beproben, und der Möglichkeit, die Rate zu steuern, mit der \_ Shadereingaben initialisiert werden.

### <a name="index-any-register"></a>Indizieren beliebiger Register

Alle Register ( [Eingaberegister](dx9-graphics-reference-asm-vs-registers-input.md) und [Ausgaberegister](dx9-graphics-reference-asm-vs-registers-output.md)) können mithilfe des Schleifenzählerregisters indiziert werden [(nur](dx9-graphics-reference-asm-vs-registers-loop-counter.md) konstante Register konnten in früheren Versionen indiziert werden).

Sie müssen Eingabe- und Ausgaberegister deklarieren, bevor Sie sie indizieren. Sie dürfen jedoch kein Ausgaberegister indizieren, das mit einer Semantik der Position oder Punktgröße deklariert wurde. Wenn die Indizierung verwendet wird, müssen die Position und die Psize-Semantik in den Registern o0 bzw. o1 deklariert werden.

Sie dürfen nur einen kontinuierlichen Bereich von Registern indizieren. Das heißt, Sie können nicht über Register hinweg indizieren, die nicht deklariert wurden. Diese Einschränkung kann zwar unwesentlich sein, ermöglicht aber die Hardwareoptimierung. Der Versuch, nicht zusammenhängende Register zu indizieren, führt zu nicht definierten Ergebnissen. Die Shaderüberprüfung erzwingt diese Einschränkung nicht.

### <a name="simplify-output-registers"></a>Vereinfachen von Ausgaberegistern

Alle verschiedenen Arten von Ausgaberegistern wurden in zwölf Ausgaberegister reduziert: 1 für Position, 2 für Farbe, 8 für Textur und 1 für Diess oder Punktgröße. Diese Register interpolieren alle Daten, die sie für den Pixel-Shader enthalten. Ausgaberegisterdeklarationen sind erforderlich, und jedem Register wird Semantik zugewiesen.

Die Register können wie folgt aufgeschlüsselt werden:

-   Mindestens ein Register muss als Positionsregister mit vier Komponenten deklariert werden. Dies ist das einzige Vertex-Shaderregister, das erforderlich ist.
-   Die ersten zehn Register, die von einem Shader genutzt werden, können maximal vier Komponenten (xyzw) verwenden.
-   Das letzte (oder zwölfte) Register darf nur einen Skalar (z. B. punktgröße) enthalten.

Eine Liste der Register finden Sie unter [Register – vs \_ 3 \_ 0](dx9-graphics-reference-asm-vs-registers-vs-3-0.md).

### <a name="texture-sample-in-a-vertex-shader"></a>Texturbeispiel in einem Vertex-Shader

Vertex-Shader 3 \_ 0 unterstützt die Textursuche im Vertex-Shader mithilfe von [Texldl im Vergleich zu](texldl---vs.md).

## <a name="pixel-shader-model-3-features"></a>Features des Pixelshadermodells 3

Die Farb- und Texturregister des Pixelshader wurden in zehn Eingaberegister reduziert (siehe [Eingaberegistertypen](dx9-graphics-reference-asm-ps-registers-ps-3-0.md)). Das Gesichtsregister ist ein Gleitkomma-Skalarregister. Nur das Vorzeichen dieses Registers ist gültig. Wenn das Vorzeichen negativ ist, ist der Grundtyp ein Rückwand. Dies kann z. B. in einem Pixel-Shader verwendet werden, um eine zweiseitige Beleuchtung zu erzielen. Das Positionsregister verweist auf die aktuellen Pixel (x,y).

Die Shaderkonstantenregister können wie hier dargestellt festgelegt werden:

-   [**SetPixelShaderConstantB**](/windows/desktop/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-setpixelshaderconstantb)
-   [**SetPixelShaderConstantI**](/windows/desktop/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-setpixelshaderconstanti)
-   [**SetPixelShaderConstantF**](/windows/desktop/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-setpixelshaderconstantf)

## <a name="match-semantics-on-vs_3_0-and-ps_3_0-shaders"></a>Match Semantics on vs \_ 3 \_ 0 and ps \_ 3 \_ 0 Shader

Es gibt einige Einschränkungen für die semantische Verwendung mit gegenüber \_ \_ 3 0 und ps \_ 3 \_ 0. Im Allgemeinen müssen Sie vorsichtig sein, wenn Sie eine Semantik für eine Shadereingabe verwenden, die einer in einer Shaderausgabe verwendeten Semantik entspricht.

Dieser Pixelshader packt beispielsweise mehrere Namen in ein Register:


```
ps_3_0 
dcl_texcoord0 v0.x 
dcl_texcoord1 v0.yz // Valid to pack multiple names into one register 
dcl_texcoord2_centroid v1.w
...
```



Jedes Register hat eine andere Semantik. Beachten Sie, dass Sie auch v0.x und v0.yz mit unterschiedlicher (mehrfacher) Semantik benennen können, da die Schreibmaske verwendet wird.

Angesichts des Pixels shaders kann der folgende und \_ der folgende \_ 3 0-Shader nicht mit ihm gekoppelt werden:


```
vs_3_0 
... 
dcl_texcoord0 o5.x 
dcl_texcoord1 o6.yzw 
...
```



Diese beiden Shader stehen in Konflikt mit der Verwendung der [**Semantik D3DDECLUSAGE \_ TEXCOORD0**](/windows/desktop/direct3d9/d3ddeclusage) und **D3DDECLUSAGE \_ TEXCOORD1.**

Schreiben Sie den Vertex-Shader wie diesen um, um die semantische Kollision zu vermeiden:


```
vs_3_0 
... 
dcl_texcoord2 o3 
dcl_texcoord3 o9 
...
```



Ebenso kann ein semantischer Name, der in verschiedenen Eingaberegistern im Pixel-Shader deklariert ist (v0 und v1 im Pixel-Shader), nicht in einem einzelnen Ausgaberegister in diesem Vertex-Shader verwendet werden. Dieser Vertex-Shader kann beispielsweise nicht mit dem Pixel-Shader gekoppelt werden, da D3DDECLUSAGE TEXCOORD1 sowohl für Pixel-Shadereingaberegister (v0, v1) als auch für das \_ Vertex-Shader-Ausgaberegister o3 verwendet wird.


```
vs_3_0 
... 
dcl_texcoord0 o3.x 
dcl_texcoord1 o3.yz 

dcl_texcoord2 o3.w // BAD! Would be valid if this were not o3 
dcl_texcoord3 o9 ... 
```



Andererseits kann dieser Vertex-Shader nicht mit dem Pixel-Shader gekoppelt werden, da die Ausgabemaske für einen Parameter mit einer bestimmten Semantik nicht die vom Pixel-Shader angeforderten Daten enthält:


```
vs_3_0 
... 
dcl_texcoord0 o5.x 
dcl_texcoord1 o5.yzw 
dcl_texcoord2 o7.yz // BAD! Would be valid if w were included 
dcl_texcoord3 o9 
... 
```



Dieser Vertex-Shader stellt keine Ausgabe mit einem der vom Pixel-Shader angeforderten semantischen Namen zur Verfügung, sodass die Shaderkopplung ungültig ist:


```
vs_3_0 
... 
dcl_texcoord0 o5.x 
dcl_texcoord1 o5.yzw 
dcl_texcoord3 o9 
// The pixel shader wants texcoord2, with a w component, 
// but it isn't output by this vertex shader at all! 
... 
```



## <a name="fog-depth-and-shading-mode-changes"></a>Änderungen im Modus "Verschatten", "Tiefe" und "Schattierung"

Wenn D3DRS SHADEMODE während der Clipping- und Dreiecksrasterung für flache Schattierung festgelegt ist, werden Attribute mit \_ D3DDECLUSAGE COLOR als flach schattiert \_ interpoliert. Wenn Komponenten eines Registers mit einer Farbsemantik deklariert werden, andere Komponenten desselben Registers jedoch eine andere Semantik erhalten, ist die flache Schattierungsinterpolation (linear im Vergleich zu flach) für die Komponenten in diesem Register ohne Farbsemantik nicht definiert.

Wenn ein Rendern von 3 0 und ps 3 0 gewünscht ist, müssen \_ \_ \_ \_ Shader 3 0 und 3 0 -Shader Eine-0-Shader implementieren. Außerhalb der Shader werden keine Berechnungsberechnungen durchgeführt. Im Vergleich zu 3 0 gibt es kein Register für 3 \_ \_ 0, und es wurden zusätzliche Semantiken wie D3DDECLUSAGE \_ PIXELS (für berechnete Blendfaktor pro Scheitelpunkt) und D3DDECLUSAGE \_ DEPTH (für die Übergabe eines Tiefenwerts an den Pixel-Shader zum Berechnen des Mischungsfaktors für Denkelemente) hinzugefügt.

Der Texturphasenzustand D3DTSS \_ TEXCOORDINDEX wird bei Verwendung des Pixelshaders 3.0 ignoriert.

Die folgenden Werte wurden hinzugefügt, um diese Änderungen zu berücksichtigen:


```
// Fog and Depth usages
D3DDECLUSAGE_FOG 
D3DDECLUSAGE_DEPTH 

// Additional wrap states for vs_3_0 attributes with D3DDECLUSAGE_TEXCOORD 
D3DRS_WRAP8 
D3DRS_WRAP9 
D3DRS_WRAP10 
D3DRS_WRAP11 
D3DRS_WRAP12 
D3DRS_WRAP13 
D3DRS_WRAP14 
D3DRS_WRAP15
```



## <a name="floating-point-and-integer-conversions"></a>Gleitkomma- und Ganzzahlkonvertierungen

Gleitkommamathematik erfolgt mit unterschiedlicher Genauigkeit und unterschiedlichen Bereichen (16-Bit, 24-Bit und 32-Bit) in verschiedenen Teilen der Pipeline. Ein Wert, der größer als der dynamische Bereich der Pipeline ist, die in diese Pipeline eintritt (z. B. wird eine 32-Bit-Floattexturzuordnung in eine 24-Bit-Floatpipeline in ps \_ 2 \_ 0 entnommen), erzeugt ein nicht definiertes Ergebnis. Für vorhersagbares Verhalten sollten Sie einen solchen Wert an den maximalen dynamischen Bereich anbinden.

Die Konvertierung von einem Gleitkommawert in eine ganze Zahl erfolgt an mehreren Stellen, z. B.:

-   Beim Auftreten einer [MOVA-Anweisung](mova---vs.md) im Vergleich zu einer -Anweisung.
-   Während der Texturadressierung.
-   Beim Schreiben in ein Nicht-Gleitkommarenderziel.

## <a name="specifying-full-or-partial-precision"></a>Angeben der vollständigen oder teilweisen Genauigkeit

Sowohl ps \_ 3 \_ 0 als auch ps \_ 2 \_ x bieten Unterstützung für zwei Genauigkeitsebenen:



| ps \_ 3 \_ 0 | ps \_ 2 \_ 0 | Precision         | Wert                |
|----------|----------|-------------------|----------------------|
| x        |          | Vollständig              | fp32 oder höher       |
| x        |          | Partielle Genauigkeit | fp16=s10e5           |
| x        | x        | Vollständig              | fp24=s16e7 oder höher |
| x        | x        | Partielle Genauigkeit | fp16=s10e5           |



 

ps \_ 3 \_ 0 unterstützt mehr Genauigkeit als ps \_ 2 \_ 0. Standardmäßig erfolgen alle Vorgänge auf der Ebene der vollständigen Genauigkeit.

Die partielle Genauigkeit (siehe Modifizierer für das [Pixel-Shaderregister)](dx9-graphics-reference-asm-ps-registers-modifiers.md)wird angefordert, indem der pp-Modifizierer zum Shadercode hinzugefügt wird (vorausgesetzt, die zugrunde liegende Implementierung \_ unterstützt ihn). Implementierungen können den Modifizierer immer ignorieren und die betroffenen Vorgänge mit voller Genauigkeit ausführen.

Der \_ pp-Modifizierer kann in zwei Kontexten auftreten:

-   In einer Texturkoordinatendeklaration, um Texturkoordinaten mit teilweiser Genauigkeit an den Pixel-Shader zu übergeben. Dies kann verwendet werden, wenn Texturkoordinaten Farbdaten an den Pixel-Shader weiterleiten, die in einigen Implementierungen möglicherweise schneller mit partieller Genauigkeit als mit vollständiger Genauigkeit sind.
-   Für jede Anweisung zum Anfordern der Verwendung von partieller Genauigkeit, einschließlich Anweisungen zum Laden von Texturen. Dies gibt an, dass die Implementierung die Anweisung mit teilweiser Genauigkeit ausführen und ein Ergebnis mit teilweiser Genauigkeit speichern darf. Ohne expliziten Modifizierer muss die Anweisung mit voller Genauigkeit ausgeführt werden (unabhängig von der Genauigkeit der Eingabeopernden).

Eine Anwendung entscheidet sich möglicherweise absichtlich dafür, genauigkeits- und leistungssenklich abzuhandeln. Es gibt mehrere Arten von Shadereingabedaten, die natürliche Kandidaten für die Verarbeitung mit teilweiser Genauigkeit sind:

-   Farb iteratoren werden durch Teilweisegenauigkeitswerte gut dargestellt.
-   Texturwerte aus den meisten Formaten können genau durch Teilweisegenauigkeitswerte dargestellt werden (Werte, die aus 32-Bit-Gleitkommaformattexturen entnommen wurden, sind eine offensichtliche Ausnahme).
-   Konstanten können entsprechend dem Shader durch eine teilweise Genauigkeitsdarstellung dargestellt werden.

In all diesen Fällen kann der Entwickler die partielle Genauigkeit angeben, um die Daten zu verarbeiten, da er weiß, dass keine Genauigkeit der Eingabedaten verloren geht. In einigen Fällen kann ein Shader erfordern, dass die internen Schritte einer Berechnung mit vollständiger Genauigkeit ausgeführt werden, auch wenn eingabe- und endgültige Ausgabewerte nicht mehr als partielle Genauigkeit haben.

## <a name="software-vertex-and-pixel-shaders"></a>Softwarevertex- und Pixel-Shader

Softwareimplementierungen (Laufzeit und Referenz für Vertex-Shader und Referenz für Pixel-Shader) von Shadern der Version 2 \_ 0 und höher haben eine gewisse Überprüfung gelockert. Dies ist für Debug- und Prototypzwecke nützlich. Die Anwendung gibt der Runtime/dem Assembler an, dass sie einen Teil der Validierung mithilfe des Flags sw im Assembler gelockert haben muss \_ (z. B. im Vergleich zu \_ 2 \_ SW). Ein Software-Shader funktioniert nicht mit Hardware.

Vs \_ 2 \_ sw ist ein Ausgleich für die maximalen Obergrenzen von vs \_ 2 \_ x; ebenso ist ps \_ 2 sw ein \_ Mäßigung für die maximalen Obergrenzen von ps \_ 2 \_ x. Insbesondere werden die folgenden Überprüfungen gelockert:



|                                            |                                      |                                                                                                                                   |
|--------------------------------------------|--------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------|
| Shadermodell                               | Resource                             | Begrenzung                                                                                                                             |
| vs \_ 2 \_ sw, vs \_ 3 \_ sw, ps \_ 2 \_ sw, ps \_ 3 \_ sw | Anweisungsanzahl                   | Unbegrenzt                                                                                                                         |
| vs \_ 2 \_ sw, vs \_ 3 \_ sw, ps \_ 2 \_ sw, ps \_ 3 \_ sw | Gleitkommakonstantenregister             | 8192                                                                                                                              |
| vs \_ 2 \_ sw, vs \_ 3 \_ sw, ps \_ 2 \_ sw, ps \_ 3 \_ sw | Integer Constant Registers           | 2048                                                                                                                              |
| vs \_ 2 \_ sw, vs \_ 3 \_ sw, ps \_ 2 \_ sw, ps \_ 3 \_ sw | Boolesche Konstantenregister           | 2048                                                                                                                              |
| ps \_ 2 \_ sw                                  | Abhängige Lesetiefe                 | Unbegrenzt                                                                                                                         |
| vs \_ 2 \_ sw                                  | Anweisungen und Bezeichnungen für die Flusssteuerung | Unbegrenzt                                                                                                                         |
| vs \_ 2 \_ sw, vs \_ 3 \_ sw, ps \_ 2 \_ sw, ps \_ 3 \_ sw | Start/Schritt/Anzahl der Schleifen               | Iterationsstart und Iterationsschrittgröße für Rep- und Schleifenanweisungen sind 32-Bit-Ganzzahlen mit Vorzeichen. Die Anzahl kann bis zu MAX \_ INT/64 sein. |
| vs \_ 2 \_ sw, vs \_ 3 \_ sw, ps \_ 2 \_ sw, ps \_ 3 \_ sw | Portgrenzwerte                          | Portgrenzwerte für alle Registerdateien werden gelockert.                                                                                   |
| vs \_ 3 \_ sw                                  | Anzahl von Interpolatoren              | 16 Ausgaberegister in im Vergleich \_ zu 3 \_ Sw.                                                                                                 |
| ps \_ 3 \_ sw                                  | Anzahl von Interpolatoren              | 14(16-2) Eingaberegister für ps \_ 3 \_ sw.                                                                                           |



 

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Shadermodell 3 (DirectX HLSL)](dx-graphics-hlsl-sm3.md)
</dt> </dl>

 

 
