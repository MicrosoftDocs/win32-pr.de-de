---
description: In diesem Thema wird veranschaulicht, wie Sie eine Linie mit GDI Plus zeichnen.
ms.assetid: 2e7444f8-94a6-40d6-b243-0764e245eec4
title: Zeichnen einer Linie
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7a1e2a330f24cd0d1771458d02b264cdaa493835477b40c95d05ca4bf71c8a1e
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119036808"
---
# <a name="drawing-a-line"></a>Zeichnen einer Linie

In diesem Thema wird veranschaulicht, wie Sie eine Linie mit GDI Plus zeichnen.

Um eine Linie in einem Windows GDI+ [](/windows/win32/api/gdiplusgraphics/nl-gdiplusgraphics-graphics) benötigen Sie ein Graphics-Objekt, ein [**Pen-Objekt**](/windows/win32/api/gdipluspen/nl-gdipluspen-pen) und ein [**Color-Objekt.**](/windows/win32/api/gdipluscolor/nl-gdipluscolor-color) Das **Graphics-Objekt** stellt die [DrawLine-Methode](/windows/win32/api/gdiplusgraphics/nf-gdiplusgraphics-graphics-drawline(inconstpen_inint_inint_inint_inint)) zur, und das **Pen-Objekt** enthält Attribute der Linie, z. B. Farbe und Breite. Die Adresse des **Pen-Objekts** wird als Argument an die **DrawLine-Methode** übergeben.

Das folgende Programm, das eine Linie von (0, 0) bis (200, 100) zeichnet, besteht aus drei Funktionen: **WinMain,** **WndProc** und **OnPaint**. Die **Funktionen WinMain** und **WndProc** stellen den grundlegenden Code zur Verfügung, der für die meisten Windows ist. Es gibt keinen GDI+ code in der **WndProc-Funktion.** Die **WinMain-Funktion** verfügt über eine kleine Menge GDI+ Code, nämlich die erforderlichen Aufrufe von [**GdiplusStartup**](/windows/win32/api/Gdiplusinit/nf-gdiplusinit-gdiplusstartup) und [**GdiplusShutdown.**](/windows/win32/api/Gdiplusinit/nf-gdiplusinit-gdiplusshutdown) Der GDI+ Code, der tatsächlich ein [**Graphics-Objekt**](/windows/win32/api/gdiplusgraphics/nl-gdiplusgraphics-graphics) erstellt und eine Linie zeichnet, befindet sich in der **OnPaint-Funktion.**

Die **OnPaint-Funktion** empfängt ein Handle für einen Gerätekontext und übergibt dieses Handle an einen [**Grafikkonstruktor.**](/windows/win32/api/gdiplusgraphics/nl-gdiplusgraphics-graphics) Das an den [**Stiftkonstruktor übergebene**](/windows/win32/api/gdipluspen/nl-gdipluspen-pen) Argument ist ein Verweis auf ein [**Color-Objekt.**](/windows/win32/api/gdipluscolor/nl-gdipluscolor-color) Die vier Zahlen, die an den Farbkonstruktor übergeben werden, stellen die Alpha-, Rot-, Grün- und Blaukomponenten der Farbe dar. Die Alphakomponente bestimmt die Transparenz der Farbe. 0 ist vollständig transparent, und 255 ist vollständig deckend. Die vier Zahlen, die an die [DrawLine-Methode](/windows/win32/api/gdiplusgraphics/nf-gdiplusgraphics-graphics-drawline(inconstpen_inint_inint_inint_inint)) übergeben werden, stellen den Anfangspunkt (0, 0) und den Endpunkt (200, 100) der Linie dar.


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



Beachten Sie den Aufruf von [**GdiplusStartup**](/windows/win32/api/Gdiplusinit/nf-gdiplusinit-gdiplusstartup) in der **WinMain-Funktion.** Der erste Parameter der **GdiplusStartup-Funktion** ist die Adresse eines ULONG \_ PTR. **GdiplusStartup** füllt diese Variable mit einem Token auf, das später an die [**GdiplusShutdown-Funktion übergeben**](/windows/win32/api/Gdiplusinit/nf-gdiplusinit-gdiplusshutdown) wird. Der zweite Parameter der **GdiplusStartup-Funktion** ist die Adresse einer [**GdiplusStartupInput-Struktur.**](/windows/win32/api/Gdiplusinit/ns-gdiplusinit-gdiplusstartupinput) Der vorangehende Code basiert auf dem **GdiplusStartupInput-Standardkonstruktor,** um die Strukturmitglieder entsprechend festlegen zu können.

 

 



