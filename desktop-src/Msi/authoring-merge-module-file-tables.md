---
description: Eine Dateitabelle ist in jedem Mergemodul erforderlich und sollte einen Datensatz für jede Datei enthalten, die vom Mergemodul an das Zielinstallationspaket übermittelt wird.
ms.assetid: 436933c7-6e5d-4b4e-9147-c60a26871dbe
title: Erstellen von Mergemodul-Dateitabellen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 715fe570a96015f62e45b0c2924b2a83be8eefc067e5d054decd59110b7797c2
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "120045470"
---
# <a name="authoring-merge-module-file-tables"></a>Erstellen von Mergemodul-Dateitabellen

Eine [Dateitabelle](file-table.md) ist in jedem Mergemodul erforderlich und sollte einen Datensatz für jede Datei enthalten, die vom Mergemodul an das Zielinstallationspaket übermittelt wird. Wenn das Mergemodul in einer .msi zusammengeführt wird, wird jede Datei in der Dateitabelle des Mergemoduls in einer [*CABINET-Datei*](c-gly.md) in der MSM-Datei gespeichert. Der Name des Schränkchens in einem Mergemodul ist immer der folgende: MergeModule.CABinet.

Weitere Informationen finden Sie unter [Generating MergeModule.CABinet Cabinet Files](generating-mergemodule-cabinet-cabinet-files.md).

-   Da die Dateien eines Mergemoduls immer in einer cabinet-Datei gespeichert werden, ist es nicht erforderlich, die **msidbFileAttributesNoncompressed-** oder **msidbFileAttributesCompressed-Bitflags** in der Attributes -Spalte der [Dateitabelle zu setzen.](file-table.md)
-   Die Namen der Dateien in MergeModule.CABinet müssen mit dem Primärschlüssel in der Dateitabelle des [Mergemoduls übereinstimmen.](file-table.md)

    Die Spalte Datei ist der [](file-table.md) Primärschlüssel der Dateitabelle, und die Einträge in diesem Feld müssen der Konvention folgen, die unter Naming Primary Keys in Merge Module Databases (Benennen von Primärschlüsseln [in Mergemoduldatenbanken) beschrieben ist.](naming-primary-keys-in-merge-module-databases.md)

-   Dateisequenznummern werden in der Spalte Sequenz der [Dateitabelle angegeben.](file-table.md)

    Dateien müssen in der Dateitabelle des Mergemoduls [in](file-table.md) derselben Reihenfolge aufgeführt werden, in der sie in MergeModule.CABwerden. Die Sequenznummern von Dateien müssen nicht aufeinanderfolgende sein, sie müssen jedoch der gleichen Reihenfolge folgen wie die Dateien, die in der Schränkung gespeichert sind. Beispielsweise kann die erste, zweite und dritte Im Schränk gespeicherte Datei die Sequenznummern 100, 200 und 300 haben.

-   Der Installer überspringt zusätzliche Dateien, die in MergeModule.CABinet enthalten sind, die nicht in der [Dateitabelle aufgeführt sind.](file-table.md)

    Eine Cabinet-Datei kann alle Dateien enthalten, die für ein Mergemodul erforderlich sind, das mehrere Sprachen mithilfe von Transformationen unterstützt. Allen Sprachdateien kann eine eindeutige Sequenznummer in der Schränkung gegeben werden, [](file-table.md) und dann kann eine Transformation Dateien der Dateitabelle hinzufügen oder daraus entfernen, wenn sie für eine bestimmte Sprache benötigt werden. Weitere Informationen finden Sie unter [Erstellen mehrerer Sprachzusammenführungsmodule.](authoring-multiple-language-merge-modules.md)

Weitere Informationen finden Sie unter [Dateitabelle.](file-table.md)

 

 



