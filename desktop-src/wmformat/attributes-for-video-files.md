---
title: Attribute für Video Dateien
description: Attribute für Video Dateien
ms.assetid: 4250ad27-075e-4daa-bc04-d24ddd2e8252
keywords:
- Windows Media-Format-SDK, Attribute
- Advanced Systems Format (ASF), Attribute
- ASF (Advanced Systems Format), Attribute
- Attribute, Videodateien
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: cd19791857d55be8017d291698a3297b395af550
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "104388092"
---
# <a name="attributes-for-video-files"></a><span data-ttu-id="9a04f-107">Attribute für Video Dateien</span><span class="sxs-lookup"><span data-stu-id="9a04f-107">Attributes for Video Files</span></span>

<span data-ttu-id="9a04f-108">In diesem Abschnitt werden die Attribute aufgelistet, die häufig für Videodateien verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="9a04f-108">This section lists the attributes commonly used for video files.</span></span> <span data-ttu-id="9a04f-109">Es wird empfohlen, dass Sie die Attribute für Dateien entsprechend diesen Listen festlegen, um sicherzustellen, dass Ihre Dateien mit einer Vielzahl von Wiedergabe Anwendungen vollständig kompatibel sind.</span><span class="sxs-lookup"><span data-stu-id="9a04f-109">It is recommended that you set attributes for files according to these lists to ensure that your files are fully compatible with a wide variety of playback applications.</span></span> <span data-ttu-id="9a04f-110">Die Attribute in diesem Abschnitt sind in drei Kategorien aufgeführt: primär, Sekundär und Tertiär.</span><span class="sxs-lookup"><span data-stu-id="9a04f-110">The attributes in this section are listed in three categories: primary, secondary, and tertiary.</span></span>

<span data-ttu-id="9a04f-111">Primäre Attribute vermitteln die grundlegendsten Informationen zu einer Datei.</span><span class="sxs-lookup"><span data-stu-id="9a04f-111">Primary attributes convey the most basic information about a file.</span></span> <span data-ttu-id="9a04f-112">Wenn Sie Videodateien für die Verteilung erstellen, ist dies der minimale Satz von Attributen, die Sie verwenden sollten.</span><span class="sxs-lookup"><span data-stu-id="9a04f-112">If you are creating video files for distribution, this is the minimum set of attributes you should use.</span></span>

<span data-ttu-id="9a04f-113">Sekundäre Attribute enthalten allgemeine Metadaten, die wichtig, aber nicht für alle Videodateien universell sind.</span><span class="sxs-lookup"><span data-stu-id="9a04f-113">Secondary attributes contain common metadata that is important but not universal to all video files.</span></span>

<span data-ttu-id="9a04f-114">Tertiäre Attribute sollten bei Bedarf eingeschlossen werden, sind jedoch für die Beschreibung der Datei nicht unbedingt erforderlich.</span><span class="sxs-lookup"><span data-stu-id="9a04f-114">Tertiary attributes should be included as needed, but are not essential to describing the file.</span></span>

## <a name="primary-attributes-for-video"></a><span data-ttu-id="9a04f-115">Primäre Attribute für Videos</span><span class="sxs-lookup"><span data-stu-id="9a04f-115">Primary Attributes for Video</span></span>

-   [<span data-ttu-id="9a04f-116">**Autor**</span><span class="sxs-lookup"><span data-stu-id="9a04f-116">**Author**</span></span>](author.md)
-   [<span data-ttu-id="9a04f-117">**Titel**</span><span class="sxs-lookup"><span data-stu-id="9a04f-117">**Title**</span></span>](title.md)
-   [<span data-ttu-id="9a04f-118">**WM/contentdistributor**</span><span class="sxs-lookup"><span data-stu-id="9a04f-118">**WM/ContentDistributor**</span></span>](wm-contentdistributor.md)
-   <span data-ttu-id="9a04f-119">[**WM/dvdid**](wm-dvdid.md) (falls verfügbar; verwenden Sie andernfalls [**WM/wmcollectionid**](wm-wmcollectionid.md), [**WM/wmcollectiongroupid**](wm-wmcollectiongroupid.md)und [**WM/wmcontentid**](wm-wmcontentid.md)).</span><span class="sxs-lookup"><span data-stu-id="9a04f-119">[**WM/DVDID**](wm-dvdid.md) (if available; otherwise use [**WM/WMCollectionID**](wm-wmcollectionid.md), [**WM/WMCollectionGroupID**](wm-wmcollectiongroupid.md), and [**WM/WMContentID**](wm-wmcontentid.md))</span></span>
-   [<span data-ttu-id="9a04f-120">**WM/Genre**</span><span class="sxs-lookup"><span data-stu-id="9a04f-120">**WM/Genre**</span></span>](wm-genre.md)
-   [<span data-ttu-id="9a04f-121">**WM/mediaclassprimaryid**</span><span class="sxs-lookup"><span data-stu-id="9a04f-121">**WM/MediaClassPrimaryID**</span></span>](wm-mediaprimaryid.md)
-   [<span data-ttu-id="9a04f-122">**WM/MediaClassSecondaryID**</span><span class="sxs-lookup"><span data-stu-id="9a04f-122">**WM/MediaClassSecondaryID**</span></span>](wm-mediasecondaryid.md)
-   [<span data-ttu-id="9a04f-123">**WM/Anbieter**</span><span class="sxs-lookup"><span data-stu-id="9a04f-123">**WM/Provider**</span></span>](wm-provider.md)

## <a name="secondary-attributes-for-video"></a><span data-ttu-id="9a04f-124">Sekundäre Attribute für Video</span><span class="sxs-lookup"><span data-stu-id="9a04f-124">Secondary Attributes for Video</span></span>

-   [<span data-ttu-id="9a04f-125">**Copyright**</span><span class="sxs-lookup"><span data-stu-id="9a04f-125">**Copyright**</span></span>](copyright.md)
-   [<span data-ttu-id="9a04f-126">**WM/Composer**</span><span class="sxs-lookup"><span data-stu-id="9a04f-126">**WM/Composer**</span></span>](wm-composer.md)
-   [<span data-ttu-id="9a04f-127">**WM/Director**</span><span class="sxs-lookup"><span data-stu-id="9a04f-127">**WM/Director**</span></span>](wm-director.md)
-   [<span data-ttu-id="9a04f-128">**WM/encodingtime**</span><span class="sxs-lookup"><span data-stu-id="9a04f-128">**WM/EncodingTime**</span></span>](wm-encodingtime.md)
-   [<span data-ttu-id="9a04f-129">**WM/Sprache**</span><span class="sxs-lookup"><span data-stu-id="9a04f-129">**WM/Language**</span></span>](wm-language.md)
-   [<span data-ttu-id="9a04f-130">**WM/parametrialbewertung**</span><span class="sxs-lookup"><span data-stu-id="9a04f-130">**WM/ParentalRating**</span></span>](wm-parentalrating.md)
-   [<span data-ttu-id="9a04f-131">**WM/Producer**</span><span class="sxs-lookup"><span data-stu-id="9a04f-131">**WM/Producer**</span></span>](wm-producer.md)
-   [<span data-ttu-id="9a04f-132">**WM/ToolName**</span><span class="sxs-lookup"><span data-stu-id="9a04f-132">**WM/ToolName**</span></span>](wm-toolname.md)
-   [<span data-ttu-id="9a04f-133">**WM/Toolversion**</span><span class="sxs-lookup"><span data-stu-id="9a04f-133">**WM/ToolVersion**</span></span>](wm-toolversion.md)
-   [<span data-ttu-id="9a04f-134">**WM/wmcollectiongroupid**</span><span class="sxs-lookup"><span data-stu-id="9a04f-134">**WM/WMCollectionGroupID**</span></span>](wm-wmcollectiongroupid.md)
-   [<span data-ttu-id="9a04f-135">**WM/wmcollectionid**</span><span class="sxs-lookup"><span data-stu-id="9a04f-135">**WM/WMCollectionID**</span></span>](wm-wmcollectionid.md)
-   [<span data-ttu-id="9a04f-136">**WM/wmcontentid**</span><span class="sxs-lookup"><span data-stu-id="9a04f-136">**WM/WMContentID**</span></span>](wm-wmcontentid.md)
-   [<span data-ttu-id="9a04f-137">**WM/Writer**</span><span class="sxs-lookup"><span data-stu-id="9a04f-137">**WM/Writer**</span></span>](wm-writer.md)

## <a name="tertiary-attributes-for-video"></a><span data-ttu-id="9a04f-138">Tertiäre Attribute für Videos</span><span class="sxs-lookup"><span data-stu-id="9a04f-138">Tertiary Attributes for Video</span></span>

-   [<span data-ttu-id="9a04f-139">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="9a04f-139">**Description**</span></span>](description.md)
-   [<span data-ttu-id="9a04f-140">**WM/authorurl**</span><span class="sxs-lookup"><span data-stu-id="9a04f-140">**WM/AuthorURL**</span></span>](wm-authorurl.md)
-   [<span data-ttu-id="9a04f-141">**WM/Dirigent**</span><span class="sxs-lookup"><span data-stu-id="9a04f-141">**WM/Conductor**</span></span>](wm-conductor.md)
-   [<span data-ttu-id="9a04f-142">**WM/contentgroupdescription**</span><span class="sxs-lookup"><span data-stu-id="9a04f-142">**WM/ContentGroupDescription**</span></span>](wm-contentgroupdescription.md)
-   [<span data-ttu-id="9a04f-143">**WM/encodby**</span><span class="sxs-lookup"><span data-stu-id="9a04f-143">**WM/EncodedBy**</span></span>](wm-encodedby.md)
-   [<span data-ttu-id="9a04f-144">**WM/encodingsettings**</span><span class="sxs-lookup"><span data-stu-id="9a04f-144">**WM/EncodingSettings**</span></span>](wm-encodingsettings.md)
-   [<span data-ttu-id="9a04f-145">**WM/Element Satz**</span><span class="sxs-lookup"><span data-stu-id="9a04f-145">**WM/PartOfSet**</span></span>](wm-partofset.md)
-   [<span data-ttu-id="9a04f-146">**WM/Bild**</span><span class="sxs-lookup"><span data-stu-id="9a04f-146">**WM/Picture**</span></span>](wmpicture.md)
-   [<span data-ttu-id="9a04f-147">**WM/promotionurl**</span><span class="sxs-lookup"><span data-stu-id="9a04f-147">**WM/PromotionURL**</span></span>](wm-promotionurl.md)
-   [<span data-ttu-id="9a04f-148">**WM/Verleger**</span><span class="sxs-lookup"><span data-stu-id="9a04f-148">**WM/Publisher**</span></span>](wm-publisher.md)
-   [<span data-ttu-id="9a04f-149">**WM/Untertitel**</span><span class="sxs-lookup"><span data-stu-id="9a04f-149">**WM/SubTitle**</span></span>](wm-subtitle.md)
-   [<span data-ttu-id="9a04f-150">**WM/UniqueFileIdentifier**</span><span class="sxs-lookup"><span data-stu-id="9a04f-150">**WM/UniqueFileIdentifier**</span></span>](wm-uniquefileidentifier.md)
-   [<span data-ttu-id="9a04f-151">**WM/userweburl**</span><span class="sxs-lookup"><span data-stu-id="9a04f-151">**WM/UserWebURL**</span></span>](wm-userweburl.md)

## <a name="related-topics"></a><span data-ttu-id="9a04f-152">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="9a04f-152">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="9a04f-153">**Attribute nach Typ**</span><span class="sxs-lookup"><span data-stu-id="9a04f-153">**Attributes By Type**</span></span>](attributes-by-type.md)
</dt> <dt>

[<span data-ttu-id="9a04f-154">**Attributliste**</span><span class="sxs-lookup"><span data-stu-id="9a04f-154">**Attribute List**</span></span>](attribute-list.md)
</dt> </dl>

 

 




