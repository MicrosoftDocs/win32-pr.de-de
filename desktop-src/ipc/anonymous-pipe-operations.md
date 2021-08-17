---
description: Anonyme Pipevorgänge, einschließlich Pipeerstellung, Schreiben in eine Pipe, Pipehandles.
ms.assetid: df81471c-1072-4456-a877-304e76ade4bd
title: Anonyme Pipevorgänge
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f0c4c684daab5dd1c18dbf5eb22e2191f193e7ecc3b088ac58e3f680f442897a
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119350710"
---
# <a name="anonymous-pipe-operations"></a>Anonyme Pipevorgänge

Die [**CreatePipe-Funktion**](/windows/win32/api/namedpipeapi/nf-namedpipeapi-createpipe) erstellt eine anonyme Pipe und gibt zwei Handles zurück: ein Lesehandles für die Pipe und ein Schreibhandles für die Pipe. Das Lesehandles verfügt über schreibgeschützten Zugriff auf die Pipe, und das Schreibhandles hat schreibgeschützten Zugriff auf die Pipe. Für die Kommunikation mithilfe der Pipe muss der Pipeserver ein Pipehand handle an einen anderen Prozess übergeben. In der Regel erfolgt dies durch Vererbung. Das heißt, der Prozess ermöglicht, dass das Handle von einem untergeordneten Prozess geerbt wird. Der Prozess kann auch ein Pipehandle mithilfe der [**DuplicateHandle-Funktion**](/windows/desktop/api/handleapi/nf-handleapi-duplicatehandle) duplizieren und an einen nicht verbundenen Prozess senden, indem eine Form der prozessübergreifenden Kommunikation verwendet wird, z. B. DDE oder freigegebener Arbeitsspeicher.

Ein Pipeserver kann entweder das Lesehandles oder das Schreibhandles an den Pipeclient senden, je nachdem, ob der Client die anonyme Pipe verwenden soll, um Informationen zu senden oder Informationen zu empfangen. Verwenden Sie zum Lesen aus der Pipe das Lesehandles der Pipe in einem Aufruf der [**ReadFile-Funktion.**](/windows/desktop/api/fileapi/nf-fileapi-readfile) Der **ReadFile-Aufruf** gibt zurück, wenn ein anderer Prozess in die Pipe geschrieben wurde. Der **ReadFile-Aufruf** kann auch zurückgeben, wenn alle Schreibhandles für die Pipe geschlossen wurden oder ein Fehler auftritt, bevor der Lesevorgang abgeschlossen wurde.

Um in die Pipe zu schreiben, verwenden Sie das Schreibhand handle der Pipe in einem Aufruf der [**WriteFile-Funktion.**](/windows/desktop/api/fileapi/nf-fileapi-writefile) Der **WriteFile-Aufruf** wird erst zurückgegeben, wenn er die angegebene Anzahl von Bytes in die Pipe geschrieben hat oder ein Fehler auftritt. Wenn der Pipepuffer voll ist und mehr Bytes geschrieben werden müssen, gibt **WriteFile** erst dann zurück, wenn ein anderer Prozess aus der Pipe liest, wodurch mehr Pufferspeicher verfügbar wird. Der Pipeserver gibt die Puffergröße für die Pipe an, wenn er [**CreatePipe aufruft.**](/windows/win32/api/namedpipeapi/nf-namedpipeapi-createpipe)

Asynchrone (überlappende) Lese- und Schreibvorgänge werden von anonymen Pipes nicht unterstützt. Dies bedeutet, dass Sie die [**Funktionen ReadFileEx**](/windows/desktop/api/fileapi/nf-fileapi-readfileex) und [**WriteFileEx nicht**](/windows/desktop/api/fileapi/nf-fileapi-writefileex) mit anonymen Pipes verwenden können. Darüber hinaus wird der *lpOverlapped-Parameter* von [**ReadFile**](/windows/desktop/api/fileapi/nf-fileapi-readfile) und [**WriteFile**](/windows/desktop/api/fileapi/nf-fileapi-writefile) ignoriert, wenn diese Funktionen mit anonymen Pipes verwendet werden.

Eine anonyme Pipe ist vorhanden, bis alle Pipehandles (Sowohl Lese- als auch Schreibzugriff) geschlossen wurden. Ein Prozess kann seine Pipehandles mithilfe der [**CloseHandle-Funktion**](/windows/desktop/api/handleapi/nf-handleapi-closehandle) schließen. Alle Pipehandles werden auch geschlossen, wenn der Prozess beendet wird.

Anonyme Pipes werden mithilfe einer Named Pipe mit einem eindeutigen Namen implementiert. Daher können Sie häufig ein Handle an eine anonyme Pipe an eine Funktion übergeben, die ein Handle an eine Named Pipe erfordert.

 

 
