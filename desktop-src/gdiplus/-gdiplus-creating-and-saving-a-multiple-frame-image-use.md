---
description: Mit bestimmten Dateiformaten können Sie mehrere Bilder (Frames) in einer einzelnen Datei speichern.
ms.assetid: 9b61e01d-0a98-4ac3-865e-7570ed0c3cde
title: Erstellen und Speichern eines Bilds mit mehreren Frames
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ecd99bc2d5f21c143b66ccc201f9a96a93f3437516a6fd1cdd03e521a00ceb59
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "120115120"
---
# <a name="creating-and-saving-a-multiple-frame-image"></a>Erstellen und Speichern eines Bilds mit mehreren Frames

Mit bestimmten Dateiformaten können Sie mehrere Bilder (Frames) in einer einzelnen Datei speichern. Beispielsweise können Sie mehrere Seiten in einer einzigen TIFF-Datei speichern. Um die erste Seite zu speichern, rufen Sie die [Save-Methode](/windows/win32/api/gdiplusheaders/nf-gdiplusheaders-image-save(inistream_inconstclsid_inconstencoderparameters)) der [**Image-Klasse**](/windows/win32/api/gdiplusheaders/nl-gdiplusheaders-image) auf. Um nachfolgende Seiten zu speichern, rufen Sie die [SaveAdd-Methode](/windows/win32/api/gdiplusheaders/nf-gdiplusheaders-image-saveadd(inimage_inconstencoderparameters)) der **Image-Klasse** auf.

> [!Note]  
> Sie können [SaveAdd](/windows/win32/api/gdiplusheaders/nf-gdiplusheaders-image-saveadd(inimage_inconstencoderparameters)) nicht verwenden, um Einer animierten GIF-Datei Frames hinzuzufügen.

 

Die folgende Konsolenanwendung erstellt eine TIFF-Datei mit vier Seiten. Die Images, die zu den Seiten der TIFF-Datei werden, stammen aus vier Datenträgerdateien: Shapes.bmp, Cereal.gif, Iron.jpg und House.png. Der Code erstellt zunächst vier [**Bildobjekte:**](/windows/win32/api/gdiplusheaders/nl-gdiplusheaders-image) **mehrere**, **page2,** **page3** und **page4**. Zunächst enthält **multi** nur das Bild aus Shapes.bmp, aber schließlich alle vier Bilder. Wenn die einzelnen Seiten dem **Objekt mit mehreren**  **Images** hinzugefügt werden, werden sie auch der Datenträgerdatei Multiframe.tif hinzugefügt.

Beachten Sie, dass der Code [Save](/windows/win32/api/gdiplusheaders/nf-gdiplusheaders-image-save(inistream_inconstclsid_inconstencoderparameters)) (nicht [SaveAdd ) aufruft,](/windows/win32/api/gdiplusheaders/nf-gdiplusheaders-image-saveadd(inimage_inconstencoderparameters))um die erste Seite zu speichern. Das erste Argument, das an die Save-Methode übergeben wird, ist der Name der Datenträgerdatei, die schließlich mehrere Frames enthält. Das zweite Argument, das an die Save-Methode übergeben wird, gibt den Encoder an, der verwendet wird, um die Daten im **Multi-Image-Objekt**[](/windows/win32/api/gdiplusheaders/nl-gdiplusheaders-image) in das Format (in diesem Fall TIFF) zu konvertieren, das für die Datenträgerdatei erforderlich ist.   Der gleiche Encoder wird automatisch von allen nachfolgenden Aufrufen der SaveAdd-Methode des **Mehrfachbildobjekts** verwendet.  

Das dritte Argument, das an die [Save-Methode](/windows/win32/api/gdiplusheaders/nf-gdiplusheaders-image-save(inistream_inconstclsid_inconstencoderparameters)) übergeben wird, ist die Adresse eines [**EncoderParameters-Objekts.**](/windows/win32/api/gdiplusimaging/nl-gdiplusimaging-encoderparameters) Das **EncoderParameters-Objekt** verfügt über ein Array, das ein einzelnes [**EncoderParameter-Objekt**](/windows/win32/api/gdiplusimaging/nl-gdiplusimaging-encoderparameter) enthält. Der **Guid-Member** dieses **EncoderParameter-Objekts** ist auf EncoderSaveFlag festgelegt. Der **Value-Member** des **EncoderParameter-Objekts** zeigt auf eine **ULONG,** die den Wert EncoderValueMultiFrame enthält.

Der Code speichert die zweite, dritte und vierte Seite, indem die [SaveAdd-Methode](/windows/win32/api/gdiplusheaders/nf-gdiplusheaders-image-saveadd(inimage_inconstencoderparameters)) des [**Multi-Image-Objekts**](/windows/win32/api/gdiplusheaders/nl-gdiplusheaders-image) aufgerufen wird.    Das erste Argument, das an die SaveAdd-Methode übergeben wird, ist die Adresse eines **Image-Objekts.** Das Bild in diesem **Image-Objekt** wird dem **Mehrfachbildobjekt** und auch der Multiframe.tif-Datenträgerdatei hinzugefügt.    Das zweite Argument, das an die SaveAdd-Methode übergeben wird, ist die Adresse desselben [**EncoderParameters-Objekts,**](/windows/win32/api/gdiplusimaging/nl-gdiplusimaging-encoderparameters) das von der [Save-Methode](/windows/win32/api/gdiplusheaders/nf-gdiplusheaders-image-save(inistream_inconstclsid_inconstencoderparameters)) verwendet wurde. Der Unterschied besteht darin, dass die **ULONG,** auf die der **Value-Member** zeigt, jetzt den Wert EncoderValueFrameDimensionPage enthält.

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



 

 
