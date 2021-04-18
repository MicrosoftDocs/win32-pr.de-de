---
title: Erkennen und Nachverfolgen mehrerer Berührungspunkte
description: Erkennen und Nachverfolgen mehrerer Berührungspunkte
ms.assetid: 7a5c7595-f341-4e11-805f-ed0b9c63cbff
keywords:
- Windows-Fingereingabe, mehrere Berührungspunkte
- Erkennen mehrerer Berührungspunkte
- Nachverfolgen mehrerer Berührungspunkte
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 13b9eaf665b850eea8925bd531ffd1e9ec3fcf40
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "104473780"
---
# <a name="detecting-and-tracking-multiple-touch-points"></a>Erkennen und Nachverfolgen mehrerer Berührungspunkte

In den folgenden Schritten wird erläutert, wie Sie mithilfe von Windows-Finger Eingaben mehrere Berührungspunkte verfolgen.

1.  Erstellen Sie eine Anwendung, und aktivieren Sie Windows-Interaktion.
2.  Fügen Sie einen Handler für [**WM- \_ Berührungs**](wm-touchdown.md) -und Verfolgungs Punkte hinzu.
3.  Zeichnen Sie die Punkte.

Nachdem Sie die Anwendung ausgeführt haben, werden die Kreise unter den einzelnen Finger Eingaben angezeigt. Der folgende Screenshot zeigt, wie Ihre Anwendung während der Ausführung aussehen könnte.

![Screenshot mit einer Anwendung, die Berührungspunkte als grüne und gelbe Kreise rendert](images/multitouchpoints.png)

## <a name="create-an-application-and-enable-windows-touch"></a>Erstellen einer Anwendung und Aktivieren von Windows-Finger Eingaben

Beginnen Sie mit einer Microsoft Win32-Anwendung mithilfe des Assistenten für Microsoft Visual Studio. Nachdem Sie den Assistenten abgeschlossen haben, fügen Sie Unterstützung für Windows-Finger Eingabenachrichten hinzu, indem Sie die Windows-Version in "targetver. h" festlegen und in Ihrer Anwendung Windows. h und WINDOWSX. h einschließen. Der folgende Code zeigt, wie Sie die Windows-Version in "targetver. h" festlegen.


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



Der folgende Code zeigt, wie die include-Direktiven hinzugefügt werden sollen. Außerdem können Sie einige globale Variablen erstellen, die später verwendet werden.


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



## <a name="add-handler-for-wm_touch-and-track-points"></a>Handler für WM \_ -Berührungs-und Verfolgungs Punkte hinzufügen

Deklarieren Sie zunächst einige Variablen, die vom [**WM- \_**](wm-touchdown.md) Fingerabdruck Handler in [**WndProc**](/previous-versions/windows/desktop/legacy/ms633573(v=vs.85))verwendet werden.


```C++
int wmId, wmEvent, i, x, y;

UINT cInputs;
PTOUCHINPUT pInputs;
POINT ptInput;   
```



Initialisieren Sie nun die Variablen, die zum Speichern von Berührungspunkten verwendet werden, und registrieren Sie das Fenster für die Berührungs Eingabe von der **InitInstance** -Methode.


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



Behandeln Sie als nächstes [**die \_ WM**](wm-touchdown.md) -Fingereingabe Nachricht von der [**WndProc**](/previous-versions/windows/desktop/legacy/ms633573(v=vs.85)) -Methode. Der folgende Code zeigt eine Implementierung des-Handlers **für \_ WM**-Finger Eingaben.


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
> Um die [**ScreenToClient**](/windows/desktop/api/winuser/nf-winuser-screentoclient) -Funktion verwenden zu können, müssen Sie in Ihrer Anwendung über eine hohe dpi-Unterstützung verfügen. Weitere Informationen zur Unterstützung von High dpi finden Sie im Abschnitt " [High dpi]( ../hidpi/high-dpi-desktop-application-development-on-windows.md) " in MSDN.

 

Wenn ein Benutzer nun den Bildschirm berührt, werden die Positionen, die er berührt, im points-Array gespeichert. Der **dwID-** Member der [**TOUCHINPUT**](/windows/win32/api/winuser/ns-winuser-touchinput) -Struktur speichert einen Bezeichner, der Hardware abhängig ist.

Um das Problem zu beheben, dass der dwID-Member von der Hardware abhängig ist, verwendet der [**WM- \_ touchfallhandler**](wm-touchdown.md) eine Funktion, **getcontactindex**, die den **dwID-** Member der [**TOUCHINPUT**](/windows/win32/api/winuser/ns-winuser-touchinput) -Struktur einem Punkt zuordnet, der auf dem Bildschirm gezeichnet wird. Der folgende Code zeigt eine Implementierung dieser Funktion.


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

Deklarieren Sie die folgenden Variablen für die Zeichnungs Routine.


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



Der Kontext-Anzeige Kontext *memdc* dient zum Speichern eines temporären Grafik Kontexts, der mit dem gerenderten Anzeige Kontext ( *hdc*) ausgetauscht wird, um das Flimmern auszuschließen. Implementieren Sie die Zeichnungs Routine, die die von Ihnen gespeicherten Punkte annimmt und einen Kreis an den Punkten zeichnet. Der folgende Code zeigt, wie Sie den [**WM- \_ Paint**](/windows/desktop/gdi/wm-paint) -Handler implementieren können.


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



Wenn Sie die Anwendung ausführen, sollte Sie nun in etwa wie in der Abbildung am Anfang dieses Abschnitts aussehen.

Um Spaß zu machen, können Sie einige zusätzliche Zeilen um die Berührungspunkte zeichnen. Der folgende Screenshot zeigt, wie die Anwendung mit einigen zusätzlichen Zeilen in den Kreisen aussehen könnte.

![Screenshot mit einer Anwendung, die Berührungspunkte als Kreise mit Linien durch die Mittelpunkte rendert und die Ränder der Berührungspunkte schneidet](images/multitouchpointsfun.png)

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Windows-Eingabe Eingabe](guide-multi-touch-input.md)
</dt> </dl>

 

 