---
description: Die Tabelle Datei enthält eine vollständige Liste aller Quelldateien für die Installation.
ms.assetid: 481fdc45-82db-4128-93de-388562f636e9
title: Sortieren von Dateisequenznummern in einem Schränk, einer Dateitabelle und einer Medientabelle
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 87f64558a570c7184da36feba8aeea6d2a7dc32c0d8add4c6963dece131c4849
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119327866"
---
# <a name="ordering-file-sequence-numbers-in-a-cabinet-file-table-and-media-table"></a>Sortieren von Dateisequenznummern in einem Schränk, einer Dateitabelle und einer Medientabelle

Die [Tabelle Datei](file-table.md) enthält eine vollständige Liste aller Quelldateien für die Installation. Dateien können auf dem Quellmedium als einzelne Dateien gespeichert oder in [Cab-Dateien](cabinet-files.md)komprimiert werden. Die Sequenznummern in der Spalte Sequenz der Dateitabelle geben zusammen mit dem Feld LastSequence der [Tabelle Media](media-table.md)sowohl die Reihenfolge der Installation für Dateien als auch die Quellmedien an, auf denen sich die einzelnen Dateien befinden. Jeder Datensatz in der Tabelle Media identifiziert den Quelldatenträger, der alle Dateien enthält, deren Sequenznummern kleiner oder gleich dem wert sind, der in der Spalte LastSequence angezeigt wird und größer als der LastSequence-Wert des vorherigen Datenträgers ist.

Angenommen, eine Datei enthält eine Sequenznummer von 92, die in die Spalte Sequenz der Dateitabelle eingegeben wurde. Um zu ermitteln, auf welchem Quelldatenträger sich diese Datei befindet, überprüft das Installationsprogramm den Datensatz der Tabelle Media auf den Eintrag mit dem kleinsten LastSequence-Wert, der größer als 92 ist. Die DiskId-Spalte ist der Primärschlüssel für die Media-Tabelle, und dieses Feld identifiziert den Datenträger in der Tabelle eindeutig.

Die maximale Anzahl von Dateien, die in der Dateitabelle eines Windows Installer-Pakets aufgeführt werden können, beträgt 32767 Dateien. Informationen zum Erstellen eines Windows Installer-Pakets mit weiteren Dateien finden Sie unter [Erstellen eines großen Pakets.](authoring-a-large-package.md)

Paketautoren können die Größe ihrer Installationspakete reduzieren, indem sie die Quelldateien komprimieren und in Cab-Dateien einschließen. Das Quelldateiimage kann komprimiert, nicht komprimiert oder eine Mischung aus beiden Typen sein. Weitere Informationen zu komprimierten und nicht komprimierten Quellen finden Sie unter [Komprimierte und unkomprimierte Quellen.](compressed-and-uncompressed-sources.md) Komprimierte Quelldateien müssen in einer Cab-Datei gespeichert werden. Die komprimierten Dateien in einem Schränk verfügen über eigene interne Sequenznummern. Die Werte dieser internen Sequenznummern müssen nicht mit dem Wert der Sequenznummern in der Dateitabelle übereinstimmen. Die Sequenz der in der Dateitabelle angegebenen Dateien muss jedoch mit der tatsächlichen Sequenz der Dateien in den Schränken identisch sein. Die Sequenznummern von nicht komprimierten Dateien müssen nicht eindeutig sein. Wenn beispielsweise alle Dateien unkomprimiert sind und sich auf einem Datenträger befinden, können alle Dateien die gleiche Sequenznummer in der Dateitabelle aufweisen.

In der Tabelle Medien werden die Datenträger beschrieben, aus denen sich die Quellmedien für die Installation zusammensetzen. Der erste Eintrag in der Tabelle Media muss immer eine 1 im Feld DiskId enthalten. Dateien sollten auf den Quellmedien so organisiert werden, dass alle Dateien auf Datenträger 1 dateitabellensequenznummern aufweisen, die kleiner sind als die Sequenznummern von Dateien auf Datenträger 2, und alle Sequenznummern auf Datenträger 2 sollten kleiner als auf Datenträger 3 usw. sein. Diese Anforderung gilt auch für einen Datenträger, der sowohl komprimierte als auch nicht komprimierte Quellen enthält. Wenn sich die Medienquellen für die Installation z. B. auf zwei Quelldatenträgern befinden und Datenträger 1 sowohl nicht komprimierte Dateien als auch eine Cab-Datei enthält, müssen beide nicht komprimierten Dateien und die Dateien im Schränk eine Sequenznummer aufweisen, die kleiner als die kleinste Dateisequenznummer einer dateigespeicherten Datei auf Datenträger 2 ist. Wenn alle Dateien auf Datenträger 1 in einer Cab-Datei komprimiert sind, kann die Medientabelle wie in der folgenden Tabelle dargestellt erstellt werden.

[Medientabelle](media-table.md) (partiell)



| DiskId | LastSequence | DiskPrompt | Kabinett   | VolumeLabel |
|--------|--------------|------------|-----------|-------------|
| 1      | 5            | 1          | mycab.cab | Datenträger 1      |
| 2      | 10           | 2          |           | Datenträger 2      |



 

Wenn einige Dateien auf Datenträger 1 in einem Schränk komprimiert und einige nicht komprimiert sind, kann die Medientabelle wie folgt erstellt werden.

[Medientabelle](media-table.md) (partiell)



| DiskId | LastSequence | DiskPrompt | Kabinett   | VolumeLabel |
|--------|--------------|------------|-----------|-------------|
| 1      | 5            | 1          |           | Datenträger 1      |
| 2      | 10           | 1          | mycab.cab | Datenträger 1      |
| 3      | 15           | 2          |           | Datenträger 2      |



 

Beachten Sie, dass die Erstellung in der folgenden Medientabelle falsch ist, da sie einige Dateisequenznummern auf Datenträger 2 angibt, die kleiner sind als einige Dateien im Cab auf Datenträger 1.

[Medientabelle](media-table.md)



| DiskId | LastSequence | DiskPrompt | Kabinett   | VolumeLabel |
|--------|--------------|------------|-----------|-------------|
| 1      | 5            | 1          |           | Datenträger 1      |
| 2      | 10           | 2          |           | Datenträger 2      |
| 3      | 15           | 1          | mycab.cab | Datenträger 1      |



 

Große Dateien können auf zwei oder mehr Cab-Dateien aufgeteilt werden. Es dürfen nicht mehr als 15 Dateien in einer Schränkdatei vorhanden sein, die sich auf die nächste Cab-Datei erstreckt. Wenn Sie z. B. über drei Cab-Dateien verfügen, kann das erste Schränke 15 Dateien enthalten, die sich auf die zweite Schränkdatei erstrecken, und das zweite kann 15 Dateien enthalten, die sich auf die dritte Cab-Datei erstrecken. Wenn Sie der Dateitabelle einen Datensatz für mehrere Schränke einer Datei hinzufügen, verwenden Sie den ersten Teil der Datei, um die Dateisequenznummer anzugeben, die Sie in der Spalte Sequenz eingeben.

Die Datei- und Medientabellen können wie folgt erstellt werden, wenn drei Dateien, zwei Schränke und zwei Datenträger vorhanden sind. In diesem Beispiel befindet sich c1.cab auf Disk1 und c2.cab auf disk2. Die Datei f2 umfasst beide Schränke. Der c1.cab Cab enthält die gesamte f1-Datei und den ersten Teil der Datei f2. Der c2.cab Cab enthält den zweiten Teil von f2 und die gesamte f3-Datei.

[Medientabelle](media-table.md) (partiell)



| DiskId | LastSequence | DiskPrompt | Kabinett | VolumeLabel |
|--------|--------------|------------|---------|-------------|
| 1      | 5            | 1          | c1.cab  | Datenträger 1      |
| 2      | 10           | 2          | c2.cab  | Datenträger 2      |



 

[Dateitabelle](file-table.md) (partiell)



| Datei | Sequenz |
|------|----------|
| f1   | 1        |
| f2   | 2        |
| f3   | 6        |



 

 

 



