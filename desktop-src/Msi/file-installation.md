---
description: 'Nach Abschluss der Dateikosten verfügt das Installationsprogramm über alle Informationen, die zum Verarbeiten der beiden Dateibearbeitungsaktionen erforderlich sind: DuplicateFiles und MoveFiles.'
ms.assetid: 2e6d6eb3-1e71-46e6-a946-d9cc0b209325
title: Dateiinstallation
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 005a987a7e61f646f58abd0ec699ce03bd29d85dfa2ddb01e8f693750acda740
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118636698"
---
# <a name="file-installation"></a>Dateiinstallation

Nach [Abschluss der Dateikosten](file-costing.md) verfügt das Installationsprogramm über alle Informationen, die zum Verarbeiten der beiden Dateibearbeitungsaktionen erforderlich sind: [DuplicateFiles](duplicatefiles-action.md) und [MoveFiles](movefiles-action.md).

Verwenden Sie die [DuplicateFiles-Aktion,](duplicatefiles-action.md) um die Dateien anzugeben, die das Installationsprogramm in der [DuplicateFile-Tabelle duplizieren soll.](duplicatefile-table.md) Verwenden Sie die [MoveFiles-Aktion,](movefiles-action.md)um zu bestimmen, welche Dateien durch Abfragen der [MoveFile-Tabelle zu verschieben sind.](movefile-table.md)

Beachten Sie, dass das Feld Optionen der [MoveFile-Tabelle](movefile-table.md) angibt, ob die ursprüngliche Datei aus ihrem aktuellen Speicherort gelöscht werden soll. Dateien, die von der MoveFiles-Aktion verschoben oder kopiert werden, werden nicht gelöscht, wenn das Produkt deinstalliert wird.

Die [InstallFiles-Aktion](installfiles-action.md) wird aufgerufen, sobald alle anderen Dateibearbeitungsvorgänge abgeschlossen sind. Die InstallFiles-Aktion [](media-table.md)verarbeitet die Media-Tabelle, die [File-Tabelle](file-table.md)und die [Component-Tabelle,](component-table.md) um zu bestimmen, welche Dateien aus der Quelle in das Ziel kopiert werden.

Die [Aktion InstallFiles erstellt](installfiles-action.md) die Verzeichnisstruktur, die zum Installieren aller Dateien erforderlich ist. Wenn ein explizit leerer Ordner installiert werden muss, kann die [CreateFolders-Aktion](createfolders-action.md) aufgerufen werden, um ihn zu erstellen.

 

 



