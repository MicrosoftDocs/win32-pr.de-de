---
title: Super Dateien
description: Super Dateien
ms.assetid: a5005d1a-4b87-482d-914e-3184a2c93267
keywords:
- Windows Media Player Mobile Skins, Art Dateien
- Skins, Art Dateien
- Dateien für Skins, Art
- kunstdateien für Skins, Super files-Dateien
- Windows Media Player Mobile Skins, Super files-Dateien
- Skins, Super files
- Super Dateien in Skins
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ece533f81f8866eb0f9848d7296cc23bcd37f453
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "106338614"
---
# <a name="super-files"></a><span data-ttu-id="cbd9d-110">Super Dateien</span><span class="sxs-lookup"><span data-stu-id="cbd9d-110">Super Files</span></span>

<span data-ttu-id="cbd9d-111">Super Dateien werden zum Speichern der deaktivierten Images für trackbars verwendet.</span><span class="sxs-lookup"><span data-stu-id="cbd9d-111">Super files are used to store the Disabled images for trackbars.</span></span> <span data-ttu-id="cbd9d-112">Da das TrackBar-Haupt Bild in der Hintergrund Datei angezeigt wird und der Benutzer auf das Thumb-Bild und nicht auf das TrackBar-Bild tippt, wird nur das deaktivierte Bild für trackbars benötigt.</span><span class="sxs-lookup"><span data-stu-id="cbd9d-112">Because the main trackbar image is displayed in the Background file, and the user taps on the thumb image, not the trackbar image, only the Disabled image is needed for trackbars.</span></span> <span data-ttu-id="cbd9d-113">Sie wird in der Datei gespeichert, die von Super im Abschnitt Bitmaps der Skin-Definitionsdatei definiert ist.</span><span class="sxs-lookup"><span data-stu-id="cbd9d-113">It is stored in the file defined by Super in the Bitmaps section of the skin definition file.</span></span> <span data-ttu-id="cbd9d-114">Eine Super-Datei kann auch die über drückten und deaktivierten Bilder für andere Schaltflächen wie stumm speichern. Dies ist nicht erforderlich, um eine Schaltfläche vom Typ "Treffer" zu sein.</span><span class="sxs-lookup"><span data-stu-id="cbd9d-114">A Super file can also store the Pushed and Disabled images for other buttons such as Mute, which is not required to be a hit-type button.</span></span>

> [!Note]  
> <span data-ttu-id="cbd9d-115">Super kunstdateien werden in Skins für Windows Media Player 10 Mobile oder höher nicht verwendet, da sich die deaktivierten Images für Such trackbars in der seekthumb-Datei befinden.</span><span class="sxs-lookup"><span data-stu-id="cbd9d-115">Super art files are not used in skins for Windows Media Player 10 Mobile or later because the disabled images for seek trackbars are located in the seekthumb file.</span></span>

 

<span data-ttu-id="cbd9d-116">Das folgende Bild ist eine typische Super-Datei.</span><span class="sxs-lookup"><span data-stu-id="cbd9d-116">The following image is a typical Super file.</span></span>

![Super-Datei](images/cesdksup.png)

<span data-ttu-id="cbd9d-118">Dadurch werden die deaktivierten Bilder für die trackbars und die stumm Schaltfläche gespeichert.</span><span class="sxs-lookup"><span data-stu-id="cbd9d-118">This stores the disabled images for the trackbars and the mute button.</span></span> <span data-ttu-id="cbd9d-119">Diese Bilder sind im Abschnitt Bitmaps definiert.</span><span class="sxs-lookup"><span data-stu-id="cbd9d-119">These images are offset as defined by the Bitmaps section.</span></span>

<span data-ttu-id="cbd9d-120">Der Hintergrundbereich des deaktivierten TrackBar-Bilds stimmt exakt mit dem entsprechenden Bereich in der Hintergrund Datei überein.</span><span class="sxs-lookup"><span data-stu-id="cbd9d-120">The background area of the disabled trackbar image exactly matches the corresponding area in the Background file.</span></span> <span data-ttu-id="cbd9d-121">Dies ist wichtig, da das gesamte Rechteck, das für das deaktivierte TrackBar-Bild definiert ist, den entsprechenden Bereich in der Hintergrund Datei ersetzt.</span><span class="sxs-lookup"><span data-stu-id="cbd9d-121">This is important, because the entire rectangle defined for the disabled trackbar image will replace the matching area in the Background file.</span></span> <span data-ttu-id="cbd9d-122">Dadurch wird sichergestellt, dass das deaktivierte TrackBar-Bild nahtlos in das Hintergrundbild integriert ist.</span><span class="sxs-lookup"><span data-stu-id="cbd9d-122">This ensures that the disabled trackbar image blends seamlessly into the background image.</span></span>

## <a name="related-topics"></a><span data-ttu-id="cbd9d-123">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="cbd9d-123">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="cbd9d-124">**Kunstdateien**</span><span class="sxs-lookup"><span data-stu-id="cbd9d-124">**Art Files**</span></span>](art-files-mobile.md)
</dt> </dl>

 

 




