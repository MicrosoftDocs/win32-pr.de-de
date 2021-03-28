---
description: Die Image-Klasse stellt grundlegende Methoden zum Laden und Anzeigen von Rasterbildern und Vektorbildern bereit. Die Metafile-Klasse, die von der Image-Klasse erbt, bietet speziellere Methoden zum Aufzeichnen, anzeigen und untersuchen von Vektorbildern.
ms.assetid: 79b8df1b-6fc5-455b-9d08-57d64bf6bffa
title: Laden und Anzeigen von Metadateien
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e5dafe6ef92e80e8487b43a22f50b44c5decd360
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104041714"
---
# <a name="loading-and-displaying-metafiles"></a><span data-ttu-id="20c42-104">Laden und Anzeigen von Metadateien</span><span class="sxs-lookup"><span data-stu-id="20c42-104">Loading and Displaying Metafiles</span></span>

<span data-ttu-id="20c42-105">Die [**Image**](/windows/desktop/api/gdiplusheaders/nl-gdiplusheaders-image) -Klasse stellt grundlegende Methoden zum Laden und Anzeigen von Rasterbildern und Vektorbildern bereit.</span><span class="sxs-lookup"><span data-stu-id="20c42-105">The [**Image**](/windows/desktop/api/gdiplusheaders/nl-gdiplusheaders-image) class provides basic methods for loading and displaying raster images and vector images.</span></span> <span data-ttu-id="20c42-106">Die [**Metafile**](/windows/desktop/api/gdiplusheaders/nl-gdiplusheaders-metafile) -Klasse, die von der **Image** -Klasse erbt, bietet speziellere Methoden zum Aufzeichnen, anzeigen und untersuchen von Vektorbildern.</span><span class="sxs-lookup"><span data-stu-id="20c42-106">The [**Metafile**](/windows/desktop/api/gdiplusheaders/nl-gdiplusheaders-metafile) class, which inherits from the **Image** class, provides more specialized methods for recording, displaying, and examining vector images.</span></span>

<span data-ttu-id="20c42-107">Zum Anzeigen eines Vektor Bilds (Metadatei) auf dem Bildschirm benötigen Sie ein [**Bild**](/windows/desktop/api/gdiplusheaders/nl-gdiplusheaders-image) Objekt und ein [**Grafik**](/windows/desktop/api/gdiplusgraphics/nl-gdiplusgraphics-graphics) Objekt.</span><span class="sxs-lookup"><span data-stu-id="20c42-107">To display a vector image (metafile) on the screen, you need an [**Image**](/windows/desktop/api/gdiplusheaders/nl-gdiplusheaders-image) object and a [**Graphics**](/windows/desktop/api/gdiplusgraphics/nl-gdiplusgraphics-graphics) object.</span></span> <span data-ttu-id="20c42-108">Übergeben Sie den Namen einer Datei (oder eines Zeigers an einen Stream) an einen **bildkonstruktor** .</span><span class="sxs-lookup"><span data-stu-id="20c42-108">Pass the name of a file (or a pointer to a stream) to an **Image** constructor.</span></span> <span data-ttu-id="20c42-109">Nachdem Sie ein **Image** -Objekt erstellt haben, übergeben Sie die Adresse dieses **Bild** Objekts an die **DrawImage** -Methode eines **Grafik** Objekts.</span><span class="sxs-lookup"><span data-stu-id="20c42-109">After you have created an **Image** object, pass the address of that **Image** object to the **DrawImage** method of a **Graphics** object.</span></span>

<span data-ttu-id="20c42-110">Im folgenden Beispiel wird ein [**Image**](/windows/desktop/api/gdiplusheaders/nl-gdiplusheaders-image) -Objekt aus einer EMF-Datei (Enhanced Metafile) erstellt. Anschließend wird das Bild mit der linken oberen Ecke bei (60, 10) gezeichnet:</span><span class="sxs-lookup"><span data-stu-id="20c42-110">The following example creates an [**Image**](/windows/desktop/api/gdiplusheaders/nl-gdiplusheaders-image) object from an EMF (enhanced metafile) file and then draws the image with its upper-left corner at (60, 10):</span></span>


```
Image image(L"SampleMetafile.emf");
graphics.DrawImage(&image, 60, 10);
```



<span data-ttu-id="20c42-111">Die folgende Abbildung zeigt das an der angegebenen Position gezeichnete Bild.</span><span class="sxs-lookup"><span data-stu-id="20c42-111">The following illustration shows the image drawn at the specified location.</span></span>

![Screenshot eines Fensters, das ein Bild enthält und den Ursprungs Punkt angibt](images/imageposition2.png)

 

 



