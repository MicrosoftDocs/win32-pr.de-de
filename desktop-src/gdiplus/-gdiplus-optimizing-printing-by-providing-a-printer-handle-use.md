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
# <a name="optimizing-printing-by-providing-a-printer-handle"></a><span data-ttu-id="c5d5d-103">Optimieren der Druckausgabe durch Bereitstellen eines Druckerhandles</span><span class="sxs-lookup"><span data-stu-id="c5d5d-103">Optimizing Printing by Providing a Printer Handle</span></span>

<span data-ttu-id="c5d5d-104">Einer der Konstruktoren für die [**Grafik**](/windows/win32/api/gdiplusgraphics/nl-gdiplusgraphics-graphics) Klasse empfängt ein Gerätekontext Handle und ein Drucker handle.</span><span class="sxs-lookup"><span data-stu-id="c5d5d-104">One of the constructors for the [**Graphics**](/windows/win32/api/gdiplusgraphics/nl-gdiplusgraphics-graphics) class receives a device context handle and a printer handle.</span></span> <span data-ttu-id="c5d5d-105">Wenn Sie Windows-GDI+-Befehle an bestimmte PostScript-Drucker senden, ist die Leistung besser, wenn Sie das **Grafik** Objekt mit diesem bestimmten Konstruktor erstellen.</span><span class="sxs-lookup"><span data-stu-id="c5d5d-105">When you send Windows GDI+ commands to certain PostScript printers, the performance will be better if you create your **Graphics** object with that particular constructor.</span></span>

<span data-ttu-id="c5d5d-106">Die folgende Konsolenanwendung ruft [GetDefaultPrinter](../printdocs/getdefaultprinter.md) auf, um den Namen des Standard Druckers abzurufen.</span><span class="sxs-lookup"><span data-stu-id="c5d5d-106">The following console application calls [GetDefaultPrinter](../printdocs/getdefaultprinter.md) to get the name of the default printer.</span></span> <span data-ttu-id="c5d5d-107">Der Code übergibt den Drucker Namen an " [kreatedc](/windows/win32/api/wingdi/nf-wingdi-createdcw) ", um ein Gerätekontext Handle für den Drucker zu erhalten.</span><span class="sxs-lookup"><span data-stu-id="c5d5d-107">The code passes the printer name to [CreateDC](/windows/win32/api/wingdi/nf-wingdi-createdcw) to obtain a device context handle for the printer.</span></span> <span data-ttu-id="c5d5d-108">Der Code übergibt auch den Drucker Namen an [OpenPrinter](../printdocs/openprinter.md) , um ein Drucker Handle zu erhalten.</span><span class="sxs-lookup"><span data-stu-id="c5d5d-108">The code also passes the printer name to [OpenPrinter](../printdocs/openprinter.md) to obtain a printer handle.</span></span> <span data-ttu-id="c5d5d-109">Sowohl das Gerätekontext Handle als auch das Drucker handle werden an den [](/windows/win32/api/gdiplusgraphics/nl-gdiplusgraphics-graphics) -grafikkonstruktor übergeben.</span><span class="sxs-lookup"><span data-stu-id="c5d5d-109">Both the device context handle and the printer handle are passed to the [**Graphics**](/windows/win32/api/gdiplusgraphics/nl-gdiplusgraphics-graphics) constructor.</span></span> <span data-ttu-id="c5d5d-110">Anschließend werden zwei Abbildungen auf dem Drucker gezeichnet.</span><span class="sxs-lookup"><span data-stu-id="c5d5d-110">Then two figures are drawn on the printer.</span></span>

> [!Note]  
> <span data-ttu-id="c5d5d-111">Die [GetDefaultPrinter](../printdocs/getdefaultprinter.md) -Funktion wird nur unter Windows 2000 und höher unterstützt.</span><span class="sxs-lookup"><span data-stu-id="c5d5d-111">The [GetDefaultPrinter](../printdocs/getdefaultprinter.md) function is supported only on Windows 2000 and later.</span></span>

 


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



 

 
