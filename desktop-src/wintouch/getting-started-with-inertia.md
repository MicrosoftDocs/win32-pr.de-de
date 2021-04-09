---
title: Trägheit
description: In diesem Abschnitt wird Trägheit für Windows-Fingereingabe erläutert.
ms.assetid: c33dda89-c715-4da0-a7af-aa0010dfd88b
keywords:
- Windows-Fingereingabe, Trägheit
- Trägheit, Info
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f3b69ad31ec4a61f8723c9e52f87883dc4af3772
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "104036447"
---
# <a name="inertia"></a>Trägheit

In diesem Abschnitt wird Trägheit für Windows-Fingereingabe erläutert.

Die in Windows 7 enthaltene Trägheit-API ermöglicht ein konsistentes Objekt Verhalten in Windows-Finger eingabeanwendungen durch Bereitstellen eines einfachen Physik Modells. Trägheit wird mithilfe des Trägheits Prozessor aktiviert, einer Klasse, die Funktionen kapselt. Der Trägheits Prozessor verarbeitet Ereignisse, die an ihn weitergeleitet werden, wenn Objekt Manipulationen abgeschlossen werden, und indem Objekt Verarbeitungen auf eine Weise verarbeitet werden, die mit anderen Anwendungen konsistent ist. Beachten Sie, dass der Trägheits Prozessor eng an den Manipulations Prozessor gekoppelt ist, um das Hinzufügen von Trägheit-Unterstützung für Anwendungen zu vereinfachen Tatsächlich löst der Trägheits Prozessor dieselben Ereignisse wie der Manipulations Prozessor aus. Im folgenden Abschnitt werden die ersten Schritte mit Trägheit erläutert.



| `Section`                                                                      | BESCHREIBUNG                                                                                                              |
|------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------|
| [Trägheit-Mechanik](inertia-mechanics.md)                                   | Erläutert die Grundlagen der Trägheits Berechnungen.                                                                             |
| [Behandeln von Trägheit in nicht verwaltetem Code](handling-inertia-in-unmanaged-code.md) | Erläutert, wie die [**IInertiaProcessor**](/windows/desktop/api/manipulations/nn-manipulations-iinertiaprocessor) -Schnittstelle für die Handhabung von Trägheit in nicht verwaltetem Code verwendet wird. |



 

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Manipulationen und Trägheit](manipulation-and-inertia.md)
</dt> </dl>

 

 




