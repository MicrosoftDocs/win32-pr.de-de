---
title: DirectComposition
description: In diesem Thema wird der Zweck von Microsoft DirectComposition erläutert, die Laufzeitanforderungen identifiziert und der Programmierhintergrund beschrieben, den Sie benötigen, um Microsoft DirectComposition effektiv zu verwenden.
ms.assetid: 40e2d02b-77e8-425f-ac5e-3dcddef08173
keywords:
- DirectComposition
- DirectComposition-API
- Microsoft DirectComposition
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ca1b13dbd0ee4893f1b208cd88d7fd1251b5fb7ece2400b7e0b195e84865b2d0
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118985410"
---
# <a name="directcomposition"></a>DirectComposition

> [!NOTE]
> Für Apps auf Windows 10 empfehlen wir die Verwendung von Windows.UI.Composition-APIs anstelle von DirectComposition. Weitere Informationen finden Sie unter [Modernisieren Ihrer Desktop-App mithilfe der visuellen Ebene](/windows/uwp/composition/visual-layer-in-desktop-apps).

## <a name="purpose"></a>Zweck

Microsoft DirectComposition ist eine Windows Komponente, die eine leistungsstarke Bitmapkomposition mit Transformationen, Effekten und Animationen ermöglicht. Anwendungsentwickler können die DirectComposition-API zum Erstellen von visuell ansprechenden Benutzeroberflächen verwenden, die umfassende und fließende animierte Übergänge von einem visuellen Objekt zum nächsten ermöglichen.

DirectComposition ermöglicht umfangreiche und fließende Übergänge, indem eine hohe Framerate erreicht wird, Grafikhardware verwendet wird und unabhängig vom UI-Thread ausgeführt wird. DirectComposition kann Bitmapinhalte akzeptieren, die von verschiedenen Renderingbibliotheken gezeichnet werden, einschließlich Microsoft DirectX-Bitmaps und Bitmaps, die in einem Fenster gerendert werden (HWND-Bitmaps). Außerdem unterstützt DirectComposition eine Vielzahl von Transformationen, z. B. 2D-affine Transformationen und 3D-Perspektiventransformationen, sowie grundlegende Effekte wie Clipping und Deckkraft.

DirectComposition wurde entwickelt, um das Verfassen von [*Visuals*](directcomposition-glossary.md) und das Erstellen animierter Übergänge zu vereinfachen. Wenn Ihre Anwendung bereits Renderingcode enthält oder bereits die empfohlene DirectX-API verwendet, müssen Sie nur einen minimalen Arbeitsaufwand durchführen, um DirectComposition effektiv zu verwenden.

## <a name="developer-audience"></a>Entwicklergruppe

Die DirectComposition-API ist für erfahrene und hochgradig leistungsfähige Grafikentwickler bestimmt, die C/C++ kennen, über ein solides Verständnis der Component Object Model (COM) verfügen und mit Windows Programmierkonzepten vertraut sind.

## <a name="run-time-requirements"></a>Laufzeitanforderungen

DirectComposition wurde in Windows 8 eingeführt. Sie ist in 32-Bit-, 64-Bit- und ARM-Plattformen enthalten.

## <a name="in-this-section"></a>In diesem Abschnitt



| Thema                                                                       | Beschreibung                                                                                                                                                    |
|-----------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Gründe für die Verwendung von DirectComposition](why-use-directcomposition-.md)<br/>     | In diesem Thema werden die Funktionen und Vorteile von DirectComposition beschrieben. <br/>                                                                           |
| [Verwenden von DirectComposition](how-to-use-directcomposition.md)<br/> | In diesem Abschnitt werden bewährte Methoden für die Verwendung der DirectComposition-API beschrieben, und es wird veranschaulicht, wie Sie die API verwenden, um mehrere allgemeine Aufgaben auszuführen. <br/> |
| [DirectComposition-Konzepte](directcomposition-concepts.md)<br/>     | Dieser Abschnitt bietet eine konzeptionelle Übersicht über DirectComposition.<br/>                                                                                   |
| [DirectComposition-Referenz](reference.md)<br/>                     | Dieser Abschnitt enthält ausführliche Referenzinformationen zu den Elementen, die die DirectComposition-API bilden.<br/>                                       |
| [DirectComposition-Beispiele](directcomposition-code-samples.md)<br/>  | Die folgenden Beispielanwendungen veranschaulichen die Verwendung der DirectComposition-API und deren Funktionen. <br/>                                      |
| [DirectComposition-Glossar](directcomposition-glossary.md)<br/>     | In diesem Thema werden DirectComposition-Begriffe definiert. <br/>                                                                                                        |



 

 

 





