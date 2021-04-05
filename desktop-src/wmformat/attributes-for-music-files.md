---
title: Attribute für Musikdateien
description: Attribute für Musikdateien
ms.assetid: 098d9241-c8b0-4b0c-b9c1-668497f91e8c
keywords:
- Windows Media-Format-SDK, Attribute
- Advanced Systems Format (ASF), Attribute
- ASF (Advanced Systems Format), Attribute
- Attribute, Audiodateien
- Attribute, Musikdateien
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7e5956296da5ef43ed3a8d35ecc2d7e6d0a4c97e
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "103708766"
---
# <a name="attributes-for-music-files"></a><span data-ttu-id="109b1-108">Attribute für Musikdateien</span><span class="sxs-lookup"><span data-stu-id="109b1-108">Attributes for Music Files</span></span>

<span data-ttu-id="109b1-109">In diesem Abschnitt werden die Attribute aufgelistet, die häufig für Audiodateien mit Musik verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="109b1-109">This section lists the attributes commonly used for audio files containing music.</span></span> <span data-ttu-id="109b1-110">Es wird empfohlen, dass Sie die Attribute für Dateien entsprechend diesen Listen festlegen, um sicherzustellen, dass Ihre Dateien mit einer Vielzahl von Wiedergabe Anwendungen vollständig kompatibel sind.</span><span class="sxs-lookup"><span data-stu-id="109b1-110">It is recommended that you set attributes for files according to these lists to ensure that your files are fully compatible with a wide variety of playback applications.</span></span> <span data-ttu-id="109b1-111">Die Attribute in diesem Abschnitt sind in drei Kategorien aufgeführt: primär, Sekundär und Tertiär.</span><span class="sxs-lookup"><span data-stu-id="109b1-111">The attributes in this section are listed in three categories: primary, secondary, and tertiary.</span></span>

<span data-ttu-id="109b1-112">Primäre Attribute vermitteln die grundlegendsten Informationen zu einer Datei.</span><span class="sxs-lookup"><span data-stu-id="109b1-112">Primary attributes convey the most basic information about a file.</span></span> <span data-ttu-id="109b1-113">Wenn Sie Audiodateien für die Verteilung erstellen, ist dies der minimale Satz von Attributen, die Sie verwenden sollten.</span><span class="sxs-lookup"><span data-stu-id="109b1-113">If you are creating audio files for distribution, this is the minimum set of attributes you should use.</span></span>

<span data-ttu-id="109b1-114">Sekundäre Attribute enthalten allgemeine Metadaten, die für alle Audiodateien wichtig, aber nicht universell sind.</span><span class="sxs-lookup"><span data-stu-id="109b1-114">Secondary attributes contain common metadata that is important but not universal to all audio files.</span></span>

<span data-ttu-id="109b1-115">Tertiäre Attribute sollten bei Bedarf eingeschlossen werden, sind jedoch für die Beschreibung der Datei nicht unbedingt erforderlich.</span><span class="sxs-lookup"><span data-stu-id="109b1-115">Tertiary attributes should be included as needed, but are not essential to describing the file.</span></span>

## <a name="primary-attributes-for-music"></a><span data-ttu-id="109b1-116">Primäre Attribute für Musik</span><span class="sxs-lookup"><span data-stu-id="109b1-116">Primary Attributes for Music</span></span>

-   [<span data-ttu-id="109b1-117">**Autor**</span><span class="sxs-lookup"><span data-stu-id="109b1-117">**Author**</span></span>](author.md)
-   [<span data-ttu-id="109b1-118">**Titel**</span><span class="sxs-lookup"><span data-stu-id="109b1-118">**Title**</span></span>](title.md)
-   [<span data-ttu-id="109b1-119">**WM/albumartist**</span><span class="sxs-lookup"><span data-stu-id="109b1-119">**WM/AlbumArtist**</span></span>](wm-albumartist.md)
-   [<span data-ttu-id="109b1-120">**WM/contentdistributor**</span><span class="sxs-lookup"><span data-stu-id="109b1-120">**WM/ContentDistributor**</span></span>](wm-contentdistributor.md)
-   [<span data-ttu-id="109b1-121">**WM/Genre**</span><span class="sxs-lookup"><span data-stu-id="109b1-121">**WM/Genre**</span></span>](wm-genre.md)
-   <span data-ttu-id="109b1-122">[**WM/MCDI**](wm-mcdi.md) (falls verfügbar; verwenden Sie andernfalls [**WM/wmcollectionid**](wm-wmcollectionid.md), [**WM/wmcollectiongroupid**](wm-wmcollectiongroupid.md)oder [**WM/wmcontentid**](wm-wmcontentid.md)).</span><span class="sxs-lookup"><span data-stu-id="109b1-122">[**WM/MCDI**](wm-mcdi.md) (if available; otherwise use [**WM/WMCollectionID**](wm-wmcollectionid.md), [**WM/WMCollectionGroupID**](wm-wmcollectiongroupid.md), or [**WM/WMContentID**](wm-wmcontentid.md))</span></span>
-   [<span data-ttu-id="109b1-123">**WM/mediaclassprimaryid**</span><span class="sxs-lookup"><span data-stu-id="109b1-123">**WM/MediaClassPrimaryID**</span></span>](wm-mediaprimaryid.md)
-   [<span data-ttu-id="109b1-124">**WM/MediaClassSecondaryID**</span><span class="sxs-lookup"><span data-stu-id="109b1-124">**WM/MediaClassSecondaryID**</span></span>](wm-mediasecondaryid.md)
-   [<span data-ttu-id="109b1-125">**WM/Anbieter**</span><span class="sxs-lookup"><span data-stu-id="109b1-125">**WM/Provider**</span></span>](wm-provider.md)
-   [<span data-ttu-id="109b1-126">**WM/tracknumber**</span><span class="sxs-lookup"><span data-stu-id="109b1-126">**WM/TrackNumber**</span></span>](wm-tracknumber.md)

## <a name="secondary-attributes-for-music"></a><span data-ttu-id="109b1-127">Sekundäre Attribute für Musik</span><span class="sxs-lookup"><span data-stu-id="109b1-127">Secondary Attributes for Music</span></span>

-   [<span data-ttu-id="109b1-128">**Copyright**</span><span class="sxs-lookup"><span data-stu-id="109b1-128">**Copyright**</span></span>](copyright.md)
-   [<span data-ttu-id="109b1-129">**WM/Composer**</span><span class="sxs-lookup"><span data-stu-id="109b1-129">**WM/Composer**</span></span>](wm-composer.md)
-   [<span data-ttu-id="109b1-130">**WM/encodingtime**</span><span class="sxs-lookup"><span data-stu-id="109b1-130">**WM/EncodingTime**</span></span>](wm-encodingtime.md)
-   [<span data-ttu-id="109b1-131">**WM/Sprache**</span><span class="sxs-lookup"><span data-stu-id="109b1-131">**WM/Language**</span></span>](wm-language.md)
-   [<span data-ttu-id="109b1-132">**WM/parametrialbewertung**</span><span class="sxs-lookup"><span data-stu-id="109b1-132">**WM/ParentalRating**</span></span>](wm-parentalrating.md)
-   [<span data-ttu-id="109b1-133">**WM/Producer**</span><span class="sxs-lookup"><span data-stu-id="109b1-133">**WM/Producer**</span></span>](wm-producer.md)
-   [<span data-ttu-id="109b1-134">**WM/ToolName**</span><span class="sxs-lookup"><span data-stu-id="109b1-134">**WM/ToolName**</span></span>](wm-toolname.md)
-   [<span data-ttu-id="109b1-135">**WM/Toolversion**</span><span class="sxs-lookup"><span data-stu-id="109b1-135">**WM/ToolVersion**</span></span>](wm-toolversion.md)
-   [<span data-ttu-id="109b1-136">**WM/wmcollectiongroupid**</span><span class="sxs-lookup"><span data-stu-id="109b1-136">**WM/WMCollectionGroupID**</span></span>](wm-wmcollectiongroupid.md)
-   [<span data-ttu-id="109b1-137">**WM/wmcollectionid**</span><span class="sxs-lookup"><span data-stu-id="109b1-137">**WM/WMCollectionID**</span></span>](wm-wmcollectionid.md)
-   [<span data-ttu-id="109b1-138">**WM/wmcontentid**</span><span class="sxs-lookup"><span data-stu-id="109b1-138">**WM/WMContentID**</span></span>](wm-wmcontentid.md)
-   [<span data-ttu-id="109b1-139">**WM/Writer**</span><span class="sxs-lookup"><span data-stu-id="109b1-139">**WM/Writer**</span></span>](wm-writer.md)

## <a name="tertiary-attributes-for-music"></a><span data-ttu-id="109b1-140">Tertiäre Attribute für Musik</span><span class="sxs-lookup"><span data-stu-id="109b1-140">Tertiary Attributes for Music</span></span>

-   [<span data-ttu-id="109b1-141">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="109b1-141">**Description**</span></span>](description.md)
-   [<span data-ttu-id="109b1-142">**WM/authorurl**</span><span class="sxs-lookup"><span data-stu-id="109b1-142">**WM/AuthorURL**</span></span>](wm-authorurl.md)
-   [<span data-ttu-id="109b1-143">**WM/beatsperminütlich**</span><span class="sxs-lookup"><span data-stu-id="109b1-143">**WM/BeatsPerMinute**</span></span>](wm-beatsperminute.md)
-   [<span data-ttu-id="109b1-144">**WM/Dirigent**</span><span class="sxs-lookup"><span data-stu-id="109b1-144">**WM/Conductor**</span></span>](wm-conductor.md)
-   [<span data-ttu-id="109b1-145">**WM/contentgroupdescription**</span><span class="sxs-lookup"><span data-stu-id="109b1-145">**WM/ContentGroupDescription**</span></span>](wm-contentgroupdescription.md)
-   [<span data-ttu-id="109b1-146">**WM/encodby**</span><span class="sxs-lookup"><span data-stu-id="109b1-146">**WM/EncodedBy**</span></span>](wm-encodedby.md)
-   [<span data-ttu-id="109b1-147">**WM/encodingsettings**</span><span class="sxs-lookup"><span data-stu-id="109b1-147">**WM/EncodingSettings**</span></span>](wm-encodingsettings.md)
-   [<span data-ttu-id="109b1-148">**WM/initialkey**</span><span class="sxs-lookup"><span data-stu-id="109b1-148">**WM/InitialKey**</span></span>](wm-initialkey.md)
-   [<span data-ttu-id="109b1-149">**WM/Liedtexte**</span><span class="sxs-lookup"><span data-stu-id="109b1-149">**WM/Lyrics**</span></span>](wm-lyrics.md)
-   [<span data-ttu-id="109b1-150">**Synchronisierte WM/Liedtexte \_**</span><span class="sxs-lookup"><span data-stu-id="109b1-150">**WM/Lyrics\_Synchronised**</span></span>](wm-lyrics-synchronised.md)
-   [<span data-ttu-id="109b1-151">**WM/Stimmung**</span><span class="sxs-lookup"><span data-stu-id="109b1-151">**WM/Mood**</span></span>](wm-mood.md)
-   [<span data-ttu-id="109b1-152">**WM/Element Satz**</span><span class="sxs-lookup"><span data-stu-id="109b1-152">**WM/PartOfSet**</span></span>](wm-partofset.md)
-   [<span data-ttu-id="109b1-153">**WM/Zeitraum**</span><span class="sxs-lookup"><span data-stu-id="109b1-153">**WM/Period**</span></span>](wm-period.md)
-   [<span data-ttu-id="109b1-154">**WM/Bild**</span><span class="sxs-lookup"><span data-stu-id="109b1-154">**WM/Picture**</span></span>](wmpicture.md)
-   [<span data-ttu-id="109b1-155">**WM/promotionurl**</span><span class="sxs-lookup"><span data-stu-id="109b1-155">**WM/PromotionURL**</span></span>](wm-promotionurl.md)
-   [<span data-ttu-id="109b1-156">**WM/Verleger**</span><span class="sxs-lookup"><span data-stu-id="109b1-156">**WM/Publisher**</span></span>](wm-publisher.md)
-   [<span data-ttu-id="109b1-157">**WM/Untertitel**</span><span class="sxs-lookup"><span data-stu-id="109b1-157">**WM/SubTitle**</span></span>](wm-subtitle.md)
-   [<span data-ttu-id="109b1-158">**WM/UniqueFileIdentifier**</span><span class="sxs-lookup"><span data-stu-id="109b1-158">**WM/UniqueFileIdentifier**</span></span>](wm-uniquefileidentifier.md)
-   [<span data-ttu-id="109b1-159">**WM/userweburl**</span><span class="sxs-lookup"><span data-stu-id="109b1-159">**WM/UserWebURL**</span></span>](wm-userweburl.md)

## <a name="related-topics"></a><span data-ttu-id="109b1-160">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="109b1-160">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="109b1-161">**Attribute nach Typ**</span><span class="sxs-lookup"><span data-stu-id="109b1-161">**Attributes By Type**</span></span>](attributes-by-type.md)
</dt> <dt>

[<span data-ttu-id="109b1-162">**Attributliste**</span><span class="sxs-lookup"><span data-stu-id="109b1-162">**Attribute List**</span></span>](attribute-list.md)
</dt> </dl>

 

 




