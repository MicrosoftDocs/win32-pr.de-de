---
description: Entwickler erstellen ein Patchpaket, indem sie eine Patcherstellungsdatei generieren und Msimsp.exe die UiCreatePatchPackageEx-Funktion in Patchwiz.dll.
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

Entwickler erstellen ein Patchpaket, indem sie eine [](msimsp-exe.md) Patcherstellungsdatei generieren undMsimsp.exeverwenden, um die [UiCreatePatchPackageEx-Funktion](uicreatepatchpackageex--patchwiz-dll-.md) [in ](patchwiz-dll.md)Patchwiz.dll. Msimsp.exe und Patchwiz.dll werden im Windows Installer SDK bereitgestellt. Weitere Informationen finden Sie unter [Beispiel für ein kleines Updatepatching.](a-small-update-patching-example.md)

Da die Anwendung eines Patches auf ein Windows Installer-Paket zur Installation der ursprünglichen Quellen mithilfe einer neuen .msi-Datei führt, muss die neue .msi-Datei mit dem Layout der ursprünglichen Quelle kompatibel bleiben.

Wenn Sie ein Patchpaket erstellen, müssen Sie ein nicht komprimiertes Setupimage verwenden, um einen Patch zu erstellen, z. B. ein administratives Image oder ein nicht komprimiertes Setupimage aus einer CD-ROM. Sie müssen auch die folgenden Einschränkungen einhalten:

-   Verschieben Sie keine Dateien aus einem Ordner in einen anderen.
-   Verschieben Sie keine Dateien von einem Schränk in ein anderes.
-   Ändern Sie die Reihenfolge der Dateien in einem Schränk nicht.
-   Ändern Sie nicht die Sequenznummer vorhandener Dateien. Die Sequenznummer ist der Wert, der in der Sequence -Spalte der [Dateitabelle angegeben ist.](file-table.md)
-   Alle neuen Dateien, die durch den Patch hinzugefügt werden, müssen am Ende der vorhandenen Dateisequenz platziert werden. Die Sequenznummer einer neuen Datei im aktualisierten Image muss größer als die größte Sequenznummer vorhandener Dateien im Zielimage sein.
-   Ändern Sie die Primärschlüssel in der [Dateitabelle](file-table.md) nicht zwischen den ursprünglichen und .msi Dateiversionen.
    > [!Note]  
    > Die Datei muss denselben Schlüssel in der Dateitabelle [des](file-table.md) Zielimages und des aktualisierten Images haben. Die Zeichenfolgenwerte in der File -Spalte beider Tabellen müssen identisch sein, einschließlich des Falls.

     

-   Erstellen Sie kein [](file-table.md) Paket mit Dateitabellenschlüsseln, die sich nur in dem Fall unterscheiden, z. B. vermeiden Sie das folgende Tabellenbeispiel.

    

    | Datei       | Komponente\_ | FileName   |
    |------------|-------------|------------|
    | ReadMe.txt | Comp1       | ReadMe.txt |
    | ReadMe.txt | Comp2       | ReadMe.txt |

    

     

    Der Windows Installer kann das vorherige Tabellenbeispiel zulassen, wenn Comp1 und Comp2 in verschiedenen [](msimsp-exe.md) Verzeichnissen installiert sind. Anschließend können SieMsimsp.exeoder [Patchwiz.dll](patchwiz-dll.md) nicht verwenden, um einen Patch für das Paket zu generieren. Msimsp.exe und Patchwiz.dll aufruft Makecab.exe, bei dem die Groß-/Kleinschreibung nicht beachtet wird und ein Fehler auftritt.

    Stellen Sie bei Verwendung von Mergemodulen im Setup sicher, dass dateisequenznummern und das Layout den oben genannten Richtlinien entsprechen.

 

 



