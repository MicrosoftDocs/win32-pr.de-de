---
description: 'Schritt 1: Erstellen des Windows Frameworks'
ms.assetid: 678c6261-cbd0-4865-a1dd-03de55eca996
title: 'Schritt 1: Erstellen des Windows Frameworks'
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: feba710c8df948e34c0da0ca9e7a1de85622bfae462290cbce3f36777854cb6e
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119072514"
---
# <a name="step-1-create-the-windows-framework"></a>Schritt 1: Erstellen des Windows Frameworks

\[Diese API wird nicht unterstützt und kann in Zukunft geändert oder nicht mehr verfügbar sein.\]

Erstellen Sie zunächst das grundlegende Framework einer Windows Anwendung, einschließlich WinMain und einer Fensterprozedur. Die WinMain-Funktion wird hier nicht angezeigt. Rufen [**Sie CoInitialize vor**](/windows/win32/api/objbase/nf-objbase-coinitialize) der Nachrichtenschleife auf, um die COM-Bibliothek zu initialisieren, und [**CoUninitialize,**](/windows/win32/api/combaseapi/nf-combaseapi-couninitialize) nachdem die Nachrichtenschleife beendet wurde. Beginnen Sie mit dem folgenden Minimalfensterprozedur:


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



Wenn Sie einen Posterrahmen aus der Media Detector abrufen, wird ein Puffer zurückgegeben, der eine [**BITMAPINFOHEADER-Struktur**](/windows/win32/api/wingdi/ns-wingdi-bitmapinfoheader) gefolgt von den Bildbits enthält. Definieren Sie daher zwei statische Variablen in der Fensterprozedur: *pbmi* enthält einen Zeiger auf die **BITMAPINFOHEADER-Struktur,** und *pBuffer* enthält einen Zeiger auf die Bitmap. Die Anwendung ordnet den Puffer in *pbmi* mit zu, sodass der Puffer gelöscht werden `new` muss, bevor das Fenster zerstört wird. Der *pBuffer-Zeiger* wird als Offset von *pbmi* berechnet, sodass er nicht gelöscht werden muss.

Weiter: [Schritt 2: Hinzufügen eines Menübefehls zum Greifen eines Posterrahmens](step-2--add-a-menu-command-to-grab-a-poster-frame.md)

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Greifen eines Posterrahmens](grabbing-a-poster-frame.md)
</dt> </dl>

 

 
