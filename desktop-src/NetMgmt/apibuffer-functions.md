---
title: ApiBuffer-Funktionen
description: Die ApiBuffer-Funktionen für die Netzwerkverwaltung werden verwendet, um die Speicherbelegung zu verwalten, die von einer Anwendung mit Netzwerkverwaltungsfunktionen verwendet wird.
ms.assetid: bf2fe8aa-dda6-4f6b-9c52-d7a96b96da18
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a4b0778c216860fe16a673e1bdcc2ac470cbb52a128f0e08d4d32d98df929bc7
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119912479"
---
# <a name="apibuffer-functions"></a>ApiBuffer-Funktionen

Die ApiBuffer-Funktionen für die Netzwerkverwaltung werden verwendet, um die Speicherbelegung zu verwalten, die von einer Anwendung mit Netzwerkverwaltungsfunktionen verwendet wird. Im Allgemeinen sollten Sie jedoch für anderen Arbeitsspeicher, der von einer Anwendung verwendet wird, die [Speicherverwaltungsfunktionen](/windows/desktop/Memory/memory-management-functions) anstelle dieser ApiBuffer-Funktionen verwenden.

Die ApiBuffer-Funktionen sind im Folgenden aufgeführt.



| Funktion                                                 | BESCHREIBUNG                                                                                                               |
|----------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------|
| [**NetApiBufferAllocate**](/windows/desktop/api/Lmapibuf/nf-lmapibuf-netapibufferallocate)     | Belegt Arbeitsspeicher aus dem Heap. Rufen Sie diese Funktion auf, wenn Sie Kompatibilität mit der **NetApiBufferFree-Funktion** benötigen. |
| [**NetApiBufferFree**](/windows/desktop/api/Lmapibuf/nf-lmapibuf-netapibufferfree)             | Gibt von der **NetApiBufferAllocate-Funktion** und anderen Netzwerkverwaltungsfunktionen belegten Arbeitsspeicher frei.                   |
| [**NetApiBufferReallocate**](/windows/desktop/api/Lmapibuf/nf-lmapibuf-netapibufferreallocate) | Ändert die Größe eines Puffers, der durch einen Aufruf der **NetApiBufferAllocate-Funktion** zugeordnet wird.                                |
| [**NetApiBufferSize**](/windows/desktop/api/Lmapibuf/nf-lmapibuf-netapibuffersize)             | Gibt die Größe eines Puffers in Bytes zurück, der durch einen Aufruf der **NetApiBufferAllocate-Funktion** zugeordnet wird.                     |



 

Für Remotable-Funktionen, die Informationen an den Aufrufer zurückgeben, ordnet die RPC-Laufzeitbibliothek den Puffer zu, der die Rückgabeinformationen enthält. Wenn der Aufrufer die Verarbeitung der Informationen abgeschlossen hat, muss er die [**NetApiBufferFree-Funktion**](/windows/desktop/api/Lmapibuf/nf-lmapibuf-netapibufferfree) aufrufen, um den zugeordneten Puffer frei zu machen.

 

 