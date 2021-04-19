---
description: Nachdem die Warteschlange den Commit für Ihre Vorgänge abgeschlossen hat, sollte Sie mithilfe der Funktion setupclosefilequeue mit dem Handle geschlossen werden, das von setupopenfilequeue erstellt wurde.
ms.assetid: 4cb21699-e476-4832-9678-2bf36f3bda08
title: Schließen der Datei Warteschlange und der INF-Datei
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 35b4005e3ce9d084d759612d70cd9fd256fe9ba4
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106361708"
---
# <a name="closing-the-file-queue-and-inf-file"></a>Schließen der Datei Warteschlange und der INF-Datei

Nachdem die Warteschlange den Commit für Ihre Vorgänge abgeschlossen hat, sollte Sie mithilfe der Funktion [**setupclosefilequeue**](/windows/desktop/api/Setupapi/nf-setupapi-setupclosefilequeue) mit dem Handle geschlossen werden, das von [**setupopenfilequeue**](/windows/desktop/api/Setupapi/nf-setupapi-setupopenfilequeue)erstellt wurde. Der Standard Warteschlangen Rückruf muss zerstört und neu erstellt werden, bevor ein Commit für eine andere Warteschlange ausgeführt werden kann.

Wenn ein Standardkontext für die Verwendung durch die standardmäßige Rückruf Routine initiiert wurde, sollte Sie auch durch Aufrufen der [**setuptermdefaultqueuecallback**](/windows/desktop/api/Setupapi/nf-setupapi-setuptermdefaultqueuecallback) -Funktion beendet werden. Der *Kontext* ist ein Zeiger auf die-Struktur, die von der [**SetupInitDefaultQueueCallback**](/windows/desktop/api/Setupapi/nf-setupapi-setupinitdefaultqueuecallback) -Funktion zurückgegeben wird.

Wenn der Zugriff auf die INF-Informationen nicht mehr benötigt wird, rufen Sie die Funktion [**setupcloseinffile**](/windows/desktop/api/Setupapi/nf-setupapi-setupcloseinffile) mit dem Handle auf, das von [**setupopenfilequeue**](/windows/desktop/api/Setupapi/nf-setupapi-setupopenfilequeue) erstellt wurde, um Systemressourcen freizugeben.

 

 



