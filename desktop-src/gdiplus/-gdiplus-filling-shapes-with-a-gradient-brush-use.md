---
description: Sie können einen Farbverlaufs Pinsel verwenden, um eine Form mit einer allmählich veränderlichen Farbe auszufüllen.
ms.assetid: e37b4c3a-b753-483a-990f-da3bcc70acf5
title: Auffüllen von Formen mit einem Farbverlaufs Pinsel
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a6784d0bfd59fd37f217e8d7a1cdd230348807d0
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104994254"
---
# <a name="filling-shapes-with-a-gradient-brush"></a><span data-ttu-id="e3693-103">Auffüllen von Formen mit einem Farbverlaufs Pinsel</span><span class="sxs-lookup"><span data-stu-id="e3693-103">Filling Shapes with a Gradient Brush</span></span>

<span data-ttu-id="e3693-104">Sie können einen Farbverlaufs Pinsel verwenden, um eine Form mit einer allmählich veränderlichen Farbe auszufüllen.</span><span class="sxs-lookup"><span data-stu-id="e3693-104">You can use a gradient brush to fill a shape with a gradually changing color.</span></span> <span data-ttu-id="e3693-105">Beispielsweise können Sie einen horizontalen Farbverlauf verwenden, um eine Form mit Farben auszufüllen, die sich allmählich ändert, wenn Sie vom linken Rand der Form zum rechten Rand wechseln.</span><span class="sxs-lookup"><span data-stu-id="e3693-105">For example, you can use a horizontal gradient to fill a shape with color that changes gradually as you move from the left edge of the shape to the right edge.</span></span> <span data-ttu-id="e3693-106">Stellen Sie sich ein Rechteck mit einem linken Rand vor, der schwarz ist (dargestellt durch die rote, grüne und blaue Komponente 0, 0, 0) und einen rechten roten Rand (dargestellt durch 255, 0, 0).</span><span class="sxs-lookup"><span data-stu-id="e3693-106">Imagine a rectangle with a left edge that is black (represented by red, green, and blue components 0, 0, 0) and a right edge that is red (represented by 255, 0, 0).</span></span> <span data-ttu-id="e3693-107">Wenn das Rechteck 256 Pixel breit ist, ist die rote Komponente eines gegebenen Pixels eine größer als die rote Komponente des Pixels links.</span><span class="sxs-lookup"><span data-stu-id="e3693-107">If the rectangle is 256 pixels wide, the red component of a given pixel will be one greater than the red component of the pixel to its left.</span></span> <span data-ttu-id="e3693-108">Das äußteste linke Pixel in einer Zeile hat Farbkomponenten (0, 0, 0), das zweite Pixel hat (1, 0, 0), das dritte Pixel hat (2, 0, 0) usw., bis Sie zum äußersten äußersten Pixel mit Farbkomponenten (255, 0,0) gelangen.</span><span class="sxs-lookup"><span data-stu-id="e3693-108">The leftmost pixel in a row has color components (0, 0, 0), the second pixel has (1, 0, 0), the third pixel has (2, 0, 0), and so on, until you get to the rightmost pixel, which has color components (255, 0, 0).</span></span> <span data-ttu-id="e3693-109">Diese interpoliert Farbwerte bilden den Farbverlauf.</span><span class="sxs-lookup"><span data-stu-id="e3693-109">These interpolated color values make up the color gradient.</span></span>

<span data-ttu-id="e3693-110">Die Farbe eines linearen Farbverlaufs ändert sich, wenn Sie horizontal, vertikal oder parallel zu einer angegebenen schrägen Linie wechseln.</span><span class="sxs-lookup"><span data-stu-id="e3693-110">A linear gradient changes color as you move horizontally, vertically, or parallel to a specified slanted line.</span></span> <span data-ttu-id="e3693-111">Ein Pfad Farbverlauf ändert die Farbe, wenn Sie zum inneren und zur Grenze eines Pfads wechseln.</span><span class="sxs-lookup"><span data-stu-id="e3693-111">A path gradient changes color as you move about the interior and boundary of a path.</span></span> <span data-ttu-id="e3693-112">Sie können Pfad Farbverläufe anpassen, um eine Vielzahl von Effekten zu erzielen.</span><span class="sxs-lookup"><span data-stu-id="e3693-112">You can customize path gradients to achieve a wide variety of effects.</span></span>

<span data-ttu-id="e3693-113">GDI+ stellt die Klassen [**LinearGradientBrush**](/windows/desktop/api/gdiplusbrush/nl-gdiplusbrush-lineargradientbrush) und [**PathGradientBrush**](/windows/desktop/api/gdipluspath/nl-gdipluspath-pathgradientbrush) bereit, von denen beide von der [**Brush**](/windows/desktop/api/gdiplusbrush/nl-gdiplusbrush-brush) -Klasse erben.</span><span class="sxs-lookup"><span data-stu-id="e3693-113">GDI+ provides the [**LinearGradientBrush**](/windows/desktop/api/gdiplusbrush/nl-gdiplusbrush-lineargradientbrush) and [**PathGradientBrush**](/windows/desktop/api/gdipluspath/nl-gdipluspath-pathgradientbrush) classes, both of which inherit from the [**Brush**](/windows/desktop/api/gdiplusbrush/nl-gdiplusbrush-brush) class.</span></span>

<span data-ttu-id="e3693-114">In den folgenden Themen werden die Farbverläufe linear und Path ausführlicher behandelt:</span><span class="sxs-lookup"><span data-stu-id="e3693-114">The following topics cover linear and path gradients in more detail:</span></span>

-   [<span data-ttu-id="e3693-115">Erstellen eines linearen Farbverlaufs</span><span class="sxs-lookup"><span data-stu-id="e3693-115">Creating a Linear Gradient</span></span>](-gdiplus-creating-a-linear-gradient-use.md)
-   [<span data-ttu-id="e3693-116">Erstellen eines Pfad Farbverlaufs</span><span class="sxs-lookup"><span data-stu-id="e3693-116">Creating a Path Gradient</span></span>](-gdiplus-creating-a-path-gradient-use.md)
-   [<span data-ttu-id="e3693-117">Anwenden der Gamma Korrektur auf einen Farbverlauf</span><span class="sxs-lookup"><span data-stu-id="e3693-117">Applying Gamma Correction to a Gradient</span></span>](-gdiplus-applying-gamma-correction-to-a-gradient-use.md)

 

 



