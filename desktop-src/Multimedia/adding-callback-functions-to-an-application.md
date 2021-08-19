---
title: Hinzufügen von Rückruffunktionen zu einer Anwendung
description: Hinzufügen von Rückruffunktionen zu einer Anwendung
ms.assetid: b7bde1be-b229-4e00-8906-22d7dcf9ea04
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6dcd72b1a95a416398f482b90d7cd15cd80e1698a66a4b1c482bc92fc523ab2f
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118941828"
---
# <a name="adding-callback-functions-to-an-application"></a>Hinzufügen von Rückruffunktionen zu einer Anwendung

Eine Anwendung kann Rückruffunktionen im Erfassungsfenster registrieren, sodass sie die Anwendung unter den folgenden Umständen benachrichtigt:

-   Der Status ändert sich.
-   Fehler treten auf
-   Videoframes und Audiopuffer werden verfügbar
-   Die Anwendung sollte während der Streamingerfassung ergebnissen.

Im folgenden Beispiel wird ein Erfassungsfenster erstellt und die Status-, Fehler-, Videostream- und Framerückruffunktionen in der Nachrichtenverarbeitungsschleife einer Anwendung registriert. Sie enthält auch eine Beispielanweisung zum Deaktivieren einer Rückruffunktion. Nachfolgende Beispiele zeigen einfache Status-, Fehler- und Framerückruffunktionen.


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



## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Verwenden von Video capture](using-video-capture.md)
</dt> </dl>

 

 




