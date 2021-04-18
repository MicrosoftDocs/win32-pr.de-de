---
title: ASX-Element
description: Das Element "ASX" definiert eine Datei als Metadatei.
ms.assetid: 130220a0-959c-4c13-aa7d-06b6bbebc9cc
keywords:
- Fenster Media Player des ASX-Elements
topic_type:
- apiref
api_name:
- ASX Element
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: b77cb6c379319c97377b2a3953a9f8fd86b65938
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106358705"
---
# <a name="asx-element"></a><span data-ttu-id="79a17-104">ASX-Element</span><span class="sxs-lookup"><span data-stu-id="79a17-104">ASX Element</span></span>

<span data-ttu-id="79a17-105">Das Element " **ASX** " definiert eine Datei als Metadatei.</span><span class="sxs-lookup"><span data-stu-id="79a17-105">The **ASX** element defines a file as a metafile.</span></span>

``` syntax
<ASX
   VERSION = "number"
   PREVIEWMODE = "YES" | "NO"
   BANNERBAR = "AUTO" | "FIXED"
>
</ASX>
```

## <a name="attributes"></a><span data-ttu-id="79a17-106">Attribute</span><span class="sxs-lookup"><span data-stu-id="79a17-106">Attributes</span></span>

<span data-ttu-id="79a17-107">`VERSION` (erforderlich)</span><span class="sxs-lookup"><span data-stu-id="79a17-107">`VERSION` (required)</span></span>

<span data-ttu-id="79a17-108">Dezimalzahl, die die Versionsnummer der Syntax für die Metadatei darstellt.</span><span class="sxs-lookup"><span data-stu-id="79a17-108">Decimal number representing the version number of the syntax for the metafile.</span></span> <span data-ttu-id="79a17-109">Legen Sie auf 3 oder 3,0 fest.</span><span class="sxs-lookup"><span data-stu-id="79a17-109">Set to 3 or 3.0.</span></span>

<span data-ttu-id="79a17-110">**PreviewMode** (optional)</span><span class="sxs-lookup"><span data-stu-id="79a17-110">**PREVIEWMODE** (optional)</span></span>

<span data-ttu-id="79a17-111">Ein Wert, der angibt, ob Windows Media Player vor dem ersten Clip in den Vorschaumodus wechselt.</span><span class="sxs-lookup"><span data-stu-id="79a17-111">Value indicating whether Windows Media Player enters preview mode before playing the first clip.</span></span>

<span data-ttu-id="79a17-112">Muss einen der folgenden Werte aufweisen.</span><span class="sxs-lookup"><span data-stu-id="79a17-112">Must be one of the following values.</span></span>



| <span data-ttu-id="79a17-113">Wert</span><span class="sxs-lookup"><span data-stu-id="79a17-113">Value</span></span> | <span data-ttu-id="79a17-114">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="79a17-114">Description</span></span>                                                                                        |
|-------|----------------------------------------------------------------------------------------------------|
| <span data-ttu-id="79a17-115">YES</span><span class="sxs-lookup"><span data-stu-id="79a17-115">YES</span></span>   | <span data-ttu-id="79a17-116">Windows Media Player wechselt in den Vorschaumodus, bevor der erste Clip wiedergegeben wird.</span><span class="sxs-lookup"><span data-stu-id="79a17-116">Windows Media Player enters preview mode before playing the first clip.</span></span>                            |
| <span data-ttu-id="79a17-117">Nein</span><span class="sxs-lookup"><span data-stu-id="79a17-117">NO</span></span>    | <span data-ttu-id="79a17-118">Der Standardwert.</span><span class="sxs-lookup"><span data-stu-id="79a17-118">The default value.</span></span> <span data-ttu-id="79a17-119">Windows Media Player wird vor der Wiedergabe des ersten Clips nicht in den Vorschaumodus wechselt.</span><span class="sxs-lookup"><span data-stu-id="79a17-119">Windows Media Player does not enter preview mode before playing the first clip.</span></span> |



 

<span data-ttu-id="79a17-120">**Bannerbar** (optional)</span><span class="sxs-lookup"><span data-stu-id="79a17-120">**BANNERBAR** (optional)</span></span>

<span data-ttu-id="79a17-121">Ein Wert, der angibt, ob Windows Media Player Platz für eine Banner Grafik reserviert.</span><span class="sxs-lookup"><span data-stu-id="79a17-121">Value indicating whether Windows Media Player reserves space for a banner graphic.</span></span>

<span data-ttu-id="79a17-122">Muss einen der folgenden Werte aufweisen.</span><span class="sxs-lookup"><span data-stu-id="79a17-122">Must be one of the following values.</span></span>



| <span data-ttu-id="79a17-123">Wert</span><span class="sxs-lookup"><span data-stu-id="79a17-123">Value</span></span> | <span data-ttu-id="79a17-124">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="79a17-124">Description</span></span>                                                                                                                                |
|-------|--------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="79a17-125">AUTO</span><span class="sxs-lookup"><span data-stu-id="79a17-125">AUTO</span></span>  | <span data-ttu-id="79a17-126">Der Standardwert.</span><span class="sxs-lookup"><span data-stu-id="79a17-126">The default value.</span></span> <span data-ttu-id="79a17-127">Windows Media Player reserviert Speicherplatz für die Banner Leiste nur dann, wenn ein Inhalts Element eine enthält.</span><span class="sxs-lookup"><span data-stu-id="79a17-127">Windows Media Player reserves space for the banner bar only when a piece of content includes one.</span></span>                       |
| <span data-ttu-id="79a17-128">FIXED</span><span class="sxs-lookup"><span data-stu-id="79a17-128">FIXED</span></span> | <span data-ttu-id="79a17-129">Windows Media Player reserviert eine Banner Grafik für jeden wiedergegebenen Inhalt, unabhängig davon, ob es ein zugeordnetes Banner gibt.</span><span class="sxs-lookup"><span data-stu-id="79a17-129">Windows Media Player reserves a fixed space for a banner graphic for every piece of content played, whether there is an associated banner.</span></span> |



 

## <a name="parentchild-elements"></a><span data-ttu-id="79a17-130">Über-/unterordnungselemente</span><span class="sxs-lookup"><span data-stu-id="79a17-130">Parent/Child Elements</span></span>



| <span data-ttu-id="79a17-131">Hierarchy</span><span class="sxs-lookup"><span data-stu-id="79a17-131">Hierarchy</span></span>       | <span data-ttu-id="79a17-132">Elemente</span><span class="sxs-lookup"><span data-stu-id="79a17-132">Elements</span></span>                                                                                                                                                               |
|-----------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="79a17-133">Übergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="79a17-133">Parent elements</span></span> | <span data-ttu-id="79a17-134">Keine.</span><span class="sxs-lookup"><span data-stu-id="79a17-134">None.</span></span> <span data-ttu-id="79a17-135">Das Element " **ASX** " muss das erste Element in jeder Metadatendatei sein.</span><span class="sxs-lookup"><span data-stu-id="79a17-135">The **ASX** element must be the first element in every metafile.</span></span>                                                                                                 |
| <span data-ttu-id="79a17-136">Untergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="79a17-136">Child elements</span></span>  | <span data-ttu-id="79a17-137">**abstract**, **Author**, **Banner**, **Base**, **Copyright**, **Entry**, **ENTRYREF**, **Event**, **moreinfo**, **previewduration**, **param**, **Repeat**, **Title**</span><span class="sxs-lookup"><span data-stu-id="79a17-137">**ABSTRACT**, **AUTHOR**, **BANNER**, **BASE**, **COPYRIGHT**, **ENTRY**, **ENTRYREF**, **EVENT**, **MOREINFO**, **PREVIEWDURATION**, **PARAM**, **REPEAT**, **TITLE**</span></span> |



 

## <a name="remarks"></a><span data-ttu-id="79a17-138">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="79a17-138">Remarks</span></span>

<span data-ttu-id="79a17-139">Die ersten vier Zeichen einer Metadatei-Wiedergabeliste müssen "<ASX" lauten.</span><span class="sxs-lookup"><span data-stu-id="79a17-139">The first four characters of a metafile playlist must be "<ASX".</span></span> <span data-ttu-id="79a17-140">Andere Elemente, die innerhalb des Gültigkeits Bereichs des **ASX** -Elements definiert sind, z. b. **Titel** und **Autor**, werden mit den von Windows Media Player angezeigten Informationen verknüpft.</span><span class="sxs-lookup"><span data-stu-id="79a17-140">Other elements defined within the scope of the **ASX** element, such as **TITLE** and **AUTHOR**, are associated with the show information displayed by Windows Media Player.</span></span>

<span data-ttu-id="79a17-141">Für Windows Media Player lautet die Syntax Versionsnummer 3,0.</span><span class="sxs-lookup"><span data-stu-id="79a17-141">For Windows Media Player, the syntax version number is 3.0.</span></span> <span data-ttu-id="79a17-142">Windows Media Player unterstützt alle früheren Versionen der metadateisyntax.</span><span class="sxs-lookup"><span data-stu-id="79a17-142">Windows Media Player supports all previous versions of metafile syntax.</span></span> <span data-ttu-id="79a17-143">Zulässige Werte für das **Versions** Attribut sind 3,0 und 3 (ohne Dezimaltrennzeichen).</span><span class="sxs-lookup"><span data-stu-id="79a17-143">Acceptable values for the **VERSION** attribute include both 3.0 and 3 (with no decimal point).</span></span>

<span data-ttu-id="79a17-144">Wenn der Wert des **PreviewMode** -Attributs "yes" lautet, wechselt Windows Media Player sofort in den Vorschaumodus, bevor der erste Clip wiedergegeben wird.</span><span class="sxs-lookup"><span data-stu-id="79a17-144">If the value of the **PREVIEWMODE** attribute is YES, Windows Media Player immediately enters preview mode before playing the first clip.</span></span> <span data-ttu-id="79a17-145">Wenn Windows Media Player in den Vorschaumodus wechselt, werden alle Clips in der Metadatei als Vorschau angezeigt.</span><span class="sxs-lookup"><span data-stu-id="79a17-145">When Windows Media Player enters preview mode, it previews each clip referenced in the metafile.</span></span> <span data-ttu-id="79a17-146">Das **previewduration** -Element bestimmt die Dauer jeder Vorschau.</span><span class="sxs-lookup"><span data-stu-id="79a17-146">The **PREVIEWDURATION** element determines the duration of each preview.</span></span>

<span data-ttu-id="79a17-147">Das Attribut " **bannerbar** " definiert, ob Windows Media Player Platz für eine Banner Grafik reserviert.</span><span class="sxs-lookup"><span data-stu-id="79a17-147">The **BANNERBAR** attribute defines whether Windows Media Player reserves space for a banner graphic.</span></span> <span data-ttu-id="79a17-148">Ein Banner ist eine Grafik, die im Videoanzeige Bereich angezeigt wird, während Medieninhalte abgespielt werden.</span><span class="sxs-lookup"><span data-stu-id="79a17-148">A banner is a graphic that is displayed in the video display area while media content is playing.</span></span> <span data-ttu-id="79a17-149">(Verwenden Sie das **Banner** -Element, um dem Inhalt ein Banner hinzuzufügen.) Wenn der Wert von " **bannerbar** " "Fixed" ist, reserviert Windows Media Player Bannerbereich für jedes Medien Inhalts Objekt, ob der Medieninhalt über ein Banner verfügt.</span><span class="sxs-lookup"><span data-stu-id="79a17-149">(Use the **BANNER** element to add a banner to the content.) If the value of **BANNERBAR** is FIXED, Windows Media Player reserves banner space for every piece of media content, whether the media content has a banner.</span></span> <span data-ttu-id="79a17-150">Wenn einem Medieninhalt kein Banner zugeordnet ist, ist der reservierte Speicherplatz schwarz.</span><span class="sxs-lookup"><span data-stu-id="79a17-150">If a piece of media content does not have a banner associated with it, the space reserved for one is black.</span></span> <span data-ttu-id="79a17-151">Wenn der Wert des **bannerbar** -Attributs "Auto" ist, reserviert Windows Media Player Platz für das Banner nur dann, wenn der Medieninhalt eine enthält.</span><span class="sxs-lookup"><span data-stu-id="79a17-151">If the value of the **BANNERBAR** attribute is AUTO, Windows Media Player reserves space for the banner only when the media content includes one.</span></span>

<span data-ttu-id="79a17-152">Wenn Sie eine Metadatei mit mehreren Clips (**Entry** -oder **ENTRYREF** -Elemente) erstellen und den Wert des Attributs " **bannerbar** " auf "Auto" festlegen, wird die Größe von Windows Media Player ggf. geändert, um Platz für eine Banner Grafik für einen Clip zuzulassen. Anschließend wird die Größe wieder geändert, wenn der nächste Clip keine Banner Grafik enthält.</span><span class="sxs-lookup"><span data-stu-id="79a17-152">If you create a metafile with multiple clips (**ENTRY** or **ENTRYREF** elements) and set the value of the **BANNERBAR** attribute to AUTO, Windows Media Player might resize to allow space for a banner graphic for one clip, and then resize again if the next clip does not contain a banner graphic.</span></span> <span data-ttu-id="79a17-153">Wenn die Größe des Fensters unverändert bleiben soll (es sei denn, die Videogröße wird geändert), verwenden Sie den Fixed-Wert für das **bannerbar** -Attribut.</span><span class="sxs-lookup"><span data-stu-id="79a17-153">If you want the size of the window to stay the same (except when the video size changes), use the FIXED value for the **BANNERBAR** attribute.</span></span>

<span data-ttu-id="79a17-154">Der für eine Banner Grafik reservierte Raum ist 32 Pixel hoch und 194 Pixel breit.</span><span class="sxs-lookup"><span data-stu-id="79a17-154">The space reserved for a banner graphic is 32 pixels high by 194 pixels wide.</span></span> <span data-ttu-id="79a17-155">Der reservierte Speicherplatz wird unter jedem gerenderten Videoinhalt und 6 Pixel oberhalb des unteren Randes des Videobereichs angezeigt. Dadurch wird Platz für den 6-Pixel-Videobereichs Rahmen ermöglicht.</span><span class="sxs-lookup"><span data-stu-id="79a17-155">The reserved space appears below any rendered video content and 6 pixels above the lower edge of the video area, allowing space for the 6-pixel video area border.</span></span> <span data-ttu-id="79a17-156">Der reservierte Bannerbereich wird horizontal zentriert.</span><span class="sxs-lookup"><span data-stu-id="79a17-156">The reserved banner space is centered horizontally.</span></span>

<span data-ttu-id="79a17-157">Windows Media Player rendert die Grafik ab dem äußersten linken Pixel des Banner Raums.</span><span class="sxs-lookup"><span data-stu-id="79a17-157">Windows Media Player renders the graphic beginning in the leftmost pixel of the banner space.</span></span> <span data-ttu-id="79a17-158">Wenn die Grafik den gesamten Bereich füllt, wird Sie horizontal zentriert angezeigt.</span><span class="sxs-lookup"><span data-stu-id="79a17-158">If the graphic fills the entire space, it will appear centered horizontally.</span></span> <span data-ttu-id="79a17-159">Andernfalls werden nachfolgende Leerzeichen angezeigt.</span><span class="sxs-lookup"><span data-stu-id="79a17-159">Otherwise there will be trailing space.</span></span> <span data-ttu-id="79a17-160">Beachten Sie, dass die minimale Breite von Windows-Media Player immer breiter als die Größe des Videoclips ist, unabhängig vom Wert des **bannerbar** -Attributs.</span><span class="sxs-lookup"><span data-stu-id="79a17-160">Note that the minimum width of Windows Media Player is always wider than the size of the video clip, regardless of the value of the **BANNERBAR** attribute.</span></span>

## <a name="examples"></a><span data-ttu-id="79a17-161">Beispiele</span><span class="sxs-lookup"><span data-stu-id="79a17-161">Examples</span></span>


```XML
<ASX VERSION="3.0" PREVIEWMODE="YES" BANNERBAR="auto"  >
   <ENTRY HREF="https://sample.microsoft.com/sample1.ASX" />
</ASX>

```



## <a name="requirements"></a><span data-ttu-id="79a17-162">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="79a17-162">Requirements</span></span>



| <span data-ttu-id="79a17-163">Anforderung</span><span class="sxs-lookup"><span data-stu-id="79a17-163">Requirement</span></span> | <span data-ttu-id="79a17-164">Wert</span><span class="sxs-lookup"><span data-stu-id="79a17-164">Value</span></span> |
|--------------------|-----------------------------------------------------|
| <span data-ttu-id="79a17-165">Version</span><span class="sxs-lookup"><span data-stu-id="79a17-165">Version</span></span><br/> | <span data-ttu-id="79a17-166">Windows Media Player, Version 70 oder höher</span><span class="sxs-lookup"><span data-stu-id="79a17-166">Windows Media Player version 70 or later</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="79a17-167">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="79a17-167">See also</span></span>

<dl> <dt>

[<span data-ttu-id="79a17-168">**Verweis auf Windows Media-Metadateielemente**</span><span class="sxs-lookup"><span data-stu-id="79a17-168">**Windows Media Metafile Elements Reference**</span></span>](windows-media-metafile-elements-reference.md)
</dt> <dt>

[<span data-ttu-id="79a17-169">**Referenz zu Windows Media-Metadateien**</span><span class="sxs-lookup"><span data-stu-id="79a17-169">**Windows Media Metafile Reference**</span></span>](windows-media-metafile-reference.md)
</dt> </dl>

 

 





