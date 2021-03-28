---
description: Wenn Sie ein Rasterbild (Bitmap) auf dem Bildschirm anzeigen möchten, benötigen Sie ein Bild Objekt und ein Grafik Objekt.
ms.assetid: 8c1a26d9-b640-4f38-8276-10c4464525f2
title: Laden und Anzeigen von Bitmaps
ms.topic: article
ms.date: 05/31/2018
ms.custom: project-verbatim
ms.openlocfilehash: ab2405462db5017215893d50d93dc0b228633cfb
ms.sourcegitcommit: af120ad5c30da2fc5eb717ca2a1c4c45878efd71
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/20/2021
ms.locfileid: "104982844"
---
# <a name="loading-and-displaying-bitmaps"></a><span data-ttu-id="014a2-103">Laden und Anzeigen von Bitmaps</span><span class="sxs-lookup"><span data-stu-id="014a2-103">Loading and displaying bitmaps</span></span>

<span data-ttu-id="014a2-104">Weitere Informationen finden Sie auch in der [WIC-Viewer-Beispiel-App](https://github.com/microsoft/Windows-classic-samples/tree/master/Samples/Win7Samples/multimedia/wic/wicviewergdiplus).</span><span class="sxs-lookup"><span data-stu-id="014a2-104">Also see the [WIC Viewer GDI+ sample app](https://github.com/microsoft/Windows-classic-samples/tree/master/Samples/Win7Samples/multimedia/wic/wicviewergdiplus).</span></span>

<span data-ttu-id="014a2-105">Wenn Sie ein Rasterbild (Bitmap) auf dem Bildschirm anzeigen möchten, benötigen Sie ein [**Bild**](/windows/desktop/api/gdiplusheaders/nl-gdiplusheaders-image) Objekt und ein [**Grafik**](/windows/desktop/api/gdiplusgraphics/nl-gdiplusgraphics-graphics) Objekt.</span><span class="sxs-lookup"><span data-stu-id="014a2-105">To display a raster image (bitmap) on the screen, you need an [**Image**](/windows/desktop/api/gdiplusheaders/nl-gdiplusheaders-image) object and a [**Graphics**](/windows/desktop/api/gdiplusgraphics/nl-gdiplusgraphics-graphics) object.</span></span> <span data-ttu-id="014a2-106">Übergeben Sie den Namen einer Datei (oder eines Zeigers an einen Stream) an einen **bildkonstruktor** .</span><span class="sxs-lookup"><span data-stu-id="014a2-106">Pass the name of a file (or a pointer to a stream) to an **Image** constructor.</span></span> <span data-ttu-id="014a2-107">Nachdem Sie ein **Image** -Objekt erstellt haben, übergeben Sie die Adresse dieses **Bild** Objekts an die **DrawImage** -Methode eines **Grafik** Objekts.</span><span class="sxs-lookup"><span data-stu-id="014a2-107">After you have created an **Image** object, pass the address of that **Image** object to the **DrawImage** method of a **Graphics** object.</span></span>

<span data-ttu-id="014a2-108">Im folgenden Beispiel wird ein [**Image**](/windows/desktop/api/gdiplusheaders/nl-gdiplusheaders-image) -Objekt aus einer JPEG-Datei erstellt, und anschließend wird das Bild mit der linken oberen Ecke bei (60, 10) gezeichnet:</span><span class="sxs-lookup"><span data-stu-id="014a2-108">The following example creates an [**Image**](/windows/desktop/api/gdiplusheaders/nl-gdiplusheaders-image) object from a JPEG file and then draws the image with its upper-left corner at (60, 10):</span></span>

```cpp
Image image(L"Grapes.jpg");
graphics.DrawImage(&image, 60, 10);
```

<span data-ttu-id="014a2-109">Die folgende Abbildung zeigt das an der angegebenen Position gezeichnete Bild.</span><span class="sxs-lookup"><span data-stu-id="014a2-109">The following illustration shows the image drawn at the specified location.</span></span>

![<span data-ttu-id="014a2-110">Screenshot eines Fensters, das ein Bild enthält, mit einer Legende für den Ursprungs Punkt</span><span class="sxs-lookup"><span data-stu-id="014a2-110">screen shot of a window that contains an image, with a callout for the origin point</span></span> ](images/imageposition1.png)

<span data-ttu-id="014a2-111">Die [**Image**](/windows/desktop/api/gdiplusheaders/nl-gdiplusheaders-image) -Klasse stellt grundlegende Methoden zum Laden und Anzeigen von Rasterbildern und Vektorbildern bereit.</span><span class="sxs-lookup"><span data-stu-id="014a2-111">The [**Image**](/windows/desktop/api/gdiplusheaders/nl-gdiplusheaders-image) class provides basic methods for loading and displaying raster images and vector images.</span></span> <span data-ttu-id="014a2-112">Die [**Bitmap**](/windows/desktop/api/gdiplusheaders/nl-gdiplusheaders-bitmap) -Klasse, die von der **Image** -Klasse erbt, bietet speziellere Methoden zum Laden, anzeigen und Bearbeiten von Rasterbildern.</span><span class="sxs-lookup"><span data-stu-id="014a2-112">The [**Bitmap**](/windows/desktop/api/gdiplusheaders/nl-gdiplusheaders-bitmap) class, which inherits from the **Image** class, provides more specialized methods for loading, displaying, and manipulating raster images.</span></span> <span data-ttu-id="014a2-113">Beispielsweise können Sie ein **Bitmap** -Objekt aus einem Symbol Handle (HICON) erstellen.</span><span class="sxs-lookup"><span data-stu-id="014a2-113">For example, you can construct a **Bitmap** object from an icon handle (HICON).</span></span>

<span data-ttu-id="014a2-114">Im folgenden Beispiel wird ein Handle für ein Symbol abgerufen, und anschließend wird dieses Handle zum Erstellen eines [**Bitmap**](/windows/desktop/api/gdiplusheaders/nl-gdiplusheaders-bitmap) -Objekts verwendet.</span><span class="sxs-lookup"><span data-stu-id="014a2-114">The following example obtains a handle to an icon and then uses that handle to construct a [**Bitmap**](/windows/desktop/api/gdiplusheaders/nl-gdiplusheaders-bitmap) object.</span></span> <span data-ttu-id="014a2-115">Im Code wird das Symbol angezeigt, indem die Adresse des **Bitmap** -Objekts an die **DrawImage** -Methode eines [**Grafik**](/windows/desktop/api/gdiplusgraphics/nl-gdiplusgraphics-graphics) Objekts übergeben wird.</span><span class="sxs-lookup"><span data-stu-id="014a2-115">The code displays the icon by passing the address of the **Bitmap** object to the **DrawImage** method of a [**Graphics**](/windows/desktop/api/gdiplusgraphics/nl-gdiplusgraphics-graphics) object.</span></span>

```cpp
HICON hIcon = LoadIcon(NULL, IDI_APPLICATION);
Bitmap bitmap(hIcon);
graphics.DrawImage(&bitmap, 10, 10);
```

## <a name="see-also"></a><span data-ttu-id="014a2-116">Weitere Informationen</span><span class="sxs-lookup"><span data-stu-id="014a2-116">See also</span></span>

[<span data-ttu-id="014a2-117">WIC-Viewer-GDI+-Beispiel-App</span><span class="sxs-lookup"><span data-stu-id="014a2-117">WIC Viewer GDI+ sample app</span></span>](https://github.com/microsoft/Windows-classic-samples/tree/master/Samples/Win7Samples/multimedia/wic/wicviewergdiplus)
