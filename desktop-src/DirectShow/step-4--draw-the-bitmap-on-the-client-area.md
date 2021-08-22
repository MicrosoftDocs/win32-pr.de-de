---
description: 'Schritt 4: Zeichnen der Bitmap im Clientbereich'
ms.assetid: fb22468c-9113-46ff-a576-8dee30c458be
title: 'Schritt 4: Zeichnen der Bitmap im Clientbereich'
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 253e7d8a5b7508d5ae9f27195dbb7d59b30508ff2aacd8ec2713e0f4d6c909f7
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118951789"
---
# <a name="step-4-draw-the-bitmap-on-the-client-area"></a>Schritt 4: Zeichnen der Bitmap im Clientbereich

\[Diese API wird nicht unterstützt und kann in Zukunft geändert oder nicht mehr verfügbar sein.\]

Dieses Thema ist Schritt 4 von [Grabbing a Poster Frame](grabbing-a-poster-frame.md).

Der letzte Schritt besteht darin, die Bitmap mithilfe der [**SetDIBitsToDevice-Funktion**](/windows/win32/api/wingdi/nf-wingdi-setdibitstodevice) in den Clientbereich des Anwendungsfensters zu zeichnen. In diesem Beispiel wird die Bitmap einfach in der oberen linken Ecke des Clientbereichs zeichnet, ohne die Fenstergröße zu berücksichtigen:


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



Die Variablen *pBuffer* und *pbmi* werden in [Schritt 1: Erstellen des Windows Framework](step-1--create-the-windows-framework.md)deklariert, und ihre Werte werden in Schritt [3: Implementieren der Frame-Grabbing-Funktion](step-3--implement-the-frame-grabbing-function.md)abgerufen.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Greifen eines Posterrahmens](grabbing-a-poster-frame.md)
</dt> </dl>

 

 
