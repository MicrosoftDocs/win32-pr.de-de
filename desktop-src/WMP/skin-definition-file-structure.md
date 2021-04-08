---
title: Struktur der Skin-Definitionsdatei
description: Struktur der Skin-Definitionsdatei
ms.assetid: 6b9ea288-ec64-473b-b796-ab637517099a
keywords:
- Windows Media Player Skins, Skin-Definitions Dateien
- Skins, Skin-Definitions Dateien
- Dateien für Skins, Skin-Definition
- Skin-Definitions Dateien, Struktur
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6a64226fb918bcbf93c95ece52075e2c8e7ed13e
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "104037229"
---
# <a name="skin-definition-file-structure"></a><span data-ttu-id="ce7e8-107">Struktur der Skin-Definitionsdatei</span><span class="sxs-lookup"><span data-stu-id="ce7e8-107">Skin Definition File Structure</span></span>

<span data-ttu-id="ce7e8-108">Die Skin-Definitionsdatei muss einer bestimmten Struktur folgen.</span><span class="sxs-lookup"><span data-stu-id="ce7e8-108">The skin definition file must follow a specific structure.</span></span> <span data-ttu-id="ce7e8-109">Sie beginnen **mit einem Design** Element, erstellen ein oder mehrere **Ansichts** Elemente und definieren dann jedes **Ansichts** Element mit den Benutzeroberflächen Elementen, die für den gewünschten Ansichtstyp geeignet sind.</span><span class="sxs-lookup"><span data-stu-id="ce7e8-109">You start with a **THEME** element, create one or more **VIEW** elements, and then define each **VIEW** element with the user interface elements appropriate for the type of view you want to use.</span></span>

## <a name="theme-elements"></a><span data-ttu-id="ce7e8-110">Designelemente</span><span class="sxs-lookup"><span data-stu-id="ce7e8-110">THEME Elements</span></span>

<span data-ttu-id="ce7e8-111">Auf der obersten Ebene müssen Sie die Skin-Definitionsdatei **mit dem Design** -Element starten und damit schließen.</span><span class="sxs-lookup"><span data-stu-id="ce7e8-111">At the top level, you must start the skin definition file with the **THEME** element and close with it.</span></span>


```C++
<THEME>
    ...
</THEME>

```



<span data-ttu-id="ce7e8-112">Das **Theme** -Element ist das Stamm Element für Ihre Skin.</span><span class="sxs-lookup"><span data-stu-id="ce7e8-112">The **THEME** element is the root element for your skin.</span></span> <span data-ttu-id="ce7e8-113">In einer Skin-Definitionsdatei kann nur ein **Designelement vorhanden** sein, und es muss sich auf der obersten Ebene befinden.</span><span class="sxs-lookup"><span data-stu-id="ce7e8-113">There can be only one **THEME** element in a skin definition file, and it must be at the top level.</span></span> <span data-ttu-id="ce7e8-114">Design **Elemente verfügen** über bestimmte Attribute und Ambient-Attribute, die in den meisten Fällen aber nicht verwendet werden müssen.</span><span class="sxs-lookup"><span data-stu-id="ce7e8-114">**THEME** elements have specific and ambient attributes, though most of the time you will not need to use them.</span></span> <span data-ttu-id="ce7e8-115">Weitere Informationen zu diesen Attributen finden Sie in der [Skin-Programmier Referenz](skin-programming-reference.md).</span><span class="sxs-lookup"><span data-stu-id="ce7e8-115">For more information about these attributes, see the [Skin Programming Reference](skin-programming-reference.md).</span></span>

## <a name="view-elements"></a><span data-ttu-id="ce7e8-116">Elemente anzeigen</span><span class="sxs-lookup"><span data-stu-id="ce7e8-116">VIEW Elements</span></span>

<span data-ttu-id="ce7e8-117">Jedes **Design** muss mindestens ein **Ansichts** Element aufweisen.</span><span class="sxs-lookup"><span data-stu-id="ce7e8-117">Each **THEME** must have at least one **VIEW** element.</span></span> <span data-ttu-id="ce7e8-118">Das **Ansichts** Element steuert das jeweilige Bild, das auf dem Bildschirm angezeigt wird.</span><span class="sxs-lookup"><span data-stu-id="ce7e8-118">The **VIEW** element governs the particular image you see on the screen.</span></span> <span data-ttu-id="ce7e8-119">Möglicherweise möchten Sie mehr als eine Ansicht haben, damit Sie hin-und herwechseln können.</span><span class="sxs-lookup"><span data-stu-id="ce7e8-119">You may want to have more than one view, so you can switch back and forth.</span></span> <span data-ttu-id="ce7e8-120">Angenommen, Sie möchten eine große Ansicht zum Arbeiten mit Wiedergabelisten, eine mittlere Ansicht zum Überwachen von Visualisierungen und eine kleine Ansicht, die in eine Ecke des Bildschirms passt.</span><span class="sxs-lookup"><span data-stu-id="ce7e8-120">For example, you might want to have a large view for working with playlists, a medium view for watching visualizations, and a tiny view that fits in a corner of the screen.</span></span>

<span data-ttu-id="ce7e8-121">Wenn Sie mehrere Ansichten erstellen, sollten Sie sicherstellen, dass jede Ansicht über einen eindeutigen **ID** -Attribut Wert verfügt, der zum Identifizieren der Sicht verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="ce7e8-121">If you are creating multiple views, you will want to make sure that each view has a unique **ID** attribute value that will be used to identify the view.</span></span> <span data-ttu-id="ce7e8-122">Sie müssen das **BackgroundImage** -Attribut definieren, oder die Ansicht enthält kein Startbild.</span><span class="sxs-lookup"><span data-stu-id="ce7e8-122">You must define the **backgroundImage** attribute or your view will have no starting image.</span></span> <span data-ttu-id="ce7e8-123">Wenn Sie kein rechteckiges Bild anzeigen möchten, verwenden Sie wahrscheinlich das **clippingcolor** -Attribut, um die Bereiche Ihrer Skin zu definieren, die nicht angezeigt werden, und Sie möchten wahrscheinlich das **TitleBar** -Attribut des **View** -Elements festlegen.</span><span class="sxs-lookup"><span data-stu-id="ce7e8-123">If you do not want to display a rectangular image, you will probably want to use the **clippingColor** attribute to define the areas of your skin that will not display, and you will probably want to set the **titleBar** attribute of the **VIEW** element.</span></span>

<span data-ttu-id="ce7e8-124">Jedes **Ansichts** Element kann auch über ein oder mehrere **untergeordnete** Elemente verfügen.</span><span class="sxs-lookup"><span data-stu-id="ce7e8-124">Each **VIEW** element can also have one or more **SUBVIEW** elements.</span></span> <span data-ttu-id="ce7e8-125">Ein **unter Ansichts** Element ähnelt einer **Ansicht** und kann für Teile der Skin verwendet werden, die Sie bewegen, ausblenden oder anzeigen möchten.</span><span class="sxs-lookup"><span data-stu-id="ce7e8-125">A **SUBVIEW** element is similar to a **VIEW** and can be used for parts of your skin that you want to move around, hide, or show.</span></span> <span data-ttu-id="ce7e8-126">Beispielsweise kann ein **subview** -Element verwendet werden, um eine Schiebe Leiste zu erstellen, die aus ihrer Skin herausspringt, um einen Grafik-Equalizer anzuzeigen.</span><span class="sxs-lookup"><span data-stu-id="ce7e8-126">For example, a **SUBVIEW** element might be used to create a sliding tray that pops out of your skin to display a graphic equalizer.</span></span> <span data-ttu-id="ce7e8-127">**Subview** -Elemente können an der **Ansicht** ausgerichtet werden und andere besondere Beziehungen zur **Ansicht** aufweisen.</span><span class="sxs-lookup"><span data-stu-id="ce7e8-127">**SUBVIEW** elements can be aligned with the **VIEW** and have other special relationships to the **VIEW**.</span></span>

## <a name="initializing-windows-media-player"></a><span data-ttu-id="ce7e8-128">Windows-Media Player werden initialisiert.</span><span class="sxs-lookup"><span data-stu-id="ce7e8-128">Initializing Windows Media Player</span></span>

<span data-ttu-id="ce7e8-129">Sie können bestimmte anfängliche Eigenschaften von Windows Media Player mit den Elementen **Player**, **Settings** und **Controls** festlegen.</span><span class="sxs-lookup"><span data-stu-id="ce7e8-129">You can set certain initial properties of Windows Media Player by using the **PLAYER**, **SETTINGS**, and **CONTROLS** elements.</span></span> <span data-ttu-id="ce7e8-130">Beispielsweise können Sie das Volume auf eine anfängliche Ebene festlegen oder einen Standardwert für einen Dateinamen festlegen.</span><span class="sxs-lookup"><span data-stu-id="ce7e8-130">For example, you could set the volume to an initial level or give a default value for a file name.</span></span>

<span data-ttu-id="ce7e8-131">Der folgende Code zeigt, wie der **URL** -Wert in einer Skin festgelegt wird:</span><span class="sxs-lookup"><span data-stu-id="ce7e8-131">The following code shows how to set the **URL** value in a skin:</span></span>


```C++
<PLAYER
  URL = "https://proseware.com/mellow.wma">
</PLAYER>

```



<span data-ttu-id="ce7e8-132">Wenn Sie das **Autostart** -Attribut der **Einstellungen** auf false festlegen möchten, verwenden Sie den folgenden Code:</span><span class="sxs-lookup"><span data-stu-id="ce7e8-132">If you wanted to set the **autoStart** attribute of **SETTINGS** to False, you would use the following code:</span></span>


```C++
<PLAYER>
  <SETTINGS
    autoStart = "False">
  </SETTINGS>
</PLAYER>

```



<span data-ttu-id="ce7e8-133">Beachten Sie, dass das **Settings** -Element im **Player** -Element geschachtelt ist.</span><span class="sxs-lookup"><span data-stu-id="ce7e8-133">Note that the **SETTINGS** element is nested inside the **PLAYER** element.</span></span>

<span data-ttu-id="ce7e8-134">Mit diesen Elementen können die folgenden Attribute und Ereignisse zur Entwurfszeit angegeben werden:</span><span class="sxs-lookup"><span data-stu-id="ce7e8-134">Using these elements, the following attributes and events can be specified at design time:</span></span>

<span data-ttu-id="ce7e8-135">**Player-Element Attribute**</span><span class="sxs-lookup"><span data-stu-id="ce7e8-135">**PLAYER Element Attributes**</span></span>

-   <span data-ttu-id="ce7e8-136">**url**</span><span class="sxs-lookup"><span data-stu-id="ce7e8-136">**url**</span></span>
-   <span data-ttu-id="ce7e8-137">**Pufferung**</span><span class="sxs-lookup"><span data-stu-id="ce7e8-137">**Buffering**</span></span>
-   <span data-ttu-id="ce7e8-138">**Ereignis Wechsel**</span><span class="sxs-lookup"><span data-stu-id="ce7e8-138">**Currentitemchange**</span></span>
-   <span data-ttu-id="ce7e8-139">**Currentplaylistchange**</span><span class="sxs-lookup"><span data-stu-id="ce7e8-139">**Currentplaylistchange**</span></span>
-   <span data-ttu-id="ce7e8-140">**Fehler**</span><span class="sxs-lookup"><span data-stu-id="ce7e8-140">**Error**</span></span>
-   <span data-ttu-id="ce7e8-141">**Markerhit**</span><span class="sxs-lookup"><span data-stu-id="ce7e8-141">**Markerhit**</span></span>
-   <span data-ttu-id="ce7e8-142">**Mediachange**</span><span class="sxs-lookup"><span data-stu-id="ce7e8-142">**Mediachange**</span></span>
-   <span data-ttu-id="ce7e8-143">**Mediacollectionchange**</span><span class="sxs-lookup"><span data-stu-id="ce7e8-143">**Mediacollectionchange**</span></span>
-   <span data-ttu-id="ce7e8-144">**Modeänderung**</span><span class="sxs-lookup"><span data-stu-id="ce7e8-144">**Modechange**</span></span>
-   <span data-ttu-id="ce7e8-145">**Mpendstatechange**</span><span class="sxs-lookup"><span data-stu-id="ce7e8-145">**Mpenstatechange**</span></span>
-   <span data-ttu-id="ce7e8-146">**Mlaylistchange**</span><span class="sxs-lookup"><span data-stu-id="ce7e8-146">**Mlaylistchange**</span></span>
-   <span data-ttu-id="ce7e8-147">**Mlaystatechange**</span><span class="sxs-lookup"><span data-stu-id="ce7e8-147">**Mlaystatechange**</span></span>
-   <span data-ttu-id="ce7e8-148">**"Musitionchange"**</span><span class="sxs-lookup"><span data-stu-id="ce7e8-148">**Mositionchange**</span></span>
-   <span data-ttu-id="ce7e8-149">**Mcriptcommand**</span><span class="sxs-lookup"><span data-stu-id="ce7e8-149">**Mcriptcommand**</span></span>
-   <span data-ttu-id="ce7e8-150">**Mtatuschange**</span><span class="sxs-lookup"><span data-stu-id="ce7e8-150">**Mtatuschange**</span></span>

<span data-ttu-id="ce7e8-151">**SETTINGS-Element Attribute**</span><span class="sxs-lookup"><span data-stu-id="ce7e8-151">**SETTINGS Element Attributes**</span></span>

-   <span data-ttu-id="ce7e8-152">**Autostart**</span><span class="sxs-lookup"><span data-stu-id="ce7e8-152">**autoStart**</span></span>
-   <span data-ttu-id="ce7e8-153">**Schwebe**</span><span class="sxs-lookup"><span data-stu-id="ce7e8-153">**balance**</span></span>
-   <span data-ttu-id="ce7e8-154">**Basis**</span><span class="sxs-lookup"><span data-stu-id="ce7e8-154">**baseURL**</span></span>
-   <span data-ttu-id="ce7e8-155">**defaultframe**</span><span class="sxs-lookup"><span data-stu-id="ce7e8-155">**defaultFrame**</span></span>
-   <span data-ttu-id="ce7e8-156">**enableerrordialogfelder**</span><span class="sxs-lookup"><span data-stu-id="ce7e8-156">**enableErrorDialogs**</span></span>
-   <span data-ttu-id="ce7e8-157">**invokeurls**</span><span class="sxs-lookup"><span data-stu-id="ce7e8-157">**invokeURLs**</span></span>
-   <span data-ttu-id="ce7e8-158">**verstum**</span><span class="sxs-lookup"><span data-stu-id="ce7e8-158">**mute**</span></span>
-   <span data-ttu-id="ce7e8-159">**playcount**</span><span class="sxs-lookup"><span data-stu-id="ce7e8-159">**playCount**</span></span>
-   <span data-ttu-id="ce7e8-160">**zinss**</span><span class="sxs-lookup"><span data-stu-id="ce7e8-160">**rate**</span></span>
-   <span data-ttu-id="ce7e8-161">**volume**</span><span class="sxs-lookup"><span data-stu-id="ce7e8-161">**volume**</span></span>

## <a name="controls-element-attributes"></a><span data-ttu-id="ce7e8-162">Steuert Element Attribute</span><span class="sxs-lookup"><span data-stu-id="ce7e8-162">CONTROLS Element Attributes</span></span>

-   <span data-ttu-id="ce7e8-163">**currentmarker**</span><span class="sxs-lookup"><span data-stu-id="ce7e8-163">**currentMarker**</span></span>
-   <span data-ttu-id="ce7e8-164">**CurrentPosition**</span><span class="sxs-lookup"><span data-stu-id="ce7e8-164">**currentPosition**</span></span>

## <a name="other-user-interface-elements"></a><span data-ttu-id="ce7e8-165">Andere Elemente der Benutzeroberfläche</span><span class="sxs-lookup"><span data-stu-id="ce7e8-165">Other User Interface Elements</span></span>

<span data-ttu-id="ce7e8-166">Nachdem Sie das **Design und die** **Ansichts** Elemente definiert haben, müssen Sie die **Ansicht** mit bestimmten Benutzeroberflächen Elementen auffüllen.</span><span class="sxs-lookup"><span data-stu-id="ce7e8-166">Once you have defined your **THEME** and **VIEW** elements, you must populate your **VIEW** with specific user interface elements.</span></span> <span data-ttu-id="ce7e8-167">Sie müssen nicht alle verfügbaren Elemente in einer Skin verwenden, sondern nur die Elemente, die Sie benötigen.</span><span class="sxs-lookup"><span data-stu-id="ce7e8-167">You do not have to use all the available elements in a skin, just the ones you need.</span></span>

<span data-ttu-id="ce7e8-168">Wenn ein Element vom Benutzer angezeigt werden kann, wird es als Steuerelement bezeichnet.</span><span class="sxs-lookup"><span data-stu-id="ce7e8-168">If an element can be seen by the user, it is called a control.</span></span> <span data-ttu-id="ce7e8-169">Die folgenden Steuerelemente sind für Skins verfügbar:</span><span class="sxs-lookup"><span data-stu-id="ce7e8-169">The following controls are available for skins:</span></span>

-   <span data-ttu-id="ce7e8-170">Schaltflächen</span><span class="sxs-lookup"><span data-stu-id="ce7e8-170">Buttons</span></span>
-   <span data-ttu-id="ce7e8-171">Schieberegler, benutzerdefinierte Schieberegler und Status leisten</span><span class="sxs-lookup"><span data-stu-id="ce7e8-171">Sliders, custom sliders, and progress bars</span></span>
-   <span data-ttu-id="ce7e8-172">Textfelder</span><span class="sxs-lookup"><span data-stu-id="ce7e8-172">Text boxes</span></span>
-   <span data-ttu-id="ce7e8-173">Video Fenster</span><span class="sxs-lookup"><span data-stu-id="ce7e8-173">Video windows</span></span>
-   <span data-ttu-id="ce7e8-174">Visualisierungs Fenster</span><span class="sxs-lookup"><span data-stu-id="ce7e8-174">Visualization windows</span></span>
-   <span data-ttu-id="ce7e8-175">Wiedergabelisten Fenster</span><span class="sxs-lookup"><span data-stu-id="ce7e8-175">Playlist windows</span></span>
-   <span data-ttu-id="ce7e8-176">Unter Ansichts Fenster</span><span class="sxs-lookup"><span data-stu-id="ce7e8-176">Subview windows</span></span>

<span data-ttu-id="ce7e8-177">Darüber hinaus können mehrere-Elemente verwendet werden, um Windows-Media Player Aktionen weiter zu definieren, Sie erfordern jedoch visuelle Elemente wie Schaltflächen oder Schieberegler:</span><span class="sxs-lookup"><span data-stu-id="ce7e8-177">In addition, several elements can be used to further define Windows Media Player actions, but they require visual elements such as buttons or sliders:</span></span>

-   <span data-ttu-id="ce7e8-178">Video Einstellungen</span><span class="sxs-lookup"><span data-stu-id="ce7e8-178">Video settings</span></span>
-   <span data-ttu-id="ce7e8-179">Ausgleichs Einstellungen</span><span class="sxs-lookup"><span data-stu-id="ce7e8-179">Equalizer Settings</span></span>
-   <span data-ttu-id="ce7e8-180">Visualisierungs Einstellungen</span><span class="sxs-lookup"><span data-stu-id="ce7e8-180">Visualization settings</span></span>

## <a name="buttons"></a><span data-ttu-id="ce7e8-181">Schaltflächen</span><span class="sxs-lookup"><span data-stu-id="ce7e8-181">Buttons</span></span>

<span data-ttu-id="ce7e8-182">Schaltflächen sind der beliebteste Teil eines Skin.</span><span class="sxs-lookup"><span data-stu-id="ce7e8-182">Buttons are the most popular part of a skin.</span></span> <span data-ttu-id="ce7e8-183">Sie können Schaltflächen verwenden, um Aktionen wie z. b. abspielen, beenden, beenden, minimieren und wechseln zu einer anderen Ansicht zu initiieren.</span><span class="sxs-lookup"><span data-stu-id="ce7e8-183">You can use buttons to trigger actions such as play, stop, quit, minimize, and switch to different view.</span></span> <span data-ttu-id="ce7e8-184">Windows Media Player stellt dem Skin-Ersteller zwei Arten von Schaltflächen Elementen bereit: das **Button** -Element und das **ButtonGroup** -Element.</span><span class="sxs-lookup"><span data-stu-id="ce7e8-184">Windows Media Player provides the skin creator with two types of button elements: the **BUTTON** element and the **BUTTONGROUP** element.</span></span> <span data-ttu-id="ce7e8-185">Außerdem gibt es mehrere vordefinierte Typen von Schaltflächen.</span><span class="sxs-lookup"><span data-stu-id="ce7e8-185">In addition, there are several predefined types of buttons.</span></span>

-   <span data-ttu-id="ce7e8-186">**Button-Element.**</span><span class="sxs-lookup"><span data-stu-id="ce7e8-186">**BUTTON element.**</span></span> <span data-ttu-id="ce7e8-187">Das **Button** -Element wird für einzelne Schaltflächen verwendet.</span><span class="sxs-lookup"><span data-stu-id="ce7e8-187">The **BUTTON** element is used for individual buttons.</span></span> <span data-ttu-id="ce7e8-188">Wenn Sie das **Button** -Element verwenden, müssen Sie für jede Schaltfläche ein Bild angeben und die genaue Position definieren, an der die Schaltfläche relativ zum Hintergrundbild angezeigt werden soll.</span><span class="sxs-lookup"><span data-stu-id="ce7e8-188">If you use the **BUTTON** element, you must supply an image for each button and define the exact location where you want the button to appear relative to the background image.</span></span> <span data-ttu-id="ce7e8-189">Einer der Vorteile des **Schalt** Flächen Elements besteht darin, dass Sie das Schaltflächen Bild dynamisch ändern können.</span><span class="sxs-lookup"><span data-stu-id="ce7e8-189">One of the advantages of the **BUTTON** element is that you can change the button image dynamically.</span></span>
-   <span data-ttu-id="ce7e8-190">**ButtonGroup-Element.**</span><span class="sxs-lookup"><span data-stu-id="ce7e8-190">**BUTTONGROUP element.**</span></span> <span data-ttu-id="ce7e8-191">Das **ButtonGroup** -Element wird für Gruppen von Schaltflächen verwendet.</span><span class="sxs-lookup"><span data-stu-id="ce7e8-191">The **BUTTONGROUP** element is used for groups of buttons.</span></span> <span data-ttu-id="ce7e8-192">Tatsächlich müssen Sie jedes **ButtonGroup** -Element mit einem Paar **ButtonGroup** -Tags einschließen.</span><span class="sxs-lookup"><span data-stu-id="ce7e8-192">In fact, you must enclose each **BUTTONGROUP** element with a pair of **BUTTONGROUP** tags.</span></span> <span data-ttu-id="ce7e8-193">Die Verwendung von Schaltflächen Gruppen ist einfacher als die Verwendung einzelner Schaltflächen, da Sie nicht den genauen Speicherort für die einzelnen Schaltflächen angeben müssen.</span><span class="sxs-lookup"><span data-stu-id="ce7e8-193">Using button groups is easier than using individual buttons because you do not have to specify the exact location for each button.</span></span> <span data-ttu-id="ce7e8-194">Stattdessen geben Sie eine separate ImageMap an, mit der die Aktionen definiert werden, die durchgeführt werden, wenn der Mauszeiger auf einen Bereich im Hintergrund bewegt oder klickt.</span><span class="sxs-lookup"><span data-stu-id="ce7e8-194">Instead, you supply a separate image map that defines the actions that will take place when the mouse hovers over or clicks an area on your background.</span></span> <span data-ttu-id="ce7e8-195">Die Verwendung von Image Maps ist einfach, da Sie die für den Hintergrund erstellte Grafik in eine Zuordnungs Ebene in Ihrem Grafikbearbeitungsprogramm kopieren können.</span><span class="sxs-lookup"><span data-stu-id="ce7e8-195">Using image maps is easy because you can take the art you created for your background and copy it to a mapping layer in your graphics editing program.</span></span> <span data-ttu-id="ce7e8-196">Die Verwendung des Programms zur Grafikbearbeitung ist schneller und präziser, als zu versuchen, genau zu definieren, wo eine einzelne Schaltfläche auf dem Hintergrund platziert werden soll.</span><span class="sxs-lookup"><span data-stu-id="ce7e8-196">Using your graphics editing program is faster and more precise than trying to define exactly where an individual button should be placed on your background.</span></span>
-   <span data-ttu-id="ce7e8-197">**Vordefinierte Schaltflächen.**</span><span class="sxs-lookup"><span data-stu-id="ce7e8-197">**Predefined buttons.**</span></span> <span data-ttu-id="ce7e8-198">Es gibt mehrere vordefinierte Schaltflächen.</span><span class="sxs-lookup"><span data-stu-id="ce7e8-198">There are several predefined buttons.</span></span> <span data-ttu-id="ce7e8-199">Beispielsweise können Sie eine playelement-Schaltfläche verwenden, um digitale Mediendateien wiederzugeben, und ein stopelement, um die Wiedergabe zu beenden.</span><span class="sxs-lookup"><span data-stu-id="ce7e8-199">For example, you can use a PLAYELEMENT button to play digital media files, and a STOPELEMENT to stop playback.</span></span> <span data-ttu-id="ce7e8-200">Weitere Informationen finden Sie unter Button [Group](buttongroup-element.md) -Element und [Button-Element](button-element.md) in der Skin-Programmier Referenz.</span><span class="sxs-lookup"><span data-stu-id="ce7e8-200">See [BUTTONGROUP](buttongroup-element.md) Element and [BUTTON Element](button-element.md) in the Skin Programming Reference.</span></span> <span data-ttu-id="ce7e8-201">Mithilfe von [ImageButton](imagebutton.md) können Bilder angezeigt werden, die sich in Reaktion auf bestimmte Ereignisse ändern können.</span><span class="sxs-lookup"><span data-stu-id="ce7e8-201">The [IMAGEBUTTON](imagebutton.md) can be used to display images that can change in response to specific events.</span></span>

## <a name="sliders"></a><span data-ttu-id="ce7e8-202">Schieberegler</span><span class="sxs-lookup"><span data-stu-id="ce7e8-202">Sliders</span></span>

<span data-ttu-id="ce7e8-203">Schieberegler sind nützlich für die Arbeit mit Informationen, die sich im Laufe der Zeit ändern.</span><span class="sxs-lookup"><span data-stu-id="ce7e8-203">Sliders are useful for working with information that changes over time.</span></span> <span data-ttu-id="ce7e8-204">Beispielsweise können Sie einen Schieberegler verwenden, um die Menge der Musik anzugeben, die bereits für eine bestimmte Mediendatei wiedergegeben wurde.</span><span class="sxs-lookup"><span data-stu-id="ce7e8-204">For example, you might use a slider to indicate the amount of music that has already played for a particular media file.</span></span> <span data-ttu-id="ce7e8-205">Schieberegler können horizontal oder vertikal, linear oder Zirkel oder eine beliebige Form sein, die Sie sich vorstellen können.</span><span class="sxs-lookup"><span data-stu-id="ce7e8-205">Sliders can be horizontal or vertical, linear or circular, or any shape you can think of.</span></span> <span data-ttu-id="ce7e8-206">Schieberegler sind in drei Varianten enthalten: Schieberegler, Status leisten und benutzerdefinierte Schieberegler.</span><span class="sxs-lookup"><span data-stu-id="ce7e8-206">Sliders come in three varieties: sliders, progress bars, and custom sliders.</span></span>

-   <span data-ttu-id="ce7e8-207">**Rutscher.**</span><span class="sxs-lookup"><span data-stu-id="ce7e8-207">**Sliders.**</span></span> <span data-ttu-id="ce7e8-208">Sie können das **Slider** -Element für volumensteuerelemente verwenden oder den Benutzer auf einen anderen Teil des Medien Inhalts verschieben.</span><span class="sxs-lookup"><span data-stu-id="ce7e8-208">You can use the **SLIDER** element for volume controls or to allow the user to move to a different part of the media content.</span></span>
-   <span data-ttu-id="ce7e8-209">**Status leisten.**</span><span class="sxs-lookup"><span data-stu-id="ce7e8-209">**Progress bars.**</span></span> <span data-ttu-id="ce7e8-210">Status anzeigen ähneln Schiebereglern.</span><span class="sxs-lookup"><span data-stu-id="ce7e8-210">Progress bars are similar to sliders.</span></span> <span data-ttu-id="ce7e8-211">Status Indikatoren sind für die grafische Darstellung des Prozentsatzes eines bestimmten Prozesses konzipiert, der abgeschlossen wurde, jedoch nicht für einen Prozess, mit dem der Benutzer interagieren soll.</span><span class="sxs-lookup"><span data-stu-id="ce7e8-211">Progress bars are designed for graphically displaying the percentage of a particular process that has been completed, but not for a process that the user will want to interact with.</span></span> <span data-ttu-id="ce7e8-212">Beispielsweise können Sie eine Statusanzeige verwenden, um den Puffer Status anzugeben.</span><span class="sxs-lookup"><span data-stu-id="ce7e8-212">For example, you might want to use a progress bar to indicate buffering progress.</span></span>
-   <span data-ttu-id="ce7e8-213">**Benutzerdefinierte Schieberegler.**</span><span class="sxs-lookup"><span data-stu-id="ce7e8-213">**Custom sliders.**</span></span> <span data-ttu-id="ce7e8-214">Es wird eine benutzerdefinierte Schieberegler-Funktionalität bereitgestellt, sodass Sie Steuerelemente wie z. b.-Knoten erstellen oder ungewöhnliche Steuerelement Mechanismen</span><span class="sxs-lookup"><span data-stu-id="ce7e8-214">Custom slider functionality is provided so you can create controls such as knobs, or make unusual control mechanisms.</span></span> <span data-ttu-id="ce7e8-215">Wenn Sie z. b. ein Volume-Steuerelement erstellen möchten, das Ihre Skin umschließt, können Sie es mit einem benutzerdefinierten Schieberegler verwenden.</span><span class="sxs-lookup"><span data-stu-id="ce7e8-215">For example, if you want to create a volume control that wraps around your skin, you can do it with a custom slider.</span></span> <span data-ttu-id="ce7e8-216">Zum Einrichten des benutzerdefinierten Schiebereglers müssen Sie eine Imagemap erstellen, die Graustufenbilder enthält, um die Speicherorte der Werte auf dem Schieberegler zu definieren.</span><span class="sxs-lookup"><span data-stu-id="ce7e8-216">To set up the custom slider, you must create an image map that contains grayscale images to define the locations of the values on the slider.</span></span> <span data-ttu-id="ce7e8-217">Dies ist relativ einfach mit einem Grafikbearbeitungsprogramm, das Ebenen unterstützt.</span><span class="sxs-lookup"><span data-stu-id="ce7e8-217">This is relatively easy to do with a graphics editing program that supports layers.</span></span>

## <a name="text"></a><span data-ttu-id="ce7e8-218">Text</span><span class="sxs-lookup"><span data-stu-id="ce7e8-218">Text</span></span>

<span data-ttu-id="ce7e8-219">Sie können das **Text** -Element verwenden, um Text auf Ihrer Skin anzuzeigen, z. b. Titel Titel.</span><span class="sxs-lookup"><span data-stu-id="ce7e8-219">You can use the **TEXT** element to display text on your skin, such as song titles.</span></span>

## <a name="video"></a><span data-ttu-id="ce7e8-220">Video</span><span class="sxs-lookup"><span data-stu-id="ce7e8-220">Video</span></span>

<span data-ttu-id="ce7e8-221">Sie können Videos in der Skin anzeigen.</span><span class="sxs-lookup"><span data-stu-id="ce7e8-221">You can display video in your skin.</span></span> <span data-ttu-id="ce7e8-222">Mit dem **Video** -Element können Sie die Größe und Position des Videofensters festlegen.</span><span class="sxs-lookup"><span data-stu-id="ce7e8-222">The **VIDEO** element allows you to set the size and position of the video window.</span></span>

<span data-ttu-id="ce7e8-223">Sie können es dem Benutzer auch ermöglichen, die Videoeinstellungen mit dem **Video Settings** -Element zu ändern.</span><span class="sxs-lookup"><span data-stu-id="ce7e8-223">You can also allow the user to change the video settings with the **VIDEOSETTINGS** element.</span></span> <span data-ttu-id="ce7e8-224">Beispielsweise können Sie Steuerelemente erstellen, um die Helligkeit des Videos anzupassen.</span><span class="sxs-lookup"><span data-stu-id="ce7e8-224">For example, you can create controls to adjust the brightness of the video.</span></span>

<span data-ttu-id="ce7e8-225">Wenn Sie kein Video Element angeben und der Inhalt Video enthält, kehrt Windows Media Player in den vollständigen Modus zurück, und ihre Skin wird nicht angezeigt.</span><span class="sxs-lookup"><span data-stu-id="ce7e8-225">If you do not supply a video element and the content contains video, Windows Media Player will return to full mode and your skin will not be displayed.</span></span>

## <a name="equalizer-settings"></a><span data-ttu-id="ce7e8-226">Ausgleichs Einstellungen</span><span class="sxs-lookup"><span data-stu-id="ce7e8-226">Equalizer Settings</span></span>

<span data-ttu-id="ce7e8-227">Sie können das Filtern für bestimmte audiohäufigkeits Bänder mit dem Element **equalizersettings** festlegen.</span><span class="sxs-lookup"><span data-stu-id="ce7e8-227">You can set the filtering for specific audio frequency bands by using the **EQUALIZERSETTINGS** element.</span></span> <span data-ttu-id="ce7e8-228">Sie können den Bass steigern, das Treble optimieren und ihre Sounds so einrichten, dass Sie Ihren Ohren oder dem Wohnraum entsprechen.</span><span class="sxs-lookup"><span data-stu-id="ce7e8-228">You can boost the bass, tweak the treble, and set up your sounds to match your ears or your living room.</span></span>

## <a name="visualizations"></a><span data-ttu-id="ce7e8-229">Visualisierungen</span><span class="sxs-lookup"><span data-stu-id="ce7e8-229">Visualizations</span></span>

<span data-ttu-id="ce7e8-230">Visualisierungen können in der Skin angezeigt werden.</span><span class="sxs-lookup"><span data-stu-id="ce7e8-230">You can display visualizations in your skin.</span></span> <span data-ttu-id="ce7e8-231">Visualisierungen sind visuelle Effekte, die sich im Laufe der Zeit ändern, wenn Audiodaten über Windows Media Player abgespielt werden.</span><span class="sxs-lookup"><span data-stu-id="ce7e8-231">Visualizations are visual effects that change over time as audio is playing through Windows Media Player.</span></span> <span data-ttu-id="ce7e8-232">Das **Effects** -Element bestimmt, wo die Visualisierungen abgespielt werden, welche Größe das Fenster darstellen wird und welche Visualisierungen wiedergegeben werden.</span><span class="sxs-lookup"><span data-stu-id="ce7e8-232">The **EFFECTS** element determines where the visualizations will play, what size the window will be, and which visualizations will be played.</span></span>

## <a name="playlists"></a><span data-ttu-id="ce7e8-233">Wiedergabelisten</span><span class="sxs-lookup"><span data-stu-id="ce7e8-233">Playlists</span></span>

<span data-ttu-id="ce7e8-234">Sie können das **Wiedergabe** Listen-Element verwenden, um dem Benutzer zu ermöglichen, ein Element aus einer bestimmten Wiedergabeliste auszuwählen.</span><span class="sxs-lookup"><span data-stu-id="ce7e8-234">You can use the **PLAYLIST** element to let the user select an item from a specific playlist.</span></span>

## <a name="subviews"></a><span data-ttu-id="ce7e8-235">Unter Ansichten</span><span class="sxs-lookup"><span data-stu-id="ce7e8-235">Subviews</span></span>

<span data-ttu-id="ce7e8-236">Mit dem **subview** -Element können Sie sekundäre Sätze von Schnittstellen Steuerelementen anzeigen, z. b. eine Wiedergabeliste oder ein Video Steuerelement.</span><span class="sxs-lookup"><span data-stu-id="ce7e8-236">You can use the **SUBVIEW** element to display secondary sets of interface controls, such as a playlist or video controls.</span></span>

## <a name="related-topics"></a><span data-ttu-id="ce7e8-237">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="ce7e8-237">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="ce7e8-238">**Skin-Dateien**</span><span class="sxs-lookup"><span data-stu-id="ce7e8-238">**Skin Files**</span></span>](skin-files.md)
</dt> </dl>

 

 




