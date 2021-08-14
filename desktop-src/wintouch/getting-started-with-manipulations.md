---
title: Manipulationen
description: In diesem Abschnitt wird die Objektbearbeitung für Windows Touch erläutert.
ms.assetid: 7f905c36-7804-422c-8a60-a281e03c5e15
keywords:
- Windows Touch,Manipulationen
- Manipulationen,About
- Manipulationen,Gestenunterschiede
- Gesten,Manipulationsunterschiede
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5368b39de1f35cc9a547bc240fc3c984fc1f10f658972b0f845a965e09bb29c8
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118435985"
---
# <a name="manipulations"></a>Manipulationen

In diesem Abschnitt wird die Objektbearbeitung für Windows Touch erläutert.

## <a name="manipulation-overview"></a>Übersicht über die Manipulation

Eine praktische Möglichkeit, sich über Manipulationen gedanken zu machen, ist, sie als Obermenge von Gesten zu betrachten. Was Sie mit Gesten tun können, können Sie mithilfe von Manipulationen mit mehr Flexibilität und mit feinerer Genauigkeit tun. Der Unterschied zwischen Manipulationen und Gesten wird am besten anhand eines einfachen Beispiels demonstriert. Sie können ein Objekt erweitern und gleichzeitig mithilfe von Bearbeitungen übersetzen. mit Gesten können Sie nur eine nach der anderen tun. Diese Möglichkeit, ein Objekt in Echtzeit zu bearbeiten, macht Anwendungen für Benutzer intuitiver, da sie eine realistischere Erfahrung ermöglichen.

Die Manipulations-APIs werden verwendet, um Transformationsvorgänge für Objekte für Touch-fähige Anwendungen zu vereinfachen. Manipulationen werden in Windows 7 über das COM-Objekt manipulations ausgeführt. Durch die Verwendung von Manipulationen können Entwickler Trägheit (Objektkörper) einfacher unterstützen und Transformationen für Objekte problemlos auf eine Weise durchführen, die mit anderen Anwendungen konsistent ist. In den folgenden Abschnitten werden verschiedene Möglichkeiten zum Ausführen von Bearbeitungen erläutert.



| `Section`                                                                                            | BESCHREIBUNG                                                                                                                                          |
|----------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Hinzufügen von Manipulationsunterstützung zu nicht verwaltetem Code](adding-manipulation-support-in-unmanaged-code.md) | Erläutert das Implementieren einer Ereignissenke für die [**\_ IManipulationEvents-Schnittstelle**](/windows/win32/api/manipulations/nn-manipulations-_imanipulationevents) und das Hinzufügen von Ereignishandlern zum Code. |
| [Erweiterte Manipulationen](advanced-manipulations.md)                                               | Erläutert das Ausführen komplexer Bearbeitungen.                                                                                                       |
| [Drehung mit einem Finger](single-finger-rotation.md)                                               | Erläutert, wie ein Objekt mithilfe eines Pivotpunkts und des Bearbeitungsprozessors gedreht wird.                                                              |



 

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Manipulationen und Trägheit](manipulation-and-inertia.md)
</dt> </dl>

 

 




