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
# <a name="step-1-create-the-windows-framework"></a>Schritt 1: Erstellen des Windows-Frameworks

\[Diese API wird nicht unterstützt und kann in Zukunft geändert oder nicht verfügbar sein.\]

Beginnen Sie mit dem Erstellen des grundlegenden Frameworks einer Windows-Anwendung, einschließlich winmain und einer Fenster Prozedur. Die WinMain-Funktion wird hier nicht angezeigt. nennen Sie [**CoInitialize**](/windows/win32/api/objbase/nf-objbase-coinitialize) vor der Nachrichten Schleife, um die com-Bibliothek zu initialisieren, [**und initialisieren**](/windows/win32/api/combaseapi/nf-combaseapi-couninitialize) Sie, nachdem die Nachrichten Schleife beendet wurde. Beginnen Sie mit der folgenden minimalen Fenster Prozedur:


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



Wenn Sie einen Poster-Frame aus dem Medien Detektor abrufen, wird ein Puffer zurückgegeben, der eine [**BITMAPINFOHEADER**](/windows/win32/api/wingdi/ns-wingdi-bitmapinfoheader) -Struktur gefolgt von den Bildbits enthält. Definieren Sie daher zwei statische Variablen in der Fenster Prozedur: *pbmi* hält einen Zeiger auf die **BITMAPINFOHEADER** -Struktur, und *pbuffer* hält einen Zeiger auf die Bitmap. Die Anwendung weist den Puffer in *pbmi* mithilfe von zu `new` . Daher muss der Puffer gelöscht werden, bevor das Fenster zerstört wird. Der *pbuffer* -Zeiger wird als Offset von *pbmi* berechnet, sodass es nicht erforderlich ist, ihn zu löschen.

Nächstes: [Schritt 2: Hinzufügen eines Menübefehls, um einen Poster-Frame zu erfassen](step-2--add-a-menu-command-to-grab-a-poster-frame.md)

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Ein Poster-Frame wird gepackt.](grabbing-a-poster-frame.md)
</dt> </dl>

 

 
