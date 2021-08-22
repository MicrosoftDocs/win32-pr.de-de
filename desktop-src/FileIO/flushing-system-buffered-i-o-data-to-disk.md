---
description: Windows speichert die Daten in Dateilese- und -schreibvorgängen in vom System verwalteten Datenpuffern, um die Datenträgerleistung zu optimieren.
ms.assetid: e8c12a1d-f6a4-4850-814d-6f0a712f8f9a
title: Leeren System-Buffered E/A-Daten auf den Datenträger
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 44740158ce1a5a2c3449a0fc5b90bc04bb0da525709cf7ee05c8768d10c39460
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119068700"
---
# <a name="flushing-system-buffered-io-data-to-disk"></a>Leeren System-Buffered E/A-Daten auf den Datenträger

Windows speichert die Daten in Dateilese- und -schreibvorgängen in vom System verwalteten Datenpuffern, um die Datenträgerleistung zu optimieren. Wenn eine Anwendung in eine Datei schreibt, puffert das System die Daten in der Regel und schreibt die Daten regelmäßig auf den Datenträger. Eine Anwendung kann das Betriebssystem zwingen, den Inhalt dieser Datenpuffer mithilfe der [**FlushFileBuffers-Funktion**](/windows/desktop/api/FileAPI/nf-fileapi-flushfilebuffers) auf den Datenträger zu schreiben. Alternativ kann eine Anwendung angeben, dass Schreibvorgänge den Datenpuffer umgehen und direkt auf den Datenträger schreiben sollen, indem das **FLAG FILE FLAG NO \_ \_ \_ BUFFERING** festgelegt wird, wenn die Datei mit der [**CreateFile-Funktion**](/windows/desktop/api/FileAPI/nf-fileapi-createfilea) erstellt oder geöffnet wird.

Wenn beim Schließen der Datei Daten im internen Puffer vorhanden sind, schreibt das Betriebssystem den Inhalt des Puffers nicht automatisch auf den Datenträger, bevor die Datei geschlossen wird. Wenn die Anwendung nicht erzwingt, dass das Betriebssystem den Puffer vor dem Schließen der Datei auf den Datenträger schreibt, bestimmt der Cachealgorithmus, wann der Puffer geschrieben wird.

> [!Note]  
> Der Zugriff auf einen Datenpuffer während eines Lese- oder Schreibvorgang kann den Puffer beschädigt. Anwendungen dürfen den Datenpuffer, den ein Lese- oder Schreibvorgang verwendet, nicht lesen, in diesen schreiben, neu erstellen oder freispeichern, bis der Vorgang abgeschlossen ist.

 

 

 



