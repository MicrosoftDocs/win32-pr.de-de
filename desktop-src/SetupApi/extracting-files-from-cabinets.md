---
description: Sie können Dateien auf zweierlei Weise aus einer CAB-Datei extrahieren. Die erste und einfachste Möglichkeit besteht darin, die in den Setup Funktionen integrierte automatische CAB-Verarbeitung zu nutzen.
ms.assetid: 113333c8-28d1-4b0e-8da4-0c94389d8038
title: Extrahieren von Dateien aus kabinatendateien
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4d94f413b4ad0ee1511dde21af747cd2665a4704
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106350486"
---
# <a name="extracting-files-from-cabinets"></a>Extrahieren von Dateien aus kabinatendateien

Sie können Dateien auf zweierlei Weise aus einer CAB-Datei extrahieren. Die erste und einfachste Möglichkeit besteht darin, die in den Setup Funktionen integrierte automatische CAB-Verarbeitung zu nutzen.

Die Installationsfunktionen, wie z. b. [**setupcommitfilequeue**](/windows/desktop/api/Setupapi/nf-setupapi-setupcommitfilequeuea), [**setupinstallfile**](/windows/desktop/api/Setupapi/nf-setupapi-setupinstallfilea)und [**setupinstallfrominbsection**](/windows/desktop/api/Setupapi/nf-setupapi-setupinstallfrominfsectiona), überprüfen die Komprimierung der einzelnen Dateien. Wenn sich die Datei in einer CAB-Datei befindet, sucht die Funktion zuerst nach einer Datei mit diesem Namen außerhalb der CAB-Datei. Wenn Sie gefunden wird, wird die externe Datei von den Funktionen installiert, und die Datei wird im CAB ignoriert. Dadurch können Sie eine einzelne Datei innerhalb der CAB-Datei aktualisieren, ohne die CAB-Datei neu zu erstellen.

Die Setup Funktionen verfolgen auch, welche Dateien in einer CAB-Datei abgerufen wurden, sodass eine Datei nur einmal extrahiert wird, auch wenn Sie mehrmals installiert wird.

Die zweite Möglichkeit zum Extrahieren von Dateien aus einer CAB-Datei ist die Verwendung von [**setupiteratecabinet**](/windows/desktop/api/Setupapi/nf-setupapi-setupiteratecabineta). Diese Funktion durchläuft jede Datei in einer CAB-Datei und sendet eine Benachrichtigung an eine Rückruf Routine für jede gefundene Datei. Die Rückruf Routine gibt dann einen Wert zurück, der angibt, ob die Datei extrahiert oder übersprungen werden soll.

> [!Note]  
> Die Setup-API stellt keine Standard Rückruf Routine zum Verarbeiten von CAB-Benachrichtigungen bereit. Wenn Sie [**setupiteratecabinet**](/windows/desktop/api/Setupapi/nf-setupapi-setupiteratecabineta) explizit aufrufen, müssen Sie eine Rückruf Routine angeben, um die CAB-Benachrichtigungen zu verarbeiten, die von der Funktion zurückgegeben werden.

 

 

 



