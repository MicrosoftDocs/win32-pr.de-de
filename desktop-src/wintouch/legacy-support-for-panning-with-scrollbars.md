---
title: Legacyunterstützung für Schwenken mit Scrollleisten
description: In diesem Abschnitt wird die Unterstützung für das Schwenken mithilfe von Scrollleisten in Windows-basierten Anwendungen beschrieben.
ms.assetid: a8906b48-b804-4f3a-bb9b-dc94b632e2f7
keywords:
- Windows Touch,Legacy-Unterstützung
- Schwenken mit Scrollleisten
- Windows Touch,Schwenken mit Bildlaufleisten
- Windows Touch,Scrollleisten
- Scrollleisten,Schwenken
- Scrollleisten,Legacyunterstützung
- Windows Touch,Gesten
- Gesten,Schwenken mit Scrollleisten
- Windows Touch,Flicks
- Flicks,Schwenken mit Scrollleisten
- Flicks,deaktivieren
- Windows Touch,Mausradmeldungen
- Mausradmeldungen
- Windows Touch,Anpassen des Schwenkens
- Schwenken, Scrollleisten
- Schwenken, Legacyunterstützung
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 97190d637cae5cc6936ecd78dca31e1e6c0f9ef1037b292b6080f973fc4e8701
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119086309"
---
# <a name="legacy-support-for-panning-with-scroll-bars"></a>Legacyunterstützung für Schwenken mit Scrollleisten

In diesem Abschnitt wird die Unterstützung für das Schwenken mithilfe von Scrollleisten in Windows-basierten Anwendungen beschrieben.

In Windows 7 generieren Schwenkgesten WM SCROLL-Nachrichten, um legacy-Unterstützung für \_ \* Schwenken zu ermöglichen. Da Ihre Anwendungen möglicherweise nicht alle WM SCROLL-Nachrichten unterstützen, funktioniert \_ \* das Schwenken möglicherweise nicht ordnungsgemäß. In diesem Thema werden die Schritte beschrieben, die Sie ausführen müssen, um sicherzustellen, dass das Legacy-Schwenken in Anwendungen wie erwartet funktioniert.

## <a name="overview"></a>Übersicht

In den folgenden Abschnitten wird erläutert, wie Sie das Legacy-Schwenken aktivieren:

-   Erstellen Sie eine Anwendung mit Bildlaufleisten.
-   Deaktivieren Sie die Licks.
-   Passen Sie die Schwenkerfahrung an.

## <a name="create-an-application-with-scroll-bars"></a>Erstellen einer Anwendung mit Bildlaufleisten

Starten Sie ein neues Win32-Projekt mithilfe des Microsoft Visual Studio Assistenten. Stellen Sie sicher, dass der Anwendungstyp auf die Windows ist. Sie müssen die Unterstützung für die Active Template Library (ATL) nicht aktivieren. Die folgende Abbildung zeigt, wie Ihr Projekt aussehen wird, nachdem Sie es gestartet haben.

![Screenshot eines Fensters ohne Bildlaufleisten](images/gpd-1.png)

Aktivieren Sie als Nächstes Bildlaufleisten auf dem Bild. Ändern Sie den Code für die Fenstererstellung in **InitInstance** so, dass der [**CreateWindow-Funktionsaufruf**](/windows/desktop/api/winuser/nf-winuser-createwindowa) ein Fenster mit Bildlaufleisten erstellt. Dies wird im folgenden Code veranschaulicht.


```C++
   hWnd = CreateWindow(
      szWindowClass, 
      szTitle, 
      WS_OVERLAPPEDWINDOW | WS_VSCROLL,  // style
      200,                               // x
      200,                               // y
      550,                               // width
      300,                               // height
      NULL,
      NULL,
      hInstance,
      NULL
    );  
```



Nachdem Sie den Code für die Fenstererstellung geändert haben, hat Ihre Anwendung eine Scrollleiste. Die folgende Abbildung zeigt, wie die Anwendung an diesem Punkt aussehen könnte.

![Screenshot eines Fensters mit einer vertikalen Scrollleiste, aber ohne Text](images/gpd-2.png)

Nachdem Sie den Code für die Fenstererstellung geändert haben, fügen Sie ihrer Anwendung ein Scrollleistenobjekt und einen Text hinzu, um einen Bildlauf zu erstellen. Platzieren Sie den folgenden Code am Anfang der **WndProc-Methode.**


```C++
    TEXTMETRIC tm;     
    SCROLLINFO si; 
     
    // These variables are required to display text. 
    static int xClient;     // width of client area 
    static int yClient;     // height of client area 
    static int xClientMax;  // maximum width of client area 
     
    static int xChar;       // horizontal scrolling unit 
    static int yChar;       // vertical scrolling unit 
    static int xUpper;      // average width of uppercase letters 
     
    static int xPos;        // current horizontal scrolling position 
    static int yPos;        // current vertical scrolling position 
     
    int i;                  // loop counter 
    int x, y;               // horizontal and vertical coordinates
     
    int FirstLine;          // first line in the invalidated area 
    int LastLine;           // last line in the invalidated area 
    HRESULT hr;
    int abcLength = 0;  // length of an abc[] item

    int lines = 0;

    // Create an array of lines to display. 
    static const int LINES=28;
    static LPCWSTR abc[] = { 
       L"anteater",  L"bear",      L"cougar", 
       L"dingo",     L"elephant",  L"falcon", 
       L"gazelle",   L"hyena",     L"iguana", 
       L"jackal",    L"kangaroo",  L"llama", 
       L"moose",     L"newt",      L"octopus", 
       L"penguin",   L"quail",     L"rat", 
       L"squid",     L"tortoise",  L"urus", 
       L"vole",      L"walrus",    L"xylophone", 
       L"yak",       L"zebra",
       L"This line contains words, but no character. Go figure.",
       L""
     };        
```



Implementieren Sie als Nächstes die Anwendungslogik zum Konfigurieren der Textberechnungen für Textmetriken. Der folgende Code sollte den vorhandenen **WM \_ CREATE-Fall** in der **WndProc-Funktion** ersetzen.


```C++
    case WM_CREATE : 
        // Get the handle to the client area's device context. 
        hdc = GetDC (hWnd); 
 
        // Extract font dimensions from the text metrics. 
        GetTextMetrics (hdc, &tm); 
        xChar = tm.tmAveCharWidth; 
        xUpper = (tm.tmPitchAndFamily & 1 ? 3 : 2) * xChar/2; 
        yChar = tm.tmHeight + tm.tmExternalLeading; 
 
        // Free the device context. 
        ReleaseDC (hWnd, hdc); 
 
        // Set an arbitrary maximum width for client area. 
        // (xClientMax is the sum of the widths of 48 average 
        // lowercase letters and 12 uppercase letters.) 
        xClientMax = 48 * xChar + 12 * xUpper; 
 
        return 0;
```



Implementieren Sie als Nächstes die Anwendungslogik für die Neuberechnung des Textblocks, wenn die Größe des Fensters geändert wird. Der folgende Code sollte in den Meldungsschalter in **WndProc platziert werden.**


```C++
    case WM_SIZE: 
 
        // Retrieve the dimensions of the client area. 
        yClient = HIWORD (lParam); 
        xClient = LOWORD (lParam); 
 
        // Set the vertical scrolling range and page size
        si.cbSize = sizeof(si); 
        si.fMask  = SIF_RANGE | SIF_PAGE; 
        si.nMin   = 0; 
        si.nMax   = LINES - 1; 
        si.nPage  = yClient / yChar; 
        SetScrollInfo(hWnd, SB_VERT, &si, TRUE); 
 
        // Set the horizontal scrolling range and page size. 
        si.cbSize = sizeof(si); 
        si.fMask  = SIF_RANGE | SIF_PAGE; 
        si.nMin   = 0; 
        si.nMax   = 2 + xClientMax / xChar; 
        si.nPage  = xClient / xChar; 
        SetScrollInfo(hWnd, SB_HORZ, &si, TRUE);            
        return 0;
```



Implementieren Sie als Nächstes die Anwendungslogik für vertikale Bildlaufnachrichten. Der folgende Code sollte in den Meldungsschalter in **WndProc platziert werden.**


```C++
        case WM_VSCROLL:
         // Get all the vertical scroll bar information
         si.cbSize = sizeof (si);
         si.fMask  = SIF_ALL;
         GetScrollInfo (hWnd, SB_VERT, &si);
         // Save the position for comparison later on
         yPos = si.nPos;
         switch (LOWORD (wParam))
         {
         // user clicked the HOME keyboard key
         case SB_TOP:
             si.nPos = si.nMin;
             break;
              
         // user clicked the END keyboard key
         case SB_BOTTOM:
             si.nPos = si.nMax;
             break;
              
         // user clicked the top arrow
         case SB_LINEUP:
             si.nPos -= 1;
             break;
              
         // user clicked the bottom arrow
         case SB_LINEDOWN:
             si.nPos += 1;
             break;
              
         // user clicked the scroll bar shaft above the scroll box
         case SB_PAGEUP:
             si.nPos -= si.nPage;
             break;
              
         // user clicked the scroll bar shaft below the scroll box
         case SB_PAGEDOWN:
             si.nPos += si.nPage;
             break;
              
         // user dragged the scroll box
         case SB_THUMBTRACK:
             si.nPos = si.nTrackPos;
             break;

         // user positioned the scroll box
         // This message is the one used by Windows Touch
         case SB_THUMBPOSITION:
             si.nPos = HIWORD(wParam);
             break;
                            
         default:
              break; 
         }
         // Set the position and then retrieve it.  Due to adjustments
         //   by Windows it may not be the same as the value set.
         si.fMask = SIF_POS;
         SetScrollInfo (hWnd, SB_VERT, &si, TRUE);
         GetScrollInfo (hWnd, SB_VERT, &si);
         // If the position has changed, scroll window and update it
         if (si.nPos != yPos)
         {                    
          ScrollWindow(hWnd, 0, yChar * (yPos - si.nPos), NULL, NULL);
          UpdateWindow (hWnd);
         }
         break;
```



Aktualisieren Sie als Nächstes den Code, um das Fenster neu zu zeichnet. Der folgende Code sollte die STANDARDMÄßIGE **WM \_ PAINT-Case** in **WndProc ersetzen.**


```C++
    case WM_PAINT:
         // Prepare the window for painting
         hdc = BeginPaint (hWnd, &ps);
         // Get vertical scroll bar position
         si.cbSize = sizeof (si);
         si.fMask  = SIF_POS;
         GetScrollInfo (hWnd, SB_VERT, &si);
         yPos = si.nPos;
         // Get horizontal scroll bar position
         GetScrollInfo (hWnd, SB_HORZ, &si);
         xPos = si.nPos;
         // Find painting limits
         FirstLine = max (0, yPos + ps.rcPaint.top / yChar);
         LastLine = min (LINES - 1, yPos + ps.rcPaint.bottom / yChar);
         
         
         
         for (i = FirstLine; i <= LastLine; i++)         
         {
              x = xChar * (1 - xPos);
              y = yChar * (i - yPos);
              
              // Note that "55" in the following depends on the 
              // maximum size of an abc[] item.
              //
              abcLength = wcslen(abc[i]);
              hr = S_OK;
              if ((FAILED(hr)))
              {
                 MessageBox(hWnd, L"err", L"err", NULL);
              }else{
                  TextOut(hdc, x, y, abc[i], abcLength);
              }
              
         }
         // Indicate that painting is finished
         EndPaint (hWnd, &ps);
         return 0;
```



Wenn Sie nun Ihre Anwendung erstellen und ausführen, sollte sie den Textbaustein und eine vertikale Bildlaufleiste enthalten. Die folgende Abbildung zeigt, wie Ihre Anwendung aussehen könnte.

![Screenshot eines Fensters mit vertikaler Scrollleiste und Text](images/gpd-3.png)

## <a name="disable-flicks"></a>Deaktivieren von Flicks

Um die Schwenkerfahrung in Ihrer Anwendung zu verbessern, sollten Sie die Blättern deaktivieren. Legen Sie hierzu fenstereigenschaften für den *hWnd-Wert* fest, wenn er initialisiert wird. Die für Flicks verwendeten Werte werden im Header tpcshrd.h gespeichert, der ebenfalls eingeschlossen werden muss. Der folgende Code sollte in Ihren include-Direktiven und in der **InitInstance-Funktion** platziert werden, nachdem Sie *hWnd erstellt haben.*

> [!Note]  
> Dies ist nützlich für Anwendungen, die sofortiges Feedback bei einem Touch- oder Pen down-Ereignis benötigen, anstatt auf einen Zeit- oder Entfernungsschwellenwert zu testen.

 


```C++
#include <tpcshrd.h>
```




```C++
[...]
BOOL InitInstance(HINSTANCE hInstance, int nCmdShow){
[...]
  
```




```C++
   const DWORD_PTR dwHwndTabletProperty = 
    TABLET_DISABLE_PRESSANDHOLD | // disables press and hold (right-click) gesture
    TABLET_DISABLE_PENTAPFEEDBACK | // disables UI feedback on pen up (waves)
    TABLET_DISABLE_PENBARRELFEEDBACK | // disables UI feedback on pen button down (circle)
    TABLET_DISABLE_FLICKS; // disables pen flicks (back, forward, drag down, drag up)
   
   SetProp(hWnd, MICROSOFT_TABLETPENSERVICE_PROPERTY, reinterpret_cast<HANDLE>(dwHwndTabletProperty));
```



## <a name="customize-the-panning-experience"></a>Anpassen der Schwenkerfahrung

Möglicherweise möchten Sie eine andere Schwenkerfahrung als Windows 7-Angebote standardmäßig. Um das Schwenken zu verbessern, müssen Sie den Handler für die [**WM \_ GESTURE-Meldung**](wm-gesture.md) hinzufügen. Weitere Informationen finden Sie unter [Improving the Single-Finger Panning Experience](improving-the-single-finger-panning-experience.md).

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Windows Touchgesten](guide-multi-touch-gestures.md)
</dt> </dl>

 

 