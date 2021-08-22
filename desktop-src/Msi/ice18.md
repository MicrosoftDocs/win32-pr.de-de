---
description: ICE18 überprüft, ob alle leeren Verzeichnisse, die als Schlüsselpfad für eine Komponente verwendet werden, in der CreateFolder-Tabelle aufgeführt sind.
ms.assetid: de31b893-831b-4a6d-809a-c4a3056b8a66
title: ICE18
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4ca102e8fdec5e30283cd879ddb5677a2bba79f90ba5a9a790ea50923e0aeedb
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119581140"
---
# <a name="ice18"></a>ICE18

ICE18 überprüft, ob alle leeren Verzeichnisse, die als Schlüsselpfad für eine Komponente verwendet werden, in der [CreateFolder-Tabelle aufgeführt sind.](createfolder-table.md)

Wenn die KeyPath-Spalte der [Component-Tabelle](component-table.md) NULL ist, bedeutet dies, dass das in der Spalte Verzeichnis aufgeführte Verzeichnis der Schlüsselpfad \_ für diese Komponente ist. Da vom Installationsprogramm erstellte Ordner gelöscht werden, wenn sie leer werden, muss dieser Ordner in der [CreateFolder-Tabelle](createfolder-table.md) aufgeführt werden, um zu verhindern, dass das Installationsprogramm jedes Mal versucht, es zu installieren.

Machen Sie das Verzeichnis SystemFolder nicht zum Schlüsselpfad einer Komponente. Da dieser Ordner auf jedem Betriebssystem vorhanden ist, erkennt das Installationsprogramm immer den Schlüsselpfad, unabhängig davon, ob die Komponente vorhanden ist. In diesem Fall sollte der Schlüsselpfad eine Datei, ein Registrierungseintrag oder eine ODBC-Datenquelle sein.

Beim Durchführen einer Validierung überprüft ICE18 zunächst, ob Folgendes zutrifft:

-   Die KeyPath-Spalte der [Component-Tabelle enthält](component-table.md) einen NULL-Wert.
-   Es sind keine Dateien für die Komponente in der [Dateitabelle aufgeführt.](file-table.md)
-   Es gibt keine Dateien für die Komponente, die in der [RemoveFile-Tabelle](removefile-table.md) aufgeführt sind, und dass der Wert in dirProperty mit dem Wert in der Directory -Spalte der \_ [Component-Tabelle identisch ist.](component-table.md)
-   Dass keine Dateien für die Komponente in der [DuplicateFile-Tabelle](duplicatefile-table.md) aufgeführt sind und dass der Wert im DestFolder mit der Directory -Spalte der \_ [Component-Tabelle identisch ist.](component-table.md)
-   Dass keine Dateien für die In der [MoveFile-Tabelle](movefile-table.md) aufgeführte Komponente vorhanden sind und dass der Wert im DestFolder mit der Directory -Spalte der \_ [Component-Tabelle identisch ist.](component-table.md)

Wenn alle zutreffen, überprüft ICE18 Folgendes:

-   Die Spalte Component \_ der [CreateFolder-Tabelle](createfolder-table.md) hat den gleichen Wert wie die Component -Spalte der [Component-Tabelle.](component-table.md)
-   Dass die Directory -Spalte der CreateFolder -Tabelle den gleichen Wert wie \_ die \_ Directory-Spalte der [Component-Tabelle auf hat.](component-table.md)

## <a name="result"></a>Ergebnis

ICE18 gibt eine Fehlermeldung aus, wenn das Installationspaket ein Verzeichnis als Schlüsselpfad für die Komponente angibt, die nicht in der [CreateFolder-Tabelle aufgeführt ist.](createfolder-table.md)

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[ICE-Referenz](ice-reference.md)
</dt> </dl>

 

 



