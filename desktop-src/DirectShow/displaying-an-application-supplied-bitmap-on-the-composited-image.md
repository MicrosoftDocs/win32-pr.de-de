---
title: Anzeigen einer von der App bereitgestellten Bitmap auf dem zusammengesetzten Bild
description: Anzeigen einer Application-Supplied Bitmap auf dem zusammengesetzten Bild
ms.assetid: c51329d3-e814-4ef9-aad8-a3e60f9fa2a7
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 90768cc9ba9ed3a7f53336c63b0112f297e1844ba9638799e8badf28588775eb
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118653516"
---
# <a name="display-an-app-supplied-bitmap-on-the-composited-image"></a>Anzeigen einer von der App bereitgestellten Bitmap auf dem zusammengesetzten Bild

Anwendungen können den Mischungsmodus der VMR verwenden, um Alpha-Blending-Kanallogos, eine Benutzeroberfläche oder Ankündigungen entweder teilweise oder vollständig innerhalb des Videorechtecks anzuzeigen. Da das Mischen auf Hardware vom Grafikprozessor durchgeführt wird, wirkt sich dies nur minimal auf die Wiedergabeleistung des Videostreams aus, und es gibt keine erkennbaren Flimmer- oder Löschartefakte. Anwendungen können das angezeigte Bild beliebig häufig ändern. Beachten Sie, dass Änderungen nur auf dem Bildschirm angezeigt werden, wenn sich das DirectShow-Filterdiagramm im Ausführungszustand befindet.

Die VMR verwendet ihre Mixerkomponente, um die Bitmap auf dem zusammengesetzten Image zu überlagern. Mit VMR-7 muss die Anwendung erzwingen, dass die VMR ihren Mixer lädt, auch wenn nur ein einzelner Videostream vorhanden ist. Dies ist bei VMR-9 nicht erforderlich, da der Mixer standardmäßig geladen wird.

Um ein statisches Bitmapbild mit dem Videostream zu kombinieren, erstellt die Anwendung die VMR und fügt sie dem Diagramm hinzu und ruft dann [**IVMRFilterConfig::SetNumberOfStreams**](/windows/desktop/api/Strmif/nf-strmif-ivmrfilterconfig-setnumberofstreams)auf. Der an diese Funktion übergebene Wert gibt die Anzahl der Eingabepins an, die die VMR erstellen soll. Anwendungen können einen beliebigen Wert zwischen 1 und MAX MIXER STREAMS angeben. Die \_ Angabe des \_ Werts 1 ist gültig, wenn die Anwendung nur einen einzelnen Videostream anzeigen möchte. Obwohl VMR-7 standardmäßig über einen einzelnen Eingabepin verfügt, muss diese Methode aufgerufen werden, um das Laden der Mixerkomponente zu erzwingen. (Die VMR-9 lädt ihren Mixer und richtet standardmäßig vier Pins ein.)

Um die Bitmap festzulegen, verwenden Sie die [**IVMRMixerBitmap-Schnittstelle**](/windows/desktop/api/Strmif/nn-strmif-ivmrmixerbitmap) auf der VMR-7 oder die [**IVMRMixerBitmap9-Schnittstelle**](/previous-versions/windows/desktop/api/Vmr9/nn-vmr9-ivmrmixerbitmap9) auf der VMR-9.

Die Bitmap kann entweder durch ein Handle für einen GDI-Gerätekontext (hDC) oder durch eine DirectDraw Surface-Schnittstelle angegeben werden. Wenn die Anwendung möchte, dass das Bild eingebettete Alphainformationen (auch als pro Pixel alpha bezeichnet) enthält, muss es die Bilddaten in einer DirectDraw Surface-Schnittstelle platzieren. Dies liegt daran, dass es derzeit nicht möglich ist, Alphainformationen pro Pixel mit einem GDI-Gerätekontext zu platzieren. Die DirectDraw-Oberfläche muss entweder RGB32 oder ARGB32 sein und sollte vorzugsweise eine Systemspeicheroberfläche sein. Es ist nicht erforderlich, dass die Oberflächendimensionen eine Potenz von 2 haben.

Mit der VMR können Anwendungen den Speicherort und einen Allgemeinen Transparenzwert für das Image angeben. Der folgende Code zeigt, wie Sie Imagedaten für die nachfolgende Mischung an die VMR übergeben:


```C++
HRESULT BlendApplicationImage( 
  HWND hwndApp,
  IVMRWindowlessControl* pWc,
  HBITMAP hbm
)
{
    LONG cx, cy;
    HRESULT hr;
    hr = pWc->GetNativeVideoSize(&cx, &cy, NULL, NULL);
    if (FAILED(hr))
        return hr;
    
    HDC hdc = GetDC(hwndApp);
    if (hdc == NULL)
    {
        return E_FAIL;
    }
    
    HDC hdcBmp = CreateCompatibleDC(hdc);
    ReleaseDC(hwndApp, hdc);
    
    if (hdcBmp == NULL)
    {
        return E_FAIL;
    }
    
    BITMAP bm;
    if (0 == GetObject(hbm, sizeof(bm), &bm))
    {
        DeleteDC(hdcBmp);
        return E_FAIL;
    }
    
    HBITMAP hbmOld = (HBITMAP)SelectObject(hdcBmp, hbm);
    if (hbmOld == 0)
    {
        DeleteDC(hdcBmp);
        return E_FAIL;
    }
    
    VMRALPHABITMAP bmpInfo;
    ZeroMemory(&bmpInfo, sizeof(bmpInfo) );
    bmpInfo.dwFlags = VMRBITMAP_HDC;
    bmpInfo.hdc = hdcBmp;
    
    // Show the entire bitmap in the top-left corner of the video image.
    SetRect(&bmpInfo.rSrc, 0, 0, bm.bmWidth, bm.bmHeight);
    bmpInfo.rDest.left = 0.f;
    bmpInfo.rDest.top = 0.f;
    bmpInfo.rDest.right = (float)bm.bmWidth / (float)cx;
    bmpInfo.rDest.bottom = (float)bm.bmHeight / (float)cy;
    
    // Set the transparency value (1.0 is opaque, 0.0 is transparent).
    bmpInfo.fAlpha = 0.2f;
    
    IVMRMixerBitmap* pBmp;
    hr = pWc->QueryInterface(IID_IVMRMixerBitmap, (LPVOID *)&pBmp);
    if (SUCCEEDED(hr)) 
    {
        pBmp->SetAlphaBitmap(&bmpInfo);
        pBmp->Release();
    }
    
    DeleteObject(SelectObject(hdcBmp, hbmOld));
    DeleteDC(hdcBmp);
    return hr;
}
```



Die in diesem Thema erläuterten Konzepte werden in der [BEISPIELanwendung VMRPlayer](vmrplayer-sample.md) veranschaulicht.

**Erstellen einfacher Animationen mit dem Bitmapbild**

Um ein einfaches animiertes Bitmaplogo zu erstellen, platzieren Sie alle Bitmapframes in einem einzelnen Bild, wie in der folgenden Abbildung dargestellt.

![VMR-Imagestreifen](images/vmr-image-strip.png)

Wenn Sie die Bitmap anfänglich mitHILFE von [**IVMRMixerBitmap::SetAlphaBitmap**](/windows/desktop/api/Strmif/nf-strmif-ivmrmixerbitmap-setalphabitmap)festlegen, wenn sich die Bitmap in einem HDC befindet, legen Sie das **rSrc-Feld** der **VMRALPHABITMAP-Struktur** fest, um die Größe der gesamten Bitmap innerhalb des HDC anzugeben. Die **oberen** und **linken** Elemente der -Struktur werden auf 0 festgelegt, und die **rechten** und **unteren** Member sind die Breite und Höhe der Bitmap. Wenn sich die Bitmap in einer DirectDraw-Oberfläche befindet, ist die Größe der Oberfläche bekannt, sodass es in dieser Methode nicht erforderlich ist, rSrc anzugeben.

Wenn Sie [**IVMRMixerBitmap::UpdateAlphaBitmapParameters**](/windows/desktop/api/Strmif/nf-strmif-ivmrmixerbitmap-updatealphabitmapparameters)aufrufen, verwenden Sie den **rSrc-Member** für HDC- und DirectDraw-Bitmaps, um den bestimmten Frame oder das Rechteck innerhalb des Bilds anzugeben, das Sie anzeigen möchten, und legen Sie das **VMRBITMAP \_ SRCRECT-Flag** im **dwFlags-Member** fest.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Verwenden des VMR-Gemischtmodus](using-vmr-mixing-mode.md)
</dt> </dl>

 

 



