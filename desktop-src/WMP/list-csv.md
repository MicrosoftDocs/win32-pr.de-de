---
title: list.csv
description: list.csv
ms.assetid: 020b213c-826c-430c-8ce7-92b819581de8
keywords:
- Windows Media Player Online Stores list.csv
- Online Stores, list.csv
- Geben Sie 1 Online Stores, list.csv
- list.csv
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1f41ed237c5f4a185f01feace8f09b4615e4922b
ms.sourcegitcommit: 48d1c892045445bcbd0f22bafa2fd3861ffaa6e7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 02/19/2020
ms.locfileid: "104101238"
---
# <a name="listcsv"></a><span data-ttu-id="4c37f-107">list.csv</span><span class="sxs-lookup"><span data-stu-id="4c37f-107">list.csv</span></span>

<span data-ttu-id="4c37f-108">Diese Datei enthält einen Eintrag für jede der Listen, die im Katalog enthalten sind.</span><span class="sxs-lookup"><span data-stu-id="4c37f-108">This file contains an entry for each of the lists the catalog contains.</span></span> <span data-ttu-id="4c37f-109">Listen können Listen von Spuren, Alben, Künstlern, Genres, unter Genres oder Radio Feeds sein. oder Sie können Listen mit anderen Listen sein.</span><span class="sxs-lookup"><span data-stu-id="4c37f-109">Lists can be lists of tracks, albums, artists, genres, subgenres, or radio feeds; or they can be lists of other lists.</span></span> <span data-ttu-id="4c37f-110">Jeder Listeneintrag ist eine Zeile, die aus den durch Tabstopps getrennten Feldern besteht, die in der folgenden Tabelle beschrieben werden.</span><span class="sxs-lookup"><span data-stu-id="4c37f-110">Each list entry is a row composed of the tab-delimited fields described in the table below.</span></span> <span data-ttu-id="4c37f-111">Felder müssen in der aufgeführten Reihenfolge angezeigt werden.</span><span class="sxs-lookup"><span data-stu-id="4c37f-111">Fields must appear in the order listed.</span></span>

<span data-ttu-id="4c37f-112">In der Spalte Format in der folgenden Tabelle wird beschrieben, wie jedes Unicode-Textfeld formatiert wird.</span><span class="sxs-lookup"><span data-stu-id="4c37f-112">The Format column in the table below describes the way each Unicode text field is formatted.</span></span> <span data-ttu-id="4c37f-113">Er verweist nicht auf den Datentyp des Inhalts.</span><span class="sxs-lookup"><span data-stu-id="4c37f-113">It does not refer to the data type of the contents.</span></span> <span data-ttu-id="4c37f-114">Wenn beispielsweise eine ganze Zahl in der Spalte Format angegeben ist, bedeutet dies, dass das Feld eine Unicode-Zeichenfolge enthält, die einen ganzzahligen Wert anstelle einer tatsächlichen Ganzzahl darstellt.</span><span class="sxs-lookup"><span data-stu-id="4c37f-114">For example, if Integer is indicated in the Format column, it means that the field contains a Unicode string representing an integral value, rather than an actual integer.</span></span>



<table>
<colgroup>
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="4c37f-115">Feld</span><span class="sxs-lookup"><span data-stu-id="4c37f-115">Field</span></span></th>
<th><span data-ttu-id="4c37f-116">Erforderlich</span><span class="sxs-lookup"><span data-stu-id="4c37f-116">Required</span></span></th>
<th><span data-ttu-id="4c37f-117">Format</span><span class="sxs-lookup"><span data-stu-id="4c37f-117">Format</span></span></th>
<th><span data-ttu-id="4c37f-118">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="4c37f-118">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="4c37f-119">Listen</span><span class="sxs-lookup"><span data-stu-id="4c37f-119">ListID</span></span></td>
<td><span data-ttu-id="4c37f-120">Ja</span><span class="sxs-lookup"><span data-stu-id="4c37f-120">Yes</span></span></td>
<td><span data-ttu-id="4c37f-121">Nicht negative ganze Zahl.</span><span class="sxs-lookup"><span data-stu-id="4c37f-121">Non-negative integer.</span></span></td>
<td><span data-ttu-id="4c37f-122">Listen Bezeichner, der innerhalb list.csv eindeutig ist.</span><span class="sxs-lookup"><span data-stu-id="4c37f-122">List identifier, unique within list.csv.</span></span> <span data-ttu-id="4c37f-123">Muss nicht negativ und kleiner als 2 ^ 32 sein. <strong>Anzeigen eines Listen Knotens im Strukturansicht-Steuerelement:</strong> Wenn die ListId 0, 1, 2, 3, 4, 5, 6 oder 7 ist, wird die Liste in dem Strukturansicht-Steuerelement des Players als benutzerdefinierter Knoten unter dem Knoten der obersten Ebene des Online Stores angezeigt.</span><span class="sxs-lookup"><span data-stu-id="4c37f-123">Must be non-negative and less than 2^32.<strong>Displaying a list node in tree view control:</strong> If the ListID is 0, 1, 2, 3, 4, 5, 6, or 7, the list will appear as a custom node under your online store's top-level node in the Player's tree view control.</span></span> <span data-ttu-id="4c37f-124">Benutzerdefinierte Knoten werden vor den Standard Knoten unter dem Knoten der obersten Ebene des Online Stores angezeigt, und Sie werden in aufsteigender Reihenfolge nach ListId positioniert.</span><span class="sxs-lookup"><span data-stu-id="4c37f-124">Custom nodes appear before the standard nodes under the online store's top-level node, and they are positioned in ascending order by ListID.</span></span> <span data-ttu-id="4c37f-125">Wenn z. b. drei benutzerdefinierte Knoten mit den listids 1, 3 und 5 vorhanden sind, werden diese zuerst unter dem Knoten der obersten Ebene des Online Stores angezeigt.</span><span class="sxs-lookup"><span data-stu-id="4c37f-125">For example, if there are three custom nodes, with ListIDs of 1, 3, and 5, they will be displayed first, second, and third under the online store's top level node.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="4c37f-126">"Listen Titel</span><span class="sxs-lookup"><span data-stu-id="4c37f-126">ListTitle</span></span></td>
<td><span data-ttu-id="4c37f-127">Nein</span><span class="sxs-lookup"><span data-stu-id="4c37f-127">No</span></span></td>
<td><span data-ttu-id="4c37f-128">Unicode-Zeichenfolge. Beispiel: Top 10-Treffer</span><span class="sxs-lookup"><span data-stu-id="4c37f-128">Unicode string.Example: Top Ten Hits</span></span><br/></td>
<td><span data-ttu-id="4c37f-129">Listen Titel.</span><span class="sxs-lookup"><span data-stu-id="4c37f-129">List title.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="4c37f-130">Listtitel</span><span class="sxs-lookup"><span data-stu-id="4c37f-130">ListSubtitle</span></span></td>
<td><span data-ttu-id="4c37f-131">Nein</span><span class="sxs-lookup"><span data-stu-id="4c37f-131">No</span></span></td>
<td><span data-ttu-id="4c37f-132">Unicode-Zeichenfolge</span><span class="sxs-lookup"><span data-stu-id="4c37f-132">Unicode string</span></span></td>
<td><span data-ttu-id="4c37f-133">Listet einen alternativen Titel auf, der in der zweiten Zeile der Kachel Ansicht angezeigt wird.</span><span class="sxs-lookup"><span data-stu-id="4c37f-133">List alternate title, displayed in the second line of the Tile view.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="4c37f-134">Listdescription</span><span class="sxs-lookup"><span data-stu-id="4c37f-134">ListDescription</span></span></td>
<td><span data-ttu-id="4c37f-135">Ja</span><span class="sxs-lookup"><span data-stu-id="4c37f-135">Yes</span></span></td>
<td><span data-ttu-id="4c37f-136">Unicode-Zeichenfolge</span><span class="sxs-lookup"><span data-stu-id="4c37f-136">Unicode string</span></span></td>
<td><span data-ttu-id="4c37f-137">Listen Anzeige Text (wird in den Eigenschaften Seiten angezeigt).</span><span class="sxs-lookup"><span data-stu-id="4c37f-137">List friendly display text (displayed in property pages).</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="4c37f-138">Linked_ItemType</span><span class="sxs-lookup"><span data-stu-id="4c37f-138">Linked_ItemType</span></span></td>
<td><span data-ttu-id="4c37f-139">Ja</span><span class="sxs-lookup"><span data-stu-id="4c37f-139">Yes</span></span></td>
<td><span data-ttu-id="4c37f-140">Unicode-Zeichenfolge. Format: [T | P | A | L | G | S | R</span><span class="sxs-lookup"><span data-stu-id="4c37f-140">Unicode string.Format: [T|P|A|L|G|S|R]</span></span><br/> <span data-ttu-id="4c37f-141">Beispiel: T</span><span class="sxs-lookup"><span data-stu-id="4c37f-141">Example: T</span></span><br/></td>
<td><span data-ttu-id="4c37f-142">Gibt den Typ der verknüpften Elemente an.</span><span class="sxs-lookup"><span data-stu-id="4c37f-142">Indicates the type of the linked items.</span></span>
<ul>
<li><span data-ttu-id="4c37f-143">T = Nachverfolgung</span><span class="sxs-lookup"><span data-stu-id="4c37f-143">T= Track</span></span></li>
<li><span data-ttu-id="4c37f-144">P = Performer</span><span class="sxs-lookup"><span data-stu-id="4c37f-144">P = Performer</span></span></li>
<li><span data-ttu-id="4c37f-145">A = Album</span><span class="sxs-lookup"><span data-stu-id="4c37f-145">A = Album</span></span></li>
<li><span data-ttu-id="4c37f-146">L = Liste</span><span class="sxs-lookup"><span data-stu-id="4c37f-146">L = List</span></span></li>
<li><span data-ttu-id="4c37f-147">G = Genre</span><span class="sxs-lookup"><span data-stu-id="4c37f-147">G = Genre</span></span></li>
<li><span data-ttu-id="4c37f-148">S = Subgenre</span><span class="sxs-lookup"><span data-stu-id="4c37f-148">S = Subgenre</span></span></li>
<li><span data-ttu-id="4c37f-149">R = Radio</span><span class="sxs-lookup"><span data-stu-id="4c37f-149">R = Radio</span></span></li>
</ul></td>
</tr>
<tr class="even">
<td><span data-ttu-id="4c37f-150">ListPrice</span><span class="sxs-lookup"><span data-stu-id="4c37f-150">ListPrice</span></span></td>
<td><span data-ttu-id="4c37f-151">Ja</span><span class="sxs-lookup"><span data-stu-id="4c37f-151">Yes</span></span></td>
<td><span data-ttu-id="4c37f-152">Unicode-Zeichenfolge. Beispiel: $9,99</span><span class="sxs-lookup"><span data-stu-id="4c37f-152">Unicode string.Example: $9.99</span></span><br/></td>
<td><span data-ttu-id="4c37f-153">Der Preis der Liste.</span><span class="sxs-lookup"><span data-stu-id="4c37f-153">Price of the list.</span></span> <span data-ttu-id="4c37f-154">Das Währungssymbol sollte eingeschlossen werden. NULL bedeutet, dass die Liste kostenlos ist.</span><span class="sxs-lookup"><span data-stu-id="4c37f-154">The currency symbol should be included.A zero means the list is free.</span></span> <span data-ttu-id="4c37f-155">Kein Wert bedeutet, dass der Preis unbekannt ist.</span><span class="sxs-lookup"><span data-stu-id="4c37f-155">No value means the price is unknown.</span></span> <span data-ttu-id="4c37f-156">Ein Bindestrich bedeutet, dass die Liste nicht erworben werden kann.</span><span class="sxs-lookup"><span data-stu-id="4c37f-156">A hyphen means the list cannot be purchased.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="4c37f-157">Beliebtheit</span><span class="sxs-lookup"><span data-stu-id="4c37f-157">Popularity</span></span></td>
<td><span data-ttu-id="4c37f-158">Ja</span><span class="sxs-lookup"><span data-stu-id="4c37f-158">Yes</span></span></td>
<td><span data-ttu-id="4c37f-159">Eine Ganzzahl oder ein Dezimalwert. Beispiel: 1259,3</span><span class="sxs-lookup"><span data-stu-id="4c37f-159">Integer or decimal value.Example: 1259.3</span></span><br/></td>
<td><span data-ttu-id="4c37f-160">Gibt die rangfolgenrangfolge an, wenn diese Liste in anderen Listen angezeigt wird.</span><span class="sxs-lookup"><span data-stu-id="4c37f-160">Indicates the popularity ranking when this list appears in other lists.</span></span> <span data-ttu-id="4c37f-161">Kann NULL sein, wenn nicht zutreffend.</span><span class="sxs-lookup"><span data-stu-id="4c37f-161">Can be zero if not applicable..</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="4c37f-162">Isrecentlyadded</span><span class="sxs-lookup"><span data-stu-id="4c37f-162">IsRecentlyAdded</span></span></td>
<td><span data-ttu-id="4c37f-163">Ja</span><span class="sxs-lookup"><span data-stu-id="4c37f-163">Yes</span></span></td>
<td><span data-ttu-id="4c37f-164">Boolescher Wert. Format: [0 | 1]</span><span class="sxs-lookup"><span data-stu-id="4c37f-164">Boolean.Format: [0|1]</span></span><br/> <span data-ttu-id="4c37f-165">Beispiel: 0</span><span class="sxs-lookup"><span data-stu-id="4c37f-165">Example: 0</span></span><br/></td>
<td><span data-ttu-id="4c37f-166">Gibt an, ob die Liste kürzlich hinzugefügt wurde.</span><span class="sxs-lookup"><span data-stu-id="4c37f-166">Indicates whether the list was recently added.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="4c37f-167">Isfeatured</span><span class="sxs-lookup"><span data-stu-id="4c37f-167">IsFeatured</span></span></td>
<td><span data-ttu-id="4c37f-168">Ja</span><span class="sxs-lookup"><span data-stu-id="4c37f-168">Yes</span></span></td>
<td><span data-ttu-id="4c37f-169">Boolescher Wert. Format: [0 | 1]</span><span class="sxs-lookup"><span data-stu-id="4c37f-169">Boolean.Format: [0|1]</span></span><br/> <span data-ttu-id="4c37f-170">Beispiel: 0</span><span class="sxs-lookup"><span data-stu-id="4c37f-170">Example: 0</span></span><br/></td>
<td><span data-ttu-id="4c37f-171">Gibt an, ob die Liste angezeigt wird.</span><span class="sxs-lookup"><span data-stu-id="4c37f-171">Indicates whether the list is featured.</span></span> <span data-ttu-id="4c37f-172">Kann zum Bestimmen der Sortierreihenfolge verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="4c37f-172">Can be used in determining sort order.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="4c37f-173">Editorialglyph</span><span class="sxs-lookup"><span data-stu-id="4c37f-173">EditorialGlyph</span></span></td>
<td><span data-ttu-id="4c37f-174">Ja</span><span class="sxs-lookup"><span data-stu-id="4c37f-174">Yes</span></span></td>
<td><span data-ttu-id="4c37f-175">Nicht negative ganze Zahl.</span><span class="sxs-lookup"><span data-stu-id="4c37f-175">Non-negative integer.</span></span> <span data-ttu-id="4c37f-176">Muss 0 sein.</span><span class="sxs-lookup"><span data-stu-id="4c37f-176">Should be 0.</span></span></td>
<td><span data-ttu-id="4c37f-177">Wird in dieser Version nicht verwendet.</span><span class="sxs-lookup"><span data-stu-id="4c37f-177">Not used in this release.</span></span> <span data-ttu-id="4c37f-178">Muss 0 sein.</span><span class="sxs-lookup"><span data-stu-id="4c37f-178">Should be 0.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="4c37f-179">ViewType</span><span class="sxs-lookup"><span data-stu-id="4c37f-179">ViewType</span></span></td>
<td><span data-ttu-id="4c37f-180">Ja</span><span class="sxs-lookup"><span data-stu-id="4c37f-180">Yes</span></span></td>
<td><span data-ttu-id="4c37f-181">Unicode-Zeichenfolge.</span><span class="sxs-lookup"><span data-stu-id="4c37f-181">Unicode string.</span></span> <span data-ttu-id="4c37f-182">Format: [I | T | R | L | O] Beispiel: T</span><span class="sxs-lookup"><span data-stu-id="4c37f-182">Format: [I|T|R|L|O]Example: T</span></span><br/></td>
<td><span data-ttu-id="4c37f-183">Gibt den Ansichtstyp an, der für die Liste verwendet werden soll.</span><span class="sxs-lookup"><span data-stu-id="4c37f-183">Indicates the view type to use for the list.</span></span>
<ul>
<li><span data-ttu-id="4c37f-184">I = Symbol</span><span class="sxs-lookup"><span data-stu-id="4c37f-184">I = Icon</span></span></li>
<li><span data-ttu-id="4c37f-185">T = Kachel</span><span class="sxs-lookup"><span data-stu-id="4c37f-185">T = Tile</span></span></li>
<li><span data-ttu-id="4c37f-186">R = Bericht</span><span class="sxs-lookup"><span data-stu-id="4c37f-186">R = Report</span></span></li>
<li><span data-ttu-id="4c37f-187">L = Liste</span><span class="sxs-lookup"><span data-stu-id="4c37f-187">L = List</span></span></li>
<li><span data-ttu-id="4c37f-188">O = geordnete Liste</span><span class="sxs-lookup"><span data-stu-id="4c37f-188">O = Ordered List</span></span></li>
</ul></td>
</tr>
<tr class="even">
<td><span data-ttu-id="4c37f-189">Viewimagesize</span><span class="sxs-lookup"><span data-stu-id="4c37f-189">ViewImageSize</span></span></td>
<td><span data-ttu-id="4c37f-190">Ja</span><span class="sxs-lookup"><span data-stu-id="4c37f-190">Yes</span></span></td>
<td><span data-ttu-id="4c37f-191">Nicht negative ganze Zahl. Beispiel: 180</span><span class="sxs-lookup"><span data-stu-id="4c37f-191">Non-negative integer.Example: 180</span></span><br/></td>
<td><span data-ttu-id="4c37f-192">Die Größe, in der das Listen Bild angezeigt wird.</span><span class="sxs-lookup"><span data-stu-id="4c37f-192">The size at which the list image is displayed.</span></span> <span data-ttu-id="4c37f-193">Wenn der Wert 0 ist, wird die Größe automatisch bestimmt.</span><span class="sxs-lookup"><span data-stu-id="4c37f-193">If 0, size is determined automatically.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="4c37f-194">GroupBy</span><span class="sxs-lookup"><span data-stu-id="4c37f-194">GroupBy</span></span></td>
<td><span data-ttu-id="4c37f-195">Ja</span><span class="sxs-lookup"><span data-stu-id="4c37f-195">Yes</span></span></td>
<td><span data-ttu-id="4c37f-196">Unicode-Zeichenfolge. Format: [-| P | A | C | R | D</span><span class="sxs-lookup"><span data-stu-id="4c37f-196">Unicode string.Format: [-|P|A|C|R|D]</span></span><br/> <span data-ttu-id="4c37f-197">Beispiel: P</span><span class="sxs-lookup"><span data-stu-id="4c37f-197">Example: P</span></span><br/></td>
<td><span data-ttu-id="4c37f-198">Gibt an, welches Feld zum Gruppieren der Elemente in der Liste verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="4c37f-198">Indicates what field is used to group the items in the list.</span></span>
<ul>
<li><span data-ttu-id="4c37f-199">- = Automatisch</span><span class="sxs-lookup"><span data-stu-id="4c37f-199">- = Automatic</span></span></li>
<li><span data-ttu-id="4c37f-200">P = Performer</span><span class="sxs-lookup"><span data-stu-id="4c37f-200">P = Performer</span></span></li>
<li><span data-ttu-id="4c37f-201">A = Album</span><span class="sxs-lookup"><span data-stu-id="4c37f-201">A = Album</span></span></li>
<li><span data-ttu-id="4c37f-202">C = Composer</span><span class="sxs-lookup"><span data-stu-id="4c37f-202">C = Composer</span></span></li>
<li><span data-ttu-id="4c37f-203">R = Bewertung</span><span class="sxs-lookup"><span data-stu-id="4c37f-203">R = Rating</span></span></li>
<li><span data-ttu-id="4c37f-204">D = Datum</span><span class="sxs-lookup"><span data-stu-id="4c37f-204">D = Date</span></span></li>
</ul></td>
</tr>
<tr class="even">
<td><span data-ttu-id="4c37f-205">Listitemsaredynamic</span><span class="sxs-lookup"><span data-stu-id="4c37f-205">ListItemsAreDynamic</span></span></td>
<td><span data-ttu-id="4c37f-206">Ja</span><span class="sxs-lookup"><span data-stu-id="4c37f-206">Yes</span></span></td>
<td><span data-ttu-id="4c37f-207">Boolesch.</span><span class="sxs-lookup"><span data-stu-id="4c37f-207">Boolean.</span></span> <span data-ttu-id="4c37f-208">Kann 0 oder 1 sein.</span><span class="sxs-lookup"><span data-stu-id="4c37f-208">Can be 0 or 1.</span></span></td>
<td><span data-ttu-id="4c37f-209">Gibt an, ob die Liste dynamisch generiert wird.</span><span class="sxs-lookup"><span data-stu-id="4c37f-209">Indicates whether the list is generated dynamically.</span></span> <span data-ttu-id="4c37f-210">Dynamische Listen enthalten keine Elemente in listitem.csv.</span><span class="sxs-lookup"><span data-stu-id="4c37f-210">Dynamic lists do not have items in listitem.csv.</span></span> <span data-ttu-id="4c37f-211">Wenn eine Liste als dynamisch markiert ist, werden die zugehörigen Elemente von <a href="/previous-versions/windows/desktop/api/contentpartner/nf-contentpartner-iwmpcontentpartner-getlistcontents">iwmpcontentpartner:: getlistcontents</a> bereitgestellt.</span><span class="sxs-lookup"><span data-stu-id="4c37f-211">If a list is marked as dynamic, its items are provided by <a href="/previous-versions/windows/desktop/api/contentpartner/nf-contentpartner-iwmpcontentpartner-getlistcontents">IWMPContentPartner::GetListContents</a></span></span></td>
</tr>
</tbody>
</table>



 

 

 





