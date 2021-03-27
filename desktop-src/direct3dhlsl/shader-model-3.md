---
title: Shader-Modell 3 (HLSL-Referenz)
description: Vertex-Shader und Pixel-Shader werden aus früheren shaderversionen erheblich vereinfacht.
ms.assetid: 01ac85cb-b309-4169-acc2-320a929b65cb
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: c3517266ace77b9235604770d9b42d10cd80e2d5
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "104390500"
---
# <a name="shader-model-3-hlsl-reference"></a>Shader-Modell 3 (HLSL-Referenz)

Vertex-Shader und Pixel-Shader werden aus früheren shaderversionen erheblich vereinfacht. Wenn Sie Shader in Hardware implementieren, dürfen Sie vs \_ 3 \_ 0 oder PS \_ 3 \_ 0 nicht mit anderen shaderversionen verwenden, und Sie dürfen keinen shadertyp mit der Fixed-Funktions Pipeline verwenden. Diese Änderungen ermöglichen es, Treiber und die Laufzeit zu vereinfachen. Die einzige Ausnahme besteht darin, dass nur-Software-oder \_ 3- \_ 0-Shader mit jeder Pixel-Shader-Version verwendet werden können. Wenn Sie einen reinen Software-vs \_ 3 \_ 0-Shader mit einer früheren Pixel-Shader-Version verwenden, kann der Vertex-Shader außerdem nur Ausgabe Semantik verwenden, die mit flexiblen Scheitelpunkt Formaten (FVF) kompatibel ist.

Die für Vertex-Shader-Ausgaben verwendete Semantik muss für Pixel-shadereingaben verwendet werden. Die Semantik wird verwendet, um die Vertex-shaderausgaben den Pixel-shadereingaben zuzuordnen, ähnlich wie die Vertex-Deklaration den Vertex-Shader-Eingabe Registern und früheren shadermodellen zugeordnet wird. Weitere Informationen finden Sie unter Match Semantik on vs 3,0 and PS 3,0 Shaders.

Zusätzliche Rendermodus-renderzustände wurden hinzugefügt, um die Möglichkeit zusätzlicher Texturkoordinaten in diesem neuen Schema abzudecken. Attribute mit D3DDECLUSAGE \_ texcoord und der Verwendungs Index von 0 bis 15 werden im Umbruch Modus interpoliert, wenn der entsprechende [**D3DRS \_ Wrap \***](/windows/desktop/direct3d9/d3drenderstatetype) festgelegt wird.

-   [Vertex-Shader Model 3-Features](#vertex-shader-model-3-features)
-   [Pixel Shader Model 3-Features](#pixel-shader-model-3-features)
-   [Übereinstimmungs Semantik für vs \_ 3 \_ 0-und PS \_ 3 \_ 0-Shader](/windows)
-   [Änderungen bei Nebel, Tiefe und Schattierungs Modus](#fog-depth-and-shading-mode-changes)
-   [Gleit Komma-und Integer-Konvertierungen](#floating-point-and-integer-conversions)
-   [Angeben der vollständigen oder partiellen Genauigkeit](#specifying-full-or-partial-precision)
-   [Software Scheitelpunkt und Pixel-Shader](#software-vertex-and-pixel-shaders)

## <a name="vertex-shader-model-3-features"></a>Vertex-Shader Model 3-Features

Die Vertex-Shader-Ausgabe Registrierungs Typen wurden in zwölf Register (siehe [Ausgabe Register](dx9-graphics-reference-asm-vs-registers-output.md)) reduziert. Jedes verwendete Register muss mithilfe der [DCL](dcl-usage---ps.md) -Anweisung und einer Semantik (z. b. dcl \_ color0 o0. xyzw) deklariert werden.

Das 3 \_ 0-Vertex-Shader-Modell (vs \_ 3 \_ 0) erweitert die Features von vs \_ 2 \_ 0 mit einer leistungsfähigeren Registrierungs Indizierung, einer Reihe von vereinfachten Ausgabe Registern, der Möglichkeit, eine Textur in einem Vertex-Shader zu modellieren, sowie der Möglichkeit, die Rate zu steuern, mit der shadereingaben initialisiert werden.

### <a name="index-any-register"></a>Index beliebiger Register

Alle Register ( [Eingabe Register](dx9-graphics-reference-asm-vs-registers-input.md) und [Ausgabe Register](dx9-graphics-reference-asm-vs-registers-output.md)) können mithilfe des [Schleifen Leistungs Zählers](dx9-graphics-reference-asm-vs-registers-loop-counter.md) indiziert werden (in früheren Versionen konnten nur konstante Register indiziert werden.)

Vor der Indizierung müssen Sie die Eingabe-und Ausgabe Register deklarieren. Allerdings können Sie keine Ausgabe Register indizieren, die mit einer Semantik der Positions-oder Punktgröße deklariert wurden. Tatsächlich muss die Position und die Psize-Semantik in den o0-und O1-Registern deklariert werden, wenn die Indizierung verwendet wird.

Sie können nur einen kontinuierlichen Bereich von Registern indizieren. Das heißt, Sie können nicht über Register hinweg indizieren, die nicht deklariert wurden. Diese Einschränkung kann zwar unpraktisch sein, Sie ermöglicht jedoch eine Hardware Optimierung. Wenn Sie versuchen, über nicht zusammenhängende Register zu indizieren, werden nicht definierte Ergebnisse erzeugt. Die Shader-Überprüfung erzwingt diese Einschränkung nicht.

### <a name="simplify-output-registers"></a>Vereinfachen von Ausgabe Registern

Alle verschiedenen Typen von Ausgabe Registern wurden in zwölf Ausgabe Register reduziert: 1 für Position, 2 für Farbe, 8 für Textur und 1 für Nebel oder Punktgröße. Diese Register interpolieren alle Daten, die Sie für den Pixelshader enthalten. Ausgabe Register Deklarationen sind erforderlich, und die Semantik wird jedem Register zugewiesen.

Die Register können wie folgt aufgegliedert werden:

-   Mindestens ein Register muss als ein vier-Komponenten-Positions Register deklariert werden. Dies ist das einzige erforderliche Vertex-Shader-Register.
-   Die ersten zehn von einem Shader genutzten Register können maximal vier Komponenten (xyzw) verwenden.
-   Das letzte (oder zwölfte) Register darf nur ein Skalar (z. b. die Punktgröße) enthalten.

Eine Auflistung der Register finden Sie unter [Registern-vs \_ 3 \_ 0](dx9-graphics-reference-asm-vs-registers-vs-3-0.md).

### <a name="texture-sample-in-a-vertex-shader"></a>Textur Beispiel in einem Scheitelpunkt-Shader

Vertex Shader 3 \_ 0 unterstützt Textur Suche im Vertex-Shader mithilfe von [texldl-vs](texldl---vs.md).

## <a name="pixel-shader-model-3-features"></a>Pixel Shader Model 3-Features

Die Pixel-Shader-Farbe und Textur Register wurden in zehn Eingabe Register reduziert (siehe [Eingabe Register Typen](dx9-graphics-reference-asm-ps-registers-ps-3-0.md)). Das Gesichts Register ist ein Gleit Komma-skalarregister. Nur das Vorzeichen dieses Registers ist gültig. Wenn das Vorzeichen negativ ist, ist der primitive ein Hintergrund. Dies kann beispielsweise in einem Pixelshader verwendet werden, um eine zweiseitige Beleuchtung zu erzielen. Das Positions Register verweist auf die aktuellen (x, y) Pixel.

Die Shader-Konstanten Register können mithilfe von festgelegt werden:

-   [**Setpixelshaderconstantb**](/windows/desktop/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-setpixelshaderconstantb)
-   [**Setpixelshaderconstanti**](/windows/desktop/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-setpixelshaderconstanti)
-   [**Setpixelshaderconstantf**](/windows/desktop/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-setpixelshaderconstantf)

## <a name="match-semantics-on-vs_3_0-and-ps_3_0-shaders"></a>Übereinstimmungs Semantik für vs \_ 3 \_ 0-und PS \_ 3 \_ 0-Shader

Es gibt einige Einschränkungen bei der semantischen Verwendung mit vs \_ 3 \_ 0 und PS \_ 3 \_ 0. Im Allgemeinen müssen Sie sorgfältig vorgehen, wenn Sie eine Semantik für eine Shadereingabe verwenden, die einer für eine shaderausgabe verwendeten Semantik entspricht.

Beispielsweise packt dieser Pixel-Shader mehrere Namen in ein Register:


```
ps_3_0 
dcl_texcoord0 v0.x 
dcl_texcoord1 v0.yz // Valid to pack multiple names into one register 
dcl_texcoord2_centroid v1.w
...
```



Jedes Register weist eine andere Semantik auf. Beachten Sie, dass Sie auch "v0. x" und "v0. YZ" mit einer anderen (mehrfachen) Semantik benennen können, weil die Schreib Maske verwendet wird.

Wenn der Pixelshader angegeben ist, kann der folgende vs \_ 3 \_ 0-Shader nicht mit ihm gekoppelt werden:


```
vs_3_0 
... 
dcl_texcoord0 o5.x 
dcl_texcoord1 o6.yzw 
...
```



Diese beiden Shader stehen in Konflikt mit der Verwendung der Semantik [**D3DDECLUSAGE \_ TEXCOORD0**](/windows/desktop/direct3d9/d3ddeclusage) und **D3DDECLUSAGE \_ TEXCOORD1** .

Schreiben Sie den Vertex-Shader wie folgt um, um die semantische Kollision zu vermeiden:


```
vs_3_0 
... 
dcl_texcoord2 o3 
dcl_texcoord3 o9 
...
```



Ebenso kann ein semantischer Name, der für verschiedene Eingabe Register im Pixelshader (V0 und v1 im Pixelshader) deklariert ist, nicht in einem einzelnen Ausgabe Register in diesem Vertex-Shader verwendet werden. Dieser Vertex-Shader kann z. b. nicht mit dem Pixelshader gekoppelt werden, da D3DDECLUSAGE \_ TEXCOORD1 sowohl für Pixel-Shader-Eingabe Register (v0, v1) als auch für das Vertex-Shader-Ausgabe Register (O3) verwendet wird.


```
vs_3_0 
... 
dcl_texcoord0 o3.x 
dcl_texcoord1 o3.yz 

dcl_texcoord2 o3.w // BAD! Would be valid if this were not o3 
dcl_texcoord3 o9 ... 
```



Der Vertex-Shader kann dagegen nicht mit dem Pixelshader kombiniert werden, da die Ausgabe Maske für einen Parameter mit einer gegebenen Semantik nicht die vom Pixelshader angeforderten Daten bereitstellt:


```
vs_3_0 
... 
dcl_texcoord0 o5.x 
dcl_texcoord1 o5.yzw 
dcl_texcoord2 o7.yz // BAD! Would be valid if w were included 
dcl_texcoord3 o9 
... 
```



Dieser Vertex-Shader stellt keine Ausgabe mit einem der vom Pixelshader angeforderten semantischen Namen bereit, sodass die Shader-Kopplung ungültig ist:


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



## <a name="fog-depth-and-shading-mode-changes"></a>Änderungen bei Nebel, Tiefe und Schattierungs Modus

Wenn D3DRS \_ SHADEMODE für die flache Schattierung während Clipping und Dreieck-rasterisierung festgelegt ist, werden Attribute mit D3DDECLUSAGE- \_ Farbe als flach schattiert interpoliert. Wenn alle Komponenten eines Registers mit einer Farb Semantik deklariert sind, aber andere Komponenten desselben Registers unterschiedliche Semantik aufweisen, ist die flache Schattierungs Interpolation (Linear und Flat) für die Komponenten in, die ohne Farb Semantik registriert werden, nicht definiert.

Wenn ein Nebel Rendering gewünscht ist, \_ müssen vs 3 \_ 0-und PS \_ 3 \_ 0-Shader Nebel implementieren. Außerhalb der Shader werden keine Nebel Berechnungen durchgeführt. In vs 3 0 gibt es kein Nebel Register \_ \_ , und zusätzliche Semantik D3DDECLUSAGE \_ Nebel (für die Berechnung pro Scheitelpunkt pro Scheitelpunkt) und die D3DDECLUSAGE- \_ Tiefe (für die Übergabe eines tiefen Werts an den Pixelshader zur Berechnung des Nebel Blend-Faktors) wurden hinzugefügt.

Textur Phasen Status D3DTSS \_ texcoordindex wird bei Verwendung von Pixel Shader 3,0 ignoriert.

Die folgenden Werte wurden hinzugefügt, um diese Änderungen zu unterstützen:


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



## <a name="floating-point-and-integer-conversions"></a>Gleit Komma-und Integer-Konvertierungen

Gleit Komma Berechnungen werden in verschiedenen Teilen der Pipeline mit unterschiedlichen Genauigkeit und Bereichen (16-Bit, 24-Bit und 32-Bit) ausgeführt. Ein Wert, der größer ist als der dynamische Bereich der Pipeline, der in diese Pipeline Eintritt (z. b. eine 32-Bit-Float-Textur Zuordnung wird in PS 2 0 in eine 24-Bit-Float-Pipeline entnommen), wird \_ \_ ein nicht definiertes Ergebnis erstellt. Für ein vorhersagbares Verhalten sollten Sie einen solchen Wert an den dynamischen Bereichs Wert binden.

Die Konvertierung von einem Gleit Komma Wert in eine Ganzzahl erfolgt an verschiedenen Stellen, z. b.:

-   Wenn eine " [MUVA-vs"-](mova---vs.md) Anweisung auftritt.
-   Während der Textur Adressierung.
-   Beim Schreiben in ein nicht Gleit Komma-Renderziel.

## <a name="specifying-full-or-partial-precision"></a>Angeben der vollständigen oder partiellen Genauigkeit

Sowohl PS \_ 3 \_ 0 als auch PS \_ 2 \_ x bieten Unterstützung für zwei Genauigkeits Stufen:



|          |          |                   |                      |
|----------|----------|-------------------|----------------------|
| PS \_ 3 \_ 0 | PS \_ 2 \_ 0 | Genauigkeit         | Wert                |
| x        |          | Vollständig              | FP32 oder höher       |
| x        |          | Partielle Genauigkeit | FP16 = s10e5           |
| x        | x        | Vollständig              | fp24 = s16e7 oder höher |
| x        | x        | Partielle Genauigkeit | FP16 = s10e5           |



 

PS \_ 3 \_ 0 unterstützt mehr Genauigkeit als PS \_ 2 \_ 0. Standardmäßig erfolgen alle Vorgänge auf der Ebene mit vollständiger Genauigkeit.

Die partielle Genauigkeit (Weitere Informationen finden Sie unter " [Pixel-Shader-registrierungsmodifizierer](dx9-graphics-reference-asm-ps-registers-modifiers.md)") wird durch Hinzufügen des \_ PP-Modifizierers zum Shader-Code angefordert Implementierungen können den-Modifizierer jederzeit ignorieren und die betroffenen Vorgänge mit vollständiger Genauigkeit ausführen.

Der \_ PP-Modifizierer kann in zwei Kontexten vorkommen:

-   In einer Texturkoordinaten Deklaration, um Texturkoordinaten mit partieller Genauigkeit an den Pixelshader zu übergeben. Dieser Wert kann verwendet werden, wenn die Textur Daten an den Pixelshader weiterleitet, was bei einigen Implementierungen mit einer partiellen Genauigkeit schneller ist als mit der vollständigen Genauigkeit.
-   Bei einer beliebigen Anweisung, um die Verwendung der partiellen Genauigkeit, einschließlich der Anweisungen zum Laden von Text, anzufordern. Dies gibt an, dass die Implementierung die Anweisung mit teilweiser Genauigkeit ausführen und ein Ergebnis mit teilweiser Genauigkeit speichern darf. Wenn kein expliziter Modifizierer vorhanden ist, muss die Anweisung mit vollständiger Genauigkeit (unabhängig von der Genauigkeit der Eingabe Operanden) ausgeführt werden.

Eine Anwendung kann sich bewusst entscheiden, dass die Genauigkeit der Leistung beeinträchtigt wird. Es gibt verschiedene Arten von shadereingabedaten, die natürliche Kandidaten für die Verarbeitung mit teilweiser Genauigkeit sind:

-   Farbiteratoren werden durch Werte mit partieller Genauigkeit gut dargestellt.
-   Textur Werte aus den meisten Formaten können durch partielle Genauigkeits Werte genau dargestellt werden (Werte, die von 32-Bit entnommen werden, und es handelt sich um eine offensichtliche Ausnahme).
-   Konstanten können entsprechend dem Shader durch eine Darstellung mit partieller Genauigkeit dargestellt werden.

In all diesen Fällen kann der Entwickler eine partielle Genauigkeit angeben, um die Daten zu verarbeiten. dabei ist zu erkennen, dass keine Genauigkeit der Eingabedaten verloren geht. In einigen Fällen erfordert ein Shader möglicherweise, dass die internen Schritte einer Berechnung mit vollständiger Genauigkeit durchgeführt werden, auch wenn Eingabe-und endgültige Ausgabewerte nicht mehr als partielle Genauigkeit aufweisen.

## <a name="software-vertex-and-pixel-shaders"></a>Software Scheitelpunkt und Pixel-Shader

Für Software Implementierungen (Laufzeit und Verweis für Vertex-Shader und Referenz für Pixel-Shader) der Versionen 2 \_ 0-Shader und höher wird die Validierung gelockert. Dies ist nützlich für das Debuggen und das Prototypen. Die Anwendung zeigt der Laufzeit/dem Assembler an, dass ein Teil der Validierung mit dem \_ SW-Flag im Assembler (z. b. vs \_ 2 \_ SW) gelockert werden muss. Ein Software-Shader funktioniert nicht mit Hardware.

vs \_ 2 \_ SW ist eine Lockerung der maximalen Anzahl von vs \_ 2 \_ x. gleichermaßen ist PS \_ 2 \_ SW eine Lockerung der maximalen Anzahl von PS \_ 2 \_ x. Insbesondere werden die folgenden Überprüfungen gelockert:



|                                            |                                      |                                                                                                                                   |
|--------------------------------------------|--------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------|
| Shadermodell                               | Resource                             | Begrenzung                                                                                                                             |
| vs \_ 2 \_ SW, vs \_ 3 \_ SW, PS \_ 2 \_ SW, PS \_ 3 \_ SW | Anweisungs Anzahl                   | Unbegrenzt                                                                                                                         |
| vs \_ 2 \_ SW, vs \_ 3 \_ SW, PS \_ 2 \_ SW, PS \_ 3 \_ SW | Float-Konstante Register             | 8192                                                                                                                              |
| vs \_ 2 \_ SW, vs \_ 3 \_ SW, PS \_ 2 \_ SW, PS \_ 3 \_ SW | Ganzzahlige Konstante Register           | 2048                                                                                                                              |
| vs \_ 2 \_ SW, vs \_ 3 \_ SW, PS \_ 2 \_ SW, PS \_ 3 \_ SW | Boolesche Konstante Register           | 2048                                                                                                                              |
| PS \_ 2 \_ SW                                  | Abhängige Lese Tiefe                 | Unbegrenzt                                                                                                                         |
| vs \_ 2 \_ SW                                  | Anweisungen und Bezeichnungen der Fluss Steuerung | Unbegrenzt                                                                                                                         |
| vs \_ 2 \_ SW, vs \_ 3 \_ SW, PS \_ 2 \_ SW, PS \_ 3 \_ SW | Schleifenstart/-Schritt/-Anzahl               | Die Iterations-und Iterations Schrittgröße für rep-und Loop-Anweisungen sind 32-Bit-Ganzzahlen mit Vorzeichen. "Count" kann bis Max \_ . int/64 betragen. |
| vs \_ 2 \_ SW, vs \_ 3 \_ SW, PS \_ 2 \_ SW, PS \_ 3 \_ SW | Port Limits                          | Die Port Limits für alle Register Dateien werden gelockert.                                                                                   |
| vs \_ 3- \_ SW                                  | Anzahl von Interpolatoren              | 16 Ausgabe Register in vs \_ 3 \_ SW.                                                                                                 |
| PS \_ 3 ( \_ SW)                                  | Anzahl von Interpolatoren              | 14 (16-2) Eingabe Register für PS \_ 3 \_ SW.                                                                                           |



 

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Shader-Modell 3 (DirectX HLSL)](dx-graphics-hlsl-sm3.md)
</dt> </dl>

 

 