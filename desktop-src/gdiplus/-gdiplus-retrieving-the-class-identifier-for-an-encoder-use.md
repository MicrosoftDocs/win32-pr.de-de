---
description: Die Funktion GetEncoderClsid im folgenden Beispiel empfängt den MIME-Typ eines Encoders und gibt den Klassenbezeichner (CLSID) dieses Encoders zurück.
ms.assetid: f78dac7c-4bc1-4614-8a26-d99d5619399a
title: Abrufen des Klassenbezeichners für einen Encoder
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9a40c31c7ad997ed3e7525ff247019f6a41c681b9523dc523105bd5ba6c7ca6d
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "120014710"
---
# <a name="retrieving-the-class-identifier-for-an-encoder"></a>Abrufen des Klassenbezeichners für einen Encoder

Die Funktion GetEncoderClsid im folgenden Beispiel empfängt den MIME-Typ eines Encoders und gibt den Klassenbezeichner (**CLSID**) dieses Encoders zurück. Die MIME-Typen der in Windows GDI+ sind wie folgt:

-   image/bmp
-   image/jpeg
-   image/gif
-   image/tiff
-   image/png

Die Funktion ruft [**GetImageEncoders auf,**](/windows/desktop/api/Gdiplusimagecodec/nf-gdiplusimagecodec-getimageencoders) um ein Array von [**ImageCodecInfo-Objekten zu**](/windows/win32/api/gdiplusimaging/nl-gdiplusimaging-imagecodecinfo) erhalten. Wenn eines der **ImageCodecInfo-Objekte** in diesem Array den angeforderten Encoder darstellt, gibt die Funktion den Index des **ImageCodecInfo-Objekts** zurück und kopiert die **CLSID** in die Variable, auf die **pClsid zeigt.** Wenn die Funktion fehlschlägt, wird –1 zurückgegeben.


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



Die folgende Konsolenanwendung ruft die GetEncoderClsid-Funktion auf, um die **CLSID** des PNG-Encoders zu bestimmen:


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



Wenn Sie die vorherige Konsolenanwendung ausführen, erhalten Sie eine Ausgabe ähnlich der folgenden:


```
An ImageCodecInfo object representing the PNG encoder
was found at position 4 in the array.
The CLSID of the PNG encoder is {557CF406-1A04-11D3-9A73-0000F81EF32E}.
```



 

 
