---
description: Die Dateitabelle enthält eine vollständige Liste aller Quelldateien für die Installation.
ms.assetid: 481fdc45-82db-4128-93de-388562f636e9
title: Anordnen von Datei Sequenznummern in einer CAB-, File Table-und Media-Tabelle
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 07f9cd530d90fb0ef4d805b8ff2c96398cd97e55
ms.sourcegitcommit: c16214e53680dc71d1c07111b51f72b82a4512d8
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/03/2021
ms.locfileid: "106361770"
---
# <a name="ordering-file-sequence-numbers-in-a-cabinet-file-table-and-media-table"></a>Anordnen von Datei Sequenznummern in einer CAB-, File Table-und Media-Tabelle

Die [Dateitabelle](file-table.md) enthält eine vollständige Liste aller Quelldateien für die Installation. Dateien können auf den Quell Medien als einzelne Dateien gespeichert oder innerhalb von CAB- [Dateien](cabinet-files.md)komprimiert werden. Die Sequenznummern in der Sequence-Spalte der Dateitabelle, zusammen mit dem LastSequence-Feld der [Medien Tabelle](media-table.md), geben sowohl die Reihenfolge der Installation für Dateien als auch das Quell Medium an, auf dem sich die einzelnen Dateien befinden. Jeder Datensatz in der Medien Tabelle identifiziert den Quell Datenträger, der alle Dateien mit den Sequenznummern enthält, die kleiner oder gleich dem in der Spalte LastSequence gezeigten Wert sind, und größer als der LastSequence-Wert des vorherigen Datenträgers.

Nehmen wir beispielsweise an, dass eine Datei in der Sequence-Spalte der Dateitabelle die Sequenznummer 92 eingegeben hat. Um zu ermitteln, auf welchem Quell Datenträger diese Datei gespeichert ist, überprüft das Installationsprogramm den Datensatz der Medien Tabelle auf den Eintrag mit dem kleinsten LastSequence-Wert, der größer als 92 ist. Die DiskId-Spalte ist der Primärschlüssel für die Medien Tabelle, und dieses Feld identifiziert den Datenträger in der Tabelle eindeutig.

Der maximale Grenzwert für die Anzahl der Dateien, die in der Dateitabelle eines Windows Installer Pakets aufgelistet werden können, sind 32767 Dateien. Informationen zum Erstellen eines Windows Installer Pakets, das weitere Dateien enthält, finden Sie unter Erstellen [eines großen Pakets](authoring-a-large-package.md).

Paket Autoren können die Größe ihrer Installationspakete verringern, indem Sie die Quelldateien komprimieren und in CAB-Dateien einschließen. Das Quelldatei Image kann komprimiert, unkomprimiert oder eine Mischung beider Typen sein. Weitere Informationen zu komprimierten und nicht komprimierten Quellen finden Sie unter [komprimierte und nicht komprimierte Quellen](compressed-and-uncompressed-sources.md). Komprimierte Quelldateien müssen in einer CAB-Datei gespeichert werden. Die komprimierten Dateien in einer CAB-Datei verfügen über eigene interne Sequenznummern. Die Werte dieser internen Sequenznummern müssen nicht mit dem Wert der Sequenznummern innerhalb der Dateitabelle verglichen werden. Die Sequenz der in der Dateitabelle angegebenen Dateien muss jedoch mit der tatsächlichen Sequenz der Dateien in den Schränken identisch sein. Die Sequenznummern von nicht komprimierten Dateien müssen nicht eindeutig sein. Wenn z. b. alle Dateien unkomprimiert sind und sich auf einem Datenträger befinden, können alle Dateien in der Dateitabelle die gleiche Sequenznummer aufweisen.

In der Medien Tabelle wird der Satz von Datenträgern beschrieben, aus denen die-Quell Medien für die-Installation gemacht werden. Der erste Eintrag in der Medien Tabelle muss immer über einen Wert von 1 im Feld DiskId verfügen. Dateien sollten auf den Quell Medien angeordnet werden, sodass alle Dateien auf Datenträger 1 Datei Tabellen-Sequenznummern aufweisen, die kleiner sind als die Sequenznummern von Dateien auf Datenträger 2. alle Sequenznummern auf Datenträger 2 sollten kleiner sein als auf Datenträger 3 usw. Diese Anforderung gilt auch für einen Datenträger, der sowohl komprimierte als auch nicht komprimierte Quellen enthält. Wenn sich die Medienquellen für die Installation z. b. auf zwei Quell Datenträgern befinden und Datenträger 1 sowohl nicht komprimierte Dateien als auch eine CAB-Datei enthält, müssen die Sequenznummern der nicht komprimierten Dateien und der Dateien in der CAB-Datei kleiner sein als die kleinste Datei Sequenznummer einer Datei, die auf Datenträger 2 gespeichert ist. Wenn alle Dateien auf Datenträger 1 in einer CAB-Datei komprimiert werden, könnte die Medien Tabelle wie in der folgenden Tabelle gezeigt erstellt werden.

[Medien Tabelle](media-table.md) (partiell)



| DiskId | LastSequence | Diskprompt | KEs   | VolumeLabel |
|--------|--------------|------------|-----------|-------------|
| 1      | 5            | 1          | mycab.cab | Datenträger 1      |
| 2      | 10           | 2          |           | Datenträger 2      |



 

Wenn einige Dateien auf Datenträger 1 in einer CAB-Datei komprimiert sind und einige nicht komprimiert sind, könnte die Medien Tabelle wie folgt erstellt werden.

[Medien Tabelle](media-table.md) (partiell)



| DiskId | LastSequence | Diskprompt | KEs   | VolumeLabel |
|--------|--------------|------------|-----------|-------------|
| 1      | 5            | 1          |           | Datenträger 1      |
| 2      | 10           | 1          | mycab.cab | Datenträger 1      |
| 3      | 15           | 2          |           | Datenträger 2      |



 

Beachten Sie, dass die Erstellung in der folgenden Medien Tabelle falsch ist, da Sie einige Datei Sequenznummern auf Datenträger 2 angibt, die kleiner sind als einige Dateien in der CAB-Datei auf Datenträger 1.

[Medien Tabelle](media-table.md)



| DiskId | LastSequence | Diskprompt | KEs   | VolumeLabel |
|--------|--------------|------------|-----------|-------------|
| 1      | 5            | 1          |           | Datenträger 1      |
| 2      | 10           | 2          |           | Datenträger 2      |
| 3      | 15           | 1          | mycab.cab | Datenträger 1      |



 

Große Dateien können zwischen zwei oder mehr CAB-Dateien aufgeteilt werden. In einer CAB-Datei, die sich auf die nächste CAB-Datei erstreckt, dürfen nicht mehr als 15 Dateien vorhanden sein. Wenn Sie z. b. über drei CAB-Dateien verfügen, kann die erste CAB-Datei 15 Dateien enthalten, die sich in der zweiten CAB-Datei befinden, und der zweite Schrank kann 15 Dateien enthalten, die sich auf die dritte CAB-Datei erstrecken. Wenn Sie der Dateitabelle einen Datensatz für mehrere CAB-Dateien hinzufügen, verwenden Sie den ersten Teil der Datei, um die Datei Sequenznummer anzugeben, die Sie in die Sequenz Spalte eingeben.

Die Datei-und Medien Tabellen können wie folgt erstellt werden, wenn drei Dateien, zwei Schränke und zwei Datenträger vorhanden sind. In diesem Beispiel befindet sich c1.cab auf Disk1, und c2.cab befindet sich auf Disk2. Die Datei F2 umfasst beide Schränke. Die c1.cab CAB-Datei enthält die gesamte F1-Datei und den ersten Teil der Datei F2. Die c2.cab CAB-Datei enthält den zweiten Teil von F2 und die gesamte F3-Datei.

[Medien Tabelle](media-table.md) (partiell)



| DiskId | LastSequence | Diskprompt | KEs | VolumeLabel |
|--------|--------------|------------|---------|-------------|
| 1      | 5            | 1          | c1.cab  | Datenträger 1      |
| 2      | 10           | 2          | c2.cab  | Datenträger 2      |



 

[Dateitabelle](file-table.md) (partiell)



| File | Sequenz |
|------|----------|
| 1   | 1        |
| Drücken   | 2        |
| F3   | 6        |



 

 

 



