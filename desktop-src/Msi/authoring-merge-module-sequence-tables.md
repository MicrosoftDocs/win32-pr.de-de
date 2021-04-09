---
description: Fügen Sie die mergemodulesequence-Tabellen in die MSM-Datei ein, wenn das Mergemodul die Aktions Sequenz Tabellen der MSI-Ziel Datei ändern muss. Beim Zusammenführen werden diese Tabellen nicht der MSI-Datei hinzugefügt. Diese Tabellen treten nur in Mergemodulen auf.
ms.assetid: 9efb75d2-43f9-404c-8e7f-918d056190cf
title: Erstellen von Mergemodul-Sequenz Tabellen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 24b21780601e626c006967cefa0dcff5700bdec4
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "103959514"
---
# <a name="authoring-merge-module-sequence-tables"></a>Erstellen von Mergemodul-Sequenz Tabellen

Fügen Sie die mergemodulesequence-Tabellen in die MSM-Datei ein, wenn das Mergemodul die Aktions [*Sequenz Tabellen*](s-gly.md) der MSI-Ziel Datei ändern muss. Beim Zusammenführen werden diese Tabellen nicht der MSI-Datei hinzugefügt. Diese Tabellen treten nur in Mergemodulen auf.

Wenn eine der modulesequence-Tabellen in einer MSM-Datei vorhanden ist, muss auch eine leere Kopie der entsprechenden Installer-Sequenz Tabelle in das Mergemodul geschrieben werden. Wenn ein Mergemodul z. b. eine moduleadminexecutesequence-Tabelle enthält, muss das Mergemodul auch eine leere AdminExecuteSequence-Tabelle einschließen. Während eines Mergevorgangs stellen diese leeren Tabellen dem Zusammenführungs Tool die erforderlichen Schema Richtlinien bereit.

Bei Verwendung von [Standard Aktionen](standard-actions.md) in Mergemodul-Sequenz Tabellen sollte der Wert in der Sequence-Spalte die empfohlene Aktions Sequenznummer für die Standardaktion sein. In den unten angegebenen Aktions Sequenzen finden Sie die empfohlenen Sequenznummern in den einzelnen Sequenz Tabellen. Wenn sich die Sequenznummer in der Sequenz Tabelle des Mergemoduls von der Sequenznummer für die gleiche Aktion in der MSI-Datei unterscheidet, verwendet das Mergetool die Sequenznummer in der MSI-Datei während des Mergevorgangs.



| Mergemodulesequence-Tabelle                                                    | Empfohlene Aktions Sequenzen                                             |
|------------------------------------------------------------------------------|--------------------------------------------------------------------------|
| [Moduleadminuisequence](moduleadminuisequence-table.md)                     | [Vorgeschlagene AdminUISequence](suggested-adminuisequence.md)               |
| [Moduleadminexecutesequence](moduleadminexecutesequence-table.md)           | [Vorgeschlagene AdminExecuteSequence](suggested-adminexecutesequence.md)     |
| [Moduleadvtuisequence](moduleadvtuisequence-table.md)                       | [Vorgeschlagene advtuisequence](suggested-advtuisequence.md)                 |
| [Moduleadvtexecutesequence](moduleadvtexecutesequence-table.md)             | [Vorgeschlagene AdvtExecuteSequence](suggested-advtexecutesequence.md)       |
| [Moduleinstalluisequence](moduleinstalluisequence-table.md)                 | [Vorgeschlagene InstallUISequence](suggested-installuisequence.md)           |
| [Moduleinstallexecutesequence-Tabelle](moduleinstallexecutesequence-table.md) | [Empfohlene InstallExecuteSequence](suggested-installexecutesequence.md) |



 

Wenn eine [Standardaktion](standard-actions.md) in der Aktionsspalte einer mergemodulsequenz-Tabelle verwendet wird, müssen die baseaction-und After-Spalten dieses Datensatzes Null sein.

Wenn eine benutzerdefinierte Aktion oder ein benutzerdefiniertes Dialogfeld in die Aktionsspalte eingegeben wird, muss die Sequenz Spalte NULL sein.

Wenn eine Aktion, die ein Beendigungs Flag zurückgibt, in die Aktionsspalte eingegeben wird, sollte die Sequenz Spalte den negativen Wert für dieses Flag enthalten, und die baseaction-und After-Spalten dieses Datensatzes müssen NULL sein. Die folgenden negativen Werte geben an, dass die Aktion aufgerufen wird, wenn das Installationsprogramm das terminierungsflag zurückgibt.



| Beendigungs Flag          | Wert | BESCHREIBUNG              |
|---------------------------|-------|--------------------------|
| msidoaktionstatus-Erfolg  | -1    | Erfolgreicher Abschluss.   |
| msidoaktionstatus ususerexit | -2    | Der Benutzer beendet die Installation. |
| msidoaktionstatus-Fehler  | -3    | Schwerwiegender Exit wird beendet.   |
| msidoaktionstatus-Suspend  | –4    | Die Installation wurde angehalten.    |



 

Die baseaction-Spalte kann eine Standardaktion, eine benutzerdefinierte Aktion, die in der benutzerdefinierten Aktionstabelle des Merge-Moduls angegeben ist, oder ein Dialogfeld enthalten, das in der Dialog Tabelle des Moduls angegeben ist. Die baseaction-Spalte ist ein Schlüssel in der Aktionsspalte dieser Tabelle. Dabei kann es sich nicht um einen Fremdschlüssel in einer anderen MERGE-Tabelle oder-Tabelle in der MSI-Datei handeln. Dies bedeutet, dass jede Standardaktion, benutzerdefinierte Aktion oder ein Dialogfeld, das in der Spalte baseaction aufgeführt ist, auch in der Aktionsspalte eines anderen Datensatzes in dieser Tabelle aufgeführt werden muss.

 

 



