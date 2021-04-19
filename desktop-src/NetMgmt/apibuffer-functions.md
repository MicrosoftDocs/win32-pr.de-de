---
title: Apibuffer-Funktionen
description: Die apibuffer-Funktionen der Netzwerkverwaltung werden verwendet, um die von einer Anwendung verwendete Speicher Belegung mit Netzwerk Verwaltungsfunktionen zu verwalten.
ms.assetid: bf2fe8aa-dda6-4f6b-9c52-d7a96b96da18
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b316c6b2ee2d4095c15d5e859dd0069978c7ff91
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "106341535"
---
# <a name="apibuffer-functions"></a>Apibuffer-Funktionen

Die apibuffer-Funktionen der Netzwerkverwaltung werden verwendet, um die von einer Anwendung verwendete Speicher Belegung mit Netzwerk Verwaltungsfunktionen zu verwalten. Im Allgemeinen sollten Sie jedoch für anderen von einer Anwendung verwendeten Arbeitsspeicher die [Speicherverwaltungsfunktionen](/windows/desktop/Memory/memory-management-functions) anstelle dieser apibuffer-Funktionen verwenden.

Die apibuffer-Funktionen sind nachfolgend aufgeführt.



| Funktion                                                 | BESCHREIBUNG                                                                                                               |
|----------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------|
| [**"Ntapibuffer" zuordnen**](/windows/desktop/api/Lmapibuf/nf-lmapibuf-netapibufferallocate)     | Belegt Speicher aus dem Heap. Wenn Sie die Kompatibilität mit der Funktion " **nettapibufferfree** " benötigen, können Sie diese Funktion aufrufen. |
| [**"Nettapibufferfree"**](/windows/desktop/api/Lmapibuf/nf-lmapibuf-netapibufferfree)             | Gibt Arbeitsspeicher frei, der von der Funktion " **nettapibufferbeleg;** " und anderen Netzwerk Verwaltungsfunktionen belegt wird                   |
| [**"Nettapibufferrezuordnen"**](/windows/desktop/api/Lmapibuf/nf-lmapibuf-netapibufferreallocate) | Ändert die Größe eines Puffers, der durch einen Aufrufen der Funktion " **nettapibufferallo"** zugeordnet wird.                                |
| [**"Nettapibuffersize"**](/windows/desktop/api/Lmapibuf/nf-lmapibuf-netapibuffersize)             | Gibt die Größe eines Puffers in Bytes zurück, der durch einen Aufrufen der Funktion " **nettapibufferallo"** zugeordnet wird.                     |



 

Für Remote fähige Funktionen, die Informationen an den Aufrufer zurückgeben, ordnet die RPC-Lauf Zeit Bibliothek den Puffer zu, der die Rückgabe Informationen enthält. Wenn der Aufrufer die Verarbeitung der Informationen abgeschlossen hat, muss er die Funktion " [**nettapibufferfree**](/windows/desktop/api/Lmapibuf/nf-lmapibuf-netapibufferfree) " aufrufen, um den zugeordneten Puffer freizugeben.

 

 