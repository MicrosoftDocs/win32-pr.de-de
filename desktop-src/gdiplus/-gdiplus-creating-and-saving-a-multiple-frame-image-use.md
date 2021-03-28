---
description: Mit bestimmten Dateiformaten können Sie mehrere Bilder (Frames) in einer einzelnen Datei speichern.
ms.assetid: 9b61e01d-0a98-4ac3-865e-7570ed0c3cde
title: Erstellen und Speichern eines Bilds mit mehreren Frames
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 532a8fc8f8fc7e8742651f3d3853e001d493609b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104131356"
---
# <a name="creating-and-saving-a-multiple-frame-image"></a>Erstellen und Speichern eines Bilds mit mehreren Frames

Mit bestimmten Dateiformaten können Sie mehrere Bilder (Frames) in einer einzelnen Datei speichern. Beispielsweise können Sie mehrere Seiten in einer einzelnen TIFF-Datei speichern. Um die erste Seite zu speichern, nennen Sie die [Save](/windows/win32/api/gdiplusheaders/nf-gdiplusheaders-image-save(inistream_inconstclsid_inconstencoderparameters)) -Methode der [**Image**](/windows/win32/api/gdiplusheaders/nl-gdiplusheaders-image) -Klasse. Um nachfolgende Seiten zu speichern, nennen [Sie die SaveAdd](/windows/win32/api/gdiplusheaders/nf-gdiplusheaders-image-saveadd(inimage_inconstencoderparameters)) -Methode der **Image** -Klasse.

> [!Note]  
> Sie können " [SaveAdd](/windows/win32/api/gdiplusheaders/nf-gdiplusheaders-image-saveadd(inimage_inconstencoderparameters)) " nicht verwenden, um einer animierten GIF-Datei Frames hinzuzufügen.

 

Die folgende Konsolenanwendung erstellt eine TIFF-Datei mit vier Seiten. Die Bilder, die zu den Seiten der TIFF-Datei werden, stammen aus vier Datenträger Dateien: Shapes.bmp, Cereal.gif, Iron.jpg und House.png. Der Code erstellt zunächst vier [**Bild**](/windows/win32/api/gdiplusheaders/nl-gdiplusheaders-image) Objekte: **Multi,** **Page2**, **page3** und **PAGE4**. Zunächst enthält " **Multi"** nur das Bild aus Shapes.bmp, aber schließlich enthält es alle vier Bilder. Wenn die einzelnen Seiten zum Objekt mit **mehreren**  **Bildern** hinzugefügt werden, werden Sie auch der Datenträger Datei Multiframe. TIF hinzugefügt.

Beachten Sie, dass der Code [Speichern](/windows/win32/api/gdiplusheaders/nf-gdiplusheaders-image-save(inistream_inconstclsid_inconstencoderparameters)) (nicht [SaveAdd](/windows/win32/api/gdiplusheaders/nf-gdiplusheaders-image-saveadd(inimage_inconstencoderparameters))) aufruft, um die erste Seite zu speichern. Das erste Argument, das an die Save-Methode übermittelt wird, ist der Name der Datenträger Datei, die schließlich mehrere Frames enthält. Das zweite Argument, das an die Save-Methode übermittelt wird, gibt den Encoder an, der zum Konvertieren der Daten im **multiimage**[](/windows/win32/api/gdiplusheaders/nl-gdiplusheaders-image) -Objekt in das Format (in diesem Fall TIFF) verwendet wird, das für die Datenträger Datei erforderlich ist.   Derselbe Encoder wird automatisch von allen nachfolgenden Aufrufen der SaveAdd-Methode des Objekts mit **mehreren**  **Bildern** verwendet.

Das dritte Argument, das an die [Save](/windows/win32/api/gdiplusheaders/nf-gdiplusheaders-image-save(inistream_inconstclsid_inconstencoderparameters)) -Methode übermittelt wird, ist die Adresse eines [**EncoderParameters**](/windows/win32/api/gdiplusimaging/nl-gdiplusimaging-encoderparameters) -Objekts. Das **EncoderParameters** -Objekt verfügt über ein Array, das ein einzelnes [**EncoderParameter**](/windows/win32/api/gdiplusimaging/nl-gdiplusimaging-encoderparameter) -Objekt enthält. Der **GUID** -Member dieses **EncoderParameter** -Objekts ist auf encodersaveflag festgelegt. Der **Wertmember** des **EncoderParameter** -Objekts verweist auf einen **ulong** -Wert, der den Wert encodervaluemultiframe enthält.

Im Code werden die zweiten, dritten und vierten Seiten gespeichert, indem die [SaveAdd](/windows/win32/api/gdiplusheaders/nf-gdiplusheaders-image-saveadd(inimage_inconstencoderparameters)) -Methode des Objekts mit **mehreren**  [**Bildern**](/windows/win32/api/gdiplusheaders/nl-gdiplusheaders-image) aufgerufen wird. Das erste Argument, das an die SaveAdd-Methode übermittelt wird, ist die Adresse eines **Bild** Objekts. Das Bild in diesem **Bild** Objekt wird dem **multiimage** -Objekt hinzugefügt und außerdem der Multiframe. TIF-Datenträger Datei hinzugefügt.   Das zweite Argument, das an die SaveAdd-Methode übermittelt wird, ist die Adresse desselben [**EncoderParameters**](/windows/win32/api/gdiplusimaging/nl-gdiplusimaging-encoderparameters) -Objekts, das von der [Save](/windows/win32/api/gdiplusheaders/nf-gdiplusheaders-image-save(inistream_inconstclsid_inconstencoderparameters)) -Methode verwendet wurde. Der Unterschied besteht darin, dass der **ulong** , auf den der **Wertemember** zeigt, jetzt den Wert encodervalueframedimensionpage enthält.

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



 

 
