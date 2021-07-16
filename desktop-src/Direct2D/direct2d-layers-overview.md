---
title: Übersicht über Ebenen
description: Beschreibt die Grundlagen von Direct2D-Ebenen.
ms.assetid: 22d161fb-8470-49cc-a523-309f90643ea9
keywords:
- Direct2D, Ebenen
ms.topic: article
ms.date: 05/31/2018
ms.custom: seodec18
ms.openlocfilehash: 027be097c5c21929f3ccdbaa169a1f3dac55b394
ms.sourcegitcommit: 698ce2d9ba2fa650f2875225d99623995fac246a
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 07/15/2021
ms.locfileid: "114231607"
---
# <a name="layers-overview"></a><span data-ttu-id="f9cb4-104">Übersicht über Ebenen</span><span class="sxs-lookup"><span data-stu-id="f9cb4-104">Layers Overview</span></span>

<span data-ttu-id="f9cb4-105">In dieser Übersicht werden die Grundlagen der Verwendung von Direct2D-Ebenen beschrieben.</span><span class="sxs-lookup"><span data-stu-id="f9cb4-105">This overview describes the basics of using Direct2D layers.</span></span> <span data-ttu-id="f9cb4-106">Der Abschnitt ist wie folgt gegliedert.</span><span class="sxs-lookup"><span data-stu-id="f9cb4-106">It contains the following sections.</span></span>

-   [<span data-ttu-id="f9cb4-107">Was sind Ebenen?</span><span class="sxs-lookup"><span data-stu-id="f9cb4-107">What Are Layers?</span></span>](#what-are-layers)
-   [<span data-ttu-id="f9cb4-108">Ebenen in Windows 8 und höher</span><span class="sxs-lookup"><span data-stu-id="f9cb4-108">Layers in Windows 8 and later</span></span>](#layers-in-windows-8-and-later)
    -   [<span data-ttu-id="f9cb4-109">ID2D1DeviceContext und PushLayer</span><span class="sxs-lookup"><span data-stu-id="f9cb4-109">ID2D1DeviceContext and PushLayer</span></span>](#id2d1devicecontext-and-pushlayer)
    -   [<span data-ttu-id="f9cb4-110">D2D1 \_ LAYER \_ PARAMETERS1 und D2D1 \_ LAYER \_ OPTIONS1</span><span class="sxs-lookup"><span data-stu-id="f9cb4-110">D2D1\_LAYER\_PARAMETERS1 and D2D1\_LAYER\_OPTIONS1</span></span>](/windows)
    -   [<span data-ttu-id="f9cb4-111">Füllmethoden</span><span class="sxs-lookup"><span data-stu-id="f9cb4-111">Blend Modes</span></span>](#blend-modes)
    -   [<span data-ttu-id="f9cb4-112">Interoperation</span><span class="sxs-lookup"><span data-stu-id="f9cb4-112">Interoperation</span></span>](#interoperation)
-   [<span data-ttu-id="f9cb4-113">Erstellen von Ebenen</span><span class="sxs-lookup"><span data-stu-id="f9cb4-113">Creating Layers</span></span>](#creating-layers)
-   [<span data-ttu-id="f9cb4-114">Inhaltsgrenze</span><span class="sxs-lookup"><span data-stu-id="f9cb4-114">Content Bounds</span></span>](#content-bounds)
-   [<span data-ttu-id="f9cb4-115">Geometrische Masken</span><span class="sxs-lookup"><span data-stu-id="f9cb4-115">Geometric Masks</span></span>](#geometric-masks)
-   [<span data-ttu-id="f9cb4-116">Deckkraftmasken</span><span class="sxs-lookup"><span data-stu-id="f9cb4-116">Opacity Masks</span></span>](#opacity-masks)
-   [<span data-ttu-id="f9cb4-117">Alternativen zu Ebenen</span><span class="sxs-lookup"><span data-stu-id="f9cb4-117">Alternatives to Layers</span></span>](#alternatives-to-layers)
-   [<span data-ttu-id="f9cb4-118">Beschneiden einer beliebigen Form</span><span class="sxs-lookup"><span data-stu-id="f9cb4-118">Clipping an arbitrary shape</span></span>](#clipping-an-arbitrary-shape)
    -   [<span data-ttu-id="f9cb4-119">An der Achse ausgerichtete Clips</span><span class="sxs-lookup"><span data-stu-id="f9cb4-119">Axis aligned clips</span></span>](#axis-aligned-clips)
-   [<span data-ttu-id="f9cb4-120">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="f9cb4-120">Related topics</span></span>](#related-topics)

## <a name="what-are-layers"></a><span data-ttu-id="f9cb4-121">Was sind Ebenen?</span><span class="sxs-lookup"><span data-stu-id="f9cb4-121">What Are Layers?</span></span>

<span data-ttu-id="f9cb4-122">Ebenen, die durch [**ID2D1Layer-Objekte dargestellt**](/windows/win32/api/d2d1/nn-d2d1-id2d1layer) werden, ermöglichen es einer Anwendung, eine Gruppe von Zeichnungsvorgängen zu bearbeiten.</span><span class="sxs-lookup"><span data-stu-id="f9cb4-122">Layers, represented by [**ID2D1Layer**](/windows/win32/api/d2d1/nn-d2d1-id2d1layer) objects, enable an application to manipulate a group of drawing operations.</span></span> <span data-ttu-id="f9cb4-123">Sie verwenden eine Ebene, indem Sie sie auf ein Renderziel "pushen".</span><span class="sxs-lookup"><span data-stu-id="f9cb4-123">You use a layer by "pushing" it onto a render target.</span></span> <span data-ttu-id="f9cb4-124">Nachfolgende Zeichnungsvorgänge durch das Renderziel werden an die Ebene geleitet.</span><span class="sxs-lookup"><span data-stu-id="f9cb4-124">Subsequent drawing operations by the render target are directed to the layer.</span></span> <span data-ttu-id="f9cb4-125">Nachdem Sie mit der Ebene fertig sind, "popen" Sie die Ebene aus dem Renderziel, wodurch der Inhalt der Ebene wieder zum Renderziel zusammengesetzt wird.</span><span class="sxs-lookup"><span data-stu-id="f9cb4-125">After you're finished with the layer, you "pop" the layer from the render target, which composites the layer's content back to the render target.</span></span>

<span data-ttu-id="f9cb4-126">Wie Pinsel sind Ebenen geräteabhängige Ressourcen, die von Renderzielen erstellt werden.</span><span class="sxs-lookup"><span data-stu-id="f9cb4-126">Like brushes, layers are device-dependent resources created by render targets.</span></span> <span data-ttu-id="f9cb4-127">Ebenen können auf jedem Renderziel in derselben Ressourcendomäne verwendet werden, die das Renderziel enthält, mit dem es erstellt wurde.</span><span class="sxs-lookup"><span data-stu-id="f9cb4-127">Layers can be used on any render target in the same resource domain that contains the render target that created it.</span></span> <span data-ttu-id="f9cb4-128">Eine Ebenenressource kann jedoch nur von einem Renderziel gleichzeitig verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="f9cb4-128">However, a layer resource can only be used by one render target at a time.</span></span> <span data-ttu-id="f9cb4-129">Weitere Informationen zu Ressourcen finden Sie unter [Übersicht über Ressourcen.](resources-and-resource-domains.md)</span><span class="sxs-lookup"><span data-stu-id="f9cb4-129">For more information about resources, see the [Resources Overview](resources-and-resource-domains.md).</span></span>

<span data-ttu-id="f9cb4-130">Ebenen bieten zwar eine leistungsstarke Renderingtechnik zum Erzeugen interessanter Effekte, aber eine übermäßige Anzahl von Ebenen in einer Anwendung kann sich aufgrund der verschiedenen Kosten für die Verwaltung von Ebenen und Ebenenressourcen negativ auf die Leistung auswirken.</span><span class="sxs-lookup"><span data-stu-id="f9cb4-130">Although layers offer a powerful rendering technique for producing interesting effects, excessive number of layers in an application can adversely affect its performance, because of the various costs associated with managing layers and layer resources.</span></span> <span data-ttu-id="f9cb4-131">Beispielsweise sind die Kosten für das Auffüllen oder Löschen der Schicht und das anschließende Wiederverblenden der Schicht erforderlich, insbesondere bei Hardware mit höherer Ebene.</span><span class="sxs-lookup"><span data-stu-id="f9cb4-131">For example, there is the cost of filling or clearing the layer and then blending it back, especially on higher-end hardware.</span></span> <span data-ttu-id="f9cb4-132">Anschließend sind die Kosten für die Verwaltung der Ebenenressourcen an.</span><span class="sxs-lookup"><span data-stu-id="f9cb4-132">Then, there is the cost of managing the layer resources.</span></span> <span data-ttu-id="f9cb4-133">Wenn Sie diese häufig neu auffinden, sind die resultierenden Stags für die GPU das größte Problem.</span><span class="sxs-lookup"><span data-stu-id="f9cb4-133">If you reallocate these frequently, the resulting stalls against the GPU will be the most significant problem.</span></span> <span data-ttu-id="f9cb4-134">Versuchen Sie beim Entwerfen Ihrer Anwendung, die Wiederverwendung von Ebenenressourcen zu maximieren.</span><span class="sxs-lookup"><span data-stu-id="f9cb4-134">When you design your application, try to maximize reusing layer resources.</span></span>

## <a name="layers-in-windows-8-and-later"></a><span data-ttu-id="f9cb4-135">Ebenen in Windows 8 und höher</span><span class="sxs-lookup"><span data-stu-id="f9cb4-135">Layers in Windows 8 and later</span></span>

<span data-ttu-id="f9cb4-136">Windows 8 neue ebenenbezogene APIs eingeführt, die die Leistung von vereinfachen, verbessern und Ebenen Features hinzufügen.</span><span class="sxs-lookup"><span data-stu-id="f9cb4-136">Windows 8 introduced new layer related APIs that simplify, improve the performance of, and add features to layers.</span></span>

### <a name="id2d1devicecontext-and-pushlayer"></a><span data-ttu-id="f9cb4-137">ID2D1DeviceContext und PushLayer</span><span class="sxs-lookup"><span data-stu-id="f9cb4-137">ID2D1DeviceContext and PushLayer</span></span>

<span data-ttu-id="f9cb4-138">Die [**ID2D1DeviceContext-Schnittstelle**](/windows/win32/api/d2d1_1/nn-d2d1_1-id2d1devicecontext) wird von der [**ID2D1RenderTarget-Schnittstelle**](/windows/win32/api/d2d1/nn-d2d1-id2d1rendertarget) abgeleitet und ist der Schlüssel zum Anzeigen von Direct2D-Inhalt in Windows 8. Weitere Informationen zu dieser Schnittstelle finden Sie unter Geräte und [Gerätekontexte](devices-and-device-contexts.md).</span><span class="sxs-lookup"><span data-stu-id="f9cb4-138">The [**ID2D1DeviceContext**](/windows/win32/api/d2d1_1/nn-d2d1_1-id2d1devicecontext) interface is derived from the [**ID2D1RenderTarget**](/windows/win32/api/d2d1/nn-d2d1-id2d1rendertarget) interface and is key to displaying Direct2D content in Windows 8, for more information about this interface see [Devices and Device Contexts](devices-and-device-contexts.md).</span></span> <span data-ttu-id="f9cb4-139">Mit der Gerätekontextschnittstelle können Sie das Aufrufen der [**CreateLayer-Methode**](/windows/desktop/api/d2d1/nf-d2d1-id2d1rendertarget-createlayer(id2d1layer)) überspringen und dann NULL an die [**ID2D1DeviceContext::P ushLayer-Methode**](/windows/win32/api/d2d1_1/nf-d2d1_1-id2d1devicecontext-pushlayer(constd2d1_layer_parameters1_id2d1layer)) übergeben.</span><span class="sxs-lookup"><span data-stu-id="f9cb4-139">With the device context interface, you can skip calling the [**CreateLayer**](/windows/desktop/api/d2d1/nf-d2d1-id2d1rendertarget-createlayer(id2d1layer)) method and then pass NULL to the [**ID2D1DeviceContext::PushLayer**](/windows/win32/api/d2d1_1/nf-d2d1_1-id2d1devicecontext-pushlayer(constd2d1_layer_parameters1_id2d1layer)) method.</span></span> <span data-ttu-id="f9cb4-140">Direct2D verwaltet die Ebenenressource automatisch und kann Ressourcen zwischen Ebenen und Effektdiagrammen freigeben.</span><span class="sxs-lookup"><span data-stu-id="f9cb4-140">Direct2D automatically manages the layer resource and can share resources between layers and effect graphs.</span></span>

### <a name="d2d1_layer_parameters1-and-d2d1_layer_options1"></a><span data-ttu-id="f9cb4-141">D2D1 \_ LAYER \_ PARAMETERS1 und D2D1 \_ LAYER \_ OPTIONS1</span><span class="sxs-lookup"><span data-stu-id="f9cb4-141">D2D1\_LAYER\_PARAMETERS1 and D2D1\_LAYER\_OPTIONS1</span></span>

<span data-ttu-id="f9cb4-142">Die [**D2D1 \_ LAYER \_ PARAMETERS1-Struktur**](/windows/desktop/api/d2d1_1/ns-d2d1_1-d2d1_layer_parameters1) ist identisch mit [**D2D1 \_ LAYER \_ PARAMETERS,**](/windows/desktop/api/d2d1/ns-d2d1-d2d1_layer_parameters)mit der Ausnahme, dass das letzte Member der Struktur jetzt eine [**D2D1 \_ LAYER \_ OPTIONS1-Enumeration**](/windows/desktop/api/d2d1_1/ne-d2d1_1-d2d1_layer_options1) ist.</span><span class="sxs-lookup"><span data-stu-id="f9cb4-142">The [**D2D1\_LAYER\_PARAMETERS1**](/windows/desktop/api/d2d1_1/ns-d2d1_1-d2d1_layer_parameters1) structure is the same as [**D2D1\_LAYER\_PARAMETERS**](/windows/desktop/api/d2d1/ns-d2d1-d2d1_layer_parameters), except the final member of the structure is now a [**D2D1\_LAYER\_OPTIONS1**](/windows/desktop/api/d2d1_1/ne-d2d1_1-d2d1_layer_options1) enumeration.</span></span>

<span data-ttu-id="f9cb4-143">[**D2D1 \_ LAYER \_ OPTIONS1**](/windows/desktop/api/d2d1_1/ne-d2d1_1-d2d1_layer_options1) verfügt über keine ClearType-Option und verfügt über zwei verschiedene Optionen, mit denen Sie die Leistung verbessern können:</span><span class="sxs-lookup"><span data-stu-id="f9cb4-143">[**D2D1\_LAYER\_OPTIONS1**](/windows/desktop/api/d2d1_1/ne-d2d1_1-d2d1_layer_options1) has no ClearType option and has two different options that you can use to improve performance:</span></span>

-   <span data-ttu-id="f9cb4-144">[**D2D1 \_ LAYER \_ OPTIONS1 \_ INITIALIZE FROM \_ \_ BACKGROUND:**](/windows/desktop/api/d2d1_1/ne-d2d1_1-d2d1_layer_options1)Direct2D rendert Primitive auf der Ebene, ohne sie mit transparentem Schwarz zu löschen.</span><span class="sxs-lookup"><span data-stu-id="f9cb4-144">[**D2D1\_LAYER\_OPTIONS1\_INITIALIZE\_FROM\_BACKGROUND**](/windows/desktop/api/d2d1_1/ne-d2d1_1-d2d1_layer_options1): Direct2D renders primitives to the layer without clearing it with transparent black.</span></span> <span data-ttu-id="f9cb4-145">Dies ist nicht die Standardeinstellung, führt aber in den meisten Fällen zu einer besseren Leistung.</span><span class="sxs-lookup"><span data-stu-id="f9cb4-145">This is not the default, but in most cases results in better performance.</span></span>

-   <span data-ttu-id="f9cb4-146">[**D2D1 \_ LAYER \_ OPTIONS1 \_ IGNORE \_ ALPHA**](/windows/desktop/api/d2d1_1/ne-d2d1_1-d2d1_layer_options1): Wenn die zugrunde liegende Oberfläche auf [**D2D1 \_ ALPHA MODE \_ \_ IGNORE**](/windows/desktop/api/dcommon/ne-dcommon-d2d1_alpha_mode)festgelegt ist, kann Direct2D mit dieser Option verhindern, dass der Alphakanal der Ebene geändert wird.</span><span class="sxs-lookup"><span data-stu-id="f9cb4-146">[**D2D1\_LAYER\_OPTIONS1\_IGNORE\_ALPHA**](/windows/desktop/api/d2d1_1/ne-d2d1_1-d2d1_layer_options1): if the underlying surface is set to [**D2D1\_ALPHA\_MODE\_IGNORE**](/windows/desktop/api/dcommon/ne-dcommon-d2d1_alpha_mode), this option lets Direct2D avoid modifying the alpha channel of the layer.</span></span> <span data-ttu-id="f9cb4-147">Verwenden Sie dies nicht in anderen Fällen.</span><span class="sxs-lookup"><span data-stu-id="f9cb4-147">Do not use this in other cases.</span></span>

### <a name="blend-modes"></a><span data-ttu-id="f9cb4-148">Füllmethoden</span><span class="sxs-lookup"><span data-stu-id="f9cb4-148">Blend Modes</span></span>

<span data-ttu-id="f9cb4-149">Ab Windows 8 verfügt der Gerätekontext über einen [**primitiven**](/windows/desktop/api/D2d1_1/ne-d2d1_1-d2d1_primitive_blend) Überblendmodus, der bestimmt, wie die einzelnen Primitiven mit der Zieloberfläche kombiniert werden.</span><span class="sxs-lookup"><span data-stu-id="f9cb4-149">Starting in Windows 8, the device context has a [**primitive blend mode**](/windows/desktop/api/D2d1_1/ne-d2d1_1-d2d1_primitive_blend) that determines how each primitive is blended with the target surface.</span></span> <span data-ttu-id="f9cb4-150">Dieser Modus gilt auch für Ebenen, wenn Sie die [**PushLayer-Methode**](/windows/win32/api/d2d1_1/nf-d2d1_1-id2d1devicecontext-pushlayer(constd2d1_layer_parameters1_id2d1layer)) aufrufen.</span><span class="sxs-lookup"><span data-stu-id="f9cb4-150">This mode also applies to layers when you call the [**PushLayer**](/windows/win32/api/d2d1_1/nf-d2d1_1-id2d1devicecontext-pushlayer(constd2d1_layer_parameters1_id2d1layer)) method.</span></span>

<span data-ttu-id="f9cb4-151">Wenn Sie beispielsweise eine Ebene zum Beschneiden von Primitiven mit Transparenz verwenden, legen Sie den [**D2D1 \_ PRIMITIVE \_ BLEND \_ COPY-Modus**](/windows/desktop/api/D2d1_1/ne-d2d1_1-d2d1_primitive_blend) für den Gerätekontext fest, um die richtigen Ergebnisse zu erzielen.</span><span class="sxs-lookup"><span data-stu-id="f9cb4-151">For example, if you are using a layer to clip primitives with transparency set the [**D2D1\_PRIMITIVE\_BLEND\_COPY**](/windows/desktop/api/D2d1_1/ne-d2d1_1-d2d1_primitive_blend) mode on the device context for proper results.</span></span> <span data-ttu-id="f9cb4-152">Durch den Kopiermodus interpoliert der Gerätekontext alle vier Farbkanäle, einschließlich des Alphakanals, jedes Pixels mit dem Inhalt der Zieloberfläche gemäß der geometrischen Maske der Ebene.</span><span class="sxs-lookup"><span data-stu-id="f9cb4-152">The copy mode makes the device context linear interpolate all 4 color channels, including the alpha channel, of each pixel with the contents of the target surface according to the geometric mask of the layer.</span></span>

### <a name="interoperation"></a><span data-ttu-id="f9cb4-153">Interoperation</span><span class="sxs-lookup"><span data-stu-id="f9cb4-153">Interoperation</span></span>

<span data-ttu-id="f9cb4-154">Ab Windows 8 unterstützt Direct2D die Interoperation mit Direct3D und GDI, während eine Ebene oder ein Clip mit pusht wird.</span><span class="sxs-lookup"><span data-stu-id="f9cb4-154">Starting in Windows 8, Direct2D supports interoperation with Direct3D and GDI while a layer or clip is pushed.</span></span> <span data-ttu-id="f9cb4-155">Sie rufen [**ID2D1GdiInteropRenderTarget::GetDC**](/windows/win32/api/d2d1/nf-d2d1-id2d1gdiinteroprendertarget-getdc) auf, während eine Ebene zur Interoperabilität mit GDI pushed wird.</span><span class="sxs-lookup"><span data-stu-id="f9cb4-155">You call [**ID2D1GdiInteropRenderTarget::GetDC**](/windows/win32/api/d2d1/nf-d2d1-id2d1gdiinteroprendertarget-getdc) while a layer is pushed to interoperate with GDI.</span></span> <span data-ttu-id="f9cb4-156">Sie rufen [**ID2D1DeviceContext::Flush**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-flush) auf und rendern dann auf der zugrunde liegenden Oberfläche, um mit Direct3D zu zusammenarbeiten.</span><span class="sxs-lookup"><span data-stu-id="f9cb4-156">You call [**ID2D1DeviceContext::Flush**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-flush) and then render to the underlying surface to interoperate with Direct3D.</span></span> <span data-ttu-id="f9cb4-157">Es liegt in Ihrer Verantwortung, innerhalb der Ebene zu rendern oder mit Direct3D oder GDI zu beschneiden.</span><span class="sxs-lookup"><span data-stu-id="f9cb4-157">It is your responsibility to render inside the layer or clip with Direct3D or GDI.</span></span> <span data-ttu-id="f9cb4-158">Wenn Sie versuchen, außerhalb der Ebene zu rendern oder die Ergebnisse zu beschneiden, sind die Ergebnisse nicht definiert.</span><span class="sxs-lookup"><span data-stu-id="f9cb4-158">If you try to render outside the layer or clip the results are undefined.</span></span>

## <a name="creating-layers"></a><span data-ttu-id="f9cb4-159">Erstellen von Ebenen</span><span class="sxs-lookup"><span data-stu-id="f9cb4-159">Creating Layers</span></span>

<span data-ttu-id="f9cb4-160">Das Arbeiten mit Ebenen erfordert Vertrautheit mit den [**Methoden CreateLayer,**](/windows/desktop/api/d2d1/nf-d2d1-id2d1rendertarget-createlayer(id2d1layer)) [**PushLayer**](/windows/win32/api/d2d1_1/nf-d2d1_1-id2d1devicecontext-pushlayer(constd2d1_layer_parameters1_id2d1layer))und [**PopLayer**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-poplayer) und der [**Struktur D2D1 \_ LAYER \_ PARAMETERS,**](/windows/desktop/api/d2d1/ns-d2d1-d2d1_layer_parameters) die eine Reihe von parametrischen Daten enthält, die definieren, wie die Ebene verwendet werden kann.</span><span class="sxs-lookup"><span data-stu-id="f9cb4-160">Working with layers requires familiarity with the [**CreateLayer**](/windows/desktop/api/d2d1/nf-d2d1-id2d1rendertarget-createlayer(id2d1layer)), [**PushLayer**](/windows/win32/api/d2d1_1/nf-d2d1_1-id2d1devicecontext-pushlayer(constd2d1_layer_parameters1_id2d1layer)), and [**PopLayer**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-poplayer) methods, and the [**D2D1\_LAYER\_PARAMETERS**](/windows/desktop/api/d2d1/ns-d2d1-d2d1_layer_parameters) structure, which contains a set of parametric data that defines how the layer can be used.</span></span> <span data-ttu-id="f9cb4-161">In der folgenden Liste werden die Methoden und die Struktur beschrieben.</span><span class="sxs-lookup"><span data-stu-id="f9cb4-161">The following list describes the methods and structure.</span></span>

-   <span data-ttu-id="f9cb4-162">Rufen Sie die [**CreateLayer-Methode**](/windows/desktop/api/d2d1/nf-d2d1-id2d1rendertarget-createlayer(id2d1layer)) auf, um eine Ebenenressource zu erstellen.</span><span class="sxs-lookup"><span data-stu-id="f9cb4-162">Call the [**CreateLayer**](/windows/desktop/api/d2d1/nf-d2d1-id2d1rendertarget-createlayer(id2d1layer)) method to create a layer resource.</span></span>
    > [!Note]  
    > <span data-ttu-id="f9cb4-163">Ab Windows 8 können Sie das Aufrufen der [**CreateLayer-Methode**](/windows/desktop/api/d2d1/nf-d2d1-id2d1rendertarget-createlayer(id2d1layer)) überspringen und dann NULL an die [**PushLayer-Methode**](/windows/win32/api/d2d1_1/nf-d2d1_1-id2d1devicecontext-pushlayer(constd2d1_layer_parameters1_id2d1layer)) auf der [**ID2D1DeviceContext-Schnittstelle**](/windows/win32/api/d2d1_1/nn-d2d1_1-id2d1devicecontext) übergeben.</span><span class="sxs-lookup"><span data-stu-id="f9cb4-163">Starting in Windows 8, you can skip calling the [**CreateLayer**](/windows/desktop/api/d2d1/nf-d2d1-id2d1rendertarget-createlayer(id2d1layer)) method and then pass NULL to the [**PushLayer**](/windows/win32/api/d2d1_1/nf-d2d1_1-id2d1devicecontext-pushlayer(constd2d1_layer_parameters1_id2d1layer)) method on the [**ID2D1DeviceContext**](/windows/win32/api/d2d1_1/nn-d2d1_1-id2d1devicecontext) interface.</span></span> <span data-ttu-id="f9cb4-164">Dies ist einfacher und ermöglicht Direct2D die automatische Verwaltung der Ebenenressource und die gemeinsame Nutzung von Ressourcen zwischen Ebenen und Effektdiagrammen.</span><span class="sxs-lookup"><span data-stu-id="f9cb4-164">This is simpler and allows Direct2D to automatically manage the layer resource and share resources between layers and effect graphs.</span></span>

     

-   <span data-ttu-id="f9cb4-165">Nachdem das Zeichnen des Renderziels begonnen hat (nachdem die [**BeginDraw-Methode**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-begindraw) aufgerufen wurde), können Sie die [**PushLayer-Methode**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-pushlayer(constd2d1_layer_parameters__id2d1layer)) verwenden.</span><span class="sxs-lookup"><span data-stu-id="f9cb4-165">After render target has begun drawing (after its [**BeginDraw**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-begindraw) method has been called), you can use the [**PushLayer**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-pushlayer(constd2d1_layer_parameters__id2d1layer)) method.</span></span> <span data-ttu-id="f9cb4-166">Die **PushLayer-Methode** fügt dem Renderziel die angegebene Ebene hinzu, sodass das Ziel alle nachfolgenden Zeichnungsvorgänge empfängt, bis [**PopLayer**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-poplayer) aufgerufen wird.</span><span class="sxs-lookup"><span data-stu-id="f9cb4-166">The **PushLayer** method adds the specified layer to the render target, so that the target receives all subsequent drawing operations until [**PopLayer**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-poplayer) is called.</span></span> <span data-ttu-id="f9cb4-167">Diese Methode verwendet ein [**ID2D1Layer-Objekt,**](/windows/win32/api/d2d1/nn-d2d1-id2d1layer) das durch Aufrufen von [**CreateLayer**](/windows/desktop/api/d2d1/nf-d2d1-id2d1rendertarget-createlayer(id2d1layer)) zurückgegeben wird, und *ein layerParameters-Objekt* in der [**D2D1 \_ LAYER \_ PARAMETERS-Struktur.**](/windows/desktop/api/d2d1/ns-d2d1-d2d1_layer_parameters)</span><span class="sxs-lookup"><span data-stu-id="f9cb4-167">This method takes an [**ID2D1Layer**](/windows/win32/api/d2d1/nn-d2d1-id2d1layer) object returned by calling [**CreateLayer**](/windows/desktop/api/d2d1/nf-d2d1-id2d1rendertarget-createlayer(id2d1layer)) and an *layerParameters* in the [**D2D1\_LAYER\_PARAMETERS**](/windows/desktop/api/d2d1/ns-d2d1-d2d1_layer_parameters) structure.</span></span> <span data-ttu-id="f9cb4-168">In der folgenden Tabelle werden die Felder der -Struktur beschrieben.</span><span class="sxs-lookup"><span data-stu-id="f9cb4-168">The following table describes the fields of the structure.</span></span> 

    | <span data-ttu-id="f9cb4-169">Feld</span><span class="sxs-lookup"><span data-stu-id="f9cb4-169">Field</span></span>                 | <span data-ttu-id="f9cb4-170">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="f9cb4-170">Description</span></span>|
    |-----------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
    | <span data-ttu-id="f9cb4-171">**contentBounds**</span><span class="sxs-lookup"><span data-stu-id="f9cb4-171">**contentBounds**</span></span>     | <span data-ttu-id="f9cb4-172">Die Inhaltsgrenze der Ebene.</span><span class="sxs-lookup"><span data-stu-id="f9cb4-172">The content bounds of the layer.</span></span> <span data-ttu-id="f9cb4-173">Inhalt wird außerhalb dieser Grenzen nicht gerendert.</span><span class="sxs-lookup"><span data-stu-id="f9cb4-173">Content won't render outside these bounds.</span></span> <span data-ttu-id="f9cb4-174">Dieser Parameter ist standardmäßig auf [**InfiniteRect festgelegt.**](/windows/desktop/api/d2d1Helper/nf-d2d1helper-infiniterect)</span><span class="sxs-lookup"><span data-stu-id="f9cb4-174">This parameter defaults to [**InfiniteRect**](/windows/desktop/api/d2d1Helper/nf-d2d1helper-infiniterect).</span></span> <span data-ttu-id="f9cb4-175">Wenn der Standardwert verwendet wird, werden die Inhaltsgrenze effektiv als Begrenzungen des Renderziels verwendet.</span><span class="sxs-lookup"><span data-stu-id="f9cb4-175">When the default value is used, the content bounds are effectively taken to be the bounds of the render target.</span></span> |
    | <span data-ttu-id="f9cb4-176">**geometricMask**</span><span class="sxs-lookup"><span data-stu-id="f9cb4-176">**geometricMask**</span></span>     | <span data-ttu-id="f9cb4-177">(Optional) Der bereich, der durch eine [**ID2D1Geometry**](/windows/win32/api/d2d1/nn-d2d1-id2d1geometry)definiert wird, auf den die Ebene abgeschnitten werden soll.</span><span class="sxs-lookup"><span data-stu-id="f9cb4-177">(Optional) The area, defined by an [**ID2D1Geometry**](/windows/win32/api/d2d1/nn-d2d1-id2d1geometry), to which the layer should be clipped.</span></span> <span data-ttu-id="f9cb4-178">Wird auf **NULL** festgelegt, wenn die Ebene nicht auf eine Geometrie abgeschnitten werden soll.</span><span class="sxs-lookup"><span data-stu-id="f9cb4-178">Set to **NULL** if the layer shouldn't be clipped to a geometry.</span></span> |
    | <span data-ttu-id="f9cb4-179">**maskAntialiasMode**</span><span class="sxs-lookup"><span data-stu-id="f9cb4-179">**maskAntialiasMode**</span></span> | <span data-ttu-id="f9cb4-180">Ein -Wert, der den Antialiasingmodus für die geometrische Maske angibt, die durch das **feld geometricMask angegeben** wird.</span><span class="sxs-lookup"><span data-stu-id="f9cb4-180">A value that specifies the antialiasing mode for the geometric mask specified by the **geometricMask** field.</span></span> |
    | <span data-ttu-id="f9cb4-181">**maskTransform**</span><span class="sxs-lookup"><span data-stu-id="f9cb4-181">**maskTransform**</span></span>     | <span data-ttu-id="f9cb4-182">Ein -Wert, der die Transformation angibt, die beim Erstellen der Ebene auf die geometrische Maske angewendet wird.</span><span class="sxs-lookup"><span data-stu-id="f9cb4-182">A value that specifies the transform that is applied to the geometric mask when composing the layer.</span></span> <span data-ttu-id="f9cb4-183">Dies ist relativ zur Welttransformation.</span><span class="sxs-lookup"><span data-stu-id="f9cb4-183">This is relative to the world transform.</span></span>  |
    | <span data-ttu-id="f9cb4-184">**Deckkraft**</span><span class="sxs-lookup"><span data-stu-id="f9cb4-184">**opacity**</span></span>           | <span data-ttu-id="f9cb4-185">Der Deckkraftwert der Ebene.</span><span class="sxs-lookup"><span data-stu-id="f9cb4-185">The opacity value of the layer.</span></span> <span data-ttu-id="f9cb4-186">Die Deckkraft jeder Ressource in der Ebene wird beim Zusammenordnen mit dem Ziel mit diesem Wert multipliziert.</span><span class="sxs-lookup"><span data-stu-id="f9cb4-186">The opacity of each resource in the layer is multiplied with this value when compositing to the target.</span></span>  |
    | <span data-ttu-id="f9cb4-187">**opacityBrush**</span><span class="sxs-lookup"><span data-stu-id="f9cb4-187">**opacityBrush**</span></span>      | <span data-ttu-id="f9cb4-188">(Optional) Ein Pinsel, der verwendet wird, um die Deckkraft der Ebene zu ändern.</span><span class="sxs-lookup"><span data-stu-id="f9cb4-188">(Optional) A brush that is used to modify the opacity of the layer.</span></span> <span data-ttu-id="f9cb4-189">Der Pinsel wird der Ebene zugeordnet, und der Alphakanal jedes zugeordneten Pinselpixels wird mit dem entsprechenden Ebenenpixel multipliziert.</span><span class="sxs-lookup"><span data-stu-id="f9cb4-189">The brush is mapped to the layer, and the alpha channel of each mapped brush pixel is multiplied against the corresponding layer pixel.</span></span> <span data-ttu-id="f9cb4-190">Wird auf **NULL** festgelegt, wenn die Schicht keine Deckkraftmaske haben soll.</span><span class="sxs-lookup"><span data-stu-id="f9cb4-190">Set to **NULL** if the layer shouldn't have an opacity mask.</span></span>   |
    | <span data-ttu-id="f9cb4-191">**layerOptions**</span><span class="sxs-lookup"><span data-stu-id="f9cb4-191">**layerOptions**</span></span>      | <span data-ttu-id="f9cb4-192">Ein -Wert, der angibt, ob die Ebene text mit ClearType-Antialiasing rendern möchte.</span><span class="sxs-lookup"><span data-stu-id="f9cb4-192">A value that specifies whether the layer intends to render text with ClearType antialiasing.</span></span> <span data-ttu-id="f9cb4-193">Dieser Parameter ist standardmäßig deaktiviert.</span><span class="sxs-lookup"><span data-stu-id="f9cb4-193">This parameter defaults to off.</span></span> <span data-ttu-id="f9cb4-194">Wenn Sie es aktivieren, funktioniert ClearType ordnungsgemäß, führt jedoch zu einer etwas langsameren Renderinggeschwindigkeit.</span><span class="sxs-lookup"><span data-stu-id="f9cb4-194">Turning it on enables ClearType to work correctly, but it results in slightly slower rendering speed.</span></span>    |

    

     

    > [!Note]  
    > <span data-ttu-id="f9cb4-195">Ab Windows 8 können Sie nicht mit ClearType in einer Ebene rendern, daher sollte der **layerOptions-Parameter** immer [**auf D2D1 \_ LAYER OPTIONS NONE festgelegt \_ \_ werden.**](/windows/desktop/api/d2d1/ne-d2d1-d2d1_layer_options)</span><span class="sxs-lookup"><span data-stu-id="f9cb4-195">Starting in Windows 8, you cannot render with ClearType in a layer, so the **layerOptions** parameter should always be set to [**D2D1\_LAYER\_OPTIONS\_NONE**](/windows/desktop/api/d2d1/ne-d2d1-d2d1_layer_options)</span></span>

     

    <span data-ttu-id="f9cb4-196">Der Einfachheit halber stellt Direct2D die [**D2D1::LayerParameters-Methode**](/windows/desktop/api/d2d1helper/nf-d2d1helper-layerparameters) zum Erstellen von [**D2D1 \_ LAYER \_ PARAMETERS-Strukturen**](/windows/desktop/api/d2d1/ns-d2d1-d2d1_layer_parameters) zur Verfügung.</span><span class="sxs-lookup"><span data-stu-id="f9cb4-196">For convenience, Direct2D provides the [**D2D1::LayerParameters**](/windows/desktop/api/d2d1helper/nf-d2d1helper-layerparameters) method to help you create [**D2D1\_LAYER\_PARAMETERS**](/windows/desktop/api/d2d1/ns-d2d1-d2d1_layer_parameters) structures.</span></span>

-   <span data-ttu-id="f9cb4-197">Um den Inhalt der Ebene in das Renderziel zu zusammengesetzt, rufen Sie die [**PopLayer-Methode**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-poplayer) auf.</span><span class="sxs-lookup"><span data-stu-id="f9cb4-197">To composite the contents of the layer into the render target, call the [**PopLayer**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-poplayer) method.</span></span> <span data-ttu-id="f9cb4-198">Sie müssen die **PopLayer-Methode aufrufen,** bevor Sie die [**EndDraw-Methode**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-enddraw) aufrufen.</span><span class="sxs-lookup"><span data-stu-id="f9cb4-198">You must call the **PopLayer** method before you call the [**EndDraw**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-enddraw) method.</span></span>

<span data-ttu-id="f9cb4-199">Das folgende Beispiel zeigt die Verwendung von [**CreateLayer,**](/windows/desktop/api/d2d1/nf-d2d1-id2d1rendertarget-createlayer(id2d1layer)) [**PushLayer**](/windows/win32/api/d2d1_1/nf-d2d1_1-id2d1devicecontext-pushlayer(constd2d1_layer_parameters1_id2d1layer))und [**PopLayer.**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-poplayer)</span><span class="sxs-lookup"><span data-stu-id="f9cb4-199">The following example shows how to use [**CreateLayer**](/windows/desktop/api/d2d1/nf-d2d1-id2d1rendertarget-createlayer(id2d1layer)), [**PushLayer**](/windows/win32/api/d2d1_1/nf-d2d1_1-id2d1devicecontext-pushlayer(constd2d1_layer_parameters1_id2d1layer)), and [**PopLayer**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-poplayer).</span></span> <span data-ttu-id="f9cb4-200">Alle Felder in der [**Struktur D2D1 \_ LAYER \_ PARAMETERS**](/windows/desktop/api/d2d1/ns-d2d1-d2d1_layer_parameters) werden auf ihre Standardwerte festgelegt, mit Ausnahme **von opacityBrush**, das auf [**id2D1RadialGradientBrush festgelegt ist.**](/windows/win32/api/d2d1/nn-d2d1-id2d1radialgradientbrush)</span><span class="sxs-lookup"><span data-stu-id="f9cb4-200">All fields in the [**D2D1\_LAYER\_PARAMETERS**](/windows/desktop/api/d2d1/ns-d2d1-d2d1_layer_parameters) structure are set to their defaults, except **opacityBrush**, which is set to an [**ID2D1RadialGradientBrush**](/windows/win32/api/d2d1/nn-d2d1-id2d1radialgradientbrush).</span></span>


```C++
// Create a layer.
ID2D1Layer *pLayer = NULL;
hr = pRT->CreateLayer(NULL, &pLayer);

if (SUCCEEDED(hr))
{
    pRT->SetTransform(D2D1::Matrix3x2F::Translation(300, 250));

    // Push the layer with the content bounds.
    pRT->PushLayer(
        D2D1::LayerParameters(
            D2D1::InfiniteRect(),
            NULL,
            D2D1_ANTIALIAS_MODE_PER_PRIMITIVE,
            D2D1::IdentityMatrix(),
            1.0,
            m_pRadialGradientBrush,
            D2D1_LAYER_OPTIONS_NONE),
        pLayer
        );

    pRT->DrawBitmap(m_pBambooBitmap, D2D1::RectF(0, 0, 190, 127));

    pRT->FillRectangle(
        D2D1::RectF(25.f, 25.f, 50.f, 50.f), 
        m_pSolidColorBrush
        );
    pRT->FillRectangle(
        D2D1::RectF(50.f, 50.f, 75.f, 75.f),
        m_pSolidColorBrush
        ); 
    pRT->FillRectangle(
        D2D1::RectF(75.f, 75.f, 100.f, 100.f),
        m_pSolidColorBrush
        );    
 
    pRT->PopLayer();
}
SafeRelease(&pLayer);
```



<span data-ttu-id="f9cb4-201">Code wurde in diesem Beispiel weggelassen.</span><span class="sxs-lookup"><span data-stu-id="f9cb4-201">Code has been omitted from this example.</span></span>

<span data-ttu-id="f9cb4-202">Beachten Sie, dass beim Aufrufen [**von PushLayer**](/windows/win32/api/d2d1_1/nf-d2d1_1-id2d1devicecontext-pushlayer(constd2d1_layer_parameters1_id2d1layer)) und [**PopLayer**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-poplayer)sichergestellt ist, dass **jedes PushLayer-Paar** über einen entsprechenden **PopLayer-Aufruf** verfügt.</span><span class="sxs-lookup"><span data-stu-id="f9cb4-202">Note that when you call [**PushLayer**](/windows/win32/api/d2d1_1/nf-d2d1_1-id2d1devicecontext-pushlayer(constd2d1_layer_parameters1_id2d1layer)) and [**PopLayer**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-poplayer), ensure that each **PushLayer** has a matching **PopLayer** call.</span></span> <span data-ttu-id="f9cb4-203">Wenn es mehr **PopLayer-Aufrufe** als **PushLayer-Aufrufe** gibt, wird das Renderziel in einen Fehlerzustand gesetzt.</span><span class="sxs-lookup"><span data-stu-id="f9cb4-203">If there are more **PopLayer** calls than **PushLayer** calls, the render target is placed into an error state.</span></span> <span data-ttu-id="f9cb4-204">Wenn [**Flush**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-flush) aufgerufen wird, bevor alle ausstehenden Ebenen aus dem Pop aufgeblendet werden, wird das Renderziel in einen Fehlerzustand gesetzt und gibt einen Fehler zurück.</span><span class="sxs-lookup"><span data-stu-id="f9cb4-204">If [**Flush**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-flush) is called before all outstanding layers are popped, the render target is placed into an error state and returns an error.</span></span> <span data-ttu-id="f9cb4-205">Um den Fehlerzustand zu löschen, verwenden [**Sie EndDraw**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-enddraw).</span><span class="sxs-lookup"><span data-stu-id="f9cb4-205">To clear the error state, use [**EndDraw**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-enddraw).</span></span>

## <a name="content-bounds"></a><span data-ttu-id="f9cb4-206">Inhaltsgrenze</span><span class="sxs-lookup"><span data-stu-id="f9cb4-206">Content Bounds</span></span>

<span data-ttu-id="f9cb4-207">**ContentBounds legt** den Grenzwert für das, was auf die Ebene gezeichnet werden soll, fest.</span><span class="sxs-lookup"><span data-stu-id="f9cb4-207">The **contentBounds** sets the limit of what is to be drawn to the layer.</span></span> <span data-ttu-id="f9cb4-208">Nur die Dinge innerhalb der Inhaltsgrenze werden wieder mit dem Renderziel zusammengesetzt.</span><span class="sxs-lookup"><span data-stu-id="f9cb4-208">Only those things within the content bounds are composited back to the render target.</span></span>

<span data-ttu-id="f9cb4-209">Das folgende Beispiel zeigt, wie **contentBounds** angegeben wird, damit das ursprüngliche Bild an die Inhaltsgrenze mit der oberen linken Ecke bei (10, 108) und der unteren rechten Ecke bei (121, 177) abgeschnitten wird.</span><span class="sxs-lookup"><span data-stu-id="f9cb4-209">The example that follows shows how to specify **contentBounds** so that the original image is clipped to the content bounds with the upper-left corner at (10, 108) and the lower-right corner at (121, 177).</span></span> <span data-ttu-id="f9cb4-210">Die folgende Abbildung zeigt das ursprüngliche Bild und das Ergebnis der Beschneidung des Bilds an die Inhaltsgrenze.</span><span class="sxs-lookup"><span data-stu-id="f9cb4-210">The following illustration shows the original image and the result of clipping the image to the content bounds.</span></span>

![Abbildung der Inhaltsgrenze eines originalen Bilds und des resultierenden abgeschnittenen Bilds](images/layers-contentbounds.png)


```C++
HRESULT DemoApp::RenderWithLayerWithContentBounds(ID2D1RenderTarget *pRT)
{
    
    HRESULT hr = S_OK;

    // Create a layer.
    ID2D1Layer *pLayer = NULL;
    hr = pRT->CreateLayer(NULL, &pLayer);

    if (SUCCEEDED(hr))
    {
        pRT->SetTransform(D2D1::Matrix3x2F::Translation(300, 0));

        // Push the layer with the content bounds.
        pRT->PushLayer(
            D2D1::LayerParameters(D2D1::RectF(10, 108, 121, 177)),
            pLayer
            );

        pRT->DrawBitmap(m_pWaterBitmap, D2D1::RectF(0, 0, 128, 192));
        pRT->PopLayer();
    }

    SafeRelease(&pLayer);

    return hr;
    
}
```



<span data-ttu-id="f9cb4-212">Code wurde in diesem Beispiel weggelassen.</span><span class="sxs-lookup"><span data-stu-id="f9cb4-212">Code has been omitted from this example.</span></span>

> [!Note]
>
> <span data-ttu-id="f9cb4-213">Das resultierende abgeschnittene Bild wird weiter beeinflusst, wenn Sie eine **geometrischeMaske angeben.**</span><span class="sxs-lookup"><span data-stu-id="f9cb4-213">The resulting clipped image is further affected if you specify a **geometricMask**.</span></span> <span data-ttu-id="f9cb4-214">Weitere Informationen [finden Sie im](#geometric-masks) Abschnitt Geometrische Masken.</span><span class="sxs-lookup"><span data-stu-id="f9cb4-214">See the [Geometric Masks](#geometric-masks) section for more information.</span></span>

 

## <a name="geometric-masks"></a><span data-ttu-id="f9cb4-215">Geometrische Masken</span><span class="sxs-lookup"><span data-stu-id="f9cb4-215">Geometric Masks</span></span>

<span data-ttu-id="f9cb4-216">Eine geometrische Maske ist ein Clip oder ein Cutout, definiert durch ein [**ID2D1Geometry-Objekt,**](/windows/win32/api/d2d1/nn-d2d1-id2d1geometry) das eine Ebene maskiert, wenn sie von einem Renderziel gezeichnet wird.</span><span class="sxs-lookup"><span data-stu-id="f9cb4-216">A geometric mask is a clip or a cutout, defined by an [**ID2D1Geometry**](/windows/win32/api/d2d1/nn-d2d1-id2d1geometry) object, that masks a layer when it is drawn by a render target.</span></span> <span data-ttu-id="f9cb4-217">Sie können das **feld geometricMask** der [**Struktur D2D1 \_ LAYER \_ PARAMETERS**](/windows/desktop/api/d2d1/ns-d2d1-d2d1_layer_parameters) verwenden, um die Ergebnisse in einer Geometrie zu maskieren.</span><span class="sxs-lookup"><span data-stu-id="f9cb4-217">You can use the **geometricMask** field of the [**D2D1\_LAYER\_PARAMETERS**](/windows/desktop/api/d2d1/ns-d2d1-d2d1_layer_parameters) structure to mask the results to a geometry.</span></span> <span data-ttu-id="f9cb4-218">Wenn Sie beispielsweise ein Bild anzeigen möchten, das mit einem Blockbuchstaben "A" maskiert ist, können Sie zuerst eine Geometrie erstellen, die den Blockbuchstaben "A" darstellt, und diese Geometrie als geometrische Maske für eine Ebene verwenden.</span><span class="sxs-lookup"><span data-stu-id="f9cb4-218">For example, if you want to display an image masked by a block letter "A", you can first create a geometry representing the block letter "A" and use that geometry as a geometric mask for a layer.</span></span> <span data-ttu-id="f9cb4-219">Nach dem Pushen der Ebene können Sie dann das Bild zeichnen.</span><span class="sxs-lookup"><span data-stu-id="f9cb4-219">Then, after pushing the layer, you can draw the image.</span></span> <span data-ttu-id="f9cb4-220">Wenn Sie die Ebene poppen, wird das Bild auf die Form "A" des Blockbuchstabens abgeschnitten.</span><span class="sxs-lookup"><span data-stu-id="f9cb4-220">Popping the layer results in the image being clipped to the block letter "A" shape.</span></span>

<span data-ttu-id="f9cb4-221">Das folgende Beispiel zeigt, wie Sie eine [**ID2D1PathGeometry**](/windows/win32/api/d2d1/nn-d2d1-id2d1pathgeometry) erstellen, die eine Form eines Mountain enthält, und dann die Pfadgeometrie an [**PushLayer übergeben.**](/windows/win32/api/d2d1_1/nf-d2d1_1-id2d1devicecontext-pushlayer(constd2d1_layer_parameters1_id2d1layer))</span><span class="sxs-lookup"><span data-stu-id="f9cb4-221">The example that follows shows how to create an [**ID2D1PathGeometry**](/windows/win32/api/d2d1/nn-d2d1-id2d1pathgeometry) containing a shape of a mountain and then pass the path geometry to the [**PushLayer**](/windows/win32/api/d2d1_1/nf-d2d1_1-id2d1devicecontext-pushlayer(constd2d1_layer_parameters1_id2d1layer)).</span></span> <span data-ttu-id="f9cb4-222">Anschließend werden eine Bitmap und Quadrate ge zeichnet.</span><span class="sxs-lookup"><span data-stu-id="f9cb4-222">It then draws a bitmap and squares.</span></span> <span data-ttu-id="f9cb4-223">Wenn nur eine Bitmap in der Ebene gerendert werden soll, verwenden Sie [**FillGeometry**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-fillgeometry) mit einem geklammerten Bitmappinsel, um die Effizienz zu erhöhen.</span><span class="sxs-lookup"><span data-stu-id="f9cb4-223">If there is only a bitmap in the layer to render, use [**FillGeometry**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-fillgeometry) with a clamped bitmap brush for efficiency.</span></span> <span data-ttu-id="f9cb4-224">Die folgende Abbildung zeigt die Ausgabe des Beispiels.</span><span class="sxs-lookup"><span data-stu-id="f9cb4-224">The following illustration shows the output from the example.</span></span>

![Abbildung eines Bilds eines Blatts und des resultierenden Bilds, nachdem eine geometrische Maske eines Mountain angewendet wurde](images/layers-bitmapmask.png)

<span data-ttu-id="f9cb4-226">Im ersten Beispiel wird die Geometrie definiert, die als Maske verwendet werden soll.</span><span class="sxs-lookup"><span data-stu-id="f9cb4-226">The first example defines the geometry to be used as a mask.</span></span>


```C++
hr = m_pD2DFactory->CreatePathGeometry(&m_pPathGeometry);
    
if(SUCCEEDED(hr))
{
    ID2D1GeometrySink *pSink = NULL;
    // Write to the path geometry using the geometry sink.
    hr = m_pPathGeometry->Open(&pSink);

    if (SUCCEEDED(hr))
    {
        pSink->SetFillMode(D2D1_FILL_MODE_WINDING);
        pSink->BeginFigure(
            D2D1::Point2F(0, 90),
            D2D1_FIGURE_BEGIN_FILLED
            );

        D2D1_POINT_2F points[7] = {
           D2D1::Point2F(35, 30),
           D2D1::Point2F(50, 50),
           D2D1::Point2F(70, 45),
           D2D1::Point2F(105, 90),
           D2D1::Point2F(130, 90),
           D2D1::Point2F(150, 60),
           D2D1::Point2F(170, 90)
           };

        pSink->AddLines(points, 7);
        pSink->EndFigure(D2D1_FIGURE_END_CLOSED);
        hr = pSink->Close();
    }
    SafeRelease(&pSink);
       }
```



<span data-ttu-id="f9cb4-227">Im nächsten Beispiel wird die Geometrie als Maske für die Ebene verwendet.</span><span class="sxs-lookup"><span data-stu-id="f9cb4-227">The next example uses the geometry as a mask for the layer.</span></span>


```C++
HRESULT DemoApp::RenderWithLayerWithGeometricMask(ID2D1RenderTarget *pRT)
{
    
    HRESULT hr;

    // Create a layer.
    ID2D1Layer *pLayer = NULL;
    hr = pRT->CreateLayer(NULL, &pLayer);

    if (SUCCEEDED(hr))
    {
        pRT->SetTransform(D2D1::Matrix3x2F::Translation(300, 450));

        pRT->PushLayer(
            D2D1::LayerParameters(D2D1::InfiniteRect(), m_pPathGeometry),
            pLayer
            );

        pRT->DrawBitmap(m_pLeafBitmap, D2D1::RectF(0, 0, 198, 132));

        pRT->FillRectangle(
            D2D1::RectF(50.f, 50.f, 75.f, 75.f), 
            m_pSolidColorBrush
            ); 
        pRT->FillRectangle(
            D2D1::RectF(75.f, 75.f, 100.f, 100.f),
            m_pSolidColorBrush
            );        

        pRT->PopLayer();
    }

    SafeRelease(&pLayer);

    return hr;
    
}
```



<span data-ttu-id="f9cb4-228">Code wurde in diesem Beispiel weggelassen.</span><span class="sxs-lookup"><span data-stu-id="f9cb4-228">Code has been omitted from this example.</span></span>

> [!Note]
>
> <span data-ttu-id="f9cb4-229">Wenn Sie eine **geometricMask** angeben, können Sie im Allgemeinen den Standardwert [**InfiniteRect**](/windows/desktop/api/d2d1Helper/nf-d2d1helper-infiniterect)für **contentBounds verwenden.**</span><span class="sxs-lookup"><span data-stu-id="f9cb4-229">In general, if you specify a **geometricMask**, you can use the default value, [**InfiniteRect**](/windows/desktop/api/d2d1Helper/nf-d2d1helper-infiniterect), for the **contentBounds**.</span></span>
>
> <span data-ttu-id="f9cb4-230">Wenn **contentBounds** NULL und **geometricMask** nicht NULL ist, sind die Inhaltsgrenze effektiv die Grenzen der geometrischen Maske, nachdem die Maskentransformation angewendet wurde.</span><span class="sxs-lookup"><span data-stu-id="f9cb4-230">If **contentBounds** is NULL, and **geometricMask** is non-NULL, then the content bounds are effectively the bounds of the geometric mask after the mask transform is applied.</span></span>
>
> <span data-ttu-id="f9cb4-231">Wenn **contentBounds** nicht NULL und **geometricMask** nicht NULL ist, wird die transformierte geometrische Maske effektiv an Inhaltsgrenze abgeschnitten, und es wird davon ausgegangen, dass die Inhaltsgrenze unendlich ist.</span><span class="sxs-lookup"><span data-stu-id="f9cb4-231">If **contentBounds** is non-NULL, and **geometricMask** is non-NULL, then the transformed geometric mask is effectively clipped against content bounds and the content bounds are assumed to be infinite.</span></span>

 

## <a name="opacity-masks"></a><span data-ttu-id="f9cb4-232">Deckkraftmasken</span><span class="sxs-lookup"><span data-stu-id="f9cb4-232">Opacity Masks</span></span>

<span data-ttu-id="f9cb4-233">Eine Deckkraftmaske ist eine Maske, die von einem Pinsel oder einer Bitmap beschrieben wird und auf ein anderes Objekt angewendet wird, um dieses Objekt teilweise oder vollständig transparent zu machen.</span><span class="sxs-lookup"><span data-stu-id="f9cb4-233">An opacity mask is a mask, described by a brush or bitmap, that is applied to another object to make that object partially or completely transparent.</span></span> <span data-ttu-id="f9cb4-234">Sie ermöglicht die Verwendung des Alphakanals eines Pinsels als Inhaltsmaske.</span><span class="sxs-lookup"><span data-stu-id="f9cb4-234">It allows the use of the alpha channel of a brush to be used as a content mask.</span></span> <span data-ttu-id="f9cb4-235">Sie können z. B. einen radialen Farbverlaufspinsel definieren, der von undurchsichtig bis transparent variiert, um einen Sterneffekt zu erstellen.</span><span class="sxs-lookup"><span data-stu-id="f9cb4-235">For example, you can define a radial gradient brush that varies from opaque to transparent to create a vignette effect.</span></span>

<span data-ttu-id="f9cb4-236">Im folgenden Beispiel wird [**id2D1RadialGradientBrush**](/windows/win32/api/d2d1/nn-d2d1-id2d1radialgradientbrush) (*m \_ pRadialGradientBrush*) als Deckkraftmaske verwendet.</span><span class="sxs-lookup"><span data-stu-id="f9cb4-236">The example that follows uses an [**ID2D1RadialGradientBrush**](/windows/win32/api/d2d1/nn-d2d1-id2d1radialgradientbrush) (*m\_pRadialGradientBrush*) as an opacity mask.</span></span> <span data-ttu-id="f9cb4-237">Anschließend werden eine Bitmap und Quadrate ge zeichnet.</span><span class="sxs-lookup"><span data-stu-id="f9cb4-237">It then draws a bitmap and squares.</span></span> <span data-ttu-id="f9cb4-238">Wenn nur eine Bitmap in der Ebene gerendert werden soll, verwenden Sie [**FillGeometry**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-fillgeometry) mit einem geklammerten Bitmappinsel, um die Effizienz zu erhöhen.</span><span class="sxs-lookup"><span data-stu-id="f9cb4-238">If there is only a bitmap in the layer to render, use [**FillGeometry**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-fillgeometry) with a clamped bitmap brush for efficiency.</span></span> <span data-ttu-id="f9cb4-239">Die folgende Abbildung zeigt die Ausgabe dieses Beispiels.</span><span class="sxs-lookup"><span data-stu-id="f9cb4-239">The following illustration shows the output from this example.</span></span>

![Abbildung eines Bilds von Strukturen und des resultierenden Bilds, nachdem eine Deckkraftmaske angewendet wurde](images/layers-opacitymask.png)


```C++
HRESULT DemoApp::RenderWithLayerWithOpacityMask(ID2D1RenderTarget *pRT)
{   

    HRESULT hr = S_OK;

    // Create a layer.
    ID2D1Layer *pLayer = NULL;
    hr = pRT->CreateLayer(NULL, &pLayer);

    if (SUCCEEDED(hr))
    {
        pRT->SetTransform(D2D1::Matrix3x2F::Translation(300, 250));

        // Push the layer with the content bounds.
        pRT->PushLayer(
            D2D1::LayerParameters(
                D2D1::InfiniteRect(),
                NULL,
                D2D1_ANTIALIAS_MODE_PER_PRIMITIVE,
                D2D1::IdentityMatrix(),
                1.0,
                m_pRadialGradientBrush,
                D2D1_LAYER_OPTIONS_NONE),
            pLayer
            );

        pRT->DrawBitmap(m_pBambooBitmap, D2D1::RectF(0, 0, 190, 127));

        pRT->FillRectangle(
            D2D1::RectF(25.f, 25.f, 50.f, 50.f), 
            m_pSolidColorBrush
            );
        pRT->FillRectangle(
            D2D1::RectF(50.f, 50.f, 75.f, 75.f),
            m_pSolidColorBrush
            ); 
        pRT->FillRectangle(
            D2D1::RectF(75.f, 75.f, 100.f, 100.f),
            m_pSolidColorBrush
            );    
 
        pRT->PopLayer();
    }
    SafeRelease(&pLayer);
   
    return hr;
    
}
```



<span data-ttu-id="f9cb4-241">Code wurde in diesem Beispiel weggelassen.</span><span class="sxs-lookup"><span data-stu-id="f9cb4-241">Code has been omitted from this example.</span></span>

> [!Note]  
> <span data-ttu-id="f9cb4-242">In diesem Beispiel wird eine Ebene verwendet, um eine Deckkraftmaske auf ein einzelnes Objekt anzuwenden, um das Beispiel so einfach wie möglich zu halten.</span><span class="sxs-lookup"><span data-stu-id="f9cb4-242">This example uses a layer to apply an opacity mask to a single object to keep the example as simple as possible.</span></span> <span data-ttu-id="f9cb4-243">Beim Anwenden einer Deckkraftmaske auf ein einzelnes Objekt ist es effizienter, die [**FillOpacityMask-**](id2d1rendertarget-fillopacitymask.md) oder [**FillGeometry-Methoden**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-fillgeometry) anstelle einer Ebene zu verwenden.</span><span class="sxs-lookup"><span data-stu-id="f9cb4-243">When applying an opacity mask to a single object, its more efficient to use the [**FillOpacityMask**](id2d1rendertarget-fillopacitymask.md) or [**FillGeometry**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-fillgeometry) methods, rather than a layer.</span></span>

 

<span data-ttu-id="f9cb4-244">Anweisungen zum Anwenden einer Deckkraftmaske ohne Verwendung einer Ebene finden Sie in der Übersicht über [Deckkraftmasken.](opacity-masks-overview.md)</span><span class="sxs-lookup"><span data-stu-id="f9cb4-244">For instructions on how to apply an opacity mask without using a layer, see the [Opacity Masks Overview](opacity-masks-overview.md).</span></span>

## <a name="alternatives-to-layers"></a><span data-ttu-id="f9cb4-245">Alternativen zu Ebenen</span><span class="sxs-lookup"><span data-stu-id="f9cb4-245">Alternatives to Layers</span></span>

<span data-ttu-id="f9cb4-246">Wie bereits erwähnt, kann sich eine übermäßige Anzahl von Ebenen negativ auf die Leistung Ihrer Anwendung auswirken.</span><span class="sxs-lookup"><span data-stu-id="f9cb4-246">As mentioned earlier, excessive number of layers can adversely affect the performance of your application.</span></span> <span data-ttu-id="f9cb4-247">Um die Leistung zu verbessern, vermeiden Sie die Verwendung von Ebenen, wann immer dies möglich ist. verwenden Sie stattdessen ihre Alternativen.</span><span class="sxs-lookup"><span data-stu-id="f9cb4-247">To improve performance, avoid using layers whenever possible; instead use their alternatives.</span></span> <span data-ttu-id="f9cb4-248">Das folgende Codebeispiel zeigt, wie [**PushAxisAlignedClip**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-pushaxisalignedclip(constd2d1_rect_f_d2d1_antialias_mode)) und [**PopAxisAlignedClip**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-popaxisalignedclip) verwendet werden, um einen Bereich zu beschneiden, als Alternative zur Verwendung einer Ebene mit Inhaltsgrenze.</span><span class="sxs-lookup"><span data-stu-id="f9cb4-248">The following code example shows how to use [**PushAxisAlignedClip**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-pushaxisalignedclip(constd2d1_rect_f_d2d1_antialias_mode)) and [**PopAxisAlignedClip**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-popaxisalignedclip) to clip a region, as an alternative to using a layer with content bounds.</span></span>


```C++
pRT->PushAxisAlignedClip(
    D2D1::RectF(20, 20, 100, 100),
    D2D1_ANTIALIAS_MODE_PER_PRIMITIVE
    );

pRT->FillRectangle(D2D1::RectF(0, 0, 200, 133), m_pOriginalBitmapBrush);
pRT->PopAxisAlignedClip();
```



<span data-ttu-id="f9cb4-249">Verwenden Sie auf ähnliche Weise [**FillGeometry**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-fillgeometry) mit einem geklammerten Bitmappinsel als Alternative zur Verwendung einer Ebene mit einer Deckkraftmaske, wenn nur ein Inhalt in der Ebene gerendert werden soll, wie im folgenden Beispiel gezeigt.</span><span class="sxs-lookup"><span data-stu-id="f9cb4-249">Similarly, use [**FillGeometry**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-fillgeometry) with a clamped bitmap brush as an alternative to using a layer with an opacity mask when there is only one content in the layer to render, as shown in the following example.</span></span>


```C++
        m_pRenderTarget->FillGeometry(
            m_pRectGeo, 
            m_pLinearFadeFlowersBitmapBrush, 
            m_pLinearGradientBrush
            );
```



<span data-ttu-id="f9cb4-250">Als Alternative zur Verwendung einer Ebene mit einer geometrischen Maske sollten Sie eine Bitmapmaske verwenden, um einen Bereich zu beschneiden, wie im folgenden Beispiel gezeigt.</span><span class="sxs-lookup"><span data-stu-id="f9cb4-250">As an alternative to using a layer with a geometric mask, consider using a bitmap mask to clip a region, as shown in the following example.</span></span>


```C++
// D2D1_ANTIALIAS_MODE_ALIASED must be set for FillOpacityMask
// to function properly.
m_pRenderTarget->SetAntialiasMode(D2D1_ANTIALIAS_MODE_ALIASED);

m_pRenderTarget->FillOpacityMask(
    m_pBitmapMask,
    m_pOriginalBitmapBrush,
    D2D1_OPACITY_MASK_CONTENT_GRAPHICS,
    &rcBrushRect,
    NULL
    );

m_pRenderTarget->SetAntialiasMode(D2D1_ANTIALIAS_MODE_PER_PRIMITIVE);

```



<span data-ttu-id="f9cb4-251">Wenn Sie die Deckkraft auf ein einzelnes Primitiv anwenden möchten, sollten Sie schließlich die Deckkraft in die Pinselfarbe multiplizieren und dann den Primitiv rendern.</span><span class="sxs-lookup"><span data-stu-id="f9cb4-251">Lastly, if you want to apply opacity to a single primitive, you should multiply the opacity into the into the brush color and then render the primitive.</span></span> <span data-ttu-id="f9cb4-252">Sie benötigen keine Ebenen- oder Deckkraftmaskenbitmap.</span><span class="sxs-lookup"><span data-stu-id="f9cb4-252">You do not need a layer or an opacity mask bitmap.</span></span>


```C++
float opacity = 0.9f;

ID2D1SolidColorBrush *pBrush = NULL;
hr = pCompatibleRenderTarget->CreateSolidColorBrush(
    D2D1::ColorF(D2D1::ColorF(0.93f, 0.94f, 0.96f, 1.0f * opacity)),
    &pBrush
    );

m_pRenderTarget->FillRectangle(
    D2D1::RectF(50.0f, 50.0f, 75.0f, 75.0f), 
    pBrush
    ); 
```



## <a name="clipping-an-arbitrary-shape"></a><span data-ttu-id="f9cb4-253">Beschneiden einer beliebigen Form</span><span class="sxs-lookup"><span data-stu-id="f9cb4-253">Clipping an arbitrary shape</span></span>

<span data-ttu-id="f9cb4-254">Die Abbildung zeigt das Ergebnis der Anwendung eines Clips auf ein Bild.</span><span class="sxs-lookup"><span data-stu-id="f9cb4-254">The figure here shows the result of applying a clip to an image.</span></span>

![Ein Bild, das ein Beispiel für ein Bild vor und nach einem Clip zeigt.](images/clip.png)

<span data-ttu-id="f9cb4-256">Sie können dieses Ergebnis erhalten, indem Sie Ebenen mit einer Geometriemaske oder die [**FillGeometry-Methode**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-fillgeometry) mit einem Deckkraftpinsel verwenden.</span><span class="sxs-lookup"><span data-stu-id="f9cb4-256">You can get this result by using layers with a geometry mask or the [**FillGeometry**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-fillgeometry) method with an opacity brush.</span></span>

<span data-ttu-id="f9cb4-257">Hier sehen Sie ein Beispiel, das eine Ebene verwendet:</span><span class="sxs-lookup"><span data-stu-id="f9cb4-257">Here's an example that uses a layer:</span></span>


```C++
// Call PushLayer() and pass in the clipping geometry.
m_d2dContext->PushLayer(
    D2D1::LayerParameters(
        boundsRect,
        geometricMask));
```



<span data-ttu-id="f9cb4-258">Hier sehen Sie ein Beispiel, in dem die [**FillGeometry-Methode verwendet**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-fillgeometry) wird:</span><span class="sxs-lookup"><span data-stu-id="f9cb4-258">Here's an example that uses the [**FillGeometry**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-fillgeometry) method:</span></span>


```C++
// Create an opacity bitmap and render content.
m_d2dContext->CreateBitmap(size, nullptr, 0,
    D2D1::BitmapProperties(
        D2D1_BITMAP_OPTIONS_TARGET,
        D2D1::PixelFormat(
            DXGI_FORMAT_A8_UNORM,
            D2D1_ALPHA_MODE_PREMULTIPLIED),
        dpiX, dpiY),
    &opacityBitmap);

m_d2dContext->SetTarget(opacityBitmap.Get());
m_d2dContext->BeginDraw();
…
m_d2dContext->EndDraw();

// Create an opacity brush from the opacity bitmap.
m_d2dContext->CreateBitmapBrush(opacityBitmap.Get(),
    D2D1::BitmapBrushProperties(),
    D2D1::BrushProperties(),
    &bitmapBrush);

// Call the FillGeometry method and pass in the clip geometry and the opacity brush
m_d2dContext->FillGeometry( 
    clipGeometry.Get(),
    brush.Get(),
    opacityBrush.Get()); 
```



<span data-ttu-id="f9cb4-259">Wenn Sie in diesem Codebeispiel die PushLayer-Methode aufrufen, übergeben Sie keine von der App erstellte Ebene.</span><span class="sxs-lookup"><span data-stu-id="f9cb4-259">In this code example, when you call the PushLayer method, you don't pass in an app created layer.</span></span> <span data-ttu-id="f9cb4-260">Direct2D erstellt eine Ebene für Sie.</span><span class="sxs-lookup"><span data-stu-id="f9cb4-260">Direct2D creates a layer for you.</span></span> <span data-ttu-id="f9cb4-261">Direct2D kann die Zuordnung und Zerstörung dieser Ressource ohne Beteiligung der App verwalten.</span><span class="sxs-lookup"><span data-stu-id="f9cb4-261">Direct2D is able to manage the allocation and destruction of this resource without any involvement from the app.</span></span> <span data-ttu-id="f9cb4-262">Dadurch kann Direct2D Ebenen intern wiederverwenden und Optimierungen der Ressourcenverwaltung anwenden.</span><span class="sxs-lookup"><span data-stu-id="f9cb4-262">This allows Direct2D to reuse layers internally and apply resource management optimizations.</span></span>

> [!Note]  
> <span data-ttu-id="f9cb4-263">In Windows 8 viele Optimierungen an der Verwendung von Ebenen vorgenommen, und es wird empfohlen, nach Möglichkeit Ebenen-APIs anstelle von [**FillGeometry**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-fillgeometry) zu verwenden.</span><span class="sxs-lookup"><span data-stu-id="f9cb4-263">In Windows 8 many optimizations have been made to the usage of layers and we recommend you try using layer APIs instead of [**FillGeometry**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-fillgeometry) whenever possible.</span></span>

 

### <a name="axis-aligned-clips"></a><span data-ttu-id="f9cb4-264">An der Achse ausgerichtete Clips</span><span class="sxs-lookup"><span data-stu-id="f9cb4-264">Axis aligned clips</span></span>

<span data-ttu-id="f9cb4-265">Wenn der bereich, der abgeschnitten werden soll, an der Achse der Zeichenoberfläche ausgerichtet ist, anstatt willkürlich.</span><span class="sxs-lookup"><span data-stu-id="f9cb4-265">If the region to be clipped is aligned to the axis of the drawing surface, instead of arbitrary.</span></span> <span data-ttu-id="f9cb4-266">Dieser Fall eignet sich für die Verwendung eines Cliprechtecks anstelle einer Ebene.</span><span class="sxs-lookup"><span data-stu-id="f9cb4-266">This case is suited for using a clip rectangle instead of a layer.</span></span> <span data-ttu-id="f9cb4-267">Die Leistungssteigerung ist für die Geometrie mit Aliasen höher als bei der Geometrie mit Antialiasing.</span><span class="sxs-lookup"><span data-stu-id="f9cb4-267">The performance gain is more for aliased geometry than antialiased geometry.</span></span> <span data-ttu-id="f9cb4-268">Weitere Informationen zu an der Achse ausgerichteten Clips finden Sie im [**Thema PushAxisAlignedClip.**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-pushaxisalignedclip(constd2d1_rect_f__d2d1_antialias_mode))</span><span class="sxs-lookup"><span data-stu-id="f9cb4-268">For more info on axis aligned clips, see the [**PushAxisAlignedClip**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-pushaxisalignedclip(constd2d1_rect_f__d2d1_antialias_mode)) topic.</span></span>

## <a name="related-topics"></a><span data-ttu-id="f9cb4-269">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="f9cb4-269">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="f9cb4-270">Direct2D-Referenz</span><span class="sxs-lookup"><span data-stu-id="f9cb4-270">Direct2D Reference</span></span>](reference.md)
</dt> </dl>

 

 