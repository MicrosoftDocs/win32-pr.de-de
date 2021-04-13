---
title: Prozessübergreifende Kommunikation
description: Die folgenden Verfahren können für die Kommunikation zwischen 32-Bit-und 64-Bit-Anwendungen verwendet werden.
ms.assetid: 9a60ccfe-4ccf-44d7-9522-42609d95217b
keywords:
- prozessübergreifende Kommunikation 64-Bit-Windows-Programmierung
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2398174f011127973dfd0b1773e6eb040cdde898
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "104390703"
---
# <a name="interprocess-communication-between-32-bit-and-64-bit-applications"></a><span data-ttu-id="7343c-104">Prozessübergreifende Kommunikation zwischen 32-Bit-und 64-Bit-Anwendungen</span><span class="sxs-lookup"><span data-stu-id="7343c-104">Interprocess Communication Between 32-bit and 64-bit Applications</span></span>

<span data-ttu-id="7343c-105">Die folgenden Verfahren können für die Kommunikation zwischen 32-Bit-und 64-Bit-Anwendungen verwendet werden:</span><span class="sxs-lookup"><span data-stu-id="7343c-105">The following techniques can be used for communication between 32-bit and 64-bit applications:</span></span>

-   <span data-ttu-id="7343c-106">64-Bit-Versionen von Windows verwenden 32-Bit-Handles für die Interoperabilität.</span><span class="sxs-lookup"><span data-stu-id="7343c-106">64-bit versions of Windows use 32-bit handles for interoperability.</span></span> <span data-ttu-id="7343c-107">Wenn ein Handle zwischen 32-Bit-und 64-Bit-Anwendungen gemeinsam genutzt wird, sind nur die niedrigeren 32 Bits signifikant, sodass es sicher ist, das Handle (bei der Übergabe von 64 Bit an 32-Bit) oder das Signieren des Handles (bei Übergabe von 32-Bit an 64-Bit) zu kürzen.</span><span class="sxs-lookup"><span data-stu-id="7343c-107">When sharing a handle between 32-bit and 64-bit applications, only the lower 32 bits are significant, so it is safe to truncate the handle (when passing it from 64-bit to 32-bit) or sign-extend the handle (when passing it from 32-bit to 64-bit).</span></span> <span data-ttu-id="7343c-108">Handles, die freigegeben werden können, sind Handles für Benutzer Objekte wie Windows (**HWND**), Handles für GDI-Objekte wie z. b. Stifte und Pinsel (**hBrush** und **HPEN**) und Handles für benannte Objekte wie Mutexen, Semaphore und Datei Handles.</span><span class="sxs-lookup"><span data-stu-id="7343c-108">Handles that can be shared include handles to user objects such as windows (**HWND**), handles to GDI objects such as pens and brushes (**HBRUSH** and **HPEN**), and handles to named objects such as mutexes, semaphores, and file handles.</span></span>
-   <span data-ttu-id="7343c-109">Remote Prozedur Aufrufe (RPC) können verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="7343c-109">Remote procedure calls (RPC) can be used.</span></span>
-   <span data-ttu-id="7343c-110">COM localservers können verwendet werden, wenn sowohl 32-Bit-als auch 64-Bit-Proxy-/Stub-DLLs für alle verwendeten Schnittstellen registriert sind.</span><span class="sxs-lookup"><span data-stu-id="7343c-110">COM LocalServers can be used if both 32-bit and 64-bit proxy/stub DLLs are registered for all interfaces used.</span></span>
-   <span data-ttu-id="7343c-111">Shared Memory kann verwendet werden, wenn Zeiger abhängige Typen ordnungsgemäß konvertiert (oder vermieden) werden.</span><span class="sxs-lookup"><span data-stu-id="7343c-111">Shared memory can be used if pointer-dependent types are converted properly (or avoided).</span></span>
-   <span data-ttu-id="7343c-112">Die Funktionen " [**deateprocess**](/windows/desktop/api/processthreadsapi/nf-processthreadsapi-createprocessa) " und " [**ShellExecute**](/windows/win32/api/shellapi/nf-shellapi-shellexecutea) " können 32-Bit-und 64-Bit-Prozesse von 32-Bit-oder 64-Bit-Prozessen mit bestimmten Einschränkungen starten.</span><span class="sxs-lookup"><span data-stu-id="7343c-112">The [**CreateProcess**](/windows/desktop/api/processthreadsapi/nf-processthreadsapi-createprocessa) and [**ShellExecute**](/windows/win32/api/shellapi/nf-shellapi-shellexecutea) functions can launch 32-bit and 64-bit processes from either 32-bit or 64-bit processes with certain limitations.</span></span>

<span data-ttu-id="7343c-113">Eine ausführbare 64-Bit-Datei unter% windir% \\ system32 kann nicht von einem 32-Bit-Prozess gestartet werden, da der Dateisystem-Redirector den Pfad umleitet.</span><span class="sxs-lookup"><span data-stu-id="7343c-113">A 64-bit executable file located under %windir%\\System32 cannot be launched from a 32-bit process, because the file system redirector redirects the path.</span></span> <span data-ttu-id="7343c-114">Deaktivieren Sie die Umleitung nicht, um dies zu erreichen. Verwenden Sie stattdessen% windir% \\ sysnative.</span><span class="sxs-lookup"><span data-stu-id="7343c-114">Do not disable redirection to accomplish this; use %windir%\\Sysnative instead.</span></span> <span data-ttu-id="7343c-115">Weitere Informationen finden Sie unter [File System Redirector](file-system-redirector.md).</span><span class="sxs-lookup"><span data-stu-id="7343c-115">For more information, see [File System Redirector](file-system-redirector.md).</span></span>

 

 