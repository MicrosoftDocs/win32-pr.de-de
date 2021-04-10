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
# <a name="how-to-clip-with-a-rectangle-clip-object"></a><span data-ttu-id="9dca9-103">Vorgehensweise beim Abschneiden mit einem Rechteck Clip-Objekt</span><span class="sxs-lookup"><span data-stu-id="9dca9-103">How to clip with a rectangle clip object</span></span>

> [!NOTE]
> <span data-ttu-id="9dca9-104">Für apps unter Windows 10 wird die Verwendung von Windows. UI. Composition-APIs anstelle von directcomposition empfohlen.</span><span class="sxs-lookup"><span data-stu-id="9dca9-104">For apps on Windows 10, we recommend using Windows.UI.Composition APIs instead of DirectComposition.</span></span> <span data-ttu-id="9dca9-105">Weitere Informationen finden Sie unter [modernisieren ihrer Desktop-App mithilfe der visuellen Ebene](/windows/uwp/composition/visual-layer-in-desktop-apps).</span><span class="sxs-lookup"><span data-stu-id="9dca9-105">For more info, see [Modernize your desktop app using the Visual layer](/windows/uwp/composition/visual-layer-in-desktop-apps).</span></span>

<span data-ttu-id="9dca9-106">In diesem Thema wird veranschaulicht, wie ein Rechteck Clip-Objekt verwendet wird, um eine visuelle Struktur oder eine visuelle Struktur zu schneiden</span><span class="sxs-lookup"><span data-stu-id="9dca9-106">This topic demonstrates how to use a rectangle clip object to clip a visual or visual tree.</span></span>

<span data-ttu-id="9dca9-107">Im Beispiel in diesem Thema wird ein rechteckiger Clip definiert, der an der Mausposition zentriert ist, und der Clip wird auf ein visuelles Element angewendet, das im Client Bereich des Kompositions Zielfensters zentriert ist.</span><span class="sxs-lookup"><span data-stu-id="9dca9-107">The example in this topic defines a rectangular clip that is centered at the mouse location, and applies the clip to a visual that is centered in the client area of the composition target window.</span></span> <span data-ttu-id="9dca9-108">Dieser Screenshot zeigt das Ergebnis der Anwendung des Rechteck Clip Objekts auf das visuelle Element.</span><span class="sxs-lookup"><span data-stu-id="9dca9-108">This screen shot shows the result of applying the rectangle clip object to the visual.</span></span>

![Ergebnis der Anwendung eines Rechteck Clip Objekts auf ein visuelles Element](images/clipwithrectangleclipobject.png)

## <a name="what-you-need-to-know"></a><span data-ttu-id="9dca9-110">Was Sie wissen müssen</span><span class="sxs-lookup"><span data-stu-id="9dca9-110">What you need to know</span></span>

### <a name="technologies"></a><span data-ttu-id="9dca9-111">Technologien</span><span class="sxs-lookup"><span data-stu-id="9dca9-111">Technologies</span></span>

-   [<span data-ttu-id="9dca9-112">DirectComposition</span><span class="sxs-lookup"><span data-stu-id="9dca9-112">DirectComposition</span></span>](directcomposition-portal.md)
-   [<span data-ttu-id="9dca9-113">Direct3D 11-Grafik</span><span class="sxs-lookup"><span data-stu-id="9dca9-113">Direct3D 11 Graphics</span></span>](/windows/desktop/direct3d11/atoc-dx-graphics-direct3d-11)
-   [<span data-ttu-id="9dca9-114">DirectX-Grafik Infrastruktur (DXGI)</span><span class="sxs-lookup"><span data-stu-id="9dca9-114">DirectX Graphics Infrastructure (DXGI)</span></span>](/windows/desktop/direct3ddxgi/dx-graphics-dxgi)

### <a name="prerequisites"></a><span data-ttu-id="9dca9-115">Voraussetzungen</span><span class="sxs-lookup"><span data-stu-id="9dca9-115">Prerequisites</span></span>

-   <span data-ttu-id="9dca9-116">C/C++</span><span class="sxs-lookup"><span data-stu-id="9dca9-116">C/C++</span></span>
-   <span data-ttu-id="9dca9-117">Microsoft Win32</span><span class="sxs-lookup"><span data-stu-id="9dca9-117">Microsoft Win32</span></span>
-   <span data-ttu-id="9dca9-118">Component Object Model (COM)</span><span class="sxs-lookup"><span data-stu-id="9dca9-118">Component Object Model (COM)</span></span>

## <a name="instructions"></a><span data-ttu-id="9dca9-119">Anweisungen</span><span class="sxs-lookup"><span data-stu-id="9dca9-119">Instructions</span></span>

### <a name="step-1-initialize-directcomposition-objects"></a><span data-ttu-id="9dca9-120">Schritt 1: Initialisieren von directcomposition-Objekten</span><span class="sxs-lookup"><span data-stu-id="9dca9-120">Step 1: Initialize DirectComposition objects</span></span>

1.  <span data-ttu-id="9dca9-121">Erstellen Sie das Geräte Objekt und das Kompositions Zielobjekt.</span><span class="sxs-lookup"><span data-stu-id="9dca9-121">Create the device object and the composition target object.</span></span>
2.  <span data-ttu-id="9dca9-122">Erstellen Sie ein visuelles Element, legen Sie seinen Inhalt fest, und fügen Sie es der visuellen Struktur hinzu.</span><span class="sxs-lookup"><span data-stu-id="9dca9-122">Create a visual, set its content, and add it to the visual tree.</span></span>

<span data-ttu-id="9dca9-123">Weitere Informationen finden Sie unter [Initialisieren von directcomposition](initialize-directcomposition.md).</span><span class="sxs-lookup"><span data-stu-id="9dca9-123">For more information, see [How to initialize DirectComposition](initialize-directcomposition.md).</span></span>

### <a name="step-2-create-the-rectangle-clip-object"></a><span data-ttu-id="9dca9-124">Schritt 2: Erstellen des Rechteck Clip-Objekts</span><span class="sxs-lookup"><span data-stu-id="9dca9-124">Step 2: Create the rectangle clip object</span></span>

<span data-ttu-id="9dca9-125">Verwenden Sie die [**idcompositiondevice::**](/windows/win32/api/dcomp/nf-dcomp-idcompositiondevice-createrectangleclip) up-Methode, um eine Instanz des Rechteck Clip Objekts zu erstellen.</span><span class="sxs-lookup"><span data-stu-id="9dca9-125">Use the [**IDCompositionDevice::CreateRectangleClip**](/windows/win32/api/dcomp/nf-dcomp-idcompositiondevice-createrectangleclip) method to create an instance of the rectangle clip object.</span></span>


```C++
    HRESULT hr = S_OK;
    
    // Create the rectangle clip object.
    if (m_pClip == NULL)
    {
        hr = m_pDevice->CreateRectangleClip(&m_pClip);
    }
```



### <a name="step-3-set-the-properties-of-the-rectangle-clip-object"></a><span data-ttu-id="9dca9-126">Schritt 3: Festlegen der Eigenschaften des Rechteck Clip Objekts</span><span class="sxs-lookup"><span data-stu-id="9dca9-126">Step 3: Set the properties of the rectangle clip object</span></span>

<span data-ttu-id="9dca9-127">Rufen Sie die Methoden der [**idcompositionrechgleclip**](/windows/win32/api/dcomp/nn-dcomp-idcompositionrectangleclip) -Schnittstelle des Rechteck Clip Objekts auf, um die Eigenschaften des Clip Rechtecks festzulegen.</span><span class="sxs-lookup"><span data-stu-id="9dca9-127">Call the methods of the rectangle clip object's [**IDCompositionRectangleClip**](/windows/win32/api/dcomp/nn-dcomp-idcompositionrectangleclip) interface to set the properties of the clip rectangle.</span></span>

<span data-ttu-id="9dca9-128">Im folgenden Beispiel wird ein Clip Rechteck definiert, das um die aktuelle Mausposition zentriert ist.</span><span class="sxs-lookup"><span data-stu-id="9dca9-128">The following example defines a clip rectangle that is centered around the current mouse location.</span></span> <span data-ttu-id="9dca9-129">Die `m_offsetX` -und-Element `m_offsetY` Variablen enthalten die Werte der OffsetX-Eigenschaft und der OffsetY-Eigenschaft des visuellen Elements.</span><span class="sxs-lookup"><span data-stu-id="9dca9-129">The `m_offsetX` and `m_offsetY` member variables contain the values of the OffsetX and OffsetY properties of the visual.</span></span>


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



<span data-ttu-id="9dca9-130">Beachten Sie, dass die [**idcompositionrechgleclip**](/windows/win32/api/dcomp/nn-dcomp-idcompositionrectangleclip) -Schnittstelle die folgenden Methoden zum Definieren eines Clip Rechtecks mit abgerundeten Ecken umfasst:</span><span class="sxs-lookup"><span data-stu-id="9dca9-130">Note that the [**IDCompositionRectangleClip**](/windows/win32/api/dcomp/nn-dcomp-idcompositionrectangleclip) interface includes the following methods for defining a clip rectangle that has rounded corners:</span></span>

-   <span data-ttu-id="9dca9-131">[**Settopleftradius x**](/windows/win32/api/dcomp/nf-dcomp-idcompositionrectangleclip-settopleftradiusx(float))</span><span class="sxs-lookup"><span data-stu-id="9dca9-131">[**SetTopLeftRadiusX**](/windows/win32/api/dcomp/nf-dcomp-idcompositionrectangleclip-settopleftradiusx(float))</span></span>
-   <span data-ttu-id="9dca9-132">[**Settopleftradius y**](/windows/win32/api/dcomp/nf-dcomp-idcompositionrectangleclip-settopleftradiusy(float))</span><span class="sxs-lookup"><span data-stu-id="9dca9-132">[**SetTopLeftRadiusY**](/windows/win32/api/dcomp/nf-dcomp-idcompositionrectangleclip-settopleftradiusy(float))</span></span>
-   <span data-ttu-id="9dca9-133">[**Settoprightradius x**](/windows/win32/api/dcomp/nf-dcomp-idcompositionrectangleclip-settoprightradiusx(float))</span><span class="sxs-lookup"><span data-stu-id="9dca9-133">[**SetTopRightRadiusX**](/windows/win32/api/dcomp/nf-dcomp-idcompositionrectangleclip-settoprightradiusx(float))</span></span>
-   <span data-ttu-id="9dca9-134">[**Settoprightradius y**](/windows/win32/api/dcomp/nf-dcomp-idcompositionrectangleclip-settoprightradiusy(float))</span><span class="sxs-lookup"><span data-stu-id="9dca9-134">[**SetTopRightRadiusY**](/windows/win32/api/dcomp/nf-dcomp-idcompositionrectangleclip-settoprightradiusy(float))</span></span>

### <a name="step-4-set-the-clip-property-of-the-visual"></a><span data-ttu-id="9dca9-135">Schritt 4: Festlegen der Clip-Eigenschaft des visuellen Elements</span><span class="sxs-lookup"><span data-stu-id="9dca9-135">Step 4: Set the Clip property of the visual</span></span>

<span data-ttu-id="9dca9-136">Verwenden Sie die [**idcompositionvisual:: SetClip**](/windows/win32/api/dcomp/nf-dcomp-idcompositionvisual-setclip(idcompositionclip)) -Methode, um die Clip-Eigenschaft des visuellen Elements dem Rechteck Clip-Objekt zuzuordnen.</span><span class="sxs-lookup"><span data-stu-id="9dca9-136">Use the [**IDCompositionVisual::SetClip**](/windows/win32/api/dcomp/nf-dcomp-idcompositionvisual-setclip(idcompositionclip)) method to associate the Clip property of the visual with the rectangle clip object.</span></span>


```C++
    if (SUCCEEDED(hr))
    {
        // Set the rectangle clip object as the Clip property 
        // of the visual.
        hr = m_pVisual->SetClip(m_pClip);
    }
```



### <a name="step-5-commit-the-composition"></a><span data-ttu-id="9dca9-137">Schritt 5: Commit der Komposition ausführen</span><span class="sxs-lookup"><span data-stu-id="9dca9-137">Step 5: Commit the composition</span></span>

<span data-ttu-id="9dca9-138">Rufen Sie die [**idcompositiondevice:: Commit**](/windows/win32/api/dcomp/nf-dcomp-idcompositiondevice-commit) -Methode auf, um einen Commit für den Batch der Befehle an Microsoft directcomposition zur Verarbeitung auszuführen.</span><span class="sxs-lookup"><span data-stu-id="9dca9-138">Call the [**IDCompositionDevice::Commit**](/windows/win32/api/dcomp/nf-dcomp-idcompositiondevice-commit) method to commit the batch of commands to Microsoft DirectComposition for processing.</span></span> <span data-ttu-id="9dca9-139">Das Ergebnis der Anwendung des Clip Rechtecks wird im Zielfenster angezeigt.</span><span class="sxs-lookup"><span data-stu-id="9dca9-139">The result of applying the clip rectangle appears in the target window.</span></span>


```C++
    if (SUCCEEDED(hr))
    {
        // Commit the visual to be composed and displayed.
        hr = m_pDevice->Commit();  
    }
```



### <a name="step-6-free-the-directcomposition-objects"></a><span data-ttu-id="9dca9-140">Schritt 6: Freigeben der directcomposition-Objekte</span><span class="sxs-lookup"><span data-stu-id="9dca9-140">Step 6: Free the DirectComposition objects</span></span>

<span data-ttu-id="9dca9-141">Stellen Sie sicher, dass Sie das Rechteck Clip-Objekt freigeben, wenn Sie es nicht mehr benötigen, sowie das Geräte Objekt, das Kompositions Zielobjekt und alle visuellen Objekte.</span><span class="sxs-lookup"><span data-stu-id="9dca9-141">Be sure to free the rectangle clip object when you no longer need it, as well as the device object, the composition target object, and any visual objects.</span></span> <span data-ttu-id="9dca9-142">Im folgenden Beispiel wird das Anwendungs definierte [**saferelease**](/windows/desktop/medfound/saferelease) -Makro aufgerufen, um die directcomposition-Objekte freizugeben.</span><span class="sxs-lookup"><span data-stu-id="9dca9-142">The following example calls the application-defined [**SafeRelease**](/windows/desktop/medfound/saferelease) macro to free the DirectComposition objects.</span></span>


```C++
    SafeRelease(&m_pClip);
    SafeRelease(&m_pDevice);
    SafeRelease(&m_pD3D11Device);
    SafeRelease(&m_pCompTarget);
    SafeRelease(&m_pVisual);
    SafeRelease(&m_pSurface);
```



## <a name="related-topics"></a><span data-ttu-id="9dca9-143">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="9dca9-143">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="9dca9-144">Freistellen</span><span class="sxs-lookup"><span data-stu-id="9dca9-144">Clipping</span></span>](clipping.md)
</dt> </dl>

 

 