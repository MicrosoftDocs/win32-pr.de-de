---
title: Trackbars
description: Trackbars
ms.assetid: b9676697-c3ab-465c-8b50-eb784f53bb11
keywords:
- Windows Media Player Mobile Skins, trackbars
- Skins, trackbars
- Verweis für Skins, trackbars
- trackbars in Skins, Info
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: cb7b64f7bada6f927b25aeecb71d584aa1ec2a68
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "106340230"
---
# <a name="trackbars"></a><span data-ttu-id="885da-107">Trackbars</span><span class="sxs-lookup"><span data-stu-id="885da-107">Trackbars</span></span>

<span data-ttu-id="885da-108">Eine TrackBar zeigt ein Bild an, das in kleinen Schritten geändert wird.</span><span class="sxs-lookup"><span data-stu-id="885da-108">A trackbar displays an image that changes in small increments.</span></span> <span data-ttu-id="885da-109">Trackbars werden für volumensteuerelemente und Wiedergabe Positions Steuerelemente verwendet.</span><span class="sxs-lookup"><span data-stu-id="885da-109">Trackbars are used for volume controls and playback position controls.</span></span> <span data-ttu-id="885da-110">Mithilfe von trackbars können Sie Informationen zum aktuellen Medien Element anzeigen oder den Benutzern die Möglichkeit geben, Einstellungen oder Wiedergabe Positionen zu ändern.</span><span class="sxs-lookup"><span data-stu-id="885da-110">You can use trackbars to display information about the current media item or to allow the user to change settings or playback position.</span></span> <span data-ttu-id="885da-111">Beispielsweise können Sie eine TrackBar verwenden, um dem Benutzer das Anpassen des Volumes und eine weitere TrackBar zu ermöglichen, die dem Benutzer die aktuelle Wiedergabe Position anzeigen kann.</span><span class="sxs-lookup"><span data-stu-id="885da-111">For example, you can use a trackbar to enable the user to adjust the volume, and another trackbar that can show the user the current playback position.</span></span> <span data-ttu-id="885da-112">Trackbars verfügen über ein Thumb-Bild, das die aktuelle Einstellung des TrackBar-Werts definiert.</span><span class="sxs-lookup"><span data-stu-id="885da-112">Trackbars have a thumb image that defines the current setting of the trackbar value.</span></span>

<span data-ttu-id="885da-113">Der trackbars-Abschnitt der Skin-Definitionsdatei muss mit der folgenden Zeile beginnen:</span><span class="sxs-lookup"><span data-stu-id="885da-113">The Trackbars section of the skin definition file must begin with this line:</span></span>


```C++
[ Trackbars ]

```



<span data-ttu-id="885da-114">Anschließend müssen Sie eine oder mehrere Zeilen hinzufügen, die Informationen zu den einzelnen trackbars in der Skin enthalten.</span><span class="sxs-lookup"><span data-stu-id="885da-114">You then must add one or more lines that contain information about each of the trackbars in your skin.</span></span>


```C++
    Seek        5,25,226,17    Disabled @ 4,1      SeekThumb.bmp      18,17
    Volume      32,220,172,23  Disabled @ 32,27    VolumeThumb.bmp    23,22

```



<span data-ttu-id="885da-115">Sie können die folgende Vorlage für den trackbars-Abschnitt Ihrer Skin-Definitionsdatei verwenden:</span><span class="sxs-lookup"><span data-stu-id="885da-115">You can use the following template for the Trackbars section of your skin definition file:</span></span>


```C++
//  <Type> <Location>     <Dis Image Src> <Thumb Image Src> <Thumb Size>
//  ------ ----------     --------------- ----------------- ------------

```



<span data-ttu-id="885da-116">Sie müssen die folgende Reihenfolge für die TrackBar-Informationen für jede Zeile im Abschnitt trackbars verwenden (jeder Teil der Zeile ist erforderlich):</span><span class="sxs-lookup"><span data-stu-id="885da-116">You must use the following order for trackbar information for each line in the Trackbars section (each part of the line is required):</span></span>

1.  [<span data-ttu-id="885da-117">TrackBar-Typ</span><span class="sxs-lookup"><span data-stu-id="885da-117">Trackbar Type</span></span>](trackbar-type.md)
2.  [<span data-ttu-id="885da-118">Position der TrackBar</span><span class="sxs-lookup"><span data-stu-id="885da-118">Trackbar Location</span></span>](trackbar-location.md)
3.  [<span data-ttu-id="885da-119">Bildquelle für deaktivierte TrackBar</span><span class="sxs-lookup"><span data-stu-id="885da-119">Image Source for Disabled Trackbar</span></span>](image-source-for-disabled-trackbar.md)
4.  [<span data-ttu-id="885da-120">Ziehpunkt Bildquelle</span><span class="sxs-lookup"><span data-stu-id="885da-120">Thumb Image Source</span></span>](thumb-image-source.md)
5.  [<span data-ttu-id="885da-121">Thumb-Größe</span><span class="sxs-lookup"><span data-stu-id="885da-121">Thumb Size</span></span>](thumb-size.md)

<span data-ttu-id="885da-122">Ein Beispiel für trackbars-Code finden Sie im [Abschnitt "Beispiel trackbars](sample-trackbars-section.md)".</span><span class="sxs-lookup"><span data-stu-id="885da-122">For an example of Trackbars code, see [Sample Trackbars Section](sample-trackbars-section.md).</span></span>

## <a name="related-topics"></a><span data-ttu-id="885da-123">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="885da-123">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="885da-124">**Skin-Referenz**</span><span class="sxs-lookup"><span data-stu-id="885da-124">**Skin Reference**</span></span>](skin-reference.md)
</dt> </dl>

 

 




