---
title: Die OnPaint-Methode
description: Die OnPaint-Methode
ms.assetid: 4b335362-4430-4b05-8aea-7de8df9cc91f
keywords:
- Windows Media Player-Plug-Ins, OnPaint-Methode
- Plug-Ins, OnPaint-Methode
- Benutzeroberflächen-Plug-Ins, OnPaint-Methode
- Benutzeroberflächen-Plug-Ins, OnPaint-Methode
- OnPaint-Methode
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: aa5e121cdaeac1c7589e58b1613a8d25bdff4f44f6db2375bcbdc34da20929e8
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "120001950"
---
# <a name="the-onpaint-method"></a>Die OnPaint-Methode

Die OnPaint-Methode wird immer dann aufgerufen, wenn das Plug-In-Fenster sich selbst zeichnen soll. Dies tritt auf, wenn das Plug-In-Fenster eine WM PAINT-Nachricht empfängt, die der OnPaint-Methode in der zuvor beschriebenen \_ Meldungszuordnung zugeordnet ist. Der Assistent bietet eine Implementierung dieser Methode, die den Hintergrund schwarz zeichnet und den Namen des Plug-Ins im Plug-In-Fenster platziert. Die einzige Änderung, die für das Search UI-Plug-In erforderlich ist, ist das Entfernen des Codes, der den Text anzeigt.

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

[**Implementieren von CPluginWindow**](implementing-cpluginwindow.md)
</dt> </dl>

 

 




