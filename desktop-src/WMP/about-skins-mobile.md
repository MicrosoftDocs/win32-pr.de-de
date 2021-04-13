---
title: Informationen zu Skins (Mobile)
description: Informationen zu Skins
ms.assetid: 105c11ce-705b-4a0c-8982-d0f9dd9ae3ac
keywords:
- Windows Media Player Mobile, Skins
- Windows Media Player Mobile Skins, Informationen zu
- Windows Media Player Mobile Skins, erstellen
- Skins, Windows Media Player Mobile
- Erstellen von Skins, Windows Media Player Mobile
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b2db0e81c45c253e3a4fe3c12d4cc97a51f4ede0
ms.sourcegitcommit: 8fa6614b715bddf14648cce36d2df22e5232801a
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/10/2020
ms.locfileid: "104340097"
---
# <a name="about-skins-mobile"></a><span data-ttu-id="4f05d-108">Informationen zu Skins (Mobile)</span><span class="sxs-lookup"><span data-stu-id="4f05d-108">About Skins (Mobile)</span></span>

<span data-ttu-id="4f05d-109">Ein Skin ist eine angepasste Benutzeroberfläche für Windows Media Player.</span><span class="sxs-lookup"><span data-stu-id="4f05d-109">A skin is a customized user interface to Windows Media Player.</span></span> <span data-ttu-id="4f05d-110">Sie können eigene Schaltflächen erstellen, um die Wiedergabe digitaler Medien zu starten und zu unterbinden, Schieberegler zum Ändern der Volume-und Wiedergabe Position im Medien Element hinzuzufügen und dem Benutzer Textinformationen wie z. b. den Namen eines Titels bereitzustellen.</span><span class="sxs-lookup"><span data-stu-id="4f05d-110">You can create your own buttons to start and stop playback of digital media, add sliders to change volume and playback position in the media item, and provide the user with text information such as the name of a song.</span></span> <span data-ttu-id="4f05d-111">Das beste ist, dass Sie Ihre eigene Kunst hinzufügen oder vorhandene Grafiken verwenden können, um eine einzigartige Darstellung für Ihre Skin zu schaffen.</span><span class="sxs-lookup"><span data-stu-id="4f05d-111">Best of all, you can add your own artwork or use existing art to create a unique appearance for your skin.</span></span>

<span data-ttu-id="4f05d-112">Die grundlegenden Schritte zum Erstellen einer Skin sind:</span><span class="sxs-lookup"><span data-stu-id="4f05d-112">The basic steps in creating a skin are:</span></span>

1.  <span data-ttu-id="4f05d-113">**Entwerfen** Sie die Benutzeroberfläche.</span><span class="sxs-lookup"><span data-stu-id="4f05d-113">**Design** your user interface.</span></span> <span data-ttu-id="4f05d-114">Entscheiden Sie, welche Schaltflächen, Textfelder und trackbars Sie für den Benutzer bereitstellen möchten, damit Sie die Funktionen steuern können, die Sie in Schritt 1 ausgewählt haben.</span><span class="sxs-lookup"><span data-stu-id="4f05d-114">Decide which buttons, text boxes, and trackbars you want to provide to the user so that they can control the functions you chose in step 1.</span></span> <span data-ttu-id="4f05d-115">Vielleicht möchten Sie Ihre Ideen herausfinden, um zu sehen, wie Sie in die Image Größe passen, mit der Sie arbeiten werden.</span><span class="sxs-lookup"><span data-stu-id="4f05d-115">You may want to sketch out your ideas to see how they fit on the image size you will be working with.</span></span>
2.  <span data-ttu-id="4f05d-116">**Erstellen** Sie die Art, in der der Benutzer angezeigt werden soll.</span><span class="sxs-lookup"><span data-stu-id="4f05d-116">**Create** the art you want to show the user.</span></span> <span data-ttu-id="4f05d-117">Dies besteht aus mehreren Bildern, die die Hintergrundbilder, andere Bilder, die Sie anzeigen können, und das Mapping von Bildern, wenn Sie Bereichs Schaltflächen verwenden.</span><span class="sxs-lookup"><span data-stu-id="4f05d-117">This will consist of several images that show the background images, other images you may want to display, and mapping images if you use region buttons.</span></span>
3.  <span data-ttu-id="4f05d-118">**Schreiben** Sie die Skin-Definitionsdatei, mit der die Funktionen, die Benutzeroberfläche und die Bilder der digitalen Medien miteinander verknüpft werden.</span><span class="sxs-lookup"><span data-stu-id="4f05d-118">**Write** the skin definition file that will link together the digital media functions, user interface, and images.</span></span> <span data-ttu-id="4f05d-119">Sie müssen bestimmte Regeln befolgen, um die Textdaten in die Datei einzugeben, aber Sie können die Standard Skin als Leitfaden betrachten.</span><span class="sxs-lookup"><span data-stu-id="4f05d-119">You must follow certain rules for entering the text data into the file, but you can look at the default skin as a guide.</span></span>

<span data-ttu-id="4f05d-120">Sie müssen diese Schritte nicht in der angegebenen Reihenfolge ausführen, aber ein guter Entwurf ist, dass Sie sich mit allen Möglichkeiten vertraut machen und alle Details berücksichtigen.</span><span class="sxs-lookup"><span data-stu-id="4f05d-120">You do not need to follow these steps in the order given, but a good design will come from being aware of all the possibilities and taking care of all the details.</span></span>

<span data-ttu-id="4f05d-121">Die folgenden Abschnitte enthalten ausführliche Informationen zu Skins.</span><span class="sxs-lookup"><span data-stu-id="4f05d-121">The following sections provide detailed information about skins.</span></span>



| <span data-ttu-id="4f05d-122">`Section`</span><span class="sxs-lookup"><span data-stu-id="4f05d-122">Section</span></span>                                                                                    | <span data-ttu-id="4f05d-123">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="4f05d-123">Description</span></span>                                                                                                                                                                                      |
|--------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="4f05d-124">Informationen zur Kompatibilität</span><span class="sxs-lookup"><span data-stu-id="4f05d-124">About Compatibility</span></span>](about-compatibility.md)                                             | <span data-ttu-id="4f05d-125">Listet die verschiedenen Versionen von Windows Media Player Mobile, die Hardwareanforderungen, die Verfügbarkeit von Windows Media Player und die für jede Version der Software eingeführten Skin-Features auf.</span><span class="sxs-lookup"><span data-stu-id="4f05d-125">Lists the different versions of Windows Media Player Mobile, the hardware requirements, availability of Windows Media Player, and the skin features introduced for each version of the software.</span></span> |
| [<span data-ttu-id="4f05d-126">Windows Media Player Mobile-Funktionalität</span><span class="sxs-lookup"><span data-stu-id="4f05d-126">Windows Media Player Mobile Functionality</span></span>](windows-media-player-mobile-functionality.md) | <span data-ttu-id="4f05d-127">Beschreibt die Funktionen, die ihre Skin unterstützen kann.</span><span class="sxs-lookup"><span data-stu-id="4f05d-127">Describes the features your skin can support.</span></span>                                                                                                                                                    |
| [<span data-ttu-id="4f05d-128">Elemente der Benutzeroberfläche</span><span class="sxs-lookup"><span data-stu-id="4f05d-128">User Interface Elements</span></span>](user-interface-elements.md)                                     | <span data-ttu-id="4f05d-129">Beschreibt die Elemente der Benutzeroberfläche, die Sie für Ihre Skin erstellen können, z. b. Schaltflächen, trackbars und Video anzeigen.</span><span class="sxs-lookup"><span data-stu-id="4f05d-129">Describes the user interface elements you can create for your skin, such as buttons, trackbars, and video displays.</span></span>                                                                              |
| [<span data-ttu-id="4f05d-130">Kunstdateien</span><span class="sxs-lookup"><span data-stu-id="4f05d-130">Art Files</span></span>](art-files-mobile.md)                                                          | <span data-ttu-id="4f05d-131">Beschreibt die kunstdateien, die Sie für Ihre Skin erstellen.</span><span class="sxs-lookup"><span data-stu-id="4f05d-131">Describes the art files you create for your skin.</span></span>                                                                                                                                                |
| [<span data-ttu-id="4f05d-132">Skin-Definitionsdatei</span><span class="sxs-lookup"><span data-stu-id="4f05d-132">Skin Definition File</span></span>](skin-definition-file-mobile.md)                                    | <span data-ttu-id="4f05d-133">Beschreibt die Datei, die Sie zum Beschreiben Ihrer Skin erstellen müssen.</span><span class="sxs-lookup"><span data-stu-id="4f05d-133">Describes the file you must create to describe your skin.</span></span>                                                                                                                                        |



 

## <a name="related-topics"></a><span data-ttu-id="4f05d-134">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="4f05d-134">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="4f05d-135">**Windows Media Player Mobile Skins**</span><span class="sxs-lookup"><span data-stu-id="4f05d-135">**Windows Media Player Mobile Skins**</span></span>](windows-media-player-mobile-skins.md)
</dt> </dl>

 

 




