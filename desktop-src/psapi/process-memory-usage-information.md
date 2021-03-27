---
title: Informationen zur Prozess Speicherauslastung
description: Die getprocessmemoryinfo-Funktion nimmt ein Prozess handle als Eingabe an und füllt \_ die \_ Struktur der Prozess speicherzähler mit Informationen über die Speicher Statistik für den Prozess auf.
ms.assetid: 683c899e-a7e8-4440-8f13-2a713c1618bf
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 133032b8cfb8a9af4ccea5661c9e0e0181ab4d93
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "103856607"
---
# <a name="process-memory-usage-information"></a>Informationen zur Prozess Speicherauslastung

Die [**getprocessmemoryinfo**](/windows/desktop/api/Psapi/nf-psapi-getprocessmemoryinfo) -Funktion nimmt ein Prozess handle als Eingabe an und füllt die Struktur der [**Prozess \_ Speicher \_ Zähler**](/windows/desktop/api/Psapi/ns-psapi-process_memory_counters) mit Informationen über die Speicher Statistik für den Prozess auf. Der **CB** -Member erhält die Größe der Struktur. Das **pagefehlercount** -Element empfängt die Anzahl der Seiten Fehler. Die verbleibenden Elemente erhalten die aktuelle und maximale Speicherauslastung in den folgenden Kategorien:

-   Arbeitssatz
-   Auslagerungs Pool
-   nicht Auslagerungs Pool
-   Auslagerungs Datei

Das *Workingset* ist die Menge an Arbeitsspeicher, die dem Prozess Kontext zu einem bestimmten Zeitpunkt physisch zugeordnet ist. Der Arbeitsspeicher im Auslagerungs *Pool* ist der System Arbeitsspeicher, der in die Auslagerungs Datei auf dem Datenträger übertragen werden kann, wenn er nicht verwendet wird. Der Arbeitsspeicher im nicht Auslagerungs *Pool* ist der System Arbeitsspeicher, der nicht auf den Datenträger ausgelagert werden kann, solange die entsprechenden Objekte zugewiesen werden. Die Verwendung der Auslagerungs *Datei* stellt dar, wie viel Arbeitsspeicher für den Prozess in der Auslagerungs Datei des Systems reserviert ist. Wenn die Speicherauslastung zu hoch ist, wird der ausgewählte Arbeitsspeicher vom virtuellen Speicher-Manager auf den Datenträger über die Wenn ein Thread eine Seite benötigt, die sich nicht im Arbeitsspeicher befindet, lädt der Speicher-Manager ihn erneut aus der Auslagerungs Datei.

 

 




