---
title: DPI-und Device-Independent Pixel
ms.assetid: d282de02-62f4-4a12-a77c-f602f6db0216
description: 'Weitere Informationen: dpi und Device-Independent Pixel'
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8e6f04e1a056611fcdfe8b59ff65b38ecec99eaf
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "103868660"
---
# <a name="dpi-and-device-independent-pixels"></a><span data-ttu-id="876b4-103">DPI-und Device-Independent Pixel</span><span class="sxs-lookup"><span data-stu-id="876b4-103">DPI and Device-Independent Pixels</span></span>

<span data-ttu-id="876b4-104">Um effektiv mit Windows-Grafiken zu programmieren, müssen Sie zwei verwandte Konzepte verstehen:</span><span class="sxs-lookup"><span data-stu-id="876b4-104">To program effectively with Windows graphics, you must understand two related concepts:</span></span>

-   <span data-ttu-id="876b4-105">Punkte pro Zoll (dpi)</span><span class="sxs-lookup"><span data-stu-id="876b4-105">Dots per inch (DPI)</span></span>
-   <span data-ttu-id="876b4-106">Geräte unabhängiges Pixel (Dips).</span><span class="sxs-lookup"><span data-stu-id="876b4-106">Device-independent pixel (DIPs).</span></span>

<span data-ttu-id="876b4-107">Beginnen wir mit dpi.</span><span class="sxs-lookup"><span data-stu-id="876b4-107">Let's start with DPI.</span></span> <span data-ttu-id="876b4-108">Dies erfordert eine kurze Umleitung in typografieweise.</span><span class="sxs-lookup"><span data-stu-id="876b4-108">This will require a short detour into typography.</span></span> <span data-ttu-id="876b4-109">In der Typografie wird die Größe des Typs in Einheiten gemessen, die als *Punkte* bezeichnet werden.</span><span class="sxs-lookup"><span data-stu-id="876b4-109">In typography, the size of type is measured in units called *points*.</span></span> <span data-ttu-id="876b4-110">Ein Punkt ist gleich 1/72 Zoll.</span><span class="sxs-lookup"><span data-stu-id="876b4-110">One point equals 1/72 of an inch.</span></span>

<dl> <span data-ttu-id="876b4-111">1 pt = 1/72 Zoll</span><span class="sxs-lookup"><span data-stu-id="876b4-111">1 pt = 1/72 inch</span></span>  
</dl>

> [!Note]  
> <span data-ttu-id="876b4-112">Dies ist die Desktop Veröffentlichungs Definition des Punkts.</span><span class="sxs-lookup"><span data-stu-id="876b4-112">This is the desktop publishing definition of point.</span></span> <span data-ttu-id="876b4-113">In der Vergangenheit hat sich das genaue Measure eines Punkts geändert.</span><span class="sxs-lookup"><span data-stu-id="876b4-113">Historically, the exact measure of a point has varied.</span></span>

 

<span data-ttu-id="876b4-114">Beispielsweise ist eine 12-Punkt-Schriftart so konzipiert, dass Sie in eine 1/6 "(12/72) Textzeile passt.</span><span class="sxs-lookup"><span data-stu-id="876b4-114">For example, a 12-point font is designed to fit within a 1/6" (12/72) line of text.</span></span> <span data-ttu-id="876b4-115">Dies bedeutet natürlich nicht, dass jedes Zeichen in der Schriftart genau 1/6 "groß ist.</span><span class="sxs-lookup"><span data-stu-id="876b4-115">Obviously, this does not mean that every character in the font is exactly 1/6" tall.</span></span> <span data-ttu-id="876b4-116">Tatsächlich können einige Zeichen größer als 1/6 "sein.</span><span class="sxs-lookup"><span data-stu-id="876b4-116">In fact, some characters might be taller than 1/6".</span></span> <span data-ttu-id="876b4-117">In vielen Schriftarten ist das Zeichen "" z. b. größer als die nominale Höhe der Schriftart.</span><span class="sxs-lookup"><span data-stu-id="876b4-117">For example, in many fonts the character Å is taller than the nominal height of the font.</span></span> <span data-ttu-id="876b4-118">Um ordnungsgemäß angezeigt zu werden, benötigt die Schriftart zusätzlichen Leerraum zwischen dem Text.</span><span class="sxs-lookup"><span data-stu-id="876b4-118">To display correctly, the font needs some additional space between the text.</span></span> <span data-ttu-id="876b4-119">Dieser Bereich wird als *führende* bezeichnet.</span><span class="sxs-lookup"><span data-stu-id="876b4-119">This space is called the *leading*.</span></span>

<span data-ttu-id="876b4-120">Die folgende Abbildung zeigt eine 72-Punkt-Schriftart.</span><span class="sxs-lookup"><span data-stu-id="876b4-120">The following illustration shows a 72-point font.</span></span> <span data-ttu-id="876b4-121">Die einschließenden Linien zeigen ein "großes Begrenzungsfeld um den Text an.</span><span class="sxs-lookup"><span data-stu-id="876b4-121">The solid lines show a 1" tall bounding box around the text.</span></span> <span data-ttu-id="876b4-122">Die gestrichelte Linie wird als *Baseline* bezeichnet.</span><span class="sxs-lookup"><span data-stu-id="876b4-122">The dashed line is called the *baseline*.</span></span> <span data-ttu-id="876b4-123">Die meisten Zeichen in einer Schriftart verbleibenden die Baseline.</span><span class="sxs-lookup"><span data-stu-id="876b4-123">Most of the characters in a font rest on the baseline.</span></span> <span data-ttu-id="876b4-124">Die Höhe der Schriftart umfasst den Teil oberhalb der Baseline (der *Aufstieg*) und den Teil unterhalb der Baseline (der *Abstieg*).</span><span class="sxs-lookup"><span data-stu-id="876b4-124">The height of the font includes the portion above the baseline (the *ascent*) and the portion below the baseline (the *descent*).</span></span> <span data-ttu-id="876b4-125">In der hier gezeigten Schriftart ist der Anstieg 56 Punkte, und der Abstieg ist 16 Punkte.</span><span class="sxs-lookup"><span data-stu-id="876b4-125">In the font shown here, the ascent is 56 points and the descent is 16 points.</span></span>

![eine Abbildung, die eine 72-Punkt-Schriftart anzeigt.](images/graphics11.png)

<span data-ttu-id="876b4-127">Bei einer Computer Anzeige ist das Messen der Textgröße jedoch problematisch, da Pixel nicht die gleiche Größe aufweisen.</span><span class="sxs-lookup"><span data-stu-id="876b4-127">When it comes to a computer display, however, measuring text size is problematic, because pixels are not all the same size.</span></span> <span data-ttu-id="876b4-128">Die Größe eines Pixels hängt von zwei Faktoren ab: der Anzeige Auflösung und der physischen Größe des Monitors.</span><span class="sxs-lookup"><span data-stu-id="876b4-128">The size of a pixel depends on two factors: the display resolution, and the physical size of the monitor.</span></span> <span data-ttu-id="876b4-129">Aus diesem Grund sind physische Zoll-Einheiten kein nützliches Measure, da es keine fixierte Beziehung zwischen physischen Zoll und Pixel gibt.</span><span class="sxs-lookup"><span data-stu-id="876b4-129">Therefore, physical inches are not a useful measure, because there is no fixed relation between physical inches and pixels.</span></span> <span data-ttu-id="876b4-130">Stattdessen werden Schriftarten in *logischen* Einheiten gemessen.</span><span class="sxs-lookup"><span data-stu-id="876b4-130">Instead, fonts are measured in *logical* units.</span></span> <span data-ttu-id="876b4-131">Eine 72-Punkt Schriftart ist als ein logischer Zoll definiert.</span><span class="sxs-lookup"><span data-stu-id="876b4-131">A 72-point font is defined to be one logical inch tall.</span></span> <span data-ttu-id="876b4-132">Logische Zoll werden dann in Pixel konvertiert.</span><span class="sxs-lookup"><span data-stu-id="876b4-132">Logical inches are then converted to pixels.</span></span> <span data-ttu-id="876b4-133">Seit vielen Jahren hat Windows die folgende Konvertierung verwendet: ein logischer Zoll ist 96 Pixel.</span><span class="sxs-lookup"><span data-stu-id="876b4-133">For many years, Windows used the following conversion: One logical inch equals 96 pixels.</span></span> <span data-ttu-id="876b4-134">Bei Verwendung dieses Skalierungsfaktors wird eine 72-Punkt-Schriftart als 96 Pixel hoch gerendert.</span><span class="sxs-lookup"><span data-stu-id="876b4-134">Using this scaling factor, a 72-point font is rendered as 96 pixels tall.</span></span> <span data-ttu-id="876b4-135">Eine 12-Punkt-Schriftart ist 16 Pixel hoch.</span><span class="sxs-lookup"><span data-stu-id="876b4-135">A 12-point font is 16 pixels tall.</span></span>

<dl> <span data-ttu-id="876b4-136">12 Punkte = 12/72 logischer Zoll = 1/6 logischer Zoll = 96/6 Pixel = 16 Pixel</span><span class="sxs-lookup"><span data-stu-id="876b4-136">12 points = 12/72 logical inch = 1/6 logical inch = 96/6 pixels = 16 pixels</span></span>  
</dl>

<span data-ttu-id="876b4-137">Dieser Skalierungsfaktor wird als 96 Punkte pro Zoll (dpi) beschrieben.</span><span class="sxs-lookup"><span data-stu-id="876b4-137">This scaling factor is described as 96 dots per inch (DPI).</span></span> <span data-ttu-id="876b4-138">Der Begriff "Punkte" leitet sich vom Druck ab, bei dem physische Handzettel auf Papier abgelegt werden.</span><span class="sxs-lookup"><span data-stu-id="876b4-138">The term dots derives from printing, where physical dots of ink are put onto paper.</span></span> <span data-ttu-id="876b4-139">Bei Computer anzeigen wäre es genauer gesagt, dass Sie 96 Pixel pro logischem Zoll, aber der Begriff dpi nicht mehr angezeigt wird.</span><span class="sxs-lookup"><span data-stu-id="876b4-139">For computer displays, it would be more accurate to say 96 pixels per logical inch, but the term DPI has stuck.</span></span>

<span data-ttu-id="876b4-140">Da die tatsächlichen Pixelgrößen variieren, kann Text, der auf einem Monitor lesbar ist, auf einem anderen Monitor zu klein sein.</span><span class="sxs-lookup"><span data-stu-id="876b4-140">Because actual pixel sizes vary, text that is readable on one monitor might be too small on another monitor.</span></span> <span data-ttu-id="876b4-141">Außerdem haben die Benutzer unterschiedliche Vorlieben – einige Personen bevorzugen größere Texte.</span><span class="sxs-lookup"><span data-stu-id="876b4-141">Also, people have different preferences—some people prefer larger text.</span></span> <span data-ttu-id="876b4-142">Aus diesem Grund ermöglicht Windows dem Benutzer das Ändern der dpi-Einstellung.</span><span class="sxs-lookup"><span data-stu-id="876b4-142">For this reason, Windows enables the user to change the DPI setting.</span></span> <span data-ttu-id="876b4-143">Wenn der Benutzer z. b. die Anzeige auf 144 dpi festlegt, ist eine 72-Punkt-Schriftart 144 Pixel hoch.</span><span class="sxs-lookup"><span data-stu-id="876b4-143">For example, if the user sets the display to 144 DPI, a 72-point font is 144 pixels tall.</span></span> <span data-ttu-id="876b4-144">Die standardmäßigen dpi-Einstellungen lauten 100% (96 dpi), 125% (120 dpi) und 150% (144 dpi).</span><span class="sxs-lookup"><span data-stu-id="876b4-144">The standard DPI settings are 100% (96 DPI), 125% (120 DPI), and 150% (144 DPI).</span></span> <span data-ttu-id="876b4-145">Der Benutzer kann auch eine benutzerdefinierte Einstellung anwenden.</span><span class="sxs-lookup"><span data-stu-id="876b4-145">The user can also apply a custom setting.</span></span> <span data-ttu-id="876b4-146">Ab Windows 7 ist dpi eine Einstellung pro Benutzer.</span><span class="sxs-lookup"><span data-stu-id="876b4-146">Starting in Windows 7, DPI is a per-user setting.</span></span>

## <a name="dwm-scaling"></a><span data-ttu-id="876b4-147">DWM-Skalierung</span><span class="sxs-lookup"><span data-stu-id="876b4-147">DWM Scaling</span></span>

<span data-ttu-id="876b4-148">Wenn ein Programm dpi nicht berücksichtigt, sind möglicherweise die folgenden Fehler bei den Einstellungen für hohe DPI-Einstellungen erkennbar:</span><span class="sxs-lookup"><span data-stu-id="876b4-148">If a program does not account for DPI, the following defects might be apparent at high-DPI settings:</span></span>

-   <span data-ttu-id="876b4-149">Clipped UI-Elemente.</span><span class="sxs-lookup"><span data-stu-id="876b4-149">Clipped UI elements.</span></span>
-   <span data-ttu-id="876b4-150">Falsches Layout.</span><span class="sxs-lookup"><span data-stu-id="876b4-150">Incorrect layout.</span></span>
-   <span data-ttu-id="876b4-151">Pixel-Bitmaps und-Symbole.</span><span class="sxs-lookup"><span data-stu-id="876b4-151">Pixelated bitmaps and icons.</span></span>
-   <span data-ttu-id="876b4-152">Falsche Maus Koordinaten, die Auswirkungen auf Treffer Tests, Drag & Drop usw. haben können.</span><span class="sxs-lookup"><span data-stu-id="876b4-152">Incorrect mouse coordinates, which can affect hit testing, drag and drop, and so forth.</span></span>

<span data-ttu-id="876b4-153">Um sicherzustellen, dass ältere Programme bei High-dpi-Einstellungen funktionieren, implementiert die DWM einen nützlichen Fallback.</span><span class="sxs-lookup"><span data-stu-id="876b4-153">To ensure that older programs work at high-DPI settings, the DWM implements a useful fallback.</span></span> <span data-ttu-id="876b4-154">Wenn ein Programm nicht als dpi-fähig gekennzeichnet ist, skaliert die DWM die gesamte Benutzeroberfläche entsprechend der dpi-Einstellung.</span><span class="sxs-lookup"><span data-stu-id="876b4-154">If a program is not marked as being DPI aware, the DWM will scale the entire UI to match the DPI setting.</span></span> <span data-ttu-id="876b4-155">Beispielsweise wird die Benutzeroberfläche bei 144 dpi um 150% skaliert, einschließlich Text, Grafiken, Steuerelementen und Fenstergrößen.</span><span class="sxs-lookup"><span data-stu-id="876b4-155">For example, at 144 DPI, the UI is scaled by 150%, including text, graphics, controls, and window sizes.</span></span> <span data-ttu-id="876b4-156">Wenn das Programm ein 500 × 500-Fenster erstellt, wird das Fenster tatsächlich als 750 × 750 Pixel angezeigt, und der Inhalt des Fensters wird entsprechend skaliert.</span><span class="sxs-lookup"><span data-stu-id="876b4-156">If the program creates a 500 × 500 window, the window actually appears as 750 × 750 pixels, and the contents of the window are scaled accordingly.</span></span>

<span data-ttu-id="876b4-157">Dieses Verhalten bedeutet, dass ältere Programme bei High-dpi-Einstellungen "just work" funktionieren.</span><span class="sxs-lookup"><span data-stu-id="876b4-157">This behavior means that older programs "just work" at high-DPI settings.</span></span> <span data-ttu-id="876b4-158">Die Skalierung führt jedoch auch zu einem etwas unscharf dargestellten aussehen, da die Skalierung nach dem Zeichnen des Fensters angewendet wird.</span><span class="sxs-lookup"><span data-stu-id="876b4-158">However, scaling also results in a somewhat blurry appearance, because the scaling is applied after the window is drawn.</span></span>

## <a name="dpi-aware-applications"></a><span data-ttu-id="876b4-159">DPI-Aware Anwendungen</span><span class="sxs-lookup"><span data-stu-id="876b4-159">DPI-Aware Applications</span></span>

<span data-ttu-id="876b4-160">Um die DWM-Skalierung zu vermeiden, kann sich ein Programm selbst als dpi-fähig kennzeichnen.</span><span class="sxs-lookup"><span data-stu-id="876b4-160">To avoid DWM scaling, a program can mark itself as DPI-aware.</span></span> <span data-ttu-id="876b4-161">Dies weist den DWM an, keine automatische DPI-Skalierung auszuführen.</span><span class="sxs-lookup"><span data-stu-id="876b4-161">This tells the DWM not to perform any automatic DPI scaling.</span></span> <span data-ttu-id="876b4-162">Alle neuen Anwendungen sollten für die dpi-Unterstützung entworfen werden, da die Darstellung der Benutzeroberfläche bei höheren dpi-Einstellungen durch die dpi-Erkennung verbessert wird.</span><span class="sxs-lookup"><span data-stu-id="876b4-162">All new applications should be designed to be DPI-aware, because DPI awareness improves the appearance of the UI at higher DPI settings.</span></span>

<span data-ttu-id="876b4-163">Ein Programm deklariert sich über sein Anwendungs Manifest mit dpi-Werten.</span><span class="sxs-lookup"><span data-stu-id="876b4-163">A program declares itself DPI-aware through its application manifest.</span></span> <span data-ttu-id="876b4-164">Ein *Manifest* ist eine einfache XML-Datei, die eine DLL oder Anwendung beschreibt.</span><span class="sxs-lookup"><span data-stu-id="876b4-164">A *manifest* is a simply an XML file that describes a DLL or application.</span></span> <span data-ttu-id="876b4-165">Das Manifest ist in der Regel in die ausführbare Datei eingebettet, obwohl es als separate Datei bereitgestellt werden kann.</span><span class="sxs-lookup"><span data-stu-id="876b4-165">The manifest is typically embedded in the executable file, although it can be provided as a separate file.</span></span> <span data-ttu-id="876b4-166">Ein Manifest enthält Informationen, wie z. b. dll-Abhängigkeiten, die angeforderte Berechtigungsebene und die Version von Windows, für die das Programm entworfen wurde.</span><span class="sxs-lookup"><span data-stu-id="876b4-166">A manifest contains information such as DLL dependencies, the requested privilege level, and what version of Windows the program was designed for.</span></span>

<span data-ttu-id="876b4-167">Um zu deklarieren, dass das Programm dpi-fähig ist, fügen Sie die folgenden Informationen in das Manifest ein.</span><span class="sxs-lookup"><span data-stu-id="876b4-167">To declare that your program is DPI-aware, include the following information in the manifest.</span></span>

``` syntax
<assembly xmlns="urn:schemas-microsoft-com:asm.v1" manifestVersion="1.0" xmlns:asmv3="urn:schemas-microsoft-com:asm.v3" >
  <asmv3:application>
    <asmv3:windowsSettings xmlns="http://schemas.microsoft.com/SMI/2005/WindowsSettings">
      <dpiAware>true</dpiAware>
    </asmv3:windowsSettings>
  </asmv3:application>
</assembly>
```

<span data-ttu-id="876b4-168">Die hier gezeigte Auflistung ist nur ein partielles Manifest, aber der Visual Studio-Linker generiert automatisch den Rest des Manifests.</span><span class="sxs-lookup"><span data-stu-id="876b4-168">The listing shown here is only a partial manifest, but the Visual Studio linker generates the rest of the manifest for you automatically.</span></span> <span data-ttu-id="876b4-169">Führen Sie in Visual Studio die folgenden Schritte aus, um ein partielles Manifest in das Projekt einzuschließen.</span><span class="sxs-lookup"><span data-stu-id="876b4-169">To include a partial manifest in your project, perform the following steps in Visual Studio.</span></span>

1.  <span data-ttu-id="876b4-170">Klicken Sie im Menü **Projekt** auf **Eigenschaft**.</span><span class="sxs-lookup"><span data-stu-id="876b4-170">On the **Project** menu, click **Property**.</span></span>
2.  <span data-ttu-id="876b4-171">Erweitern Sie im linken Bereich **Konfigurations Eigenschaften**, erweitern Sie **Manifest-Tool**, und klicken Sie dann auf **Eingabe und Ausgabe**.</span><span class="sxs-lookup"><span data-stu-id="876b4-171">In the left pane, expand **Configuration Properties**, expand **Manifest Tool**, and then click **Input and Output**.</span></span>
3.  <span data-ttu-id="876b4-172">Geben Sie im Textfeld **zusätzliche Manifest-Dateien** den Namen der Manifest-Datei ein, und klicken Sie dann auf **OK**.</span><span class="sxs-lookup"><span data-stu-id="876b4-172">In the **Additional Manifest Files** text box, type the name of the manifest file, and then click **OK**.</span></span>

<span data-ttu-id="876b4-173">Wenn Sie Ihr Programm als dpi-fähig markieren, weisen Sie die DWM an, das Anwendungsfenster nicht zu skalieren.</span><span class="sxs-lookup"><span data-stu-id="876b4-173">By marking your program as DPI-aware, you are telling the DWM not to scale your application window.</span></span> <span data-ttu-id="876b4-174">Wenn Sie nun ein Fenster mit dem Wert 500 × 500 erstellen, belegt das Fenster unabhängig von der dpi-Einstellung des Benutzers 500 × 500 Pixel.</span><span class="sxs-lookup"><span data-stu-id="876b4-174">Now if you create a 500 × 500 window, the window will occupy 500 × 500 pixels, regardless of the user's DPI setting.</span></span>

## <a name="gdi-and-dpi"></a><span data-ttu-id="876b4-175">GDI und dpi</span><span class="sxs-lookup"><span data-stu-id="876b4-175">GDI and DPI</span></span>

<span data-ttu-id="876b4-176">Die GDI-Zeichnung wird in Pixel gemessen.</span><span class="sxs-lookup"><span data-stu-id="876b4-176">GDI drawing is measured in pixels.</span></span> <span data-ttu-id="876b4-177">Dies bedeutet Folgendes: Wenn Ihr Programm als dpi-fähig markiert ist, und Sie GDI zum Zeichnen eines 200 × 100-Rechtecks auffordern, wird das resultierende Rechteck 200 Pixel breit und 100 Pixel auf dem Bildschirm angezeigt.</span><span class="sxs-lookup"><span data-stu-id="876b4-177">That means if your program is marked as DPI-aware, and you ask GDI to draw a 200 × 100 rectangle, the resulting rectangle will be 200 pixels wide and 100 pixels tall on the screen.</span></span> <span data-ttu-id="876b4-178">GDI-Schriftgrößen werden jedoch auf die aktuelle dpi-Einstellung skaliert.</span><span class="sxs-lookup"><span data-stu-id="876b4-178">However, GDI font sizes are scaled to the current DPI setting.</span></span> <span data-ttu-id="876b4-179">Anders ausgedrückt: Wenn Sie eine 72-Punkt-Schriftart erstellen, beträgt die Schriftart 96 Pixel bei 96 dpi, aber 144 Pixel bei 144 dpi.</span><span class="sxs-lookup"><span data-stu-id="876b4-179">In other words, if you create a 72-point font, the size of the font will be 96 pixels at 96 DPI, but 144 pixels at 144 DPI.</span></span> <span data-ttu-id="876b4-180">Hier sehen Sie eine 72-Punkt Schriftart, die mit GDI bei 144 dpi gerendert wird</span><span class="sxs-lookup"><span data-stu-id="876b4-180">Here is a 72 point font rendered at 144 DPI using GDI.</span></span>

![ein Diagramm, das die Skalierung von dpi-Schriftart in GDI anzeigt.](images/graphics12.png)

<span data-ttu-id="876b4-182">Wenn Ihre Anwendung dpi-fähig ist und Sie GDI zum Zeichnen verwenden, Skalieren Sie alle Zeichnungs Koordinaten entsprechend der dpi-Größe.</span><span class="sxs-lookup"><span data-stu-id="876b4-182">If your application is DPI-aware and you use GDI for drawing, scale all of your drawing coordinates to match the DPI.</span></span>

## <a name="direct2d-and-dpi"></a><span data-ttu-id="876b4-183">Direct2D und dpi</span><span class="sxs-lookup"><span data-stu-id="876b4-183">Direct2D and DPI</span></span>

<span data-ttu-id="876b4-184">Direct2D führt die Skalierung automatisch entsprechend der dpi-Einstellung aus.</span><span class="sxs-lookup"><span data-stu-id="876b4-184">Direct2D automatically performs scaling to match the DPI setting.</span></span> <span data-ttu-id="876b4-185">In Direct2D werden Koordinaten in Einheiten gemessen, die als *geräteunabhängige Pixel (Device-Independent Pixels* , Dips) bezeichnet werden.</span><span class="sxs-lookup"><span data-stu-id="876b4-185">In Direct2D, coordinates are measured in units called *device-independent pixels* (DIPs).</span></span> <span data-ttu-id="876b4-186">Eine DIP ist als 1/96-eines *logischen* Zoll definiert.</span><span class="sxs-lookup"><span data-stu-id="876b4-186">A DIP is defined as 1/96th of a *logical* inch.</span></span> <span data-ttu-id="876b4-187">In Direct2D werden alle Zeichnungsvorgänge in Dips angegeben und dann auf die aktuelle dpi-Einstellung skaliert.</span><span class="sxs-lookup"><span data-stu-id="876b4-187">In Direct2D, all drawing operations are specified in DIPs and then scaled to the current DPI setting.</span></span>



| <span data-ttu-id="876b4-188">DPI-Einstellung</span><span class="sxs-lookup"><span data-stu-id="876b4-188">DPI setting</span></span> | <span data-ttu-id="876b4-189">DIP-Größe</span><span class="sxs-lookup"><span data-stu-id="876b4-189">DIP size</span></span>    |
|-------------|-------------|
| <span data-ttu-id="876b4-190">96</span><span class="sxs-lookup"><span data-stu-id="876b4-190">96</span></span>          | <span data-ttu-id="876b4-191">1 Pixel</span><span class="sxs-lookup"><span data-stu-id="876b4-191">1 pixel</span></span>     |
| <span data-ttu-id="876b4-192">120</span><span class="sxs-lookup"><span data-stu-id="876b4-192">120</span></span>         | <span data-ttu-id="876b4-193">1,25 Pixel</span><span class="sxs-lookup"><span data-stu-id="876b4-193">1.25 pixels</span></span> |
| <span data-ttu-id="876b4-194">144</span><span class="sxs-lookup"><span data-stu-id="876b4-194">144</span></span>         | <span data-ttu-id="876b4-195">1,5 Pixel</span><span class="sxs-lookup"><span data-stu-id="876b4-195">1.5 pixels</span></span>  |



 

<span data-ttu-id="876b4-196">Wenn die dpi-Einstellung des Benutzers z. b. 144 dpi ist und Sie Direct2D zum Zeichnen eines 200 × 100-Rechtecks auffordern, wird das Rechteck 300 × 150 physischer Pixel sein.</span><span class="sxs-lookup"><span data-stu-id="876b4-196">For example, if the user's DPI setting is 144 DPI, and you ask Direct2D to draw a 200 × 100 rectangle, the rectangle will be 300 × 150 physical pixels.</span></span> <span data-ttu-id="876b4-197">Außerdem misst DirectWrite Schriftgrößen in Dips anstelle von Punkten.</span><span class="sxs-lookup"><span data-stu-id="876b4-197">In addition, DirectWrite measures font sizes in DIPs, rather than points.</span></span> <span data-ttu-id="876b4-198">Um eine Schriftart mit 12 Punkten zu erstellen, geben Sie 16 Dips an (12 Punkte = 1/6 logischer Zoll = 96/6 Dips).</span><span class="sxs-lookup"><span data-stu-id="876b4-198">To create a 12-point font, specify 16 DIPs (12 points = 1/6 logical inch = 96/6 DIPs).</span></span> <span data-ttu-id="876b4-199">Wenn der Text auf dem Bildschirm gezeichnet wird, konvertiert Direct2D die Dips in physische Pixel.</span><span class="sxs-lookup"><span data-stu-id="876b4-199">When the text is drawn on the screen, Direct2D converts the DIPs to physical pixels.</span></span> <span data-ttu-id="876b4-200">Der Vorteil dieses Systems besteht darin, dass die Maßeinheiten sowohl für Text als auch für Zeichnung konsistent sind, unabhängig von der aktuellen dpi-Einstellung.</span><span class="sxs-lookup"><span data-stu-id="876b4-200">The benefit of this system is that the units of measurement are consistent for both text and drawing, regardless of the current DPI setting.</span></span>

<span data-ttu-id="876b4-201">Ein Wort mit Vorsicht: Maus-und Fenster Koordinaten werden immer noch in physischen Pixeln, nicht in Dips angegeben.</span><span class="sxs-lookup"><span data-stu-id="876b4-201">A word of caution: Mouse and window coordinates are still given in physical pixels, not DIPs.</span></span> <span data-ttu-id="876b4-202">Wenn Sie z. b. die [**WM- \_ lbuttondown**](/windows/desktop/inputdev/wm-lbuttondown) -Meldung verarbeiten, wird die MouseDown-Position in physischen Pixeln angegeben.</span><span class="sxs-lookup"><span data-stu-id="876b4-202">For example, if you process the [**WM\_LBUTTONDOWN**](/windows/desktop/inputdev/wm-lbuttondown) message, the mouse-down position is given in physical pixels.</span></span> <span data-ttu-id="876b4-203">Um einen Punkt an dieser Position zu zeichnen, müssen Sie die Pixelkoordinaten in Dips konvertieren.</span><span class="sxs-lookup"><span data-stu-id="876b4-203">To draw a point at that position, you must convert the pixel coordinates to DIPs.</span></span>

## <a name="converting-physical-pixels-to-dips"></a><span data-ttu-id="876b4-204">Umstellen physischer Pixel in Dips</span><span class="sxs-lookup"><span data-stu-id="876b4-204">Converting Physical Pixels to DIPs</span></span>

<span data-ttu-id="876b4-205">Die Konvertierung von physischen Pixeln in Dips verwendet die folgende Formel.</span><span class="sxs-lookup"><span data-stu-id="876b4-205">The conversion from physical pixels to DIPs uses the following formula.</span></span>

<dl> <span data-ttu-id="876b4-206">Dips = Pixel/(dpi/96.0)</span><span class="sxs-lookup"><span data-stu-id="876b4-206">DIPs = pixels / (DPI/96.0)</span></span>  
</dl>

<span data-ttu-id="876b4-207">Um die dpi-Einstellung abzurufen, müssen Sie die [**ID2D1Factory:: getdesktopdpi**](/windows/desktop/api/d2d1/nf-d2d1-id2d1factory-getdesktopdpi) -Methode aufrufen.</span><span class="sxs-lookup"><span data-stu-id="876b4-207">To get the DPI setting, call the [**ID2D1Factory::GetDesktopDpi**](/windows/desktop/api/d2d1/nf-d2d1-id2d1factory-getdesktopdpi) method.</span></span> <span data-ttu-id="876b4-208">Der dpi-Wert wird als zwei Gleit Komma Werte zurückgegeben, eine für die x-Achse und eine für die y-Achse.</span><span class="sxs-lookup"><span data-stu-id="876b4-208">The DPI is returned as two floating-point values, one for the x-axis and one for the y-axis.</span></span> <span data-ttu-id="876b4-209">Theoretisch können sich diese Werte unterscheiden.</span><span class="sxs-lookup"><span data-stu-id="876b4-209">In theory, these values can differ.</span></span> <span data-ttu-id="876b4-210">Berechnen Sie einen separaten Skalierungsfaktor für jede Achse.</span><span class="sxs-lookup"><span data-stu-id="876b4-210">Calculate a separate scaling factor for each axis.</span></span>


```C++
float g_DPIScaleX = 1.0f;
float g_DPIScaleY = 1.0f;

void InitializeDPIScale(ID2D1Factory *pFactory)
{
    FLOAT dpiX, dpiY;

    pFactory->GetDesktopDpi(&dpiX, &dpiY);

    g_DPIScaleX = dpiX/96.0f;
    g_DPIScaleY = dpiY/96.0f;
}

template <typename T>
float PixelsToDipsX(T x)
{
    return static_cast<float>(x) / g_DPIScaleX;
}

template <typename T>
float PixelsToDipsY(T y)
{
    return static_cast<float>(y) / g_DPIScaleY;
}
```



<span data-ttu-id="876b4-211">Dies ist eine alternative Möglichkeit, die dpi-Einstellung zu erhalten, wenn Sie nicht Direct2D verwenden:</span><span class="sxs-lookup"><span data-stu-id="876b4-211">Here is an alternate way to get the DPI setting if you are not using Direct2D:</span></span>


```C++
void InitializeDPIScale(HWND hwnd)
{
    HDC hdc = GetDC(hwnd);
    g_DPIScaleX = GetDeviceCaps(hdc, LOGPIXELSX) / 96.0f;
    g_DPIScaleY = GetDeviceCaps(hdc, LOGPIXELSY) / 96.0f;
    ReleaseDC(hwnd, hdc);
}
```
> [!Note]  
> <span data-ttu-id="876b4-212">Unter Windows 10, Version 1903, ist  [**ID2D1Factory:: getdesktopdpi**](/windows/win32/api/d2d1/nf-d2d1-id2d1factory-getdesktopdpi) veraltet, und die Empfehlung lautet " [**Displayinformation:: logicaldpi**](/uwp/api/windows.graphics.display.displayinformation.logicaldpi?view=winrt-19041) for Windows Store Apps" oder " [**getdpiforwindow**](/windows/win32/api/winuser/nf-winuser-getdpiforwindow) " für Desktop-Apps.</span><span class="sxs-lookup"><span data-stu-id="876b4-212">On Windows 10, version 1903,  [**ID2D1Factory::GetDesktopDpi**](/windows/win32/api/d2d1/nf-d2d1-id2d1factory-getdesktopdpi) is deprecated and the recommendation is [**DisplayInformation::LogicalDpi**](/uwp/api/windows.graphics.display.displayinformation.logicaldpi?view=winrt-19041) for Windows Store Apps or [**GetDpiForWindow**](/windows/win32/api/winuser/nf-winuser-getdpiforwindow) for desktop apps.</span></span> <span data-ttu-id="876b4-213">Wenn Sie Sie weiterhin verwenden möchten, unterdrücken Sie die Compilerfehlermeldung, indem Sie die Zeile [**#pragma Warnung (unterdrücken: 4996)**](/cpp/error-messages/compiler-warnings/compiler-warning-level-3-c4996?view=vs-2019) direkt vor dem [**ID2D1Factory:: getdesktopdpi**](/windows/win32/api/d2d1/nf-d2d1-id2d1factory-getdesktopdpi) -Befehl schreiben.</span><span class="sxs-lookup"><span data-stu-id="876b4-213">If you still want to use it, suppress the compiler error message by writing the line [**#pragma warning(suppress: 4996)**](/cpp/error-messages/compiler-warnings/compiler-warning-level-3-c4996?view=vs-2019) just before the [**ID2D1Factory::GetDesktopDpi**](/windows/win32/api/d2d1/nf-d2d1-id2d1factory-getdesktopdpi) call.</span></span> <span data-ttu-id="876b4-214">Obwohl dies nicht empfohlen wird, ist es möglich, das standardmäßige dpi-Bewusstsein mithilfe von [**setprocessdpiawareness Context**](/windows/win32/api/winuser/nf-winuser-setprocessdpiawarenesscontext)Programm gesteuert festzulegen.</span><span class="sxs-lookup"><span data-stu-id="876b4-214">Although it is not recommended, it is possible to set the default DPI awareness programmatically using [**SetProcessDpiAwarenessContext**](/windows/win32/api/winuser/nf-winuser-setprocessdpiawarenesscontext).</span></span> <span data-ttu-id="876b4-215">Sobald ein Fenster (ein HWND) in Ihrem Prozess erstellt wurde, wird das Ändern des dpi-Informationsmodus nicht mehr unterstützt.</span><span class="sxs-lookup"><span data-stu-id="876b4-215">Once a window (an HWND) has been created in your process, changing the DPI awareness mode is no longer supported.</span></span> <span data-ttu-id="876b4-216">Wenn Sie den Prozess-Standard-dpi-Informationsmodus Programm gesteuert festlegen, müssen Sie die entsprechende API vor dem Erstellen von HWNDs aufruft.</span><span class="sxs-lookup"><span data-stu-id="876b4-216">If you are setting the process-default DPI awareness mode programmatically, you must call the corresponding API before any HWNDs have been created.</span></span> <span data-ttu-id="876b4-217">Weitere Informationen finden Sie [unter Festlegen der Standard-dpi-Informationen für einen Prozess](../hidpi/setting-the-default-dpi-awareness-for-a-process.md).</span><span class="sxs-lookup"><span data-stu-id="876b4-217">For information see [Setting the default DPI awareness for a process](../hidpi/setting-the-default-dpi-awareness-for-a-process.md).</span></span>

## <a name="resizing-the-render-target"></a><span data-ttu-id="876b4-218">Ändern der Größe des Renderziels</span><span class="sxs-lookup"><span data-stu-id="876b4-218">Resizing the Render Target</span></span>

<span data-ttu-id="876b4-219">Wenn die Größe des Fensters geändert wird, müssen Sie die Größe des Renderziels entsprechend anpassen.</span><span class="sxs-lookup"><span data-stu-id="876b4-219">If the size of the window changes, you must resize the render target to match.</span></span> <span data-ttu-id="876b4-220">In den meisten Fällen müssen Sie auch das Layout aktualisieren und das Fenster neu zeichnen.</span><span class="sxs-lookup"><span data-stu-id="876b4-220">In most cases, you will also need to update the layout and repaint the window.</span></span> <span data-ttu-id="876b4-221">Der folgende Code zeigt diese Schritte.</span><span class="sxs-lookup"><span data-stu-id="876b4-221">The following code shows these steps.</span></span>


```C++
void MainWindow::Resize()
{
    if (pRenderTarget != NULL)
    {
        RECT rc;
        GetClientRect(m_hwnd, &rc);

        D2D1_SIZE_U size = D2D1::SizeU(rc.right, rc.bottom);

        pRenderTarget->Resize(size);
        CalculateLayout();
        InvalidateRect(m_hwnd, NULL, FALSE);
    }
}
```



<span data-ttu-id="876b4-222">Die [**GetClientRect**](/windows/desktop/api/winuser/nf-winuser-getclientrect) -Funktion Ruft die neue Größe des Client Bereichs in physischen Pixeln (nicht Dips) ab.</span><span class="sxs-lookup"><span data-stu-id="876b4-222">The [**GetClientRect**](/windows/desktop/api/winuser/nf-winuser-getclientrect) function gets the new size of the client area, in physical pixels (not DIPs).</span></span> <span data-ttu-id="876b4-223">Die [**ID2D1HwndRenderTarget:: Resize**](../direct2d/id2d1hwndrendertarget-resize.md) -Methode aktualisiert die Größe des Renderziels, auch in Pixel angegeben.</span><span class="sxs-lookup"><span data-stu-id="876b4-223">The [**ID2D1HwndRenderTarget::Resize**](../direct2d/id2d1hwndrendertarget-resize.md) method updates the size of the render target, also specified in pixels.</span></span> <span data-ttu-id="876b4-224">Die [**invalidatup**](/windows/desktop/api/winuser/nf-winuser-invalidaterect) -Funktion erzwingt eine Umgestaltung durch Hinzufügen des gesamten Client Bereichs zum Aktualisierungs Bereich des Fensters.</span><span class="sxs-lookup"><span data-stu-id="876b4-224">The [**InvalidateRect**](/windows/desktop/api/winuser/nf-winuser-invalidaterect) function forces a repaint by adding the entire client area to the window's update region.</span></span> <span data-ttu-id="876b4-225">(Siehe zeichnen [des Fensters](painting-the-window.md)in Modul 1.)</span><span class="sxs-lookup"><span data-stu-id="876b4-225">(See [Painting the Window](painting-the-window.md), in Module 1.)</span></span>

<span data-ttu-id="876b4-226">Wenn das Fenster wächst oder verkleinert wird, müssen Sie in der Regel die Position der Objekte neu berechnen, die Sie zeichnen.</span><span class="sxs-lookup"><span data-stu-id="876b4-226">As the window grows or shrinks, you will typically need to recalculate the position of the objects that you draw.</span></span> <span data-ttu-id="876b4-227">Im kreisprogramm müssen z. b. der RADIUS und der Mittelpunkt aktualisiert werden:</span><span class="sxs-lookup"><span data-stu-id="876b4-227">For example, in the circle program, the radius and center point must be updated:</span></span>


```C++
void MainWindow::CalculateLayout()
{
    if (pRenderTarget != NULL)
    {
        D2D1_SIZE_F size = pRenderTarget->GetSize();
        const float x = size.width / 2;
        const float y = size.height / 2;
        const float radius = min(x, y);
        ellipse = D2D1::Ellipse(D2D1::Point2F(x, y), radius, radius);
    }
}
```



<span data-ttu-id="876b4-228">Die [**ID2D1RenderTarget:: GetSize**](/windows/desktop/api/d2d1/nf-d2d1-id2d1rendertarget-getsize) -Methode gibt die Größe des Renderziels in Dips (nicht Pixel) zurück. Dies ist die geeignete Einheit zum Berechnen des Layouts.</span><span class="sxs-lookup"><span data-stu-id="876b4-228">The [**ID2D1RenderTarget::GetSize**](/windows/desktop/api/d2d1/nf-d2d1-id2d1rendertarget-getsize) method returns the size of the render target in DIPs (not pixels), which is the appropriate unit for calculating layout.</span></span> <span data-ttu-id="876b4-229">Es gibt eine eng verwandte Methode, [**ID2D1RenderTarget:: getpixelsize**](/windows/desktop/api/d2d1/nf-d2d1-id2d1rendertarget-getpixelsize), die die Größe in physischen Pixeln zurückgibt.</span><span class="sxs-lookup"><span data-stu-id="876b4-229">There is a closely related method, [**ID2D1RenderTarget::GetPixelSize**](/windows/desktop/api/d2d1/nf-d2d1-id2d1rendertarget-getpixelsize), that returns the size in physical pixels.</span></span> <span data-ttu-id="876b4-230">Für ein **HWND** -Renderziel entspricht dieser Wert der Größe, die von [**GetClientRect**](/windows/desktop/api/winuser/nf-winuser-getclientrect)zurückgegeben wurde.</span><span class="sxs-lookup"><span data-stu-id="876b4-230">For an **HWND** render target, this value matches the size returned by [**GetClientRect**](/windows/desktop/api/winuser/nf-winuser-getclientrect).</span></span> <span data-ttu-id="876b4-231">Beachten Sie jedoch, dass das Zeichnen in Dips und nicht in Pixel erfolgt.</span><span class="sxs-lookup"><span data-stu-id="876b4-231">But remember that drawing is performed in DIPs, not pixels.</span></span>

## <a name="next"></a><span data-ttu-id="876b4-232">Nächste</span><span class="sxs-lookup"><span data-stu-id="876b4-232">Next</span></span>

[<span data-ttu-id="876b4-233">Verwenden von Color in Direct2D</span><span class="sxs-lookup"><span data-stu-id="876b4-233">Using Color in Direct2D</span></span>](using-color-in-direct2d.md)

 

 
