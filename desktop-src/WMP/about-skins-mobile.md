---
title: Informationen zu Skins (Mobil)
description: Erfahren Sie mehr über Skins für mobile Player. Eine Skin ist eine benutzerdefinierte Benutzeroberfläche für Windows Media Player.
ms.assetid: 105c11ce-705b-4a0c-8982-d0f9dd9ae3ac
keywords:
- Windows Media Player Mobile,skins
- Windows Media Player Mobile-Skins, Informationen
- Windows Media Player Mobile-Skins,erstellen
- skins,Windows Media Player Mobile
- Erstellen von Skins,Windows Media Player Mobile
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ebdffdc4075456c6cb7ccf9d1940c5253c732cd3
ms.sourcegitcommit: 8f0a1d212dd154e8d94ab4c0e4ced053fa16823a
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2021
ms.locfileid: "112011223"
---
# <a name="about-skins-mobile"></a><span data-ttu-id="60f5b-109">Informationen zu Skins (Mobil)</span><span class="sxs-lookup"><span data-stu-id="60f5b-109">About Skins (Mobile)</span></span>

<span data-ttu-id="60f5b-110">Eine Skin ist eine benutzerdefinierte Benutzeroberfläche für Windows Media Player.</span><span class="sxs-lookup"><span data-stu-id="60f5b-110">A skin is a customized user interface to Windows Media Player.</span></span> <span data-ttu-id="60f5b-111">Sie können eigene Schaltflächen erstellen, um die Wiedergabe digitaler Medien zu starten und zu beenden, Schieberegler zum Ändern der Lautstärke und Wiedergabeposition im Medienelement hinzufügen und dem Benutzer Textinformationen wie den Namen eines Musiktitels zur Verfügung stellen.</span><span class="sxs-lookup"><span data-stu-id="60f5b-111">You can create your own buttons to start and stop playback of digital media, add sliders to change volume and playback position in the media item, and provide the user with text information such as the name of a song.</span></span> <span data-ttu-id="60f5b-112">Das Beste ist, dass Sie Ihre eigenen Grafiken hinzufügen oder vorhandene Grafiken verwenden können, um eine einzigartige Darstellung für Ihre Skin zu erstellen.</span><span class="sxs-lookup"><span data-stu-id="60f5b-112">Best of all, you can add your own artwork or use existing art to create a unique appearance for your skin.</span></span>

<span data-ttu-id="60f5b-113">Die grundlegenden Schritte zum Erstellen einer Skin sind:</span><span class="sxs-lookup"><span data-stu-id="60f5b-113">The basic steps in creating a skin are:</span></span>

1.  <span data-ttu-id="60f5b-114">**Entwerfen** Sie Ihre Benutzeroberfläche.</span><span class="sxs-lookup"><span data-stu-id="60f5b-114">**Design** your user interface.</span></span> <span data-ttu-id="60f5b-115">Entscheiden Sie, welche Schaltflächen, Textfelder und Trackleisten Sie dem Benutzer zur Verfügung stellen möchten, damit er die Funktionen steuern kann, die Sie in Schritt 1 ausgewählt haben.</span><span class="sxs-lookup"><span data-stu-id="60f5b-115">Decide which buttons, text boxes, and trackbars you want to provide to the user so that they can control the functions you chose in step 1.</span></span> <span data-ttu-id="60f5b-116">Vielleicht möchten Sie Ihre Ideen skizzieren, um zu sehen, wie sie zu der Bildgröße passen, mit der Sie arbeiten werden.</span><span class="sxs-lookup"><span data-stu-id="60f5b-116">You may want to sketch out your ideas to see how they fit on the image size you will be working with.</span></span>
2.  <span data-ttu-id="60f5b-117">**Erstellen** Sie die Art, die Sie dem Benutzer zeigen möchten.</span><span class="sxs-lookup"><span data-stu-id="60f5b-117">**Create** the art you want to show the user.</span></span> <span data-ttu-id="60f5b-118">Dies besteht aus mehreren Bildern, die die Hintergrundbilder, andere Bilder, die Sie möglicherweise anzeigen möchten, und Zuordnungsbilder, wenn Sie Schaltflächen für Regionen verwenden.</span><span class="sxs-lookup"><span data-stu-id="60f5b-118">This will consist of several images that show the background images, other images you may want to display, and mapping images if you use region buttons.</span></span>
3.  <span data-ttu-id="60f5b-119">**Schreiben** Sie die Skindefinitionsdatei, die die digitalen Medienfunktionen, die Benutzeroberfläche und Bilder miteinander verknüpfen soll.</span><span class="sxs-lookup"><span data-stu-id="60f5b-119">**Write** the skin definition file that will link together the digital media functions, user interface, and images.</span></span> <span data-ttu-id="60f5b-120">Sie müssen bestimmte Regeln für die Eingabe der Textdaten in die Datei befolgen, aber Sie können sich die Standard-Skin als Leitfaden angesehen werden.</span><span class="sxs-lookup"><span data-stu-id="60f5b-120">You must follow certain rules for entering the text data into the file, but you can look at the default skin as a guide.</span></span>

<span data-ttu-id="60f5b-121">Sie müssen diese Schritte nicht in der angegebenen Reihenfolge ausführen, aber ein guter Entwurf ergibt sich daraus, dass Sie alle Möglichkeiten kennen und sich um alle Details kümmern.</span><span class="sxs-lookup"><span data-stu-id="60f5b-121">You do not need to follow these steps in the order given, but a good design will come from being aware of all the possibilities and taking care of all the details.</span></span>

<span data-ttu-id="60f5b-122">Die folgenden Abschnitte enthalten ausführliche Informationen zu Skins.</span><span class="sxs-lookup"><span data-stu-id="60f5b-122">The following sections provide detailed information about skins.</span></span>



| <span data-ttu-id="60f5b-123">`Section`</span><span class="sxs-lookup"><span data-stu-id="60f5b-123">Section</span></span>                                                                                    | <span data-ttu-id="60f5b-124">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="60f5b-124">Description</span></span>                                                                                                                                                                                      |
|--------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="60f5b-125">Informationen zur Kompatibilität</span><span class="sxs-lookup"><span data-stu-id="60f5b-125">About Compatibility</span></span>](about-compatibility.md)                                             | <span data-ttu-id="60f5b-126">Listet die verschiedenen Versionen von Windows Media Player Mobile, die Hardwareanforderungen, die Verfügbarkeit von Windows Media Player und die Skinfeatures, die für jede Version der Software eingeführt wurden.</span><span class="sxs-lookup"><span data-stu-id="60f5b-126">Lists the different versions of Windows Media Player Mobile, the hardware requirements, availability of Windows Media Player, and the skin features introduced for each version of the software.</span></span> |
| [<span data-ttu-id="60f5b-127">Windows Media Player Mobile-Funktionalität</span><span class="sxs-lookup"><span data-stu-id="60f5b-127">Windows Media Player Mobile Functionality</span></span>](windows-media-player-mobile-functionality.md) | <span data-ttu-id="60f5b-128">Beschreibt die Features, die Ihre Skin unterstützen kann.</span><span class="sxs-lookup"><span data-stu-id="60f5b-128">Describes the features your skin can support.</span></span>                                                                                                                                                    |
| [<span data-ttu-id="60f5b-129">Benutzeroberfläche Elements</span><span class="sxs-lookup"><span data-stu-id="60f5b-129">User Interface Elements</span></span>](user-interface-elements.md)                                     | <span data-ttu-id="60f5b-130">Beschreibt die Benutzeroberflächenelemente, die Sie für Ihre Skin erstellen können, z. B. Schaltflächen, Trackbars und Videoanzeigen.</span><span class="sxs-lookup"><span data-stu-id="60f5b-130">Describes the user interface elements you can create for your skin, such as buttons, trackbars, and video displays.</span></span>                                                                              |
| [<span data-ttu-id="60f5b-131">Art-Dateien</span><span class="sxs-lookup"><span data-stu-id="60f5b-131">Art Files</span></span>](art-files-mobile.md)                                                          | <span data-ttu-id="60f5b-132">Beschreibt die Artdateien, die Sie für Ihre Skin erstellen.</span><span class="sxs-lookup"><span data-stu-id="60f5b-132">Describes the art files you create for your skin.</span></span>                                                                                                                                                |
| [<span data-ttu-id="60f5b-133">Skindefinitionsdatei</span><span class="sxs-lookup"><span data-stu-id="60f5b-133">Skin Definition File</span></span>](skin-definition-file-mobile.md)                                    | <span data-ttu-id="60f5b-134">Beschreibt die Datei, die Sie erstellen müssen, um Ihre Skin zu beschreiben.</span><span class="sxs-lookup"><span data-stu-id="60f5b-134">Describes the file you must create to describe your skin.</span></span>                                                                                                                                        |



 

## <a name="related-topics"></a><span data-ttu-id="60f5b-135">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="60f5b-135">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="60f5b-136">**Windows Media Player Mobile Skins**</span><span class="sxs-lookup"><span data-stu-id="60f5b-136">**Windows Media Player Mobile Skins**</span></span>](windows-media-player-mobile-skins.md)
</dt> </dl>

 

 




