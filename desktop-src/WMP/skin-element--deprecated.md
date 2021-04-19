---
title: Skin-Element (veraltet)
description: Diese Seite dokumentiert eine Funktion, die in zukünftigen Versionen von Windows Media Player und dem Windows Media Player SDK möglicherweise nicht verfügbar ist.
ms.assetid: 593244c1-f850-46d7-8b84-14dcd59b024e
keywords:
- Skin-Element (veraltet) Windows-Media Player
topic_type:
- apiref
api_name:
- SKIN Element (deprecated)
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: abf503706dec131eef411ebaf3625071e2b31098
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106355958"
---
# <a name="skin-element-deprecated"></a><span data-ttu-id="61f44-104">Skin-Element (veraltet)</span><span class="sxs-lookup"><span data-stu-id="61f44-104">SKIN Element (deprecated)</span></span>

<span data-ttu-id="61f44-105">Diese Seite dokumentiert eine Funktion, die in zukünftigen Versionen von Windows Media Player und dem Windows Media Player SDK möglicherweise nicht verfügbar ist.</span><span class="sxs-lookup"><span data-stu-id="61f44-105">This page documents a feature that may be unavailable in future versions of Windows Media Player and the Windows Media Player SDK.</span></span>

<span data-ttu-id="61f44-106">Das **Skin** -Element gibt eine URL zu einem Rahmen an.</span><span class="sxs-lookup"><span data-stu-id="61f44-106">The **SKIN** element specifies a URL to a border.</span></span>

``` syntax
<SKIN
   HREF = "URL"
/>
```

## <a name="attributes"></a><span data-ttu-id="61f44-107">Attribute</span><span class="sxs-lookup"><span data-stu-id="61f44-107">Attributes</span></span>

<span data-ttu-id="61f44-108">**Href** (erforderlich)</span><span class="sxs-lookup"><span data-stu-id="61f44-108">**HREF** (required)</span></span>

<span data-ttu-id="61f44-109">URL für eine komprimierte Rahmen Datei mit der Dateinamenerweiterung. WMZ.</span><span class="sxs-lookup"><span data-stu-id="61f44-109">URL for a compressed border file with a file name extension .wmz.</span></span> <span data-ttu-id="61f44-110">Für Windows Media Player 9-Serie oder höher kann dieser Wert nur auf Border-Dateien auf der Festplatte des Benutzers verweisen, die sich im gleichen Verzeichnis wie die Metadatendatei-Wiedergabeliste befindet.</span><span class="sxs-lookup"><span data-stu-id="61f44-110">For Windows Media Player 9 Series or later, this value can reference only border files on the user's hard disk located in the same directory as the metafile playlist.</span></span> <span data-ttu-id="61f44-111">Weitere Informationen finden Sie im Beispielcode.</span><span class="sxs-lookup"><span data-stu-id="61f44-111">See the example code.</span></span>

## <a name="parentchild-elements"></a><span data-ttu-id="61f44-112">Über-/unterordnungselemente</span><span class="sxs-lookup"><span data-stu-id="61f44-112">Parent/Child Elements</span></span>



| <span data-ttu-id="61f44-113">Hierarchy</span><span class="sxs-lookup"><span data-stu-id="61f44-113">Hierarchy</span></span>       | <span data-ttu-id="61f44-114">Elemente</span><span class="sxs-lookup"><span data-stu-id="61f44-114">Elements</span></span> |
|-----------------|----------|
| <span data-ttu-id="61f44-115">Übergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="61f44-115">Parent elements</span></span> | <span data-ttu-id="61f44-116">**ASX**</span><span class="sxs-lookup"><span data-stu-id="61f44-116">**ASX**</span></span>  |
| <span data-ttu-id="61f44-117">Untergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="61f44-117">Child elements</span></span>  | <span data-ttu-id="61f44-118">Keine</span><span class="sxs-lookup"><span data-stu-id="61f44-118">None</span></span>     |



 

## <a name="remarks"></a><span data-ttu-id="61f44-119">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="61f44-119">Remarks</span></span>

<span data-ttu-id="61f44-120">Das **Skin** -Element wird zum Erstellen eines Rahmens verwendet, der mit einer Skin vergleichbar ist, aber im Bereich **jetzt Wiedergabe** der Windows-Media Player im Vollmodus angezeigt wird.</span><span class="sxs-lookup"><span data-stu-id="61f44-120">The **SKIN** element is used to create a border, which is similar to a skin but is displayed in the **Now Playing** area of the full mode Windows Media Player.</span></span> <span data-ttu-id="61f44-121">Das **Skin** -Element wird nur für Rahmen verwendet, die innerhalb des Windows-Media Player im Vollmodus angezeigt werden, und nicht für reguläre Skins, die den Windows-Media Player im Compact-Modus vollständig ersetzen.</span><span class="sxs-lookup"><span data-stu-id="61f44-121">The **SKIN** element is used only for borders, which appear inside the full mode Windows Media Player, and not for regular skins, which entirely replace the compact mode Windows Media Player.</span></span>

<span data-ttu-id="61f44-122">In einem Windows Media-Download Paket (mit der Dateinamenerweiterung ". WMD") ermöglicht das **Skin** -Element einem Rahmen, Inhalte zu erhalten und mit anderen Websites zu verknüpfen.</span><span class="sxs-lookup"><span data-stu-id="61f44-122">In a Windows Media Download Package (with a .wmd file name extension), the **SKIN** element enables a border to have content and link to other sites.</span></span> <span data-ttu-id="61f44-123">Das Windows Media-Download Paket ist eine komprimierte Datei, die eine Rahmen Datei und eine Windows Media-Metadatendatei enthält.</span><span class="sxs-lookup"><span data-stu-id="61f44-123">The Windows Media Download Package is a compressed file that contains a border file and a Windows Media metafile.</span></span> <span data-ttu-id="61f44-124">Die Rahmen Datei (mit der Dateinamenerweiterung. wmz) ist komprimiert und enthält eine Skin-Definitionsdatei (mit der Dateinamenerweiterung. WMS).</span><span class="sxs-lookup"><span data-stu-id="61f44-124">The border file (with a .wmz file name extension) is compressed, and includes a skin definition file (with a .wms file name extension).</span></span>

<span data-ttu-id="61f44-125">Ein **Skin** -Element hat drei Komponenten:</span><span class="sxs-lookup"><span data-stu-id="61f44-125">A **SKIN** element has three components:</span></span>

-   <span data-ttu-id="61f44-126">Ein Skin</span><span class="sxs-lookup"><span data-stu-id="61f44-126">A skin</span></span>
-   <span data-ttu-id="61f44-127">Inhalt</span><span class="sxs-lookup"><span data-stu-id="61f44-127">Some content</span></span>
-   <span data-ttu-id="61f44-128">Eine Metadatei</span><span class="sxs-lookup"><span data-stu-id="61f44-128">A metafile</span></span>

<span data-ttu-id="61f44-129">In Windows Media-Download Paketen enthaltene Skins müssen rechteckig in Form sein.</span><span class="sxs-lookup"><span data-stu-id="61f44-129">Skins included with Windows Media Download Packages must be rectangular in shape.</span></span> <span data-ttu-id="61f44-130">Das Erstellen von Rahmen mit nicht rechteckigen Skins kann zu unerwarteten Ergebnissen führen.</span><span class="sxs-lookup"><span data-stu-id="61f44-130">Creating borders with skins that are not rectangular may yield unexpected results.</span></span>

## <a name="examples"></a><span data-ttu-id="61f44-131">Beispiele</span><span class="sxs-lookup"><span data-stu-id="61f44-131">Examples</span></span>


```XML
<ASX version = "3.0">
    <TITLE>A Skin Element</TITLE>
    <SKIN HREF = "YourTest.wmz" />

    <ENTRY>
        <PARAM name="YourAlbumTitle" value="YourTitle.jpg"/>
        <PARAM name="link" value="https://www.proseware.com"/>
        <TITLE>(The Artist)-YourTitle</TITLE>
        <REF HREF="(The Artist)-YourSongTitle.wma"/>
    </ENTRY>

</ASX>
```



## <a name="requirements"></a><span data-ttu-id="61f44-132">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="61f44-132">Requirements</span></span>



| <span data-ttu-id="61f44-133">Anforderung</span><span class="sxs-lookup"><span data-stu-id="61f44-133">Requirement</span></span> | <span data-ttu-id="61f44-134">Wert</span><span class="sxs-lookup"><span data-stu-id="61f44-134">Value</span></span> |
|--------------------|-----------------------------------------------------|
| <span data-ttu-id="61f44-135">Version</span><span class="sxs-lookup"><span data-stu-id="61f44-135">Version</span></span><br/> | <span data-ttu-id="61f44-136">Windows Media Player, Version 70 oder höher</span><span class="sxs-lookup"><span data-stu-id="61f44-136">Windows Media Player version 70 or later</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="61f44-137">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="61f44-137">See also</span></span>

<dl> <dt>

[<span data-ttu-id="61f44-138">**Rahmen für Windows-Media Player (veraltet)**</span><span class="sxs-lookup"><span data-stu-id="61f44-138">**Borders for Windows Media Player (deprecated)**</span></span>](borders-for-windows-media-player--deprecated.md)
</dt> <dt>

[<span data-ttu-id="61f44-139">**Verweis auf Windows Media-Metadateielemente**</span><span class="sxs-lookup"><span data-stu-id="61f44-139">**Windows Media Metafile Elements Reference**</span></span>](windows-media-metafile-elements-reference.md)
</dt> <dt>

[<span data-ttu-id="61f44-140">**Referenz zu Windows Media-Metadateien**</span><span class="sxs-lookup"><span data-stu-id="61f44-140">**Windows Media Metafile Reference**</span></span>](windows-media-metafile-reference.md)
</dt> </dl>

 

 





