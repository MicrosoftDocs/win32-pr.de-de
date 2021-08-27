---
description: Dieses Thema ist Schritt 2 des Tutorials Audio-/Videowiedergabe in DirectShow.
ms.assetid: 61106781-d10c-41a8-993e-121e0a1e4c4d
title: 'Schritt 2: Deklarieren von CVideoRenderer und abgeleiteten Klassen'
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: fae4c9c391a13acd0ede06b9a74c3b09bd264a6b74c42d7f6c7ca5e9dbb17051
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "120050360"
---
# <a name="step-2-declare-cvideorenderer-and-derived-classes"></a>Schritt 2: Deklarieren von CVideoRenderer und abgeleiteten Klassen

Dieses Thema ist Schritt 2 des Tutorials [Audio-/Videowiedergabe in DirectShow](audio-video-playback-in-directshow.md). Der vollständige Code wird im Thema [DirectShow Playback Example (DirectShow-Wiedergabebeispiel)](directshow-playback-example.md)gezeigt.

DirectShow bietet mehrere verschiedene Filter zum Rendern von Videos:

-   [**Erweiterter Videorendererfilter**](enhanced-video-renderer-filter.md) (EVR)
-   [Video Mixing Renderer Filter 9](video-mixing-renderer-filter-9.md) (VMR-9)
-   [Video Mixing Renderer Filter 7](video-mixing-renderer-filter-7.md) (VMR-7)

Weitere Informationen zu den Unterschieden zwischen diesen Filtern finden Sie unter [Auswählen des richtigen Videorenderers.](choosing-the-right-renderer.md)

In diesem Tutorial wird die folgende abstrakte Klasse verwendet, um den Filter des Videorenderers zu umschließen.


```C++
// Abstract class to manage the video renderer filter.
// Specific implementations handle the VMR-7, VMR-9, or EVR filter.

class CVideoRenderer
{
public:
    virtual ~CVideoRenderer() {};
    virtual BOOL    HasVideo() const = 0;
    virtual HRESULT AddToGraph(IGraphBuilder *pGraph, HWND hwnd) = 0;
    virtual HRESULT FinalizeGraph(IGraphBuilder *pGraph) = 0;
    virtual HRESULT UpdateVideoWindow(HWND hwnd, const LPRECT prc) = 0;
    virtual HRESULT Repaint(HWND hwnd, HDC hdc) = 0;
    virtual HRESULT DisplayModeChanged() = 0;
};
```



Hinweise:

-   Die `HasVideo` -Methode gibt **TRUE** zurück, wenn der Videorenderer erstellt wurde.
-   Die `AddToGraph` -Methode fügt den Videorenderer dem Filterdiagramm hinzu.
-   Die `FinalizeGraph` -Methode schließt den Grapherstellungsschritt ab.
-   Die `UpdateVideoWindow` -Methode aktualisiert das Zielrechteck des Videos.
-   Mit der -Methode wird `Repaint` der aktuelle Videoframe neu gezeichnet.
-   Die `DisplayModeChanged` -Methode verarbeitet Änderungen im Anzeigemodus.

Jede dieser Methoden wird weiter unten in diesem Tutorial ausführlich beschrieben.

Deklarieren Sie als Nächstes eine abgeleitete Klasse, um jeden der drei Videorenderer zu umschließen: EVR, VMR-9 und VMR-7.

### <a name="cevr-class"></a>CEVR-Klasse

Die `CEVR` -Klasse verwaltet die EVR. Sie enthält einen Zeiger auf die Schnittstellen [**IBaseFilter**](/windows/desktop/api/Strmif/nn-strmif-ibasefilter) und [**POINTERVideoDisplayControl**](/windows/win32/api/evr/nn-evr-imfvideodisplaycontrol) der EVR.


```C++
// Manages the EVR video renderer filter.

class CEVR : public CVideoRenderer
{
    IBaseFilter            *m_pEVR;
    IMFVideoDisplayControl *m_pVideoDisplay;

public:
    CEVR();
    ~CEVR();
    BOOL    HasVideo() const;
    HRESULT AddToGraph(IGraphBuilder *pGraph, HWND hwnd);
    HRESULT FinalizeGraph(IGraphBuilder *pGraph);
    HRESULT UpdateVideoWindow(HWND hwnd, const LPRECT prc);
    HRESULT Repaint(HWND hwnd, HDC hdc);
    HRESULT DisplayModeChanged();
};
```



### <a name="cvmr9-class"></a>CVMR9-Klasse

Die `CVMR9` -Klasse verwaltet VMR-9. Sie enthält einen Zeiger auf die [**IVMRWindowlessControl9-Schnittstelle.**](/previous-versions/windows/desktop/api/Vmr9/nn-vmr9-ivmrwindowlesscontrol9)


```C++
// Manages the VMR-9 video renderer filter.

class CVMR9 : public CVideoRenderer
{
    IVMRWindowlessControl9 *m_pWindowless;

public:
    CVMR9();
    ~CVMR9();
    BOOL    HasVideo() const;
    HRESULT AddToGraph(IGraphBuilder *pGraph, HWND hwnd);
    HRESULT FinalizeGraph(IGraphBuilder *pGraph);
    HRESULT UpdateVideoWindow(HWND hwnd, const LPRECT prc);
    HRESULT Repaint(HWND hwnd, HDC hdc);
    HRESULT DisplayModeChanged();
};
```



### <a name="cvmr7-class"></a>CVMR7-Klasse

Die `CVMR7` -Klasse verwaltet VMR-7. Sie enthält einen Zeiger auf die [**IVMRWindowlessControl-Schnittstelle.**](/windows/desktop/api/Strmif/nn-strmif-ivmrwindowlesscontrol)


```C++
// Manages the VMR-7 video renderer filter.

class CVMR7 : public CVideoRenderer
{
    IVMRWindowlessControl   *m_pWindowless;

public:
    CVMR7();
    ~CVMR7();
    BOOL    HasVideo() const;
    HRESULT AddToGraph(IGraphBuilder *pGraph, HWND hwnd);
    HRESULT FinalizeGraph(IGraphBuilder *pGraph);
    HRESULT UpdateVideoWindow(HWND hwnd, const LPRECT prc);
    HRESULT Repaint(HWND hwnd, HDC hdc);
    HRESULT DisplayModeChanged();
};
```



Weiter: [Schritt 3: Erstellen des Filters Graph](step-3--build-the-filter-graph.md).

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Audio-/Videowiedergabe in DirectShow](audio-video-playback-in-directshow.md)
</dt> <dt>

[Verwenden des Videomischungsrenderers](using-the-video-mixing-renderer.md)
</dt> <dt>

[Videorendering](video-rendering.md)
</dt> </dl>

 

 
