---
description: 'Nachdem die Datei Kosten verarbeitet wurde, verfügt das Installationsprogramm über alle Informationen, die zum Verarbeiten der beiden Datei Bearbeitungs Aktionen erforderlich sind: duplicatefiles und muvefiles.'
ms.assetid: 2e6d6eb3-1e71-46e6-a946-d9cc0b209325
title: Datei Installation
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 472c58db3dc2e9094a26d57f871359a38930877b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "104131785"
---
# <a name="file-installation"></a>Datei Installation

Nachdem die [Datei Kosten](file-costing.md) verarbeitet wurde, verfügt das Installationsprogramm über alle Informationen, die zum Verarbeiten der beiden Datei Bearbeitungs Aktionen erforderlich sind: [duplicatefiles](duplicatefiles-action.md) und [muvefiles](movefiles-action.md).

Verwenden Sie die [duplicatefiles-Aktion](duplicatefiles-action.md) , um die Dateien anzugeben, die das Installationsprogramm in der [duplicatefile-Tabelle](duplicatefile-table.md)duplizieren soll. Verwenden Sie die [Aktion movefiles](movefiles-action.md), um zu bestimmen, welche Dateien verschoben werden sollen, indem Sie die [MoveFile-Tabelle](movefile-table.md)Abfragen.

Beachten Sie, dass das Options Feld der [Tabelle "muvefile](movefile-table.md) " angibt, ob die ursprüngliche Datei aus Ihrem aktuellen Speicherort gelöscht werden soll. Dateien, die von der Aktion "muvefiles" verschoben oder kopiert werden, werden bei der Installation des Produkts nicht gelöscht.

Die [Aktion InstallFiles](installfiles-action.md) wird aufgerufen, sobald alle anderen Datei Bearbeitungsvorgänge abgeschlossen wurden. Die Aktion InstallFiles verarbeitet die [Medien Tabelle](media-table.md), die [Dateitabelle](file-table.md)und die [Komponenten Tabelle](component-table.md) , um zu bestimmen, welche Dateien aus der Quelle in das Ziel kopiert werden.

Mit der [Aktion InstallFiles](installfiles-action.md) wird die Verzeichnisstruktur erstellt, die für die Installation aller Dateien erforderlich ist. Wenn ein explizit leerer Ordner installiert werden muss, kann die Aktion "up [Folder](createfolders-action.md) " aufgerufen werden, um Sie zu erstellen.

 

 



