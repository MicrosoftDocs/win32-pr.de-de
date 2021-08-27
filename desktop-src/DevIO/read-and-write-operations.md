---
description: Windows unterstützt sowohl synchrone als auch asynchrone (überlappende) Datei-E/A-Vorgänge für serielle Kommunikationsressourcen.
ms.assetid: cee44596-ad73-4afb-b86a-744b0b46d9d5
title: Lese- und Schreibvorgänge
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b3a1c9cca5079cc6f473b07c02212da6f42156305b43f4b30eb1de3e6b67e593
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "120109010"
---
# <a name="read-and-write-operations"></a>Lese- und Schreibvorgänge

Windows unterstützt sowohl synchrone als auch asynchrone (überlappende) Datei-E/A-Vorgänge für serielle Kommunikationsressourcen. Überlappende Vorgänge ermöglichen es dem aufrufenden Thread, andere Aufgaben auszuführen, während der Vorgang im Hintergrund ausgeführt wird. Ein Thread verwendet die [**ReadFile-**](/windows/desktop/api/fileapi/nf-fileapi-readfile) oder [**ReadFileEx-Funktion**](/windows/desktop/api/fileapi/nf-fileapi-readfileex) zum Lesen aus einer Kommunikationsressource und die [**WriteFile-**](/windows/desktop/api/fileapi/nf-fileapi-writefile) oder [**WriteFileEx-Funktion**](/windows/desktop/api/fileapi/nf-fileapi-writefileex) zum Schreiben in eine Kommunikationsressource. **ReadFile** und **WriteFile** können synchron oder asynchron ausgeführt werden. **ReadFileEx** und **WriteFileEx** können nur asynchron ausgeführt werden.

Das Verhalten dieser Lese- und Schreibfunktionen wird davon beeinflusst, ob die Funktion als überlappender Vorgang ausgeführt wird, ob die Time out-Parameter dem Handle zugeordnet sind und ob Flusssteuerungsparameter dem Handle zugeordnet sind.

Ein Thread kann auch mithilfe der [**TransmitCommChar-Funktion**](/windows/desktop/api/Winbase/nf-winbase-transmitcommchar) in eine Kommunikationsressource schreiben, die ein angegebenes Zeichen vor allen ausstehenden Daten im Ausgabepuffer überträgt. Diese Funktion ist nützlich für die Übertragung eines Signalzeichens mit hoher Priorität an das empfangende System. Die Übertragung des Zeichens mit hoher Priorität unterliegt weiterhin Time outs der Flusssteuerung und des Schreibvorgangs, und der Vorgang wird synchron ausgeführt.

Ein Thread kann die [**PurgeComm-Funktion**](/windows/desktop/api/Winbase/nf-winbase-purgecomm) verwenden, um alle Zeichen im Ausgabe- oder Eingabepuffer eines Geräts zu verwerfen. **PurgeComm** kann auch ausstehende Lese- oder Schreibvorgänge beenden, auch wenn die Vorgänge nicht abgeschlossen wurden. Wenn ein Thread **PurgeComm** verwendet, um einen Ausgabepuffer zu leeren, werden die gelöschten Zeichen nicht übertragen. Um den Ausgabepuffer zu leeren und gleichzeitig sicherzustellen, dass der Inhalt übertragen wird, kann ein Thread die [**FlushFileBuffers-Funktion**](/windows/desktop/api/fileapi/nf-fileapi-flushfilebuffers) aufrufen (ein synchroner Vorgang). Beachten Sie jedoch, dass **FlushFileBuffers** der Flusssteuerung unterliegt, aber keinen Schreibtime outs unterliegt und erst dann zurückgegeben wird, wenn alle ausstehenden Schreibvorgänge übertragen wurden.

 

 
