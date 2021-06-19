---
description: Erfahren Sie mehr über die Verwendung von Bildern, Bitmaps und Metadateien. Windows GDI+ stellt die Image-Klasse zum Arbeiten mit Rasterbildern (Bitmaps) und Vektorbildern (Metadateien) bereit.
ms.assetid: 57e3bf33-5490-4f4a-addf-356ef8f1aeed
title: Verwenden von Bildern, Bitmaps und Metadateien
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 49d0603c8a428c45feac8cdeb47a46b61dc5e3bd
ms.sourcegitcommit: 91530c19d26ba4c57a6af1f37b57f211f580464e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/19/2021
ms.locfileid: "112395535"
---
# <a name="using-images-bitmaps-and-metafiles"></a><span data-ttu-id="0b79e-104">Verwenden von Bildern, Bitmaps und Metadateien</span><span class="sxs-lookup"><span data-stu-id="0b79e-104">Using Images, Bitmaps, and Metafiles</span></span>

<span data-ttu-id="0b79e-105">Windows GDI+ stellt die [**Image-Klasse**](/windows/desktop/api/gdiplusheaders/nl-gdiplusheaders-image) zum Arbeiten mit Rasterbildern (Bitmaps) und Vektorbildern (Metadateien) bereit.</span><span class="sxs-lookup"><span data-stu-id="0b79e-105">Windows GDI+ provides the [**Image**](/windows/desktop/api/gdiplusheaders/nl-gdiplusheaders-image) class for working with raster images (bitmaps) and vector images (metafiles).</span></span> <span data-ttu-id="0b79e-106">Die [**Bitmap-Klasse**](/windows/desktop/api/gdiplusheaders/nl-gdiplusheaders-bitmap) und die [**Metafile-Klasse**](/windows/desktop/api/gdiplusheaders/nl-gdiplusheaders-metafile) erben beide von der **Image-Klasse.**</span><span class="sxs-lookup"><span data-stu-id="0b79e-106">The [**Bitmap**](/windows/desktop/api/gdiplusheaders/nl-gdiplusheaders-bitmap) class and the [**Metafile**](/windows/desktop/api/gdiplusheaders/nl-gdiplusheaders-metafile) class both inherit from the **Image** class.</span></span> <span data-ttu-id="0b79e-107">Die **Bitmap-Klasse** erweitert die Funktionen der **Image-Klasse,** indem sie zusätzliche Methoden zum Laden, Speichern und Bearbeiten von Rasterbildern bereitstellt.</span><span class="sxs-lookup"><span data-stu-id="0b79e-107">The **Bitmap** class expands on the capabilities of the **Image** class by providing additional methods for loading, saving, and manipulating raster images.</span></span> <span data-ttu-id="0b79e-108">Die **Metafile-Klasse** erweitert die Funktionen der **Image-Klasse,** indem sie zusätzliche Methoden zum Aufzeichnen und Untersuchen von Vektorbildern bereitstellt.</span><span class="sxs-lookup"><span data-stu-id="0b79e-108">The **Metafile** class expands on the capabilities of the **Image** class by providing additional methods for recording and examining vector images.</span></span>

<span data-ttu-id="0b79e-109">In den folgenden Themen werden die Klassen [**Image,**](/windows/desktop/api/gdiplusheaders/nl-gdiplusheaders-image) [**Bitmap**](/windows/desktop/api/gdiplusheaders/nl-gdiplusheaders-bitmap)und [**Metafile**](/windows/desktop/api/gdiplusheaders/nl-gdiplusheaders-metafile) ausführlicher behandelt:</span><span class="sxs-lookup"><span data-stu-id="0b79e-109">The following topics cover the [**Image**](/windows/desktop/api/gdiplusheaders/nl-gdiplusheaders-image), [**Bitmap**](/windows/desktop/api/gdiplusheaders/nl-gdiplusheaders-bitmap), and [**Metafile**](/windows/desktop/api/gdiplusheaders/nl-gdiplusheaders-metafile) classes in more detail:</span></span>

-   [<span data-ttu-id="0b79e-110">Laden und Anzeigen von Bitmaps</span><span class="sxs-lookup"><span data-stu-id="0b79e-110">Loading and Displaying Bitmaps</span></span>](-gdiplus-loading-and-displaying-bitmaps-use.md)
-   [<span data-ttu-id="0b79e-111">Laden und Anzeigen von Metadateien</span><span class="sxs-lookup"><span data-stu-id="0b79e-111">Loading and Displaying Metafiles</span></span>](-gdiplus-loading-and-displaying-metafiles-use.md)
-   [<span data-ttu-id="0b79e-112">Aufzeichnen von Metadateien</span><span class="sxs-lookup"><span data-stu-id="0b79e-112">Recording Metafiles</span></span>](-gdiplus-recording-metafiles-use.md)
-   [<span data-ttu-id="0b79e-113">Zuschneiden und Skalieren von Bildern</span><span class="sxs-lookup"><span data-stu-id="0b79e-113">Cropping and Scaling Images</span></span>](-gdiplus-cropping-and-scaling-images-use.md)
-   [<span data-ttu-id="0b79e-114">Drehen, Spiegeln und Skewing von Bildern</span><span class="sxs-lookup"><span data-stu-id="0b79e-114">Rotating, Reflecting, and Skewing Images</span></span>](-gdiplus-rotating-reflecting-and-skewing-images-use.md)
-   [<span data-ttu-id="0b79e-115">Verwenden des Interpolationsmodus zum Steuern der Bildqualität während der Skalierung</span><span class="sxs-lookup"><span data-stu-id="0b79e-115">Using Interpolation Mode to Control Image Quality During Scaling</span></span>](-gdiplus-using-interpolation-mode-to-control-image-quality-during-scaling-use.md)
-   [<span data-ttu-id="0b79e-116">Erstellen von Miniaturbildern</span><span class="sxs-lookup"><span data-stu-id="0b79e-116">Creating Thumbnail Images</span></span>](-gdiplus-creating-thumbnail-images-use.md)
-   [<span data-ttu-id="0b79e-117">Verwenden einer zwischengespeicherten Bitmap zur Verbesserung der Leistung</span><span class="sxs-lookup"><span data-stu-id="0b79e-117">Using a Cached Bitmap to Improve Performance</span></span>](-gdiplus-using-a-cached-bitmap-to-improve-performance-use.md)
-   [<span data-ttu-id="0b79e-118">Verbessern der Leistung durch Vermeiden der automatischen Skalierung</span><span class="sxs-lookup"><span data-stu-id="0b79e-118">Improving Performance by Avoiding Automatic Scaling</span></span>](-gdiplus-improving-performance-by-avoiding-automatic-scaling-use.md)
-   [<span data-ttu-id="0b79e-119">Lesen und Schreiben von Metadaten</span><span class="sxs-lookup"><span data-stu-id="0b79e-119">Reading and Writing Metadata</span></span>](-gdiplus-reading-and-writing-metadata-use.md)

 

 



