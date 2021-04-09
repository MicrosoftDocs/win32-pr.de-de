---
title: Mit Design und Ansicht beginnen
description: Mit Design und Ansicht beginnen
ms.assetid: 1ac92f3a-463a-4343-a269-5230c644b57f
keywords:
- Erstellen von Skins, Theme-Element
- Windows Media Player Skins, Theme-Element
- Skins, Theme-Element
- Skin-Definitions Dateien, Designelement
- Design-Element
- Erstellen von Skins, Ansichts Element
- Windows Media Player Skins, Ansichts Element
- Skins, Ansichts Element
- Skin-Definitions Dateien, Element anzeigen
- View-Element
- Elemente, Ansicht
- Elemente, Design
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 499444ee2093e743f58174797794a50fbf74555a
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "103856827"
---
# <a name="start-with-theme-and-view"></a><span data-ttu-id="136c2-115">Mit Design und Ansicht beginnen</span><span class="sxs-lookup"><span data-stu-id="136c2-115">Start with THEME and VIEW</span></span>

<span data-ttu-id="136c2-116">Jede Skin muss genau ein Design **Element und mindestens ein** **Ansichts** Element aufweisen.</span><span class="sxs-lookup"><span data-stu-id="136c2-116">Every skin must have exactly one **THEME** element and at least one **VIEW** element.</span></span>

<span data-ttu-id="136c2-117">Erstellen Sie mit dem Text-Editor den folgenden Text:</span><span class="sxs-lookup"><span data-stu-id="136c2-117">Using your text editor, create the following text:</span></span>


```C++
<THEME>
    <VIEW
        clippingColor = "#CCCC00"
        backgroundImage = "background.bmp"
        titleBar = "False">


    </VIEW>
</THEME>

```



<span data-ttu-id="136c2-118">Belassen Sie vor dem schließenden **Ansichts** Kennzeichen einige leere Zeilen, da Sie später weiteren Code hinzufügen.</span><span class="sxs-lookup"><span data-stu-id="136c2-118">Leave some blank lines before the closing **VIEW** tag because you'll be adding more code here later.</span></span>

<span data-ttu-id="136c2-119">Speichern Sie die Datei mit einem beliebigen Dateinamen, die Sie wünschen, aber stellen Sie sicher, dass die Erweiterung. WMS lautet.</span><span class="sxs-lookup"><span data-stu-id="136c2-119">Save your file with any file name you wish, but be sure that the extension is .wms.</span></span> <span data-ttu-id="136c2-120">Ein typischer Dateiname könnte z. b. "skinone. WMS" lauten.</span><span class="sxs-lookup"><span data-stu-id="136c2-120">For example, a typical file name might be skinone.wms.</span></span>

<span data-ttu-id="136c2-121">Jede Skin muss mit beginnen <THEME> und mit Enden </THEME>.</span><span class="sxs-lookup"><span data-stu-id="136c2-121">Every skin must start with <THEME> and end with </THEME>.</span></span> <span data-ttu-id="136c2-122">Es kann nur ein Design **Element in** der Skin vorhanden sein, aber Sie müssen über ein Element verfügen.</span><span class="sxs-lookup"><span data-stu-id="136c2-122">You can only have one **THEME** element in your skin, but you must have one.</span></span>

<span data-ttu-id="136c2-123">Sie müssen auch über mindestens ein **Ansichts** Element verfügen.</span><span class="sxs-lookup"><span data-stu-id="136c2-123">You must also have at least one **VIEW** element.</span></span> <span data-ttu-id="136c2-124">Sie können mehr als eine Ansicht haben, aber in diesem Beispiel ist nur eine **Ansicht** vorhanden.</span><span class="sxs-lookup"><span data-stu-id="136c2-124">You can have more than one **VIEW**, but this example only has one.</span></span> <span data-ttu-id="136c2-125">Sie müssen über ein öffnendes <VIEW> und ein Schließ Endes verfügen <VIEW>. Beachten Sie, dass das öffnende </VIEW> Tag das Tag nicht sofort schließt, sondern mehrere Attribute vor der schließenden Spitze Klammer (>) enthält.</span><span class="sxs-lookup"><span data-stu-id="136c2-125">You must have an opening <VIEW> and a closing <VIEW>. Notice that the opening </VIEW> tag does not close the tag right away, but includes several attributes before the closing angle bracket (>).</span></span> <span data-ttu-id="136c2-126">In diesem Beispiel werden die folgenden Attribute im **Theme** -Element verwendet:</span><span class="sxs-lookup"><span data-stu-id="136c2-126">The following attributes are used in the **THEME** element in this example:</span></span>

<span data-ttu-id="136c2-127">**clippingcolor**</span><span class="sxs-lookup"><span data-stu-id="136c2-127">**clippingColor**</span></span>

<span data-ttu-id="136c2-128">Das **clippingcolor** -Attribut wird nicht immer benötigt, wenn die Ränder der Skin rechteckig sind.</span><span class="sxs-lookup"><span data-stu-id="136c2-128">You will not always need the **clippingColor** attribute if the edges of your skin are rectangular.</span></span> <span data-ttu-id="136c2-129">Die Skin in diesem Beispiel ist Oval-geformt, sodass Sie eine clippingfarbe für die Teile der Skin benötigen, über die der Desktop angezeigt werden soll. im Wesentlichen alle Teile außerhalb der Oval.</span><span class="sxs-lookup"><span data-stu-id="136c2-129">The skin in this example is oval-shaped, so you need a clipping color for the parts of the skin that you want to see the desktop through; essentially all parts outside the oval.</span></span> <span data-ttu-id="136c2-130">In diesem Beispiel wird ein dunkles gelb verwendet, das als " \# CCCC00" im Webformat angegeben wird.</span><span class="sxs-lookup"><span data-stu-id="136c2-130">In this example skin, we will use a dark yellow, specified as "\#CCCC00" in Web format.</span></span> <span data-ttu-id="136c2-131">Die Gründe für diese Auswahl werden bei [der Erstellung der primären Grafikdatei](creating-the-primary-art-file.md)angegeben.</span><span class="sxs-lookup"><span data-stu-id="136c2-131">The reasons for this choice are given in [Creating the Primary Art File](creating-the-primary-art-file.md).</span></span> <span data-ttu-id="136c2-132">Im Grunde ist dieser Wert immer eine Zahl, die Sie aus Ihrem Kunstprogramm erhalten.</span><span class="sxs-lookup"><span data-stu-id="136c2-132">Essentially, this value will always be a number that you get from your art program.</span></span>

<span data-ttu-id="136c2-133">**backgroundImage**</span><span class="sxs-lookup"><span data-stu-id="136c2-133">**backgroundImage**</span></span>

<span data-ttu-id="136c2-134">Dies ist der Name der primären Grafikdatei.</span><span class="sxs-lookup"><span data-stu-id="136c2-134">This is the name of the primary art file.</span></span> <span data-ttu-id="136c2-135">Dabei sollte es sich um den genauen Dateinamen und den Pfad der primären Grafikdatei handeln.</span><span class="sxs-lookup"><span data-stu-id="136c2-135">It should be the exact file name and path of your primary art file.</span></span> <span data-ttu-id="136c2-136">Nur BMP-, JPG-, GIF-und PNG-Dateien werden unterstützt, und BMP wird empfohlen.</span><span class="sxs-lookup"><span data-stu-id="136c2-136">Only BMP, JPG, GIF, and PNG files are supported, and BMP is recommended.</span></span>

<span data-ttu-id="136c2-137">**TitleBar**</span><span class="sxs-lookup"><span data-stu-id="136c2-137">**titleBar**</span></span>

<span data-ttu-id="136c2-138">Diese Skin besitzt keine **TitleBar**, sodass der Wert "false" lautet.</span><span class="sxs-lookup"><span data-stu-id="136c2-138">This skin does not have a **titleBar**, so the value will be "false".</span></span> <span data-ttu-id="136c2-139">Sie benötigen nur eine Titelleiste, wenn Sie möchten, dass Ihre Skin eine Hintergrundfarbe hat und rechteckig ist.</span><span class="sxs-lookup"><span data-stu-id="136c2-139">You will only want a title bar if you want your skin to have a background color and be rectangular.</span></span>

<span data-ttu-id="136c2-140">Stellen Sie sicher, dass Sie die schließende spitze Klammer (>) hinter dem **TitleBar** -Wert ablegen, um anzugeben, dass Sie die **Sicht** definiert haben.</span><span class="sxs-lookup"><span data-stu-id="136c2-140">Be sure that you put the closing angle bracket (>) after the **titleBar** value to indicate that you are finished defining the **VIEW**.</span></span> <span data-ttu-id="136c2-141">Lassen Sie vor der schließenden **Ansicht** **und den** Design Tags einige Leerzeilen.</span><span class="sxs-lookup"><span data-stu-id="136c2-141">Leave a few blank lines before the closing **VIEW** and **THEME** tags.</span></span> <span data-ttu-id="136c2-142">Sie benötigen die Zeilen für Code, die Sie später hinzufügen werden.</span><span class="sxs-lookup"><span data-stu-id="136c2-142">You will need the lines for code that you will add later.</span></span>

## <a name="related-topics"></a><span data-ttu-id="136c2-143">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="136c2-143">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="136c2-144">**Erstellen der Skin-Definitionsdatei**</span><span class="sxs-lookup"><span data-stu-id="136c2-144">**Creating the Skin Definition File**</span></span>](creating-the-skin-definition-file.md)
</dt> </dl>

 

 




