---
description: 'Schritt 4: Zeichnen der Bitmap im Client Bereich'
ms.assetid: fb22468c-9113-46ff-a576-8dee30c458be
title: 'Schritt 4: Zeichnen der Bitmap im Client Bereich'
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4975215e5d75de9909f029a3378bd6cc8bc60916
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "104393814"
---
# <a name="step-4-draw-the-bitmap-on-the-client-area"></a>Schritt 4: Zeichnen der Bitmap im Client Bereich

\[Diese API wird nicht unterstützt und kann in Zukunft geändert oder nicht verfügbar sein.\]

In diesem Thema wird Schritt 4 beschrieben, wie [ein Poster-Frame gepackt](grabbing-a-poster-frame.md)wird.

Der letzte Schritt besteht darin, die Bitmap mithilfe der [**SetDIBitsToDevice**](/windows/win32/api/wingdi/nf-wingdi-setdibitstodevice) -Funktion auf den Client Bereich des Anwendungsfensters zu zeichnen. In diesem Beispiel wird die Bitmap einfach in der oberen linken Ecke des Client Bereichs ohne Berücksichtigung der Fenstergröße gezeichnet:


```C++
case WM_PAINT:
    {
        PAINTSTRUCT ps;
        HDC hdc = BeginPaint(hwnd, &ps);
        if (pbmi)
        {
            int result = SetDIBitsToDevice(hdc, 0, 0, 
                pbmi->biWidth,
                pbmi->biHeight,
                0, 0, 0,
                pbmi->biHeight,
                pBuffer,
                reinterpret_cast<BITMAPINFO*>(pbmi),
                DIB_RGB_COLORS);
        }
        EndPaint(hwnd, &ps);
    }
    break;
```



Die Variablen *pbuffer* und *pbmi* werden in [Schritt 1: Erstellen des Windows-Frameworks](step-1--create-the-windows-framework.md)deklariert, und ihre Werte werden in [Schritt 3: Implementieren der Frame-Grabbing-Funktion](step-3--implement-the-frame-grabbing-function.md)abgerufen.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Ein Poster-Frame wird gepackt.](grabbing-a-poster-frame.md)
</dt> </dl>

 

 
