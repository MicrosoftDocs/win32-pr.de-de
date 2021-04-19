---
description: Wenn Sie einen Prozess mit der Funktion "-Funktion" erstellen, können Sie angeben, dass der Prozess Handles für Mutex, Ereignis, Semaphore oder Zeit Geber Objekte mithilfe der Struktur der Sicherheits Attribute erbt \_ .
ms.assetid: 36491a5c-7599-4f69-ab76-d3a62261a151
title: Objektvererbung
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6087ae3699e7628ab97871ede41cc2e406e40157
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106349522"
---
# <a name="object-inheritance"></a><span data-ttu-id="7e7a1-103">Objektvererbung</span><span class="sxs-lookup"><span data-stu-id="7e7a1-103">Object Inheritance</span></span>

<span data-ttu-id="7e7a1-104">Wenn Sie einen Prozess mit [**der Funktion "**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-createprocessa) -Funktion" erstellen, können Sie angeben, dass der Prozess Handles für Mutex, Ereignis, Semaphore oder Zeit Geber Objekte mithilfe der Struktur der [**Sicherheits \_ Attribute**](/previous-versions/windows/desktop/legacy/aa379560(v=vs.85)) erbt.</span><span class="sxs-lookup"><span data-stu-id="7e7a1-104">When you create a process with the [**CreateProcess**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-createprocessa) function, you can specify that the process inherit handles to mutex, event, semaphore, or timer objects using the [**SECURITY\_ATTRIBUTES**](/previous-versions/windows/desktop/legacy/aa379560(v=vs.85)) structure.</span></span> <span data-ttu-id="7e7a1-105">Das vom Prozess geerbte handle hat denselben Zugriff auf das Objekt wie das ursprüngliche handle.</span><span class="sxs-lookup"><span data-stu-id="7e7a1-105">The handle inherited by the process has the same access to the object as the original handle.</span></span> <span data-ttu-id="7e7a1-106">Der geerbte Handle wird in der Handle-Tabelle des erstellten Prozesses angezeigt, aber Sie müssen den Handle-Wert an den erstellten Prozess übermitteln.</span><span class="sxs-lookup"><span data-stu-id="7e7a1-106">The inherited handle appears in the handle table of the created process, but you must communicate the handle value to the created process.</span></span> <span data-ttu-id="7e7a1-107">Dies können Sie erreichen, indem Sie den Wert als Befehlszeilenargument angeben, wenn Sie "up **Process Process**" aufrufen.</span><span class="sxs-lookup"><span data-stu-id="7e7a1-107">You can do this by specifying the value as a command-line argument when you call **CreateProcess**.</span></span> <span data-ttu-id="7e7a1-108">Der erstellte Prozess verwendet dann die [**GetCommandLine**](/windows/win32/api/processenv/nf-processenv-getcommandlinea) -Funktion, um die Befehlszeilen Zeichenfolge abzurufen, und konvertiert das Handle-Argument in ein verwendbares handle.</span><span class="sxs-lookup"><span data-stu-id="7e7a1-108">The created process then uses the [**GetCommandLine**](/windows/win32/api/processenv/nf-processenv-getcommandlinea) function to retrieve the command-line string and convert the handle argument into a usable handle.</span></span> <span data-ttu-id="7e7a1-109">Weitere Informationen finden Sie unter [Vererbung](../procthread/inheritance.md).</span><span class="sxs-lookup"><span data-stu-id="7e7a1-109">For more information, see [Inheritance](../procthread/inheritance.md).</span></span>

 

 
