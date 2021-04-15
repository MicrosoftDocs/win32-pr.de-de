---
description: Windows speichert die Daten in Datei Lese-und Schreibvorgängen in vom System verwalteten Daten Puffern, um die Datenträger Leistung zu optimieren.
ms.assetid: e8c12a1d-f6a4-4850-814d-6f0a712f8f9a
title: Leeren von System-Buffered e/a-Daten auf den Datenträger
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0639c5ea909d96a248bb563f1c6a08cd7a526d98
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "104529999"
---
# <a name="flushing-system-buffered-io-data-to-disk"></a>Leeren von System-Buffered e/a-Daten auf den Datenträger

Windows speichert die Daten in Datei Lese-und Schreibvorgängen in vom System verwalteten Daten Puffern, um die Datenträger Leistung zu optimieren. Wenn eine Anwendung in eine Datei schreibt, puffert das System in der Regel die Daten und schreibt die Daten in regelmäßigen Abständen auf den Datenträger. Eine Anwendung kann erzwingen, dass das Betriebssystem den Inhalt dieser Datenpuffer mithilfe der [**FlushFileBuffers**](/windows/desktop/api/FileAPI/nf-fileapi-flushfilebuffers) -Funktion auf den Datenträger schreibt. Alternativ kann eine Anwendung festlegen, dass Schreibvorgänge den Datenpuffer umgehen und direkt auf den Datenträger schreiben, indem das **\_ Dateiflag \_ No \_ buffereing** Flag festgelegt wird, [**Wenn die Datei**](/windows/desktop/api/FileAPI/nf-fileapi-createfilea) erstellt oder mit der Funktion "Funktion" geöffnet wird.

Wenn beim Schließen der Datei Daten im internen Puffer vorhanden sind, schreibt das Betriebssystem nicht automatisch den Inhalt des Puffers auf den Datenträger, bevor die Datei geschlossen wird. Wenn die Anwendung das Betriebssystem nicht zwingt, den Puffer vor dem Schließen der Datei auf den Datenträger zu schreiben, bestimmt der cachingalgorithmus, wann der Puffer geschrieben wird.

> [!Note]  
> Wenn Sie auf einen Datenpuffer zugreifen, während ein Lese-oder Schreibvorgang verwendet wird, kann der Puffer beschädigt werden. Anwendungen dürfen den Datenpuffer, den ein Lese-oder Schreibvorgang verwendet, nicht lesen, schreiben, neu zuordnen oder freigeben, bis der Vorgang abgeschlossen ist.

 

 

 



