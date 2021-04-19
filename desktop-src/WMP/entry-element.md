---
title: Entry-Element
description: Das Entry-Element gibt eine Windows Media-Datei an, die als Clip dargestellt werden soll.
ms.assetid: 7fd16aff-2eed-4f95-92b3-b48a9d785e7c
keywords:
- Fenster "Entry Element Windows Media Player"
topic_type:
- apiref
api_name:
- ENTRY Element
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 13da18c72022c916f91bcffe7382f673ba3d4fa4
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106367187"
---
# <a name="entry-element"></a><span data-ttu-id="d2123-104">Entry-Element</span><span class="sxs-lookup"><span data-stu-id="d2123-104">ENTRY Element</span></span>

<span data-ttu-id="d2123-105">Das **Entry** -Element gibt eine Windows Media-Datei an, die als Clip dargestellt werden soll.</span><span class="sxs-lookup"><span data-stu-id="d2123-105">The **ENTRY** element specifies a Windows Media file to render as a clip.</span></span>

``` syntax
<ENTRY
   CLIENTSKIP = "YES" | "NO"
   SKIPIFREF = "YES" | "NO"
>
</ENTRY>
```

## <a name="attributes"></a><span data-ttu-id="d2123-106">Attribute</span><span class="sxs-lookup"><span data-stu-id="d2123-106">Attributes</span></span>

<span data-ttu-id="d2123-107">**Clientskip**</span><span class="sxs-lookup"><span data-stu-id="d2123-107">**CLIENTSKIP**</span></span>

<span data-ttu-id="d2123-108">Ein Wert, der angibt, ob der Benutzer den Clip vorwärts überspringen kann.</span><span class="sxs-lookup"><span data-stu-id="d2123-108">Value indicating whether the user can skip forward past the clip.</span></span>

<span data-ttu-id="d2123-109">Die folgenden Werte sind möglich.</span><span class="sxs-lookup"><span data-stu-id="d2123-109">Possible values include the following.</span></span>



| <span data-ttu-id="d2123-110">Wert</span><span class="sxs-lookup"><span data-stu-id="d2123-110">Value</span></span> | <span data-ttu-id="d2123-111">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="d2123-111">Description</span></span>                                   |
|-------|-----------------------------------------------|
| <span data-ttu-id="d2123-112">YES</span><span class="sxs-lookup"><span data-stu-id="d2123-112">YES</span></span>   | <span data-ttu-id="d2123-113">Standard.</span><span class="sxs-lookup"><span data-stu-id="d2123-113">Default.</span></span> <span data-ttu-id="d2123-114">Der Benutzer kann den Clip vorwärts überspringen.</span><span class="sxs-lookup"><span data-stu-id="d2123-114">User can skip forward past the clip.</span></span> |
| <span data-ttu-id="d2123-115">Nein</span><span class="sxs-lookup"><span data-stu-id="d2123-115">NO</span></span>    | <span data-ttu-id="d2123-116">Der Benutzer kann den Clip nicht überspringen.</span><span class="sxs-lookup"><span data-stu-id="d2123-116">User cannot skip forward past the clip.</span></span>       |



 

<span data-ttu-id="d2123-117">**Skipifref**</span><span class="sxs-lookup"><span data-stu-id="d2123-117">**SKIPIFREF**</span></span>

<span data-ttu-id="d2123-118">Ein Wert, der angibt, ob Windows Media Player diesen Clip überspringen soll, wenn das **Entry** -Element durch die Verwendung eines **ENTRYREF** -Elements in einer zweiten Metadatendatei enthalten ist.</span><span class="sxs-lookup"><span data-stu-id="d2123-118">Value indicating whether Windows Media Player should skip this clip when the **ENTRY** element is included in a second metafile through the use of an **ENTRYREF** element.</span></span>

<span data-ttu-id="d2123-119">Die folgenden Werte sind möglich.</span><span class="sxs-lookup"><span data-stu-id="d2123-119">Possible values include the following.</span></span>



| <span data-ttu-id="d2123-120">Wert</span><span class="sxs-lookup"><span data-stu-id="d2123-120">Value</span></span> | <span data-ttu-id="d2123-121">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="d2123-121">Description</span></span>                                                                                 |
|-------|---------------------------------------------------------------------------------------------|
| <span data-ttu-id="d2123-122">YES</span><span class="sxs-lookup"><span data-stu-id="d2123-122">YES</span></span>   | <span data-ttu-id="d2123-123">Windows Media Player ignoriert diesen Eintrag, wenn er über ein **ENTRYREF** -Element referenziert wird.</span><span class="sxs-lookup"><span data-stu-id="d2123-123">Windows Media Player will ignore this entry, if referenced through an **ENTRYREF** element.</span></span> |
| <span data-ttu-id="d2123-124">Nein</span><span class="sxs-lookup"><span data-stu-id="d2123-124">NO</span></span>    | <span data-ttu-id="d2123-125">Standard.</span><span class="sxs-lookup"><span data-stu-id="d2123-125">Default.</span></span> <span data-ttu-id="d2123-126">Dieser Eintrag wird von Windows Media Player nicht ignoriert.</span><span class="sxs-lookup"><span data-stu-id="d2123-126">Windows Media Player will not ignore this entry.</span></span>                                   |



 

## <a name="parentchild-elements"></a><span data-ttu-id="d2123-127">Über-/unterordnungselemente</span><span class="sxs-lookup"><span data-stu-id="d2123-127">Parent/Child Elements</span></span>



| <span data-ttu-id="d2123-128">Hierarchy</span><span class="sxs-lookup"><span data-stu-id="d2123-128">Hierarchy</span></span>       | <span data-ttu-id="d2123-129">Elemente</span><span class="sxs-lookup"><span data-stu-id="d2123-129">Elements</span></span>                                                                                                                                                                                     |
|-----------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="d2123-130">Übergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="d2123-130">Parent elements</span></span> | <span data-ttu-id="d2123-131">**ASX**, **Ereignis**, **Wiederholung**</span><span class="sxs-lookup"><span data-stu-id="d2123-131">**ASX**, **EVENT**, **REPEAT**</span></span>                                                                                                                                                               |
| <span data-ttu-id="d2123-132">Untergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="d2123-132">Child elements</span></span>  | <span data-ttu-id="d2123-133">**abstract**, **Author**, **Banner**, **Base**, **Copyright**, **Duration**, **Endmarker**, **moreinfo**, **param**, **previewduration**, **ref**, **Startmarker**, **StartTime**, **Title**</span><span class="sxs-lookup"><span data-stu-id="d2123-133">**ABSTRACT**, **AUTHOR**, **BANNER**, **BASE**, **COPYRIGHT**, **DURATION**, **ENDMARKER**, **MOREINFO**, **PARAM**, **PREVIEWDURATION**, **REF**, **STARTMARKER**, **STARTTIME**, **TITLE**</span></span> |



 

## <a name="remarks"></a><span data-ttu-id="d2123-134">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="d2123-134">Remarks</span></span>

<span data-ttu-id="d2123-135">Dieses Element ist das grundlegende Konstrukt in einer Windows Media-Metadatei.</span><span class="sxs-lookup"><span data-stu-id="d2123-135">This element is the fundamental construct in a Windows Media metafile.</span></span> <span data-ttu-id="d2123-136">Das **Entry** -Element und die zugehörigen Attribute definieren Meta-Informationen für ein einzelnes, logisches Inhalts Element, das als Clip bezeichnet wird.</span><span class="sxs-lookup"><span data-stu-id="d2123-136">The **ENTRY** element and its associated attributes define meta-information for a single, logical piece of content, called a clip.</span></span> <span data-ttu-id="d2123-137">Untergeordnete Elemente im Bereich eines **Eintrags** Elements definieren Medieninhalte für Windows-Media Player geöffnet (**ref**), Informationen zu dem Clip, den Windows Media Player als Text (**Autor**, **Copyright**, **Titel**) und andere Einstellungen im Zusammenhang mit dem Clip anzeigen wird.</span><span class="sxs-lookup"><span data-stu-id="d2123-137">Child elements within the scope of an **ENTRY** element define media content for Windows Media Player to open (**REF**), information about the clip that Windows Media Player will display as text (**AUTHOR**, **COPYRIGHT**, **TITLE**), and other settings related to the clip.</span></span> <span data-ttu-id="d2123-138">Das untergeordnete **ref** -Element verknüpft den Inhalt, der für das übergeordnete **Entry** -Element gestreamt werden soll.</span><span class="sxs-lookup"><span data-stu-id="d2123-138">The **REF** child element links the content to be streamed for the parent **ENTRY** element.</span></span> <span data-ttu-id="d2123-139">Obwohl das Skript nicht unterbricht, ist der **Eintrag** ohne untergeordnetes  Verweis bedeutungslos.</span><span class="sxs-lookup"><span data-stu-id="d2123-139">Though the script will not break, the **ENTRY** is meaningless without a **REF** child.</span></span>

<span data-ttu-id="d2123-140">Wenn der Wert des **clientskip** -Attributs "No" ist, kann der Benutzer den Inhalt nicht überspringen, der durch das **Entry** -Element definiert ist.</span><span class="sxs-lookup"><span data-stu-id="d2123-140">If the value of the **CLIENTSKIP** attribute is NO, the user cannot skip forward past the piece of content defined by the **ENTRY** element.</span></span> <span data-ttu-id="d2123-141">Dies funktioniert nicht, wenn das untergeordnete **ref** -Element auf eine andere Metadatei verweist.</span><span class="sxs-lookup"><span data-stu-id="d2123-141">This does not work if the child **REF** element references another metafile.</span></span> <span data-ttu-id="d2123-142">Auf die auf die netsted-Metadateien sollte mithilfe des **ENTRYREF** -Elements verwiesen werden.</span><span class="sxs-lookup"><span data-stu-id="d2123-142">Nested metafiles should be referenced using the **ENTRYREF** element.</span></span>

<span data-ttu-id="d2123-143">Das **skipifref** -Attribut bezieht sich nur auf **Einstiegs** Elemente, die in einer zweiten Metadatendatei durch die Verwendung eines **ENTRYREF** -Elements enthalten sind.</span><span class="sxs-lookup"><span data-stu-id="d2123-143">The **SKIPIFREF** attribute pertains only to **ENTRY** elements that are included in a second metafile through the use of an **ENTRYREF** element.</span></span> <span data-ttu-id="d2123-144">Das **ENTRYREF** -Element verweist auf eine andere Metadatendatei für die logische Einbindung in die aktuelle Datei.</span><span class="sxs-lookup"><span data-stu-id="d2123-144">The **ENTRYREF** element references another metafile for logical inclusion in the current file.</span></span> <span data-ttu-id="d2123-145">Wenn der Wert des **skipifref** -Attributs für ein **Entry** -Element aus der Metadatendatei, auf die verwiesen wird, auf "yes" gesetzt ist, ignoriert Windows Media Player diesen gezogenen Eintrag und wechselt zum nächsten **Entry** -Element, sofern vorhanden.</span><span class="sxs-lookup"><span data-stu-id="d2123-145">If the value of the **SKIPIFREF** attribute for an **ENTRY** element from the referenced metafile file is YES, Windows Media Player ignores this pulled-in entry, and moves on to the next **ENTRY** element, if any.</span></span> <span data-ttu-id="d2123-146">Das nächste **Einstiegs** Element kann der nächste Eintrag in der ursprünglichen Datei oder der nächste Eintrag in der Metadatei sein, auf die im **ENTRYREF** -Element verwiesen wird.</span><span class="sxs-lookup"><span data-stu-id="d2123-146">The next **ENTRY** element can be the next entry in the original file, or the next entry in the metafile referenced in the **ENTRYREF** element.</span></span>

## <a name="examples"></a><span data-ttu-id="d2123-147">Beispiele</span><span class="sxs-lookup"><span data-stu-id="d2123-147">Examples</span></span>


```XML
<ASX VERSION="3.0">
   <TITLE>Example Windows Media Player Show</TITLE>
   
   <ENTRY>
      <TITLE>Example Clip</TITLE>
      <REF HREF="https://example.microsoft.com/media.asf" />
   </ENTRY>
   
   <ENTRY>
      <TITLE>Another Clip</TITLE>
      <REF HREF="https://example.microsoft.com/more_media.asf" />
   </ENTRY>
</ASX>

```



## <a name="requirements"></a><span data-ttu-id="d2123-148">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="d2123-148">Requirements</span></span>



| <span data-ttu-id="d2123-149">Anforderung</span><span class="sxs-lookup"><span data-stu-id="d2123-149">Requirement</span></span> | <span data-ttu-id="d2123-150">Wert</span><span class="sxs-lookup"><span data-stu-id="d2123-150">Value</span></span> |
|--------------------|-----------------------------------------------------|
| <span data-ttu-id="d2123-151">Version</span><span class="sxs-lookup"><span data-stu-id="d2123-151">Version</span></span><br/> | <span data-ttu-id="d2123-152">Windows Media Player, Version 70 oder höher</span><span class="sxs-lookup"><span data-stu-id="d2123-152">Windows Media Player version 70 or later</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="d2123-153">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="d2123-153">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d2123-154">**Verweis auf Windows Media-Metadateielemente**</span><span class="sxs-lookup"><span data-stu-id="d2123-154">**Windows Media Metafile Elements Reference**</span></span>](windows-media-metafile-elements-reference.md)
</dt> <dt>

[<span data-ttu-id="d2123-155">**Referenz zu Windows Media-Metadateien**</span><span class="sxs-lookup"><span data-stu-id="d2123-155">**Windows Media Metafile Reference**</span></span>](windows-media-metafile-reference.md)
</dt> </dl>

 

 





