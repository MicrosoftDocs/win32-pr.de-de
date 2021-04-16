---
title: Anzeigen einer von der APP bereitgestellten Bitmap auf dem zusammengesetzten Image
description: Anzeigen einer Application-Supplied Bitmap auf dem zusammengesetzten Image
ms.assetid: c51329d3-e814-4ef9-aad8-a3e60f9fa2a7
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 06ecd8ac931d0a0bb83eafba09d8ca7dc8263f0d
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/06/2021
ms.locfileid: "104520576"
---
# <a name="display-an-app-supplied-bitmap-on-the-composited-image"></a>Anzeigen einer von der APP bereitgestellten Bitmap auf dem zusammengesetzten Image

Anwendungen können den Mischungs Modus von VMR verwenden, um Alpha gemischte channellogos, eine Benutzeroberfläche oder Ankündigungen entweder teilweise oder vollständig innerhalb des Video Rechtecks anzuzeigen. Da die Mischung in Hardware durch den Grafikprozessor erfolgt, wirkt sich dies nur minimal auf die Wiedergabe Leistung des Videostreams aus, und es gibt keine erkennbaren Flimmern oder zerreißen von Artefakten. Anwendungen können das Abbild so oft wie gewünscht ändern. Beachten Sie, dass Änderungen nur auf dem Bildschirm angezeigt werden, wenn sich das DirectShow-Filter Diagramm im Status wird ausgeführt befindet.

Der VMR verwendet seine Mischungs Komponente, um die Bitmap auf dem zusammengesetzten Bild zu überlagern. Mit VMR-7 muss die Anwendung erzwingen, dass die VMR ihren Mixer lädt, auch wenn nur ein einzelner Videostream vorhanden ist. Dies ist bei VMR-9 nicht erforderlich, da der zugehörige Mixer standardmäßig geladen wird.

Um ein statisches Bitmap-Bild mit dem Videostream zu mischen, erstellt die Anwendung den VMR und fügt Sie dem Diagramm hinzu. Anschließend wird [**ivmrfilterconfig:: setnumofstreams**](/windows/desktop/api/Strmif/nf-strmif-ivmrfilterconfig-setnumberofstreams)aufgerufen. Der an diese Funktion über gegebene Wert identifiziert die Anzahl der Eingabe Pins, die der VMR erstellen sollte. Anwendungen können einen beliebigen Wert zwischen 1 und Max \_ - \_ mischungsstreams angeben. die Angabe des Werts 1 ist gültig, wenn die Anwendung nur einen einzigen Videostream anzeigen soll. Obwohl VMR-7 standardmäßig über eine einzelne Eingabe-PIN verfügt, muss diese Methode aufgerufen werden, um zu erzwingen, dass Sie Ihre Mischungs Komponente lädt. (VMR-9 lädt seinen Mixer und richtet standardmäßig vier Pins ein.)

Verwenden Sie zum Festlegen der Bitmap die [**ivmrmixerbitmap**](/windows/desktop/api/Strmif/nn-strmif-ivmrmixerbitmap) -Schnittstelle auf der VMR-7-oder [**IVMRMixerBitmap9**](/previous-versions/windows/desktop/api/Vmr9/nn-vmr9-ivmrmixerbitmap9) -Schnittstelle für VMR-9.

Die Bitmap kann entweder durch ein Handle für einen GDI-Gerätekontext (HDC) oder durch eine DirectDraw-Oberflächen Schnittstelle angegeben werden. Wenn das Bild in der Anwendung eingebettete Alpha Informationen (auch als pro Pixel Alpha bezeichnet) enthalten soll, muss es die Bilddaten in eine DirectDraw-Oberflächen Schnittstelle platzieren. Dies liegt daran, dass es derzeit nicht möglich ist, Pixel bezogene Alpha Informationen mit einem GDI-Gerätekontext zu platzieren. Die DirectDraw-Oberfläche muss entweder "RGB32" oder "ARGB32" lauten und sollte vorzugsweise eine Systemspeicher Oberfläche darstellen. Es ist nicht erforderlich, dass die Oberflächen Dimensionen eine Potenz von 2 sein.

Mit VMR können Anwendungen den Speicherort und einen allgemeinen Transparenz Wert für das Image angeben. Der folgende Code zeigt, wie Bilddaten für nachfolgende Blending an den VMR übergeben werden:


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



Die in diesem Thema erläuterten Konzepte werden in der Beispielanwendung [vmrplayer](vmrplayer-sample.md) veranschaulicht.

**Erstellen einfacher Animationen mit dem Bitmap-Bild**

Zum Erstellen eines einfachen animierten Bitmap-Logos platzieren Sie alle Bitmap-Frames in einem einzelnen Bild, wie in der folgenden Abbildung dargestellt.

![VMR-Bildstreifen](images/vmr-image-strip.png)

Wenn Sie die Bitmap anfänglich mit [**ivmrmixerbitmap:: setalphabitmap**](/windows/desktop/api/Strmif/nf-strmif-ivmrmixerbitmap-setalphabitmap)festlegen und sich die Bitmap in einem hdc befindet, legen Sie das **rsrc** -Feld der **vmralphabitmap** -Struktur fest, um die Größe der gesamten Bitmap innerhalb des HDC anzugeben. Die **oberen** und **linken** Elemente der-Struktur werden auf 0 festgelegt, und die **Rechte** und **unteren** Elemente sind Breite und Höhe der Bitmap. Wenn sich die Bitmap in einer DirectDraw-Oberfläche befindet, ist die Größe der Oberfläche bekannt, daher ist es nicht erforderlich, rsrc in dieser Methode anzugeben.

Wenn Sie [**ivmrmixerbitmap:: updatealphabitmapparameters**](/windows/desktop/api/Strmif/nf-strmif-ivmrmixerbitmap-updatealphabitmapparameters)aufrufen, verwenden Sie den **rsrc** -Member sowohl für HDC-als auch für DirectDraw-Bitmaps, um den jeweiligen Frame oder das gewünschte Rechteck innerhalb des Bilds anzugeben, das Sie anzeigen möchten, und legen Sie das **vmrbitmap-Flag \_ srcRect** im **dwFlags** -Member fest

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Verwenden des VMR-Mischungs Modus](using-vmr-mixing-mode.md)
</dt> </dl>

 

 



