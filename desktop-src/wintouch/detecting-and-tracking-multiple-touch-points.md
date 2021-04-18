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
# <a name="detecting-and-tracking-multiple-touch-points"></a><span data-ttu-id="24dc2-106">Erkennen und Nachverfolgen mehrerer Berührungspunkte</span><span class="sxs-lookup"><span data-stu-id="24dc2-106">Detecting and Tracking Multiple Touch Points</span></span>

<span data-ttu-id="24dc2-107">In den folgenden Schritten wird erläutert, wie Sie mithilfe von Windows-Finger Eingaben mehrere Berührungspunkte verfolgen.</span><span class="sxs-lookup"><span data-stu-id="24dc2-107">The following steps explain how to track multiple touch points using Windows Touch.</span></span>

1.  <span data-ttu-id="24dc2-108">Erstellen Sie eine Anwendung, und aktivieren Sie Windows-Interaktion.</span><span class="sxs-lookup"><span data-stu-id="24dc2-108">Create an application and enable Windows Touch.</span></span>
2.  <span data-ttu-id="24dc2-109">Fügen Sie einen Handler für [**WM- \_ Berührungs**](wm-touchdown.md) -und Verfolgungs Punkte hinzu.</span><span class="sxs-lookup"><span data-stu-id="24dc2-109">Add a handler for [**WM\_TOUCH**](wm-touchdown.md) and track points.</span></span>
3.  <span data-ttu-id="24dc2-110">Zeichnen Sie die Punkte.</span><span class="sxs-lookup"><span data-stu-id="24dc2-110">Draw the points.</span></span>

<span data-ttu-id="24dc2-111">Nachdem Sie die Anwendung ausgeführt haben, werden die Kreise unter den einzelnen Finger Eingaben angezeigt.</span><span class="sxs-lookup"><span data-stu-id="24dc2-111">After you have your application running, it will render circles under each touch.</span></span> <span data-ttu-id="24dc2-112">Der folgende Screenshot zeigt, wie Ihre Anwendung während der Ausführung aussehen könnte.</span><span class="sxs-lookup"><span data-stu-id="24dc2-112">The following screen shot shows how your application might look while running.</span></span>

![Screenshot mit einer Anwendung, die Berührungspunkte als grüne und gelbe Kreise rendert](images/multitouchpoints.png)

## <a name="create-an-application-and-enable-windows-touch"></a><span data-ttu-id="24dc2-114">Erstellen einer Anwendung und Aktivieren von Windows-Finger Eingaben</span><span class="sxs-lookup"><span data-stu-id="24dc2-114">Create an Application and Enable Windows Touch</span></span>

<span data-ttu-id="24dc2-115">Beginnen Sie mit einer Microsoft Win32-Anwendung mithilfe des Assistenten für Microsoft Visual Studio.</span><span class="sxs-lookup"><span data-stu-id="24dc2-115">Start with a Microsoft Win32 application using the Microsoft Visual Studio wizard.</span></span> <span data-ttu-id="24dc2-116">Nachdem Sie den Assistenten abgeschlossen haben, fügen Sie Unterstützung für Windows-Finger Eingabenachrichten hinzu, indem Sie die Windows-Version in "targetver. h" festlegen und in Ihrer Anwendung Windows. h und WINDOWSX. h einschließen.</span><span class="sxs-lookup"><span data-stu-id="24dc2-116">After you have completed the wizard, add support for Windows Touch messages by setting the Windows version in targetver.h and including windows.h and windowsx.h in your application.</span></span> <span data-ttu-id="24dc2-117">Der folgende Code zeigt, wie Sie die Windows-Version in "targetver. h" festlegen.</span><span class="sxs-lookup"><span data-stu-id="24dc2-117">The following code shows how to set the Windows version in targetver.h.</span></span>


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



<span data-ttu-id="24dc2-118">Der folgende Code zeigt, wie die include-Direktiven hinzugefügt werden sollen.</span><span class="sxs-lookup"><span data-stu-id="24dc2-118">The following code shows how your include directives should be added.</span></span> <span data-ttu-id="24dc2-119">Außerdem können Sie einige globale Variablen erstellen, die später verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="24dc2-119">Also, you can create some global variables that will be used later.</span></span>


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



## <a name="add-handler-for-wm_touch-and-track-points"></a><span data-ttu-id="24dc2-120">Handler für WM \_ -Berührungs-und Verfolgungs Punkte hinzufügen</span><span class="sxs-lookup"><span data-stu-id="24dc2-120">Add Handler for WM\_TOUCH and Track Points</span></span>

<span data-ttu-id="24dc2-121">Deklarieren Sie zunächst einige Variablen, die vom [**WM- \_**](wm-touchdown.md) Fingerabdruck Handler in [**WndProc**](/previous-versions/windows/desktop/legacy/ms633573(v=vs.85))verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="24dc2-121">First, declare some variables that are used by the [**WM\_TOUCH**](wm-touchdown.md) handler in [**WndProc**](/previous-versions/windows/desktop/legacy/ms633573(v=vs.85)).</span></span>


```C++
int wmId, wmEvent, i, x, y;

UINT cInputs;
PTOUCHINPUT pInputs;
POINT ptInput;   
```



<span data-ttu-id="24dc2-122">Initialisieren Sie nun die Variablen, die zum Speichern von Berührungspunkten verwendet werden, und registrieren Sie das Fenster für die Berührungs Eingabe von der **InitInstance** -Methode.</span><span class="sxs-lookup"><span data-stu-id="24dc2-122">Now, initialize the variables used for storing touch points and register the window for touch input from the **InitInstance** method.</span></span>


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



<span data-ttu-id="24dc2-123">Behandeln Sie als nächstes [**die \_ WM**](wm-touchdown.md) -Fingereingabe Nachricht von der [**WndProc**](/previous-versions/windows/desktop/legacy/ms633573(v=vs.85)) -Methode.</span><span class="sxs-lookup"><span data-stu-id="24dc2-123">Next, handle the [**WM\_TOUCH**](wm-touchdown.md) message from the [**WndProc**](/previous-versions/windows/desktop/legacy/ms633573(v=vs.85)) method.</span></span> <span data-ttu-id="24dc2-124">Der folgende Code zeigt eine Implementierung des-Handlers **für \_ WM**-Finger Eingaben.</span><span class="sxs-lookup"><span data-stu-id="24dc2-124">The following code shows an implementation of the handler for **WM\_TOUCH**.</span></span>


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
> <span data-ttu-id="24dc2-125">Um die [**ScreenToClient**](/windows/desktop/api/winuser/nf-winuser-screentoclient) -Funktion verwenden zu können, müssen Sie in Ihrer Anwendung über eine hohe dpi-Unterstützung verfügen.</span><span class="sxs-lookup"><span data-stu-id="24dc2-125">In order to use the [**ScreenToClient**](/windows/desktop/api/winuser/nf-winuser-screentoclient) function, you must have high DPI support in your application.</span></span> <span data-ttu-id="24dc2-126">Weitere Informationen zur Unterstützung von High dpi finden Sie im Abschnitt " [High dpi]( ../hidpi/high-dpi-desktop-application-development-on-windows.md) " in MSDN.</span><span class="sxs-lookup"><span data-stu-id="24dc2-126">For more information on supporting high DPI, see the [High DPI]( ../hidpi/high-dpi-desktop-application-development-on-windows.md) section of MSDN.</span></span>

 

<span data-ttu-id="24dc2-127">Wenn ein Benutzer nun den Bildschirm berührt, werden die Positionen, die er berührt, im points-Array gespeichert.</span><span class="sxs-lookup"><span data-stu-id="24dc2-127">Now when a user touches the screen, the positions that he or she is touching will be stored in the points array.</span></span> <span data-ttu-id="24dc2-128">Der **dwID-** Member der [**TOUCHINPUT**](/windows/win32/api/winuser/ns-winuser-touchinput) -Struktur speichert einen Bezeichner, der Hardware abhängig ist.</span><span class="sxs-lookup"><span data-stu-id="24dc2-128">The **dwID** member of the [**TOUCHINPUT**](/windows/win32/api/winuser/ns-winuser-touchinput) structure stores an identifier that will be hardware dependent.</span></span>

<span data-ttu-id="24dc2-129">Um das Problem zu beheben, dass der dwID-Member von der Hardware abhängig ist, verwendet der [**WM- \_ touchfallhandler**](wm-touchdown.md) eine Funktion, **getcontactindex**, die den **dwID-** Member der [**TOUCHINPUT**](/windows/win32/api/winuser/ns-winuser-touchinput) -Struktur einem Punkt zuordnet, der auf dem Bildschirm gezeichnet wird.</span><span class="sxs-lookup"><span data-stu-id="24dc2-129">To address the issue of the dwID member being dependent on hardware, the [**WM\_TOUCH**](wm-touchdown.md) case handler uses a function, **GetContactIndex**, that maps the **dwID** member of the [**TOUCHINPUT**](/windows/win32/api/winuser/ns-winuser-touchinput) structure to a point that is drawn on the screen.</span></span> <span data-ttu-id="24dc2-130">Der folgende Code zeigt eine Implementierung dieser Funktion.</span><span class="sxs-lookup"><span data-stu-id="24dc2-130">The following code shows an implementation of this function.</span></span>


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



## <a name="draw-the-points"></a><span data-ttu-id="24dc2-131">Zeichnen der Punkte</span><span class="sxs-lookup"><span data-stu-id="24dc2-131">Draw the Points</span></span>

<span data-ttu-id="24dc2-132">Deklarieren Sie die folgenden Variablen für die Zeichnungs Routine.</span><span class="sxs-lookup"><span data-stu-id="24dc2-132">Declare the following variables for the drawing routine.</span></span>


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



<span data-ttu-id="24dc2-133">Der Kontext-Anzeige Kontext *memdc* dient zum Speichern eines temporären Grafik Kontexts, der mit dem gerenderten Anzeige Kontext ( *hdc*) ausgetauscht wird, um das Flimmern auszuschließen.</span><span class="sxs-lookup"><span data-stu-id="24dc2-133">The memory display context *memDC* is used for storing a temporary graphics context that is swapped with the rendered display context, *hdc*, to eliminate flickering.</span></span> <span data-ttu-id="24dc2-134">Implementieren Sie die Zeichnungs Routine, die die von Ihnen gespeicherten Punkte annimmt und einen Kreis an den Punkten zeichnet.</span><span class="sxs-lookup"><span data-stu-id="24dc2-134">Implement the drawing routine, which takes the points you have stored and draws a circle at the points.</span></span> <span data-ttu-id="24dc2-135">Der folgende Code zeigt, wie Sie den [**WM- \_ Paint**](/windows/desktop/gdi/wm-paint) -Handler implementieren können.</span><span class="sxs-lookup"><span data-stu-id="24dc2-135">The following code shows how you could implement the [**WM\_PAINT**](/windows/desktop/gdi/wm-paint) handler.</span></span>


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



<span data-ttu-id="24dc2-136">Wenn Sie die Anwendung ausführen, sollte Sie nun in etwa wie in der Abbildung am Anfang dieses Abschnitts aussehen.</span><span class="sxs-lookup"><span data-stu-id="24dc2-136">When you run your application, it now should look something like the illustration at the beginning of this section.</span></span>

<span data-ttu-id="24dc2-137">Um Spaß zu machen, können Sie einige zusätzliche Zeilen um die Berührungspunkte zeichnen.</span><span class="sxs-lookup"><span data-stu-id="24dc2-137">For fun, you can draw some extra lines around the touch points.</span></span> <span data-ttu-id="24dc2-138">Der folgende Screenshot zeigt, wie die Anwendung mit einigen zusätzlichen Zeilen in den Kreisen aussehen könnte.</span><span class="sxs-lookup"><span data-stu-id="24dc2-138">The following screen shot shows how the application could look with a few extra lines drawn around the circles.</span></span>

![Screenshot mit einer Anwendung, die Berührungspunkte als Kreise mit Linien durch die Mittelpunkte rendert und die Ränder der Berührungspunkte schneidet](images/multitouchpointsfun.png)

## <a name="related-topics"></a><span data-ttu-id="24dc2-140">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="24dc2-140">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="24dc2-141">Windows-Eingabe Eingabe</span><span class="sxs-lookup"><span data-stu-id="24dc2-141">Windows Touch Input</span></span>](guide-multi-touch-input.md)
</dt> </dl>

 

 