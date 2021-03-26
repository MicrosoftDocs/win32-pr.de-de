---
description: Die Verwendung von Windows GDI+ zum Zeichnen auf einem Drucker ähnelt der Verwendung von GDI+ zum Zeichnen auf einem Computerbildschirm. Um auf einem Drucker zu zeichnen, rufen Sie ein Gerätekontext Handle für den Drucker ab, und übergeben Sie dieses Handle dann an einen grafikkonstruktor.
ms.assetid: a76cca57-6ed8-44cd-a9f6-f2692d14b68a
title: Senden von GDI+-Ausgabe an einen Drucker
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 96c1c4f6c05e4918663284e6d7747952040dcddf
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104042103"
---
# <a name="sending-gdi-output-to-a-printer"></a><span data-ttu-id="7870e-104">Senden von GDI+-Ausgabe an einen Drucker</span><span class="sxs-lookup"><span data-stu-id="7870e-104">Sending GDI+ Output to a Printer</span></span>

<span data-ttu-id="7870e-105">Die Verwendung von Windows GDI+ zum Zeichnen auf einem Drucker ähnelt der Verwendung von GDI+ zum Zeichnen auf einem Computerbildschirm.</span><span class="sxs-lookup"><span data-stu-id="7870e-105">Using Windows GDI+ to draw on a printer is similar to using GDI+ to draw on a computer screen.</span></span> <span data-ttu-id="7870e-106">Um auf einem Drucker zu zeichnen, rufen Sie ein Gerätekontext Handle für den Drucker ab, und übergeben Sie [](/windows/win32/api/gdiplusgraphics/nl-gdiplusgraphics-graphics) dieses Handle dann an einen grafikkonstruktor.</span><span class="sxs-lookup"><span data-stu-id="7870e-106">To draw on a printer, obtain a device context handle for the printer and then pass that handle to a [**Graphics**](/windows/win32/api/gdiplusgraphics/nl-gdiplusgraphics-graphics) constructor.</span></span>

<span data-ttu-id="7870e-107">Die folgende Konsolenanwendung zeichnet eine Linie, ein Rechteck und eine Ellipse auf einem Drucker mit dem Namen myprinter:</span><span class="sxs-lookup"><span data-stu-id="7870e-107">The following console application draws a line, a rectangle, and an ellipse on a printer named MyPrinter:</span></span>


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



<span data-ttu-id="7870e-108">Im vorangehenden Code befinden sich die drei GDI+-Zeichnungs Befehle zwischen Aufrufen der [StartDoc](/windows/win32/api/wingdi/nf-wingdi-startdocw) -Funktion und der [EndDoc](/windows/win32/api/wingdi/nf-wingdi-enddoc) -Funktion, die jeweils das Drucker Geräte-Kontext Handle erhalten.</span><span class="sxs-lookup"><span data-stu-id="7870e-108">In the preceding code, the three GDI+ drawing commands are in between calls to the [StartDoc](/windows/win32/api/wingdi/nf-wingdi-startdocw) and [EndDoc](/windows/win32/api/wingdi/nf-wingdi-enddoc) functions, each of which receives the printer device context handle.</span></span> <span data-ttu-id="7870e-109">Alle Grafikbefehle zwischen StartDoc und EndDoc werden an eine temporäre Metadatendatei weitergeleitet.</span><span class="sxs-lookup"><span data-stu-id="7870e-109">All graphics commands between StartDoc and EndDoc are routed to a temporary metafile.</span></span> <span data-ttu-id="7870e-110">Nach dem Aufrufe von EndDoc konvertiert der Druckertreiber die Daten in der Metadatei in das Format, das für den verwendeten Drucker benötigt wird.</span><span class="sxs-lookup"><span data-stu-id="7870e-110">After the call to EndDoc, the printer driver converts the data in the metafile into the format required by the specific printer being used.</span></span>

> [!Note]  
> <span data-ttu-id="7870e-111">Wenn für den verwendeten Drucker kein Spoolvorgang aktiviert ist, wird die Grafikausgabe nicht an eine Metadatei weitergeleitet.</span><span class="sxs-lookup"><span data-stu-id="7870e-111">If spooling is not enabled for the printer being used, the graphics output is not routed to a metafile.</span></span> <span data-ttu-id="7870e-112">Stattdessen werden einzelne Grafikbefehle vom Druckertreiber verarbeitet und dann an den Drucker gesendet.</span><span class="sxs-lookup"><span data-stu-id="7870e-112">Instead, individual graphics commands are processed by the printer driver and then sent to the printer.</span></span>

 

<span data-ttu-id="7870e-113">Im Allgemeinen ist es nicht ratsam, den Namen eines Druckers wie in der vorherigen Konsolenanwendung fest zu codieren.</span><span class="sxs-lookup"><span data-stu-id="7870e-113">Generally you won't want to hard-code the name of a printer as was done in the preceding console application.</span></span> <span data-ttu-id="7870e-114">Eine Alternative zum hart codieren des Namens besteht darin, [GetDefaultPrinter](../printdocs/getdefaultprinter.md) aufzurufen, um den Namen des Standard Druckers abzurufen.</span><span class="sxs-lookup"><span data-stu-id="7870e-114">One alternative to hard-coding the name is to call [GetDefaultPrinter](../printdocs/getdefaultprinter.md) to obtain the name of the default printer.</span></span> <span data-ttu-id="7870e-115">Vor dem Aufrufen von GetDefaultPrinter müssen Sie einen Puffer zuordnen, der groß genug ist, um den Drucker Namen zu speichern.</span><span class="sxs-lookup"><span data-stu-id="7870e-115">Before you call GetDefaultPrinter, you must allocate a buffer large enough to hold the printer name.</span></span> <span data-ttu-id="7870e-116">Sie können die Größe des erforderlichen Puffers ermitteln, indem Sie GetDefaultPrinter aufrufen und **null** als erstes Argument übergeben.</span><span class="sxs-lookup"><span data-stu-id="7870e-116">You can determine the size of the required buffer by calling GetDefaultPrinter, passing **NULL** as the first argument.</span></span>

> [!Note]  
> <span data-ttu-id="7870e-117">Die [GetDefaultPrinter](../printdocs/getdefaultprinter.md) -Funktion wird nur unter Windows 2000 und höher unterstützt.</span><span class="sxs-lookup"><span data-stu-id="7870e-117">The [GetDefaultPrinter](../printdocs/getdefaultprinter.md) function is supported only on Windows 2000 and later.</span></span>

 

<span data-ttu-id="7870e-118">Die folgende Konsolenanwendung ruft den Namen des Standard Druckers ab und zeichnet dann ein Rechteck und eine Ellipse auf diesem Drucker.</span><span class="sxs-lookup"><span data-stu-id="7870e-118">The following console application gets the name of the default printer and then draws a rectangle and an ellipse on that printer.</span></span> <span data-ttu-id="7870e-119">Der [**Grafik:D rawrechteck**](/windows/win32/api/gdiplusgraphics/nf-gdiplusgraphics-graphics-drawrectangle(inconstpen_inint_inint_inint_inint)) -Aufruf befindet sich zwischen Aufrufen von [Startpage](/windows/win32/api/wingdi/nf-wingdi-startpage) und [EndPage](/windows/win32/api/wingdi/nf-wingdi-endpage), sodass sich das Rechteck selbst auf einer Seite befindet.</span><span class="sxs-lookup"><span data-stu-id="7870e-119">The [**Graphics::DrawRectangle**](/windows/win32/api/gdiplusgraphics/nf-gdiplusgraphics-graphics-drawrectangle(inconstpen_inint_inint_inint_inint)) call is in between calls to [StartPage](/windows/win32/api/wingdi/nf-wingdi-startpage) and [EndPage](/windows/win32/api/wingdi/nf-wingdi-endpage), so the rectangle is on a page by itself.</span></span> <span data-ttu-id="7870e-120">Ebenso befindet sich die Ellipse auf einer Seite.</span><span class="sxs-lookup"><span data-stu-id="7870e-120">Similarly, the ellipse is on a page by itself.</span></span>


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



 

 
