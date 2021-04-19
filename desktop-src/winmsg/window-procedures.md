---
description: In diesem Abschnitt werden Fenster Prozeduren erläutert. Jedes Fenster verfügt über eine zugeordnete Fenster Prozedur, die alle Nachrichten verarbeitet, die gesendet oder an alle Fenster der Klasse gesendet werden.
ms.assetid: vs|winui|~\winui\windowsuserinterface\windowing\windowprocedures.htm
title: Fenster Prozeduren
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 92ae68ba9b64557a6dc70d5c83788b8337648a2f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106349663"
---
# <a name="window-procedures"></a><span data-ttu-id="2bccd-104">Fenster Prozeduren</span><span class="sxs-lookup"><span data-stu-id="2bccd-104">Window Procedures</span></span>

<span data-ttu-id="2bccd-105">Jedes Fenster verfügt über eine zugeordnete Fenster Prozedur – eine Funktion, die alle Nachrichten verarbeitet, die gesendet oder an alle Fenster der Klasse gesendet werden.</span><span class="sxs-lookup"><span data-stu-id="2bccd-105">Every window has an associated window procedure — a function that processes all messages sent or posted to all windows of the class.</span></span> <span data-ttu-id="2bccd-106">Alle Aspekte der Darstellung und des Verhaltens eines Fensters hängen von der Reaktion der Fenster Prozedur auf diese Nachrichten ab.</span><span class="sxs-lookup"><span data-stu-id="2bccd-106">All aspects of a window's appearance and behavior depend on the window procedure's response to these messages.</span></span>

### <a name="in-this-section"></a><span data-ttu-id="2bccd-107">In diesem Abschnitt</span><span class="sxs-lookup"><span data-stu-id="2bccd-107">In This Section</span></span>



| <span data-ttu-id="2bccd-108">Name</span><span class="sxs-lookup"><span data-stu-id="2bccd-108">Name</span></span>                                                         | <span data-ttu-id="2bccd-109">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="2bccd-109">Description</span></span>                                                                                                                                                                                                    |
|--------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="2bccd-110">Informationen zu Fenster Verfahren</span><span class="sxs-lookup"><span data-stu-id="2bccd-110">About Window Procedures</span></span>](about-window-procedures.md)       | <span data-ttu-id="2bccd-111">Erläutert Fenster Prozeduren.</span><span class="sxs-lookup"><span data-stu-id="2bccd-111">Discusses window procedures.</span></span> <span data-ttu-id="2bccd-112">Jedes Fenster ist ein Member einer bestimmten Fenster Klasse.</span><span class="sxs-lookup"><span data-stu-id="2bccd-112">Each window is a member of a particular window class.</span></span> <span data-ttu-id="2bccd-113">Die Fenster Klasse bestimmt die Standardfenster Prozedur, die von einem einzelnen Fenster zum Verarbeiten der Nachrichten verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="2bccd-113">The window class determines the default window procedure that an individual window uses to process its messages.</span></span><br/> |
| [<span data-ttu-id="2bccd-114">Verwenden von Window</span><span class="sxs-lookup"><span data-stu-id="2bccd-114">Using Window Procedures</span></span>](using-window-procedures.md)       | <span data-ttu-id="2bccd-115">Erläutert, wie die folgenden Aufgaben ausgeführt werden, die Fenster Prozeduren zugeordnet sind.</span><span class="sxs-lookup"><span data-stu-id="2bccd-115">Covers how to perform the following tasks associated with window procedures.</span></span><br/>                                                                                                                        |
| [<span data-ttu-id="2bccd-116">Fenster Prozedur Referenz</span><span class="sxs-lookup"><span data-stu-id="2bccd-116">Window Procedure Reference</span></span>](window-procedure-reference.md) | <span data-ttu-id="2bccd-117">Enthält die API-Referenz.</span><span class="sxs-lookup"><span data-stu-id="2bccd-117">Contains the API reference.</span></span><br/>                                                                                                                                                                         |



 

### <a name="functions"></a><span data-ttu-id="2bccd-118">Functions</span><span class="sxs-lookup"><span data-stu-id="2bccd-118">Functions</span></span>



| <span data-ttu-id="2bccd-119">Name</span><span class="sxs-lookup"><span data-stu-id="2bccd-119">Name</span></span>                                     | <span data-ttu-id="2bccd-120">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="2bccd-120">Description</span></span>                                                                                                                                                                                                                                                                                                   |
|------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="2bccd-121">**Callwindowproc**</span><span class="sxs-lookup"><span data-stu-id="2bccd-121">**CallWindowProc**</span></span>](/windows/win32/api/winuser/nf-winuser-callwindowproca) | <span data-ttu-id="2bccd-122">Übergibt Nachrichten Informationen an die angegebene Fenster Prozedur.</span><span class="sxs-lookup"><span data-stu-id="2bccd-122">Passes message information to the specified window procedure.</span></span> <br/>                                                                                                                                                                                                                                     |
| [<span data-ttu-id="2bccd-123">**DefWindowProc**</span><span class="sxs-lookup"><span data-stu-id="2bccd-123">**DefWindowProc**</span></span>](/windows/desktop/api/winuser/nf-winuser-defwindowproca)   | <span data-ttu-id="2bccd-124">Ruft die Standardfenster Prozedur auf, um die Standard Verarbeitung für alle Fenster Meldungen bereitzustellen, die von einer Anwendung nicht verarbeitet werden.</span><span class="sxs-lookup"><span data-stu-id="2bccd-124">Calls the default window procedure to provide default processing for any window messages that an application does not process.</span></span> <span data-ttu-id="2bccd-125">Diese Funktion stellt sicher, dass jede Nachricht verarbeitet wird.</span><span class="sxs-lookup"><span data-stu-id="2bccd-125">This function ensures that every message is processed.</span></span> <span data-ttu-id="2bccd-126">[**Defwindowproc**](/windows/desktop/api/winuser/nf-winuser-defwindowproca) wird mit denselben Parametern aufgerufen, die von der Fenster Prozedur empfangen werden.</span><span class="sxs-lookup"><span data-stu-id="2bccd-126">[**DefWindowProc**](/windows/desktop/api/winuser/nf-winuser-defwindowproca) is called with the same parameters received by the window procedure.</span></span> <br/> |
| <span data-ttu-id="2bccd-127">[*WindowProc*](/previous-versions/windows/desktop/legacy/ms633573(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="2bccd-127">[*WindowProc*](/previous-versions/windows/desktop/legacy/ms633573(v=vs.85))</span></span>           | <span data-ttu-id="2bccd-128">Eine Anwendungs definierte Funktion, die an ein Fenster gesendete Nachrichten verarbeitet.</span><span class="sxs-lookup"><span data-stu-id="2bccd-128">An application-defined function that processes messages sent to a window.</span></span> <span data-ttu-id="2bccd-129">Der **WndProc** -Typ definiert einen Zeiger auf diese Rückruffunktion.</span><span class="sxs-lookup"><span data-stu-id="2bccd-129">The **WNDPROC** type defines a pointer to this callback function.</span></span> <span data-ttu-id="2bccd-130">[*WindowProc*](/previous-versions/windows/desktop/legacy/ms633573(v=vs.85)) ist ein Platzhalter für den Namen der Anwendungs definierten Funktion.</span><span class="sxs-lookup"><span data-stu-id="2bccd-130">[*WindowProc*](/previous-versions/windows/desktop/legacy/ms633573(v=vs.85)) is a placeholder for the application-defined function name.</span></span> <br/>                                                            |



 

 

 
