---
description: Um die Komprimierungs Ebene beim Speichern eines JPEG-Bilds anzugeben, initialisieren Sie ein EncoderParameters-Objekt, und übergeben Sie die Adresse des Objekts an die Save-Methode der Image-Klasse.
ms.assetid: b8365c00-2223-4aff-9fb2-422976af4c31
title: Festlegen der JPEG-Komprimierungs Ebene
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 07d2e82dfb21e121609d5e09e5c31e2242ec652f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "103751305"
---
# <a name="setting-jpeg-compression-level"></a><span data-ttu-id="8c3c9-103">Festlegen der JPEG-Komprimierungs Ebene</span><span class="sxs-lookup"><span data-stu-id="8c3c9-103">Setting JPEG Compression Level</span></span>

<span data-ttu-id="8c3c9-104">Um die Komprimierungs Ebene beim Speichern eines JPEG-Bilds anzugeben, initialisieren Sie ein [**EncoderParameters**](/windows/win32/api/gdiplusimaging/nl-gdiplusimaging-encoderparameters) -Objekt, und übergeben Sie die Adresse des Objekts an die [Save](/windows/win32/api/gdiplusheaders/nf-gdiplusheaders-image-save(inistream_inconstclsid_inconstencoderparameters)) -Methode der [**Image**](/windows/win32/api/gdiplusheaders/nl-gdiplusheaders-image) -Klasse.</span><span class="sxs-lookup"><span data-stu-id="8c3c9-104">To specify the compression level when you save a JPEG image, initialize an [**EncoderParameters**](/windows/win32/api/gdiplusimaging/nl-gdiplusimaging-encoderparameters) object and pass the address of that object to the [Save](/windows/win32/api/gdiplusheaders/nf-gdiplusheaders-image-save(inistream_inconstclsid_inconstencoderparameters)) method of the [**Image**](/windows/win32/api/gdiplusheaders/nl-gdiplusheaders-image) class.</span></span> <span data-ttu-id="8c3c9-105">Initialisieren Sie das **EncoderParameters** -Objekt, sodass es über ein Array verfügt, das aus einem [**EncoderParameter**](/windows/win32/api/gdiplusimaging/nl-gdiplusimaging-encoderparameter) -Objekt besteht.</span><span class="sxs-lookup"><span data-stu-id="8c3c9-105">Initialize the **EncoderParameters** object so that it has an array consisting of one [**EncoderParameter**](/windows/win32/api/gdiplusimaging/nl-gdiplusimaging-encoderparameter) object.</span></span> <span data-ttu-id="8c3c9-106">Initialisieren Sie dieses einzelne **EncoderParameter** -Objekt, sodass sein **Wertmember** auf einen **ulong** -Wert zwischen 0 und 100 zeigt.</span><span class="sxs-lookup"><span data-stu-id="8c3c9-106">Initialize that one **EncoderParameter** object so that its **Value** member points to a **ULONG** value from 0 through 100.</span></span> <span data-ttu-id="8c3c9-107">Legen Sie den **GUID** -Member des **EncoderParameter** -Objekts auf encoderquality fest.</span><span class="sxs-lookup"><span data-stu-id="8c3c9-107">Set the **Guid** member of the **EncoderParameter** object to EncoderQuality.</span></span>

<span data-ttu-id="8c3c9-108">Die folgende Konsolenanwendung speichert drei JPEG-Bilder, die jeweils eine andere Qualitätsstufe haben.</span><span class="sxs-lookup"><span data-stu-id="8c3c9-108">The following console application saves three JPEG images, each with a different quality level.</span></span> <span data-ttu-id="8c3c9-109">Die Qualitätsstufe 0 steht für die höchste, die Qualitätsstufe 100 für die niedrigste Komprimierung.</span><span class="sxs-lookup"><span data-stu-id="8c3c9-109">A quality level of 0 corresponds to the greatest compression, and a quality level of 100 corresponds to the least compression.</span></span>

<span data-ttu-id="8c3c9-110">Die Main-Funktion basiert auf der-Hilfsfunktion getencoderclsid, die unter [Abrufen des Klassen Bezeichners für einen Encoder](-gdiplus-retrieving-the-class-identifier-for-an-encoder-use.md)angezeigt wird:</span><span class="sxs-lookup"><span data-stu-id="8c3c9-110">The main function relies on the helper function GetEncoderClsid, which is shown in [Retrieving the Class Identifier for an Encoder](-gdiplus-retrieving-the-class-identifier-for-an-encoder-use.md):</span></span>


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

   CLSID             encoderClsid;
   EncoderParameters encoderParameters;
   ULONG             quality;
   Status            stat;

   // Get an image from the disk.
   Image* image = new Image(L"Shapes.bmp");

   // Get the CLSID of the JPEG encoder.
   GetEncoderClsid(L"image/jpeg", &encoderClsid);

   // Before we call Image::Save, we must initialize an
   // EncoderParameters object. The EncoderParameters object
   // has an array of EncoderParameter objects. In this
   // case, there is only one EncoderParameter object in the array.
   // The one EncoderParameter object has an array of values.
   // In this case, there is only one value (of type ULONG)
   // in the array. We will let this value vary from 0 to 100.

   encoderParameters.Count = 1;
   encoderParameters.Parameter[0].Guid = EncoderQuality;
   encoderParameters.Parameter[0].Type = EncoderParameterValueTypeLong;
   encoderParameters.Parameter[0].NumberOfValues = 1;

   // Save the image as a JPEG with quality level 0.
   quality = 0;
   encoderParameters.Parameter[0].Value = &quality;
   stat = image->Save(L"Shapes001.jpg", &encoderClsid, &encoderParameters);

   if(stat == Ok)
      wprintf(L"%s saved successfully.\n", L"Shapes001.jpg");
   else
      wprintf(L"%d  Attempt to save %s failed.\n", stat, L"Shapes001.jpg");

   // Save the image as a JPEG with quality level 50.
   quality = 50;
   encoderParameters.Parameter[0].Value = &quality;
   stat = image->Save(L"Shapes050.jpg", &encoderClsid, &encoderParameters);

   if(stat == Ok)
      wprintf(L"%s saved successfully.\n", L"Shapes050.jpg");
   else
      wprintf(L"%d  Attempt to save %s failed.\n", stat, L"Shapes050.jpg");

      // Save the image as a JPEG with quality level 100.
   quality = 100;
   encoderParameters.Parameter[0].Value = &quality;
   stat = image->Save(L"Shapes100.jpg", &encoderClsid, &encoderParameters);

   if(stat == Ok)
      wprintf(L"%s saved successfully.\n", L"Shapes100.jpg");
   else
      wprintf(L"%d  Attempt to save %s failed.\n", stat, L"Shapes100.jpg");

   delete image;
   GdiplusShutdown(gdiplusToken);
   return 0;
}
```



 

 
