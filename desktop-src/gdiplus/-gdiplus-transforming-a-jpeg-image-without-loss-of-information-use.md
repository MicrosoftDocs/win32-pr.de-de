---
title: Verlustfreie Transformation eines JPEG-Bilds
description: Wenn Sie ein JPEG-Bild komprimieren, gehen einige der Informationen im Bild verloren.
ms.assetid: d7342195-9634-4968-87c1-a94bc6a7e112
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 25ea7011f25a97a228c44bdb87ba09ca8b284ddd
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104977544"
---
# <a name="lossless-transform-of-a-jpeg-image"></a><span data-ttu-id="930c8-103">Verlustfreie Transformation eines JPEG-Bilds</span><span class="sxs-lookup"><span data-stu-id="930c8-103">Lossless transform of a JPEG image</span></span>

<span data-ttu-id="930c8-104">Wenn Sie ein JPEG-Bild komprimieren, gehen einige der Informationen im Bild verloren.</span><span class="sxs-lookup"><span data-stu-id="930c8-104">When you compress a JPEG image, some of the information in the image is lost.</span></span> <span data-ttu-id="930c8-105">Wenn Sie eine JPEG-Datei öffnen, das Bild ändern und es in einer anderen JPEG-Datei speichern, wird die Qualität verringert.</span><span class="sxs-lookup"><span data-stu-id="930c8-105">If you open a JPEG file, alter the image, and save it to another JPEG file, the quality will decrease.</span></span> <span data-ttu-id="930c8-106">Wenn Sie diesen Prozess mehrmals wiederholen, wird eine deutliche Beeinträchtigung der Bildqualität festzustellen.</span><span class="sxs-lookup"><span data-stu-id="930c8-106">If you repeat that process many times, you will see a substantial degradation in the image quality.</span></span>

<span data-ttu-id="930c8-107">Da JPEG eines der beliebtesten Bildformate im Internet ist und die Benutzer häufig JPEG-Bilder ändern möchten, bietet GDI+ die folgenden Transformationen, die für JPEG-Bilder ohne Informationsverlust ausgeführt werden können:</span><span class="sxs-lookup"><span data-stu-id="930c8-107">Because JPEG is one of the most popular image formats on the Web, and because people often like to modify JPEG images, GDI+ provides the following transformations that can be performed on JPEG images without loss of information:</span></span>

-   <span data-ttu-id="930c8-108">Drehen von 90 Grad</span><span class="sxs-lookup"><span data-stu-id="930c8-108">Rotate 90 degrees</span></span>
-   <span data-ttu-id="930c8-109">Drehen von 180 Grad</span><span class="sxs-lookup"><span data-stu-id="930c8-109">Rotate 180 degrees</span></span>
-   <span data-ttu-id="930c8-110">Drehen von 270 Grad</span><span class="sxs-lookup"><span data-stu-id="930c8-110">Rotate 270 degrees</span></span>
-   <span data-ttu-id="930c8-111">Horizontal kippen</span><span class="sxs-lookup"><span data-stu-id="930c8-111">Flip horizontally</span></span>
-   <span data-ttu-id="930c8-112">Vertikal kippen</span><span class="sxs-lookup"><span data-stu-id="930c8-112">Flip vertically</span></span>

<span data-ttu-id="930c8-113">Sie können eine der Transformationen, die in der vorangehenden Liste angezeigt werden, anwenden, wenn Sie die [Save](/windows/win32/api/gdiplusheaders/nf-gdiplusheaders-image-save(inistream_inconstclsid_inconstencoderparameters)) -Methode eines [**Bild**](/windows/win32/api/gdiplusheaders/nl-gdiplusheaders-image) Objekts aufzurufen.</span><span class="sxs-lookup"><span data-stu-id="930c8-113">You can apply one of the transformations shown in the preceding list when you call the [Save](/windows/win32/api/gdiplusheaders/nf-gdiplusheaders-image-save(inistream_inconstclsid_inconstencoderparameters)) method of an [**Image**](/windows/win32/api/gdiplusheaders/nl-gdiplusheaders-image) object.</span></span> <span data-ttu-id="930c8-114">Wenn die folgenden Bedingungen erfüllt sind, wird die Transformation ohne Informationsverlust fortgesetzt:</span><span class="sxs-lookup"><span data-stu-id="930c8-114">If the following conditions are met, then the transformation will proceed without loss of information:</span></span>

-   <span data-ttu-id="930c8-115">Die Datei, die zum Erstellen des [**Image**](/windows/win32/api/gdiplusheaders/nl-gdiplusheaders-image) -Objekts verwendet wird, ist eine JPEG-Datei.</span><span class="sxs-lookup"><span data-stu-id="930c8-115">The file used to construct the [**Image**](/windows/win32/api/gdiplusheaders/nl-gdiplusheaders-image) object is a JPEG file.</span></span>
-   <span data-ttu-id="930c8-116">Breite und Höhe des Bilds sind jeweils ein Vielfaches von 16.</span><span class="sxs-lookup"><span data-stu-id="930c8-116">The width and height of the image are both multiples of 16.</span></span>

<span data-ttu-id="930c8-117">Wenn die Breite und Höhe des Bilds nicht gleichzeitig ein Vielfaches von 16 ist, wird die Bildqualität von GDI+ am besten beibehalten, wenn Sie eine der Drehung-oder flippingtransformationen anwenden, die in der vorangehenden Liste angezeigt werden.</span><span class="sxs-lookup"><span data-stu-id="930c8-117">If the width and height of the image are not both multiples of 16, GDI+ will do its best to preserve the image quality when you apply one of the rotation or flipping transformations shown in the preceding list.</span></span>

<span data-ttu-id="930c8-118">Zum Transformieren eines JPEG-Bilds initialisieren Sie ein [**EncoderParameters**](/windows/win32/api/gdiplusimaging/nl-gdiplusimaging-encoderparameters) -Objekt, und übergeben Sie die Adresse des Objekts an die [Save](/windows/win32/api/gdiplusheaders/nf-gdiplusheaders-image-save(inistream_inconstclsid_inconstencoderparameters)) -Methode der [**Image**](/windows/win32/api/gdiplusheaders/nl-gdiplusheaders-image) -Klasse.</span><span class="sxs-lookup"><span data-stu-id="930c8-118">To transform a JPEG image, initialize an [**EncoderParameters**](/windows/win32/api/gdiplusimaging/nl-gdiplusimaging-encoderparameters) object and pass the address of that object to the [Save](/windows/win32/api/gdiplusheaders/nf-gdiplusheaders-image-save(inistream_inconstclsid_inconstencoderparameters)) method of the [**Image**](/windows/win32/api/gdiplusheaders/nl-gdiplusheaders-image) class.</span></span> <span data-ttu-id="930c8-119">Initialisieren Sie das **EncoderParameters** -Objekt so, dass es über ein Array verfügt, das aus einem [**EncoderParameter**](/windows/win32/api/gdiplusimaging/nl-gdiplusimaging-encoderparameter) -Objekt besteht.</span><span class="sxs-lookup"><span data-stu-id="930c8-119">Initialize the **EncoderParameters** object so that it has an array that consists of one [**EncoderParameter**](/windows/win32/api/gdiplusimaging/nl-gdiplusimaging-encoderparameter) object.</span></span> <span data-ttu-id="930c8-120">Initialisieren Sie dieses einzelne **EncoderParameter** -Objekt, sodass sein **Wertmember** auf eine **ulong** -Variable verweist, die eines der folgenden Elemente der [**EncoderValue**](/windows/win32/api/Gdiplusenums/ne-gdiplusenums-encodervalue) -Enumeration enthält:</span><span class="sxs-lookup"><span data-stu-id="930c8-120">Initialize that one **EncoderParameter** object so that its **Value** member points to a **ULONG** variable that holds one of the following elements of the [**EncoderValue**](/windows/win32/api/Gdiplusenums/ne-gdiplusenums-encodervalue) enumeration:</span></span>

-   <span data-ttu-id="930c8-121">EncoderValueTransformRotate90,</span><span class="sxs-lookup"><span data-stu-id="930c8-121">EncoderValueTransformRotate90,</span></span>
-   <span data-ttu-id="930c8-122">EncoderValueTransformRotate180,</span><span class="sxs-lookup"><span data-stu-id="930c8-122">EncoderValueTransformRotate180,</span></span>
-   <span data-ttu-id="930c8-123">EncoderValueTransformRotate270,</span><span class="sxs-lookup"><span data-stu-id="930c8-123">EncoderValueTransformRotate270,</span></span>
-   <span data-ttu-id="930c8-124">Encodervaluetransformfliphorizontal,</span><span class="sxs-lookup"><span data-stu-id="930c8-124">EncoderValueTransformFlipHorizontal,</span></span>
-   <span data-ttu-id="930c8-125">Encodervaluetransformflipvertical</span><span class="sxs-lookup"><span data-stu-id="930c8-125">EncoderValueTransformFlipVertical</span></span>

<span data-ttu-id="930c8-126">Legen Sie den **GUID** -Member des [**EncoderParameter**](/windows/win32/api/gdiplusimaging/nl-gdiplusimaging-encoderparameter) -Objekts auf encodertransformation fest.</span><span class="sxs-lookup"><span data-stu-id="930c8-126">Set the **Guid** member of the [**EncoderParameter**](/windows/win32/api/gdiplusimaging/nl-gdiplusimaging-encoderparameter) object to EncoderTransformation.</span></span>

<span data-ttu-id="930c8-127">Die folgende Konsolenanwendung erstellt ein [**Image**](/windows/win32/api/gdiplusheaders/nl-gdiplusheaders-image) -Objekt aus einer JPEG-Datei und speichert das Bild dann in einer neuen Datei.</span><span class="sxs-lookup"><span data-stu-id="930c8-127">The following console application creates an [**Image**](/windows/win32/api/gdiplusheaders/nl-gdiplusheaders-image) object from a JPEG file and then saves the image to a new file.</span></span> <span data-ttu-id="930c8-128">Während des Speicher Vorgangs wird das Bild um 90 Grad gedreht.</span><span class="sxs-lookup"><span data-stu-id="930c8-128">During the save process, the image is rotated 90 degrees.</span></span> <span data-ttu-id="930c8-129">Wenn die Breite und Höhe des Bilds ein Vielfaches von 16 ist, verursacht der Prozess der Rotation und Speicherung des Bilds keinen Verlust von Informationen.</span><span class="sxs-lookup"><span data-stu-id="930c8-129">If the width and height of the image are both multiples of 16, the process of rotating and saving the image causes no loss of information.</span></span>

<span data-ttu-id="930c8-130">Die Main-Funktion basiert auf der-Hilfsfunktion getencoderclsid, die unter [Abrufen des Klassen Bezeichners für einen Encoder](-gdiplus-retrieving-the-class-identifier-for-an-encoder-use.md)angezeigt wird.</span><span class="sxs-lookup"><span data-stu-id="930c8-130">The main function relies on the helper function GetEncoderClsid, which is shown in [Retrieving the Class Identifier for an Encoder](-gdiplus-retrieving-the-class-identifier-for-an-encoder-use.md).</span></span>


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
   ULONG             transformation;
   UINT              width;
   UINT              height;
   Status            stat;

   // Get a JPEG image from the disk.
   Image* image = new Image(L"Shapes.jpg");

   // Determine whether the width and height of the image 
   // are multiples of 16.
   width = image->GetWidth();
   height = image->GetHeight();

   printf("The width of the image is %u", width);
   if(width / 16.0 - width / 16 == 0)
      printf(", which is a multiple of 16.\n");
   else
      printf(", which is not a multiple of 16.\n");

   printf("The height of the image is %u", height);
   if(height / 16.0 - height / 16 == 0)
      printf(", which is a multiple of 16.\n");
   else
      printf(", which is not a multiple of 16.\n");

   // Get the CLSID of the JPEG encoder.
   GetEncoderClsid(L"image/jpeg", &encoderClsid);

   // Before we call Image::Save, we must initialize an
   // EncoderParameters object. The EncoderParameters object
   // has an array of EncoderParameter objects. In this
   // case, there is only one EncoderParameter object in the array.
   // The one EncoderParameter object has an array of values.
   // In this case, there is only one value (of type ULONG)
   // in the array. We will set that value to EncoderValueTransformRotate90.

   encoderParameters.Count = 1;
   encoderParameters.Parameter[0].Guid = EncoderTransformation;
   encoderParameters.Parameter[0].Type = EncoderParameterValueTypeLong;
   encoderParameters.Parameter[0].NumberOfValues = 1;

   // Rotate and save the image.
   transformation = EncoderValueTransformRotate90;
   encoderParameters.Parameter[0].Value = &transformation;
   stat = image->Save(L"ShapesR90.jpg", &encoderClsid, &encoderParameters);

   if(stat == Ok)
      wprintf(L"%s saved successfully.\n", L"ShapesR90.jpg");
   else
      wprintf(L"%d  Attempt to save %s failed.\n", stat, L"ShapesR90.jpg");

   delete image;
   GdiplusShutdown(gdiplusToken);
   return 0;
}
```



 

 
