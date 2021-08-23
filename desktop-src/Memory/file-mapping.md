---
description: Die Dateizuordnung ist die Zuordnung des Inhalts einer Datei zu einem Teil des virtuellen Adressraums eines Prozesses.
ms.assetid: 86a8bc81-914d-46a2-99fd-65dfd03bbcdd
title: Dateizuordnung
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8efa02b7de4565adc6ec9cc4c252a7b3114169f1897a2950340a492035409008
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119067854"
---
# <a name="file-mapping"></a>Dateizuordnung

*Dateizuordnung* ist die Zuordnung des Inhalts einer Datei zu einem Teil des virtuellen Adressraums eines Prozesses. Das System erstellt ein *Dateizuordnungsobjekt* (auch als *Abschnittsobjekt bezeichnet),* um diese Zuordnung zu verwalten. Eine *Dateiansicht ist* der Teil des virtuellen Adressraums, den ein Prozess für den Zugriff auf den Inhalt der Datei verwendet. Die Dateizuordnung ermöglicht es dem Prozess, sowohl zufällige Ein- und Ausgaben (E/A) als auch sequenzielle E/A zu verwenden. Außerdem kann der Prozess effizient mit einer großen Datendatei wie einer Datenbank arbeiten, ohne die gesamte Datei dem Arbeitsspeicher zuordnen zu müssen. Mehrere Prozesse können auch speicherzuordnungsbasierte Dateien verwenden, um Daten gemeinsam zu nutzen.

Prozesse, die aus der Dateiansicht lesen und in die Dateiansicht schreiben, mit Zeigern, genau wie bei dynamisch zugewiesenen Arbeitsspeicher. Die Verwendung der Dateizuordnung verbessert die Effizienz, da sich die Datei auf dem Datenträger befindet, die Dateiansicht sich jedoch im Arbeitsspeicher befindet. Prozesse können die Dateiansicht auch mit der [**VirtualProtect-Funktion**](/windows/win32/api/memoryapi/nf-memoryapi-virtualprotect) bearbeiten.

Die folgende Abbildung zeigt die Beziehung zwischen der Datei auf dem Datenträger, einem Dateizuordnungsobjekt und einer Dateiansicht.

![Beziehung zwischen der Datei auf dem Datenträger, einem Dateizuordnungsobjekt und einer Dateiansicht.](images/fmap.png)

Die Datei auf dem Datenträger kann eine beliebige Datei sein, die Sie dem Arbeitsspeicher zuordnen möchten, oder die Systemseitendatei. Das Dateizuordnungsobjekt kann aus der Ganzen oder nur einem Teil der Datei bestehen. Sie wird durch die Datei auf dem Datenträger gespeichert. Dies bedeutet, dass alle Änderungen, die am Dateizuordnungsobjekt vorgenommen werden, in die Datei geschrieben werden, wenn das System Seiten des Dateizuordnungsobjekts austauscht. Wenn die Seiten des Dateizuordnungsobjekts zurück getauscht werden, werden sie aus der Datei wiederhergestellt.

Eine Dateiansicht kann aus dem ganzen oder nur einem Teil des Dateizuordnungsobjekts bestehen. Ein Prozess bearbeitet die Datei über die Dateiansichten. Ein Prozess kann mehrere Ansichten für ein Dateizuordnungsobjekt erstellen. Die von jedem Prozess erstellten Dateiansichten befinden sich im virtuellen Adressraum dieses Prozesses. Wenn der Prozess Daten aus einem anderen Teil der Datei als dem in der aktuellen Dateiansicht benötigt, kann die Aktuelle Dateiansicht entfernt und dann eine neue Dateiansicht erstellt werden.

Wenn mehrere Prozesse dasselbe Dateizuordnungsobjekt verwenden, um Ansichten für eine lokale Datei zu erstellen, sind die Daten einheitlich. Das heißt, die Ansichten enthalten identische Kopien der Datei auf dem Datenträger. Die Datei kann sich nicht auf einem Remotecomputer befinden, wenn Sie Arbeitsspeicher für mehrere Prozesse freigeben möchten.

Weitere Informationen finden Sie in den folgenden Themen:

-   [Erstellen eines Dateizuordnungsobjekts](creating-a-file-mapping-object.md)
-   [Erstellen einer Dateiansicht](creating-a-file-view.md)
-   [Freigeben von Dateien und Arbeitsspeicher](sharing-files-and-memory.md)
-   [Lesen und Schreiben aus einer Dateiansicht](reading-and-writing-from-a-file-view.md)
-   [Schließen eines Dateizuordnungsobjekts](closing-a-file-mapping-object.md)
-   [Sicherheit und Zugriffsrechte für die Dateizuordnung](file-mapping-security-and-access-rights.md)
-   [Verwenden der Dateizuordnung](using-file-mapping.md)

 

 
