---
title: Flip model, dirty rectangles, scrolled areas (Flip-Modell, dirty rectangles, scrolled areas)
description: DXGI 1.2 unterstützt eine neue Flip-Model-Swapkette, geänderte Rechtecke und scrollende Bereiche. Wir erläutern die Vorteile der Verwendung der neuen Flip-Model-Swapkette und der Optimierung der Darstellung durch Angabe von geänderten Rechtecke und scrollenden Bereichen.
ms.assetid: 22236FBD-E881-49B5-8AE9-96FB526DFEF8
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 12f191af4a94b1379e2539b8d544163467fe4dc49141f244e8dcc1f13a3e36af
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119984227"
---
# <a name="flip-model-dirty-rectangles-scrolled-areas"></a>Flip model, dirty rectangles, scrolled areas (Flip-Modell, dirty rectangles, scrolled areas)

DXGI 1.2 unterstützt eine neue Flip-Model-Swapkette, geänderte Rechtecke und scrollende Bereiche. Wir erläutern die Vorteile der Verwendung der neuen Flip-Model-Swapkette und der Optimierung der Darstellung durch Angabe von geänderten Rechtecke und scrollenden Bereichen.

## <a name="dxgi-flip-model-presentation"></a>DXGI– Flip-Model-Präsentation

DXGI 1.2 fügt Unterstützung für das Flip-Präsentationsmodell für Direct3D 10 und höhere APIs hinzu. In Windows 7 hat Direct3D 9EX erstmals die Präsentation des [Flip-Modells](../direct3darticles/direct3d-9ex-improvements.md) übernommen, um zu vermeiden, dass der Swapkettenpuffer unnötig kopiert wird. Bei Verwendung des Flip-Modells werden Hintergrundpuffer zwischen der Laufzeit und Desktopfenster-Manager (DWM) gekippt, sodass DWM immer direkt aus dem Hintergrundpuffer erstellt wird, anstatt den Inhalt des Hintergrundpuffers zu kopieren.

DXGI 1.2-APIs enthalten eine überarbeitete DXGI-Swap-Chain-Schnittstelle, [**IDXGISwapChain1.**](/windows/desktop/api/DXGI1_2/nn-dxgi1_2-idxgiswapchain1) Sie können mehrere [**IDXGIFactory2-Schnittstellenmethoden**](/windows/desktop/api/DXGI1_2/nn-dxgi1_2-idxgifactory2) verwenden, um das entsprechende **IDXGISwapChain1-Objekt** zu erstellen, das mit einem [**HWND-Handle,**](../winprog/windows-data-types.md) einem [CoreWindow-Objekt,](/uwp/api/Windows.UI.Core.CoreWindow?view=winrt-19041) [DirectComposition](../directcomp/directcomposition-portal.md)oder dem Windows verwendet werden [**soll. Benutzeroberfläche. Xaml-Framework.**](/uwp/api/Windows.UI.Xaml?view=winrt-19041)

Sie wählen das Flip-Präsentationsmodell aus, indem Sie den [**DXGI \_ SWAP EFFECT \_ FLIP \_ \_ SEQUENTIAL-Enumerationswert**](/windows/desktop/api/DXGI/ne-dxgi-dxgi_swap_effect) im **SwapEffect-Member** der [**DXGI SWAP CHAIN \_ \_ \_ DESC1-Struktur**](/windows/desktop/api/DXGI1_2/ns-dxgi1_2-dxgi_swap_chain_desc1) angeben und indem Sie den **BufferCount-Member** von **DXGI SWAP CHAIN \_ \_ \_ DESC1** auf mindestens 2 festlegen. Weitere Informationen zur Verwendung des DXGI-Flip-Modells finden Sie unter [DXGI-Flipmodell.](dxgi-flip-model.md) Aufgrund der reibungsloseren Darstellung des Flip-Präsentationsmodells und anderer neuer Funktionen empfiehlt es sich, das Flip-Präsentationsmodell für alle neuen Apps zu verwenden, die Sie mit Direct3D 10 und höher-APIs schreiben.

## <a name="using-dirty-rectangles-and-the-scroll-rectangle-in-swap-chain-presentation"></a>Verwenden von geänderten Rechtecke und des Scrollrechtecks in der Swap chain-Darstellung

Durch die Verwendung von geänderten Rechtecke und dem Scrollrechteck in der Swap chain-Darstellung sparen Sie die Nutzung der Speicherbandbreite und die damit verbundene Nutzung der Systemleistung, da die Menge der Pixeldaten, die das Betriebssystem zum Zeichnen des nächsten dargestellten Frames benötigt, reduziert wird, wenn das Betriebssystem nicht den gesamten Frame zeichnen muss. Bei Apps, die häufig über Remotedesktopverbindung und andere Remotezugriffstechnologien angezeigt werden, sind die Einsparungen bei der Anzeigequalität besonders deutlich, da diese Technologien geänderte Rechtecke und Scrollmetadaten verwenden.

Sie können scrollen nur mit DXGI-Swapketten verwenden, die im Flip-Präsentationsmodell ausgeführt werden. Sie können geänderte Rechtecke mit DXGI-Swapketten verwenden, die sowohl im Flip-Modell als auch im Bitblt-Modell ausgeführt werden (mit [**DXGI \_ SWAP EFFECT \_ \_ SEQUENTIAL**](/windows/desktop/api/DXGI/ne-dxgi-dxgi_swap_effect)festgelegt).

In diesem Szenario und in dieser Abbildung zeigen wir die Funktionalität der Verwendung von geänderten Rechtecke und Scrollen. Hier enthält eine bildlauffähige App Text und animierendes Video. Die App verwendet geänderte Rechtecke, um nur das animierende Video und die neue Zeile für das Fenster zu aktualisieren, anstatt das gesamte Fenster zu aktualisieren. Das Scrollrechteck ermöglicht dem Betriebssystem, den zuvor gerenderten Inhalt auf dem neuen Frame zu kopieren und zu übersetzen und nur die neue Zeile auf dem neuen Frame zu rendern.

Die App führt eine Präsentation durch, indem sie die [**IDXGISwapChain1::P resent1-Methode aufruft.**](/windows/desktop/api/DXGI1_2/nf-dxgi1_2-idxgiswapchain1-present1) In diesem Aufruf übergibt die App einen Zeiger auf eine [**DXGI \_ PRESENT \_ PARAMETERS-Struktur,**](/windows/desktop/api/DXGI1_2/ns-dxgi1_2-dxgi_present_parameters) die geänderte Rechtecke und die Anzahl der geänderten Rechtecke, das Scrollrechteck und den zugeordneten Scrolloffset oder beide geänderten Rechtecke und das Scrollrechteck enthält. Unsere App übergibt zwei geänderte Rechtecke und das Scrollrechteck. Das Scrollrechteck ist der Bereich des vorherigen Frames, den das Betriebssystem in den aktuellen Frame kopieren muss, bevor der aktuelle Frame gerendert wird. Die App gibt das animierende Video und die neue Zeile als geänderte Rechtecke an, und das Betriebssystem rendert sie im aktuellen Frame.

![Abbildung der Überlappung von Scrollen und geänderten Rechtecke](images/dxgipresentparam.png)

``` syntax
DirtyRectsCount = 2
pDirtyRects[ 0 ] = { 10, 30, 40, 50 } // Video
pDirtyRects[ 1 ] = { 0, 70, 50, 80 } // New line
*pScrollRect = { 0, 0, 50, 70 }
*pScrollOffset = { 0, -10 }
```

Das gestrichelte Rechteck zeigt das Scrollrechteck im aktuellen Frame an. Das Scrollrechteck wird durch den **pScrollRect-Member** von [**DXGI \_ PRESENT \_ PARAMETERS**](/windows/desktop/api/DXGI1_2/ns-dxgi1_2-dxgi_present_parameters)angegeben. Der Pfeil zeigt den Bildlaufoffset an. Der Bildlaufoffset wird vom **pScrollOffset-Member** von **DXGI \_ PRESENT \_ PARAMETERS** angegeben. Gefüllte Rechtecke zeigen geänderte Rechtecke an, die die App mit neuem Inhalt aktualisiert hat. Die ausgefüllten Rechtecke werden von den **DirtyRectsCount-** und **pDirtyRects-Membern** von **DXGI \_ PRESENT \_ PARAMETERS** angegeben.

### <a name="sample-2-buffer-flip-model-swap-chain-with-dirty-rectangles-and-scroll-rectangle"></a>Beispiel für eine 2-Puffer-Swap-Model-Swapkette mit geänderten Rechtecke und Scrollrechteck

Die nächste Abbildung und Sequenz zeigt ein Beispiel für einen DXGI-Flip-Model-Präsentationsvorgang, der geänderte Rechtecke und ein Scrollrechteck verwendet. In diesem Beispiel verwenden wir die Mindestanzahl von Puffern für die Flip-Model-Darstellung. Dabei handelt es sich um eine Pufferanzahl von zwei Puffern, einen Frontpuffer, der den App-Anzeigeinhalt enthält, und einen Hintergrundpuffer, der den aktuellen Frame enthält, den die App rendern möchte.

1.  Wie im Frontpuffer am Anfang des Frames gezeigt, zeigt die scrollbare App zunächst einen Frame mit Text und animierendem Video an.
2.  Um den nächsten Frame zu rendern, rendert die App auf dem Hintergrundpuffer die geänderten Rechtecke, die das animierende Video und die neue Zeile für das Fenster aktualisieren.
3.  Wenn die App [**IDXGISwapChain1::P resent1 aufruft,**](/windows/desktop/api/DXGI1_2/nf-dxgi1_2-idxgiswapchain1-present1)gibt sie die geänderten Rechtecke sowie das Scrollrechteck und den Offset an. Die Runtime kopiert als Nächstes das Scrollrechteck aus dem vorherigen Frame abzüglich der aktualisierten geänderten Rechtecke in den aktuellen Hintergrundpuffer.
4.  Die Laufzeit tauscht schließlich die Front- und Back-Puffer aus.

![Beispiel für den Austausch von Flip-Model-Verkettungen mit Scrollen und geänderten Rechtecke](images/2-buffer-flip-model-swap-chain.png)

### <a name="tracking-dirty-rectangles-and-scroll-rectangles-across-multiple-frames"></a>Nachverfolgen von geänderten Rechtecke und Scrollrechtecke über mehrere Frames hinweg

Wenn Sie dirty rectangles in Ihrer App verwenden, müssen Sie die geänderten Rechtecke nachverfolgen, um inkrementelles Rendering zu unterstützen. Wenn Ihre App [**IDXGISwapChain1::P resent1**](/windows/desktop/api/DXGI1_2/nf-dxgi1_2-idxgiswapchain1-present1) mit geänderten Rechtecke aufruft, müssen Sie sicherstellen, dass jedes Pixel innerhalb der geänderten Rechtecke auf dem neuesten Stand ist. Wenn Sie den gesamten Bereich des geänderten Rechtecks nicht vollständig neu rendern oder für bestimmte Bereiche, die ausgelagert sind, nicht wissen können, müssen Sie einige Daten aus dem vorherigen vollständig zusammenhängenden Hintergrundpuffer in den aktuellen, veralteten Hintergrundpuffer kopieren, bevor Sie mit dem Rendern beginnen.

Die Runtime kopiert nur die Unterschiede zwischen aktualisierten Bereichen des vorherigen Frames und aktualisierten Bereichen des aktuellen Frames in den aktuellen Hintergrundpuffer. Wenn sich diese Bereiche überschneiden, kopiert die Laufzeit nur den Unterschied zwischen ihnen. Wie Sie im folgenden Diagramm und in der folgenden Sequenz sehen können, müssen Sie die Schnittmenge zwischen dem geänderten Rechteck aus Frame 1 und dem geänderten Rechteck aus Frame 2 in das geänderte Rechteck von Frame 2 kopieren.

1.  Darstellung des geänderten Rechtecks in Frame 1.
2.  Kopieren Sie die Schnittmenge zwischen dem geänderten Rechteck aus Frame 1 und dem geänderten Rechteck aus Frame 2 in das geänderte Rechteck von Frame 2.
3.  Stellen Sie ein geändertes Rechteck in Frame 2 dar.

![Nachverfolgen von Scrollen und geänderten Rechtecke über mehrere Frames hinweg](images/track-dirty-rects-scroll-rects.png)

Um für eine Swapkette mit N Puffern den Bereich zu generalisieren, der von der Laufzeit vom letzten Frame in den aktuellen Frame auf dem aktuellen Frame kopiert wird, lautet der folgende:

![Gleichung zum Berechnen des Von der Laufzeit kopierten Bereichs](images/runtime-copy-equation.png)

wobei buffer den Pufferindex in einer Swapkette angibt, beginnend mit dem aktuellen Pufferindex bei 0 (null).

Sie können alle Schnittmengen zwischen dem vorherigen Frame und den geänderten Rechtecke des aktuellen Frames nachverfolgen, indem Sie eine Kopie der geänderten Rechtecke des vorherigen Frames beibehalten oder die geänderten Rechtecke des neuen Frames mit dem entsprechenden Inhalt aus dem vorherigen Frame neu rendern.

Ebenso müssen Sie in Fällen, in denen die Swapkette über mehr als zwei Hintergrundpuffer verfügt, sicherstellen, dass überlappende Bereiche zwischen den geänderten Rechtecke des aktuellen Puffers und den geänderten Rechtecke aller vorherigen Frames kopiert oder erneut gerendert werden.

### <a name="tracking-a-single-intersection-between-2-dirty-rectangles"></a>Nachverfolgen einer einzelnen Schnittmenge zwischen zwei geänderten Rechtecke

Im einfachsten Fall können sich die geänderten Rechtecke über zwei Frames überschneiden, wenn Sie ein einzelnes geändertes Rechteck pro Frame aktualisieren. Um herauszufinden, ob sich das geänderte Rechteck des vorherigen Frames und das geänderte Rechteck des aktuellen Rahmens überschneiden, müssen Sie überprüfen, ob sich das geänderte Rechteck des vorherigen Frames mit dem geänderten Rechteck des aktuellen Rahmens überschneidet. Sie können die GDI [**IntersectRect-Funktion**](/windows/win32/api/winuser/nf-winuser-intersectrect) aufrufen, um zu bestimmen, ob sich zwei [**RECT-Strukturen**](/previous-versions//dd162897(v=vs.85)) überschneiden, die die beiden geänderten Rechtecke darstellen.

In diesem Codeausschnitt gibt ein Aufruf von [**IntersectRect**](/windows/win32/api/winuser/nf-winuser-intersectrect) die Schnittmenge von zwei geänderten Rechtecke in einem anderen [**RECT**](/previous-versions//dd162897(v=vs.85)) mit dem Namen dirtyRectCopy zurück. Nachdem der Codeausschnitt ermittelt hat, dass sich die beiden geänderten Rechtecke überschneiden, ruft er die [**ID3D11DeviceContext1::CopySubresourceRegion1-Methode**](/windows/win32/api/d3d11_1/nf-d3d11_1-id3d11devicecontext1-copysubresourceregion1) auf, um den Schnittpunktbereich in den aktuellen Frame zu kopieren.

```
RECT dirtyRectPrev, dirtyRectCurrent, dirtyRectCopy;
 
if (IntersectRect( &dirtyRectCopy, &dirtyRectPrev, &dirtyRectCurrent ))
{
       D3D11_BOX intersectBox;
       intersectBox.left    = dirtyRectCopy.left;
       intersectBox.top     = dirtyRectCopy.top;
       intersectBox.front   = 0;
       intersectBox.right   = dirtyRectCopy.right;
       intersectBox.bottom  = dirtyRectCopy.bottom;
       intersectBox.back    = 1;
 
       d3dContext->CopySubresourceRegion1(pBackbuffer,
                                    0,
                                    0,
                                    0,
                                    0,
                                    pPrevBackbuffer,
                                    0,
                                    &intersectBox,
                                    0
                                    );
}

// Render additional content to the current pBackbuffer and call Present1.
```

Wenn Sie diesen Codeausschnitt in Ihrer Anwendung verwenden, kann die App [**IDXGISwapChain1::P resent1**](/windows/desktop/api/DXGI1_2/nf-dxgi1_2-idxgiswapchain1-present1) aufrufen, um den aktuellen Frame mit dem aktuellen geänderten Rechteck zu aktualisieren.

### <a name="tracking-intersections-between-n-dirty-rectangles"></a>Nachverfolgen von Schnittmengen zwischen N geänderten Rechtecke

Wenn Sie mehrere geänderte Rechtecke angeben, die ein geändertes Rechteck für die neu angezeigte Scrolllinie pro Frame enthalten können, müssen Sie alle Überlappungen überprüfen und nachverfolgen, die zwischen allen geänderten Rechtecke des vorherigen Frames und allen geänderten Rechtecke des aktuellen Frames auftreten können. Um die Schnittmengen zwischen den geänderten Rechtecke des vorherigen Rahmens und den geänderten Rechtecke des aktuellen Frames zu berechnen, können Sie die geänderten Rechtecke in Bereiche gruppieren.

In diesem Codeausschnitt rufen wir die GDI [**SetRectRgn-Funktion**](/windows/win32/api/wingdi/nf-wingdi-setrectrgn) auf, um jedes geänderte Rechteck in einen rechteckigen Bereich zu konvertieren, und dann rufen wir die GDI [**CombineRgn-Funktion**](/windows/win32/api/wingdi/nf-wingdi-combinergn) auf, um alle geänderten rechteckigen Bereiche in einer Gruppe zu kombinieren.

```
HRGN hDirtyRgnPrev, hDirtyRgnCurrent, hRectRgn; // Handles to regions 
// Save all the dirty rectangles from the previous frame.
 
RECT dirtyRect[N]; // N is the number of dirty rectangles in current frame, which includes newly scrolled area.
 
int iReturn;
SetRectRgn(hDirtyRgnCurrent, 
       dirtyRect[0].left, 
       dirtyRect[0].top, 
       dirtyRect[0].right, 
       dirtyRect[0].bottom 
       );

for (int i = 1; i<N; i++)
{
   SetRectRgn(hRectRgn, 
          dirtyRect[0].left, 
          dirtyRect[0].top, 
          dirtyRect[0].right, 
          dirtyRect[0].bottom 
          );

   iReturn = CombineRgn(hDirtyRgnCurrent,
                        hDirtyRgnCurrent,
                        hRectRgn,
                        RGN_OR
                        );
   // Handle the error that CombineRgn returns for iReturn.
}
```

Sie können jetzt die GDI [**CombineRgn-Funktion**](/windows/win32/api/wingdi/nf-wingdi-combinergn) verwenden, um die Schnittmenge zwischen dem geänderten Bereich des vorherigen Frames und dem geänderten Bereich des aktuellen Frames zu bestimmen. Nachdem Sie den schnittenden Bereich erhalten haben, rufen Sie die GDI [**GetRegionData-Funktion**](/windows/win32/api/wingdi/nf-wingdi-getregiondata) auf, um jedes einzelne Rechteck aus dem sich überschneidenden Bereich abzurufen, und rufen Sie dann die [**ID3D11DeviceContext1::CopySubresourceRegion1-Methode**](/windows/win32/api/d3d11_1/nf-d3d11_1-id3d11devicecontext1-copysubresourceregion1) auf, um jedes sich überschneidende Rechteck in den aktuellen Hintergrundpuffer zu kopieren. Der nächste Codeausschnitt zeigt, wie diese GDI- und Direct3D-Funktionen verwendet werden.

```
HRGN hIntersectRgn;
bool bRegionsIntersect;
iReturn = CombineRgn(hIntersectRgn, hDirtyRgnCurrent, hDirtyRgnPrev, RGN_AND);
if (iReturn == ERROR)
{
       // Handle error.
}
else if(iReturn == NULLREGION)
{
       bRegionsIntersect = false;
}
else
{
       bRegionsIntersect = true;
}
 
if (bRegionsIntersect)
{
       int rgnDataSize = GetRegionData(hIntersectRgn, 0, NULL);
       if (rgnDataSize)
       {
              char pMem[] = new char[size];
              RGNDATA* pRgnData = reinterpret_cast<RGNDATA*>(pMem);
              iReturn = GetRegionData(hIntersectRgn, rgnDataSize, pRgnData);
              // Handle iReturn failure.
 
              for (int rectcount = 0; rectcount < pRgnData->rdh.nCount; ++r)
              {
                     const RECT* pIntersectRect = reinterpret_cast<RECT*>(pRgnData->Buffer) +                                            
                                                  rectcount;                
                     D3D11_BOX intersectBox;
                     intersectBox.left    = pIntersectRect->left;
                     intersectBox.top     = pIntersectRect->top;
                     intersectBox.front   = 0;
                     intersectBox.right   = pIntersectRect->right;
                     intersectBox.bottom  = pIntersectRect->bottom;
                     intersectBox.back    = 1;
 
                     d3dContext->CopySubresourceRegion1(pBackbuffer,
                                                      0,
                                                      0,
                                                      0,
                                                      0,
                                                      pPrevBackbuffer,
                                                      0,
                                                      &intersectBox,
                                                      0
                                                      );
              }

              delete [] pMem;
       }
}
```

### <a name="bitblt-model-swap-chain-with-dirty-rectangles"></a>Bitblt-Modellaustauschkette mit geänderten Rechtecke

Sie können geänderte Rechtecke mit DXGI-Swapketten verwenden, die im Bitblt-Modell ausgeführt werden (mit [**DXGI \_ SWAP EFFECT \_ \_ SEQUENTIAL**](/windows/desktop/api/DXGI/ne-dxgi-dxgi_swap_effect)festgelegt). Bitblt-Modellaustauschketten, die mehr als einen Puffer verwenden, müssen auch überlappende geänderte Rechtecke über Frames hinweg auf die gleiche Weise nachverfolgen, wie unter [Nachverfolgen von geänderten Rechtecke und Scrollrechtecke über mehrere Frames](#tracking-dirty-rectangles-and-scroll-rectangles-across-multiple-frames) für Austauschketten des Flipmodells beschrieben. Bitblt-Modellaustauschketten mit nur einem Puffer müssen keine überlappenden geänderten Rechtecke nachverfolgen, da der gesamte Puffer in jedem Frame neu gezeichnet wird.

## <a name="related-topics"></a>Zugehörige Themen

[DXGI 1.2-Verbesserungen](dxgi-1-2-improvements.md)
