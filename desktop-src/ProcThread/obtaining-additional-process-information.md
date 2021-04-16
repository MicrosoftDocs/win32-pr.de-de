---
description: Es gibt eine Vielzahl von Funktionen zum Abrufen von Informationen zu Prozessen.
ms.assetid: f9ec6aa5-15ad-47e6-b5f8-8ac4daaf178f
title: Abrufen zusätzlicher Prozessinformationen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b90f7c68a89e2989c33c5f57a4e4fb5cead86a74
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104529090"
---
# <a name="obtaining-additional-process-information"></a>Abrufen zusätzlicher Prozessinformationen

Es gibt eine Vielzahl von Funktionen zum Abrufen von Informationen zu Prozessen. Einige dieser Funktionen können nur für den aufrufenden Prozess verwendet werden, da Sie kein Prozess handle als Parameter akzeptieren. Sie können Funktionen verwenden, die ein Prozess handle zum Abrufen von Informationen über andere Prozesse verwenden.

-   Verwenden Sie die [**GetCommandLine**](/windows/win32/api/processenv/nf-processenv-getcommandlinea) -Funktion, um die Befehlszeilen Zeichenfolge für den aktuellen Prozess zu erhalten.
-   Zum Abrufen der [**STARTUPINFO**](/windows/win32/api/processthreadsapi/ns-processthreadsapi-startupinfoa) -Struktur, die beim Erstellen des aktuellen Prozesses angegeben wurde, verwenden Sie die [**getstartupinfo**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-getstartupinfow) -Funktion.
-   Um die Versionsinformationen aus dem ausführbaren Header zu erhalten, verwenden Sie die [**getprocessversion**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-getprocessversion) -Funktion.
-   Zum Abrufen des vollständigen Pfads und des Datei namens für die ausführbare Datei, die den Prozess Code enthält, verwenden Sie die [**GetModuleFileName**](/windows/win32/api/libloaderapi/nf-libloaderapi-getmodulefilenamea) -Funktion.
-   Verwenden Sie die [**getguiresources**](/windows/desktop/api/Winuser/nf-winuser-getguiresources) -Funktion, um die Anzahl von Handles für grafische Benutzeroberflächen Objekte (GUI) zu erhalten.
-   Verwenden Sie die [**isdebuggerpresent**](/windows/win32/api/debugapi/nf-debugapi-isdebuggerpresent) -Funktion, um zu bestimmen, ob ein Prozess gedebuggt wird.
-   Zum Abrufen von Buchhaltungsinformationen für alle e/a-Vorgänge, die vom Prozess ausgeführt werden, verwenden Sie die Funktion [**getprocessiocounters**](/windows/desktop/api/WinBase/nf-winbase-getprocessiocounters) .

 

 
