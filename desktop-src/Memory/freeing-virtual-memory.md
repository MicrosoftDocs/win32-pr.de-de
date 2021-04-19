---
description: Die VirtualFree-Funktion hebt die Commits auf und gibt Seiten gemäß den folgenden Regeln frei.
ms.assetid: 8fbd7960-f3f0-4326-ad1d-12b636c0039e
title: Freigeben von virtuellem Speicher
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a7628ed53f956d5cd13f0c7d2d1157443d529129
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106343657"
---
# <a name="freeing-virtual-memory"></a>Freigeben von virtuellem Speicher

Mit der [**VirtualFree**](/windows/win32/api/memoryapi/nf-memoryapi-virtualfree) -Funktion werden Seiten gemäß den folgenden Regeln deaktiviert und freigegeben:

-   Führt einen Commit für mindestens eine zugesicherte Seite aus, wobei der Status der Seiten in "reserviert" geändert wird. Beim Debuggen von Seiten wird der physische Speicher, der den Seiten zugeordnet ist, freigegeben, sodass Sie von einem beliebigen Prozess zugeordnet werden können. Für jeden Block mit zugesicherte Seiten kann ein Commit ausgeführt werden.
-   Gibt einen Block von mindestens einer reservierten Seite frei, wobei der Status der Seiten in "Free" geändert wird. Wenn Sie einen Seiten Block freigeben, wird der Bereich reservierter Adressen vom Prozess zur Verfügung gestellt. Reservierte Seiten können nur freigegeben werden, indem der gesamte Block freigegeben wird, der anfänglich von [**virtualzuordc**](/windows/win32/api/memoryapi/nf-memoryapi-virtualalloc)reserviert wurde.
-   Führt einen Block von mindestens einer übergebenen Seite gleichzeitig aus und gibt den Zustand der Seiten frei. Der angegebene Block muss den gesamten Block enthalten, der anfänglich von [**virtualzuordc**](/windows/win32/api/memoryapi/nf-memoryapi-virtualalloc)reserviert ist, und für alle Seiten muss zurzeit ein Commit ausgeführt werden.

Nachdem ein Speicherblock freigegeben oder freigegeben wurde, können Sie nicht mehr darauf verweisen. Alle Informationen, die möglicherweise in diesem Speicher vorhanden waren, sind nicht mehr vorhanden. Der Versuch, eine freie Seite zu lesen oder auf diese zu schreiben, führt zu einer Zugriffs Verletzungs Ausnahme. Wenn Sie Informationen benötigen, können Sie keinen Arbeitsspeicher mit diesen Informationen Debuggen oder freigeben.

Um anzugeben, dass die Daten in einem Speicherbereich nicht mehr von Interesse sind, nennen Sie [**virtualbelegc**](/windows/win32/api/memoryapi/nf-memoryapi-virtualalloc) mit dem **\_ Zurücksetzen** von Arbeitsbereichen. Die Seiten werden nicht aus der Auslagerungs Datei gelesen oder in diese geschrieben. Der Speicherblock kann jedoch später wieder verwendet werden.

 

 
