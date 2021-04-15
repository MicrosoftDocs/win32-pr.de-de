---
title: Angeben von Menüband-Bild Ressourcen
description: Als umfassendes Befehls Präsentationssystem ist das Windows-Menüband-Framework so konzipiert, dass Bild Ressourcen in der gesamten Multifunktionsleisten-Benutzeroberfläche (UI) unterstützt werden. Alle Bild Ressourcen werden im Menüband-Markup deklariert oder von einer Menüband-Host Anwendung abgefragt.
ms.assetid: 37b57992-8da8-4e6b-869d-72a136f6ad77
keywords:
- Windows-Menüband, Bild Ressourcen
- Menüband, Bild Ressourcen
- Windows-Menüband, Transparenz
- Multifunktionsleiste, Transparenz
- Windows-Menüband, Farbtiefe
- Menüband, Farbtiefe
- Windows-Menüband, Kontrast
- Menüband, Kontrast
- Bild Ressourcen in der Windows-Multifunktionsleiste
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 13e7666126e5b8f7fbe8b610678a8a1d71589373
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "104473924"
---
# <a name="specifying-ribbon-image-resources"></a><span data-ttu-id="89760-113">Angeben von Menüband-Bild Ressourcen</span><span class="sxs-lookup"><span data-stu-id="89760-113">Specifying Ribbon Image Resources</span></span>

<span data-ttu-id="89760-114">Als umfassendes Befehls Präsentationssystem ist das Windows-Menüband-Framework so konzipiert, dass Bild Ressourcen in der gesamten Multifunktionsleisten-Benutzeroberfläche (UI) unterstützt werden.</span><span class="sxs-lookup"><span data-stu-id="89760-114">As a rich command presentation system, the Windows Ribbon framework is designed to support image resources extensively throughout the Ribbon user interface (UI).</span></span> <span data-ttu-id="89760-115">Alle Bild Ressourcen werden im [Menüband-Markup](windowsribbon-schema.md) deklariert oder von einer Menüband-Host Anwendung abgefragt.</span><span class="sxs-lookup"><span data-stu-id="89760-115">All image resources are declared in [Ribbon markup](windowsribbon-schema.md) or queried from a Ribbon host application.</span></span>

<span data-ttu-id="89760-116">Für Windows 8 und höher unterstützt das Menüband-Framework die folgenden Grafikformate: 32-Bit-ARGB-Bitmap-Dateien (BMP) und Portable Network Graphics-Dateien (PNG) mit Transparenz.</span><span class="sxs-lookup"><span data-stu-id="89760-116">For Windows 8 and later, the Ribbon framework supports the following graphics formats: 32-bit ARGB bitmap (BMP) files and Portable Network Graphics (PNG) files with transparency.</span></span>

<span data-ttu-id="89760-117">Für Windows 7 und früher müssen Bild Ressourcen dem standardmäßigen BMP-Grafikformat entsprechen, das in Windows verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="89760-117">For Windows 7 and earlier, image resources must conform to the standard BMP graphics format used in Windows.</span></span>

> [!Note]  
> <span data-ttu-id="89760-118">Ein Kompilierungsfehler kann auftreten, wenn ein nicht unterstütztes Bildformat für das Framework bereitgestellt wird.</span><span class="sxs-lookup"><span data-stu-id="89760-118">A compilation error may occur if an unsupported image format is supplied to the framework.</span></span>

 

## <a name="image-sizes"></a><span data-ttu-id="89760-119">Bildgrößen</span><span class="sxs-lookup"><span data-stu-id="89760-119">Image Sizes</span></span>

<span data-ttu-id="89760-120">Um bei der Größenänderung eines Anwendungsfensters eine größere Flexibilität für die Layouts von Menüband-Steuerelementen zu bieten, akzeptiert und rendert das Menüband-Framework Bilder in einer von zwei Größen: groß oder klein.</span><span class="sxs-lookup"><span data-stu-id="89760-120">To provide greater flexibility for Ribbon control layouts when resizing an application window, the Ribbon framework accepts and renders images in one of two sizes: large or small.</span></span>

<span data-ttu-id="89760-121">Die folgenden Bilder veranschaulichen eine Multifunktionsleistenanwendung, die mehrere Menü Bandgrößen durch flexible Steuerelement Layouts und die Ersetzung großer Bilder mit kleinen, soweit verfügbaren Bildern unterstützt.</span><span class="sxs-lookup"><span data-stu-id="89760-121">The following images illustrate a Ribbon application that supports multiple Ribbon sizes through flexible control layouts and the replacement of large images with small images where available.</span></span>

<span data-ttu-id="89760-122">Der folgende Screenshot zeigt das Menüband mit großen Bildern für die Zoom Steuerelemente.</span><span class="sxs-lookup"><span data-stu-id="89760-122">The following screen shot shows the Ribbon with large images for the Zoom controls.</span></span>

![Screenshot, der ein Menüband anzeigt, das große Bilder für die Zoom Steuerelemente verwendet.](images/overviews/imageresources-largeimage.png)

<span data-ttu-id="89760-124">Der folgende Screenshot zeigt, wie die Größe des Menübands mit kleinen Bildern für die Zoom Steuerelemente geändert wird.</span><span class="sxs-lookup"><span data-stu-id="89760-124">The following screen shot shows the same Ribbon resized with small images for the Zoom controls</span></span>

![Screenshot, der ein Menüband anzeigt, das kleine Bilder für die Zoom Steuerelemente verwendet.](images/overviews/imageresources-smallimage.png)

<span data-ttu-id="89760-126">Der folgende Screenshot zeigt das Menüband im ausgeblendeten Zustand.</span><span class="sxs-lookup"><span data-stu-id="89760-126">The following screen shot shows the ribbon in hidden state.</span></span> <span data-ttu-id="89760-127">Das Menüband ist ausgeblendet, wenn alle möglichen Layouts der Steuerelemente erschöpft sind und das Menüband nicht mit einem verwendbaren Anwendungs Arbeitsbereich gerendert werden kann.</span><span class="sxs-lookup"><span data-stu-id="89760-127">The ribbon is hidden when all potential control layouts have been exhausted and the ribbon cannot be rendered with a usable application workspace.</span></span>

![Screenshot mit einem reduzierten Menüband](images/overviews/imageresources-noimage.png)

<span data-ttu-id="89760-129">Für ein beliebiges Bild ist die genaue Pixelgröße von der Bildschirmauflösung oder von dpi (dots per inch) des verwendeten Monitors abhängig.</span><span class="sxs-lookup"><span data-stu-id="89760-129">For any image, the exact pixel size is dependent on the display resolution, or dots per inch (dpi), of the monitor being used.</span></span> <span data-ttu-id="89760-130">Bei 96 dpi liegen große Bilder bei einer Größe von 32 x 32 Pixel und bei kleinen Bildern um 16 x 16 Pixel.</span><span class="sxs-lookup"><span data-stu-id="89760-130">At 96 dpi, large images are 32x32 pixels in size and small images are 16x16 pixels in size.</span></span> <span data-ttu-id="89760-131">Die Bildgrößen steigen auf lineare Weise relativ zu dpi, wie in der folgenden Tabelle dargestellt.</span><span class="sxs-lookup"><span data-stu-id="89760-131">The image sizes increase in a linear fashion relative to dpi as illustrated in the following table.</span></span>



| <span data-ttu-id="89760-132">DPI</span><span class="sxs-lookup"><span data-stu-id="89760-132">DPI</span></span>     | <span data-ttu-id="89760-133">Kleines Bild</span><span class="sxs-lookup"><span data-stu-id="89760-133">Small Image</span></span>  | <span data-ttu-id="89760-134">Großes Bild</span><span class="sxs-lookup"><span data-stu-id="89760-134">Large Image</span></span>  |
|---------|--------------|--------------|
| <span data-ttu-id="89760-135">96 dpi</span><span class="sxs-lookup"><span data-stu-id="89760-135">96 dpi</span></span>  | <span data-ttu-id="89760-136">16x16 Pixel</span><span class="sxs-lookup"><span data-stu-id="89760-136">16x16 pixels</span></span> | <span data-ttu-id="89760-137">32 x 32 Pixel</span><span class="sxs-lookup"><span data-stu-id="89760-137">32x32 pixels</span></span> |
| <span data-ttu-id="89760-138">120 dpi</span><span class="sxs-lookup"><span data-stu-id="89760-138">120 dpi</span></span> | <span data-ttu-id="89760-139">20 x 20 Pixel</span><span class="sxs-lookup"><span data-stu-id="89760-139">20x20 pixels</span></span> | <span data-ttu-id="89760-140">40 x 40 Pixel</span><span class="sxs-lookup"><span data-stu-id="89760-140">40x40 pixels</span></span> |
| <span data-ttu-id="89760-141">144 dpi</span><span class="sxs-lookup"><span data-stu-id="89760-141">144 dpi</span></span> | <span data-ttu-id="89760-142">24 x 24 Pixel</span><span class="sxs-lookup"><span data-stu-id="89760-142">24x24 pixels</span></span> | <span data-ttu-id="89760-143">48 x 48 Pixel</span><span class="sxs-lookup"><span data-stu-id="89760-143">48x48 pixels</span></span> |
| <span data-ttu-id="89760-144">192 dpi</span><span class="sxs-lookup"><span data-stu-id="89760-144">192 dpi</span></span> | <span data-ttu-id="89760-145">32 x 32 Pixel</span><span class="sxs-lookup"><span data-stu-id="89760-145">32x32 pixels</span></span> | <span data-ttu-id="89760-146">64x64 Pixel</span><span class="sxs-lookup"><span data-stu-id="89760-146">64x64 pixels</span></span> |



 

<span data-ttu-id="89760-147">Das Menüband-Framework skaliert Bild Ressourcen nach Bedarf.</span><span class="sxs-lookup"><span data-stu-id="89760-147">The Ribbon framework scales image resources as required.</span></span> <span data-ttu-id="89760-148">Da die Größe der Größe jedoch unerwünschte Artefakte und Bildverschlechterung verursachen kann, wird dringend empfohlen, dass die Anwendung einen kleinen Satz von Bild Ressourcen bereitstellt, die verschiedene häufig verwendete dpi-Einstellungen umfassen.</span><span class="sxs-lookup"><span data-stu-id="89760-148">However, because resizing may yield undesirable artifacts and image degradation, it is highly recommended that the application provide a small set of image resources that span various commonly used dpi settings.</span></span> <span data-ttu-id="89760-149">Wenn keine genaue Entsprechung gefunden wird, wird das nächste Bild zentral hoch-oder herunterskaliert.</span><span class="sxs-lookup"><span data-stu-id="89760-149">If an exact match is not found, the nearest image will be scaled up or down.</span></span>

<span data-ttu-id="89760-150">Um dies zu vereinfachen, können Bild Ressourcen in Menüband-Markup mithilfe eines Satzes von [**Bild**](windowsribbon-element-image.md) Elementen für jedes [**Command**](windowsribbon-element-command.md) -Element deklariert werden.</span><span class="sxs-lookup"><span data-stu-id="89760-150">To facilitate this, image resources can be declared in Ribbon markup by using a set of [**Image**](windowsribbon-element-image.md) elements for each [**Command**](windowsribbon-element-command.md) element.</span></span> <span data-ttu-id="89760-151">Zur Laufzeit wählt das Framework das Bild aus, das auf der Grundlage des *mindpi* -Attributs der einzelnen **Bild** Elemente angezeigt werden soll.</span><span class="sxs-lookup"><span data-stu-id="89760-151">At run time, the framework selects the image to display based on the *MinDPI* attribute of each **Image** element.</span></span>

> [!IMPORTANT]
>
> <span data-ttu-id="89760-152">Wenn eine Auflistung von Bild Ressourcen, die für die Unterstützung bestimmter Bildschirm DPI-Einstellungen entworfen wurden, über einen Satz von [**Bild**](windowsribbon-element-image.md) Elementen an das Menüband-Framework übergeben wird, verwendet das Framework das **Bild** mit einem *mindpi* -Attribut Wert, der mit der aktuellen Bildschirm-dpi-Einstellung übereinstimmt.</span><span class="sxs-lookup"><span data-stu-id="89760-152">When a collection of image resources that are designed to support specific screen dpi settings is supplied to the Ribbon framework through a set of [**Image**](windowsribbon-element-image.md) elements, the framework uses the **Image** with a *MinDPI* attribute value that matches the current screen dpi setting.</span></span>
>
> <span data-ttu-id="89760-153">Wenn kein [**Bild**](windowsribbon-element-image.md) Element mit einem *mindpi* -Wert deklariert wird, der mit der aktuellen Bildschirm dpi-Einstellung übereinstimmt, wählt das Framework das **Bild** aus, das den nächstgelegenen *mindpi* -Wert aufweist, der kleiner ist als die aktuelle Bildschirm dpi-Einstellung, und skaliert die Bildressource</span><span class="sxs-lookup"><span data-stu-id="89760-153">If no [**Image**](windowsribbon-element-image.md) element is declared with a *MinDPI* value that matches the current screen dpi setting, the framework picks the **Image** that has the nearest *MinDPI* value less than the current screen dpi setting and scales the image resource up.</span></span> <span data-ttu-id="89760-154">Wenn kein **Bild** Element mit einem *mindpi* -Attribut Wert, der kleiner als die aktuelle Bildschirm dpi-Einstellung ist, deklariert ist, wählt das Framework den nächsten *mindpi* -Wert aus, der größer als die aktuelle Bildschirm dpi-Einstellung ist, und skaliert die Bildressource nach unten.</span><span class="sxs-lookup"><span data-stu-id="89760-154">Otherwise, if no **Image** element is declared with a *MinDPI* attribute value less than the current screen dpi setting, the framework picks the nearest *MinDPI* value greater than the current screen dpi setting and scales the image resource down.</span></span>

 

<span data-ttu-id="89760-155">Im folgenden Beispiel wird veranschaulicht, wie Sie einen Satz von Bildern deklarieren, um verschiedene Menü Bandgrößen und Systemeinstellungen zu unterstützen.</span><span class="sxs-lookup"><span data-stu-id="89760-155">The following example illustrates how to declare a set of images to accommodate various Ribbon sizes and system settings.</span></span>


```C++
<Command.LargeImages>
  <Image Source="res/CutLargeImage32.bmp" Id="116" Symbol="ID_CUT_LARGEIMAGE1" MinDPI="96" />
  <Image Source="res/CutLargeImage40.bmp" Id="117" Symbol="ID_CUT_LARGEIMAGE2" MinDPI="120" />
  <Image Source="res/CutLargeImage48.bmp" Id="118" Symbol="ID_CUT_LARGEIMAGE3" MinDPI="144" />
  <Image Source="res/CutLargeImage64.bmp" Id="119" Symbol="ID_CUT_LARGEIMAGE4" MinDPI="192" />
</Command.LargeImages>
<Command.SmallImages>
  <Image Source="res/CutSmallImage16.bmp" Id="122" Symbol="ID_CUT_SMALLIMAGE1" MinDPI="96" />
  <Image Source="res/CutSmallImage20.bmp" Id="123" Symbol="ID_CUT_SMALLIMAGE2" MinDPI="120" />
  <Image Source="res/CutSmallImage24.bmp" Id="124" Symbol="ID_CUT_SMALLIMAGE3" MinDPI="144" />
  <Image Source="res/CutSmallImage32.bmp" Id="125" Symbol="ID_CUT_SMALLIMAGE4" MinDPI="192" />
</Command.SmallImages>
<Command.LargeHighContrastImages>
  <Image Source="res/CutLargeImage32HC.bmp" Id="130" Symbol="ID_CUT_LARGEIMAGE1HC" MinDPI="96" />
  <Image Source="res/CutLargeImage40HC.bmp" Id="131" Symbol="ID_CUT_LARGEIMAGE2HC" MinDPI="120" />
  <Image Source="res/CutLargeImage48HC.bmp" Id="132" Symbol="ID_CUT_LARGEIMAGE3HC" MinDPI="144" />
  <Image Source="res/CutLargeImage64HC.bmp" Id="133" Symbol="ID_CUT_LARGEIMAGE4HC" MinDPI="192" />
</Command.LargeHighContrastImages>
<Command.SmallHighContrastImages>
  <Image Source="res/CutSmallImage16HC.bmp" Id="135" Symbol="ID_CUT_SMALLIMAGE1HC" MinDPI="96" />
  <Image Source="res/CutSmallImage20HC.bmp" Id="136" Symbol="ID_CUT_SMALLIMAGE2HC" MinDPI="120" />
  <Image Source="res/CutSmallImage24HC.bmp" Id="137" Symbol="ID_CUT_SMALLIMAGE3HC" MinDPI="144" />
  <Image Source="res/CutSmallImage32HC.bmp" Id="138" Symbol="ID_CUT_SMALLIMAGE4HC" MinDPI="192" />
</Command.SmallHighContrastImages>
```



<span data-ttu-id="89760-156">Wenn Images, die im Markup deklariert sind, zur Laufzeit aus irgendeinem Grund ungültig gemacht werden, wird die Host Anwendung nach neuen Bildern abgefragt.</span><span class="sxs-lookup"><span data-stu-id="89760-156">If images declared in markup are invalidated at run time for any reason, the host application is queried for new images.</span></span> <span data-ttu-id="89760-157">Wenn diese Images Programm gesteuert generiert und geladen werden, sollte die Anwendung versuchen, Bilder zurückzugeben, deren Größe den von der [SM \_ cxicon-System Metrik](/windows/win32/api/winuser/nf-winuser-getsystemmetrics)festgelegten Standard-System Symbolgrößen entspricht.</span><span class="sxs-lookup"><span data-stu-id="89760-157">When these images are generated and loaded programmatically, the application should attempt to return images that are sized according to the default system icon sizes determined by the [SM\_CXICON system metric](/windows/win32/api/winuser/nf-winuser-getsystemmetrics).</span></span>

> [!Note]  
> <span data-ttu-id="89760-158">Große Bilder haben eine Größe von SM \_ cxicon von SM \_ cxicon, und kleine Images haben eine Größe von SM \_ cxicon/2 von SM \_ cxicon/2.</span><span class="sxs-lookup"><span data-stu-id="89760-158">Large images have a size of SM\_CXICON by SM\_CXICON and small images have a size of SM\_CXICON/2 by SM\_CXICON/2.</span></span>

 

## <a name="color-depth-transparency-and-contrast"></a><span data-ttu-id="89760-159">Farbtiefe, Transparenz und Kontrast</span><span class="sxs-lookup"><span data-stu-id="89760-159">Color Depth, Transparency, and Contrast</span></span>

<span data-ttu-id="89760-160">Es wird erwartet, dass reguläre Images im BPP-ARGB-Pixel Format (32 Bits pro Pixel) vorliegen und auf die standardmäßige System Symbolgröße skaliert werden.</span><span class="sxs-lookup"><span data-stu-id="89760-160">Regular images are expected to be in 32 bits per pixel (BPP) ARGB pixel format and scaled to the default system icon size.</span></span> <span data-ttu-id="89760-161">Dieses Format unterstützt Transparenz und Antialiasing (bei Verwendung von 8 Bits pro Kanal).</span><span class="sxs-lookup"><span data-stu-id="89760-161">This format supports both transparency and antialiasing (using 8 bits per channel).</span></span>

> [!WARNING]
> <span data-ttu-id="89760-162">Viele Tools zur Bildbearbeitung behalten beim Laden oder Speichern von 32 bpp-Images nicht den 8-Bit-Alphakanal mit der höchsten Ordnung bei.</span><span class="sxs-lookup"><span data-stu-id="89760-162">Many image editing tools do not preserve the highest order 8-bit alpha channel when loading or saving 32 BPP images.</span></span>

 

<span data-ttu-id="89760-163">Damit ein Bild im Modus mit hohem Kontrast ordnungsgemäß angezeigt wird, muss es in einem 4-bpp-Format mit Palettengröße angezeigt werden.</span><span class="sxs-lookup"><span data-stu-id="89760-163">For an image to display correctly in high-contrast mode, it must be in a 4 BPP palletized pixel format.</span></span> <span data-ttu-id="89760-164">Wenn das Bild gerendert wird, ordnet das Menüband-Framework bestimmte Farben auf Grundlage des Kontrast Bilds des Bilds neu zu.</span><span class="sxs-lookup"><span data-stu-id="89760-164">When the image is rendered, the Ribbon framework remaps specific colors based on the high-contrast context of the image.</span></span>

<span data-ttu-id="89760-165">In der folgenden Tabelle wird das Farb Rendering Verhalten mit hohem Kontrast des Frameworks aufgelistet.</span><span class="sxs-lookup"><span data-stu-id="89760-165">The following table lists the high-contrast color rendering behavior of the framework.</span></span>



<span data-ttu-id="89760-166">Pixelfarbe</span><span class="sxs-lookup"><span data-stu-id="89760-166">Pixel color</span></span>

<span data-ttu-id="89760-167">RGB-Wert</span><span class="sxs-lookup"><span data-stu-id="89760-167">RGB value</span></span>

<span data-ttu-id="89760-168">Verhalten</span><span class="sxs-lookup"><span data-stu-id="89760-168">Behavior</span></span>

<span data-ttu-id="89760-169">Weißer Hintergrund</span><span class="sxs-lookup"><span data-stu-id="89760-169">White background</span></span>

<span data-ttu-id="89760-170">Dunkler Hintergrund</span><span class="sxs-lookup"><span data-stu-id="89760-170">Dark Background</span></span>

<span data-ttu-id="89760-171">Magenta</span><span class="sxs-lookup"><span data-stu-id="89760-171">MAGENTA</span></span>

<span data-ttu-id="89760-172">800080</span><span class="sxs-lookup"><span data-stu-id="89760-172">800080</span></span>

<span data-ttu-id="89760-173">Transparent</span><span class="sxs-lookup"><span data-stu-id="89760-173">Transparent</span></span>

<span data-ttu-id="89760-174">Transparent</span><span class="sxs-lookup"><span data-stu-id="89760-174">Transparent</span></span>

<span data-ttu-id="89760-175">Box</span><span class="sxs-lookup"><span data-stu-id="89760-175">BLACK</span></span>

<span data-ttu-id="89760-176">000000</span><span class="sxs-lookup"><span data-stu-id="89760-176">000000</span></span>

<span data-ttu-id="89760-177">\_WindowText-Farbe</span><span class="sxs-lookup"><span data-stu-id="89760-177">COLOR\_WINDOWTEXT</span></span>

<span data-ttu-id="89760-178">Weisse</span><span class="sxs-lookup"><span data-stu-id="89760-178">WHITE</span></span>

<span data-ttu-id="89760-179">Weisse</span><span class="sxs-lookup"><span data-stu-id="89760-179">WHITE</span></span>

<span data-ttu-id="89760-180">FFFFFF</span><span class="sxs-lookup"><span data-stu-id="89760-180">FFFFFF</span></span>

<span data-ttu-id="89760-181">Farb \_ Fenster</span><span class="sxs-lookup"><span data-stu-id="89760-181">COLOR\_WINDOW</span></span>

<span data-ttu-id="89760-182">Box</span><span class="sxs-lookup"><span data-stu-id="89760-182">BLACK</span></span>

<span data-ttu-id="89760-183">dunkelgrau</span><span class="sxs-lookup"><span data-stu-id="89760-183">DARK GRAY</span></span>

<span data-ttu-id="89760-184">808080</span><span class="sxs-lookup"><span data-stu-id="89760-184">808080</span></span>

<span data-ttu-id="89760-185">Farbe \_ 3dshadow</span><span class="sxs-lookup"><span data-stu-id="89760-185">COLOR\_3DSHADOW</span></span>

<span data-ttu-id="89760-186">Farbe \_ 3dshadow</span><span class="sxs-lookup"><span data-stu-id="89760-186">COLOR\_3DSHADOW</span></span>

<span data-ttu-id="89760-187">Grau</span><span class="sxs-lookup"><span data-stu-id="89760-187">GRAY</span></span>

<span data-ttu-id="89760-188">C0C0C0</span><span class="sxs-lookup"><span data-stu-id="89760-188">C0C0C0</span></span>

<span data-ttu-id="89760-189">Farbe \_ 3dface</span><span class="sxs-lookup"><span data-stu-id="89760-189">COLOR\_3DFACE</span></span>

<span data-ttu-id="89760-190">Farbe \_ 3dface</span><span class="sxs-lookup"><span data-stu-id="89760-190">COLOR\_3DFACE</span></span>

<span data-ttu-id="89760-191">hellgrau</span><span class="sxs-lookup"><span data-stu-id="89760-191">LIGHT GRAY</span></span>

<span data-ttu-id="89760-192">Dfdfdf</span><span class="sxs-lookup"><span data-stu-id="89760-192">DFDFDF</span></span>

<span data-ttu-id="89760-193">Farbe \_ 3dlight</span><span class="sxs-lookup"><span data-stu-id="89760-193">COLOR\_3DLIGHT</span></span>

<span data-ttu-id="89760-194">Farbe \_ 3dlight</span><span class="sxs-lookup"><span data-stu-id="89760-194">COLOR\_3DLIGHT</span></span>

<span data-ttu-id="89760-195">dunkelblau</span><span class="sxs-lookup"><span data-stu-id="89760-195">DARK BLUE</span></span>

<span data-ttu-id="89760-196">000080</span><span class="sxs-lookup"><span data-stu-id="89760-196">000080</span></span>

<span data-ttu-id="89760-197">–</span><span class="sxs-lookup"><span data-stu-id="89760-197">n/a</span></span>

<span data-ttu-id="89760-198">Weisse</span><span class="sxs-lookup"><span data-stu-id="89760-198">WHITE</span></span>



 

<span data-ttu-id="89760-199">Weitere Informationen zu den vom Menüband-Framework unterstützten Bildformaten finden Sie in den folgenden Bereichen:</span><span class="sxs-lookup"><span data-stu-id="89760-199">For more information on the image formats supported by the Ribbon framework, see the following:</span></span>

-   <span data-ttu-id="89760-200">[BITMAPINFOHEADER-Struktur](/previous-versions//dd183376(v=vs.85)) : Beschreibt das 32 bpp-ARGB-Pixel Format.</span><span class="sxs-lookup"><span data-stu-id="89760-200">[BITMAPINFOHEADER structure](/previous-versions//dd183376(v=vs.85)) - describes the 32 BPP ARGB pixel format.</span></span>
-   <span data-ttu-id="89760-201">[Funktion "deedibsection](/windows/win32/api/wingdi/nf-wingdi-createdibsection) ": Beschreibt das Erstellen eines 32 bpp-ARGB-Pixel Formatierungs Bilds.</span><span class="sxs-lookup"><span data-stu-id="89760-201">[CreateDIBSection function](/windows/win32/api/wingdi/nf-wingdi-createdibsection) - describes how to create a 32 BPP ARGB pixel format image.</span></span>
-   <span data-ttu-id="89760-202">[LoadImage-Funktion](/windows/win32/api/winuser/nf-winuser-loadimagea) : Beschreibt das Laden eines 32 bpp-ARGB-Pixel Formatierungs Bilds.</span><span class="sxs-lookup"><span data-stu-id="89760-202">[LoadImage function](/windows/win32/api/winuser/nf-winuser-loadimagea) - describes how to load a 32 BPP ARGB pixel format image.</span></span>

## <a name="accessibility"></a><span data-ttu-id="89760-203">Eingabehilfen</span><span class="sxs-lookup"><span data-stu-id="89760-203">Accessibility</span></span>

<span data-ttu-id="89760-204">Die Verwendung von Bild Ressourcen, um Informationen bereitzustellen, Steuerungsfunktionen zu vermitteln und den Anwendungs Zustand verfügbar zu machen, erhöht den Bedarf an Barrierefreiheits Anforderungen beim Entwerfen und entwickeln von Anwendungen.</span><span class="sxs-lookup"><span data-stu-id="89760-204">Relying on image resources to provide information, convey control functionality, and expose application state, increases the need for accessibility requirements during application design and development.</span></span>

<span data-ttu-id="89760-205">Für grundlegende Unterstützung für hohe Kontraste ermöglicht das Menüband, dass ein separater Satz von Bilddateien angezeigt wird, wenn ein Design mit hohem Kontrast aktiv ist.</span><span class="sxs-lookup"><span data-stu-id="89760-205">For basic high contrast support, the Ribbon allows for a separate set of image files to be displayed when a high-contrast theme is active.</span></span> <span data-ttu-id="89760-206">Diese Bilder können 32 bpp oder 4 bpp sein, wobei Farben einer speziellen Palette zugeordnet werden, wobei dunkle und helle Farben in Abhängigkeit von der Vordergrund-und Hintergrundfarbe des aktiven Designs mit hohem Kontrast invertiert werden.</span><span class="sxs-lookup"><span data-stu-id="89760-206">These images can be 32 BPP or 4 BPP, with colors mapped to a special palette where dark and light colors are inverted depending on the foreground and background colors of the active high-contrast theme.</span></span>

<span data-ttu-id="89760-207">Im folgenden Beispiel wird veranschaulicht, wie Bild Ressourcen mit hohem Kontrast im Menüband-Markup deklariert werden:</span><span class="sxs-lookup"><span data-stu-id="89760-207">The following example demonstrates how high-contrast image resources are declared in Ribbon markup:</span></span>


```C++
<Command Name="cmdNew" Id="0xE100" Symbol="ID_CMD_NEW" LabelTitle="New document" Keytip="N" >
      <Command.TooltipTitle>New (Ctrl+N)</Command.TooltipTitle>
      <Command.TooltipDescription>Create a new document.</Command.TooltipDescription>
      <Command.LargeImages>
        <Image Source="cmdNew-32px.bmp" MinDPI="96" />
        <Image Source="cmdNew-40px.bmp" MinDPI="120" />
        <Image Source="cmdNew-48px.bmp" MinDPI="144" />
        <Image Source="cmdNew-64px.bmp" MinDPI="192" />
      </Command.LargeImages>
      <Command.LargeHighContrastImages>
        <Image Source="cmdNew-32px-HC.bmp" MinDPI="96" />
        <Image Source="cmdNew-40px-HC.bmp" MinDPI="120" />
        <Image Source="cmdNew-48px-HC.bmp" MinDPI="144" />
        <Image Source="cmdNew-64px-HC.bmp" MinDPI="192" />
      </Command.LargeHighContrastImages>
      <Command.SmallImages>
        <Image Source="cmdNew-16px.bmp" MinDPI="96" />
        <Image Source="cmdNew-20px.bmp" MinDPI="120" />
        <Image Source="cmdNew-24px.bmp" MinDPI="144" />
        <Image Source="cmdNew-32px.bmp" MinDPI="192" />
      </Command.SmallImages>
      <Command.SmallHighContrastImages>
        <Image Source="cmdNew-16px-HC.bmp" MinDPI="96" />
        <Image Source="cmdNew-20px-HC.bmp" MinDPI="120" />
        <Image Source="cmdNew-24px-HC.bmp" MinDPI="144" />
        <Image Source="cmdNew-32px-HC.bmp" MinDPI="192" />
      </Command.SmallHighContrastImages>
    </Command>
```



## <a name="related-topics"></a><span data-ttu-id="89760-208">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="89760-208">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="89760-209">**Command. smallimages**</span><span class="sxs-lookup"><span data-stu-id="89760-209">**Command.SmallImages**</span></span>](windowsribbon-element-command-smallimages.md)
</dt> <dt>

[<span data-ttu-id="89760-210">UI \_ pkey \_ smallImage</span><span class="sxs-lookup"><span data-stu-id="89760-210">UI\_PKEY\_SmallImage</span></span>](windowsribbon-reference-properties-uipkey-smallimage.md)
</dt> <dt>

[<span data-ttu-id="89760-211">**Command. largeimages**</span><span class="sxs-lookup"><span data-stu-id="89760-211">**Command.LargeImages**</span></span>](windowsribbon-element-command-largeimages.md)
</dt> <dt>

[<span data-ttu-id="89760-212">UI \_ pkey \_ largeimage</span><span class="sxs-lookup"><span data-stu-id="89760-212">UI\_PKEY\_LargeImage</span></span>](windowsribbon-reference-properties-uipkey-largeimage.md)
</dt> <dt>

[<span data-ttu-id="89760-213">**Command. smallhighkontra stimages**</span><span class="sxs-lookup"><span data-stu-id="89760-213">**Command.SmallHighContrastImages**</span></span>](windowsribbon-element-command-smallhighcontrastimages.md)
</dt> <dt>

[<span data-ttu-id="89760-214">UI \_ pkey \_ smallhighkontra stimage</span><span class="sxs-lookup"><span data-stu-id="89760-214">UI\_PKEY\_SmallHighContrastImage</span></span>](windowsribbon-reference-properties-uipkey-smallhighcontrastimage.md)
</dt> <dt>

[<span data-ttu-id="89760-215">**Command. largehighkontra stimages**</span><span class="sxs-lookup"><span data-stu-id="89760-215">**Command.LargeHighContrastImages**</span></span>](windowsribbon-element-command-largehighcontrastimages.md)
</dt> <dt>

[<span data-ttu-id="89760-216">UI \_ pkey \_ largehighkontra stimage</span><span class="sxs-lookup"><span data-stu-id="89760-216">UI\_PKEY\_LargeHighContrastImage</span></span>](windowsribbon-reference-properties-uipkey-largehighcontrastimage.md)
</dt> </dl>

 

 