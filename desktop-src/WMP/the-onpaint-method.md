---
title: Die OnPaint-Methode
description: Die OnPaint-Methode
ms.assetid: 4b335362-4430-4b05-8aea-7de8df9cc91f
keywords:
- Windows Media Player-Plug-ins, OnPaint-Methode
- Plug-ins, OnPaint-Methode
- Benutzeroberflächen-Plug-ins, OnPaint-Methode
- UI-Plug-ins, OnPaint-Methode
- OnPaint-Methode
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 22641c34bb2edab30c1bf97011e893bc1d9d44a6
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "104471628"
---
# <a name="the-onpaint-method"></a>Die OnPaint-Methode

Die OnPaint-Methode wird immer dann aufgerufen, wenn sich das Plug-in-Fenster selbst zeichnen soll. Dies tritt auf, wenn das Plug-in-Fenster eine WM \_ Paint-Meldung empfängt, die der OnPaint-Methode in der zuvor beschriebenen Meldungs Zuordnung zugeordnet ist. Der Assistent stellt eine Implementierung dieser Methode bereit, die den Hintergrund schwarz zeichnet und den Namen des Plug-ins im Plug-in-Fenster platziert. Die einzige Änderung, die für das Such Benutzeroberflächen-Plug-in erforderlich ist, ist das Entfernen des Codes, in dem der Text angezeigt wird.

Der folgende Code wird verwendet, um diese Methode zu implementieren:


```C++
LRESULT OnPaint(UINT nMsg, WPARAM wParam, 
                         LPARAM lParam, BOOL& bHandled)
{
    PAINTSTRUCT ps;

    HDC hDC = BeginPaint(&ps);

    RECT rc;
    GetClientRect(&rc);

    HBRUSH hNewBrush = ::CreateSolidBrush( RGB(0, 0, 0) );

    if (hNewBrush)
    {
        ::FillRect(hDC, &rc, hNewBrush );
        ::DeleteObject( hNewBrush );
    }

    EndPaint(&ps);
    return 0;
}

```



## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[**Implementieren von cpluginwindow**](implementing-cpluginwindow.md)
</dt> </dl>

 

 




