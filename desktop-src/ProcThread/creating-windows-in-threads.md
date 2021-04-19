---
description: Jeder Thread kann ein Fenster erstellen.
ms.assetid: 27f04f9f-52d9-46d6-8e06-9b032682b7c7
title: Erstellen von Fenstern in Threads
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: aebcde45ca37696b6dbc90e639f630a689498b04
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106367936"
---
# <a name="creating-windows-in-threads"></a><span data-ttu-id="9b273-103">Erstellen von Fenstern in Threads</span><span class="sxs-lookup"><span data-stu-id="9b273-103">Creating Windows in Threads</span></span>

<span data-ttu-id="9b273-104">Jeder Thread kann ein Fenster erstellen.</span><span class="sxs-lookup"><span data-stu-id="9b273-104">Any thread can create a window.</span></span> <span data-ttu-id="9b273-105">Der Thread, der das Fenster erstellt, besitzt das Fenster und die zugehörige Meldungs Warteschlange.</span><span class="sxs-lookup"><span data-stu-id="9b273-105">The thread that creates the window owns the window and its associated message queue.</span></span> <span data-ttu-id="9b273-106">Daher muss der Thread eine Nachrichten Schleife bereitstellen, um die Nachrichten in der Nachrichten Warteschlange zu verarbeiten.</span><span class="sxs-lookup"><span data-stu-id="9b273-106">Therefore, the thread must provide a message loop to process the messages in its message queue.</span></span> <span data-ttu-id="9b273-107">Außerdem müssen Sie in diesem Thread [**MsgWaitForMultipleObjects**](/windows/desktop/api/winuser/nf-winuser-msgwaitformultipleobjects) oder [**MsgWaitForMultipleObjectsEx**](/windows/desktop/api/winuser/nf-winuser-msgwaitformultipleobjectsex) verwenden, damit Nachrichten [verarbeitet werden können](/windows/desktop/Sync/wait-functions).</span><span class="sxs-lookup"><span data-stu-id="9b273-107">In addition, you must use [**MsgWaitForMultipleObjects**](/windows/desktop/api/winuser/nf-winuser-msgwaitformultipleobjects) or [**MsgWaitForMultipleObjectsEx**](/windows/desktop/api/winuser/nf-winuser-msgwaitformultipleobjectsex) in that thread, rather than the other [wait functions](/windows/desktop/Sync/wait-functions), so that it can process messages.</span></span> <span data-ttu-id="9b273-108">Andernfalls kann das System blockiert werden, wenn dem Thread beim warten eine Nachricht gesendet wird.</span><span class="sxs-lookup"><span data-stu-id="9b273-108">Otherwise, the system can become deadlocked when the thread is sent a message while it is waiting.</span></span>

<span data-ttu-id="9b273-109">Die [**attachthreadinput**](/windows/desktop/api/Winuser/nf-winuser-attachthreadinput) -Funktion kann verwendet werden, um zuzulassen, dass eine Gruppe von Threads denselben Eingabe Zustand verwendet.</span><span class="sxs-lookup"><span data-stu-id="9b273-109">The [**AttachThreadInput**](/windows/desktop/api/Winuser/nf-winuser-attachthreadinput) function can be used to allow a set of threads to share the same input state.</span></span> <span data-ttu-id="9b273-110">Durch die Freigabe des Eingabe Zustands teilen die Threads ihr Konzept des aktiven Fensters.</span><span class="sxs-lookup"><span data-stu-id="9b273-110">By sharing input state, the threads share their concept of the active window.</span></span> <span data-ttu-id="9b273-111">Auf diese Weise kann ein Thread immer das Fenster eines anderen Threads aktivieren.</span><span class="sxs-lookup"><span data-stu-id="9b273-111">By doing this, one thread can always activate another thread's window.</span></span> <span data-ttu-id="9b273-112">Diese Funktion eignet sich auch zum Freigeben des Fokus Zustands, des Maus Erfassungs Zustands, des Tastatur Zustands und des Fenster-Z-Reihen folgen Zustands zwischen Fenstern, die von verschiedenen Threads erstellt wurden, deren Eingabe Zustand freigegeben ist.</span><span class="sxs-lookup"><span data-stu-id="9b273-112">This function is also useful for sharing focus state, mouse capture state, keyboard state, and window Z-order state among windows created by different threads whose input state is shared.</span></span>

<span data-ttu-id="9b273-113">Weitere Informationen zum Erstellen von Windows finden Sie unter [Windows-Klassen](../winmsg/window-classes.md).</span><span class="sxs-lookup"><span data-stu-id="9b273-113">For information about creating windows, see [Windows Classes](../winmsg/window-classes.md).</span></span>

 

 
