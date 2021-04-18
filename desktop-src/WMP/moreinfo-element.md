---
title: Moreingefo-Element
description: Das moreinfo-Element gibt eine URL zu einer Website, einer e-Mail-Adresse oder einem Skript Befehl an, die einer Show, einem Clip oder einem Banner zugeordnet ist.
ms.assetid: b817ef1d-4ca0-45f4-942b-695eaf537110
keywords:
- Moreingefo-Element Fenster Media Player
topic_type:
- apiref
api_name:
- MOREINFO Element
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: efc54fe9745566ec7eaa87b7f0f4645b07a055f0
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106358260"
---
# <a name="moreinfo-element"></a><span data-ttu-id="31f76-104">Moreingefo-Element</span><span class="sxs-lookup"><span data-stu-id="31f76-104">MOREINFO Element</span></span>

<span data-ttu-id="31f76-105">Das **moreinfo** -Element gibt eine URL zu einer Website, einer e-Mail-Adresse oder einem Skript Befehl an, die einer Show, einem Clip oder einem Banner zugeordnet ist.</span><span class="sxs-lookup"><span data-stu-id="31f76-105">The **MOREINFO** element specifies a URL to a website, email address, or script command associated with a show, clip, or banner.</span></span>

``` syntax
<MOREINFO
   HREF = "URL"
   TARGET = "Frame"
/>
```

## <a name="attributes"></a><span data-ttu-id="31f76-106">Attribute</span><span class="sxs-lookup"><span data-stu-id="31f76-106">Attributes</span></span>

<span data-ttu-id="31f76-107">**Href** (erforderlich)</span><span class="sxs-lookup"><span data-stu-id="31f76-107">**HREF** (required)</span></span>

<span data-ttu-id="31f76-108">URL zu einer Website, einer e-Mail-Adresse oder einem Skript Befehl.</span><span class="sxs-lookup"><span data-stu-id="31f76-108">URL to a website, email address, or script command.</span></span>

<span data-ttu-id="31f76-109">**Spar**</span><span class="sxs-lookup"><span data-stu-id="31f76-109">**TARGET**</span></span>

<span data-ttu-id="31f76-110">Ein Wert, der den Frame oder das Fenster definiert, in dem der Browser die durch das **href** -Attribut definierte Seite öffnet.</span><span class="sxs-lookup"><span data-stu-id="31f76-110">Value defining the frame or window in which the browser will open the page defined by the **HREF** attribute.</span></span>

<span data-ttu-id="31f76-111">Dabei kann es sich um eine Zeichenfolge handeln, die einen Fensternamen oder einen der folgenden Werte enthält.</span><span class="sxs-lookup"><span data-stu-id="31f76-111">This can be a string containing a window name, or one of the following values.</span></span>



| <span data-ttu-id="31f76-112">Wert</span><span class="sxs-lookup"><span data-stu-id="31f76-112">Value</span></span>    | <span data-ttu-id="31f76-113">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="31f76-113">Description</span></span>                                                                                                              |
|----------|--------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="31f76-114">\_Blitz</span><span class="sxs-lookup"><span data-stu-id="31f76-114">\_blank</span></span>  | <span data-ttu-id="31f76-115">Das Dokument wird in einem neuen Browserfenster geladen.</span><span class="sxs-lookup"><span data-stu-id="31f76-115">The document loads in a new browser window.</span></span>                                                                              |
| <span data-ttu-id="31f76-116">\_self</span><span class="sxs-lookup"><span data-stu-id="31f76-116">\_self</span></span>   | <span data-ttu-id="31f76-117">Das Dokument wird im gleichen Frame geladen wie das aktuelle Dokument, das das Windows Media Player-Steuerelement enthält.</span><span class="sxs-lookup"><span data-stu-id="31f76-117">The document loads in the same frame as the current document containing the Windows Media Player control.</span></span>                |
| <span data-ttu-id="31f76-118">\_übergeordneten</span><span class="sxs-lookup"><span data-stu-id="31f76-118">\_parent</span></span> | <span data-ttu-id="31f76-119">Das Dokument wird in den unmittelbar übergeordneten Frame des aktuellen Frames oder den aktuellen Frame geladen, wenn kein übergeordneter Frame vorhanden ist.</span><span class="sxs-lookup"><span data-stu-id="31f76-119">The document loads in the immediate parent frame of the current frame, or the current frame if there is no parent frame.</span></span> |
| <span data-ttu-id="31f76-120">\_top</span><span class="sxs-lookup"><span data-stu-id="31f76-120">\_top</span></span>    | <span data-ttu-id="31f76-121">Das Dokument wird im vollständigen Browserfenster geladen und ersetzt alle anderen Frames oder Dokumente.</span><span class="sxs-lookup"><span data-stu-id="31f76-121">The document loads in the full browser window, replacing all other frames or documents.</span></span>                                  |



 

## <a name="parentchild-elements"></a><span data-ttu-id="31f76-122">Über-/unterordnungselemente</span><span class="sxs-lookup"><span data-stu-id="31f76-122">Parent/Child Elements</span></span>



| <span data-ttu-id="31f76-123">Hierarchy</span><span class="sxs-lookup"><span data-stu-id="31f76-123">Hierarchy</span></span>       | <span data-ttu-id="31f76-124">Elemente</span><span class="sxs-lookup"><span data-stu-id="31f76-124">Elements</span></span>                       |
|-----------------|--------------------------------|
| <span data-ttu-id="31f76-125">Übergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="31f76-125">Parent elements</span></span> | <span data-ttu-id="31f76-126">**ASX**, **Eintrag**, **Banner**</span><span class="sxs-lookup"><span data-stu-id="31f76-126">**ASX**, **ENTRY**, **BANNER**</span></span> |
| <span data-ttu-id="31f76-127">Untergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="31f76-127">Child elements</span></span>  | <span data-ttu-id="31f76-128">Keine</span><span class="sxs-lookup"><span data-stu-id="31f76-128">None</span></span>                           |



 

## <a name="remarks"></a><span data-ttu-id="31f76-129">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="31f76-129">Remarks</span></span>

<span data-ttu-id="31f76-130">Dieses Element gibt eine URL zu einer Website, einer e-Mail-Adresse **oder einem Skript Befehl an. Der Benutzer kann auf das Ziel der URL zugreifen, indem er auf die Grafik oder den Text klickt, der dem Morein FO-Element zugeordnet ist** .</span><span class="sxs-lookup"><span data-stu-id="31f76-130">This element specifies a URL to a website, email address, **or script command. The user can access the target of the URL by clicking on the graphic or text associated with the MOREINFO** element.</span></span> <span data-ttu-id="31f76-131">Die Details hängen von dem übergeordneten Element des **moreingefo** -Elements ab:</span><span class="sxs-lookup"><span data-stu-id="31f76-131">The details depend on the parent element of the **MOREINFO** element:</span></span>

-   <span data-ttu-id="31f76-132">Wenn das **moreinfo** -Element das untergeordnete Element eines **ASX** -Elements ist, kann der Benutzer auf die URL zugreifen, indem er auf den Titel anzeigen klickt.</span><span class="sxs-lookup"><span data-stu-id="31f76-132">If the **MOREINFO** element is the child of an **ASX** element, the user can access the URL by clicking the show title.</span></span>
-   <span data-ttu-id="31f76-133">Wenn das **moreinfo** -Element das untergeordnete Element eines **Entry** -Elements ist, kann der Benutzer auf die URL zugreifen, indem er auf den Clip-Titel klickt.</span><span class="sxs-lookup"><span data-stu-id="31f76-133">If the **MOREINFO** element is the child of an **ENTRY** element, the user can access the URL by clicking the clip title.</span></span>
-   <span data-ttu-id="31f76-134">Wenn das **Moran FO** -Element das untergeordnete Element eines **Banner** Elements ist, kann der Benutzer auf die URL zugreifen, indem er auf die Banner Grafik klickt.</span><span class="sxs-lookup"><span data-stu-id="31f76-134">If the **MOREINFO** element is the child of a **BANNER** element, the user can access the URL by clicking the banner graphic.</span></span>

<span data-ttu-id="31f76-135">Wenn das **href** -Attribut eine URL zu einer Website angibt, wird der Browser geöffnet und navigiert zur URL.</span><span class="sxs-lookup"><span data-stu-id="31f76-135">If the **HREF** attribute specifies a URL to a website, the browser opens and navigates to the URL.</span></span> <span data-ttu-id="31f76-136">Wenn das **href** -Attribut eine e-Mail-Adresse angibt, wird die e-Mail des Benutzers gestartet.</span><span class="sxs-lookup"><span data-stu-id="31f76-136">If the **HREF** attribute specifies an email address, the user's email application starts.</span></span> <span data-ttu-id="31f76-137">Wenn das **href** -Attribut einen Skript Befehl angibt, wird der Skript Befehl im Browser ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="31f76-137">If the **HREF** attribute specifies a script command, the script command executes in the browser.</span></span>

<span data-ttu-id="31f76-138">**Hinweis**</span><span class="sxs-lookup"><span data-stu-id="31f76-138">**Note**</span></span>

<span data-ttu-id="31f76-139">Wenn das **moreinfo** -Element in einem **ASX** -oder **Entry** -Element angezeigt wird, wenn der Mauszeiger über dem Titel der Anzeige (für **ein-** Element des-Elements) oder von Clip (bei einem **Entry** -Element) gehalten wird, kann die im **href** -Attribut definierte URL ausgewählt und von Windows Media Player aufgerufen werden.</span><span class="sxs-lookup"><span data-stu-id="31f76-139">If the **MOREINFO** element appears within an **ASX** or **ENTRY** element, when the mouse cursor is held over the title of the show (for an **ASX** element) or clip (for an **ENTRY** element), the URL defined in the **HREF** attribute can be selected and accessed by Windows Media Player.</span></span>

<span data-ttu-id="31f76-140">Das **Ziel** Attribut definiert den Frame oder das Fenster, in dem der Browser die durch das **href** -Attribut definierte Seite öffnet.</span><span class="sxs-lookup"><span data-stu-id="31f76-140">The **TARGET** attribute defines the frame or window in which the browser will open the page defined by the **HREF** attribute.</span></span> <span data-ttu-id="31f76-141">Die Werte für dieses Attribut entsprechen standardmäßigen HTML-Syntax und-Definitionen.</span><span class="sxs-lookup"><span data-stu-id="31f76-141">The values for this attribute follow standard HTML syntax and definitions.</span></span> <span data-ttu-id="31f76-142">Wenn ein in einer Webseite eingebettetes Steuerelement kein **Ziel** Attribut definiert ist, lädt die URL das aktuelle Browserfenster und ersetzt die vorhandene Seite, was bedeutet, dass die Inhalte nicht mehr abgespielt werden.</span><span class="sxs-lookup"><span data-stu-id="31f76-142">In the case of a control embedded in a webpage, if no **TARGET** attribute is defined, the URL loads the current browser window and replaces the existing page, which means the content stops playing.</span></span> <span data-ttu-id="31f76-143">Daher wird empfohlen, beim Einbetten des Windows Media Player-Steuer Elements auf einer Webseite immer ein **Ziel** Attribut anzugeben.</span><span class="sxs-lookup"><span data-stu-id="31f76-143">Therefore, it is recommended that you always specify a **TARGET** attribute when embedding the Windows Media Player control in a webpage.</span></span>

<span data-ttu-id="31f76-144">Wenn die Metadatendatei im eigenständigen Windows-Media Player geöffnet ist, wird das **Ziel** Attribut ignoriert, und die URL wird in ein vorhandenes Browserfenster geladen.</span><span class="sxs-lookup"><span data-stu-id="31f76-144">If the metafile is opened in the stand-alone Windows Media Player, the **TARGET** attribute is ignored, and the URL loads in an existing browser window.</span></span> <span data-ttu-id="31f76-145">Wenn derzeit kein Browserfenster geöffnet ist, wird die URL in einem neuen Browserfenster geladen.</span><span class="sxs-lookup"><span data-stu-id="31f76-145">If there is no browser window currently open, the URL loads in a new browser window.</span></span>

## <a name="examples"></a><span data-ttu-id="31f76-146">Beispiele</span><span class="sxs-lookup"><span data-stu-id="31f76-146">Examples</span></span>


```XML
<ASX VERSION="3.0">

   <TITLE>Example Media Player Show</TITLE>
   <MOREINFO HREF="https://example.microsoft.com/info/show_info.htm" />
   
   <ENTRY>
      <TITLE>Example Clip</TITLE>
      <MOREINFO HREF="https://example.microsoft.com/info/clip1_info.htm" />
      <REF HREF="mms://example.microsoft.com/media.asf" />
   </ENTRY>
   
</ASX>

```



## <a name="requirements"></a><span data-ttu-id="31f76-147">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="31f76-147">Requirements</span></span>



| <span data-ttu-id="31f76-148">Anforderung</span><span class="sxs-lookup"><span data-stu-id="31f76-148">Requirement</span></span> | <span data-ttu-id="31f76-149">Wert</span><span class="sxs-lookup"><span data-stu-id="31f76-149">Value</span></span> |
|--------------------|-----------------------------------------------------|
| <span data-ttu-id="31f76-150">Version</span><span class="sxs-lookup"><span data-stu-id="31f76-150">Version</span></span><br/> | <span data-ttu-id="31f76-151">Windows Media Player, Version 70 oder höher</span><span class="sxs-lookup"><span data-stu-id="31f76-151">Windows Media Player version 70 or later</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="31f76-152">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="31f76-152">See also</span></span>

<dl> <dt>

[<span data-ttu-id="31f76-153">**Verweis auf Windows Media-Metadateielemente**</span><span class="sxs-lookup"><span data-stu-id="31f76-153">**Windows Media Metafile Elements Reference**</span></span>](windows-media-metafile-elements-reference.md)
</dt> <dt>

[<span data-ttu-id="31f76-154">**Referenz zu Windows Media-Metadateien**</span><span class="sxs-lookup"><span data-stu-id="31f76-154">**Windows Media Metafile Reference**</span></span>](windows-media-metafile-reference.md)
</dt> </dl>

 

 





