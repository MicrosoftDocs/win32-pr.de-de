---
title: Wiedergabeliste. Spalten
description: Das Columns-Attribut definiert die Spalten, die im Wiedergabelisten Element angezeigt werden.
ms.assetid: a805ee06-cf73-4eab-bcda-c374e55cd11a
keywords:
- Wiedergabeliste. Spalten (Fenster) Media Player
topic_type:
- apiref
api_name:
- PLAYLIST.columns
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: fcc5f8ef5dc76428ca892d079b60692e6949a5ca
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106366939"
---
# <a name="playlistcolumns"></a><span data-ttu-id="f4764-104">Wiedergabeliste. Spalten</span><span class="sxs-lookup"><span data-stu-id="f4764-104">PLAYLIST.columns</span></span>

<span data-ttu-id="f4764-105">Das **Columns** -Attribut definiert die Spalten, die im **Wiedergabe** Listenelement angezeigt werden.</span><span class="sxs-lookup"><span data-stu-id="f4764-105">The **columns** attribute defines the columns that appear in the **PLAYLIST** element.</span></span>

``` syntax
        elementID.columns
```

## <a name="possible-values"></a><span data-ttu-id="f4764-106">Mögliche Werte</span><span class="sxs-lookup"><span data-stu-id="f4764-106">Possible Values</span></span>

<span data-ttu-id="f4764-107">Dieses Attribut ist eine Lese- **/schreibzeichenfolge** im folgenden Format:</span><span class="sxs-lookup"><span data-stu-id="f4764-107">This attribute is a read/write **String** in the following format:</span></span>

<span data-ttu-id="f4764-108">DB \_ Name = Anzeige \_ Name; DB \_ Name = Anzeige \_ Name;</span><span class="sxs-lookup"><span data-stu-id="f4764-108">DB\_NAME=FRIENDLY\_NAME;DB\_NAME=FRIENDLY\_NAME;</span></span>

<span data-ttu-id="f4764-109">\_Der Anzeige Name ist der Wert, der im Spaltenheader des Wiedergabelisten Elements angezeigt wird, und DB \_ Name ist ein Wert aus der folgenden Tabelle.</span><span class="sxs-lookup"><span data-stu-id="f4764-109">FRIENDLY\_NAME is the value shown in the column header of the PLAYLIST element, and DB\_NAME is a value from the following table.</span></span> <span data-ttu-id="f4764-110">Beachten Sie, dass ein Wiedergabelisten Element ein Medien Element aus der Bibliothek oder einer CD sein kann, oder es kann sich um eine andere **Wiedergabeliste** handeln, die entweder von einem Benutzer erstellt oder von einer CD stammt.</span><span class="sxs-lookup"><span data-stu-id="f4764-110">Note that a Playlist item might be a media item from the library or from a CD, or it might be another **Playlist** that is either user-created or taken from a CD.</span></span> <span data-ttu-id="f4764-111">Einige Spalten sind nur mit bestimmten Wiedergabelisten Elementen gültig, wie in der Beschreibungs Spalte angegeben.</span><span class="sxs-lookup"><span data-stu-id="f4764-111">Some columns are valid only with certain Playlist items as indicated in the Description column.</span></span>



| <span data-ttu-id="f4764-112">Wert</span><span class="sxs-lookup"><span data-stu-id="f4764-112">Value</span></span>             | <span data-ttu-id="f4764-113">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="f4764-113">Description</span></span>                                                                                                             |
|-------------------|-------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="f4764-114">Aufzunehmen</span><span class="sxs-lookup"><span data-stu-id="f4764-114">Album</span></span>             | <span data-ttu-id="f4764-115">Der Name des Albums.</span><span class="sxs-lookup"><span data-stu-id="f4764-115">The name of the album.</span></span> <span data-ttu-id="f4764-116">Wird nur für Medienelemente verwendet.</span><span class="sxs-lookup"><span data-stu-id="f4764-116">Used with media items only.</span></span>                                                                      |
| <span data-ttu-id="f4764-117">Interpret</span><span class="sxs-lookup"><span data-stu-id="f4764-117">Artist</span></span>            | <span data-ttu-id="f4764-118">Der Name des Künstlers.</span><span class="sxs-lookup"><span data-stu-id="f4764-118">The name of the artist.</span></span> <span data-ttu-id="f4764-119">Wird nicht mit vom Benutzer erstellten Wiedergabelisten verwendet.</span><span class="sxs-lookup"><span data-stu-id="f4764-119">Not used with user-created playlists.</span></span>                                                           |
| <span data-ttu-id="f4764-120">Autor</span><span class="sxs-lookup"><span data-stu-id="f4764-120">Author</span></span>            | <span data-ttu-id="f4764-121">Der Name des Künstlers.</span><span class="sxs-lookup"><span data-stu-id="f4764-121">The name of the artist.</span></span>                                                                                                 |
| <span data-ttu-id="f4764-122">Bitrate</span><span class="sxs-lookup"><span data-stu-id="f4764-122">Bitrate</span></span>           | <span data-ttu-id="f4764-123">Die Bitrate des Inhalts.</span><span class="sxs-lookup"><span data-stu-id="f4764-123">The bit rate of the content.</span></span> <span data-ttu-id="f4764-124">Wird nur für Medienelemente aus der Bibliothek verwendet.</span><span class="sxs-lookup"><span data-stu-id="f4764-124">Used only with media items from the library.</span></span>                                               |
| <span data-ttu-id="f4764-125">Cdtrackaktivierte</span><span class="sxs-lookup"><span data-stu-id="f4764-125">CDTrackEnabled</span></span>    | <span data-ttu-id="f4764-126">Gibt an, ob der CD-Track aktiviert ist.</span><span class="sxs-lookup"><span data-stu-id="f4764-126">Indicates whether the CD track is enabled.</span></span> <span data-ttu-id="f4764-127">Wird nur für CD-Medienelemente verwendet.</span><span class="sxs-lookup"><span data-stu-id="f4764-127">Used only with CD media items.</span></span>                                               |
| <span data-ttu-id="f4764-128">Überprüft</span><span class="sxs-lookup"><span data-stu-id="f4764-128">Checked</span></span>           | <span data-ttu-id="f4764-129">Für die zukünftige Verwendung reserviert.</span><span class="sxs-lookup"><span data-stu-id="f4764-129">Reserved for future use.</span></span>                                                                                                |
| <span data-ttu-id="f4764-130">Copyright</span><span class="sxs-lookup"><span data-stu-id="f4764-130">Copyright</span></span>         | <span data-ttu-id="f4764-131">Das Copyright der Wiedergabeliste.</span><span class="sxs-lookup"><span data-stu-id="f4764-131">The copyright of the playlist.</span></span> <span data-ttu-id="f4764-132">Wird nicht für CD-Wiedergabelisten oder Medienelemente verwendet.</span><span class="sxs-lookup"><span data-stu-id="f4764-132">Not used with CD playlists or media items.</span></span>                                               |
| <span data-ttu-id="f4764-133">CreationDate</span><span class="sxs-lookup"><span data-stu-id="f4764-133">CreationDate</span></span>      | <span data-ttu-id="f4764-134">Das Datum und die Uhrzeit der Erstellung des Eintrags in der Bibliothek.</span><span class="sxs-lookup"><span data-stu-id="f4764-134">The date and time that the entry in the library was created.</span></span> <span data-ttu-id="f4764-135">Wird nur mit Elementen aus der Bibliothek verwendet.</span><span class="sxs-lookup"><span data-stu-id="f4764-135">Used only with items from the library.</span></span>                     |
| <span data-ttu-id="f4764-136">Digitallysecure</span><span class="sxs-lookup"><span data-stu-id="f4764-136">DigitallySecure</span></span>   | <span data-ttu-id="f4764-137">Gibt an, ob das Element mit Windows Media Rights Manager geschützt wird.</span><span class="sxs-lookup"><span data-stu-id="f4764-137">Indicates whether the item is protected with Windows Media Rights Manager.</span></span> <span data-ttu-id="f4764-138">Wird nur für Medienelemente aus der Bibliothek verwendet.</span><span class="sxs-lookup"><span data-stu-id="f4764-138">Used only with media items from the library.</span></span> |
| <span data-ttu-id="f4764-139">Duration</span><span class="sxs-lookup"><span data-stu-id="f4764-139">Duration</span></span>          | <span data-ttu-id="f4764-140">Die Dauer des Medien Elements.</span><span class="sxs-lookup"><span data-stu-id="f4764-140">The duration of the media item.</span></span>                                                                                         |
| <span data-ttu-id="f4764-141">FileType</span><span class="sxs-lookup"><span data-stu-id="f4764-141">FileType</span></span>          | <span data-ttu-id="f4764-142">Für die zukünftige Verwendung reserviert.</span><span class="sxs-lookup"><span data-stu-id="f4764-142">Reserved for future use.</span></span>                                                                                                |
| <span data-ttu-id="f4764-143">Genre</span><span class="sxs-lookup"><span data-stu-id="f4764-143">Genre</span></span>             | <span data-ttu-id="f4764-144">Das Genre der Wiedergabeliste.</span><span class="sxs-lookup"><span data-stu-id="f4764-144">The genre of the playlist.</span></span> <span data-ttu-id="f4764-145">Wird nicht mit Wiedergabelisten von CDs verwendet.</span><span class="sxs-lookup"><span data-stu-id="f4764-145">Not used with playlists from CDs.</span></span>                                                            |
| <span data-ttu-id="f4764-146">MediaAttribute</span><span class="sxs-lookup"><span data-stu-id="f4764-146">MediaAttribute</span></span>    | <span data-ttu-id="f4764-147">Für die zukünftige Verwendung reserviert.</span><span class="sxs-lookup"><span data-stu-id="f4764-147">Reserved for future use.</span></span>                                                                                                |
| <span data-ttu-id="f4764-148">MediaType</span><span class="sxs-lookup"><span data-stu-id="f4764-148">MediaType</span></span>         | <span data-ttu-id="f4764-149">Der Typ des Medien Elements (Audiodatei oder Video).</span><span class="sxs-lookup"><span data-stu-id="f4764-149">The type of the media item (audio or video).</span></span>                                                                            |
| <span data-ttu-id="f4764-150">MetadataSource</span><span class="sxs-lookup"><span data-stu-id="f4764-150">MetadataSource</span></span>    | <span data-ttu-id="f4764-151">Die Quelle der Metadaten für diesen CD-Track (AMG, WindowsMedia.com usw.).</span><span class="sxs-lookup"><span data-stu-id="f4764-151">The source of the metadata for this CD track (AMG, WindowsMedia.com, and so on).</span></span> <span data-ttu-id="f4764-152">Wird nur für CD-Medienelemente verwendet.</span><span class="sxs-lookup"><span data-stu-id="f4764-152">Used only with CD media items.</span></span>         |
| <span data-ttu-id="f4764-153">ModifiedBy</span><span class="sxs-lookup"><span data-stu-id="f4764-153">ModifiedBy</span></span>        | <span data-ttu-id="f4764-154">Für die zukünftige Verwendung reserviert.</span><span class="sxs-lookup"><span data-stu-id="f4764-154">Reserved for future use.</span></span>                                                                                                |
| <span data-ttu-id="f4764-155">Name</span><span class="sxs-lookup"><span data-stu-id="f4764-155">Name</span></span>              | <span data-ttu-id="f4764-156">Der Name der Wiedergabeliste.</span><span class="sxs-lookup"><span data-stu-id="f4764-156">The name of the playlist.</span></span>                                                                                               |
| <span data-ttu-id="f4764-157">Originalindex</span><span class="sxs-lookup"><span data-stu-id="f4764-157">OriginalIndex</span></span>     | <span data-ttu-id="f4764-158">Falls zutreffend, der entsprechende CD-Track-Bezeichner.</span><span class="sxs-lookup"><span data-stu-id="f4764-158">If applicable, the corresponding CD track identifier.</span></span> <span data-ttu-id="f4764-159">Wird nur für CD-Medienelemente verwendet.</span><span class="sxs-lookup"><span data-stu-id="f4764-159">Used only with CD media items.</span></span>                                    |
| <span data-ttu-id="f4764-160">Playcount</span><span class="sxs-lookup"><span data-stu-id="f4764-160">PlayCount</span></span>         | <span data-ttu-id="f4764-161">Gibt an, wie oft der Inhalt bis zum Ende wiedergegeben wurde.</span><span class="sxs-lookup"><span data-stu-id="f4764-161">The number of times the content has been played through to the end.</span></span> <span data-ttu-id="f4764-162">Wird nur für Medienelemente aus der Bibliothek verwendet.</span><span class="sxs-lookup"><span data-stu-id="f4764-162">Used only with media items from the library.</span></span>        |
| <span data-ttu-id="f4764-163">Playlistatutribute</span><span class="sxs-lookup"><span data-stu-id="f4764-163">PlaylistAttribute</span></span> | <span data-ttu-id="f4764-164">Für die zukünftige Verwendung reserviert.</span><span class="sxs-lookup"><span data-stu-id="f4764-164">Reserved for future use.</span></span>                                                                                                |
| <span data-ttu-id="f4764-165">Rating</span><span class="sxs-lookup"><span data-stu-id="f4764-165">Rating</span></span>            | <span data-ttu-id="f4764-166">Für die zukünftige Verwendung reserviert.</span><span class="sxs-lookup"><span data-stu-id="f4764-166">Reserved for future use.</span></span>                                                                                                |
| <span data-ttu-id="f4764-167">SourceURL</span><span class="sxs-lookup"><span data-stu-id="f4764-167">SourceURL</span></span>         | <span data-ttu-id="f4764-168">Der Pfad oder die URL zum Inhalt.</span><span class="sxs-lookup"><span data-stu-id="f4764-168">The path or URL to the content.</span></span> <span data-ttu-id="f4764-169">Wird nur für Medienelemente aus der Bibliothek verwendet.</span><span class="sxs-lookup"><span data-stu-id="f4764-169">Used only with media items from the library.</span></span>                                            |
| <span data-ttu-id="f4764-170">Status</span><span class="sxs-lookup"><span data-stu-id="f4764-170">Status</span></span>            | <span data-ttu-id="f4764-171">Der Kopier Status einer CD-Spur, die kopiert wird.</span><span class="sxs-lookup"><span data-stu-id="f4764-171">The copying status of a CD track being copied.</span></span> <span data-ttu-id="f4764-172">Wird nur für CD-Medienelemente verwendet.</span><span class="sxs-lookup"><span data-stu-id="f4764-172">Used only with CD media items.</span></span>                                           |
| <span data-ttu-id="f4764-173">Stil</span><span class="sxs-lookup"><span data-stu-id="f4764-173">Style</span></span>             | <span data-ttu-id="f4764-174">Für die zukünftige Verwendung reserviert.</span><span class="sxs-lookup"><span data-stu-id="f4764-174">Reserved for future use.</span></span>                                                                                                |
| <span data-ttu-id="f4764-175">INHALTSVERZEICHNIS</span><span class="sxs-lookup"><span data-stu-id="f4764-175">TOC</span></span>               | <span data-ttu-id="f4764-176">Falls zutreffend, das entsprechende CD-Inhaltsverzeichnis.</span><span class="sxs-lookup"><span data-stu-id="f4764-176">If applicable, the corresponding CD Table of Contents Identifier.</span></span> <span data-ttu-id="f4764-177">Wird nicht mit vom Benutzer erstellten Wiedergabelisten verwendet.</span><span class="sxs-lookup"><span data-stu-id="f4764-177">Not used with user-created playlists.</span></span>                 |



 

## <a name="remarks"></a><span data-ttu-id="f4764-178">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="f4764-178">Remarks</span></span>

<span data-ttu-id="f4764-179">Wenn eine der Spalten nicht in der Bibliothek vorhanden ist, wird Sie leer gelassen.</span><span class="sxs-lookup"><span data-stu-id="f4764-179">If one of the columns does not exist in the library, it is left blank.</span></span>

<span data-ttu-id="f4764-180">Es können maximal 31 Spalten angegeben werden.</span><span class="sxs-lookup"><span data-stu-id="f4764-180">A maximum of 31 columns may be specified.</span></span>

<span data-ttu-id="f4764-181">Wenn Sie eine doppelte Spalte angeben, werden die Daten in der ersten Spalte linksbündig ausgerichtet, aber alle anderen doppelten Spalten werden rechtsbündig ausgerichtet.</span><span class="sxs-lookup"><span data-stu-id="f4764-181">If you specify a duplicate column, the data in the first column will be left-aligned but all other duplicate columns will be right-aligned.</span></span> <span data-ttu-id="f4764-182">Wenn Sie z. b. über zwei Duration-Spalten verfügen, werden die Daten im ersten und rechtsbündig ausgerichtet.</span><span class="sxs-lookup"><span data-stu-id="f4764-182">For example, if you have two duration columns, the data will be left-aligned in the first and right-aligned in the second.</span></span>

## <a name="requirements"></a><span data-ttu-id="f4764-183">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="f4764-183">Requirements</span></span>



| <span data-ttu-id="f4764-184">Anforderung</span><span class="sxs-lookup"><span data-stu-id="f4764-184">Requirement</span></span> | <span data-ttu-id="f4764-185">Wert</span><span class="sxs-lookup"><span data-stu-id="f4764-185">Value</span></span> |
|--------------------|------------------------------------------------------|
| <span data-ttu-id="f4764-186">Version</span><span class="sxs-lookup"><span data-stu-id="f4764-186">Version</span></span><br/> | <span data-ttu-id="f4764-187">Windows Media Player, Version 7,0 oder höher</span><span class="sxs-lookup"><span data-stu-id="f4764-187">Windows Media Player version 7.0 or later</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="f4764-188">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="f4764-188">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f4764-189">**Wiedergabelisten Element**</span><span class="sxs-lookup"><span data-stu-id="f4764-189">**PLAYLIST Element**</span></span>](playlist-element.md)
</dt> <dt>

[<span data-ttu-id="f4764-190">**Wiedergabeliste. columnsvisible**</span><span class="sxs-lookup"><span data-stu-id="f4764-190">**PLAYLIST.columnsVisible**</span></span>](playlist-columnsvisible.md)
</dt> </dl>

 

 





