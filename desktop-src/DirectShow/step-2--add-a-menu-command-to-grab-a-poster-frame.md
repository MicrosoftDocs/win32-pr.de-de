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
# <a name="step-2-add-a-menu-command-to-grab-a-poster-frame"></a><span data-ttu-id="3f00f-103">Schritt 2: Hinzufügen eines Menübefehls, um einen Poster-Frame zu erfassen</span><span class="sxs-lookup"><span data-stu-id="3f00f-103">Step 2: Add a Menu Command to Grab a Poster Frame</span></span>

<span data-ttu-id="3f00f-104">\[Diese API wird nicht unterstützt und kann in Zukunft geändert oder nicht verfügbar sein.\]</span><span class="sxs-lookup"><span data-stu-id="3f00f-104">\[This API is not supported and may be altered or unavailable in the future.\]</span></span>

<span data-ttu-id="3f00f-105">Dieses Thema ist Schritt 2 zum Durchlaufen [eines Poster Frame](grabbing-a-poster-frame.md).</span><span class="sxs-lookup"><span data-stu-id="3f00f-105">This topic is Step 2 of [Grabbing a Poster Frame](grabbing-a-poster-frame.md).</span></span>

<span data-ttu-id="3f00f-106">Fügen Sie als nächstes einen Befehl für den Benutzer hinzu, um einen Poster-Frame aus einer Datei abzurufen.</span><span class="sxs-lookup"><span data-stu-id="3f00f-106">Next, add a command for the user to grab a poster frame from a file.</span></span> <span data-ttu-id="3f00f-107">Erstellen Sie ein Menü Element mit der Ressourcen-ID IDM \_ Bitmap, und fügen Sie der Fenster Prozedur die folgende Case-Anweisung hinzu:</span><span class="sxs-lookup"><span data-stu-id="3f00f-107">Create a menu item with a resource ID of IDM\_BITMAP, and add the following case statement to the window procedure:</span></span>


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



<span data-ttu-id="3f00f-108">Die doshowbitmap-Funktion gibt den zugeordneten Puffer in *pbmi* zurück.</span><span class="sxs-lookup"><span data-stu-id="3f00f-108">The DoShowBitmap function will return the allocated buffer in *pbmi*.</span></span> <span data-ttu-id="3f00f-109">Wenn die Funktion erfolgreich ausgeführt wird, wird die Adresse der Bitmap (</span><span class="sxs-lookup"><span data-stu-id="3f00f-109">Assuming the function succeeds, the address of the bitmap (</span></span>


```C++
pBuffer
```



<span data-ttu-id="3f00f-110">) kann als Offset von *pbmi* berechnet werden.</span><span class="sxs-lookup"><span data-stu-id="3f00f-110">) can be calculated as an offset from *pbmi*.</span></span> <span data-ttu-id="3f00f-111">Zeigen Sie in der doshowbitmap-Funktion ein Dialogfeld **Datei öffnen** an, in dem der Benutzer eine Datei auswählen kann, und rufen Sie dann die Anwendungs definierte getbitmap-Funktion auf, die die Bitmap abruft:</span><span class="sxs-lookup"><span data-stu-id="3f00f-111">In the DoShowBitmap function, display an **Open File** dialog box for the user to choose a file, and then call the application-defined GetBitmap function, which will retrieve the bitmap:</span></span>


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



<span data-ttu-id="3f00f-112">Weiter: [Schritt 3: Implementieren der Frame-Grabbing-Funktion](step-3--implement-the-frame-grabbing-function.md)</span><span class="sxs-lookup"><span data-stu-id="3f00f-112">Next: [Step 3: Implement the Frame-Grabbing Function](step-3--implement-the-frame-grabbing-function.md)</span></span>

## <a name="related-topics"></a><span data-ttu-id="3f00f-113">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="3f00f-113">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="3f00f-114">Ein Poster-Frame wird gepackt.</span><span class="sxs-lookup"><span data-stu-id="3f00f-114">Grabbing a Poster Frame</span></span>](grabbing-a-poster-frame.md)
</dt> </dl>

 

 



