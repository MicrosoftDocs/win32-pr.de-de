---
title: Verarbeiten von Speicherauslastungsinformationen
description: Die GetProcessMemoryInfo-Funktion verwendet ein Prozesshandle als Eingabe und füllt eine PROCESS \_ MEMORY \_ COUNTERS-Struktur mit Informationen über die Speicherstatistiken für den Prozess aus.
ms.assetid: 683c899e-a7e8-4440-8f13-2a713c1618bf
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ac85a62853cf95dcf42380c76b914f23045152b32499870182a47ee2449e8ed1
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119094702"
---
# <a name="process-memory-usage-information"></a>Verarbeiten von Speicherauslastungsinformationen

Die [**GetProcessMemoryInfo-Funktion**](/windows/desktop/api/Psapi/nf-psapi-getprocessmemoryinfo) verwendet ein Prozesshandle als Eingabe und füllt eine [**PROCESS MEMORY \_ \_ COUNTERS-Struktur**](/windows/desktop/api/Psapi/ns-psapi-process_memory_counters) mit Informationen über die Speicherstatistiken für den Prozess aus. Der **cb-Member** empfängt die Größe der -Struktur. Das **PageFaultCount-Element** empfängt die Anzahl der Seitenfehler. Die verbleibenden Member erhalten die aktuelle und die maximale Arbeitsspeicherauslastung in den folgenden Kategorien:

-   Arbeitssatz
-   Ausgelagerungspool
-   Nicht ausgelagerte Pools
-   Auslagerungsdatei

Der *Arbeitssatz* ist die Menge des Arbeitsspeichers, der dem Prozesskontext zu einem bestimmten Zeitpunkt physisch zugeordnet ist. Arbeitsspeicher im *ausgelagerten Pool* ist Systemspeicher, der an die Auslagerungsdatei auf dem Datenträger (ausgelagert) übertragen werden kann, wenn er nicht verwendet wird. Arbeitsspeicher im *nicht ausgelagerten Pool* ist Systemspeicher, der nicht auf den Datenträger ausgelagert werden kann, solange die entsprechenden Objekte zugeordnet sind. Die Verwendung der *Auslagerungsdatei* gibt an, wie viel Arbeitsspeicher für den Prozess in der Auslagerungsdatei des Systems vorgesehen ist. Wenn die Arbeitsspeicherauslastung zu hoch ist, wählt der Manager für virtuellen Arbeitsspeicher die Option Arbeitsspeicher auf Datenträger aus. Wenn ein Thread eine Seite benötigt, die sich nicht im Arbeitsspeicher befindet, lädt der Speicher-Manager sie erneut aus der Auslagerungsdatei.

 

 




