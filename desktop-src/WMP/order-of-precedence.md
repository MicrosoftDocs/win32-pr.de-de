---
title: Rangfolge
description: Rangfolge
ms.assetid: 3865ea8a-2489-4714-9a05-d1082589841f
keywords:
- Windows Media-Metadateien, Rangfolge
- Windows Media-Metadateien, Rangfolge
- Metadateien, Rangfolge
- Metadateien, Rangfolge
- Windows Media, Metafiles
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 9161d1e43f61ae1b1a7231c640e33c4c6ec6527f
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "104036615"
---
# <a name="order-of-precedence"></a><span data-ttu-id="6fb7f-108">Rangfolge</span><span class="sxs-lookup"><span data-stu-id="6fb7f-108">Order of Precedence</span></span>

<span data-ttu-id="6fb7f-109">Nicht alle Metadatei-Element Attribute werden gleich erstellt.</span><span class="sxs-lookup"><span data-stu-id="6fb7f-109">Not all metafile element attributes are created equal.</span></span> <span data-ttu-id="6fb7f-110">Einige Metadatei-Element Attribute überschreiben andere Element Attribute.</span><span class="sxs-lookup"><span data-stu-id="6fb7f-110">Some metafile element attributes override other element attributes.</span></span> <span data-ttu-id="6fb7f-111">Element Attribute können von ähnlichen Element Attributen abhängig von Position und Reihenfolge überschrieben werden.</span><span class="sxs-lookup"><span data-stu-id="6fb7f-111">Element attributes can be overridden by similar element attributes depending on position and order.</span></span> <span data-ttu-id="6fb7f-112">Alle Attribute einer metadateiwiedergabe Liste überschreiben diejenigen, die in einer referenzierten Windows-Mediendatei enthalten sind.</span><span class="sxs-lookup"><span data-stu-id="6fb7f-112">Any attributes of a metafile playlist override those contained in a referenced Windows Media file.</span></span> <span data-ttu-id="6fb7f-113">Ein Attribut, das eine andere überschreibt, hat eine höhere Rangfolge.</span><span class="sxs-lookup"><span data-stu-id="6fb7f-113">An attribute that overrides another has higher precedence.</span></span>

<span data-ttu-id="6fb7f-114">In der folgenden Tabelle wird die Hierarchie mit der höchsten Rangfolge als der niedrigste Wert angezeigt.</span><span class="sxs-lookup"><span data-stu-id="6fb7f-114">The hierarchy, highest precedence to lowest, is shown in the following table.</span></span> <span data-ttu-id="6fb7f-115">Das Element mit der höchsten Rangfolge wird nie überschrieben.</span><span class="sxs-lookup"><span data-stu-id="6fb7f-115">The highest precedence item is never overridden.</span></span>



| <span data-ttu-id="6fb7f-116">Bereich</span><span class="sxs-lookup"><span data-stu-id="6fb7f-116">Scope</span></span>                    | <span data-ttu-id="6fb7f-117">Hierarchy</span><span class="sxs-lookup"><span data-stu-id="6fb7f-117">Hierarchy</span></span>                                   |
|--------------------------|---------------------------------------------|
| <span data-ttu-id="6fb7f-118">"Signierter DRM-Inhalt"</span><span class="sxs-lookup"><span data-stu-id="6fb7f-118">"Signed DRM content"</span></span>     | <span data-ttu-id="6fb7f-119">Nie überschrieben.</span><span class="sxs-lookup"><span data-stu-id="6fb7f-119">Never overridden.</span></span>                           |
| <span data-ttu-id="6fb7f-120">Verweis **Element Bereich**</span><span class="sxs-lookup"><span data-stu-id="6fb7f-120">**REF** element scope</span></span>    | <span data-ttu-id="6fb7f-121">Wird nur von signiertem DRM-Inhalt überschrieben.</span><span class="sxs-lookup"><span data-stu-id="6fb7f-121">Only overridden by signed DRM content.</span></span>      |
| <span data-ttu-id="6fb7f-122">Bereich des **Einstiegs** Elements</span><span class="sxs-lookup"><span data-stu-id="6fb7f-122">**ENTRY** element scope</span></span>  | <span data-ttu-id="6fb7f-123">Überschreibt Elemente der unten aufgeführten Kategorien.</span><span class="sxs-lookup"><span data-stu-id="6fb7f-123">Overrides elements of the categories below.</span></span> |
| <span data-ttu-id="6fb7f-124">Bereich von **ASX**</span><span class="sxs-lookup"><span data-stu-id="6fb7f-124">**ASX** scope</span></span>            | <span data-ttu-id="6fb7f-125">Überschreibt Mediendatei Elemente.</span><span class="sxs-lookup"><span data-stu-id="6fb7f-125">Overrides media file elements.</span></span>              |
| <span data-ttu-id="6fb7f-126">Windows Media-Datei Bereich</span><span class="sxs-lookup"><span data-stu-id="6fb7f-126">Windows Media file scope</span></span> | <span data-ttu-id="6fb7f-127">Überschrieben von allen oben genannten.</span><span class="sxs-lookup"><span data-stu-id="6fb7f-127">Overridden by all of the above.</span></span>             |



 

-   <span data-ttu-id="6fb7f-128">"Signierter DRM-Inhalt"-digitales Signatur Objekt.</span><span class="sxs-lookup"><span data-stu-id="6fb7f-128">"Signed DRM content" - Digital signature object.</span></span>

    <span data-ttu-id="6fb7f-129">Attribute von signiertem DRM-Inhalt überschreiben alle anderen.</span><span class="sxs-lookup"><span data-stu-id="6fb7f-129">Attributes of Signed DRM content will override all others.</span></span> <span data-ttu-id="6fb7f-130">Beispielsweise werden die Copyright Informationen von "signiertem DRM-Inhalt" nicht überschrieben.</span><span class="sxs-lookup"><span data-stu-id="6fb7f-130">For example, the Copyright information of "Signed DRM content" will not be overridden.</span></span> <span data-ttu-id="6fb7f-131">Sie wird immer gestreamt und präsentiert.</span><span class="sxs-lookup"><span data-stu-id="6fb7f-131">It will always be streamed and presented.</span></span>

-   <span data-ttu-id="6fb7f-132">Verweis **Element Bereich**</span><span class="sxs-lookup"><span data-stu-id="6fb7f-132">**REF** element scope</span></span>

    <span data-ttu-id="6fb7f-133">Attribute des **ref** -Elements überschreiben andere Element Attribute, aber keinen signierten DRM-Inhalt.</span><span class="sxs-lookup"><span data-stu-id="6fb7f-133">Attributes of the **REF** element will override other element attributes, but not signed DRM content.</span></span>

-   <span data-ttu-id="6fb7f-134">**Einstiegs** Bereich</span><span class="sxs-lookup"><span data-stu-id="6fb7f-134">**ENTRY** scope</span></span>

    <span data-ttu-id="6fb7f-135">Attribute des **Entry** -Elements werden durch das **ref** -Element Attribut überschrieben, überschreiben jedoch andere Element Attribute.</span><span class="sxs-lookup"><span data-stu-id="6fb7f-135">Attributes of the **ENTRY** element will be overridden by the **REF** element attribute but will override other element attributes.</span></span> <span data-ttu-id="6fb7f-136">Anstelle der Titelinformationen aus der Mediendatei werden **Titel** Metadaten aus dem **Entry** -Element angezeigt.</span><span class="sxs-lookup"><span data-stu-id="6fb7f-136">**TITLE** metadata from the **ENTRY** element is displayed instead of the title information from the media file.</span></span>

-   <span data-ttu-id="6fb7f-137">Bereich von **ASX**</span><span class="sxs-lookup"><span data-stu-id="6fb7f-137">**ASX** scope</span></span>

    <span data-ttu-id="6fb7f-138">Alle Eigenschaften, die in der Metadatei eingegeben werden, überschreiben diejenigen, die in der Windows Media-Datei enthalten sind.</span><span class="sxs-lookup"><span data-stu-id="6fb7f-138">Any properties that are entered in the metafile override those contained in the Windows Media file.</span></span> <span data-ttu-id="6fb7f-139">Attribute des **Entry** -Elements überschreiben die **ASX** -Element Attribute.</span><span class="sxs-lookup"><span data-stu-id="6fb7f-139">Attributes of the **ENTRY** element override **ASX** element attributes.</span></span> <span data-ttu-id="6fb7f-140">Während der referenzierte Medien Clip des **Eintrags** Elements abgespielt wird, werden **Titel** Metadaten aus dem **Entry** -Element anstelle von Titelinformationen **aus dem-** Element des-Elements angezeigt.</span><span class="sxs-lookup"><span data-stu-id="6fb7f-140">While the **ENTRY** element's referenced media clip is playing, **TITLE** metadata from the **ENTRY** element is displayed instead of title information from the **ASX** element.</span></span>

-   <span data-ttu-id="6fb7f-141">Windows Media-Datei Bereich</span><span class="sxs-lookup"><span data-stu-id="6fb7f-141">Windows Media file scope</span></span>

    <span data-ttu-id="6fb7f-142">Attribute der Windows-Mediendatei werden von allen metadateiattributen überschrieben.</span><span class="sxs-lookup"><span data-stu-id="6fb7f-142">Attributes of the Windows Media file are overridden by any metafile attributes.</span></span> <span data-ttu-id="6fb7f-143">Die Metadaten der Mediendatei werden nur angezeigt, wenn für dieses Element in der Metadatei keine Metadaten definiert sind.</span><span class="sxs-lookup"><span data-stu-id="6fb7f-143">Media file metadata is displayed only if there is no metadata defined for that element in the metafile.</span></span>

## <a name="related-topics"></a><span data-ttu-id="6fb7f-144">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="6fb7f-144">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="6fb7f-145">**Erstellen von Metafile-Wiedergabelisten**</span><span class="sxs-lookup"><span data-stu-id="6fb7f-145">**Creating Metafile Playlists**</span></span>](creating-metafile-playlists.md)
</dt> <dt>

[<span data-ttu-id="6fb7f-146">**Metafile-Wiedergabelisten**</span><span class="sxs-lookup"><span data-stu-id="6fb7f-146">**Metafile Playlists**</span></span>](metafile-playlists.md)
</dt> <dt>

[<span data-ttu-id="6fb7f-147">**Verweis auf Windows Media-Metadateielemente**</span><span class="sxs-lookup"><span data-stu-id="6fb7f-147">**Windows Media Metafile Elements Reference**</span></span>](windows-media-metafile-elements-reference.md)
</dt> <dt>

[<span data-ttu-id="6fb7f-148">**Leitfaden für Windows Media-Metadateien**</span><span class="sxs-lookup"><span data-stu-id="6fb7f-148">**Windows Media Metafile Guide**</span></span>](windows-media-metafile-guide.md)
</dt> </dl>

 

 




