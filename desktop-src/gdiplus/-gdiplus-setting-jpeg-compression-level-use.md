---
description: Initialisieren Sie zum Angeben des Komprimierungsgrads beim Speichern eines JPEG-Bilds ein EncoderParameters-Objekt, und übergeben Sie die Adresse dieses Objekts an die Save-Methode der Image-Klasse.
ms.assetid: b8365c00-2223-4aff-9fb2-422976af4c31
title: Festlegen der JPEG-Komprimierungsstufe
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6dd72762d27f1e9179b8a1f9bd52ea5b4b7df6cf97a6af658f9e603b87a629e5
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119778630"
---
# <a name="setting-jpeg-compression-level"></a>Festlegen der JPEG-Komprimierungsstufe

Initialisieren Sie zum Angeben des Komprimierungsgrads beim Speichern eines JPEG-Bilds ein [**EncoderParameters-Objekt,**](/windows/win32/api/gdiplusimaging/nl-gdiplusimaging-encoderparameters) und übergeben Sie die Adresse dieses Objekts an die [Save-Methode](/windows/win32/api/gdiplusheaders/nf-gdiplusheaders-image-save(inistream_inconstclsid_inconstencoderparameters)) der [**Image-Klasse.**](/windows/win32/api/gdiplusheaders/nl-gdiplusheaders-image) Initialisieren Sie **das EncoderParameters-Objekt** so, dass es über ein Array verfügt, das aus einem [**EncoderParameter-Objekt**](/windows/win32/api/gdiplusimaging/nl-gdiplusimaging-encoderparameter) besteht. Initialisieren Sie dieses **ein EncoderParameter-Objekt,** sodass dessen **Value-Member** auf einen **ULONG-Wert** von 0 bis 100 zeigt. Legen Sie **den GUID-Member** des **EncoderParameter-Objekts** auf EncoderQuality fest.

Die folgende Konsolenanwendung speichert drei JPEG-Bilder mit jeweils einem anderen Qualitätsgrad. Die Qualitätsstufe 0 steht für die höchste, die Qualitätsstufe 100 für die niedrigste Komprimierung.

Die main-Funktion basiert auf der Hilfsfunktion GetEncoderClsid, die unter Abrufen des Klassenbezeichners für einen [Encoder gezeigt wird:](-gdiplus-retrieving-the-class-identifier-for-an-encoder-use.md)


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



 

 
