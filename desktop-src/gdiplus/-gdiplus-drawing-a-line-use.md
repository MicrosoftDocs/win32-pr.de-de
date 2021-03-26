---
description: In diesem Thema wird veranschaulicht, wie Sie mithilfe von GDI plus eine Linie zeichnen.
ms.assetid: 2e7444f8-94a6-40d6-b243-0764e245eec4
title: Zeichnen einer Linie
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b5284a178baab624633dd427cad84b35933a72fc
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104979048"
---
# <a name="drawing-a-line"></a><span data-ttu-id="4ad0c-103">Zeichnen einer Linie</span><span class="sxs-lookup"><span data-stu-id="4ad0c-103">Drawing a Line</span></span>

<span data-ttu-id="4ad0c-104">In diesem Thema wird veranschaulicht, wie Sie mithilfe von GDI plus eine Linie zeichnen.</span><span class="sxs-lookup"><span data-stu-id="4ad0c-104">This topic demonstrates how to draw a line using GDI Plus.</span></span>

<span data-ttu-id="4ad0c-105">Zum Zeichnen einer Linie in Windows GDI+ benötigen Sie ein [**Grafik**](/windows/win32/api/gdiplusgraphics/nl-gdiplusgraphics-graphics) Objekt, ein [**Pen**](/windows/win32/api/gdipluspen/nl-gdipluspen-pen) -Objekt und ein [**Color**](/windows/win32/api/gdipluscolor/nl-gdipluscolor-color) -Objekt.</span><span class="sxs-lookup"><span data-stu-id="4ad0c-105">To draw a line in Windows GDI+ you need a [**Graphics**](/windows/win32/api/gdiplusgraphics/nl-gdiplusgraphics-graphics) object, a [**Pen**](/windows/win32/api/gdipluspen/nl-gdipluspen-pen) object, and a [**Color**](/windows/win32/api/gdipluscolor/nl-gdipluscolor-color) object.</span></span> <span data-ttu-id="4ad0c-106">Das **Grafik** Objekt stellt die [DrawLine](/windows/win32/api/gdiplusgraphics/nf-gdiplusgraphics-graphics-drawline(inconstpen_inint_inint_inint_inint)) -Methode bereit, und das **Pen** -Objekt enthält Attribute der Zeile, z. b. Farbe und Breite.</span><span class="sxs-lookup"><span data-stu-id="4ad0c-106">The **Graphics** object provides the [DrawLine](/windows/win32/api/gdiplusgraphics/nf-gdiplusgraphics-graphics-drawline(inconstpen_inint_inint_inint_inint)) method, and the **Pen** object holds attributes of the line, such as color and width.</span></span> <span data-ttu-id="4ad0c-107">Die Adresse des **Stift** Objekts wird als Argument an die **DrawLine** -Methode übermittelt.</span><span class="sxs-lookup"><span data-stu-id="4ad0c-107">The address of the **Pen** object is passed as an argument to the **DrawLine** method.</span></span>

<span data-ttu-id="4ad0c-108">Das folgende Programm, das eine Linie von (0,0) bis (200, 100) zeichnet, besteht aus drei Funktionen: **WinMain**, **WndProc** und **OnPaint**.</span><span class="sxs-lookup"><span data-stu-id="4ad0c-108">The following program, which draws a line from (0, 0) to (200, 100), consists of three functions: **WinMain**, **WndProc**, and **OnPaint**.</span></span> <span data-ttu-id="4ad0c-109">Die Funktionen **WinMain** und **WndProc** stellen den grundlegenden Code dar, der für die meisten Windows-Anwendungen gemeinsam ist.</span><span class="sxs-lookup"><span data-stu-id="4ad0c-109">The **WinMain** and **WndProc** functions provide the fundamental code common to most Windows applications.</span></span> <span data-ttu-id="4ad0c-110">Es gibt keinen GDI+-Code in der **WndProc** -Funktion.</span><span class="sxs-lookup"><span data-stu-id="4ad0c-110">There is no GDI+ code in the **WndProc** function.</span></span> <span data-ttu-id="4ad0c-111">Die **WinMain** -Funktion verfügt über eine kleine Menge von GDI+-Code, nämlich die erforderlichen Aufrufe von [**gdipl-Start**](/windows/win32/api/Gdiplusinit/nf-gdiplusinit-gdiplusstartup) und [**gdiplstartshutdown**](/windows/win32/api/Gdiplusinit/nf-gdiplusinit-gdiplusshutdown).</span><span class="sxs-lookup"><span data-stu-id="4ad0c-111">The **WinMain** function has a small amount of GDI+ code, namely the required calls to [**GdiplusStartup**](/windows/win32/api/Gdiplusinit/nf-gdiplusinit-gdiplusstartup) and [**GdiplusShutdown**](/windows/win32/api/Gdiplusinit/nf-gdiplusinit-gdiplusshutdown).</span></span> <span data-ttu-id="4ad0c-112">Der GDI+-Code, der tatsächlich ein [**Grafik**](/windows/win32/api/gdiplusgraphics/nl-gdiplusgraphics-graphics) Objekt erstellt und eine Linie zeichnet, befindet sich in der **OnPaint** -Funktion.</span><span class="sxs-lookup"><span data-stu-id="4ad0c-112">The GDI+ code that actually creates a [**Graphics**](/windows/win32/api/gdiplusgraphics/nl-gdiplusgraphics-graphics) object and draws a line is in the **OnPaint** function.</span></span>

<span data-ttu-id="4ad0c-113">Die **OnPaint** -Funktion empfängt ein Handle für einen Gerätekontext und übergibt dieses Handle an einen [**grafikkonstruktor**](/windows/win32/api/gdiplusgraphics/nl-gdiplusgraphics-graphics) .</span><span class="sxs-lookup"><span data-stu-id="4ad0c-113">The **OnPaint** function receives a handle to a device context and passes that handle to a [**Graphics**](/windows/win32/api/gdiplusgraphics/nl-gdiplusgraphics-graphics) constructor.</span></span> <span data-ttu-id="4ad0c-114">Das an den [**Stift**](/windows/win32/api/gdipluspen/nl-gdipluspen-pen) -Konstruktor übergeben Argument ist ein Verweis auf ein [**Color**](/windows/win32/api/gdipluscolor/nl-gdipluscolor-color) -Objekt.</span><span class="sxs-lookup"><span data-stu-id="4ad0c-114">The argument passed to the [**Pen**](/windows/win32/api/gdipluspen/nl-gdipluspen-pen) constructor is a reference to a [**Color**](/windows/win32/api/gdipluscolor/nl-gdipluscolor-color) object.</span></span> <span data-ttu-id="4ad0c-115">Die vier Zahlen, die an den farbkonstruktor übergeben werden, stellen die Alpha-, rot-, grün-und Blau-Komponenten der Farbe dar.</span><span class="sxs-lookup"><span data-stu-id="4ad0c-115">The four numbers passed to the color constructor represent the alpha, red, green, and blue components of the color.</span></span> <span data-ttu-id="4ad0c-116">Die Alpha Komponente bestimmt die Transparenz der Farbe. 0 ist vollständig transparent, und 255 ist vollständig undurchsichtig.</span><span class="sxs-lookup"><span data-stu-id="4ad0c-116">The alpha component determines the transparency of the color; 0 is fully transparent and 255 is fully opaque.</span></span> <span data-ttu-id="4ad0c-117">Die vier Zahlen, die an die [DrawLine](/windows/win32/api/gdiplusgraphics/nf-gdiplusgraphics-graphics-drawline(inconstpen_inint_inint_inint_inint)) -Methode übermittelt werden, stellen den Anfangspunkt (0,0) und den Endpunkt (200, 100) der Zeile dar.</span><span class="sxs-lookup"><span data-stu-id="4ad0c-117">The four numbers passed to the [DrawLine](/windows/win32/api/gdiplusgraphics/nf-gdiplusgraphics-graphics-drawline(inconstpen_inint_inint_inint_inint)) method represent the starting point (0, 0) and the ending point (200, 100) of the line.</span></span>


```C++
#include <stdafx.h>
#include <windows.h>
#include <objidl.h>
#include <gdiplus.h>
using namespace Gdiplus;
#pragma comment (lib,"Gdiplus.lib")

VOID OnPaint(HDC hdc)
{
   Graphics graphics(hdc);
   Pen      pen(Color(255, 0, 0, 255));
   graphics.DrawLine(&pen, 0, 0, 200, 100);
}

LRESULT CALLBACK WndProc(HWND, UINT, WPARAM, LPARAM);

INT WINAPI WinMain(HINSTANCE hInstance, HINSTANCE, PSTR, INT iCmdShow)
{
   HWND                hWnd;
   MSG                 msg;
   WNDCLASS            wndClass;
   GdiplusStartupInput gdiplusStartupInput;
   ULONG_PTR           gdiplusToken;
   
   // Initialize GDI+.
   GdiplusStartup(&gdiplusToken, &gdiplusStartupInput, NULL);
   
   wndClass.style          = CS_HREDRAW | CS_VREDRAW;
   wndClass.lpfnWndProc    = WndProc;
   wndClass.cbClsExtra     = 0;
   wndClass.cbWndExtra     = 0;
   wndClass.hInstance      = hInstance;
   wndClass.hIcon          = LoadIcon(NULL, IDI_APPLICATION);
   wndClass.hCursor        = LoadCursor(NULL, IDC_ARROW);
   wndClass.hbrBackground  = (HBRUSH)GetStockObject(WHITE_BRUSH);
   wndClass.lpszMenuName   = NULL;
   wndClass.lpszClassName  = TEXT("GettingStarted");
   
   RegisterClass(&wndClass);
   
   hWnd = CreateWindow(
      TEXT("GettingStarted"),   // window class name
      TEXT("Getting Started"),  // window caption
      WS_OVERLAPPEDWINDOW,      // window style
      CW_USEDEFAULT,            // initial x position
      CW_USEDEFAULT,            // initial y position
      CW_USEDEFAULT,            // initial x size
      CW_USEDEFAULT,            // initial y size
      NULL,                     // parent window handle
      NULL,                     // window menu handle
      hInstance,                // program instance handle
      NULL);                    // creation parameters
      
   ShowWindow(hWnd, iCmdShow);
   UpdateWindow(hWnd);
   
   while(GetMessage(&msg, NULL, 0, 0))
   {
      TranslateMessage(&msg);
      DispatchMessage(&msg);
   }
   
   GdiplusShutdown(gdiplusToken);
   return msg.wParam;
}  // WinMain

LRESULT CALLBACK WndProc(HWND hWnd, UINT message, 
   WPARAM wParam, LPARAM lParam)
{
   HDC          hdc;
   PAINTSTRUCT  ps;
   
   switch(message)
   {
   case WM_PAINT:
      hdc = BeginPaint(hWnd, &ps);
      OnPaint(hdc);
      EndPaint(hWnd, &ps);
      return 0;
   case WM_DESTROY:
      PostQuitMessage(0);
      return 0;
   default:
      return DefWindowProc(hWnd, message, wParam, lParam);
   }
} // WndProc
```



<span data-ttu-id="4ad0c-118">Beachten Sie den " [**gdiplstart**](/windows/win32/api/Gdiplusinit/nf-gdiplusinit-gdiplusstartup) "-Befehl in der **WinMain** -Funktion.</span><span class="sxs-lookup"><span data-stu-id="4ad0c-118">Note the call to [**GdiplusStartup**](/windows/win32/api/Gdiplusinit/nf-gdiplusinit-gdiplusstartup) in the **WinMain** function.</span></span> <span data-ttu-id="4ad0c-119">Der erste Parameter der **gdiplfestartup** -Funktion ist die Adresse eines ULONG \_ ptr.</span><span class="sxs-lookup"><span data-stu-id="4ad0c-119">The first parameter of the **GdiplusStartup** function is the address of a ULONG\_PTR.</span></span> <span data-ttu-id="4ad0c-120">**Gdiplstartstartup** füllt diese Variable mit einem Token aus, das später an die Funktion " [**gdipl-Shutdown**](/windows/win32/api/Gdiplusinit/nf-gdiplusinit-gdiplusshutdown) -Funktion" weitergeleitet wird.</span><span class="sxs-lookup"><span data-stu-id="4ad0c-120">**GdiplusStartup** fills that variable with a token that is later passed to the [**GdiplusShutdown**](/windows/win32/api/Gdiplusinit/nf-gdiplusinit-gdiplusshutdown) function.</span></span> <span data-ttu-id="4ad0c-121">Der zweite Parameter der **gdiplfestartup** -Funktion ist die Adresse einer [**gdipl\startupinput**](/windows/win32/api/Gdiplusinit/ns-gdiplusinit-gdiplusstartupinput) -Struktur.</span><span class="sxs-lookup"><span data-stu-id="4ad0c-121">The second parameter of the **GdiplusStartup** function is the address of a [**GdiplusStartupInput**](/windows/win32/api/Gdiplusinit/ns-gdiplusinit-gdiplusstartupinput) structure.</span></span> <span data-ttu-id="4ad0c-122">Der vorangehende Code basiert auf dem standardmäßigen **gdipl\startupinput** -Konstruktor, um die Strukturmember entsprechend festzulegen.</span><span class="sxs-lookup"><span data-stu-id="4ad0c-122">The preceding code relies on the default **GdiplusStartupInput** constructor to set the structure members appropriately.</span></span>

 

 



