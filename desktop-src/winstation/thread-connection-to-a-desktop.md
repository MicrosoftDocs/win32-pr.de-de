---
title: Thread Verbindung mit einem Desktop
description: Nachdem ein Prozess eine Verbindung mit einer Fenster Station hergestellt hat, weist das System dem Thread, der die Verbindung herstellt, einen Desktop zu.
ms.assetid: 45016619-ed11-4b0c-84e3-f8662553c64d
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a503390468ea5ed1771ece7a942a2d615ac6f0a9
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "104209250"
---
# <a name="thread-connection-to-a-desktop"></a><span data-ttu-id="97f27-103">Thread Verbindung mit einem Desktop</span><span class="sxs-lookup"><span data-stu-id="97f27-103">Thread Connection to a Desktop</span></span>

<span data-ttu-id="97f27-104">Nachdem ein Prozess eine Verbindung mit einer Fenster Station hergestellt hat, weist das System dem Thread, der die Verbindung herstellt, einen Desktop zu.</span><span class="sxs-lookup"><span data-stu-id="97f27-104">After a process connects to a window station, the system assigns a desktop to the thread making the connection.</span></span> <span data-ttu-id="97f27-105">Das System bestimmt den Desktop, der dem Thread gemäß den folgenden Regeln zugewiesen werden soll:</span><span class="sxs-lookup"><span data-stu-id="97f27-105">The system determines the desktop to assign to the thread according to the following rules:</span></span>

1.  <span data-ttu-id="97f27-106">Wenn der Thread die Funktion " [**SetThreadDesktop**](/windows/win32/api/winuser/nf-winuser-setthreaddesktop) " aufgerufen hat, stellt er eine Verbindung mit dem angegebenen Desktop her.</span><span class="sxs-lookup"><span data-stu-id="97f27-106">If the thread has called the [**SetThreadDesktop**](/windows/win32/api/winuser/nf-winuser-setthreaddesktop) function, it connects to the specified desktop.</span></span>
2.  <span data-ttu-id="97f27-107">Wenn der Thread [**SetThreadDesktop**](/windows/win32/api/winuser/nf-winuser-setthreaddesktop)nicht aufgerufen hat, stellt er eine Verbindung mit dem Desktop her, der vom übergeordneten Prozess geerbt wurde.</span><span class="sxs-lookup"><span data-stu-id="97f27-107">If the thread did not call [**SetThreadDesktop**](/windows/win32/api/winuser/nf-winuser-setthreaddesktop), it connects to the desktop inherited from the parent process.</span></span>
3.  <span data-ttu-id="97f27-108">Wenn der Thread [**SetThreadDesktop**](/windows/win32/api/winuser/nf-winuser-setthreaddesktop) nicht aufgerufen hat und keinen Desktop geerbt hat, versucht das System, den maximal \_ zulässigen Zugriff zu öffnen und wie folgt eine Verbindung mit einem Desktop herzustellen:</span><span class="sxs-lookup"><span data-stu-id="97f27-108">If the thread did not call [**SetThreadDesktop**](/windows/win32/api/winuser/nf-winuser-setthreaddesktop) and did not inherit a desktop, the system attempts to open for MAXIMUM\_ALLOWED access and connect to a desktop as follows:</span></span>
    -   <span data-ttu-id="97f27-109">Wenn im **lpdesktop-** Member der [**STARTUPINFO**](/windows/desktop/api/processthreadsapi/ns-processthreadsapi-startupinfoa) -Struktur, die beim Erstellen des Prozesses verwendet wurde, ein Desktop Name angegeben wurde, stellt der Thread eine Verbindung mit dem angegebenen Desktop her.</span><span class="sxs-lookup"><span data-stu-id="97f27-109">If a desktop name was specified in the **lpDesktop** member of the [**STARTUPINFO**](/windows/desktop/api/processthreadsapi/ns-processthreadsapi-startupinfoa) structure that was used when the process was created, the thread connects to the specified desktop.</span></span>
    -   <span data-ttu-id="97f27-110">Andernfalls stellt der Thread eine Verbindung mit dem Standard Desktop der Fenster Station her, mit der der Prozess verbunden ist.</span><span class="sxs-lookup"><span data-stu-id="97f27-110">Otherwise, the thread connects to the default desktop of the window station to which the process connected.</span></span>

<span data-ttu-id="97f27-111">Der während dieses Verbindungs Vorgangs zugewiesene Desktop kann nicht durch Aufrufen der [**closedesktop-**](/windows/win32/api/winuser/nf-winuser-closedesktop) Funktion geschlossen werden.</span><span class="sxs-lookup"><span data-stu-id="97f27-111">The desktop assigned during this connection process cannot be closed by calling the [**CloseDesktop**](/windows/win32/api/winuser/nf-winuser-closedesktop) function.</span></span>

<span data-ttu-id="97f27-112">Wenn ein Prozess eine Verbindung mit einem Desktop herstellt, durchsucht das System die Handle-Tabelle des Prozesses nach geerbten Handles.</span><span class="sxs-lookup"><span data-stu-id="97f27-112">When a process is connecting to a desktop, the system searches the process's handle table for inherited handles.</span></span> <span data-ttu-id="97f27-113">Das System verwendet das erste gefundene Desktop handle.</span><span class="sxs-lookup"><span data-stu-id="97f27-113">The system uses the first desktop handle it finds.</span></span> <span data-ttu-id="97f27-114">Wenn Sie möchten, dass ein untergeordneter Prozess eine Verbindung mit einem bestimmten geerbten Desktop herstellt, müssen Sie sicherstellen, dass nur das gewünschte Handle als vererbbar gekennzeichnet ist.</span><span class="sxs-lookup"><span data-stu-id="97f27-114">If you want a child process to connect to a particular inherited desktop, you must ensure that the only the desired handle is marked inheritable.</span></span> <span data-ttu-id="97f27-115">Wenn ein untergeordneter Prozess mehrere Desktop Handles erbt, sind die Ergebnisse der Desktop Verbindung nicht definiert.</span><span class="sxs-lookup"><span data-stu-id="97f27-115">If a child process inherits multiple desktop handles, the results of the desktop connection are undefined.</span></span>

<span data-ttu-id="97f27-116">Handles für einen Desktop, den das System öffnet, während ein Prozess mit einem Desktop verbunden wird, können nicht vererbt werden.</span><span class="sxs-lookup"><span data-stu-id="97f27-116">Handles to a desktop that the system opens while connecting a process to a desktop are not inheritable.</span></span>

## <a name="related-topics"></a><span data-ttu-id="97f27-117">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="97f27-117">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="97f27-118">Verarbeiten der Verbindung mit einer Fenster Station</span><span class="sxs-lookup"><span data-stu-id="97f27-118">Process Connection to a Window Station</span></span>](process-connection-to-a-window-station.md)
</dt> </dl>

 

 