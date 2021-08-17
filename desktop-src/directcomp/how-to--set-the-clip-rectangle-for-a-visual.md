---
title: Beschneiden mit einem Rechteck-Clipobjekt
description: In diesem Thema wird veranschaulicht, wie sie ein Rechteck-Clip-Objekt verwenden, um eine visuelle oder visuelle Struktur zu beschneiden.
ms.assetid: 377EF49A-F9F2-4A72-9D22-DEC33803AD0D
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 10386f3e99dead7fff04a57463c2ee753bd1d712e9a59e6b928136c32f25ae75
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119119098"
---
# <a name="how-to-clip-with-a-rectangle-clip-object"></a>Beschneiden mit einem Rechteck-Clipobjekt

> [!NOTE]
> Für Apps auf Windows 10 empfehlen wir die Verwendung von Windows.UI.Composition-APIs anstelle von DirectComposition. Weitere Informationen finden Sie unter [Modernisieren Ihrer Desktop-App mithilfe der visuellen Ebene.](/windows/uwp/composition/visual-layer-in-desktop-apps)

In diesem Thema wird veranschaulicht, wie sie ein Rechteck-Clip-Objekt verwenden, um eine visuelle oder visuelle Struktur zu beschneiden.

Das Beispiel in diesem Thema definiert einen rechteckigen Clip, der an der Mausposition zentriert ist, und wendet den Clip auf ein Visual an, das im Clientbereich des Kompositionszielfensters zentriert ist. Dieser Screenshot zeigt das Ergebnis der Anwendung des Rechteck-Clipobjekts auf das Visual.

![Ergebnis der Anwendung eines Rechteck-Clipobjekts auf ein Visual](images/clipwithrectangleclipobject.png)

## <a name="what-you-need-to-know"></a>Wichtige Informationen

### <a name="technologies"></a>Technologien

-   [DirectComposition](directcomposition-portal.md)
-   [Direct3D 11-Grafik](/windows/desktop/direct3d11/atoc-dx-graphics-direct3d-11)
-   [DirectX Graphic Infrastructure (DXGI)](/windows/desktop/direct3ddxgi/dx-graphics-dxgi)

### <a name="prerequisites"></a>Voraussetzungen

-   C/C++
-   Microsoft Win32
-   Component Object Model (COM)

## <a name="instructions"></a>Anweisungen

### <a name="step-1-initialize-directcomposition-objects"></a>Schritt 1: Initialisieren von DirectComposition-Objekten

1.  Erstellen Sie das Geräteobjekt und das Kompositionszielobjekt.
2.  Erstellen Sie ein Visual, legen Sie dessen Inhalt fest, und fügen Sie es der visuellen Struktur hinzu.

Weitere Informationen finden Sie unter [Initialisieren von DirectComposition.](initialize-directcomposition.md)

### <a name="step-2-create-the-rectangle-clip-object"></a>Schritt 2: Erstellen des Rechteck-Clipobjekts

Verwenden Sie [**die IDCompositionDevice::CreateRectangleClip-Methode,**](/windows/win32/api/dcomp/nf-dcomp-idcompositiondevice-createrectangleclip) um eine Instanz des Rechteck-Clipobjekts zu erstellen.


```C++
    HRESULT hr = S_OK;
    
    // Create the rectangle clip object.
    if (m_pClip == NULL)
    {
        hr = m_pDevice->CreateRectangleClip(&m_pClip);
    }
```



### <a name="step-3-set-the-properties-of-the-rectangle-clip-object"></a>Schritt 3: Festlegen der Eigenschaften des Rechteck-Clipobjekts

Rufen Sie die Methoden der [**IDCompositionRectangleClip-Schnittstelle**](/windows/win32/api/dcomp/nn-dcomp-idcompositionrectangleclip) des Rechteckclipobjekts auf, um die Eigenschaften des Cliprechtecks zu festlegen.

Im folgenden Beispiel wird ein Cliprechteck definiert, das um die aktuelle Mausposition zentriert ist. Die `m_offsetX` `m_offsetY` Membervariablen und enthalten die Werte der OffsetX- und OffsetY-Eigenschaften des Visuals.


```C++
    if (SUCCEEDED(hr))
    {
        // Get the location of the mouse.
        POINT ptMouse = { };
        GetCursorPos(&ptMouse);
        ScreenToClient(m_hwnd, &ptMouse);

        // Create a 100-by-100 pixel rectangular clip that is 
        // centered at the mouse location, and is mapped to
        // the rectangle of the visual.
        m_pClip->SetLeft((ptMouse.x - m_offsetX) - 50.f);
        m_pClip->SetTop((ptMouse.y - m_offsetY) - 50.f);
        m_pClip->SetRight((ptMouse.x - m_offsetX) + 50.f);
        m_pClip->SetBottom((ptMouse.y - m_offsetY) + 50.f);
    }
```



Beachten Sie, dass die [**IDCompositionRectangleClip-Schnittstelle**](/windows/win32/api/dcomp/nn-dcomp-idcompositionrectangleclip) die folgenden Methoden zum Definieren eines Cliprechtecks mit abgerundeten Ecken enthält:

-   [**SetTopLeftRadiusX**](/windows/win32/api/dcomp/nf-dcomp-idcompositionrectangleclip-settopleftradiusx(float))
-   [**SetTopLeftRadiusY**](/windows/win32/api/dcomp/nf-dcomp-idcompositionrectangleclip-settopleftradiusy(float))
-   [**SetTopRightRadiusX**](/windows/win32/api/dcomp/nf-dcomp-idcompositionrectangleclip-settoprightradiusx(float))
-   [**SetTopRightRadiusY**](/windows/win32/api/dcomp/nf-dcomp-idcompositionrectangleclip-settoprightradiusy(float))

### <a name="step-4-set-the-clip-property-of-the-visual"></a>Schritt 4: Festlegen der Clip-Eigenschaft des Visuals

Verwenden Sie [**die IDCompositionVisual::SetClip-Methode,**](/windows/win32/api/dcomp/nf-dcomp-idcompositionvisual-setclip(idcompositionclip)) um die Clip-Eigenschaft des Visuals dem Rechteck-Clipobjekt zu zuordnen.


```C++
    if (SUCCEEDED(hr))
    {
        // Set the rectangle clip object as the Clip property 
        // of the visual.
        hr = m_pVisual->SetClip(m_pClip);
    }
```



### <a name="step-5-commit-the-composition"></a>Schritt 5: Commit der Komposition

Rufen Sie die [**IDCompositionDevice::Commit-Methode auf,**](/windows/win32/api/dcomp/nf-dcomp-idcompositiondevice-commit) um den Batch von Befehlen zur Verarbeitung an Microsoft DirectComposition zu commiten. Das Ergebnis der Anwendung des Cliprechtecks wird im Zielfenster angezeigt.


```C++
    if (SUCCEEDED(hr))
    {
        // Commit the visual to be composed and displayed.
        hr = m_pDevice->Commit();  
    }
```



### <a name="step-6-free-the-directcomposition-objects"></a>Schritt 6: Freisetzung der DirectComposition-Objekte

Achten Sie darauf, das Rechteck-Clipobjekt frei zu geben, wenn Sie es nicht mehr benötigen, sowie das Geräteobjekt, das Kompositionszielobjekt und alle visuellen Objekte. Das folgende Beispiel ruft das anwendungsdefinierte [**SafeRelease-Makro**](/windows/desktop/medfound/saferelease) auf, um die DirectComposition-Objekte frei zu geben.


```C++
    SafeRelease(&m_pClip);
    SafeRelease(&m_pDevice);
    SafeRelease(&m_pD3D11Device);
    SafeRelease(&m_pCompTarget);
    SafeRelease(&m_pVisual);
    SafeRelease(&m_pSurface);
```



## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Freistellen](clipping.md)
</dt> </dl>

 

 