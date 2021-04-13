---
description: Windows GDI+ bietet die Funktion "GetImageDecoders", damit Sie bestimmen können, welche Bild-Decoder auf Ihrem Computer verfügbar sind.
ms.assetid: 793e23de-d959-4feb-8bf6-647a455c85ae
title: Auflisten installierter decoderer
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4a20a4e8ac88fa884483ebeaf6592b8085fde807
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104978993"
---
# <a name="listing-installed-decoders"></a><span data-ttu-id="b921d-103">Auflisten installierter decoderer</span><span class="sxs-lookup"><span data-stu-id="b921d-103">Listing Installed Decoders</span></span>

<span data-ttu-id="b921d-104">Windows GDI+ bietet die Funktion " [**GetImageDecoders**](/windows/desktop/api/Gdiplusimagecodec/nf-gdiplusimagecodec-getimagedecoders) ", damit Sie bestimmen können, welche Bild-Decoder auf Ihrem Computer verfügbar sind.</span><span class="sxs-lookup"><span data-stu-id="b921d-104">Windows GDI+ provides the [**GetImageDecoders**](/windows/desktop/api/Gdiplusimagecodec/nf-gdiplusimagecodec-getimagedecoders) function so that you can determine which image decoders are available on your computer.</span></span> <span data-ttu-id="b921d-105">**GetImageDecoders** gibt ein Array von [**ImageCodecInfo**](/windows/win32/api/gdiplusimaging/nl-gdiplusimaging-imagecodecinfo) -Objekten zurück.</span><span class="sxs-lookup"><span data-stu-id="b921d-105">**GetImageDecoders** returns an array of [**ImageCodecInfo**](/windows/win32/api/gdiplusimaging/nl-gdiplusimaging-imagecodecinfo) objects.</span></span> <span data-ttu-id="b921d-106">Vor dem Aufrufen von **GetImageDecoders** müssen Sie einen Puffer zuordnen, der groß genug ist, um das Array zu erhalten.</span><span class="sxs-lookup"><span data-stu-id="b921d-106">Before you call **GetImageDecoders**, you must allocate a buffer large enough to receive that array.</span></span> <span data-ttu-id="b921d-107">Sie können [**getimagedecoderssize**](/windows/desktop/api/Gdiplusimagecodec/nf-gdiplusimagecodec-getimagedecoderssize) aufrufen, um die Größe des erforderlichen Puffers zu bestimmen.</span><span class="sxs-lookup"><span data-stu-id="b921d-107">You can call [**GetImageDecodersSize**](/windows/desktop/api/Gdiplusimagecodec/nf-gdiplusimagecodec-getimagedecoderssize) to determine the size of the required buffer.</span></span>

<span data-ttu-id="b921d-108">In der folgenden Konsolenanwendung werden die verfügbaren Image-Decoders aufgelistet:</span><span class="sxs-lookup"><span data-stu-id="b921d-108">The following console application lists the available image decoders:</span></span>


```
#include <windows.h>
#include <gdiplus.h>
#include <stdio.h>
using namespace Gdiplus;

INT main()
{
   // Initialize GDI+.
   GdiplusStartupInput gdiplusStartupInput;
   ULONG_PTR gdiplusToken;
   GdiplusStartup(&gdiplusToken, &gdiplusStartupInput, NULL);

   UINT  num;        // number of image decoders
   UINT  size;       // size, in bytes, of the image decoder array

   ImageCodecInfo* pImageCodecInfo;

   // How many decoders are there?
   // How big (in bytes) is the array of all ImageCodecInfo objects?
   GetImageDecodersSize(&num, &size);

   // Create a buffer large enough to hold the array of ImageCodecInfo
   // objects that will be returned by GetImageDecoders.
   pImageCodecInfo = (ImageCodecInfo*)(malloc(size));

   // GetImageDecoders creates an array of ImageCodecInfo objects
   // and copies that array into a previously allocated buffer. 
   // The third argument, imageCodecInfo, is a pointer to that buffer. 
   GetImageDecoders(num, size, pImageCodecInfo);

   // Display the graphics file format (MimeType)
   // for each ImageCodecInfo object.
   for(UINT j = 0; j < num; ++j)
   { 
      wprintf(L"%s\n", pImageCodecInfo[j].MimeType);   
   }

   free(pImageCodecInfo);
   GdiplusShutdown(gdiplusToken);
   return 0;
}
```



<span data-ttu-id="b921d-109">Wenn Sie die vorherige Konsolenanwendung ausführen, sieht die Ausgabe in etwa wie folgt aus:</span><span class="sxs-lookup"><span data-stu-id="b921d-109">When you run the preceding console application, the output will be similar to the following:</span></span>


```
image/bmp
image/jpeg
image/gif
image/x-emf
image/x-wmf
image/tiff
image/png
image/x-icon
```



 

 
