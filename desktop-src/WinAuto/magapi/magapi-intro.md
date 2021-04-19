---
title: Übersicht über die Vergrößerung
description: In diesem Thema wird die Vergrößerungs-API beschrieben und erläutert, wie Sie in einer Anwendung verwendet wird.
ms.assetid: 8dcecb73-db73-4043-b922-0b92f299eb1d
keywords:
- Vergrößern
- Anwendungen zur Bildschirm Vergrößerung
- Vergrößern
- benutzerdefinierte Abbild Verarbeitung
- Magnification.dll
- Erstellen von Lupe Steuerelementen
- selektive Vergrößerung
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 16d66595cc2f5fdd8402ecd9d525e6deb1d07078
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "106342356"
---
# <a name="magnification-api-overview"></a><span data-ttu-id="769ba-110">Übersicht über die Vergrößerung</span><span class="sxs-lookup"><span data-stu-id="769ba-110">Magnification API Overview</span></span>

<span data-ttu-id="769ba-111">Die Vergrößerungs-API ermöglicht hilfstechnologieanbietern, Bildschirm Vergrößerungs Anwendungen zu entwickeln, die unter Microsoft Windows ausgeführt werden.</span><span class="sxs-lookup"><span data-stu-id="769ba-111">The Magnification API enables assistive technology vendors to develop screen magnification applications that run on Microsoft Windows.</span></span> <span data-ttu-id="769ba-112">In diesem Thema wird die Vergrößerungs-API beschrieben und erläutert, wie Sie in einer Anwendung verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="769ba-112">This topic describes the Magnification API and explains how to use it in an application.</span></span> <span data-ttu-id="769ba-113">Sie enthält die folgenden Abschnitte:</span><span class="sxs-lookup"><span data-stu-id="769ba-113">It contains the following sections:</span></span>

- [<span data-ttu-id="769ba-114">Erste Schritte</span><span class="sxs-lookup"><span data-stu-id="769ba-114">Getting Started</span></span>](#getting-started)
- [<span data-ttu-id="769ba-115">Grundlegende Konzepte</span><span class="sxs-lookup"><span data-stu-id="769ba-115">Basic Concepts</span></span>](#basic-concepts)
  - [<span data-ttu-id="769ba-116">Typen von Bildschirmlupe</span><span class="sxs-lookup"><span data-stu-id="769ba-116">Types of Magnifiers</span></span>](#types-of-magnifiers)
  - [<span data-ttu-id="769ba-117">Vergrößerungsfaktor</span><span class="sxs-lookup"><span data-stu-id="769ba-117">Magnification Factor</span></span>](#magnification-factor)
  - [<span data-ttu-id="769ba-118">Farbeffekte</span><span class="sxs-lookup"><span data-stu-id="769ba-118">Color Effects</span></span>](#color-effects)
  - [<span data-ttu-id="769ba-119">Quell Rechteck</span><span class="sxs-lookup"><span data-stu-id="769ba-119">Source Rectangle</span></span>](#source-rectangle)
  - [<span data-ttu-id="769ba-120">Filter Liste</span><span class="sxs-lookup"><span data-stu-id="769ba-120">Filter List</span></span>](#filter-list)
  - [<span data-ttu-id="769ba-121">Eingabe Transformation</span><span class="sxs-lookup"><span data-stu-id="769ba-121">Input Transform</span></span>](#input-transform)
  - [<span data-ttu-id="769ba-122">System Cursor</span><span class="sxs-lookup"><span data-stu-id="769ba-122">System Cursor</span></span>](#system-cursor)
- [<span data-ttu-id="769ba-123">Initialisieren der Lauf Zeit Bibliothek für die Bildschirmlupe</span><span class="sxs-lookup"><span data-stu-id="769ba-123">Initializing the Magnifier Run-time Library</span></span>](#initializing-the-magnifier-run-time-library)
- [<span data-ttu-id="769ba-124">Verwenden der Full-Screen Bildschirmlupe</span><span class="sxs-lookup"><span data-stu-id="769ba-124">Using the Full-Screen Magnifier</span></span>](#using-the-full-screen-magnifier)
- [<span data-ttu-id="769ba-125">Verwenden des Vergrößerungs Steuer Elements</span><span class="sxs-lookup"><span data-stu-id="769ba-125">Using the Magnifier Control</span></span>](#using-the-magnifier-control)
  - [<span data-ttu-id="769ba-126">Erstellen des Vergrößerungs Steuer Elements</span><span class="sxs-lookup"><span data-stu-id="769ba-126">Creating the Magnifier Control</span></span>](#creating-the-magnifier-control)
  - [<span data-ttu-id="769ba-127">Initialisieren des Steuerelements</span><span class="sxs-lookup"><span data-stu-id="769ba-127">Initializing the Control</span></span>](#initializing-the-control)
  - [<span data-ttu-id="769ba-128">Festlegen des Quell Rechtecks</span><span class="sxs-lookup"><span data-stu-id="769ba-128">Setting the Source Rectangle</span></span>](#setting-the-source-rectangle)
  - [<span data-ttu-id="769ba-129">Anwenden von Farbeffekten</span><span class="sxs-lookup"><span data-stu-id="769ba-129">Applying Color Effects</span></span>](#applying-color-effects)
  - [<span data-ttu-id="769ba-130">Selektive Vergrößerung</span><span class="sxs-lookup"><span data-stu-id="769ba-130">Selective Magnification</span></span>](#selective-magnification)
- [<span data-ttu-id="769ba-131">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="769ba-131">Related topics</span></span>](#related-topics)

## <a name="getting-started"></a><span data-ttu-id="769ba-132">Erste Schritte</span><span class="sxs-lookup"><span data-stu-id="769ba-132">Getting Started</span></span>

<span data-ttu-id="769ba-133">Die ursprüngliche Version der Vergrößerungs-API wird unter Windows Vista und höheren Betriebssystemen unterstützt.</span><span class="sxs-lookup"><span data-stu-id="769ba-133">The original release of the Magnification API is supported on Windows Vista and later operating systems.</span></span> <span data-ttu-id="769ba-134">Unter Windows 8 und höher unterstützt die API zusätzliche Funktionen, darunter die voll Bildvergrößerung und das Festlegen der Sichtbarkeit des vergrößerten System Cursors.</span><span class="sxs-lookup"><span data-stu-id="769ba-134">On Windows 8 and later, the API supports additional features, including full-screen magnification and setting the visibility of the magnified system cursor.</span></span>

<span data-ttu-id="769ba-135">Die Unterstützung für die Vergrößerungs-API wird von Magnification.dll bereitgestellt.</span><span class="sxs-lookup"><span data-stu-id="769ba-135">Support for the Magnification API is provided by Magnification.dll.</span></span> <span data-ttu-id="769ba-136">Wenn Sie die Anwendung kompilieren möchten, schließen Sie "Vergrößerung. h" ein, und verknüpfen Sie Sie mit "</span><span class="sxs-lookup"><span data-stu-id="769ba-136">To compile your application, include Magnification.h and link to Magnification.lib.</span></span>

> [!Note]  
> <span data-ttu-id="769ba-137">Die Vergrößerungs-API wird unter WOW64 nicht unterstützt. Das heißt, eine 32-Bit-Bildschirmlupe wird auf 64-Bit-Fenstern nicht ordnungsgemäß ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="769ba-137">The Magnification API is not supported under WOW64; that is, a 32-bit magnifier application will not run correctly on 64-bit Windows.</span></span>

## <a name="basic-concepts"></a><span data-ttu-id="769ba-138">Grundlegende Konzepte</span><span class="sxs-lookup"><span data-stu-id="769ba-138">Basic Concepts</span></span>

<span data-ttu-id="769ba-139">In diesem Abschnitt werden die grundlegenden Konzepte beschrieben, auf denen die Vergrößerungs-API basiert.</span><span class="sxs-lookup"><span data-stu-id="769ba-139">This section describes the fundamental concepts that the magnification API is based on.</span></span> <span data-ttu-id="769ba-140">Sie enthält die folgenden Teile:</span><span class="sxs-lookup"><span data-stu-id="769ba-140">It contains the following parts:</span></span>

- [<span data-ttu-id="769ba-141">Typen von Bildschirmlupe</span><span class="sxs-lookup"><span data-stu-id="769ba-141">Types of Magnifiers</span></span>](#types-of-magnifiers)
- [<span data-ttu-id="769ba-142">Vergrößerungsfaktor</span><span class="sxs-lookup"><span data-stu-id="769ba-142">Magnification Factor</span></span>](#magnification-factor)
- [<span data-ttu-id="769ba-143">Farbeffekte</span><span class="sxs-lookup"><span data-stu-id="769ba-143">Color Effects</span></span>](#color-effects)
- [<span data-ttu-id="769ba-144">Quell Rechteck</span><span class="sxs-lookup"><span data-stu-id="769ba-144">Source Rectangle</span></span>](#source-rectangle)
- [<span data-ttu-id="769ba-145">Filter Liste</span><span class="sxs-lookup"><span data-stu-id="769ba-145">Filter List</span></span>](#filter-list)
- [<span data-ttu-id="769ba-146">Eingabe Transformation</span><span class="sxs-lookup"><span data-stu-id="769ba-146">Input Transform</span></span>](#input-transform)
- [<span data-ttu-id="769ba-147">System Cursor</span><span class="sxs-lookup"><span data-stu-id="769ba-147">System Cursor</span></span>](#system-cursor)

### <a name="types-of-magnifiers"></a><span data-ttu-id="769ba-148">Typen von Bildschirmlupe</span><span class="sxs-lookup"><span data-stu-id="769ba-148">Types of Magnifiers</span></span>

<span data-ttu-id="769ba-149">Die API unterstützt zwei Arten von Bildschirmlupe, die *Vollbild-Bildschirmlupe* und das Bildschirm *Lupe-Steuer* Element.</span><span class="sxs-lookup"><span data-stu-id="769ba-149">The API supports two types of magnifiers, the *full-screen magnifier* and the *magnifier control*.</span></span> <span data-ttu-id="769ba-150">Die Vollbild-Bildschirmlupe vergrößert den Inhalt des gesamten Bildschirms, während das Vergrößerungs Steuerelement den Inhalt eines bestimmten Bereichs des Bildschirms vergrößert und den Inhalt in einem Fenster anzeigt.</span><span class="sxs-lookup"><span data-stu-id="769ba-150">The full-screen magnifier magnifies the content of the entire screen, while the magnifier control magnifies the content of a particular area of the screen and displays the content in a window.</span></span> <span data-ttu-id="769ba-151">Bei beiden Vergrößerungen werden Bilder und Text vergrößert, und beide ermöglichen es Ihnen, den Umfang der Vergrößerung zu steuern.</span><span class="sxs-lookup"><span data-stu-id="769ba-151">For both magnifiers, images and text are magnified, and both enable you to control the amount of magnification.</span></span> <span data-ttu-id="769ba-152">Sie können auch Farbeffekte auf den vergrößerten Bildschirminhalt anwenden, um die Anzeige für Personen mit Farbfehlern zu erleichtern oder Farben mit mehr oder weniger Kontrast zu benötigen.</span><span class="sxs-lookup"><span data-stu-id="769ba-152">You can also apply color effects to the magnified screen content, making it easier to see for people who have color deficiencies or need colors that have more or less contrast.</span></span>

> [!Important]  
> <span data-ttu-id="769ba-153">Die Lupe-Steuerelement-API ist unter Windows Vista und höheren Betriebssystemen verfügbar, während die Vollbild-Bildschirmlupe nur unter Windows 8 und höheren Betriebssystemen verfügbar ist.</span><span class="sxs-lookup"><span data-stu-id="769ba-153">The magnifier control API is available on Windows Vista and later operating systems, while the full-screen magnifier API is available only on Windows 8 and later operating systems.</span></span>

### <a name="magnification-factor"></a><span data-ttu-id="769ba-154">Vergrößerungsfaktor</span><span class="sxs-lookup"><span data-stu-id="769ba-154">Magnification Factor</span></span>

<span data-ttu-id="769ba-155">Sowohl der Vollbild-Bildschirmlupe als auch das Lupe-Steuerelement wenden eine Skalierungs Transformation an, um Bildschirminhalte zu vergrößern.</span><span class="sxs-lookup"><span data-stu-id="769ba-155">Both the full-screen magnifier and the magnifier control apply a scale transformation to magnify screen content.</span></span> <span data-ttu-id="769ba-156">Die von der Skalierungs Transformation angewendete Vergrößerung wird als *Vergrößerungsfaktor* bezeichnet.</span><span class="sxs-lookup"><span data-stu-id="769ba-156">The amount of magnification applied by the scale transformation is called the *magnification factor*.</span></span> <span data-ttu-id="769ba-157">Sie wird als Gleit Komma Wert ausgedrückt, wobei 1,0 keiner Vergrößerung entspricht und größere Werte zu einer entsprechenden Vergrößerung führen.</span><span class="sxs-lookup"><span data-stu-id="769ba-157">It is expressed as a floating-point value where 1.0 corresponds to no magnification, and larger values result in a corresponding amount of magnification.</span></span> <span data-ttu-id="769ba-158">Mit dem Wert 1,5 wird der Bildschirminhalt beispielsweise um 50 Prozent vergrößert.</span><span class="sxs-lookup"><span data-stu-id="769ba-158">For example, a value of 1.5 makes the screen content 50 percent larger.</span></span> <span data-ttu-id="769ba-159">Ein Vergrößerungsfaktor, der kleiner als 1,0 ist, ist ungültig.</span><span class="sxs-lookup"><span data-stu-id="769ba-159">A magnification factor less than 1.0 is not valid.</span></span>

### <a name="color-effects"></a><span data-ttu-id="769ba-160">Farbeffekte</span><span class="sxs-lookup"><span data-stu-id="769ba-160">Color Effects</span></span>

<span data-ttu-id="769ba-161">Farbeffekte werden erzielt, indem eine 5-x 5-Farb Transformationsmatrix auf die Farben der vergrößerten Bildschirminhalte angewendet wird.</span><span class="sxs-lookup"><span data-stu-id="769ba-161">Color effects are achieved by applying a 5-by-5 color transformation matrix to the colors of the magnified screen content.</span></span> <span data-ttu-id="769ba-162">Die Matrix bestimmt die Intensitäten der roten, blauen, grünen und Alpha Komponenten des Inhalts.</span><span class="sxs-lookup"><span data-stu-id="769ba-162">The matrix determines the intensities of the red, blue, green, and alpha components of the content.</span></span> <span data-ttu-id="769ba-163">Weitere Informationen finden Sie unter [Verwenden einer Farb Matrix zum Transformieren einer einzelnen Farbe](../../gdiplus/-gdiplus-using-a-color-matrix-to-transform-a-single-color-use.md) in der Windows-GDI+-Dokumentation.</span><span class="sxs-lookup"><span data-stu-id="769ba-163">For more information, see [Using a Color Matrix to Transform a Single Color](../../gdiplus/-gdiplus-using-a-color-matrix-to-transform-a-single-color-use.md) in the Windows GDI+ documentation.</span></span>

### <a name="source-rectangle"></a><span data-ttu-id="769ba-164">Quell Rechteck</span><span class="sxs-lookup"><span data-stu-id="769ba-164">Source Rectangle</span></span>

<span data-ttu-id="769ba-165">Die Vollbild-Bildschirmlupe wendet die Transformation für Skalierung und die Farb Transformation auf den gesamten Bildschirm an.</span><span class="sxs-lookup"><span data-stu-id="769ba-165">The full-screen magnifier applies the scale transformation and color transformation to the entire screen.</span></span> <span data-ttu-id="769ba-166">Das Bildschirm Steuerelement kopiert dagegen einen Bildschirm, der als *Quell Rechteck* bezeichnet wird, in eine Offscreen-Bitmap.</span><span class="sxs-lookup"><span data-stu-id="769ba-166">The magnifier control, on the other hand, copies an area of the screen, called the *source rectangle*, to an off-screen bitmap.</span></span> <span data-ttu-id="769ba-167">Anschließend wendet das-Steuerelement die Skalierungs Transformation und die Farb Transformation (sofern vorhanden) auf die Off-Screen-Bitmap an.</span><span class="sxs-lookup"><span data-stu-id="769ba-167">Next, the control applies the scale transformation and the color transformation, if any, to the off-screen bitmap.</span></span> <span data-ttu-id="769ba-168">Zum Schluss zeigt das Steuerelement die skalierte und Farb transformierte Bitmap im Fenster "Bildschirmlupe" an.</span><span class="sxs-lookup"><span data-stu-id="769ba-168">Finally, the control displays the scaled and color-transformed bitmap in the magnifier control window.</span></span>

### <a name="filter-list"></a><span data-ttu-id="769ba-169">Filter Liste</span><span class="sxs-lookup"><span data-stu-id="769ba-169">Filter List</span></span>

<span data-ttu-id="769ba-170">Standardmäßig vergrößert das Bildschirmlupe-Steuerelement alle Fenster im angegebenen Quell Rechteck.</span><span class="sxs-lookup"><span data-stu-id="769ba-170">By default, the magnifier control magnifies all windows in the specified source rectangle.</span></span> <span data-ttu-id="769ba-171">Durch Bereitstellen einer *Filterliste* von Fenster Handles können Sie jedoch steuern, welche Fenster in den vergrößerten Inhalt eingeschlossen werden und welche nicht.</span><span class="sxs-lookup"><span data-stu-id="769ba-171">However, by providing a *filter list* of window handles, you can control which windows are included in the magnified content, and which are not.</span></span> <span data-ttu-id="769ba-172">Weitere Informationen finden Sie unter [selektive Vergrößerung](#selective-magnification).</span><span class="sxs-lookup"><span data-stu-id="769ba-172">For more information, see [Selective Magnification](#selective-magnification).</span></span>

<span data-ttu-id="769ba-173">Die Vollbild-Bildschirmlupe unterstützt keine Filterliste. alle Fenster werden immer auf dem Bildschirm vergrößert.</span><span class="sxs-lookup"><span data-stu-id="769ba-173">The full-screen magnifier does not support a filter list; it always magnifies all windows on the screen.</span></span>

### <a name="input-transform"></a><span data-ttu-id="769ba-174">Eingabe Transformation</span><span class="sxs-lookup"><span data-stu-id="769ba-174">Input Transform</span></span>

<span data-ttu-id="769ba-175">Normalerweise ist die Vergrößerung des Bildschirm Inhalts "unsichtbar" für Benutzer Stift-oder toucheingaben.</span><span class="sxs-lookup"><span data-stu-id="769ba-175">Normally, magnified screen content is "invisible" to user pen or touch input.</span></span> <span data-ttu-id="769ba-176">Wenn der Benutzer z. b. auf das vergrößerte Bild eines-Steuer Elements tippt, übergibt das System nicht notwendigerweise die Eingabe an das-Steuerelement.</span><span class="sxs-lookup"><span data-stu-id="769ba-176">For example, if the user taps the magnified image of a control, the system does not necessarily pass the input to the control.</span></span> <span data-ttu-id="769ba-177">Stattdessen übergibt das System die Eingabe an das beliebige Element (sofern vorhanden) an den angeprüften Bildschirm Koordinaten auf dem nicht vergrößerten Desktop.</span><span class="sxs-lookup"><span data-stu-id="769ba-177">Instead, the system passes the input to whatever item (if any) resides at the tapped screen coordinates on the unmagnified desktop.</span></span> <span data-ttu-id="769ba-178">Mit der Funktion " [**magsettinputtransform**](/windows/win32/api/Magnification/nf-magnification-magsetinputtransform) " können Sie eine *Eingabe Transformation* angeben, die den Koordinaten Bereich des vergrößerten Bildschirm Inhalts dem tatsächlichen (nicht vergrößerten) Bildschirm Koordinaten Bereich zuordnet.</span><span class="sxs-lookup"><span data-stu-id="769ba-178">The [**MagSetInputTransform**](/windows/win32/api/Magnification/nf-magnification-magsetinputtransform) function enables you to specify an *input transformation* that maps the coordinate space of the magnified screen content to the actual (unmagnified) screen coordinate space.</span></span> <span data-ttu-id="769ba-179">Dadurch kann das System Stift-oder toucheingaben, die in vergrößertem Bildschirminhalt eingegeben werden, an das richtige Benutzeroberflächen Element auf dem Bildschirm übergeben.</span><span class="sxs-lookup"><span data-stu-id="769ba-179">This enables the system to pass pen or touch input that is entered in magnified screen content, to the correct UI element on the screen.</span></span>

> [!Note]  
> <span data-ttu-id="769ba-180">Der Aufrufprozess muss über UIAccess-Berechtigungen verfügen, um die Eingabe Transformation festzulegen.</span><span class="sxs-lookup"><span data-stu-id="769ba-180">The calling process must have UIAccess privileges to set the input transform.</span></span> <span data-ttu-id="769ba-181">Weitere Informationen finden Sie unter [Sicherheitsüberlegungen zur Benutzeroberflächen Automatisierung](../uiauto-securityoverview.md) und [/MANIFESTUAC (bettet UAC-Informationen in Manifest ein)](/cpp/build/reference/manifestuac-embeds-uac-information-in-manifest).</span><span class="sxs-lookup"><span data-stu-id="769ba-181">For more information, see [UI Automation Security Considerations](../uiauto-securityoverview.md) and [/MANIFESTUAC (Embeds UAC information in manifest)](/cpp/build/reference/manifestuac-embeds-uac-information-in-manifest).</span></span>

### <a name="system-cursor"></a><span data-ttu-id="769ba-182">System Cursor</span><span class="sxs-lookup"><span data-stu-id="769ba-182">System Cursor</span></span>

<span data-ttu-id="769ba-183">Mit der Funktion " [**magshowsystemcursor**](/windows/win32/api/Magnification/nf-magnification-magshowsystemcursor) " können Sie den System Cursor anzeigen oder ausblenden.</span><span class="sxs-lookup"><span data-stu-id="769ba-183">The [**MagShowSystemCursor**](/windows/win32/api/Magnification/nf-magnification-magshowsystemcursor) function enables you to show or hide the system cursor.</span></span> <span data-ttu-id="769ba-184">Wenn Sie den System Cursor beim Aktivieren der Vollbildschirm Bildschirmlupe anzeigen, wird der System Cursor immer zusammen mit dem restlichen Bildschirminhalt vergrößert.</span><span class="sxs-lookup"><span data-stu-id="769ba-184">If you show the system cursor when the full-screen magnifier is active, the system cursor is always magnified along with the rest of the screen content.</span></span> <span data-ttu-id="769ba-185">Wenn Sie den System Cursor ausblenden, wenn die Vollbild-Bildschirmlupe aktiv ist, ist der System Cursor überhaupt nicht sichtbar.</span><span class="sxs-lookup"><span data-stu-id="769ba-185">If you hide the system cursor when the full-screen magnifier is active, the system cursor is not visible at all.</span></span>

<span data-ttu-id="769ba-186">Mit dem Bildschirmlupe-Steuerelement zeigt die Funktion " [**magshowsystemcursor**](/windows/win32/api/Magnification/nf-magnification-magshowsystemcursor) " den nicht vergrößerten System Cursor an oder blendet sie aus, hat jedoch keine Auswirkung auf den vergrößerten System Cursor.</span><span class="sxs-lookup"><span data-stu-id="769ba-186">With the magnifier control, the [**MagShowSystemCursor**](/windows/win32/api/Magnification/nf-magnification-magshowsystemcursor) function shows or hides the unmagnified system cursor, but has no effect on the magnified system cursor.</span></span> <span data-ttu-id="769ba-187">Die Sichtbarkeit des vergrößerten System Cursors hängt davon ab, ob das Lupe Steuerelement den [**MS_SHOWMAGNIFIEDCURSOR**](magapi-magnifier-styles.md) Stil aufweist.</span><span class="sxs-lookup"><span data-stu-id="769ba-187">The visibility of the magnified system cursor depends on whether the magnifier control has the [**MS_SHOWMAGNIFIEDCURSOR**](magapi-magnifier-styles.md) style.</span></span> <span data-ttu-id="769ba-188">Wenn dieses Format festgehalten wird, zeigt das Steuerelement für die Bildschirmlupe den vergrößerten System Cursor zusammen mit dem vergrößerten Bildschirminhalt an, wenn der System Cursor in das Quell Rechteck eintritt.</span><span class="sxs-lookup"><span data-stu-id="769ba-188">If it has this style, the magnifier control displays the magnified system cursor, along with the magnified screen content, whenever the system cursor enters the source rectangle.</span></span>

## <a name="initializing-the-magnifier-run-time-library"></a><span data-ttu-id="769ba-189">Initialisieren der Lauf Zeit Bibliothek für die Bildschirmlupe</span><span class="sxs-lookup"><span data-stu-id="769ba-189">Initializing the Magnifier Run-time Library</span></span>

<span data-ttu-id="769ba-190">Bevor Sie beliebige andere Funktionen der Bildschirmlupe-API aufrufen können, müssen Sie die Bildschirm Lauf Zeit Objekte durch Aufrufen der Funktion " [**maginitialize**](/windows/win32/api/Magnification/nf-magnification-maginitialize) " erstellen und initialisieren.</span><span class="sxs-lookup"><span data-stu-id="769ba-190">Before you can call any other magnifier API functions, you must create and initialize the magnifier run-time objects by calling the [**MagInitialize**](/windows/win32/api/Magnification/nf-magnification-maginitialize) function.</span></span> <span data-ttu-id="769ba-191">Wenn Sie die Bildschirmlupe abgeschlossen haben, müssen Sie die Funktion " [**maguninitialize**](/windows/win32/api/Magnification/nf-magnification-maguninitialize) " verwenden, um die Bildschirm Lauf Zeit Objekte zu zerstören und die zugeordneten Systemressourcen freizugeben.</span><span class="sxs-lookup"><span data-stu-id="769ba-191">Similarly, after you finish using the magnifier API, call the [**MagUninitialize**](/windows/win32/api/Magnification/nf-magnification-maguninitialize) function to destroy the magnifier run-time objects and free the associated system resources.</span></span>

## <a name="using-the-full-screen-magnifier"></a><span data-ttu-id="769ba-192">Verwenden der Full-Screen Bildschirmlupe</span><span class="sxs-lookup"><span data-stu-id="769ba-192">Using the Full-Screen Magnifier</span></span>

<span data-ttu-id="769ba-193">Um die Vollbild-Bildschirmlupe zu verwenden, müssen Sie die Funktion [**magsetfullscreentransform**](/windows/win32/api/Magnification/nf-magnification-magsetfullscreentransform) aufrufen.</span><span class="sxs-lookup"><span data-stu-id="769ba-193">To use the full-screen magnifier, call the [**MagSetFullscreenTransform**](/windows/win32/api/Magnification/nf-magnification-magsetfullscreentransform) function.</span></span> <span data-ttu-id="769ba-194">Der *maglevel* -Parameter gibt den Vergrößerungsfaktor an.</span><span class="sxs-lookup"><span data-stu-id="769ba-194">The *magLevel* parameter specifies the magnification factor.</span></span> <span data-ttu-id="769ba-195">Mit den Parametern *xoffset* und *yoffset* wird angegeben, wie der Bildschirm mit vergrößertem Bildschirm relativ zum Bildschirm positioniert wird.</span><span class="sxs-lookup"><span data-stu-id="769ba-195">The *xOffset* and *yOffset* parameters specify how the magnified screen content is positioned relative to the screen.</span></span>

<span data-ttu-id="769ba-196">Wenn der Bildschirminhalt vergrößert wird, wird er größer als der Bildschirm.</span><span class="sxs-lookup"><span data-stu-id="769ba-196">When the screen content is magnified, it becomes larger than the screen itself.</span></span> <span data-ttu-id="769ba-197">Ein Teil des Inhalts erstreckt sich über die Ränder des Bildschirms hinaus und ist für den Benutzer unsichtbar.</span><span class="sxs-lookup"><span data-stu-id="769ba-197">Some portion of the content extends beyond the edges of the screen and becomes invisible to the user.</span></span> <span data-ttu-id="769ba-198">Mit den Parametern *xoffset* und *yoffset* der Funktion [**magsetfullscreentransform**](/windows/win32/api/Magnification/nf-magnification-magsetfullscreentransform) wird festgelegt, welcher Teil des vergrößerten Bildschirm Inhalts auf dem Bildschirm angezeigt wird.</span><span class="sxs-lookup"><span data-stu-id="769ba-198">The *xOffset* and *yOffset* parameters of the [**MagSetFullscreenTransform**](/windows/win32/api/Magnification/nf-magnification-magsetfullscreentransform) function determine which portion of the magnified screen content appears on the screen.</span></span> <span data-ttu-id="769ba-199">Die Parameter geben die Koordinaten eines Punkts in den Bildschirm Inhalten ohne Vergrößerung an.</span><span class="sxs-lookup"><span data-stu-id="769ba-199">Together, the parameters specify the coordinates of a point in the unmagnified screen content.</span></span> <span data-ttu-id="769ba-200">Wenn der Inhalt vergrößert wird, wird er mit dem angegebenen Punkt in der oberen linken Ecke des Bildschirms positioniert.</span><span class="sxs-lookup"><span data-stu-id="769ba-200">When the content is magnified, it is positioned with the specified point at the upper-left corner of the screen.</span></span>

<span data-ttu-id="769ba-201">Im folgenden Beispiel wird der Vergrößerungsfaktor für die Vollbild-Bildschirmlupe festgelegt, und der Mittelpunkt der vergrößerten Bildschirminhalte wird in der Mitte des Bildschirms platziert.</span><span class="sxs-lookup"><span data-stu-id="769ba-201">The following example sets the magnification factor for the full-screen magnifier and places the center of the magnified screen content at the center of the screen.</span></span>

```C++
BOOL SetZoom(float magnificationFactor)
{
    // A magnification factor less than 1.0 is not valid.
    if (magnificationFactor < 1.0)
    {
        return FALSE;
    }

    // Calculate offsets such that the center of the magnified screen content 
    // is at the center of the screen. The offsets are relative to the 
    // unmagnified screen content.
    int xDlg = (int)((float)GetSystemMetrics(
            SM_CXSCREEN) * (1.0 - (1.0 / magnificationFactor)) / 2.0);
    int yDlg = (int)((float)GetSystemMetrics(
            SM_CYSCREEN) * (1.0 - (1.0 / magnificationFactor)) / 2.0);

    return MagSetFullscreenTransform(magnificationFactor, xDlg, yDlg);
}
```

<span data-ttu-id="769ba-202">Verwenden Sie die Funktion " [**magsetfullscreencoloreffect**](/windows/win32/api/Magnification/nf-magnification-magsetfullscreencoloreffect) ", um Farbeffekte auf den voll Bildinhalt anzuwenden, indem Sie eine Anwendungs definierte Farb Transformationsmatrix festlegen.</span><span class="sxs-lookup"><span data-stu-id="769ba-202">Use the [**MagSetFullscreenColorEffect**](/windows/win32/api/Magnification/nf-magnification-magsetfullscreencoloreffect) function to apply color effects to the full-screen content by setting an application-defined color transformation matrix.</span></span> <span data-ttu-id="769ba-203">Im folgenden Beispiel wird z. b. eine Farb Transformationsmatrix festgelegt, die Farben in Graustufen konvertiert.</span><span class="sxs-lookup"><span data-stu-id="769ba-203">For example, the following example sets a color transformation matrix that converts colors to grayscale.</span></span>

```C++
// Initialize color transformation matrices used to apply grayscale and to 
// restore the original screen color.
MAGCOLOREFFECT g_MagEffectGrayscale = {0.3f,  0.3f,  0.3f,  0.0f,  0.0f,
                                       0.6f,  0.6f,  0.6f,  0.0f,  0.0f,
                                       0.1f,  0.1f,  0.1f,  0.0f,  0.0f,
                                       0.0f,  0.0f,  0.0f,  1.0f,  0.0f,
                                       0.0f,  0.0f,  0.0f,  0.0f,  1.0f};

MAGCOLOREFFECT g_MagEffectIdentity = {1.0f,  0.0f,  0.0f,  0.0f,  0.0f,
                                      0.0f,  1.0f,  0.0f,  0.0f,  0.0f,
                                      0.0f,  0.0f,  1.0f,  0.0f,  0.0f,
                                      0.0f,  0.0f,  0.0f,  1.0f,  0.0f,
                                      0.0f,  0.0f,  0.0f,  0.0f,  1.0f};

BOOL SetColorGrayscale(__in BOOL fGrayscaleOn)
{
    // Apply the color matrix required to either apply grayscale to the screen 
    // colors or to show the regular colors.
    PMAGCOLOREFFECT pEffect = 
                (fGrayscaleOn ? &amp;g_MagEffectGrayscale : &amp;g_MagEffectIdentity);

    return MagSetFullscreenColorEffect(pEffect);
}
```

<span data-ttu-id="769ba-204">Sie können den aktuellen Vergrößerungsfaktor und die Offset Werte abrufen, indem Sie die [**maggetfullscreentransform**](/windows/win32/api/Magnification/nf-magnification-maggetfullscreentransform) -Funktion aufrufen.</span><span class="sxs-lookup"><span data-stu-id="769ba-204">You can retrieve the current magnification factor and offset values by calling the [**MagGetFullscreenTransform**](/windows/win32/api/Magnification/nf-magnification-maggetfullscreentransform) function.</span></span> <span data-ttu-id="769ba-205">Sie können die aktuelle Farb Transformationsmatrix abrufen, indem Sie die [**maggetfullscreencoloreffect**](/windows/win32/api/Magnification/nf-magnification-maggetfullscreencoloreffect) -Funktion aufrufen.</span><span class="sxs-lookup"><span data-stu-id="769ba-205">You can retrieve the current color transformation matrix by calling the [**MagGetFullscreenColorEffect**](/windows/win32/api/Magnification/nf-magnification-maggetfullscreencoloreffect) function.</span></span>

## <a name="using-the-magnifier-control"></a><span data-ttu-id="769ba-206">Verwenden des Vergrößerungs Steuer Elements</span><span class="sxs-lookup"><span data-stu-id="769ba-206">Using the Magnifier Control</span></span>

<span data-ttu-id="769ba-207">Das Lupe Steuerelement vergrößert den Inhalt eines bestimmten Bereichs des Bildschirms und zeigt den Inhalt in einem Fenster an.</span><span class="sxs-lookup"><span data-stu-id="769ba-207">The magnifier control magnifies the content of a particular area of the screen and displays the content in a window.</span></span> <span data-ttu-id="769ba-208">In diesem Abschnitt wird beschrieben, wie Sie das Bildschirmlupe-Steuerelement verwenden.</span><span class="sxs-lookup"><span data-stu-id="769ba-208">This section describes how to use the magnifier control.</span></span> <span data-ttu-id="769ba-209">Sie enthält die folgenden Teile:</span><span class="sxs-lookup"><span data-stu-id="769ba-209">It contains the following parts:</span></span>

- [<span data-ttu-id="769ba-210">Erstellen des Vergrößerungs Steuer Elements</span><span class="sxs-lookup"><span data-stu-id="769ba-210">Creating the Magnifier Control</span></span>](#creating-the-magnifier-control)
- [<span data-ttu-id="769ba-211">Initialisieren des Steuerelements</span><span class="sxs-lookup"><span data-stu-id="769ba-211">Initializing the Control</span></span>](#initializing-the-control)
- [<span data-ttu-id="769ba-212">Festlegen des Quell Rechtecks</span><span class="sxs-lookup"><span data-stu-id="769ba-212">Setting the Source Rectangle</span></span>](#setting-the-source-rectangle)
- [<span data-ttu-id="769ba-213">Anwenden von Farbeffekten</span><span class="sxs-lookup"><span data-stu-id="769ba-213">Applying Color Effects</span></span>](#applying-color-effects)
- [<span data-ttu-id="769ba-214">Selektive Vergrößerung</span><span class="sxs-lookup"><span data-stu-id="769ba-214">Selective Magnification</span></span>](#selective-magnification)

### <a name="creating-the-magnifier-control"></a><span data-ttu-id="769ba-215">Erstellen des Vergrößerungs Steuer Elements</span><span class="sxs-lookup"><span data-stu-id="769ba-215">Creating the Magnifier Control</span></span>

<span data-ttu-id="769ba-216">Das Vergrößerungs Steuerelement muss in einem Fenster gehostet werden, das mit dem [**WS_EX_LAYERED**](../../winmsg/extended-window-styles.md) erweiterten Stil erstellt wurde.</span><span class="sxs-lookup"><span data-stu-id="769ba-216">The magnifier control must be hosted in a window created with the [**WS_EX_LAYERED**](../../winmsg/extended-window-styles.md) extended style.</span></span> <span data-ttu-id="769ba-217">Nachdem Sie das Host Fenster erstellt haben, können Sie [**SetLayeredWindowAttributes**](/windows/win32/api/winuser/nf-winuser-setlayeredwindowattributes) aufrufen, um die Deckkraft des Host Fensters festzulegen.</span><span class="sxs-lookup"><span data-stu-id="769ba-217">After creating the host window, call [**SetLayeredWindowAttributes**](/windows/win32/api/winuser/nf-winuser-setlayeredwindowattributes) to set the opacity of the host window.</span></span> <span data-ttu-id="769ba-218">Das Host Fenster wird in der Regel auf vollständige Deckkraft festgelegt, um zu verhindern, dass der zugrunde liegende Bildschirminhalt angezeigt wird.</span><span class="sxs-lookup"><span data-stu-id="769ba-218">The host window is typically set to full opacity to prevent the underlying screen content from showing though.</span></span> <span data-ttu-id="769ba-219">Im folgenden Beispiel wird gezeigt, wie das Host Fenster auf vollständige Deckkraft festgelegt wird:</span><span class="sxs-lookup"><span data-stu-id="769ba-219">The following example shows how to set the host window to full opacity:</span></span>

```C++
SetLayeredWindowAttributes(hwndHost, NULL, 255, LWA_ALPHA);
```

<span data-ttu-id="769ba-220">Wenn Sie den [**WS_EX_TRANSPARENT**](../../winmsg/extended-window-styles.md) Stil auf das Host Fenster anwenden, werden Mausklicks an die Position des Mauszeigers zurückgegeben, die sich hinter dem Host Fenster befindet.</span><span class="sxs-lookup"><span data-stu-id="769ba-220">If you apply the [**WS_EX_TRANSPARENT**](../../winmsg/extended-window-styles.md) style to the host window, mouse clicks are passed to whatever object is behind the host window at the location of the mouse cursor.</span></span> <span data-ttu-id="769ba-221">Beachten Sie, dass der Benutzer nicht in der Lage ist, das Vergrößerungs Fenster mit der Maus zu verschieben oder die Größe der Größe zu ändern, da das Host Fenster keine Mausklicks verarbeitet.</span><span class="sxs-lookup"><span data-stu-id="769ba-221">Be aware that, because the host window does not process mouse clicks, the user will not be able to move or resize the magnification window by using the mouse.</span></span>

<span data-ttu-id="769ba-222">Die Fenster Klasse des Fenster Fensters der Bildschirmlupe muss **WC_MAGNIFIER** werden.</span><span class="sxs-lookup"><span data-stu-id="769ba-222">The window class of the magnifier control window must be **WC_MAGNIFIER**.</span></span> <span data-ttu-id="769ba-223">Wenn Sie die [**MS_SHOWMAGNIFIEDCURSOR**](magapi-magnifier-styles.md) Formatvorlage anwenden, enthält das Vergrößerungs Steuerelement den System Cursor in den vergrößerten Bildschirminhalt, und der Cursor wird zusammen mit den Bildschirm Inhalten vergrößert.</span><span class="sxs-lookup"><span data-stu-id="769ba-223">If you apply the [**MS_SHOWMAGNIFIEDCURSOR**](magapi-magnifier-styles.md) style, the magnifier control includes the system cursor in the magnified screen contents, and the cursor is magnified along with the screen contents.</span></span>

<span data-ttu-id="769ba-224">Nachdem Sie das Vergrößerungs Steuerelement erstellt haben, behalten Sie das Fenster Handle bei, damit Sie es an andere Funktionen übergeben können.</span><span class="sxs-lookup"><span data-stu-id="769ba-224">After you create the magnifier control, keep the window handle so that you can pass it to other functions.</span></span>

<span data-ttu-id="769ba-225">Im folgenden Beispiel wird gezeigt, wie das Bildschirm Steuerelement erstellt wird.</span><span class="sxs-lookup"><span data-stu-id="769ba-225">The following example shows how to create the magnifier control.</span></span>

```C++
// Description: 
//   Registers the host window class, creates the host window, sets the layered
//   window attributes, and creates the magnifier control. 
// Parameters:
//   hInstance - Instance handle of the application.
// Variables:
//   HostWndProc - Window procedure of the host window.
//   WindowClassName - Name of the window class.
//   WindowTitle - Title of the host window.
// Constants and global variables:
//   hwndHost - Handle of the host window.
//   hwndMag - Handle of the magnifier window.
//   LENS_WIDTH - Width of the magnifier window.
//   LENS_HEIGHT - Height of the magnifier window.
// 
BOOL CreateMagnifier(HINSTANCE hInstance)
{
   // Register the host window class.
    WNDCLASSEX wcex = {};
    wcex.cbSize = sizeof(WNDCLASSEX); 
    wcex.style          = 0;
    wcex.lpfnWndProc    = HostWndProc;
    wcex.hInstance      = hInstance;
    wcex.hCursor        = LoadCursor(NULL, IDC_ARROW);
    wcex.hbrBackground  = (HBRUSH)(1 + COLOR_BTNFACE);
    wcex.lpszClassName  = WindowClassName;
    
    if (RegisterClassEx(&amp;wcex) == 0)
        return FALSE;

    // Create the host window. 
    hwndHost = CreateWindowEx(WS_EX_TOPMOST | WS_EX_LAYERED | WS_EX_TRANSPARENT, 
        WindowClassName, WindowTitle, 
        WS_CLIPCHILDREN,
        0, 0, 0, 0,
        NULL, NULL, hInstance, NULL);
    if (!hwndHost)
    {
        return FALSE;
    }

    // Make the window opaque.
    SetLayeredWindowAttributes(hwndHost, 0, 255, LWA_ALPHA);

    // Create a magnifier control that fills the client area.
    hwndMag = CreateWindow(WC_MAGNIFIER, TEXT("MagnifierWindow"), 
        WS_CHILD | MS_SHOWMAGNIFIEDCURSOR | WS_VISIBLE,
        0, 0, 
        LENS_WIDTH, 
        LENS_HEIGHT, 
        hwndHost, NULL, hInstance, NULL );
    if (!hwndMag)
    {
        return FALSE;
    }

    return TRUE;
}
```

### <a name="initializing-the-control"></a><span data-ttu-id="769ba-226">Initialisieren des Steuerelements</span><span class="sxs-lookup"><span data-stu-id="769ba-226">Initializing the Control</span></span>

<span data-ttu-id="769ba-227">Nachdem Sie das Steuerelement für die Bildschirmlupe erstellt haben, müssen Sie die Funktion " [**magsetwindowtransform**](/windows/win32/api/Magnification/nf-magnification-magsetwindowtransform) " aufrufen, um den Vergrößerungsfaktor anzugeben.</span><span class="sxs-lookup"><span data-stu-id="769ba-227">After creating the magnifier control, you must call the [**MagSetWindowTransform**](/windows/win32/api/Magnification/nf-magnification-magsetwindowtransform) function to specify the magnification factor.</span></span> <span data-ttu-id="769ba-228">Das ist einfach eine Frage der Angabe einer Matrix von</span><span class="sxs-lookup"><span data-stu-id="769ba-228">This is simply a matter of specifying a matrix of</span></span>

<span data-ttu-id="769ba-229">(*n*, 0,0, 0,0)</span><span class="sxs-lookup"><span data-stu-id="769ba-229">(*n*, 0.0, 0.0)</span></span>

<span data-ttu-id="769ba-230">(0,0, *n*, 0,0)</span><span class="sxs-lookup"><span data-stu-id="769ba-230">(0.0, *n*, 0.0)</span></span>

<span data-ttu-id="769ba-231">(0,0, 0,0, 1,0)</span><span class="sxs-lookup"><span data-stu-id="769ba-231">(0.0, 0.0, 1.0)</span></span>

<span data-ttu-id="769ba-232">wobei *n* der Vergrößerungsfaktor ist.</span><span class="sxs-lookup"><span data-stu-id="769ba-232">where *n* is the magnification factor.</span></span>

<span data-ttu-id="769ba-233">Im folgenden Beispiel wird gezeigt, wie der Vergrößerungsfaktor für das Lupe Steuerelement festgelegt wird.</span><span class="sxs-lookup"><span data-stu-id="769ba-233">The following example shows how to set the magnification factor for the magnifier control.</span></span>

```C++
// Description:
//   Sets the magnification factor for a magnifier control.
// Parameters:
//   hwndMag - Handle of the magnifier control.
//   magFactor - New magnification factor.
//
BOOL SetMagnificationFactor(HWND hwndMag, float magFactor)
{
    MAGTRANSFORM matrix;
    memset(&amp;matrix, 0, sizeof(matrix));
    matrix.v[0][0] = magFactor;
    matrix.v[1][1] = magFactor;
    matrix.v[2][2] = 1.0f;

    return MagSetWindowTransform(hwndMag, &amp;matrix);  
}
```

### <a name="setting-the-source-rectangle"></a><span data-ttu-id="769ba-234">Festlegen des Quell Rechtecks</span><span class="sxs-lookup"><span data-stu-id="769ba-234">Setting the Source Rectangle</span></span>

<span data-ttu-id="769ba-235">Wenn der Benutzer den Mauszeiger auf dem Bildschirm bewegt, ruft die Anwendung die Funktion " [**magsetwindowsource**](/windows/win32/api/Magnification/nf-magnification-magsetwindowsource) " auf, um den Teil des zugrunde liegenden Bildschirms anzugeben, der vergrößert werden soll.</span><span class="sxs-lookup"><span data-stu-id="769ba-235">As the user moves the mouse cursor around the screen, your application calls the [**MagSetWindowSource**](/windows/win32/api/Magnification/nf-magnification-magsetwindowsource) function to specify the part of the underlying screen that is to be magnified.</span></span>

<span data-ttu-id="769ba-236">Die folgende Beispiel Funktion berechnet die Position und die Dimensionen des Quell Rechtecks (basierend auf der Mausposition und den Abmessungen des Vergrößerungs Fensters dividiert durch den Vergrößerungsfaktor) und legt das Quell Rechteck entsprechend fest.</span><span class="sxs-lookup"><span data-stu-id="769ba-236">The following example function calculates the position and dimensions of the source rectangle (based on the mouse position and the dimensions of the magnifier window divided by the magnification factor) and sets the source rectangle accordingly.</span></span> <span data-ttu-id="769ba-237">Die-Funktion zentriert auch den Client Bereich des Host Fensters an der Mausposition.</span><span class="sxs-lookup"><span data-stu-id="769ba-237">The function also centers the client area of the host window at the mouse position.</span></span> <span data-ttu-id="769ba-238">Diese Funktion wird in Intervallen aufgerufen, um das Vergrößerungs Fenster zu aktualisieren.</span><span class="sxs-lookup"><span data-stu-id="769ba-238">This function would be called at intervals to update the magnification window.</span></span>

```C++
// Description: 
//   Called by a timer to update the contents of the magnifier window and to set
//   the position of the host window. 
// Constants and global variables:
//   hwndHost - Handle of the host window.
//   hwndMag - Handle of the magnifier window.
//   LENS_WIDTH - Width of the magnifier window.
//   LENS_HEIGHT - Height of the magnifier window.
//   MAGFACTOR - The magnification factor.
//
void CALLBACK UpdateMagWindow(HWND /*hwnd*/, UINT /*uMsg*/, 
        UINT_PTR /*idEvent*/, DWORD /*dwTime*/)
{
    // Get the mouse coordinates.
    POINT mousePoint;
    GetCursorPos(&amp;mousePoint);

    // Calculate a source rectangle that is centered at the mouse coordinates. 
    // Size the rectangle so that it fits into the magnifier window (the lens).
    RECT sourceRect;
    int borderWidth = GetSystemMetrics(SM_CXFIXEDFRAME);
    int captionHeight = GetSystemMetrics(SM_CYCAPTION);
    sourceRect.left = (mousePoint.x - (int)((LENS_WIDTH / 2) / MAGFACTOR)) + 
             (int)(borderWidth / MAGFACTOR);
    sourceRect.top = (mousePoint.y - (int)((LENS_HEIGHT / 2) / MAGFACTOR)) + 
             (int)(captionHeight / MAGFACTOR) + (int)(borderWidth / MAGFACTOR); 
    sourceRect.right = LENS_WIDTH;
    sourceRect.bottom = LENS_HEIGHT;

    // Pass the source rectangle to the magnifier control.
    MagSetWindowSource(hwndMag, sourceRect);

    // Move the host window so that the origin of the client area lines up
    // with the origin of the magnified source rectangle.
    MoveWindow(hwndHost, 
        (mousePoint.x - LENS_WIDTH / 2), 
        (mousePoint.y - LENS_HEIGHT / 2), 
        LENS_WIDTH, 
        LENS_HEIGHT,
        FALSE);

    // Force the magnifier control to redraw itself.
    InvalidateRect(hwndMag, NULL, TRUE);

    return;
}
```

### <a name="applying-color-effects"></a><span data-ttu-id="769ba-239">Anwenden von Farbeffekten</span><span class="sxs-lookup"><span data-stu-id="769ba-239">Applying Color Effects</span></span>

<span data-ttu-id="769ba-240">Ein Vergrößerungs Steuerelement mit dem [**MS_INVERTCOLORS**](magapi-magnifier-styles.md) -Stil wendet eine integrierte Farb Transformationsmatrix an, die die Farben der vergrößerten Bildschirminhalte umkehrt.</span><span class="sxs-lookup"><span data-stu-id="769ba-240">A magnifier control that has the [**MS_INVERTCOLORS**](magapi-magnifier-styles.md) style applies a built-in color transformation matrix that inverts the colors of the magnified screen content.</span></span> <span data-ttu-id="769ba-241">Die folgende Abbildung zeigt Bildschirminhalt in einem Bildschirm Steuerelement, das den **MS_INVERTCOLORS** Stil hat.</span><span class="sxs-lookup"><span data-stu-id="769ba-241">The following illustration shows screen content in a magnifier control that has the **MS_INVERTCOLORS** style.</span></span>

![Screenshot des vergrößerten Inhalts mit umgekehrten Farben](images/color-inversion.png)

<span data-ttu-id="769ba-243">Mithilfe der Funktion " [**magsetcoloreffect**](/windows/win32/api/Magnification/nf-magnification-magsetcoloreffect) " können Sie andere Farbeffekte durch Festlegen einer Anwendungs definierten Farb Transformationsmatrix anwenden.</span><span class="sxs-lookup"><span data-stu-id="769ba-243">The [**MagSetColorEffect**](/windows/win32/api/Magnification/nf-magnification-magsetcoloreffect) function enables you to apply other color effects by setting an application-defined color transformation matrix.</span></span> <span data-ttu-id="769ba-244">Beispielsweise wird mit der folgenden Funktion eine Farb Transformationsmatrix festgelegt, die Farben in Graustufen konvertiert.</span><span class="sxs-lookup"><span data-stu-id="769ba-244">For example, the following function sets a color transformation matrix that converts colors to grayscale.</span></span>


```C++
// Description:
//   Converts the colors displayed in the magnifier window to grayscale, or
//   returns the colors to normal.
// Parameters:
//   hwndMag - Handle of the magnifier control.
//   fInvert - TRUE to convert to grayscale, or FALSE for normal colors.
//
BOOL ConvertToGrayscale(HWND hwndMag, BOOL fConvert)
{
    // Convert the screen colors in the magnifier window.
    if (fConvert)
    {
        MAGCOLOREFFECT magEffectGrayscale = 
            {{ // MagEffectGrayscale
                {  0.3f,  0.3f,  0.3f,  0.0f,  0.0f },
                {  0.6f,  0.6f,  0.6f,  0.0f,  0.0f },
                {  0.1f,  0.1f,  0.1f,  0.0f,  0.0f },
                {  0.0f,  0.0f,  0.0f,  1.0f,  0.0f },
                {  0.0f,  0.0f,  0.0f,  0.0f,  1.0f } 
            }};

        return MagSetColorEffect(hwndMag, &amp;magEffectGrayscale);
    }

    // Return the colors to normal.
    else
    {
        return MagSetColorEffect(hwndMag, NULL);
    }
}
```

<span data-ttu-id="769ba-245">Weitere Informationen zur Funktionsweise von Farb Transformationen finden [Sie unter Verwenden einer Farb Matrix zum Transformieren einer einzelnen Farbe](../../gdiplus/-gdiplus-using-a-color-matrix-to-transform-a-single-color-use.md) in der GDI+-Dokumentation.</span><span class="sxs-lookup"><span data-stu-id="769ba-245">For more information about how color transformations work, see [Using a Color Matrix to Transform a Single Color](../../gdiplus/-gdiplus-using-a-color-matrix-to-transform-a-single-color-use.md) in the GDI+ documentation.</span></span>

### <a name="selective-magnification"></a><span data-ttu-id="769ba-246">Selektive Vergrößerung</span><span class="sxs-lookup"><span data-stu-id="769ba-246">Selective Magnification</span></span>

<span data-ttu-id="769ba-247">Standardmäßig wird die Vergrößerung auf alle Fenster außer dem Vergrößerungs Fenster selbst angewendet.</span><span class="sxs-lookup"><span data-stu-id="769ba-247">By default, magnification is applied to all windows other than the magnification window itself.</span></span> <span data-ttu-id="769ba-248">Um anzugeben, welche Fenster vergrößert werden sollen, nennen Sie die Funktion " [**magsetwindowfilterlist**](/windows/win32/api/Magnification/nf-magnification-magsetwindowfilterlist) ".</span><span class="sxs-lookup"><span data-stu-id="769ba-248">To specify which windows are to be magnified, call the [**MagSetWindowFilterList**](/windows/win32/api/Magnification/nf-magnification-magsetwindowfilterlist) function.</span></span> <span data-ttu-id="769ba-249">Diese Methode übernimmt entweder eine Liste von Fenstern, die vergrößert werden soll, oder eine Liste von Fenstern, die von der Vergrößerung ausgeschlossen werden sollen.</span><span class="sxs-lookup"><span data-stu-id="769ba-249">This method takes either a list of windows to magnify, or a list of windows to exclude from magnification.</span></span>

## <a name="related-topics"></a><span data-ttu-id="769ba-250">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="769ba-250">Related topics</span></span>

[<span data-ttu-id="769ba-251">API zur Vergrößerung</span><span class="sxs-lookup"><span data-stu-id="769ba-251">Magnification API</span></span>](entry-magapi-sdk.md)