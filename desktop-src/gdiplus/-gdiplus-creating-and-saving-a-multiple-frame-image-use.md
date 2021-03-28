---
description: Mit bestimmten Dateiformaten können Sie mehrere Bilder (Frames) in einer einzelnen Datei speichern.
ms.assetid: 9b61e01d-0a98-4ac3-865e-7570ed0c3cde
title: Erstellen und Speichern eines Bilds mit mehreren Frames
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 532a8fc8f8fc7e8742651f3d3853e001d493609b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104131356"
---
# <a name="creating-and-saving-a-multiple-frame-image"></a><span data-ttu-id="2519c-103">Erstellen und Speichern eines Bilds mit mehreren Frames</span><span class="sxs-lookup"><span data-stu-id="2519c-103">Creating and Saving a Multiple-Frame Image</span></span>

<span data-ttu-id="2519c-104">Mit bestimmten Dateiformaten können Sie mehrere Bilder (Frames) in einer einzelnen Datei speichern.</span><span class="sxs-lookup"><span data-stu-id="2519c-104">With certain file formats, you can save multiple images (frames) to a single file.</span></span> <span data-ttu-id="2519c-105">Beispielsweise können Sie mehrere Seiten in einer einzelnen TIFF-Datei speichern.</span><span class="sxs-lookup"><span data-stu-id="2519c-105">For example, you can save several pages to a single TIFF file.</span></span> <span data-ttu-id="2519c-106">Um die erste Seite zu speichern, nennen Sie die [Save](/windows/win32/api/gdiplusheaders/nf-gdiplusheaders-image-save(inistream_inconstclsid_inconstencoderparameters)) -Methode der [**Image**](/windows/win32/api/gdiplusheaders/nl-gdiplusheaders-image) -Klasse.</span><span class="sxs-lookup"><span data-stu-id="2519c-106">To save the first page, call the [Save](/windows/win32/api/gdiplusheaders/nf-gdiplusheaders-image-save(inistream_inconstclsid_inconstencoderparameters)) method of the [**Image**](/windows/win32/api/gdiplusheaders/nl-gdiplusheaders-image) class.</span></span> <span data-ttu-id="2519c-107">Um nachfolgende Seiten zu speichern, nennen [Sie die SaveAdd](/windows/win32/api/gdiplusheaders/nf-gdiplusheaders-image-saveadd(inimage_inconstencoderparameters)) -Methode der **Image** -Klasse.</span><span class="sxs-lookup"><span data-stu-id="2519c-107">To save subsequent pages, call the [SaveAdd](/windows/win32/api/gdiplusheaders/nf-gdiplusheaders-image-saveadd(inimage_inconstencoderparameters)) method of the **Image** class.</span></span>

> [!Note]  
> <span data-ttu-id="2519c-108">Sie können " [SaveAdd](/windows/win32/api/gdiplusheaders/nf-gdiplusheaders-image-saveadd(inimage_inconstencoderparameters)) " nicht verwenden, um einer animierten GIF-Datei Frames hinzuzufügen.</span><span class="sxs-lookup"><span data-stu-id="2519c-108">You cannot use [SaveAdd](/windows/win32/api/gdiplusheaders/nf-gdiplusheaders-image-saveadd(inimage_inconstencoderparameters)) to add frames to an animated gif file.</span></span>

 

<span data-ttu-id="2519c-109">Die folgende Konsolenanwendung erstellt eine TIFF-Datei mit vier Seiten.</span><span class="sxs-lookup"><span data-stu-id="2519c-109">The following console application creates a TIFF file with four pages.</span></span> <span data-ttu-id="2519c-110">Die Bilder, die zu den Seiten der TIFF-Datei werden, stammen aus vier Datenträger Dateien: Shapes.bmp, Cereal.gif, Iron.jpg und House.png.</span><span class="sxs-lookup"><span data-stu-id="2519c-110">The images that become the pages of the TIFF file come from four disk files: Shapes.bmp, Cereal.gif, Iron.jpg, and House.png.</span></span> <span data-ttu-id="2519c-111">Der Code erstellt zunächst vier [**Bild**](/windows/win32/api/gdiplusheaders/nl-gdiplusheaders-image) Objekte: **Multi,** **Page2**, **page3** und **PAGE4**.</span><span class="sxs-lookup"><span data-stu-id="2519c-111">The code first constructs four [**Image**](/windows/win32/api/gdiplusheaders/nl-gdiplusheaders-image) objects: **multi**, **page2**, **page3**, and **page4**.</span></span> <span data-ttu-id="2519c-112">Zunächst enthält " **Multi"** nur das Bild aus Shapes.bmp, aber schließlich enthält es alle vier Bilder.</span><span class="sxs-lookup"><span data-stu-id="2519c-112">At first, **multi** contains only the image from Shapes.bmp, but eventually it contains all four images.</span></span> <span data-ttu-id="2519c-113">Wenn die einzelnen Seiten zum Objekt mit **mehreren**  **Bildern** hinzugefügt werden, werden Sie auch der Datenträger Datei Multiframe. TIF hinzugefügt.</span><span class="sxs-lookup"><span data-stu-id="2519c-113">As the individual pages are added to the **multi**  **Image** object, they are also added to the disk file Multiframe.tif.</span></span>

<span data-ttu-id="2519c-114">Beachten Sie, dass der Code [Speichern](/windows/win32/api/gdiplusheaders/nf-gdiplusheaders-image-save(inistream_inconstclsid_inconstencoderparameters)) (nicht [SaveAdd](/windows/win32/api/gdiplusheaders/nf-gdiplusheaders-image-saveadd(inimage_inconstencoderparameters))) aufruft, um die erste Seite zu speichern.</span><span class="sxs-lookup"><span data-stu-id="2519c-114">Note that the code calls [Save](/windows/win32/api/gdiplusheaders/nf-gdiplusheaders-image-save(inistream_inconstclsid_inconstencoderparameters)) (not [SaveAdd](/windows/win32/api/gdiplusheaders/nf-gdiplusheaders-image-saveadd(inimage_inconstencoderparameters))) to save the first page.</span></span> <span data-ttu-id="2519c-115">Das erste Argument, das an die Save-Methode übermittelt wird, ist der Name der Datenträger Datei, die schließlich mehrere Frames enthält.</span><span class="sxs-lookup"><span data-stu-id="2519c-115">The first argument passed to the Save method is the name of the disk file that will eventually contain several frames.</span></span> <span data-ttu-id="2519c-116">Das zweite Argument, das an die Save-Methode übermittelt wird, gibt den Encoder an, der zum Konvertieren der Daten im **multiimage**[](/windows/win32/api/gdiplusheaders/nl-gdiplusheaders-image) -Objekt in das Format (in diesem Fall TIFF) verwendet wird, das für die Datenträger Datei erforderlich ist.  </span><span class="sxs-lookup"><span data-stu-id="2519c-116">The second argument passed to the Save method specifies the encoder that will be used to convert the data in the **multi**  [**Image**](/windows/win32/api/gdiplusheaders/nl-gdiplusheaders-image) object to the format (in this case TIFF) required by the disk file.</span></span> <span data-ttu-id="2519c-117">Derselbe Encoder wird automatisch von allen nachfolgenden Aufrufen der SaveAdd-Methode des Objekts mit **mehreren**  **Bildern** verwendet.</span><span class="sxs-lookup"><span data-stu-id="2519c-117">That same encoder is used automatically by all subsequent calls to the SaveAdd method of the **multi**  **Image** object.</span></span>

<span data-ttu-id="2519c-118">Das dritte Argument, das an die [Save](/windows/win32/api/gdiplusheaders/nf-gdiplusheaders-image-save(inistream_inconstclsid_inconstencoderparameters)) -Methode übermittelt wird, ist die Adresse eines [**EncoderParameters**](/windows/win32/api/gdiplusimaging/nl-gdiplusimaging-encoderparameters) -Objekts.</span><span class="sxs-lookup"><span data-stu-id="2519c-118">The third argument passed to the [Save](/windows/win32/api/gdiplusheaders/nf-gdiplusheaders-image-save(inistream_inconstclsid_inconstencoderparameters)) method is the address of an [**EncoderParameters**](/windows/win32/api/gdiplusimaging/nl-gdiplusimaging-encoderparameters) object.</span></span> <span data-ttu-id="2519c-119">Das **EncoderParameters** -Objekt verfügt über ein Array, das ein einzelnes [**EncoderParameter**](/windows/win32/api/gdiplusimaging/nl-gdiplusimaging-encoderparameter) -Objekt enthält.</span><span class="sxs-lookup"><span data-stu-id="2519c-119">The **EncoderParameters** object has an array that contains a single [**EncoderParameter**](/windows/win32/api/gdiplusimaging/nl-gdiplusimaging-encoderparameter) object.</span></span> <span data-ttu-id="2519c-120">Der **GUID** -Member dieses **EncoderParameter** -Objekts ist auf encodersaveflag festgelegt.</span><span class="sxs-lookup"><span data-stu-id="2519c-120">The **Guid** member of that **EncoderParameter** object is set to EncoderSaveFlag.</span></span> <span data-ttu-id="2519c-121">Der **Wertmember** des **EncoderParameter** -Objekts verweist auf einen **ulong** -Wert, der den Wert encodervaluemultiframe enthält.</span><span class="sxs-lookup"><span data-stu-id="2519c-121">The **Value** member of the **EncoderParameter** object points to a **ULONG** that contains the value EncoderValueMultiFrame.</span></span>

<span data-ttu-id="2519c-122">Im Code werden die zweiten, dritten und vierten Seiten gespeichert, indem die [SaveAdd](/windows/win32/api/gdiplusheaders/nf-gdiplusheaders-image-saveadd(inimage_inconstencoderparameters)) -Methode des Objekts mit **mehreren**  [**Bildern**](/windows/win32/api/gdiplusheaders/nl-gdiplusheaders-image) aufgerufen wird.</span><span class="sxs-lookup"><span data-stu-id="2519c-122">The code saves the second, third, and fourth pages by calling the [SaveAdd](/windows/win32/api/gdiplusheaders/nf-gdiplusheaders-image-saveadd(inimage_inconstencoderparameters)) method of the **multi**  [**Image**](/windows/win32/api/gdiplusheaders/nl-gdiplusheaders-image) object.</span></span> <span data-ttu-id="2519c-123">Das erste Argument, das an die SaveAdd-Methode übermittelt wird, ist die Adresse eines **Bild** Objekts.</span><span class="sxs-lookup"><span data-stu-id="2519c-123">The first argument passed to the SaveAdd method is the address of an **Image** object.</span></span> <span data-ttu-id="2519c-124">Das Bild in diesem **Bild** Objekt wird dem **multiimage** -Objekt hinzugefügt und außerdem der Multiframe. TIF-Datenträger Datei hinzugefügt.  </span><span class="sxs-lookup"><span data-stu-id="2519c-124">The image in that **Image** object is added to the **multi**  **Image** object and is also added to the Multiframe.tif disk file.</span></span> <span data-ttu-id="2519c-125">Das zweite Argument, das an die SaveAdd-Methode übermittelt wird, ist die Adresse desselben [**EncoderParameters**](/windows/win32/api/gdiplusimaging/nl-gdiplusimaging-encoderparameters) -Objekts, das von der [Save](/windows/win32/api/gdiplusheaders/nf-gdiplusheaders-image-save(inistream_inconstclsid_inconstencoderparameters)) -Methode verwendet wurde.</span><span class="sxs-lookup"><span data-stu-id="2519c-125">The second argument passed to the SaveAdd method is the address of the same [**EncoderParameters**](/windows/win32/api/gdiplusimaging/nl-gdiplusimaging-encoderparameters) object that was used by the [Save](/windows/win32/api/gdiplusheaders/nf-gdiplusheaders-image-save(inistream_inconstclsid_inconstencoderparameters)) method.</span></span> <span data-ttu-id="2519c-126">Der Unterschied besteht darin, dass der **ulong** , auf den der **Wertemember** zeigt, jetzt den Wert encodervalueframedimensionpage enthält.</span><span class="sxs-lookup"><span data-stu-id="2519c-126">The difference is that the **ULONG** pointed to by the **Value** member now contains the value EncoderValueFrameDimensionPage.</span></span>

<span data-ttu-id="2519c-127">Die Main-Funktion basiert auf der-Hilfsfunktion getencoderclsid, die unter [Abrufen des Klassen Bezeichners für einen Encoder](-gdiplus-retrieving-the-class-identifier-for-an-encoder-use.md)angezeigt wird.</span><span class="sxs-lookup"><span data-stu-id="2519c-127">The main function relies on the helper function GetEncoderClsid, which is shown in [Retrieving the Class Identifier for an Encoder](-gdiplus-retrieving-the-class-identifier-for-an-encoder-use.md).</span></span>


```
#include <windows.h>
#include <gdiplus.h>
#include <stdio.h>
using namespace Gdiplus;

INT GetEncoderClsid(const WCHAR* format, CLSID* pClsid);  // helper function

INT main()
{
   // Initialize GDI+.
   GdiplusStartupInput gdiplusStartupInput;
   ULONG_PTR gdiplusToken;
   GdiplusStartup(&gdiplusToken, &gdiplusStartupInput, NULL);

   EncoderParameters encoderParameters;
   ULONG             parameterValue;
   Status            stat;

   // An EncoderParameters object has an array of
   // EncoderParameter objects. In this case, there is only
   // one EncoderParameter object in the array.
   encoderParameters.Count = 1;

   // Initialize the one EncoderParameter object.
   encoderParameters.Parameter[0].Guid = EncoderSaveFlag;
   encoderParameters.Parameter[0].Type = EncoderParameterValueTypeLong;
   encoderParameters.Parameter[0].NumberOfValues = 1;
   encoderParameters.Parameter[0].Value = &parameterValue;

   // Get the CLSID of the TIFF encoder.
   CLSID encoderClsid;
   GetEncoderClsid(L"image/tiff", &encoderClsid);

   // Create four image objects.
   Image* multi = new Image(L"Shapes.bmp");
   Image* page2 = new Image(L"Cereal.gif");
   Image* page3 = new Image(L"Iron.jpg");
   Image* page4 = new Image(L"House.png");

   // Save the first page (frame).
   parameterValue = EncoderValueMultiFrame;
   stat = multi->Save(L"MultiFrame.tif", &encoderClsid, &encoderParameters);
   if(stat == Ok)
      printf("Page 1 saved successfully.\n");

   // Save the second page (frame).
   parameterValue = EncoderValueFrameDimensionPage;
   stat = multi->SaveAdd(page2, &encoderParameters);
   if(stat == Ok)
      printf("Page 2 saved successfully.\n");

   // Save the third page (frame).
   parameterValue = EncoderValueFrameDimensionPage;
   stat = multi->SaveAdd(page3, &encoderParameters);
   if(stat == Ok)
      printf("Page 3 saved successfully.\n");

   // Save the fourth page (frame).
   parameterValue = EncoderValueFrameDimensionPage;
   stat = multi->SaveAdd(page4, &encoderParameters);
   if(stat == Ok)
      printf("Page 4 saved successfully.\n");

   // Close the multiframe file.
   parameterValue = EncoderValueFlush;
   stat = multi->SaveAdd(&encoderParameters);
   if(stat == Ok)
      printf("File closed successfully.\n");

   delete multi;
   delete page2;
   delete page3;
   delete page4;
   GdiplusShutdown(gdiplusToken);
   return 0;
}
```



 

 
