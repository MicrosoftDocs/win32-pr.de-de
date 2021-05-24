---
title: Output-Merger Phase
description: Die Ausgabezusammenführungsphase (OM) generiert die endgültige gerenderte Pixelfarbe mithilfe einer Kombination aus Pipelinezustand, den von den Pixel-Shadern generierten Pixeldaten, dem Inhalt der Renderziele und dem Inhalt der Tiefen-/Schablonenpuffer.
ms.assetid: 8be68c15-2deb-4804-b683-30080a876189
keywords:
- Ausgabezusammenführungsphase (Direct3D 10)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c8de2851fdea3a22cc42033d2c13454be72ba8ab
ms.sourcegitcommit: ca37395fd832e798375e81142b97cffcffabf184
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 05/24/2021
ms.locfileid: "110335214"
---
# <a name="output-merger-stage"></a>Output-Merger Phase

Die Ausgabezusammenführungsphase (OM) generiert die endgültige gerenderte Pixelfarbe mithilfe einer Kombination aus Pipelinezustand, den von den Pixel-Shadern generierten Pixeldaten, dem Inhalt der Renderziele und dem Inhalt der Tiefen-/Schablonenpuffer. Die OM-Phase ist der letzte Schritt zum Bestimmen der sichtbaren Pixel (mit Tiefenschablonentests) und zum Mischen der endgültigen Pixelfarben.



Unterschiede zwischen Direct3D 9 und Direct3D 10:

- Direct3D 9 implementiert Alphatests (unter Verwendung des [Alphatestzustands](/windows/desktop/direct3d9/alpha-testing-state)), um zu steuern, ob ein Pixel in ein Ausgaberenderziel geschrieben wird.
- Direct3D 10 und höher implementiert keinen Alphatest (oder Alphatestzustand). Dies kann mit einem Pixel-Shader oder mit Tiefen-/Schablonenfunktionalität gesteuert werden.



 

## <a name="depth-stencil-testing-overview"></a>Übersicht über Depth-Stencil-Tests

Ein Tiefenschablonenpuffer, der als Texturressource erstellt wird, kann sowohl Tiefendaten als auch Schablonendaten enthalten. Die Tiefendaten werden verwendet, um zu bestimmen, welche Pixel der Kamera am nächsten liegen, und die Schablonendaten werden verwendet, um zu maskieren, welche Pixel aktualisiert werden können. Letztendlich werden sowohl die Daten der Tiefen- als auch der Schablonenwerte von der Ausgabezusammenführungsphase verwendet, um zu bestimmen, ob ein Pixel gezeichnet werden soll oder nicht. Das folgende Diagramm zeigt konzeptionell, wie Tiefenschablonentests durchgeführt werden.

![Diagramm der Funktionsweise von Tiefenschablonentests](images/d3d10-depth-stencil-test.png)

Informationen zum Konfigurieren von Tiefenschablonentests finden Sie unter [Konfigurieren Depth-Stencil Funktionalität.](d3d10-graphics-programming-guide-depth-stencil.md) Ein Tiefenschablonenobjekt kapselt den Tiefenschablonenzustand. Eine Anwendung kann den Tiefenschablonenzustand angeben, oder die OM-Phase verwendet Standardwerte. Blendingvorgänge werden pixelweise ausgeführt, wenn Multisampling deaktiviert ist. Wenn Multisampling aktiviert ist, erfolgt das Mischen pro Multisample.

Der Prozess der Verwendung des Tiefenpuffers, um zu bestimmen, welches Pixel gezeichnet werden soll, wird als Tiefenpufferung bezeichnet, auch als Z-Pufferung bezeichnet.

Sobald Die Tiefenwerte die Ausgabe-Merger-Phase erreichen (unabhängig davon, ob sie von interpolation oder von einem Pixel-Shader kommen), werden sie immer entsprechend dem Format/der Genauigkeit des Tiefenpuffers mitHilfe von Gleitkommaregeln an die Klammern z = min(Viewport.MaxDepth,max(Viewport.MinDepth,z)) klammern. Nach dem Anschließen wird der Tiefenwert (mit DepthFunc) mit dem vorhandenen Tiefenpufferwert verglichen. Wenn kein Tiefenpuffer gebunden ist, wird der Tiefentest immer bestanden.

Wenn keine Schablonenkomponente im Tiefenpufferformat oder kein Tiefenpuffer gebunden ist, wird der Schablonentest immer bestanden. Andernfalls bleibt die Funktionalität von Direct3D 9 unverändert.

Es kann immer nur ein Tiefen-/Schablonenpuffer aktiv sein. Jede gebundene Ressourcenansicht muss mit der Tiefen-/Schablonenansicht übereinstimmen (gleiche Größe und Größe). Dies bedeutet nicht, dass die Ressourcengröße übereinstimmen muss, sondern nur, dass die Ansichtsgröße übereinstimmen muss.

Weitere Informationen zu Tiefen-Schablonentests finden Sie im [Tutorial 14](https://msdn.microsoft.com/library/Ee416550(v=VS.85).aspx).

## <a name="blending-overview"></a>Übersicht über Blending

Blending kombiniert einen oder mehrere Pixelwerte, um eine endgültige Pixelfarbe zu erstellen. Das folgende Diagramm zeigt den Prozess, der beim Mischen von Pixeldaten beteiligt ist.

![Diagramm der Funktionsweise des Mischens von Daten](images/d3d10-blend-state.png)

Konzeptionell können Sie dieses Flussdiagramm visualisieren, das zweimal in der Ausgabe-Merger-Phase implementiert wurde: Das erste kombiniert RGB-Daten, während ein zweites parallel Alphadaten kombiniert. Informationen zur Verwendung der API zum Erstellen und Festlegen des Überblendungszustands finden Sie unter [Configuring Blending Functionality (Konfigurieren der Blendingfunktionalität).](d3d10-graphics-programming-guide-blend-state.md)

Fixed-Function Blend kann unabhängig für jedes Renderziel aktiviert werden. Es gibt jedoch nur einen Satz von Blend-Steuerelementen, sodass die gleiche Mischung auf alle RenderTargets mit aktivierter Mischung angewendet wird. Blend-Werte (einschließlich BlendFactor) werden vor dem Mischen immer an den Bereich des Renderzielformats klammern. Die Klammer wird pro Renderziel unter Einhaltung des Renderzieltyps durchgeführt. Die einzige Ausnahme ist für die Formate float16, float11 oder float10, die nicht geklammert sind, sodass Überblendvorgänge für diese Formate mit mindestens gleicher Genauigkeit/gleichem Bereich wie das Ausgabeformat durchgeführt werden können. NaNs und signierte Nullen werden für alle Fälle (einschließlich 0,0 Überblendgewichtungen) propagiert.

Wenn Sie sRGB-Renderziele verwenden, konvertiert die Laufzeit die Renderzielfarbe in einen linearen Raum, bevor die Mischung ausgeführt wird. Die Runtime konvertiert den endgültigen kombinierten Wert wieder in den sRGB-Raum, bevor der Wert wieder im Renderziel speichert wird.

Unterschiede zwischen Direct3D 9 und Direct3D 10:

- In Direct3D 9 kann das Blending fester Funktionen unabhängig für jedes Renderziel aktiviert werden.
- In Direct3D 10 und höher gibt es eine Beschreibung des Blendzustands. daher kann ein Überblendungswert für alle Renderziele festgelegt werden.



 

### <a name="dual-source-color-blending"></a>Dual-Source Farbblending

Dieses Feature ermöglicht es der Ausgabe-Merger-Phase, gleichzeitig sowohl Pixelschattenausgabe (o0 und o1) als Eingaben für einen Blendingvorgang mit dem einzelnen Renderziel an Slot 0 zu verwenden. Gültige Überblendvorgänge sind: add, subtract und revsubtract. Gültige Blendoptionen für SrcBlend, DestBlend, SrcBlendAlpha oder DestBlendAlpha sind: **D3D11 \_ BLEND \_ SRC1 \_ COLOR,** **D3D11 \_ BLEND \_ INV \_ SRC1 \_ COLOR,** **D3D11 \_ BLEND \_ SRC1 \_ ALPHA,** **D3D11 \_ BLEND \_ INV \_ SRC1 \_ ALPHA**. Die Mischungsgleichung und die Ausgabe-Schreibmaske geben an, welche Komponenten der Pixel-Shader ausausgabet. Zusätzliche Komponenten werden ignoriert.

Das Schreiben in andere Pixel-Shader-Ausgaben (o2, o3 usw.) ist nicht definiert. Sie dürfen nicht in ein Renderziel schreiben, wenn es nicht an Slot 0 gebunden ist. Das Schreiben von oDepth ist beim Dual Source Color Blending gültig.

Beispiele finden Sie unter Blending pixel shader outputs (Mischen von [Pixel-Shader-Ausgaben).](d3d10-graphics-programming-guide-blend-state.md)

## <a name="multiple-rendertargets-overview"></a>Übersicht über mehrere RenderTargets

Ein Pixel-Shader kann verwendet werden, um auf mindestens acht separate Renderziele zu rendern, die alle denselben Typ aufweisen müssen (buffer, Texture1D, Texture1DArray und so weiter). Darüber hinaus müssen alle Renderziele in allen Dimensionen (Breite, Höhe, Tiefe, Arraygröße, Stichprobenanzahl) die gleiche Größe aufweisen. Jedes Renderziel kann ein anderes Datenformat aufweisen.

Sie können eine beliebige Kombination von Renderzielslots (bis zu 8) verwenden. Eine Ressourcenansicht kann jedoch nicht gleichzeitig an mehrere Renderzielslots gebunden werden. Eine Sicht kann wiederverwendet werden, solange die Ressourcen nicht gleichzeitig verwendet werden.

## <a name="output-write-mask-overview"></a>Übersicht über Output-Write Mask

Verwenden Sie eine Ausgabe-/Schreibmaske, um (pro Komponente) zu steuern, welche Daten in ein Renderziel geschrieben werden können.

## <a name="sample-mask-overview"></a>Übersicht über Beispielmasken

Eine Beispielmaske ist eine 32-Bit-Multisample-Abdeckungsmaske, die bestimmt, welche Stichproben in aktiven Renderzielen aktualisiert werden. Es ist nur eine Beispielmaske zulässig. Die Zuordnung von Bits in einer Beispielmaske zu den Beispielen in einer Ressource wird von einem Benutzer definiert. Für das n-Sample-Rendering werden die ersten n Bits (aus dem LSB) der Beispielmaske verwendet (32 Bits die maximale Anzahl von Bits).


## <a name="in-this-section"></a>In diesem Abschnitt



| Thema                                                                                                    | Beschreibung                                                                                                                                                                                                                                                      |
|----------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Konfigurieren Depth-Stencil Funktionalität](d3d10-graphics-programming-guide-depth-stencil.md)<br/> | In diesem Abschnitt werden die Schritte zum Einrichten des Tiefenschablonenpuffers und des Tiefenschablonenzustands für die Ausgabezusammenführungsphase beschrieben.<br/>                                                                                                                           |
| [Konfigurieren der Blendingfunktionalität](d3d10-graphics-programming-guide-blend-state.md)<br/>        | Blendingvorgänge werden für jede Pixel-Shaderausgabe (RGBA-Wert) ausgeführt, bevor der Ausgabewert in ein Renderziel geschrieben wird. Wenn Multisampling aktiviert ist, erfolgt das Mischen für jedes Multisample. Andernfalls wird das Mischen für jedes Pixel ausgeführt.<br/> |
| [Tiefenausrichtung](d3d10-graphics-programming-guide-output-merger-stage-depth-bias.md)<br/>             | Polygone, die im 3D-Raum koplanar sind, können so dargestellt werden, als wären sie nicht koplanar, indem sie jeweils eine Z-Voreingenommenheit (oder Tiefenabweichung) hinzufügen.<br/>                                                                                                              |



 

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Grafikpipeline](overviews-direct3d-11-graphics-pipeline.md)
</dt> <dt>

[Pipelinestufen (Direct3D 10)](/windows/desktop/direct3d10/d3d10-graphics-programming-guide-pipeline-stages)
</dt> </dl>

 

