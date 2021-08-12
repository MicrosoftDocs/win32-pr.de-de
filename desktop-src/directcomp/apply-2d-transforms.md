---
title: Anwenden von 2D-Transformationen
description: In diesem Thema wird veranschaulicht, wie Sie 2D-Transformationen mithilfe von Microsoft DirectComposition auf ein Visual anwenden.
ms.assetid: DED74416-C85A-4220-89BD-3F9BEF786B7D
keywords:
- Anwenden von DirectComposition 2D-Transformationen
- DirectComposition 2D-Transformationen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6ef965ce98bb064eb63b34de569160c9b68932c96ce757e3e5d13450f73098b4
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118281955"
---
# <a name="how-to-apply-2d-transforms"></a>Anwenden von 2D-Transformationen

> [!NOTE]
> Für Apps auf Windows 10 empfehlen wir die Verwendung von Windows.UI.Composition-APIs anstelle von DirectComposition. Weitere Informationen finden Sie unter [Modernisieren Ihrer Desktop-App mithilfe der visuellen Ebene](/windows/uwp/composition/visual-layer-in-desktop-apps).

In diesem Thema wird veranschaulicht, wie Sie 2D-Transformationen mithilfe von Microsoft DirectComposition auf ein Visual anwenden. Im Beispiel in diesem Thema wird eine Gruppe von Transformationen angewendet, die:

1.  Drehen Sie das Visual um 180 Grad.
2.  Skalieren Sie das Visual auf das Dreifache seiner ursprünglichen Größe hoch.
3.  Übersetzen (Verschieben) des Visuals um 150 Pixel nach rechts von seiner ursprünglichen Position.

Die folgenden Screenshots zeigen das Visual vor und nach dem Anwenden der 2D-Transformationen.

![Ergebnis der Anwendung einer Gruppe von 2d-Transformationen auf ein Visual](images/apply2dtransform.png)

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

### <a name="step-2-create-the-transform-group-array"></a>Schritt 2: Erstellen des Transformationsgruppenarrays


```C++
IDCompositionTransform *pTransforms[3];
```



### <a name="step-3-create-the-transform-objects-set-their-properties-and-add-them-to-the-transform-group-array"></a>Schritt 3: Erstellen der Transformationsobjekte, Festlegen ihrer Eigenschaften und Hinzufügen zum Transformationsgruppenarray

1.  Verwenden Sie die Methoden [**IDCompositionDevice::CreateRotateTransform,**](/windows/win32/api/dcomp/nf-dcomp-idcompositiondevice-createrotatetransform) [**::CreateScaleTransform**](/windows/win32/api/dcomp/nf-dcomp-idcompositiondevice-createscaletransform)und [**::CreateTranslateTransform,**](/windows/win32/api/dcomp/nf-dcomp-idcompositiondevice-createtranslatetransform) um die Transformationsobjekte zu erstellen.
2.  Verwenden Sie die Memberfunktionen der Schnittstellen [**IDCompositionRotateTransform,**](/windows/win32/api/dcomp/nn-dcomp-idcompositionrotatetransform) [**IDCompositionScaleTransform**](/windows/win32/api/dcomp/nn-dcomp-idcompositionscaletransform)und [**IDCompositionTranslateTransform,**](/windows/win32/api/dcomp/nn-dcomp-idcompositiontranslatetransform) um die Eigenschaften der Transformationen festzulegen.
3.  Kopieren Sie die Transformationsschnittstellenzeiger auf das Transformationsgruppenarray.


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



### <a name="step-4-create-the-transform-group-object"></a>Schritt 4: Erstellen des Transformationsgruppenobjekts

Rufen Sie die [**IDCompositionDevice::CreateTransformGroup-Methode**](/windows/win32/api/dcomp/nf-dcomp-idcompositiondevice-createtransformgroup) auf, um das Transformationsgruppenobjekt zu erstellen.


```C++
if (SUCCEEDED(hr))
{
    // Create the transform group.
    hr = pDevice->CreateTransformGroup(pTransforms, 3, &pTransformGroup);
}
```



### <a name="step-5-apply-the-transform-group-object-to-the-visual"></a>Schritt 5: Anwenden des Transformationsgruppenobjekts auf das Visual

Verwenden Sie die [**IDCompositionVisual::SetTransform-Methode,**](/windows/win32/api/dcomp/nf-dcomp-idcompositionvisual-settransform(constd2d_matrix_3x2_f_)) um die Transform-Eigenschaft des Visuals dem Transformationsgruppenobjekt zuzuordnen.


```C++
if (SUCCEEDED(hr))
{
    // Apply the transform group to the visual.
    hr = pVisual->SetTransform(pTransformGroup);
}
```



### <a name="step-6-commit-the-composition"></a>Schritt 6: Committen der Komposition

Rufen Sie die [**IDCompositionDevice::Commit-Methode**](/windows/win32/api/dcomp/nf-dcomp-idcompositiondevice-commit) auf, um die Aktualisierungen des Visuals zur Verarbeitung an DirectComposition zu committen. Das Ergebnis der Anwendung der Gruppe von 2D-Transformationen wird im Zielfenster angezeigt.


```C++
if (SUCCEEDED(hr))
{
    // Commit the composition.
    hr = pDevice->Commit();
}
```



### <a name="step-7-free-the-directcomposition-objects"></a>Schritt 7: Freigeben der DirectComposition-Objekte

Stellen Sie sicher, dass Sie die Gruppe von 2D-Transformationsobjekten freigeben, wenn Sie sie nicht mehr benötigen. Im folgenden Beispiel wird das anwendungsdefinierte [**SafeRelease-Makro**](/windows/desktop/medfound/saferelease) zum Freigeben der Transformationsobjekte aufrufen.


```C++
// Release the transform objects.
for (int i = 0; i < 3; i++)
{
    SafeRelease(&pTransforms[i]);
}
```



Denken Sie auch daran, das Geräteobjekt, das Kompositionszielobjekt und die Visuals frei zu lassen, bevor Ihre Anwendung beendet wird.

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

 

 