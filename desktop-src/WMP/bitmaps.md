---
title: Bitmaps (Windows Media Player SDK)
description: Bitmaps
ms.assetid: cd10bc7d-1167-485e-8acf-13c021bc608b
keywords:
- Windows Media Player Mobile Skins, Bitmaps
- Skins, Bitmaps
- Verweis für Skins, Bitmaps
- Bitmaps in Skins, Info
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 15ad690b691c22154bad4db0981e2b5ab760400b
ms.sourcegitcommit: 8fa6614b715bddf14648cce36d2df22e5232801a
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/10/2020
ms.locfileid: "104474763"
---
# <a name="bitmaps-windows-media-player-sdk"></a><span data-ttu-id="b6bc3-107">Bitmaps (Windows Media Player SDK)</span><span class="sxs-lookup"><span data-stu-id="b6bc3-107">Bitmaps (Windows Media Player SDK)</span></span>

<span data-ttu-id="b6bc3-108">Sie müssen ein oder mehrere Bilder in der Skin verwenden, und jedes Image muss in der Skin-Definitionsdatei definiert werden.</span><span class="sxs-lookup"><span data-stu-id="b6bc3-108">You must use one or more images in your skin, and each image must be defined in the skin definition file.</span></span> <span data-ttu-id="b6bc3-109">Wenn Sie in diesem Abschnitt kein Bild definieren, kann es von der Skin nicht verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="b6bc3-109">If you do not define an image in this section, your skin will not be able to use it.</span></span>

<span data-ttu-id="b6bc3-110">Der Begriff "Bitmap" wird in einem generischen Sinn in der gesamten Referenz verwendet und bezieht sich auf Bitmap-Bilder mit der Erweiterung. BMP, GIF-Bilder mit der Erweiterung GIF, JPEG-Bilder mit der Erweiterung JPG und PNG-Bilder mit der Erweiterung PNG.</span><span class="sxs-lookup"><span data-stu-id="b6bc3-110">The term "bitmap" is used throughout the reference in a generic sense, and refers to bitmap images with a .bmp extension, GIF images with a .gif extension, JPEG images with a .jpg extension, and PNG images with a .png extension.</span></span>

<span data-ttu-id="b6bc3-111">Der Bitmaps-Abschnitt der Skin-Definitionsdatei beginnt mit der folgenden Zeile:</span><span class="sxs-lookup"><span data-stu-id="b6bc3-111">The Bitmaps section of the skin definition file begins with this line:</span></span>


```C++
[ Bitmaps ]

```



<span data-ttu-id="b6bc3-112">Anschließend müssen Sie eine oder mehrere Zeilen hinzufügen, die Informationen zu den einzelnen Bildern in der Skin enthalten.</span><span class="sxs-lookup"><span data-stu-id="b6bc3-112">You then must add one or more lines that contain information about each of the images in your skin.</span></span>

<span data-ttu-id="b6bc3-113">Eine typische Zeile könnte wie folgt lauten:</span><span class="sxs-lookup"><span data-stu-id="b6bc3-113">A typical line might be:</span></span>


```C++
    Background  Background.bmp  0,0

```



<span data-ttu-id="b6bc3-114">Sie können die folgende Vorlage für den Bitmaps-Abschnitt Ihrer Skin-Definitionsdatei verwenden:</span><span class="sxs-lookup"><span data-stu-id="b6bc3-114">You can use the following template for the Bitmaps section of your skin definition file:</span></span>


```C++
//  <Type>      <Filename>      <X,Y>
//  ------      -----------     -----

```



<span data-ttu-id="b6bc3-115">Sie müssen die folgende Reihenfolge für Bitmapinformationen für jede Zeile im Bitmap-Abschnitt verwenden.</span><span class="sxs-lookup"><span data-stu-id="b6bc3-115">You must use the following order for bitmap information for each line in the Bitmap section.</span></span> <span data-ttu-id="b6bc3-116">Jeder Teil der Zeile ist erforderlich.</span><span class="sxs-lookup"><span data-stu-id="b6bc3-116">Each part of the line is required.</span></span>

1.  [<span data-ttu-id="b6bc3-117">Bitmaptyp</span><span class="sxs-lookup"><span data-stu-id="b6bc3-117">Bitmap Type</span></span>](bitmap-type.md)
2.  [<span data-ttu-id="b6bc3-118">Dateiname</span><span class="sxs-lookup"><span data-stu-id="b6bc3-118">File Name</span></span>](file-name.md)
3.  [<span data-ttu-id="b6bc3-119">Koordinaten</span><span class="sxs-lookup"><span data-stu-id="b6bc3-119">Coordinates</span></span>](coordinates.md)

<span data-ttu-id="b6bc3-120">Ein Beispiel für einen bitmapcode finden Sie unter [Sample Bitmap section](sample-bitmap-section.md).</span><span class="sxs-lookup"><span data-stu-id="b6bc3-120">For an example of bitmap code, see [Sample Bitmap Section](sample-bitmap-section.md).</span></span>

## <a name="related-topics"></a><span data-ttu-id="b6bc3-121">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="b6bc3-121">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="b6bc3-122">**Skin-Referenz**</span><span class="sxs-lookup"><span data-stu-id="b6bc3-122">**Skin Reference**</span></span>](skin-reference.md)
</dt> </dl>

 

 




