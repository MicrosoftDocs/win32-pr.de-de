---
title: Zuordnung von RSS-Feeds zu Windows Media Device Manager-Eigenschaften
description: Zuordnung von RSS-Feeds zu Windows Media Device Manager-Eigenschaften
ms.assetid: 354c98ab-1392-476f-a650-75b948dc971a
keywords:
- Windows Media Device Manager, RSS-Feeds
- Device Manager, RSS-Feeds
- Programmier Handbuch, RSS-Feeds
- Desktop Anwendungen, RSS-Feeds
- Erstellen von Windows Media Device Manager-Anwendungen, RSS-Feeds
- RSS-Feeds
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c3a81d52b4099d77542963d2e87ae5b7dc26b034
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "103855572"
---
# <a name="mapping-rss-feeds-to-windows-media-device-manager-properties"></a><span data-ttu-id="b4e53-109">Zuordnung von RSS-Feeds zu Windows Media Device Manager-Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="b4e53-109">Mapping RSS Feeds to Windows Media Device Manager Properties</span></span>

<span data-ttu-id="b4e53-110">Windows Media Player 11 stellt eine RSS-Aggregator-Funktion bereit, die es Benutzern ermöglicht, Inhalte aus Podcasts auf ihren Computern zu speichern.</span><span class="sxs-lookup"><span data-stu-id="b4e53-110">Windows Media Player 11 provides an RSS aggregator feature that enables users to store content obtained from podcasts on their computers.</span></span> <span data-ttu-id="b4e53-111">In diesem Thema werden die in einem RSS-Feed gefundenen XML-Elemente beschrieben.</span><span class="sxs-lookup"><span data-stu-id="b4e53-111">This topic describes the XML elements found in an RSS feed.</span></span> <span data-ttu-id="b4e53-112">Außerdem werden diese RSS-Elemente den Windows Media Device Manager-Eigenschaften zugeordnet.</span><span class="sxs-lookup"><span data-stu-id="b4e53-112">In addition, it maps these RSS elements to Windows Media Device Manager properties.</span></span>

<span data-ttu-id="b4e53-113">Die Elemente in einem RSS-Feed verfügen über die folgende Hierarchie und Attribute:</span><span class="sxs-lookup"><span data-stu-id="b4e53-113">The elements in an RSS feed have the following hierarchy and attributes:</span></span>


```C++
<channel>
    <title />
    <link />
    <description />
    <language />
    <copyright />
    <managingEditor />
    <webMaster />
    <pubDate />
    <lastBuildDate />
    <category />
    <generator />
    <docs />
    <cloud />
    <ttl />

    <image>
        <url />
        <title />
        <link />
        <width />
        <height />
        <description />
    </image>

    <rating />

    <textInput>
        <title />
        <description />
        <name />
        <link />
    </textInput>

    <skipHours />
    <skipDays />

    <item>
        <title />
        <link />
        <description />
        <author />
        <category domain = " "/>
        <comments />
        <enclousure url = " " length = " " type = " "/>
        <guid isPermaLink = " "/>
        <pubDate />
        <source url = " " />
    </item>
</channel>
```



<span data-ttu-id="b4e53-114">In der folgenden Tabelle sind die Channelelemente in einem RSS-Feed und die entsprechenden Eigenschaften des Windows Media-Device Manager aufgeführt.</span><span class="sxs-lookup"><span data-stu-id="b4e53-114">The following table lists the channel elements in an RSS feed and the corresponding Windows Media Device Manager properties.</span></span>



| <span data-ttu-id="b4e53-115">Channel-Element</span><span class="sxs-lookup"><span data-stu-id="b4e53-115">Channel element</span></span> | <span data-ttu-id="b4e53-116">Status</span><span class="sxs-lookup"><span data-stu-id="b4e53-116">Status</span></span>         | <span data-ttu-id="b4e53-117">Zugehörige Windows Media Device Manager-Eigenschaft</span><span class="sxs-lookup"><span data-stu-id="b4e53-117">Corresponding Windows Media Device Manager property</span></span>   |
|-----------------|----------------|-------------------------------------------------------|
| <span data-ttu-id="b4e53-118">category</span><span class="sxs-lookup"><span data-stu-id="b4e53-118">category</span></span>        | <span data-ttu-id="b4e53-119">Optional</span><span class="sxs-lookup"><span data-stu-id="b4e53-119">Optional</span></span>       | [<span data-ttu-id="b4e53-120">g \_ wszwmdmgenre</span><span class="sxs-lookup"><span data-stu-id="b4e53-120">g\_wszWMDMGenre</span></span>](metadata-constants.md)             |
| <span data-ttu-id="b4e53-121">cloud</span><span class="sxs-lookup"><span data-stu-id="b4e53-121">cloud</span></span>           | <span data-ttu-id="b4e53-122">Nicht verfügbar</span><span class="sxs-lookup"><span data-stu-id="b4e53-122">Not applicable</span></span> | <span data-ttu-id="b4e53-123">Nicht verfügbar</span><span class="sxs-lookup"><span data-stu-id="b4e53-123">Not applicable</span></span>                                        |
| <span data-ttu-id="b4e53-124">Copyright</span><span class="sxs-lookup"><span data-stu-id="b4e53-124">copyright</span></span>       | <span data-ttu-id="b4e53-125">Optional</span><span class="sxs-lookup"><span data-stu-id="b4e53-125">Optional</span></span>       | [<span data-ttu-id="b4e53-126">g \_ wszwmdmprovidercopyright</span><span class="sxs-lookup"><span data-stu-id="b4e53-126">g\_wszWMDMProviderCopyright</span></span>](metadata-constants.md) |
| <span data-ttu-id="b4e53-127">description</span><span class="sxs-lookup"><span data-stu-id="b4e53-127">description</span></span>     | <span data-ttu-id="b4e53-128">Erforderlich</span><span class="sxs-lookup"><span data-stu-id="b4e53-128">Required</span></span>       | [<span data-ttu-id="b4e53-129">g \_ wszwmdmdescription</span><span class="sxs-lookup"><span data-stu-id="b4e53-129">g\_wszWMDMDescription</span></span>](metadata-constants.md)       |
| <span data-ttu-id="b4e53-130">Docs</span><span class="sxs-lookup"><span data-stu-id="b4e53-130">docs</span></span>            | <span data-ttu-id="b4e53-131">Nicht verfügbar</span><span class="sxs-lookup"><span data-stu-id="b4e53-131">Not applicable</span></span> | <span data-ttu-id="b4e53-132">Nicht verfügbar</span><span class="sxs-lookup"><span data-stu-id="b4e53-132">Not applicable</span></span>                                        |
| <span data-ttu-id="b4e53-133">Generator</span><span class="sxs-lookup"><span data-stu-id="b4e53-133">generator</span></span>       | <span data-ttu-id="b4e53-134">Nicht verfügbar</span><span class="sxs-lookup"><span data-stu-id="b4e53-134">Not applicable</span></span> | <span data-ttu-id="b4e53-135">Nicht verfügbar</span><span class="sxs-lookup"><span data-stu-id="b4e53-135">Not applicable</span></span>                                        |
| <span data-ttu-id="b4e53-136">language</span><span class="sxs-lookup"><span data-stu-id="b4e53-136">language</span></span>        | <span data-ttu-id="b4e53-137">Nicht verfügbar</span><span class="sxs-lookup"><span data-stu-id="b4e53-137">Not applicable</span></span> | <span data-ttu-id="b4e53-138">Nicht verfügbar</span><span class="sxs-lookup"><span data-stu-id="b4e53-138">Not applicable</span></span>                                        |
| <span data-ttu-id="b4e53-139">lastBuildDate</span><span class="sxs-lookup"><span data-stu-id="b4e53-139">lastBuildDate</span></span>   | <span data-ttu-id="b4e53-140">Optional</span><span class="sxs-lookup"><span data-stu-id="b4e53-140">Optional</span></span>       | [<span data-ttu-id="b4e53-141">g \_ wszwmdmlastmodifieddate</span><span class="sxs-lookup"><span data-stu-id="b4e53-141">g\_wszWMDMLastModifiedDate</span></span>](metadata-constants.md)  |
| <span data-ttu-id="b4e53-142">link</span><span class="sxs-lookup"><span data-stu-id="b4e53-142">link</span></span>            | <span data-ttu-id="b4e53-143">Erforderlich</span><span class="sxs-lookup"><span data-stu-id="b4e53-143">Required</span></span>       | [<span data-ttu-id="b4e53-144">g \_ wszwmdmdestinationurl</span><span class="sxs-lookup"><span data-stu-id="b4e53-144">g\_wszWMDMDestinationURL</span></span>](metadata-constants.md)    |
| <span data-ttu-id="b4e53-145">managingEditor</span><span class="sxs-lookup"><span data-stu-id="b4e53-145">managingEditor</span></span>  | <span data-ttu-id="b4e53-146">Optional</span><span class="sxs-lookup"><span data-stu-id="b4e53-146">Optional</span></span>       | [<span data-ttu-id="b4e53-147">g \_ wszwmdmeditor</span><span class="sxs-lookup"><span data-stu-id="b4e53-147">g\_wszWMDMEditor</span></span>](metadata-constants.md)            |
| <span data-ttu-id="b4e53-148">pubDate</span><span class="sxs-lookup"><span data-stu-id="b4e53-148">pubDate</span></span>         | <span data-ttu-id="b4e53-149">Optional</span><span class="sxs-lookup"><span data-stu-id="b4e53-149">Optional</span></span>       | [<span data-ttu-id="b4e53-150">g \_ wszwmdmyear</span><span class="sxs-lookup"><span data-stu-id="b4e53-150">g\_wszWMDMYear</span></span>](metadata-constants.md)              |
| <span data-ttu-id="b4e53-151">rating</span><span class="sxs-lookup"><span data-stu-id="b4e53-151">rating</span></span>          | <span data-ttu-id="b4e53-152">Nicht verfügbar</span><span class="sxs-lookup"><span data-stu-id="b4e53-152">Not applicable</span></span> | <span data-ttu-id="b4e53-153">Nicht verfügbar</span><span class="sxs-lookup"><span data-stu-id="b4e53-153">Not applicable</span></span>                                        |
| <span data-ttu-id="b4e53-154">skipdays</span><span class="sxs-lookup"><span data-stu-id="b4e53-154">skipDays</span></span>        | <span data-ttu-id="b4e53-155">Nicht verfügbar</span><span class="sxs-lookup"><span data-stu-id="b4e53-155">Not applicable</span></span> | <span data-ttu-id="b4e53-156">Nicht verfügbar</span><span class="sxs-lookup"><span data-stu-id="b4e53-156">Not applicable</span></span>                                        |
| <span data-ttu-id="b4e53-157">skiphours</span><span class="sxs-lookup"><span data-stu-id="b4e53-157">skipHours</span></span>       | <span data-ttu-id="b4e53-158">Nicht verfügbar</span><span class="sxs-lookup"><span data-stu-id="b4e53-158">Not applicable</span></span> | <span data-ttu-id="b4e53-159">Nicht verfügbar</span><span class="sxs-lookup"><span data-stu-id="b4e53-159">Not applicable</span></span>                                        |
| <span data-ttu-id="b4e53-160">TextInput</span><span class="sxs-lookup"><span data-stu-id="b4e53-160">textInput</span></span>       | <span data-ttu-id="b4e53-161">Nicht verfügbar</span><span class="sxs-lookup"><span data-stu-id="b4e53-161">Not applicable</span></span> | <span data-ttu-id="b4e53-162">Nicht verfügbar</span><span class="sxs-lookup"><span data-stu-id="b4e53-162">Not applicable</span></span>                                        |
| <span data-ttu-id="b4e53-163">title</span><span class="sxs-lookup"><span data-stu-id="b4e53-163">title</span></span>           | <span data-ttu-id="b4e53-164">Erforderlich</span><span class="sxs-lookup"><span data-stu-id="b4e53-164">Required</span></span>       | [<span data-ttu-id="b4e53-165">g \_ wszwmdmtitle</span><span class="sxs-lookup"><span data-stu-id="b4e53-165">g\_wszWMDMTitle</span></span>](metadata-constants.md)             |
| <span data-ttu-id="b4e53-166">ttl</span><span class="sxs-lookup"><span data-stu-id="b4e53-166">ttl</span></span>             | <span data-ttu-id="b4e53-167">Optional</span><span class="sxs-lookup"><span data-stu-id="b4e53-167">Optional</span></span>       | [<span data-ttu-id="b4e53-168">g \_ wszwmdmtimeeslive</span><span class="sxs-lookup"><span data-stu-id="b4e53-168">g\_wszWMDMTimeToLive</span></span>](metadata-constants.md)        |
| <span data-ttu-id="b4e53-169">webMaster</span><span class="sxs-lookup"><span data-stu-id="b4e53-169">webMaster</span></span>       | <span data-ttu-id="b4e53-170">Optional</span><span class="sxs-lookup"><span data-stu-id="b4e53-170">Optional</span></span>       | [<span data-ttu-id="b4e53-171">g \_ wszwmdmwebmaster</span><span class="sxs-lookup"><span data-stu-id="b4e53-171">g\_wszWMDMWebMaster</span></span>](metadata-constants.md)         |



 

<span data-ttu-id="b4e53-172">In der folgenden Tabelle sind die Bildelemente in einem RSS-Feed und die entsprechenden WMDM-Eigenschaften aufgeführt.</span><span class="sxs-lookup"><span data-stu-id="b4e53-172">The following table lists the image elements in an RSS feed and the corresponding WMDM properties.</span></span>



| <span data-ttu-id="b4e53-173">Image-Element</span><span class="sxs-lookup"><span data-stu-id="b4e53-173">Image element</span></span> | <span data-ttu-id="b4e53-174">Status</span><span class="sxs-lookup"><span data-stu-id="b4e53-174">Status</span></span>   | <span data-ttu-id="b4e53-175">Zugehörige Windows Media Device Manager-Eigenschaft</span><span class="sxs-lookup"><span data-stu-id="b4e53-175">Corresponding Windows Media Device Manager property</span></span> |
|---------------|----------|-----------------------------------------------------|
| <span data-ttu-id="b4e53-176">description</span><span class="sxs-lookup"><span data-stu-id="b4e53-176">description</span></span>   | <span data-ttu-id="b4e53-177">Optional</span><span class="sxs-lookup"><span data-stu-id="b4e53-177">Optional</span></span> | [<span data-ttu-id="b4e53-178">g \_ wszwmdmdescription</span><span class="sxs-lookup"><span data-stu-id="b4e53-178">g\_wszWMDMDescription</span></span>](metadata-constants.md)     |
| <span data-ttu-id="b4e53-179">height</span><span class="sxs-lookup"><span data-stu-id="b4e53-179">height</span></span>        | <span data-ttu-id="b4e53-180">Optional</span><span class="sxs-lookup"><span data-stu-id="b4e53-180">Optional</span></span> | [<span data-ttu-id="b4e53-181">g \_ wszwmdmheight</span><span class="sxs-lookup"><span data-stu-id="b4e53-181">g\_wszWMDMHeight</span></span>](metadata-constants.md)          |
| <span data-ttu-id="b4e53-182">link</span><span class="sxs-lookup"><span data-stu-id="b4e53-182">link</span></span>          | <span data-ttu-id="b4e53-183">Optional</span><span class="sxs-lookup"><span data-stu-id="b4e53-183">Optional</span></span> | [<span data-ttu-id="b4e53-184">g \_ wszwmdmdestinationurl</span><span class="sxs-lookup"><span data-stu-id="b4e53-184">g\_wszWMDMDestinationURL</span></span>](metadata-constants.md)  |
| <span data-ttu-id="b4e53-185">title</span><span class="sxs-lookup"><span data-stu-id="b4e53-185">title</span></span>         | <span data-ttu-id="b4e53-186">Optional</span><span class="sxs-lookup"><span data-stu-id="b4e53-186">Optional</span></span> | [<span data-ttu-id="b4e53-187">g \_ wszwmdmtitle</span><span class="sxs-lookup"><span data-stu-id="b4e53-187">g\_wszWMDMTitle</span></span>](metadata-constants.md)           |
| <span data-ttu-id="b4e53-188">url</span><span class="sxs-lookup"><span data-stu-id="b4e53-188">url</span></span>           | <span data-ttu-id="b4e53-189">Optional</span><span class="sxs-lookup"><span data-stu-id="b4e53-189">Optional</span></span> | [<span data-ttu-id="b4e53-190">g \_ wszwmdmsourceurl</span><span class="sxs-lookup"><span data-stu-id="b4e53-190">g\_wszWMDMSourceURL</span></span>](metadata-constants.md)       |
| <span data-ttu-id="b4e53-191">width</span><span class="sxs-lookup"><span data-stu-id="b4e53-191">width</span></span>         | <span data-ttu-id="b4e53-192">Optional</span><span class="sxs-lookup"><span data-stu-id="b4e53-192">Optional</span></span> | [<span data-ttu-id="b4e53-193">g \_ wszwmdmwidth</span><span class="sxs-lookup"><span data-stu-id="b4e53-193">g\_wszWMDMWidth</span></span>](metadata-constants.md)           |



 

<span data-ttu-id="b4e53-194">In der folgenden Tabelle sind die Element Elemente in einem RSS-Feed und die entsprechenden Eigenschaften des Windows Media-Device Manager aufgeführt.</span><span class="sxs-lookup"><span data-stu-id="b4e53-194">The following table lists the item elements in an RSS feed and the corresponding Windows Media Device Manager properties.</span></span>



| <span data-ttu-id="b4e53-195">Item-Element</span><span class="sxs-lookup"><span data-stu-id="b4e53-195">Item element</span></span> | <span data-ttu-id="b4e53-196">Attribut</span><span class="sxs-lookup"><span data-stu-id="b4e53-196">Attribute</span></span>   | <span data-ttu-id="b4e53-197">Status</span><span class="sxs-lookup"><span data-stu-id="b4e53-197">Status</span></span>         | <span data-ttu-id="b4e53-198">Zugehörige Windows Media Device Manager-Eigenschaft</span><span class="sxs-lookup"><span data-stu-id="b4e53-198">Corresponding Windows Media Device Manager property</span></span>            |
|--------------|-------------|----------------|----------------------------------------------------------------|
| <span data-ttu-id="b4e53-199">author</span><span class="sxs-lookup"><span data-stu-id="b4e53-199">author</span></span>       |             | <span data-ttu-id="b4e53-200">Optional</span><span class="sxs-lookup"><span data-stu-id="b4e53-200">Optional</span></span>       | [<span data-ttu-id="b4e53-201">g \_ wszwmdmauthor</span><span class="sxs-lookup"><span data-stu-id="b4e53-201">g\_wszWMDMAuthor</span></span>](metadata-constants.md)                     |
| <span data-ttu-id="b4e53-202">category</span><span class="sxs-lookup"><span data-stu-id="b4e53-202">category</span></span>     |             | <span data-ttu-id="b4e53-203">Optional</span><span class="sxs-lookup"><span data-stu-id="b4e53-203">Optional</span></span>       | [<span data-ttu-id="b4e53-204">g \_ wszwmdmgenre</span><span class="sxs-lookup"><span data-stu-id="b4e53-204">g\_wszWMDMGenre</span></span>](metadata-constants.md)                      |
|              | <span data-ttu-id="b4e53-205">Domäne</span><span class="sxs-lookup"><span data-stu-id="b4e53-205">domain</span></span>      | <span data-ttu-id="b4e53-206">Nicht verfügbar</span><span class="sxs-lookup"><span data-stu-id="b4e53-206">Not applicable</span></span> | <span data-ttu-id="b4e53-207">Nicht verfügbar</span><span class="sxs-lookup"><span data-stu-id="b4e53-207">Not applicable</span></span>                                                 |
| <span data-ttu-id="b4e53-208">description</span><span class="sxs-lookup"><span data-stu-id="b4e53-208">description</span></span>  |             | <span data-ttu-id="b4e53-209">Optional</span><span class="sxs-lookup"><span data-stu-id="b4e53-209">Optional</span></span>       | [<span data-ttu-id="b4e53-210">g \_ wszwmdmdescription</span><span class="sxs-lookup"><span data-stu-id="b4e53-210">g\_wszWMDMDescription</span></span>](metadata-constants.md)                |
| <span data-ttu-id="b4e53-211">ungs</span><span class="sxs-lookup"><span data-stu-id="b4e53-211">enclosure</span></span>    |             | <span data-ttu-id="b4e53-212">Optional</span><span class="sxs-lookup"><span data-stu-id="b4e53-212">Optional</span></span>       | <span data-ttu-id="b4e53-213">Nicht verfügbar</span><span class="sxs-lookup"><span data-stu-id="b4e53-213">Not applicable</span></span>                                                 |
|              | <span data-ttu-id="b4e53-214">length</span><span class="sxs-lookup"><span data-stu-id="b4e53-214">length</span></span>      | <span data-ttu-id="b4e53-215">Erforderlich</span><span class="sxs-lookup"><span data-stu-id="b4e53-215">Required</span></span>       | [<span data-ttu-id="b4e53-216">g \_ wszwmdmfilesize</span><span class="sxs-lookup"><span data-stu-id="b4e53-216">g\_wszWMDMFileSize</span></span>](metadata-constants.md)                   |
|              | <span data-ttu-id="b4e53-217">type</span><span class="sxs-lookup"><span data-stu-id="b4e53-217">type</span></span>        | <span data-ttu-id="b4e53-218">Erforderlich</span><span class="sxs-lookup"><span data-stu-id="b4e53-218">Required</span></span>       | <span data-ttu-id="b4e53-219">(Der MIME-Typ sollte dem Eigenschafts Inhaltstyp zugeordnet werden.)</span><span class="sxs-lookup"><span data-stu-id="b4e53-219">(The MIME type should be mapped to the property content type.)</span></span> |
|              | <span data-ttu-id="b4e53-220">url</span><span class="sxs-lookup"><span data-stu-id="b4e53-220">url</span></span>         | <span data-ttu-id="b4e53-221">Erforderlich</span><span class="sxs-lookup"><span data-stu-id="b4e53-221">Required</span></span>       | [<span data-ttu-id="b4e53-222">g \_ wszwmdmsourceurl</span><span class="sxs-lookup"><span data-stu-id="b4e53-222">g\_wszWMDMSourceURL</span></span>](metadata-constants.md)                  |
| <span data-ttu-id="b4e53-223">guid</span><span class="sxs-lookup"><span data-stu-id="b4e53-223">guid</span></span>         |             | <span data-ttu-id="b4e53-224">Optional</span><span class="sxs-lookup"><span data-stu-id="b4e53-224">Optional</span></span>       | [<span data-ttu-id="b4e53-225">g \_ wszwmdmediaguid</span><span class="sxs-lookup"><span data-stu-id="b4e53-225">g\_wszWMDMediaGuid</span></span>](metadata-constants.md)                   |
|              | <span data-ttu-id="b4e53-226">ispermalink</span><span class="sxs-lookup"><span data-stu-id="b4e53-226">isPermaLink</span></span> | <span data-ttu-id="b4e53-227">Nicht verfügbar</span><span class="sxs-lookup"><span data-stu-id="b4e53-227">Not applicable</span></span> | <span data-ttu-id="b4e53-228">Nicht verfügbar</span><span class="sxs-lookup"><span data-stu-id="b4e53-228">Not applicable</span></span>                                                 |
| <span data-ttu-id="b4e53-229">link</span><span class="sxs-lookup"><span data-stu-id="b4e53-229">link</span></span>         |             | <span data-ttu-id="b4e53-230">Optional</span><span class="sxs-lookup"><span data-stu-id="b4e53-230">Optional</span></span>       | [<span data-ttu-id="b4e53-231">g \_ wszwmdmdestinationurl</span><span class="sxs-lookup"><span data-stu-id="b4e53-231">g\_wszWMDMDestinationURL</span></span>](metadata-constants.md)             |
| <span data-ttu-id="b4e53-232">pubDate</span><span class="sxs-lookup"><span data-stu-id="b4e53-232">pubDate</span></span>      |             | <span data-ttu-id="b4e53-233">Optional</span><span class="sxs-lookup"><span data-stu-id="b4e53-233">Optional</span></span>       | [<span data-ttu-id="b4e53-234">g \_ wszwmdmyear</span><span class="sxs-lookup"><span data-stu-id="b4e53-234">g\_wszWMDMYear</span></span>](metadata-constants.md)                       |
| <span data-ttu-id="b4e53-235">source</span><span class="sxs-lookup"><span data-stu-id="b4e53-235">source</span></span>       |             | <span data-ttu-id="b4e53-236">Nicht verfügbar</span><span class="sxs-lookup"><span data-stu-id="b4e53-236">Not applicable</span></span> | <span data-ttu-id="b4e53-237">Nicht verfügbar</span><span class="sxs-lookup"><span data-stu-id="b4e53-237">Not applicable</span></span>                                                 |
| <span data-ttu-id="b4e53-238">title</span><span class="sxs-lookup"><span data-stu-id="b4e53-238">title</span></span>        |             | <span data-ttu-id="b4e53-239">Optional</span><span class="sxs-lookup"><span data-stu-id="b4e53-239">Optional</span></span>       | [<span data-ttu-id="b4e53-240">g \_ wszwmdmtitle</span><span class="sxs-lookup"><span data-stu-id="b4e53-240">g\_wszWMDMTitle</span></span>](metadata-constants.md)                      |



 

<span data-ttu-id="b4e53-241">Beispiel</span><span class="sxs-lookup"><span data-stu-id="b4e53-241">Example</span></span>

<span data-ttu-id="b4e53-242">Das folgende Beispiel zeigt einen kompletten RSS-Feed für einen fiktiven Podcast, der vom CEO eines Veröffentlichungs Unternehmens bereitgestellt wird.</span><span class="sxs-lookup"><span data-stu-id="b4e53-242">The following example shows a complete RSS feed for a fictitious podcast supplied by the CEO of a publishing company.</span></span>


```C++
<channel>
    <title>The Digital Publication</title>
    <link>https://www.lucernepublishing.com/podcasting</link>
    <description>Lucerne Publishing CEO Peter Bankov takes a look at the latest trends in online publications.</description>
    <language>en-us</language>
    <copyright>2006 Lucerne Publishing LP, LLLP. All Rights Reserved.</copyright>
    <managingEditor>someone@example.com</managingEditor>
    <webMaster>someone@example.com</webMaster>
    <pubDate>Fri, 9 June 2006 14:00:28 EDT</pubDate>
    <lastBuildDate Fri, 9 June 2006 14:00:28 EDT />
    <category>News</category>
    <generator>Podcaster version 1.0</generator>
    <docs>https://www.lucernepublishing.com/tech/rss</docs>
    <cloud />
    <ttl>240</ttl>
    <rating />
    <textInput />
    <skipHours />
    <skipDays />

<image>
     <url>https://www.lucernepublishing.com/images/logo.gif</url>
     <title>Lucerne Publishing</title>
     <link>https://www.lucernepublishing.com/community/podcasts</link>
     <width>300</width>
     <height>300</height>
     <description>Lucerne Logo</description>
</image>

<item>
    <title>The Digital Publication</title>
    <link>https://www.lucernepublishing/services/podcasting/digital.publishing/audio/2006/06/digital0601.mp3</link>
    <description>Online publications are rapidly changing. A publishing house CEO examines the trends of the past five years and their implications.</description>
    <author>Lucerne</author>
    <category>News</category>
    <comments />
    <enclosure url="https://www.lucernepublishing/services/podcasting/digital.publishing/audio/2006/06/digital0601.mp3" length="10329011" type="audio/mpeg" />
    <guid>https://www.lucernepublishing/services/podcasting/digital.publishing/audio/2006/06/digital0601.mp3</guid>
    <pubDate>Thur, 1 June 2006 14:00:28 EDT</pubDate>
    <source />
</item>

</channel>
```



<span data-ttu-id="b4e53-243">Zuordnung von RSS-Channel-Elementen zu Windows Media Device Manager-Eigenschafts Werten</span><span class="sxs-lookup"><span data-stu-id="b4e53-243">Mapping of RSS Channel Elements to Windows Media Device Manager Property Values</span></span>

<span data-ttu-id="b4e53-244">In der folgenden Tabelle wird beschrieben, wie die Werte in den RSS-channelelementen im vorherigen Beispiel bestimmten Windows Media Device Manager-Eigenschaften zugeordnet werden.</span><span class="sxs-lookup"><span data-stu-id="b4e53-244">The following table describes how the values in the RSS Channel elements in the previous example map to particular Windows Media Device Manager properties.</span></span>



| <span data-ttu-id="b4e53-245">Windows Media Device Manager-Eigenschaft</span><span class="sxs-lookup"><span data-stu-id="b4e53-245">Windows Media Device Manager property</span></span>                    | <span data-ttu-id="b4e53-246">Wert</span><span class="sxs-lookup"><span data-stu-id="b4e53-246">Value</span></span>                                                                                         |
|----------------------------------------------------------|-----------------------------------------------------------------------------------------------|
| [<span data-ttu-id="b4e53-247">g \_ wszwmdmauthordate</span><span class="sxs-lookup"><span data-stu-id="b4e53-247">g\_wszWMDMAuthorDate</span></span>](metadata-constants.md)           | <span data-ttu-id="b4e53-248">Fr, 9. Juni 2006 14:00:28 (EDT)</span><span class="sxs-lookup"><span data-stu-id="b4e53-248">Fri, 9 June 2006 14:00:28 EDT</span></span>                                                                 |
| [<span data-ttu-id="b4e53-249">g \_ wszwmdmdescription</span><span class="sxs-lookup"><span data-stu-id="b4e53-249">g\_wszWMDMDESCRIPTION</span></span>](metadata-constants.md)          | <span data-ttu-id="b4e53-250">Lucerne Publishing CEO Peter Bankow befasst sich mit den neuesten Trends in Online Veröffentlichungen.</span><span class="sxs-lookup"><span data-stu-id="b4e53-250">Lucerne Publishing CEO Peter Bankov takes a look at the latest trends in online publications.</span></span> |
| [<span data-ttu-id="b4e53-251">g \_ wszwmdmdestination- \_ URL</span><span class="sxs-lookup"><span data-stu-id="b4e53-251">g\_wszWMDMDESTINATION\_URL</span></span>](metadata-constants.md)     | https://www.lucernepublishing/services/podcasting                                              |
| [<span data-ttu-id="b4e53-252">g \_ wszwmdmeditor</span><span class="sxs-lookup"><span data-stu-id="b4e53-252">g\_wszWMDMEDITOR</span></span>](metadata-constants.md)               | someone@example.com                                                                           |
| [<span data-ttu-id="b4e53-253">g \_ wszwmdmfilekreationdate</span><span class="sxs-lookup"><span data-stu-id="b4e53-253">g\_wszWMDMFileCreationDate</span></span>](metadata-constants.md)     | <span data-ttu-id="b4e53-254">Fr, 9. Juni 2006 14:00:28 (EDT)</span><span class="sxs-lookup"><span data-stu-id="b4e53-254">Fri, 9 June 2006 14:00:28 EDT</span></span>                                                                 |
| [<span data-ttu-id="b4e53-255">g \_ wszwmdmfilename</span><span class="sxs-lookup"><span data-stu-id="b4e53-255">g\_wszWMDMFileName</span></span>](metadata-constants.md)             | <span data-ttu-id="b4e53-256">Die digitale Veröffentlichung</span><span class="sxs-lookup"><span data-stu-id="b4e53-256">The Digital Publication</span></span>                                                                       |
| [<span data-ttu-id="b4e53-257">g \_ wszwmdmfilesize</span><span class="sxs-lookup"><span data-stu-id="b4e53-257">g\_wszWMDMFileSize</span></span>](metadata-constants.md)             | <span data-ttu-id="b4e53-258">13.790</span><span class="sxs-lookup"><span data-stu-id="b4e53-258">13,790</span></span>                                                                                        |
| [<span data-ttu-id="b4e53-259">g \_ wszwmdmformatcode</span><span class="sxs-lookup"><span data-stu-id="b4e53-259">g\_wszWMDMFormatCode</span></span>](metadata-constants.md)           | <span data-ttu-id="b4e53-260">WMDM- \_ Formatcode- \_ Medien Umwandlung \_</span><span class="sxs-lookup"><span data-stu-id="b4e53-260">WMDM\_FORMATCODE\_MEDIA\_CAST</span></span>                                                                 |
| [<span data-ttu-id="b4e53-261">g \_ wszwmdmgenre</span><span class="sxs-lookup"><span data-stu-id="b4e53-261">g\_wszWMDMGENRE</span></span>](metadata-constants.md)                | <span data-ttu-id="b4e53-262">News</span><span class="sxs-lookup"><span data-stu-id="b4e53-262">News</span></span>                                                                                          |
| [<span data-ttu-id="b4e53-263">g \_ wszwmdmlast-Änderungs \_ \_ Datum</span><span class="sxs-lookup"><span data-stu-id="b4e53-263">g\_wszWMDMLAST\_MODIFIED\_DATE</span></span>](metadata-constants.md) | <span data-ttu-id="b4e53-264">Fr, 9. Juni 2006 14:00:28 (EDT)</span><span class="sxs-lookup"><span data-stu-id="b4e53-264">Fri, 9 June 2006 14:00:28 EDT</span></span>                                                                 |
| [<span data-ttu-id="b4e53-265">g \_ wszwmdmlastmodifieddate</span><span class="sxs-lookup"><span data-stu-id="b4e53-265">g\_wszWMDMLastModifiedDate</span></span>](metadata-constants.md)     | <span data-ttu-id="b4e53-266">Fr, 9. Juni 2006 14:00:28 (EDT)</span><span class="sxs-lookup"><span data-stu-id="b4e53-266">Fri, 9 June 2006 14:00:28 EDT</span></span>                                                                 |
| [<span data-ttu-id="b4e53-267">g \_ wszwmdmprovidercopyright</span><span class="sxs-lookup"><span data-stu-id="b4e53-267">g\_wszWMDMProviderCopyright</span></span>](metadata-constants.md)    | <span data-ttu-id="b4e53-268">2006 Lucerne Publishing LP, LLLP.</span><span class="sxs-lookup"><span data-stu-id="b4e53-268">2006 Lucerne Publishing LP, LLLP.</span></span> <span data-ttu-id="b4e53-269">Alle Rechte vorbehalten.</span><span class="sxs-lookup"><span data-stu-id="b4e53-269">All Rights Reserved.</span></span>                                        |
| [<span data-ttu-id="b4e53-270">g \_ wszwmdmtimeeslive</span><span class="sxs-lookup"><span data-stu-id="b4e53-270">g\_wszWMDMTimeToLive</span></span>](metadata-constants.md)           | <span data-ttu-id="b4e53-271">240</span><span class="sxs-lookup"><span data-stu-id="b4e53-271">240</span></span>                                                                                           |
| [<span data-ttu-id="b4e53-272">g \_ wszwmdmtitle</span><span class="sxs-lookup"><span data-stu-id="b4e53-272">g\_wszWMDMTitle</span></span>](metadata-constants.md)                | <span data-ttu-id="b4e53-273">Die digitale Veröffentlichung</span><span class="sxs-lookup"><span data-stu-id="b4e53-273">The Digital Publication</span></span>                                                                       |
| [<span data-ttu-id="b4e53-274">g \_ wszwmdmwebmaster</span><span class="sxs-lookup"><span data-stu-id="b4e53-274">g\_wszWMDMWEBMASTER</span></span>](metadata-constants.md)            | someone@example.com                                                                           |
| [<span data-ttu-id="b4e53-275">g \_ wszwmdmyear</span><span class="sxs-lookup"><span data-stu-id="b4e53-275">g\_wszWMDMYear</span></span>](metadata-constants.md)                 | <span data-ttu-id="b4e53-276">Fr, 9. Juni 2006 14:00:28 (EDT)</span><span class="sxs-lookup"><span data-stu-id="b4e53-276">Fri, 9 June 2006 14:00:28 EDT</span></span>                                                                 |



 

<span data-ttu-id="b4e53-277">Zuordnung von RSS-Bildelementen zu Windows Media Device Manager-Eigenschafts Werten</span><span class="sxs-lookup"><span data-stu-id="b4e53-277">Mapping of RSS Image Elements to Windows Media Device Manager Property Values</span></span>

<span data-ttu-id="b4e53-278">In der folgenden Tabelle wird beschrieben, wie die Werte in den RSS-Bildelementen im vorherigen Beispiel bestimmten Windows Media Device Manager-Eigenschaften zugeordnet werden.</span><span class="sxs-lookup"><span data-stu-id="b4e53-278">The following table describes how the values in the RSS Image elements in the previous example map to particular Windows Media Device Manager properties.</span></span>



| <span data-ttu-id="b4e53-279">Windows Media Device Manager-Eigenschaft</span><span class="sxs-lookup"><span data-stu-id="b4e53-279">Windows Media Device Manager property</span></span>                | <span data-ttu-id="b4e53-280">Wert</span><span class="sxs-lookup"><span data-stu-id="b4e53-280">Value</span></span>                                            |
|------------------------------------------------------|--------------------------------------------------|
| [<span data-ttu-id="b4e53-281">g \_ wszwmdmalbumcoverformat</span><span class="sxs-lookup"><span data-stu-id="b4e53-281">g\_wszWMDMAlbumCoverFormat</span></span>](metadata-constants.md) | <span data-ttu-id="b4e53-282">WPD- \_ Objekt \_ Format \_ GIF</span><span class="sxs-lookup"><span data-stu-id="b4e53-282">WPD\_OBJECT\_FORMAT\_GIF</span></span>                         |
| [<span data-ttu-id="b4e53-283">g \_ wszwmdmalbumcoversize</span><span class="sxs-lookup"><span data-stu-id="b4e53-283">g\_wszWMDMAlbumCoverSize</span></span>](metadata-constants.md)   | <span data-ttu-id="b4e53-284">512</span><span class="sxs-lookup"><span data-stu-id="b4e53-284">512</span></span>                                              |
| [<span data-ttu-id="b4e53-285">g \_ wszwmdmdescription</span><span class="sxs-lookup"><span data-stu-id="b4e53-285">g\_wszWMDMDescription</span></span>](metadata-constants.md)      | <span data-ttu-id="b4e53-286">Lucerne-Logo</span><span class="sxs-lookup"><span data-stu-id="b4e53-286">Lucerne Logo</span></span>                                     |
| [<span data-ttu-id="b4e53-287">g \_ wszwmdmdestinationurl</span><span class="sxs-lookup"><span data-stu-id="b4e53-287">g\_wszWMDMDestinationURL</span></span>](metadata-constants.md)   | <span data-ttu-id="b4e53-288">www.lucernepublishing.com/community/podcasts</span><span class="sxs-lookup"><span data-stu-id="b4e53-288">//www.lucernepublishing.com/community/podcasts</span></span>   |
| [<span data-ttu-id="b4e53-289">g \_ wszwmdmheight</span><span class="sxs-lookup"><span data-stu-id="b4e53-289">g\_wszWMDMHeight</span></span>](metadata-constants.md)           | <span data-ttu-id="b4e53-290">300</span><span class="sxs-lookup"><span data-stu-id="b4e53-290">300</span></span>                                              |
| [<span data-ttu-id="b4e53-291">g \_ wszwmdmsourceurl</span><span class="sxs-lookup"><span data-stu-id="b4e53-291">g\_wszWMDMSourceURL</span></span>](metadata-constants.md)        | https://www.lucernepublishing.com/images/logo.gif |
| [<span data-ttu-id="b4e53-292">g \_ wszwmdmtitle</span><span class="sxs-lookup"><span data-stu-id="b4e53-292">g\_wszWMDMTitle</span></span>](metadata-constants.md)            | <span data-ttu-id="b4e53-293">Lucerne Publishing</span><span class="sxs-lookup"><span data-stu-id="b4e53-293">Lucerne Publishing</span></span>                               |
| [<span data-ttu-id="b4e53-294">g \_ wszwmdmwidth</span><span class="sxs-lookup"><span data-stu-id="b4e53-294">g\_wszWMDMWidth</span></span>](metadata-constants.md)            | <span data-ttu-id="b4e53-295">300</span><span class="sxs-lookup"><span data-stu-id="b4e53-295">300</span></span>                                              |



 

<span data-ttu-id="b4e53-296">Zuordnung von RSS-Element Elementen zu Windows Media Device Manager-Eigenschafts Werten</span><span class="sxs-lookup"><span data-stu-id="b4e53-296">Mapping of RSS Item Elements to Windows Media Device Manager Property Values</span></span>

<span data-ttu-id="b4e53-297">In der folgenden Tabelle wird beschrieben, wie die Werte in den RSS-Element Elementen im vorherigen Beispiel bestimmten Windows Media Device Manager-Eigenschaften zugeordnet werden.</span><span class="sxs-lookup"><span data-stu-id="b4e53-297">The following table describes how the values in the RSS Item elements in the previous example map to particular Windows Media Device Manager properties.</span></span>



| <span data-ttu-id="b4e53-298">Windows Media Device Manager-Eigenschaft</span><span class="sxs-lookup"><span data-stu-id="b4e53-298">Windows Media Device Manager property</span></span>                | <span data-ttu-id="b4e53-299">Wert</span><span class="sxs-lookup"><span data-stu-id="b4e53-299">Value</span></span>                                                                                                                               |
|------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="b4e53-300">g \_ wszwmdmauthor</span><span class="sxs-lookup"><span data-stu-id="b4e53-300">g\_wszWMDMAuthor</span></span>](metadata-constants.md)           | <span data-ttu-id="b4e53-301">Luzerner</span><span class="sxs-lookup"><span data-stu-id="b4e53-301">Lucerne</span></span>                                                                                                                             |
| [<span data-ttu-id="b4e53-302">g \_ wszwmdmauthordate</span><span class="sxs-lookup"><span data-stu-id="b4e53-302">g\_wszWMDMAuthorDate</span></span>](metadata-constants.md)       | <span data-ttu-id="b4e53-303">Thur, 1. Juni 2006 14:00:28 (EDT)</span><span class="sxs-lookup"><span data-stu-id="b4e53-303">Thur, 1 June 2006 14:00:28 EDT</span></span>                                                                                                      |
| [<span data-ttu-id="b4e53-304">g \_ wszwmdmdescription</span><span class="sxs-lookup"><span data-stu-id="b4e53-304">g\_wszWMDMDescription</span></span>](metadata-constants.md)      | <span data-ttu-id="b4e53-305">Online Veröffentlichungen werden rasch geändert.</span><span class="sxs-lookup"><span data-stu-id="b4e53-305">Online publications are rapidly changing.</span></span> <span data-ttu-id="b4e53-306">Ein Publishing House-CEO untersucht die Trends der letzten fünf Jahre und deren Auswirkungen.</span><span class="sxs-lookup"><span data-stu-id="b4e53-306">A publishing house CEO examines the trends of the past five years and their implications.</span></span> |
| [<span data-ttu-id="b4e53-307">g \_ wszwmdmdestinationurl</span><span class="sxs-lookup"><span data-stu-id="b4e53-307">g\_wszWMDMDestinationURL</span></span>](metadata-constants.md)   | https://www.lucernepublishing/services/podcasting/digital.publishing/audio/2006/06/digital0601.mp3                                   |
| [<span data-ttu-id="b4e53-308">g \_ wszwmdmduration</span><span class="sxs-lookup"><span data-stu-id="b4e53-308">g\_wszWMDMDuration</span></span>](metadata-constants.md)         | <span data-ttu-id="b4e53-309">120325445</span><span class="sxs-lookup"><span data-stu-id="b4e53-309">120325445</span></span>                                                                                                                           |
| [<span data-ttu-id="b4e53-310">g \_ wszwmdmfilekreationdate</span><span class="sxs-lookup"><span data-stu-id="b4e53-310">g\_wszWMDMFileCreationDate</span></span>](metadata-constants.md) | <span data-ttu-id="b4e53-311">Thur, 1. Juni 2006 14:00:28 (EDT)</span><span class="sxs-lookup"><span data-stu-id="b4e53-311">Thur, 1 June 2006 14:00:28 EDT</span></span>                                                                                                      |
| [<span data-ttu-id="b4e53-312">g \_ wszwmdmfilesize</span><span class="sxs-lookup"><span data-stu-id="b4e53-312">g\_wszWMDMFileSize</span></span>](metadata-constants.md)         | <span data-ttu-id="b4e53-313">10329011</span><span class="sxs-lookup"><span data-stu-id="b4e53-313">10329011</span></span>                                                                                                                            |
| [<span data-ttu-id="b4e53-314">g \_ wszwmdmformatcode</span><span class="sxs-lookup"><span data-stu-id="b4e53-314">g\_wszWMDMFormatCode</span></span>](metadata-constants.md)       | <span data-ttu-id="b4e53-315">WMDM \_ Formatcode \_ MP3</span><span class="sxs-lookup"><span data-stu-id="b4e53-315">WMDM\_FORMATCODE\_MP3</span></span>                                                                                                               |
| [<span data-ttu-id="b4e53-316">g \_ wszwmdmgenre</span><span class="sxs-lookup"><span data-stu-id="b4e53-316">g\_wszWMDMGenre</span></span>](metadata-constants.md)            | <span data-ttu-id="b4e53-317">News</span><span class="sxs-lookup"><span data-stu-id="b4e53-317">News</span></span>                                                                                                                                |
| [<span data-ttu-id="b4e53-318">g \_ wszwmdmlastmodifieddate</span><span class="sxs-lookup"><span data-stu-id="b4e53-318">g\_wszWMDMLastModifiedDate</span></span>](metadata-constants.md) | <span data-ttu-id="b4e53-319">Thur, 1. Juni 2006 14:00:28 (EDT)</span><span class="sxs-lookup"><span data-stu-id="b4e53-319">Thur, 1 June 2006 14:00:28 EDT</span></span>                                                                                                      |
| [<span data-ttu-id="b4e53-320">g \_ wszwmdmmediaguid</span><span class="sxs-lookup"><span data-stu-id="b4e53-320">g\_wszWMDMMediaGuid</span></span>](metadata-constants.md)        | https://www.lucernepublishing/services/podcasting/digital.publishing/audio/2006/06/digital0601.mp3                                   |
| [<span data-ttu-id="b4e53-321">g \_ wszwmdmsourceurl</span><span class="sxs-lookup"><span data-stu-id="b4e53-321">g\_wszWMDMSourceURL</span></span>](metadata-constants.md)        | https://www.lucernepublishing/services/podcasting/digital.publishing/audio/2006/06/digital0601.mp3                                   |
| [<span data-ttu-id="b4e53-322">g \_ wszwmdmtitle</span><span class="sxs-lookup"><span data-stu-id="b4e53-322">g\_wszWMDMTitle</span></span>](metadata-constants.md)            | <span data-ttu-id="b4e53-323">Die digitale Veröffentlichung</span><span class="sxs-lookup"><span data-stu-id="b4e53-323">The Digital Publication</span></span>                                                                                                             |
| [<span data-ttu-id="b4e53-324">g \_ wszwmdmyear</span><span class="sxs-lookup"><span data-stu-id="b4e53-324">g\_wszWMDMYear</span></span>](metadata-constants.md)             | <span data-ttu-id="b4e53-325">Thur, 1. Juni 2006 14:00:28 (EDT)</span><span class="sxs-lookup"><span data-stu-id="b4e53-325">Thur, 1 June 2006 14:00:28 EDT</span></span>                                                                                                      |



 

## <a name="related-topics"></a><span data-ttu-id="b4e53-326">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="b4e53-326">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="b4e53-327">**Metadatenkonstanten**</span><span class="sxs-lookup"><span data-stu-id="b4e53-327">**Metadata Constants**</span></span>](metadata-constants.md)
</dt> </dl>

 

 




