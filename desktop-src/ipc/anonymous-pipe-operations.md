---
description: Anonyme Pipe-Vorgänge, einschließlich Pipe-Erstellung, Schreiben in eine Pipe, Pipehandles.
ms.assetid: df81471c-1072-4456-a877-304e76ade4bd
title: Anonyme Pipe-Vorgänge
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 963d7127c51859b05e570d00291470a49be5ba66
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106348332"
---
# <a name="anonymous-pipe-operations"></a>Anonyme Pipe-Vorgänge

Die Funktion " [**kreatepipe**](/windows/win32/api/namedpipeapi/nf-namedpipeapi-createpipe) " erstellt eine anonyme Pipe und gibt zwei Handles zurück: ein Lese Handle für die Pipe und ein Schreib Handle für die Pipe. Das Lese handle hat schreibgeschützten Zugriff auf die Pipe, und das Schreib handle hat schreibgeschützten Zugriff auf die Pipe. Um mithilfe der Pipe zu kommunizieren, muss der Pipeserver ein Pipehandle an einen anderen Prozess übergeben. Dies erfolgt in der Regel durch Vererbung. Das heißt, der Prozess ermöglicht es, dass das Handle von einem untergeordneten Prozess geerbt wird. Der Prozess kann auch ein Pipehandle mithilfe der [**duplikatandle**](/windows/desktop/api/handleapi/nf-handleapi-duplicatehandle) -Funktion duplizieren und an einen nicht verknüpften Prozess über eine Form der prozessübergreifenden Kommunikation (z. b. DDE oder Shared Memory) senden.

Abhängig davon, ob der Client die anonyme Pipe zum Senden von Informationen oder zum Empfangen von Informationen verwenden soll, kann ein Pipeserver entweder das Lese handle oder das Schreib Handle an den Pipe-Client senden. Um aus der Pipe zu lesen, verwenden Sie den Lese Handle der Pipe in einem aufzurufenden Vorgang der Funktion "read [**File**](/windows/desktop/api/fileapi/nf-fileapi-readfile) ". Der Read **File** -Rückruf gibt zurück, wenn ein anderer Prozess in die Pipe geschrieben hat. Der **Vorgang** zum Lesen von Dateien kann auch zurückgeben, wenn alle Schreib Handles für die Pipe geschlossen wurden, oder wenn ein Fehler auftritt, bevor der Lesevorgang abgeschlossen wurde.

Verwenden Sie zum Schreiben in die Pipe den Schreib Handle der Pipe in einem Aufrufe der Funktion "Write [**File**](/windows/desktop/api/fileapi/nf-fileapi-writefile) ". Der **schreibdatei** -Aufrufvorgang wird erst zurückgegeben, wenn die angegebene Anzahl von Bytes in die Pipe geschrieben wurde oder ein Fehler auftritt. Wenn der Pipe-Puffer voll ist und mehr Bytes geschrieben werden müssen, wird " **Write File** " erst zurückgegeben, wenn ein anderer Prozess aus der Pipe liest und somit mehr Puffer Speicherplatz zur Verfügung steht. Der Pipeserver gibt die Puffergröße für die Pipe an, wenn er " [**featepipe**](/windows/win32/api/namedpipeapi/nf-namedpipeapi-createpipe)" aufruft.

Asynchrone (überlappende) Lese-und Schreibvorgänge werden von anonymen Pipes nicht unterstützt. Dies bedeutet, dass Sie die Funktionen "read [**fileex**](/windows/desktop/api/fileapi/nf-fileapi-readfileex) " und " [**schreitefileex**](/windows/desktop/api/fileapi/nf-fileapi-writefileex) " nicht mit anonymen Pipes verwenden können. Außerdem wird der *lpoverlused* -Parameter von "read [**File**](/windows/desktop/api/fileapi/nf-fileapi-readfile) " und " [**Write File**](/windows/desktop/api/fileapi/nf-fileapi-writefile) " ignoriert, wenn diese Funktionen mit anonymen Pipes verwendet werden.

Eine anonyme Pipe ist so lange vorhanden, bis alle Pipe-Handles, sowohl Lese-als auch Schreibvorgänge, geschlossen wurden. Ein Prozess kann seine Pipehandles mithilfe der [**CloseHandle**](/windows/desktop/api/handleapi/nf-handleapi-closehandle) -Funktion schließen. Alle Pipehandles werden auch geschlossen, wenn der Prozess beendet wird.

Anonyme Pipes werden mithilfe einer Named Pipe mit einem eindeutigen Namen implementiert. Daher können Sie häufig ein Handle an eine anonyme Pipe an eine Funktion übergeben, die ein Handle für eine Named Pipe erfordert.

 

 
