---
title: sRGB Standardfarbraum
description: Aufgrund von Überlegungen zur Internetbandbreite haben Hewlett-Packard und Microsoft die Einführung eines vordefinierten Standardfarbraums namens sRGB (IEC 61966-2-1) vorgeschlagen, um eine genaue Farbzuordnung mit sehr geringem Datenaufwand zu ermöglichen.
ms.assetid: b9017702-7dca-4d79-bed0-936f97cb6109
keywords:
- Windows Color System (WCS), sRGB-Farbraum
- WCS (Windows-Farbsystem),sRGB-Farbraum
- Bildfarbverwaltung, sRGB-Farbraum
- Farbverwaltung,sRGB-Farbraum
- Farben, sRGB-Farbraum
- sRGB-Farbraum
- Farbräume, sRGB
ms.localizationpriority: high
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: aa5d1b2d87cdca5424f8393ae47e592718f33985
ms.sourcegitcommit: 099ecdda1e83618b844387405da0db0ebda93a65
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/04/2021
ms.locfileid: "111443641"
---
# <a name="srgb-a-standard-color-space"></a><span data-ttu-id="c3715-110">sRGB: Ein Standardfarbraum</span><span class="sxs-lookup"><span data-stu-id="c3715-110">sRGB: A Standard Color Space</span></span>

<span data-ttu-id="c3715-111">Aufgrund von Überlegungen zur Internetbandbreite haben Hewlett-Packard und Microsoft die Einführung eines vordefinierten [Standardfarbraums](c.md) namens *sRGB* (IEC 61966-2-1) vorgeschlagen, um eine genaue [Farbzuordnung](c.md) mit sehr geringem Datenaufwand zu ermöglichen.</span><span class="sxs-lookup"><span data-stu-id="c3715-111">As a result of Internet bandwidth considerations, Hewlett-Packard and Microsoft have proposed the adoption of a standard predefined [color space](c.md) known as *sRGB* (IEC 61966-2-1), so as to allow accurate [color mapping](c.md) with very little data overhead.</span></span>

<span data-ttu-id="c3715-112">Eine Hilfedateiversion eines Whitepapers, in dem die technischen Details von sRGB, sRGB.hlp, erörtert werden, finden Sie im \\ Hilfeordner der WCS 1.0-Programmierreferenz.</span><span class="sxs-lookup"><span data-stu-id="c3715-112">A help-file version of a white paper discussing the technical details of sRGB, sRGB.hlp, is available in the \\Help folder of the WCS 1.0 Programmer's Reference.</span></span>

<span data-ttu-id="c3715-113">Verschiedene Dateiformate können ein Flag verwenden oder hinzufügen, um anzugeben, dass sich das Bild im sRGB-Farbraum befindet.</span><span class="sxs-lookup"><span data-stu-id="c3715-113">Different file formats may use or add a flag to specify that the image is in sRGB color space.</span></span> <span data-ttu-id="c3715-114">Im Windows-DIB-Format (Device-Independent Bitmap) gibt das Festlegen des **bV5CSType-Elements** der [**BITMAPV5HEADER-Struktur**](using-structures-in-wcs-1-0.md) auf **LCS \_ sRGB** an, dass sich die DIB-Farben im sRGB-Farbraum befinden.</span><span class="sxs-lookup"><span data-stu-id="c3715-114">In the Windows device-independent bitmap (DIB) format, setting the **bV5CSType** member of the [**BITMAPV5HEADER**](using-structures-in-wcs-1-0.md) structure to **LCS\_sRGB** specifies that the DIB colors are in the sRGB color space.</span></span>

<span data-ttu-id="c3715-115">WCS 1.0 bietet native Unterstützung für sRGB.</span><span class="sxs-lookup"><span data-stu-id="c3715-115">WCS 1.0 provides native support for sRGB.</span></span> <span data-ttu-id="c3715-116">Es gibt zwei Möglichkeiten, WCS 1.0 zum Rendern eines im sRGB-Farbraum definierten Bilds zu verwenden:</span><span class="sxs-lookup"><span data-stu-id="c3715-116">There are two ways to use WCS 1.0 for rendering an image defined in the sRGB color space:</span></span>

<span data-ttu-id="c3715-117">**So rendern Sie ein Bild im Gerätekontext**</span><span class="sxs-lookup"><span data-stu-id="c3715-117">**To render an image inside the device context**</span></span>

1.  <span data-ttu-id="c3715-118">Erstellen Sie einen Gerätekontext (DC) auf dem Anzeigegerät.</span><span class="sxs-lookup"><span data-stu-id="c3715-118">Create a device context (DC) on the display device.</span></span>
2.  <span data-ttu-id="c3715-119">Legen Sie die Farbverwaltung mithilfe der [**SetICMMode-Funktion**](/windows/desktop/api/Wingdi/nf-wingdi-seticmmode) fest.</span><span class="sxs-lookup"><span data-stu-id="c3715-119">Set color management using the [**SetICMMode**](/windows/desktop/api/Wingdi/nf-wingdi-seticmmode) function.</span></span>
3.  <span data-ttu-id="c3715-120">Verwenden Sie die [**SetDIBitsToDevice-Funktion,**](/windows/win32/api/wingdi/nf-wingdi-setdibitstodevice) um das DIB auf den DC zu übertragen.</span><span class="sxs-lookup"><span data-stu-id="c3715-120">Use the [**SetDIBitsToDevice**](/windows/win32/api/wingdi/nf-wingdi-setdibitstodevice) function to transfer the DIB into the DC.</span></span> <span data-ttu-id="c3715-121">Solange das **bV5CSMType-Element** der [**BITMAPV5HEADER-Struktur**](using-structures-in-wcs-1-0.md) des DIBs auf **LCS \_ sRGB** festgelegt ist, führt das System die entsprechende Farbverwaltung durch.</span><span class="sxs-lookup"><span data-stu-id="c3715-121">As long as the **bV5CSMType** member of the DIBs [**BITMAPV5HEADER**](using-structures-in-wcs-1-0.md) structure is set to **LCS\_sRGB**, the system will perform the appropriate color management.</span></span>

<span data-ttu-id="c3715-122">**So rendern Sie ein Bild außerhalb des Gerätekontexts**</span><span class="sxs-lookup"><span data-stu-id="c3715-122">**To render an image outside the device context**</span></span>

1.  <span data-ttu-id="c3715-123">Erstellen Sie mit [**CreateColorTransformW**](/windows/win32/api/icm/nf-icm-createcolortransformw)eine Transformation.</span><span class="sxs-lookup"><span data-stu-id="c3715-123">Create a transform using [**CreateColorTransformW**](/windows/win32/api/icm/nf-icm-createcolortransformw).</span></span> <span data-ttu-id="c3715-124">Der **lcsCSType-Member** der [**LOGCOLORSPACE-Struktur,**](/windows/desktop/api/Wingdi/ns-wingdi-taglogcolorspacea) auf den der *pLogColorSpace-Parameter* zeigt, sollte auf **LCS \_ sRGB** festgelegt werden.</span><span class="sxs-lookup"><span data-stu-id="c3715-124">The **lcsCSType** member of the [**LOGCOLORSPACE**](/windows/desktop/api/Wingdi/ns-wingdi-taglogcolorspacea) structure pointed to by the *pLogColorSpace* parameter should be set to **LCS\_sRGB**.</span></span> <span data-ttu-id="c3715-125">Der *Parameter hDestProfile* gibt den Farbraum des Anzeigegeräts an.</span><span class="sxs-lookup"><span data-stu-id="c3715-125">The *hDestProfile* parameter indicates the display device's color space.</span></span>
2.  <span data-ttu-id="c3715-126">Verwenden Sie die erstellte Farbtransformation, um die Farbe mit dem Bild abzugleichen, bevor Sie es auf dem Gerät anzeigen.</span><span class="sxs-lookup"><span data-stu-id="c3715-126">Use the created color transform to color match the image before displaying it on the device.</span></span>

## <a name="wcs-10-defaults-for-input-color-space-and-output-profile"></a><span data-ttu-id="c3715-127">WCS 1.0-Standardwerte für Eingabefarbraum und Ausgabeprofil</span><span class="sxs-lookup"><span data-stu-id="c3715-127">WCS 1.0 Defaults for Input Color Space and Output Profile</span></span>

<span data-ttu-id="c3715-128">Wenn kein Eingabefarbraum angegeben ist, verwendet WCS 1.0 standardmäßig den sRGB-Farbraum als Eingabefarbraum für die [Farbzuordnung.](c.md)</span><span class="sxs-lookup"><span data-stu-id="c3715-128">When no input color space is specified, by default WCS 1.0 uses the sRGB color space as the input color space for [color mapping](c.md).</span></span>

<span data-ttu-id="c3715-129">Wenn kein Ausgabeprofil angegeben ist, aber ein Standardgerät angegeben ist, wählt WCS 1.0 ein Standardausgabeprofil aus.</span><span class="sxs-lookup"><span data-stu-id="c3715-129">When no output profile is specified, but a default device is specified, WCS 1.0 selects a default output profile.</span></span> <span data-ttu-id="c3715-130">Wenn dem Standardgerät kein Profil zugeordnet ist, verwendet WCS 1.0 den sRGB-Farbraum als Ausgabeprofil.</span><span class="sxs-lookup"><span data-stu-id="c3715-130">If the default device does not have an associated profile, WCS 1.0 uses the sRGB color space as the output profile.</span></span>

<span data-ttu-id="c3715-131">Die folgende Tabelle zeigt die resultierenden Farbtransformationen, wenn kein Standardgerät verfügbar ist.</span><span class="sxs-lookup"><span data-stu-id="c3715-131">The following table shows the resulting color transforms when a default device is not available.</span></span>



|  &nbsp;                               | <span data-ttu-id="c3715-132">Angegebenes Ausgabeprofil</span><span class="sxs-lookup"><span data-stu-id="c3715-132">Output Profile Specified</span></span>                              | <span data-ttu-id="c3715-133">Ausgabeprofil nicht angegeben</span><span class="sxs-lookup"><span data-stu-id="c3715-133">Output Profile Not Specified</span></span>                             |
|---------------------------------|-------------------------------------------------------|----------------------------------------------------------|
| <span data-ttu-id="c3715-134">Eingabefarbraum angegeben</span><span class="sxs-lookup"><span data-stu-id="c3715-134">Input Color Space Specified</span></span>     | <span data-ttu-id="c3715-135">Die Transformation verwendet die angegebenen Profile.</span><span class="sxs-lookup"><span data-stu-id="c3715-135">Transform uses the specified profiles.</span></span>                | <span data-ttu-id="c3715-136">Transformiert Konvertierungen aus dem bekannten Eingabefarbraum in sRGB.</span><span class="sxs-lookup"><span data-stu-id="c3715-136">Transform converts from known input color space to sRGB.</span></span> |
| <span data-ttu-id="c3715-137">Eingabefarbraum nicht angegeben</span><span class="sxs-lookup"><span data-stu-id="c3715-137">Input Color Space Not Specified</span></span> | <span data-ttu-id="c3715-138">Transformiert Konvertierungen von sRGB in ein bekanntes Ausgabeprofil.</span><span class="sxs-lookup"><span data-stu-id="c3715-138">Transform converts from sRGB to known output profile.</span></span> | <span data-ttu-id="c3715-139">Die Transformation von sRGB in sRGB wird angenommen. es wird nichts ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="c3715-139">Transform from sRGB to sRGB is assumed; nothing is done.</span></span> |



 

## <a name="srgb-and-embedded-profiles"></a><span data-ttu-id="c3715-140">sRGB und eingebettete Profile</span><span class="sxs-lookup"><span data-stu-id="c3715-140">sRGB and Embedded Profiles</span></span>

<span data-ttu-id="c3715-141">Ab ICM Version 2.0 können Anwendungen, die WCS verwenden, Profile in Images einbetten.</span><span class="sxs-lookup"><span data-stu-id="c3715-141">Beginning with ICM version 2.0, applications that utilize WCS can embed profiles in images.</span></span> <span data-ttu-id="c3715-142">Eingebettete Profile unterstützen Die Anwendungen von Benutzern dabei, eine konsistente Farbdarstellung beizubehalten, auch wenn Bilder über das Internet übertragen werden.</span><span class="sxs-lookup"><span data-stu-id="c3715-142">Embedded profiles assist users' applications in maintaining a consistent color appearance even if images are transmitted across the Internet.</span></span>

<span data-ttu-id="c3715-143">Bilder, die den sRGB-Farbraum verwenden, benötigen kein eingebettetes Farbprofil.</span><span class="sxs-lookup"><span data-stu-id="c3715-143">Images that use the sRGB color space do not need an embedded color profile.</span></span> <span data-ttu-id="c3715-144">Da sie über kein eingebettetes Profil verfügen, sind sRGB-basierte Images kleiner und leichter über Datenkanäle mit begrenzter Bandbreite übertragbar.</span><span class="sxs-lookup"><span data-stu-id="c3715-144">Because they have no embedded profile, sRGB-based images are smaller and more readily transferable across data channels with limited bandwidth.</span></span>

<span data-ttu-id="c3715-145">Anwendungen sollten das **LCS \_ sRGB-Flag** im Bitmapheader des Bilds festlegen, um anzugeben, dass das Bild den sRGB-Farbraum verwendet.</span><span class="sxs-lookup"><span data-stu-id="c3715-145">Applications should set the **LCS\_sRGB** flag in the image's bitmap header to indicate that the image uses the sRGB color space.</span></span> <span data-ttu-id="c3715-146">Weitere Informationen finden Sie unter [Windows Bitmap Header Structures](using-structures-in-wcs-1-0.md) und [**LOGCOLORSPACE**](/windows/desktop/api/Wingdi/ns-wingdi-taglogcolorspacea).</span><span class="sxs-lookup"><span data-stu-id="c3715-146">For details, see [Windows Bitmap Header Structures](using-structures-in-wcs-1-0.md) and [**LOGCOLORSPACE**](/windows/desktop/api/Wingdi/ns-wingdi-taglogcolorspacea).</span></span>

 

 