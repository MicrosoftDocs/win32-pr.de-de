---
description: Wenn ein Thread darauf wartet, dass ein Kernel Modus-Rückruf ausgeführt wird, verzögert sich die benutzermodusseite des Threads bei einem Aufruf der zwcallbackreturn-Funktion.
ms.assetid: 6d6d4f94-0e8c-4469-b905-731be6c4083d
title: Erkennen von Kernel-Mode Rückrufen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c899615be416b266779236ea8bc36978a517b7ed
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "103958494"
---
# <a name="detecting-kernel-mode-callbacks"></a><span data-ttu-id="6de16-103">Erkennen von Kernel-Mode Rückrufen</span><span class="sxs-lookup"><span data-stu-id="6de16-103">Detecting Kernel-Mode Callbacks</span></span>

<span data-ttu-id="6de16-104">Der größte Teil des Codes für das Windows-Betriebssystem wird im Kernel Modus ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="6de16-104">Most of the code for the Windows operating system runs in kernel mode.</span></span> <span data-ttu-id="6de16-105">Der Prozessor Modus wechselt vom Benutzermodus in den Kernel Modus, wenn ein Anwendungs Thread eine Funktion von der Windows-API aufruft, die wiederum eine interne Systemfunktion aufruft, die im Kernel Modus ausgeführt werden muss.</span><span class="sxs-lookup"><span data-stu-id="6de16-105">The processor mode switches from user mode to kernel mode whenever an application thread calls a function from the Windows API that in turn calls an internal system function that must execute in kernel mode.</span></span> <span data-ttu-id="6de16-106">Der Prozessor Modus kehrt in den Benutzermodus zurück, bevor die Steuerung an die Funktion zurückgegeben wird, sodass die Systemdaten geschützt sind.</span><span class="sxs-lookup"><span data-stu-id="6de16-106">The processor mode returns to user mode before control returns to the function so that the system data is protected.</span></span>

<span data-ttu-id="6de16-107">Wenn ein Thread darauf wartet, dass ein Kernel Modus-Rückruf ausgeführt wird, verzögert sich die benutzermodusseite des Threads bei einem Aufruf der **zwcallbackreturn** -Funktion.</span><span class="sxs-lookup"><span data-stu-id="6de16-107">If a thread is waiting for a kernel-mode callback to complete, the user-mode side of the thread will delay at a call to the **ZwCallbackReturn** function.</span></span>

 

 



