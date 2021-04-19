---
description: Ein untergeordneter Prozess kann mehrere Eigenschaften und Ressourcen von seinem übergeordneten Prozess erben.
ms.assetid: c530e723-2d40-4022-a259-dfc650604e44
title: Vererbung (Prozesse und Threads)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4713fe398360b510fab3c66f5cf74dc07b642dac
ms.sourcegitcommit: 3d718d8f69d3f86eaecf94c5705d761c5a9ef4a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/20/2020
ms.locfileid: "106341753"
---
# <a name="inheritance"></a>Vererbung

Ein untergeordneter Prozess kann mehrere Eigenschaften und Ressourcen von seinem übergeordneten Prozess erben. Sie können auch verhindern, dass ein untergeordneter Prozess Eigenschaften aus dem übergeordneten Prozess erbt. Folgendes kann geerbt werden:

-   Geöffnete Handles, die von der Funktion "up [**File**](/windows/desktop/api/fileapi/nf-fileapi-createfilea) " zurückgegeben werden. Dies umfasst Handles für Dateien, Konsolen Eingabepuffer, Konsolenbildschirm Puffer, Named Pipes, serielle Kommunikationsgeräte und Postfächer.
-   Öffnende Handles zum verarbeiten, Thread, Mutex, Ereignis, Semaphore, Named Pipe, anonymen Pipe und Datei Zuordnungsobjekten. Diese werden von den Funktionen " [**forateprocess**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-createprocessa)", " [**foratethread**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-createthread)", " [**foratemutex**](/windows/desktop/api/synchapi/nf-synchapi-createmutexa)", "up [**Event**](/windows/desktop/api/synchapi/nf-synchapi-createeventa)", " [**foratesemaphore**](/windows/desktop/api/winbase/nf-winbase-createsemaphorea)", " [**foratenamedpipe**](/windows/desktop/api/winbase/nf-winbase-createnamedpipea)", " [**foratepipe**](/windows/desktop/api/namedpipeapi/nf-namedpipeapi-createpipe)" und " [**foratefilemapping**](/windows/desktop/api/winbase/nf-winbase-createfilemappinga) " zurückgegeben.
-   Umgebungsvariablen.
-   Das aktuelle Verzeichnis.
-   Die Konsole, es sei denn, der Prozess ist getrennt, oder es wird eine neue Konsole erstellt. Bei einem untergeordneten Konsolen Prozess können auch die Standard Handles des übergeordneten Elements sowie der Zugriff auf den Eingabepuffer und den aktiven Bildschirm Puffer vererbt werden.
-   Der Fehler Modus, wie von der [**SetErrorMode**](/windows/desktop/api/errhandlingapi/nf-errhandlingapi-seterrormode) -Funktion festgelegt.
-   Die Prozessor Affinitäts Maske.
-   Die Zuordnung zu einem Auftrag.

Der untergeordnete Prozess erbt nicht Folgendes:

-   Prioritäts Klasse.
-   Handles, die von " [**localzuweisung**](/windows/desktop/api/winbase/nf-winbase-localalloc)", " [**Globalzuweisung**](/windows/desktop/api/winbase/nf-winbase-globalalloc)", " [**HeapCreate**](/windows/desktop/api/heapapi/nf-heapapi-heapcreate)" und " [**Heapzuweisung**](/windows/desktop/api/heapapi/nf-heapapi-heapalloc)" zurückgegeben werden.
-   Pseudo Handles, wie in den Handles, die von der [**GetCurrentProcess**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-getcurrentprocess) -Funktion oder der [**GetCurrentThread**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-getcurrentthread) -Funktion zurückgegeben werden. Diese Handles sind nur für den aufrufenden Prozess gültig.
-   Von der [**LoadLibrary**](/windows/desktop/api/libloaderapi/nf-libloaderapi-loadlibrarya) -Funktion zurückgegebene dll-Modul Handles.
-   GDI oder Benutzer Handles, z. b. **hBitmap** oder **HMENU**.

## <a name="inheriting-handles"></a>Erben von Handles

Ein untergeordneter Prozess kann einige der übergeordneten Handles erben, aber keine anderen erben. Um die Vererbung eines Handles zu bewirken, müssen Sie zwei Schritte ausführen:

-   Geben Sie an, dass das Handle geerbt werden soll, wenn Sie das Handle erstellen, öffnen oder duplizieren. Erstellungs Funktionen verwenden in der Regel den **binherithandle** -Member einer Struktur von [**Sicherheits \_ Attributen**](/previous-versions/windows/desktop/legacy/aa379560(v=vs.85)) zu diesem Zweck. [**Duplialisiehandle**](/windows/desktop/api/handleapi/nf-handleapi-duplicatehandle) verwendet den *binherithandles* -Parameter.
-   Gibt an, dass vererbbare Handles geerbt werden sollen, indem der *binherithandles* -Parameter beim Aufrufen der [**CreateProcess**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-createprocessa) -Funktion auf true festgelegt wird. Außerdem muss der **dwFlags** -Member der [**STARTUPINFO**](/windows/win32/api/processthreadsapi/ns-processthreadsapi-startupinfoa) -Struktur Startf-usestdhandles enthalten, um die Standardeingabe, Standardausgabe und Standardfehler Handles zu erben \_ .

Um eine Liste der Handles anzugeben, die von einem bestimmten untergeordneten Prozess geerbt werden sollen, müssen Sie die Funktion [**updateprocthreadattribute**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-updateprocthreadattribute) mit dem *PROC_THREAD_ATTRIBUTE_HANDLE_LIST* -Flag aufrufen.

Ein geerbtes Handle verweist auf das gleiche Objekt im untergeordneten Prozess wie im übergeordneten Prozess. Außerdem verfügt sie über dieselben Werte und Zugriffsberechtigungen. Wenn ein Prozess den Status des Objekts ändert, wirkt sich die Änderung daher auf beide Prozesse aus. Um ein Handle zu verwenden, muss der untergeordnete Prozess den Handle-Wert abrufen und das Objekt, auf das es verweist, "wissen". Normalerweise kommuniziert der übergeordnete Prozess diese Informationen über die Befehlszeile, den Umgebungsblock oder eine Form der [prozessübergreifenden Kommunikation](/windows/desktop/ipc/interprocess-communications)an den untergeordneten Prozess.

Verwenden Sie [**die Funktion**](/windows/win32/api/handleapi/nf-handleapi-sethandleinformation) "-Funktion", um zu steuern, ob ein vorhandenes handle vererbbar ist.

## <a name="inheriting-environment-variables"></a>Erbt Umgebungsvariablen

Ein untergeordneter Prozess erbt die Umgebungsvariablen des übergeordneten Prozesses standardmäßig. Allerdings [**kann der**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-createprocessa) übergeordnete Prozess über den übergeordneten Prozess einen anderen Block von Umgebungsvariablen angeben. Weitere Informationen finden Sie unter [Umgebungsvariablen](environment-variables.md).

## <a name="inheriting-the-current-directory"></a>Erbt das aktuelle Verzeichnis.

Die [**GetCurrentDirectory**](/windows/desktop/api/winbase/nf-winbase-getcurrentdirectory) -Funktion Ruft das aktuelle Verzeichnis des aufrufenden Prozesses ab. Ein untergeordneter Prozess erbt standardmäßig das aktuelle Verzeichnis seines übergeordneten Prozesses. Allerdings [**ermöglicht der übergeordnete Prozess dem**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-createprocessa) übergeordneten Prozess das Angeben eines anderen aktuellen Verzeichnisses für den untergeordneten Prozess. Verwenden Sie die [**SetCurrentDirectory**](/windows/desktop/api/winbase/nf-winbase-setcurrentdirectory) -Funktion, um das aktuelle Verzeichnis des aufrufenden Prozesses zu ändern.
