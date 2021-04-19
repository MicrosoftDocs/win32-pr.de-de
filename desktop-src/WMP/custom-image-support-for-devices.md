---
title: Unterstützung für benutzerdefinierte Images für Geräte
description: Unterstützung für benutzerdefinierte Images für Geräte
ms.assetid: 0ccc327c-e953-4348-9802-705331b574ac
keywords:
- Windows Media Player, Unterstützung für benutzerdefinierte Images für Geräte
- Windows Media Player, Abbild Unterstützung für Geräte
- Unterstützung für benutzerdefinierte Geräte Images
- Unterstützung für benutzerdefinierte Images für Geräte
- imageunterstützung für Geräte
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5ffdf318df39935e844cc84919bb4d6e50cc259a
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "106342358"
---
# <a name="custom-image-support-for-devices"></a><span data-ttu-id="19536-108">Unterstützung für benutzerdefinierte Images für Geräte</span><span class="sxs-lookup"><span data-stu-id="19536-108">Custom Image Support for Devices</span></span>

> [!Note]  
> <span data-ttu-id="19536-109">In diesem Abschnitt wird ein Feature von Windows Media Player 10 dokumentiert, das verfügbar ist, wenn das Betriebssystem Windows XP verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="19536-109">This section documents a feature of Windows Media Player 10 that is available when using the Windows XP operating system.</span></span> <span data-ttu-id="19536-110">Er ist möglicherweise in nachfolgenden Versionen nicht verfügbar.</span><span class="sxs-lookup"><span data-stu-id="19536-110">It may be unavailable in subsequent versions.</span></span>

 

<span data-ttu-id="19536-111">Gerätehersteller können zwei spezielle Bilddateien bereitstellen, um die Art und Weise anzupassen, wie ein Gerät in der Windows Media Player 10-Benutzeroberfläche dargestellt wird.</span><span class="sxs-lookup"><span data-stu-id="19536-111">Device manufacturers can provide two special image files to customize the way a device is represented in the Windows Media Player 10 user interface.</span></span> <span data-ttu-id="19536-112">Diese beiden Dateien lauten:</span><span class="sxs-lookup"><span data-stu-id="19536-112">These two files are:</span></span>

-   <span data-ttu-id="19536-113">"Debug".</span><span class="sxs-lookup"><span data-stu-id="19536-113">DevIcon.fil.</span></span> <span data-ttu-id="19536-114">Eine Windows-Symbol Format Datei, die die Gerätehardware darstellt.</span><span class="sxs-lookup"><span data-stu-id="19536-114">A Windows icon format file that represents the device hardware.</span></span> <span data-ttu-id="19536-115">Dieses Bild wird in Windows Media Player 10 angezeigt, wo ein Symbol zur Darstellung eines Geräts verwendet wird, z. b. die Geräteliste in der **Synchronisierungs** Funktion.</span><span class="sxs-lookup"><span data-stu-id="19536-115">This image displays in Windows Media Player 10 anywhere an icon is used to represent a device, such as the device list in the **Sync** feature.</span></span>
-   <span data-ttu-id="19536-116">Devlogo. fil.</span><span class="sxs-lookup"><span data-stu-id="19536-116">DevLogo.fil.</span></span> <span data-ttu-id="19536-117">Eine PNG-Format Datei, die das Firmenlogo des Geräteherstellers darstellt.</span><span class="sxs-lookup"><span data-stu-id="19536-117">A PNG format file that represents the corporate logo of the device manufacturer.</span></span> <span data-ttu-id="19536-118">Dieses Bild wird in Windows Media Player 10, wo das Unternehmens Branding verwendet wird, z. b. im Dialogfeld " **Geräte Einrichtung** ", angezeigt.</span><span class="sxs-lookup"><span data-stu-id="19536-118">This image displays in Windows Media Player 10 anywhere corporate branding is used, such as the **Device Setup** dialog box.</span></span>

## <a name="general-guidelines-for-images"></a><span data-ttu-id="19536-119">Allgemeine Richtlinien für Images</span><span class="sxs-lookup"><span data-stu-id="19536-119">General Guidelines for Images</span></span>

<span data-ttu-id="19536-120">Die folgenden Richtlinien gelten für die Unterstützung für benutzerdefinierte Images im allgemeinen:</span><span class="sxs-lookup"><span data-stu-id="19536-120">The following guidelines apply to custom image support in general:</span></span>

-   <span data-ttu-id="19536-121">Dieses Feature ist optional.</span><span class="sxs-lookup"><span data-stu-id="19536-121">This feature is optional.</span></span> <span data-ttu-id="19536-122">Geräte, die keine Abbilder bereitstellen, werden standardmäßig dargestellt.</span><span class="sxs-lookup"><span data-stu-id="19536-122">Devices that do not supply images will be represented by default images.</span></span>
-   <span data-ttu-id="19536-123">Diese Funktion wird nur für MTP-aktivierte Geräte unterstützt.</span><span class="sxs-lookup"><span data-stu-id="19536-123">This feature is supported for MTP-enabled devices only.</span></span>
-   <span data-ttu-id="19536-124">Um Änderungen an den Dateien zu verhindern, empfiehlt es sich, die Bilddateien in der Firmware oder einem geschützten Speichermedium (nicht mit vom Benutzer erstellten Dateien) zu speichern.</span><span class="sxs-lookup"><span data-stu-id="19536-124">To prevent changes to the files, it is recommended that the image files be stored in firmware or a protected storage medium, not with user-created files.</span></span>
-   <span data-ttu-id="19536-125">Die Dateien sollten nicht an Windows Media Device Manager-Clients zurückgegeben werden, die den Stamm Speicher des Geräts auflisten.</span><span class="sxs-lookup"><span data-stu-id="19536-125">The files should not be returned to Windows Media Device Manager clients that enumerate the root storage of the device.</span></span> <span data-ttu-id="19536-126">Außerdem sollte das Löschen, verschieben oder Umbenennen der Dateien fehlschlagen.</span><span class="sxs-lookup"><span data-stu-id="19536-126">Also, deleting, moving, or renaming the files should fail.</span></span>
-   <span data-ttu-id="19536-127">Wenn das Gerät mehr als ein Speichermedium bereitstellt, sollte das Gerät die Bilddateien als Reaktion auf Datei Öffnungs Anforderungen von einem beliebigen Medium zurückgeben.</span><span class="sxs-lookup"><span data-stu-id="19536-127">If the device provides more than one storage medium, the device should return the image files in response to file open requests from any medium.</span></span> <span data-ttu-id="19536-128">Verschiedene Geräte Symbole können von jedem Speichermedium zurückgegeben werden.</span><span class="sxs-lookup"><span data-stu-id="19536-128">Different device icons may be returned from each storage medium.</span></span>
-   <span data-ttu-id="19536-129">Bei Windows Media Device Manager 1,2-fähigen Clients haben diese Images Vorrang vor Symbol Eigenschaften, die von Windows-Setup Mechanismen, z. b. Geräteknoten Eigenschaften, bereitgestellt werden.</span><span class="sxs-lookup"><span data-stu-id="19536-129">For Windows Media Device Manager 1.2-enabled clients, these images will take precedence over icon properties supplied by Windows setup mechanisms, such as device node properties.</span></span>
-   <span data-ttu-id="19536-130">Die Bilder dürfen keine Informationen enthalten, die eine Lokalisierung erfordern.</span><span class="sxs-lookup"><span data-stu-id="19536-130">The images must not contain any information that requires localization.</span></span>
-   <span data-ttu-id="19536-131">Bei Geräten mit mehreren Funktionen werden diese Images nur für die Musikwiedergabe Features von Windows XP verwendet.</span><span class="sxs-lookup"><span data-stu-id="19536-131">For multi-function devices, only the music playback features of Windows XP will use these images.</span></span>

## <a name="creating-the-device-icon-image"></a><span data-ttu-id="19536-132">Erstellen des Gerätesymbol Bilds</span><span class="sxs-lookup"><span data-stu-id="19536-132">Creating the Device Icon Image</span></span>

<span data-ttu-id="19536-133">Die Gerätesymbol-Bilddatei Devicon. fil muss eine Datei im Windows-Symbol Format enthalten.</span><span class="sxs-lookup"><span data-stu-id="19536-133">The device icon image file, DevIcon.fil, must contain a file in Windows icon format.</span></span> <span data-ttu-id="19536-134">In den MSDN-Artikel [Symbolen in Win32](/previous-versions/ms997538(v=msdn.10)) wird beschrieben, wie eine solche Datei erstellt wird.</span><span class="sxs-lookup"><span data-stu-id="19536-134">The MSDN article [Icons in Win32](/previous-versions/ms997538(v=msdn.10)) describes how to create such a file.</span></span> <span data-ttu-id="19536-135">Der MSDN-Artikel [Erstellen von Windows XP-Symbolen](/previous-versions/ms997636(v=msdn.10)) bietet Stilrichtlinien für Windows XP-Symbole.</span><span class="sxs-lookup"><span data-stu-id="19536-135">The MSDN article [Creating Windows XP Icons](/previous-versions/ms997636(v=msdn.10)) provides style guidelines for Windows XP icons.</span></span> <span data-ttu-id="19536-136">Die Gerätesymbol-Bilddatei enthält zwölf Bilder in einer einzelnen Datei, indem vier verschiedene Größen mit jeweils drei unterschiedlichen Farbtiefen bereitgestellt werden.</span><span class="sxs-lookup"><span data-stu-id="19536-136">The device icon image file incorporates twelve images in a single file by providing four different sizes with three different color depths each.</span></span>

<span data-ttu-id="19536-137">Achten Sie besonders auf die folgenden Richtlinien:</span><span class="sxs-lookup"><span data-stu-id="19536-137">Be certain to pay particular attention to the following guidelines:</span></span>

-   <span data-ttu-id="19536-138">Empfohlene Größen (in Pixel) sind 16x16, 32x32, 48x48 und 256x256.</span><span class="sxs-lookup"><span data-stu-id="19536-138">Recommended sizes (in pixels) are 16x16, 32x32, 48x48, and 256x256.</span></span>
-   <span data-ttu-id="19536-139">Empfohlene Farbtiefe sind 24 Bit mit 8-Bit-Alphakanal, 8-Bit-Transparenz und 1-Bit-Transparenz und 4 Bit mit 1-Bit-Transparenz.</span><span class="sxs-lookup"><span data-stu-id="19536-139">Recommended color depths are 24-bit with 8-bit alpha channel, 8-bit with 1-bit transparency, and 4-bit with 1-bit transparency.</span></span>
-   <span data-ttu-id="19536-140">Verwenden Sie die in den zuvor erwähnten MSDN-Artikeln beschriebenen Empfehlungen Perspektive Angle und Drop Shadow.</span><span class="sxs-lookup"><span data-stu-id="19536-140">Use the perspective angle and drop shadow recommendations described in the MSDN articles mentioned previously.</span></span>

<span data-ttu-id="19536-141">Nachdem Sie die Symbol Datei erstellt haben, benennen Sie Sie einfach Devicon. fil um.</span><span class="sxs-lookup"><span data-stu-id="19536-141">Once you have created the icon file, simply rename it DevIcon.fil.</span></span>

## <a name="creating-the-corporate-logo-image"></a><span data-ttu-id="19536-142">Erstellen des Firmen Logo Bilds</span><span class="sxs-lookup"><span data-stu-id="19536-142">Creating the Corporate Logo Image</span></span>

<span data-ttu-id="19536-143">Die Bilddatei für das Firmenlogo, devlogo. fil, muss eine Datei im PNG-Format enthalten.</span><span class="sxs-lookup"><span data-stu-id="19536-143">The corporate logo image file, DevLogo.fil, must contain a file in PNG format.</span></span> <span data-ttu-id="19536-144">Beachten Sie beim Erstellen des Images die folgenden Richtlinien:</span><span class="sxs-lookup"><span data-stu-id="19536-144">Use the following guidelines when creating the image:</span></span>

-   <span data-ttu-id="19536-145">Die maximalen Abmessungen für das Bild sind 150 x 32 Pixel.</span><span class="sxs-lookup"><span data-stu-id="19536-145">The maximum dimensions for the image are 150x32 pixels.</span></span>
-   <span data-ttu-id="19536-146">Das Bild sollte Alpha Blending unterstützen, um einen reibungslosen Übergang zwischen der Windows Media Player 10-Benutzeroberfläche und dem Logo zu ermöglichen.</span><span class="sxs-lookup"><span data-stu-id="19536-146">The image should support alpha blending to enable a smooth transition between the Windows Media Player 10 user interface and the logo.</span></span>

<span data-ttu-id="19536-147">Nachdem Sie die Firmenlogo Datei erstellt haben, benennen Sie Sie einfach "devlogo. fil" um.</span><span class="sxs-lookup"><span data-stu-id="19536-147">Once you have created the corporate logo file, simply rename it DevLogo.fil.</span></span>

## <a name="related-topics"></a><span data-ttu-id="19536-148">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="19536-148">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="19536-149">**Windows Media Player**</span><span class="sxs-lookup"><span data-stu-id="19536-149">**Windows Media Player**</span></span>](windows-media-player.md)
</dt> </dl>

 

 