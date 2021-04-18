---
title: Ref-Element
description: Das ref-Element gibt eine URL für den Inhalt digitaler Medien an.
ms.assetid: 0ba11a1e-3802-4156-83ca-f1bae1eb366c
keywords:
- Windows Media Player Ref-Element
topic_type:
- apiref
api_name:
- REF Element
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 739ac61007e619055c28732c5c5aa763e84054fa
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106368397"
---
# <a name="ref-element"></a><span data-ttu-id="11cf4-104">Ref-Element</span><span class="sxs-lookup"><span data-stu-id="11cf4-104">REF Element</span></span>

<span data-ttu-id="11cf4-105">Das **ref** -Element gibt eine URL für den Inhalt digitaler Medien an.</span><span class="sxs-lookup"><span data-stu-id="11cf4-105">The **REF** element specifies a URL for digital media content.</span></span>

``` syntax
<REF
   HREF = "URL"
>
</REF>
```

## <a name="attributes"></a><span data-ttu-id="11cf4-106">Attribute</span><span class="sxs-lookup"><span data-stu-id="11cf4-106">Attributes</span></span>

<span data-ttu-id="11cf4-107">**Href** (erforderlich)</span><span class="sxs-lookup"><span data-stu-id="11cf4-107">**HREF** (required)</span></span>

<span data-ttu-id="11cf4-108">URL zu beliebigen Medieninhalten, die von Windows Media Player unterstützt werden.</span><span class="sxs-lookup"><span data-stu-id="11cf4-108">URL to any piece of media content supported by Windows Media Player.</span></span>

## <a name="parentchild-elements"></a><span data-ttu-id="11cf4-109">Über-/unterordnungselemente</span><span class="sxs-lookup"><span data-stu-id="11cf4-109">Parent/Child Elements</span></span>



| <span data-ttu-id="11cf4-110">Hierarchy</span><span class="sxs-lookup"><span data-stu-id="11cf4-110">Hierarchy</span></span>       | <span data-ttu-id="11cf4-111">Elemente</span><span class="sxs-lookup"><span data-stu-id="11cf4-111">Elements</span></span>                                                                         |
|-----------------|----------------------------------------------------------------------------------|
| <span data-ttu-id="11cf4-112">Übergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="11cf4-112">Parent elements</span></span> | <span data-ttu-id="11cf4-113">**Ein**</span><span class="sxs-lookup"><span data-stu-id="11cf4-113">**ENTRY**</span></span>                                                                        |
| <span data-ttu-id="11cf4-114">Untergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="11cf4-114">Child elements</span></span>  | <span data-ttu-id="11cf4-115">**Duration**, **Endmarker**, **previewduration**, **Startmarker**, **StartTime**</span><span class="sxs-lookup"><span data-stu-id="11cf4-115">**DURATION**, **ENDMARKER**, **PREVIEWDURATION**, **STARTMARKER**, **STARTTIME**</span></span> |



 

## <a name="remarks"></a><span data-ttu-id="11cf4-116">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="11cf4-116">Remarks</span></span>

<span data-ttu-id="11cf4-117">Dieses Element gibt eine URL für ein Medien Inhalts Element an.</span><span class="sxs-lookup"><span data-stu-id="11cf4-117">This element specifies a URL for a piece of media content.</span></span> <span data-ttu-id="11cf4-118">Die URL kann auf jeden unterstützten Medientyp verweisen, wobei jedes Protokoll verwendet wird, das von Windows Media Player unterstützt wird.</span><span class="sxs-lookup"><span data-stu-id="11cf4-118">The URL can point to any media type supported, using any protocol supported by Windows Media Player.</span></span>

<span data-ttu-id="11cf4-119">Zu den unterstützten Medientypen zählen weiterhin Bilder wie GIF-und JPG-Images sowie Flash-Dateien mit der Dateinamenerweiterung ". swf".</span><span class="sxs-lookup"><span data-stu-id="11cf4-119">The media types supported include still images such as .gif and .jpg images and Flash files with an .swf file name extension.</span></span> <span data-ttu-id="11cf4-120">Diese Medientypen sind nützlich, um Werbeinhalte in eine Wiedergabeliste einzubeziehen.</span><span class="sxs-lookup"><span data-stu-id="11cf4-120">These media types are useful for including advertising content within a playlist.</span></span> <span data-ttu-id="11cf4-121">Mit Bilddateien und Flash Dateien, die in einer Schleife wiedergegeben werden, müssen Sie auch den Zeitraum angeben, in dem das Medien Element angezeigt werden soll, indem Sie ein **Duration** -Element innerhalb des **ref** -Elements einschließen.</span><span class="sxs-lookup"><span data-stu-id="11cf4-121">With image files and Flash files that play in a loop, you must also specify the amount of time to display the media item by including a **DURATION** element within the **REF** element.</span></span> <span data-ttu-id="11cf4-122">Wenn Sie möchten, dass ein Bild weiterhin angezeigt wird, während der nächste Eintrag in der Wiedergabeliste gepuffert wird, schließen Sie ein **param** -Element in das **Entry** -Element ein, legen Sie das **Name** -Attribut auf showwhilebuffereing fest, und legen Sie das Attribut **value** auf true fest.</span><span class="sxs-lookup"><span data-stu-id="11cf4-122">If you want an image to continue displaying while the next entry in the playlist is buffered, include a **PARAM** element within the **ENTRY** element, set its **name** attribute to ShowWhileBuffering, and set its **value** attribute to true.</span></span>

<span data-ttu-id="11cf4-123">Zum Verweisen auf Inhalte auf einer CD oder DVD, die dies zulässt, werden die Protokolle wmpcd und wmpdvd bereitgestellt.</span><span class="sxs-lookup"><span data-stu-id="11cf4-123">To reference content on a CD or a DVD that allows it, the wmpcd and wmpdvd protocols are provided.</span></span> <span data-ttu-id="11cf4-124">Wenn Sie z. b. das **href** -Attribut auf "wmpdvd://f/5/3" festlegen, wird Kapitel 3 von Titel 5 auf einer DVD wiedergegeben, aber nur, wenn die DVD erstellt wurde, um Sie zuzulassen.</span><span class="sxs-lookup"><span data-stu-id="11cf4-124">For example, setting the **HREF** attribute to "wmpdvd://f/5/3" will play chapter 3 of title 5 on a DVD, but only if the DVD has been authored to allow it.</span></span>

<span data-ttu-id="11cf4-125">Anwendungen, die digitale Medien aus einer Firewall öffnen, haben beim Öffnen der Medienelemente eine bessere Leistung, wenn die Adresse mit dem DNS-Namen (Domain Nameserver) anstelle der IP-Adresse angegeben wird.</span><span class="sxs-lookup"><span data-stu-id="11cf4-125">Applications that open digital media from behind a firewall will have better performance when opening the media items if the address is specified using the domain name server (DNS) name instead of the IP address.</span></span>

<span data-ttu-id="11cf4-126">Dieses Element wird am häufigsten für den URL-Rollover verwendet.</span><span class="sxs-lookup"><span data-stu-id="11cf4-126">The most common use of this element is for URL rollover.</span></span> <span data-ttu-id="11cf4-127">Wenn Windows Media Player ein in einem **ref** -Element definiertes Medien Medium nicht öffnen kann, wird die URL im nächsten **ref** -Element ausprobiert.</span><span class="sxs-lookup"><span data-stu-id="11cf4-127">If Windows Media Player is unable to open a piece of media defined in a **REF** element, it tries the URL in the next **REF** element.</span></span> <span data-ttu-id="11cf4-128">Sobald Windows Media Player Medieninhalte über eine URL öffnet, die im Bereich eines **Eintrags** Elements definiert ist, ignoriert Sie nachfolgende **ref** -Tags innerhalb dieses **Eintrags** Elements.</span><span class="sxs-lookup"><span data-stu-id="11cf4-128">Once Windows Media Player opens media content from a URL defined within the scope of one **ENTRY** element, it ignores subsequent **REF** tags within that **ENTRY** element.</span></span> <span data-ttu-id="11cf4-129">Wenn die Wiedergabe des Inhalts abgeschlossen ist, wechselt Windows Media Player zum nächsten **Eintrags** Element, sofern vorhanden.</span><span class="sxs-lookup"><span data-stu-id="11cf4-129">After the piece of content is done playing, Windows Media Player moves on to the next **ENTRY** element, if any.</span></span>

-   <span data-ttu-id="11cf4-130">**Wichtig** Sobald Windows Media Player eine Verbindung mit einem Inhalt herstellt, auf den verwiesen wird, werden alle **anderen Verweis** Elemente in diesem **Eintrag** ignoriert, unabhängig davon, ob die Verbindung normal oder nicht ordnungsgemäß beendet wird.</span><span class="sxs-lookup"><span data-stu-id="11cf4-130">**Important** Once Windows Media Player establishes a connection to a referenced piece of content, it ignores all other **REF** elements in that **ENTRY**, whether the connection terminates normally or abnormally.</span></span>

<span data-ttu-id="11cf4-131">Wenn das Medien Element, auf das verwiesen wird, eine Bilddatei ist, muss das **Duration** -Element verwendet werden, um die Anzeigezeit für das Bild anzugeben.</span><span class="sxs-lookup"><span data-stu-id="11cf4-131">If the media item referenced is an image file, the **DURATION** element must be used to specify the display time for the image.</span></span>

<span data-ttu-id="11cf4-132">**Hinweis**</span><span class="sxs-lookup"><span data-stu-id="11cf4-132">**Note**</span></span>

<span data-ttu-id="11cf4-133">Der Versuch, Flash Medien wiederzugeben, die Sound mit dem ersten Frame enthalten, kann zu unerwarteten Ergebnissen führen.</span><span class="sxs-lookup"><span data-stu-id="11cf4-133">Attempting to play Flash media that includes sound with the first frame may yield unexpected results.</span></span> <span data-ttu-id="11cf4-134">Sie sollten Flash Inhalte erstellen, um Sound ab dem zweiten Frame wiederzugeben.</span><span class="sxs-lookup"><span data-stu-id="11cf4-134">You should author Flash content to play sound starting no earlier than the second frame.</span></span>

## <a name="examples"></a><span data-ttu-id="11cf4-135">Beispiele</span><span class="sxs-lookup"><span data-stu-id="11cf4-135">Examples</span></span>


```XML
<ASX VERSION="3.0">
   <ENTRY>
   <TITLE>Example Clip</TITLE>
      <REF HREF="mms://example.microsoft.com/selection1.asf" />
      <REF HREF="mms://sample.microsoft.com/mirror/selection1.asf" />
   </ENTRY>
</ASX>
```



## <a name="requirements"></a><span data-ttu-id="11cf4-136">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="11cf4-136">Requirements</span></span>



| <span data-ttu-id="11cf4-137">Anforderung</span><span class="sxs-lookup"><span data-stu-id="11cf4-137">Requirement</span></span> | <span data-ttu-id="11cf4-138">Wert</span><span class="sxs-lookup"><span data-stu-id="11cf4-138">Value</span></span> |
|--------------------|------------------------------------------------------|
| <span data-ttu-id="11cf4-139">Version</span><span class="sxs-lookup"><span data-stu-id="11cf4-139">Version</span></span><br/> | <span data-ttu-id="11cf4-140">Windows Media Player, Version 7,0 oder höher</span><span class="sxs-lookup"><span data-stu-id="11cf4-140">Windows Media Player version 7.0 or later</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="11cf4-141">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="11cf4-141">See also</span></span>

<dl> <dt>

[<span data-ttu-id="11cf4-142">**Unterstützte Protokolle und Dateitypen**</span><span class="sxs-lookup"><span data-stu-id="11cf4-142">**Supported Protocols and File Types**</span></span>](supported-protocols-and-file-types.md)
</dt> <dt>

[<span data-ttu-id="11cf4-143">**Verweis auf Windows Media-Metadateielemente**</span><span class="sxs-lookup"><span data-stu-id="11cf4-143">**Windows Media Metafile Elements Reference**</span></span>](windows-media-metafile-elements-reference.md)
</dt> <dt>

[<span data-ttu-id="11cf4-144">**Referenz zu Windows Media-Metadateien**</span><span class="sxs-lookup"><span data-stu-id="11cf4-144">**Windows Media Metafile Reference**</span></span>](windows-media-metafile-reference.md)
</dt> </dl>

 

 





