---
title: Erstellen der primären Grafikdatei
description: Erstellen der primären Grafikdatei
ms.assetid: 50099050-2ce8-4cbf-82b7-3018f6579bd2
keywords:
- Erstellen von Skins, Primary Art-Dateien
- Windows Media Player Skins, Grafikdateien
- Skins, Art Dateien
- Dateien für Skins, Art
- kunstdateien für Skins, primäre Bilder
- Windows Media Player Skins, primäre Images
- Skins, primäre Bilder
- primäre Images in Skins
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c9ceb92a5a87c1fc03ec7336a7ca5dd7814e4a1c
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "104562369"
---
# <a name="creating-the-primary-art-file"></a><span data-ttu-id="9a2cd-111">Erstellen der primären Grafikdatei</span><span class="sxs-lookup"><span data-stu-id="9a2cd-111">Creating the Primary Art File</span></span>

<span data-ttu-id="9a2cd-112">Die primäre Grafikdatei enthält die Kunst, die der Benutzer Ihrer Skin zuerst sieht.</span><span class="sxs-lookup"><span data-stu-id="9a2cd-112">The primary art file will contain the art that the user of your skin first sees.</span></span> <span data-ttu-id="9a2cd-113">In diesem Fall erstellen Sie Images auf unterschiedlichen Ebenen Ihres Kunstprogramms.</span><span class="sxs-lookup"><span data-stu-id="9a2cd-113">In this case, you will be creating images in different layers of your art program.</span></span> <span data-ttu-id="9a2cd-114">Der Grund für die Verwendung von Ebenen ist, dass Sie bestimmte Ebenen später kopieren, um Kartendateien und Alternative kunstdateien zu erstellen.</span><span class="sxs-lookup"><span data-stu-id="9a2cd-114">The reason for using layers is that you will copy specific layers later to create map files and alternate art files.</span></span>

<span data-ttu-id="9a2cd-115">Zum Erstellen der primären Grafikdatei erstellen Sie die folgenden Ebenen in der folgenden Reihenfolge:</span><span class="sxs-lookup"><span data-stu-id="9a2cd-115">To create the primary art file, you will create the following layers in the following order:</span></span>

<span data-ttu-id="9a2cd-116">Skin-Hintergrund Ebene</span><span class="sxs-lookup"><span data-stu-id="9a2cd-116">Skin background layer</span></span>

<span data-ttu-id="9a2cd-117">Dies ist die Farbe, die transparent ist, wenn die Skin angezeigt wird.</span><span class="sxs-lookup"><span data-stu-id="9a2cd-117">This is the color that will be transparent when the skin is displayed.</span></span> <span data-ttu-id="9a2cd-118">Erstellen Sie zuerst eine Ebene, aber wählen Sie die endgültige Farbe dieser Ebene aus, nachdem Sie eine Farbe für die Skin-Container Ebene ausgewählt haben.</span><span class="sxs-lookup"><span data-stu-id="9a2cd-118">Create a layer for this first, but choose the final color of this layer after you chose a color for the skin container layer.</span></span> <span data-ttu-id="9a2cd-119">Diese Farbe sollte ähnlich wie die Skin-Container Schicht sein, um Antialiasing-Effekte auszublenden.</span><span class="sxs-lookup"><span data-stu-id="9a2cd-119">This color should be similar to, but not the same as, the skin container layer, to hide any anti-aliasing effects.</span></span>

<span data-ttu-id="9a2cd-120">Skin-Container Ebene</span><span class="sxs-lookup"><span data-stu-id="9a2cd-120">Skin container layer</span></span>

<span data-ttu-id="9a2cd-121">Dies ist das Bild, das die Gliederung ihrer Skin bildet und die dem Benutzer angezeigt wird.</span><span class="sxs-lookup"><span data-stu-id="9a2cd-121">This is the image that will form the outline of your skin and will be what the user sees.</span></span> <span data-ttu-id="9a2cd-122">Es ist auch der Container für die beiden Schaltflächen in diesem Beispiel.</span><span class="sxs-lookup"><span data-stu-id="9a2cd-122">It also will be the container for the two buttons in this example.</span></span> <span data-ttu-id="9a2cd-123">Stellen Sie sich Ihre Skin als Container für Steuerelemente der Benutzeroberfläche wie Schaltflächen, Schieberegler usw. vor.</span><span class="sxs-lookup"><span data-stu-id="9a2cd-123">Think of your skin as a container for user interface controls such as buttons, sliders, and so on.</span></span> <span data-ttu-id="9a2cd-124">In diesem Beispiel ist der Container ein gelbes Oval.</span><span class="sxs-lookup"><span data-stu-id="9a2cd-124">In this example, the container is a yellow oval.</span></span>

<span data-ttu-id="9a2cd-125">Schaltflächen Ebenen wiedergeben und schließen</span><span class="sxs-lookup"><span data-stu-id="9a2cd-125">Play and Close button layers</span></span>

<span data-ttu-id="9a2cd-126">Dies sind die beiden Steuerelemente der Benutzeroberfläche, die in diesem Beispiel verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="9a2cd-126">These are the two user interface controls that this example uses.</span></span> <span data-ttu-id="9a2cd-127">Sie werden Sie in separaten Ebenen platzieren, damit Sie Sie problemlos anpassen oder später kopieren können.</span><span class="sxs-lookup"><span data-stu-id="9a2cd-127">You will put them in separate layers so that you can easily adjust them or copy them later.</span></span>

<span data-ttu-id="9a2cd-128">Bevor Sie die Ebenen erstellen, müssen Sie die Datei erstellen, die die Ebenen enthält.</span><span class="sxs-lookup"><span data-stu-id="9a2cd-128">Before you create your layers, you must create the file that will hold your layers.</span></span> <span data-ttu-id="9a2cd-129">Starten Sie Photoshop, und erstellen Sie eine neue Datei, die 100 Pixel hoch und 200 Pixel breit ist.</span><span class="sxs-lookup"><span data-stu-id="9a2cd-129">Start up Photoshop and create a new file that is 100 pixels high and 200 pixels wide.</span></span> <span data-ttu-id="9a2cd-130">Die Datei, die zum Erstellen der Kunst für dieses Beispiel verwendet wird, wird als tiny.psd bezeichnet und ist im SDK enthalten.</span><span class="sxs-lookup"><span data-stu-id="9a2cd-130">The file used to create the art for this sample is called tiny.psd and is included with the SDK.</span></span>

<span data-ttu-id="9a2cd-131">Alle Anweisungen werden in Form von Photoshop angegeben, aber jedes andere Kunstprogramm kann zum Erstellen von Skins verwendet werden, solange Sie in einem der Dateiformate speichern können, die von der Windows-Media Player unterstützt werden (BMP, GIF, JPG und PNG).</span><span class="sxs-lookup"><span data-stu-id="9a2cd-131">All instructions are given in terms of Photoshop, but any other art program can be used to create skins as long as you can save to one of the file formats supported by the Windows Media Player (BMP, GIF, JPG, and PNG).</span></span> <span data-ttu-id="9a2cd-132">Sie werden die Skin-Erstellung vereinfachen, wenn Sie ein Kunstprogramm verwenden, das über Ebenen wie Adobe Photoshop, Jasc Paint Shop Pro oder jedor-viskosity verfügt.</span><span class="sxs-lookup"><span data-stu-id="9a2cd-132">You will find skin creation easier if you use an art program that has layers, such as Adobe Photoshop, Jasc Paint Shop Pro, or Jedor Viscosity.</span></span> <span data-ttu-id="9a2cd-133">Ebenen sind äußerst nützlich, da Bilder ordnungsgemäß für die Bild Zuordnung und die Anzeige alternativer Bilder ausgerichtet werden müssen.</span><span class="sxs-lookup"><span data-stu-id="9a2cd-133">Layers are extremely useful because images must be properly aligned for image mapping and display of alternative images.</span></span>

## <a name="skin-background-layer"></a><span data-ttu-id="9a2cd-134">Skin-Hintergrund Ebene</span><span class="sxs-lookup"><span data-stu-id="9a2cd-134">Skin Background Layer</span></span>

<span data-ttu-id="9a2cd-135">Erstellen Sie eine neue Ebene, und nennen Sie Sie "Skin Background".</span><span class="sxs-lookup"><span data-stu-id="9a2cd-135">Create a new layer and name it "Skin background".</span></span> <span data-ttu-id="9a2cd-136">Dies wird zu der Transparenz Farbe, die Sie in der Skin-Definitionsdatei definieren.</span><span class="sxs-lookup"><span data-stu-id="9a2cd-136">This will become the transparency color you will define in the skin definition file.</span></span> <span data-ttu-id="9a2cd-137">Warten Sie, bis die Farbe für den Skin-Container ausgewählt ist, bevor Sie die Hintergrund Ebene der Skin mit einer bestimmten Farbe auffüllen.</span><span class="sxs-lookup"><span data-stu-id="9a2cd-137">Wait until the color for the skin container is chosen before filling the skin background layer with a specific color.</span></span>

## <a name="skin-container-layer"></a><span data-ttu-id="9a2cd-138">Skin-Container Ebene</span><span class="sxs-lookup"><span data-stu-id="9a2cd-138">Skin Container Layer</span></span>

<span data-ttu-id="9a2cd-139">Erstellen Sie als nächstes eine neue Ebene, und nennen Sie Sie "Skin Container".</span><span class="sxs-lookup"><span data-stu-id="9a2cd-139">Next create a new layer and call it "Skin container".</span></span> <span data-ttu-id="9a2cd-140">Dadurch werden die Kanten ihrer Skin definiert, und es handelt sich um den Container für die Schaltflächen.</span><span class="sxs-lookup"><span data-stu-id="9a2cd-140">This will define the edges of your skin and will be the container for the buttons.</span></span>

<span data-ttu-id="9a2cd-141">Wählen Sie mithilfe der Webfarb Schieberegler eine Vordergrundfarbe für die Form aus.</span><span class="sxs-lookup"><span data-stu-id="9a2cd-141">Choose a foreground color for the shape, using the Web color sliders.</span></span> <span data-ttu-id="9a2cd-142">In diesem Beispiel wurde die Farbe " \# DBDD11" ausgewählt.</span><span class="sxs-lookup"><span data-stu-id="9a2cd-142">In this example, the color "\#DBDD11" was chosen.</span></span>

<span data-ttu-id="9a2cd-143">Erstellen Sie als nächstes eine Oval-Form.</span><span class="sxs-lookup"><span data-stu-id="9a2cd-143">Next create an oval shape.</span></span> <span data-ttu-id="9a2cd-144">Die einfachste Möglichkeit besteht darin, das Eliptical-Marquee-Tool zu verwenden und eine Oval-Auswahl zu erstellen.</span><span class="sxs-lookup"><span data-stu-id="9a2cd-144">The easiest way is to use the Eliptical Marquee tool and create an oval selection.</span></span> <span data-ttu-id="9a2cd-145">Wenn Sie eine Oval-Auswahl erstellt haben, die die gewünschte Größe und Form hat, füllen Sie die Auswahl mit der Vordergrundfarbe aus, und brechen Sie die Auswahl ab.</span><span class="sxs-lookup"><span data-stu-id="9a2cd-145">When you have created an oval selection that is the size and shape you want, fill the selection with the foreground color and cancel the selection.</span></span>

<span data-ttu-id="9a2cd-146">Um dieses Aussehen etwas interessanter zu gestalten, wenden Sie den Ebeneneffekt von "Bevel" und "emboss" auf die Standardwerte an.</span><span class="sxs-lookup"><span data-stu-id="9a2cd-146">Finally, to make this look a bit more interesting, apply the layer effect of Bevel and Emboss with the default values.</span></span>

<span data-ttu-id="9a2cd-147">Ihre Skin-Container Schicht sollte wie in der folgenden Abbildung aussehen.</span><span class="sxs-lookup"><span data-stu-id="9a2cd-147">Your skin container layer should look like the following illustration.</span></span>

![Skin-Container Ebene](images/g01cont.png)

## <a name="background-skin-color"></a><span data-ttu-id="9a2cd-149">Farbe für Hintergrundfarbe</span><span class="sxs-lookup"><span data-stu-id="9a2cd-149">Background Skin Color</span></span>

<span data-ttu-id="9a2cd-150">Nachdem Sie nun eine Vordergrundfarbe für Ihre Skin-Container-Form ausgewählt haben, können Sie eine ähnliche Farbe für die Hintergrund Ebene der Skin auswählen.</span><span class="sxs-lookup"><span data-stu-id="9a2cd-150">Now that you have chosen a foreground color for your skin container shape, you can choose a similar color for your skin background layer.</span></span> <span data-ttu-id="9a2cd-151">Sie möchten nicht genau dieselbe Farbe, oder der Skin-Container ist auch transparent.</span><span class="sxs-lookup"><span data-stu-id="9a2cd-151">You do not want the exact same color, or your skin container will be transparent also.</span></span> <span data-ttu-id="9a2cd-152">Stellen Sie sicher, dass Sie diese genaue Farbe nicht an einer anderen Stelle in der Skin verwenden, sogar in Fotos, denn immer, wenn diese Farbe angezeigt wird, wird stattdessen das Desktop Bild angezeigt.</span><span class="sxs-lookup"><span data-stu-id="9a2cd-152">In fact, be sure you do not use this exact color anywhere else in your skin, even in photographs, because wherever this color appears, the desktop image will appear instead.</span></span>

<span data-ttu-id="9a2cd-153">Sie möchten eine Farbe in der Nähe der Skin-Container Farbe, um Antialiasing-Effekte zu vermeiden.</span><span class="sxs-lookup"><span data-stu-id="9a2cd-153">You want a color close to the skin container color to avoid anti-aliasing effects.</span></span> <span data-ttu-id="9a2cd-154">Wenn Sie z. b. einen schwarzen Hintergrund haben, werden möglicherweise einige Teile von schwarz um den Rand der Skin angezeigt.</span><span class="sxs-lookup"><span data-stu-id="9a2cd-154">For example, if you have a black background, some bits of black may show up around the edge of your skin.</span></span> <span data-ttu-id="9a2cd-155">Wenn Sie eine Farbe in der Nähe der Farbe des Skin-Containers auswählen, werden alle im Anti-Aliasing-Prozess aufzurufenden ungebundenen Pixel nicht angezeigt.</span><span class="sxs-lookup"><span data-stu-id="9a2cd-155">By choosing a color close to the color of the skin container, any stray pixels that show up in the anti-aliasing process will be unnoticed.</span></span>

<span data-ttu-id="9a2cd-156">Antialiasing ist der Prozess der Glättung der Kanten von schrägen oder gekrümmten Formen.</span><span class="sxs-lookup"><span data-stu-id="9a2cd-156">Anti-aliasing is the process of smoothing the edges of slanted or curved shapes.</span></span> <span data-ttu-id="9a2cd-157">Antialiasing erstellt neue Farben für Pixel entlang der Kanten einer Form, die eine Mischung aus der Vordergrundfarbe und der Hintergrundfarbe sind.</span><span class="sxs-lookup"><span data-stu-id="9a2cd-157">Anti-aliasing creates new colors, for pixels along the edges of a shape, that are a blend of the foreground color and the background color.</span></span> <span data-ttu-id="9a2cd-158">Einige dieser zwischen Farben können dazu führen, dass Pixel übersehen werden, wenn die Hintergrundfarbe transparent gemacht wird.</span><span class="sxs-lookup"><span data-stu-id="9a2cd-158">Some of these in-between colors can cause pixels to be missed when the background color is made transparent.</span></span>

<span data-ttu-id="9a2cd-159">Die Hintergrund Ebene der Skin sollte wie in der folgenden Abbildung aussehen.</span><span class="sxs-lookup"><span data-stu-id="9a2cd-159">Your skin background layer should look like the following illustration.</span></span>

![Hintergrund-Skin-Ebene](images/g01backg.png)

## <a name="play-and-close-button-layers"></a><span data-ttu-id="9a2cd-161">Schaltflächen Ebenen wiedergeben und schließen</span><span class="sxs-lookup"><span data-stu-id="9a2cd-161">Play and Close Button Layers</span></span>

<span data-ttu-id="9a2cd-162">Erstellen Sie eine neue Ebene, und benennen Sie Sie mit "Schaltfläche" Schließen ".</span><span class="sxs-lookup"><span data-stu-id="9a2cd-162">Create a new layer and name it "Close button".</span></span> <span data-ttu-id="9a2cd-163">Wenn Sie das Eliptical-Marquee-Auswahl Tool erneut verwenden, erstellen Sie einen Kreis und positionieren ihn auf der linken Seite des Gesamt Bilds.</span><span class="sxs-lookup"><span data-stu-id="9a2cd-163">Using the Eliptical Marquee selection tool again, create a circle and position it on the left side of the overall image.</span></span> <span data-ttu-id="9a2cd-164">Aktivieren Sie die Sichtbarkeit der Skin-Containerdatei, um die Auswahl zu platzieren.</span><span class="sxs-lookup"><span data-stu-id="9a2cd-164">Turn on the visibility of the skin container file to help place the selection.</span></span>

<span data-ttu-id="9a2cd-165">Wenn Sie mit der Platzierung zufrieden sind, füllen Sie die Auswahl mit einer beliebigen Farbe aus (außer der Farbe des Skin-Containers oder des Skin-Hintergrunds).</span><span class="sxs-lookup"><span data-stu-id="9a2cd-165">When you are satisfied with the placement, fill the selection with any color (except the color of the skin container or the skin background).</span></span> <span data-ttu-id="9a2cd-166">In diesem Beispiel wurde eine lila Farbe ausgewählt.</span><span class="sxs-lookup"><span data-stu-id="9a2cd-166">In this example, a purple color was chosen.</span></span> <span data-ttu-id="9a2cd-167">Sie müssen sich nicht die Anzahl der Farben merken.</span><span class="sxs-lookup"><span data-stu-id="9a2cd-167">You do not need to remember the number of the color.</span></span> <span data-ttu-id="9a2cd-168">Brechen Sie dann die Auswahl ab, und wenden Sie eine weitere Standard Abschrägung und einen emboss-Ebenen</span><span class="sxs-lookup"><span data-stu-id="9a2cd-168">Then cancel the selection and apply another default Bevel and Emboss layer effect.</span></span> <span data-ttu-id="9a2cd-169">Wenn Sie auf die Schaltfläche keine Ebeneneffekte anwenden möchten, erstellen Sie eine Kopie des Originals zur späteren Verwendung in der Zuordnung.</span><span class="sxs-lookup"><span data-stu-id="9a2cd-169">If you want to apply non-layer effects to your button, make a copy of the original for later use in mapping.</span></span>

<span data-ttu-id="9a2cd-170">Die Schaltfläche schließen sollte wie in der folgenden Abbildung aussehen.</span><span class="sxs-lookup"><span data-stu-id="9a2cd-170">Your Close button should look like the following illustration.</span></span>

![Schließ-Schaltfläche](images/g01qbut.png)

<span data-ttu-id="9a2cd-172">Erstellen Sie eine neue Ebene, und benennen Sie Sie "Wiedergabe Schaltfläche".</span><span class="sxs-lookup"><span data-stu-id="9a2cd-172">Create a new layer and name it "Play button".</span></span> <span data-ttu-id="9a2cd-173">Verwenden Sie die gleichen Verfahren wie für die Schaltfläche "Schließen", aber weisen Sie eine andere Farbe zu.</span><span class="sxs-lookup"><span data-stu-id="9a2cd-173">Use the same techniques you did for the Close button, but give it a different color.</span></span> <span data-ttu-id="9a2cd-174">In diesem Fall wurde eine rosa Schaltflächen Farbe ausgewählt, aber jede Farbe kann verwendet werden, solange Sie nicht die gleiche Farbe wie der Skin-Container hat (da Sie in den Container integriert würde) oder die Hintergrundfarbe der Skin (da Sie transparent werden würde).</span><span class="sxs-lookup"><span data-stu-id="9a2cd-174">In this case, a pink button color was chosen, but any color can be used as long as it is not the same color as the skin container (because it would blend into the container) or the skin background color (because it would become transparent).</span></span>

<span data-ttu-id="9a2cd-175">Die Wiedergabe Schaltfläche sollte wie in der folgenden Abbildung aussehen.</span><span class="sxs-lookup"><span data-stu-id="9a2cd-175">Your Play button should look like the following illustration.</span></span>

![Wiedergabe Schaltfläche](images/g01pbut.png)

## <a name="combine-layers-and-save"></a><span data-ttu-id="9a2cd-177">Kombinieren von Ebenen und speichern</span><span class="sxs-lookup"><span data-stu-id="9a2cd-177">Combine Layers and Save</span></span>

<span data-ttu-id="9a2cd-178">Nun können Sie die primäre Grafikdatei erstellen.</span><span class="sxs-lookup"><span data-stu-id="9a2cd-178">You are now ready to create the primary art file.</span></span> <span data-ttu-id="9a2cd-179">Alle Ebenen ausblenden und dann nur die folgenden Ebenen anzeigen (von oben nach unten):</span><span class="sxs-lookup"><span data-stu-id="9a2cd-179">Hide all layers and then show only the following layers, in this order (top to bottom):</span></span>

<span data-ttu-id="9a2cd-180">Wiedergabeschaltfläche</span><span class="sxs-lookup"><span data-stu-id="9a2cd-180">Play button</span></span>

<span data-ttu-id="9a2cd-181">Schaltfläche „Schließen“</span><span class="sxs-lookup"><span data-stu-id="9a2cd-181">Close button</span></span>

<span data-ttu-id="9a2cd-182">Skin-Container</span><span class="sxs-lookup"><span data-stu-id="9a2cd-182">Skin container</span></span>

<span data-ttu-id="9a2cd-183">Skin-Hintergrund</span><span class="sxs-lookup"><span data-stu-id="9a2cd-183">Skin background</span></span>

<span data-ttu-id="9a2cd-184">Speichern Sie die Datei in einer neuen Datei, indem Sie im Menü Datei den Befehl Kopie speichern verwenden.</span><span class="sxs-lookup"><span data-stu-id="9a2cd-184">Save to a new file using the Save a Copy command from the File menu.</span></span> <span data-ttu-id="9a2cd-185">Wählen Sie im Bereich speichern als des Dialog Felds Kopie speichern die Option BMP aus, und geben Sie einen Dateinamen ein, auf den Sie später in der Skin-Definitionsdatei verweisen werden.</span><span class="sxs-lookup"><span data-stu-id="9a2cd-185">Select the BMP option in the Save As portion of the Save a Copy dialog box and type a file name that you will refer to later in your skin definition file.</span></span> <span data-ttu-id="9a2cd-186">Im Idealfall sollten Sie diese im gleichen Verzeichnis speichern wie Ihre Skin-Definitionsdatei.</span><span class="sxs-lookup"><span data-stu-id="9a2cd-186">Ideally you should save this in the same directory as your skin definition file.</span></span> <span data-ttu-id="9a2cd-187">Beispielsweise können Sie diese background.bmp nennen.</span><span class="sxs-lookup"><span data-stu-id="9a2cd-187">For example, you could call this background.bmp.</span></span> <span data-ttu-id="9a2cd-188">Wählen Sie die Standardeinstellungen aus, und speichern Sie die Datei.</span><span class="sxs-lookup"><span data-stu-id="9a2cd-188">Choose the default settings and save the file.</span></span>

<span data-ttu-id="9a2cd-189">Ihre primäre Grafikdatei sollte wie folgt aussehen:</span><span class="sxs-lookup"><span data-stu-id="9a2cd-189">Your primary art file should look like this:</span></span>

![primäre Grafikdatei](images/g01prime.png)

<span data-ttu-id="9a2cd-191">Sie verwenden diesen Dateinamen als Wert für das **BackgroundImage** -Attribut des **View** -Elements in der Skin-Definitionsdatei.</span><span class="sxs-lookup"><span data-stu-id="9a2cd-191">You will use this file name as the value for the **backgroundImage** attribute of the **VIEW** element in your skin definition file.</span></span>

## <a name="related-topics"></a><span data-ttu-id="9a2cd-192">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="9a2cd-192">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="9a2cd-193">**Aufbauen Ihrer ersten Skin**</span><span class="sxs-lookup"><span data-stu-id="9a2cd-193">**Building Your First Skin**</span></span>](building-your-first-skin.md)
</dt> </dl>

 

 




