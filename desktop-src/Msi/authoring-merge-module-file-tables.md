---
description: Eine Dateitabelle ist in jedem Mergemodul erforderlich und sollte über einen Datensatz für jede Datei verfügen, die vom Mergemodul an das Ziel Installationspaket übermittelt wird.
ms.assetid: 436933c7-6e5d-4b4e-9147-c60a26871dbe
title: Erstellen von Mergemodul-Datei Tabellen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8e2687ed69c1a0362f96db896a5fdf4237ac4681
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104042154"
---
# <a name="authoring-merge-module-file-tables"></a>Erstellen von Mergemodul-Datei Tabellen

Eine [Dateitabelle](file-table.md) ist in jedem Mergemodul erforderlich und sollte über einen Datensatz für jede Datei verfügen, die vom Mergemodul an das Ziel Installationspaket übermittelt wird. Wenn das Mergemodul in eine MSI-Datei zusammengeführt wird, wird jede Datei in der Dateitabelle des Mergemoduls in einer CAB- [*Datei*](c-gly.md) in der MSM-Datei gespeichert. Der Name der CAB-Module in einem Mergemodul lautet immer wie folgt: MergeModule.CABinet.

Weitere Informationen finden Sie unter [Erstellen von MergeModule.CABinet](generating-mergemodule-cabinet-cabinet-files.md)-CAB-Dateien.

-   Da die Dateien eines Mergemoduls immer in einer CAB-Datei gespeichert werden, ist es nicht erforderlich, die Bitflags **msidbfileattributesnoncompressed** oder **msidbfileattributescompressed** in der Spalte Attribute der [Dateitabelle](file-table.md)festzulegen.
-   Die Namen der Dateien in MergeModule.CABinet müssen mit dem Primärschlüssel in der [Dateitabelle](file-table.md)des Mergemoduls identisch sein.

    Die Datei Spalte ist der Primärschlüssel der [Dateitabelle](file-table.md) , und die Einträge in diesem Feld müssen der Konvention folgen, die unter [Benennen von primär Schlüsseln in mergemoduldatenbanken](naming-primary-keys-in-merge-module-databases.md)beschrieben wird.

-   Datei Sequenznummern werden in der Sequence-Spalte der [File-Tabelle](file-table.md)angegeben.

    Dateien müssen in der [Dateitabelle](file-table.md) des Merge-Moduls in derselben Reihenfolge aufgelistet werden, in der Sie in MergeModule.CABinet gespeichert sind. Die Sequenznummern von Dateien müssen nicht aufeinander folgen, aber Sie müssen derselben Reihenfolge wie die Dateien entsprechen, die in der CAB-Datei gespeichert werden. Beispielsweise können die ersten, zweiten und dritten Dateien, die in der CAB-Datei gespeichert sind, über die Sequenznummer 100, 200 und 300 verfügen.

-   Das Installationsprogramm überspringt zusätzliche Dateien, die in MergeModule.CABinet enthalten sind und nicht in der [Dateitabelle](file-table.md)aufgeführt sind.

    Eine CAB-Datei kann alle Dateien enthalten, die für ein Mergemodul erforderlich sind, das mehrere Sprachen mithilfe von Transformationen unterstützt. Allen Sprachdateien kann eine eindeutige Sequenznummer in der CAB-Datei zugewiesen werden, und dann kann eine Transformation Dateien hinzufügen oder aus der [Dateitabelle](file-table.md) entfernen, wenn dies für eine bestimmte Sprache erforderlich ist. Weitere Informationen finden Sie unter [Erstellen mehrerer sprachmergemodule](authoring-multiple-language-merge-modules.md).

Weitere Informationen finden Sie unter [File Table](file-table.md).

 

 



