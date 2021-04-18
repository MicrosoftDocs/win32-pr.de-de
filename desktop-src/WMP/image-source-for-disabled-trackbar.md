---
title: Bildquelle für deaktivierte TrackBar
description: Bildquelle für deaktivierte TrackBar
ms.assetid: ecbe1670-2914-4b66-92bd-d854e6c1e897
keywords:
- Windows Media Player Mobile Skins, trackbars
- Skins, trackbars
- Verweis für Skins, trackbars
- trackbars in Skins, Bildquelle
- Bildquelle für Skins, trackbars
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: fbae540f97c7d1f7241035b074f45e6267e51615
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "106337988"
---
# <a name="image-source-for-disabled-trackbar"></a><span data-ttu-id="7317c-108">Bildquelle für deaktivierte TrackBar</span><span class="sxs-lookup"><span data-stu-id="7317c-108">Image Source for Disabled Trackbar</span></span>

<span data-ttu-id="7317c-109">Sie müssen die Quelle des Bilds definieren, das Sie anzeigen möchten, wenn eine TrackBar deaktiviert ist. verwenden Sie dazu den Bitmaptyp, aus dem das Bild gezeichnet werden soll.</span><span class="sxs-lookup"><span data-stu-id="7317c-109">You must define the source of the image you want to display when a trackbar is disabled, using the bitmap type you want to draw the image from.</span></span> <span data-ttu-id="7317c-110">Das Bild, das Sie anzeigen, befindet sich in der Regel in der Super Datei, oder wenn Sie ein Skin für Windows Media Player 10 Mobile erstellen, befindet sich das Bild in der seekthumb-Datei.</span><span class="sxs-lookup"><span data-stu-id="7317c-110">The image you display will usually be inside the Super file or if you are creating a skin for Windows Media Player 10 Mobile, the image would be inside the SeekThumb file.</span></span> <span data-ttu-id="7317c-111">Sie müssen den Bildtyp gefolgt von einem Leerzeichen und dem @-Symbol und einem weiteren Leerzeichen eingeben.</span><span class="sxs-lookup"><span data-stu-id="7317c-111">You must enter the image type followed by a space and the @ symbol and another space.</span></span> <span data-ttu-id="7317c-112">Sie müssen dann zwei positive ganze Zahlen eingeben, die die oberen linken Koordinaten (in Pixel) des Bilds definieren, das Sie in den zu zeichnenden Bitmaptyp verwenden möchten.</span><span class="sxs-lookup"><span data-stu-id="7317c-112">You must then enter two positive integers that define the top-left coordinates (in pixels) of the image you want to use inside the bitmap type you are drawing from.</span></span>

<span data-ttu-id="7317c-113">Wenn Sie z. b. ein Bild aus der seekthumb-Bitmap mit einer oberen und linken Position von 50, 60 Pixeln verwenden möchten, geben Sie Folgendes ein:</span><span class="sxs-lookup"><span data-stu-id="7317c-113">For example, to use an image from the SeekThumb bitmap that has a top and left position of 50,60 pixels, type:</span></span>


```C++
Disabled @ 50,60

```



<span data-ttu-id="7317c-114">Sie müssen einen bildort für ein deaktiviertes TrackBar-Bild definieren.</span><span class="sxs-lookup"><span data-stu-id="7317c-114">You must define an image location for a disabled trackbar image.</span></span> <span data-ttu-id="7317c-115">Wenn Sie kein neues Bild anzeigen möchten, können Sie das Hintergrundbild als deaktiviertes Bild mit einem Offset von 0 (null) definieren:</span><span class="sxs-lookup"><span data-stu-id="7317c-115">If you do not want to display a new image, you can define the Background image as your Disabled image with an offset of 0,0:</span></span>


```C++
Disabled @ 50,60

```



<span data-ttu-id="7317c-116">Im vorherigen Beispiel stellt 50, 60 den Speicherort der Schaltfläche dar, mit der Sie in der seekthumb-Datei arbeiten (in diesem Fall die gleiche Position wie die Schaltfläche auf der Hintergrund Bitmap).</span><span class="sxs-lookup"><span data-stu-id="7317c-116">In the preceding example, 50,60 represents the location of the button you are working with in the SeekThumb file (in this case, the same location as the button on the Background bitmap).</span></span> <span data-ttu-id="7317c-117">Es wird jedoch dringend empfohlen, ein deaktiviertes Bild für alle trackbars anzuzeigen, um dem Benutzer einen visuellen Hinweis zu geben, da trackbars unter bestimmten Bedingungen nicht verwendbar sind.</span><span class="sxs-lookup"><span data-stu-id="7317c-117">However, it is highly recommended that you display a Disabled image for all trackbars to give your user a visual indication, because trackbars will not be useable under certain conditions.</span></span> <span data-ttu-id="7317c-118">Beispielsweise können Such trackbars deaktiviert werden, wenn die aktuelle Wiedergabeliste leer ist.</span><span class="sxs-lookup"><span data-stu-id="7317c-118">For example, Seek trackbars may be disabled when the current playlist is empty.</span></span>

## <a name="related-topics"></a><span data-ttu-id="7317c-119">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="7317c-119">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="7317c-120">**Trackbars**</span><span class="sxs-lookup"><span data-stu-id="7317c-120">**Trackbars**</span></span>](trackbars.md)
</dt> </dl>

 

 




