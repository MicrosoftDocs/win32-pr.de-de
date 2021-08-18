---
title: Verlustfreie Transformation eines JPEG-Bilds
description: Wenn Sie ein JPEG-Bild komprimieren, geht ein Teil der Informationen im Bild verloren.
ms.assetid: d7342195-9634-4968-87c1-a94bc6a7e112
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 67152084f95220db3fe7afecfa4be07b366a92b31eb713ec192a2805ecb42ea9
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118977290"
---
# <a name="lossless-transform-of-a-jpeg-image"></a>Verlustfreie Transformation eines JPEG-Bilds

Wenn Sie ein JPEG-Bild komprimieren, geht ein Teil der Informationen im Bild verloren. Wenn Sie eine JPEG-Datei öffnen, das Bild ändern und in einer anderen JPEG-Datei speichern, wird die Qualität verringert. Wenn Sie diesen Vorgang mehrmals wiederholen, kommt es zu einer erheblichen Beeinträchtigung der Imagequalität.

Da JPEG eines der beliebtesten Bildformate im Web ist und Personen häufig JPEG-Bilder ändern möchten, bietet GDI+ die folgenden Transformationen, die ohne Informationsverlust für JPEG-Bilder ausgeführt werden können:

-   Um 90 Grad drehen
-   Um 180° drehen Grad
-   Um 270° drehen Grad
-   Horizontales Flippen
-   Vertikal drehen

Sie können eine der Transformationen anwenden, die in der vorherigen Liste angezeigt werden, wenn Sie die [Save-Methode](/windows/win32/api/gdiplusheaders/nf-gdiplusheaders-image-save(inistream_inconstclsid_inconstencoderparameters)) eines [**Image-Objekts**](/windows/win32/api/gdiplusheaders/nl-gdiplusheaders-image) aufrufen. Wenn die folgenden Bedingungen erfüllt sind, wird die Transformation ohne Informationsverlust fortgesetzt:

-   Die Datei, die zum Erstellen des [**Image-Objekts**](/windows/win32/api/gdiplusheaders/nl-gdiplusheaders-image) verwendet wird, ist eine JPEG-Datei.
-   Breite und Höhe des Bilds sind jeweils ein Vielfaches von 16.

Wenn Breite und Höhe des Bilds nicht beide Vielfache von 16 sind, wird GDI+ alles tun, um die Bildqualität beizubehalten, wenn Sie eine der Drehungs- oder Flippingtransformationen anwenden, die in der vorherigen Liste angezeigt werden.

Initialisieren Sie zum Transformieren eines JPEG-Bilds ein [**EncoderParameters-Objekt,**](/windows/win32/api/gdiplusimaging/nl-gdiplusimaging-encoderparameters) und übergeben Sie die Adresse dieses Objekts an die [Save-Methode](/windows/win32/api/gdiplusheaders/nf-gdiplusheaders-image-save(inistream_inconstclsid_inconstencoderparameters)) der [**Image-Klasse.**](/windows/win32/api/gdiplusheaders/nl-gdiplusheaders-image) Initialisieren Sie das **EncoderParameters-Objekt, sodass** es über ein Array verfügt, das aus einem [**EncoderParameter-Objekt**](/windows/win32/api/gdiplusimaging/nl-gdiplusimaging-encoderparameter) besteht. Initialisieren Sie dieses **EncoderParameter-Objekt** so, dass sein **Value-Member** auf eine **ULONG-Variable** zeigt, die eines der folgenden Elemente der [**EncoderValue-Enumeration**](/windows/win32/api/Gdiplusenums/ne-gdiplusenums-encodervalue) enthält:

-   EncoderValueTransformRotate90,
-   EncoderValueTransformRotate180,
-   EncoderValueTransformRotate270,
-   EncoderValueTransformFlipHorizontal,
-   EncoderValueTransformFlipVertical

Legen Sie den **Guid-Member** des [**EncoderParameter-Objekts**](/windows/win32/api/gdiplusimaging/nl-gdiplusimaging-encoderparameter) auf EncoderTransformation fest.

Die folgende Konsolenanwendung erstellt ein [**Image-Objekt**](/windows/win32/api/gdiplusheaders/nl-gdiplusheaders-image) aus einer JPEG-Datei und speichert das Bild dann in einer neuen Datei. Während des Speichervorgangs wird das Bild um 90 Grad gedreht. Wenn die Breite und Höhe des Bilds jeweils ein Vielfaches von 16 sind, verursacht der Prozess der Drehung und Speicherung des Bilds keinen Informationsverlust.

Die main-Funktion basiert auf der Hilfsfunktion GetEncoderClsid, die unter [Abrufen des Klassenbezeichners für einen Encoder](-gdiplus-retrieving-the-class-identifier-for-an-encoder-use.md)gezeigt wird.


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



 

 
