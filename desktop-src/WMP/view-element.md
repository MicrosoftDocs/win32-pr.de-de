---
title: View-Element
description: View-Element
ms.assetid: e1dfde08-33a0-4f12-8db0-ad62e4a1d467
keywords:
- Windows Media Player Skins, Ansichts Element
- Skins, Ansichts Element
- View-Element
- Verweis für Skins, Ansichts Element
- Elemente, Ansicht
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 07e907cced22b4d1cd498054df06ac8677a7488b
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "104388435"
---
# <a name="view-element"></a><span data-ttu-id="cb295-108">View-Element</span><span class="sxs-lookup"><span data-stu-id="cb295-108">VIEW Element</span></span>

<span data-ttu-id="cb295-109">Das **View** -Element enthält die Benutzeroberflächen Details eines Skin und verwendet die in den folgenden Tabellen gezeigten Attribute, Methoden und Ereignishandler.</span><span class="sxs-lookup"><span data-stu-id="cb295-109">The **VIEW** element contains the user interface details of a skin, and uses the attributes, methods, and event handlers shown in the following tables.</span></span>

<span data-ttu-id="cb295-110">Mehrere **Ansichts** Elemente können als untergeordnete Elemente des Design **-Elements eines** Skin definiert werden, um verschiedene Schnittstellen für verschiedene Situationen bereitzustellen.</span><span class="sxs-lookup"><span data-stu-id="cb295-110">Multiple **VIEW** elements can be defined as children of the **THEME** element of a skin to provide different interfaces for different situations.</span></span> <span data-ttu-id="cb295-111">**Ansichts** Elemente können nicht als untergeordnete Elemente eines anderen Elements angegeben werden, und Sie enthalten alle anderen Skin-Elemente.</span><span class="sxs-lookup"><span data-stu-id="cb295-111">**VIEW** elements cannot be specified as children of any other element, and they contain all other skin elements.</span></span> <span data-ttu-id="cb295-112">Beachten Sie, dass jede Sicht einen eigenen Variablen Bereich hat, d. h., Sie kann keine Attributwerte für andere Sichten freigeben.</span><span class="sxs-lookup"><span data-stu-id="cb295-112">Note that each view has its own variable scope, which means it cannot share attribute values with other views.</span></span>

<span data-ttu-id="cb295-113">Das **View** Global-Attribut kann verwendet werden, um von überall darin auf ein bestimmtes **Ansichts** Element zu verweisen.</span><span class="sxs-lookup"><span data-stu-id="cb295-113">The **view** global attribute can be used to reference a specific **VIEW** element from anywhere within it.</span></span> <span data-ttu-id="cb295-114">Dies ist eine Alternative zur Verwendung des **ID** -Attributs, das in anderen **Ansichts** Elementen oder innerhalb des **Theme** -Elements verwendet werden muss.</span><span class="sxs-lookup"><span data-stu-id="cb295-114">This is an alternative to using its **id** attribute, which must be used from within other **VIEW** elements or from within the **THEME** element.</span></span>

<span data-ttu-id="cb295-115">Das **View** -Element unterstützt die folgenden Attribute.</span><span class="sxs-lookup"><span data-stu-id="cb295-115">The **VIEW** element supports the following attributes.</span></span> <span data-ttu-id="cb295-116">Attribute, die mit einem Sternchen ( \* ) gekennzeichnet sind, werden auch vom **subview** -Element unterstützt.</span><span class="sxs-lookup"><span data-stu-id="cb295-116">Attributes marked with an asterisk (\*) are also supported by the **SUBVIEW** element.</span></span>



| <span data-ttu-id="cb295-117">Attribut</span><span class="sxs-lookup"><span data-stu-id="cb295-117">Attribute</span></span>                                                       | <span data-ttu-id="cb295-118">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="cb295-118">Description</span></span>                                                                                                             |
|-----------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="cb295-119">[BackgroundColor](view-backgroundcolor.md)\*</span><span class="sxs-lookup"><span data-stu-id="cb295-119">[backgroundColor](view-backgroundcolor.md) \*</span></span>                  | <span data-ttu-id="cb295-120">Gibt die Hintergrundfarbe der **Ansicht** oder **unter Ansicht** an oder ruft diese ab.</span><span class="sxs-lookup"><span data-stu-id="cb295-120">Specifies or retrieves the background color of the **VIEW** or **SUBVIEW**.</span></span>                                             |
| <span data-ttu-id="cb295-121">[backgroundImage](view-backgroundimage.md) \*</span><span class="sxs-lookup"><span data-stu-id="cb295-121">[backgroundImage](view-backgroundimage.md) \*</span></span>                  | <span data-ttu-id="cb295-122">Gibt das Hintergrundbild der **Ansicht** oder **unter Ansicht** an oder ruft es ab.</span><span class="sxs-lookup"><span data-stu-id="cb295-122">Specifies or retrieves the background image of the **VIEW** or **SUBVIEW**.</span></span>                                             |
| [<span data-ttu-id="cb295-123">backgroundimagehueshift</span><span class="sxs-lookup"><span data-stu-id="cb295-123">backgroundImageHueShift</span></span>](view-backgroundimagehueshift.md)     | <span data-ttu-id="cb295-124">Gibt den Betrag an, um den der Farbton des Hintergrund Bilds verschoben wird, oder ruft diesen ab.</span><span class="sxs-lookup"><span data-stu-id="cb295-124">Specifies or retrieves the amount by which the hue of the background image is shifted.</span></span>                                  |
| [<span data-ttu-id="cb295-125">backgroundimagesationations</span><span class="sxs-lookup"><span data-stu-id="cb295-125">backgroundImageSaturation</span></span>](view-backgroundimagesaturation.md) | <span data-ttu-id="cb295-126">Gibt den Sättigungswert des Hintergrund Bilds an oder ruft ihn ab.</span><span class="sxs-lookup"><span data-stu-id="cb295-126">Specifies or retrieves the saturation value of the background image.</span></span>                                                    |
| <span data-ttu-id="cb295-127">[backgroundkacheln](view-backgroundtiled.md)\*</span><span class="sxs-lookup"><span data-stu-id="cb295-127">[backgroundTiled](view-backgroundtiled.md) \*</span></span>                  | <span data-ttu-id="cb295-128">Gibt einen Wert an oder Ruft einen Wert ab, der angibt, ob das Hintergrundbild der **Ansicht** oder der **unter Ansicht** gekachelt wird.</span><span class="sxs-lookup"><span data-stu-id="cb295-128">Specifies or retrieves a value indicating whether the background image of the **VIEW** or **SUBVIEW** is tiled.</span></span>         |
| [<span data-ttu-id="cb295-129">category</span><span class="sxs-lookup"><span data-stu-id="cb295-129">category</span></span>](view-category.md)                                   | <span data-ttu-id="cb295-130">Gibt die Kategorie an, für die die Benutzeroberfläche angezeigt wird, oder ruft Sie ab.</span><span class="sxs-lookup"><span data-stu-id="cb295-130">Specifies or retrieves the category for which the user interface will appear.</span></span>                                           |
| [<span data-ttu-id="cb295-131">focusobjectid</span><span class="sxs-lookup"><span data-stu-id="cb295-131">focusObjectID</span></span>](view-focusobjectid.md)                         | <span data-ttu-id="cb295-132">Gibt einen Wert an, der angibt, welches Element den Tastaturfokus besitzt, oder ruft diesen ab</span><span class="sxs-lookup"><span data-stu-id="cb295-132">Specifies or retrieves a value indicating which element has keyboard focus.</span></span>                                             |
| [<span data-ttu-id="cb295-133">MaxHeight</span><span class="sxs-lookup"><span data-stu-id="cb295-133">maxHeight</span></span>](view-maxheight.md)                                 | <span data-ttu-id="cb295-134">Gibt die maximale Höhe der **Ansicht** an, wenn die Größe geändert wird, oder ruft Sie ab.</span><span class="sxs-lookup"><span data-stu-id="cb295-134">Specifies or retrieves the maximum height of the **VIEW** when resizing.</span></span>                                                |
| [<span data-ttu-id="cb295-135">maxWidth</span><span class="sxs-lookup"><span data-stu-id="cb295-135">maxWidth</span></span>](view-maxwidth.md)                                   | <span data-ttu-id="cb295-136">Gibt die maximale Breite der **Ansicht** an, wenn die Größe geändert wird, oder ruft Sie ab.</span><span class="sxs-lookup"><span data-stu-id="cb295-136">Specifies or retrieves the maximum width of the **VIEW** when resizing.</span></span>                                                 |
| [<span data-ttu-id="cb295-137">minHeight</span><span class="sxs-lookup"><span data-stu-id="cb295-137">minHeight</span></span>](view-minheight.md)                                 | <span data-ttu-id="cb295-138">Gibt die Mindesthöhe der **Ansicht** an, wenn die Größe geändert wird, oder ruft Sie ab.</span><span class="sxs-lookup"><span data-stu-id="cb295-138">Specifies or retrieves the minimum height of the **VIEW** when resizing.</span></span>                                                |
| [<span data-ttu-id="cb295-139">minWidth</span><span class="sxs-lookup"><span data-stu-id="cb295-139">minWidth</span></span>](view-minwidth.md)                                   | <span data-ttu-id="cb295-140">Gibt die minimale Breite der **Ansicht** an, wenn die Größe geändert wird, oder ruft Sie ab.</span><span class="sxs-lookup"><span data-stu-id="cb295-140">Specifies or retrieves the minimum width of the **VIEW** when resizing.</span></span>                                                 |
| [<span data-ttu-id="cb295-141">geändert</span><span class="sxs-lookup"><span data-stu-id="cb295-141">resizable</span></span>](view-resizable.md)                                 | <span data-ttu-id="cb295-142">Gibt einen Wert an, der angibt, ob die **Ansicht** geändert werden kann, oder ruft ihn ab.</span><span class="sxs-lookup"><span data-stu-id="cb295-142">Specifies or retrieves a value indicating whether the **VIEW** can be resized.</span></span>                                          |
| [<span data-ttu-id="cb295-143">resizebackgroundimage</span><span class="sxs-lookup"><span data-stu-id="cb295-143">resizeBackgroundImage</span></span>](view-resizebackgroundimage.md)         | <span data-ttu-id="cb295-144">Gibt einen Wert an oder ruft ihn ab, der angibt, ob die Größe des Hintergrund Bilds geändert werden kann.</span><span class="sxs-lookup"><span data-stu-id="cb295-144">Specifies or retrieves a value indicating whether the background image can be resized.</span></span>                                  |
| [<span data-ttu-id="cb295-145">scriptFile</span><span class="sxs-lookup"><span data-stu-id="cb295-145">scriptFile</span></span>](view-scriptfile.md)                               | <span data-ttu-id="cb295-146">Gibt die Dateinamen der begleitenden JScript-Dateien an.</span><span class="sxs-lookup"><span data-stu-id="cb295-146">Specifies the file names of accompanying JScript files.</span></span>                                                                 |
| [<span data-ttu-id="cb295-147">TimerInterval</span><span class="sxs-lookup"><span data-stu-id="cb295-147">timerInterval</span></span>](view-timerinterval.md)                         | <span data-ttu-id="cb295-148">Gibt das Intervall (in Millisekunden) an, in dem der Timer Ereignisse in den **OnTimer** -Ereignishandler auslöst, oder ruft es ab.</span><span class="sxs-lookup"><span data-stu-id="cb295-148">Specifies or retrieves the interval, in milliseconds, at which the timer fires events to the **ontimer** event handler.</span></span> |
| [<span data-ttu-id="cb295-149">title</span><span class="sxs-lookup"><span data-stu-id="cb295-149">title</span></span>](view-title.md)                                         | <span data-ttu-id="cb295-150">Gibt den Titel der **Ansicht** an oder ruft ihn ab.</span><span class="sxs-lookup"><span data-stu-id="cb295-150">Specifies or retrieves the title of the **VIEW**.</span></span> <span data-ttu-id="cb295-151">Kann nur zur Entwurfszeit festgelegt werden.</span><span class="sxs-lookup"><span data-stu-id="cb295-151">Can only be set at design time.</span></span>                                       |
| [<span data-ttu-id="cb295-152">TitleBar</span><span class="sxs-lookup"><span data-stu-id="cb295-152">titleBar</span></span>](view-titlebar.md)                                   | <span data-ttu-id="cb295-153">Gibt einen Wert an, der angibt, ob die Fenstertitelleiste angezeigt wird, oder ruft diesen ab.</span><span class="sxs-lookup"><span data-stu-id="cb295-153">Specifies or retrieves a value indicating whether the window title bar is shown.</span></span>                                        |
| <span data-ttu-id="cb295-154">[transparendcolor](view-transparencycolor.md)\*</span><span class="sxs-lookup"><span data-stu-id="cb295-154">[transparencyColor](view-transparencycolor.md) \*</span></span>              | <span data-ttu-id="cb295-155">Gibt die Transparenz Farbe des Hintergrund Bilds an oder ruft diese ab.</span><span class="sxs-lookup"><span data-stu-id="cb295-155">Specifies or retrieves the transparency color of the background image.</span></span>                                                  |



 

<span data-ttu-id="cb295-156">Das **View** -Element unterstützt die folgenden Methoden.</span><span class="sxs-lookup"><span data-stu-id="cb295-156">The **VIEW** element supports the following methods.</span></span>



| <span data-ttu-id="cb295-157">Methode</span><span class="sxs-lookup"><span data-stu-id="cb295-157">Method</span></span>                                              | <span data-ttu-id="cb295-158">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="cb295-158">Description</span></span>                                                |
|-----------------------------------------------------|------------------------------------------------------------|
| [<span data-ttu-id="cb295-159">close</span><span class="sxs-lookup"><span data-stu-id="cb295-159">close</span></span>](view-close.md)                             | <span data-ttu-id="cb295-160">Schließt die **Ansicht**.</span><span class="sxs-lookup"><span data-stu-id="cb295-160">Closes the **VIEW**.</span></span>                                       |
| [<span data-ttu-id="cb295-161">optimieren</span><span class="sxs-lookup"><span data-stu-id="cb295-161">maximize</span></span>](view-maximize.md)                       | <span data-ttu-id="cb295-162">Maximiert die **Ansicht**.</span><span class="sxs-lookup"><span data-stu-id="cb295-162">Maximizes the **VIEW**.</span></span>                                    |
| [<span data-ttu-id="cb295-163">Verkleinern</span><span class="sxs-lookup"><span data-stu-id="cb295-163">minimize</span></span>](view-minimize.md)                       | <span data-ttu-id="cb295-164">Minimiert die **Ansicht**.</span><span class="sxs-lookup"><span data-stu-id="cb295-164">Minimizes the **VIEW**.</span></span>                                    |
| [<span data-ttu-id="cb295-165">restore</span><span class="sxs-lookup"><span data-stu-id="cb295-165">restore</span></span>](view-restore.md)                         | <span data-ttu-id="cb295-166">Stellt die **Ansicht** wieder her.</span><span class="sxs-lookup"><span data-stu-id="cb295-166">Restores the **VIEW**.</span></span>                                     |
| [<span data-ttu-id="cb295-167">returntomediacenter</span><span class="sxs-lookup"><span data-stu-id="cb295-167">returnToMediaCenter</span></span>](view-returntomediacenter.md) | <span data-ttu-id="cb295-168">Gibt den Benutzer in den vollständigen Modus von Windows-Media Player zurück.</span><span class="sxs-lookup"><span data-stu-id="cb295-168">Returns the user to the full mode of Windows Media Player.</span></span> |
| [<span data-ttu-id="cb295-169">size</span><span class="sxs-lookup"><span data-stu-id="cb295-169">size</span></span>](view-size.md)                               | <span data-ttu-id="cb295-170">Ändert die Größe der **Ansicht** an einem angegebenen Rand.</span><span class="sxs-lookup"><span data-stu-id="cb295-170">Resizes the **VIEW** on a specified edge.</span></span>                  |



 

<span data-ttu-id="cb295-171">Das **View** -Element kann die folgenden Ereignishandler implementieren.</span><span class="sxs-lookup"><span data-stu-id="cb295-171">The **VIEW** element can implement the following event handlers.</span></span>



| <span data-ttu-id="cb295-172">Ereignishandler</span><span class="sxs-lookup"><span data-stu-id="cb295-172">Event handler</span></span>               | <span data-ttu-id="cb295-173">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="cb295-173">Description</span></span>                                                                |
|-----------------------------|----------------------------------------------------------------------------|
| [<span data-ttu-id="cb295-174">OnClose</span><span class="sxs-lookup"><span data-stu-id="cb295-174">onclose</span></span>](view-onclose.md) | <span data-ttu-id="cb295-175">Behandelt ein Ereignis, das auftritt, wenn die **Ansicht** geschlossen wird.</span><span class="sxs-lookup"><span data-stu-id="cb295-175">Handles an event that occurs when the **VIEW** is about to be closed.</span></span>      |
| [<span data-ttu-id="cb295-176">OnError</span><span class="sxs-lookup"><span data-stu-id="cb295-176">onerror</span></span>](view-onerror.md) | <span data-ttu-id="cb295-177">Behandelt ein Fehler Ereignis, wenn **Settings. enableerrordialogs** auf false festgelegt ist.</span><span class="sxs-lookup"><span data-stu-id="cb295-177">Handles an error event if **Settings.enableErrorDialogs** is set to false.</span></span> |
| [<span data-ttu-id="cb295-178">OnLoad</span><span class="sxs-lookup"><span data-stu-id="cb295-178">onload</span></span>](view-onload.md)   | <span data-ttu-id="cb295-179">Behandelt ein Ereignis, das auftritt, wenn die **Ansicht** zum ersten Mal angezeigt wird.</span><span class="sxs-lookup"><span data-stu-id="cb295-179">Handles an event that occurs when the **VIEW** is first displayed.</span></span>         |
| [<span data-ttu-id="cb295-180">OnTimer</span><span class="sxs-lookup"><span data-stu-id="cb295-180">ontimer</span></span>](view-ontimer.md) | <span data-ttu-id="cb295-181">Behandelt Timer-Ereignisse.</span><span class="sxs-lookup"><span data-stu-id="cb295-181">Handles timer events.</span></span>                                                      |



 

<span data-ttu-id="cb295-182">Das **View** -Element unterstützt die Ambient-Attribute und kann die Umgebungs Ereignishandler implementieren, sofern nicht angegeben.</span><span class="sxs-lookup"><span data-stu-id="cb295-182">The **VIEW** element supports the ambient attributes and can implement the ambient event handlers, except where noted.</span></span> <span data-ttu-id="cb295-183">Weitere Informationen finden Sie unter [Ambient-Attribute](ambient-attributes.md) und [Ambient-Ereignishandler](ambient-event-handlers.md).</span><span class="sxs-lookup"><span data-stu-id="cb295-183">For more information, see [Ambient Attributes](ambient-attributes.md) and [Ambient Event Handlers](ambient-event-handlers.md),</span></span>

## <a name="related-topics"></a><span data-ttu-id="cb295-184">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="cb295-184">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="cb295-185">**Referenz zur Skin-Programmierung**</span><span class="sxs-lookup"><span data-stu-id="cb295-185">**Skin Programming Reference**</span></span>](skin-programming-reference.md)
</dt> </dl>

 

 




