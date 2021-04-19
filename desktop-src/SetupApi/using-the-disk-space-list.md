---
description: Bevor Sie Datei Vorgänge in der Liste der Speicherplätze hinzufügen oder entfernen können, müssen Sie Sie mithilfe der setupkreatediskspacelist-Funktion erstellen.
ms.assetid: 287fd84a-dc8c-4a5c-b998-db5f2fbee5f1
title: Verwenden der Disk-Space Liste
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8a19f100fd5190472f5f6bfebaf74affe1a789cb
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106349789"
---
# <a name="using-the-disk-space-list"></a>Verwenden der Disk-Space Liste

Bevor Sie Datei Vorgänge in der Liste der Speicherplätze hinzufügen oder entfernen können, müssen Sie Sie mithilfe der [**setupkreatediskspacelist**](/windows/desktop/api/Setupapi/nf-setupapi-setupcreatediskspacelista) -Funktion erstellen.

Nachdem Sie eine Speicherplatz Liste erstellt haben, können Sie mithilfe von [**setupadddediskspacelist**](/windows/desktop/api/Setupapi/nf-setupapi-setupaddtodiskspacelista)einzelne Datei Kopier-oder Löschvorgänge zur Liste hinzufügen. Wenn Sie alle Datei Kopier-oder Löschvorgänge in einem gesamten INF-Abschnitt hinzufügen möchten, verwenden Sie entweder die [**setupaddsectiondediskspacelist**](/windows/desktop/api/Setupapi/nf-setupapi-setupaddsectiontodiskspacelista) -oder die [**setupaddinstallsectiondediskspacelist**](/windows/desktop/api/Setupapi/nf-setupapi-setupaddinstallsectiontodiskspacelista) -Funktion.

Nachdem Sie alle Installations Vorgänge der Liste Speicherplatz hinzugefügt haben, können Sie Sie Abfragen, um herauszufinden, wie viel Speicherplatz für die angegebene Installation erforderlich ist, indem Sie die [**setupqueryspacerequiredondrive**](/windows/desktop/api/Setupapi/nf-setupapi-setupqueryspacerequiredondrivea) -Funktion verwenden.

Die [**setupquerydrivesindiskspacelist**](/windows/desktop/api/Setupapi/nf-setupapi-setupquerydrivesindiskspacelista) -Funktion gibt die Laufwerk Spezifikationen für jedes Ziellaufwerk zurück, auf das in den Datei Vorgängen auf der Speicherplatz Liste verwiesen wird. Sie können diese Informationen verwenden, um den verfügbaren Speicherplatz auf diesen Laufwerken Programm gesteuert mit dem für die Installation erforderlichen Speicherplatz zu vergleichen.

Um einen Datei Vorgang aus der Liste der Speicherplätze zu entfernen, verwenden Sie die Funktion [**setupremuvefromdiskspacelist**](/windows/desktop/api/Setupapi/nf-setupapi-setupremovefromdiskspacelista) . Um alle Kopier-oder Löschvorgänge für Dateien aus einem gesamten INF-Abschnitt zu entfernen, verwenden Sie die Funktion [**setupremuvesectionfromdiskspacelist**](/windows/desktop/api/Setupapi/nf-setupapi-setupremovesectionfromdiskspacelista) oder [**SetupRemoveInstallSectionFromDiskSpaceList**](/windows/desktop/api/Setupapi/nf-setupapi-setupremoveinstallsectionfromdiskspacelista) .

Nachdem die Speicherplatz Liste nicht mehr benötigt wird, können Sie die Ihnen zugeordneten Ressourcen freigeben, indem Sie die [**setupdestroydiskspacelist**](/windows/desktop/api/Setupapi/nf-setupapi-setupdestroydiskspacelist) -Funktion aufrufen.

 

 



