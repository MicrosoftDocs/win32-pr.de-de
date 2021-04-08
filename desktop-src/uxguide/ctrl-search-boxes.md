---
title: Suchfelder
description: Mithilfe eines Suchfeld können Benutzer mithilfe von Filtern oder Hervorhebungen von Übereinstimmungen bestimmte Objekte oder Text innerhalb eines großen Satzes von Daten schnell finden.
ms.assetid: e2d77b36-e001-403c-9b66-2d136c394a24
ms.topic: article
ms.date: 10/20/2020
ms.openlocfilehash: e9d1fca8fdb96b17098cee79fd5b62ecd7ab7531
ms.sourcegitcommit: 3bdf30edb314e0fcd17dc4ddbc70e4ec7d3596e6
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 02/10/2021
ms.locfileid: "103961078"
---
# <a name="search-boxes"></a><span data-ttu-id="88ebd-103">Suchfelder</span><span class="sxs-lookup"><span data-stu-id="88ebd-103">Search Boxes</span></span>

> [!NOTE]
> <span data-ttu-id="88ebd-104">Dieses Entwurfs Handbuch wurde für Windows 7 erstellt und wurde für neuere Versionen von Windows nicht aktualisiert.</span><span class="sxs-lookup"><span data-stu-id="88ebd-104">This design guide was created for Windows 7 and has not been updated for newer versions of Windows.</span></span> <span data-ttu-id="88ebd-105">Ein Großteil der Anleitungen gilt weiterhin im Prinzip, aber die Präsentation und die Beispiele entsprechen nicht unseren [aktuellen Entwurfs Anleitungen](/windows/uwp/design/).</span><span class="sxs-lookup"><span data-stu-id="88ebd-105">Much of the guidance still applies in principle, but the presentation and examples do not reflect our [current design guidance](/windows/uwp/design/).</span></span>

<span data-ttu-id="88ebd-106">Mithilfe eines Suchfeld können Benutzer mithilfe von Filtern oder Hervorhebungen von Übereinstimmungen bestimmte Objekte oder Text innerhalb eines großen Satzes von Daten schnell finden.</span><span class="sxs-lookup"><span data-stu-id="88ebd-106">With a Search box, users can quickly locate specific objects or text within a large set of data by filtering or highlighting matches.</span></span> <span data-ttu-id="88ebd-107">Es gibt kein Standard-Such Steuerelement, aber Sie sollten sich darauf konzentrieren, die Suchfunktionen Ihres Programms mit denen von Windows konsistent zu machen.</span><span class="sxs-lookup"><span data-stu-id="88ebd-107">There is no standard search control, but you should strive to make your program's search features consistent with those of Windows.</span></span>

<span data-ttu-id="88ebd-108">Es gibt zwei Arten von Such Vorgängen:</span><span class="sxs-lookup"><span data-stu-id="88ebd-108">There are two types of searches:</span></span>

-   <span data-ttu-id="88ebd-109">**Sofortige Suche**, bei der die Ergebnisse sofort angezeigt werden, wenn der Benutzer Sie eingibt.</span><span class="sxs-lookup"><span data-stu-id="88ebd-109">**Instant search**, where the results are displayed immediately as the user types.</span></span> <span data-ttu-id="88ebd-110">Es muss keine Schaltfläche geklickt werden, sodass das Lupen Suchsymbol als Grafik und nicht als Schaltfläche angezeigt wird.</span><span class="sxs-lookup"><span data-stu-id="88ebd-110">No button needs to be clicked, so the magnifying glass search symbol is shown as a graphic, not a button.</span></span>

    ![Screenshot, der ein sofortiges Suchfeld mit einer "Prompt"-Legende anzeigt, die auf das Suchfeld zeigt, und ein Symbol "Suchsymbol", das auf die Lupen Grafik zeigt.](images/ctrl-search-boxes-image1.png)

    <span data-ttu-id="88ebd-112">Ein typisches Suchfeld mit sofortiger Suche.</span><span class="sxs-lookup"><span data-stu-id="88ebd-112">A typical Search box using Instant search.</span></span> <span data-ttu-id="88ebd-113">Die Suche wird automatisch auf jedem Tastatur Strich ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="88ebd-113">Search is automatically executed on every keystroke.</span></span>

-   <span data-ttu-id="88ebd-114">**Reguläre Suche**, bei der eine Suche durchgeführt wird, wenn der Benutzer auf die Such Schaltfläche klickt.</span><span class="sxs-lookup"><span data-stu-id="88ebd-114">**Regular search**, where a search is performed when the user clicks the search button.</span></span> <span data-ttu-id="88ebd-115">Das Lupen Suchsymbol wird auf einer Schaltfläche angezeigt.</span><span class="sxs-lookup"><span data-stu-id="88ebd-115">The magnifying glass search symbol is shown on a button.</span></span>

    ![<span data-ttu-id="88ebd-116">Screenshot eines regulären Suchfelds</span><span class="sxs-lookup"><span data-stu-id="88ebd-116">screen shot of a regular search box</span></span> ](images/ctrl-search-boxes-image2.png)

    <span data-ttu-id="88ebd-117">Ein typisches Suchfeld mit regulärer Suche.</span><span class="sxs-lookup"><span data-stu-id="88ebd-117">A typical Search box using regular search.</span></span> <span data-ttu-id="88ebd-118">Benutzer klicken auf eine Schaltfläche, um die Suche auszuführen.</span><span class="sxs-lookup"><span data-stu-id="88ebd-118">Users click a button to perform the search.</span></span>

    <span data-ttu-id="88ebd-119">Sie können eine oder beide Arten von Suchoptionen für Ihre Benutzer bereitstellen.</span><span class="sxs-lookup"><span data-stu-id="88ebd-119">You can provide either or both kinds of search options for your users.</span></span>

## <a name="is-this-the-right-control"></a><span data-ttu-id="88ebd-120">Ist dies das richtige Steuerelement?</span><span class="sxs-lookup"><span data-stu-id="88ebd-120">Is this the right control?</span></span>

<span data-ttu-id="88ebd-121">Orientieren Sie sich an folgenden Fragen:</span><span class="sxs-lookup"><span data-stu-id="88ebd-121">To decide, consider these questions:</span></span>

-   <span data-ttu-id="88ebd-122">**Sind bestimmte Objekte schwer zu finden?**</span><span class="sxs-lookup"><span data-stu-id="88ebd-122">**Are specific objects difficult to find?**</span></span> <span data-ttu-id="88ebd-123">Dies kann passieren, wenn:</span><span class="sxs-lookup"><span data-stu-id="88ebd-123">This can happen when:</span></span>
    -   <span data-ttu-id="88ebd-124">Es sind viele Objekte vorhanden.</span><span class="sxs-lookup"><span data-stu-id="88ebd-124">There are many objects.</span></span>
    -   <span data-ttu-id="88ebd-125">Die Objekte befinden sich nicht an einem einzigen Speicherort.</span><span class="sxs-lookup"><span data-stu-id="88ebd-125">The objects aren't located in a single location.</span></span> <span data-ttu-id="88ebd-126">Die Suche ist besonders nützlich für das Auffinden von Objekten in Strukturen.</span><span class="sxs-lookup"><span data-stu-id="88ebd-126">Search is especially useful for finding objects in trees.</span></span>
    -   <span data-ttu-id="88ebd-127">Die Suchdaten sind schwer zu finden (z. b. Metadaten).</span><span class="sxs-lookup"><span data-stu-id="88ebd-127">The search data is difficult to find (for example, metadata).</span></span>
-   <span data-ttu-id="88ebd-128">**Müssen Benutzer bestimmten Text in Dokumenten finden?**</span><span class="sxs-lookup"><span data-stu-id="88ebd-128">**Do users need to find specific text within documents?**</span></span>
-   <span data-ttu-id="88ebd-129">**Gibt ihre Funktion relevante Suchergebnisse innerhalb von fünf Sekunden zurück?**</span><span class="sxs-lookup"><span data-stu-id="88ebd-129">**Does your feature return relevant search results within five seconds?**</span></span> <span data-ttu-id="88ebd-130">Wenn dies nicht der Fall ist, können Sie eine Suchfunktion bereitstellen, aber einen alternativen Entwurf verwenden, der ein sichtbares Feedback bietet, um Suchvorgänge mit langer Ausführungszeit zu ermöglichen</span><span class="sxs-lookup"><span data-stu-id="88ebd-130">If not, you can provide a search feature, but use an alternative design that gives visible feedback to accommodate long-running searches, such as a search dialog box.</span></span>

## <a name="design-concepts"></a><span data-ttu-id="88ebd-131">Entwurfskonzepte</span><span class="sxs-lookup"><span data-stu-id="88ebd-131">Design concepts</span></span>

<span data-ttu-id="88ebd-132">Die Suche ist ein wichtiger erster Schritt in vielen Szenarien: Benutzer müssen Objekte suchen, bevor Sie Sie verwenden können.</span><span class="sxs-lookup"><span data-stu-id="88ebd-132">Searching is a crucial first step in many scenarios: Users must find objects before they can use them.</span></span> <span data-ttu-id="88ebd-133">Benutzer speichern mehr und mehr Objekte auf immer größeren Festplatten, aber das Durchsuchen nach Objekten ist nicht gut skalierbar.</span><span class="sxs-lookup"><span data-stu-id="88ebd-133">Users are saving more and more objects on increasingly larger hard disks, but browsing for objects doesn't scale well.</span></span> <span data-ttu-id="88ebd-134">Die Suche muss ein einfacher, konsistentes und zuverlässiger Teil des Benutzer Erlebnisses sein.</span><span class="sxs-lookup"><span data-stu-id="88ebd-134">Search must be a simple, consistent, reliable part of the user experience.</span></span>

<span data-ttu-id="88ebd-135">Suchfelder in Windows:</span><span class="sxs-lookup"><span data-stu-id="88ebd-135">Search boxes in Windows:</span></span>

-   <span data-ttu-id="88ebd-136">Sind Teil aller Explorer-Fenster, sodass Sie leicht zu finden und zu erkennen sind.</span><span class="sxs-lookup"><span data-stu-id="88ebd-136">Are part of all Explorer windows, so they are easy to find and recognize.</span></span>
-   <span data-ttu-id="88ebd-137">Konsistente Darstellung und Verhalten.</span><span class="sxs-lookup"><span data-stu-id="88ebd-137">Have consistent appearance and behavior.</span></span>
-   <span data-ttu-id="88ebd-138">Sind effizient und schnell und geben sofortige Ergebnisse im sofort Suchmodus aus.</span><span class="sxs-lookup"><span data-stu-id="88ebd-138">Are efficient and fast, giving instant results in Instant search mode.</span></span>

<span data-ttu-id="88ebd-139">In Windows wird an diesen Stellen ein Suchfeld verwendet:</span><span class="sxs-lookup"><span data-stu-id="88ebd-139">A Search box is used in Windows in these places:</span></span>

-   <span data-ttu-id="88ebd-140">Explorer</span><span class="sxs-lookup"><span data-stu-id="88ebd-140">Explorers</span></span>
-   <span data-ttu-id="88ebd-141">Erlebnisse (Microsoft Windows Media Player, Windows-Fotogalerie, Windows Internet Explorer)</span><span class="sxs-lookup"><span data-stu-id="88ebd-141">Experiences (Microsoft Windows Media Player, Windows Photo Gallery, Windows Internet Explorer)</span></span>
-   <span data-ttu-id="88ebd-142">Startmenü (zum Suchen nach Programmen und zuletzt verwendeten Dateien)</span><span class="sxs-lookup"><span data-stu-id="88ebd-142">Start menu (to find programs and recent files)</span></span>
-   <span data-ttu-id="88ebd-143">Startseite der Systemsteuerung (um System Steuerungselemente und Aufgaben zu suchen)</span><span class="sxs-lookup"><span data-stu-id="88ebd-143">Control Panel home page (to find control panel items and tasks)</span></span>
-   <span data-ttu-id="88ebd-144">Hilfe (um relevante Hilfe Themen zu finden)</span><span class="sxs-lookup"><span data-stu-id="88ebd-144">Help (to find relevant Help topics)</span></span>

### <a name="look-and-feel"></a><span data-ttu-id="88ebd-145">Aussehen und Gefühl</span><span class="sxs-lookup"><span data-stu-id="88ebd-145">Look and feel</span></span>

<span data-ttu-id="88ebd-146">Das Gefühl der Suche in Windows wird durch die Unterstützung der sofortigen Suche erheblich verbessert.</span><span class="sxs-lookup"><span data-stu-id="88ebd-146">The feel of Search in Windows is significantly enhanced by supporting Instant search.</span></span> <span data-ttu-id="88ebd-147">Wenn Sie sofortige Ergebnisse haben, ist das Gefühl von Windows leistungsfähiger und direkter.</span><span class="sxs-lookup"><span data-stu-id="88ebd-147">Having instant results makes Windows feel more powerful and direct.</span></span>

<span data-ttu-id="88ebd-148">In Windows-Explorer und Anwendungs Fenstern befindet sich die Suche in der oberen rechten Ecke, wenn es sich um einen ergänzenden Einstiegspunkt handelt.</span><span class="sxs-lookup"><span data-stu-id="88ebd-148">In Windows Explorer and application windows, Search is located in the upper-right corner if it is a supplemental entry point.</span></span> <span data-ttu-id="88ebd-149">In diesem Fall suchen Benutzer nach einem Suchmechanismus, wenn Sie im Fenster nicht finden, was Sie suchen.</span><span class="sxs-lookup"><span data-stu-id="88ebd-149">In this case, users look for a search mechanism when they don't find what they are looking for in the window.</span></span> <span data-ttu-id="88ebd-150">Wenn die Suche jedoch der primäre Einstiegspunkt ist, wird Sie am oberen Rand des Fensters zentriert.</span><span class="sxs-lookup"><span data-stu-id="88ebd-150">However, if Search is the primary entry point, it is centered at the top of the window.</span></span>

<span data-ttu-id="88ebd-151">Die Such Schaltfläche ist visuell mit einem Suchfeld verbunden.</span><span class="sxs-lookup"><span data-stu-id="88ebd-151">The Search button is visually connected to a Search box.</span></span> <span data-ttu-id="88ebd-152">Um den Speicherplatz zu minimieren, wird eine optionale [Eingabeaufforderung](ctrl-text-boxes.md) in einem Suchfeld anstelle einer Bezeichnung verwendet.</span><span class="sxs-lookup"><span data-stu-id="88ebd-152">To minimize space, an optional [prompt](ctrl-text-boxes.md) is used inside a Search box instead of a label.</span></span> <span data-ttu-id="88ebd-153">Die Eingabeaufforderung kann eine Anweisung sein (z. b. zum Suchen eingeben) oder den Suchbereich angeben (z. b. Suche nach Bildern).</span><span class="sxs-lookup"><span data-stu-id="88ebd-153">The prompt may be an instruction (for example, Type to search) or indicate the scope of the search (for example, Search for pictures).</span></span>

![<span data-ttu-id="88ebd-154">Screenshot eines sofort Suchfelds</span><span class="sxs-lookup"><span data-stu-id="88ebd-154">screen shot of an instant search box</span></span> ](images/ctrl-search-boxes-image3.png)

<span data-ttu-id="88ebd-155">Ohne Bezeichnungen und separate Schaltflächen weist die sofortige Suche in Windows ein schlankes Aussehen auf.</span><span class="sxs-lookup"><span data-stu-id="88ebd-155">Without labels and separate buttons, Instant search in Windows has a lightweight look.</span></span>

<span data-ttu-id="88ebd-156">Durch das Durchführen einer erfolgreichen Suche wird eine virtuelle Seite der Suchergebnisse erstellt und dem Hintergrund Stapel und der Adressleiste hinzugefügt.</span><span class="sxs-lookup"><span data-stu-id="88ebd-156">Performing a successful search creates a virtual page of the search results and adds it to the Back stack and Address bar.</span></span> <span data-ttu-id="88ebd-157">Benutzer haben mehrere Möglichkeiten, die ursprüngliche Seite wiederherzustellen und ein Suchfeld zu löschen. dazu gehören das Klicken auf die ursprüngliche Seite in der Adressleiste, das Drücken der ESC-Taste oder das Löschen des Suchfelds.</span><span class="sxs-lookup"><span data-stu-id="88ebd-157">Users have several ways to restore the original page and clear a Search box, including clicking Back, clicking the original page in the Address bar, pressing Esc, or clearing the Search box.</span></span>

<span data-ttu-id="88ebd-158">Benutzer können auch einfach das Suchfeld löschen, ohne eine vorherige Seite der Ergebnisse wiederherzustellen.</span><span class="sxs-lookup"><span data-stu-id="88ebd-158">Users can also simply clear the Search box without restoring a previous page of results.</span></span> <span data-ttu-id="88ebd-159">Im sofort Suchmodus wird eine Schaltfläche Clear angezeigt, nachdem der Benutzer mit der Eingabe begonnen hat. ein "x" ersetzt das Lupen Suchsymbol.</span><span class="sxs-lookup"><span data-stu-id="88ebd-159">In Instant search mode, a clear button appears after the user starts typing; an "x" replaces the magnifying glass search symbol.</span></span> <span data-ttu-id="88ebd-160">Wenn Sie darauf zeigen, erhält das "x" eine Schaltfläche, auf die geklickt werden kann.</span><span class="sxs-lookup"><span data-stu-id="88ebd-160">On hover, the "x" gets a button look and can be clicked.</span></span>

![<span data-ttu-id="88ebd-161">Screenshot eines Suchfeld mit dem Symbol "x"</span><span class="sxs-lookup"><span data-stu-id="88ebd-161">screen shot of a search box with an 'x' icon</span></span> ](images/ctrl-search-boxes-image4.png)

<span data-ttu-id="88ebd-162">Der Benutzer kann das Suchfeld durch Klicken auf "x" am rechten Ende des Steuer Elements löschen.</span><span class="sxs-lookup"><span data-stu-id="88ebd-162">The user can clear the Search box by clicking "x" at the right end of the control.</span></span>

<span data-ttu-id="88ebd-163">Im regulären Suchmodus ist die Schaltfläche Clear optional.</span><span class="sxs-lookup"><span data-stu-id="88ebd-163">In regular search mode, the clear button is optional.</span></span> <span data-ttu-id="88ebd-164">Benutzer sind möglicherweise hilfreich, z. b. Wenn eine Suche eine lange Zeit in Anspruch nimmt.</span><span class="sxs-lookup"><span data-stu-id="88ebd-164">Users may find it useful, for example, if a search is taking a long time to complete.</span></span> <span data-ttu-id="88ebd-165">Benutzer können auf das "x" klicken, um die Suche zu verhindern.</span><span class="sxs-lookup"><span data-stu-id="88ebd-165">Users can click the "x" to stop the search in progress.</span></span> <span data-ttu-id="88ebd-166">Wenn eine Suche bereits abgeschlossen ist, können Benutzer auf das "x" klicken, um das Suchfeld zu löschen.</span><span class="sxs-lookup"><span data-stu-id="88ebd-166">If a search has already completed, users can click the "x" to clear the Search box.</span></span>

## <a name="guidelines"></a><span data-ttu-id="88ebd-167">Richtlinien</span><span class="sxs-lookup"><span data-stu-id="88ebd-167">Guidelines</span></span>

### <a name="location"></a><span data-ttu-id="88ebd-168">Standort</span><span class="sxs-lookup"><span data-stu-id="88ebd-168">Location</span></span>

-   <span data-ttu-id="88ebd-169">Suchen Sie unter Anwendungsfenster in der oberen rechten Ecke nach suchen.</span><span class="sxs-lookup"><span data-stu-id="88ebd-169">For application windows, locate Search in the upper-right corner.</span></span>
-   <span data-ttu-id="88ebd-170">Für Popup Fenster Suchen Sie nach wo immer sinnvollsten und bequemsten.</span><span class="sxs-lookup"><span data-stu-id="88ebd-170">For popup windows, locate Search wherever is most sensible and convenient.</span></span>
-   <span data-ttu-id="88ebd-171">**Ausnahme:** Wenn die Suche in der Regel das erste ist, das Benutzer in einem Fenster ausführen (der primäre Einstiegspunkt), zentrieren Sie es am oberen Rand des Fensters.</span><span class="sxs-lookup"><span data-stu-id="88ebd-171">**Exception:** If Search is usually the first thing users do in a window (the primary entry point), center it at the top of the window.</span></span>

### <a name="look"></a><span data-ttu-id="88ebd-172">Blicke</span><span class="sxs-lookup"><span data-stu-id="88ebd-172">Look</span></span>

-   <span data-ttu-id="88ebd-173">Verwenden Sie die Standardgrafiken für die Such Schaltfläche.</span><span class="sxs-lookup"><span data-stu-id="88ebd-173">Use the standard search button graphics.</span></span> <span data-ttu-id="88ebd-174">Es gibt drei Versionen:</span><span class="sxs-lookup"><span data-stu-id="88ebd-174">There are three versions:</span></span>
    -   <span data-ttu-id="88ebd-175">**Nur Lupen Suchsymbol (keine Schaltfläche auf dem Mauszeiger).**</span><span class="sxs-lookup"><span data-stu-id="88ebd-175">**Magnifying glass search symbol only (no button on hover).**</span></span> <span data-ttu-id="88ebd-176">Verwenden Sie für die sofortige Suche.</span><span class="sxs-lookup"><span data-stu-id="88ebd-176">Use for Instant search.</span></span>
    -   <span data-ttu-id="88ebd-177">**Lupen Suchsymbol mit Schaltfläche.**</span><span class="sxs-lookup"><span data-stu-id="88ebd-177">**Magnifying glass search symbol with button.**</span></span> <span data-ttu-id="88ebd-178">Verwenden Sie, wenn auf die Schaltfläche zum Starten der Suche geklickt werden muss.</span><span class="sxs-lookup"><span data-stu-id="88ebd-178">Use when button needs to be clicked to start the search.</span></span>
    -   <span data-ttu-id="88ebd-179">**Lupen Suchsymbol mit Schaltfläche und Dropdown Pfeil.**</span><span class="sxs-lookup"><span data-stu-id="88ebd-179">**Magnifying glass search symbol with button and drop-down arrow.**</span></span> <span data-ttu-id="88ebd-180">Fügen Sie einen Dropdown Pfeil hinzu, wenn Benutzer den Bereich ändern können oder wenn andere Einstellungen verfügbar sind.</span><span class="sxs-lookup"><span data-stu-id="88ebd-180">Add a drop-down arrow when users can change the scope or when other settings are available.</span></span>
        -   <span data-ttu-id="88ebd-181">Verwenden Sie für die sofortige Suche nur einen Dropdown Pfeil, und klicken Sie auf die Schaltfläche mit dem Mauszeiger.</span><span class="sxs-lookup"><span data-stu-id="88ebd-181">For Instant search, use a drop-down arrow only, and show a button on hover.</span></span>
        -   <span data-ttu-id="88ebd-182">Zeigen Sie bei regulärer Suche den Dropdown Pfeil auf einer Schaltfläche an.</span><span class="sxs-lookup"><span data-stu-id="88ebd-182">For regular search, show the drop-down arrow on a button.</span></span>

![<span data-ttu-id="88ebd-183">Abbildung der Felder für die sofortige Suche in verschiedenen Zuständen</span><span class="sxs-lookup"><span data-stu-id="88ebd-183">figure of instant search boxes in different states</span></span> ](images/ctrl-search-boxes-image5.png)

<span data-ttu-id="88ebd-184">Visuelle Spezifikationen für die sofortige Suche.</span><span class="sxs-lookup"><span data-stu-id="88ebd-184">Visual specifications for Instant search.</span></span>

![<span data-ttu-id="88ebd-185">Abbildung regulärer Suchfelder in unterschiedlichen Zuständen</span><span class="sxs-lookup"><span data-stu-id="88ebd-185">figure of regular search boxes in different states</span></span> ](images/ctrl-search-boxes-image6.png)

<span data-ttu-id="88ebd-186">Visuelle Spezifikationen für die reguläre Suche.</span><span class="sxs-lookup"><span data-stu-id="88ebd-186">Visual specifications for regular search.</span></span>

-   <span data-ttu-id="88ebd-187">Verwenden Sie keine Bezeichnung. Verwenden Sie stattdessen eine optionale Eingabeaufforderung.</span><span class="sxs-lookup"><span data-stu-id="88ebd-187">Don't use a label; use an optional prompt instead.</span></span> <span data-ttu-id="88ebd-188">Wenn Benutzer tendenziell davon ausgehen, dass es sich bei der Suche um eine generische Dateisuche handelt, verwenden Sie die Eingabeaufforderung, um den Bereich anzugeben.</span><span class="sxs-lookup"><span data-stu-id="88ebd-188">If users tend to assume that the search is a generic file search, use the prompt to give the scope.</span></span> <span data-ttu-id="88ebd-189">Verwenden Sie andernfalls Type, um zu suchen, oder einen ähnlichen, präzisen Ausdruck.</span><span class="sxs-lookup"><span data-stu-id="88ebd-189">Otherwise, use Type to search or a similar, concise phrase.</span></span>

    ![<span data-ttu-id="88ebd-190">Screenshot der Eingabeaufforderung "Typ für Suche"</span><span class="sxs-lookup"><span data-stu-id="88ebd-190">screen shot of 'type to search' prompt</span></span> ](images/ctrl-search-boxes-image7.png)

    ![<span data-ttu-id="88ebd-191">Screenshot der Eingabeaufforderung "alle Gadgets suchen"</span><span class="sxs-lookup"><span data-stu-id="88ebd-191">screen shot of 'search all gadgets' prompt</span></span> ](images/ctrl-search-boxes-image8.png)

    <span data-ttu-id="88ebd-192">In diesen Beispielen helfen Ihnen kurze Text Aufforderungen beim Arbeiten mit der Suche.</span><span class="sxs-lookup"><span data-stu-id="88ebd-192">In these examples, brief textual prompts help users work with Search.</span></span>

### <a name="interaction"></a><span data-ttu-id="88ebd-193">Interaktion</span><span class="sxs-lookup"><span data-stu-id="88ebd-193">Interaction</span></span>

-   <span data-ttu-id="88ebd-194">**Wählen Sie im Eingabefokus automatisch einen zuvor eingegebenen Text aus.**</span><span class="sxs-lookup"><span data-stu-id="88ebd-194">**On input focus, automatically select any previously entered text.**</span></span> <span data-ttu-id="88ebd-195">Auf diese Weise können Benutzer eine neue Suche eingeben, indem Sie eingeben oder die vorherige Suche ändern, indem Sie die Einfügemarke mithilfe der Pfeiltasten positionieren.</span><span class="sxs-lookup"><span data-stu-id="88ebd-195">Doing so allows users to enter a new search by typing, or to modify the previous search by positioning the caret using the arrow keys.</span></span>

    ![<span data-ttu-id="88ebd-196">Screenshot des Suchfelds mit markiertem Text</span><span class="sxs-lookup"><span data-stu-id="88ebd-196">screen shot of search box with highlighted text</span></span> ](images/ctrl-search-boxes-image9.png)

    <span data-ttu-id="88ebd-197">In diesem Beispiel wird der zuvor eingegebene Text im Eingabefokus ausgewählt.</span><span class="sxs-lookup"><span data-stu-id="88ebd-197">In this example, previously entered text is selected on input focus.</span></span>

-   <span data-ttu-id="88ebd-198">**Weisen Sie die Tastenkombination für das Suchfeld STRG + E zu.**</span><span class="sxs-lookup"><span data-stu-id="88ebd-198">**Assign the keyboard shortcut for the Search box to be Ctrl+E.**</span></span>

### <a name="functionality"></a><span data-ttu-id="88ebd-199">Funktionalität</span><span class="sxs-lookup"><span data-stu-id="88ebd-199">Functionality</span></span>

-   <span data-ttu-id="88ebd-200">**Unterstützung von Instant Search, wann immer möglich.**</span><span class="sxs-lookup"><span data-stu-id="88ebd-200">**Support Instant search whenever possible.**</span></span> <span data-ttu-id="88ebd-201">Stellen Sie sowohl reguläre als auch sofortige suchen bereit, wenn es Szenarien gibt, in denen die reguläre Suche die zusätzliche Wartezeit Wert ist.</span><span class="sxs-lookup"><span data-stu-id="88ebd-201">Provide both regular and Instant searches if there are scenarios where regular searching is worth the extra wait time.</span></span>
-   <span data-ttu-id="88ebd-202">Reguläre Suchvorgänge müssen innerhalb von fünf Sekunden relevante Ergebnisse zurückgeben, und die sofortige Suche muss innerhalb von zwei Sekunden Ergebnisse zurückgeben.</span><span class="sxs-lookup"><span data-stu-id="88ebd-202">Regular searches must return relevant results within five seconds and Instant search must return results within two seconds.</span></span> <span data-ttu-id="88ebd-203">Nach diesem Punkt kann die Suche weiterhin weniger relevante Ergebnisse im Laufe der Zeit ausfüllen, wenn das Programm reaktionsfähig ist und Benutzer andere Aufgaben ausführen können.</span><span class="sxs-lookup"><span data-stu-id="88ebd-203">After this point, Search may continue to fill in less relevant results over time as long as the program is responsive and users can perform other tasks.</span></span> <span data-ttu-id="88ebd-204">Möglicherweise müssen Sie Ihre Suchdaten indizieren, um die Reaktionsfähigkeit sicherzustellen.</span><span class="sxs-lookup"><span data-stu-id="88ebd-204">You may have to index your search data to ensure this responsiveness.</span></span>
-   <span data-ttu-id="88ebd-205">Wenn Sie sowohl reguläre als auch sofortige Suchmodi bereitstellen, muss es sich bei den unmittelbaren Suchergebnissen um eine Teilmenge der regulären Suchergebnisse handeln.</span><span class="sxs-lookup"><span data-stu-id="88ebd-205">If you provide both regular and Instant search modes, the Instant search results must be a subset of the regular search results.</span></span>
-   <span data-ttu-id="88ebd-206">Alle Suchvorgänge sind Präfix basiert (keine Teil Zeichenfolge oder suffixsuche).</span><span class="sxs-lookup"><span data-stu-id="88ebd-206">All searching is prefix-based (no substring or suffix searching).</span></span> <span data-ttu-id="88ebd-207">Die Verwendung von nachfolgenden Platzhalter Zeichen ist optional und wirkt sich nicht auf die Ergebnisse aus.</span><span class="sxs-lookup"><span data-stu-id="88ebd-207">The use of trailing wildcard characters is optional and doesn't affect the results.</span></span> <span data-ttu-id="88ebd-208">Wenn mehrere Wörter eingegeben werden, verwenden Sie, oder suchen Sie nach.</span><span class="sxs-lookup"><span data-stu-id="88ebd-208">If multiple words are entered, use OR searching.</span></span>
-   <span data-ttu-id="88ebd-209">Bei einer erfolgreichen Suche wird dem BackStack und der Adressleiste eine virtuelle Seite mit den Suchergebnissen hinzugefügt.</span><span class="sxs-lookup"><span data-stu-id="88ebd-209">A successful search adds a virtual page with the search results to the Back stack and Address bar.</span></span> <span data-ttu-id="88ebd-210">Mehrere Suchvorgänge führen zu einer einzelnen virtuellen Seite. Wenn Sie auf "zurück" klicken, wird die ursprüngliche Seite zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="88ebd-210">Multiple searches result in a single virtual page, so clicking Back always returns the original page.</span></span>
-   <span data-ttu-id="88ebd-211">Ordnen Sie bei Bedarf die Suchergebnisse nach Relevanz zu.</span><span class="sxs-lookup"><span data-stu-id="88ebd-211">If necessary for scale, rank the search results by relevance.</span></span>
-   <span data-ttu-id="88ebd-212">Bei einer leeren Suche wird die ursprüngliche Seite zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="88ebd-212">A blank search returns the original page.</span></span>

## <a name="recommended-sizing-and-spacing"></a><span data-ttu-id="88ebd-213">Empfohlene Größe und Abstände</span><span class="sxs-lookup"><span data-stu-id="88ebd-213">Recommended sizing and spacing</span></span>

![<span data-ttu-id="88ebd-214">Abbildung der Größe und des Abstands des unmittelbaren Suchfelds</span><span class="sxs-lookup"><span data-stu-id="88ebd-214">figure of instant search box sizing and spacing</span></span> ](images/ctrl-search-boxes-image10.png)

<span data-ttu-id="88ebd-215">Empfohlene Größe und Abstände für die sofortige Suche.</span><span class="sxs-lookup"><span data-stu-id="88ebd-215">Recommended sizing and spacing for Instant search.</span></span>

![<span data-ttu-id="88ebd-216">Abbildung der regulären Größe und des Abstands von Suchfeldern</span><span class="sxs-lookup"><span data-stu-id="88ebd-216">figure of regular search box sizing and spacing</span></span> ](images/ctrl-search-boxes-image11.png)

<span data-ttu-id="88ebd-217">Empfohlene Größe und Abstände für die reguläre Suche.</span><span class="sxs-lookup"><span data-stu-id="88ebd-217">Recommended sizing and spacing for regular search.</span></span>

## <a name="text"></a><span data-ttu-id="88ebd-218">Text</span><span class="sxs-lookup"><span data-stu-id="88ebd-218">Text</span></span>

-   <span data-ttu-id="88ebd-219">Geben Sie für den Wortlaut der Eingabeaufforderung im Suchfeld entweder eine Anweisung an (z. b. zum Suchen eingeben), oder geben Sie den Suchbereich an (z. b. nach Bildern suchen).</span><span class="sxs-lookup"><span data-stu-id="88ebd-219">For the wording of the prompt in the Search box, either make it an instruction (for example, Type to search) or indicate the scope of the search (for example, Search for pictures).</span></span>
-   <span data-ttu-id="88ebd-220">Der Eingabe Aufforderungs Text sollte kurz sein.</span><span class="sxs-lookup"><span data-stu-id="88ebd-220">Prompt text should be brief.</span></span> <span data-ttu-id="88ebd-221">Ein einzelnes Wort oder ein kurzer Ausdruck sollten ausreichen.</span><span class="sxs-lookup"><span data-stu-id="88ebd-221">A single word or short phrase should suffice.</span></span>
-   <span data-ttu-id="88ebd-222">Verwenden Sie für Überschriften die Standardgroß- und kleinschreibung.</span><span class="sxs-lookup"><span data-stu-id="88ebd-222">Use sentence-style capitalization.</span></span>
-   <span data-ttu-id="88ebd-223">Verwenden Sie keine endinterpunktions Zeichen oder Ellipsen.</span><span class="sxs-lookup"><span data-stu-id="88ebd-223">Don't use ending punctuation or ellipsis.</span></span>

## <a name="documentation"></a><span data-ttu-id="88ebd-224">Dokumentation</span><span class="sxs-lookup"><span data-stu-id="88ebd-224">Documentation</span></span>

-   <span data-ttu-id="88ebd-225">Dieses Steuerelement wird als Suchfeld bezeichnet.</span><span class="sxs-lookup"><span data-stu-id="88ebd-225">Refer to this control as the Search box.</span></span> <span data-ttu-id="88ebd-226">Den ersten Buchstaben des ersten Worts groß schreiben; Schreiben Sie den ersten Buchstaben von Box nicht in Großbuchstaben.</span><span class="sxs-lookup"><span data-stu-id="88ebd-226">Capitalize the initial letter of the first word; don't capitalize the initial letter of box.</span></span>
-   <span data-ttu-id="88ebd-227">Weitere Informationen finden Sie in den beiden Such Typen als sofortige Suche und reguläre Suche.</span><span class="sxs-lookup"><span data-stu-id="88ebd-227">Refer to the two types of search as Instant search and regular search.</span></span> <span data-ttu-id="88ebd-228">Den anfänglichen Buchstaben der sofortigen Suche groß schreiben Schreiben Sie den ersten Buchstaben der regulären Suche nicht groß.</span><span class="sxs-lookup"><span data-stu-id="88ebd-228">Capitalize the initial letter of Instant search; don't capitalize the initial letter of regular search.</span></span>

## <a name="related-topics"></a><span data-ttu-id="88ebd-229">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="88ebd-229">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="88ebd-230">Glossar</span><span class="sxs-lookup"><span data-stu-id="88ebd-230">Glossary</span></span>](glossary.md)
</dt> </dl>

 

 