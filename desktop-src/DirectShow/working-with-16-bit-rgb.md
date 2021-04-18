---
description: Arbeiten mit 16-Bit-RGB
ms.assetid: 0a245187-4120-4003-9a8f-6b1e8fa40d38
title: Arbeiten mit 16-Bit-RGB
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3f6bf4b3217af4d0261d4ab26ca011881762a2a7
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106347418"
---
# <a name="working-with-16-bit-rgb"></a><span data-ttu-id="c7807-103">Arbeiten mit 16-Bit-RGB</span><span class="sxs-lookup"><span data-stu-id="c7807-103">Working with 16-bit RGB</span></span>

<span data-ttu-id="c7807-104">Zwei Formate sind für 16-Bit-unkomprimierte RGB definiert:</span><span class="sxs-lookup"><span data-stu-id="c7807-104">Two formats are defined for 16-bit uncompressed RGB:</span></span>

-   <span data-ttu-id="c7807-105">Mediasubtype \_ 555 verwendet jeweils fünf Bits für die roten, grünen und blauen Komponenten in einem Pixel.</span><span class="sxs-lookup"><span data-stu-id="c7807-105">MEDIASUBTYPE\_555 uses five bits each for the red, green, and blue components in a pixel.</span></span> <span data-ttu-id="c7807-106">Das signifikanteste Bit im **Wort** wird ignoriert.</span><span class="sxs-lookup"><span data-stu-id="c7807-106">The most significant bit in the **WORD** is ignored.</span></span>
-   <span data-ttu-id="c7807-107">Mediasubtype \_ 565 verwendet fünf Bits für die roten und blauen Komponenten und sechs Bits für die grüne Komponente.</span><span class="sxs-lookup"><span data-stu-id="c7807-107">MEDIASUBTYPE\_565 uses five bits for the red and blue components, and six bits for the green component.</span></span> <span data-ttu-id="c7807-108">Dieses Format spiegelt die Tatsache wider, dass die menschliche Vision für die grünen Teile des sichtbaren Spektrums am empfindlichsten ist.</span><span class="sxs-lookup"><span data-stu-id="c7807-108">This format reflects the fact that human vision is most sensitive to the green portions of the visible spectrum.</span></span>

<span data-ttu-id="c7807-109">**RGB 565**</span><span class="sxs-lookup"><span data-stu-id="c7807-109">**RGB 565**</span></span>

<span data-ttu-id="c7807-110">Wenn Sie die Farbkomponenten aus einem RGB-565-Image extrahieren möchten, behandeln Sie jedes Pixel als **Worttyp** , und verwenden Sie die folgenden Bitmasken:</span><span class="sxs-lookup"><span data-stu-id="c7807-110">To extract the color components from an RGB 565 image, treat each pixel as a **WORD** type and use the following bit masks:</span></span>


```C++
WORD red_mask = 0xF800;
WORD green_mask = 0x7E0;
WORD blue_mask = 0x1F;
```



<span data-ttu-id="c7807-111">Nehmen Sie die Farbkomponenten aus einem Pixel wie folgt:</span><span class="sxs-lookup"><span data-stu-id="c7807-111">Get the color components from a pixel as follows:</span></span>


```C++
BYTE red_value = (pixel & red_mask) >> 11;
BYTE green_value = (pixel & green_mask) >> 5;
BYTE blue_value = (pixel & blue_mask);
```



<span data-ttu-id="c7807-112">Beachten Sie, dass die roten und blauen Kanäle 5 Bits und der grüne Kanal 6 Bits sind.</span><span class="sxs-lookup"><span data-stu-id="c7807-112">Remember that the red and blue channels are 5 bits and the green channel is 6 bits.</span></span> <span data-ttu-id="c7807-113">Um diese Werte in 8-Bit-Komponenten (24-Bit-oder 32-Bit-RGB) zu konvertieren, müssen Sie die entsprechende Anzahl von Bits nach links verschieben:</span><span class="sxs-lookup"><span data-stu-id="c7807-113">To convert these values to 8-bit components (for 24-bit or 32-bit RGB), you must left-shift the appropriate number of bits:</span></span>


```C++
// Expand to 8-bit values.
BYTE red   = red_value << 3;
BYTE green = green_value << 2;
BYTE blue  = blue_value << 3;
```



<span data-ttu-id="c7807-114">Umkehren Sie diesen Prozess, um ein RGB-565-Pixel zu erstellen.</span><span class="sxs-lookup"><span data-stu-id="c7807-114">Reverse this process to create an RGB 565 pixel.</span></span> <span data-ttu-id="c7807-115">Angenommen, die Farbwerte wurden auf die richtige Anzahl von Bits gekürzt:</span><span class="sxs-lookup"><span data-stu-id="c7807-115">Assuming the color values have been truncated to the correct number of bits:</span></span>


```C++
WORD pixel565 = (red_value << 11) | (green_value << 5) | blue_value;
```



<span data-ttu-id="c7807-116">**RGB 555**</span><span class="sxs-lookup"><span data-stu-id="c7807-116">**RGB 555**</span></span>

<span data-ttu-id="c7807-117">Das Arbeiten mit RGB 555 ist im Wesentlichen mit RGB 565 identisch, mit der Ausnahme, dass Bitmasken und Bitverschiebungs Vorgänge unterschiedlich sind.</span><span class="sxs-lookup"><span data-stu-id="c7807-117">Working with RGB 555 is essentially the same as RGB 565, except the bit masks and bit shift operations are different.</span></span> <span data-ttu-id="c7807-118">Gehen Sie folgendermaßen vor, um die Farbkomponenten aus einem RGB-555-Pixel zu erhalten:</span><span class="sxs-lookup"><span data-stu-id="c7807-118">To get the color components from an RGB 555 pixel, do the following:</span></span>


```C++
WORD red_mask = 0x7C00;
WORD green_mask = 0x3E0;
WORD blue_mask = 0x1F;

BYTE red_value = (pixel & red_mask) >> 10;
BYTE green_value = (pixel & green_mask) >> 5;
BYTE blue_value = (pixel & blue_mask);

// Expand to 8-bit values:
BYTE red   = red_value << 3;
BYTE green = green_value << 3;
BYTE blue  = blue_value << 3;
```



<span data-ttu-id="c7807-119">Gehen Sie folgendermaßen vor, um die roten, grünen und blauen Farbwerte in ein RGB-555-Pixel zu packen:</span><span class="sxs-lookup"><span data-stu-id="c7807-119">To pack the red, green, and blue color values into an RGB 555 pixel, do the following:</span></span>


```C++
WORD pixel565 = (red << 10) | (green << 5) | blue;
```



## <a name="related-topics"></a><span data-ttu-id="c7807-120">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="c7807-120">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="c7807-121">Unkomprimierte RGB-Video Untertypen</span><span class="sxs-lookup"><span data-stu-id="c7807-121">Uncompressed RGB Video Subtypes</span></span>](uncompressed-rgb-video-subtypes.md)
</dt> </dl>

 

 



