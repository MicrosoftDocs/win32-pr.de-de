---
description: Zukünftige Verbesserungen am Winsock-Beispiel Anwendungscode.
ms.assetid: 317baa53-6bc8-42bd-8f56-480cab29ae6b
title: Zukünftige Verbesserungen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 938f38334a4bbe392e83efc0be12905fb7ae66a8
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106345106"
---
# <a name="future-improvements"></a>Zukünftige Verbesserungen

An dieser Anwendung können mehrere Verbesserungen vorgenommen werden, wie z. b.:

-   Eine einzelne, permanente Verbindung konnte von der Anwendung erstellt werden. Die entsprechende Fehlerbehandlung muss hinzugefügt werden. Dadurch wird der Aufwand für das Starten und Löschen der Verbindung reduziert.
-   Der Antwort Code auf dem Server kann zum Konsolidieren von Antworten optimiert werden, wodurch die Anzahl der vom Server gesendeten Pakete reduziert wird.
-   Es können Verbesserungen am Protokoll vorgenommen werden. Beispielsweise könnte eine Update-Bitmaske verwendet werden, um anzugeben, welche Zellen aktualisiert werden sollen, und nur die zu sendenden Zellen Daten.
-   Updates können mithilfe verschiedener Threads überlappen, sodass das Netzwerk nicht im Leerlauf ist, während die **computenext** -Funktion ausgeführt wird.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Verbessern einer langsamen Anwendung](improving-a-slow-application-2.md)
</dt> <dt>

[Baselineversion: eine sehr schlechte leistungsfähige Anwendung](the-baseline-version-a-very-poor-performing-application-2.md)
</dt> <dt>

[Revision 1: Bereinigen der offensichtlichen](revision-1-cleaning-up-the-obvious-2.md)
</dt> <dt>

[Revision 2: Neuentwerfen für eine geringere Anzahl von Verbindungen](revision-2-redesigning-for-fewer-connects-2.md)
</dt> <dt>

[Revision 3: komprimierte Block-Sendevorgang](revision-3-compressed-block-send-2.md)
</dt> </dl>

 

 



