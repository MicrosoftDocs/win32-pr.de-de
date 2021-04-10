---
title: Übersicht über Schichten
description: Beschreibt die Grundlagen von Direct2D Ebenen.
ms.assetid: 22d161fb-8470-49cc-a523-309f90643ea9
keywords:
- Direct2D, Ebenen
ms.topic: article
ms.date: 05/31/2018
ms.custom: seodec18
ms.openlocfilehash: 0e86b32296718a975ebabccd5fc4ef0ee30cf289
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "103948945"
---
# <a name="layers-overview"></a><span data-ttu-id="6401d-104">Übersicht über Schichten</span><span class="sxs-lookup"><span data-stu-id="6401d-104">Layers Overview</span></span>

<span data-ttu-id="6401d-105">In dieser Übersicht werden die Grundlagen der Verwendung von Direct2D Ebenen beschrieben.</span><span class="sxs-lookup"><span data-stu-id="6401d-105">This overview describes the basics of using Direct2D layers.</span></span> <span data-ttu-id="6401d-106">Der Abschnitt ist wie folgt gegliedert.</span><span class="sxs-lookup"><span data-stu-id="6401d-106">It contains the following sections.</span></span>

-   [<span data-ttu-id="6401d-107">Was sind Ebenen?</span><span class="sxs-lookup"><span data-stu-id="6401d-107">What Are Layers?</span></span>](#what-are-layers)
-   [<span data-ttu-id="6401d-108">Schichten in Windows 8 und höher</span><span class="sxs-lookup"><span data-stu-id="6401d-108">Layers in Windows 8 and later</span></span>](#layers-in-windows-8-and-later)
    -   [<span data-ttu-id="6401d-109">ID2D1DeviceContext und pushlayer</span><span class="sxs-lookup"><span data-stu-id="6401d-109">ID2D1DeviceContext and PushLayer</span></span>](#id2d1devicecontext-and-pushlayer)
    -   [<span data-ttu-id="6401d-110">D2D1 \_ Layer \_ PARAMETERS1 und D2D1 \_ Layer \_ OPTIONS1</span><span class="sxs-lookup"><span data-stu-id="6401d-110">D2D1\_LAYER\_PARAMETERS1 and D2D1\_LAYER\_OPTIONS1</span></span>](/windows)
    -   [<span data-ttu-id="6401d-111">Füllmethoden</span><span class="sxs-lookup"><span data-stu-id="6401d-111">Blend Modes</span></span>](#blend-modes)
    -   [<span data-ttu-id="6401d-112">Interoperation</span><span class="sxs-lookup"><span data-stu-id="6401d-112">Interoperation</span></span>](#interoperation)
-   [<span data-ttu-id="6401d-113">Erstellen von Ebenen</span><span class="sxs-lookup"><span data-stu-id="6401d-113">Creating Layers</span></span>](#creating-layers)
-   [<span data-ttu-id="6401d-114">Inhalts Begrenzungen</span><span class="sxs-lookup"><span data-stu-id="6401d-114">Content Bounds</span></span>](#content-bounds)
-   [<span data-ttu-id="6401d-115">Geometrische Masken</span><span class="sxs-lookup"><span data-stu-id="6401d-115">Geometric Masks</span></span>](#geometric-masks)
-   [<span data-ttu-id="6401d-116">Deck Kraft Masken</span><span class="sxs-lookup"><span data-stu-id="6401d-116">Opacity Masks</span></span>](#opacity-masks)
-   [<span data-ttu-id="6401d-117">Alternativen zu Ebenen</span><span class="sxs-lookup"><span data-stu-id="6401d-117">Alternatives to Layers</span></span>](#alternatives-to-layers)
-   [<span data-ttu-id="6401d-118">Clipping einer beliebigen Form</span><span class="sxs-lookup"><span data-stu-id="6401d-118">Clipping an arbitrary shape</span></span>](#clipping-an-arbitrary-shape)
    -   [<span data-ttu-id="6401d-119">Achsen ausgerichtete Clips</span><span class="sxs-lookup"><span data-stu-id="6401d-119">Axis aligned clips</span></span>](#axis-aligned-clips)
-   [<span data-ttu-id="6401d-120">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="6401d-120">Related topics</span></span>](#related-topics)

## <a name="what-are-layers"></a><span data-ttu-id="6401d-121">Was sind Ebenen?</span><span class="sxs-lookup"><span data-stu-id="6401d-121">What Are Layers?</span></span>

<span data-ttu-id="6401d-122">Ebenen, die durch [**ID2D1Layer**](/windows/win32/api/d2d1/nn-d2d1-id2d1layer) -Objekte dargestellt werden, ermöglichen es einer Anwendung, eine Gruppe von Zeichnungs Vorgängen zu bearbeiten.</span><span class="sxs-lookup"><span data-stu-id="6401d-122">Layers, represented by [**ID2D1Layer**](/windows/win32/api/d2d1/nn-d2d1-id2d1layer) objects, enable an application to manipulate a group of drawing operations.</span></span> <span data-ttu-id="6401d-123">Sie verwenden eine Ebene, indem Sie Sie auf ein Renderziel schieben.</span><span class="sxs-lookup"><span data-stu-id="6401d-123">You use a layer by "pushing" it onto a render target.</span></span> <span data-ttu-id="6401d-124">Nachfolgende Zeichnungsvorgänge durch das Renderziel werden an die Ebene weitergeleitet.</span><span class="sxs-lookup"><span data-stu-id="6401d-124">Subsequent drawing operations by the render target are directed to the layer.</span></span> <span data-ttu-id="6401d-125">Wenn Sie die Ebene fertiggestellt haben, können Sie die Ebene aus dem Renderziel "Pop", das den Inhalt der Ebene an das Renderziel zurückgibt.</span><span class="sxs-lookup"><span data-stu-id="6401d-125">After you're finished with the layer, you "pop" the layer from the render target, which composites the layer's content back to the render target.</span></span>

<span data-ttu-id="6401d-126">Wie bei Pinseln sind Ebenen Geräte abhängige Ressourcen, die durch Renderziele erstellt werden.</span><span class="sxs-lookup"><span data-stu-id="6401d-126">Like brushes, layers are device-dependent resources created by render targets.</span></span> <span data-ttu-id="6401d-127">Ebenen können für alle Renderziele in derselben Ressourcen Domäne verwendet werden, die das Renderziel enthält, von dem Sie erstellt wurde.</span><span class="sxs-lookup"><span data-stu-id="6401d-127">Layers can be used on any render target in the same resource domain that contains the render target that created it.</span></span> <span data-ttu-id="6401d-128">Eine ebenenressource kann jedoch nur von einem Renderziel gleichzeitig verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="6401d-128">However, a layer resource can only be used by one render target at a time.</span></span> <span data-ttu-id="6401d-129">Weitere Informationen zu Ressourcen finden Sie in der [Übersicht über Ressourcen](resources-and-resource-domains.md).</span><span class="sxs-lookup"><span data-stu-id="6401d-129">For more information about resources, see the [Resources Overview](resources-and-resource-domains.md).</span></span>

<span data-ttu-id="6401d-130">Obwohl Ebenen eine leistungsstarke renderingtechnik zum erzeugen interessanter Effekte bieten, kann eine übermäßige Anzahl von Ebenen in einer Anwendung sich negativ auf die Leistung auswirken, aufgrund der verschiedenen Kosten bei der Verwaltung von Ebenen und ebenenressourcen.</span><span class="sxs-lookup"><span data-stu-id="6401d-130">Although layers offer a powerful rendering technique for producing interesting effects, excessive number of layers in an application can adversely affect its performance, because of the various costs associated with managing layers and layer resources.</span></span> <span data-ttu-id="6401d-131">Beispielsweise gibt es die Kosten für das Ausfüllen oder Löschen der Ebene und die anschließende wieder Mischung, insbesondere für die Hardware mit höherem Ende.</span><span class="sxs-lookup"><span data-stu-id="6401d-131">For example, there is the cost of filling or clearing the layer and then blending it back, especially on higher-end hardware.</span></span> <span data-ttu-id="6401d-132">Dann gibt es die Kosten für die Verwaltung der ebenenressourcen.</span><span class="sxs-lookup"><span data-stu-id="6401d-132">Then, there is the cost of managing the layer resources.</span></span> <span data-ttu-id="6401d-133">Wenn Sie diese regelmäßig neu zuordnen, sind die resultierenden Staus gegen die GPU das größte Problem.</span><span class="sxs-lookup"><span data-stu-id="6401d-133">If you reallocate these frequently, the resulting stalls against the GPU will be the most significant problem.</span></span> <span data-ttu-id="6401d-134">Wenn Sie die Anwendung entwerfen, versuchen Sie, die Wiederverwendung von ebenenressourcen zu maximieren.</span><span class="sxs-lookup"><span data-stu-id="6401d-134">When you design your application, try to maximize reusing layer resources.</span></span>

## <a name="layers-in-windows-8-and-later"></a><span data-ttu-id="6401d-135">Schichten in Windows 8 und höher</span><span class="sxs-lookup"><span data-stu-id="6401d-135">Layers in Windows 8 and later</span></span>

<span data-ttu-id="6401d-136">Mit Windows 8 wurden neue ebenenbezogene APIs eingeführt, die die Leistung von vereinfachen, verbessern und Features zu Ebenen hinzufügen.</span><span class="sxs-lookup"><span data-stu-id="6401d-136">Windows 8 introduced new layer related APIs that simplify, improve the performance of, and add features to layers.</span></span>

### <a name="id2d1devicecontext-and-pushlayer"></a><span data-ttu-id="6401d-137">ID2D1DeviceContext und pushlayer</span><span class="sxs-lookup"><span data-stu-id="6401d-137">ID2D1DeviceContext and PushLayer</span></span>

<span data-ttu-id="6401d-138">Die [**ID2D1DeviceContext**](/windows/win32/api/d2d1_1/nn-d2d1_1-id2d1devicecontext) -Schnittstelle wird von der [**ID2D1RenderTarget**](/windows/win32/api/d2d1/nn-d2d1-id2d1rendertarget) -Schnittstelle abgeleitet und ist der Schlüssel zum Anzeigen von Direct2D-Inhalten in Windows 8. Weitere Informationen zu dieser Schnittstelle finden Sie unter [Geräte und Geräte Kontexte](devices-and-device-contexts.md).</span><span class="sxs-lookup"><span data-stu-id="6401d-138">The [**ID2D1DeviceContext**](/windows/win32/api/d2d1_1/nn-d2d1_1-id2d1devicecontext) interface is derived from the [**ID2D1RenderTarget**](/windows/win32/api/d2d1/nn-d2d1-id2d1rendertarget) interface and is key to displaying Direct2D content in Windows 8, for more information about this interface see [Devices and Device Contexts](devices-and-device-contexts.md).</span></span> <span data-ttu-id="6401d-139">Mit der Gerätekontext Schnittstelle können Sie den Aufruf der [**createlayer**](/windows/desktop/api/d2d1/nf-d2d1-id2d1rendertarget-createlayer(id2d1layer)) -Methode überspringen und dann NULL an die [**ID2D1DeviceContext::P ushlayer**](/windows/win32/api/d2d1_1/nf-d2d1_1-id2d1devicecontext-pushlayer(constd2d1_layer_parameters1_id2d1layer)) -Methode übergeben.</span><span class="sxs-lookup"><span data-stu-id="6401d-139">With the device context interface, you can skip calling the [**CreateLayer**](/windows/desktop/api/d2d1/nf-d2d1-id2d1rendertarget-createlayer(id2d1layer)) method and then pass NULL to the [**ID2D1DeviceContext::PushLayer**](/windows/win32/api/d2d1_1/nf-d2d1_1-id2d1devicecontext-pushlayer(constd2d1_layer_parameters1_id2d1layer)) method.</span></span> <span data-ttu-id="6401d-140">Direct2D verwaltet die ebenenressource automatisch und kann Ressourcen zwischen Ebenen und Effekt Diagrammen freigeben.</span><span class="sxs-lookup"><span data-stu-id="6401d-140">Direct2D automatically manages the layer resource and can share resources between layers and effect graphs.</span></span>

### <a name="d2d1_layer_parameters1-and-d2d1_layer_options1"></a><span data-ttu-id="6401d-141">D2D1 \_ Layer \_ PARAMETERS1 und D2D1 \_ Layer \_ OPTIONS1</span><span class="sxs-lookup"><span data-stu-id="6401d-141">D2D1\_LAYER\_PARAMETERS1 and D2D1\_LAYER\_OPTIONS1</span></span>

<span data-ttu-id="6401d-142">Die [**D2D1 \_ Layer \_ PARAMETERS1**](/windows/desktop/api/d2d1_1/ns-d2d1_1-d2d1_layer_parameters1) -Struktur ist identisch mit [**D2D1 \_ - \_ ebenenparametern**](/windows/desktop/api/d2d1/ns-d2d1-d2d1_layer_parameters), mit dem Unterschied, dass der endgültige Member der-Struktur jetzt eine [**D2D1 \_ Layer \_ OPTIONS1**](/windows/desktop/api/d2d1_1/ne-d2d1_1-d2d1_layer_options1) -Enumeration ist.</span><span class="sxs-lookup"><span data-stu-id="6401d-142">The [**D2D1\_LAYER\_PARAMETERS1**](/windows/desktop/api/d2d1_1/ns-d2d1_1-d2d1_layer_parameters1) structure is the same as [**D2D1\_LAYER\_PARAMETERS**](/windows/desktop/api/d2d1/ns-d2d1-d2d1_layer_parameters), except the final member of the structure is now a [**D2D1\_LAYER\_OPTIONS1**](/windows/desktop/api/d2d1_1/ne-d2d1_1-d2d1_layer_options1) enumeration.</span></span>

<span data-ttu-id="6401d-143">[**D2D1 \_ Layer \_ OPTIONS1**](/windows/desktop/api/d2d1_1/ne-d2d1_1-d2d1_layer_options1) verfügt über keine ClearType-Option und bietet zwei verschiedene Optionen, die Sie verwenden können, um die Leistung zu verbessern:</span><span class="sxs-lookup"><span data-stu-id="6401d-143">[**D2D1\_LAYER\_OPTIONS1**](/windows/desktop/api/d2d1_1/ne-d2d1_1-d2d1_layer_options1) has no ClearType option and has two different options that you can use to improve performance:</span></span>

-   <span data-ttu-id="6401d-144">[**D2D1 \_ Ebene \_ OPTIONS1 \_ initialisieren \_ von \_ Background**](/windows/desktop/api/d2d1_1/ne-d2d1_1-d2d1_layer_options1): Direct2D rendert primitive auf der Ebene, ohne Sie mit transparentem Schwarz zu löschen.</span><span class="sxs-lookup"><span data-stu-id="6401d-144">[**D2D1\_LAYER\_OPTIONS1\_INITIALIZE\_FROM\_BACKGROUND**](/windows/desktop/api/d2d1_1/ne-d2d1_1-d2d1_layer_options1): Direct2D renders primitives to the layer without clearing it with transparent black.</span></span> <span data-ttu-id="6401d-145">Dies ist nicht die Standardeinstellung, aber in den meisten Fällen führt dies zu einer besseren Leistung.</span><span class="sxs-lookup"><span data-stu-id="6401d-145">This is not the default, but in most cases results in better performance.</span></span>

-   <span data-ttu-id="6401d-146">[**D2D1 \_ Layer \_ OPTIONS1 \_ \_ Alpha ignorieren**](/windows/desktop/api/d2d1_1/ne-d2d1_1-d2d1_layer_options1): Wenn die zugrunde liegende Oberfläche auf den [**D2D1 Alpha- \_ \_ Modus \_ ignorieren**](/windows/desktop/api/dcommon/ne-dcommon-d2d1_alpha_mode)festgelegt ist, ermöglicht diese Option Direct2D das Ändern des Alphakanals der Ebene zu vermeiden.</span><span class="sxs-lookup"><span data-stu-id="6401d-146">[**D2D1\_LAYER\_OPTIONS1\_IGNORE\_ALPHA**](/windows/desktop/api/d2d1_1/ne-d2d1_1-d2d1_layer_options1): if the underlying surface is set to [**D2D1\_ALPHA\_MODE\_IGNORE**](/windows/desktop/api/dcommon/ne-dcommon-d2d1_alpha_mode), this option lets Direct2D avoid modifying the alpha channel of the layer.</span></span> <span data-ttu-id="6401d-147">Verwenden Sie dies nicht in anderen Fällen.</span><span class="sxs-lookup"><span data-stu-id="6401d-147">Do not use this in other cases.</span></span>

### <a name="blend-modes"></a><span data-ttu-id="6401d-148">Füllmethoden</span><span class="sxs-lookup"><span data-stu-id="6401d-148">Blend Modes</span></span>

<span data-ttu-id="6401d-149">Ab Windows 8 hat der Gerätekontext einen [**primitiven Blend-Modus**](/windows/desktop/api/D2d1_1/ne-d2d1_1-d2d1_primitive_blend) , der bestimmt, wie die einzelnen primitiven mit der Ziel Oberfläche gemischt werden.</span><span class="sxs-lookup"><span data-stu-id="6401d-149">Starting in Windows 8, the device context has a [**primitive blend mode**](/windows/desktop/api/D2d1_1/ne-d2d1_1-d2d1_primitive_blend) that determines how each primitive is blended with the target surface.</span></span> <span data-ttu-id="6401d-150">Dieser Modus gilt auch für Ebenen, wenn Sie die [**pushlayer**](/windows/win32/api/d2d1_1/nf-d2d1_1-id2d1devicecontext-pushlayer(constd2d1_layer_parameters1_id2d1layer)) -Methode aufzurufen.</span><span class="sxs-lookup"><span data-stu-id="6401d-150">This mode also applies to layers when you call the [**PushLayer**](/windows/win32/api/d2d1_1/nf-d2d1_1-id2d1devicecontext-pushlayer(constd2d1_layer_parameters1_id2d1layer)) method.</span></span>

<span data-ttu-id="6401d-151">Wenn Sie z. b. eine Ebene zum Ausschneiden primitiver Elemente mit Transparenz verwenden, legen Sie den [**D2D1 \_ primitive \_ Blend- \_ Kopier**](/windows/desktop/api/D2d1_1/ne-d2d1_1-d2d1_primitive_blend) Modus im Gerätekontext auf die richtigen Ergebnisse fest.</span><span class="sxs-lookup"><span data-stu-id="6401d-151">For example, if you are using a layer to clip primitives with transparency set the [**D2D1\_PRIMITIVE\_BLEND\_COPY**](/windows/desktop/api/D2d1_1/ne-d2d1_1-d2d1_primitive_blend) mode on the device context for proper results.</span></span> <span data-ttu-id="6401d-152">Der Kopiermodus macht den Gerätekontext linear interpolieren alle vier Farbkanäle, einschließlich des Alphakanals, jedes Pixels mit dem Inhalt der Ziel Oberfläche entsprechend der geometrischen Maske der Ebene.</span><span class="sxs-lookup"><span data-stu-id="6401d-152">The copy mode makes the device context linear interpolate all 4 color channels, including the alpha channel, of each pixel with the contents of the target surface according to the geometric mask of the layer.</span></span>

### <a name="interoperation"></a><span data-ttu-id="6401d-153">Interoperation</span><span class="sxs-lookup"><span data-stu-id="6401d-153">Interoperation</span></span>

<span data-ttu-id="6401d-154">Ab Windows 8 unterstützt Direct2D die Interaktion mit Direct3D und GDI, während eine Ebene oder ein Clip per Pushvorgang übermittelt wird.</span><span class="sxs-lookup"><span data-stu-id="6401d-154">Starting in Windows 8, Direct2D supports interoperation with Direct3D and GDI while a layer or clip is pushed.</span></span> <span data-ttu-id="6401d-155">Sie können [**ID2D1GdiInteropRenderTarget:: GetDC**](/windows/win32/api/d2d1/nf-d2d1-id2d1gdiinteroprendertarget-getdc) aufrufen, während eine Ebene für die Zusammenarbeit mit GDI per pushübertragung verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="6401d-155">You call [**ID2D1GdiInteropRenderTarget::GetDC**](/windows/win32/api/d2d1/nf-d2d1-id2d1gdiinteroprendertarget-getdc) while a layer is pushed to interoperate with GDI.</span></span> <span data-ttu-id="6401d-156">Sie werden [**ID2D1DeviceContext:: Flush**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-flush) aufgerufen und dann auf der zugrunde liegenden Oberfläche renderzum interagieren mit Direct3D.</span><span class="sxs-lookup"><span data-stu-id="6401d-156">You call [**ID2D1DeviceContext::Flush**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-flush) and then render to the underlying surface to interoperate with Direct3D.</span></span> <span data-ttu-id="6401d-157">Es liegt in ihrer Verantwortung, in der Schicht zu werden, oder Sie können mit Direct3D oder GDI Ausschneiden.</span><span class="sxs-lookup"><span data-stu-id="6401d-157">It is your responsibility to render inside the layer or clip with Direct3D or GDI.</span></span> <span data-ttu-id="6401d-158">Wenn Sie versuchen, außerhalb der Ebene zu Rendering oder zu schneiden, sind die Ergebnisse nicht definiert.</span><span class="sxs-lookup"><span data-stu-id="6401d-158">If you try to render outside the layer or clip the results are undefined.</span></span>

## <a name="creating-layers"></a><span data-ttu-id="6401d-159">Erstellen von Ebenen</span><span class="sxs-lookup"><span data-stu-id="6401d-159">Creating Layers</span></span>

<span data-ttu-id="6401d-160">Das Arbeiten mit Ebenen erfordert Vertrautheit mit [**den Methoden**](/windows/desktop/api/d2d1/nf-d2d1-id2d1rendertarget-createlayer(id2d1layer))"Methode", " [**pushlayer**](/windows/win32/api/d2d1_1/nf-d2d1_1-id2d1devicecontext-pushlayer(constd2d1_layer_parameters1_id2d1layer))" und " [**poplayer**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-poplayer) " und der Struktur " [**D2D1 \_ Layer \_ Parameters**](/windows/desktop/api/d2d1/ns-d2d1-d2d1_layer_parameters) ", die einen Satz von parametrischen Daten enthält, die definieren, wie die Ebene verwendet werden kann.</span><span class="sxs-lookup"><span data-stu-id="6401d-160">Working with layers requires familiarity with the [**CreateLayer**](/windows/desktop/api/d2d1/nf-d2d1-id2d1rendertarget-createlayer(id2d1layer)), [**PushLayer**](/windows/win32/api/d2d1_1/nf-d2d1_1-id2d1devicecontext-pushlayer(constd2d1_layer_parameters1_id2d1layer)), and [**PopLayer**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-poplayer) methods, and the [**D2D1\_LAYER\_PARAMETERS**](/windows/desktop/api/d2d1/ns-d2d1-d2d1_layer_parameters) structure, which contains a set of parametric data that defines how the layer can be used.</span></span> <span data-ttu-id="6401d-161">In der folgenden Liste werden die Methoden und die Struktur beschrieben.</span><span class="sxs-lookup"><span data-stu-id="6401d-161">The following list describes the methods and structure.</span></span>

-   <span data-ttu-id="6401d-162">Rufen Sie die Methode " [**kreatelayer**](/windows/desktop/api/d2d1/nf-d2d1-id2d1rendertarget-createlayer(id2d1layer)) " zum Erstellen einer ebenenressource auf.</span><span class="sxs-lookup"><span data-stu-id="6401d-162">Call the [**CreateLayer**](/windows/desktop/api/d2d1/nf-d2d1-id2d1rendertarget-createlayer(id2d1layer)) method to create a layer resource.</span></span>
    > [!Note]  
    > <span data-ttu-id="6401d-163">Ab Windows 8 können Sie den Aufruf der [**createlayer**](/windows/desktop/api/d2d1/nf-d2d1-id2d1rendertarget-createlayer(id2d1layer)) -Methode überspringen und dann NULL an die [**pushlayer**](/windows/win32/api/d2d1_1/nf-d2d1_1-id2d1devicecontext-pushlayer(constd2d1_layer_parameters1_id2d1layer)) -Methode der [**ID2D1DeviceContext**](/windows/win32/api/d2d1_1/nn-d2d1_1-id2d1devicecontext) -Schnittstelle übergeben.</span><span class="sxs-lookup"><span data-stu-id="6401d-163">Starting in Windows 8, you can skip calling the [**CreateLayer**](/windows/desktop/api/d2d1/nf-d2d1-id2d1rendertarget-createlayer(id2d1layer)) method and then pass NULL to the [**PushLayer**](/windows/win32/api/d2d1_1/nf-d2d1_1-id2d1devicecontext-pushlayer(constd2d1_layer_parameters1_id2d1layer)) method on the [**ID2D1DeviceContext**](/windows/win32/api/d2d1_1/nn-d2d1_1-id2d1devicecontext) interface.</span></span> <span data-ttu-id="6401d-164">Dies ist einfacher und ermöglicht Direct2D die automatische Verwaltung der ebenenressource und die gemeinsame Nutzung von Ressourcen zwischen Ebenen und Effekt Diagrammen.</span><span class="sxs-lookup"><span data-stu-id="6401d-164">This is simpler and allows Direct2D to automatically manage the layer resource and share resources between layers and effect graphs.</span></span>

     

-   <span data-ttu-id="6401d-165">Nachdem das Renderziel mit dem zeichnen begonnen hat (nachdem die [**beginDraw**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-begindraw) -Methode aufgerufen wurde), können Sie die [**pushlayer**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-pushlayer(constd2d1_layer_parameters__id2d1layer)) -Methode verwenden.</span><span class="sxs-lookup"><span data-stu-id="6401d-165">After render target has begun drawing (after its [**BeginDraw**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-begindraw) method has been called), you can use the [**PushLayer**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-pushlayer(constd2d1_layer_parameters__id2d1layer)) method.</span></span> <span data-ttu-id="6401d-166">Die **pushlayer** -Methode fügt die angegebene Ebene zum Renderziel hinzu, sodass das Ziel alle nachfolgenden Zeichnungsvorgänge empfängt, bis [**poplayer**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-poplayer) aufgerufen wird.</span><span class="sxs-lookup"><span data-stu-id="6401d-166">The **PushLayer** method adds the specified layer to the render target, so that the target receives all subsequent drawing operations until [**PopLayer**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-poplayer) is called.</span></span> <span data-ttu-id="6401d-167">Diese Methode nimmt ein [**ID2D1Layer**](/windows/win32/api/d2d1/nn-d2d1-id2d1layer) -Objekt an, das durch Aufrufen von [**createlayer**](/windows/desktop/api/d2d1/nf-d2d1-id2d1rendertarget-createlayer(id2d1layer)) und einem *layerparameters* in der [**D2D1 \_ Layer \_ Parameters**](/windows/desktop/api/d2d1/ns-d2d1-d2d1_layer_parameters) -Struktur zurückgegeben wird.</span><span class="sxs-lookup"><span data-stu-id="6401d-167">This method takes an [**ID2D1Layer**](/windows/win32/api/d2d1/nn-d2d1-id2d1layer) object returned by calling [**CreateLayer**](/windows/desktop/api/d2d1/nf-d2d1-id2d1rendertarget-createlayer(id2d1layer)) and an *layerParameters* in the [**D2D1\_LAYER\_PARAMETERS**](/windows/desktop/api/d2d1/ns-d2d1-d2d1_layer_parameters) structure.</span></span> <span data-ttu-id="6401d-168">In der folgenden Tabelle werden die Felder der-Struktur beschrieben.</span><span class="sxs-lookup"><span data-stu-id="6401d-168">The following table describes the fields of the structure.</span></span> 

    | <span data-ttu-id="6401d-169">Feld</span><span class="sxs-lookup"><span data-stu-id="6401d-169">Field</span></span>                 | <span data-ttu-id="6401d-170">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="6401d-170">Description</span></span>                                                                                                                                                                                                                                                                 |     |
    |-----------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-----|
    | <span data-ttu-id="6401d-171">**ContentBounds**</span><span class="sxs-lookup"><span data-stu-id="6401d-171">**contentBounds**</span></span>     | <span data-ttu-id="6401d-172">Die Inhalts Begrenzungen der Ebene.</span><span class="sxs-lookup"><span data-stu-id="6401d-172">The content bounds of the layer.</span></span> <span data-ttu-id="6401d-173">Inhalte außerhalb dieser Grenzen werden garantiert nicht angezeigt.</span><span class="sxs-lookup"><span data-stu-id="6401d-173">Content outside these bounds is guaranteed not to render.</span></span> <span data-ttu-id="6401d-174">Dieser Parameter ist standardmäßig [**infiniterect**](/windows/desktop/api/d2d1Helper/nf-d2d1helper-infiniterect).</span><span class="sxs-lookup"><span data-stu-id="6401d-174">This parameter defaults to [**InfiniteRect**](/windows/desktop/api/d2d1Helper/nf-d2d1helper-infiniterect).</span></span> <span data-ttu-id="6401d-175">Wenn der Standardwert verwendet wird, werden die Inhalts Begrenzungen effektiv in die Grenzen des Renderziels übernommen.</span><span class="sxs-lookup"><span data-stu-id="6401d-175">When the default value is used, the content bounds are effectively taken to be the bounds of the render target.</span></span> |     |
    | <span data-ttu-id="6401d-176">**geometricmask**</span><span class="sxs-lookup"><span data-stu-id="6401d-176">**geometricMask**</span></span>     | <span data-ttu-id="6401d-177">Optionale Der durch ein [**ID2D1Geometry**](/windows/win32/api/d2d1/nn-d2d1-id2d1geometry)definierte Bereich, auf den die Ebene abgeschnitten werden soll.</span><span class="sxs-lookup"><span data-stu-id="6401d-177">(Optional) The area, defined by an [**ID2D1Geometry**](/windows/win32/api/d2d1/nn-d2d1-id2d1geometry), to which the layer should be clipped.</span></span> <span data-ttu-id="6401d-178">Auf **null** festgelegt, wenn die Ebene nicht auf eine Geometrie zugeschnitten werden soll.</span><span class="sxs-lookup"><span data-stu-id="6401d-178">Set to **NULL** if the layer shouldn't be clipped to a geometry.</span></span>                                                                                           |     |
    | <span data-ttu-id="6401d-179">**maskantialiasmode**</span><span class="sxs-lookup"><span data-stu-id="6401d-179">**maskAntialiasMode**</span></span> | <span data-ttu-id="6401d-180">Ein-Wert, der den Antialiasing Modus für die geometrische Maske angibt, die durch das **geometricmask** -Feld angegeben wird.</span><span class="sxs-lookup"><span data-stu-id="6401d-180">A value that specifies the antialiasing mode for the geometric mask specified by the **geometricMask** field.</span></span>                                                                                                                                                               |     |
    | <span data-ttu-id="6401d-181">**masktransform**</span><span class="sxs-lookup"><span data-stu-id="6401d-181">**maskTransform**</span></span>     | <span data-ttu-id="6401d-182">Ein-Wert, der die Transformation angibt, die beim Erstellen der Ebene auf die geometrische Maske angewendet wird.</span><span class="sxs-lookup"><span data-stu-id="6401d-182">A value that specifies the transform that is applied to the geometric mask when composing the layer.</span></span> <span data-ttu-id="6401d-183">Dies ist relativ zur Welt Transformation.</span><span class="sxs-lookup"><span data-stu-id="6401d-183">This is relative to the world transform.</span></span>                                                                                                                               |     |
    | <span data-ttu-id="6401d-184">**Deck Kraft**</span><span class="sxs-lookup"><span data-stu-id="6401d-184">**opacity**</span></span>           | <span data-ttu-id="6401d-185">Der Deckkraft Wert der Ebene.</span><span class="sxs-lookup"><span data-stu-id="6401d-185">The opacity value of the layer.</span></span> <span data-ttu-id="6401d-186">Die Deckkraft der einzelnen Ressourcen in der Ebene wird bei der Zusammensetzung mit dem Ziel mit diesem Wert multipliziert.</span><span class="sxs-lookup"><span data-stu-id="6401d-186">The opacity of each resource in the layer is multiplied with this value when compositing to the target.</span></span>                                                                                                                                     |     |
    | <span data-ttu-id="6401d-187">**opacitybrush**</span><span class="sxs-lookup"><span data-stu-id="6401d-187">**opacityBrush**</span></span>      | <span data-ttu-id="6401d-188">Optionale Ein Pinsel, der verwendet wird, um die Deckkraft der Ebene zu ändern.</span><span class="sxs-lookup"><span data-stu-id="6401d-188">(Optional) A brush that is used to modify the opacity of the layer.</span></span> <span data-ttu-id="6401d-189">Der Pinsel wird der Ebene zugeordnet, und der Alphakanal der einzelnen zugeordneten Pinsel Pixel wird mit dem entsprechenden Ebenenpixel multipliziert.</span><span class="sxs-lookup"><span data-stu-id="6401d-189">The brush is mapped to the layer, and the alpha channel of each mapped brush pixel is multiplied against the corresponding layer pixel.</span></span> <span data-ttu-id="6401d-190">Auf **null** festgelegt, wenn die Ebene keine Deckkraft Maske aufweisen soll.</span><span class="sxs-lookup"><span data-stu-id="6401d-190">Set to **NULL** if the layer shouldn't have an opacity mask.</span></span>    |     |
    | <span data-ttu-id="6401d-191">**layeroptions**</span><span class="sxs-lookup"><span data-stu-id="6401d-191">**layerOptions**</span></span>      | <span data-ttu-id="6401d-192">Ein-Wert, der angibt, ob die Ebene den Text mit ClearType-Antialiasing darstellen soll.</span><span class="sxs-lookup"><span data-stu-id="6401d-192">A value that specifies whether the layer intends to render text with ClearType antialiasing.</span></span> <span data-ttu-id="6401d-193">Dieser Parameter ist standardmäßig auf OFF eingestellt.</span><span class="sxs-lookup"><span data-stu-id="6401d-193">This parameter defaults to off.</span></span> <span data-ttu-id="6401d-194">Wenn Sie diese Einstellung aktivieren, kann ClearType ordnungsgemäß verwendet werden, was jedoch zu einer etwas langsameren renderinggeschwindigkeit führt.</span><span class="sxs-lookup"><span data-stu-id="6401d-194">Turning it on enables ClearType to work correctly, but it results in slightly slower rendering speed.</span></span>                                          |     |

    

     

    > [!Note]  
    > <span data-ttu-id="6401d-195">Ab Windows 8 können Sie nicht mit ClearType in einer Schicht gerenstet werden, daher sollte der **layeroptions** -Parameter immer [**auf \_ D2D1 Layer \_ options \_ None**](/windows/desktop/api/d2d1/ne-d2d1-d2d1_layer_options) festgelegt werden.</span><span class="sxs-lookup"><span data-stu-id="6401d-195">Starting in Windows 8, you cannot render with ClearType in a layer, so the **layerOptions** parameter should always be set to [**D2D1\_LAYER\_OPTIONS\_NONE**](/windows/desktop/api/d2d1/ne-d2d1-d2d1_layer_options)</span></span>

     

    <span data-ttu-id="6401d-196">Zur einfacheren Bereitstellung stellt Direct2D die [**D2D1:: layerparameters**](/windows/desktop/api/d2d1helper/nf-d2d1helper-layerparameters) -Methode bereit, die Sie beim Erstellen von Strukturen für [**D2D1 \_ Layer- \_ Parameter**](/windows/desktop/api/d2d1/ns-d2d1-d2d1_layer_parameters) unterstützt</span><span class="sxs-lookup"><span data-stu-id="6401d-196">For convenience, Direct2D provides the [**D2D1::LayerParameters**](/windows/desktop/api/d2d1helper/nf-d2d1helper-layerparameters) method to help you create [**D2D1\_LAYER\_PARAMETERS**](/windows/desktop/api/d2d1/ns-d2d1-d2d1_layer_parameters) structures.</span></span>

-   <span data-ttu-id="6401d-197">Um den Inhalt der Ebene in das Renderziel zusammenzusetzen, nennen Sie die [**poplayer**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-poplayer) -Methode.</span><span class="sxs-lookup"><span data-stu-id="6401d-197">To composite the contents of the layer into the render target, call the [**PopLayer**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-poplayer) method.</span></span> <span data-ttu-id="6401d-198">Sie müssen die **poplayer** -Methode aufrufen, bevor Sie die [**EndDraw**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-enddraw) -Methode aufrufen.</span><span class="sxs-lookup"><span data-stu-id="6401d-198">You must call the **PopLayer** method before you call the [**EndDraw**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-enddraw) method.</span></span>

<span data-ttu-id="6401d-199">Im folgenden Beispiel wird die Verwendung von " [**kreatelayer**](/windows/desktop/api/d2d1/nf-d2d1-id2d1rendertarget-createlayer(id2d1layer))", " [**pushlayer**](/windows/win32/api/d2d1_1/nf-d2d1_1-id2d1devicecontext-pushlayer(constd2d1_layer_parameters1_id2d1layer))" und " [**poplayer**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-poplayer)" veranschaulicht.</span><span class="sxs-lookup"><span data-stu-id="6401d-199">The following example shows how to use [**CreateLayer**](/windows/desktop/api/d2d1/nf-d2d1-id2d1rendertarget-createlayer(id2d1layer)), [**PushLayer**](/windows/win32/api/d2d1_1/nf-d2d1_1-id2d1devicecontext-pushlayer(constd2d1_layer_parameters1_id2d1layer)), and [**PopLayer**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-poplayer).</span></span> <span data-ttu-id="6401d-200">Alle Felder in der [**D2D1 \_ Layer \_ Parameters**](/windows/desktop/api/d2d1/ns-d2d1-d2d1_layer_parameters) -Struktur werden auf ihre Standardwerte festgelegt, mit Ausnahme von **opacitybrush**, die auf eine [**ID2D1RadialGradientBrush**](/windows/win32/api/d2d1/nn-d2d1-id2d1radialgradientbrush)festgelegt ist.</span><span class="sxs-lookup"><span data-stu-id="6401d-200">All fields in the [**D2D1\_LAYER\_PARAMETERS**](/windows/desktop/api/d2d1/ns-d2d1-d2d1_layer_parameters) structure are set to their defaults, except **opacityBrush**, which is set to an [**ID2D1RadialGradientBrush**](/windows/win32/api/d2d1/nn-d2d1-id2d1radialgradientbrush).</span></span>


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



<span data-ttu-id="6401d-201">Code wurde in diesem Beispiel ausgelassen.</span><span class="sxs-lookup"><span data-stu-id="6401d-201">Code has been omitted from this example.</span></span>

<span data-ttu-id="6401d-202">Beachten Sie, dass beim Aufschieben von [**pushlayer**](/windows/win32/api/d2d1_1/nf-d2d1_1-id2d1devicecontext-pushlayer(constd2d1_layer_parameters1_id2d1layer)) und [**poplayer**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-poplayer)sichergestellt wird, dass jede **pushschicht** über einen passenden **poplayer** -Befehl verfügt.</span><span class="sxs-lookup"><span data-stu-id="6401d-202">Note that when you call [**PushLayer**](/windows/win32/api/d2d1_1/nf-d2d1_1-id2d1devicecontext-pushlayer(constd2d1_layer_parameters1_id2d1layer)) and [**PopLayer**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-poplayer), ensure that each **PushLayer** has a matching **PopLayer** call.</span></span> <span data-ttu-id="6401d-203">Wenn mehr **poplayer** -Aufrufe als **pushlayer** -Aufrufe vorhanden sind, wird das Renderziel in einen Fehlerzustand versetzt.</span><span class="sxs-lookup"><span data-stu-id="6401d-203">If there are more **PopLayer** calls than **PushLayer** calls, the render target is placed into an error state.</span></span> <span data-ttu-id="6401d-204">Wenn [**Flush**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-flush) vor allen ausstehenden Ebenen aufgerufen wird, wird das Renderziel in einen Fehlerzustand versetzt, und es wird ein Fehler zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="6401d-204">If [**Flush**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-flush) is called before all outstanding layers are popped, the render target is placed into an error state and returns an error.</span></span> <span data-ttu-id="6401d-205">Verwenden Sie [**EndDraw**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-enddraw), um den Fehlerzustand zu löschen.</span><span class="sxs-lookup"><span data-stu-id="6401d-205">To clear the error state, use [**EndDraw**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-enddraw).</span></span>

## <a name="content-bounds"></a><span data-ttu-id="6401d-206">Inhalts Begrenzungen</span><span class="sxs-lookup"><span data-stu-id="6401d-206">Content Bounds</span></span>

<span data-ttu-id="6401d-207">Die **ContentBounds** legt den Grenzwert fest, der auf die Ebene gezogen werden soll.</span><span class="sxs-lookup"><span data-stu-id="6401d-207">The **contentBounds** sets the limit of what is to be drawn to the layer.</span></span> <span data-ttu-id="6401d-208">Nur die Elemente innerhalb der Inhalts Begrenzungen werden wieder zum Renderziel zusammengesetzt.</span><span class="sxs-lookup"><span data-stu-id="6401d-208">Only those things within the content bounds are composited back to the render target.</span></span>

<span data-ttu-id="6401d-209">Im folgenden Beispiel wird gezeigt, wie **ContentBounds** angegeben wird, sodass das ursprüngliche Bild auf die Inhalts Begrenzungen mit der oberen linken Ecke auf (10, 108) und der unteren rechten Ecke um (121, 177) abgeschnitten wird.</span><span class="sxs-lookup"><span data-stu-id="6401d-209">The example that follows shows how to specify **contentBounds** so that the original image is clipped to the content bounds with the upper-left corner at (10, 108) and the lower-right corner at (121, 177).</span></span> <span data-ttu-id="6401d-210">Die folgende Abbildung zeigt das ursprüngliche Bild und das Ergebnis des Clipping des Bilds auf die Inhalts Begrenzungen.</span><span class="sxs-lookup"><span data-stu-id="6401d-210">The following illustration shows the original image and the result of clipping the image to the content bounds.</span></span>

![Abbildung der Inhalts Begrenzungen auf einem ursprünglichen Bild und dem resultierenden geschnittenen Bild](images/layers-contentbounds.png)


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



<span data-ttu-id="6401d-212">Code wurde in diesem Beispiel ausgelassen.</span><span class="sxs-lookup"><span data-stu-id="6401d-212">Code has been omitted from this example.</span></span>

> [!Note]
>
> <span data-ttu-id="6401d-213">Das resultierende abgeschnitten-Image wird weiter beeinflusst, wenn Sie eine **geometricmask** angeben.</span><span class="sxs-lookup"><span data-stu-id="6401d-213">The resulting clipped image is further affected if you specify a **geometricMask**.</span></span> <span data-ttu-id="6401d-214">Weitere Informationen finden Sie im Abschnitt [geometrische Masken](#geometric-masks) .</span><span class="sxs-lookup"><span data-stu-id="6401d-214">See the [Geometric Masks](#geometric-masks) section for more information.</span></span>

 

## <a name="geometric-masks"></a><span data-ttu-id="6401d-215">Geometrische Masken</span><span class="sxs-lookup"><span data-stu-id="6401d-215">Geometric Masks</span></span>

<span data-ttu-id="6401d-216">Eine geometrische Maske ist ein Clip oder ein Ausschnitt, der durch ein [**ID2D1Geometry**](/windows/win32/api/d2d1/nn-d2d1-id2d1geometry) -Objekt definiert wird, das eine Ebene maskiert, wenn Sie von einem Renderziel gezeichnet wird.</span><span class="sxs-lookup"><span data-stu-id="6401d-216">A geometric mask is a clip or a cutout, defined by an [**ID2D1Geometry**](/windows/win32/api/d2d1/nn-d2d1-id2d1geometry) object, that masks a layer when it is drawn by a render target.</span></span> <span data-ttu-id="6401d-217">Sie können das Feld **geomecmask** der [**D2D1 \_ Layer \_ Parameters**](/windows/desktop/api/d2d1/ns-d2d1-d2d1_layer_parameters) -Struktur verwenden, um die Ergebnisse in einer Geometrie zu maskieren.</span><span class="sxs-lookup"><span data-stu-id="6401d-217">You can use the **geometricMask** field of the [**D2D1\_LAYER\_PARAMETERS**](/windows/desktop/api/d2d1/ns-d2d1-d2d1_layer_parameters) structure to mask the results to a geometry.</span></span> <span data-ttu-id="6401d-218">Wenn Sie z. b. ein Bild anzeigen möchten, das durch den Blockbuchstaben "a" maskiert wird, können Sie zuerst eine Geometrie erstellen, die den Blockbuchstaben "a" darstellt, und diese Geometrie als geometrische Maske für eine Ebene verwenden.</span><span class="sxs-lookup"><span data-stu-id="6401d-218">For example, if you want to display an image masked by a block letter "A", you can first create a geometry representing the block letter "A" and use that geometry as a geometric mask for a layer.</span></span> <span data-ttu-id="6401d-219">Nachdem Sie die Ebene gedrückt haben, können Sie das Bild zeichnen.</span><span class="sxs-lookup"><span data-stu-id="6401d-219">Then, after pushing the layer, you can draw the image.</span></span> <span data-ttu-id="6401d-220">Das popping der Ebene führt dazu, dass das Bild auf den Blockbuchstaben "A" abgeschnitten wird.</span><span class="sxs-lookup"><span data-stu-id="6401d-220">Popping the layer results in the image being clipped to the block letter "A" shape.</span></span>

<span data-ttu-id="6401d-221">Das folgende Beispiel zeigt, wie ein [**ID2D1PathGeometry**](/windows/win32/api/d2d1/nn-d2d1-id2d1pathgeometry) erstellt wird, das eine Form eines Berges enthält, und dann die Pfad Geometrie an die [**pushschicht**](/windows/win32/api/d2d1_1/nf-d2d1_1-id2d1devicecontext-pushlayer(constd2d1_layer_parameters1_id2d1layer))übergibt.</span><span class="sxs-lookup"><span data-stu-id="6401d-221">The example that follows shows how to create an [**ID2D1PathGeometry**](/windows/win32/api/d2d1/nn-d2d1-id2d1pathgeometry) containing a shape of a mountain and then pass the path geometry to the [**PushLayer**](/windows/win32/api/d2d1_1/nf-d2d1_1-id2d1devicecontext-pushlayer(constd2d1_layer_parameters1_id2d1layer)).</span></span> <span data-ttu-id="6401d-222">Anschließend werden eine Bitmap und Quadrate gezeichnet.</span><span class="sxs-lookup"><span data-stu-id="6401d-222">It then draws a bitmap and squares.</span></span> <span data-ttu-id="6401d-223">Wenn in der zu Rendering-Ebene nur eine Bitmap vorhanden ist, verwenden Sie [**fillgeometry**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-fillgeometry) mit einem gebundenen Bitmap-Pinsel, um Effizienz zu erzielen.</span><span class="sxs-lookup"><span data-stu-id="6401d-223">If there is only a bitmap in the layer to render, use [**FillGeometry**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-fillgeometry) with a clamped bitmap brush for efficiency.</span></span> <span data-ttu-id="6401d-224">Die folgende Abbildung zeigt die Ausgabe des Beispiels.</span><span class="sxs-lookup"><span data-stu-id="6401d-224">The following illustration shows the output from the example.</span></span>

![Darstellung eines Bilds und des resultierenden Bilds nach dem Anwenden einer geometrischen Maske eines Berges](images/layers-bitmapmask.png)

<span data-ttu-id="6401d-226">Im ersten Beispiel wird die Geometrie definiert, die als Maske verwendet werden soll.</span><span class="sxs-lookup"><span data-stu-id="6401d-226">The first example defines the geometry to be used as a mask.</span></span>


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



<span data-ttu-id="6401d-227">Im nächsten Beispiel wird die Geometrie als Maske für die Ebene verwendet.</span><span class="sxs-lookup"><span data-stu-id="6401d-227">The next example uses the geometry as a mask for the layer.</span></span>


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



<span data-ttu-id="6401d-228">Code wurde in diesem Beispiel ausgelassen.</span><span class="sxs-lookup"><span data-stu-id="6401d-228">Code has been omitted from this example.</span></span>

> [!Note]
>
> <span data-ttu-id="6401d-229">Im Allgemeinen können Sie, wenn Sie eine **geometricmask** angeben, den Standardwert [**infiniterect**](/windows/desktop/api/d2d1Helper/nf-d2d1helper-infiniterect)für die **ContentBounds**-Werte verwenden.</span><span class="sxs-lookup"><span data-stu-id="6401d-229">In general, if you specify a **geometricMask**, you can use the default value, [**InfiniteRect**](/windows/desktop/api/d2d1Helper/nf-d2d1helper-infiniterect), for the **contentBounds**.</span></span>
>
> <span data-ttu-id="6401d-230">Wenn **ContentBounds** den Wert NULL aufweist und **geometricmask** nicht NULL ist, sind die Inhalts Begrenzungen tatsächlich die Begrenzungen der geometrischen Maske, nachdem die Masken Transformation angewendet wurde.</span><span class="sxs-lookup"><span data-stu-id="6401d-230">If **contentBounds** is NULL, and **geometricMask** is non-NULL, then the content bounds are effectively the bounds of the geometric mask after the mask transform is applied.</span></span>
>
> <span data-ttu-id="6401d-231">Wenn **ContentBounds** nicht NULL ist und **geometricmask** nicht NULL ist, wird die transformierte geometrische Maske effektiv auf die Inhalts Begrenzungen zugeschnitten, und die Inhalts Begrenzungen werden als unendlich angenommen.</span><span class="sxs-lookup"><span data-stu-id="6401d-231">If **contentBounds** is non-NULL, and **geometricMask** is non-NULL, then the transformed geometric mask is effectively clipped against content bounds and the content bounds are assumed to be infinite.</span></span>

 

## <a name="opacity-masks"></a><span data-ttu-id="6401d-232">Deck Kraft Masken</span><span class="sxs-lookup"><span data-stu-id="6401d-232">Opacity Masks</span></span>

<span data-ttu-id="6401d-233">Eine Deck Kraft Maske ist eine Maske, die durch einen Pinsel oder eine Bitmap beschrieben wird, der auf ein anderes Objekt angewendet wird, um dieses Objekt teilweise oder vollständig transparent zu machen.</span><span class="sxs-lookup"><span data-stu-id="6401d-233">An opacity mask is a mask, described by a brush or bitmap, that is applied to another object to make that object partially or completely transparent.</span></span> <span data-ttu-id="6401d-234">Es ermöglicht die Verwendung des Alphakanals eines Pinsels als Inhalts Maske.</span><span class="sxs-lookup"><span data-stu-id="6401d-234">It allows the use of the alpha channel of a brush to be used as a content mask.</span></span> <span data-ttu-id="6401d-235">Sie können z. b. einen radialen Farbverlaufs Pinsel definieren, der von "nicht transparent" zu "transparent" abweicht, um einen</span><span class="sxs-lookup"><span data-stu-id="6401d-235">For example, you can define a radial gradient brush that varies from opaque to transparent to create a vignette effect.</span></span>

<span data-ttu-id="6401d-236">Im folgenden Beispiel wird ein [**ID2D1RadialGradientBrush**](/windows/win32/api/d2d1/nn-d2d1-id2d1radialgradientbrush) (*m \_ pradialgradientbrush*) als Deck Kraft Maske verwendet.</span><span class="sxs-lookup"><span data-stu-id="6401d-236">The example that follows uses an [**ID2D1RadialGradientBrush**](/windows/win32/api/d2d1/nn-d2d1-id2d1radialgradientbrush) (*m\_pRadialGradientBrush*) as an opacity mask.</span></span> <span data-ttu-id="6401d-237">Anschließend werden eine Bitmap und Quadrate gezeichnet.</span><span class="sxs-lookup"><span data-stu-id="6401d-237">It then draws a bitmap and squares.</span></span> <span data-ttu-id="6401d-238">Wenn in der zu Rendering-Ebene nur eine Bitmap vorhanden ist, verwenden Sie [**fillgeometry**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-fillgeometry) mit einem gebundenen Bitmap-Pinsel, um Effizienz zu erzielen.</span><span class="sxs-lookup"><span data-stu-id="6401d-238">If there is only a bitmap in the layer to render, use [**FillGeometry**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-fillgeometry) with a clamped bitmap brush for efficiency.</span></span> <span data-ttu-id="6401d-239">Die folgende Abbildung zeigt die Ausgabe dieses Beispiels.</span><span class="sxs-lookup"><span data-stu-id="6401d-239">The following illustration shows the output from this example.</span></span>

![Abbildung eines Bilds und des resultierenden Bilds nach dem Anwenden einer Deck Kraft Maske](images/layers-opacitymask.png)


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



<span data-ttu-id="6401d-241">Code wurde in diesem Beispiel ausgelassen.</span><span class="sxs-lookup"><span data-stu-id="6401d-241">Code has been omitted from this example.</span></span>

> [!Note]  
> <span data-ttu-id="6401d-242">In diesem Beispiel wird eine Ebene verwendet, um eine Deckkraft Maske auf ein einzelnes Objekt anzuwenden, um das Beispiel so einfach wie möglich zu halten.</span><span class="sxs-lookup"><span data-stu-id="6401d-242">This example uses a layer to apply an opacity mask to a single object to keep the example as simple as possible.</span></span> <span data-ttu-id="6401d-243">Wenn eine Deck Kraft Maske auf ein einzelnes Objekt angewendet wird, ist es effizienter, die [**fillopacitymask**](id2d1rendertarget-fillopacitymask.md) -Methode oder die [**fillgeometry**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-fillgeometry) -Methode anstelle einer Ebene zu verwenden.</span><span class="sxs-lookup"><span data-stu-id="6401d-243">When applying an opacity mask to a single object, its more efficient to use the [**FillOpacityMask**](id2d1rendertarget-fillopacitymask.md) or [**FillGeometry**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-fillgeometry) methods, rather than a layer.</span></span>

 

<span data-ttu-id="6401d-244">Anweisungen zum Anwenden einer Deck Kraft Maske ohne Verwendung einer Ebene finden Sie in der [Übersicht über die Deck Kraft Masken](opacity-masks-overview.md).</span><span class="sxs-lookup"><span data-stu-id="6401d-244">For instructions on how to apply an opacity mask without using a layer, see the [Opacity Masks Overview](opacity-masks-overview.md).</span></span>

## <a name="alternatives-to-layers"></a><span data-ttu-id="6401d-245">Alternativen zu Ebenen</span><span class="sxs-lookup"><span data-stu-id="6401d-245">Alternatives to Layers</span></span>

<span data-ttu-id="6401d-246">Wie bereits erwähnt, kann sich eine übermäßige Anzahl von Ebenen nachteilig auf die Leistung Ihrer Anwendung auswirken.</span><span class="sxs-lookup"><span data-stu-id="6401d-246">As mentioned earlier, excessive number of layers can adversely affect the performance of your application.</span></span> <span data-ttu-id="6401d-247">Um die Leistung zu verbessern, sollten Sie möglichst keine Ebenen verwenden. Verwenden Sie stattdessen ihre Alternativen.</span><span class="sxs-lookup"><span data-stu-id="6401d-247">To improve performance, avoid using layers whenever possible; instead use their alternatives.</span></span> <span data-ttu-id="6401d-248">Im folgenden Codebeispiel wird gezeigt, wie Sie mithilfe von [**pushaxisalignedclip**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-pushaxisalignedclip(constd2d1_rect_f_d2d1_antialias_mode)) und [**popaxisalignedclip**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-popaxisalignedclip) einen Bereich als Alternative zur Verwendung einer Ebene mit Inhalts Begrenzungen verwenden.</span><span class="sxs-lookup"><span data-stu-id="6401d-248">The following code example shows how to use [**PushAxisAlignedClip**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-pushaxisalignedclip(constd2d1_rect_f_d2d1_antialias_mode)) and [**PopAxisAlignedClip**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-popaxisalignedclip) to clip a region, as an alternative to using a layer with content bounds.</span></span>


```C++
pRT->PushAxisAlignedClip(
    D2D1::RectF(20, 20, 100, 100),
    D2D1_ANTIALIAS_MODE_PER_PRIMITIVE
    );

pRT->FillRectangle(D2D1::RectF(0, 0, 200, 133), m_pOriginalBitmapBrush);
pRT->PopAxisAlignedClip();
```



<span data-ttu-id="6401d-249">Verwenden Sie auch [**fillgeometry**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-fillgeometry) mit einem gebundenen Bitmap-Pinsel als Alternative zur Verwendung einer Ebene mit einer Deck Kraft Maske, wenn es nur einen Inhalt in der zu Rendering enden Ebene gibt, wie im folgenden Beispiel gezeigt.</span><span class="sxs-lookup"><span data-stu-id="6401d-249">Similarly, use [**FillGeometry**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-fillgeometry) with a clamped bitmap brush as an alternative to using a layer with an opacity mask when there is only one content in the layer to render, as shown in the following example.</span></span>


```C++
        m_pRenderTarget->FillGeometry(
            m_pRectGeo, 
            m_pLinearFadeFlowersBitmapBrush, 
            m_pLinearGradientBrush
            );
```



<span data-ttu-id="6401d-250">Als Alternative zur Verwendung einer Ebene mit einer geometrischen Maske sollten Sie die Verwendung einer Bitmap-Maske zum Ausschneiden eines Bereichs in Erwägung gezogen, wie im folgenden Beispiel gezeigt.</span><span class="sxs-lookup"><span data-stu-id="6401d-250">As an alternative to using a layer with a geometric mask, consider using a bitmap mask to clip a region, as shown in the following example.</span></span>


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



<span data-ttu-id="6401d-251">Wenn Sie die Deckkraft auf ein einzelnes primitiv anwenden möchten, sollten Sie die Deckkraft im in die Pinsel Farbe multiplizieren und dann das primitive Rendering.</span><span class="sxs-lookup"><span data-stu-id="6401d-251">Lastly, if you want to apply opacity to a single primitive, you should multiply the opacity into the into the brush color and then render the primitive.</span></span> <span data-ttu-id="6401d-252">Sie benötigen keine Ebene oder eine Deck Kraft Maske-Bitmap.</span><span class="sxs-lookup"><span data-stu-id="6401d-252">You do not need a layer or an opacity mask bitmap.</span></span>


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



## <a name="clipping-an-arbitrary-shape"></a><span data-ttu-id="6401d-253">Clipping einer beliebigen Form</span><span class="sxs-lookup"><span data-stu-id="6401d-253">Clipping an arbitrary shape</span></span>

<span data-ttu-id="6401d-254">Die Abbildung zeigt das Ergebnis der Anwendung eines Clips auf ein Bild.</span><span class="sxs-lookup"><span data-stu-id="6401d-254">The figure here shows the result of applying a clip to an image.</span></span>

![ein Bild, das ein Beispiel eines Bilds vor und nach einem Clip anzeigt.](images/clip.png)

<span data-ttu-id="6401d-256">Sie können dieses Ergebnis mithilfe von Ebenen mit einer Geometrie Maske oder der [**fillgeometry**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-fillgeometry) -Methode mit einem Deckkraft Pinsel erhalten.</span><span class="sxs-lookup"><span data-stu-id="6401d-256">You can get this result by using layers with a geometry mask or the [**FillGeometry**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-fillgeometry) method with an opacity brush.</span></span>

<span data-ttu-id="6401d-257">Im folgenden finden Sie ein Beispiel, in dem eine Ebene verwendet wird:</span><span class="sxs-lookup"><span data-stu-id="6401d-257">Here's an example that uses a layer:</span></span>


```C++
// Call PushLayer() and pass in the clipping geometry.
m_d2dContext->PushLayer(
    D2D1::LayerParameters(
        boundsRect,
        geometricMask));
```



<span data-ttu-id="6401d-258">Es folgt ein Beispiel, in dem die [**fillgeometry**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-fillgeometry) -Methode verwendet wird:</span><span class="sxs-lookup"><span data-stu-id="6401d-258">Here's an example that uses the [**FillGeometry**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-fillgeometry) method:</span></span>


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



<span data-ttu-id="6401d-259">Wenn Sie in diesem Codebeispiel die pushlayer-Methode aufzurufen, übergeben Sie keine von der APP erstellte Ebene.</span><span class="sxs-lookup"><span data-stu-id="6401d-259">In this code example, when you call the PushLayer method, you don't pass in an app created layer.</span></span> <span data-ttu-id="6401d-260">Direct2D erstellt eine Ebene für Sie.</span><span class="sxs-lookup"><span data-stu-id="6401d-260">Direct2D creates a layer for you.</span></span> <span data-ttu-id="6401d-261">Direct2D ist in der Lage, die Zuordnung und Zerstörung dieser Ressource ohne Beteiligung der APP zu verwalten.</span><span class="sxs-lookup"><span data-stu-id="6401d-261">Direct2D is able to manage the allocation and destruction of this resource without any involvement from the app.</span></span> <span data-ttu-id="6401d-262">Dadurch kann Direct2D Ebenen intern wieder verwenden und Ressourcen Verwaltungs Optimierungen anwenden.</span><span class="sxs-lookup"><span data-stu-id="6401d-262">This allows Direct2D to reuse layers internally and apply resource management optimizations.</span></span>

> [!Note]  
> <span data-ttu-id="6401d-263">In Windows 8 wurden viele Optimierungen an der Verwendung von Ebenen vorgenommen, und es wird empfohlen, die Verwendung von ebenenapis anstelle von [**fillgeometry**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-fillgeometry) zu verwenden, wenn dies möglich ist.</span><span class="sxs-lookup"><span data-stu-id="6401d-263">In Windows 8 many optimizations have been made to the usage of layers and we recommend you try using layer APIs instead of [**FillGeometry**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-fillgeometry) whenever possible.</span></span>

 

### <a name="axis-aligned-clips"></a><span data-ttu-id="6401d-264">Achsen ausgerichtete Clips</span><span class="sxs-lookup"><span data-stu-id="6401d-264">Axis aligned clips</span></span>

<span data-ttu-id="6401d-265">, Wenn der Bereich, der abgeschnitten werden soll, an der Achse der Zeichen Oberfläche ausgerichtet ist, anstatt beliebig.</span><span class="sxs-lookup"><span data-stu-id="6401d-265">If the region to be clipped is aligned to the axis of the drawing surface, instead of arbitrary.</span></span> <span data-ttu-id="6401d-266">Dieser Fall eignet sich für die Verwendung eines Clip Rechtecks anstelle einer Ebene.</span><span class="sxs-lookup"><span data-stu-id="6401d-266">This case is suited for using a clip rectangle instead of a layer.</span></span> <span data-ttu-id="6401d-267">Der Leistungsgewinn liegt eher bei der Aliasing Geometrie als bei der Geometrie mit Antialiasing.</span><span class="sxs-lookup"><span data-stu-id="6401d-267">The performance gain is more for aliased geometry than antialiased geometry.</span></span> <span data-ttu-id="6401d-268">Weitere Informationen zu den Achsen ausgerichteten Clips finden Sie im Thema [**pushaxisalignedclip**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-pushaxisalignedclip(constd2d1_rect_f__d2d1_antialias_mode)) .</span><span class="sxs-lookup"><span data-stu-id="6401d-268">For more info on axis aligned clips, see the [**PushAxisAlignedClip**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-pushaxisalignedclip(constd2d1_rect_f__d2d1_antialias_mode)) topic.</span></span>

## <a name="related-topics"></a><span data-ttu-id="6401d-269">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="6401d-269">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="6401d-270">Direct2D-Referenz</span><span class="sxs-lookup"><span data-stu-id="6401d-270">Direct2D Reference</span></span>](reference.md)
</dt> </dl>

 

 