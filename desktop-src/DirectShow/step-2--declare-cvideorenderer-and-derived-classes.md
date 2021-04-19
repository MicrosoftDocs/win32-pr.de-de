---
description: Dieses Thema ist Schritt 2 des Tutorials Audio-/Videowiedergabe in DirectShow.
ms.assetid: 61106781-d10c-41a8-993e-121e0a1e4c4d
title: 'Schritt 2: Deklarieren von cvideorenderer und abgeleiteten Klassen'
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 11474c57e70d8632a53ac0b858d61d2bddf1e86b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106362837"
---
# <a name="step-2-declare-cvideorenderer-and-derived-classes"></a>Schritt 2: Deklarieren von cvideorenderer und abgeleiteten Klassen

Dieses Thema ist Schritt 2 des Tutorials [Audio-/Videowiedergabe in DirectShow](audio-video-playback-in-directshow.md). Der gesamte Code wird im Thema [DirectShow-Wiedergabe Beispiel](directshow-playback-example.md)dargestellt.

DirectShow bietet verschiedene Filter zum Rendering von Videos:

-   [**Erweiterter Videorenderer-Filter**](enhanced-video-renderer-filter.md) (EVR)
-   [Video Mischungs-Renderer Filter 9](video-mixing-renderer-filter-9.md) (VMR-9)
-   [Video Mischungs-Renderer Filter 7](video-mixing-renderer-filter-7.md) (VMR-7)

Weitere Informationen zu den Unterschieden zwischen diesen Filtern finden Sie unter [auswählen des richtigen Videorenderers](choosing-the-right-renderer.md).

In diesem Tutorial wird die folgende abstrakte Klasse verwendet, um den Videorenderer-Filter zu umschließen.


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

-   Die- `HasVideo` Methode gibt **true** zurück, wenn der Videorenderer erstellt wurde.
-   Die- `AddToGraph` Methode fügt dem Filter Diagramm den Videorenderer hinzu.
-   Die `FinalizeGraph` -Methode schließt den Schritt für die Diagramm Bildung ab.
-   Die- `UpdateVideoWindow` Methode aktualisiert das Video Ziel Rechteck.
-   Mit der- `Repaint` Methode wird der aktuelle Videoframe neu gezeichnet.
-   Die `DisplayModeChanged` -Methode behandelt Änderungen im Anzeigemodus.

Diese Methoden werden weiter unten in diesem Tutorial ausführlich beschrieben.

Als nächstes deklarieren Sie eine abgeleitete Klasse, um jeden der drei Videorenderer zu umschließen: den EVR, den VMR-9 und den VMR-7.

### <a name="cevr-class"></a>Cevr-Klasse

Die- `CEVR` Klasse verwaltet den EVR. Sie enthält einen Zeiger auf die Schnittstellen [**ibasefilter**](/windows/desktop/api/Strmif/nn-strmif-ibasefilter) und [**imfvideodisplaycontrol**](/windows/win32/api/evr/nn-evr-imfvideodisplaycontrol) der EVR.


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

Die `CVMR9` -Klasse verwaltet VMR-9. Sie enthält einen Zeiger auf die [**IVMRWindowlessControl9**](/previous-versions/windows/desktop/api/Vmr9/nn-vmr9-ivmrwindowlesscontrol9) -Schnittstelle.


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

Die `CVMR7` -Klasse verwaltet VMR-7. Sie enthält einen Zeiger auf die [**ivmrwindowlesscontrol**](/windows/desktop/api/Strmif/nn-strmif-ivmrwindowlesscontrol) -Schnittstelle.


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



Weiter: [Schritt 3: Erstellen des Filter Diagramms](step-3--build-the-filter-graph.md).

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Audiowiedergabe und Video Wiedergabe in DirectShow](audio-video-playback-in-directshow.md)
</dt> <dt>

[Verwenden des Video Mischungs Renderers](using-the-video-mixing-renderer.md)
</dt> <dt>

[Videorendering](video-rendering.md)
</dt> </dl>

 

 
