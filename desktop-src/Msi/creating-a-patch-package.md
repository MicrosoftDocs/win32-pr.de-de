---
description: Entwickler erstellen ein Patchpaket, indem sie eine Patcherstellungsdatei generieren und Msimsp.exe verwenden, um die UiCreatePatchPackageEx-Funktion in Patchwiz.dll aufzurufen.
ms.assetid: 8a163653-6ba1-46ea-9832-f998749d29ae
title: Erstellen eines Patchpakets
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5b2d784e02374eeee84a0c8b047e5a7b4db31f9c2b3090a68c31f35dece8c978
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118638290"
---
# <a name="creating-a-patch-package"></a>Erstellen eines Patchpakets

Entwickler erstellen ein Patchpaket, indem sie eine Patcherstellungsdatei generieren und [Msimsp.exe](msimsp-exe.md) verwenden, um die [UiCreatePatchPackageEx-Funktion](uicreatepatchpackageex--patchwiz-dll-.md) in [Patchwiz.dll](patchwiz-dll.md)aufzurufen. Msimsp.exe und Patchwiz.dll werden im Windows Installer SDK bereitgestellt. Weitere Informationen finden Sie unter Beispiel für [ein kleines Updatepatching.](a-small-update-patching-example.md)

Da die Anwendung eines Patches auf ein Windows Installer-Paket zur Installation der ursprünglichen Quellen mithilfe einer neuen .msi-Datei führt, muss die neue .msi-Datei mit dem Layout der ursprünglichen Quelle kompatibel bleiben.

Wenn Sie ein Patchpaket erstellen, müssen Sie ein nicht komprimiertes Setupimage verwenden, um einen Patch zu erstellen, z. B. ein Administratives Image oder ein nicht komprimiertes Setupimage von einer CD-ROM. Sie müssen auch die folgenden Einschränkungen einhalten:

-   Verschieben Sie Dateien nicht aus einem Ordner in einen anderen.
-   Verschieben Sie Dateien nicht aus einem Schränk in einen anderen.
-   Ändern Sie nicht die Reihenfolge der Dateien in einem Schränk.
-   Ändern Sie nicht die Sequenznummer vorhandener Dateien. Die Sequenznummer ist der Wert, der in der Sequenzspalte der [Dateitabelle](file-table.md)angegeben ist.
-   Alle neuen Dateien, die vom Patch hinzugefügt werden, müssen am Ende der vorhandenen Dateisequenz platziert werden. Die Sequenznummer einer beliebigen neuen Datei im aktualisierten Image muss größer als die größte Sequenznummer der vorhandenen Dateien im Zielimage sein.
-   Ändern Sie die Primärschlüssel in der [Dateitabelle](file-table.md) nicht zwischen der ursprünglichen und der neuen .msi Dateiversion.
    > [!Note]  
    > Die Datei muss in der [Dateitabelle](file-table.md) des Zielimages und des aktualisierten Images denselben Schlüssel aufweisen. Die Zeichenfolgenwerte in der Spalte Datei beider Tabellen müssen identisch sein, einschließlich der Fall.

     

-   Erstellen Sie kein [](file-table.md) Paket mit Dateitabellenschlüsseln, die sich nur für den Fall unterscheiden, z. B. vermeiden Sie das folgende Tabellenbeispiel.

    

    | Datei       | Komponente\_ | FileName   |
    |------------|-------------|------------|
    | ReadMe.txt | Comp1       | ReadMe.txt |
    | ReadMe.txt | Comp2       | ReadMe.txt |

    

     

    Der Windows Installer kann das vorherige Tabellenbeispiel zulassen, wenn Comp1 und Comp2 in verschiedenen Verzeichnissen installiert sind. Anschließend können Sie jedoch [Msimsp.exe](msimsp-exe.md) oder [Patchwiz.dll](patchwiz-dll.md) nicht verwenden, um einen Patch für das Paket zu generieren. Msimsp.exe und Patchwiz.dll aufruft Makecab.exe, bei dem die Groß-/Kleinschreibung nicht beachtet wird und ein Fehler auftritt.

    Wenn Sie Mergemodule im Setup verwenden, stellen Sie sicher, dass die Dateisequenznummern und das Layout den oben genannten Richtlinien entsprechen.

 

 



