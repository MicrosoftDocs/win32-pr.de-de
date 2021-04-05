---
title: Beispiel für einfache Kunst
description: Beispiel für einfache Kunst
ms.assetid: e17c29c3-3bc6-43f5-83e1-94005218417f
keywords:
- Windows Media Player Skins, Grafikdateien
- Skins, Art Dateien
- Dateien für Skins, Art
- kunstdateien für Skins, Beispiele
- Windows Media Player Skins, Beispiele
- Skins, Beispiele
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: cab7b25dc33da70a627f8b0e126d6797b1bcdd9f
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "103710008"
---
# <a name="simple-art-example"></a><span data-ttu-id="a091a-109">Beispiel für einfache Kunst</span><span class="sxs-lookup"><span data-stu-id="a091a-109">Simple Art Example</span></span>

<span data-ttu-id="a091a-110">Drei kunstdateien sind erforderlich, um eine einfache Skin mit zwei Schaltflächen zu erstellen.</span><span class="sxs-lookup"><span data-stu-id="a091a-110">Three art files are needed to create a simple skin with two buttons.</span></span> <span data-ttu-id="a091a-111">Ein primäres Image und ein Mapping-Image sind erforderlich, und ein alternatives Bild bietet dem Benutzer einen visuellen Hinweis darauf, dass eine Schaltfläche klickbar ist.</span><span class="sxs-lookup"><span data-stu-id="a091a-111">A primary image and a mapping image are required, and an alternate image provides a visual cue to the user that a button is clickable.</span></span>

<span data-ttu-id="a091a-112">Diese kunstdateien wurden in einem Kunstprogramm erstellt, das Ebenen verwendet.</span><span class="sxs-lookup"><span data-stu-id="a091a-112">These art files were created in an art program that uses layers.</span></span> <span data-ttu-id="a091a-113">Durch die Verwendung von Ebenen ist es einfacher, sicherzustellen, dass das primäre, das Mapping-und das alternative Image die gleiche Größe haben und einander zueinander stehen.</span><span class="sxs-lookup"><span data-stu-id="a091a-113">Using layers makes it easier to make sure that your primary, mapping, and alternate images are all the same size and line up with each other.</span></span>

<span data-ttu-id="a091a-114">Ausführliche Anweisungen zum Erstellen der Kunst finden Sie im [Handbuch zur Erstellung von Skin](skin-creation-guide.md).</span><span class="sxs-lookup"><span data-stu-id="a091a-114">The detailed instructions on creating the art are in the [Skin Creation Guide](skin-creation-guide.md).</span></span>

## <a name="primary-image"></a><span data-ttu-id="a091a-115">Primäres Bild</span><span class="sxs-lookup"><span data-stu-id="a091a-115">Primary Image</span></span>

<span data-ttu-id="a091a-116">Das primäre Abbild ist ein einfaches gelbes Oval mit zwei Schaltflächen, ein rosa zum Starten von Windows Media Player und eine violette Schaltfläche, um es anzuhalten.</span><span class="sxs-lookup"><span data-stu-id="a091a-116">The primary image is a simple yellow oval with two buttons, a pink one to start Windows Media Player and purple button to stop it.</span></span> <span data-ttu-id="a091a-117">Der Hintergrund ist etwas dunkler gelb als das Oval.</span><span class="sxs-lookup"><span data-stu-id="a091a-117">The background is a slightly darker yellow than the oval.</span></span> <span data-ttu-id="a091a-118">Dieses Bild wird in der folgenden Abbildung dargestellt.</span><span class="sxs-lookup"><span data-stu-id="a091a-118">This image is shown in the following illustration.</span></span>

![primäres Image](images/absam01b.png)

<span data-ttu-id="a091a-120">Das primäre Abbild stammt aus den folgenden Images, jeweils in einer separaten Ebene.</span><span class="sxs-lookup"><span data-stu-id="a091a-120">The primary image was from the following images, each in a separate layer.</span></span> <span data-ttu-id="a091a-121">Zuerst wurde eine Oval mit einer ebenenschrägung und einem Prägung-Effekt erstellt.</span><span class="sxs-lookup"><span data-stu-id="a091a-121">First an oval was created with a layer bevel and emboss effect.</span></span> <span data-ttu-id="a091a-122">Dieses Bild wird in der folgenden Abbildung dargestellt.</span><span class="sxs-lookup"><span data-stu-id="a091a-122">This image is shown in the following illustration.</span></span>

![Oval-Image](images/absam01s.png)

<span data-ttu-id="a091a-124">Anschließend wurden die beiden Schaltflächen erstellt, auch mit der ebenenschrägung und den Prägung-Effekten.</span><span class="sxs-lookup"><span data-stu-id="a091a-124">Then the two buttons were created, also with layer bevel and emboss effects.</span></span> <span data-ttu-id="a091a-125">Dies ist in der folgenden Abbildung dargestellt.</span><span class="sxs-lookup"><span data-stu-id="a091a-125">This is shown in the following illustration.</span></span>

![zwei Schaltflächen](images/absam01p.png)

<span data-ttu-id="a091a-127">Im nächsten Schritt wurde der Bild Hintergrund erstellt.</span><span class="sxs-lookup"><span data-stu-id="a091a-127">Next the image background was created.</span></span> <span data-ttu-id="a091a-128">Es wurde ein etwas dunkleres gelbes ausgewählt, sodass alle Antialiasing zwischen dem Oval und dem Hintergrund nicht bemerkt werden.</span><span class="sxs-lookup"><span data-stu-id="a091a-128">A slightly darker yellow was chosen so that any anti-aliasing between the oval and the background will not be noticed.</span></span> <span data-ttu-id="a091a-129">Der Farbwert ist \# CCCC00.</span><span class="sxs-lookup"><span data-stu-id="a091a-129">The color value is \#CCCC00.</span></span> <span data-ttu-id="a091a-130">Dieses Bild wird in der folgenden Abbildung dargestellt.</span><span class="sxs-lookup"><span data-stu-id="a091a-130">This image is shown in the following illustration.</span></span>

![Hintergrundbild](images/absam01y.png)

<span data-ttu-id="a091a-132">Die Ebenen, in denen diese Bilder enthalten waren, wurden sichtbar gemacht und als Kopie im Bitmapformat gespeichert, wodurch das primäre Image erstellt wurde.</span><span class="sxs-lookup"><span data-stu-id="a091a-132">The layers that contained these images were made visible and saved as a copy in bitmap format, creating the primary image.</span></span> <span data-ttu-id="a091a-133">Das primäre zusammengesetzte Image wird vom **BackgroundImage** -Attribut des **Ansichts** Elements verwendet.</span><span class="sxs-lookup"><span data-stu-id="a091a-133">The primary composite image will be used by the **backgroundImage** attribute of the **VIEW** element.</span></span>

## <a name="mapping-image"></a><span data-ttu-id="a091a-134">Bild Zuordnung</span><span class="sxs-lookup"><span data-stu-id="a091a-134">Mapping Image</span></span>

<span data-ttu-id="a091a-135">Ein Mapping-Bild wird benötigt, um anzugeben, wann und wo ein Skin geklickt wird.</span><span class="sxs-lookup"><span data-stu-id="a091a-135">A mapping image is needed to specify when and where a skin is clicked.</span></span> <span data-ttu-id="a091a-136">Ein Mapping-Bild wurde mit einem roten Bereich und einem grünen Bereich erstellt.</span><span class="sxs-lookup"><span data-stu-id="a091a-136">A mapping image was created with a red area and a green area.</span></span> <span data-ttu-id="a091a-137">Dieses Bild wird in der folgenden Abbildung dargestellt.</span><span class="sxs-lookup"><span data-stu-id="a091a-137">This image is shown in the following illustration.</span></span>

![Bild Zuordnung](images/absam01m.png)

<span data-ttu-id="a091a-139">Der grüne Bereich wird verwendet, um den Bereich auf der Skin zu identifizieren, der die Windows-Media Player startet, und der Rote Bereich wird verwendet, um ihn zu verhindern.</span><span class="sxs-lookup"><span data-stu-id="a091a-139">The green area will be used to identify the area on the skin that will start Windows Media Player and the red area will be used to stop it.</span></span> <span data-ttu-id="a091a-140">Das Mapping-Image entspricht der Größe des primären Bilds.</span><span class="sxs-lookup"><span data-stu-id="a091a-140">The mapping image is the same size as the primary image.</span></span>

<span data-ttu-id="a091a-141">Das Zuordnungsbild wurde erstellt, indem die Schaltflächen Ebene in eine neue Ebene kopiert und die Abschrägung und der Prägung-Effekt deaktiviert wurde.</span><span class="sxs-lookup"><span data-stu-id="a091a-141">The mapping image was created by copying the button layer to a new layer and turning off the bevel and emboss effect.</span></span> <span data-ttu-id="a091a-142">Flatimages werden für die Zuordnung benötigt, da Windows-Media Player in jedem Bereich nach einzelnen Farbwerten suchen werden.</span><span class="sxs-lookup"><span data-stu-id="a091a-142">Flat images are needed for mapping because Windows Media Player will be looking for single color values in each area.</span></span> <span data-ttu-id="a091a-143">Sie kann nur nach einer von Ihnen definierten Farbe suchen, z. b \# . rot (FF0000).</span><span class="sxs-lookup"><span data-stu-id="a091a-143">It can only search for a color you define, such as red (\#FF0000).</span></span> <span data-ttu-id="a091a-144">Wenn das Image eine Abschrägung oder eine andere Auswirkung hat, ist nicht alles genau das rote, das Sie benötigen.</span><span class="sxs-lookup"><span data-stu-id="a091a-144">If your image has a bevel or other effect, not all of it will be the exact red you need.</span></span>

<span data-ttu-id="a091a-145">Damit die zuordnungsschaltflächen leicht zu merken sind, wurden die Bilder mit reiner roter und reiner grüner Farbe gefüllt, aber es kann eine beliebige Farbe verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="a091a-145">To make the mapping buttons an easy color to remember, the images were filled with pure red and pure green, but any color can be used.</span></span> <span data-ttu-id="a091a-146">Sie müssen sich die Farbnummern in der Zuordnung merken, damit Sie in der XML-Datei mit den Skin-Definitionen eingegeben werden können.</span><span class="sxs-lookup"><span data-stu-id="a091a-146">You will need to remember the color numbers in your map so that they can be entered in the XML skin definition file.</span></span> <span data-ttu-id="a091a-147">In diesem Fall ist rot \# FF0000 und grün ist \# 00FF00.</span><span class="sxs-lookup"><span data-stu-id="a091a-147">In this case, red is \#FF0000 and green is \#00FF00.</span></span>

<span data-ttu-id="a091a-148">Wenn nur die neue Ebene sichtbar ist, wurde das Image als Kopie in eine BMP-Datei gespeichert.</span><span class="sxs-lookup"><span data-stu-id="a091a-148">Then, with only the new layer visible, the image was saved as a copy to a BMP file.</span></span> <span data-ttu-id="a091a-149">Sie wird vom **mappingImage** -Attribut des **ButtonGroup** -Elements aufgerufen.</span><span class="sxs-lookup"><span data-stu-id="a091a-149">It will be called by the **mappingImage** attribute of the **BUTTONGROUP** element.</span></span>

## <a name="alternate-image"></a><span data-ttu-id="a091a-150">Alternatives Bild</span><span class="sxs-lookup"><span data-stu-id="a091a-150">Alternate Image</span></span>

<span data-ttu-id="a091a-151">Alternative Bilder sind nicht erforderlich, aber Sie sind sehr nützlich, um dem Benutzer visuelle Hinweise zu übergeben.</span><span class="sxs-lookup"><span data-stu-id="a091a-151">Alternate images are not required but are very useful to give visual cues to the user.</span></span> <span data-ttu-id="a091a-152">In diesem Fall wird ein Hover-Bild empfohlen, damit der Benutzer weiß, auf welche Bereiche geklickt werden kann.</span><span class="sxs-lookup"><span data-stu-id="a091a-152">In this case, a hover image is recommended so that the user knows what areas can be clicked on.</span></span>

<span data-ttu-id="a091a-153">Ein alternatives Bild wurde mit zwei gelben Schaltflächen erstellt.</span><span class="sxs-lookup"><span data-stu-id="a091a-153">An alternate image was created with two yellow buttons.</span></span> <span data-ttu-id="a091a-154">Dies ist in der folgenden Abbildung dargestellt.</span><span class="sxs-lookup"><span data-stu-id="a091a-154">This is shown in the following illustration.</span></span>

![Bild mit Hover](images/absam01h.png)

<span data-ttu-id="a091a-156">Das alternative Bild wurde erstellt, indem die ursprüngliche Schaltflächen Ebene in eine neue Ebene kopiert und anschließend die Füllfarbe in Gelb geändert wurde.</span><span class="sxs-lookup"><span data-stu-id="a091a-156">The alternate image was created by copying the original button layer to a new layer and then changing the fill color to yellow.</span></span> <span data-ttu-id="a091a-157">Der Effekt der einschrägung und der Prägung wurde beibehalten.</span><span class="sxs-lookup"><span data-stu-id="a091a-157">The bevel and emboss effect was kept.</span></span> <span data-ttu-id="a091a-158">Anschließend wurde eine neue Ebene erstellt, und es wurden Bilder hinzugefügt: der Pfeil gibt "Play" an, und das Quadrat zeigt "Ende" an.</span><span class="sxs-lookup"><span data-stu-id="a091a-158">Then a new layer was created and images were added: the arrow indicates "play" and the square indicates "stop".</span></span> <span data-ttu-id="a091a-159">Wenn nur die neue gelbe Schaltfläche und die typebenen sichtbar sind, wurde das Bild als Kopie in eine Bitmapdatei gespeichert.</span><span class="sxs-lookup"><span data-stu-id="a091a-159">Then, with only the new yellow button and type layers visible, the image was saved as a copy to a bitmap file.</span></span>

<span data-ttu-id="a091a-160">Das Ergebnis ist, dass wenn mit dem Mauszeiger auf einen durch das Zuordnungsbild definierten Bereich gezeigt wird, das Hover-Bild angezeigt wird, um den Reader zu warnen, dass Sie die Windows-Media Player wiedergeben oder beenden können, wenn Sie auf diese Stelle klicken.</span><span class="sxs-lookup"><span data-stu-id="a091a-160">The result is that when the mouse hovers over an area defined by the mapping image, the hover image will be displayed, alerting the reader that if they click on that spot, they can play or stop Windows Media Player.</span></span>

## <a name="final-image"></a><span data-ttu-id="a091a-161">Endgültiges Image</span><span class="sxs-lookup"><span data-stu-id="a091a-161">Final Image</span></span>

<span data-ttu-id="a091a-162">Hier ist das endgültige Bild der Skin.</span><span class="sxs-lookup"><span data-stu-id="a091a-162">Here is the final image of the skin.</span></span>

![Endgültiges Image](images/absam01f.png)

<span data-ttu-id="a091a-164">Das Bild wird angezeigt, wenn Sie auf der rechten Seite auf die rosa Schaltfläche zeigen.</span><span class="sxs-lookup"><span data-stu-id="a091a-164">And this is the image you will see if you hover over the pink button on the right.</span></span>

![zeigen Sie auf die Rechte Schaltfläche](images/absam01r.png)

## <a name="xml-code-for-the-art-example"></a><span data-ttu-id="a091a-166">XML-Code für das Beispiel "Kunst"</span><span class="sxs-lookup"><span data-stu-id="a091a-166">XML Code for the Art Example</span></span>

<span data-ttu-id="a091a-167">Die Details zum Schreiben von XML-Code finden Sie im [Handbuch zur Erstellung von Skin](skin-creation-guide.md), aber um zu veranschaulichen, wie wenig Code zum Erstellen einer funktionierenden Skin benötigt wird, finden Sie hier den Code für die-Grafik in diesem Beispiel.</span><span class="sxs-lookup"><span data-stu-id="a091a-167">The details of how to write XML code are given in the [Skin Creation Guide](skin-creation-guide.md), but to show how little code is needed to create a working skin, here is the code for the artwork in this example.</span></span>

<span data-ttu-id="a091a-168">Für die Funktionen zum wiedergeben und Abbrechen werden vordefinierte Schaltflächen verwendet.</span><span class="sxs-lookup"><span data-stu-id="a091a-168">Predefined buttons are used for the play and stop functions.</span></span> <span data-ttu-id="a091a-169">Sie müssen eine Datei oder eine Wiedergabeliste aus dem Windows Media-Anker laden.</span><span class="sxs-lookup"><span data-stu-id="a091a-169">You must load a file or playlist from the Windows Media anchor.</span></span> <span data-ttu-id="a091a-170">Wenn Windows Media Player in den Skin-Modus wechselt, wird ein kleines Feld in der unteren rechten Ecke des Bildschirms angezeigt.</span><span class="sxs-lookup"><span data-stu-id="a091a-170">When Windows Media Player changes to skin mode, a small box appears in the lower-right corner of the screen.</span></span> <span data-ttu-id="a091a-171">Dieses Feld wird als "Anker" bezeichnet.</span><span class="sxs-lookup"><span data-stu-id="a091a-171">This box is called the "anchor".</span></span> <span data-ttu-id="a091a-172">Wenn Sie auf den Anker klicken, erhalten Sie die erforderliche Mindestfunktionalität, falls ein Skin keine Möglichkeit bietet, zum vollständigen Modus von Windows Media Player zurückzukehren.</span><span class="sxs-lookup"><span data-stu-id="a091a-172">Clicking the anchor gives you the minimum functionality needed, in case a skin does not provide a way to return to the full mode of Windows Media Player.</span></span> <span data-ttu-id="a091a-173">Der Benutzer kann mithilfe des Menüs **Ansicht** im vollständigen Modus oder durch Klicken auf den Anker im Skin-Modus zwischen den Modi wechseln.</span><span class="sxs-lookup"><span data-stu-id="a091a-173">The user can switch between modes by using the **View** menu if in full mode, or by clicking the anchor if in skin mode.</span></span>


```C++
<THEME>
    <VIEW
        clippingColor = "#CCCC00"
        backgroundImage = "background.bmp"
        titleBar = "false">
         
        <BUTTONGROUP
            mappingImage = "map.bmp"
            hoverImage = "hover.bmp">
                
        <PLAYELEMENT
            mappingColor = "#00FF00"/>

        <STOPELEMENT
            mappingColor = "#FF0000"/>
                
        </BUTTONGROUP>
    </VIEW>
</THEME>

```



## <a name="related-topics"></a><span data-ttu-id="a091a-174">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="a091a-174">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="a091a-175">**Kunstdateien**</span><span class="sxs-lookup"><span data-stu-id="a091a-175">**Art Files**</span></span>](art-files.md)
</dt> </dl>

 

 




