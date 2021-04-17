---
description: Einer der Konstruktoren für die Grafikklasse empfängt ein Gerätekontext Handle und ein Drucker handle.
ms.assetid: 9be67cb2-4bf9-4758-af03-7d92dd04feaf
title: Optimieren der Druckausgabe durch Bereitstellen eines Druckerhandles
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a247af3de037e220432c424c408b4055690ff861
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104977569"
---
# <a name="optimizing-printing-by-providing-a-printer-handle"></a>Optimieren der Druckausgabe durch Bereitstellen eines Druckerhandles

Einer der Konstruktoren für die [**Grafik**](/windows/win32/api/gdiplusgraphics/nl-gdiplusgraphics-graphics) Klasse empfängt ein Gerätekontext Handle und ein Drucker handle. Wenn Sie Windows-GDI+-Befehle an bestimmte PostScript-Drucker senden, ist die Leistung besser, wenn Sie das **Grafik** Objekt mit diesem bestimmten Konstruktor erstellen.

Die folgende Konsolenanwendung ruft [GetDefaultPrinter](../printdocs/getdefaultprinter.md) auf, um den Namen des Standard Druckers abzurufen. Der Code übergibt den Drucker Namen an " [kreatedc](/windows/win32/api/wingdi/nf-wingdi-createdcw) ", um ein Gerätekontext Handle für den Drucker zu erhalten. Der Code übergibt auch den Drucker Namen an [OpenPrinter](../printdocs/openprinter.md) , um ein Drucker Handle zu erhalten. Sowohl das Gerätekontext Handle als auch das Drucker handle werden an den [](/windows/win32/api/gdiplusgraphics/nl-gdiplusgraphics-graphics) -grafikkonstruktor übergeben. Anschließend werden zwei Abbildungen auf dem Drucker gezeichnet.

> [!Note]  
> Die [GetDefaultPrinter](../printdocs/getdefaultprinter.md) -Funktion wird nur unter Windows 2000 und höher unterstützt.

 


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

   DWORD   size;
   HDC     hdcPrint;
   HANDLE  printerHandle;

   DOCINFO docInfo;
   ZeroMemory(&docInfo, sizeof(docInfo));
   docInfo.cbSize = sizeof(docInfo);
   docInfo.lpszDocName = "GdiplusPrint";

   // Get the length of the printer name.
   GetDefaultPrinter(NULL, &size);
   TCHAR* buffer = new TCHAR[size];

   // Get the printer name.
   if(!GetDefaultPrinter(buffer, &size))
   {
      printf("Failure");
   }
   else
   {
      // Get a device context for the printer.
      hdcPrint = CreateDC(NULL, buffer, NULL, NULL);

      // Get a printer handle.
      OpenPrinter(buffer, &printerHandle, NULL);

      StartDoc(hdcPrint, &docInfo);
      StartPage(hdcPrint);
         Graphics* graphics = new Graphics(hdcPrint, printerHandle);
         Pen* pen = new Pen(Color(255, 0, 0, 0));
         graphics->DrawRectangle(pen, 200, 500, 200, 150);
         graphics->DrawEllipse(pen, 200, 500, 200, 150);
         delete(pen);
         delete(graphics);
      EndPage(hdcPrint);
      EndDoc(hdcPrint);

      ClosePrinter(printerHandle);
      DeleteDC(hdcPrint);
   }

   delete buffer;
   
   GdiplusShutdown(gdiplusToken);
   return 0;
}
```



 

 
