---
title: Output-Merger Phase
description: In der Output-Fusion (OM)-Phase wird die endgültige gerenderte Pixelfarbe mithilfe einer Kombination aus dem Pipeline Status, den von den Pixel-Shadern generierten Pixeldaten, dem Inhalt der Renderingziele und dem Inhalt der tiefen/Schablonen Puffer generiert.
ms.assetid: 8be68c15-2deb-4804-b683-30080a876189
keywords:
- Ausgabe Zusammenführungs Stufe (Direct3D 10)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ec77eaff506a0be87a3f0e98de691b50c27c0c3f
ms.sourcegitcommit: a716ca2a6a22a400f02c6b31699cf4da83ee3619
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 11/04/2020
ms.locfileid: "104391232"
---
# <a name="output-merger-stage"></a>Output-Merger Phase

In der Output-Fusion (OM)-Phase wird die endgültige gerenderte Pixelfarbe mithilfe einer Kombination aus dem Pipeline Status, den von den Pixel-Shadern generierten Pixeldaten, dem Inhalt der Renderingziele und dem Inhalt der tiefen/Schablonen Puffer generiert. Der OM-Schritt ist der letzte Schritt, um zu bestimmen, welche Pixel sichtbar sind (mit tiefen Schablone-Tests) und wie die endgültigen Pixel Farben gemischt werden.



|                                                                                                                                                                                                                                                                                                                                                                                                             |
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Unterschiede zwischen Direct3D 9 und Direct3D 10: Direct3D 9 implementieren Alpha Tests (mit dem [Alpha Testzustand](/windows/desktop/direct3d9/alpha-testing-state)), um zu steuern, ob ein Pixel in ein Ausgabe Renderziel geschrieben wird.<br/> Direct3D 10 und höher implementiert keinen Alpha-Test (oder Alpha Testzustand). Dies kann mit einem Pixelshader oder mit tiefen-/Stencil-Funktionen gesteuert werden.<br/> |



 

## <a name="depth-stencil-testing-overview"></a>Übersicht über Depth-Stencil Tests

Ein tiefen Schablone-Puffer, der als Textur Ressource erstellt wird, kann sowohl Tiefendaten als auch Daten der Schablone enthalten. Die Tiefendaten werden verwendet, um zu bestimmen, welche Pixel der Kamera am nächsten liegen, und die Schablonen Daten werden verwendet, um die zu aktualisierenden Pixel zu maskieren. Letztendlich werden die Daten der tiefen-und Schablonen Werte von der Ausgabe-Fusion-Phase verwendet, um zu bestimmen, ob ein Pixel gezeichnet werden soll oder nicht. Das folgende Diagramm zeigt konzeptionell, wie tiefen Schablonen getestet werden.

![Diagramm der Funktionsweise von tiefen Schablone](images/d3d10-depth-stencil-test.png)

Informationen zum Konfigurieren von tiefen Schablonen Tests finden Sie unter [Konfigurieren von Depth-Stencil Funktionen](d3d10-graphics-programming-guide-depth-stencil.md). Ein tiefen Schablone-Objekt kapselt den Zustand der tiefen Schablone. Eine Anwendung kann den Status der tiefen Schablone angeben, oder die OM-Phase verwendet die Standardwerte. Mischungs Vorgänge werden pro Pixel ausgeführt, wenn multisamplinggrad deaktiviert ist. Wenn die multisamplinggrad-Funktion aktiviert ist, erfolgt die Mischung pro Multisample-Basis.

Der Prozess der Verwendung des tiefen Puffers, um zu bestimmen, welches Pixel gezeichnet werden soll, wird als tiefen Pufferung bezeichnet, auch manchmal als z-Pufferung bezeichnet.

Sobald die tiefen Werte die Ausgabe-Fusion-Phase erreichen (unabhängig davon, ob Sie von der Interpolations-oder von einem Pixelshader stammt), werden Sie immer mit einem klammergen (z = min (Viewport. maxtiefe, Max (Viewport. mintiefe, z)) entsprechend dem Format/der Genauigkeit des tiefen Puffers, mithilfe von Gleit Komma Regeln. Nach dem Einspannen wird der tiefen Wert (mit depthfunc) mit dem vorhandenen tiefen Puffer Wert verglichen. Wenn kein tiefen Puffer gebunden ist, verläuft der tiefen Test immer.

Wenn im tiefen Puffer Format keine Schablonen Komponente vorhanden ist oder kein tiefen Puffer gebunden ist, wird der Schablone-Test immer weitergeleitet. Andernfalls ist die Funktionalität von Direct3D 9 unverändert.

Es kann immer nur ein tiefen-/Schablone-Puffer aktiv sein. die Ansicht "Tiefe/Schablone" muss eine beliebige gebundene Ressourcen Ansicht (Größe und Größe) entsprechen. Dies bedeutet nicht, dass die Ressourcen Größe entsprechen muss, nur dass die Ansichts Größe Stimmen muss.

Weitere Informationen zum Testen von tiefen Schablonen finden Sie unter [Tutorial 14](https://msdn.microsoft.com/library/Ee416550(v=VS.85).aspx).

## <a name="blending-overview"></a>Übersicht über das Mischen

Blending kombiniert einen oder mehrere Pixelwerte, um eine endgültige Pixelfarbe zu erstellen. Das folgende Diagramm zeigt den Prozess, der zum Mischen von Pixeldaten beteiligt ist.

![Diagramm zur Funktionsweise von Mischungs Daten](images/d3d10-blend-state.png)

Konzeptionell können Sie dieses Flussdiagramm visualisieren, das zweimal in der Ausgabe-Fusion-Phase implementiert wird: das erste kombiniert RGB-Daten, während gleichzeitig ein zweites Alpha-Daten kombiniert. Informationen zur Verwendung der-API zum Erstellen und Festlegen des Blend-Zustands finden Sie unter [Konfigurieren von Mischungs Funktionen](d3d10-graphics-programming-guide-blend-state.md).

Die Kombination von "Fixed-Function" kann für jedes Renderziel unabhängig aktiviert werden. Es gibt jedoch nur einen Satz von Blend-Steuerelementen, sodass die gleiche Blend auf alle Rendertargets mit aktivierter Mischung angewendet wird. Blend-Werte (einschließlich blendfactor) werden vor dem Mischen immer an den Bereich des renderzielformats gebunden. Die Klammer erfolgt pro Renderziel und respektiert den renderzieltyp. Die einzige Ausnahme sind die float16-, float11-oder float10-Formate, die nicht geklammert werden, sodass Blend-Vorgänge für diese Formate mit mindestens gleicher Genauigkeit/Bereich als Ausgabeformat durchgeführt werden können. Nan-und signed Nullen werden für alle Fälle (einschließlich 0,0 Blend-Gewichtungen) weitergegeben.

Wenn Sie sRGB-Renderziele verwenden, konvertiert die Common Language Runtime die renderzielfarbe in linearen Raum, bevor Sie gemischt funktioniert. Die Laufzeit konvertiert den endgültigen gemischten Wert wieder in den sRGB-Speicherplatz, bevor der Wert wieder in das Renderziel gespeichert wird.



|                                                                                                                                                                                                                                                                                                     |
|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Unterschiede zwischen Direct3D 9 und Direct3D 10: in Direct3D 9 können Mischungs Funktionen mit fester Funktion unabhängig für jedes Renderziel aktiviert werden.<br/> In Direct3D 10 und höher gibt es eine Beschreibung des Blend-Zustands. Daher kann für alle Renderziele ein Mischungs Wert festgelegt werden.<br/> |



 

### <a name="dual-source-color-blending"></a>Dual-Source Farbmischung

Diese Funktion ermöglicht der Ausgabe Zusammenführungs Phase das gleichzeitige verwenden beider Pixel-Shader-Ausgaben (o0 und O1) als Eingaben für einen Mischungs Vorgang mit dem einzelnen Renderziel bei Slot 0. Gültige Blend-Vorgänge sind: Add, subtrahieren und revsubtract. Gültige Blend-Optionen für srcblend, destblend, srcblendalpha oder destblendalpha umfassen **: D3D11 \_ Blend \_ Quelle1 \_ Color**, **D3D11 \_ Blend \_ Inv \_ Quelle1 \_ Color**, **D3D11 \_ Blend \_ Quelle1 \_ Alpha**, **D3D11 \_ Blend \_ Inv \_ Quelle1 \_ Alpha**. Die Blend-Gleichung und die Ausgabe Schreib Maske geben an, welche Komponenten der Pixelshader ausgibt. Zusätzliche Komponenten werden ignoriert.

Das Schreiben in andere Pixel-Shader-Ausgaben (O2, O3 usw.) ist nicht definiert. Sie dürfen nicht in ein Renderziel schreiben, wenn es nicht an Slot 0 gebunden ist. Das Schreiben der otiefe ist während der Dual-Source-Farbmischung gültig.

Beispiele finden Sie unter [Blending von Pixel-Shader-Ausgaben](d3d10-graphics-programming-guide-blend-state.md).

## <a name="multiple-rendertargets-overview"></a>Übersicht über mehrere Rendertargets

Ein Pixelshader kann zum Rendern von mindestens 8 separaten renderzielen verwendet werden, von denen alle denselben Typ aufweisen müssen (buffer, Texture1D, Texture1DArray usw.). Außerdem müssen alle Renderziele in allen Dimensionen (Breite, Höhe, Tiefe, Array Größe, Anzahl von Stichproben) dieselbe Größe aufweisen. Jedes Renderziel weist möglicherweise ein anderes Datenformat auf.

Sie können eine beliebige Kombination von renderzielslots verwenden (bis zu 8). Eine Ressourcen Ansicht kann jedoch nicht gleichzeitig an mehrere renderzielslots gebunden werden. Eine Sicht kann wieder verwendet werden, solange die Ressourcen nicht gleichzeitig verwendet werden.

## <a name="output-write-mask-overview"></a>Übersicht über Output-Write Mask

Verwenden Sie eine Ausgabe-/Schreibmaske, um (pro Komponente) zu steuern, welche Daten in ein Renderziel geschrieben werden können.

## <a name="sample-mask-overview"></a>Übersicht über die Beispiel Maske

Eine Beispiel Maske ist eine 32-Bit-Abdeckungs Maske, die bestimmt, welche Beispiele in aktiven Renderingzielen aktualisiert werden. Es ist nur eine Beispiel Maske zulässig. Die Zuordnung von Bits in einer Beispiel Maske zu den Beispielen in einer Ressource wird von einem Benutzer definiert. Für das Rendering von n-Stichproben werden die ersten n Bits (aus dem LSB) der Beispiel Maske verwendet (32 Bits ist die maximale Anzahl von Bits).


## <a name="in-this-section"></a>In diesem Abschnitt



| Thema                                                                                                    | BESCHREIBUNG                                                                                                                                                                                                                                                      |
|----------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Konfigurieren von Depth-Stencil Funktionen](d3d10-graphics-programming-guide-depth-stencil.md)<br/> | In diesem Abschnitt werden die Schritte zum Einrichten des tiefen Schablone-Puffers und der Status der tiefen Schablone für die Ausgabe-Fusion-Phase behandelt.<br/>                                                                                                                           |
| [Konfigurieren von Mischungs Funktionen](d3d10-graphics-programming-guide-blend-state.md)<br/>        | Mischungs Vorgänge werden für jede Pixel-Shader-Ausgabe (RGBA-Wert) ausgeführt, bevor der Ausgabewert in ein Renderziel geschrieben wird. Wenn die multisamplinggrad-Funktion aktiviert ist, erfolgt die Mischung in jedem Multisample. Andernfalls wird für jedes Pixel ein Mischungs Vorgang durchgeführt.<br/> |
| [Tiefenausrichtung](d3d10-graphics-programming-guide-output-merger-stage-depth-bias.md)<br/>             | Polygone, die in 3D-Raum kopiert werden, können so dargestellt werden, als wären Sie nicht durch Hinzufügen einer z-Bias (oder einer tiefen Abweichung) zu jeder Form.<br/>                                                                                                              |



 

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Grafik Pipeline](overviews-direct3d-11-graphics-pipeline.md)
</dt> <dt>

[Pipeline Stufen (Direct3D 10)](/windows/desktop/direct3d10/d3d10-graphics-programming-guide-pipeline-stages)
</dt> </dl>

 

