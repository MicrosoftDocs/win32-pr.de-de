---
description: Sie können Dateien auf zwei Arten aus einem Schränk extrahieren. Die erste und einfachste Möglichkeit besteht in der Nutzung der automatischen Schränkverarbeitung, die in die Setupfunktionen integriert ist.
ms.assetid: 113333c8-28d1-4b0e-8da4-0c94389d8038
title: Extrahieren von Dateien aus Schränken
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0cfd7f41d4951e43bb58fac6efb9b1fd11895373398643e7c8c9cc00821dd72d
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118887251"
---
# <a name="extracting-files-from-cabinets"></a>Extrahieren von Dateien aus Schränken

Sie können Dateien auf zwei Arten aus einem Schränk extrahieren. Die erste und einfachste Möglichkeit besteht in der Nutzung der automatischen Schränkverarbeitung, die in die Setupfunktionen integriert ist.

Die Installationsfunktionen wie [**SetupCommitFileQueue,**](/windows/desktop/api/Setupapi/nf-setupapi-setupcommitfilequeuea) [**SetupInstallFile**](/windows/desktop/api/Setupapi/nf-setupapi-setupinstallfilea)und [**SetupInstallFromInfSection**](/windows/desktop/api/Setupapi/nf-setupapi-setupinstallfrominfsectiona)überprüfen die Komprimierung für jede Datei. Wenn sich die Datei in einem Schränk befindet, suchen die Funktionen zunächst nach einer Datei mit diesem Namen außerhalb des Schränks. Wenn sie gefunden werden, installieren die Funktionen die externe Datei und ignorieren die Datei innerhalb der Schränkung. Auf diese Weise können Sie eine einzelne Datei im Schränk aktualisieren, ohne den Schränk neu zu erstellen.

Die Setupfunktionen verfolgen auch nach, welche Dateien in einer Schränkung abgerufen wurden, sodass eine Datei nur einmal extrahiert wird, auch wenn sie mehrmals installiert wurde.

Die zweite Möglichkeit zum Extrahieren von Dateien aus einer Schränkung ist die [**Verwendung von SetupIterateCabinet.**](/windows/desktop/api/Setupapi/nf-setupapi-setupiteratecabineta) Diese Funktion durch iteriert jede Datei in einer Schränkung und sendet eine Benachrichtigung an eine Rückrufroutine für jede gefundene Datei. Die Rückrufroutine gibt dann einen Wert zurück, der angibt, ob die Datei extrahiert oder übersprungen werden soll.

> [!Note]  
> Die Setup-API stellt keine Standardrückrufroutine für die Handhabung von Benachrichtigungen des Schränkungsspeichers bereit. Wenn Sie [**SetupIterateCabinet**](/windows/desktop/api/Setupapi/nf-setupapi-setupiteratecabineta) explizit aufrufen, müssen Sie eine Rückrufroutine zum Verarbeiten der von der Funktion zurückgegebenen Benachrichtigungen des Schränkens verwenden.

 

 

 



