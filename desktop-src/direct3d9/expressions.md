---
description: Ausdrücke sind mathematische oder logische Anweisungen, die auf der rechten Seite eines Gleichheitszeichens verwendet werden. Es gibt viele Arten von Ausdrücken.
ms.assetid: 642aa188-5dd7-49fc-b6cc-845f8fc22530
title: Ausdrücke (Direct3D 9)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3aa574069094853eb506f7a1b38cdb6cd4379d3b
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/06/2021
ms.locfileid: "106342541"
---
# <a name="expressions-direct3d-9"></a>Ausdrücke (Direct3D 9)

Ausdrücke sind mathematische oder logische Anweisungen, die auf der rechten Seite eines Gleichheitszeichens verwendet werden. Es gibt viele Arten von Ausdrücken.

## <a name="expressions"></a>Ausdrücke

1.  Variablen Verweis
    ```
    ( variable ) or<variable >
    ```

    

2.  Numerischer Skalar
    ```
    scalar 
    ```

    

3.  Numerischer Ausdruck

    ```
    ( numeric expression )
    ```

    

    Alle standardmäßigen numerischen HLL-Ausdrücke werden hier unterstützt.

4.  Konstruktor
    ```
    type ( constructor arguments )
    ```

    

5.  Liste der Initialisierer

    ```
    { scalar value [, scalar value ...  ] }
    
    ```

    

    Die skalare müssen literalskalare Werte sein.

    Die Anzahl der Initialisierer muss mit der Variablen (State) auf der linken Seite des Gleichheitszeichens kompatibel sein.

6.  OR-Ausdruck

    ```
    token [ | token ... ]
    ```

    

    Die Token müssen mit der Variablen (State) auf der linken Seite des Gleichheitszeichens kompatibel sein.

    Beim Token wird die Groß-/Kleinschreibung nicht beachtet.

7.  NULL

    ```
    NULL
    ```

    

    NULL kann nur einem Shader, einem Sampler oder einem Textur Objekt zugewiesen werden.

8.  Assemblyblock

    ```
    asm { code }
    ```

    

    PS-assemblyblöcke müssen dem Pixelshader-Zustand zugewiesen werden.

    VS-assemblyblöcke müssen dem Vertexshader-Zustand zugewiesen werden.

9.  Sampler-Zustands Block

    ```
    sampler_state { [ state = expression ; [ state = ... ] ] }
    ```

    

    Samplerstatusblöcke sind Sequenzen von nicht indizierten samplingstatus-oder Textur Zuweisungen.

    Samplerstatusblöcke müssen dem samplereffekts-Zustand zugewiesen werden.

10. Zustands Block des Effekt Zustands

    ```
    stateblock_state { [ state [ [index] ] = expression; 
        [ state [ [index] ] = ... ] ] }
    ```

    

    Zustands Blöcke sind Sequenzen des allgemeinen Zustands. Zustands Blöcke können eingebettet werden, aber keine Zirkel Verweise enthalten.

    Zustands Blöcke müssen dem Status des stateblock-Effekts zugewiesen werden.

11. HLSL-Kompilierung

    ```
    compile target entrypoint ( [ arguments ] )
    ```

    

    Der Vertex-Shader im Vergleich zu \_ m \_ n-Ziel gibt die \_ Vertexshader-Version von D3DVS Version (m, n) an. Das Pixel-Shader PS \_ m \_ n-Ziel gibt die Pixel- \_ Shader-Version von D3DPS Version (m, n) an.

    Die sprach Kompilierungs Ausdrücke auf hoher Ebene des Vertex-Shaders können nur dem Vertexshader-Effekt Zustand zugewiesen werden. Der Pixel-Shader auf hoher Ebene kompilierte sprach Kompilierungs Ausdrücke können nur dem Pixelshader-Effekt Zustand zugewiesen werden.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Effekt Format](dx9-graphics-reference-effects-file-format.md)
</dt> </dl>

 

 



