---
description: ICE27 überprüft die Sequenz Tabellen eines Installationspakets auf gültige Aktionen, Aktions Sequenz Einschränkungen und Organisationen in den Abschnitten "suchen", "Kosten", "Auswahl" und "Ausführung".
ms.assetid: c5292a3c-57bb-4203-96a1-6d747f554178
title: ICE27
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4eb4b90b313f5f78874fb93ce9d32c3650b97064
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "103864095"
---
# <a name="ice27"></a>ICE27

ICE27 überprüft die [*Sequenz Tabellen*](s-gly.md) eines Installationspakets auf gültige Aktionen, Aktions Sequenz Einschränkungen und Organisationen in den Abschnitten "suchen", "Kosten", "Auswahl" und "Ausführung".

Die benutzerdefinierte Aktion ICE27 überprüft Folgendes:

-   Die in der Spalte Aktion der Sequenz Tabellen aufgeführten Aktionen sind [Standard Aktionen](standard-actions.md), eine benutzerdefinierte Aktion, die in der [Tabelle CustomAction](customaction-table.md)aufgeführt ist, oder ein Dialogfeld, das in der [Dialogfeld Tabelle](dialog-table.md)aufgeführt ist.
-   Diese Aktionen, die sich auf die Sequenz Einschränkungen beziehen, befinden sich in der richtigen Reihenfolge in der Aktions Sequenz. Sequenz Einschränkungen ergeben sich, wenn eine Aktion von einer anderen abhängt.
-   Die Aktionen, die auf einen bestimmten Abschnitt der Sequenz beschränkt sind, befinden sich dort, wo Sie angehören. ICE27 überprüft die folgende Organisation der Sequenz Tabellen. Beachten Sie, dass nicht jede Sequenz Tabelle jeden Abschnitt enthält. Weitere Informationen finden Sie in den vorgeschlagenen Sequenz Tabellen unter [Verwenden einer Sequenz Tabelle](using-a-sequence-table.md).



| Abschnitt Sequenz Tabelle | Bereich in Aktions Sequenz                                                                       | Zu Abschnitt gehörende Aktionen                                                                                                                                                                                                                     |
|------------------------|------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Suchen,                 | {Start} zu [costinitialize](costinitialize-action.md)                                         | Aktionen, die nach vorhandenen Anwendungen suchen. [AppSearch](appsearch-action.md)<br/> [Ccpsearch](ccpsearch-action.md)<br/>                                                                                                         |
| Rechnung                | [Costinitialize](costinitialize-action.md) zu [costfinalize-Aktion](costfinalize-action.md)  | Aktionen für die [Datei Kosten](file-costing.md). [Costinitialize](costinitialize-action.md)<br/> [Datei Kosten](filecost-action.md)<br/> [Costfinalize](costfinalize-action.md)<br/>                                           |
| Auswahl              | [Costfinalize](costfinalize-action.md) zu [InstallValidate](installvalidate-action.md)       | Aktionen, mit denen Ordner oder Funktions Zustände festgelegt werden. ["Stodbcfolders"-Aktion](setodbcfolders-action.md)<br/>                                                                                                                                        |
| Ausführung              | [Installvalidieren](installvalidate-action.md) zu [InstallFinalize](installfinalize-action.md) | Skript Aktionen, z. b. Registrierung, Veröffentlichung, Installation (bei der Dateien kopiert werden). Beachten Sie, dass die [InstallFinalize-Aktion](installfinalize-action.md) nur dann in der Tabelle erfolgen muss, wenn im Ausführungs Abschnitt Aktionen vorhanden sind.<br/> |
| Postexecution          | [InstallFinalize](installfinalize-action.md) in {End}                                         | [RemoveExistingProducts](removeexistingproducts-action.md)                                                                                                                                                                                      |



 

ICE27 überprüft die folgenden Tabellen:

-   [AdvtExecuteSequence](advtexecutesequence-table.md)
-   [AdminUISequence](adminuisequence-table.md)
-   ["AdminExecuteSequence"](adminexecutesequence-table.md)
-   [InstallUISequence](installuisequence-table.md)
-   [InstallExecuteSequence](installexecutesequence-table.md)

## <a name="result"></a>Ergebnis

ICE27 gibt eine Fehlermeldung aus, wenn im Paket Sequenz Tabellen mit ungültiger Aktions Sequenzierung oder Organisation vorhanden sind.

## <a name="example"></a>Beispiel



| ICE27-Fehler                                                                                                                         | BESCHREIBUNG                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                         |
|-------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Unbekannte Aktion: ' Action1 ' der installexecutesequnence-Tabelle. Keine Standardaktion und nicht in CustomAction-oder Dialog Feld Tabellen gefunden.    | In der Sequenz Tabelle ist eine Aktion aufgelistet, die angibt, dass es sich nicht um [Standard Aktionen](standard-actions.md), eine benutzerdefinierte Aktion handelt, die in der [Tabelle CustomAction](customaction-table.md)aufgeführt ist, oder ein Dialogfeld, das in der [Dialogfeld Tabelle](dialog-table.md)aufgeführt ist.                                                                                                                                                                                                                                                                       |
| "Action2" in der Tabelle InstallExecute an falscher Stelle. Aktuell: suchen, richtig: Kosten                                                 | Es gibt eine Aktion in einer Sequenz Tabelle, die in Bezug auf die Sequenznummer in der Sequenz Spalte falsch platziert wird. "Current" gibt die aktuelle Platzierung der Aktion in den Abschnitten "suchen", "Kosten", "Auswahl" oder "Ausführung" der ausgewählten Sequenz Tabelle an.<br/> "Correct" gibt an, in welchem Abschnitt die Aktion gehört.<br/> Ändern Sie die Sequenznummer der Aktion in den richtigen Abschnitt, um diesen Fehler zu beheben. Beachten Sie, dass sich einige Aktionen in mehr als einem Abschnitt befinden können.<br/> |
| Die "InstallFinalize"-Aktion in der InstallExecuteSequence-Tabelle kann nur aufgerufen werden, wenn Skript Vorgänge für die Ausführung vorhanden sind.             | Es gibt eine [InstallFinalize-Aktion](installfinalize-action.md) in einer Sequenz Tabelle, die keine Skript Vorgänge im Ausführungs Abschnitt der Tabelle enthält. Fügen Sie dem Ausführungs Abschnitt Aktionen hinzu, oder entfernen Sie die InstallFinalize-Aktion aus der Tabelle.<br/>                                                                                                                                                                                                                                                        |
| InstallFinalize muss in der InstallExecuteSequence-Tabelle aufgerufen werden, da Skript Vorgänge für die Ausführung vorhanden sind.                            | Es gibt eine Sequenz Tabelle mit Aktionen im Ausführungs Abschnitt, die nicht die [InstallFinalize-Aktion](installfinalize-action.md)enthält. Fügen Sie dieser Sequenz Tabelle die InstallFinalize-Aktion hinzu, und geben Sie Ihr die größte Sequenznummer an, um Sie zuletzt in der Aktions Sequenz zu platzieren.<br/>                                                                                                                                                                                                                            |
| Aktion: ' Action3 ' in der InstallExecuteSequence-Tabelle muss vor der ' Action5 '-Aktion stehen. Aktueller ABF \# : 1200. Abhängige ABF \# : 1100 | In der angegeben Sequenz Tabelle ist eine Aktion vorhanden, die nach einer abhängigen Aktion sequenziert wird. Ändern Sie die Sequenznummer der abhängigen Aktion, sodass Sie vor der Aktion steht.<br/>                                                                                                                                                                                                                                                                                                                                    |
| Aktion: "Action4" in der InstallExecuteSequence-Tabelle muss nach der Aktion "Action6" stehen.                                             | In der Sequenz Tabelle ist eine Aktion vorhanden, die vor einer Aktion sequenziert wird, von der Sie abhängig ist. Ändern Sie die Sequenznummer für die Aktion, sodass Sie nach ihrer abhängigen Aktion erfolgt.<br/>                                                                                                                                                                                                                                                                                                                   |



 

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Ice-Referenz](ice-reference.md)
</dt> </dl>

 

 




