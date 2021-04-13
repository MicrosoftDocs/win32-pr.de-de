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
# <a name="how-to-apply-2d-transforms"></a><span data-ttu-id="08869-105">Anwenden von 2D-Transformationen</span><span class="sxs-lookup"><span data-stu-id="08869-105">How to apply 2D transforms</span></span>

> [!NOTE]
> <span data-ttu-id="08869-106">Für apps unter Windows 10 wird die Verwendung von Windows. UI. Composition-APIs anstelle von directcomposition empfohlen.</span><span class="sxs-lookup"><span data-stu-id="08869-106">For apps on Windows 10, we recommend using Windows.UI.Composition APIs instead of DirectComposition.</span></span> <span data-ttu-id="08869-107">Weitere Informationen finden Sie unter [modernisieren ihrer Desktop-App mithilfe der visuellen Ebene](/windows/uwp/composition/visual-layer-in-desktop-apps).</span><span class="sxs-lookup"><span data-stu-id="08869-107">For more info, see [Modernize your desktop app using the Visual layer](/windows/uwp/composition/visual-layer-in-desktop-apps).</span></span>

<span data-ttu-id="08869-108">In diesem Thema wird veranschaulicht, wie 2D-Transformationen mithilfe von Microsoft directcomposition auf ein visuelles Element angewendet werden.</span><span class="sxs-lookup"><span data-stu-id="08869-108">This topic demonstrates how to apply 2D transforms to a visual by using Microsoft DirectComposition.</span></span> <span data-ttu-id="08869-109">Im Beispiel in diesem Thema wird eine Gruppe von Transformationen angewendet, die Folgendes ausführen:</span><span class="sxs-lookup"><span data-stu-id="08869-109">The example in this topic applies a group of transforms that:</span></span>

1.  <span data-ttu-id="08869-110">Drehen Sie die Visualisierung um 180 Grad.</span><span class="sxs-lookup"><span data-stu-id="08869-110">Rotate the visual by 180 degrees.</span></span>
2.  <span data-ttu-id="08869-111">Skalieren Sie die Visualisierung um das Dreifache der ursprünglichen Größe.</span><span class="sxs-lookup"><span data-stu-id="08869-111">Scale up the visual to three times its original size.</span></span>
3.  <span data-ttu-id="08869-112">Übersetzen (verschieben) Sie die Visual 150 Pixel nach rechts von der ursprünglichen Position.</span><span class="sxs-lookup"><span data-stu-id="08869-112">Translate (move) the visual 150 pixels to the right of its original position.</span></span>

<span data-ttu-id="08869-113">Die folgenden Screenshots zeigen das visuelle Element vor und nach dem Anwenden der 2D-Transformationen.</span><span class="sxs-lookup"><span data-stu-id="08869-113">The following screen shots show the visual before and after applying the 2D transforms.</span></span>

![Ergebnis der Anwendung einer Gruppe von 2D-Transformationen auf ein visuelles Element](images/apply2dtransform.png)

## <a name="what-you-need-to-know"></a><span data-ttu-id="08869-115">Was Sie wissen müssen</span><span class="sxs-lookup"><span data-stu-id="08869-115">What you need to know</span></span>

### <a name="technologies"></a><span data-ttu-id="08869-116">Technologien</span><span class="sxs-lookup"><span data-stu-id="08869-116">Technologies</span></span>

-   [<span data-ttu-id="08869-117">DirectComposition</span><span class="sxs-lookup"><span data-stu-id="08869-117">DirectComposition</span></span>](directcomposition-portal.md)
-   [<span data-ttu-id="08869-118">Direct3D 11-Grafik</span><span class="sxs-lookup"><span data-stu-id="08869-118">Direct3D 11 Graphics</span></span>](/windows/desktop/direct3d11/atoc-dx-graphics-direct3d-11)
-   [<span data-ttu-id="08869-119">DirectX-Grafik Infrastruktur (DXGI)</span><span class="sxs-lookup"><span data-stu-id="08869-119">DirectX Graphics Infrastructure (DXGI)</span></span>](/windows/desktop/direct3ddxgi/dx-graphics-dxgi)

### <a name="prerequisites"></a><span data-ttu-id="08869-120">Voraussetzungen</span><span class="sxs-lookup"><span data-stu-id="08869-120">Prerequisites</span></span>

-   <span data-ttu-id="08869-121">C/C++</span><span class="sxs-lookup"><span data-stu-id="08869-121">C/C++</span></span>
-   <span data-ttu-id="08869-122">Microsoft Win32</span><span class="sxs-lookup"><span data-stu-id="08869-122">Microsoft Win32</span></span>
-   <span data-ttu-id="08869-123">Component Object Model (COM)</span><span class="sxs-lookup"><span data-stu-id="08869-123">Component Object Model (COM)</span></span>

## <a name="instructions"></a><span data-ttu-id="08869-124">Anweisungen</span><span class="sxs-lookup"><span data-stu-id="08869-124">Instructions</span></span>

### <a name="step-1-initialize-directcomposition-objects"></a><span data-ttu-id="08869-125">Schritt 1: Initialisieren von directcomposition-Objekten</span><span class="sxs-lookup"><span data-stu-id="08869-125">Step 1: Initialize DirectComposition objects</span></span>

1.  <span data-ttu-id="08869-126">Erstellen Sie das Geräte Objekt und das Kompositions Zielobjekt.</span><span class="sxs-lookup"><span data-stu-id="08869-126">Create the device object and the composition target object.</span></span>
2.  <span data-ttu-id="08869-127">Erstellen Sie ein visuelles Element, legen Sie seinen Inhalt fest, und fügen Sie es der visuellen Struktur hinzu.</span><span class="sxs-lookup"><span data-stu-id="08869-127">Create a visual, set its content, and add it to the visual tree.</span></span>

<span data-ttu-id="08869-128">Weitere Informationen finden Sie unter [Initialisieren von directcomposition](initialize-directcomposition.md).</span><span class="sxs-lookup"><span data-stu-id="08869-128">For more information, see [How to initialize DirectComposition](initialize-directcomposition.md).</span></span>

### <a name="step-2-create-the-transform-group-array"></a><span data-ttu-id="08869-129">Schritt 2: Erstellen des Transformationsgruppen Arrays</span><span class="sxs-lookup"><span data-stu-id="08869-129">Step 2: Create the transform group array</span></span>


```C++
IDCompositionTransform *pTransforms[3];
```



### <a name="step-3-create-the-transform-objects-set-their-properties-and-add-them-to-the-transform-group-array"></a><span data-ttu-id="08869-130">Schritt 3: Erstellen der Transformations Objekte, Festlegen ihrer Eigenschaften und Hinzufügen der Objekte zum Transformationsgruppen Array</span><span class="sxs-lookup"><span data-stu-id="08869-130">Step 3: Create the transform objects, set their properties, and add them to the transform group array</span></span>

1.  <span data-ttu-id="08869-131">Verwenden Sie die Methoden [**idcompositiondevice:: kreaterotatetransform**](/windows/win32/api/dcomp/nf-dcomp-idcompositiondevice-createrotatetransform), [**:: kreatescaletransform**](/windows/win32/api/dcomp/nf-dcomp-idcompositiondevice-createscaletransform)und [**:: kreatetranslatetransform**](/windows/win32/api/dcomp/nf-dcomp-idcompositiondevice-createtranslatetransform) , um die Transformations Objekte zu erstellen.</span><span class="sxs-lookup"><span data-stu-id="08869-131">Use the [**IDCompositionDevice::CreateRotateTransform**](/windows/win32/api/dcomp/nf-dcomp-idcompositiondevice-createrotatetransform), [**::CreateScaleTransform**](/windows/win32/api/dcomp/nf-dcomp-idcompositiondevice-createscaletransform), and [**::CreateTranslateTransform**](/windows/win32/api/dcomp/nf-dcomp-idcompositiondevice-createtranslatetransform) methods to create the transform objects.</span></span>
2.  <span data-ttu-id="08869-132">Verwenden Sie die Member-Funktionen der Schnittstellen [**idcompositionrotatetransform**](/windows/win32/api/dcomp/nn-dcomp-idcompositionrotatetransform), [**idcompositionscaletransform**](/windows/win32/api/dcomp/nn-dcomp-idcompositionscaletransform)und [**idcompositiontranslatetransform**](/windows/win32/api/dcomp/nn-dcomp-idcompositiontranslatetransform) , um die Eigenschaften der Transformationen festzulegen.</span><span class="sxs-lookup"><span data-stu-id="08869-132">Use the member functions of the [**IDCompositionRotateTransform**](/windows/win32/api/dcomp/nn-dcomp-idcompositionrotatetransform), [**IDCompositionScaleTransform**](/windows/win32/api/dcomp/nn-dcomp-idcompositionscaletransform), and [**IDCompositionTranslateTransform**](/windows/win32/api/dcomp/nn-dcomp-idcompositiontranslatetransform) interfaces to set the properties of the transforms.</span></span>
3.  <span data-ttu-id="08869-133">Kopieren Sie die Transformations Schnittstellen Zeiger in das Transformationsgruppen Array.</span><span class="sxs-lookup"><span data-stu-id="08869-133">Copy the transform interface pointers to the transform group array.</span></span>


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



### <a name="step-4-create-the-transform-group-object"></a><span data-ttu-id="08869-134">Schritt 4: Erstellen des Transformationsgruppen Objekts</span><span class="sxs-lookup"><span data-stu-id="08869-134">Step 4: Create the transform group object</span></span>

<span data-ttu-id="08869-135">Rufen Sie die [**idcompositiondevice:: kreatetransformgroup**](/windows/win32/api/dcomp/nf-dcomp-idcompositiondevice-createtransformgroup) -Methode auf, um das Transformationsgruppen Objekt zu erstellen.</span><span class="sxs-lookup"><span data-stu-id="08869-135">Call the [**IDCompositionDevice::CreateTransformGroup**](/windows/win32/api/dcomp/nf-dcomp-idcompositiondevice-createtransformgroup) method to create the transform group object.</span></span>


```C++
if (SUCCEEDED(hr))
{
    // Create the transform group.
    hr = pDevice->CreateTransformGroup(pTransforms, 3, &pTransformGroup);
}
```



### <a name="step-5-apply-the-transform-group-object-to-the-visual"></a><span data-ttu-id="08869-136">Schritt 5: Anwenden des Transformationsgruppen Objekts auf das visuelle Element</span><span class="sxs-lookup"><span data-stu-id="08869-136">Step 5: Apply the transform group object to the visual</span></span>

<span data-ttu-id="08869-137">Verwenden Sie die [**idcompositionvisual:: setTransform**](/windows/win32/api/dcomp/nf-dcomp-idcompositionvisual-settransform(constd2d_matrix_3x2_f_)) -Methode, um die Transform-Eigenschaft der Visualisierung dem Transformationsgruppen Objekt zuzuordnen.</span><span class="sxs-lookup"><span data-stu-id="08869-137">Use the [**IDCompositionVisual::SetTransform**](/windows/win32/api/dcomp/nf-dcomp-idcompositionvisual-settransform(constd2d_matrix_3x2_f_)) method to associate the Transform property of the visual with the transform group object.</span></span>


```C++
if (SUCCEEDED(hr))
{
    // Apply the transform group to the visual.
    hr = pVisual->SetTransform(pTransformGroup);
}
```



### <a name="step-6-commit-the-composition"></a><span data-ttu-id="08869-138">Schritt 6: Commit der Komposition ausführen</span><span class="sxs-lookup"><span data-stu-id="08869-138">Step 6: Commit the composition</span></span>

<span data-ttu-id="08869-139">Rufen Sie die [**idcompositiondevice:: Commit**](/windows/win32/api/dcomp/nf-dcomp-idcompositiondevice-commit) -Methode auf, um die Aktualisierungen für die Visualisierung für die Verarbeitung in directcomposition zu committen.</span><span class="sxs-lookup"><span data-stu-id="08869-139">Call the [**IDCompositionDevice::Commit**](/windows/win32/api/dcomp/nf-dcomp-idcompositiondevice-commit) method to commit the updates to the visual to DirectComposition for processing.</span></span> <span data-ttu-id="08869-140">Das Ergebnis der Anwendung der Gruppe von 2D-Transformationen wird im Zielfenster angezeigt.</span><span class="sxs-lookup"><span data-stu-id="08869-140">The result of applying the group of 2D transforms appears in the target window.</span></span>


```C++
if (SUCCEEDED(hr))
{
    // Commit the composition.
    hr = pDevice->Commit();
}
```



### <a name="step-7-free-the-directcomposition-objects"></a><span data-ttu-id="08869-141">Schritt 7: Freigeben der directcomposition-Objekte</span><span class="sxs-lookup"><span data-stu-id="08869-141">Step 7: Free the DirectComposition objects</span></span>

<span data-ttu-id="08869-142">Stellen Sie sicher, dass Sie die Gruppe von 2D-Transformations Objekten freigeben, wenn Sie Sie nicht mehr benötigen.</span><span class="sxs-lookup"><span data-stu-id="08869-142">Be sure to free the group of 2D transform objects when you no longer need them.</span></span> <span data-ttu-id="08869-143">Im folgenden Beispiel wird das Anwendungs definierte [**saferelease**](/windows/desktop/medfound/saferelease) -Makro aufgerufen, um die Transformations Objekte freizugeben.</span><span class="sxs-lookup"><span data-stu-id="08869-143">The following example calls the application-defined [**SafeRelease**](/windows/desktop/medfound/saferelease) macro to free the transform objects.</span></span>


```C++
// Release the transform objects.
for (int i = 0; i < 3; i++)
{
    SafeRelease(&pTransforms[i]);
}
```



<span data-ttu-id="08869-144">Denken Sie auch daran, das Geräte Objekt, das Kompositions Zielobjekt und die visuellen Elemente freizugeben, bevor die Anwendung beendet wird.</span><span class="sxs-lookup"><span data-stu-id="08869-144">Also remember to free the device object, the composition target object, and the visuals before your application exits.</span></span>

## <a name="complete-example"></a><span data-ttu-id="08869-145">Vollständiges Beispiel</span><span class="sxs-lookup"><span data-stu-id="08869-145">Complete example</span></span>


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



## <a name="related-topics"></a><span data-ttu-id="08869-146">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="08869-146">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="08869-147">Transformationen</span><span class="sxs-lookup"><span data-stu-id="08869-147">Transforms</span></span>](transforms.md)
</dt> </dl>

 

 