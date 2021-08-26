---
description: Ein Multitaskingbetriebssystem teilt die verfügbare Prozessorzeit auf die Prozesse oder Threads auf, die sie benötigen.
ms.assetid: ac45bef6-f078-40ac-95f4-06bd61ff46c4
title: Multitasking
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ee7826ca79d6095715c722b4b5c3da479e276444825343ac096cd9822d9e365a
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "120032180"
---
# <a name="multitasking"></a>Multitasking

Ein Multitaskingbetriebssystem teilt die verfügbare Prozessorzeit auf die Prozesse oder Threads auf, die sie benötigen. Das System ist für präemptives Multitasking konzipiert. jedem ausgeführten Thread wird ein *Prozessorzeitslice* zugeordnet. Der aktuell ausgeführte Thread wird angehalten, wenn sein Zeitslice verstrichen ist, sodass ein anderer Thread ausgeführt werden kann. Wenn das System von einem Thread zu einem anderen wechselt, speichert es den Kontext des vorzeitig entfernten Threads und stellt den gespeicherten Kontext des nächsten Threads in der Warteschlange wieder her.

Die Länge des Zeitsegments hängt vom Betriebssystem und vom Prozessor ab. Da jedes Zeitslice klein ist (ca. 20 Millisekunden), scheinen mehrere Threads gleichzeitig ausgeführt zu werden. Dies ist tatsächlich bei Multiprozessorsystemen der Fall, bei denen die ausführbaren Threads auf die verfügbaren Prozessoren verteilt sind. Bei der Verwendung mehrerer Threads in einer Anwendung müssen Sie jedoch Vorsicht walten lassen, da die Systemleistung abnehmen kann, wenn zu viele Threads vorhanden sind.

Weitere Informationen finden Sie in den folgenden Themen:

-   [Vorteile von Multitasking](advantages-of-multitasking.md)
-   [Verwendung von Multitasking](when-to-use-multitasking.md)
-   [Überlegungen zu Multitasking](multitasking-considerations.md)

 

 



