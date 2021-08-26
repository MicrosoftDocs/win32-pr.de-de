---
description: Es gibt eine Vielzahl von Funktionen zum Abrufen von Informationen zu Prozessen.
ms.assetid: f9ec6aa5-15ad-47e6-b5f8-8ac4daaf178f
title: Abrufen zusätzlicher Prozessinformationen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 98b4ed87fca02dfcee4cbcd36621fffb9920a3f320cfeac771507748a151cf33
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "120032120"
---
# <a name="obtaining-additional-process-information"></a>Abrufen zusätzlicher Prozessinformationen

Es gibt eine Vielzahl von Funktionen zum Abrufen von Informationen zu Prozessen. Einige dieser Funktionen können nur für den aufrufenden Prozess verwendet werden, da sie kein Prozesshand handle als Parameter verwenden. Sie können Funktionen verwenden, die ein Prozesshand handle verwenden, um Informationen zu anderen Prozessen zu erhalten.

-   Verwenden Sie die [**GetCommandLine-Funktion,**](/windows/win32/api/processenv/nf-processenv-getcommandlinea) um die Befehlszeilenzeichenfolge für den aktuellen Prozess zu erhalten.
-   Verwenden Sie die [**GetStartupInfo-Funktion,**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-getstartupinfow) um die [**STARTUPINFO-Struktur**](/windows/win32/api/processthreadsapi/ns-processthreadsapi-startupinfoa) abzurufen, die beim Erstellen des aktuellen Prozesses angegeben wurde.
-   Um die Versionsinformationen aus dem ausführbaren Header zu erhalten, verwenden Sie die [**GetProcessVersion-Funktion.**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-getprocessversion)
-   Verwenden Sie die [**GetModuleFileName-Funktion,**](/windows/win32/api/libloaderapi/nf-libloaderapi-getmodulefilenamea) um den vollständigen Pfad und Dateinamen für die ausführbare Datei mit dem Prozesscode zu erhalten.
-   Verwenden Sie die [**GetGuiResources-Funktion,**](/windows/desktop/api/Winuser/nf-winuser-getguiresources) um die Anzahl der Handles für die objekte der grafischen Benutzeroberfläche (GUI) zu erhalten.
-   Um zu bestimmen, ob ein Prozess gedebuggt wird, verwenden Sie die [**IsDebuggerPresent-Funktion.**](/windows/win32/api/debugapi/nf-debugapi-isdebuggerpresent)
-   Verwenden Sie die GetProcessIoCounters-Funktion, um Buchhaltungsinformationen für alle vom Prozess ausgeführten [**E/A-Vorgänge**](/windows/desktop/api/WinBase/nf-winbase-getprocessiocounters) abzurufen.

 

 
