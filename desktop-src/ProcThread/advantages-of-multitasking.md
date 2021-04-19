---
description: Der Vorteil von Multitasking besteht darin, dass mehrere Anwendungen gleichzeitig geöffnet und funktionieren können. Ein Benutzer kann z. b. eine Datei mit einer Anwendung bearbeiten, während eine andere Anwendung eine Kalkulations Tabelle neu berechnet.
ms.assetid: 163291ce-78bd-43ee-98ca-564ce91c520c
title: Vorteile von Multitasking
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 119e327ba07a226a8422c61a100d6ff000b48ed9
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106368744"
---
# <a name="advantages-of-multitasking"></a><span data-ttu-id="0bbd6-104">Vorteile von Multitasking</span><span class="sxs-lookup"><span data-stu-id="0bbd6-104">Advantages of Multitasking</span></span>

<span data-ttu-id="0bbd6-105">Der Vorteil von Multitasking besteht darin, dass mehrere Anwendungen gleichzeitig geöffnet und funktionieren können.</span><span class="sxs-lookup"><span data-stu-id="0bbd6-105">To the user, the advantage of multitasking is the ability to have several applications open and working at the same time.</span></span> <span data-ttu-id="0bbd6-106">Ein Benutzer kann z. b. eine Datei mit einer Anwendung bearbeiten, während eine andere Anwendung eine Kalkulations Tabelle neu berechnet.</span><span class="sxs-lookup"><span data-stu-id="0bbd6-106">For example, a user can edit a file with one application while another application is recalculating a spreadsheet.</span></span>

<span data-ttu-id="0bbd6-107">Der Vorteil von Multitasking besteht im Anwendungsentwickler in der Möglichkeit, Anwendungen zu erstellen, die mehr als einen Prozess verwenden, und Prozesse zu erstellen, die mehr als einen Ausführungs Thread verwenden.</span><span class="sxs-lookup"><span data-stu-id="0bbd6-107">To the application developer, the advantage of multitasking is the ability to create applications that use more than one process and to create processes that use more than one thread of execution.</span></span> <span data-ttu-id="0bbd6-108">Ein Prozess kann z. b. über einen Benutzeroberflächen Thread verfügen, der Interaktionen mit dem Benutzer verwaltet (Tastatur-und Maus Eingaben), und Arbeitsthreads, die andere Aufgaben ausführen, während der Benutzeroberflächen Thread auf Benutzereingaben wartet.</span><span class="sxs-lookup"><span data-stu-id="0bbd6-108">For example, a process can have a user interface thread that manages interactions with the user (keyboard and mouse input), and worker threads that perform other tasks while the user interface thread waits for user input.</span></span> <span data-ttu-id="0bbd6-109">Wenn Sie dem Benutzeroberflächen Thread eine höhere Priorität geben, reagiert die Anwendung besser auf den Benutzer, während die Arbeitsthreads den Prozessor während der Zeiten, in denen keine Benutzereingaben vorhanden sind, effizient nutzen.</span><span class="sxs-lookup"><span data-stu-id="0bbd6-109">If you give the user interface thread a higher priority, the application will be more responsive to the user, while the worker threads use the processor efficiently during the times when there is no user input.</span></span>

 

 



