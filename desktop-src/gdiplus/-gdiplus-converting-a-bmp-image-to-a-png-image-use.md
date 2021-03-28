---
description: Wenn Sie ein Bild in einer Datenträger Datei speichern möchten, müssen Sie die Save-Methode der Image-Klasse aufzurufen.
ms.assetid: a95fa3ea-2013-45d5-bdec-61eddcefc2fa
title: Wandeln eines BMP-Bilds in ein PNG-Bild
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9d165809bb4cfa7f37685b8b130e2b895b35c0ae
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104994294"
---
# <a name="converting-a-bmp-image-to-a-png-image"></a>Wandeln eines BMP-Bilds in ein PNG-Bild

Wenn Sie ein Bild in einer Datenträger Datei speichern möchten, müssen Sie die [Save](/windows/win32/api/gdiplusheaders/nf-gdiplusheaders-image-save(inistream_inconstclsid_inconstencoderparameters)) -Methode der [**Image**](/windows/win32/api/gdiplusheaders/nl-gdiplusheaders-image) -Klasse aufzurufen. Die folgende Konsolenanwendung lädt ein BMP-Bild aus einer Datenträger Datei, konvertiert das Image in das PNG-Format und speichert das konvertierte Bild in einer neuen Datenträger Datei. Die Main-Funktion basiert auf der-Hilfsfunktion getencoderclsid, die unter [Abrufen des Klassen Bezeichners für einen Encoder](-gdiplus-retrieving-the-class-identifier-for-an-encoder-use.md)angezeigt wird.


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

   CLSID   encoderClsid;
   Status  stat;
   Image*   image = new Image(L"Bird.bmp");

   // Get the CLSID of the PNG encoder.
   GetEncoderClsid(L"image/png", &encoderClsid);

   stat = image->Save(L"Bird.png", &encoderClsid, NULL);

   if(stat == Ok)
      printf("Bird.png was saved successfully\n");
   else
      printf("Failure: stat = %d\n", stat); 

   delete image;
   GdiplusShutdown(gdiplusToken);
   return 0;
}
```



 

 



