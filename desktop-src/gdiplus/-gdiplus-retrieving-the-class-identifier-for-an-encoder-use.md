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
# <a name="retrieving-the-class-identifier-for-an-encoder"></a>Abrufen des Klassen Bezeichners für einen Encoder

Die Funktion getencoderclsid im folgenden Beispiel empfängt den MIME-Typ eines Encoders und gibt den Klassen Bezeichner (**CLSID**) dieses Encoders zurück. Die MIME-Typen der in Windows GDI+ integrierten Codierern lauten wie folgt:

-   image/bmp
-   image/jpeg
-   image/gif
-   image/tiff
-   image/png

Die-Funktion ruft [**GetImageEncoders**](/windows/desktop/api/Gdiplusimagecodec/nf-gdiplusimagecodec-getimageencoders) auf, um ein Array von [**ImageCodecInfo**](/windows/win32/api/gdiplusimaging/nl-gdiplusimaging-imagecodecinfo) -Objekten zu erhalten. Wenn eines der **ImageCodecInfo** -Objekte in diesem Array den angeforderten Encoder darstellt, gibt die Funktion den Index des **ImageCodecInfo** -Objekts zurück und kopiert die **CLSID** in die Variable, auf die von **pclsid** verwiesen wird. Wenn die Funktion fehlschlägt, wird – 1 zurückgegeben.


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



Die folgende Konsolenanwendung ruft die getencoderclsid-Funktion auf, um die **CLSID** des PNG-Encoders zu ermitteln:


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



Wenn Sie die vorherige Konsolenanwendung ausführen, erhalten Sie eine Ausgabe wie die folgende:


```
An ImageCodecInfo object representing the PNG encoder
was found at position 4 in the array.
The CLSID of the PNG encoder is {557CF406-1A04-11D3-9A73-0000F81EF32E}.
```



 

 
