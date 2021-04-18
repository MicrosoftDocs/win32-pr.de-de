---
title: Hinzufügen von Rückruf Funktionen zu einer Anwendung
description: Hinzufügen von Rückruf Funktionen zu einer Anwendung
ms.assetid: b7bde1be-b229-4e00-8906-22d7dcf9ea04
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1d4f5f3dc43227f92305032decaf917bf521d95b
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "104515794"
---
# <a name="adding-callback-functions-to-an-application"></a><span data-ttu-id="2cd81-103">Hinzufügen von Rückruf Funktionen zu einer Anwendung</span><span class="sxs-lookup"><span data-stu-id="2cd81-103">Adding Callback Functions to an Application</span></span>

<span data-ttu-id="2cd81-104">Eine Anwendung kann Rückruf Funktionen mit dem Erfassungsfenster registrieren, damit die Anwendung in den folgenden Situationen benachrichtigt wird:</span><span class="sxs-lookup"><span data-stu-id="2cd81-104">An application can register callback functions with the capture window so that it notifies the application in the following circumstances:</span></span>

-   <span data-ttu-id="2cd81-105">Statusänderungen</span><span class="sxs-lookup"><span data-stu-id="2cd81-105">The status changes</span></span>
-   <span data-ttu-id="2cd81-106">Fehler treten auf</span><span class="sxs-lookup"><span data-stu-id="2cd81-106">Errors occur</span></span>
-   <span data-ttu-id="2cd81-107">Video Frame-und Audiopuffer werden verfügbar</span><span class="sxs-lookup"><span data-stu-id="2cd81-107">Video frame and audio buffers become available</span></span>
-   <span data-ttu-id="2cd81-108">Die Anwendung sollte während der streamingerfassung ergeben.</span><span class="sxs-lookup"><span data-stu-id="2cd81-108">The application should yield during streaming capture</span></span>

<span data-ttu-id="2cd81-109">Im folgenden Beispiel wird ein Aufzeichnungs Fenster erstellt und Status-, Fehler-, Videostream-und Frame Rückruf Funktionen in der Nachrichten Verarbeitungs Schleife einer Anwendung registriert.</span><span class="sxs-lookup"><span data-stu-id="2cd81-109">The following example creates a capture window and registers status, error, video stream, and frame callback functions in the message-processing loop of an application.</span></span> <span data-ttu-id="2cd81-110">Sie enthält auch eine Beispiel Anweisung zum Deaktivieren einer Rückruffunktion.</span><span class="sxs-lookup"><span data-stu-id="2cd81-110">It also includes a sample statement for disabling a callback function.</span></span> <span data-ttu-id="2cd81-111">Nachfolgende Beispiele zeigen einfache Status-, Fehler-und Frame Rückruf Funktionen.</span><span class="sxs-lookup"><span data-stu-id="2cd81-111">Subsequent examples show simple status, error, and frame callback functions.</span></span>


```C++
case WM_CREATE: 
{ 
    char    achDeviceName[80] ; 
    char    achDeviceVersion[100] ; 
    char    achBuffer[100] ; 
    WORD    wDriverCount = 0 ; 
    WORD    wIndex ; 
    WORD    wError ; 
    HMENU   hMenu ; 
 
    // Create a capture window using the capCreateCaptureWindow macro.
    ghWndCap = capCreateCaptureWindow((LPSTR)"Capture Window", 
        WS_CHILD | WS_VISIBLE, 0, 0, 160, 120, (HWND) hWnd, (int) 0); 
 
    // Register the error callback function using the 
    // capSetCallbackOnError macro. 
    capSetCallbackOnError(ghWndCap, fpErrorCallback); 
 
    // Register the status callback function using the 
    // capSetCallbackOnStatus macro. 
    capSetCallbackOnStatus(ghWndCap, fpStatusCallback); 
 
    // Register the video-stream callback function using the
    // capSetCallbackOnVideoStream macro. 
    capSetCallbackOnVideoStream(ghWndCap, fpVideoCallback); 
 
    // Register the frame callback function using the
    // capSetCallbackOnFrame macro. 
    capSetCallbackOnFrame(ghWndCap, fpFrameCallback); 
 
    // Connect to a capture driver 

    break; 
} 
case WM_CLOSE: 
{ 
// Use the capSetCallbackOnFrame macro to 
// disable the frame callback. Similar calls exist for the other 
// callback functions.

    capSetCallbackOnFrame(ghWndCap, NULL); 

    break; 
} 
 
```



## <a name="related-topics"></a><span data-ttu-id="2cd81-112">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="2cd81-112">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="2cd81-113">Verwenden der Video Erfassung</span><span class="sxs-lookup"><span data-stu-id="2cd81-113">Using Video Capture</span></span>](using-video-capture.md)
</dt> </dl>

 

 




