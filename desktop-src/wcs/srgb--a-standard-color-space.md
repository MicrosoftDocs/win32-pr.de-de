---
title: sRGB Standardfarbraum
description: Aufgrund von Überlegungen zur Internet Bandbreite hat Hewlett-Packard und Microsoft die Annahme eines standardmäßigen vordefinierten Farbraum vorgeschlagen, der als sRGB (IEC 61966-2-1) bezeichnet wird, damit eine exakte Farbzuordnung mit sehr geringem Daten Aufwand ermöglicht wird.
ms.assetid: b9017702-7dca-4d79-bed0-936f97cb6109
keywords:
- Windows Color System (WCS), sRGB-Farbraum
- WCS (Windows Color System), sRGB-Farbraum
- Bild Farbverwaltung, sRGB-Farbraum
- Farbverwaltung, sRGB-Farbraum
- Farben, sRGB-Farbraum
- sRGB-Farbraum
- Farbbereiche, sRGB
ms.localizationpriority: high
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ed3167e44f149982a809826bcb9b64b3ec6e3c24
ms.sourcegitcommit: da13d459791d115df883fa4dd348931d0902c2cc
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/30/2021
ms.locfileid: "106349749"
---
# <a name="srgb-a-standard-color-space"></a><span data-ttu-id="d3240-110">sRGB: ein Standard Farbraum</span><span class="sxs-lookup"><span data-stu-id="d3240-110">sRGB: A Standard Color Space</span></span>

<span data-ttu-id="d3240-111">Aufgrund von Überlegungen zur Internet Bandbreite hat Hewlett-Packard und Microsoft die Annahme eines standardmäßigen vordefinierten [Farbraum](c.md) vorgeschlagen, der als *sRGB* (IEC 61966-2-1) bezeichnet wird, damit eine exakte [Farbzuordnung](c.md) mit sehr geringem Daten Aufwand ermöglicht wird.</span><span class="sxs-lookup"><span data-stu-id="d3240-111">As a result of Internet bandwidth considerations, Hewlett-Packard and Microsoft have proposed the adoption of a standard predefined [color space](c.md) known as *sRGB* (IEC 61966-2-1), so as to allow accurate [color mapping](c.md) with very little data overhead.</span></span>

<span data-ttu-id="d3240-112">Eine Hilfedatei Version eines Whitepaper, in dem die technischen Details von sRGB (sRGB. hlp) erörtert werden, finden Sie im \\ Hilfe Ordner der WCS 1,0-Programmier Referenz.</span><span class="sxs-lookup"><span data-stu-id="d3240-112">A help-file version of a white paper discussing the technical details of sRGB, sRGB.hlp, is available in the \\Help folder of the WCS 1.0 Programmer's Reference.</span></span>

<span data-ttu-id="d3240-113">Unterschiedliche Dateiformate können ein Flag verwenden oder hinzufügen, um anzugeben, dass sich das Image im sRGB-Farbraum befindet.</span><span class="sxs-lookup"><span data-stu-id="d3240-113">Different file formats may use or add a flag to specify that the image is in sRGB color space.</span></span> <span data-ttu-id="d3240-114">Im Windows-DIB-Format (geräteunabhängige Bitmap) wird durch Festlegen des **bV5CSType** -Members der [**BITMAPV5HEADER**](using-structures-in-wcs-1-0.md) -Struktur auf **LCS \_ sRGB** festgelegt, dass die DIB-Farben den sRGB-Farbraum aufweisen.</span><span class="sxs-lookup"><span data-stu-id="d3240-114">In the Windows device-independent bitmap (DIB) format, setting the **bV5CSType** member of the [**BITMAPV5HEADER**](using-structures-in-wcs-1-0.md) structure to **LCS\_sRGB** specifies that the DIB colors are in the sRGB color space.</span></span>

<span data-ttu-id="d3240-115">WCS 1,0 bietet native Unterstützung für sRGB.</span><span class="sxs-lookup"><span data-stu-id="d3240-115">WCS 1.0 provides native support for sRGB.</span></span> <span data-ttu-id="d3240-116">Es gibt zwei Möglichkeiten, WCS 1,0 zum Rendern eines Bilds zu verwenden, das im sRGB-Farbraum definiert ist:</span><span class="sxs-lookup"><span data-stu-id="d3240-116">There are two ways to use WCS 1.0 for rendering an image defined in the sRGB color space:</span></span>

<span data-ttu-id="d3240-117">**So Rendering Sie ein Bild innerhalb des Geräte Kontexts**</span><span class="sxs-lookup"><span data-stu-id="d3240-117">**To render an image inside the device context**</span></span>

1.  <span data-ttu-id="d3240-118">Erstellen Sie einen Gerätekontext (DC) auf dem Anzeigegerät.</span><span class="sxs-lookup"><span data-stu-id="d3240-118">Create a device context (DC) on the display device.</span></span>
2.  <span data-ttu-id="d3240-119">Legen Sie die Farbverwaltung mithilfe der [**SetICMMode**](/windows/desktop/api/Wingdi/nf-wingdi-seticmmode) -Funktion fest.</span><span class="sxs-lookup"><span data-stu-id="d3240-119">Set color management using the [**SetICMMode**](/windows/desktop/api/Wingdi/nf-wingdi-seticmmode) function.</span></span>
3.  <span data-ttu-id="d3240-120">Verwenden Sie die Funktion [**SetDIBitsToDevice**](/windows/win32/api/wingdi/nf-wingdi-setdibitstodevice) , um das DIB in den DC zu übertragen.</span><span class="sxs-lookup"><span data-stu-id="d3240-120">Use the [**SetDIBitsToDevice**](/windows/win32/api/wingdi/nf-wingdi-setdibitstodevice) function to transfer the DIB into the DC.</span></span> <span data-ttu-id="d3240-121">Solange der **bV5CSMType** -Member der Disb [**BITMAPV5HEADER**](using-structures-in-wcs-1-0.md) -Struktur auf **LCS \_ sRGB** festgelegt ist, führt das System die entsprechende Farbverwaltung aus.</span><span class="sxs-lookup"><span data-stu-id="d3240-121">As long as the **bV5CSMType** member of the DIBs [**BITMAPV5HEADER**](using-structures-in-wcs-1-0.md) structure is set to **LCS\_sRGB**, the system will perform the appropriate color management.</span></span>

<span data-ttu-id="d3240-122">**So Rendering Sie ein Bild außerhalb des Geräte Kontexts**</span><span class="sxs-lookup"><span data-stu-id="d3240-122">**To render an image outside the device context**</span></span>

1.  <span data-ttu-id="d3240-123">Erstellen Sie eine Transformation mithilfe von " [**kreatecolortransformw**](/windows/win32/api/icm/nf-icm-createcolortransformw)".</span><span class="sxs-lookup"><span data-stu-id="d3240-123">Create a transform using [**CreateColorTransformW**](/windows/win32/api/icm/nf-icm-createcolortransformw).</span></span> <span data-ttu-id="d3240-124">Der **lcscstype** -Member der [**logcolorspace**](/windows/desktop/api/Wingdi/ns-wingdi-taglogcolorspacea) -Struktur, auf die der *plogcolorspace* -Parameter verweist, sollte auf **LCS \_ sRGB** festgelegt werden.</span><span class="sxs-lookup"><span data-stu-id="d3240-124">The **lcsCSType** member of the [**LOGCOLORSPACE**](/windows/desktop/api/Wingdi/ns-wingdi-taglogcolorspacea) structure pointed to by the *pLogColorSpace* parameter should be set to **LCS\_sRGB**.</span></span> <span data-ttu-id="d3240-125">Der *hdestprofile* -Parameter gibt den Farbraum des Anzeige Geräts an.</span><span class="sxs-lookup"><span data-stu-id="d3240-125">The *hDestProfile* parameter indicates the display device's color space.</span></span>
2.  <span data-ttu-id="d3240-126">Verwenden Sie die erstellte Farb Transformation, um die Farbe der Abbildung zuzuordnen, bevor Sie auf dem Gerät angezeigt wird.</span><span class="sxs-lookup"><span data-stu-id="d3240-126">Use the created color transform to color match the image before displaying it on the device.</span></span>

## <a name="wcs-10-defaults-for-input-color-space-and-output-profile"></a><span data-ttu-id="d3240-127">WCS 1,0-Standardwerte für Eingabe Farbraum und Ausgabeprofil</span><span class="sxs-lookup"><span data-stu-id="d3240-127">WCS 1.0 Defaults for Input Color Space and Output Profile</span></span>

<span data-ttu-id="d3240-128">Wenn kein Eingabe Farbraum angegeben ist, verwendet WCS 1,0 standardmäßig den sRGB-Farbraum als Eingabe Farbraum für die [Farbzuordnung](c.md).</span><span class="sxs-lookup"><span data-stu-id="d3240-128">When no input color space is specified, by default WCS 1.0 uses the sRGB color space as the input color space for [color mapping](c.md).</span></span>

<span data-ttu-id="d3240-129">Wenn kein Ausgabeprofil angegeben wird, aber ein Standardgerät angegeben ist, wählt WCS 1,0 ein Standardausgabe Profil aus.</span><span class="sxs-lookup"><span data-stu-id="d3240-129">When no output profile is specified, but a default device is specified, WCS 1.0 selects a default output profile.</span></span> <span data-ttu-id="d3240-130">Wenn dem Standardgerät kein Profil zugeordnet ist, verwendet WCS 1,0 den sRGB-Farbraum als Ausgabeprofil.</span><span class="sxs-lookup"><span data-stu-id="d3240-130">If the default device does not have an associated profile, WCS 1.0 uses the sRGB color space as the output profile.</span></span>

<span data-ttu-id="d3240-131">Die folgende Tabelle zeigt die resultierenden Farb Transformationen, wenn ein Standardgerät nicht verfügbar ist.</span><span class="sxs-lookup"><span data-stu-id="d3240-131">The following table shows the resulting color transforms when a default device is not available.</span></span>



|                                 | <span data-ttu-id="d3240-132">Ausgabeprofil angegeben</span><span class="sxs-lookup"><span data-stu-id="d3240-132">Output Profile Specified</span></span>                              | <span data-ttu-id="d3240-133">Das Ausgabeprofil ist nicht angegeben.</span><span class="sxs-lookup"><span data-stu-id="d3240-133">Output Profile Not Specified</span></span>                             |
|---------------------------------|-------------------------------------------------------|----------------------------------------------------------|
| <span data-ttu-id="d3240-134">Eingegebener Eingabe Farbraum</span><span class="sxs-lookup"><span data-stu-id="d3240-134">Input Color Space Specified</span></span>     | <span data-ttu-id="d3240-135">Die Transformation verwendet die angegebenen Profile.</span><span class="sxs-lookup"><span data-stu-id="d3240-135">Transform uses the specified profiles.</span></span>                | <span data-ttu-id="d3240-136">Transform konvertiert von einem bekannten Eingabe Farbraum in sRGB.</span><span class="sxs-lookup"><span data-stu-id="d3240-136">Transform converts from known input color space to sRGB.</span></span> |
| <span data-ttu-id="d3240-137">Der Eingabe Farbraum ist nicht angegeben.</span><span class="sxs-lookup"><span data-stu-id="d3240-137">Input Color Space Not Specified</span></span> | <span data-ttu-id="d3240-138">Transformation konvertiert von sRGB in ein bekanntes Ausgabeprofil.</span><span class="sxs-lookup"><span data-stu-id="d3240-138">Transform converts from sRGB to known output profile.</span></span> | <span data-ttu-id="d3240-139">Es wird davon ausgegangen, dass die Transformation von sRGB in sRGB erfolgt Es erfolgt nichts.</span><span class="sxs-lookup"><span data-stu-id="d3240-139">Transform from sRGB to sRGB is assumed; nothing is done.</span></span> |



 

## <a name="srgb-and-embedded-profiles"></a><span data-ttu-id="d3240-140">sRGB und eingebettete Profile</span><span class="sxs-lookup"><span data-stu-id="d3240-140">sRGB and Embedded Profiles</span></span>

<span data-ttu-id="d3240-141">Ab ICM, Version 2,0, können Anwendungen, die WCS verwenden, Profile in Bilder einbetten.</span><span class="sxs-lookup"><span data-stu-id="d3240-141">Beginning with ICM version 2.0, applications that utilize WCS can embed profiles in images.</span></span> <span data-ttu-id="d3240-142">Eingebettete Profile unterstützen Benutzer Anwendungen bei der Beibehaltung einer konsistenten Farbdarstellung, auch wenn Bilder über das Internet übertragen werden.</span><span class="sxs-lookup"><span data-stu-id="d3240-142">Embedded profiles assist users' applications in maintaining a consistent color appearance even if images are transmitted across the Internet.</span></span>

<span data-ttu-id="d3240-143">Für Images, die den sRGB-Farbraum verwenden, ist kein eingebettetes Farbprofil erforderlich.</span><span class="sxs-lookup"><span data-stu-id="d3240-143">Images that use the sRGB color space do not need an embedded color profile.</span></span> <span data-ttu-id="d3240-144">Da Sie kein eingebettetes Profil aufweisen, sind sRGB-basierte Images kleiner und leichter über Datenkanäle mit eingeschränkter Bandbreite hinweg übertragbar.</span><span class="sxs-lookup"><span data-stu-id="d3240-144">Because they have no embedded profile, sRGB-based images are smaller and more readily transferable across data channels with limited bandwidth.</span></span>

<span data-ttu-id="d3240-145">Anwendungen sollten das **LCS \_ sRGB** -Flag im Bitmap-Header des Bilds festlegen, um anzugeben, dass das Bild den sRGB-Farbraum verwendet.</span><span class="sxs-lookup"><span data-stu-id="d3240-145">Applications should set the **LCS\_sRGB** flag in the image's bitmap header to indicate that the image uses the sRGB color space.</span></span> <span data-ttu-id="d3240-146">Weitere Informationen finden Sie unter [Windows-Bitmap-Header Strukturen](using-structures-in-wcs-1-0.md) und [**logcolorspace**](/windows/desktop/api/Wingdi/ns-wingdi-taglogcolorspacea).</span><span class="sxs-lookup"><span data-stu-id="d3240-146">For details, see [Windows Bitmap Header Structures](using-structures-in-wcs-1-0.md) and [**LOGCOLORSPACE**](/windows/desktop/api/Wingdi/ns-wingdi-taglogcolorspacea).</span></span>

 

 