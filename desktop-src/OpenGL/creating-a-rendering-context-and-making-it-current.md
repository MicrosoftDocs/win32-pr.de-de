---
title: Erstellen eines Renderingkontexts und Erstellen des aktuellen Kontexts
description: Das folgende Codebeispiel zeigt, wie Sie als Reaktion auf eine WM CREATE-Nachricht einen OpenGL-Renderingkontext \_ erstellen.
ms.assetid: eacf0475-6845-48f9-b016-7f0150679419
keywords:
- OpenGL auf Windows,Renderingkontexte
- Renderingkontexte
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1768506eba506506a7198fbccc7dfefc0491adc96dd1e7bd03d2ec2aa5df8eb8
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119868790"
---
# <a name="creating-a-rendering-context-and-making-it-current"></a>Erstellen eines Renderingkontexts und Erstellen des aktuellen Kontexts

Das folgende Codebeispiel zeigt, wie Sie als Reaktion auf eine WM CREATE-Nachricht einen OpenGL-Renderingkontext \_ erstellen. Beachten Sie, dass Sie das Pixelformat eingerichtet haben, bevor Sie den Renderingkontext erstellen. Beachten Sie auch, dass in diesem Szenario der Gerätekontext nicht lokal freigegeben wird. Sie geben sie frei, wenn das Fenster geschlossen wird, nachdem der Renderingkontext nicht aktuell ist. Weitere Informationen finden Sie unter [Löschen eines Renderingkontexts.](deleting-a-rendering-context.md) Beachten Sie schließlich, dass Sie lokale Variablen für den Gerätekontext und Renderingkontexthandles verwenden können, da Sie mit den [**Funktionen wglGetCurrentContext**](/windows/desktop/api/wingdi/nf-wingdi-wglgetcurrentcontext) und [**wglGetCurrentDC**](/windows/desktop/api/wingdi/nf-wingdi-wglgetcurrentdc) nach Bedarf Handles für diese Kontexte abrufen können.

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

 

 




