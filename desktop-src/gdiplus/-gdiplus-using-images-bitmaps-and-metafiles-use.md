---
description: Windows GDI+ bietet die Image-Klasse zum Arbeiten mit Rasterbildern (Bitmaps) und Vektorbildern (Metafiles).
ms.assetid: 57e3bf33-5490-4f4a-addf-356ef8f1aeed
title: Verwenden von Bildern, Bitmaps und Metadateien
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 445b37caa488fa4b83bcfb7792eb83f6ee1e6e75
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104042100"
---
# <a name="using-images-bitmaps-and-metafiles"></a><span data-ttu-id="3d353-103">Verwenden von Bildern, Bitmaps und Metadateien</span><span class="sxs-lookup"><span data-stu-id="3d353-103">Using Images, Bitmaps, and Metafiles</span></span>

<span data-ttu-id="3d353-104">Windows GDI+ bietet die [**Image**](/windows/desktop/api/gdiplusheaders/nl-gdiplusheaders-image) -Klasse zum Arbeiten mit Rasterbildern (Bitmaps) und Vektorbildern (Metafiles).</span><span class="sxs-lookup"><span data-stu-id="3d353-104">Windows GDI+ provides the [**Image**](/windows/desktop/api/gdiplusheaders/nl-gdiplusheaders-image) class for working with raster images (bitmaps) and vector images (metafiles).</span></span> <span data-ttu-id="3d353-105">Die [**Bitmap**](/windows/desktop/api/gdiplusheaders/nl-gdiplusheaders-bitmap) -Klasse und die [**Metafile**](/windows/desktop/api/gdiplusheaders/nl-gdiplusheaders-metafile) -Klasse erben beide von der **Image** -Klasse.</span><span class="sxs-lookup"><span data-stu-id="3d353-105">The [**Bitmap**](/windows/desktop/api/gdiplusheaders/nl-gdiplusheaders-bitmap) class and the [**Metafile**](/windows/desktop/api/gdiplusheaders/nl-gdiplusheaders-metafile) class both inherit from the **Image** class.</span></span> <span data-ttu-id="3d353-106">Die **Bitmap** -Klasse erweitert die Funktionen der **Image** -Klasse, indem zusätzliche Methoden zum Laden, speichern und Bearbeiten von Rasterbildern bereitgestellt werden.</span><span class="sxs-lookup"><span data-stu-id="3d353-106">The **Bitmap** class expands on the capabilities of the **Image** class by providing additional methods for loading, saving, and manipulating raster images.</span></span> <span data-ttu-id="3d353-107">Die **Metafile** -Klasse erweitert die Funktionen der **Image** -Klasse, indem zusätzliche Methoden zum Aufzeichnen und untersuchen von Vektorbildern bereitgestellt werden.</span><span class="sxs-lookup"><span data-stu-id="3d353-107">The **Metafile** class expands on the capabilities of the **Image** class by providing additional methods for recording and examining vector images.</span></span>

<span data-ttu-id="3d353-108">In den folgenden Themen werden die [**Image**](/windows/desktop/api/gdiplusheaders/nl-gdiplusheaders-image)-, [**Bitmap**](/windows/desktop/api/gdiplusheaders/nl-gdiplusheaders-bitmap)-und [**Metafile**](/windows/desktop/api/gdiplusheaders/nl-gdiplusheaders-metafile) -Klassen ausführlicher behandelt:</span><span class="sxs-lookup"><span data-stu-id="3d353-108">The following topics cover the [**Image**](/windows/desktop/api/gdiplusheaders/nl-gdiplusheaders-image), [**Bitmap**](/windows/desktop/api/gdiplusheaders/nl-gdiplusheaders-bitmap), and [**Metafile**](/windows/desktop/api/gdiplusheaders/nl-gdiplusheaders-metafile) classes in more detail:</span></span>

-   [<span data-ttu-id="3d353-109">Laden und Anzeigen von Bitmaps</span><span class="sxs-lookup"><span data-stu-id="3d353-109">Loading and Displaying Bitmaps</span></span>](-gdiplus-loading-and-displaying-bitmaps-use.md)
-   [<span data-ttu-id="3d353-110">Laden und Anzeigen von Metadateien</span><span class="sxs-lookup"><span data-stu-id="3d353-110">Loading and Displaying Metafiles</span></span>](-gdiplus-loading-and-displaying-metafiles-use.md)
-   [<span data-ttu-id="3d353-111">Aufzeichnen von Metafiles</span><span class="sxs-lookup"><span data-stu-id="3d353-111">Recording Metafiles</span></span>](-gdiplus-recording-metafiles-use.md)
-   [<span data-ttu-id="3d353-112">Zuschneiden und Skalieren von Bildern</span><span class="sxs-lookup"><span data-stu-id="3d353-112">Cropping and Scaling Images</span></span>](-gdiplus-cropping-and-scaling-images-use.md)
-   [<span data-ttu-id="3d353-113">Rotation, Spiegelung und Neigung von Bildern</span><span class="sxs-lookup"><span data-stu-id="3d353-113">Rotating, Reflecting, and Skewing Images</span></span>](-gdiplus-rotating-reflecting-and-skewing-images-use.md)
-   [<span data-ttu-id="3d353-114">Verwenden des Interpolations Modus zum Steuern der Bildqualität während der Skalierung</span><span class="sxs-lookup"><span data-stu-id="3d353-114">Using Interpolation Mode to Control Image Quality During Scaling</span></span>](-gdiplus-using-interpolation-mode-to-control-image-quality-during-scaling-use.md)
-   [<span data-ttu-id="3d353-115">Erstellen von Miniaturbildern</span><span class="sxs-lookup"><span data-stu-id="3d353-115">Creating Thumbnail Images</span></span>](-gdiplus-creating-thumbnail-images-use.md)
-   [<span data-ttu-id="3d353-116">Verwenden einer zwischengespeicherten Bitmap zum Verbessern der Leistung</span><span class="sxs-lookup"><span data-stu-id="3d353-116">Using a Cached Bitmap to Improve Performance</span></span>](-gdiplus-using-a-cached-bitmap-to-improve-performance-use.md)
-   [<span data-ttu-id="3d353-117">Verbessern der Leistung durch vermeiden der automatischen Skalierung</span><span class="sxs-lookup"><span data-stu-id="3d353-117">Improving Performance by Avoiding Automatic Scaling</span></span>](-gdiplus-improving-performance-by-avoiding-automatic-scaling-use.md)
-   [<span data-ttu-id="3d353-118">Lesen und Schreiben von Metadaten</span><span class="sxs-lookup"><span data-stu-id="3d353-118">Reading and Writing Metadata</span></span>](-gdiplus-reading-and-writing-metadata-use.md)

 

 



