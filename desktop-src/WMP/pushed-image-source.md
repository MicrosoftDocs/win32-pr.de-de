---
title: Bildquelle mit pushübertragung
description: Bildquelle mit pushübertragung
ms.assetid: 6cc290d8-2c15-4789-970d-9a3663a64d08
keywords:
- Windows Media Player Mobile Skins, Schaltflächen Bildquelle
- Skins, Schaltflächen Bildquelle
- Verweis für Skins, Schaltflächen
- Schaltflächen in Skins, Bildquelle
- Bildquelle für Skins, Schaltflächen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 021c77a305e0f6981823c8a1e471862554c32e08
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "103711555"
---
# <a name="pushed-image-source"></a><span data-ttu-id="ae7aa-108">Bildquelle mit pushübertragung</span><span class="sxs-lookup"><span data-stu-id="ae7aa-108">Pushed Image Source</span></span>

<span data-ttu-id="ae7aa-109">Sie müssen die Quelle des Bilds definieren, das Sie anzeigen möchten, wenn der Benutzer eine Schaltfläche drückt.</span><span class="sxs-lookup"><span data-stu-id="ae7aa-109">You must define the source of the image you want to display when the user pushes a button.</span></span> <span data-ttu-id="ae7aa-110">Das Bild stammt aus der Datei, die Sie im Abschnitt Bitmaps als per pushübertragung definiert haben.</span><span class="sxs-lookup"><span data-stu-id="ae7aa-110">The image comes from the file you defined as Pushed in the Bitmaps section.</span></span> <span data-ttu-id="ae7aa-111">Sie müssen den Bildtyp gefolgt von einem Leerzeichen und dem @-Symbol und einem weiteren Leerzeichen eingeben.</span><span class="sxs-lookup"><span data-stu-id="ae7aa-111">You must enter the image type followed by a space and the @ symbol and another space.</span></span> <span data-ttu-id="ae7aa-112">Sie müssen dann zwei positive ganze Zahlen eingeben, die die oberen und linken Koordinaten (in Pixel) des Bilds definieren, das Sie in der Datei mit dem pushbild verwenden möchten.</span><span class="sxs-lookup"><span data-stu-id="ae7aa-112">You must then enter two positive integers that define the top and left coordinates (in pixels) of the image you want to use inside the Pushed image file.</span></span> <span data-ttu-id="ae7aa-113">Die Position, an der das Bild angezeigt wird, stammt aus den Koordinaten, die für die Schaltfläche relativ zum Hintergrundbild definiert sind. der Speicherort, von dem Sie stammt, wird jedoch durch die beiden Zahlen definiert, die auf "gedrücktes @" folgen</span><span class="sxs-lookup"><span data-stu-id="ae7aa-113">The location at which the image will be displayed comes from the coordinates defined for the button relative to the Background image; but the location it comes from is defined by the two numbers following "Pushed @" and is relative to the Pushed image you are reading the image from.</span></span>

<span data-ttu-id="ae7aa-114">Wenn Sie z. b. ein Bild aus dem gedrückten Bild verwenden möchten, das sich in der über drückten Datei befindet, deren Links oben links ist, verwenden Sie den folgenden Code:</span><span class="sxs-lookup"><span data-stu-id="ae7aa-114">For example, to use an image from the Pushed image that is in the Pushed file whose top-left location is 50,60 you would use the following code:</span></span>


```C++
Pushed @ 50,60

```



<span data-ttu-id="ae7aa-115">Wenn Sie kein anderes Bild anzeigen möchten, können Sie die Bitmap des Hintergrunds als pushbitmap definieren.</span><span class="sxs-lookup"><span data-stu-id="ae7aa-115">If you do not want to display a different image, you can define the Background bitmap as your Pushed bitmap.</span></span> <span data-ttu-id="ae7aa-116">Geben Sie hierzu die Hintergrund Datei als die übersetzte Datei an, und geben Sie den Offset in der oberen linken Ecke der Schaltfläche an:</span><span class="sxs-lookup"><span data-stu-id="ae7aa-116">To do this, specify the Background file as your pushed file and specify the offset to the top-left corner of the button:</span></span>


```C++
Pushed @ 50,60

```



<span data-ttu-id="ae7aa-117">Wenn Sie dies tun, kann keine der Schaltflächen ein gedrücktes Bild anzeigen.</span><span class="sxs-lookup"><span data-stu-id="ae7aa-117">If you do this, none of your buttons can display a Pushed image.</span></span> <span data-ttu-id="ae7aa-118">Es wird empfohlen, ein gedrücktes Bild für alle Schaltflächen anzuzeigen, um dem Benutzer einen visuellen Hinweis zu geben, denn es ist nicht immer klar, ob ein TAP ein Ergebnis liefert, insbesondere wenn Musik abgespielt wird oder der Bildschirm für das Tippen ausgeschaltet ist.</span><span class="sxs-lookup"><span data-stu-id="ae7aa-118">We recommend that you display a Pushed image for all buttons to give your user a visual indication, because it is not always clear whether a tap produces a result, especially when music is playing or the tapping sound is turned off.</span></span>

## <a name="related-topics"></a><span data-ttu-id="ae7aa-119">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="ae7aa-119">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="ae7aa-120">**Schaltflächen**</span><span class="sxs-lookup"><span data-stu-id="ae7aa-120">**Buttons**</span></span>](buttons.md)
</dt> </dl>

 

 




