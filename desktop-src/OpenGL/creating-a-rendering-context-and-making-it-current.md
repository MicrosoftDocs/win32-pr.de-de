---
title: Erstellen eines renderingkontexts und Erstellen des aktuellen
description: Im folgenden Codebeispiel wird gezeigt, wie ein OpenGL-renderingkontext als Antwort auf eine WM Create-Meldung erstellt wird \_ .
ms.assetid: eacf0475-6845-48f9-b016-7f0150679419
keywords:
- OpenGL unter Windows, renderingkontexte
- renderingkontexte
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c7bcb8eb5a3892aac977f465894808adc19809a7
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "104310623"
---
# <a name="creating-a-rendering-context-and-making-it-current"></a>Erstellen eines renderingkontexts und Erstellen des aktuellen

Im folgenden Codebeispiel wird gezeigt, wie ein OpenGL-renderingkontext als Antwort auf eine WM Create-Meldung erstellt wird \_ . Beachten Sie, dass Sie das Pixel Format vor dem Erstellen des renderingkontexts einrichten. Beachten Sie auch, dass der Gerätekontext in diesem Szenario nicht lokal veröffentlicht wird. Wenn das Fenster geschlossen wird, wird es freigegeben, nachdem der renderingkontext nicht aktuell ist. Weitere Informationen finden Sie unter [Löschen eines renderingkontexts](deleting-a-rendering-context.md). Beachten Sie schließlich, dass Sie lokale Variablen für den Gerätekontext und renderingkontexthandles verwenden können, da Sie mit den [**wglgetcurrentcontext**](/windows/desktop/api/wingdi/nf-wingdi-wglgetcurrentcontext) -und [**wglgetcurrentdc**](/windows/desktop/api/wingdi/nf-wingdi-wglgetcurrentdc) -Funktionen bei Bedarf Handles für diese Kontexte abrufen können.

``` syntax
// a window has been created, but is not yet visible  
case WM_CREATE: 
    { 
    // local variables  
    HDC      hdc ; 
    HGLRC    hglrc ; 
 
    // obtain a device context for the window  
    hdc = GetDC(hWnd); 
     
    // set an appropriate pixel format   
    myPixelFormatSetupFunction(hdc); 
 
    // if we can create a rendering context ...   
    if (hglrc = wglCreateContext( hdc ) ) { 
 
        // try to make it the thread's current rendering context  
        bHaveCurrentRC = wglMakeCurrent(hdc, hglrc) ; 
 
        } 
 
    // perform miscellaneous other WM_CREATE chores ...  
 
    }  
    break;
```

 

 




