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
# <a name="obtaining-additional-process-information"></a><span data-ttu-id="49822-103">Abrufen zusätzlicher Prozessinformationen</span><span class="sxs-lookup"><span data-stu-id="49822-103">Obtaining Additional Process Information</span></span>

<span data-ttu-id="49822-104">Es gibt eine Vielzahl von Funktionen zum Abrufen von Informationen zu Prozessen.</span><span class="sxs-lookup"><span data-stu-id="49822-104">There are a variety of functions for obtaining information about processes.</span></span> <span data-ttu-id="49822-105">Einige dieser Funktionen können nur für den aufrufenden Prozess verwendet werden, da Sie kein Prozess handle als Parameter akzeptieren.</span><span class="sxs-lookup"><span data-stu-id="49822-105">Some of these functions can be used only for the calling process, because they do not take a process handle as a parameter.</span></span> <span data-ttu-id="49822-106">Sie können Funktionen verwenden, die ein Prozess handle zum Abrufen von Informationen über andere Prozesse verwenden.</span><span class="sxs-lookup"><span data-stu-id="49822-106">You can use functions that take a process handle to obtain information about other processes.</span></span>

-   <span data-ttu-id="49822-107">Verwenden Sie die [**GetCommandLine**](/windows/win32/api/processenv/nf-processenv-getcommandlinea) -Funktion, um die Befehlszeilen Zeichenfolge für den aktuellen Prozess zu erhalten.</span><span class="sxs-lookup"><span data-stu-id="49822-107">To obtain the command-line string for the current process, use the [**GetCommandLine**](/windows/win32/api/processenv/nf-processenv-getcommandlinea) function.</span></span>
-   <span data-ttu-id="49822-108">Zum Abrufen der [**STARTUPINFO**](/windows/win32/api/processthreadsapi/ns-processthreadsapi-startupinfoa) -Struktur, die beim Erstellen des aktuellen Prozesses angegeben wurde, verwenden Sie die [**getstartupinfo**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-getstartupinfow) -Funktion.</span><span class="sxs-lookup"><span data-stu-id="49822-108">To retrieve the [**STARTUPINFO**](/windows/win32/api/processthreadsapi/ns-processthreadsapi-startupinfoa) structure specified when the current process was created, use the [**GetStartupInfo**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-getstartupinfow) function.</span></span>
-   <span data-ttu-id="49822-109">Um die Versionsinformationen aus dem ausführbaren Header zu erhalten, verwenden Sie die [**getprocessversion**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-getprocessversion) -Funktion.</span><span class="sxs-lookup"><span data-stu-id="49822-109">To obtain the version information from the executable header, use the [**GetProcessVersion**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-getprocessversion) function.</span></span>
-   <span data-ttu-id="49822-110">Zum Abrufen des vollständigen Pfads und des Datei namens für die ausführbare Datei, die den Prozess Code enthält, verwenden Sie die [**GetModuleFileName**](/windows/win32/api/libloaderapi/nf-libloaderapi-getmodulefilenamea) -Funktion.</span><span class="sxs-lookup"><span data-stu-id="49822-110">To obtain the full path and file name for the executable file containing the process code, use the [**GetModuleFileName**](/windows/win32/api/libloaderapi/nf-libloaderapi-getmodulefilenamea) function.</span></span>
-   <span data-ttu-id="49822-111">Verwenden Sie die [**getguiresources**](/windows/desktop/api/Winuser/nf-winuser-getguiresources) -Funktion, um die Anzahl von Handles für grafische Benutzeroberflächen Objekte (GUI) zu erhalten.</span><span class="sxs-lookup"><span data-stu-id="49822-111">To obtain the count of handles to graphical user interface (GUI) objects in use, use the [**GetGuiResources**](/windows/desktop/api/Winuser/nf-winuser-getguiresources) function.</span></span>
-   <span data-ttu-id="49822-112">Verwenden Sie die [**isdebuggerpresent**](/windows/win32/api/debugapi/nf-debugapi-isdebuggerpresent) -Funktion, um zu bestimmen, ob ein Prozess gedebuggt wird.</span><span class="sxs-lookup"><span data-stu-id="49822-112">To determine whether a process is being debugged, use the [**IsDebuggerPresent**](/windows/win32/api/debugapi/nf-debugapi-isdebuggerpresent) function.</span></span>
-   <span data-ttu-id="49822-113">Zum Abrufen von Buchhaltungsinformationen für alle e/a-Vorgänge, die vom Prozess ausgeführt werden, verwenden Sie die Funktion [**getprocessiocounters**](/windows/desktop/api/WinBase/nf-winbase-getprocessiocounters) .</span><span class="sxs-lookup"><span data-stu-id="49822-113">To retrieve accounting information for all I/O operations performed by the process, use the [**GetProcessIoCounters**](/windows/desktop/api/WinBase/nf-winbase-getprocessiocounters) function.</span></span>

 

 
