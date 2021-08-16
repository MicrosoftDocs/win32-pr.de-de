---
description: Schließen Sie die MergeModuleSequence-Tabellen in die MSM-Datei ein, wenn das Mergemodul die Aktionssequenztabellen der Zieldatei .msi muss. Beim Zusammenführen werden diese Tabellen nicht der .msi hinzugefügt. Diese Tabellen treten nur in Mergemodulen auf.
ms.assetid: 9efb75d2-43f9-404c-8e7f-918d056190cf
title: Erstellen von Mergemodulsequenztabellen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5f45e4cf86c846030854054d7ab700e34210d4e27367cd31d606c78c24f2a9a7
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118381185"
---
# <a name="authoring-merge-module-sequence-tables"></a>Erstellen von Mergemodulsequenztabellen

Schließen Sie die MergeModuleSequence-Tabellen in die MSM-Datei [](s-gly.md) ein, wenn das Mergemodul die Aktionssequenztabellen der Zieldatei .msi muss. Beim Zusammenführen werden diese Tabellen nicht der .msi hinzugefügt. Diese Tabellen treten nur in Mergemodulen auf.

Wenn eine der ModuleSequence-Tabellen in einer MSM-Datei vorhanden ist, muss auch eine leere Kopie der entsprechenden Installationssequenztabelle im Mergemodul erstellt werden. Wenn ein Mergemodul beispielsweise eine ModuleAdminExecuteSequence-Tabelle enthält, muss das Mergemodul auch eine leere AdminExecuteSequence-Tabelle enthalten. Während eines Merges stellen diese leeren Tabellen dem Mergetool die erforderlichen Schemarichtlinien zur Verfügung.

Wenn Sie [Standardaktionen](standard-actions.md) in Mergemodulsequenztabellen verwenden, sollte der Wert in der Spalte Sequenz die empfohlene Aktionssequenznummer für die Standardaktion sein. Die empfohlenen Sequenznummern in den einzelnen Sequenztabellen finden Sie in den unten angegebenen empfohlenen Aktionssequenzen. Wenn sich die Sequenznummer in der Sequenztabelle des Mergemoduls von der Sequenznummer für dieselbe Aktion in der .msi-Datei unterscheidet, verwendet das Mergetool die Sequenznummer in der .msi-Datei während des Merges.



| MergeModuleSequence-Tabelle                                                    | Empfohlene Aktionssequenzen                                             |
|------------------------------------------------------------------------------|--------------------------------------------------------------------------|
| [ModuleAdminUISequence](moduleadminuisequence-table.md)                     | [Vorgeschlagene AdminUISequence](suggested-adminuisequence.md)               |
| [ModuleAdminExecuteSequence](moduleadminexecutesequence-table.md)           | [Vorgeschlagener AdministratorExecuteSequence](suggested-adminexecutesequence.md)     |
| [ModuleAdvtUISequence](moduleadvtuisequence-table.md)                       | [Vorgeschlagene AdvtUISequence](suggested-advtuisequence.md)                 |
| [ModuleAdvtExecuteSequence](moduleadvtexecutesequence-table.md)             | [Vorgeschlagene AdvtExecuteSequence](suggested-advtexecutesequence.md)       |
| [ModuleInstallUISequence](moduleinstalluisequence-table.md)                 | [Empfohlene InstallationUISequence](suggested-installuisequence.md)           |
| [ModuleInstallExecuteSequence-Tabelle](moduleinstallexecutesequence-table.md) | [Vorgeschlagene InstallationExecuteSequence](suggested-installexecutesequence.md) |



 

Wenn eine [Standardaktion](standard-actions.md) in der Action -Spalte einer Mergemodulsequenztabelle verwendet wird, müssen die BaseAction- und After-Spalten dieses Datensatzes NULL sein.

Wenn eine benutzerdefinierte Aktion oder ein benutzerdefiniertes Dialogfeld in die Spalte Aktion eingegeben wird, muss die Spalte Sequenz NULL sein.

Wenn eine Aktion, die ein Beendigungsflag zurückgibt, in die Spalte Aktion eingegeben wird, sollte die Spalte Sequenz den negativen Wert für dieses Flag enthalten, und die BaseAction- und After-Spalten dieses Datensatzes müssen NULL sein. Die folgenden negativen Werte geben an, dass die Aktion aufgerufen wird, wenn das Installationsprogramm das Beendigungsflag zurückgibt.



| Beendigungsflag          | Wert | BESCHREIBUNG              |
|---------------------------|-------|--------------------------|
| msiDoActionStatusSuccess  | –1    | Erfolgreicher Abschluss.   |
| msiDoActionStatusUserExit | –2    | Der Benutzer beendet die Installation. |
| msiDoActionStatusFailure  | -3    | Schwerwiegendes Beenden wird beendet.   |
| msiDoActionStatusSuspend  | –4    | Die Installation wurde angehalten.    |



 

Die BaseAction-Spalte kann eine Standardaktion, eine benutzerdefinierte Aktion, die in der benutzerdefinierten Aktionstabelle des Mergemoduls angegeben ist, oder einen Dialog enthalten, der in der Dialogtabelle des Moduls angegeben ist. Die BaseAction-Spalte ist ein Schlüssel in der Spalte Aktion dieser Tabelle. Es darf sich nicht um einen Fremdschlüssel in einer anderen Mergetabelle oder Tabelle in der .msi datei. Dies bedeutet, dass jede Standardaktion, benutzerdefinierte Aktion oder jeder Dialog, der in der Spalte BaseAction aufgeführt ist, auch in der Spalte Aktion eines anderen Datensatzes in dieser Tabelle aufgeführt werden muss.

 

 



