---
description: 'Schritt 1: Erstellen des Windows-Frameworks'
ms.assetid: 678c6261-cbd0-4865-a1dd-03de55eca996
title: 'Schritt 1: Erstellen des Windows-Frameworks'
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 91ff1712f631db520ff30065e8943d13b280f3d9
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106356264"
---
# <a name="step-1-create-the-windows-framework"></a><span data-ttu-id="31508-103">Schritt 1: Erstellen des Windows-Frameworks</span><span class="sxs-lookup"><span data-stu-id="31508-103">Step 1: Create the Windows Framework</span></span>

<span data-ttu-id="31508-104">\[Diese API wird nicht unterstützt und kann in Zukunft geändert oder nicht verfügbar sein.\]</span><span class="sxs-lookup"><span data-stu-id="31508-104">\[This API is not supported and may be altered or unavailable in the future.\]</span></span>

<span data-ttu-id="31508-105">Beginnen Sie mit dem Erstellen des grundlegenden Frameworks einer Windows-Anwendung, einschließlich winmain und einer Fenster Prozedur.</span><span class="sxs-lookup"><span data-stu-id="31508-105">Start by creating the basic framework of a Windows application, including WinMain and a window procedure.</span></span> <span data-ttu-id="31508-106">Die WinMain-Funktion wird hier nicht angezeigt. nennen Sie [**CoInitialize**](/windows/win32/api/objbase/nf-objbase-coinitialize) vor der Nachrichten Schleife, um die com-Bibliothek zu initialisieren, [**und initialisieren**](/windows/win32/api/combaseapi/nf-combaseapi-couninitialize) Sie, nachdem die Nachrichten Schleife beendet wurde.</span><span class="sxs-lookup"><span data-stu-id="31508-106">The WinMain function is not shown here; call [**CoInitialize**](/windows/win32/api/objbase/nf-objbase-coinitialize) before the message loop to initialize the COM library, and [**CoUninitialize**](/windows/win32/api/combaseapi/nf-combaseapi-couninitialize) after the message loop exits.</span></span> <span data-ttu-id="31508-107">Beginnen Sie mit der folgenden minimalen Fenster Prozedur:</span><span class="sxs-lookup"><span data-stu-id="31508-107">Start with the following minimal window procedure:</span></span>


```C++
LRESULT CALLBACK MainWndProc(HWND hwnd, UINT msg, WPARAM wparam, LPARAM lparam)
{
    static BITMAPINFOHEADER *pbmi = NULL;
    static BYTE *pBuffer = NULL;
    switch (msg)
    {
    case WM_CLOSE:
        DestroyWindow(hwnd);
        break;
    case WM_DESTROY:
        if (pbmi) delete [] pbmi;
        PostQuitMessage(0);
        break;
    default:
        return DefWindowProc(hwnd, msg, wparam, lparam);
    }
    return 0;
}
```



<span data-ttu-id="31508-108">Wenn Sie einen Poster-Frame aus dem Medien Detektor abrufen, wird ein Puffer zurückgegeben, der eine [**BITMAPINFOHEADER**](/windows/win32/api/wingdi/ns-wingdi-bitmapinfoheader) -Struktur gefolgt von den Bildbits enthält.</span><span class="sxs-lookup"><span data-stu-id="31508-108">When you retrieve a poster frame from the Media Detector, it returns a buffer that contains a [**BITMAPINFOHEADER**](/windows/win32/api/wingdi/ns-wingdi-bitmapinfoheader) structure followed by the image bits.</span></span> <span data-ttu-id="31508-109">Definieren Sie daher zwei statische Variablen in der Fenster Prozedur: *pbmi* hält einen Zeiger auf die **BITMAPINFOHEADER** -Struktur, und *pbuffer* hält einen Zeiger auf die Bitmap.</span><span class="sxs-lookup"><span data-stu-id="31508-109">Therefore, define two static variables in the window procedure: *pbmi* will hold a pointer to the **BITMAPINFOHEADER** structure, and *pBuffer* will hold a pointer to the bitmap.</span></span> <span data-ttu-id="31508-110">Die Anwendung weist den Puffer in *pbmi* mithilfe von zu `new` . Daher muss der Puffer gelöscht werden, bevor das Fenster zerstört wird.</span><span class="sxs-lookup"><span data-stu-id="31508-110">The application will allocate the buffer in *pbmi* using `new`, so it must delete the buffer before the window is destroyed.</span></span> <span data-ttu-id="31508-111">Der *pbuffer* -Zeiger wird als Offset von *pbmi* berechnet, sodass es nicht erforderlich ist, ihn zu löschen.</span><span class="sxs-lookup"><span data-stu-id="31508-111">The *pBuffer* pointer is calculated as an offset from *pbmi*, so there is no need to delete it.</span></span>

<span data-ttu-id="31508-112">Nächstes: [Schritt 2: Hinzufügen eines Menübefehls, um einen Poster-Frame zu erfassen](step-2--add-a-menu-command-to-grab-a-poster-frame.md)</span><span class="sxs-lookup"><span data-stu-id="31508-112">Next: [Step 2: Add a Menu Command to Grab a Poster Frame](step-2--add-a-menu-command-to-grab-a-poster-frame.md)</span></span>

## <a name="related-topics"></a><span data-ttu-id="31508-113">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="31508-113">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="31508-114">Ein Poster-Frame wird gepackt.</span><span class="sxs-lookup"><span data-stu-id="31508-114">Grabbing a Poster Frame</span></span>](grabbing-a-poster-frame.md)
</dt> </dl>

 

 
