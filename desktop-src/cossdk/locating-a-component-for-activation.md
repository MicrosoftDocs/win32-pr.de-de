---
description: Suchen einer Komponente zur Aktivierung
ms.assetid: 2ba9484a-c646-4a35-8b32-268fe7a9520f
title: Suchen einer Komponente zur Aktivierung
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 80bd90068c34469d61af36e6de8c409cb02e078c
ms.sourcegitcommit: bf526e267d3991892733bdd229c66d5365cf244a
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 02/05/2021
ms.locfileid: "104561179"
---
# <a name="locating-a-component-for-activation"></a>Suchen einer Komponente zur Aktivierung

Wenn com+ die richtige Partition gefunden hat – über den standardmäßigen Partitions Satz der Benutzeridentität, einen partitionmoniker oder die Partitions-ID im Kontext des Objekts – com + muss dann die richtige Komponente innerhalb dieser Partition suchen. In der folgenden Abbildung wird gezeigt, wie eine Komponente gefunden und aktiviert wird, wenn sich diese Komponente in einer Partition befindet.

> [!Note]  
> Vor der Aktivierung einer Komponente führt com+ eine Validierung durch, um zu überprüfen, ob die Benutzeridentität, die versucht, die Komponente zu aktivieren, über Zugriffsrechte für den Partitions Satz verfügt, in dem sich die Komponente befindet.

 

![Diagramm, das eine Problem Behandlungs Struktur zum Auffinden einer Komponente zur Aktivierung anzeigt.](images/26c26a37-ec95-4f9f-aa59-4d84a7bb0fa3.png)

Die vorherige Abbildung zeigt Folgendes:

-   Wenn sich die aufgerufene Komponente in einer Partition befindet und sich in der gleichen Anwendung wie die aufrufende Komponente befindet, wird die Komponente aktiviert, unabhängig davon, ob die aufgerufene Komponente als öffentlich oder privat gekennzeichnet ist.
-   Wenn sich die aufgerufene Komponente in einer Partition befindet, aber nicht in der gleichen Anwendung wie die aufrufende Komponente vorhanden ist, prüft com+, ob die Komponente als öffentlich markiert ist. Wenn keine öffentliche Version gefunden wird, durchsucht com+ die globale Partition, um nach einer öffentlichen Version der Komponente zu suchen. Wenn keine öffentliche Version der Komponente in der globalen Partition gefunden wird oder die Benutzeridentität keine Berechtigungen für die Partition hat, tritt bei der Aktivierung ein Fehler auf.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Suchen von Partitionen während der Aktivierung](locating-partitions-during-activation.md)
</dt> </dl>

 

 



