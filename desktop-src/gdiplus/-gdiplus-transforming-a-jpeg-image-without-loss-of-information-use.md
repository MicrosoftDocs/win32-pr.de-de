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
# <a name="lossless-transform-of-a-jpeg-image"></a>Verlustfreie Transformation eines JPEG-Bilds

Wenn Sie ein JPEG-Bild komprimieren, gehen einige der Informationen im Bild verloren. Wenn Sie eine JPEG-Datei öffnen, das Bild ändern und es in einer anderen JPEG-Datei speichern, wird die Qualität verringert. Wenn Sie diesen Prozess mehrmals wiederholen, wird eine deutliche Beeinträchtigung der Bildqualität festzustellen.

Da JPEG eines der beliebtesten Bildformate im Internet ist und die Benutzer häufig JPEG-Bilder ändern möchten, bietet GDI+ die folgenden Transformationen, die für JPEG-Bilder ohne Informationsverlust ausgeführt werden können:

-   Drehen von 90 Grad
-   Drehen von 180 Grad
-   Drehen von 270 Grad
-   Horizontal kippen
-   Vertikal kippen

Sie können eine der Transformationen, die in der vorangehenden Liste angezeigt werden, anwenden, wenn Sie die [Save](/windows/win32/api/gdiplusheaders/nf-gdiplusheaders-image-save(inistream_inconstclsid_inconstencoderparameters)) -Methode eines [**Bild**](/windows/win32/api/gdiplusheaders/nl-gdiplusheaders-image) Objekts aufzurufen. Wenn die folgenden Bedingungen erfüllt sind, wird die Transformation ohne Informationsverlust fortgesetzt:

-   Die Datei, die zum Erstellen des [**Image**](/windows/win32/api/gdiplusheaders/nl-gdiplusheaders-image) -Objekts verwendet wird, ist eine JPEG-Datei.
-   Breite und Höhe des Bilds sind jeweils ein Vielfaches von 16.

Wenn die Breite und Höhe des Bilds nicht gleichzeitig ein Vielfaches von 16 ist, wird die Bildqualität von GDI+ am besten beibehalten, wenn Sie eine der Drehung-oder flippingtransformationen anwenden, die in der vorangehenden Liste angezeigt werden.

Zum Transformieren eines JPEG-Bilds initialisieren Sie ein [**EncoderParameters**](/windows/win32/api/gdiplusimaging/nl-gdiplusimaging-encoderparameters) -Objekt, und übergeben Sie die Adresse des Objekts an die [Save](/windows/win32/api/gdiplusheaders/nf-gdiplusheaders-image-save(inistream_inconstclsid_inconstencoderparameters)) -Methode der [**Image**](/windows/win32/api/gdiplusheaders/nl-gdiplusheaders-image) -Klasse. Initialisieren Sie das **EncoderParameters** -Objekt so, dass es über ein Array verfügt, das aus einem [**EncoderParameter**](/windows/win32/api/gdiplusimaging/nl-gdiplusimaging-encoderparameter) -Objekt besteht. Initialisieren Sie dieses einzelne **EncoderParameter** -Objekt, sodass sein **Wertmember** auf eine **ulong** -Variable verweist, die eines der folgenden Elemente der [**EncoderValue**](/windows/win32/api/Gdiplusenums/ne-gdiplusenums-encodervalue) -Enumeration enthält:

-   EncoderValueTransformRotate90,
-   EncoderValueTransformRotate180,
-   EncoderValueTransformRotate270,
-   Encodervaluetransformfliphorizontal,
-   Encodervaluetransformflipvertical

Legen Sie den **GUID** -Member des [**EncoderParameter**](/windows/win32/api/gdiplusimaging/nl-gdiplusimaging-encoderparameter) -Objekts auf encodertransformation fest.

Die folgende Konsolenanwendung erstellt ein [**Image**](/windows/win32/api/gdiplusheaders/nl-gdiplusheaders-image) -Objekt aus einer JPEG-Datei und speichert das Bild dann in einer neuen Datei. Während des Speicher Vorgangs wird das Bild um 90 Grad gedreht. Wenn die Breite und Höhe des Bilds ein Vielfaches von 16 ist, verursacht der Prozess der Rotation und Speicherung des Bilds keinen Verlust von Informationen.

Die Main-Funktion basiert auf der-Hilfsfunktion getencoderclsid, die unter [Abrufen des Klassen Bezeichners für einen Encoder](-gdiplus-retrieving-the-class-identifier-for-an-encoder-use.md)angezeigt wird.


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



 

 
