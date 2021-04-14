---
title: track.csv
description: track.csv
ms.assetid: 5ce782b7-5fb8-4e6e-80cb-fa1dd7c47716
keywords:
- Windows Media Player Online Stores track.csv
- Online Stores, track.csv
- Geben Sie 1 Online Stores, track.csv
- track.csv
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9826dbcc7b553caba89b2288057b643cdb0712bf
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "104310371"
---
# <a name="trackcsv"></a><span data-ttu-id="90401-107">track.csv</span><span class="sxs-lookup"><span data-stu-id="90401-107">track.csv</span></span>

<span data-ttu-id="90401-108">Diese Datei enthält einen Eintrag für jede Spur im Katalog.</span><span class="sxs-lookup"><span data-stu-id="90401-108">This file contains an entry for each track in the catalog.</span></span> <span data-ttu-id="90401-109">Jeder Eintrag ist eine Zeile, die aus den durch Tabstopps getrennten Feldern besteht, die in der folgenden Tabelle beschrieben werden.</span><span class="sxs-lookup"><span data-stu-id="90401-109">Each entry is a row composed of the tab-delimited fields described in the table below.</span></span> <span data-ttu-id="90401-110">Felder müssen in der aufgeführten Reihenfolge angezeigt werden.</span><span class="sxs-lookup"><span data-stu-id="90401-110">Fields must appear in the order listed.</span></span>

<span data-ttu-id="90401-111">In der Spalte Format in der folgenden Tabelle wird beschrieben, wie jedes Unicode-Textfeld formatiert wird.</span><span class="sxs-lookup"><span data-stu-id="90401-111">The Format column in the table below describes the way each Unicode text field is formatted.</span></span> <span data-ttu-id="90401-112">Er verweist nicht auf den Datentyp des Inhalts.</span><span class="sxs-lookup"><span data-stu-id="90401-112">It does not refer to the data type of the contents.</span></span> <span data-ttu-id="90401-113">Wenn beispielsweise eine ganze Zahl in der Spalte Format angegeben ist, bedeutet dies, dass das Feld eine Unicode-Zeichenfolge enthält, die einen ganzzahligen Wert anstelle einer tatsächlichen Ganzzahl darstellt.</span><span class="sxs-lookup"><span data-stu-id="90401-113">For example, if Integer is indicated in the Format column, it means that the field contains a Unicode string representing an integral value, rather than an actual integer.</span></span>



<table>
<colgroup>
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="90401-114">Feld</span><span class="sxs-lookup"><span data-stu-id="90401-114">Field</span></span></th>
<th><span data-ttu-id="90401-115">Erforderlich</span><span class="sxs-lookup"><span data-stu-id="90401-115">Required</span></span></th>
<th><span data-ttu-id="90401-116">Format</span><span class="sxs-lookup"><span data-stu-id="90401-116">Format</span></span></th>
<th><span data-ttu-id="90401-117">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="90401-117">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="90401-118">TrackID</span><span class="sxs-lookup"><span data-stu-id="90401-118">TrackID</span></span></td>
<td><span data-ttu-id="90401-119">Ja</span><span class="sxs-lookup"><span data-stu-id="90401-119">Yes</span></span></td>
<td><span data-ttu-id="90401-120">Nicht negative ganze Zahl. Beispiel: 32789</span><span class="sxs-lookup"><span data-stu-id="90401-120">Non-negative integer.Example: 32789</span></span><br/></td>
<td><span data-ttu-id="90401-121">Vom Inhaltsanbieter bereitgestellter eindeutiger Bezeichner.</span><span class="sxs-lookup"><span data-stu-id="90401-121">Unique identifier provided by the content provider.</span></span> <span data-ttu-id="90401-122">Muss kleiner als 2 ^ 32 sein. Leistungs Tipp: Wenn die IDs, die den Spuren desselben Albums zugewiesen sind, nacheinander nummeriert werden, ist die Katalog Komprimierung effizienter.</span><span class="sxs-lookup"><span data-stu-id="90401-122">Must be less than 2^32.Performance tip: If the IDs assigned to tracks from the same album are numbered consecutively, catalog compression will be more efficient.</span></span> <span data-ttu-id="90401-123">Die aufeinanderfolgende Nummerierung von Albumtiteln ist jedoch nicht erforderlich.</span><span class="sxs-lookup"><span data-stu-id="90401-123">However, consecutive numbering of album tracks is not required.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="90401-124">Tracktitle</span><span class="sxs-lookup"><span data-stu-id="90401-124">TrackTitle</span></span></td>
<td><span data-ttu-id="90401-125">Ja</span><span class="sxs-lookup"><span data-stu-id="90401-125">Yes</span></span></td>
<td><span data-ttu-id="90401-126">Unicode-Zeichenfolge.</span><span class="sxs-lookup"><span data-stu-id="90401-126">Unicode string.</span></span> <span data-ttu-id="90401-127">Beispiel: Raygun Räuber ' Blues</span><span class="sxs-lookup"><span data-stu-id="90401-127">Example: Raygun Robbers' Blues</span></span></td>
<td><span data-ttu-id="90401-128">Name der Spur</span><span class="sxs-lookup"><span data-stu-id="90401-128">Name of the track.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="90401-129">Duration</span><span class="sxs-lookup"><span data-stu-id="90401-129">Duration</span></span></td>
<td><span data-ttu-id="90401-130">Ja</span><span class="sxs-lookup"><span data-stu-id="90401-130">Yes</span></span></td>
<td><span data-ttu-id="90401-131">Nicht negative ganze Zahl. Beispiel: 543</span><span class="sxs-lookup"><span data-stu-id="90401-131">Non-negative integer.Example: 543</span></span><br/></td>
<td><span data-ttu-id="90401-132">Dauer der Spur in Sekunden.</span><span class="sxs-lookup"><span data-stu-id="90401-132">Duration of the track in seconds.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="90401-133">Tracknumber</span><span class="sxs-lookup"><span data-stu-id="90401-133">TrackNumber</span></span></td>
<td><span data-ttu-id="90401-134">Ja</span><span class="sxs-lookup"><span data-stu-id="90401-134">Yes</span></span></td>
<td><span data-ttu-id="90401-135">Nicht negative ganze Zahl. Beispiel: 7</span><span class="sxs-lookup"><span data-stu-id="90401-135">Non-negative integer.Example: 7</span></span><br/></td>
<td><span data-ttu-id="90401-136">Verfolgen Sie die Nummer im Titel des Titels.</span><span class="sxs-lookup"><span data-stu-id="90401-136">Track number on the track's album.</span></span> <span data-ttu-id="90401-137">Nachverfolgen von Zahlen beginnen bei 1 und erhöhen die Anzahl von Festplatten Sätzen.</span><span class="sxs-lookup"><span data-stu-id="90401-137">Track numbers begin at 1 and increase across disc sets.</span></span> <span data-ttu-id="90401-138">Die Nachverfolgung muss kleiner als 256 sein.</span><span class="sxs-lookup"><span data-stu-id="90401-138">The track number must be less than 256.</span></span> <span data-ttu-id="90401-139">Eine Nachverfolgung, die größer oder gleich 256 ist, führt zu unerwartetem Verhalten in Windows Media Player.</span><span class="sxs-lookup"><span data-stu-id="90401-139">A track number greater than or equal to 256 will cause unexpected behavior in Windows Media Player.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="90401-140">Trackprice</span><span class="sxs-lookup"><span data-stu-id="90401-140">TrackPrice</span></span></td>
<td><span data-ttu-id="90401-141">Ja</span><span class="sxs-lookup"><span data-stu-id="90401-141">Yes</span></span></td>
<td><span data-ttu-id="90401-142">Unicode-Zeichenfolge.</span><span class="sxs-lookup"><span data-stu-id="90401-142">Unicode string.</span></span> <span data-ttu-id="90401-143">Beispiel: $0,99.</span><span class="sxs-lookup"><span data-stu-id="90401-143">Example: $0.99.</span></span></td>
<td><span data-ttu-id="90401-144">Preis nachverfolgen.</span><span class="sxs-lookup"><span data-stu-id="90401-144">Track price.</span></span> <span data-ttu-id="90401-145">Das Währungssymbol sollte eingeschlossen werden.</span><span class="sxs-lookup"><span data-stu-id="90401-145">The currency symbol should be included.</span></span> <span data-ttu-id="90401-146">Die leere Zeichenfolge 0 und-haben eine besondere Bedeutung.</span><span class="sxs-lookup"><span data-stu-id="90401-146">The empty string, 0, and - have special meaning.</span></span> <span data-ttu-id="90401-147">Eine leere Zeichenfolge gibt an, dass der Preis unbekannt ist.</span><span class="sxs-lookup"><span data-stu-id="90401-147">An empty string indicates that the price is unknown.</span></span> <span data-ttu-id="90401-148">Ein NULL-Wert in diesem Feld bedeutet, dass der Titel frei ist, und ein Bindestrich (-) gibt an, dass der Track nicht gekauft werden kann.</span><span class="sxs-lookup"><span data-stu-id="90401-148">A zero in this field means the track is free, and a hyphen (-) indicates that the track cannot be bought.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="90401-149">Canstream</span><span class="sxs-lookup"><span data-stu-id="90401-149">CanStream</span></span></td>
<td><span data-ttu-id="90401-150">Ja</span><span class="sxs-lookup"><span data-stu-id="90401-150">Yes</span></span></td>
<td><span data-ttu-id="90401-151">Boolesch.</span><span class="sxs-lookup"><span data-stu-id="90401-151">Boolean.</span></span> <span data-ttu-id="90401-152">Kann 0 oder 1 sein. Beispiel: 0</span><span class="sxs-lookup"><span data-stu-id="90401-152">Can be 0 or 1.Example: 0</span></span><br/></td>
<td><span data-ttu-id="90401-153">Gibt an, ob der Track gestreamt werden kann.</span><span class="sxs-lookup"><span data-stu-id="90401-153">Indicates whether the track can be streamed.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="90401-154">Kerzen laden</span><span class="sxs-lookup"><span data-stu-id="90401-154">CanDownload</span></span></td>
<td><span data-ttu-id="90401-155">Ja</span><span class="sxs-lookup"><span data-stu-id="90401-155">Yes</span></span></td>
<td><span data-ttu-id="90401-156">Boolesch.</span><span class="sxs-lookup"><span data-stu-id="90401-156">Boolean.</span></span> <span data-ttu-id="90401-157">Kann 0 oder 1 sein. Beispiel: 0</span><span class="sxs-lookup"><span data-stu-id="90401-157">Can be 0 or 1.Example: 0</span></span><br/></td>
<td><span data-ttu-id="90401-158">Gibt an, ob der Track heruntergeladen werden kann.</span><span class="sxs-lookup"><span data-stu-id="90401-158">Indicates whether the track can be downloaded.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="90401-159">Haspreviewclip</span><span class="sxs-lookup"><span data-stu-id="90401-159">HasPreviewClip</span></span></td>
<td><span data-ttu-id="90401-160">Ja</span><span class="sxs-lookup"><span data-stu-id="90401-160">Yes</span></span></td>
<td><span data-ttu-id="90401-161">Boolesch.</span><span class="sxs-lookup"><span data-stu-id="90401-161">Boolean.</span></span> <span data-ttu-id="90401-162">Kann 0 oder 1 sein. Beispiel: 0</span><span class="sxs-lookup"><span data-stu-id="90401-162">Can be 0 or 1.Example: 0</span></span><br/></td>
<td><span data-ttu-id="90401-163">Gibt an, ob der Titel einen Vorschau Clip aufweist.</span><span class="sxs-lookup"><span data-stu-id="90401-163">Indicates whether the track has a preview clip.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="90401-164">Hasvideoclip</span><span class="sxs-lookup"><span data-stu-id="90401-164">HasVideoClip</span></span></td>
<td><span data-ttu-id="90401-165">Ja</span><span class="sxs-lookup"><span data-stu-id="90401-165">Yes</span></span></td>
<td><span data-ttu-id="90401-166">Boolesch.</span><span class="sxs-lookup"><span data-stu-id="90401-166">Boolean.</span></span> <span data-ttu-id="90401-167">Kann 0 oder 1 sein. Beispiel: 0</span><span class="sxs-lookup"><span data-stu-id="90401-167">Can be 0 or 1.Example: 0</span></span><br/></td>
<td><span data-ttu-id="90401-168">Gibt an, ob der Track über einen Videoclip verfügt.</span><span class="sxs-lookup"><span data-stu-id="90401-168">Indicates whether the track has a video clip.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="90401-169">Parametrialbewertung</span><span class="sxs-lookup"><span data-stu-id="90401-169">ParentalRating</span></span></td>
<td><span data-ttu-id="90401-170">Ja</span><span class="sxs-lookup"><span data-stu-id="90401-170">Yes</span></span></td>
<td><span data-ttu-id="90401-171">Enumeration.</span><span class="sxs-lookup"><span data-stu-id="90401-171">Enumeration.</span></span> <span data-ttu-id="90401-172">Kann n, E oder C sein. Beispiel: n</span><span class="sxs-lookup"><span data-stu-id="90401-172">Can be N, E, or C.Example: N</span></span><br/></td>
<td><span data-ttu-id="90401-173">Gibt die Bewertung des Elternbeirats an.</span><span class="sxs-lookup"><span data-stu-id="90401-173">Indicates the Parental Advisory Rating.</span></span> <span data-ttu-id="90401-174">Die Werte N, E und C stehen für "Normal", "explizit" und "Clean".</span><span class="sxs-lookup"><span data-stu-id="90401-174">The values N, E, and C stand for Normal, Explicit, and Clean.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="90401-175">Linkedalbumid</span><span class="sxs-lookup"><span data-stu-id="90401-175">LinkedAlbumID</span></span></td>
<td><span data-ttu-id="90401-176">Ja</span><span class="sxs-lookup"><span data-stu-id="90401-176">Yes</span></span></td>
<td><span data-ttu-id="90401-177">Nicht negative ganze Zahl.</span><span class="sxs-lookup"><span data-stu-id="90401-177">Non-negative integer.</span></span> <span data-ttu-id="90401-178">Muss die ID eines-Albums sein.</span><span class="sxs-lookup"><span data-stu-id="90401-178">Must be the ID of an Album.</span></span> <span data-ttu-id="90401-179">Beispiel: 32423</span><span class="sxs-lookup"><span data-stu-id="90401-179">Example: 32423</span></span></td>
<td><span data-ttu-id="90401-180">Die ID des Albums, das diese Spur enthält.</span><span class="sxs-lookup"><span data-stu-id="90401-180">The ID of the album that contains this track.</span></span>
<blockquote>
[!Note]<br />
<span data-ttu-id="90401-181">Jeder Track muss zu einem Album gehören.</span><span class="sxs-lookup"><span data-stu-id="90401-181">Every track must belong to an album.</span></span> <span data-ttu-id="90401-182">Das heißt, für jede Spur muss das Feld linkedalbumid gleich einer der Album-IDs in der album.csv-Datei sein.</span><span class="sxs-lookup"><span data-stu-id="90401-182">That is, for each track, the LinkedAlbumID field must be equal to one of the album IDs in the album.csv file.</span></span>
</blockquote>
<br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="90401-183">LinkedTrackArtist_ArtistIDs</span><span class="sxs-lookup"><span data-stu-id="90401-183">LinkedTrackArtist_ArtistIDs</span></span></td>
<td><span data-ttu-id="90401-184">Ja</span><span class="sxs-lookup"><span data-stu-id="90401-184">Yes</span></span></td>
<td><span data-ttu-id="90401-185">Liste mit ganzen Zahlen.</span><span class="sxs-lookup"><span data-stu-id="90401-185">List of integers.</span></span> <span data-ttu-id="90401-186">Die Liste enthält die durch Semikolons getrennten Interpreten-IDs.</span><span class="sxs-lookup"><span data-stu-id="90401-186">The list contains artist IDs, separated by semicolons.</span></span> <span data-ttu-id="90401-187">Beispiel: 41322; 12321; 82123;</span><span class="sxs-lookup"><span data-stu-id="90401-187">Example: 41322;12321; 82123;</span></span></td>
<td><span data-ttu-id="90401-188">Eine Liste von IDs, die den beteiligten Künstlern entsprechen.</span><span class="sxs-lookup"><span data-stu-id="90401-188">A list of IDs corresponding to the contributing artists.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="90401-189">Composer</span><span class="sxs-lookup"><span data-stu-id="90401-189">Composer</span></span></td>
<td><span data-ttu-id="90401-190">Nein</span><span class="sxs-lookup"><span data-stu-id="90401-190">No</span></span></td>
<td><span data-ttu-id="90401-191">Unicode-Zeichenfolge.</span><span class="sxs-lookup"><span data-stu-id="90401-191">Unicode string.</span></span> <span data-ttu-id="90401-192">Beispiel: Beethoven</span><span class="sxs-lookup"><span data-stu-id="90401-192">Example: Beethoven</span></span></td>
<td><span data-ttu-id="90401-193">Der Ersteller des Titels. Wenn für das Genre des Titels das hascomposer-Feld nicht festgelegt ist, wird der Wert des Felds Composer ignoriert.</span><span class="sxs-lookup"><span data-stu-id="90401-193">The composer of the track. If the track's genre does not have the HasComposer field set, the value of the Composer field will be ignored.</span></span> <span data-ttu-id="90401-194">Wird normalerweise nur für Jazz-oder klassische Titel verwendet.</span><span class="sxs-lookup"><span data-stu-id="90401-194">Typically used only for jazz or classical tracks.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="90401-195">Beliebtheit</span><span class="sxs-lookup"><span data-stu-id="90401-195">Popularity</span></span></td>
<td><span data-ttu-id="90401-196">Ja</span><span class="sxs-lookup"><span data-stu-id="90401-196">Yes</span></span></td>
<td><span data-ttu-id="90401-197">Nicht negative ganze Zahl oder float. Beispiel: 1252,6</span><span class="sxs-lookup"><span data-stu-id="90401-197">Non-negative integer or Float.Example: 1252.6</span></span><br/></td>
<td><span data-ttu-id="90401-198">Bestimmt die Position des Titels in der Liste, wenn nach Beliebtheit sortiert.</span><span class="sxs-lookup"><span data-stu-id="90401-198">Determines the position of the track in the list when sorted by popularity.</span></span> <span data-ttu-id="90401-199">Eine niedrigere Zahl weist auf eine höhere Beliebtheit hin.</span><span class="sxs-lookup"><span data-stu-id="90401-199">A lower number indicates higher popularity.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="90401-200">Star Rating</span><span class="sxs-lookup"><span data-stu-id="90401-200">StarRating</span></span></td>
<td><span data-ttu-id="90401-201">Nein</span><span class="sxs-lookup"><span data-stu-id="90401-201">No</span></span></td>
<td><span data-ttu-id="90401-202">Float. Beispiel: 4,21</span><span class="sxs-lookup"><span data-stu-id="90401-202">Float.Example: 4.21</span></span><br/></td>
<td><span data-ttu-id="90401-203">Die Stern Bewertung wird von Windows Media Player auf den nächsten 1/4-Stern gerundet, bevor Sie auf der Windows Media Player-Benutzeroberfläche angezeigt wird.</span><span class="sxs-lookup"><span data-stu-id="90401-203">The star rating will be rounded to the nearest 1/4 star by Windows Media Player before being displayed in the Windows Media Player user interface.</span></span></td>
</tr>
</tbody>
</table>



 

 

 





