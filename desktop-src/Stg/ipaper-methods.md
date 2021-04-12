---
title: IPaper-Methoden
description: Stellt copaper-Objekte bereit, die hauptsächlich von ihrer nativen iPaper-Schnittstelle gesteuert werden.
ms.assetid: 3b77a6b3-8ec3-4a91-82cd-1f08d10fbf73
keywords:
- IPaper
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f84153c9fcec021d9084807d73d46198e3a56482
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "104207301"
---
# <a name="ipaper-methods"></a><span data-ttu-id="c19fe-104">IPaper-Methoden</span><span class="sxs-lookup"><span data-stu-id="c19fe-104">IPaper Methods</span></span>

<span data-ttu-id="c19fe-105">**Stoservice** bietet copaper-Objekte, die in erster Linie von ihrer nativen **iPaper** -Schnittstelle gesteuert werden.</span><span class="sxs-lookup"><span data-stu-id="c19fe-105">**StoServe** provides COPaper objects that are controlled primarily by their native **IPaper** interface.</span></span>

<span data-ttu-id="c19fe-106">In der folgenden Tabelle sind die **iPaper** -Methoden aus iPaper aufgeführt. H im neben geordneten \\ Inc-Verzeichnis.</span><span class="sxs-lookup"><span data-stu-id="c19fe-106">The following table lists **IPaper** methods from IPAPER.H in the sibling \\INC directory.</span></span>



| <span data-ttu-id="c19fe-107">Methode</span><span class="sxs-lookup"><span data-stu-id="c19fe-107">Method</span></span>    | <span data-ttu-id="c19fe-108">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="c19fe-108">Description</span></span>                                                         |
|-----------|---------------------------------------------------------------------|
| <span data-ttu-id="c19fe-109">Initpaper</span><span class="sxs-lookup"><span data-stu-id="c19fe-109">InitPaper</span></span> | <span data-ttu-id="c19fe-110">Initialisiert ein Papierobjekt und erstellt ein frei Hand Daten Array.</span><span class="sxs-lookup"><span data-stu-id="c19fe-110">Initializes paper object and create ink data array.</span></span>                 |
| <span data-ttu-id="c19fe-111">Sperre</span><span class="sxs-lookup"><span data-stu-id="c19fe-111">Lock</span></span>      | <span data-ttu-id="c19fe-112">Ermöglicht die Client Steuerung des Papiers und sperrt andere Clients.</span><span class="sxs-lookup"><span data-stu-id="c19fe-112">Gives client control of the paper and locks out other clients.</span></span>      |
| <span data-ttu-id="c19fe-113">Unlock</span><span class="sxs-lookup"><span data-stu-id="c19fe-113">Unlock</span></span>    | <span data-ttu-id="c19fe-114">Gibt die Client Steuerung des Papiers aus.</span><span class="sxs-lookup"><span data-stu-id="c19fe-114">Relinquishes client control of the paper.</span></span>                           |
| <span data-ttu-id="c19fe-115">Laden</span><span class="sxs-lookup"><span data-stu-id="c19fe-115">Load</span></span>      | <span data-ttu-id="c19fe-116">Lädt Papier Inhalt aus der Verbund Datei des Clients und benachrichtigt senken.</span><span class="sxs-lookup"><span data-stu-id="c19fe-116">Loads paper content from client's compound file and notifies sinks.</span></span> |
| <span data-ttu-id="c19fe-117">Speichern</span><span class="sxs-lookup"><span data-stu-id="c19fe-117">Save</span></span>      | <span data-ttu-id="c19fe-118">Speichert Papier Inhalt in der Verbund Datei des Clients.</span><span class="sxs-lookup"><span data-stu-id="c19fe-118">Saves paper content to client's compound file.</span></span>                      |
| <span data-ttu-id="c19fe-119">Inkstart</span><span class="sxs-lookup"><span data-stu-id="c19fe-119">InkStart</span></span>  | <span data-ttu-id="c19fe-120">Startet das Zeichnen von Farb Freihand auf der Papieroberfläche.</span><span class="sxs-lookup"><span data-stu-id="c19fe-120">Starts color ink drawing to the paper surface.</span></span>                      |
| <span data-ttu-id="c19fe-121">Inkdraw</span><span class="sxs-lookup"><span data-stu-id="c19fe-121">InkDraw</span></span>   | <span data-ttu-id="c19fe-122">Legt frei Hand Datenpunkte auf der elektronischen Papieroberfläche ab.</span><span class="sxs-lookup"><span data-stu-id="c19fe-122">Puts ink data points on the electronic paper surface.</span></span>               |
| <span data-ttu-id="c19fe-123">Inkstopps</span><span class="sxs-lookup"><span data-stu-id="c19fe-123">InkStop</span></span>   | <span data-ttu-id="c19fe-124">Stoppt das Zeichnen von frei Hand Eingaben auf die Papieroberfläche.</span><span class="sxs-lookup"><span data-stu-id="c19fe-124">Stops ink drawing to the paper surface.</span></span>                             |
| <span data-ttu-id="c19fe-125">Löschen</span><span class="sxs-lookup"><span data-stu-id="c19fe-125">Erase</span></span>     | <span data-ttu-id="c19fe-126">Löscht den aktuellen Papier Inhalt und benachrichtigt senken.</span><span class="sxs-lookup"><span data-stu-id="c19fe-126">Erase the current paper content and notifies sinks.</span></span>                 |
| <span data-ttu-id="c19fe-127">Größe ändern</span><span class="sxs-lookup"><span data-stu-id="c19fe-127">Resize</span></span>    | <span data-ttu-id="c19fe-128">Ändert die Größe der Größe des Zeichnungs Papier Rechtecks und benachrichtigt senken.</span><span class="sxs-lookup"><span data-stu-id="c19fe-128">Resizes the drawing paper rectangle size and notifies sinks.</span></span>        |
| <span data-ttu-id="c19fe-129">Neu zeichnen</span><span class="sxs-lookup"><span data-stu-id="c19fe-129">Redraw</span></span>    | <span data-ttu-id="c19fe-130">Zeichnet den Inhalt des Papier Objekts neu und benachrichtigt senken.</span><span class="sxs-lookup"><span data-stu-id="c19fe-130">Redraws contents of paper object and notifies sinks.</span></span>                |



 

<span data-ttu-id="c19fe-131">Relevante Methoden für dieses Codebeispiel für Verbund Dateien sind [**Laden**](ipaper--load.md), [**Speichern**](ipaper--save.md)und [**neu zeichnen**](ipaper--redraw.md).</span><span class="sxs-lookup"><span data-stu-id="c19fe-131">Methods of interest for this code sample on compound files are [**Load**](ipaper--load.md), [**Save**](ipaper--save.md), and [**Redraw**](ipaper--redraw.md).</span></span>

<span data-ttu-id="c19fe-132">[**Inkstart**](inkstart-method.md), [**inkdraw**](inkdraw-method.md)und [**inkstopps**](cguipaper-methods.md) sind Methoden, die von Clients verwendet werden, um copaper zum Aufzeichnen von Handzeichen Sequenzen zu Befehlen.</span><span class="sxs-lookup"><span data-stu-id="c19fe-132">[**InkStart**](inkstart-method.md), [**InkDraw**](inkdraw-method.md), and [**InkStop**](cguipaper-methods.md) are methods used by clients to command COPaper to record ink drawing sequences.</span></span> <span data-ttu-id="c19fe-133">Der Client antwortet in der Regel auf eine WM- \_ lbuttondown-Meldung als Anfang einer frei Hand Zeichnungs Sequenz durch Aufrufen von **inkstart** bei copaper.</span><span class="sxs-lookup"><span data-stu-id="c19fe-133">The client will typically respond to a WM\_LBUTTONDOWN message as the start of an ink drawing sequence by calling **InkStart** on COPaper.</span></span> <span data-ttu-id="c19fe-134">Wenn der Benutzer die Maus oder den Stift zum Zeichnen bewegt, während er die linke Schaltfläche gedrückt hält, antwortet der Client auf wiederholte WM- \_ MouseMove-Meldungen mit entsprechenden Aufrufen von **inkdraw**.</span><span class="sxs-lookup"><span data-stu-id="c19fe-134">As the user moves the mouse or pen to draw while holding down the left button, the client will respond to repeated WM\_MOUSEMOVE messages with corresponding calls to **InkDraw**.</span></span> <span data-ttu-id="c19fe-135">Wenn der Benutzer die linke Maustaste loslässt, antwortet der Client auf eine WM- \_ lbuttonup-Meldung mit dem aufzurufenden Ink-Befehl, der das Ende der frei Hand Zeichnungs Sequenz markiert. </span><span class="sxs-lookup"><span data-stu-id="c19fe-135">When the user releases the left mouse button, the client will respond to a WM\_LBUTTONUP message with a call to **InkStop**, which marks the end of the ink drawing sequence.</span></span>

<span data-ttu-id="c19fe-136">[**Inkstart**](inkstart-method.md) weist copaper die Anfangsposition der Zeichnungs Sequenz in Client Fenster Koordinaten zu.</span><span class="sxs-lookup"><span data-stu-id="c19fe-136">[**InkStart**](inkstart-method.md) tells COPaper the start position for the drawing sequence in client window coordinates.</span></span> <span data-ttu-id="c19fe-137">Außerdem übergibt Sie die aktuell ausgewählte frei Hand Farbe und-Breite.</span><span class="sxs-lookup"><span data-stu-id="c19fe-137">It also passes the currently selected ink color and width.</span></span> <span data-ttu-id="c19fe-138">Diese Auswahl wird vom Client beibehalten. Copaper zeichnet Sie nur auf, wenn der **inkstart** -Rückruf erfolgt.</span><span class="sxs-lookup"><span data-stu-id="c19fe-138">The client maintains these selections; COPaper merely records them when the **InkStart** call is made.</span></span> <span data-ttu-id="c19fe-139">[**Inkdraw**](inkdraw-method.md) wird wiederholt aufgerufen, um copaper die Abfolge der Fenster Koordinaten anzugeben, die die Zeichnungs Bewegung der Maus oder des Stifts darstellen.</span><span class="sxs-lookup"><span data-stu-id="c19fe-139">[**InkDraw**](inkdraw-method.md) is called repeatedly to tell COPaper the succession of window coordinates that represent the drawing motion of the mouse or pen.</span></span> <span data-ttu-id="c19fe-140">[**Inkbeenden**](cguipaper-methods.md) weist copaper an, das Ende einer Zeichnungs Sequenz zu markieren.</span><span class="sxs-lookup"><span data-stu-id="c19fe-140">[**InkStop**](cguipaper-methods.md) instructs COPaper to mark the end of a drawing sequence.</span></span>

 

 




