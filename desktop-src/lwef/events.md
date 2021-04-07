---
title: Iagentnotifysink
description: Iagentnotifysink
ms.assetid: vs|msagent|~\paface_2xet.htm
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: cb2ccfd4acf4a64c229379aeea5847fbe044b7d5
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/19/2020
ms.locfileid: "104038912"
---
# <a name="iagentnotifysink"></a><span data-ttu-id="fb29b-103">Iagentnotifysink</span><span class="sxs-lookup"><span data-stu-id="fb29b-103">IAgentNotifySink</span></span>

<span data-ttu-id="fb29b-104">\[Der Microsoft-Agent ist ab Windows 7 veraltet und in nachfolgenden Versionen von Windows möglicherweise nicht verfügbar.\]</span><span class="sxs-lookup"><span data-stu-id="fb29b-104">\[Microsoft Agent is deprecated as of Windows 7, and may be unavailable in subsequent versions of Windows.\]</span></span>

<span data-ttu-id="fb29b-105">Iagentnotifysink benachrichtigt Clients, wenn bestimmte Zustandsänderungen auftreten.</span><span class="sxs-lookup"><span data-stu-id="fb29b-105">IAgentNotifySink notifies clients when certain state changes occur.</span></span> <span data-ttu-id="fb29b-106">Diese Funktionen sind auch über [iagentnotifysinkex](iagentnotifysinkex.md)verfügbar.</span><span class="sxs-lookup"><span data-stu-id="fb29b-106">These functions are also available from [IAgentNotifySinkEx](iagentnotifysinkex.md).</span></span>

<span data-ttu-id="fb29b-107">**Methoden in Vtable-Reihenfolge**</span><span class="sxs-lookup"><span data-stu-id="fb29b-107">**Methods in Vtable Order**</span></span>



| <span data-ttu-id="fb29b-108">Iagentnotifysink</span><span class="sxs-lookup"><span data-stu-id="fb29b-108">IAgentNotifySink</span></span>                                                      | <span data-ttu-id="fb29b-109">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="fb29b-109">Description</span></span>                                                                              |
|-----------------------------------------------------------------------|------------------------------------------------------------------------------------------|
| [<span data-ttu-id="fb29b-110">**S**</span><span class="sxs-lookup"><span data-stu-id="fb29b-110">**Command**</span></span>](command-method.md)                                     | <span data-ttu-id="fb29b-111">Tritt auf, wenn der Server einen Client definierten Befehl verarbeitet.</span><span class="sxs-lookup"><span data-stu-id="fb29b-111">Occurs when the server processes a client-defined command.</span></span>                               |
| [<span data-ttu-id="fb29b-112">**Activatinput State**</span><span class="sxs-lookup"><span data-stu-id="fb29b-112">**ActivateInputState**</span></span>](iagentnotifysink--activateinputstate.md)    | <span data-ttu-id="fb29b-113">Tritt auf, wenn ein Zeichen als Eingabe aktiv wird oder beendet wird.</span><span class="sxs-lookup"><span data-stu-id="fb29b-113">Occurs when a character becomes or ceases to be input-active.</span></span>                            |
| [<span data-ttu-id="fb29b-114">**Balloonvisiblestate**</span><span class="sxs-lookup"><span data-stu-id="fb29b-114">**BalloonVisibleState**</span></span>](iagentnotifysink---balloonvisiblestate.md) | <span data-ttu-id="fb29b-115">Tritt ein, wenn der **sichtbare** Zustand des Zeichens geändert wird.</span><span class="sxs-lookup"><span data-stu-id="fb29b-115">Occurs when the character's **Visible** state changes.</span></span>                                   |
| [<span data-ttu-id="fb29b-116">**Click-Ereignis**</span><span class="sxs-lookup"><span data-stu-id="fb29b-116">**Click Event**</span></span>](click-event.md)                                    | <span data-ttu-id="fb29b-117">Tritt auf, wenn auf ein Zeichen geklickt wird.</span><span class="sxs-lookup"><span data-stu-id="fb29b-117">Occurs when a character is clicked.</span></span>                                                      |
| [<span data-ttu-id="fb29b-118">**DblClick-Ereignis**</span><span class="sxs-lookup"><span data-stu-id="fb29b-118">**DblClick Event**</span></span>](dblclick-event.md)                              | <span data-ttu-id="fb29b-119">Tritt auf, wenn auf ein Zeichen Doppel geklickt wird.</span><span class="sxs-lookup"><span data-stu-id="fb29b-119">Occurs when a character is double-clicked.</span></span>                                               |
| [<span data-ttu-id="fb29b-120">**DragStart**</span><span class="sxs-lookup"><span data-stu-id="fb29b-120">**DragStart**</span></span>](/windows/desktop/lwef/dragstart-event)                                | <span data-ttu-id="fb29b-121">Tritt auf, wenn ein Benutzer mit dem Ziehen eines Zeichens beginnt.</span><span class="sxs-lookup"><span data-stu-id="fb29b-121">Occurs when a user starts dragging a character.</span></span>                                          |
| [<span data-ttu-id="fb29b-122">**Dragcomplete**</span><span class="sxs-lookup"><span data-stu-id="fb29b-122">**DragComplete**</span></span>](https://www.bing.com/search?q=**DragComplete**)                          | <span data-ttu-id="fb29b-123">Tritt auf, wenn ein Benutzer das Ziehen eines Zeichens beendet.</span><span class="sxs-lookup"><span data-stu-id="fb29b-123">Occurs when a user stops dragging a character.</span></span>                                           |
| [<span data-ttu-id="fb29b-124">**RequestStart**</span><span class="sxs-lookup"><span data-stu-id="fb29b-124">**RequestStart**</span></span>](iagentnotifysink--requeststart.md)                | <span data-ttu-id="fb29b-125">Tritt auf, wenn der Server mit der Verarbeitung eines [**Anforderungs**](/windows/desktop/lwef/the-request-object) Objekts beginnt.</span><span class="sxs-lookup"><span data-stu-id="fb29b-125">Occurs when the server begins processing a [**Request**](/windows/desktop/lwef/the-request-object) object.</span></span>    |
| [<span data-ttu-id="fb29b-126">**Requestcomplete**</span><span class="sxs-lookup"><span data-stu-id="fb29b-126">**RequestComplete**</span></span>](iagentnotifysink--requestcomplete.md)          | <span data-ttu-id="fb29b-127">Tritt auf, wenn der Server die Verarbeitung eines [**Anforderungs**](/windows/desktop/lwef/the-request-object) Objekts abschließt.</span><span class="sxs-lookup"><span data-stu-id="fb29b-127">Occurs when the server completes processing a [**Request**](/windows/desktop/lwef/the-request-object) object.</span></span> |
| [<span data-ttu-id="fb29b-128">**Lesezeichen**</span><span class="sxs-lookup"><span data-stu-id="fb29b-128">**Bookmark**</span></span>](iagentnotifysink--bookmark.md)                        | <span data-ttu-id="fb29b-129">Tritt auf, wenn der Server ein Lesezeichen verarbeitet.</span><span class="sxs-lookup"><span data-stu-id="fb29b-129">Occurs when the server processes a bookmark.</span></span>                                             |
| [<span data-ttu-id="fb29b-130">**Idle**</span><span class="sxs-lookup"><span data-stu-id="fb29b-130">**Idle**</span></span>](iagentnotifysink--idle.md)                                | <span data-ttu-id="fb29b-131">Tritt auf, wenn der Server die Leerlauf Verarbeitung startet oder beendet.</span><span class="sxs-lookup"><span data-stu-id="fb29b-131">Occurs when the server starts or ends idle processing.</span></span>                                   |
| [<span data-ttu-id="fb29b-132">**Move**</span><span class="sxs-lookup"><span data-stu-id="fb29b-132">**Move**</span></span>](iagentnotifysink--move.md)                                | <span data-ttu-id="fb29b-133">Tritt auf, wenn ein Zeichen verschoben wurde.</span><span class="sxs-lookup"><span data-stu-id="fb29b-133">Occurs when a character has been moved.</span></span>                                                  |
| [<span data-ttu-id="fb29b-134">**Größe**</span><span class="sxs-lookup"><span data-stu-id="fb29b-134">**Size**</span></span>](iagentnotifysink---size.md)                               | <span data-ttu-id="fb29b-135">Tritt auf, wenn die Größe eines Zeichens geändert wurde.</span><span class="sxs-lookup"><span data-stu-id="fb29b-135">Occurs when a character has been resized.</span></span>                                                |
| [<span data-ttu-id="fb29b-136">**Balloonvisiblestate**</span><span class="sxs-lookup"><span data-stu-id="fb29b-136">**BalloonVisibleState**</span></span>](iagentnotifysink---balloonvisiblestate.md) | <span data-ttu-id="fb29b-137">Tritt auf, wenn sich der Sichtbarkeits Zustand der Word-Sprechblase eines Zeichens ändert.</span><span class="sxs-lookup"><span data-stu-id="fb29b-137">Occurs when the visibility state of a character's word balloon changes.</span></span>                  |



 

<span data-ttu-id="fb29b-138">Die iagentnotifysink:: Restart-und iagentnotifysink:: Shutdown-Ereignisse, die in früheren Versionen des Microsoft-Agents unterstützt wurden, sind mittlerweile veraltet.</span><span class="sxs-lookup"><span data-stu-id="fb29b-138">The IAgentNotifySink::Restart and IAgentNotifySink::Shutdown events, supported in earlier versions of Microsoft Agent, are now obsolete.</span></span> <span data-ttu-id="fb29b-139">Der Server sendet diese Ereignisse nicht mehr, obwohl er aus Gründen der Abwärtskompatibilität unterstützt wird.</span><span class="sxs-lookup"><span data-stu-id="fb29b-139">While supported for backward compatibility, the server no longer sends these events.</span></span>

 

 