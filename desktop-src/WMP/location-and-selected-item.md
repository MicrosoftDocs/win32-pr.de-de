---
title: Speicherort und ausgewähltes Element
description: Speicherort und ausgewähltes Element
ms.assetid: 9556e01f-1f75-4089-9e62-b41a9aa53e93
keywords:
- Windows Media Player Online Stores, Standorte
- Online Stores, Standorte
- Typ 1 Online Stores, Standorte
- Windows Media Player Online Stores, Bibliotheks Standorte
- Online Stores, Bibliotheks Standorte
- Typ 1 Online Stores, Bibliotheks Standorte
- Windows Media Player Online Stores, ausgewählte Elemente
- Online Stores, ausgewählte Elemente
- Typ 1 Online Stores, ausgewählte Elemente
- Windows Media Player-Bibliothek, Standorte
- Windows Media Player-Bibliothek, ausgewählte Elemente
- Bibliothek, Standorte
- Bibliothek, ausgewählte Elemente
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d665b11e7509e369224d3e85db30dddb4a988a14
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "104206672"
---
# <a name="location-and-selected-item"></a><span data-ttu-id="e7c1d-116">Speicherort und ausgewähltes Element</span><span class="sxs-lookup"><span data-stu-id="e7c1d-116">Location and Selected Item</span></span>

<span data-ttu-id="e7c1d-117">In Windows Media Player werden die folgenden fünf Elemente verwendet, um die aktuelle Ansicht des Online Store-Inhalts zu bezeichnen:</span><span class="sxs-lookup"><span data-stu-id="e7c1d-117">Windows Media Player uses the following five items to characterize its current view of online store content:</span></span>

-   <span data-ttu-id="e7c1d-118">task</span><span class="sxs-lookup"><span data-stu-id="e7c1d-118">task</span></span>
-   <span data-ttu-id="e7c1d-119">bibliothekationstyp</span><span class="sxs-lookup"><span data-stu-id="e7c1d-119">library location type</span></span>
-   <span data-ttu-id="e7c1d-120">Bibliotheks Speicherort-ID</span><span class="sxs-lookup"><span data-stu-id="e7c1d-120">library location ID</span></span>
-   <span data-ttu-id="e7c1d-121">Typ des ausgewählten Elements</span><span class="sxs-lookup"><span data-stu-id="e7c1d-121">selected item type</span></span>
-   <span data-ttu-id="e7c1d-122">ID des ausgewählten Elements</span><span class="sxs-lookup"><span data-stu-id="e7c1d-122">selected item ID</span></span>

<span data-ttu-id="e7c1d-123">In der Regel können Sie sich die Ansicht in Windows Media Player als Container von Elementen vorstellen.</span><span class="sxs-lookup"><span data-stu-id="e7c1d-123">Typically, you can think of the view in Windows Media Player as a container of items.</span></span> <span data-ttu-id="e7c1d-124">Der Container weist einen Typ auf, und ein Element weist einen Typ auf.</span><span class="sxs-lookup"><span data-stu-id="e7c1d-124">The container has a type, and an item has a type.</span></span> <span data-ttu-id="e7c1d-125">Alle Elemente in einem Container haben denselben Typ.</span><span class="sxs-lookup"><span data-stu-id="e7c1d-125">All the items in a container have the same type.</span></span> <span data-ttu-id="e7c1d-126">Location-und Elementtypen werden von den [Bibliotheks Speicherort Konstanten](library-location-constants.md)angegeben.</span><span class="sxs-lookup"><span data-stu-id="e7c1d-126">Location types and item types are both specified by the [library location constants](library-location-constants.md).</span></span> <span data-ttu-id="e7c1d-127">Wenn die aktuelle Ansicht z. b. ein einzelnes Album anzeigt, ist der Speicherort der Bibliothek cpalbumid, und da ein Album nachverfolgt, ist der ausgewählte Elementtyp cptrackid.</span><span class="sxs-lookup"><span data-stu-id="e7c1d-127">For example, if the current view is showing an individual album, the library location type is CPAlbumID, and, because an album contains tracks, the selected item type is CPTrackID.</span></span>

<span data-ttu-id="e7c1d-128">In der folgenden Tabelle sind die Speicherort-und Elementtypen für mehrere Container aufgeführt.</span><span class="sxs-lookup"><span data-stu-id="e7c1d-128">The following table shows the location and item types for several containers.</span></span>



| <span data-ttu-id="e7c1d-129">Beschreibung des Containers</span><span class="sxs-lookup"><span data-stu-id="e7c1d-129">Description of container</span></span>                              | <span data-ttu-id="e7c1d-130">Bibliothekationstyp</span><span class="sxs-lookup"><span data-stu-id="e7c1d-130">Library location type</span></span> | <span data-ttu-id="e7c1d-131">Typ des ausgewählten Elements</span><span class="sxs-lookup"><span data-stu-id="e7c1d-131">Selected item type</span></span> |
|-------------------------------------------------------|-----------------------|--------------------|
| <span data-ttu-id="e7c1d-132">Ein Album, das ein Container von Spuren ist.</span><span class="sxs-lookup"><span data-stu-id="e7c1d-132">An album that is a container of tracks</span></span>                | <span data-ttu-id="e7c1d-133">Cpalbumid</span><span class="sxs-lookup"><span data-stu-id="e7c1d-133">CPAlbumID</span></span>             | <span data-ttu-id="e7c1d-134">Cptrackid</span><span class="sxs-lookup"><span data-stu-id="e7c1d-134">CPTrackID</span></span>          |
| <span data-ttu-id="e7c1d-135">Eine Liste, die ein Container von Spuren ist.</span><span class="sxs-lookup"><span data-stu-id="e7c1d-135">A list that is a container of tracks</span></span>                  | <span data-ttu-id="e7c1d-136">Cplistid</span><span class="sxs-lookup"><span data-stu-id="e7c1d-136">CPListID</span></span>              | <span data-ttu-id="e7c1d-137">Cptrackid</span><span class="sxs-lookup"><span data-stu-id="e7c1d-137">CPTrackID</span></span>          |
| <span data-ttu-id="e7c1d-138">Eine Liste, die ein Container von Alben ist.</span><span class="sxs-lookup"><span data-stu-id="e7c1d-138">A list that is a container of albums</span></span>                  | <span data-ttu-id="e7c1d-139">Cplistid</span><span class="sxs-lookup"><span data-stu-id="e7c1d-139">CPListID</span></span>              | <span data-ttu-id="e7c1d-140">Cpalbumid</span><span class="sxs-lookup"><span data-stu-id="e7c1d-140">CPAlbumID</span></span>          |
| <span data-ttu-id="e7c1d-141">Eine Radio Station, bei der es sich um einen Container von Listen handelt</span><span class="sxs-lookup"><span data-stu-id="e7c1d-141">A radio station that is a container of lists</span></span>          | <span data-ttu-id="e7c1d-142">Cpradioid</span><span class="sxs-lookup"><span data-stu-id="e7c1d-142">CPRadioID</span></span>             | <span data-ttu-id="e7c1d-143">Cplistid</span><span class="sxs-lookup"><span data-stu-id="e7c1d-143">CPListID</span></span>           |
| <span data-ttu-id="e7c1d-144">Der Satz aller Alben, bei dem es sich um einen Container von Alben handelt</span><span class="sxs-lookup"><span data-stu-id="e7c1d-144">The set of all albums, which is a container of albums</span></span> | <span data-ttu-id="e7c1d-145">Allcpalbumids</span><span class="sxs-lookup"><span data-stu-id="e7c1d-145">AllCPAlbumIDs</span></span>         | <span data-ttu-id="e7c1d-146">Cpalbumid</span><span class="sxs-lookup"><span data-stu-id="e7c1d-146">CPAlbumID</span></span>          |
| <span data-ttu-id="e7c1d-147">Der Satz aller Genres, bei dem es sich um einen Container von Genres handelt.</span><span class="sxs-lookup"><span data-stu-id="e7c1d-147">The set of all genres, which is a container of genres</span></span> | <span data-ttu-id="e7c1d-148">Allcpgenreids</span><span class="sxs-lookup"><span data-stu-id="e7c1d-148">AllCPGenreIDs</span></span>         | <span data-ttu-id="e7c1d-149">Cpgenreid</span><span class="sxs-lookup"><span data-stu-id="e7c1d-149">CPGenreID</span></span>          |



 

<span data-ttu-id="e7c1d-150">Die Registerkarten in Windows Media Player die verschiedene Aufgaben darstellen.</span><span class="sxs-lookup"><span data-stu-id="e7c1d-150">The tabs in Windows Media Player represent different tasks.</span></span> <span data-ttu-id="e7c1d-151">Der Player zeigt Online Store-Inhalte in drei verschiedenen Aufgabenbereichen an: **Bibliothek**, **Brennen** und **Synchronisierung**. Der Aufgabenbereich Bibliothek wird auch als Aufgabenbereich **Durchsuchen** bezeichnet.</span><span class="sxs-lookup"><span data-stu-id="e7c1d-151">The Player displays online store content in three different task panes: **Library**, **Burn**, and **Sync**. The Library task pane is also called the **Browse** task pane.</span></span> <span data-ttu-id="e7c1d-152">Manchmal wird ein Aufgabenbereich als *Feature* bezeichnet, sodass Sie in dieser Dokumentation Begriffe wie " *Burn Feature* " und " *Sync Feature* " sehen können.</span><span class="sxs-lookup"><span data-stu-id="e7c1d-152">Sometimes, a task pane is called a *feature*, so you might see terms like *Burn feature* and *Sync feature* in this documentation.</span></span>

<span data-ttu-id="e7c1d-153">In den folgenden Beispielen wird veranschaulicht, wie Windows Media Player die fünf Informationen verwendet (Task, bibliothekationsort, Bibliotheks Speicherort-ID, ausgewählter Elementtyp, ausgewählte Element-ID), um unterschiedliche Ansichten zu bezeichnen.</span><span class="sxs-lookup"><span data-stu-id="e7c1d-153">The following examples show how Windows Media Player uses the five pieces of information (task, library location type, library location ID, selected item type, selected Item ID) to characterize different views.</span></span>

<span data-ttu-id="e7c1d-154">Im Aufgabenbereich " **Burn** " zeigt der Spieler ein Album als Container für Titel an.</span><span class="sxs-lookup"><span data-stu-id="e7c1d-154">In the **Burn** task pane, the Player is displaying an album as a container of tracks.</span></span> <span data-ttu-id="e7c1d-155">Das Album weist die ID 250 auf.</span><span class="sxs-lookup"><span data-stu-id="e7c1d-155">The album has an ID of 250.</span></span> <span data-ttu-id="e7c1d-156">In der Ansicht ist das ausgewählte Element der Titel mit der ID 800.</span><span class="sxs-lookup"><span data-stu-id="e7c1d-156">In the view, the selected item is the track that has an ID of 800.</span></span> <span data-ttu-id="e7c1d-157">Beachten Sie, dass 800 die ID des Titels im Katalog des Online Stores ist, nicht die Nummer des Titels im Album.</span><span class="sxs-lookup"><span data-stu-id="e7c1d-157">Note that 800 is the ID of the track in the online store's catalog, not the number of the track on the album.</span></span>



| <span data-ttu-id="e7c1d-158">Element</span><span class="sxs-lookup"><span data-stu-id="e7c1d-158">Item</span></span>                  | <span data-ttu-id="e7c1d-159">Wert</span><span class="sxs-lookup"><span data-stu-id="e7c1d-159">Value</span></span>     |
|-----------------------|-----------|
| <span data-ttu-id="e7c1d-160">task</span><span class="sxs-lookup"><span data-stu-id="e7c1d-160">task</span></span>                  | <span data-ttu-id="e7c1d-161">Brenn</span><span class="sxs-lookup"><span data-stu-id="e7c1d-161">Burn</span></span>      |
| <span data-ttu-id="e7c1d-162">bibliothekationstyp</span><span class="sxs-lookup"><span data-stu-id="e7c1d-162">library location type</span></span> | <span data-ttu-id="e7c1d-163">Cpalbumid</span><span class="sxs-lookup"><span data-stu-id="e7c1d-163">CPAlbumID</span></span> |
| <span data-ttu-id="e7c1d-164">Bibliotheks Speicherort-ID</span><span class="sxs-lookup"><span data-stu-id="e7c1d-164">library location ID</span></span>   | <span data-ttu-id="e7c1d-165">250</span><span class="sxs-lookup"><span data-stu-id="e7c1d-165">250</span></span>       |
| <span data-ttu-id="e7c1d-166">Typ des ausgewählten Elements</span><span class="sxs-lookup"><span data-stu-id="e7c1d-166">selected item type</span></span>    | <span data-ttu-id="e7c1d-167">Cptrackid</span><span class="sxs-lookup"><span data-stu-id="e7c1d-167">CPTrackID</span></span> |
| <span data-ttu-id="e7c1d-168">ID des ausgewählten Elements</span><span class="sxs-lookup"><span data-stu-id="e7c1d-168">selected item ID</span></span>      | <span data-ttu-id="e7c1d-169">800</span><span class="sxs-lookup"><span data-stu-id="e7c1d-169">800</span></span>       |



 

<span data-ttu-id="e7c1d-170">Im Aufgabenbereich **Synchronisieren** zeigt der Player den Satz aller Alben an, bei dem es sich um einen Container von Alben handelt.</span><span class="sxs-lookup"><span data-stu-id="e7c1d-170">In the **Sync** task pane, the Player is displaying the set of all albums, which is a container of albums.</span></span> <span data-ttu-id="e7c1d-171">Das ausgewählte Element in der Ansicht ist das Album mit der ID 300.</span><span class="sxs-lookup"><span data-stu-id="e7c1d-171">In the view, the selected item is the album that has an ID of 300.</span></span> <span data-ttu-id="e7c1d-172">Beachten Sie, dass die Bibliotheks Speicherort-ID für diese Sicht nicht anwendbar ist.</span><span class="sxs-lookup"><span data-stu-id="e7c1d-172">Note that the library location ID is not applicable to this view.</span></span>



| <span data-ttu-id="e7c1d-173">Element</span><span class="sxs-lookup"><span data-stu-id="e7c1d-173">Item</span></span>                  | <span data-ttu-id="e7c1d-174">Wert</span><span class="sxs-lookup"><span data-stu-id="e7c1d-174">Value</span></span>         |
|-----------------------|---------------|
| <span data-ttu-id="e7c1d-175">task</span><span class="sxs-lookup"><span data-stu-id="e7c1d-175">task</span></span>                  | <span data-ttu-id="e7c1d-176">Synchronisierung</span><span class="sxs-lookup"><span data-stu-id="e7c1d-176">Sync</span></span>          |
| <span data-ttu-id="e7c1d-177">bibliothekationstyp</span><span class="sxs-lookup"><span data-stu-id="e7c1d-177">library location type</span></span> | <span data-ttu-id="e7c1d-178">Allcpalbumids</span><span class="sxs-lookup"><span data-stu-id="e7c1d-178">AllCPAlbumIDs</span></span> |
| <span data-ttu-id="e7c1d-179">Bibliotheks Speicherort-ID</span><span class="sxs-lookup"><span data-stu-id="e7c1d-179">library location ID</span></span>   | <span data-ttu-id="e7c1d-180">–</span><span class="sxs-lookup"><span data-stu-id="e7c1d-180">N/A</span></span>           |
| <span data-ttu-id="e7c1d-181">Typ des ausgewählten Elements</span><span class="sxs-lookup"><span data-stu-id="e7c1d-181">selected item type</span></span>    | <span data-ttu-id="e7c1d-182">Cpalbumid</span><span class="sxs-lookup"><span data-stu-id="e7c1d-182">CPAlbumID</span></span>     |
| <span data-ttu-id="e7c1d-183">ID des ausgewählten Elements</span><span class="sxs-lookup"><span data-stu-id="e7c1d-183">selected item ID</span></span>      | <span data-ttu-id="e7c1d-184">300</span><span class="sxs-lookup"><span data-stu-id="e7c1d-184">300</span></span>           |



 

<span data-ttu-id="e7c1d-185">Im Strukturansicht-Steuerelement ist der Stamm Knoten für den Online Store ausgewählt.</span><span class="sxs-lookup"><span data-stu-id="e7c1d-185">In the tree-view control, the root node for the online store is selected.</span></span> <span data-ttu-id="e7c1d-186">In diesem Fall gibt es keinen Container, und folglich gibt es keine Elemente.</span><span class="sxs-lookup"><span data-stu-id="e7c1d-186">In this case, there is no container, and consequently, there are no items.</span></span> <span data-ttu-id="e7c1d-187">Im Aufgabenbereich gesamte **Bibliothek** wird eine Ermittlungs Seite angezeigt.</span><span class="sxs-lookup"><span data-stu-id="e7c1d-187">The entire **Library** task pane is displaying a discovery page.</span></span>



| <span data-ttu-id="e7c1d-188">Element</span><span class="sxs-lookup"><span data-stu-id="e7c1d-188">Item</span></span>                  | <span data-ttu-id="e7c1d-189">Wert</span><span class="sxs-lookup"><span data-stu-id="e7c1d-189">Value</span></span>           |
|-----------------------|-----------------|
| <span data-ttu-id="e7c1d-190">task</span><span class="sxs-lookup"><span data-stu-id="e7c1d-190">task</span></span>                  | <span data-ttu-id="e7c1d-191">Durchsuchen</span><span class="sxs-lookup"><span data-stu-id="e7c1d-191">Browse</span></span>          |
| <span data-ttu-id="e7c1d-192">bibliothekationstyp</span><span class="sxs-lookup"><span data-stu-id="e7c1d-192">library location type</span></span> | <span data-ttu-id="e7c1d-193">Rootlocation</span><span class="sxs-lookup"><span data-stu-id="e7c1d-193">RootLocation</span></span>    |
| <span data-ttu-id="e7c1d-194">Bibliotheks Speicherort-ID</span><span class="sxs-lookup"><span data-stu-id="e7c1d-194">library location ID</span></span>   | <span data-ttu-id="e7c1d-195">–</span><span class="sxs-lookup"><span data-stu-id="e7c1d-195">N/A</span></span>             |
| <span data-ttu-id="e7c1d-196">Typ des ausgewählten Elements</span><span class="sxs-lookup"><span data-stu-id="e7c1d-196">selected item type</span></span>    | <span data-ttu-id="e7c1d-197">Unknownlocation</span><span class="sxs-lookup"><span data-stu-id="e7c1d-197">UnknownLocation</span></span> |
| <span data-ttu-id="e7c1d-198">ID des ausgewählten Elements</span><span class="sxs-lookup"><span data-stu-id="e7c1d-198">selected item ID</span></span>      | <span data-ttu-id="e7c1d-199">–</span><span class="sxs-lookup"><span data-stu-id="e7c1d-199">N/A</span></span>             |



 

<span data-ttu-id="e7c1d-200">Im Aufgabenbereich **Synchronisieren** zeigt der Spieler das Jahr 2002 als Container für Titel an.</span><span class="sxs-lookup"><span data-stu-id="e7c1d-200">In the **Sync** task pane, the Player is displaying the year 2002 as a container of tracks.</span></span> <span data-ttu-id="e7c1d-201">In der Ansicht ist das ausgewählte Element der Titel mit der ID 450.</span><span class="sxs-lookup"><span data-stu-id="e7c1d-201">In the view, the selected item is the track that has an ID of 450.</span></span>



| <span data-ttu-id="e7c1d-202">Element</span><span class="sxs-lookup"><span data-stu-id="e7c1d-202">Item</span></span>                  | <span data-ttu-id="e7c1d-203">Wert</span><span class="sxs-lookup"><span data-stu-id="e7c1d-203">Value</span></span>           |
|-----------------------|-----------------|
| <span data-ttu-id="e7c1d-204">task</span><span class="sxs-lookup"><span data-stu-id="e7c1d-204">task</span></span>                  | <span data-ttu-id="e7c1d-205">Synchronisierung</span><span class="sxs-lookup"><span data-stu-id="e7c1d-205">Sync</span></span>            |
| <span data-ttu-id="e7c1d-206">bibliothekationstyp</span><span class="sxs-lookup"><span data-stu-id="e7c1d-206">library location type</span></span> | <span data-ttu-id="e7c1d-207">Releasedateyear</span><span class="sxs-lookup"><span data-stu-id="e7c1d-207">ReleaseDateYear</span></span> |
| <span data-ttu-id="e7c1d-208">Bibliotheks Speicherort-ID</span><span class="sxs-lookup"><span data-stu-id="e7c1d-208">library location ID</span></span>   | <span data-ttu-id="e7c1d-209">2002</span><span class="sxs-lookup"><span data-stu-id="e7c1d-209">2002</span></span>            |
| <span data-ttu-id="e7c1d-210">Typ des ausgewählten Elements</span><span class="sxs-lookup"><span data-stu-id="e7c1d-210">selected item type</span></span>    | <span data-ttu-id="e7c1d-211">Cptrackid</span><span class="sxs-lookup"><span data-stu-id="e7c1d-211">CPTrackID</span></span>       |
| <span data-ttu-id="e7c1d-212">ID des ausgewählten Elements</span><span class="sxs-lookup"><span data-stu-id="e7c1d-212">selected item ID</span></span>      | <span data-ttu-id="e7c1d-213">450</span><span class="sxs-lookup"><span data-stu-id="e7c1d-213">450</span></span>             |



 

## <a name="related-topics"></a><span data-ttu-id="e7c1d-214">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="e7c1d-214">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="e7c1d-215">**Informationen zu Typ 1 Online Stores**</span><span class="sxs-lookup"><span data-stu-id="e7c1d-215">**About Type 1 Online Stores**</span></span>](about-type-1-online-stores.md)
</dt> <dt>

[<span data-ttu-id="e7c1d-216">**Ermittlungs Seiten**</span><span class="sxs-lookup"><span data-stu-id="e7c1d-216">**Discovery Pages**</span></span>](discovery-pages.md)
</dt> </dl>

 

 




