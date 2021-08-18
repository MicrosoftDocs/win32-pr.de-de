---
description: Ausdrücke sind mathematische oder logische Anweisungen, die auf der rechten Seite eines Gleichheitszeichens verwendet werden. Es gibt viele Arten von Ausdrücken.
ms.assetid: 642aa188-5dd7-49fc-b6cc-845f8fc22530
title: Ausdrücke (Direct3D 9)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: daeffeb09a2c2f496f73d492581cb2b51ac2e518e176bbbc848889bef5716b25
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119985700"
---
# <a name="expressions-direct3d-9"></a>Ausdrücke (Direct3D 9)

Ausdrücke sind mathematische oder logische Anweisungen, die auf der rechten Seite eines Gleichheitszeichens verwendet werden. Es gibt viele Arten von Ausdrücken.

## <a name="expressions"></a>Ausdrücke

1.  Variablenverweis
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

    

    Die Skalarwerte müssen literale Skalarwerte sein.

    Die Anzahl der Initialisierer muss mit der Variablen (Status) auf der linken Seite des Gleichheitszeichens kompatibel sein.

6.  OR-Ausdruck

    ```
    token [ | token ... ]
    ```

    

    Die Token müssen mit der Variablen (Status) auf der linken Seite des Gleichheitszeichens kompatibel sein.

    Bei den Token wird die Groß-/Kleinschreibung nicht beachtet.

7.  NULL

    ```
    NULL
    ```

    

    NULL kann nur einem Shader, Sampler oder Texturobjekt zugewiesen werden.

8.  Assemblyblock

    ```
    asm { code }
    ```

    

    PS-Assemblyblöcke müssen dem PIXELSHADER-Zustand zugewiesen werden.

    VS-Assemblyblöcke müssen dem VERTEXSHADER-Zustand zugewiesen werden.

9.  Sampler-Zustandsblock

    ```
    sampler_state { [ state = expression ; [ state = ... ] ] }
    ```

    

    Samplerzustandsblöcke sind Sequenzen von nicht indizierten Samplerphasenzustands- oder Texturzuweisungen.

    Samplerzustandsblöcke müssen dem SAMPLER-Effektzustand zugewiesen werden.

10. Zustandsblock "Effekt"

    ```
    stateblock_state { [ state [ [index] ] = expression; 
        [ state [ [index] ] = ... ] ] }
    ```

    

    Zustandsblöcke sind Sequenzen des allgemeinen Zustands. Zustandsblöcke können geschachtelt werden, dürfen jedoch keine Zirkelverweise enthalten.

    Zustandsblöcke müssen dem StateBLOCK-Effektzustand zugewiesen werden.

11. HLSL Compile

    ```
    compile target entrypoint ( [ arguments ] )
    ```

    

    Der Vertex-Shader im Vergleich zum Ziel m n gibt die Version des \_ \_ Vertex-Shaders D3DVS \_ VERSION(m, n) an. Der Pixel-Shader ps m n target gibt die Version des \_ \_ D3DPS-Pixelshader \_ (m, n) an.

    Vertexshader-Kompilierungsausdrücke auf hoher Ebene können nur dem VERTEXSHADER-Effektzustand zugewiesen werden. Ausdrücke für die Sprachkompilierung auf hoher Ebene des Pixelshaders können nur dem Pixelshader-Effektzustand zugewiesen werden.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Effektformat](dx9-graphics-reference-effects-file-format.md)
</dt> </dl>

 

 



