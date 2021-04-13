---
title: Anwenden von 2D-Transformationen
description: In diesem Thema wird veranschaulicht, wie 2D-Transformationen mithilfe von Microsoft directcomposition auf ein visuelles Element angewendet werden.
ms.assetid: DED74416-C85A-4220-89BD-3F9BEF786B7D
keywords:
- Anwenden von 2D-Transformationen für directcomposition
- Directcomposition 2D-Transformationen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b52d2e0ce9fbb56547c42ea4ea18d57d173a7e40
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "104390811"
---
# <a name="how-to-apply-2d-transforms"></a>Anwenden von 2D-Transformationen

> [!NOTE]
> Für apps unter Windows 10 wird die Verwendung von Windows. UI. Composition-APIs anstelle von directcomposition empfohlen. Weitere Informationen finden Sie unter [modernisieren ihrer Desktop-App mithilfe der visuellen Ebene](/windows/uwp/composition/visual-layer-in-desktop-apps).

In diesem Thema wird veranschaulicht, wie 2D-Transformationen mithilfe von Microsoft directcomposition auf ein visuelles Element angewendet werden. Im Beispiel in diesem Thema wird eine Gruppe von Transformationen angewendet, die Folgendes ausführen:

1.  Drehen Sie die Visualisierung um 180 Grad.
2.  Skalieren Sie die Visualisierung um das Dreifache der ursprünglichen Größe.
3.  Übersetzen (verschieben) Sie die Visual 150 Pixel nach rechts von der ursprünglichen Position.

Die folgenden Screenshots zeigen das visuelle Element vor und nach dem Anwenden der 2D-Transformationen.

![Ergebnis der Anwendung einer Gruppe von 2D-Transformationen auf ein visuelles Element](images/apply2dtransform.png)

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

### <a name="step-2-create-the-transform-group-array"></a>Schritt 2: Erstellen des Transformationsgruppen Arrays


```C++
IDCompositionTransform *pTransforms[3];
```



### <a name="step-3-create-the-transform-objects-set-their-properties-and-add-them-to-the-transform-group-array"></a>Schritt 3: Erstellen der Transformations Objekte, Festlegen ihrer Eigenschaften und Hinzufügen der Objekte zum Transformationsgruppen Array

1.  Verwenden Sie die Methoden [**idcompositiondevice:: kreaterotatetransform**](/windows/win32/api/dcomp/nf-dcomp-idcompositiondevice-createrotatetransform), [**:: kreatescaletransform**](/windows/win32/api/dcomp/nf-dcomp-idcompositiondevice-createscaletransform)und [**:: kreatetranslatetransform**](/windows/win32/api/dcomp/nf-dcomp-idcompositiondevice-createtranslatetransform) , um die Transformations Objekte zu erstellen.
2.  Verwenden Sie die Member-Funktionen der Schnittstellen [**idcompositionrotatetransform**](/windows/win32/api/dcomp/nn-dcomp-idcompositionrotatetransform), [**idcompositionscaletransform**](/windows/win32/api/dcomp/nn-dcomp-idcompositionscaletransform)und [**idcompositiontranslatetransform**](/windows/win32/api/dcomp/nn-dcomp-idcompositiontranslatetransform) , um die Eigenschaften der Transformationen festzulegen.
3.  Kopieren Sie die Transformations Schnittstellen Zeiger in das Transformationsgruppen Array.


```C++
IDCompositionRotateTransform *pRotateTransform = nullptr;
IDCompositionScaleTransform *pScaleTransform = nullptr;
IDCompositionTranslateTransform *pTranslateTransform = nullptr;
IDCompositionTransform *pTransformGroup = nullptr;

// Create the rotate transform.
hr = pDevice->CreateRotateTransform(&pRotateTransform);

if (SUCCEEDED(hr))
{
    // Set the center of rotation to the center point of the visual.
    hr = pRotateTransform->SetCenterX(BITMAP_WIDTH/2.0f);
    
    if (SUCCEEDED(hr)) {
        hr = pRotateTransform->SetCenterY(BITMAP_HEIGHT/2.0f);
    }

    // Set the rotate angle to 180 degrees.
    if (SUCCEEDED(hr)) {
        hr = pRotateTransform->SetAngle(180.0f);
    }

    // Add the rotate transform to the transform group array.
    pTransforms[0] = pRotateTransform;

    // Create the scale transform.
    if (SUCCEEDED(hr)) {
        hr = pDevice->CreateScaleTransform(&pScaleTransform);
    }
}

if (SUCCEEDED(hr))
{
    // Set the scaling origin to the upper-right corner of the visual.
    hr = pScaleTransform->SetCenterX(0.0f);
    if (SUCCEEDED(hr)) {
        hr = pScaleTransform->SetCenterY(0.0f);
    }

    // Set the scaling factor to three for both the width and height. 
    if (SUCCEEDED(hr)) {
        hr = pScaleTransform->SetScaleX(3.0f);
    }
    if (SUCCEEDED(hr)) {
        hr = pScaleTransform->SetScaleY(3.0f);
    }

    // Add the scale transform to the transform group array.
    pTransforms[1] = pScaleTransform;

    // Create the translate transform.
    if (SUCCEEDED(hr)) {
        hr = pDevice->CreateTranslateTransform(&pTranslateTransform);
    }
}

if (SUCCEEDED(hr))
{
    // Move the visual 150 pixels to the right.
    hr = pTranslateTransform->SetOffsetX(150.0f);
    if (SUCCEEDED(hr)) {
        hr = pTranslateTransform->SetOffsetY(0.0f);
    }

    // Add the translate transform to the transform group array.
    pTransforms[2] = pTranslateTransform;
}
```



### <a name="step-4-create-the-transform-group-object"></a>Schritt 4: Erstellen des Transformationsgruppen Objekts

Rufen Sie die [**idcompositiondevice:: kreatetransformgroup**](/windows/win32/api/dcomp/nf-dcomp-idcompositiondevice-createtransformgroup) -Methode auf, um das Transformationsgruppen Objekt zu erstellen.


```C++
if (SUCCEEDED(hr))
{
    // Create the transform group.
    hr = pDevice->CreateTransformGroup(pTransforms, 3, &pTransformGroup);
}
```



### <a name="step-5-apply-the-transform-group-object-to-the-visual"></a>Schritt 5: Anwenden des Transformationsgruppen Objekts auf das visuelle Element

Verwenden Sie die [**idcompositionvisual:: setTransform**](/windows/win32/api/dcomp/nf-dcomp-idcompositionvisual-settransform(constd2d_matrix_3x2_f_)) -Methode, um die Transform-Eigenschaft der Visualisierung dem Transformationsgruppen Objekt zuzuordnen.


```C++
if (SUCCEEDED(hr))
{
    // Apply the transform group to the visual.
    hr = pVisual->SetTransform(pTransformGroup);
}
```



### <a name="step-6-commit-the-composition"></a>Schritt 6: Commit der Komposition ausführen

Rufen Sie die [**idcompositiondevice:: Commit**](/windows/win32/api/dcomp/nf-dcomp-idcompositiondevice-commit) -Methode auf, um die Aktualisierungen für die Visualisierung für die Verarbeitung in directcomposition zu committen. Das Ergebnis der Anwendung der Gruppe von 2D-Transformationen wird im Zielfenster angezeigt.


```C++
if (SUCCEEDED(hr))
{
    // Commit the composition.
    hr = pDevice->Commit();
}
```



### <a name="step-7-free-the-directcomposition-objects"></a>Schritt 7: Freigeben der directcomposition-Objekte

Stellen Sie sicher, dass Sie die Gruppe von 2D-Transformations Objekten freigeben, wenn Sie Sie nicht mehr benötigen. Im folgenden Beispiel wird das Anwendungs definierte [**saferelease**](/windows/desktop/medfound/saferelease) -Makro aufgerufen, um die Transformations Objekte freizugeben.


```C++
// Release the transform objects.
for (int i = 0; i < 3; i++)
{
    SafeRelease(&pTransforms[i]);
}
```



Denken Sie auch daran, das Geräte Objekt, das Kompositions Zielobjekt und die visuellen Elemente freizugeben, bevor die Anwendung beendet wird.

## <a name="complete-example"></a>Vollständiges Beispiel


```C++
#define BITMAP_WIDTH  80.0
#define BITMAP_HEIGHT 80.0

HRESULT DemoApp::ApplyTransformGroup(IDCompositionDevice *pDevice, 
                                     IDCompositionVisual *pVisual)
{
    HRESULT hr = S_OK;

    if (pDevice == nullptr || pVisual == nullptr)
        return E_INVALIDARG; 
    
    IDCompositionTransform *pTransforms[3];

    IDCompositionRotateTransform *pRotateTransform = nullptr;
    IDCompositionScaleTransform *pScaleTransform = nullptr;
    IDCompositionTranslateTransform *pTranslateTransform = nullptr;
    IDCompositionTransform *pTransformGroup = nullptr;

    // Create the rotate transform.
    hr = pDevice->CreateRotateTransform(&pRotateTransform);

    if (SUCCEEDED(hr))
    {
        // Set the center of rotation to the center point of the visual.
        hr = pRotateTransform->SetCenterX(BITMAP_WIDTH/2.0f);
        
        if (SUCCEEDED(hr)) {
            hr = pRotateTransform->SetCenterY(BITMAP_HEIGHT/2.0f);
        }

        // Set the rotate angle to 180 degrees.
        if (SUCCEEDED(hr)) {
            hr = pRotateTransform->SetAngle(180.0f);
        }

        // Add the rotate transform to the transform group array.
        pTransforms[0] = pRotateTransform;

        // Create the scale transform.
        if (SUCCEEDED(hr)) {
            hr = pDevice->CreateScaleTransform(&pScaleTransform);
        }
    }

    if (SUCCEEDED(hr))
    {
        // Set the scaling origin to the upper-right corner of the visual.
        hr = pScaleTransform->SetCenterX(0.0f);
        if (SUCCEEDED(hr)) {
            hr = pScaleTransform->SetCenterY(0.0f);
        }

        // Set the scaling factor to three for both the width and height. 
        if (SUCCEEDED(hr)) {
            hr = pScaleTransform->SetScaleX(3.0f);
        }
        if (SUCCEEDED(hr)) {
            hr = pScaleTransform->SetScaleY(3.0f);
        }

        // Add the scale transform to the transform group array.
        pTransforms[1] = pScaleTransform;

        // Create the translate transform.
        if (SUCCEEDED(hr)) {
            hr = pDevice->CreateTranslateTransform(&pTranslateTransform);
        }
    }

    if (SUCCEEDED(hr))
    {
        // Move the visual 150 pixels to the right.
        hr = pTranslateTransform->SetOffsetX(150.0f);
        if (SUCCEEDED(hr)) {
            hr = pTranslateTransform->SetOffsetY(0.0f);
        }

        // Add the translate transform to the transform group array.
        pTransforms[2] = pTranslateTransform;
    }

    if (SUCCEEDED(hr))
    {
        // Create the transform group.
        hr = pDevice->CreateTransformGroup(pTransforms, 3, &pTransformGroup);
    }

    if (SUCCEEDED(hr))
    {
        // Apply the transform group to the visual.
        hr = pVisual->SetTransform(pTransformGroup);
    }

    if (SUCCEEDED(hr))
    {
        // Commit the composition.
        hr = pDevice->Commit();
    }

    // Release the transform objects.
    for (int i = 0; i < 3; i++)
    {
        SafeRelease(&pTransforms[i]);
    }

    // Release the transform group pointer.
    SafeRelease(&pTransformGroup);

    return hr;
}
```



## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Transformationen](transforms.md)
</dt> </dl>

 

 