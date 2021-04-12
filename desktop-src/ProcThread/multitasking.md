---
description: Ein Multitasking-Betriebssystem dividiert die verfügbare Prozessorzeit für die Prozesse oder Threads, die es benötigen.
ms.assetid: ac45bef6-f078-40ac-95f4-06bd61ff46c4
title: Multitasking
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3d06c1d8d44f397f06923c793971bcb20f35b2b4
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104345468"
---
# <a name="multitasking"></a>Multitasking

Ein Multitasking-Betriebssystem dividiert die verfügbare Prozessorzeit für die Prozesse oder Threads, die es benötigen. Das System ist für ein präemptives Multitasking konzipiert. Er ordnet jedem ausgeführten Thread einen Prozessor *Zeit Slice* zu. Der aktuell ausgeführte Thread wird angehalten, wenn der Zeit Slice abläuft, sodass ein anderer Thread ausgeführt werden kann. Wenn das System von einem Thread zu einem anderen wechselt, speichert es den Kontext des vorzeitig entfernten Threads und stellt den gespeicherten Kontext des nächsten Threads in der Warteschlange wieder her.

Die Länge des Zeitsegments hängt vom Betriebssystem und vom Prozessor ab. Da jeder Zeit Slice klein ist (ungefähr 20 Millisekunden), scheinen mehrere Threads gleichzeitig ausgeführt zu werden. Dies ist tatsächlich bei Multiprozessorsystemen der Fall, bei denen die ausführbaren Threads auf die verfügbaren Prozessoren verteilt sind. Sie müssen jedoch Vorsicht walten lassen, wenn Sie mehrere Threads in einer Anwendung verwenden, da sich die Systemleistung verringern kann, wenn zu viele Threads vorhanden sind.

Weitere Informationen finden Sie unter den folgenden Themen:

-   [Vorteile von Multitasking](advantages-of-multitasking.md)
-   [Verwendung von Multitasking](when-to-use-multitasking.md)
-   [Überlegungen zum Multitasking](multitasking-considerations.md)

 

 



