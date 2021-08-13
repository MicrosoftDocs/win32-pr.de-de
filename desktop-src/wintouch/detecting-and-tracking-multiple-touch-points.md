---
title: Erkennen und Nachverfolgen mehrerer Berührungspunkte
description: Erkennen und Nachverfolgen mehrerer Berührungspunkte
ms.assetid: 7a5c7595-f341-4e11-805f-ed0b9c63cbff
keywords:
- Windows Toucheingabe, mehrere Berührungspunkte
- Erkennen mehrerer Berührungspunkte
- Nachverfolgen mehrerer Berührungspunkte
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a4a5b8086988dc1a87b5596d5a0ac74ec1f1df5ce4b85d928cbe306b791d17b0
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118436065"
---
# <a name="detecting-and-tracking-multiple-touch-points"></a>Erkennen und Nachverfolgen mehrerer Berührungspunkte

In den folgenden Schritten wird erläutert, wie Sie mehrere Berührungspunkte mit Windows Touch nachverfolgen.

1.  Erstellen Sie eine Anwendung, und aktivieren Sie Windows Touch.
2.  Fügen Sie einen Handler für [**WM \_ TOUCH**](wm-touchdown.md) und Verfolgungspunkte hinzu.
3.  Zeichnen Sie die Punkte.

Sobald Ihre Anwendung ausgeführt wird, werden bei jeder Berührung Kreise gerendert. Der folgende Screenshot zeigt, wie Ihre Anwendung während der Ausführung aussehen kann.

![Screenshot einer Anwendung, die Berührungspunkte als grüne und gelbe Kreise rendert](images/multitouchpoints.png)

## <a name="create-an-application-and-enable-windows-touch"></a>Erstellen einer Anwendung und Aktivieren von Windows Touch

Beginnen Sie mit einer Microsoft Win32-Anwendung mithilfe des Assistenten für Microsoft Visual Studio. Nachdem Sie den Assistenten abgeschlossen haben, fügen Sie Unterstützung für Windows Touch-Nachrichten hinzu, indem Sie die Windows-Version in targetver.h festlegen und windows.h und windowsx.h in Ihre Anwendung einschließen. Der folgende Code zeigt, wie Sie die Windows Version in targetver.h festlegen.


```C++
#ifndef WINVER                  // Specifies that the minimum required platform is Windows 7.
#define WINVER 0x0601           // Change this to the appropriate value to target other versions of Windows.
#endif

#ifndef _WIN32_WINNT            // Specifies that the minimum required platform is Windows 7.
#define _WIN32_WINNT 0x0601     // Change this to the appropriate value to target other versions of Windows.
#endif     

#ifndef _WIN32_WINDOWS          // Specifies that the minimum required platform is Windows 98.
#define _WIN32_WINDOWS 0x0410 // Change this to the appropriate value to target Windows Me or later.
#endif

#ifndef _WIN32_IE                       // Specifies that the minimum required platform is Internet Explorer 7.0.
#define _WIN32_IE 0x0700        // Change this to the appropriate value to target other versions of IE.
#endif
```



Der folgende Code zeigt, wie Die include-Anweisungen hinzugefügt werden sollen. Außerdem können Sie einige globale Variablen erstellen, die später verwendet werden.


```C++
#include <windows.h>    // included for Windows Touch
#include <windowsx.h>   // included for point conversion

#define MAXPOINTS 10

// You will use this array to track touch points
int points[MAXPOINTS][2];

// You will use this array to switch the color / track ids
int idLookup[MAXPOINTS];


// You can make the touch points larger
// by changing this radius value
static int radius      = 50;

// There should be at least as many colors
// as there can be touch points so that you
// can have different colors for each point
COLORREF colors[] = { RGB(153,255,51), 
                      RGB(153,0,0), 
                      RGB(0,153,0), 
                      RGB(255,255,0), 
                      RGB(255,51,204), 
                      RGB(0,0,0),
                      RGB(0,153,0), 
                      RGB(153, 255, 255), 
                      RGB(153,153,255), 
                      RGB(0,51,153)
                    };

```



## <a name="add-handler-for-wm_touch-and-track-points"></a>Hinzufügen eines Handlers für WM \_ TOUCH und Track Points

Deklarieren Sie zunächst einige Variablen, die vom [**WM \_ TOUCH-Handler**](wm-touchdown.md) in [**WndProc**](/previous-versions/windows/desktop/legacy/ms633573(v=vs.85))verwendet werden.


```C++
int wmId, wmEvent, i, x, y;

UINT cInputs;
PTOUCHINPUT pInputs;
POINT ptInput;   
```



Initialisieren Sie nun die Variablen, die zum Speichern von Berührungspunkten verwendet werden, und registrieren Sie das Fenster für die Toucheingabe über die **InitInstance-Methode.**


```C++
BOOL InitInstance(HINSTANCE hInstance, int nCmdShow)
{
   HWND hWnd;

   hInst = hInstance; // Store instance handle in our global variable

   hWnd = CreateWindow(szWindowClass, szTitle, WS_OVERLAPPEDWINDOW,
      CW_USEDEFAULT, 0, CW_USEDEFAULT, 0, NULL, NULL, hInstance, NULL);

   if (!hWnd) {
      return FALSE;
   }

   // register the window for touch instead of gestures
   RegisterTouchWindow(hWnd, 0);  

   // the following code initializes the points
   for (int i=0; i< MAXPOINTS; i++){
     points[i][0] = -1;
     points[i][1] = -1;
     idLookup[i]  = -1;
   }  

   ShowWindow(hWnd, nCmdShow);
   UpdateWindow(hWnd);

   return TRUE;
}
```



Behandeln Sie als Nächstes die [**WM \_ TOUCH-Nachricht**](wm-touchdown.md) der [**WndProc-Methode.**](/previous-versions/windows/desktop/legacy/ms633573(v=vs.85)) Der folgende Code zeigt eine Implementierung des Handlers für **WM \_ TOUCH**.


```C++
case WM_TOUCH:        
  cInputs = LOWORD(wParam);
  pInputs = new TOUCHINPUT[cInputs];
  if (pInputs){
    if (GetTouchInputInfo((HTOUCHINPUT)lParam, cInputs, pInputs, sizeof(TOUCHINPUT))){
      for (int i=0; i < static_cast<INT>(cInputs); i++){
        TOUCHINPUT ti = pInputs[i];
        index = GetContactIndex(ti.dwID);
        if (ti.dwID != 0 && index < MAXPOINTS){                            
          // Do something with your touch input handle
          ptInput.x = TOUCH_COORD_TO_PIXEL(ti.x);
          ptInput.y = TOUCH_COORD_TO_PIXEL(ti.y);
          ScreenToClient(hWnd, &ptInput);
          
          if (ti.dwFlags & TOUCHEVENTF_UP){                      
            points[index][0] = -1;
            points[index][1] = -1;                
          }else{
            points[index][0] = ptInput.x;
            points[index][1] = ptInput.y;                
          }
        }
      }
    }
    // If you handled the message and don't want anything else done with it, you can close it
    CloseTouchInputHandle((HTOUCHINPUT)lParam);
    delete [] pInputs;
  }else{
    // Handle the error here 
  }  
```



> [!Note]  
> Um die [**ScreenToClient-Funktion**](/windows/desktop/api/winuser/nf-winuser-screentoclient) verwenden zu können, benötigen Sie eine hohe DPI-Unterstützung in Ihrer Anwendung. Weitere Informationen zur Unterstützung hoher DPI-Daten finden Sie im MSDN-Abschnitt [High DPI (Hohe DPI-Anzahl).]( ../hidpi/high-dpi-desktop-application-development-on-windows.md)

 

Wenn ein Benutzer nun den Bildschirm berührt, werden die Positionen, die er berührt, im Punktarray gespeichert. Der **dwID-Member** der [**TOUCHINPUT-Struktur**](/windows/win32/api/winuser/ns-winuser-touchinput) speichert einen Bezeichner, der hardwareabhängig sein wird.

Um das Problem zu beheben, dass der dwID-Member von der Hardware abhängig ist, verwendet der [**WM \_ TOUCH-Fallhandler**](wm-touchdown.md) die Funktion **GetContactIndex,** die den **dwID-Member** der [**TOUCHINPUT-Struktur**](/windows/win32/api/winuser/ns-winuser-touchinput) einem Punkt zuweist, der auf dem Bildschirm gezeichnet wird. Der folgende Code zeigt eine Implementierung dieser Funktion.


```C++
// This function is used to return an index given an ID
int GetContactIndex(int dwID){
  for (int i=0; i < MAXPOINTS; i++){
    if (idLookup[i] == -1){
      idLookup[i] = dwID;
      return i;
    }else{
      if (idLookup[i] == dwID){
        return i;
      }
    }
  }
  // Out of contacts
  return -1;
}
```



## <a name="draw-the-points"></a>Zeichnen der Punkte

Deklarieren Sie die folgenden Variablen für die Zeichnungsroutine.


```C++
    // For double buffering
    static HDC memDC       = 0;
    static HBITMAP hMemBmp = 0;
    HBITMAP hOldBmp        = 0;
   
    // For drawing / fills
    PAINTSTRUCT ps;
    HDC hdc;
    
    // For tracking dwId to points
    int index;
```



Der Arbeitsspeicheranzeigekontext *memDC* wird zum Speichern eines temporären Grafikkontexts verwendet, der mit dem gerenderten Anzeigekontext *hdc* ausgetauscht wird, um Flackern zu vermeiden. Implementieren Sie die Zeichnungsroutine, die die gespeicherten Punkte annimmt und einen Kreis an den Punkten zeichnet. Der folgende Code zeigt, wie Sie den [**WM \_ PAINT-Handler**](/windows/desktop/gdi/wm-paint) implementieren können.


```C++
  case WM_PAINT:
    hdc = BeginPaint(hWnd, &ps);    
    RECT client;
    GetClientRect(hWnd, &client);        
  
    // start double buffering
    if (!memDC){
      memDC = CreateCompatibleDC(hdc);
    }
    hMemBmp = CreateCompatibleBitmap(hdc, client.right, client.bottom);
    hOldBmp = (HBITMAP)SelectObject(memDC, hMemBmp);          
  
    FillRect(memDC, &client, CreateSolidBrush(RGB(255,255,255)));
     
    //Draw Touched Points                
    for (i=0; i < MAXPOINTS; i++){        
      SelectObject( memDC, CreateSolidBrush(colors[i]));           
      x = points[i][0];
      y = points[i][1];
      if  (x >0 && y>0){              
        Ellipse(memDC, x - radius, y - radius, x+ radius, y + radius);
      }
    }
  
    BitBlt(hdc, 0,0, client.right, client.bottom, memDC, 0,0, SRCCOPY);      

    EndPaint(hWnd, &ps);
    break;
```



Wenn Sie Ihre Anwendung ausführen, sollte sie nun in etwa wie die Abbildung am Anfang dieses Abschnitts aussehen.

Zum Spaß können Sie einige zusätzliche Linien um die Berührungspunkte zeichnen. Der folgende Screenshot zeigt, wie die Anwendung mit einigen zusätzlichen Linien aussehen kann, die um die Kreise gezeichnet werden.

![Screenshot einer Anwendung, die Berührungspunkte als Kreise mit Linien durch die Mittelpunkte rendert und die Kanten der Berührungspunkte überschneidet](images/multitouchpointsfun.png)

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Windows Toucheingabe](guide-multi-touch-input.md)
</dt> </dl>

 

 