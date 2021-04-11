---
description: Mit der InstallValidate-Aktion wird überprüft, ob alle Volumes, denen die Kosten zugewiesen wurden, über ausreichend Speicherplatz für die Installation verfügen. Durch die InstallValidate-Aktion wird die Installation mit einem schwerwiegenden Fehler beendet, wenn auf einem Volume wenig Speicherplatz vorhanden ist.
ms.assetid: 1c55794d-1ecc-43bf-956f-96afc5f36964
title: InstallValidate-Aktion
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e650ce136ac3b1b62e41ce34f79f5d28540d1292
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "104217802"
---
# <a name="installvalidate-action"></a>InstallValidate-Aktion

Mit der InstallValidate-Aktion wird überprüft, ob alle [*Volumes*](v-gly.md) , denen die [*Kosten*](c-gly.md) zugewiesen wurden, über ausreichend Speicherplatz für die Installation verfügen. Durch die InstallValidate-Aktion wird die Installation mit einem schwerwiegenden Fehler beendet, wenn auf einem Volume wenig Speicherplatz vorhanden ist.

Die InstallValidate-Aktion benachrichtigt den Benutzer auch, wenn eine oder mehrere Dateien, die überschrieben oder entfernt werden sollen, zurzeit von einem aktiven Prozess verwendet werden. Weitere Informationen finden Sie unter [System Neustarts](system-reboots.md).

## <a name="sequence-restrictions"></a>Sequenz Einschränkungen

Die Aktion " [costfinalize](costfinalize-action.md) " und alle Benutzeroberflächen-Dialogfeld Sequenzen, die es dem Benutzer ermöglichen, die Auswahl Zustände und/oder Verzeichnisse zu ändern, sollten vor der InstallValidate-Aktion sequenziert werden.

[Benutzerdefinierte Aktionen](custom-actions.md) , mit denen der Installationsstatus von Features oder Komponenten geändert wird, müssen vor der InstallValidate-Aktion sequenziert werden.

## <a name="actiondata-messages"></a>Aktions Daten Meldungen

Es sind keine Aktions Daten Meldungen vorhanden.

## <a name="remarks"></a>Bemerkungen

In der Regel sollte eine frühere UI-Dialogfeld Sequenz dieselbe Überprüfung wie die InstallValidate-Aktion durchführen, wenn der Benutzer versucht, das Kopieren von Dateien zu initiieren. In dieser Benutzeroberflächen-Dialogfeld Sequenz sollte das Dialogfeld nicht genügend **Speicherplatz** vorhanden sein, wenn die ausgewählten Volumes nicht über genügend Speicherplatz für die Installation verfügen. Die Dialogfelder für die Benutzeroberfläche sollten so erstellt werden, dass der Benutzer nicht mit der Installation fortfahren kann, wenn nicht genügend Speicherplatz vorhanden ist. Bei einer stillen Installation gibt es keine Benutzeroberfläche, und die InstallValidate-Aktion beendet die Installation, wenn nicht genügend Speicherplatz vorhanden ist. Die Ursache für die vorzeitige Beendigung wird in der Protokolldatei aufgezeichnet, wenn die Protokollierung aktiviert ist.

Ein Eintrag wird einer internen FilesInUse-Tabelle hinzugefügt, wenn eine Datei überschrieben oder entfernt wird, während Sie für die Ausführung geöffnet ist oder von einem beliebigen Prozess während der Datei [*Kosten*](c-gly.md)geändert wird. Die FilesInUse-Tabelle enthält Spalten für den Namen und den vollständigen Pfad der Datei. Wenn die InstallValidate-Aktion ausgeführt wird, fragt das Installationsprogramm die FilesInUse-Tabelle nach Einträgen ab und bestimmt den Namen des Prozesses, der die Datei verwendet. Die InstallValidate-Aktion fügt der [ListBox](listbox-table.md) -Benutzerschnittstellen Tabelle für jeden eindeutigen, von dieser Abfrage identifizierten Prozess einen Datensatz hinzu. Der Datensatz enthält die folgenden Werte in den einzelnen Spalten:

**Eigenschaft**: filinput useprocess

 

**Wert**: *Name des Prozesses*

 

**Text**: *Text, der in der Beschriftung des Hauptfensters des Prozesses enthalten* ist.

Die Aktion InstallValidate zeigt dann das Dialogfeld **verwendete Dateien an** . In diesem Dialogfeld werden die Prozesse angezeigt, die heruntergefahren werden müssen, um zu verhindern, dass das System neu gestartet wird, um verwendete Dateien zu ersetzen.

Die InstallValidate-Aktion fragt die [Dialog](dialog-table.md) Feld Tabelle nach einem erstellten Dialogfeld mit dem reservierten Namen [FilesInUse](filesinuse-dialog.md) -Dialogfeld ab und zeigt es an. Dieses Dialogfeld muss ein [ListBox](listbox-control.md) -Steuerelement enthalten, das an eine Eigenschaft namens filinput useprocess gebunden ist. Gemäß der Konvention weist dieses Dialogfeld eine Schaltfläche zum **Beenden**, **wiederholen** oder **ignorieren** auf, aber dies ist der Benutzeroberflächen Autor. Jede Schaltfläche muss an einen [EndDialog](enddialog-controlevent.md) -ControlEvent in der Tabelle [ControlEvent](controlevent-table.md) gebunden werden. Die InstallValidate-Aktion antwortet wie folgt auf den Wert, der von der [doaction](doaction-controlevent.md) -ControlEvent zurückgegeben wird, wie von einem dieser [EndDialog](enddialog-controlevent.md) -Argumente vorgegeben, das der Schaltfläche zugeordnet ist, die vom Benutzer übermittelt wird:

**Wiederholung**: alle Werte, die der [ListBox](listbox-table.md) -Tabelle hinzugefügt werden, werden gelöscht, und die gesamte Datei [*Kosten*](c-gly.md) wird wiederholt, und die Dateien, die noch verwendet werden, werden erneut überprüft. Wenn ein oder mehrere Prozesse weiterhin als Verwendung von Dateien identifiziert werden, die überschrieben oder gelöscht werden sollen, wird der Prozess wiederholt. Andernfalls gibt InstallValidate die Steuerung mit dem Status msidoaktionstatussuccess an das Installationsprogramm zurück.

**Exit**: mit der InstallValidate-Aktion wird die Steuerung sofort an das Installationsprogramm mit dem Status "msidoaction statususerexit" zurückgegeben. Dadurch wird die Installation beendet.

**Jeder andere Rückgabewert**: die InstallValidate-Aktion gibt die Steuerung sofort mit dem Status "msidoaction StatusSuccess" an das Installationsprogramm zurück. Da in diesem Fall eine oder mehrere Dateien weiterhin verwendet werden, müssen die nachfolgenden [InstallFiles](installfiles-action.md) -und/oder [installadminpackage](installadminpackage-action.md) -Aktionen festlegen, dass die verwendeten Dateien beim Neustart des Systems ersetzt oder gelöscht werden.

Wenn in der Datenbank keine [ListBox](listbox-table.md) -Tabelle vorhanden ist, wird InstallValidate ohne Fehler automatisch beendet.

Das Semikolon ist das Listen Trennzeichen für Transformationen, Quellen und Patches und sollte in diesen Dateinamen oder Pfaden nicht verwendet werden.

Dateien, die in einem schreibgeschützten Speicherort als schreibgeschützt gekennzeichnet sind, werden vom Installer nie als verwendet.

Ein standardmäßiges Dialogfeld " **nicht genügend Speicherplatz** " mit **Abbruch** -und **Wiederholungs** Schaltflächen wird dem Benutzer angezeigt, wenn die Benutzeroberflächen Ebene "Basic" ist.

 

 



