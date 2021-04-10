---
title: DirectComposition
description: In diesem Thema wird der Zweck von Microsoft directcomposition erläutert, dessen Lauf Zeitanforderungen identifiziert und der Programmier Hintergrund beschrieben, den Sie für die effektive Verwendung von Microsoft directcomposition benötigen.
ms.assetid: 40e2d02b-77e8-425f-ac5e-3dcddef08173
keywords:
- DirectComposition
- Directcomposition-API
- Microsoft directcomposition
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bb34a4bb3bb7c0ffe370777888e20704fd0165d0
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "104309631"
---
# <a name="directcomposition"></a>DirectComposition

> [!NOTE]
> Für apps unter Windows 10 wird die Verwendung von Windows. UI. Composition-APIs anstelle von directcomposition empfohlen. Weitere Informationen finden Sie unter [modernisieren ihrer Desktop-App mithilfe der visuellen Ebene](/windows/uwp/composition/visual-layer-in-desktop-apps).

## <a name="purpose"></a>Zweck

Microsoft directcomposition ist eine Windows-Komponente, die eine leistungsstarke bitmapkomposition mit Transformationen, Effekten und Animationen ermöglicht. Anwendungsentwickler können die DirectComposition-API zum Erstellen von visuell ansprechenden Benutzeroberflächen verwenden, die umfassende und fließende animierte Übergänge von einem visuellen Objekt zum nächsten ermöglichen.

Directcomposition ermöglicht umfassende und fließende Übergänge durch das Erreichen einer hohen Framerate, die Verwendung von Grafikhardware und die unabhängige Funktionsweise des UI-Threads. Directcomposition kann bitmapinhalte akzeptieren, die von verschiedenen renderingbibliotheken gezeichnet werden, einschließlich Microsoft DirectX-Bitmaps und Bitmaps, die in einem Fenster (HWND-Bitmaps) gerendert werden. Außerdem unterstützt directcomposition eine Vielzahl von Transformationen, wie z. b. 2D-affine Transformationen und 3D-Perspektiven Transformationen, sowie grundlegende Effekte wie Clipping und Deckkraft.

Directcomposition ist so konzipiert, dass die Erstellung von [*visuellen*](directcomposition-glossary.md) Elementen und die Erstellung animierter Übergänge vereinfacht werden. Wenn Ihre Anwendung bereits Renderingcode enthält oder bereits die empfohlene DirectX-API verwendet, müssen Sie nur eine minimale Menge an Arbeit durchführen, um directcomposition effektiv zu verwenden.

## <a name="developer-audience"></a>Entwicklergruppe

Die directcomposition-API ist für erfahrene und hochgradig leistungsfähige Grafik Entwickler gedacht, die C/C++ kennen, ein solides Verständnis der Component Object Model (com) haben und mit den Windows-Programmier Konzepten vertraut sind.

## <a name="run-time-requirements"></a>Laufzeitanforderungen

Directcomposition wurde in Windows 8 eingeführt. Es ist in 32-Bit-, 64-Bit-und Arm-Plattformen enthalten.

## <a name="in-this-section"></a>In diesem Abschnitt



| Thema                                                                       | BESCHREIBUNG                                                                                                                                                    |
|-----------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Gründe für die Verwendung von directcomposition](why-use-directcomposition-.md)<br/>     | In diesem Thema werden die Funktionen und Vorteile von directcomposition beschrieben. <br/>                                                                           |
| [Verwenden von directcomposition](how-to-use-directcomposition.md)<br/> | In diesem Abschnitt werden bewährte Methoden für die Verwendung der directcomposition-API beschrieben, und es wird veranschaulicht, wie die API verwendet wird, um mehrere gängige Aufgaben auszuführen. <br/> |
| [Directcomposition-Konzepte](directcomposition-concepts.md)<br/>     | Dieser Abschnitt enthält eine konzeptionelle Übersicht über directcomposition.<br/>                                                                                   |
| [Directcomposition-Referenz](reference.md)<br/>                     | Dieser Abschnitt enthält ausführliche Referenzinformationen zu den Elementen, die die directcomposition-API bilden.<br/>                                       |
| [Directcomposition-Beispiele](directcomposition-code-samples.md)<br/>  | Die folgenden Beispielanwendungen zeigen, wie Sie die directcomposition-API verwenden und ihre Funktionen veranschaulichen. <br/>                                      |
| [Directcomposition-Glossar](directcomposition-glossary.md)<br/>     | In diesem Thema werden die directcomposition-Begriffe definiert. <br/>                                                                                                        |



 

 

 





