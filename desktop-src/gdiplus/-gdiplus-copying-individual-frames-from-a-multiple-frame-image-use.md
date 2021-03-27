---
title: Einzelne Frames aus einem Bild mit mehreren Frames kopieren
description: Im folgenden Beispiel werden die einzelnen Frames aus einer TIFF-Datei mit mehreren Frames abgerufen.
ms.assetid: dfed0b61-2230-4911-a642-0a6e4beb08d6
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3d6bdb5668bcebb9babcbcb7d07839694750aec4
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104215592"
---
# <a name="copy-individual-frames-from-a-multiple-frame-image"></a><span data-ttu-id="12400-103">Einzelne Frames aus einem Bild mit mehreren Frames kopieren</span><span class="sxs-lookup"><span data-stu-id="12400-103">Copy individual frames from a multiple-frame image</span></span>

<span data-ttu-id="12400-104">Im folgenden Beispiel werden die einzelnen Frames aus einer TIFF-Datei mit mehreren Frames abgerufen.</span><span class="sxs-lookup"><span data-stu-id="12400-104">The following example retrieves the individual frames from a multiple-frame TIFF file.</span></span> <span data-ttu-id="12400-105">Beim Erstellen der TIFF-Datei wurden die einzelnen Frames der Seiten Dimension hinzugefügt (Weitere Informationen finden Sie unter [Erstellen und Speichern eines Multiple-Frame Bilds](-gdiplus-creating-and-saving-a-multiple-frame-image-use.md)).</span><span class="sxs-lookup"><span data-stu-id="12400-105">When the TIFF file was created, the individual frames were added to the Page dimension (see [Creating and Saving a Multiple-Frame Image](-gdiplus-creating-and-saving-a-multiple-frame-image-use.md)).</span></span> <span data-ttu-id="12400-106">Der Code zeigt jede der vier Seiten an und speichert jede Seite in einer separaten PNG-Datenträger Datei.</span><span class="sxs-lookup"><span data-stu-id="12400-106">The code displays each of the four pages and saves each page to a separate PNG disk file.</span></span>

<span data-ttu-id="12400-107">Der Code erstellt ein [**Image**](/windows/desktop/api/gdiplusheaders/nl-gdiplusheaders-image) -Objekt aus der TIFF-Datei mit mehreren Frames.</span><span class="sxs-lookup"><span data-stu-id="12400-107">The code constructs an [**Image**](/windows/desktop/api/gdiplusheaders/nl-gdiplusheaders-image) object from the multiple-frame TIFF file.</span></span> <span data-ttu-id="12400-108">Um die einzelnen Frames (Seiten) abzurufen, ruft der Code die [**Image:: SelectActiveFrame**](/windows/desktop/api/Gdiplusheaders/nf-gdiplusheaders-image-selectactiveframe) -Methode dieses **Bild** Objekts auf.</span><span class="sxs-lookup"><span data-stu-id="12400-108">To retrieve the individual frames (pages), the code calls the [**Image::SelectActiveFrame**](/windows/desktop/api/Gdiplusheaders/nf-gdiplusheaders-image-selectactiveframe) method of that **Image** object.</span></span> <span data-ttu-id="12400-109">Das erste Argument, das an die **Image:: SelectActiveFrame** -Methode übermittelt wird, ist die Adresse einer GUID, die die Dimension angibt, in der die Frames zuvor der TIFF-Datei mit mehreren Frames hinzugefügt wurden.</span><span class="sxs-lookup"><span data-stu-id="12400-109">The first argument passed to the **Image::SelectActiveFrame** method is the address of a GUID that specifies the dimension in which the frames were previously added to the multiple-frame TIFF file.</span></span> <span data-ttu-id="12400-110">Die GUID ' framedimensionpage ' ist in ' gdiplusimaging. h ' definiert.</span><span class="sxs-lookup"><span data-stu-id="12400-110">The GUID FrameDimensionPage is defined in Gdiplusimaging.h.</span></span> <span data-ttu-id="12400-111">Andere GUIDs, die in der Header Datei definiert sind, sind framedimensiontime und framedimensionresolution.</span><span class="sxs-lookup"><span data-stu-id="12400-111">Other GUIDs defined in that header file are FrameDimensionTime and FrameDimensionResolution.</span></span> <span data-ttu-id="12400-112">Das zweite Argument, das an die Methode **Image:: SelectActiveFrame** übermittelt wird, ist der null basierte Index der gewünschten Seite.</span><span class="sxs-lookup"><span data-stu-id="12400-112">The second argument passed to the **Image::SelectActiveFrame** method is the zero-based index of the desired page.</span></span>

<span data-ttu-id="12400-113">Der Code basiert auf der Hilfsfunktion getencoderclsid, die unter [Abrufen des Klassen Bezeichners für einen Encoder](-gdiplus-retrieving-the-class-identifier-for-an-encoder-use.md)angezeigt wird.</span><span class="sxs-lookup"><span data-stu-id="12400-113">The code relies on the helper function GetEncoderClsid, which is shown in [Retrieving the Class Identifier for an Encoder](-gdiplus-retrieving-the-class-identifier-for-an-encoder-use.md).</span></span>


```
GUID   pageGuid = FrameDimensionPage;
CLSID  encoderClsid;
Image  multi(L"Multiframe.tif");

// Get the CLSID of the PNG encoder.
GetEncoderClsid(L"image/png", &encoderClsid);

// Display and save the first page (index 0).
multi.SelectActiveFrame(&pageGuid, 0);
graphics.DrawImage(&multi, 10, 10);
multi.Save(L"Page0.png", &encoderClsid, NULL);

// Display and save the second page.
multi.SelectActiveFrame(&pageGuid, 1);
graphics.DrawImage(&multi, 200, 10);
multi.Save(L"Page1.png", &encoderClsid, NULL);

// Display and save the third page.
multi.SelectActiveFrame(&pageGuid, 2);
graphics.DrawImage(&multi, 10, 150);
multi.Save(L"Page2.png", &encoderClsid, NULL);

// Display and save the fourth page.
multi.SelectActiveFrame(&pageGuid, 3);
graphics.DrawImage(&multi, 200, 150);
multi.Save(L"Page3.png", &encoderClsid, NULL);
```



<span data-ttu-id="12400-114">In der folgenden Abbildung werden die einzelnen Seiten dargestellt, die im vorangehenden Code angezeigt werden.</span><span class="sxs-lookup"><span data-stu-id="12400-114">The following illustration shows the individual pages as displayed by the preceding code.</span></span>

![Darstellung einer geometrischen Form, eines Farbfotos, eines monochrome Fotos und einer anderen geometrischen Form](images/multiframe1.png)

 

 



