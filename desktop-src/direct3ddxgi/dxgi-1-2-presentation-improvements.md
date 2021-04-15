---
title: Kippen von Modellen, Dirty Rechtecke, scrollt-Bereiche
description: DXGI 1,2 unterstützt eine neue Swapkette für das Flip-Modell, geänderte Rechtecke und aufgeschlüsselten Bereichen. Wir erläutern die Vorteile der Verwendung der neuen pullmodellaustauschkette und der Optimierung der Präsentation durch die Angabe von Änderungs Rechtecke und den Bereichen mit Rollup.
ms.assetid: 22236FBD-E881-49B5-8AE9-96FB526DFEF8
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1a3abbb784de82f5bf647a4b66503497edcd4f89
ms.sourcegitcommit: 5724b38883e518ac565e1b266defa85ad0941bb2
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 02/14/2021
ms.locfileid: "104570187"
---
# <a name="flip-model-dirty-rectangles-scrolled-areas"></a>Kippen von Modellen, Dirty Rechtecke, scrollt-Bereiche

DXGI 1,2 unterstützt eine neue Swapkette für das Flip-Modell, geänderte Rechtecke und aufgeschlüsselten Bereichen. Wir erläutern die Vorteile der Verwendung der neuen pullmodellaustauschkette und der Optimierung der Präsentation durch die Angabe von Änderungs Rechtecke und den Bereichen mit Rollup.

## <a name="dxgi-flip-model-presentation"></a>DXGI-Flip-Model-Präsentation

DXGI 1,2 fügt Unterstützung für das Flip Presentation Model für Direct3D 10-APIs und spätere APIs hinzu. In Windows 7 hat Direct3D 9Ex zuerst die [Flip-Model-Präsentation](../direct3darticles/direct3d-9ex-improvements.md) angenommen, um zu verhindern, dass der Austausch Ketten Puffer unnötig kopiert wird. Durch die Verwendung von Flip Model werden backpuffervorgänge zwischen der Laufzeit und der Desktopfenster-Manager (DWM) gekippt, sodass DWM immer direkt aus dem Hintergrund Puffer besteht, anstatt den Inhalt des hinterpuffers zu kopieren.

DXGI 1,2-APIs enthalten eine überarbeitete DXGI-SwapChain-Schnittstelle, [**IDXGISwapChain1**](/windows/desktop/api/DXGI1_2/nn-dxgi1_2-idxgiswapchain1). Sie können mehrere [**IDXGIFactory2**](/windows/desktop/api/DXGI1_2/nn-dxgi1_2-idxgifactory2) -Schnittstellen Methoden verwenden, um das entsprechende **IDXGISwapChain1** -Objekt für die Verwendung mit einem [**HWND**](../winprog/windows-data-types.md) -handle, einem [corewindow](/uwp/api/Windows.UI.Core.CoreWindow?view=winrt-19041) -Objekt, einer [directcomposition](../directcomp/directcomposition-portal.md)oder dem [**Windows. UI. XAML**](/uwp/api/Windows.UI.Xaml?view=winrt-19041) -Framework zu erstellen.

Wählen Sie das Modell zum Kippen der Darstellung aus, indem Sie den [**DXGI-swapffekt-Wert für die \_ \_ \_ \_ sequenzielle**](/windows/desktop/api/DXGI/ne-dxgi-dxgi_swap_effect) Enumeration im **SwapEffect** -Member der [**DXGI- \_ \_ SwapChain \_ DESC1**](/windows/desktop/api/DXGI1_2/ns-dxgi1_2-dxgi_swap_chain_desc1) -Struktur und den **BUFFERCOUNT** -Member der **DXGI- \_ Swap- \_ Kette \_ DESC1** auf mindestens 2 festlegen. Weitere Informationen zur Verwendung des DXGI-Flip-Modells finden Sie unter [DXGI Flip Model](dxgi-flip-model.md). Aufgrund der glatteren Präsentation des Flip Presentation Model und anderer neuer Funktionen empfiehlt es sich, das Modell "Flip Presentation Model" für alle neuen apps zu verwenden, die Sie mit Direct3D 10-und höher-APIs schreiben.

## <a name="using-dirty-rectangles-and-the-scroll-rectangle-in-swap-chain-presentation"></a>Verwenden von Dirty Rechtecke und des Schiebe Rechtecks bei der Präsentation der Austausch Kette

Durch die Verwendung von Dirty Rechtecke und des Bild Lauf Rechtecks in der Präsentation der Austausch Kette sparen Sie die Nutzung der Speicherbandbreite und die damit verbundene Nutzung der Systemleistung, da die Menge der Pixeldaten, die das Betriebssystem zum Zeichnen des nächsten dargestellten Frames benötigt, reduziert wird, wenn das Betriebssystem nicht den gesamten Frame zeichnen muss. Für apps, die häufig über Remotedesktopverbindung und andere Technologien für den Remote Zugriff angezeigt werden, sind die Einsparungen besonders in der Anzeigequalität erkennbar, da diese Technologien geänderte Rechtecke und Bild Lauf Metadaten verwenden.

Sie können Scroll nur mit DXGI-Swapketten verwenden, die im Flip Presentation Model ausgeführt werden. Sie können Dirty Rechtecke mit DXGI-Swapketten verwenden, die sowohl im Flip Model-als auch im BitBLT-Modell ausgeführt werden (festgelegt mit [**DXGI- \_ \_ swapffekt \_**](/windows/desktop/api/DXGI/ne-dxgi-dxgi_swap_effect)

In diesem Szenario und dieser Abbildung zeigen wir die Funktionalität der Verwendung von Änderungs Rechtecke und des Bildlaufs. Hier enthält eine Bild lauffähigen App Text und animationsvideos. Die APP verwendet Dirty Rechtecke, um nur das Animationsvideo und die neue Zeile für das Fenster zu aktualisieren, anstatt das gesamte Fenster zu aktualisieren. Mit dem scrollrechteck kann das Betriebssystem den zuvor gerenderten Inhalt in den neuen Frame kopieren und übersetzen und nur die neue Zeile im neuen Frame rendern.

Die APP führt eine Präsentation durch Aufrufen der [**IDXGISwapChain1::P resent1**](/windows/desktop/api/DXGI1_2/nf-dxgi1_2-idxgiswapchain1-present1) -Methode aus. In diesem-Befehl übergibt die APP einen Zeiger auf eine [**DXGI-Struktur der \_ vorhandenen \_ Parameter**](/windows/desktop/api/DXGI1_2/ns-dxgi1_2-dxgi_present_parameters) , die geänderte Rechtecke und die Anzahl der modifizierten Rechtecke, das Schiebe Rechteck und den zugeordneten Bild Lauf Offset oder sowohl geänderte Rechtecke als auch das Schiebe Rechteck enthält. Unsere App übergibt 2 geänderte Rechtecke und das Schiebe Rechteck. Das Schiebe Rechteck ist der Bereich des vorherigen Frames, der vom Betriebssystem in den aktuellen Frame kopiert werden muss, bevor der aktuelle Frame gerendert wird. Die APP gibt das Animationsvideo und die neue Zeile als modifizierte Rechtecke an, und das Betriebssystem rendert Sie im aktuellen Frame.

![Abbildung der überlappenden Scroll-und Dirty Rechtecke](images/dxgipresentparam.png)

``` syntax
DirtyRectsCount = 2
pDirtyRects[ 0 ] = { 10, 30, 40, 50 } // Video
pDirtyRects[ 1 ] = { 0, 70, 50, 80 } // New line
*pScrollRect = { 0, 0, 50, 70 }
*pScrollOffset = { 0, -10 }
```

Das gestrichelte Rechteck zeigt das Bild Lauf Rechteck im aktuellen Frame an. Das Bild Lauf Rechteck wird vom **pscrollrect** -Member von [**DXGI \_ Present- \_ Parametern**](/windows/desktop/api/DXGI1_2/ns-dxgi1_2-dxgi_present_parameters)angegeben. Der Pfeil zeigt den scrolloffset an. Der Bild Lauf Offset wird vom **pscrolloffset** -Member von **DXGI \_ Present- \_ Parametern** angegeben. Gefüllte Rechtecke zeigen geänderte Rechtecke an, dass die APP mit neuem Inhalt aktualisiert wurde. Die gefüllten Rechtecke werden von den **dirtyreczcount** -und **pdirtyrects** -Membern von **DXGI \_ Present- \_ Parametern** angegeben.

### <a name="sample-2-buffer-flip-model-swap-chain-with-dirty-rectangles-and-scroll-rectangle"></a>Beispiel 2: Puffer-Swap-Kette mit Änderungs Rechtecke und Schiebe Rechteck

Die nächste Abbildung und Sequenz zeigt ein Beispiel für einen DXGI Flip-Model Presentation-Vorgang, der geänderte Rechtecke und ein scrollrechteck verwendet. In diesem Beispiel verwenden wir die minimale Anzahl von Puffern für die Darstellung von Flip-Modellen, bei der es sich um eine Puffer Anzahl von zwei handelt, einen vorderen Puffer, der den Inhalt der APP anzeigt, und einen Hintergrund Puffer, der den aktuellen Frame enthält, den die APP Renderen möchte.

1.  Wie im Vorder-Puffer am Anfang des Frames gezeigt, zeigt die scrollbare App anfänglich einen Frame mit Text und animationsvideos an.
2.  Um den nächsten Frame zu rendern, rendert die APP auf dem Hintergrund Puffer die geänderten Rechtecke, die das Animationsvideo aktualisieren, und die neue Zeile für das Fenster.
3.  Wenn die APP [**IDXGISwapChain1::P resent1**](/windows/desktop/api/DXGI1_2/nf-dxgi1_2-idxgiswapchain1-present1)aufruft, werden die Änderungs Rechtecke und das Schiebe Rechteck und der Offset angegeben. Die Laufzeit kopiert das Schiebe Rechteck aus dem vorherigen Frame minus den aktualisierten, modifizierten Rechtecke auf den aktuellen Hintergrund Puffer.
4.  Die Laufzeit vertauscht schließlich die Vorder-und Hintergrund Puffer.

![Beispiel für eine Swap-Modell-SwapChain mit Scroll-und Dirty Rechtecke](images/2-buffer-flip-model-swap-chain.png)

### <a name="tracking-dirty-rectangles-and-scroll-rectangles-across-multiple-frames"></a>Nachverfolgen von Dirty Rechtecke und scrollrechtecke über mehrere Frames hinweg

Wenn Sie in Ihrer APP modifizierte Rechtecke verwenden, müssen Sie die geänderten Rechtecke nachverfolgen, um inkrementelles Rendering zu unterstützen Wenn Ihre APP [**IDXGISwapChain1::P resent1**](/windows/desktop/api/DXGI1_2/nf-dxgi1_2-idxgiswapchain1-present1) mit Dirty Rechtecke aufruft, müssen Sie sicherstellen, dass jedes Pixel innerhalb der modifizierten Rechtecke auf dem neuesten Stand ist. Wenn Sie den gesamten Bereich des Dirty-Rechtecks nicht vollständig neu rendern oder wenn Sie für bestimmte Bereiche, die sich in der Hand befinden, nicht wissen, müssen Sie einige Daten aus dem vorherigen vollständig zusammenhängenden Hintergrund Puffer in den aktuellen, veralteten Hintergrund Puffer kopieren, bevor Sie das Rendering starten.

Die Laufzeit kopiert nur die Unterschiede zwischen den aktualisierten Bereichen des vorherigen Frames und den aktualisierten Bereichen des aktuellen Frames auf den aktuellen Hintergrund Puffer. Wenn sich diese Bereiche überschneiden, kopiert die Runtime nur den Unterschied zwischen Ihnen. Wie Sie im folgenden Diagramm und in der folgenden Reihenfolge sehen können, müssen Sie die Schnittmenge zwischen dem Dirty-Rechteck von Frame 1 und dem Dirty Rechteck von Frame 2 in das Dirty-Rechteck von Frame 2 kopieren.

1.  In Frame 1 ist ein Dirty Rechteck vorhanden.
2.  Kopieren Sie die Schnittmenge zwischen dem Dirty-Rechteck von Frame 1 und dem Dirty Rechteck von Frame 2 in das geänderte Rechteck von Frame 2.
3.  Geändertes Rechteck in Frame 2 vorhanden.

![Nachverfolgen von Scroll-und Dirty Rechtecke über mehrere Frames hinweg](images/track-dirty-rects-scroll-rects.png)

Zum verallgemeinern für eine Swapkette mit N Puffern wird der Bereich, der von der Laufzeit vom letzten Frame zum aktuellen Frame auf dem aktuellen Frame kopiert wird, wie folgt dargestellt:

![Gleichung zum Berechnen des Bereichs, der von der Laufzeit kopiert wird](images/runtime-copy-equation.png)

Where Buffer gibt den Puffer Index in einer Swapkette an, beginnend mit dem aktuellen Puffer Index bei Null.

Sie können alle Schnittpunkte zwischen dem vorherigen Frame und den geänderten Rechtecke des aktuellen Frames nachverfolgen, indem Sie eine Kopie der modifizierten Rechtecke des vorherigen Frames aufbewahren oder die Änderungs Rechtecke des neuen Frames mit dem entsprechenden Inhalt aus dem vorherigen Frame neu rendern.

Entsprechend müssen Sie in den Fällen, in denen die Swapkette mehr als zwei Back-Puffer aufweist, sicherstellen, dass sich überlappende Bereiche zwischen den geänderten Rechtecke des aktuellen Puffers und den geänderten Rechtecke aller vorherigen Frames kopiert oder erneut gerendert werden.

### <a name="tracking-a-single-intersection-between-2-dirty-rectangles"></a>Nachverfolgen einer einzelnen Schnittmenge zwischen 2 modifizierten Rechtecke

Im einfachsten Fall, wenn Sie ein einzelnes Dirty Rechteck pro Frame aktualisieren, können sich die geänderten Rechtecke über zwei Frames hinweg überschneiden. Um herauszufinden, ob sich das geänderte Rechteck des vorherigen Frames und das geänderte Rechteck des aktuellen Frames überlappen, müssen Sie überprüfen, ob sich das geänderte Rechteck des vorherigen Frames mit dem modifizierten Rechteck des aktuellen Frames überschneidet. Sie können die GDI [**intersectRect**](/windows/win32/api/winuser/nf-winuser-intersectrect) -Funktion aufzurufen, um zu bestimmen, ob zwei [**Rect**](/previous-versions//dd162897(v=vs.85)) -Strukturen, die die beiden geänderten Rechtecke darstellen, sich überschneiden.

In diesem Code Ausschnitt gibt ein Aufruf von [**intersectRect**](/windows/win32/api/winuser/nf-winuser-intersectrect) die Schnittmenge zweier Dirty Rechtecke in einem anderen [**Rect**](/previous-versions//dd162897(v=vs.85)) namens dirtyrectcopy zurück. Nachdem der Code Ausschnitt feststellt, dass sich die beiden modifizierten Rechtecke überschneiden, wird die [**ID3D11DeviceContext1:: CopySubresourceRegion1**](/windows/win32/api/d3d11_1/nf-d3d11_1-id3d11devicecontext1-copysubresourceregion1) -Methode aufgerufen, um den Bereich der Schnittmenge in den aktuellen Frame zu kopieren.

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

Wenn Sie diesen Code Ausschnitt in Ihrer Anwendung verwenden, ist die APP bereit zum Abrufen von [**IDXGISwapChain1::P resent1**](/windows/desktop/api/DXGI1_2/nf-dxgi1_2-idxgiswapchain1-present1) , um den aktuellen Frame mit dem aktuellen, geänderten Rechteck zu aktualisieren.

### <a name="tracking-intersections-between-n-dirty-rectangles"></a>Nachverfolgen von Schnittpunkten zwischen N Änderungs Rechtecke

Wenn Sie mehrere modifizierte Rechtecke angeben, die ein geändertes Rechteck für die neu aufgezeigte scrolllinie pro Frame einschließen können, müssen Sie alle Überschneidungen überprüfen und nachverfolgen, die zwischen allen modifizierten Rechtecke des vorherigen Frames und allen geänderten Rechtecke des aktuellen Frames auftreten können. Um die Schnittpunkte zwischen den modifizierten Rechtecke des vorherigen Frames und den geänderten Rechtecke des aktuellen Frames zu berechnen, können Sie die geänderten Rechtecke in den Regionen gruppieren.

In diesem Code Ausschnitt wird die GDI-Funktion " [**setrectrgn**](/windows/win32/api/wingdi/nf-wingdi-setrectrgn) " aufgerufen, um jedes geänderte Rechteck in einen rechteckigen Bereich zu konvertieren. Anschließend wird die GDI [**combinergn**](/windows/win32/api/wingdi/nf-wingdi-combinergn) -Funktion aufgerufen, um alle geänderten rechteckigen Bereiche in einer Gruppe zu kombinieren.

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

Sie können jetzt die GDI [**combinergn**](/windows/win32/api/wingdi/nf-wingdi-combinergn) -Funktion verwenden, um die Schnittmenge zwischen dem geänderten Bereich des vorherigen Frames und dem geänderten Bereich des aktuellen Frames zu bestimmen. Nachdem Sie den sich überschneidenden Bereich abgerufen haben, rufen Sie die GDI [**GetRegionData**](/windows/win32/api/wingdi/nf-wingdi-getregiondata) -Funktion auf, um jedes einzelne Rechteck aus dem überschneidenden Bereich abzurufen, und rufen Sie dann die [**ID3D11DeviceContext1:: CopySubresourceRegion1**](/windows/win32/api/d3d11_1/nf-d3d11_1-id3d11devicecontext1-copysubresourceregion1) -Methode auf, um jedes überschneidende Rechteck in den aktuellen Hintergrund Puffer zu kopieren. Der nächste Code Ausschnitt zeigt, wie diese GDI-und Direct3D-Funktionen verwendet werden.

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

### <a name="bitblt-model-swap-chain-with-dirty-rectangles"></a>BitBLT-Modell Austausch Kette mit Dirty Rechtecke

Sie können Dirty Rechtecke mit DXGI-Austausch Ketten verwenden, die im BitBLT-Modell ausgeführt werden (festgelegt mit [**DXGI- \_ Swap- \_ Effekt \_ sequenziell**](/windows/desktop/api/DXGI/ne-dxgi-dxgi_swap_effect)). BitBLT-Modell Austausch Ketten, die mehr als einen Puffer verwenden, müssen überlappende geänderte Rechtecke auf die gleiche Weise nachverfolgen, wie in nach [Verfolgen von Dirty Rechtecke und Bild Lauf Rechtecke über mehrere Frames](#tracking-dirty-rectangles-and-scroll-rectangles-across-multiple-frames) für das Kippen von Modell Austausch Ketten beschrieben. BitBLT-Modell Austausch Ketten mit nur einem Puffer müssen überlappende geänderte Rechtecke nicht nachverfolgt werden, da der gesamte Puffer jedes Frame neu gezeichnet wird.

## <a name="related-topics"></a>Zugehörige Themen

[DXGI 1,2-Verbesserungen](dxgi-1-2-improvements.md)
