---
description: Die Funktion getencoderclsid im folgenden Beispiel empfängt den MIME-Typ eines Encoders und gibt den Klassen Bezeichner (CLSID) dieses Encoders zurück.
ms.assetid: f78dac7c-4bc1-4614-8a26-d99d5619399a
title: Abrufen des Klassen Bezeichners für einen Encoder
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a03193bfa9f2e86e92f66a649280828f12d4807c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104978945"
---
# <a name="retrieving-the-class-identifier-for-an-encoder"></a><span data-ttu-id="ae759-103">Abrufen des Klassen Bezeichners für einen Encoder</span><span class="sxs-lookup"><span data-stu-id="ae759-103">Retrieving the Class Identifier for an Encoder</span></span>

<span data-ttu-id="ae759-104">Die Funktion getencoderclsid im folgenden Beispiel empfängt den MIME-Typ eines Encoders und gibt den Klassen Bezeichner (**CLSID**) dieses Encoders zurück.</span><span class="sxs-lookup"><span data-stu-id="ae759-104">The function GetEncoderClsid in the following example receives the MIME type of an encoder and returns the class identifier (**CLSID**) of that encoder.</span></span> <span data-ttu-id="ae759-105">Die MIME-Typen der in Windows GDI+ integrierten Codierern lauten wie folgt:</span><span class="sxs-lookup"><span data-stu-id="ae759-105">The MIME types of the encoders built into Windows GDI+ are as follows:</span></span>

-   <span data-ttu-id="ae759-106">image/bmp</span><span class="sxs-lookup"><span data-stu-id="ae759-106">image/bmp</span></span>
-   <span data-ttu-id="ae759-107">image/jpeg</span><span class="sxs-lookup"><span data-stu-id="ae759-107">image/jpeg</span></span>
-   <span data-ttu-id="ae759-108">image/gif</span><span class="sxs-lookup"><span data-stu-id="ae759-108">image/gif</span></span>
-   <span data-ttu-id="ae759-109">image/tiff</span><span class="sxs-lookup"><span data-stu-id="ae759-109">image/tiff</span></span>
-   <span data-ttu-id="ae759-110">image/png</span><span class="sxs-lookup"><span data-stu-id="ae759-110">image/png</span></span>

<span data-ttu-id="ae759-111">Die-Funktion ruft [**GetImageEncoders**](/windows/desktop/api/Gdiplusimagecodec/nf-gdiplusimagecodec-getimageencoders) auf, um ein Array von [**ImageCodecInfo**](/windows/win32/api/gdiplusimaging/nl-gdiplusimaging-imagecodecinfo) -Objekten zu erhalten.</span><span class="sxs-lookup"><span data-stu-id="ae759-111">The function calls [**GetImageEncoders**](/windows/desktop/api/Gdiplusimagecodec/nf-gdiplusimagecodec-getimageencoders) to get an array of [**ImageCodecInfo**](/windows/win32/api/gdiplusimaging/nl-gdiplusimaging-imagecodecinfo) objects.</span></span> <span data-ttu-id="ae759-112">Wenn eines der **ImageCodecInfo** -Objekte in diesem Array den angeforderten Encoder darstellt, gibt die Funktion den Index des **ImageCodecInfo** -Objekts zurück und kopiert die **CLSID** in die Variable, auf die von **pclsid** verwiesen wird.</span><span class="sxs-lookup"><span data-stu-id="ae759-112">If one of the **ImageCodecInfo** objects in that array represents the requested encoder, the function returns the index of the **ImageCodecInfo** object and copies the **CLSID** into the variable pointed to by **pClsid**.</span></span> <span data-ttu-id="ae759-113">Wenn die Funktion fehlschlägt, wird – 1 zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="ae759-113">If the function fails, it returns –1.</span></span>


```
int GetEncoderClsid(const WCHAR* format, CLSID* pClsid)
{
   UINT  num = 0;          // number of image encoders
   UINT  size = 0;         // size of the image encoder array in bytes

   ImageCodecInfo* pImageCodecInfo = NULL;

   GetImageEncodersSize(&num, &size);
   if(size == 0)
      return -1;  // Failure

   pImageCodecInfo = (ImageCodecInfo*)(malloc(size));
   if(pImageCodecInfo == NULL)
      return -1;  // Failure

   GetImageEncoders(num, size, pImageCodecInfo);

   for(UINT j = 0; j < num; ++j)
   {
      if( wcscmp(pImageCodecInfo[j].MimeType, format) == 0 )
      {
         *pClsid = pImageCodecInfo[j].Clsid;
         free(pImageCodecInfo);
         return j;  // Success
      }    
   }

   free(pImageCodecInfo);
   return -1;  // Failure
}
```



<span data-ttu-id="ae759-114">Die folgende Konsolenanwendung ruft die getencoderclsid-Funktion auf, um die **CLSID** des PNG-Encoders zu ermitteln:</span><span class="sxs-lookup"><span data-stu-id="ae759-114">The following console application calls the GetEncoderClsid function to determine the **CLSID** of the PNG encoder:</span></span>


```
#include <windows.h>
#include <gdiplus.h>
#include <stdio.h>
using namespace Gdiplus;

#include "GdiplusHelperFunctions.h"

INT main()
{
   // Initialize GDI+.
   GdiplusStartupInput gdiplusStartupInput;
   ULONG_PTR gdiplusToken;
   GdiplusStartup(&gdiplusToken, &gdiplusStartupInput, NULL);

   CLSID  encoderClsid;
   INT    result;
   WCHAR  strGuid[39];

   result = GetEncoderClsid(L"image/png", &encoderClsid);

   if(result < 0)
   {
      printf("The PNG encoder is not installed.\n");
   }
   else
   {
      StringFromGUID2(encoderClsid, strGuid, 39);
      printf("An ImageCodecInfo object representing the PNG encoder\n");
      printf("was found at position %d in the array.\n", result);
      wprintf(L"The CLSID of the PNG encoder is %s.\n", strGuid);
   }

   GdiplusShutdown(gdiplusToken);
   return 0;
}
```



<span data-ttu-id="ae759-115">Wenn Sie die vorherige Konsolenanwendung ausführen, erhalten Sie eine Ausgabe wie die folgende:</span><span class="sxs-lookup"><span data-stu-id="ae759-115">When you run the preceding console application, you get an output similar to the following:</span></span>


```
An ImageCodecInfo object representing the PNG encoder
was found at position 4 in the array.
The CLSID of the PNG encoder is {557CF406-1A04-11D3-9A73-0000F81EF32E}.
```



 

 
