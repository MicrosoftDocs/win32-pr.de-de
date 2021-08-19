---
description: Die Aktion InstallValidate überprüft, ob alle Volumes, denen Kosten zugeordnet wurden, über ausreichend Speicherplatz für die Installation verfügen. Die Aktion InstallValidate beendet die Installation mit einem schwerwiegenden Fehler, wenn auf einem Volume nicht viel Speicherplatz verfügbar ist.
ms.assetid: 1c55794d-1ecc-43bf-956f-96afc5f36964
title: InstallValidate-Aktion
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6dd8a5e2f69df5e588c2366f7cf9fff0fb3621889e9b725605a38acc14f39457
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "117805638"
---
# <a name="installvalidate-action"></a>InstallValidate-Aktion

Die Aktion InstallValidate überprüft, [](v-gly.md) ob [](c-gly.md) alle Volumes, denen Kosten zugeordnet wurden, über ausreichend Speicherplatz für die Installation verfügen. Die Aktion InstallValidate beendet die Installation mit einem schwerwiegenden Fehler, wenn auf einem Volume nicht viel Speicherplatz verfügbar ist.

Die Aktion InstallValidate benachrichtigt den Benutzer auch, wenn eine oder mehrere zu überschreibende oder zu entfernende Dateien derzeit von einem aktiven Prozess verwendet werden. Weitere Informationen finden Sie unter [Systemneustarts.](system-reboots.md)

## <a name="sequence-restrictions"></a>Sequenzeinschränkungen

Die [Aktion CostFinalize](costfinalize-action.md) und alle Benutzeroberflächendialogfeldsequenzen, die dem Benutzer das Ändern von Auswahlzuständen und/oder Verzeichnissen ermöglichen, sollten vor der InstallValidate-Aktion sequenziert werden.

[Benutzerdefinierte Aktionen,](custom-actions.md) die den Installationsstatus von Features oder Komponenten ändern, müssen vor der InstallValidate-Aktion sequenziert werden.

## <a name="actiondata-messages"></a>ActionData-Meldungen

Es sind keine ActionData-Meldungen enthalten.

## <a name="remarks"></a>Hinweise

In der Regel sollte eine frühere Benutzeroberflächendialogfeldsequenz die gleiche Überprüfung wie die InstallValidate-Aktion ausführen, wenn der Benutzer versucht, das Kopieren von Dateien zu initiieren. In dieser Benutzeroberflächendialogfeldsequenz sollte ein Dialogfeld **Nicht** genügend Speicherplatz angezeigt werden, wenn die ausgewählten Volumes nicht über genügend Speicherplatz für die Installation verfügen. Die Dialogfelder der Benutzeroberfläche sollten so geschrieben werden, dass der Benutzer nicht mit der Installation fortfahren kann, wenn nicht genügend Speicherplatz vorhanden ist. Bei einer stillen Installation gibt es keine Benutzeroberfläche, und die Aktion InstallValidate beendet die Installation, wenn nicht genügend Speicherplatz vorhanden ist. Die Ursache der vorzeitigen Beendigung wird in der Protokolldatei aufgezeichnet, wenn die Protokollierung aktiviert ist.

Ein Eintrag wird einer internen FilesInUse-Tabelle hinzugefügt, wenn eine Datei überschrieben oder entfernt wird, während sie während der Dateikosten von einem Prozess ausgeführt oder [*geändert werden kann.*](c-gly.md) Die Tabelle FilesInUse enthält Spalten für den Namen und den vollständigen Pfad der Datei. Wenn die InstallValidate-Aktion ausgeführt wird, fragt das Installationsprogramm die Tabelle FilesInUse nach Einträgen ab und bestimmt den Namen des Prozesses mithilfe der Datei. Mit der Aktion InstallValidate [](listbox-table.md) wird der ListBox-Benutzeroberflächentabelle für jeden eindeutigen Prozess, der von dieser Abfrage identifiziert wird, ein Datensatz hinzugefügt. Der Datensatz enthält die folgenden Werte in jeder Spalte:

**Property**: FileInUseProcess

 

**Wert:** *Name des Prozesses*

 

**Text:** *Text, der in der Beschriftung des Hauptfensters des Prozesses enthalten ist*

Die Aktion InstallValidate zeigt dann das Dialogfeld **Verwendete** Dateien an. In diesem Dialogfeld werden die Prozesse angezeigt, die heruntergefahren werden müssen, um zu vermeiden, dass das System neu gestartet werden muss, um die in Gebrauchenen Dateien zu ersetzen.

Die Aktion InstallValidate fragt die [Tabelle Dialog](dialog-table.md) nach einem erstellten Dialogfeld mit dem reservierten Namen [FilesInUse](filesinuse-dialog.md) ab und zeigt es an. Dieses Dialogfeld muss ein [ListBox-Steuerelement](listbox-control.md) enthalten, das an eine Eigenschaft namens FileInUseProcess gebunden ist. Standardmäßig verfügt dieses Dialogfeld über die Schaltfläche  **Beenden,** **Wiederholen** oder Ignorieren, aber dies liegt beim Benutzeroberflächenautor. Jede Schaltfläche sollte an ein [EndDialog](enddialog-controlevent.md) ControlEvent in der [ControlEvent-Tabelle gebunden](controlevent-table.md) sein. Die InstallValidate-Aktion antwortet wie folgt auf den wert, der vom [DoAction](doaction-controlevent.md) ControlEvent zurückgegeben wird, wie von einem der [folgenden EndDialog-Argumente](enddialog-controlevent.md) bestimmt, die der vom Benutzer gedrückten Schaltfläche zugeordnet sind:

**Wiederholen:** Alle Werte, die der [ListBox-Tabelle](listbox-table.md) hinzugefügt [](c-gly.md) werden, werden deaktiviert, und die gesamte Dateikostenprozedur wird wiederholt, und es wird erneut nach Dateien geprüft, die noch verwendet werden. Wenn ein oder mehrere Prozesse weiterhin als zu überschreibende oder zu löschende Dateien identifiziert werden, wird der Prozess wiederholt. Andernfalls gibt InstallValidate die Steuerung an das Installationsprogramm mit dem Status msiDoActionStatusSuccess zurück.

**Beenden:** Die Aktion InstallValidate gibt die Steuerung sofort an das Installationsprogramm mit dem Status msiDoActionStatusUserExit zurück. Dadurch wird die Installation beendet.

**Jeder andere Rückgabewert:** Die InstallValidate-Aktion gibt die Steuerung sofort an das Installationsprogramm mit dem Status msiDoActionStatusSuccess zurück. Da in diesem Fall mindestens eine Datei noch verwendet wird, müssen die nachfolgenden [InstallFiles-](installfiles-action.md) und/oder [InstallAdminPackage-Aktionen](installadminpackage-action.md) planen, dass die in Gebrauch genommenen Dateien ersetzt oder gelöscht werden, wenn das System neu gestartet wird.

Wenn keine [ListBox-Tabelle](listbox-table.md) in der Datenbank vorhanden ist, wird InstallValidate ohne Fehler automatisch beendet.

Das Semikolon ist das Listentrennzeichen für Transformationen, Quellen und Patches und sollte nicht in diesen Dateinamen oder Pfaden verwendet werden.

Dateien, die an einem schreibgeschützten Speicherort als schreibgeschützt gekennzeichnet sind, werden vom Installationsprogramm nie als verwendet betrachtet.

Wenn die **Benutzeroberflächenebene**  einfach ist, wird dem Benutzer ein Standarddialogfeld mit den Schaltflächen "Abbrechen" und "Wiederholen" angezeigt. 

 

 



