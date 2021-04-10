---
title: Vorgehensweise beim Abschneiden mit einem Rechteck Clip-Objekt
description: In diesem Thema wird veranschaulicht, wie ein Rechteck Clip-Objekt verwendet wird, um eine visuelle Struktur oder eine visuelle Struktur zu schneiden
ms.assetid: 377EF49A-F9F2-4A72-9D22-DEC33803AD0D
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0d26019f37949b0111ee9b5958fa3fba2c9507cb
ms.sourcegitcommit: 73417d55867c804274a55abe5ca71bcba7006119
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/20/2020
ms.locfileid: "104039820"
---
# <a name="how-to-clip-with-a-rectangle-clip-object"></a>Vorgehensweise beim Abschneiden mit einem Rechteck Clip-Objekt

> [!NOTE]
> Für apps unter Windows 10 wird die Verwendung von Windows. UI. Composition-APIs anstelle von directcomposition empfohlen. Weitere Informationen finden Sie unter [modernisieren ihrer Desktop-App mithilfe der visuellen Ebene](/windows/uwp/composition/visual-layer-in-desktop-apps).

In diesem Thema wird veranschaulicht, wie ein Rechteck Clip-Objekt verwendet wird, um eine visuelle Struktur oder eine visuelle Struktur zu schneiden

Im Beispiel in diesem Thema wird ein rechteckiger Clip definiert, der an der Mausposition zentriert ist, und der Clip wird auf ein visuelles Element angewendet, das im Client Bereich des Kompositions Zielfensters zentriert ist. Dieser Screenshot zeigt das Ergebnis der Anwendung des Rechteck Clip Objekts auf das visuelle Element.

![Ergebnis der Anwendung eines Rechteck Clip Objekts auf ein visuelles Element](images/clipwithrectangleclipobject.png)

## <a name="what-you-need-to-know"></a>Was Sie wissen müssen

### <a name="technologies"></a>Technologien

-   [DirectComposition](directcomposition-portal.md)
-   [Direct3D 11-Grafik](/windows/desktop/direct3d11/atoc-dx-graphics-direct3d-11)
-   [DirectX-Grafik Infrastruktur (DXGI)](/windows/desktop/direct3ddxgi/dx-graphics-dxgi)

### <a name="prerequisites"></a>Voraussetzungen

-   C/C++
-   Microsoft Win32
-   Component Object Model (COM)

## <a name="instructions"></a>Anweisungen

### <a name="step-1-initialize-directcomposition-objects"></a>Schritt 1: Initialisieren von directcomposition-Objekten

1.  Erstellen Sie das Geräte Objekt und das Kompositions Zielobjekt.
2.  Erstellen Sie ein visuelles Element, legen Sie seinen Inhalt fest, und fügen Sie es der visuellen Struktur hinzu.

Weitere Informationen finden Sie unter [Initialisieren von directcomposition](initialize-directcomposition.md).

### <a name="step-2-create-the-rectangle-clip-object"></a>Schritt 2: Erstellen des Rechteck Clip-Objekts

Verwenden Sie die [**idcompositiondevice::**](/windows/win32/api/dcomp/nf-dcomp-idcompositiondevice-createrectangleclip) up-Methode, um eine Instanz des Rechteck Clip Objekts zu erstellen.


```C++
    HRESULT hr = S_OK;
    
    // Create the rectangle clip object.
    if (m_pClip == NULL)
    {
        hr = m_pDevice->CreateRectangleClip(&m_pClip);
    }
```



### <a name="step-3-set-the-properties-of-the-rectangle-clip-object"></a>Schritt 3: Festlegen der Eigenschaften des Rechteck Clip Objekts

Rufen Sie die Methoden der [**idcompositionrechgleclip**](/windows/win32/api/dcomp/nn-dcomp-idcompositionrectangleclip) -Schnittstelle des Rechteck Clip Objekts auf, um die Eigenschaften des Clip Rechtecks festzulegen.

Im folgenden Beispiel wird ein Clip Rechteck definiert, das um die aktuelle Mausposition zentriert ist. Die `m_offsetX` -und-Element `m_offsetY` Variablen enthalten die Werte der OffsetX-Eigenschaft und der OffsetY-Eigenschaft des visuellen Elements.


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



Beachten Sie, dass die [**idcompositionrechgleclip**](/windows/win32/api/dcomp/nn-dcomp-idcompositionrectangleclip) -Schnittstelle die folgenden Methoden zum Definieren eines Clip Rechtecks mit abgerundeten Ecken umfasst:

-   [**Settopleftradius x**](/windows/win32/api/dcomp/nf-dcomp-idcompositionrectangleclip-settopleftradiusx(float))
-   [**Settopleftradius y**](/windows/win32/api/dcomp/nf-dcomp-idcompositionrectangleclip-settopleftradiusy(float))
-   [**Settoprightradius x**](/windows/win32/api/dcomp/nf-dcomp-idcompositionrectangleclip-settoprightradiusx(float))
-   [**Settoprightradius y**](/windows/win32/api/dcomp/nf-dcomp-idcompositionrectangleclip-settoprightradiusy(float))

### <a name="step-4-set-the-clip-property-of-the-visual"></a>Schritt 4: Festlegen der Clip-Eigenschaft des visuellen Elements

Verwenden Sie die [**idcompositionvisual:: SetClip**](/windows/win32/api/dcomp/nf-dcomp-idcompositionvisual-setclip(idcompositionclip)) -Methode, um die Clip-Eigenschaft des visuellen Elements dem Rechteck Clip-Objekt zuzuordnen.


```C++
    if (SUCCEEDED(hr))
    {
        // Set the rectangle clip object as the Clip property 
        // of the visual.
        hr = m_pVisual->SetClip(m_pClip);
    }
```



### <a name="step-5-commit-the-composition"></a>Schritt 5: Commit der Komposition ausführen

Rufen Sie die [**idcompositiondevice:: Commit**](/windows/win32/api/dcomp/nf-dcomp-idcompositiondevice-commit) -Methode auf, um einen Commit für den Batch der Befehle an Microsoft directcomposition zur Verarbeitung auszuführen. Das Ergebnis der Anwendung des Clip Rechtecks wird im Zielfenster angezeigt.


```C++
    if (SUCCEEDED(hr))
    {
        // Commit the visual to be composed and displayed.
        hr = m_pDevice->Commit();  
    }
```



### <a name="step-6-free-the-directcomposition-objects"></a>Schritt 6: Freigeben der directcomposition-Objekte

Stellen Sie sicher, dass Sie das Rechteck Clip-Objekt freigeben, wenn Sie es nicht mehr benötigen, sowie das Geräte Objekt, das Kompositions Zielobjekt und alle visuellen Objekte. Im folgenden Beispiel wird das Anwendungs definierte [**saferelease**](/windows/desktop/medfound/saferelease) -Makro aufgerufen, um die directcomposition-Objekte freizugeben.


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

 

 