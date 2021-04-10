---
description: 'Schritt 2: Hinzufügen eines Menübefehls, um einen Poster-Frame zu erfassen'
ms.assetid: 9a0f807b-5543-41d4-ad2a-030a4346131c
title: 'Schritt 2: Hinzufügen eines Menübefehls, um einen Poster-Frame zu erfassen'
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 58d049dc4e79197cfbe0a86b065eaf67a5ea567a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "104131889"
---
# <a name="step-2-add-a-menu-command-to-grab-a-poster-frame"></a>Schritt 2: Hinzufügen eines Menübefehls, um einen Poster-Frame zu erfassen

\[Diese API wird nicht unterstützt und kann in Zukunft geändert oder nicht verfügbar sein.\]

Dieses Thema ist Schritt 2 zum Durchlaufen [eines Poster Frame](grabbing-a-poster-frame.md).

Fügen Sie als nächstes einen Befehl für den Benutzer hinzu, um einen Poster-Frame aus einer Datei abzurufen. Erstellen Sie ein Menü Element mit der Ressourcen-ID IDM \_ Bitmap, und fügen Sie der Fenster Prozedur die folgende Case-Anweisung hinzu:


```C++
case WM_COMMAND:
    switch (LOWORD(wparam))
    {
    case IDM_BITMAP:
        {
            HRESULT hr = DoShowBitmap(hwnd, &pbmi);
            if (SUCCEEDED(hr))
            {
                pBuffer = reinterpret_cast<BYTE*>(pbmi) + 
                    sizeof(BITMAPINFOHEADER);
                InvalidateRect(hwnd, NULL, TRUE);
            }
            else
            {
                MessageBox(hwnd, TEXT("Cannot display the image."),
                    TEXT("Error"), MB_OK | MB_ICONERROR);
            }
        }
        break;  // IDM_BITMAP
    }
    break;  // WM_COMMAND
```



Die doshowbitmap-Funktion gibt den zugeordneten Puffer in *pbmi* zurück. Wenn die Funktion erfolgreich ausgeführt wird, wird die Adresse der Bitmap (


```C++
pBuffer
```



) kann als Offset von *pbmi* berechnet werden. Zeigen Sie in der doshowbitmap-Funktion ein Dialogfeld **Datei öffnen** an, in dem der Benutzer eine Datei auswählen kann, und rufen Sie dann die Anwendungs definierte getbitmap-Funktion auf, die die Bitmap abruft:


```C++
HRESULT DoShowBitmap(HWND hwnd, BITMAPINFOHEADER** ppbmih)
{
    OPENFILENAME ofn;       // common dialog box structure
    // Initialize OPENFILENAME (not shown).
    // Display the Open File dialog box.  
    if (GetOpenFileName(&ofn) != TRUE) // failed to open file
    {
        return E_FAIL;
    }
    return GetBitmap(ofn.lpstrFile, ppbmih);
}
```



Weiter: [Schritt 3: Implementieren der Frame-Grabbing-Funktion](step-3--implement-the-frame-grabbing-function.md)

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Ein Poster-Frame wird gepackt.](grabbing-a-poster-frame.md)
</dt> </dl>

 

 



