---
title: Ersten Einstieg in Windows-Touchbewegungen
description: In diesem Abschnitt werden die grundlegenden Schritte für die Verwendung von multitouchgesten beschrieben.
ms.assetid: 0ffe222a-a0ac-498b-a4ca-85cfb1caba93
keywords:
- Windows-Toucheingabe, Gesten
- Windows-Fingereingabe, Meldungen
- Gesten, Informationen
- Gesten, Meldungen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 506fee0667e6eb38469bda10af9ded0ea6d3439f
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "104388012"
---
# <a name="getting-started-with-windows-touch-gestures"></a><span data-ttu-id="82910-107">Ersten Einstieg in Windows-Touchbewegungen</span><span class="sxs-lookup"><span data-stu-id="82910-107">Getting Started with Windows Touch Gestures</span></span>

<span data-ttu-id="82910-108">In diesem Abschnitt werden die grundlegenden Schritte für die Verwendung von multitouchgesten beschrieben.</span><span class="sxs-lookup"><span data-stu-id="82910-108">This section describes the basic steps for using multitouch gestures.</span></span>

<span data-ttu-id="82910-109">Die folgenden Schritte werden in der Regel bei der Verwendung von Windows-Touchgesten durchgeführt:</span><span class="sxs-lookup"><span data-stu-id="82910-109">The following steps are typically performed when using Windows Touch gestures:</span></span>

1.  <span data-ttu-id="82910-110">Einrichten eines Fensters zum Empfangen von Gesten.</span><span class="sxs-lookup"><span data-stu-id="82910-110">Set up a window for receiving gestures.</span></span>
2.  <span data-ttu-id="82910-111">Behandelt die Gesten Nachrichten.</span><span class="sxs-lookup"><span data-stu-id="82910-111">Handle the gesture messages.</span></span>
3.  <span data-ttu-id="82910-112">Interpretiert die Gesten Nachrichten.</span><span class="sxs-lookup"><span data-stu-id="82910-112">Interpret the gesture messages.</span></span>

## <a name="setting-up-a-window-to-receive-gestures"></a><span data-ttu-id="82910-113">Einrichten eines Fensters zum Empfangen von Gesten</span><span class="sxs-lookup"><span data-stu-id="82910-113">Setting up a Window to Receive Gestures</span></span>

<span data-ttu-id="82910-114">Standardmäßig erhalten Sie [**WM- \_ Gesten**](wm-gesture.md) Nachrichten.</span><span class="sxs-lookup"><span data-stu-id="82910-114">By default, you receive [**WM\_GESTURE**](wm-gesture.md) messages.</span></span>

> [!Note]  
> <span data-ttu-id="82910-115">Wenn Sie [**RegisterTouchWindow**](/windows/desktop/api/winuser/nf-winuser-registertouchwindow)aufrufen, wird der Empfang von [**WM- \_ Gesten**](wm-gesture.md) Nachrichten beendet.</span><span class="sxs-lookup"><span data-stu-id="82910-115">If you call [**RegisterTouchWindow**](/windows/desktop/api/winuser/nf-winuser-registertouchwindow), you will stop receiving [**WM\_GESTURE**](wm-gesture.md) messages.</span></span> <span data-ttu-id="82910-116">Wenn Sie keine Nachrichten der **WM- \_ Geste** empfangen, stellen Sie sicher, dass Sie **RegisterTouchWindow** nicht aufgerufen haben.</span><span class="sxs-lookup"><span data-stu-id="82910-116">If you are not receiving **WM\_GESTURE** messages, make sure that you haven't called **RegisterTouchWindow**.</span></span>

 

<span data-ttu-id="82910-117">Der folgende Code zeigt eine einfache InitInstance-Implementierung.</span><span class="sxs-lookup"><span data-stu-id="82910-117">The following code shows a simple InitInstance implementation.</span></span>


```C++
#include <windows.h>


BOOL InitInstance(HINSTANCE hInstance, int nCmdShow)
{
   HWND hWnd;

   hInst = hInstance; // Store instance handle in our global variable

   hWnd = CreateWindow(szWindowClass, szTitle, WS_OVERLAPPEDWINDOW,
      CW_USEDEFAULT, 0, CW_USEDEFAULT, 0, NULL, NULL, hInstance, NULL);

   if (!hWnd)
   {
      return FALSE;
   }

   ShowWindow(hWnd, nCmdShow);
   UpdateWindow(hWnd);

   return TRUE;
}
```



## <a name="handling-gesture-messages"></a><span data-ttu-id="82910-118">Verarbeiten von Gesten Nachrichten</span><span class="sxs-lookup"><span data-stu-id="82910-118">Handling Gesture Messages</span></span>

<span data-ttu-id="82910-119">Ähnlich wie bei der Handhabung von Windows-toucheingabenachrichten können Sie Gesten Nachrichten in vielerlei Hinsicht verarbeiten.</span><span class="sxs-lookup"><span data-stu-id="82910-119">Similar to handling Windows Touch input messages, you can handle gesture messages in many ways.</span></span> <span data-ttu-id="82910-120">Wenn Sie Win32 verwenden, können Sie in WndProc nach der Meldung der [**WM- \_ Geste**](wm-gesture.md) suchen.</span><span class="sxs-lookup"><span data-stu-id="82910-120">If you are using Win32, you can check for the [**WM\_GESTURE**](wm-gesture.md) message in WndProc.</span></span> <span data-ttu-id="82910-121">Wenn Sie einen anderen Anwendungstyp erstellen, können Sie die **WM- \_ Gesten** Nachricht der Meldungs Zuordnung hinzufügen und dann einen benutzerdefinierten Handler implementieren.</span><span class="sxs-lookup"><span data-stu-id="82910-121">If you are creating another type of application, you can add the **WM\_GESTURE** message to the message map and then implement a custom handler.</span></span>

<span data-ttu-id="82910-122">Der folgende Code zeigt, wie Gesten Nachrichten behandelt werden könnten.</span><span class="sxs-lookup"><span data-stu-id="82910-122">The following code shows how gesture messages could be handled.</span></span>


```C++
LRESULT CALLBACK WndProc(HWND hWnd, UINT message, WPARAM wParam, LPARAM lParam)
{
    int wmId, wmEvent;
    PAINTSTRUCT ps;
    HDC hdc;

    switch (message)
    {    
    case WM_GESTURE:
            // Insert handler code here to interpret the gesture.            
            return DecodeGesture(hWnd, message, wParam, lParam);            
```



## <a name="interpreting-the-gesture-messages"></a><span data-ttu-id="82910-123">Interpretieren der Gesten Nachrichten</span><span class="sxs-lookup"><span data-stu-id="82910-123">Interpreting the Gesture Messages</span></span>

<span data-ttu-id="82910-124">Mit der [**getgestureinfo**](/windows/desktop/api/winuser/nf-winuser-getgestureinfo) -Funktion wird eine Gesten Nachricht in eine Struktur interpretiert, in der die Geste beschrieben wird.</span><span class="sxs-lookup"><span data-stu-id="82910-124">The [**GetGestureInfo**](/windows/desktop/api/winuser/nf-winuser-getgestureinfo) function is used to interpret a gesture message into a structure describing the gesture.</span></span> <span data-ttu-id="82910-125">Die Struktur " [**GESTUREINFO**](/windows/win32/api/winuser/ns-winuser-gestureinfo)" enthält Informationen über die Geste, wie z. b. den Speicherort, an dem die Geste ausgeführt wurde, und den Typ der Geste.</span><span class="sxs-lookup"><span data-stu-id="82910-125">The structure, [**GESTUREINFO**](/windows/win32/api/winuser/ns-winuser-gestureinfo), has information about the gesture such as the location where the gesture was performed and the type of gesture.</span></span> <span data-ttu-id="82910-126">Der folgende Code zeigt, wie Sie eine Gesten Nachricht abrufen und interpretieren können.</span><span class="sxs-lookup"><span data-stu-id="82910-126">The following code shows how you can retrieve and interpret a gesture message.</span></span>


```C++
  LRESULT DecodeGesture(HWND hWnd, UINT message, WPARAM wParam, LPARAM lParam){
    // Create a structure to populate and retrieve the extra message info.
    GESTUREINFO gi;  
    
    ZeroMemory(&gi, sizeof(GESTUREINFO));
    
    gi.cbSize = sizeof(GESTUREINFO);

    BOOL bResult  = GetGestureInfo((HGESTUREINFO)lParam, &gi);
    BOOL bHandled = FALSE;

    if (bResult){
        // now interpret the gesture
        switch (gi.dwID){
           case GID_ZOOM:
               // Code for zooming goes here     
               bHandled = TRUE;
               break;
           case GID_PAN:
               // Code for panning goes here
               bHandled = TRUE;
               break;
           case GID_ROTATE:
               // Code for rotation goes here
               bHandled = TRUE;
               break;
           case GID_TWOFINGERTAP:
               // Code for two-finger tap goes here
               bHandled = TRUE;
               break;
           case GID_PRESSANDTAP:
               // Code for roll over goes here
               bHandled = TRUE;
               break;
           default:
               // A gesture was not recognized
               break;
        }
    }else{
        DWORD dwErr = GetLastError();
        if (dwErr > 0){
            //MessageBoxW(hWnd, L"Error!", L"Could not retrieve a GESTUREINFO structure.", MB_OK);
        }
    }
    if (bHandled){
        return 0;
    }else{
        return DefWindowProc(hWnd, message, wParam, lParam);
    }
  }
```



## <a name="related-topics"></a><span data-ttu-id="82910-127">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="82910-127">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="82910-128">Windows-Touchgesten</span><span class="sxs-lookup"><span data-stu-id="82910-128">Windows Touch Gestures</span></span>](guide-multi-touch-gestures.md)
</dt> </dl>

 

 




