---
description: Entwickler erstellen ein Patchpaket, indem Sie eine Datei für die Patcherstellung erzeugen und Msimsp.exe verwenden, um die uikreatepatchpackageex-Funktion in Patchwiz.dll aufzurufen.
ms.assetid: 8a163653-6ba1-46ea-9832-f998749d29ae
title: Erstellen eines Patchpakets
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2561cb6729dc7b4e0e48acd13b6338f08a8ba943
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "104216379"
---
# <a name="creating-a-patch-package"></a>Erstellen eines Patchpakets

Entwickler erstellen ein Patchpaket, indem Sie eine Datei für die Patcherstellung erzeugen und [Msimsp.exe](msimsp-exe.md) verwenden, um die [uikreatepatchpackageex](uicreatepatchpackageex--patchwiz-dll-.md) -Funktion in [Patchwiz.dll](patchwiz-dll.md)aufzurufen. Msimsp.exe und Patchwiz.dll werden im Windows Installer SDK bereitgestellt. Weitere Informationen finden Sie unter [Beispiel für ein kleines Update-Patching](a-small-update-patching-example.md).

Da die Anwendung eines Patches für ein Windows Installer Paket zur Installation der ursprünglichen Quellen mit einer neuen MSI-Datei führt, muss die neue MSI-Datei mit dem Layout der ursprünglichen Quelle kompatibel bleiben.

Wenn Sie ein Patchpaket erstellen, müssen Sie ein nicht komprimiertes Setup Abbild verwenden, um einen Patch zu erstellen, z. b. ein administratives Image oder ein nicht komprimiertes Setup Abbild von einer CD-ROM. Außerdem müssen Sie die folgenden Einschränkungen einhalten:

-   Verschieben Sie keine Dateien aus einem Ordner in einen anderen.
-   Verschieben Sie Dateien nicht aus einer CAB-Datei in eine andere.
-   Ändern Sie die Reihenfolge der Dateien in einer CAB-Datei nicht.
-   Ändern Sie nicht die Sequenznummer vorhandener Dateien. Die Sequenznummer ist der Wert, der in der Sequence-Spalte der [File-Tabelle](file-table.md)angegeben ist.
-   Alle neuen Dateien, die vom Patch hinzugefügt werden, müssen am Ende der vorhandenen Datei Sequenz abgelegt werden. Die Sequenznummer einer neuen Datei im aktualisierten Image muss größer als die größte Sequenznummer vorhandener Dateien im Zielbild sein.
-   Ändern Sie die Primärschlüssel in der [Dateitabelle](file-table.md) nicht zwischen den ursprünglichen und neuen MSI-Dateiversionen.
    > [!Note]  
    > Die Datei muss den gleichen Schlüssel in der [Dateitabelle](file-table.md) sowohl für das Ziel Image als auch für das aktualisierte Image aufweisen. Die Zeichen folgen Werte in der Datei Spalte beider Tabellen müssen identisch sein, einschließlich der Groß-/Kleinschreibung.

     

-   Erstellen Sie kein Paket mit [Datei Tabellen](file-table.md) Schlüsseln, die sich nur in der Groß-/Kleinschreibung unterscheiden. vermeiden Sie z. b. das folgende Tabellen Beispiel.

    

    | File       | Komponente\_ | FileName   |
    |------------|-------------|------------|
    | ReadMe.txt | Comp1       | ReadMe.txt |
    | ReadMe.txt | Comp2       | ReadMe.txt |

    

     

    Der Windows Installer kann das Beispiel der vorherigen Tabelle zulassen, wenn Comp1 und Comp2 in unterschiedlichen Verzeichnissen installiert sind. Sie können jedoch [Msimsp.exe](msimsp-exe.md) oder [Patchwiz.dll](patchwiz-dll.md) nicht verwenden, um einen Patch für das Paket zu generieren. Msimsp.exe und Patchwiz.dll Makecab.exe aufgerufen, bei dem die Groß-und Kleinschreibung nicht beachtet wird.

    Wenn Sie beim Setup Zusammenführungs Module verwenden, stellen Sie sicher, dass die oben aufgeführten Richtlinien von Datei Sequenznummern und-Layout befolgt werden.

 

 



