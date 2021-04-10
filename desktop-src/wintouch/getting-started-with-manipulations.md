---
title: Manipulationen
description: In diesem Abschnitt wird die Objekt Bearbeitung für Windows-Fingerabdruck erläutert.
ms.assetid: 7f905c36-7804-422c-8a60-a281e03c5e15
keywords:
- Windows-Fingereingabe, Manipulationen
- Manipulationen, Informationen zu
- Manipulationen, Gesten Unterschiede
- Gesten, Manipulations Unterschiede
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 10fe65494de990305e4268aa4191b5dabaa267f4
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "104309348"
---
# <a name="manipulations"></a>Manipulationen

In diesem Abschnitt wird die Objekt Bearbeitung für Windows-Fingerabdruck erläutert.

## <a name="manipulation-overview"></a>Übersicht über Manipulationen

Eine praktische Möglichkeit, Manipulationen zu berücksichtigen, besteht darin, Sie als eine Reihe von Gesten zu betrachten. Mit Gesten können Sie mehr Flexibilität und eine präzisere Genauigkeit durch die Verwendung von Manipulationen erreichen. Der Unterschied zwischen Manipulationen und Gesten wird am besten anhand eines einfachen Beispiels veranschaulicht. Sie können ein Objekt erweitern und gleichzeitig mithilfe von Manipulationen übersetzen. mit Gesten können Sie nur eine gleichzeitig ausführen. Diese Möglichkeit, ein Objekt in Echtzeit zu manipulieren, macht Anwendungen intuitiver für Benutzer, indem es eine realistischere Benutzerfreundlichkeit ermöglicht.

Die Manipulations-APIs werden verwendet, um Transformations Vorgänge für Objekte für Anwendungen mit aktiviertem Touchscreen zu vereinfachen. Manipulationen werden in Windows 7 durch das Manipulationen-com-Objekt durchgeführt. Mithilfe von Manipulationen können Entwickler die Trägheit (Objekt Physik) leichter unterstützen und problemlos Transformationen für Objekte auf eine Weise durchführen, die mit anderen Anwendungen konsistent ist. In den folgenden Abschnitten werden verschiedene Möglichkeiten erläutert, wie Sie Manipulationen durchführen können.



| `Section`                                                                                            | BESCHREIBUNG                                                                                                                                          |
|----------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Hinzufügen von Manipulations Unterstützung zu nicht verwaltetem Code](adding-manipulation-support-in-unmanaged-code.md) | Erläutert das Implementieren einer Ereignis Senke für die [**\_ imanipulationevents**](/windows/win32/api/manipulations/nn-manipulations-_imanipulationevents) -Schnittstelle und das Hinzufügen von Ereignis Handlern zu Ihrem Code. |
| [Erweiterte Manipulationen](advanced-manipulations.md)                                               | Erläutert, wie komplexe Manipulationen durchgeführt werden.                                                                                                       |
| [Drehung mit einem Finger](single-finger-rotation.md)                                               | Erläutert, wie ein Objekt mithilfe eines pivotpunkts und des Manipulations Prozessors gedreht wird.                                                              |



 

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Manipulationen und Trägheit](manipulation-and-inertia.md)
</dt> </dl>

 

 




