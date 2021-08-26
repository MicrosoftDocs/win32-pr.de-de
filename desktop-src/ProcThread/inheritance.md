---
description: Ein untergeordneter Prozess kann mehrere Eigenschaften und Ressourcen von seinem übergeordneten Prozess erben.
ms.assetid: c530e723-2d40-4022-a259-dfc650604e44
title: Vererbung (Prozesse und Threads)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2f50b191ee24783f7213ac15f61c435ebd696175a3042d79e2f359ef61097fe0
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "120032590"
---
# <a name="inheritance"></a>Vererbung

Ein untergeordneter Prozess kann mehrere Eigenschaften und Ressourcen von seinem übergeordneten Prozess erben. Sie können auch verhindern, dass ein untergeordneter Prozess Eigenschaften von seinem übergeordneten Prozess erbt. Folgendes kann geerbt werden:

-   Öffnen Sie handles, die von der [**CreateFile-Funktion**](/windows/desktop/api/fileapi/nf-fileapi-createfilea) zurückgegeben werden. Dies schließt Handles für Dateien, Konsoleneingabepuffer, Konsolenbildschirmpuffer, Named Pipes, serielle Kommunikationsgeräte und Mailslots ein.
-   Öffnen Sie Handles für Verarbeitungs-, Thread-, Mutex-, Ereignis-, Semaphor-, Named Pipe-, anonymous-pipe- und Dateizuordnungsobjekte. Diese werden von den Funktionen [**CreateProcess,**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-createprocessa) [**CreateThread,**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-createthread) [**CreateMutex,**](/windows/desktop/api/synchapi/nf-synchapi-createmutexa) [**CreateEvent,**](/windows/desktop/api/synchapi/nf-synchapi-createeventa) [**CreateSemaphore,**](/windows/desktop/api/winbase/nf-winbase-createsemaphorea) [**CreateNamedPipe,**](/windows/desktop/api/winbase/nf-winbase-createnamedpipea) [**CreatePipe**](/windows/desktop/api/namedpipeapi/nf-namedpipeapi-createpipe)und [**CreateFileMapping**](/windows/desktop/api/winbase/nf-winbase-createfilemappinga) zurückgegeben.
-   Umgebungsvariablen.
-   Das aktuelle Verzeichnis.
-   Die Konsole, es sei denn, der Prozess wird getrennt oder eine neue Konsole erstellt. Ein untergeordneter Konsolenprozess kann auch die Standardhandles des übergeordneten Elements erben sowie Zugriff auf den Eingabepuffer und den aktiven Bildschirmpuffer.
-   Der Fehlermodus, wie von der [**SetErrorMode-Funktion**](/windows/desktop/api/errhandlingapi/nf-errhandlingapi-seterrormode) festgelegt.
-   Die Prozessoraffinitätsmaske.
-   Die Zuordnung zu einem Auftrag.

Der untergeordnete Prozess erbt nicht Folgendes:

-   Priority-Klasse.
-   Handles, die von [**LocalAlloc,**](/windows/desktop/api/winbase/nf-winbase-localalloc) [**GlobalAlloc,**](/windows/desktop/api/winbase/nf-winbase-globalalloc) [**HeapCreate**](/windows/desktop/api/heapapi/nf-heapapi-heapcreate)und [**HeapAlloc**](/windows/desktop/api/heapapi/nf-heapapi-heapalloc)zurückgegeben werden.
-   Pseudohandles, wie in den Handles, die von der [**GetCurrentProcess-**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-getcurrentprocess) oder [**GetCurrentThread-Funktion**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-getcurrentthread) zurückgegeben werden. Diese Handles sind nur für den aufrufenden Prozess gültig.
-   Dll-Modulhandles, die von der [**LoadLibrary-Funktion**](/windows/desktop/api/libloaderapi/nf-libloaderapi-loadlibrarya) zurückgegeben werden.
-   GDI- oder USER-Handles, z. B. **HBITMAP** oder **HMENU.**

## <a name="inheriting-handles"></a>Vererben von Handles

Ein untergeordneter Prozess kann einige der Handles des übergeordneten Elements erben, andere jedoch nicht. Um zu bewirken, dass ein Handle geerbt wird, müssen Sie zwei Dinge tun:

-   Geben Sie an, dass das Handle geerbt werden soll, wenn Sie das Handle erstellen, öffnen oder duplizieren. Erstellungsfunktionen verwenden in der Regel den **bInheritHandle-Member** einer [**SECURITY \_ ATTRIBUTES-Struktur**](/previous-versions/windows/desktop/legacy/aa379560(v=vs.85)) für diesen Zweck. [**DuplicateHandle**](/windows/desktop/api/handleapi/nf-handleapi-duplicatehandle) verwendet den *bInheritHandles-Parameter.*
-   Geben Sie an, dass vererbbare Handles geerbt werden sollen, indem Sie den *bInheritHandles-Parameter* beim Aufrufen der [**CreateProcess-Funktion**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-createprocessa) auf TRUE festlegen. Darüber hinaus muss der **dwFlags-Member** der [**STARTUPINFO-Struktur**](/windows/win32/api/processthreadsapi/ns-processthreadsapi-startupinfoa) STARTF USESTDHANDLES enthalten, um die Standardeingabe, die Standardausgabe und die Standardfehlerhandles zu \_ erben.

Um eine Liste der Handles anzugeben, die von einem bestimmten untergeordneten Prozess geerbt werden sollen, rufen Sie die [**UpdateProcThreadAttribute-Funktion**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-updateprocthreadattribute) mit dem *flag PROC_THREAD_ATTRIBUTE_HANDLE_LIST* auf.

Ein geerbtes Handle bezieht sich auf das gleiche Objekt im untergeordneten Prozess wie im übergeordneten Prozess. Sie verfügt auch über den gleichen Wert und die gleichen Zugriffsberechtigungen. Wenn also ein Prozess den Zustand des Objekts ändert, wirkt sich die Änderung auf beide Prozesse aus. Um ein Handle zu verwenden, muss der untergeordnete Prozess den Handlewert abrufen und das Objekt, auf das er verweist, "kennen". In der Regel kommuniziert der übergeordnete Prozess diese Informationen über die Befehlszeile, den Umgebungsblock oder eine Form der [prozessübergreifenden Kommunikation](/windows/desktop/ipc/interprocess-communications)an den untergeordneten Prozess.

Verwenden Sie die [**SetHandleInformation-Funktion,**](/windows/win32/api/handleapi/nf-handleapi-sethandleinformation) um zu steuern, ob ein vorhandenes Handle vererbbar ist oder nicht.

## <a name="inheriting-environment-variables"></a>Erben von Umgebungsvariablen

Ein untergeordneter Prozess erbt standardmäßig die Umgebungsvariablen des übergeordneten Prozesses. Mit [**CreateProcess**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-createprocessa) kann der übergeordnete Prozess jedoch einen anderen Block von Umgebungsvariablen angeben. Weitere Informationen finden Sie unter [Umgebungsvariablen.](environment-variables.md)

## <a name="inheriting-the-current-directory"></a>Erben des aktuellen Verzeichnisses

Die [**GetCurrentDirectory-Funktion**](/windows/desktop/api/winbase/nf-winbase-getcurrentdirectory) ruft das aktuelle Verzeichnis des aufrufenden Prozesses ab. Ein untergeordneter Prozess erbt standardmäßig das aktuelle Verzeichnis des übergeordneten Prozesses. Mit [**CreateProcess**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-createprocessa) kann der übergeordnete Prozess jedoch ein anderes aktuelles Verzeichnis für den untergeordneten Prozess angeben. Verwenden Sie die [**Funktion SetCurrentDirectory,**](/windows/desktop/api/winbase/nf-winbase-setcurrentdirectory) um das aktuelle Verzeichnis des aufrufenden Prozesses zu ändern.
