---
description: Wenn eine Datei von einem Prozess mithilfe der Funktion "deatefile" geöffnet wird, wird ihr ein Datei Handle zugeordnet, bis der Prozess beendet oder das Handle mit der Funktion "CloseHandle" geschlossen wird.
ms.assetid: c8188e28-ec1b-4746-86f6-5996ff271677
title: Datei Handles
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 63a54db1935108ab18666fb460a071d77c50f793
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "103868244"
---
# <a name="file-handles"></a>Datei Handles

Wenn eine Datei von einem Prozess mithilfe der Funktion " [**deatefile**](/windows/desktop/api/FileAPI/nf-fileapi-createfilea) " geöffnet wird, wird ihr ein *Datei Handle* zugeordnet, bis der Prozess beendet oder das Handle mit der Funktion " [**CloseHandle**](/windows/desktop/api/handleapi/nf-handleapi-closehandle) " geschlossen wird. Das Datei Handle wird verwendet, um die Datei in vielen Funktionsaufrufen zu identifizieren.

Jedes Datei Handle-und Datei Objekt ist im Allgemeinen für jeden Prozess eindeutig, der eine Datei öffnet – die einzige Ausnahme ist, wenn ein Datei Handle, das von einem Prozess gehalten wird, dupliziert wird oder wenn ein untergeordneter Prozess die Datei Handles des übergeordneten Prozesses erbt. In diesen Fällen sind diese Datei Handles eindeutig, aber sehen Sie sich ein einzelnes, frei gegebenes Datei Objekt an. Weitere Informationen zum Duplizieren von Datei Handles, die von Prozessen gehalten werden, finden Sie unter [**duplialisierandle**](/windows/desktop/api/handleapi/nf-handleapi-duplicatehandle) .

Beachten Sie Folgendes: während die Datei Handles in der Regel für einen Prozess privat sind, ist die Datei, auf die die Datei behandelt, nicht. Daher müssen Prozesse und Threads, die dieselbe Datei gemeinsam verwenden, Ihren Zugriff synchronisieren. Bei den meisten Vorgängen in einer Datei identifiziert ein Prozess die Datei über den privaten Pool von Handles.

 

 
