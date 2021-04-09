---
description: Windows unterstützt sowohl synchrone als auch asynchrone (überlappende) Datei-e/a-Vorgänge für serielle Kommunikationsressourcen.
ms.assetid: cee44596-ad73-4afb-b86a-744b0b46d9d5
title: Lese-und Schreibvorgänge
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a26cc53dbe8c52286fe53c81202ab3828808b1aa
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104126637"
---
# <a name="read-and-write-operations"></a>Lese-und Schreibvorgänge

Windows unterstützt sowohl synchrone als auch asynchrone (überlappende) Datei-e/a-Vorgänge für serielle Kommunikationsressourcen. Überlappende Vorgänge ermöglichen dem aufrufenden Thread, andere Aufgaben auszuführen, während der Vorgang im Hintergrund ausgeführt wird. Ein Thread verwendet die Funktion "read [**File**](/windows/desktop/api/fileapi/nf-fileapi-readfile) " oder " [**lesefileex**](/windows/desktop/api/fileapi/nf-fileapi-readfileex) ", um aus einer Kommunikations Ressource zu lesen, und die Funktion "Write [**File**](/windows/desktop/api/fileapi/nf-fileapi-writefile) " oder " [**Write fileex**](/windows/desktop/api/fileapi/nf-fileapi-writefileex) ", um in eine Kommunikations Ressource zu schreiben. "Read **File** " und " **Write File** " können synchron oder asynchron ausgeführt werden. "Read **fileex** " und " **Write fileex** " können nur asynchron ausgeführt werden.

Das Verhalten dieser Lese-und Schreibfunktionen ist davon betroffen, ob die Funktion als überlappende Operation ausgeführt wird, ob die Timeout Parameter dem Handle zugeordnet sind und ob Fluss Steuerungsparameter dem Handle zugeordnet sind.

Ein Thread kann auch mithilfe der [**transmitcommchar**](/windows/desktop/api/Winbase/nf-winbase-transmitcommchar) -Funktion in eine Kommunikations Ressource schreiben, die ein bestimmtes Zeichen vor allen ausstehenden Daten im Ausgabepuffer überträgt. Diese Funktion ist nützlich, wenn ein Signal Zeichen mit hoher Priorität an das empfangende System übertragen werden soll. Die Übertragung des Zeichens mit hoher Priorität unterliegt weiterhin der Fluss Steuerung und der Schreib Timeouts, und der Vorgang wird synchron ausgeführt.

Ein Thread kann die [**PurgeComm**](/windows/desktop/api/Winbase/nf-winbase-purgecomm) -Funktion verwenden, um alle Zeichen in der Ausgabe des Geräts oder im Eingabepuffer zu verwerfen. **PurgeComm** kann auch ausstehende Lese-oder Schreibvorgänge beenden, auch wenn die Vorgänge nicht abgeschlossen wurden. Wenn ein Thread **PurgeComm** zum leeren eines Ausgabepuffers verwendet, werden die gelöschten Zeichen nicht übertragen. Um den Ausgabepuffer zu leeren, während sichergestellt wird, dass der Inhalt übertragen wird, kann ein Thread die [**FlushFileBuffers**](/windows/desktop/api/fileapi/nf-fileapi-flushfilebuffers) -Funktion aufrufen (ein synchroner Vorgang). Beachten Sie jedoch, dass **FlushFileBuffers** der Fluss Steuerung unterliegt, aber keine Timeouts schreiben und erst dann zurückgegeben wird, wenn alle ausstehenden Schreibvorgänge übertragen wurden.

 

 
