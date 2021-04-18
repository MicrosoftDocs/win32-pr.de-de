---
title: Hinzufügen des "Play"-ButtonElement
description: Hinzufügen des "Play"-ButtonElement
ms.assetid: 895850a7-7538-4581-8348-41cbb3bc9717
keywords:
- Erstellen von Skins, ButtonElement-Element
- Windows Media Player Skins, ButtonElement-Element
- Skins, ButtonElement-Element
- Skin-Definitions Dateien, ButtonElement-Element
- ButtonElement-Element
- Elemente, ButtonElement
- Erstellen von Skins, Wiedergabe Schaltflächen
- Windows Media Player Skins, Wiedergabe Schaltflächen
- Skins, Wiedergabe Schaltflächen
- Skin-Definitions Dateien, Wiedergabe Schaltflächen
- Wiedergabe Schaltflächen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a92b5416adf2e323043eb563ec08e1e4d2525733
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "104515788"
---
# <a name="adding-the-play-buttonelement"></a><span data-ttu-id="3c9a2-114">Hinzufügen des "Play"-ButtonElement</span><span class="sxs-lookup"><span data-stu-id="3c9a2-114">Adding the Play BUTTONELEMENT</span></span>

<span data-ttu-id="3c9a2-115">Schließlich können Sie die **ButtonElement** -Elemente, die die visuellen Schaltflächen auf dem Bildschirm verbinden, mit Windows-Media Player Aktionen hinzufügen.</span><span class="sxs-lookup"><span data-stu-id="3c9a2-115">Finally, you can add the **BUTTONELEMENT** elements that connect the visual buttons on the screen to Windows Media Player actions.</span></span> <span data-ttu-id="3c9a2-116">Dabei handelt es sich um den Kern ihrer Skin, den Sie als Verkabelung der Oberfläche der Skin an die inneren Maschinen von Windows Media Player vorstellen können.</span><span class="sxs-lookup"><span data-stu-id="3c9a2-116">This is the core of your skin and you can think of it as wiring the surface of the skin to the inner machinery of Windows Media Player.</span></span>

<span data-ttu-id="3c9a2-117">**ButtonElement** s sind in einer **Button Group** enthalten.</span><span class="sxs-lookup"><span data-stu-id="3c9a2-117">**BUTTONELEMENT** s are contained within a **BUTTONGROUP**.</span></span> <span data-ttu-id="3c9a2-118">In jeder **ButtonGroup** muss immer mindestens ein **ButtonElement** vorhanden sein.</span><span class="sxs-lookup"><span data-stu-id="3c9a2-118">You must always have at least one **BUTTONELEMENT** inside each **BUTTONGROUP**.</span></span>

<span data-ttu-id="3c9a2-119">Fügen Sie den Code für die Wiedergabe **ButtonElement** nach der schließenden Spitze Klammer der **ButtonGroup** ein.</span><span class="sxs-lookup"><span data-stu-id="3c9a2-119">Put the Play **BUTTONELEMENT** code after the closing angle bracket of **BUTTONGROUP**.</span></span>


```C++
        <BUTTONELEMENT
            mappingColor = "#00FF00"
            upToolTip = "Play"
            onClick = "JScript: player.URL='https://proseware.com/laure.wma';" />

```



<span data-ttu-id="3c9a2-120">Die folgenden Attribute werden verwendet, um das **ButtonElement** für die Wiedergabe Schaltfläche zu definieren:</span><span class="sxs-lookup"><span data-stu-id="3c9a2-120">The following attributes are used to define the **BUTTONELEMENT** for the Play button:</span></span>

<span data-ttu-id="3c9a2-121">**mappingColor**</span><span class="sxs-lookup"><span data-stu-id="3c9a2-121">**mappingColor**</span></span>

<span data-ttu-id="3c9a2-122">Dies ist der Farbwert eines Bereichs in der Mapping-Grafikdatei, den Sie zuvor erstellt haben.</span><span class="sxs-lookup"><span data-stu-id="3c9a2-122">This is the color value of a region in the mapping art file you created before.</span></span> <span data-ttu-id="3c9a2-123">In diesem Fall handelt es sich um eine solide grüne Farbe.</span><span class="sxs-lookup"><span data-stu-id="3c9a2-123">In this case it is the solid green color.</span></span> <span data-ttu-id="3c9a2-124">Dieses Attribut ist für ein beliebiges **ButtonElement** erforderlich.</span><span class="sxs-lookup"><span data-stu-id="3c9a2-124">This attribute is required for any **BUTTONELEMENT**.</span></span> <span data-ttu-id="3c9a2-125">Wenn Sie diese Farbe definieren, sagen Sie Windows Media Player, diesen Farbbereich dem XML-Code dieser Schaltfläche zuzuordnen.</span><span class="sxs-lookup"><span data-stu-id="3c9a2-125">By defining this color, you are telling Windows Media Player to associate this color area with the XML code of this button.</span></span>

<span data-ttu-id="3c9a2-126">**uptooltip**</span><span class="sxs-lookup"><span data-stu-id="3c9a2-126">**upToolTip**</span></span>

<span data-ttu-id="3c9a2-127">Definiert den Text, der angezeigt wird, wenn der Benutzer mit dem Mauszeiger auf die Schaltfläche zeigt.</span><span class="sxs-lookup"><span data-stu-id="3c9a2-127">This defines the text that will be displayed if the user hovers the mouse over the button.</span></span> <span data-ttu-id="3c9a2-128">Verwechseln Sie dies nicht mit der Maus, die angezeigt wird.</span><span class="sxs-lookup"><span data-stu-id="3c9a2-128">Do not confuse this with the hover art that will be displayed.</span></span> <span data-ttu-id="3c9a2-129">Eine QuickInfo ist eine kleine Sprechblase, die eine Weile dauert.</span><span class="sxs-lookup"><span data-stu-id="3c9a2-129">A ToolTip is a small balloon caption that takes a moment to appear.</span></span> <span data-ttu-id="3c9a2-130">Das Hover-Kunst Bild wird jedoch sofort in der von Ihnen gewählten Farbe und Form angezeigt.</span><span class="sxs-lookup"><span data-stu-id="3c9a2-130">The hover art image, however, will appear instantly in whatever color and shape you choose.</span></span>

<span data-ttu-id="3c9a2-131">**OnClick**</span><span class="sxs-lookup"><span data-stu-id="3c9a2-131">**onClick**</span></span>

<span data-ttu-id="3c9a2-132">Definiert das Ereignis, das auftritt, wenn mit der Maus auf die Schaltfläche geklickt wird.</span><span class="sxs-lookup"><span data-stu-id="3c9a2-132">This defines the event that occurs when the mouse clicks on the button.</span></span> <span data-ttu-id="3c9a2-133">Der Wert dieses Ereignis Attributs wird als Ereignishandler bezeichnet und ist entweder eine Zeile von Microsoft JScript-Code oder eine JScript-Funktion in einer externen Textdatei, die vom **loadscript** -Attribut einer **Ansicht** geladen wird.</span><span class="sxs-lookup"><span data-stu-id="3c9a2-133">The value of this event attribute is called an event handler and will be either a line of Microsoft JScript code, or a JScript function in an external text file that is loaded by the **loadScript** attribute of a **VIEW**.</span></span> <span data-ttu-id="3c9a2-134">In diesem Fall ruft der JScript-Code die **URL** -Methode von Windows Media Player auf, die eine Datei mit dem Namen "Laure. wma" lädt und damit beginnt.</span><span class="sxs-lookup"><span data-stu-id="3c9a2-134">In this case, the JScript code calls the **URL** method of Windows Media Player, which loads and starts playing a file named "laure.wma".</span></span> <span data-ttu-id="3c9a2-135">Beachten Sie, dass die Zeile mit einem Semikolon innerhalb der Anführungszeichen endet, was eine gute JScript-Codierungs Praxis ist.</span><span class="sxs-lookup"><span data-stu-id="3c9a2-135">Note that the line ends with a semicolon inside the quotes, which is good JScript coding practice.</span></span> <span data-ttu-id="3c9a2-136">Beachten Sie auch, dass einfache Anführungszeichen innerhalb der doppelten Anführungszeichen verwendet werden, um den Dateinamen festzulegen.</span><span class="sxs-lookup"><span data-stu-id="3c9a2-136">Note also the use of single quotes inside the double quotes to set off the file name.</span></span> <span data-ttu-id="3c9a2-137">Weitere Informationen zu JScript finden Sie im Abschnitt über die [Verwendung von JScript](using-jscript.md) im Abschnitt about Skins dieses SDK.</span><span class="sxs-lookup"><span data-stu-id="3c9a2-137">For more information about JScript, see [Using JScript](using-jscript.md) in the About Skins section of this SDK.</span></span>

<span data-ttu-id="3c9a2-138">Beachten Sie, dass kein **endbuttonelement** -Tag vorhanden ist.</span><span class="sxs-lookup"><span data-stu-id="3c9a2-138">Notice that there is no ending **BUTTONELEMENT** tag.</span></span> <span data-ttu-id="3c9a2-139">Wenn ein Element kein anderes Element einschließt, können Sie es mit dem Schrägstrich direkt vor der schließenden Spitze Klammer schließen.</span><span class="sxs-lookup"><span data-stu-id="3c9a2-139">If an element does not enclose another element, you can close it off with the forward slash just before the closing angle bracket.</span></span> <span data-ttu-id="3c9a2-140">Dies teilt XML mit, dass Sie mit diesem Element fertig sind.</span><span class="sxs-lookup"><span data-stu-id="3c9a2-140">This tells XML that you are finished with that element.</span></span> <span data-ttu-id="3c9a2-141">Beispiel:</span><span class="sxs-lookup"><span data-stu-id="3c9a2-141">For example,</span></span>


```C++
<BUTTONELEMENT></BUTTONELEMENT>
```



<span data-ttu-id="3c9a2-142">und</span><span class="sxs-lookup"><span data-stu-id="3c9a2-142">and</span></span>


```C++
<BUTTONELEMENT/>
```



<span data-ttu-id="3c9a2-143">vermitteln Sie dieselben Informationen in XML.</span><span class="sxs-lookup"><span data-stu-id="3c9a2-143">convey the same information in XML.</span></span>

<span data-ttu-id="3c9a2-144">Die Leistungsfähigkeit von Skins ergibt sich aus der Verwendung von Ereignis Handlern.</span><span class="sxs-lookup"><span data-stu-id="3c9a2-144">The power of skins comes from using event handlers.</span></span> <span data-ttu-id="3c9a2-145">Wenn der Benutzer mit einer Maus etwas bewirkt, kann dieses Ereignis mit JScript behandelt werden.</span><span class="sxs-lookup"><span data-stu-id="3c9a2-145">If the user does something with a mouse, you can handle that event with JScript.</span></span> <span data-ttu-id="3c9a2-146">Ihr Code kann eine einzelne Zeile sein, die es Windows Media Player ermöglicht, etwas einfaches Spiel auszuführen, oder es kann sich um eine in JScript geschriebene komplette Anwendung handeln.</span><span class="sxs-lookup"><span data-stu-id="3c9a2-146">Your code can be a single line that makes Windows Media Player do something simple like play, or it can be a complete application written in JScript.</span></span>

## <a name="related-topics"></a><span data-ttu-id="3c9a2-147">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="3c9a2-147">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="3c9a2-148">**Erstellen der Skin-Definitionsdatei**</span><span class="sxs-lookup"><span data-stu-id="3c9a2-148">**Creating the Skin Definition File**</span></span>](creating-the-skin-definition-file.md)
</dt> </dl>

 

 




