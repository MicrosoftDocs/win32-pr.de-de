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
# <a name="drawing-a-line"></a>Zeichnen einer Linie

In diesem Thema wird veranschaulicht, wie Sie mithilfe von GDI plus eine Linie zeichnen.

Zum Zeichnen einer Linie in Windows GDI+ benötigen Sie ein [**Grafik**](/windows/win32/api/gdiplusgraphics/nl-gdiplusgraphics-graphics) Objekt, ein [**Pen**](/windows/win32/api/gdipluspen/nl-gdipluspen-pen) -Objekt und ein [**Color**](/windows/win32/api/gdipluscolor/nl-gdipluscolor-color) -Objekt. Das **Grafik** Objekt stellt die [DrawLine](/windows/win32/api/gdiplusgraphics/nf-gdiplusgraphics-graphics-drawline(inconstpen_inint_inint_inint_inint)) -Methode bereit, und das **Pen** -Objekt enthält Attribute der Zeile, z. b. Farbe und Breite. Die Adresse des **Stift** Objekts wird als Argument an die **DrawLine** -Methode übermittelt.

Das folgende Programm, das eine Linie von (0,0) bis (200, 100) zeichnet, besteht aus drei Funktionen: **WinMain**, **WndProc** und **OnPaint**. Die Funktionen **WinMain** und **WndProc** stellen den grundlegenden Code dar, der für die meisten Windows-Anwendungen gemeinsam ist. Es gibt keinen GDI+-Code in der **WndProc** -Funktion. Die **WinMain** -Funktion verfügt über eine kleine Menge von GDI+-Code, nämlich die erforderlichen Aufrufe von [**gdipl-Start**](/windows/win32/api/Gdiplusinit/nf-gdiplusinit-gdiplusstartup) und [**gdiplstartshutdown**](/windows/win32/api/Gdiplusinit/nf-gdiplusinit-gdiplusshutdown). Der GDI+-Code, der tatsächlich ein [**Grafik**](/windows/win32/api/gdiplusgraphics/nl-gdiplusgraphics-graphics) Objekt erstellt und eine Linie zeichnet, befindet sich in der **OnPaint** -Funktion.

Die **OnPaint** -Funktion empfängt ein Handle für einen Gerätekontext und übergibt dieses Handle an einen [**grafikkonstruktor**](/windows/win32/api/gdiplusgraphics/nl-gdiplusgraphics-graphics) . Das an den [**Stift**](/windows/win32/api/gdipluspen/nl-gdipluspen-pen) -Konstruktor übergeben Argument ist ein Verweis auf ein [**Color**](/windows/win32/api/gdipluscolor/nl-gdipluscolor-color) -Objekt. Die vier Zahlen, die an den farbkonstruktor übergeben werden, stellen die Alpha-, rot-, grün-und Blau-Komponenten der Farbe dar. Die Alpha Komponente bestimmt die Transparenz der Farbe. 0 ist vollständig transparent, und 255 ist vollständig undurchsichtig. Die vier Zahlen, die an die [DrawLine](/windows/win32/api/gdiplusgraphics/nf-gdiplusgraphics-graphics-drawline(inconstpen_inint_inint_inint_inint)) -Methode übermittelt werden, stellen den Anfangspunkt (0,0) und den Endpunkt (200, 100) der Zeile dar.


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



Beachten Sie den " [**gdiplstart**](/windows/win32/api/Gdiplusinit/nf-gdiplusinit-gdiplusstartup) "-Befehl in der **WinMain** -Funktion. Der erste Parameter der **gdiplfestartup** -Funktion ist die Adresse eines ULONG \_ ptr. **Gdiplstartstartup** füllt diese Variable mit einem Token aus, das später an die Funktion " [**gdipl-Shutdown**](/windows/win32/api/Gdiplusinit/nf-gdiplusinit-gdiplusshutdown) -Funktion" weitergeleitet wird. Der zweite Parameter der **gdiplfestartup** -Funktion ist die Adresse einer [**gdipl\startupinput**](/windows/win32/api/Gdiplusinit/ns-gdiplusinit-gdiplusstartupinput) -Struktur. Der vorangehende Code basiert auf dem standardmäßigen **gdipl\startupinput** -Konstruktor, um die Strukturmember entsprechend festzulegen.

 

 



