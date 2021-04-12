---
description: Die Datei Zuordnung ist die Zuordnung des Inhalts einer Datei zu einem Teil des virtuellen Adressraums eines Prozesses.
ms.assetid: 86a8bc81-914d-46a2-99fd-65dfd03bbcdd
title: Datei Zuordnung
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b7f49162a4545d0e087e6b291e429d89049dbf57
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104526369"
---
# <a name="file-mapping"></a>Datei Zuordnung

Die *Datei Zuordnung* ist die Zuordnung des Inhalts einer Datei zu einem Teil des virtuellen Adressraums eines Prozesses. Das System erstellt ein *Datei* Zuordnungs Objekt (auch als *Abschnitts Objekt* bezeichnet), um diese Zuordnung aufrechtzuerhalten. Eine *Dateiansicht* ist der Teil des virtuellen Adressraums, den ein Prozess verwendet, um auf den Inhalt der Datei zuzugreifen. Die Datei Zuordnung ermöglicht dem Prozess die Verwendung von Zufalls Eingaben und Ausgaben (e/a) und sequenziellen e/a-Vorgängen. Außerdem kann der Prozess mit einer großen Datendatei (z. b. einer Datenbank) effizient arbeiten, ohne dass die gesamte Datei dem Arbeitsspeicher zugeordnet werden muss. Mehrere Prozesse können auch Speicher Abbild Dateien zum Freigeben von Daten verwenden.

Prozesse, die mithilfe von Zeigern aus der Dateiansicht gelesen und in diese geschrieben werden, ebenso wie bei dynamisch zugewiesener Arbeitsspeicher. Die Verwendung der Datei Zuordnung erhöht die Effizienz, da sich die Datei auf dem Datenträger befindet, die Dateiansicht jedoch im Arbeitsspeicher gespeichert ist. Prozesse können die Dateiansicht auch mit der [**VirtualProtect**](/windows/win32/api/memoryapi/nf-memoryapi-virtualprotect) -Funktion bearbeiten.

Die folgende Abbildung zeigt die Beziehung zwischen der Datei auf dem Datenträger, einem Datei Mapping-Objekt und einer Dateiansicht.

![Beziehung zwischen der Datei auf dem Datenträger, einem Datei Mapping-Objekt und einer Dateiansicht.](images/fmap.png)

Bei der Datei auf dem Datenträger kann es sich um eine beliebige Datei handeln, die Sie dem Arbeitsspeicher zuordnen möchten, oder um die System Auslagerungs Datei. Das Datei Zuordnung-Objekt kann aus allen oder nur einem Teil der Datei bestehen. Sie wird von der Datei auf dem Datenträger unterstützt. Dies bedeutet, dass alle Änderungen, die am Datei Zuordnungsobjekt vorgenommen werden, in die Datei geschrieben werden, wenn das System Seiten des Datei Zuordnungsobjekts austauscht. Wenn die Seiten des Datei Zuordnungsobjekts wieder in ausgetauscht werden, werden Sie aus der Datei wieder hergestellt.

Eine Dateiansicht kann aus dem gesamten oder nur einem Teil des Datei Mapping-Objekts bestehen. Ein Prozess manipuliert die Datei über die Datei Ansichten. Ein Prozess kann mehrere Sichten für ein Datei Zuordnung-Objekt erstellen. Die von den einzelnen Prozessen erstellten Datei Sichten befinden sich im virtuellen Adressraum dieses Prozesses. Wenn der Prozessdaten aus einem Teil der Datei benötigt, der nicht der aktuellen Dateiansicht entspricht, kann er die Zuordnung der aktuellen Dateiansicht aufheben und dann eine neue Dateiansicht erstellen.

Wenn mehrere Prozesse das gleiche Datei Zuordnung-Objekt verwenden, um Sichten für eine lokale Datei zu erstellen, sind die Daten kohärent. Das heißt, dass die Ansichten identische Kopien der Datei auf dem Datenträger enthalten. Die Datei darf sich nicht auf einem Remote Computer befinden, wenn Sie Arbeitsspeicher zwischen mehreren Prozessen freigeben möchten.

Weitere Informationen finden Sie unter den folgenden Themen:

-   [Erstellen eines Datei Mapping-Objekts](creating-a-file-mapping-object.md)
-   [Erstellen einer Dateiansicht](creating-a-file-view.md)
-   [Freigeben von Dateien und Arbeitsspeicher](sharing-files-and-memory.md)
-   [Lesen und schreiben aus einer Dateiansicht](reading-and-writing-from-a-file-view.md)
-   [Schließen eines Datei Mapping-Objekts](closing-a-file-mapping-object.md)
-   [Sicherheit und Zugriffsrechte für die Datei Zuordnung](file-mapping-security-and-access-rights.md)
-   [Verwenden der Datei Zuordnung](using-file-mapping.md)

 

 
