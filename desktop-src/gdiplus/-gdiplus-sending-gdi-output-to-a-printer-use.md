---
description: Die Windows GDI+ zeichnen auf einem Drucker ähnelt der Verwendung von GDI+ zum Zeichnen auf einem Computerbildschirm. Um auf einem Drucker zu zeichnen, erhalten Sie ein Gerätekontexthand handle für den Drucker, und übergeben Sie dieses Handle dann an einen Grafikkonstruktor.
ms.assetid: a76cca57-6ed8-44cd-a9f6-f2692d14b68a
title: Senden von GDI+-Ausgabe an einen Drucker
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 51116e27f3ef4e457d2d3cf8d39b26c1a5e2275da4b964bd4de58ec273db1e2b
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119943780"
---
# <a name="sending-gdi-output-to-a-printer"></a>Senden von GDI+-Ausgabe an einen Drucker

Die Windows GDI+ zeichnen auf einem Drucker ähnelt der Verwendung von GDI+ zum Zeichnen auf einem Computerbildschirm. Um auf einem Drucker zu zeichnen, erhalten Sie ein Gerätekontexthand handle für den Drucker, und übergeben Sie dieses Handle dann an einen [**Grafikkonstruktor.**](/windows/win32/api/gdiplusgraphics/nl-gdiplusgraphics-graphics)

Die folgende Konsolenanwendung zeichnet eine Linie, ein Rechteck und eine Ellipse auf einem Drucker namens MyPrinter:


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

   // Get a device context for the printer.
   HDC hdcPrint = CreateDC(NULL, TEXT("\\\\printserver\\print1"), NULL, NULL);

   DOCINFO docInfo;
   ZeroMemory(&docInfo, sizeof(docInfo));
   docInfo.cbSize = sizeof(docInfo);
   docInfo.lpszDocName = "GdiplusPrint";

   StartDoc(hdcPrint, &docInfo);
   StartPage(hdcPrint);
      Graphics* graphics = new Graphics(hdcPrint);
      Pen* pen = new Pen(Color(255, 0, 0, 0));
      graphics->DrawLine(pen, 50, 50, 350, 550);
      graphics->DrawRectangle(pen, 50, 50, 300, 500);
      graphics->DrawEllipse(pen, 50, 50, 300, 500);
      delete pen;
      delete graphics;
   EndPage(hdcPrint);
   EndDoc(hdcPrint);
   
   DeleteDC(hdcPrint);
   GdiplusShutdown(gdiplusToken);
   return 0;
}
```



Im vorangehenden Code befinden sich die drei GDI+ Zeichenbefehle zwischen Aufrufen der [Funktionen StartDoc](/windows/win32/api/wingdi/nf-wingdi-startdocw) und [EndDoc,](/windows/win32/api/wingdi/nf-wingdi-enddoc) von denen jeder das Druckergerätekontexthand handle empfängt. Alle Grafikbefehle zwischen StartDoc und EndDoc werden an eine temporäre Metadatei geroutet. Nach dem Aufruf von EndDoc konvertiert der Druckertreiber die Daten in der Metadatei in das Format, das für den verwendeten Drucker erforderlich ist.

> [!Note]  
> Wenn das Spoolen für den verwendeten Drucker nicht aktiviert ist, wird die Grafikausgabe nicht an eine Metadatei geroutet. Stattdessen werden einzelne Grafikbefehle vom Druckertreiber verarbeitet und dann an den Drucker gesendet.

 

Im Allgemeinen möchten Sie den Namen eines Druckers nicht wie in der vorherigen Konsolenanwendung hart codieren. Eine Alternative zum hart codierenden Namen ist der Aufruf [von GetDefaultPrinter,](../printdocs/getdefaultprinter.md) um den Namen des Standarddruckers zu erhalten. Bevor Sie GetDefaultPrinter aufrufen, müssen Sie einen Puffer zuordnen, der groß genug ist, um den Druckernamen zu speichern. Sie können die Größe des erforderlichen Puffers ermitteln, indem Sie GetDefaultPrinter aufrufen und **NULL** als erstes Argument übergeben.

> [!Note]  
> Die [GetDefaultPrinter-Funktion](../printdocs/getdefaultprinter.md) wird nur für Windows 2000 und höher unterstützt.

 

Die folgende Konsolenanwendung ruft den Namen des Standarddruckers ab und zeichnet dann ein Rechteck und eine Ellipse auf diesem Drucker. Der [**Graphics::D rawRectangle-Aufruf**](/windows/win32/api/gdiplusgraphics/nf-gdiplusgraphics-graphics-drawrectangle(inconstpen_inint_inint_inint_inint)) befindet sich zwischen Aufrufen von [StartPage](/windows/win32/api/wingdi/nf-wingdi-startpage) und [EndPage,](/windows/win32/api/wingdi/nf-wingdi-endpage)sodass sich das Rechteck allein auf einer Seite befindet. Ebenso befindet sich die Ellipse allein auf einer Seite.


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

   DWORD size;
   HDC hdcPrint;

   DOCINFO docInfo;
   ZeroMemory(&docInfo, sizeof(docInfo));
   docInfo.cbSize = sizeof(docInfo);
   docInfo.lpszDocName = "GdiplusPrint";

   // Get the size of the default printer name.
   GetDefaultPrinter(NULL, &size);

   // Allocate a buffer large enough to hold the printer name.
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

      StartDoc(hdcPrint, &docInfo);
         Graphics* graphics;
         Pen* pen = new Pen(Color(255, 0, 0, 0));

         StartPage(hdcPrint);
            graphics = new Graphics(hdcPrint);
            graphics->DrawRectangle(pen, 50, 50, 200, 300);
            delete graphics;
         EndPage(hdcPrint);

         StartPage(hdcPrint);
            graphics = new Graphics(hdcPrint);
            graphics->DrawEllipse(pen, 50, 50, 200, 300);
            delete graphics;
         EndPage(hdcPrint);

         delete pen;
      EndDoc(hdcPrint);

      DeleteDC(hdcPrint);
   }

   delete buffer;

   GdiplusShutdown(gdiplusToken);
   return 0;
}
```



 

 
