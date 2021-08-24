---
description: Die Prioritätsumkehr tritt auf, wenn zwei oder mehr Threads mit unterschiedlichen Prioritäten zu planende Konflikte aufweisen.
ms.assetid: 1cb2f3c9-4641-40d8-892c-768abaf6affb
title: Prioritätsumkehr
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 09a891655196b8f7e81c118d39fb8516a244411f1f4f6d9505e2fb40818d71f7
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "120031930"
---
# <a name="priority-inversion"></a>Prioritätsumkehr

Die Prioritätsumkehr tritt auf, wenn zwei oder mehr Threads mit unterschiedlichen Prioritäten zu planende Konflikte aufweisen. Betrachten Sie einen einfachen Fall mit drei Threads: Thread 1, Thread 2 und Thread 3. Thread 1 hat hohe Priorität und kann geplant werden. Thread 2, ein Thread mit niedriger Priorität, führt Code in einem kritischen Abschnitt aus. Thread 1, der Thread mit hoher Priorität, beginnt mit dem Warten auf eine freigegebene Ressource aus Thread 2. Thread 3 hat mittlere Priorität. Thread 3 empfängt die gesamte Prozessorzeit, da der Thread mit hoher Priorität (Thread 1) auf freigegebene Ressourcen vom Thread mit niedriger Priorität (Thread 2) wartet. Thread 2 verlässt den kritischen Abschnitt nicht, da er nicht die höchste Priorität hat und nicht geplant wird.

Der Planer löst dieses Problem, indem er die Priorität der bereiten Threads zufällig erhöht (in diesem Fall die Sperreninhaber mit niedriger Priorität). Die Threads mit niedriger Priorität werden lange genug ausgeführt, um den kritischen Abschnitt zu beenden, und der Thread mit hoher Priorität kann in den kritischen Abschnitt gelangen. Wenn der Thread mit niedriger Priorität nicht genügend CPU-Zeit erhält, um den kritischen Abschnitt beim ersten Mal zu beenden, erhält er während der nächsten Planungsrunde eine weitere Chance.

 

 



