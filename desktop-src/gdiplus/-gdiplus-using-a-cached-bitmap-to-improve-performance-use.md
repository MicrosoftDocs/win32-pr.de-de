---
description: Image-und Bitmap-Objekte speichern Bilder in einem geräteunabhängigen Format.
ms.assetid: 42e2b664-197c-4c54-9220-b6231d6439d0
title: Verwenden einer zwischengespeicherten Bitmap zum Verbessern der Leistung
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7a8e546460741342bcac8f1633e21d104984af9b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104994174"
---
# <a name="using-a-cached-bitmap-to-improve-performance"></a><span data-ttu-id="30982-103">Verwenden einer zwischengespeicherten Bitmap zum Verbessern der Leistung</span><span class="sxs-lookup"><span data-stu-id="30982-103">Using a Cached Bitmap to Improve Performance</span></span>

<span data-ttu-id="30982-104">[**Image**](/windows/desktop/api/gdiplusheaders/nl-gdiplusheaders-image) -und [**Bitmap**](/windows/desktop/api/gdiplusheaders/nl-gdiplusheaders-bitmap) -Objekte speichern Bilder in einem geräteunabhängigen Format.</span><span class="sxs-lookup"><span data-stu-id="30982-104">[**Image**](/windows/desktop/api/gdiplusheaders/nl-gdiplusheaders-image) and [**Bitmap**](/windows/desktop/api/gdiplusheaders/nl-gdiplusheaders-bitmap) objects store images in a device-independent format.</span></span> <span data-ttu-id="30982-105">Ein [**CachedBitmap**](/windows/desktop/api/gdiplusheaders/nl-gdiplusheaders-cachedbitmap) -Objekt speichert ein Bild im Format des aktuellen Anzeige Geräts.</span><span class="sxs-lookup"><span data-stu-id="30982-105">A [**CachedBitmap**](/windows/desktop/api/gdiplusheaders/nl-gdiplusheaders-cachedbitmap) object stores an image in the format of the current display device.</span></span> <span data-ttu-id="30982-106">Das Rendern eines in einem **CachedBitmap** -Objekt gespeicherten Bilds ist schnell, da keine Verarbeitungszeit aufgewendet wird, um das Abbild in das vom Anzeigegerät benötigte Format zu wandeln.</span><span class="sxs-lookup"><span data-stu-id="30982-106">Rendering an image stored in a **CachedBitmap** object is fast because no processing time is spent converting the image to the format required by the display device.</span></span>

<span data-ttu-id="30982-107">Im folgenden Beispiel werden ein [**Bitmap**](/windows/desktop/api/gdiplusheaders/nl-gdiplusheaders-bitmap) -Objekt und ein [**CachedBitmap**](/windows/desktop/api/gdiplusheaders/nl-gdiplusheaders-cachedbitmap) -Objekt aus dem Datei Texture.jpg erstellt.</span><span class="sxs-lookup"><span data-stu-id="30982-107">The following example creates a [**Bitmap**](/windows/desktop/api/gdiplusheaders/nl-gdiplusheaders-bitmap) object and a [**CachedBitmap**](/windows/desktop/api/gdiplusheaders/nl-gdiplusheaders-cachedbitmap) object from the file Texture.jpg.</span></span> <span data-ttu-id="30982-108">Die **Bitmap** und die **CachedBitmap** werden jeweils 30.000-Mal gezeichnet.</span><span class="sxs-lookup"><span data-stu-id="30982-108">The **Bitmap** and the **CachedBitmap** are each drawn 30,000 times.</span></span> <span data-ttu-id="30982-109">Wenn Sie den Code ausführen, werden Sie feststellen, dass die **CachedBitmap** -Bilder wesentlich schneller gezeichnet werden als die **Bitmap** -Bilder.</span><span class="sxs-lookup"><span data-stu-id="30982-109">If you run the code, you will see that the **CachedBitmap** images are drawn substantially faster than the **Bitmap** images.</span></span>


```
Bitmap        bitmap(L"Texture.jpg");
UINT          width = bitmap.GetWidth();
UINT          height = bitmap.GetHeight();
CachedBitmap  cBitmap(&bitmap, &graphics);
int           j, k;
for(j = 0; j < 300; j += 10)
   for(k = 0; k < 1000; ++k)
     graphics.DrawImage(&bitmap, j, j / 2, width, height);
for(j = 0; j < 300; j += 10)
   for(k = 0; k < 1000; ++k)
      graphics.DrawCachedBitmap(&cBitmap, j, 150 + j / 2 );
```



> [!Note]  
> <span data-ttu-id="30982-110">Ein [**CachedBitmap**](/windows/desktop/api/gdiplusheaders/nl-gdiplusheaders-cachedbitmap) -Objekt entspricht dem Format des Anzeige Geräts zu dem Zeitpunkt, zu dem das **CachedBitmap** -Objekt erstellt wurde.</span><span class="sxs-lookup"><span data-stu-id="30982-110">A [**CachedBitmap**](/windows/desktop/api/gdiplusheaders/nl-gdiplusheaders-cachedbitmap) object matches the format of the display device at the time the **CachedBitmap** object was constructed.</span></span> <span data-ttu-id="30982-111">Wenn der Benutzer des Programms die Anzeigeeinstellungen ändert, sollte der Code ein neues **CachedBitmap** -Objekt erstellen.</span><span class="sxs-lookup"><span data-stu-id="30982-111">If the user of your program changes the display settings, your code should construct a new **CachedBitmap** object.</span></span> <span data-ttu-id="30982-112">Bei der **DrawImage** -Methode tritt ein Fehler auf, wenn Sie ein **CachedBitmap** -Objekt übergeben, das vor einer Änderung im Anzeige Format erstellt wurde.</span><span class="sxs-lookup"><span data-stu-id="30982-112">The **DrawImage** method will fail if you pass it a **CachedBitmap** object that was created prior to a change in the display format.</span></span>

 

 

 



