---
description: Die dynamische Verknüpfung bietet im Vergleich zur statischen Verknüpfung die folgenden Vorteile.
ms.assetid: adfd941d-1a36-4dd8-af1f-b105466e0668
title: Vorteile dynamischer Verknüpfungen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1764e25a051522600bd6b485b75f414f8a280e0b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106349469"
---
# <a name="advantages-of-dynamic-linking"></a><span data-ttu-id="af7c9-103">Vorteile dynamischer Verknüpfungen</span><span class="sxs-lookup"><span data-stu-id="af7c9-103">Advantages of Dynamic Linking</span></span>

<span data-ttu-id="af7c9-104">Die dynamische Verknüpfung bietet im Vergleich zur statischen Verknüpfung folgende Vorteile:</span><span class="sxs-lookup"><span data-stu-id="af7c9-104">Dynamic linking has the following advantages over static linking:</span></span>

-   <span data-ttu-id="af7c9-105">Bei mehreren Prozessen, die dieselbe DLL in derselben Basisadresse laden, wird eine einzelne Kopie der dll im physischen Speicher gemeinsam genutzt.</span><span class="sxs-lookup"><span data-stu-id="af7c9-105">Multiple processes that load the same DLL at the same base address share a single copy of the DLL in physical memory.</span></span> <span data-ttu-id="af7c9-106">Dadurch wird der System Arbeitsspeicher gespart und der Austausch reduziert.</span><span class="sxs-lookup"><span data-stu-id="af7c9-106">Doing this saves system memory and reduces swapping.</span></span>
-   <span data-ttu-id="af7c9-107">Wenn sich die Funktionen in einer DLL ändern, müssen die Anwendungen, die Sie verwenden, nicht neu kompiliert oder erneut verknüpft werden, solange sich die Funktionsargumente, die Aufruf Konventionen und die Rückgabewerte nicht ändern.</span><span class="sxs-lookup"><span data-stu-id="af7c9-107">When the functions in a DLL change, the applications that use them do not need to be recompiled or relinked as long as the function arguments, calling conventions, and return values do not change.</span></span> <span data-ttu-id="af7c9-108">Im Gegensatz dazu erfordert ein statisch verknüpfter Objektcode, dass die Anwendung neu verknüpft wird, wenn sich die Funktionen ändern.</span><span class="sxs-lookup"><span data-stu-id="af7c9-108">In contrast, statically linked object code requires that the application be relinked when the functions change.</span></span>
-   <span data-ttu-id="af7c9-109">Eine DLL kann nach Marktunterstützung bereitstellen.</span><span class="sxs-lookup"><span data-stu-id="af7c9-109">A DLL can provide after-market support.</span></span> <span data-ttu-id="af7c9-110">So kann z. b. eine Anzeigetreiber-DLL geändert werden, um eine Anzeige zu unterstützen, die beim ersten Versand der Anwendung nicht verfügbar war.</span><span class="sxs-lookup"><span data-stu-id="af7c9-110">For example, a display driver DLL can be modified to support a display that was not available when the application was initially shipped.</span></span>
-   <span data-ttu-id="af7c9-111">Programme, die in verschiedenen Programmiersprachen geschrieben wurden, können dieselbe DLL-Funktion aufrufen, solange die Programme derselben Aufruf Konvention folgen, die von der Funktion verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="af7c9-111">Programs written in different programming languages can call the same DLL function as long as the programs follow the same calling convention that the function uses.</span></span> <span data-ttu-id="af7c9-112">Die Aufruf Konvention (z. b. C, Pascal oder Standard Aufruf) steuert die Reihenfolge, in der die aufrufende Funktion die Argumente auf den Stapel übertragen muss, unabhängig davon, ob die Funktion oder die aufrufende Funktion für das Bereinigen des Stapels zuständig ist und ob Argumente in Registern übermittelt werden.</span><span class="sxs-lookup"><span data-stu-id="af7c9-112">The calling convention (such as C, Pascal, or standard call) controls the order in which the calling function must push the arguments onto the stack, whether the function or the calling function is responsible for cleaning up the stack, and whether any arguments are passed in registers.</span></span> <span data-ttu-id="af7c9-113">Weitere Informationen finden Sie in der Dokumentation, die in Ihrem Compiler enthalten ist.</span><span class="sxs-lookup"><span data-stu-id="af7c9-113">For more information, see the documentation included with your compiler.</span></span>

<span data-ttu-id="af7c9-114">Ein möglicher Nachteil bei der Verwendung von DLLs liegt darin, dass die Anwendung nicht unabhängig ausgeführt werden kann; sie hängt von der Existenz eines separaten DLL-Moduls ab.</span><span class="sxs-lookup"><span data-stu-id="af7c9-114">A potential disadvantage to using DLLs is that the application is not self-contained; it depends on the existence of a separate DLL module.</span></span> <span data-ttu-id="af7c9-115">Das System beendet Prozesse mithilfe dynamischer Ladezeit-Verknüpfungen, wenn Sie eine DLL benötigen, die beim Prozessstart nicht gefunden wurde, und eine Fehlermeldung an den Benutzer übergibt.</span><span class="sxs-lookup"><span data-stu-id="af7c9-115">The system terminates processes using load-time dynamic linking if they require a DLL that is not found at process startup and gives an error message to the user.</span></span> <span data-ttu-id="af7c9-116">Das System beendet einen Prozess nicht mithilfe der dynamischen Lauf Zeit Verknüpfung in dieser Situation, aber Funktionen, die von der fehlenden dll exportiert werden, sind für das Programm nicht verfügbar.</span><span class="sxs-lookup"><span data-stu-id="af7c9-116">The system does not terminate a process using run-time dynamic linking in this situation, but functions exported by the missing DLL are not available to the program.</span></span>

 

 



