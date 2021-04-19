---
description: ICE18 überprüft, ob alle leeren Verzeichnisse, die als Schlüssel Pfad für eine Komponente verwendet werden, in der Tabelle "| atefolder" aufgeführt sind.
ms.assetid: de31b893-831b-4a6d-809a-c4a3056b8a66
title: ICE18
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a60a3032a285604197e4c0bfda4225d519b0b744
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106350488"
---
# <a name="ice18"></a>ICE18

ICE18 überprüft, ob alle leeren Verzeichnisse, die als Schlüssel Pfad für eine Komponente verwendet werden, in der Tabelle "| [atefolder](createfolder-table.md)" aufgeführt sind.

Wenn die KEYPATH-Spalte der [Komponenten Tabelle](component-table.md) NULL ist, bedeutet dies, dass das in der Spalte Verzeichnis aufgeführte Verzeichnis \_ der Schlüssel Pfad für diese Komponente ist. Da Ordner, die vom Installationsprogramm erstellt werden, gelöscht werden, wenn Sie leer sind, muss dieser Ordner in der [Tabelle](createfolder-table.md) "" erstellt werden, um zu verhindern, dass das Installationsprogramm jedes Mal versucht, eine Installation durchzuführen.

Machen Sie das Verzeichnis System Folder nicht zum Schlüssel Pfad einer Komponente. Da dieser Ordner auf jedem Betriebssystem vorhanden ist, erkennt das Installationsprogramm immer den Schlüssel Pfad, unabhängig davon, ob die Komponente vorhanden ist. In diesem Fall sollte der Schlüssel Pfad eine Datei, ein Registrierungs Eintrag oder eine ODBC-Datenquelle sein.

Beim Durchführen einer Validierung wird zuerst überprüft, ob Folgendes zutrifft:

-   Die KEYPATH-Spalte der [Component-Tabelle](component-table.md) enthält einen NULL-Wert.
-   Es sind keine Dateien für die Komponente in der [Dateitabelle](file-table.md)aufgeführt.
-   Es sind keine Dateien für die in der [Tabelle "RemoveFile](removefile-table.md) " aufgeführte Komponente vorhanden, und der Wert in "dirproperty" ist mit der Verzeichnis \_ Spalte der [Komponenten Tabelle](component-table.md)identisch.
-   Es sind keine Dateien für die in der [duplicatefile-Tabelle](duplicatefile-table.md) aufgeführte Komponente vorhanden, und der Wert im Ordner "destfolder" ist mit der Verzeichnis \_ Spalte der [Komponenten Tabelle](component-table.md)identisch.
-   Es sind keine Dateien für die in der [Tabelle "muvefile](movefile-table.md) " aufgeführten Komponenten vorhanden, und der Wert im Ordner "destfolder" ist mit der Verzeichnis \_ Spalte der [Komponenten Tabelle](component-table.md)identisch.

Wenn diese alle zutreffen, überprüft ICE18 Folgendes:

-   Die Komponenten \_ Spalte der Tabelle "| [atefolder](createfolder-table.md) " weist den gleichen Wert auf wie die Komponenten Spalte der [Komponenten Tabelle](component-table.md).
-   Die Verzeichnis \_ Spalte der Tabelle "| atefolder" hat denselben Wert wie die Verzeichnis \_ Spalte der [Komponenten Tabelle](component-table.md).

## <a name="result"></a>Ergebnis

ICE18 gibt eine Fehlermeldung aus, wenn das Installationspaket ein Verzeichnis als Schlüssel Pfad für die Komponente angibt, die nicht in der Tabelle "| [atefolder](createfolder-table.md)" aufgeführt ist.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Ice-Referenz](ice-reference.md)
</dt> </dl>

 

 



