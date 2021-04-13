---
title: Bildquelle für deaktivierte Schaltfläche
description: Bildquelle für deaktivierte Schaltfläche
ms.assetid: 6c50e0bd-c174-4335-8d34-ae25feec9ec6
keywords:
- Windows Media Player Mobile Skins, Schaltflächen Bildquelle
- Skins, Schaltflächen Bildquelle
- Verweis für Skins, Schaltflächen
- Schaltflächen in Skins, Bildquelle
- Bildquelle für Skins, Schaltflächen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d05ccd0362f3dd11acec71eaf0b92574f2c27c77
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "104388334"
---
# <a name="image-source-for-disabled-button"></a><span data-ttu-id="90229-108">Bildquelle für deaktivierte Schaltfläche</span><span class="sxs-lookup"><span data-stu-id="90229-108">Image Source for Disabled Button</span></span>

<span data-ttu-id="90229-109">Sie müssen die Quelle des Abbilds definieren, das angezeigt werden soll, wenn eine Schaltfläche deaktiviert ist oder einen Zustand aufweist, der auf OFF festgelegt ist.</span><span class="sxs-lookup"><span data-stu-id="90229-109">You must define the source of the image you want to display when a button is disabled or has a state that corresponds to off.</span></span> <span data-ttu-id="90229-110">Das Bild stammt aus der Datei, die Sie im Abschnitt Bitmaps als deaktiviert definiert haben.</span><span class="sxs-lookup"><span data-stu-id="90229-110">The image comes from the file you defined as Disabled in the Bitmaps section.</span></span> <span data-ttu-id="90229-111">Sie müssen den Bildtyp gefolgt von einem Leerzeichen und dem @-Symbol und einem weiteren Leerzeichen eingeben.</span><span class="sxs-lookup"><span data-stu-id="90229-111">You must enter the image type followed by a space and the @ symbol and another space.</span></span> <span data-ttu-id="90229-112">Sie müssen dann zwei positive ganze Zahlen eingeben, die die oberen linken Koordinaten (in Pixel) des Bilds definieren, das Sie in der Bitmapdatei verwenden möchten.</span><span class="sxs-lookup"><span data-stu-id="90229-112">You must then enter two positive integers that define the top-left coordinates (in pixels) of the image you want to use inside the bitmap file.</span></span> <span data-ttu-id="90229-113">Der Speicherort, an dem das Bild angezeigt wird, stammt aus den Koordinaten, die für die Schaltfläche relativ zum Hintergrundbild definiert sind, aber der Speicherort, von dem Sie stammt, wird durch die beiden Zahlen definiert, die nach "deaktiviertem @" stehen, und ist relativ zur deaktivierten Bitmap, aus der das Bild</span><span class="sxs-lookup"><span data-stu-id="90229-113">The location at which the image will be displayed comes from the coordinates defined for the button relative to the Background image, but the location it comes from is defined by the two numbers following "Disabled @" and is relative to the Disabled bitmap you are reading the image from.</span></span>

<span data-ttu-id="90229-114">Verwenden Sie z. b. den folgenden Code, um ein Bild aus der deaktivierten Bitmap zu verwenden, das sich in der deaktivierten Datei an einer oberen und linken Position von 50, 60 Pixeln befindet:</span><span class="sxs-lookup"><span data-stu-id="90229-114">For example, to use an image from the Disabled bitmap that is in the Disabled file at a top and left location of 50,60 pixels, use the following code:</span></span>


```C++
Disabled @ 50,60

```



<span data-ttu-id="90229-115">Sie müssen eine deaktivierte Bitmap definieren.</span><span class="sxs-lookup"><span data-stu-id="90229-115">You must define a Disabled bitmap.</span></span> <span data-ttu-id="90229-116">Wenn Sie kein anderes Bild anzeigen möchten, können Sie die Hintergrund Bitmap als deaktivierte Bitmap mit einem Offset von 0 (null) definieren:</span><span class="sxs-lookup"><span data-stu-id="90229-116">If you do not want to display a different image, you can define the Background bitmap as your Disabled bitmap with an offset of 0,0:</span></span>


```C++
Disabled @ 50,60

```



<span data-ttu-id="90229-117">Im vorherigen Beispiel ist 50, 60 der Speicherort der Schaltfläche, mit der Sie in der deaktivierten Datei arbeiten (in diesem Fall der gleiche Speicherort wie die Schaltfläche auf der Hintergrund Bitmap).</span><span class="sxs-lookup"><span data-stu-id="90229-117">In the preceding example, 50,60 is the location of the button you are working with in the Disabled file (in this case, the same location as the button on the Background bitmap).</span></span> <span data-ttu-id="90229-118">Es wird jedoch dringend empfohlen, dass Sie ein deaktiviertes Bild für alle Schaltflächen anzeigen, um Ihren Benutzern einen visuellen Hinweis zu geben, da viele Schaltflächen unter bestimmten Bedingungen nicht verwendbar sind, wie z. b. eine leere Wiedergabeliste.</span><span class="sxs-lookup"><span data-stu-id="90229-118">However, it is highly recommended that you display a Disabled image for all buttons to give your users a visual indication, because many buttons will not be useable under certain conditions, such as an empty playlist.</span></span> <span data-ttu-id="90229-119">Wenn Benutzer wissen, dass eine Schaltfläche deaktiviert ist, versuchen Sie nicht, darauf zu klicken, oder denken Sie daran, dass Ihre Skin nicht wie vorgesehen funktioniert.</span><span class="sxs-lookup"><span data-stu-id="90229-119">If users know a button is disabled, they will not keep trying to click on it or think your skin is not functioning as designed.</span></span>

## <a name="related-topics"></a><span data-ttu-id="90229-120">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="90229-120">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="90229-121">**Schaltflächen**</span><span class="sxs-lookup"><span data-stu-id="90229-121">**Buttons**</span></span>](buttons.md)
</dt> </dl>

 

 




