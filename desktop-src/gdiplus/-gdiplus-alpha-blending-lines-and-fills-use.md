---
description: In Windows GDI+ ist eine Farbe ein 32-Bit-Wert mit 8 Bits für Alpha, rot, grün und blau.
ms.assetid: f8c22d1a-b96b-4d16-928e-20adbae4c4a7
title: Alphablending von Linien und Füllungen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: dd13fe306dbf31c2a60a0bd38bf71b9e96edb201
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "103864284"
---
# <a name="alpha-blending-lines-and-fills"></a><span data-ttu-id="8b69b-103">Alphablending von Linien und Füllungen</span><span class="sxs-lookup"><span data-stu-id="8b69b-103">Alpha Blending Lines and Fills</span></span>

<span data-ttu-id="8b69b-104">In Windows GDI+ ist eine Farbe ein 32-Bit-Wert mit 8 Bits für Alpha, rot, grün und blau.</span><span class="sxs-lookup"><span data-stu-id="8b69b-104">In Windows GDI+, a color is a 32-bit value with 8 bits each for alpha, red, green, and blue.</span></span> <span data-ttu-id="8b69b-105">Der Alpha-Wert gibt die Transparenz der Farbe an – das Ausmaß, in dem die Farbe mit der Hintergrundfarbe gemischt wird.</span><span class="sxs-lookup"><span data-stu-id="8b69b-105">The alpha value indicates the transparency of the color — the extent to which the color is blended with the background color.</span></span> <span data-ttu-id="8b69b-106">Alpha Werte reichen von 0 bis 255, wobei 0 eine vollständig transparente Farbe darstellt und 255 eine vollständig nicht transparente Farbe darstellt.</span><span class="sxs-lookup"><span data-stu-id="8b69b-106">Alpha values range from 0 through 255, where 0 represents a fully transparent color, and 255 represents a fully opaque color.</span></span>

<span data-ttu-id="8b69b-107">Alpha Blending ist eine pixelweise Mischung aus Quell-und Hintergrund Farbdaten.</span><span class="sxs-lookup"><span data-stu-id="8b69b-107">Alpha blending is a pixel-by-pixel blending of source and background color data.</span></span> <span data-ttu-id="8b69b-108">Jede der drei Komponenten (rot, grün, blau) einer angegebenen Quellfarbe wird mit der entsprechenden Komponente der Hintergrundfarbe entsprechend der folgenden Formel gemischt:</span><span class="sxs-lookup"><span data-stu-id="8b69b-108">Each of the three components (red, green, blue) of a given source color is blended with the corresponding component of the background color according to the following formula:</span></span>

<span data-ttu-id="8b69b-109">Display Color = sourcecolor × Alpha/255 + BackgroundColor × (255 – Alpha)/255</span><span class="sxs-lookup"><span data-stu-id="8b69b-109">displayColor = sourceColor × alpha / 255 + backgroundColor × (255 – alpha) / 255</span></span>

<span data-ttu-id="8b69b-110">Nehmen wir beispielsweise an, die rote Komponente der Quellfarbe ist 150, und die rote Komponente der Hintergrundfarbe ist 100.</span><span class="sxs-lookup"><span data-stu-id="8b69b-110">For example, suppose the red component of the source color is 150 and the red component of the background color is 100.</span></span> <span data-ttu-id="8b69b-111">Wenn der Alpha-Wert 200 ist, wird die rote Komponente der resultierenden Farbe wie folgt berechnet:</span><span class="sxs-lookup"><span data-stu-id="8b69b-111">If the alpha value is 200, the red component of the resultant color is calculated as follows:</span></span>

<span data-ttu-id="8b69b-112">150 × 200 / 255 + 100 × (255 – 200) / 255 = 139</span><span class="sxs-lookup"><span data-stu-id="8b69b-112">150 × 200 / 255 + 100 × (255 – 200) / 255 = 139</span></span>

<span data-ttu-id="8b69b-113">In den folgenden Themen wird die Alpha Mischung ausführlicher behandelt:</span><span class="sxs-lookup"><span data-stu-id="8b69b-113">The following topics cover alpha blending in more detail:</span></span>

-   [<span data-ttu-id="8b69b-114">Zeichnen deckender und halb transparenter Linien</span><span class="sxs-lookup"><span data-stu-id="8b69b-114">Drawing Opaque and Semitransparent Lines</span></span>](-gdiplus-drawing-opaque-and-semitransparent-lines-use.md)
-   [<span data-ttu-id="8b69b-115">Zeichnen mit nicht transparenten und halbtransparenten Pinseln</span><span class="sxs-lookup"><span data-stu-id="8b69b-115">Drawing with Opaque and Semitransparent Brushes</span></span>](-gdiplus-drawing-with-opaque-and-semitransparent-brushes-use.md)
-   [<span data-ttu-id="8b69b-116">Verwenden des Compositing-Modus zum Steuern der Alpha Mischung</span><span class="sxs-lookup"><span data-stu-id="8b69b-116">Using Compositing Mode to Control Alpha Blending</span></span>](-gdiplus-using-compositing-mode-to-control-alpha-blending-use.md)
-   [<span data-ttu-id="8b69b-117">Verwenden einer Farbmatrix zum Festlegen von Alphawerten in Bildern</span><span class="sxs-lookup"><span data-stu-id="8b69b-117">Using a Color Matrix to Set Alpha Values in Images</span></span>](-gdiplus-using-a-color-matrix-to-set-alpha-values-in-images-use.md)
-   [<span data-ttu-id="8b69b-118">Festlegen der Alpha Werte einzelner Pixel</span><span class="sxs-lookup"><span data-stu-id="8b69b-118">Setting the Alpha Values of Individual Pixels</span></span>](-gdiplus-setting-the-alpha-values-of-individual-pixels-use.md)

 

 



