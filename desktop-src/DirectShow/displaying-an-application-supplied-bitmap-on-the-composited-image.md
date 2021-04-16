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
# <a name="display-an-app-supplied-bitmap-on-the-composited-image"></a><span data-ttu-id="41700-103">Anzeigen einer von der APP bereitgestellten Bitmap auf dem zusammengesetzten Image</span><span class="sxs-lookup"><span data-stu-id="41700-103">Display an app-supplied bitmap on the composited image</span></span>

<span data-ttu-id="41700-104">Anwendungen können den Mischungs Modus von VMR verwenden, um Alpha gemischte channellogos, eine Benutzeroberfläche oder Ankündigungen entweder teilweise oder vollständig innerhalb des Video Rechtecks anzuzeigen.</span><span class="sxs-lookup"><span data-stu-id="41700-104">Applications can use the VMR's mixing mode to display alpha-blended channel logos, a user interface, or advertisements either partially or completely within the video rectangle.</span></span> <span data-ttu-id="41700-105">Da die Mischung in Hardware durch den Grafikprozessor erfolgt, wirkt sich dies nur minimal auf die Wiedergabe Leistung des Videostreams aus, und es gibt keine erkennbaren Flimmern oder zerreißen von Artefakten.</span><span class="sxs-lookup"><span data-stu-id="41700-105">Because the blending is performed in hardware by the graphics processor, there is minimal impact to the playback performance of the Video Stream, and there are no detectable flicker or tearing artifacts.</span></span> <span data-ttu-id="41700-106">Anwendungen können das Abbild so oft wie gewünscht ändern.</span><span class="sxs-lookup"><span data-stu-id="41700-106">Applications can change the image displayed as frequently as they wish.</span></span> <span data-ttu-id="41700-107">Beachten Sie, dass Änderungen nur auf dem Bildschirm angezeigt werden, wenn sich das DirectShow-Filter Diagramm im Status wird ausgeführt befindet.</span><span class="sxs-lookup"><span data-stu-id="41700-107">It should be noted that changes are only reflected on the screen when the DirectShow filter graph is in the running state.</span></span>

<span data-ttu-id="41700-108">Der VMR verwendet seine Mischungs Komponente, um die Bitmap auf dem zusammengesetzten Bild zu überlagern.</span><span class="sxs-lookup"><span data-stu-id="41700-108">The VMR uses its mixer component to overlay the bitmap onto the composited image.</span></span> <span data-ttu-id="41700-109">Mit VMR-7 muss die Anwendung erzwingen, dass die VMR ihren Mixer lädt, auch wenn nur ein einzelner Videostream vorhanden ist.</span><span class="sxs-lookup"><span data-stu-id="41700-109">With the VMR-7, the application must force the VMR to load its mixer, even if there is only a single video stream.</span></span> <span data-ttu-id="41700-110">Dies ist bei VMR-9 nicht erforderlich, da der zugehörige Mixer standardmäßig geladen wird.</span><span class="sxs-lookup"><span data-stu-id="41700-110">This is not necessary with the VMR-9 since it loads its mixer by default.</span></span>

<span data-ttu-id="41700-111">Um ein statisches Bitmap-Bild mit dem Videostream zu mischen, erstellt die Anwendung den VMR und fügt Sie dem Diagramm hinzu. Anschließend wird [**ivmrfilterconfig:: setnumofstreams**](/windows/desktop/api/Strmif/nf-strmif-ivmrfilterconfig-setnumberofstreams)aufgerufen.</span><span class="sxs-lookup"><span data-stu-id="41700-111">To blend a static bitmap image with the video stream, the application creates the VMR and adds it to the graph, and then calls [**IVMRFilterConfig::SetNumberOfStreams**](/windows/desktop/api/Strmif/nf-strmif-ivmrfilterconfig-setnumberofstreams).</span></span> <span data-ttu-id="41700-112">Der an diese Funktion über gegebene Wert identifiziert die Anzahl der Eingabe Pins, die der VMR erstellen sollte.</span><span class="sxs-lookup"><span data-stu-id="41700-112">The value passed to this function identifies the number of input pins that the VMR should create.</span></span> <span data-ttu-id="41700-113">Anwendungen können einen beliebigen Wert zwischen 1 und Max \_ - \_ mischungsstreams angeben. die Angabe des Werts 1 ist gültig, wenn die Anwendung nur einen einzigen Videostream anzeigen soll.</span><span class="sxs-lookup"><span data-stu-id="41700-113">Applications can specify any value between 1 and MAX\_MIXER\_STREAMS; specifying a value of 1 is valid if the application only intends to display a single video stream.</span></span> <span data-ttu-id="41700-114">Obwohl VMR-7 standardmäßig über eine einzelne Eingabe-PIN verfügt, muss diese Methode aufgerufen werden, um zu erzwingen, dass Sie Ihre Mischungs Komponente lädt.</span><span class="sxs-lookup"><span data-stu-id="41700-114">Even though the VMR-7 has a single input pin by default, this method must be called in order to force it to load its mixer component.</span></span> <span data-ttu-id="41700-115">(VMR-9 lädt seinen Mixer und richtet standardmäßig vier Pins ein.)</span><span class="sxs-lookup"><span data-stu-id="41700-115">(The VMR-9 loads its mixer and sets up four pins by default.)</span></span>

<span data-ttu-id="41700-116">Verwenden Sie zum Festlegen der Bitmap die [**ivmrmixerbitmap**](/windows/desktop/api/Strmif/nn-strmif-ivmrmixerbitmap) -Schnittstelle auf der VMR-7-oder [**IVMRMixerBitmap9**](/previous-versions/windows/desktop/api/Vmr9/nn-vmr9-ivmrmixerbitmap9) -Schnittstelle für VMR-9.</span><span class="sxs-lookup"><span data-stu-id="41700-116">To set the bitmap, use the [**IVMRMixerBitmap**](/windows/desktop/api/Strmif/nn-strmif-ivmrmixerbitmap) interface on the VMR-7 or the [**IVMRMixerBitmap9**](/previous-versions/windows/desktop/api/Vmr9/nn-vmr9-ivmrmixerbitmap9) interface on the VMR-9.</span></span>

<span data-ttu-id="41700-117">Die Bitmap kann entweder durch ein Handle für einen GDI-Gerätekontext (HDC) oder durch eine DirectDraw-Oberflächen Schnittstelle angegeben werden.</span><span class="sxs-lookup"><span data-stu-id="41700-117">The bitmap can be specified by either a handle to a GDI Device Context (hDC) or by a DirectDraw Surface interface.</span></span> <span data-ttu-id="41700-118">Wenn das Bild in der Anwendung eingebettete Alpha Informationen (auch als pro Pixel Alpha bezeichnet) enthalten soll, muss es die Bilddaten in eine DirectDraw-Oberflächen Schnittstelle platzieren.</span><span class="sxs-lookup"><span data-stu-id="41700-118">If the application wants the image to contain embedded alpha information (also known as per pixel alpha) it must place the image data in a DirectDraw Surface interface.</span></span> <span data-ttu-id="41700-119">Dies liegt daran, dass es derzeit nicht möglich ist, Pixel bezogene Alpha Informationen mit einem GDI-Gerätekontext zu platzieren.</span><span class="sxs-lookup"><span data-stu-id="41700-119">This is because it is not currently possible to place per-pixel alpha information with a GDI Device Context.</span></span> <span data-ttu-id="41700-120">Die DirectDraw-Oberfläche muss entweder "RGB32" oder "ARGB32" lauten und sollte vorzugsweise eine Systemspeicher Oberfläche darstellen.</span><span class="sxs-lookup"><span data-stu-id="41700-120">The DirectDraw surface must be either RGB32 or ARGB32, and should preferably be a system memory surface.</span></span> <span data-ttu-id="41700-121">Es ist nicht erforderlich, dass die Oberflächen Dimensionen eine Potenz von 2 sein.</span><span class="sxs-lookup"><span data-stu-id="41700-121">It is not necessary for the surface dimensions to be a power of 2.</span></span>

<span data-ttu-id="41700-122">Mit VMR können Anwendungen den Speicherort und einen allgemeinen Transparenz Wert für das Image angeben.</span><span class="sxs-lookup"><span data-stu-id="41700-122">The VMR allows applications to specify the location and an overall transparency value for the image.</span></span> <span data-ttu-id="41700-123">Der folgende Code zeigt, wie Bilddaten für nachfolgende Blending an den VMR übergeben werden:</span><span class="sxs-lookup"><span data-stu-id="41700-123">The following code shows how to pass image data down to the VMR for subsequent blending:</span></span>


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



<span data-ttu-id="41700-124">Die in diesem Thema erläuterten Konzepte werden in der Beispielanwendung [vmrplayer](vmrplayer-sample.md) veranschaulicht.</span><span class="sxs-lookup"><span data-stu-id="41700-124">The concepts discussed in this topic are demonstrated in the [VMRPlayer Sample](vmrplayer-sample.md) sample application.</span></span>

<span data-ttu-id="41700-125">**Erstellen einfacher Animationen mit dem Bitmap-Bild**</span><span class="sxs-lookup"><span data-stu-id="41700-125">**Creating Simple Animations with the Bitmap Image**</span></span>

<span data-ttu-id="41700-126">Zum Erstellen eines einfachen animierten Bitmap-Logos platzieren Sie alle Bitmap-Frames in einem einzelnen Bild, wie in der folgenden Abbildung dargestellt.</span><span class="sxs-lookup"><span data-stu-id="41700-126">To create a simple animated bitmap logo, put all of the bitmap "frames" into a single image, as shown in the following illustration.</span></span>

![VMR-Bildstreifen](images/vmr-image-strip.png)

<span data-ttu-id="41700-128">Wenn Sie die Bitmap anfänglich mit [**ivmrmixerbitmap:: setalphabitmap**](/windows/desktop/api/Strmif/nf-strmif-ivmrmixerbitmap-setalphabitmap)festlegen und sich die Bitmap in einem hdc befindet, legen Sie das **rsrc** -Feld der **vmralphabitmap** -Struktur fest, um die Größe der gesamten Bitmap innerhalb des HDC anzugeben.</span><span class="sxs-lookup"><span data-stu-id="41700-128">When you set the bitmap initially using [**IVMRMixerBitmap::SetAlphaBitmap**](/windows/desktop/api/Strmif/nf-strmif-ivmrmixerbitmap-setalphabitmap), if the bitmap is in an HDC, set the **rSrc** field of the **VMRALPHABITMAP** structure to specify the size of the entire bitmap within the HDC.</span></span> <span data-ttu-id="41700-129">Die **oberen** und **linken** Elemente der-Struktur werden auf 0 festgelegt, und die **Rechte** und **unteren** Elemente sind Breite und Höhe der Bitmap.</span><span class="sxs-lookup"><span data-stu-id="41700-129">The **top** and **left** members of the structure are set to 0, and the **right** and **bottom** members are the width and height of the bitmap.</span></span> <span data-ttu-id="41700-130">Wenn sich die Bitmap in einer DirectDraw-Oberfläche befindet, ist die Größe der Oberfläche bekannt, daher ist es nicht erforderlich, rsrc in dieser Methode anzugeben.</span><span class="sxs-lookup"><span data-stu-id="41700-130">If the bitmap is in a DirectDraw surface, then the size of the surface is known, so there is no need to specify rSrc in this method.</span></span>

<span data-ttu-id="41700-131">Wenn Sie [**ivmrmixerbitmap:: updatealphabitmapparameters**](/windows/desktop/api/Strmif/nf-strmif-ivmrmixerbitmap-updatealphabitmapparameters)aufrufen, verwenden Sie den **rsrc** -Member sowohl für HDC-als auch für DirectDraw-Bitmaps, um den jeweiligen Frame oder das gewünschte Rechteck innerhalb des Bilds anzugeben, das Sie anzeigen möchten, und legen Sie das **vmrbitmap-Flag \_ srcRect** im **dwFlags** -Member fest</span><span class="sxs-lookup"><span data-stu-id="41700-131">When you call [**IVMRMixerBitmap::UpdateAlphaBitmapParameters**](/windows/desktop/api/Strmif/nf-strmif-ivmrmixerbitmap-updatealphabitmapparameters), use the **rSrc** member for both HDC and DirectDraw bitmaps, to specify the particular frame or rectangle within the image that you wish to display, and set the **VMRBITMAP\_SRCRECT** flag in the **dwFlags** member.</span></span>

## <a name="related-topics"></a><span data-ttu-id="41700-132">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="41700-132">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="41700-133">Verwenden des VMR-Mischungs Modus</span><span class="sxs-lookup"><span data-stu-id="41700-133">Using VMR Mixing Mode</span></span>](using-vmr-mixing-mode.md)
</dt> </dl>

 

 



