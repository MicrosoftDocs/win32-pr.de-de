---
description: In Direct3D werden alle zweidimensionalen (2D) Bilder durch einen linearen Bereich von Speicher dargestellt, der als Oberfläche bezeichnet wird.
ms.assetid: 33430f01-cd26-45f4-9ce8-ca2c17c7ae6b
title: Oberflächen Formate (Direct3D 9)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 78aad64940510a080ba05d0513e7f66d33912a41
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/06/2021
ms.locfileid: "104124813"
---
# <a name="surface-formats-direct3d-9"></a><span data-ttu-id="9247c-103">Oberflächen Formate (Direct3D 9)</span><span class="sxs-lookup"><span data-stu-id="9247c-103">Surface Formats (Direct3D 9)</span></span>

<span data-ttu-id="9247c-104">In Direct3D werden alle zweidimensionalen (2D) Bilder durch einen linearen Bereich von Speicher dargestellt, der als Oberfläche bezeichnet wird.</span><span class="sxs-lookup"><span data-stu-id="9247c-104">In Direct3D, all two-dimensional (2D) images are represented by a linear range of memory called a surface.</span></span> <span data-ttu-id="9247c-105">Eine Oberfläche kann als 2D-Array betrachtet werden, wobei jedes Element einen Farbwert enthält, der einen kleinen Abschnitt des Bilds darstellt, der als Pixel bezeichnet wird.</span><span class="sxs-lookup"><span data-stu-id="9247c-105">A surface can be thought of as a 2D array where each element holds a color value representing a small section of the image, called a pixel.</span></span> <span data-ttu-id="9247c-106">Die Detailebene eines Bilds wird sowohl durch die Anzahl der Pixel, die zum Darstellen des Bilds benötigt werden, als auch durch die Anzahl der Bits definiert, die für das Farbspektrum des Bilds benötigt werden.</span><span class="sxs-lookup"><span data-stu-id="9247c-106">An image's detail level is defined by both the number of pixels needed to represent the image, and the number of bits needed for the image's color spectrum.</span></span> <span data-ttu-id="9247c-107">Beispielsweise wird ein Bild, das 800 Pixel breit und 600 Pixel hoch und 32 Bits Farben für jedes Pixel ist (als 800x600x32 geschrieben), ausführlicher als ein Bild mit einer Breite 480 von 640 Pixel und einer Höhe von jeweils 16 Bits pro Pixel (als 640 x480x16 geschrieben) dargestellt.</span><span class="sxs-lookup"><span data-stu-id="9247c-107">For example, an image that is 800 pixels wide by 600 pixels high with 32 bits of color for each pixel (written as 800x600x32) will be more detailed than an image that is 640 pixels wide by 480 pixels tall with 16 bits of color for each pixel (written as 640x480x16).</span></span> <span data-ttu-id="9247c-108">Entsprechend ist für das ausführlichere Bild eine größere Oberfläche erforderlich, um die Daten zu speichern.</span><span class="sxs-lookup"><span data-stu-id="9247c-108">Likewise, the more detailed image will require a larger surface to store the data.</span></span> <span data-ttu-id="9247c-109">Bei einem 800x600x32-Bild sind die Array Dimensionen der Oberfläche 800x600, und jedes Element enthält einen 32-Bit-Wert, der seine Farbe darstellt.</span><span class="sxs-lookup"><span data-stu-id="9247c-109">For an 800x600x32 image, the surface's array dimensions will be 800x600, and each element will hold a 32-bit value to represent its color.</span></span>

<span data-ttu-id="9247c-110">Alle Oberflächen verfügen über eine Größe und speichern eine bestimmte Anzahl von Bits, die Farbe darstellen.</span><span class="sxs-lookup"><span data-stu-id="9247c-110">All surfaces have a size and store a specific number of bits that represent color.</span></span> <span data-ttu-id="9247c-111">Die Bits, die die Farbe darstellen, werden in einzelne Farbelemente aufgeteilt: rot, grün und blau.</span><span class="sxs-lookup"><span data-stu-id="9247c-111">The bits that represent color are separated into individual color elements: red, green, and blue.</span></span> <span data-ttu-id="9247c-112">In Direct3D werden alle Color-Elemente durch den [D3DFORMAT](d3dformat.md) -enumerierten Typ definiert.</span><span class="sxs-lookup"><span data-stu-id="9247c-112">In Direct3D all color elements are defined by the [D3DFORMAT](d3dformat.md) enumerated type.</span></span> <span data-ttu-id="9247c-113">Ein Direct3D-Farb Format wird in die Anzahl der für die einzelnen Farben reservierten Byes aufgeteilt.</span><span class="sxs-lookup"><span data-stu-id="9247c-113">A Direct3D color format is broken down into the number of byes reserved for each color.</span></span> <span data-ttu-id="9247c-114">Beispielsweise wird ein 16-Bit-Farb Format in Direct3D als D3DFMT \_ R5G6B5 definiert, wobei 5 Bits für Rot (R), 6 Bits für Grün (G) und 5 Bits für blau (B) reserviert sind.</span><span class="sxs-lookup"><span data-stu-id="9247c-114">For example, a 16-bit color format in Direct3D is defined as D3DFMT\_R5G6B5, where 5 bits are reserved for red (R), 6 bits for green (G), and 5 bits for blue (B).</span></span>

## <a name="related-topics"></a><span data-ttu-id="9247c-115">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="9247c-115">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="9247c-116">Direct3D-Oberflächen</span><span class="sxs-lookup"><span data-stu-id="9247c-116">Direct3D Surfaces</span></span>](direct3d-surfaces.md)
</dt> </dl>

 

 



