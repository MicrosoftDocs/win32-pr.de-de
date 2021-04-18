---
title: Banner-Element
description: Das Banner Element definiert eine URL zu einer Grafikdatei, die im Anzeigebereich angezeigt wird.
ms.assetid: 8b4a3369-a687-40a8-b5df-afb0e0518cd1
keywords:
- Banner Element Windows Media Player
topic_type:
- apiref
api_name:
- BANNER Element
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 8e257c14e5908482cdf8de458c259bc64a55c6d5
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106354705"
---
# <a name="banner-element"></a><span data-ttu-id="3b8d8-104">Banner-Element</span><span class="sxs-lookup"><span data-stu-id="3b8d8-104">BANNER Element</span></span>

<span data-ttu-id="3b8d8-105">Das **Banner** Element definiert eine URL zu einer Grafikdatei, die im Anzeigebereich angezeigt wird.</span><span class="sxs-lookup"><span data-stu-id="3b8d8-105">The **BANNER** element defines a URL to a graphic file that will appear in the display panel.</span></span>

``` syntax
<BANNER
   HREF = "URL"
>
</BANNER>
```

## <a name="attributes"></a><span data-ttu-id="3b8d8-106">Attribute</span><span class="sxs-lookup"><span data-stu-id="3b8d8-106">Attributes</span></span>

<span data-ttu-id="3b8d8-107">**Href** (erforderlich)</span><span class="sxs-lookup"><span data-stu-id="3b8d8-107">**HREF** (required)</span></span>

<span data-ttu-id="3b8d8-108">URL zu einer Grafikdatei, die im Anzeigebereich angezeigt wird.</span><span class="sxs-lookup"><span data-stu-id="3b8d8-108">URL to a graphic file that is displayed in the display panel.</span></span>

## <a name="parentchild-elements"></a><span data-ttu-id="3b8d8-109">Über-/unterordnungselemente</span><span class="sxs-lookup"><span data-stu-id="3b8d8-109">Parent/Child Elements</span></span>



| <span data-ttu-id="3b8d8-110">Hierarchy</span><span class="sxs-lookup"><span data-stu-id="3b8d8-110">Hierarchy</span></span>       | <span data-ttu-id="3b8d8-111">Elemente</span><span class="sxs-lookup"><span data-stu-id="3b8d8-111">Elements</span></span>                   |
|-----------------|----------------------------|
| <span data-ttu-id="3b8d8-112">Übergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="3b8d8-112">Parent elements</span></span> | <span data-ttu-id="3b8d8-113">**ASX**, **Eintrag**</span><span class="sxs-lookup"><span data-stu-id="3b8d8-113">**ASX**, **ENTRY**</span></span>         |
| <span data-ttu-id="3b8d8-114">Untergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="3b8d8-114">Child elements</span></span>  | <span data-ttu-id="3b8d8-115">**abstract**, **moreingefo**</span><span class="sxs-lookup"><span data-stu-id="3b8d8-115">**ABSTRACT**, **MOREINFO**</span></span> |



 

## <a name="remarks"></a><span data-ttu-id="3b8d8-116">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="3b8d8-116">Remarks</span></span>

<span data-ttu-id="3b8d8-117">Dieses Element definiert eine URL zu einer Grafikdatei, die im Windows-Media Player Anzeigebereich unterhalb des Video Inhalts angezeigt wird.</span><span class="sxs-lookup"><span data-stu-id="3b8d8-117">This element defines a URL to a graphic file that appears in the Windows Media Player display panel, beneath the video content.</span></span> <span data-ttu-id="3b8d8-118">Wenn das Medium nur Audiodaten ist, wird die Banner Grafik eigenständig angezeigt.</span><span class="sxs-lookup"><span data-stu-id="3b8d8-118">If the media is audio only, the banner graphic is displayed by itself.</span></span> <span data-ttu-id="3b8d8-119">Windows Media Player reserviert einen Bereich von 32 Pixel, der um 194 Pixel breit (die Banner Leiste) für die Grafik ist.</span><span class="sxs-lookup"><span data-stu-id="3b8d8-119">Windows Media Player reserves a space 32 pixels high by 194 pixels wide (the banner bar) for the graphic.</span></span> <span data-ttu-id="3b8d8-120">Wenn die in der URL definierte Grafik kleiner als diese ist, wird Sie in ihrer ursprünglichen Größe angezeigt.</span><span class="sxs-lookup"><span data-stu-id="3b8d8-120">If the graphic defined in the URL is smaller than that, it displays at its original size.</span></span> <span data-ttu-id="3b8d8-121">Wenn die Grafik größer als der reservierte Platz ist, wird das Bild von Windows Media Player an den Platz angepasst.</span><span class="sxs-lookup"><span data-stu-id="3b8d8-121">If the graphic is larger than the reserved space, Windows Media Player will crop the image to fit the space.</span></span>

<span data-ttu-id="3b8d8-122">Sie können ein **abstraktes** Element innerhalb des Gültigkeits Bereichs des **Banner** Elements verwenden, um Text als QuickInfo anzuzeigen, wenn der Benutzer den Mauszeiger über die Banner Grafik hält.</span><span class="sxs-lookup"><span data-stu-id="3b8d8-122">You can use an **ABSTRACT** element within the scope of the **BANNER** element to display text as a ToolTip when the user pauses the mouse pointer over the banner graphic.</span></span> <span data-ttu-id="3b8d8-123">Ein **Moran FO** -Element innerhalb eines **Banner** Elements definiert eine URL, auf die der Benutzer klickt, wenn der Benutzer auf die Banner Grafik klickt.</span><span class="sxs-lookup"><span data-stu-id="3b8d8-123">A **MOREINFO** element within a **BANNER** element defines a URL to which the user is taken when the user clicks the banner graphic.</span></span> <span data-ttu-id="3b8d8-124">(Die URL kann ein beliebiger Pfad oder Protokoll sein, z. b. ein e-Mail-Link, eine HTTP-URL (Hypertext Transfer Protocol) zu einer Website oder sogar ein Microsoft JScript-Befehl.) Wenn der Zeiger über die Grafik bewegt wird, wird die Grafik als geprägt und sieht wie eine Schaltfläche aus.</span><span class="sxs-lookup"><span data-stu-id="3b8d8-124">(The URL can be any path or protocol, such as an email link, a Hypertext Transfer Protocol (HTTP) URL to a website, or even a Microsoft JScript command.) When the pointer is moved over the graphic, the graphic becomes embossed and looks like a button.</span></span>

<span data-ttu-id="3b8d8-125">Ein für ein **ASX** -Element definiertes **Banner** Element wird angezeigt, während alle Clips in der Wiedergabeliste abgespielt werden.</span><span class="sxs-lookup"><span data-stu-id="3b8d8-125">A **BANNER** element defined for an **ASX** element displays while all clips in the playlist are playing.</span></span> <span data-ttu-id="3b8d8-126">Ein **Banner** Element, das in einem **Entry** -Element definiert ist, wird nur angezeigt, während dieser Clip wiedergegeben wird, und während dieser Zeit überschreibt jedes Banner, das im übergeordneten **ASX** -Element definiert</span><span class="sxs-lookup"><span data-stu-id="3b8d8-126">A **BANNER** element defined in an **ENTRY** element displays only while that clip is playing, and during that time overrides any banner defined within the parent **ASX** element.</span></span> <span data-ttu-id="3b8d8-127">Sie können angeben, wie Windows Media Player Speicherplatz für das Banner reserviert, indem Sie das **bannerbar** -Attribut des **ASX** -Elements festlegen.</span><span class="sxs-lookup"><span data-stu-id="3b8d8-127">You can specify how Windows Media Player reserves space for the banner by setting the **BANNERBAR** attribute of the **ASX** element.</span></span>

<span data-ttu-id="3b8d8-128">Banner Bilder werden bei DRM-Dateien nicht unterstützt, oder wenn Windows Media Player in eine Webseite eingebettet ist.</span><span class="sxs-lookup"><span data-stu-id="3b8d8-128">Banner images are not supported with DRM files or when Windows Media Player is embedded in a webpage.</span></span>

## <a name="examples"></a><span data-ttu-id="3b8d8-129">Beispiele</span><span class="sxs-lookup"><span data-stu-id="3b8d8-129">Examples</span></span>

<span data-ttu-id="3b8d8-130">Im folgenden finden Sie ein Beispiel für ein **Banner** Element ohne untergeordnete Elemente:</span><span class="sxs-lookup"><span data-stu-id="3b8d8-130">The following is an example of a **BANNER** element without child elements:</span></span>


```XML
<BANNER HREF="https://sample.microsoft.com/art/banner1.bmp" />
```



<span data-ttu-id="3b8d8-131">Im folgenden finden Sie ein Beispiel für ein **Banner** -Element, das **abstrakte** und **morumfo** -Elemente enthält.</span><span class="sxs-lookup"><span data-stu-id="3b8d8-131">The following is an example of a **BANNER** element containing **ABSTRACT** and **MOREINFO** elements.</span></span>


```XML
<BANNER HREF="https://www.proseware.com/logos/banner1.bmp">
    <ABSTRACT>Click here to go to our website.</ABSTRACT>
    <MOREINFO HREF="https://sample.microsoft.com" />
    <!-- The text in the Abstract element displays as a 
         ToolTip when the mouse hovers over the banner 
         graphic. When a user clicks the banner, the URL 
         given in the MoreInfo element opens in the 
         browser. -->
</BANNER>
```



## <a name="requirements"></a><span data-ttu-id="3b8d8-132">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="3b8d8-132">Requirements</span></span>



| <span data-ttu-id="3b8d8-133">Anforderung</span><span class="sxs-lookup"><span data-stu-id="3b8d8-133">Requirement</span></span> | <span data-ttu-id="3b8d8-134">Wert</span><span class="sxs-lookup"><span data-stu-id="3b8d8-134">Value</span></span> |
|--------------------|------------------------------------------------------|
| <span data-ttu-id="3b8d8-135">Version</span><span class="sxs-lookup"><span data-stu-id="3b8d8-135">Version</span></span><br/> | <span data-ttu-id="3b8d8-136">Windows Media Player, Version 7,0 oder höher</span><span class="sxs-lookup"><span data-stu-id="3b8d8-136">Windows Media Player version 7.0 or later</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="3b8d8-137">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="3b8d8-137">See also</span></span>

<dl> <dt>

[<span data-ttu-id="3b8d8-138">**Verweis auf Windows Media-Metadateielemente**</span><span class="sxs-lookup"><span data-stu-id="3b8d8-138">**Windows Media Metafile Elements Reference**</span></span>](windows-media-metafile-elements-reference.md)
</dt> <dt>

[<span data-ttu-id="3b8d8-139">**Referenz zu Windows Media-Metadateien**</span><span class="sxs-lookup"><span data-stu-id="3b8d8-139">**Windows Media Metafile Reference**</span></span>](windows-media-metafile-reference.md)
</dt> </dl>

 

 





