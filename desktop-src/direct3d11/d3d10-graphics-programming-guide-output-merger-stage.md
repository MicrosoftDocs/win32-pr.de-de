---
title: Output-Merger Phase
description: Die Ausgabezusammenführungsphase (OM) generiert die endgültige gerenderte Pixelfarbe mithilfe einer Kombination aus Pipelinezustand, den von den Pixel-Shadern generierten Pixeldaten, dem Inhalt der Renderziele und dem Inhalt der Tiefen-/Schablonenpuffer.
ms.assetid: 8be68c15-2deb-4804-b683-30080a876189
keywords:
- Ausgabezusammenführungsphase (Direct3D 10)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c56566e6c193af2ea41c2553d4dffe9a6a9b673f53e21dba9b75b3dfb3f0cd2b
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119752420"
---
# <a name="output-merger-stage"></a>Output-Merger Phase

Die Ausgabezusammenführungsphase (OM) generiert die endgültige gerenderte Pixelfarbe mithilfe einer Kombination aus Pipelinezustand, den von den Pixel-Shadern generierten Pixeldaten, dem Inhalt der Renderziele und dem Inhalt der Tiefen-/Schablonenpuffer. Die OM-Phase ist der letzte Schritt, um zu bestimmen, welche Pixel sichtbar sind (mit Tiefenschablonentests) und die endgültigen Pixelfarben zu mischen.



Unterschiede zwischen Direct3D 9 und Direct3D 10:

- Direct3D 9 implementiert Alphatests (unter Verwendung des [Alphatestzustands](/windows/desktop/direct3d9/alpha-testing-state)), um zu steuern, ob ein Pixel in ein Ausgaberenderziel geschrieben wird.
- Direct3D 10 und höher implementiert keinen Alphatest (oder Alphatestzustand). Dies kann mit einem Pixel-Shader oder mit Tiefen-/Schablonenfunktionalität gesteuert werden.



 

## <a name="depth-stencil-testing-overview"></a>Übersicht über Depth-Stencil-Tests

Ein Tiefenschablonenpuffer, der als Texturressource erstellt wird, kann sowohl Tiefendaten als auch Schablonendaten enthalten. Die Tiefendaten werden verwendet, um zu bestimmen, welche Pixel der Kamera am nächsten liegen, und die Schablonendaten werden verwendet, um zu maskieren, welche Pixel aktualisiert werden können. Letztendlich werden sowohl die Daten der Tiefen- als auch der Schablonenwerte von der Ausgabezusammenführungsphase verwendet, um zu bestimmen, ob ein Pixel gezeichnet werden soll oder nicht. Das folgende Diagramm zeigt konzeptionell, wie Tiefenschablonentests durchgeführt werden.

![Diagramm der Funktionsweise von Tiefenschablonentests](images/d3d10-depth-stencil-test.png)

Informationen zum Konfigurieren von Tiefenschablonentests finden Sie unter [Konfigurieren Depth-Stencil Funktionalität.](d3d10-graphics-programming-guide-depth-stencil.md) Ein Tiefenschablonenobjekt kapselt den Tiefenschablonenzustand. Eine Anwendung kann den Tiefenschablonenzustand angeben, oder die OM-Phase verwendet Standardwerte. Blendingvorgänge werden pixelweise ausgeführt, wenn Multisampling deaktiviert ist. Wenn Multisampling aktiviert ist, erfolgt das Mischen pro Multisample.

Der Prozess der Verwendung des Tiefenpuffers, um zu bestimmen, welches Pixel gezeichnet werden soll, wird als Tiefenpufferung bezeichnet, manchmal auch als Z-Pufferung bezeichnet.

Sobald Tiefenwerte die Ausgabezusammenführungsphase erreichen (unabhängig davon, ob sie von der Interpolation oder von einem Pixel-Shader stammen), werden sie immer geklammert: z = min(Viewport.MaxDepth,max(Viewport.MinDepth,z)) entsprechend dem Format/der Genauigkeit des Tiefenpuffers unter Verwendung von Gleitkommaregeln. Nach dem Zusammenbinden wird der Tiefenwert (unter Verwendung von DepthFunc) mit dem vorhandenen Tiefenpufferwert verglichen. Wenn kein Tiefenpuffer gebunden ist, ist der Tiefentest immer erfolgreich.

Wenn keine Schablonenkomponente im Tiefenpufferformat oder keine Tiefenpuffergrenze vorhanden ist, ist der Schablonentest immer erfolgreich. Andernfalls bleibt die Funktionalität von Direct3D 9 unverändert.

Es kann jeweils nur ein Tiefen-/Schablonenpuffer aktiv sein. jede gebundene Ressourcenansicht muss mit der Tiefen-/Schablonenansicht übereinstimmen (gleiche Größe und Größe). Dies bedeutet nicht, dass die Ressourcengröße übereinstimmen muss, nur dass die Ansichtsgröße übereinstimmen muss.

Weitere Informationen zu Tiefenschablonentests finden Sie in [Tutorial 14.](https://msdn.microsoft.com/library/Ee416550(v=VS.85).aspx)

## <a name="blending-overview"></a>Übersicht über Blending

Blending kombiniert einen oder mehrere Pixelwerte, um eine endgültige Pixelfarbe zu erstellen. Das folgende Diagramm zeigt den Prozess zum Mischen von Pixeldaten.

![Diagramm der Funktionsweise der Datenmischung](images/d3d10-blend-state.png)

Konzeptionell können Sie dieses Flussdiagramm visualisieren, das in der Ausgabezusammenführungsphase zweimal implementiert wurde: Die erste kombiniert RGB-Daten, während parallel ein zweites Alphadaten kombiniert. Informationen zur Verwendung der API zum Erstellen und Festlegen des Blendzustands finden Sie unter [Konfigurieren der Blendingfunktionalität.](d3d10-graphics-programming-guide-blend-state.md)

Blend mit festen Funktionen kann unabhängig für jedes Renderziel aktiviert werden. Es gibt jedoch nur einen Satz von Blend-Steuerelementen, sodass dieselbe Mischung auf alle RenderTargets mit aktivierter Blending angewendet wird. Blend-Werte (einschließlich BlendFactor) werden vor dem Mischen immer an den Bereich des Renderzielformats klammern. Die Klammer erfolgt pro Renderziel unter Berücksichtigung des Renderzieltyps. Die einzige Ausnahme gilt für die Formate float16, float11 oder float10, die nicht verbunden sind, sodass Blendvorgänge für diese Formate mit mindestens gleicher Genauigkeit/gleichem Bereich wie das Ausgabeformat ausgeführt werden können. NaNs und Nullen mit Vorzeichen werden für alle Fälle weitergegeben (einschließlich 0,0 Mischungsgewichtungen).

Wenn Sie sRGB-Renderziele verwenden, konvertiert die Laufzeit die Renderzielfarbe in linearen Raum, bevor eine Mischung durchgeführt wird. Die Runtime konvertiert den endgültigen kombinierten Wert wieder in sRGB-Speicherplatz, bevor der Wert wieder im Renderziel gespeichert wird.

Unterschiede zwischen Direct3D 9 und Direct3D 10:

- In Direct3D 9 kann das Überblenden fester Funktionen unabhängig für jedes Renderziel aktiviert werden.
- In Direct3D 10 und höher gibt es eine Beschreibung des Blendzustands. daher kann ein Blendingwert für alle Renderziele festgelegt werden.



 

### <a name="dual-source-color-blending"></a>Dual-Source Farbmischung

Dieses Feature ermöglicht es der Ausgabezusammenführungsphase, gleichzeitig beide Pixel-Shaderausgaben (o0 und o1) als Eingaben für einen Blendingvorgang mit dem einzelnen Renderziel an Slot 0 zu verwenden. Gültige Blend-Vorgänge sind: add, subtract und revsubtract. Gültige Blendoptionen für SrcBlend, DestBlend, SrcBlendAlpha oder DestBlendAlpha sind: **D3D11 \_ BLEND \_ SRC1 \_ COLOR**, **D3D11 \_ BLEND \_ INV \_ SRC1 \_ COLOR**, **D3D11 \_ BLEND \_ SRC1 \_ ALPHA**, **D3D11 \_ BLEND \_ INV \_ SRC1 \_ ALPHA**. Die Mischungsgleichung und die Ausgabeschreibmaske geben an, welche Komponenten der Pixel-Shader ausgibt. Zusätzliche Komponenten werden ignoriert.

Das Schreiben in andere Pixel-Shaderausgaben (o2, o3 usw.) ist nicht definiert. Sie dürfen nicht in ein Renderziel schreiben, wenn es nicht an Slot 0 gebunden ist. Das Schreiben von oDepth ist während der Dual-Source-Farbmischung gültig.

Beispiele finden Sie unter [Blending pixel shader outputs (Mischen von Pixel-Shaderausgaben).](d3d10-graphics-programming-guide-blend-state.md)

## <a name="multiple-rendertargets-overview"></a>Übersicht über mehrere RenderTargets

Ein Pixel-Shader kann verwendet werden, um auf mindestens 8 separate Renderziele zu rendern, die alle denselben Typ aufweisen müssen (buffer, Texture1D, Texture1DArray usw.). Darüber hinaus müssen alle Renderziele in allen Dimensionen (Breite, Höhe, Tiefe, Arraygröße, Stichprobenanzahl) die gleiche Größe aufweisen. Jedes Renderziel kann ein anderes Datenformat aufweisen.

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
| [Tiefenausrichtung](d3d10-graphics-programming-guide-output-merger-stage-depth-bias.md)<br/>             | Polygone, die im 3D-Raum koplanar sind, können so aussehen, als wären sie nicht koplanar, indem sie jeweils eine Z-Voreingenommenheit (oder Tiefenabweichung) hinzufügen.<br/>                                                                                                              |



 

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Grafikpipeline](overviews-direct3d-11-graphics-pipeline.md)
</dt> <dt>

[Pipelinestufen (Direct3D 10)](/windows/desktop/direct3d10/d3d10-graphics-programming-guide-pipeline-stages)
</dt> </dl>

 

