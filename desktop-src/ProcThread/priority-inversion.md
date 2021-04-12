---
description: Die Inversion der Priorität tritt auf, wenn mindestens zwei Threads mit unterschiedlichen Prioritäten zu planen sind.
ms.assetid: 1cb2f3c9-4641-40d8-892c-768abaf6affb
title: Inversion der Priorität
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 79a0f4c9d57000e9e81429ee882e70dc14f63ae4
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104345458"
---
# <a name="priority-inversion"></a>Inversion der Priorität

Die Inversion der Priorität tritt auf, wenn mindestens zwei Threads mit unterschiedlichen Prioritäten zu planen sind. Ziehen Sie einen einfachen Fall mit drei Threads in Erwägung: Thread 1, Thread 2 und Thread 3. Thread 1 hat eine hohe Priorität und ist für die Planung bereit. Thread 2, ein Thread mit niedriger Priorität, führt Code in einem kritischen Abschnitt aus. Thread 1, der Thread mit hoher Priorität, wartet auf eine freigegebene Ressource aus Thread 2. Thread 3 hat mittlere Priorität. Thread 3 empfängt die gesamte Prozessorzeit, da der Thread mit hoher Priorität (Thread 1) auf gemeinsame Ressourcen aus dem Thread mit niedriger Priorität (Thread 2) wartet. Thread 2 verlässt den kritischen Abschnitt nicht, da er nicht die höchste Priorität hat und nicht geplant wird.

Das Zeit Planungs Modul löst dieses Problem, indem es die Priorität der geeigneten Threads (in diesem Fall die Sperren-Inhaber mit niedriger Priorität) nach dem Zufallsprinzip erhöht. Die Threads mit niedriger Priorität laufen lang genug, um den kritischen Abschnitt zu beenden, und der Thread mit hoher Priorität kann in den kritischen Abschnitt wechseln. Wenn der Thread mit niedriger Priorität nicht genügend CPU-Zeit benötigt, um den kritischen Abschnitt zum ersten Mal zu verlassen, erhält er während der nächsten Zeitplanung eine weitere Chance.

 

 



