---
title: Konfigurieren von Mischungs Funktionen
description: Mischungs Vorgänge werden für jede Pixel-Shader-Ausgabe (RGBA-Wert) ausgeführt, bevor der Ausgabewert in ein Renderziel geschrieben wird. Wenn die multisamplinggrad-Funktion aktiviert ist, erfolgt die Mischung in jedem Multisample. Andernfalls wird für jedes Pixel ein Mischungs Vorgang durchgeführt.
ms.assetid: f5c79baf-7bd3-4f58-abe7-8e96cd6be9d3
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 08acf1ea286b29a1cb96873bbfe170c6f38699f7
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "104993391"
---
# <a name="configuring-blending-functionality"></a>Konfigurieren von Mischungs Funktionen

Mischungs Vorgänge werden für jede Pixel-Shader-Ausgabe (RGBA-Wert) ausgeführt, bevor der Ausgabewert in ein Renderziel geschrieben wird. Wenn die multisamplinggrad-Funktion aktiviert ist, erfolgt die Mischung in jedem Multisample. Andernfalls wird für jedes Pixel ein Mischungs Vorgang durchgeführt.

-   [Erstellen des Blend-Status](#create-the-blend-state)
-   [Binden des Blend-Status](#bind-the-blend-state)
-   [Erweiterte Mischungs Themen](#advanced-blending-topics)
    -   [Alpha-zu-Abdeckung](#alpha-to-coverage)
    -   [Mischen von Pixel-Shader-Ausgaben](#blending-pixel-shader-outputs)
-   [Zugehörige Themen](#related-topics)

## <a name="create-the-blend-state"></a>Erstellen des Blend-Status

Der Blend-Status ist eine Auflistung von Zuständen, die zum Steuern von Mischungen verwendet werden. Diese Zustände (definiert in [**D3D11 \_ Blend \_ DESC1**](/windows/desktop/api/D3D11_1/ns-d3d11_1-cd3d11_blend_desc1)) werden zum Erstellen des Blend-Zustands Objekts durch Aufrufen von [**ID3D11Device1:: CreateBlendState1**](/windows/desktop/api/D3D11_1/nf-d3d11_1-id3d11device1-createblendstate1)verwendet.

Im folgenden finden Sie ein sehr einfaches Beispiel für die Erstellung von Blend-Zuständen, mit dem Alpha Blending deaktiviert und keine Pixel Maskierung pro Komponente verwendet wird.


```
ID3D11BlendState1* g_pBlendStateNoBlend = NULL;

D3D11_BLEND_DESC1 BlendState;
ZeroMemory(&BlendState, sizeof(D3D11_BLEND_DESC1));
BlendState.RenderTarget[0].BlendEnable = FALSE;
BlendState.RenderTarget[0].RenderTargetWriteMask = D3D11_COLOR_WRITE_ENABLE_ALL;
pd3dDevice->CreateBlendState1(&BlendState, &g_pBlendStateNoBlend);
```



Dieses Beispiel ähnelt dem [HLSLWithoutFX10](https://msdn.microsoft.com/library/Ee416414(v=VS.85).aspx)-Beispiel.

## <a name="bind-the-blend-state"></a>Binden des Blend-Status

Nachdem Sie das Blend-State-Objekt erstellt haben, binden Sie das Blend-State-Objekt an die Output-Merger-Phase durch Aufrufen von [**Verknüpfung id3d11devicecontext aus:: omsetblendstate**](/windows/desktop/api/D3D11/nf-d3d11-id3d11devicecontext-omsetblendstate).


```
float blendFactor[4] = { 0.0f, 0.0f, 0.0f, 0.0f };
UINT sampleMask   = 0xffffffff;

pd3dDevice->OMSetBlendState(g_pBlendStateNoBlend, blendFactor, sampleMask);
```



Diese API übernimmt drei Parameter: das Blend-State-Objekt, einen Kombination aus vier Komponenten und eine Beispiel Maske. Sie können **null** für das Blend-State-Objekt übergeben, um den standardmäßigen Blend-Status anzugeben, oder übergeben Sie ein Blend-State-Objekt. Wenn Sie das Blend-State-Objekt mit [**D3D11 \_ Blend \_ Blend \_ Factor**](/windows/desktop/api/D3D11/ne-d3d11-d3d11_blend) oder [**D3D11 \_ Blend \_ Inv \_ Blend \_ Factor**](/windows/desktop/api/D3D11/ne-d3d11-d3d11_blend)erstellt haben, können Sie einen Blend-Faktor übergeben, um Werte für den Pixelshader, das Renderziel oder beides zu modulieren. Wenn Sie das Blend-State-Objekt nicht mit dem **D3D11 \_ Blend- \_ \_ Faktor** oder **D3D11 Blend- \_ \_ Inv- \_ Blend \_**-Faktor erstellt haben, können Sie trotzdem einen nicht-NULL-Blend-Faktor übergeben, aber die Mischungs Phase verwendet nicht den Blend-Faktor. die Laufzeit speichert den Blend-Faktor, und Sie können später [**Verknüpfung id3d11devicecontext aus:**](/windows/desktop/api/D3D11/nf-d3d11-id3d11devicecontext-omgetblendstate) Wenn Sie **null** übergeben, verwendet die Common Language Runtime einen Blend-Faktor, der gleich {1, 1, 1, 1} ist, oder speichert diesen. Bei der Sample Mask handelt es sich um eine benutzerdefinierte Maske, die bestimmt, wie das vorhandene Renderziel vor dem Aktualisieren Stichproben wird. Die standardmäßige Samplings-Maske ist 0xFFFFFFFF und legt die Punkt Stichproben Entnahme fest.

In den meisten tiefen Puffer Schemas ist das Pixel, das der Kamera am nächsten ist, das, das gezeichnet wird. Beim [Einrichten des Status der tiefen Schablone](d3d10-graphics-programming-guide-depth-stencil.md)kann es sich bei dem **depthfunc** -Member der [**D3D11- \_ tiefen \_ Schablone \_**](/windows/desktop/api/D3D11/ns-d3d11-d3d11_depth_stencil_desc) um einen beliebigen [**D3D11- \_ Vergleichs \_ Func**](/windows/desktop/api/D3D11/ne-d3d11-d3d11_comparison_func)handeln. Normalerweise sollte **depthfunc** den **D3D11- \_ Vergleich \_ weniger** betragen, sodass die Pixel, die der Kamera am nächsten sind, die dahinter liegenden Pixel überschreiben werden. Abhängig von den Anforderungen Ihrer Anwendung können jedoch alle anderen Vergleichsfunktionen für den tiefen Test verwendet werden.

## <a name="advanced-blending-topics"></a>Erweiterte Mischungs Themen

-   [Alpha-zu-Abdeckung](#alpha-to-coverage)
-   [Mischen von Pixel-Shader-Ausgaben](#blending-pixel-shader-outputs)

### <a name="alpha-to-coverage"></a>Alpha-zu-Abdeckung

Alpha-zu-Abdeckung ist eine multisamplinggrad-Technik, die besonders nützlich für Situationen wie z. b. ein dichtes Laub ist, bei dem mehrere überlappende Polygone verwendet werden, um die Ränder innerhalb der Oberfläche zu definieren.

Sie können den **Alpha atocoverageenable** -Member von [**D3D11 \_ Blend \_ DESC1**](/windows/desktop/api/D3D11_1/ns-d3d11_1-cd3d11_blend_desc1) oder [**D3D11 \_ Blend \_ DESC**](/windows/desktop/api/D3D11/ns-d3d11-d3d11_blend_desc) verwenden, um zu wechseln, ob die Common Language Runtime die. a-Komponente (Alpha) des Ausgabe Registers [SV \_ target](/windows/desktop/direct3dhlsl/dx-graphics-hlsl-semantics)0 aus dem Pixel-Shader in eine n-Sample-Abdeckungs Maske (bei einem n-Sample- **renderTarget**) konvertiert. Die Laufzeit führt eine **and-** Operation dieser Maske mit der typischen Beispiel Abdeckung für das Pixel im primitiven (zusätzlich zur Beispiel Maske) aus, um zu bestimmen, welche Beispiele in allen aktiven **renderTarget** s aktualisiert werden müssen.

Wenn der Pixelshader die [SV- \_ Abdeckung](/windows/desktop/direct3dhlsl/dx-graphics-hlsl-semantics)ausgibt, deaktiviert die Runtime die Alpha-zu-Abdeckung.

> [!Note]  
> Bei Multisampling gibt die Laufzeit nur eine Abdeckung für alle **renderTarget** s frei. Die Tatsache, dass die Laufzeit liest und konvertiert. ein von der Ausgabe [SV \_ target](/windows/desktop/direct3dhlsl/dx-graphics-hlsl-semantics)0 in die Abdeckung, wenn **Alpha atocoverageenable** den Wert true hat, ändert sich nicht. ein Wert, der an den Blender bei **renderTarget** 0 übergeht (wenn ein **renderTarget** festgelegt wird). Im Allgemeinen haben Sie, wenn Sie Alpha-zu-Abdeckung aktivieren, nicht Einfluss darauf, wie alle Farb Ausgaben von Pixel-Shadern mit **renderTarget** s über die [Ausgabe-Fusion-Phase](d3d10-graphics-programming-guide-output-merger-stage.md) interagieren, mit der Ausnahme, dass die Laufzeit eine **and** -Operation der Abdeckungs Maske mit der Alpha-zu-Coverage-Maske ausführt. Die Alpha-zu-Abdeckung funktioniert unabhängig davon, ob die Laufzeit **renderTarget** mischen kann oder ob Sie Blending auf **renderTarget** verwenden.

 

Die Grafikhardware gibt nicht genau an, wie der Pixelshader [SV \_ target](/windows/desktop/direct3dhlsl/dx-graphics-hlsl-semantics)0. a (Alpha) in eine Abdeckungs Maske konvertiert wird, mit dem Unterschied, dass Alpha von 0 (oder weniger) keiner Abdeckung zugeordnet werden muss und Alpha von 1 (oder höher) der vollständigen Abdeckung zugeordnet werden muss (bevor die Laufzeit eine **and-** Operation mit tatsächlicher primitiver Abdeckung ausführt). Da Alpha zwischen 0 und 1 wechselt, sollte sich die resultierende Abdeckung in der Regel monoton steigern. Allerdings kann die Hardware eine Bereichs Auflösung durchführen, um eine bessere Quantisierung von Alpha Werten zu ermöglichen, die sich aus räumlichen Lösungen und Geräuschen zusammenbringt. Der Alpha-Wert NaN (keine Zahl) führt zu einer nichtabdeckung (null) Maske.

Die Alpha-zu-Abdeckung wird auch normalerweise für die Bildschirm-und türtransparenz verwendet, oder es werden ausführliche Silhouetten für anderweitig nicht transparente Sprites definiert.

### <a name="blending-pixel-shader-outputs"></a>Mischen von Pixel-Shader-Ausgaben

Diese Funktion ermöglicht der Ausgabe Zusammenführung, beide Pixel-Shader-Ausgaben gleichzeitig als Eingabe Quellen für einen Mischungs Vorgang mit dem einzelnen Renderziel an Slot 0 zu verwenden.

In diesem Beispiel werden zwei Ergebnisse angenommen und in einem einzigen Durchlauf kombiniert. dabei wird ein Array mit einer Multiplikation und der andere mit einem Add-in das Ziel gemischt:


```
SrcBlend = D3D11_BLEND_ONE;
DestBlend = D3D11_BLEND_SRC1_COLOR;
```



In diesem Beispiel wird die erste Pixel-Shader-Ausgabe als Quellfarbe und die zweite Ausgabe als Farbkomponenten-Blend Faktor pro Farbe konfiguriert.


```
SrcBlend = D3D11_BLEND_SRC1_COLOR;
DestBlend = D3D11_BLEND_INV_SRC1_COLOR;
```



In diesem Beispiel wird veranschaulicht, wie die Blend-Faktoren den Shader-wischen entsprechen müssen:


```
SrcFactor = D3D11_BLEND_SRC1_ALPHA;
DestFactor = D3D11_BLEND_SRC_COLOR;
OutputWriteMask[0] = .ra; // pseudocode for setting the mask at
                          // RenderTarget slot 0 to .ra
```



Die Blend-Faktoren und der Shader-Code implizieren miteinander, dass der Pixelshader mindestens o0. r und o1. a ausgeben muss. Zusätzliche Ausgabe Komponenten können vom Shader ausgegeben werden, werden jedoch ignoriert, aber weniger Komponenten würden nicht definierte Ergebnisse verursachen.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Ausgabe-Fusion-Phase](d3d10-graphics-programming-guide-output-merger-stage.md)
</dt> <dt>

[Pipeline Stufen (Direct3D 10)](/windows/desktop/direct3d10/d3d10-graphics-programming-guide-pipeline-stages)
</dt> </dl>

 

 