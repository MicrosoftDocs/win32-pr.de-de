---
description: Nachdem die Warteschlange den Commit für ihre Vorgänge abgeschlossen hat, sollte sie mithilfe der SetupCloseFileQueue-Funktion mit dem handle geschlossen werden, das von SetupOpenFileQueue erstellt wurde.
ms.assetid: 4cb21699-e476-4832-9678-2bf36f3bda08
title: Schließen der Dateiwarteschlange und der INF-Datei
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ce5c81c75f7515acfb346b4277e416b0cb2c2a9be6e40464dcfdfc21c3b23bba
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118887575"
---
# <a name="closing-the-file-queue-and-inf-file"></a>Schließen der Dateiwarteschlange und der INF-Datei

Nachdem die Warteschlange den Commit für ihre Vorgänge abgeschlossen hat, sollte sie mithilfe der [**SetupCloseFileQueue-Funktion**](/windows/desktop/api/Setupapi/nf-setupapi-setupclosefilequeue) mit dem Handle geschlossen werden, das von [**SetupOpenFileQueue erstellt wurde.**](/windows/desktop/api/Setupapi/nf-setupapi-setupopenfilequeue) Der Standardmäßige Warteschlangenrückruf muss zerstört und neu erstellt werden, bevor ein Committed für eine andere Warteschlange möglich ist.

Wenn ein Standardkontext für die Verwendung durch die Standardrückrufroutine initiiert wurde, sollte er auch durch Aufrufen der [**SetupTermDefaultQueueCallback-Funktion beendet**](/windows/desktop/api/Setupapi/nf-setupapi-setuptermdefaultqueuecallback) werden. Der *Kontext* ist ein Zeiger auf die -Struktur, die von der [**SetupInitDefaultQueueCallback-Funktion zurückgegeben**](/windows/desktop/api/Setupapi/nf-setupapi-setupinitdefaultqueuecallback) wird.

Wenn der Zugriff auf die INF-Informationen nicht mehr benötigt wird, rufen Sie die [**SetupCloseInfFile-Funktion**](/windows/desktop/api/Setupapi/nf-setupapi-setupcloseinffile) mit dem Handle auf, das von [**SetupOpenFileQueue**](/windows/desktop/api/Setupapi/nf-setupapi-setupopenfilequeue) erstellt wurde, um Systemressourcen frei zu machen.

 

 



