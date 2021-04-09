---
title: Benutzerdefinierte Effekte
description: Zeigt, wie Sie Ihre eigenen benutzerdefinierten Effekte mit dem Standard-HLSL schreiben.
ms.assetid: 5D22CA84-6465-4882-863D-81A632ACDD9C
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: eca6b15fe81ff4ccbd6cebbcee8c0d1955967056
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "104102294"
---
# <a name="custom-effects"></a><span data-ttu-id="08b11-103">Benutzerdefinierte Effekte</span><span class="sxs-lookup"><span data-stu-id="08b11-103">Custom effects</span></span>

<span data-ttu-id="08b11-104">[Direct2D](./direct2d-portal.md) wird mit einer Reihe von Effekten ausgeliefert, die eine Reihe von gängigen Bild Vorgängen ausführen.</span><span class="sxs-lookup"><span data-stu-id="08b11-104">[Direct2D](./direct2d-portal.md) ships with a library of effects that perform a variety of common image operations.</span></span> <span data-ttu-id="08b11-105">Eine umfassende Liste der Effekte finden Sie im Thema [integrierte Effekte](built-in-effects.md) .</span><span class="sxs-lookup"><span data-stu-id="08b11-105">See the [built-in effects](built-in-effects.md) topic for the complete list of effects.</span></span> <span data-ttu-id="08b11-106">Für Funktionen, die mit den integrierten Effekten nicht erreicht werden können, können Sie mit Direct2D ihre eigenen benutzerdefinierten Effekte mithilfe von Standard [HLSL](/windows/desktop/direct3dhlsl/overviews-direct3d-11-hlsl)schreiben.</span><span class="sxs-lookup"><span data-stu-id="08b11-106">For functionality that cannot be achieved with the built-in effects, Direct2D allows you to write your own custom effects using standard [HLSL](/windows/desktop/direct3dhlsl/overviews-direct3d-11-hlsl).</span></span> <span data-ttu-id="08b11-107">Sie können diese benutzerdefinierten Effekte neben den integrierten Effekten verwenden, die mit Direct2D ausgeliefert werden.</span><span class="sxs-lookup"><span data-stu-id="08b11-107">You can use these custom effects alongside the built-in effects that ship with Direct2D.</span></span>

<span data-ttu-id="08b11-108">Beispiele für einen kompletten Pixel-, Vertex-und Compute-Shadereffekt finden Sie im [D2DCustomEffects SDK-Beispiel](https://github.com/Microsoft/Windows-universal-samples/tree/master/Samples/D2DCustomEffects).</span><span class="sxs-lookup"><span data-stu-id="08b11-108">To see examples of a complete pixel, vertex, and compute shader effect, see the [D2DCustomEffects SDK sample](https://github.com/Microsoft/Windows-universal-samples/tree/master/Samples/D2DCustomEffects).</span></span>

<span data-ttu-id="08b11-109">In diesem Thema werden die Schritte und Konzepte erläutert, die Sie zum Entwerfen und Erstellen eines benutzerdefinierten Effekts mit vollem Funktionsumfang benötigen.</span><span class="sxs-lookup"><span data-stu-id="08b11-109">In this topic, we show you the steps and concepts you need to design and create a fully-featured custom effect.</span></span>

## <a name="introduction-what-is-inside-an-effect"></a><span data-ttu-id="08b11-110">Einführung: Was ist innerhalb eines Effekts?</span><span class="sxs-lookup"><span data-stu-id="08b11-110">Introduction: What is inside an effect?</span></span>

![Diagramm zum Ablegen des Schatten Effekts.](images/custom-effects1.png)

<span data-ttu-id="08b11-112">Konzeptionell führt ein [Direct2D](./direct2d-portal.md) Effect eine Abbild Erstellung aus, wie z. b. das Ändern der Helligkeit, das desätalisieren eines Bilds oder, wie oben gezeigt, das Erstellen eines Schlag Schattens.</span><span class="sxs-lookup"><span data-stu-id="08b11-112">Conceptually, a [Direct2D](./direct2d-portal.md) effect performs an imaging task, like changing brightness, de-saturating an image, or as shown above, creating a drop shadow.</span></span> <span data-ttu-id="08b11-113">Für die APP sind Sie einfach.</span><span class="sxs-lookup"><span data-stu-id="08b11-113">To the app, they are simple.</span></span> <span data-ttu-id="08b11-114">Sie können NULL oder mehr Eingabe Bilder akzeptieren, mehrere Eigenschaften verfügbar machen, die ihren Vorgang steuern, und ein einzelnes Ausgabe Bild generieren.</span><span class="sxs-lookup"><span data-stu-id="08b11-114">They can accept zero or more input images, expose multiple properties that control their operation, and generate a single output image.</span></span>

<span data-ttu-id="08b11-115">Es gibt vier verschiedene Teile eines benutzerdefinierten Effekts, für den ein Effekt Autor zuständig ist:</span><span class="sxs-lookup"><span data-stu-id="08b11-115">There are four different parts of a custom effect that an effect author is responsible for:</span></span>

1.  <span data-ttu-id="08b11-116">Wirkungs Schnittstelle: die Effekt Schnittstelle definiert konzeptionell, wie eine APP mit einem benutzerdefinierten Effekt interagiert (z. b. wie viele Eingaben der Effekt annimmt und welche Eigenschaften verfügbar sind).</span><span class="sxs-lookup"><span data-stu-id="08b11-116">Effect Interface: The effect interface conceptually defines how an app interacts with a custom effect (like how many inputs the effect accepts and what properties are available).</span></span> <span data-ttu-id="08b11-117">Die Effect-Schnittstelle verwaltet ein Transformations Diagramm, das die eigentlichen Abbild Erstellungs Vorgänge enthält.</span><span class="sxs-lookup"><span data-stu-id="08b11-117">The effect interface manages a transform graph, which contains the actual imaging operations.</span></span>
2.  <span data-ttu-id="08b11-118">Transformations Diagramm: jeder Effekt erstellt ein internes Transformations Diagramm, das aus einzelnen Transformationen besteht.</span><span class="sxs-lookup"><span data-stu-id="08b11-118">Transform graph: Each effect creates an internal transform graph made up of individual transforms.</span></span> <span data-ttu-id="08b11-119">Jede Transformation stellt einen einzelnen Bild Vorgang dar.</span><span class="sxs-lookup"><span data-stu-id="08b11-119">Each transform represents a single image operation.</span></span> <span data-ttu-id="08b11-120">Der Effekt ist dafür verantwortlich, diese Transformationen in einem Diagramm zu verknüpfen, um den beabsichtigten Abbild Erstellungs Effekt auszuführen.</span><span class="sxs-lookup"><span data-stu-id="08b11-120">The effect is responsible for linking these transforms together into a graph to perform the intended imaging effect.</span></span> <span data-ttu-id="08b11-121">Ein Effekt kann Transformationen als Reaktion auf Änderungen an den externen Eigenschaften des Effekts hinzufügen, entfernen, ändern und neu anordnen.</span><span class="sxs-lookup"><span data-stu-id="08b11-121">An effect can add, remove, modify, and reorder transforms in response to changes to the effect's external properties.</span></span>
3.  <span data-ttu-id="08b11-122">Transformation: eine Transformation stellt einen einzelnen Bild Vorgang dar.</span><span class="sxs-lookup"><span data-stu-id="08b11-122">Transform: A transform represents a single image operation.</span></span> <span data-ttu-id="08b11-123">Der Hauptzweck besteht darin, die Shader zu beherbergen, die für jedes Ausgabe Pixel ausgeführt werden.</span><span class="sxs-lookup"><span data-stu-id="08b11-123">Its main purpose is to house the shaders that are executed for each output pixel.</span></span> <span data-ttu-id="08b11-124">Zu diesem Zweck ist er für die Berechnung der neuen Größe seines Ausgabe Bilds basierend auf der Logik in seinen Shadern verantwortlich.</span><span class="sxs-lookup"><span data-stu-id="08b11-124">To that end, it is responsible for calculating the new size of its output image based on logic in its shaders.</span></span> <span data-ttu-id="08b11-125">Außerdem muss berechnet werden, aus welchem Bereich des Eingabe Bilds die Shader lesen müssen, um den angeforderten Ausgabebereich zu rendern.</span><span class="sxs-lookup"><span data-stu-id="08b11-125">It also must calculate which area of its input image the shaders need to read from to render the requested output region.</span></span>
4.  <span data-ttu-id="08b11-126">Shader: ein Shader wird für die Eingabe der Transformation auf der GPU ausgeführt (oder CPU, wenn das Software Rendering beim Erstellen des Direct3D-Geräts angegeben wird).</span><span class="sxs-lookup"><span data-stu-id="08b11-126">Shader: A shader is executed against the transform's input on the GPU (or CPU if software rendering is specified when the app creates the Direct3D device).</span></span> <span data-ttu-id="08b11-127">Effekt-Shader werden in High Level Shading Language ([HLSL](/windows/desktop/direct3dhlsl/overviews-direct3d-11-hlsl)) geschrieben und während der Kompilierung des Effekts in Bytecode kompiliert, der dann von der Auswirkung zur Laufzeit geladen wird.</span><span class="sxs-lookup"><span data-stu-id="08b11-127">Effect shaders are written in High Level Shading Language ([HLSL](/windows/desktop/direct3dhlsl/overviews-direct3d-11-hlsl)) and are compiled into byte code during the effect's compilation, which is then loaded by the effect during run-time.</span></span> <span data-ttu-id="08b11-128">In diesem Referenzdokument wird beschrieben, wie Sie [Direct2D](./direct2d-portal.md)-kompatible HLSL schreiben.</span><span class="sxs-lookup"><span data-stu-id="08b11-128">This reference document describes how to write [Direct2D](./direct2d-portal.md)-compliant HLSL.</span></span> <span data-ttu-id="08b11-129">Die Direct3D-Dokumentation enthält eine grundlegende HLSL-Übersicht.</span><span class="sxs-lookup"><span data-stu-id="08b11-129">The Direct3D documentation contains a basic HLSL overview.</span></span>

## <a name="creating-an-effect-interface"></a><span data-ttu-id="08b11-130">Erstellen einer Wirkungs Schnittstelle</span><span class="sxs-lookup"><span data-stu-id="08b11-130">Creating an effect interface</span></span>

<span data-ttu-id="08b11-131">Die Effekt Schnittstelle definiert, wie eine APP mit den benutzerdefinierten Effekten interagiert.</span><span class="sxs-lookup"><span data-stu-id="08b11-131">The effect interface defines how an app interacts with the custom effect.</span></span> <span data-ttu-id="08b11-132">Um eine Effekt Schnittstelle zu erstellen, muss eine Klasse ID2D1EffectImpl implementieren, Metadaten definieren, die den Effekt beschreiben (z. b. Name, Eingabe Anzahl und Eigenschaften), und Methoden erstellen, die den benutzerdefinierten Effekt für die Verwendung mit [Direct2D](./direct2d-portal.md)registrieren.</span><span class="sxs-lookup"><span data-stu-id="08b11-132">To create an effect interface, a class must implement ID2D1EffectImpl, define metadata that describes the effect (such as its name, input count and properties), and create methods that register the custom effect for use with [Direct2D](./direct2d-portal.md).</span></span>

<span data-ttu-id="08b11-133">Nachdem alle Komponenten für eine Effekt Schnittstelle implementiert wurden, wird der Header der Klasse wie folgt angezeigt:</span><span class="sxs-lookup"><span data-stu-id="08b11-133">Once all of the components for an effect interface have been implemented, the class' header will appear like this:</span></span>


```C++
#include <d2d1_1.h>
#include <d2d1effectauthor.h>  
#include <d2d1effecthelpers.h>

// Example GUID used to uniquely identify the effect. It is passed to Direct2D during
// effect registration, and used by the developer to identify the effect for any
// ID2D1DeviceContext::CreateEffect calls in the app. The app should create
// a unique name for the effect, as well as a unique GUID using a generation tool.
DEFINE_GUID(CLSID_SampleEffect, 0x00000000, 0x0000, 0x0000, 0x00, 0x00, 0x00, 0x00, 0x00, 0x00, 0x00, 0x00);

class SampleEffect : public ID2D1EffectImpl
{
public:
    // 2.1 Declare ID2D1EffectImpl implementation methods.
    IFACEMETHODIMP Initialize(
        _In_ ID2D1EffectContext* pContextInternal,
        _In_ ID2D1TransformGraph* pTransformGraph
        );

    IFACEMETHODIMP PrepareForRender(D2D1_CHANGE_TYPE changeType);
    IFACEMETHODIMP SetGraph(_In_ ID2D1TransformGraph* pGraph);

    // 2.2 Declare effect registration methods.
    static HRESULT Register(_In_ ID2D1Factory1* pFactory);
    static HRESULT CreateEffect(_Outptr_ IUnknown** ppEffectImpl);

    // 2.3 Declare IUnknown implementation methods.
    IFACEMETHODIMP_(ULONG) AddRef();
    IFACEMETHODIMP_(ULONG) Release();
    IFACEMETHODIMP QueryInterface(_In_ REFIID riid, _Outptr_ void** ppOutput);

private:
    // Constructor should be private since it should never be called externally.
    SampleEffect();

    LONG m_refCount; // Internal ref count used by AddRef() and Release() methods.
};
```



### <a name="implement-id2d1effectimpl"></a><span data-ttu-id="08b11-134">Implementieren von ID2D1EffectImpl</span><span class="sxs-lookup"><span data-stu-id="08b11-134">Implement ID2D1EffectImpl</span></span>

<span data-ttu-id="08b11-135">Die [**ID2D1EffectImpl**](/windows/win32/api/d2d1effectauthor/nn-d2d1effectauthor-id2d1effectimpl) -Schnittstelle enthält drei Methoden, die Sie implementieren müssen:</span><span class="sxs-lookup"><span data-stu-id="08b11-135">The [**ID2D1EffectImpl**](/windows/win32/api/d2d1effectauthor/nn-d2d1effectauthor-id2d1effectimpl) interface contains three methods that you must implement:</span></span>

### <a name="initializeid2d1effectcontext-pcontextinternal-id2d1transformgraph-ptransformgraph"></a><span data-ttu-id="08b11-136">Initialize (ID2D1EffectContext \* pcontextinternal, ID2D1TransformGraph \* ptransformgraph)</span><span class="sxs-lookup"><span data-stu-id="08b11-136">Initialize(ID2D1EffectContext \*pContextInternal, ID2D1TransformGraph \*pTransformGraph)</span></span>

<span data-ttu-id="08b11-137">[Direct2D](./direct2d-portal.md) Ruft die [**Initialize**](/windows/win32/api/d2d1effectauthor/nf-d2d1effectauthor-id2d1effectimpl-initialize) -Methode auf, nachdem die [**ID2D1DeviceContext:: kreateeffect**](/windows/win32/api/d2d1_1/nf-d2d1_1-id2d1devicecontext-createeffect) -Methode von der app aufgerufen wurde.</span><span class="sxs-lookup"><span data-stu-id="08b11-137">[Direct2D](./direct2d-portal.md) calls the [**Initialize**](/windows/win32/api/d2d1effectauthor/nf-d2d1effectauthor-id2d1effectimpl-initialize) method after the [**ID2D1DeviceContext::CreateEffect**](/windows/win32/api/d2d1_1/nf-d2d1_1-id2d1devicecontext-createeffect) method has been called by the app.</span></span> <span data-ttu-id="08b11-138">Sie können diese Methode verwenden, um die interne Initialisierung oder alle anderen Vorgänge auszuführen, die für den Effekt benötigt werden.</span><span class="sxs-lookup"><span data-stu-id="08b11-138">You can use this method to perform internal initialization or any other operations needed for the effect.</span></span> <span data-ttu-id="08b11-139">Außerdem können Sie damit den ursprünglichen Transformations Graphen des Effekts erstellen.</span><span class="sxs-lookup"><span data-stu-id="08b11-139">Additionally, you can use it to create the effect's initial transform graph.</span></span>

### <a name="setgraphid2d1transformgraph-ptransformgraph"></a><span data-ttu-id="08b11-140">Setgraph (ID2D1TransformGraph \* ptransformgraph)</span><span class="sxs-lookup"><span data-stu-id="08b11-140">SetGraph(ID2D1TransformGraph \*pTransformGraph)</span></span>

<span data-ttu-id="08b11-141">[Direct2D](./direct2d-portal.md) Ruft die [**setgraph**](/windows/win32/api/d2d1effectauthor/nf-d2d1effectauthor-id2d1effectimpl-setgraph) -Methode auf, wenn die Anzahl der Eingaben für den Effekt geändert wird.</span><span class="sxs-lookup"><span data-stu-id="08b11-141">[Direct2D](./direct2d-portal.md) calls the [**SetGraph**](/windows/win32/api/d2d1effectauthor/nf-d2d1effectauthor-id2d1effectimpl-setgraph) method when the number of inputs to the effect is changed.</span></span> <span data-ttu-id="08b11-142">Obwohl die meisten Effekte eine Konstante Anzahl von Eingaben aufweisen, unterstützen andere wie der zusammen [gesetzte Effekt](composite.md) eine Variable Anzahl von Eingaben.</span><span class="sxs-lookup"><span data-stu-id="08b11-142">While most effects have a constant number of inputs, others like the [Composite effect](composite.md) support a variable number of inputs.</span></span> <span data-ttu-id="08b11-143">Diese Methode ermöglicht es diesen Effekten, das Transformations Diagramm als Reaktion auf eine veränderliche Eingabe Anzahl zu aktualisieren.</span><span class="sxs-lookup"><span data-stu-id="08b11-143">This method allows these effects to update their transform graph in response to a changing input count.</span></span> <span data-ttu-id="08b11-144">Wenn ein Effekt eine Variable Eingabe Anzahl nicht unterstützt, kann diese Methode einfach E \_ notimpl zurückgeben.</span><span class="sxs-lookup"><span data-stu-id="08b11-144">If an effect does not support a variable input count, this method can simply return E\_NOTIMPL.</span></span>

### <a name="prepareforrender-d2d1_change_type-changetype"></a><span data-ttu-id="08b11-145">Prepareforrendering (D2D1 \_ \_ Änderungstyp ChangeType)</span><span class="sxs-lookup"><span data-stu-id="08b11-145">PrepareForRender (D2D1\_CHANGE\_TYPE changeType)</span></span>

<span data-ttu-id="08b11-146">Die [**prepareforrendering**](/windows/win32/api/d2d1effectauthor/nf-d2d1effectauthor-id2d1effectimpl-prepareforrender) -Methode bietet die Möglichkeit, alle Vorgänge als Reaktion auf externe Änderungen auszuführen.</span><span class="sxs-lookup"><span data-stu-id="08b11-146">The [**PrepareForRender**](/windows/win32/api/d2d1effectauthor/nf-d2d1effectauthor-id2d1effectimpl-prepareforrender) method provides an opportunity for effects to perform any operations in response to external changes.</span></span> <span data-ttu-id="08b11-147">[Direct2D](./direct2d-portal.md) ruft diese Methode direkt vor dem Rendern eines Effekts auf, wenn mindestens einer dieser Aktionen true ist:</span><span class="sxs-lookup"><span data-stu-id="08b11-147">[Direct2D](./direct2d-portal.md) calls this method just before it renders an effect if at least one of these is true:</span></span>

-   <span data-ttu-id="08b11-148">Der Effekt wurde zuvor initialisiert, aber noch nicht gezeichnet.</span><span class="sxs-lookup"><span data-stu-id="08b11-148">The effect has been previously initialized but not yet drawn.</span></span>
-   <span data-ttu-id="08b11-149">Eine Effekt Eigenschaft hat sich seit dem letzten zeichnen-Befehl geändert.</span><span class="sxs-lookup"><span data-stu-id="08b11-149">An effect property has changed since the last draw call.</span></span>
-   <span data-ttu-id="08b11-150">Der Status des aufrufenden [Direct2D](./direct2d-portal.md) -Kontexts (wie dpi) wurde seit dem letzten zeichnen-Befehl geändert.</span><span class="sxs-lookup"><span data-stu-id="08b11-150">The state of the calling [Direct2D](./direct2d-portal.md) context (like DPI) has changed since the last draw call.</span></span>

### <a name="implement-the-effect-registration-and-callback-methods"></a><span data-ttu-id="08b11-151">Implementieren der Effekt Registrierungs-und Rückruf Methoden</span><span class="sxs-lookup"><span data-stu-id="08b11-151">Implement the effect registration and callback methods</span></span>

<span data-ttu-id="08b11-152">Apps müssen Effekte mit [Direct2D](./direct2d-portal.md) registrieren, bevor Sie instanziiert werden.</span><span class="sxs-lookup"><span data-stu-id="08b11-152">Apps must register effects with [Direct2D](./direct2d-portal.md) before instantiating them.</span></span> <span data-ttu-id="08b11-153">Diese Registrierung bezieht sich auf eine Instanz einer Direct2D Factory und muss jedes Mal wiederholt werden, wenn die app ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="08b11-153">This registration is scoped to an instance of a Direct2D factory, and must be repeated each time the app is run.</span></span> <span data-ttu-id="08b11-154">Zum Aktivieren dieser Registrierung definiert ein benutzerdefinierter Effekt eine eindeutige GUID, eine öffentliche Methode, die den Effekt registriert, und eine private Rückruf Methode, die eine Instanz des Effekts zurückgibt.</span><span class="sxs-lookup"><span data-stu-id="08b11-154">To enable this registration, a custom effect defines a unique GUID, a public method that registers the effect, and a private callback method that returns an instance of the effect.</span></span>

### <a name="define-a-guid"></a><span data-ttu-id="08b11-155">Definieren einer GUID</span><span class="sxs-lookup"><span data-stu-id="08b11-155">Define a GUID</span></span>

<span data-ttu-id="08b11-156">Sie müssen eine GUID definieren, die die Auswirkungen auf die Registrierung bei [Direct2D](./direct2d-portal.md)eindeutig identifiziert.</span><span class="sxs-lookup"><span data-stu-id="08b11-156">You must define a GUID that uniquely identifies the effect for registration with [Direct2D](./direct2d-portal.md).</span></span> <span data-ttu-id="08b11-157">Die APP verwendet dieselbe, um den Effekt zu identifizieren, wenn Sie [**ID2D1DeviceContext:: kreateeffect**](/windows/win32/api/d2d1_1/nf-d2d1_1-id2d1devicecontext-createeffect)aufruft.</span><span class="sxs-lookup"><span data-stu-id="08b11-157">The app uses the same to identify the effect when it calls [**ID2D1DeviceContext::CreateEffect**](/windows/win32/api/d2d1_1/nf-d2d1_1-id2d1devicecontext-createeffect).</span></span>

<span data-ttu-id="08b11-158">In diesem Code wird veranschaulicht, wie eine GUID für einen Effekt definiert wird.</span><span class="sxs-lookup"><span data-stu-id="08b11-158">This code demonstrates defining such a GUID for an effect.</span></span> <span data-ttu-id="08b11-159">Sie müssen eine eigene eindeutige GUID erstellen, indem Sie ein GUID-Generierungs Tool wie guidgen.exe verwenden.</span><span class="sxs-lookup"><span data-stu-id="08b11-159">You must create its own unique GUID using a GUID generation tool such as guidgen.exe.</span></span>


```C++
// Example GUID used to uniquely identify the effect. It is passed to Direct2D during
// effect registration, and used by the developer to identify the effect for any
// ID2D1DeviceContext::CreateEffect calls in the app. The app should create
// a unique name for the effect, as well as a unique GUID using a generation tool.
DEFINE_GUID(CLSID_SampleEffect, 0x00000000, 0x0000, 0x0000, 0x00, 0x00, 0x00, 0x00, 0x00, 0x00, 0x00, 0x00);
```



### <a name="define-a-public-registration-method"></a><span data-ttu-id="08b11-160">Definieren einer öffentlichen Registrierungsmethode</span><span class="sxs-lookup"><span data-stu-id="08b11-160">Define a public registration method</span></span>

<span data-ttu-id="08b11-161">Definieren Sie als nächstes eine öffentliche Methode, mit der die APP den Effekt mit [Direct2D](./direct2d-portal.md)registriert.</span><span class="sxs-lookup"><span data-stu-id="08b11-161">Next, define a public method for the app to call to register the effect with [Direct2D](./direct2d-portal.md).</span></span> <span data-ttu-id="08b11-162">Da die Auswirkung-Registrierung spezifisch für eine Instanz einer Direct2D Factory ist, akzeptiert die Methode eine [**ID2D1Factory1**](/windows/win32/api/d2d1_1/nn-d2d1_1-id2d1factory1) -Schnittstelle als Parameter.</span><span class="sxs-lookup"><span data-stu-id="08b11-162">Because effect registration is specific to an instance of a Direct2D factory, the method accepts an [**ID2D1Factory1**](/windows/win32/api/d2d1_1/nn-d2d1_1-id2d1factory1) interface as a parameter.</span></span> <span data-ttu-id="08b11-163">Um den Effekt zu registrieren, ruft die-Methode dann die [**ID2D1Factory1:: registereffectfromstring**](/windows/win32/api/d2d1_1/nf-d2d1_1-id2d1factory1-registereffectfromstring) -API für den **ID2D1Factory1** -Parameter auf.</span><span class="sxs-lookup"><span data-stu-id="08b11-163">To register the effect, the method then calls the [**ID2D1Factory1::RegisterEffectFromString**](/windows/win32/api/d2d1_1/nf-d2d1_1-id2d1factory1-registereffectfromstring) API on the **ID2D1Factory1** parameter.</span></span>

<span data-ttu-id="08b11-164">Diese API akzeptiert eine XML-Zeichenfolge, die die Metadaten, Eingaben und Eigenschaften des Effekts beschreibt.</span><span class="sxs-lookup"><span data-stu-id="08b11-164">This API accepts an XML string that describes the metadata, inputs, and properties of the effect.</span></span> <span data-ttu-id="08b11-165">Die Metadaten für einen Effekt dienen nur zu Informationszwecken und können von der APP über die [**ID2D1Properties**](/windows/win32/api/d2d1_1/nn-d2d1_1-id2d1properties) -Schnittstelle abgefragt werden.</span><span class="sxs-lookup"><span data-stu-id="08b11-165">The metadata for an effect is for informational purposes only, and can be queried by the app through the [**ID2D1Properties**](/windows/win32/api/d2d1_1/nn-d2d1_1-id2d1properties) interface.</span></span> <span data-ttu-id="08b11-166">Die Eingabe-und Eigenschaften Daten werden hingegen von [Direct2D](./direct2d-portal.md) verwendet und repräsentieren die Funktionalität des Effekts.</span><span class="sxs-lookup"><span data-stu-id="08b11-166">The input and property data, on the other hand, is used by [Direct2D](./direct2d-portal.md) and represents the effect's functionality.</span></span>

<span data-ttu-id="08b11-167">Eine XML-Zeichenfolge für einen minimalen Beispiel Effekt wird hier dargestellt.</span><span class="sxs-lookup"><span data-stu-id="08b11-167">An XML string for a minimal sample effect is shown here.</span></span> <span data-ttu-id="08b11-168">Das Hinzufügen von benutzerdefinierten Eigenschaften zum XML-Code wird im Abschnitt Hinzufügen von benutzerdefinierten Eigenschaften zu einem Effekt beschrieben.</span><span class="sxs-lookup"><span data-stu-id="08b11-168">Adding custom properties to the XML is covered in the Adding custom properties to an effect section.</span></span>


```XML
#define XML(X) TEXT(#X) // This macro creates a single string from multiple lines of text.

PCWSTR pszXml =
    XML(
        <?xml version='1.0'?>
        <Effect>
            <!-- System Properties -->
            <Property name='DisplayName' type='string' value='SampleEffect'/>
            <Property name='Author' type='string' value='Contoso'/>
            <Property name='Category' type='string' value='Sample'/>
            <Property name='Description' type='string' value='This is a demo effect.'/>
            <Inputs>
                <Input name='SourceOne'/>
                <!-- <Input name='SourceTwo'/> -->
                <!-- Additional inputs go here. -->
            </Inputs>
            <!-- Custom Properties go here. -->
        </Effect>
        );
```



### <a name="define-an-effect-factory-callback-method"></a><span data-ttu-id="08b11-169">Definieren einer Effect Factory-Rückruf Methode</span><span class="sxs-lookup"><span data-stu-id="08b11-169">Define an effect factory callback method</span></span>

<span data-ttu-id="08b11-170">Der Effekt muss außerdem eine private Rückruf Methode bereitstellen, die eine Instanz des Effekts über einen einzelnen IUnknown-Parameter zurückgibt \* \* .</span><span class="sxs-lookup"><span data-stu-id="08b11-170">The effect must also provide a private callback method that returns an instance of the effect through a single IUnknown\*\* parameter.</span></span> <span data-ttu-id="08b11-171">Ein Zeiger auf diese Methode wird für [Direct2D](./direct2d-portal.md) bereitgestellt, wenn der Effekt über die [**ID2D1Factory1:: registereffectfromstring**](/windows/win32/api/d2d1_1/nf-d2d1_1-id2d1factory1-registereffectfromstring) -API über den [**PD2D1 \_ Effect \_ Factory**](/windows/desktop/api/D2D1_1/nc-d2d1_1-pd2d1_effect_factory) -Parameter registriert wird \\ .</span><span class="sxs-lookup"><span data-stu-id="08b11-171">A pointer to this method is provided to [Direct2D](./direct2d-portal.md) when the effect is registered via the [**ID2D1Factory1::RegisterEffectFromString**](/windows/win32/api/d2d1_1/nf-d2d1_1-id2d1factory1-registereffectfromstring) API through the [**PD2D1\_EFFECT\_FACTORY**](/windows/desktop/api/D2D1_1/nc-d2d1_1-pd2d1_effect_factory)\\ parameter.</span></span>


```C++
HRESULT __stdcall SampleEffect::CreateEffect(_Outptr_ IUnknown** ppEffectImpl)
{
    // This code assumes that the effect class initializes its reference count to 1.
    *ppEffectImpl = static_cast<ID2D1EffectImpl*>(new SampleEffect());

    if (*ppEffectImpl == nullptr)
    {
        return E_OUTOFMEMORY;
    }

    return S_OK;
}
```



### <a name="implement-the-iunknown-interface"></a><span data-ttu-id="08b11-172">Implementieren der IUnknown-Schnittstelle</span><span class="sxs-lookup"><span data-stu-id="08b11-172">Implement the IUnknown interface</span></span>

<span data-ttu-id="08b11-173">Schließlich muss der Effekt die IUnknown-Schnittstelle implementieren, um Kompatibilität mit com zu erzielen.</span><span class="sxs-lookup"><span data-stu-id="08b11-173">Finally, the effect must implement the IUnknown interface for compatibility with COM.</span></span>

## <a name="creating-the-effects-transform-graph"></a><span data-ttu-id="08b11-174">Erstellen des Transformations Diagramms des Effekts</span><span class="sxs-lookup"><span data-stu-id="08b11-174">Creating the effect's transform graph</span></span>

<span data-ttu-id="08b11-175">Ein Effekt kann verschiedene Transformationen (einzelne Bild Vorgänge) verwenden, um den gewünschten Bild Verarbeitungs Effekt zu erstellen.</span><span class="sxs-lookup"><span data-stu-id="08b11-175">An effect can use several different transforms (individual image operations) to create its desired imaging effect.</span></span> <span data-ttu-id="08b11-176">Um die Reihenfolge zu steuern, in der diese Transformationen auf das Eingabebild angewendet werden, ordnet der Effekt Sie in einem Transformations Diagramm an.</span><span class="sxs-lookup"><span data-stu-id="08b11-176">To control the order in which these transforms are applied to the input image, the effect arranges them into a transform graph.</span></span> <span data-ttu-id="08b11-177">Ein Transformations Diagramm kann die Effekte und Transformationen verwenden, die in [Direct2D](./direct2d-portal.md) enthalten sind, sowie benutzerdefinierte Transformationen, die vom Effekt Autor erstellt werden.</span><span class="sxs-lookup"><span data-stu-id="08b11-177">A transform graph can make use of the effects and transforms included in [Direct2D](./direct2d-portal.md) as well as custom transforms created by the effect author.</span></span>

### <a name="using-transforms-included-with-direct2d"></a><span data-ttu-id="08b11-178">Verwenden von in Direct2D enthaltenen Transformationen</span><span class="sxs-lookup"><span data-stu-id="08b11-178">Using transforms included with Direct2D</span></span>

<span data-ttu-id="08b11-179">Dies sind die am häufigsten verwendeten Transformationen, die mit [Direct2D](./direct2d-portal.md)bereitgestellt werden.</span><span class="sxs-lookup"><span data-stu-id="08b11-179">These are the most commonly used transforms provided with [Direct2D](./direct2d-portal.md).</span></span>

-   <span data-ttu-id="08b11-180">[**ID2D1BlendTransform**](/windows/win32/api/d2d1effectauthor/nn-d2d1effectauthor-id2d1blendtransform): Diese Transformation kombiniert eine beliebige Anzahl von Eingaben basierend auf einer Blend-Beschreibung. Weitere Beispiele finden Sie im Thema [**D2D1 \_ Blend \_ Description**](/windows/desktop/api/D2d1effectauthor/ns-d2d1effectauthor-d2d1_blend_description) und im [Beispiel Direct2D Composite Effect Modes](https://github.com/microsoftarchive/msdn-code-gallery-microsoft/tree/master/Official%20Windows%20Platform%20Sample/Direct2D%20composite%20effect%20modes%20sample) .</span><span class="sxs-lookup"><span data-stu-id="08b11-180">[**ID2D1BlendTransform**](/windows/win32/api/d2d1effectauthor/nn-d2d1effectauthor-id2d1blendtransform): This transform blends an arbitrary number of inputs together based on a blend description, see the [**D2D1\_BLEND\_DESCRIPTION**](/windows/desktop/api/D2d1effectauthor/ns-d2d1effectauthor-d2d1_blend_description) topic and the [Direct2D composite effect modes sample](https://github.com/microsoftarchive/msdn-code-gallery-microsoft/tree/master/Official%20Windows%20Platform%20Sample/Direct2D%20composite%20effect%20modes%20sample) for blending examples.</span></span> <span data-ttu-id="08b11-181">Diese Transformation wird von der [**ID2D1EffectContext:: kreateblendtransform**](/windows/win32/api/d2d1effectauthor/nf-d2d1effectauthor-id2d1effectcontext-createblendtransform) -Methode zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="08b11-181">This transform is returned by the [**ID2D1EffectContext::CreateBlendTransform**](/windows/win32/api/d2d1effectauthor/nf-d2d1effectauthor-id2d1effectcontext-createblendtransform) method.</span></span>
-   <span data-ttu-id="08b11-182">[**ID2D1BorderTransform**](/windows/win32/api/d2d1effectauthor/nn-d2d1effectauthor-id2d1bordertransform): mit dieser Transformation wird die Ausgabegröße eines Bilds entsprechend dem angegebenen D2D1-Erweiterungs [**\_ \_ Modus**](/windows/desktop/api/d2d1/ne-d2d1-d2d1_extend_mode) erweitert.</span><span class="sxs-lookup"><span data-stu-id="08b11-182">[**ID2D1BorderTransform**](/windows/win32/api/d2d1effectauthor/nn-d2d1effectauthor-id2d1bordertransform): This transform expands an image's output size according to the [**D2D1\_EXTEND\_MODE**](/windows/desktop/api/d2d1/ne-d2d1-d2d1_extend_mode) specified.</span></span> <span data-ttu-id="08b11-183">Diese Transformation wird von der [**ID2D1EffectContext:: kreatebordertransform**](/windows/win32/api/d2d1effectauthor/nf-d2d1effectauthor-id2d1effectcontext-createbordertransform) -Methode zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="08b11-183">This transform is returned by the [**ID2D1EffectContext::CreateBorderTransform**](/windows/win32/api/d2d1effectauthor/nf-d2d1effectauthor-id2d1effectcontext-createbordertransform) method.</span></span>
-   <span data-ttu-id="08b11-184">[**ID2D1OffsetTransform**](/windows/win32/api/d2d1effectauthor/nn-d2d1effectauthor-id2d1offsettransform): mit dieser Transformation wird die Eingabe durch eine beliebige ganze Anzahl von Pixeln verlagert (übersetzt).</span><span class="sxs-lookup"><span data-stu-id="08b11-184">[**ID2D1OffsetTransform**](/windows/win32/api/d2d1effectauthor/nn-d2d1effectauthor-id2d1offsettransform): This transform offsets (translates) its input by any whole number of pixels.</span></span> <span data-ttu-id="08b11-185">Diese Transformation wird von der [**ID2D1EffectContext:: kreateoffsettransform**](/windows/win32/api/d2d1effectauthor/nf-d2d1effectauthor-id2d1effectcontext-createoffsettransform) -Methode zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="08b11-185">This transform is returned by the [**ID2D1EffectContext::CreateOffsetTransform**](/windows/win32/api/d2d1effectauthor/nf-d2d1effectauthor-id2d1effectcontext-createoffsettransform) method.</span></span>
-   <span data-ttu-id="08b11-186">Alle vorhandenen Effekte können als Transformation für die Transformation des Transformations Diagramms mithilfe der [**ID2D1EffectContext:: deatetransformnodefromeffect**](/windows/win32/api/d2d1effectauthor/nf-d2d1effectauthor-id2d1effectcontext-createtransformnodefromeffect) -Methode behandelt werden.</span><span class="sxs-lookup"><span data-stu-id="08b11-186">Any existing effect can be treated as a transform for the purposes of transform graph creation by using the [**ID2D1EffectContext::CreateTransformNodeFromEffect**](/windows/win32/api/d2d1effectauthor/nf-d2d1effectauthor-id2d1effectcontext-createtransformnodefromeffect) method.</span></span>

### <a name="creating-a-single-node-transform-graph"></a><span data-ttu-id="08b11-187">Erstellen eines Transformations Diagramms mit einem einzelnen Knoten</span><span class="sxs-lookup"><span data-stu-id="08b11-187">Creating a single-node transform graph</span></span>

<span data-ttu-id="08b11-188">Nachdem Sie eine Transformation erstellt haben, muss die Eingabe des Effekts mit der Eingabe der Transformation verbunden werden, und die Ausgabe der Transformation muss mit der Ausgabe des Effekts verbunden werden.</span><span class="sxs-lookup"><span data-stu-id="08b11-188">Once you create a transform, the effect's input needs to be connected to the transform's input, and the transform's output needs to be connected to the effect's output.</span></span> <span data-ttu-id="08b11-189">Wenn ein Effekt nur eine einzelne Transformation enthält, können Sie dies problemlos mit der [**ID2D1TransformGraph:: setsingletransformnode**](/windows/win32/api/d2d1effectauthor/nf-d2d1effectauthor-id2d1transformgraph-setsingletransformnode) -Methode erreichen.</span><span class="sxs-lookup"><span data-stu-id="08b11-189">When an effect only contains a single transform, you can use the [**ID2D1TransformGraph::SetSingleTransformNode**](/windows/win32/api/d2d1effectauthor/nf-d2d1effectauthor-id2d1transformgraph-setsingletransformnode) method to easily accomplish this.</span></span>

<span data-ttu-id="08b11-190">Sie können eine Transformation in den [**Initialisierungs**](/windows/win32/api/d2d1effectauthor/nf-d2d1effectauthor-id2d1effectimpl-initialize) -oder [**setgraph**](/windows/win32/api/d2d1effectauthor/nf-d2d1effectauthor-id2d1effectimpl-setgraph) -Methoden des Effekts mithilfe des bereitgestellten ID2D1TransformGraph-Parameters erstellen oder ändern.</span><span class="sxs-lookup"><span data-stu-id="08b11-190">You can create or modify a transform in the effect's [**Initialize**](/windows/win32/api/d2d1effectauthor/nf-d2d1effectauthor-id2d1effectimpl-initialize) or [**SetGraph**](/windows/win32/api/d2d1effectauthor/nf-d2d1effectauthor-id2d1effectimpl-setgraph) methods using the provided ID2D1TransformGraph parameter.</span></span> <span data-ttu-id="08b11-191">Wenn ein Effekt Änderungen am Transformations Diagramm in einer anderen Methode vornehmen muss, bei der dieser Parameter nicht verfügbar ist, kann der Effekt den [**ID2D1TransformGraph**](/windows/win32/api/d2d1effectauthor/nn-d2d1effectauthor-id2d1transformgraph) -Parameter als Member-Variable der Klasse speichern und an anderer Stelle darauf zugreifen, wie z. b. [**prepareforrendering**](/windows/win32/api/d2d1effectauthor/nf-d2d1effectauthor-id2d1effectimpl-prepareforrender) oder eine benutzerdefinierte Eigenschaft Rückruf Methode.</span><span class="sxs-lookup"><span data-stu-id="08b11-191">If an effect needs to make changes to the transform graph in another method where this parameter is not available, the effect can save the [**ID2D1TransformGraph**](/windows/win32/api/d2d1effectauthor/nn-d2d1effectauthor-id2d1transformgraph) parameter as a member variable of the class and access it elsewhere, such as [**PrepareForRender**](/windows/win32/api/d2d1effectauthor/nf-d2d1effectauthor-id2d1effectimpl-prepareforrender) or a custom property callback method.</span></span>

<span data-ttu-id="08b11-192">Hier sehen Sie eine Beispiel [**Initialisierungs**](/windows/win32/api/d2d1effectauthor/nf-d2d1effectauthor-id2d1effectimpl-initialize) Methode.</span><span class="sxs-lookup"><span data-stu-id="08b11-192">A sample [**Initialize**](/windows/win32/api/d2d1effectauthor/nf-d2d1effectauthor-id2d1effectimpl-initialize) method is shown here.</span></span> <span data-ttu-id="08b11-193">Diese Methode erstellt ein Transformations Diagramm mit einem einzelnen Knoten, das das Bild auf jeder Achse um 100 Pixel verlagert.</span><span class="sxs-lookup"><span data-stu-id="08b11-193">This method creates a single-node transform graph that offsets the image by one hundred pixels in each axis.</span></span>


```C++
IFACEMETHODIMP SampleEffect::Initialize(
    _In_ ID2D1EffectContext* pEffectContext,
    _In_ ID2D1TransformGraph* pTransformGraph
    )
{
    HRESULT hr = pEffectContext->CreateOffsetTransform(
        D2D1::Point2L(100,100),  // Offsets the input by 100px in each axis.
        &m_pOffsetTransform
        );

    if (SUCCEEDED(hr))
    {
        // Connects the effect's input to the transform's input, and connects
        // the transform's output to the effect's output.
        hr = pTransformGraph->SetSingleTransformNode(m_pOffsetTransform);
    }

    return hr;
}
```



### <a name="creating-a-multi-node-transform-graph"></a><span data-ttu-id="08b11-194">Erstellen eines Transformations Diagramms mit mehreren Knoten</span><span class="sxs-lookup"><span data-stu-id="08b11-194">Creating a multi-node transform graph</span></span>

<span data-ttu-id="08b11-195">Das Hinzufügen mehrerer Transformationen zum Transformations Diagramm eines Effekts ermöglicht die interne Ausführung mehrerer Bild Vorgänge, die einer App als einzelner einheitlicher Effekt präsentiert werden.</span><span class="sxs-lookup"><span data-stu-id="08b11-195">Adding multiple transforms to an effect's transform graph allows effects to internally perform multiple image operations that are presented to an app as a single unified effect.</span></span>

<span data-ttu-id="08b11-196">Wie bereits erwähnt, kann das Transformations Diagramm des Effekts in jeder Effekt Methode mithilfe des [**ID2D1TransformGraph**](/windows/win32/api/d2d1effectauthor/nn-d2d1effectauthor-id2d1transformgraph) -Parameters bearbeitet werden, der in der [**Initialize**](/windows/win32/api/d2d1effectauthor/nf-d2d1effectauthor-id2d1effectimpl-initialize) -Methode des Effekts empfangen wird.</span><span class="sxs-lookup"><span data-stu-id="08b11-196">As noted above, the effect's transform graph may be edited in any effect method using the [**ID2D1TransformGraph**](/windows/win32/api/d2d1effectauthor/nn-d2d1effectauthor-id2d1transformgraph) parameter received in the effect's [**Initialize**](/windows/win32/api/d2d1effectauthor/nf-d2d1effectauthor-id2d1effectimpl-initialize) method.</span></span> <span data-ttu-id="08b11-197">Die folgenden APIs für diese Schnittstelle können verwendet werden, um das Transformations Diagramm eines Effekts zu erstellen oder zu ändern:</span><span class="sxs-lookup"><span data-stu-id="08b11-197">The following APIs on that interface can be used to create or modify an effect's transform graph:</span></span>

### <a name="addnodeid2d1transformnode-pnode"></a><span data-ttu-id="08b11-198">AddNode (ID2D1TransformNode \* pNode)</span><span class="sxs-lookup"><span data-stu-id="08b11-198">AddNode(ID2D1TransformNode \*pNode)</span></span>

<span data-ttu-id="08b11-199">Die [**AddNode**](/windows/win32/api/d2d1effectauthor/nf-d2d1effectauthor-id2d1transformgraph-addnode) -Methode registriert die Transformation in der Tat mit dem Effekt und muss aufgerufen werden, bevor die Transformation mit einer der anderen Transformations Diagramm Methoden verwendet werden kann.</span><span class="sxs-lookup"><span data-stu-id="08b11-199">The [**AddNode**](/windows/win32/api/d2d1effectauthor/nf-d2d1effectauthor-id2d1transformgraph-addnode) method, in effect, 'registers' the transform with the effect, and must be called before the transform can be used with any of the other transform graph methods.</span></span>

### <a name="connecttoeffectinputuint32-toeffectinputindex-id2d1transformnode-pnode-uint32-tonodeinputindex"></a><span data-ttu-id="08b11-200">Connectumeffectinput (UInt32-Objekt, ID2D1TransformNode \* pNode, UInt32 tonodeinputindex)</span><span class="sxs-lookup"><span data-stu-id="08b11-200">ConnectToEffectInput(UINT32 toEffectInputIndex, ID2D1TransformNode \*pNode, UINT32 toNodeInputIndex)</span></span>

<span data-ttu-id="08b11-201">Die [**connectdeeffectinput**](/windows/win32/api/d2d1effectauthor/nf-d2d1effectauthor-id2d1transformgraph-connecttoeffectinput) -Methode verbindet die Bild Eingabe des Effekts mit der Eingabe einer Transformation.</span><span class="sxs-lookup"><span data-stu-id="08b11-201">The [**ConnectToEffectInput**](/windows/win32/api/d2d1effectauthor/nf-d2d1effectauthor-id2d1transformgraph-connecttoeffectinput) method connects the effect's image input to a transform's input.</span></span> <span data-ttu-id="08b11-202">Dieselbe Effekt Eingabe kann mit mehreren Transformationen verbunden werden.</span><span class="sxs-lookup"><span data-stu-id="08b11-202">The same effect input can be connected to multiple transforms.</span></span>

### <a name="connectnodeid2d1transformnode-pfromnode-id2d1transformnode-ptonode-uint32-tonodeinputindex"></a><span data-ttu-id="08b11-203">Connectnode (ID2D1TransformNode \* pfromnode, ID2D1TransformNode \* ptonode, UInt32 tonodeinputindex)</span><span class="sxs-lookup"><span data-stu-id="08b11-203">ConnectNode(ID2D1TransformNode \*pFromNode, ID2D1TransformNode \*pToNode, UINT32 toNodeInputIndex)</span></span>

<span data-ttu-id="08b11-204">Die [**connectnode**](/windows/win32/api/d2d1effectauthor/nf-d2d1effectauthor-id2d1transformgraph-connectnode) -Methode verbindet die Ausgabe einer Transformation mit der Eingabe einer anderen Transformation.</span><span class="sxs-lookup"><span data-stu-id="08b11-204">The [**ConnectNode**](/windows/win32/api/d2d1effectauthor/nf-d2d1effectauthor-id2d1transformgraph-connectnode) method connects a transform's output to another transform's input.</span></span> <span data-ttu-id="08b11-205">Eine Transformations Ausgabe kann mit mehreren Transformationen verbunden werden.</span><span class="sxs-lookup"><span data-stu-id="08b11-205">A transform output can be connected to multiple transforms.</span></span>

### <a name="setoutputnodeid2d1transformnode-pnode"></a><span data-ttu-id="08b11-206">Setoutputnode (ID2D1TransformNode \* pNode)</span><span class="sxs-lookup"><span data-stu-id="08b11-206">SetOutputNode(ID2D1TransformNode \*pNode)</span></span>

<span data-ttu-id="08b11-207">Die [**setoutputnode**](/windows/win32/api/d2d1effectauthor/nf-d2d1effectauthor-id2d1transformgraph-setoutputnode) -Methode verbindet die Ausgabe einer Transformation mit der Ausgabe des Effekts.</span><span class="sxs-lookup"><span data-stu-id="08b11-207">The [**SetOutputNode**](/windows/win32/api/d2d1effectauthor/nf-d2d1effectauthor-id2d1transformgraph-setoutputnode) method connects a transform's output to the effect's output.</span></span> <span data-ttu-id="08b11-208">Da ein Effekt nur eine Ausgabe hat, kann nur eine einzelne Transformation als "Ausgabe Knoten" festgelegt werden.</span><span class="sxs-lookup"><span data-stu-id="08b11-208">Because an effect only has one output, only a single transform can be designated as the 'output node'.</span></span>

<span data-ttu-id="08b11-209">In diesem Code werden zwei separate Transformationen verwendet, um einen einheitlichen Effekt zu erzielen.</span><span class="sxs-lookup"><span data-stu-id="08b11-209">This code uses two separate transforms to create a unified effect.</span></span> <span data-ttu-id="08b11-210">In diesem Fall ist der Effekt ein übersetzter Schlag Schatten.</span><span class="sxs-lookup"><span data-stu-id="08b11-210">In this case, the effect is a translated drop shadow.</span></span>


```C++
IFACEMETHODIMP SampleEffect::Initialize(
    _In_ ID2D1EffectContext* pEffectContext, 
    _In_ ID2D1TransformGraph* pTransformGraph
    )
{   
    // Create the shadow effect.
    HRESULT hr = pEffectContext->CreateEffect(CLSID_D2D1Shadow, &m_pShadowEffect);

    // Create the shadow transform from the shadow effect.
    if (SUCCEEDED(hr))
    {
        hr = pEffectContext->CreateTransformNodeFromEffect(m_pShadowEffect, &m_pShadowTransform);
    }

    // Create the offset transform.
    if (SUCCEEDED(hr))
    {
        hr = pEffectContext->CreateOffsetTransform(
            D2D1::Point2L(0,0),
            &m_pOffsetTransform
            );
    }

    // Register both transforms with the effect graph.
    if (SUCCEEDED(hr))
    {
        hr = pTransformGraph->AddNode(m_pShadowTransform);
    }

    if (SUCCEEDED(hr))
    {
        hr = pTransformGraph->AddNode(m_pOffsetTransform);
    }

    // Connect the custom effect's input to the shadow transform's input.
    if (SUCCEEDED(hr))
    {
        hr = pTransformGraph->ConnectToEffectInput(
            0,                  // Input index of the effect.
            m_pShadowTransform, // The receiving transform.
            0                   // Input index of the receiving transform.
            );
    }

    // Connect the shadow transform's output to the offset transform's input.
    if (SUCCEEDED(hr))
    {
        hr = pTransformGraph->ConnectNode(
            m_pShadowTransform, // 'From' node.
            m_pOffsetTransform, // 'To' node.
            0                   // Input index of the 'to' node. There is only one output for the 'From' node.
            );
    }

    // Connect the offset transform's output to the custom effect's output.
    if (SUCCEEDED(hr))
    {
        hr = pTransformGraph->SetOutputNode(
            m_pOffsetTransform
            );
    }

    return hr;
}
```



## <a name="adding-custom-properties-to-an-effect"></a><span data-ttu-id="08b11-211">Hinzufügen von benutzerdefinierten Eigenschaften zu einem Effekt</span><span class="sxs-lookup"><span data-stu-id="08b11-211">Adding custom properties to an effect</span></span>

<span data-ttu-id="08b11-212">Effekte können benutzerdefinierte Eigenschaften definieren, die es einer APP ermöglichen, das Verhalten des Effekts während der Laufzeit zu ändern.</span><span class="sxs-lookup"><span data-stu-id="08b11-212">Effects can define custom properties that allow an app to change the effect's behavior during runtime.</span></span> <span data-ttu-id="08b11-213">Es gibt drei Schritte, um eine Eigenschaft für einen benutzerdefinierten Effekt zu definieren:</span><span class="sxs-lookup"><span data-stu-id="08b11-213">There are three steps to define a property for a custom effect:</span></span>

### <a name="add-the-property-metadata-to-the-effects-registration-data"></a><span data-ttu-id="08b11-214">Hinzufügen der Eigenschafts Metadaten zu den Registrierungsdaten des Effekts</span><span class="sxs-lookup"><span data-stu-id="08b11-214">Add the property metadata to the effect's registration data</span></span>

### <a name="add-property-to-registration-xml"></a><span data-ttu-id="08b11-215">Eigenschaft zum Registrierungs-XML hinzufügen</span><span class="sxs-lookup"><span data-stu-id="08b11-215">Add property to registration XML</span></span>

<span data-ttu-id="08b11-216">Sie müssen die Eigenschaften eines benutzerdefinierten Effekts während der anfänglichen Registrierung des Effekts bei [Direct2D](./direct2d-portal.md)definieren.</span><span class="sxs-lookup"><span data-stu-id="08b11-216">You must define a custom effect's properties during the effect's initial registration with [Direct2D](./direct2d-portal.md).</span></span> <span data-ttu-id="08b11-217">Zunächst müssen Sie die Registrierungs-XML-Datei des Effekts in der öffentlichen Registrierungsmethode mit der neuen Eigenschaft aktualisieren:</span><span class="sxs-lookup"><span data-stu-id="08b11-217">First, you must update the effect's registration XML in its public registration method with the new property:</span></span>


```C++
PCWSTR pszXml =
    TEXT(
        <?xml version='1.0'?>
        <Effect>
            <!-- System Properties -->
            <Property name='DisplayName' type='string' value='SampleEffect'/>
            <Property name='Author' type='string' value='Contoso'/>
            <Property name='Category' type='string' value='Sample'/>
            <Property name='Description'
                type='string'
                value='Translates an image by a user-specifiable amount.'/>
            <Inputs>
                <Input name='Source'/>
                <!-- Additional inputs go here. -->
            </Inputs>
            <!-- Custom Properties go here. -->
            <Property name='Offset' type='vector2'>
                <Property name='DisplayName' type='string' value='Image Offset'/>
                <!— Optional sub-properties -->
                <Property name='Min' type='vector2' value='(-1000.0, -1000.0)' />
                <Property name='Max' type='vector2' value='(1000.0, 1000.0)' />
                <Property name='Default' type='vector2' value='(0.0, 0.0)' />
            </Property>
        </Effect>
        );
```



<span data-ttu-id="08b11-218">Wenn Sie eine Effect-Eigenschaft in XML definieren, benötigen Sie einen Namen, einen Typ und einen anzeigen Amen.</span><span class="sxs-lookup"><span data-stu-id="08b11-218">When you define an effect property in XML, it needs a name, a type, and a display name.</span></span> <span data-ttu-id="08b11-219">Der Anzeige Name einer Eigenschaft sowie die Werte für Kategorie, Autor und Beschreibung des Gesamt Effekts können lokalisiert werden und sollten lokalisiert werden.</span><span class="sxs-lookup"><span data-stu-id="08b11-219">A property's display name, as well as the overall effect's category, author, and description values can and should be localized.</span></span>

<span data-ttu-id="08b11-220">Für jede Eigenschaft können mit einem Effekt optional die Werte Default, min und Max angegeben werden.</span><span class="sxs-lookup"><span data-stu-id="08b11-220">For each property, an effect can optionally specify default, min, and max values.</span></span> <span data-ttu-id="08b11-221">Diese Werte dienen nur zur Informations Verwendung.</span><span class="sxs-lookup"><span data-stu-id="08b11-221">These values are for informational use only.</span></span> <span data-ttu-id="08b11-222">Sie werden nicht durch [Direct2D](./direct2d-portal.md)erzwungen.</span><span class="sxs-lookup"><span data-stu-id="08b11-222">They are not enforced by [Direct2D](./direct2d-portal.md).</span></span> <span data-ttu-id="08b11-223">Sie müssen jede angegebene Standard-/min-/Maximum-Logik selbst in der Effekt Klasse implementieren.</span><span class="sxs-lookup"><span data-stu-id="08b11-223">It is up to you to implement any specified default/min/max logic in the effect class yourself.</span></span>

<span data-ttu-id="08b11-224">Der im XML-Code für die-Eigenschaft aufgelistete Typwert muss mit dem entsprechenden Datentyp übereinstimmen, der von den Methoden Getter und Setter der Eigenschaft verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="08b11-224">The type value listed in the XML for the property must match the corresponding data type used by the property's getter and setter methods.</span></span> <span data-ttu-id="08b11-225">In dieser Tabelle werden die entsprechenden XML-Werte für jeden Datentyp angezeigt:</span><span class="sxs-lookup"><span data-stu-id="08b11-225">Corresponding XML values for each data type are shown in this table:</span></span>



| <span data-ttu-id="08b11-226">Datentyp</span><span class="sxs-lookup"><span data-stu-id="08b11-226">Data type</span></span>                                                                                                                              | <span data-ttu-id="08b11-227">Entsprechender XML-Wert</span><span class="sxs-lookup"><span data-stu-id="08b11-227">Corresponding XML value</span></span> |
|----------------------------------------------------------------------------------------------------------------------------------------|-------------------------|
| <span data-ttu-id="08b11-228">Pwstr</span><span class="sxs-lookup"><span data-stu-id="08b11-228">PWSTR</span></span>                                                                                                                                  | <span data-ttu-id="08b11-229">Zeichenfolge</span><span class="sxs-lookup"><span data-stu-id="08b11-229">string</span></span>                  |
| <span data-ttu-id="08b11-230">BOOL</span><span class="sxs-lookup"><span data-stu-id="08b11-230">BOOL</span></span>                                                                                                                                   | <span data-ttu-id="08b11-231">bool</span><span class="sxs-lookup"><span data-stu-id="08b11-231">bool</span></span>                    |
| <span data-ttu-id="08b11-232">UINT</span><span class="sxs-lookup"><span data-stu-id="08b11-232">UINT</span></span>                                                                                                                                   | <span data-ttu-id="08b11-233">uint32</span><span class="sxs-lookup"><span data-stu-id="08b11-233">uint32</span></span>                  |
| <span data-ttu-id="08b11-234">INT</span><span class="sxs-lookup"><span data-stu-id="08b11-234">INT</span></span>                                                                                                                                    | <span data-ttu-id="08b11-235">int32</span><span class="sxs-lookup"><span data-stu-id="08b11-235">int32</span></span>                   |
| <span data-ttu-id="08b11-236">GLEITKOMMAZAHL</span><span class="sxs-lookup"><span data-stu-id="08b11-236">FLOAT</span></span>                                                                                                                                  | <span data-ttu-id="08b11-237">float</span><span class="sxs-lookup"><span data-stu-id="08b11-237">float</span></span>                   |
| [<span data-ttu-id="08b11-238">**D2D \_ Vector \_ 2F**</span><span class="sxs-lookup"><span data-stu-id="08b11-238">**D2D\_VECTOR\_2F**</span></span>](/windows/desktop/api/dcommon/ns-dcommon-d2d_vector_2f)                                                                                               | <span data-ttu-id="08b11-239">Vector2</span><span class="sxs-lookup"><span data-stu-id="08b11-239">vector2</span></span>                 |
| [<span data-ttu-id="08b11-240">**D2D \_ Vector \_ 3F**</span><span class="sxs-lookup"><span data-stu-id="08b11-240">**D2D\_VECTOR\_3F**</span></span>](/windows/desktop/api/dcommon/ns-dcommon-d2d_vector_3f)                                                                                               | <span data-ttu-id="08b11-241">Vector3</span><span class="sxs-lookup"><span data-stu-id="08b11-241">vector3</span></span>                 |
| [<span data-ttu-id="08b11-242">**D2D \_ Vector \_ 4f**</span><span class="sxs-lookup"><span data-stu-id="08b11-242">**D2D\_VECTOR\_4F**</span></span>](/windows/desktop/api/dcommon/ns-dcommon-d2d_vector_4f)                                                                                               | <span data-ttu-id="08b11-243">Vector4</span><span class="sxs-lookup"><span data-stu-id="08b11-243">vector4</span></span>                 |
| <span data-ttu-id="08b11-244">[**D2D \_ Matrix \_ 3x2 \_ F**](/windows/win32/api/d2d1/nf-d2d1-id2d1geometry-strokecontainspoint(d2d1_point_2f_float_id2d1strokestyle_constd2d1_matrix_3x2_f__bool))</span><span class="sxs-lookup"><span data-stu-id="08b11-244">[**D2D\_MATRIX\_3X2\_F**](/windows/win32/api/d2d1/nf-d2d1-id2d1geometry-strokecontainspoint(d2d1_point_2f_float_id2d1strokestyle_constd2d1_matrix_3x2_f__bool))</span></span> | <span data-ttu-id="08b11-245">matrix3x2</span><span class="sxs-lookup"><span data-stu-id="08b11-245">matrix3x2</span></span>               |
| [<span data-ttu-id="08b11-246">**D2D \_ Matrix \_ 4X3 \_ F**</span><span class="sxs-lookup"><span data-stu-id="08b11-246">**D2D\_MATRIX\_4X3\_F**</span></span>](/windows/desktop/api/dcommon/ns-dcommon-d2d_matrix_4x3_f)                                                                                        | <span data-ttu-id="08b11-247">matrix4x3</span><span class="sxs-lookup"><span data-stu-id="08b11-247">matrix4x3</span></span>               |
| [<span data-ttu-id="08b11-248">**D2D \_ Matrix 4 \_ x 4 \_ F**</span><span class="sxs-lookup"><span data-stu-id="08b11-248">**D2D\_MATRIX\_4X4\_F**</span></span>](/windows/desktop/api/dcommon/ns-dcommon-d2d_matrix_4x4_f)                                                                                        | <span data-ttu-id="08b11-249">matrix4x4</span><span class="sxs-lookup"><span data-stu-id="08b11-249">matrix4x4</span></span>               |
| [<span data-ttu-id="08b11-250">**D2D \_ Matrix \_ 5X4 \_ F**</span><span class="sxs-lookup"><span data-stu-id="08b11-250">**D2D\_MATRIX\_5X4\_F**</span></span>](/windows/desktop/api/dcommon/ns-dcommon-d2d_matrix_5x4_f)                                                                                        | <span data-ttu-id="08b11-251">matrix5x4</span><span class="sxs-lookup"><span data-stu-id="08b11-251">matrix5x4</span></span>               |
| <span data-ttu-id="08b11-252">Hobby\[\]</span><span class="sxs-lookup"><span data-stu-id="08b11-252">BYTE\[\]</span></span>                                                                                                                               | <span data-ttu-id="08b11-253">Blob</span><span class="sxs-lookup"><span data-stu-id="08b11-253">blob</span></span>                    |
| <span data-ttu-id="08b11-254">IUnknown\*</span><span class="sxs-lookup"><span data-stu-id="08b11-254">IUnknown\*</span></span>                                                                                                                             | <span data-ttu-id="08b11-255">IUnknown</span><span class="sxs-lookup"><span data-stu-id="08b11-255">iunknown</span></span>                |
| <span data-ttu-id="08b11-256">[**ID2D1ColorContext**](/windows/win32/api/d2d1_1/nn-d2d1_1-id2d1colorcontext)\*</span><span class="sxs-lookup"><span data-stu-id="08b11-256">[**ID2D1ColorContext**](/windows/win32/api/d2d1_1/nn-d2d1_1-id2d1colorcontext)\*</span></span>                                                                                       | <span data-ttu-id="08b11-257">ColorContext</span><span class="sxs-lookup"><span data-stu-id="08b11-257">colorcontext</span></span>            |
| <span data-ttu-id="08b11-258">CLSID</span><span class="sxs-lookup"><span data-stu-id="08b11-258">CLSID</span></span>                                                                                                                                  | <span data-ttu-id="08b11-259">clsid</span><span class="sxs-lookup"><span data-stu-id="08b11-259">clsid</span></span>                   |
| <span data-ttu-id="08b11-260">Enumeration ([**D2D1 \_ Interpolations \_ Modus**](/windows/desktop/api/d2d1_1/ne-d2d1_1-d2d1_interpolation_mode)usw.)</span><span class="sxs-lookup"><span data-stu-id="08b11-260">Enumeration ([**D2D1\_INTERPOLATION\_MODE**](/windows/desktop/api/d2d1_1/ne-d2d1_1-d2d1_interpolation_mode), etc.)</span></span>                                                | <span data-ttu-id="08b11-261">enum</span><span class="sxs-lookup"><span data-stu-id="08b11-261">enum</span></span>                    |



 

### <a name="map-the-new-property-to-getter-and-setter-methods"></a><span data-ttu-id="08b11-262">Zuordnen der neuen Eigenschaft zu Getter-und Setter-Methoden</span><span class="sxs-lookup"><span data-stu-id="08b11-262">Map the new property to getter and setter methods</span></span>

<span data-ttu-id="08b11-263">Als nächstes muss der Effekt diese neue Eigenschaft den Getter-und Setter-Methoden zuordnen.</span><span class="sxs-lookup"><span data-stu-id="08b11-263">Next, the effect must map this new property to getter and setter methods.</span></span> <span data-ttu-id="08b11-264">Dies erfolgt über das [**D2D1- \_ Eigenschafts \_ Bindungs**](/windows/desktop/api/d2d1effectauthor/ns-d2d1effectauthor-d2d1_property_binding) Array, das an die [**ID2D1Factory1:: registereffectfromstring**](/windows/win32/api/d2d1_1/nf-d2d1_1-id2d1factory1-registereffectfromstring) -Methode übergeben wird.</span><span class="sxs-lookup"><span data-stu-id="08b11-264">This is done through the [**D2D1\_PROPERTY\_BINDING**](/windows/desktop/api/d2d1effectauthor/ns-d2d1effectauthor-d2d1_property_binding) array that is passed into the [**ID2D1Factory1::RegisterEffectFromString**](/windows/win32/api/d2d1_1/nf-d2d1_1-id2d1factory1-registereffectfromstring) method.</span></span>

<span data-ttu-id="08b11-265">Das [**\_ \_ Bindungs**](/windows/desktop/api/d2d1effectauthor/ns-d2d1effectauthor-d2d1_property_binding) Array der D2D1-Eigenschaft sieht wie folgt aus:</span><span class="sxs-lookup"><span data-stu-id="08b11-265">The [**D2D1\_PROPERTY\_BINDING**](/windows/desktop/api/d2d1effectauthor/ns-d2d1effectauthor-d2d1_property_binding) array looks like this:</span></span>


```C++
const D2D1_PROPERTY_BINDING bindings[] =
{
    D2D1_VALUE_TYPE_BINDING(
        L"Offset",      // The name of property. Must match name attribute in XML.
        &SetOffset,     // The setter method that is called on "SetValue".
        &GetOffset      // The getter method that is called on "GetValue".
        )
};
```



<span data-ttu-id="08b11-266">Nachdem Sie das XML-und das Bindungs Array erstellt haben, übergeben Sie Sie an die [**registereffectfromstring**](/windows/win32/api/d2d1_1/nf-d2d1_1-id2d1factory1-registereffectfromstring) -Methode:</span><span class="sxs-lookup"><span data-stu-id="08b11-266">Once you create the XML and bindings array, pass them into the [**RegisterEffectFromString**](/windows/win32/api/d2d1_1/nf-d2d1_1-id2d1factory1-registereffectfromstring) method:</span></span>


```C++
pFactory->RegisterEffectFromString(
    CLSID_SampleEffect,  // GUID defined in class header file.
    pszXml,              // Previously-defined XML that describes effect.
    bindings,            // The previously-defined property bindings array.
    ARRAYSIZE(bindings), // Number of entries in the property bindings array.    
    CreateEffect         // Static method that returns an instance of the effect's class.
    );
```



<span data-ttu-id="08b11-267">Das Bindungs Makro des D2D1- \_ \_ Werttyps \_ erfordert, dass die Effect-Klasse vor jeder anderen Schnittstelle von [**ID2D1EffectImpl**](/windows/win32/api/d2d1effectauthor/nn-d2d1effectauthor-id2d1effectimpl) geerbt wird.</span><span class="sxs-lookup"><span data-stu-id="08b11-267">The D2D1\_VALUE\_TYPE\_BINDING macro requires the effect class to inherit from [**ID2D1EffectImpl**](/windows/win32/api/d2d1effectauthor/nn-d2d1effectauthor-id2d1effectimpl) before any other interface.</span></span>

<span data-ttu-id="08b11-268">Benutzerdefinierte Eigenschaften für einen Effekt werden in der Reihenfolge indiziert, in der Sie in der XML-Datei deklariert sind. nach der Erstellung kann die App mithilfe der [**ID2D1Properties:: SetValue**](id2d1properties-setvalue-overload.md) -Methode und der [**ID2D1Properties:: GetValue**](id2d1properties-getvalue-overload.md) -Methode darauf zugreifen.</span><span class="sxs-lookup"><span data-stu-id="08b11-268">Custom properties for an effect are indexed in the order they are declared in the XML, and once created can be accessed by the app using the [**ID2D1Properties::SetValue**](id2d1properties-setvalue-overload.md) and [**ID2D1Properties::GetValue**](id2d1properties-getvalue-overload.md) methods.</span></span> <span data-ttu-id="08b11-269">Zur einfacheren Handhabung können Sie eine öffentliche Enumeration erstellen, die jede Eigenschaft in der Header Datei des Effekts auflistet:</span><span class="sxs-lookup"><span data-stu-id="08b11-269">For convenience, you can create a public enumeration that lists each property in the effect's header file:</span></span>


```C++
typedef enum SAMPLEEFFECT_PROP
{
    SAMPLEFFECT_PROP_OFFSET = 0
};
```



### <a name="create-the-getter-and-setter-methods-for-the-property"></a><span data-ttu-id="08b11-270">Erstellen der Getter-und Setter-Methoden für die Eigenschaft</span><span class="sxs-lookup"><span data-stu-id="08b11-270">Create the getter and setter methods for the property</span></span>

<span data-ttu-id="08b11-271">Der nächste Schritt besteht darin, die Getter-und Setter-Methoden für die neue Eigenschaft zu erstellen.</span><span class="sxs-lookup"><span data-stu-id="08b11-271">The next step is to create the getter and setter methods for the new property.</span></span> <span data-ttu-id="08b11-272">Die Namen der Methoden müssen mit den Namen der Methoden identisch sein, die im [**\_ \_ Bindungs**](/windows/desktop/api/d2d1effectauthor/ns-d2d1effectauthor-d2d1_property_binding) Array der D2D1-Eigenschaft angegeben sind.</span><span class="sxs-lookup"><span data-stu-id="08b11-272">The names of the methods must match the ones specified in the [**D2D1\_PROPERTY\_BINDING**](/windows/desktop/api/d2d1effectauthor/ns-d2d1effectauthor-d2d1_property_binding) array.</span></span> <span data-ttu-id="08b11-273">Außerdem muss der im XML-Code des Effekts angegebene Eigenschaftentyp mit dem Typ des Parameters der Setter-Methode und dem Rückgabewert der Getter-Methode identisch sein.</span><span class="sxs-lookup"><span data-stu-id="08b11-273">In addition, the property type specified in the effect's XML must match the type of the setter method's parameter and the getter method's return value.</span></span>


```C++
HRESULT SampleEffect::SetOffset(D2D_VECTOR_2F offset)
{
    // Method must manually clamp to values defined in XML.
    offset.x = min(offset.x, 1000.0f); 
    offset.x = max(offset.x, -1000.0f); 

    offset.y = min(offset.y, 1000.0f); 
    offset.y = max(offset.y, -1000.0f); 

    m_offset = offset;

    return S_OK;
}

D2D_VECTOR_2F SampleEffect::GetOffset() const
{
    return m_offset;
}
```



### <a name="update-effects-transforms-in-response-to-property-change"></a><span data-ttu-id="08b11-274">Aktualisieren von Effekt Transformationen als Reaktion auf Eigenschafts Änderung</span><span class="sxs-lookup"><span data-stu-id="08b11-274">Update effect's transforms in response to property change</span></span>

<span data-ttu-id="08b11-275">Um die Bild Ausgabe eines Effekts als Reaktion auf eine Eigenschafts Änderung tatsächlich zu aktualisieren, muss der Effekt die zugrunde liegenden Transformationen ändern.</span><span class="sxs-lookup"><span data-stu-id="08b11-275">To actually update an effect's image output in response to a property change, the effect needs to change its underlying transforms.</span></span> <span data-ttu-id="08b11-276">Dies erfolgt in der Regel in der [**prepareforrendering**](/windows/win32/api/d2d1effectauthor/nf-d2d1effectauthor-id2d1effectimpl-prepareforrender) -Methode des Effekts, die [Direct2D](./direct2d-portal.md) automatisch aufruft, wenn eine der Eigenschaften eines Effekts geändert wurde.</span><span class="sxs-lookup"><span data-stu-id="08b11-276">This is typically done in the effect's [**PrepareForRender**](/windows/win32/api/d2d1effectauthor/nf-d2d1effectauthor-id2d1effectimpl-prepareforrender) method which [Direct2D](./direct2d-portal.md) automatically calls when one of an effect's properties has been changed.</span></span> <span data-ttu-id="08b11-277">Allerdings können Transformationen in den Methoden des Effekts aktualisiert werden, wie z. b. Initialize oder die Eigenschaften Setter-Methoden des Effekts.</span><span class="sxs-lookup"><span data-stu-id="08b11-277">However, transforms can be updated in any of the effect's methods: such as Initialize or the effect's property setter methods.</span></span>

<span data-ttu-id="08b11-278">Wenn beispielsweise ein Effekt ein [**ID2D1OffsetTransform**](/windows/win32/api/d2d1effectauthor/nn-d2d1effectauthor-id2d1offsettransform) enthielt und den Offset Wert in Reaktion auf die geänderte Offset Eigenschaft des Effekts ändern wollte, würde er den folgenden Code in [**prepareforrendering**](/windows/win32/api/d2d1effectauthor/nf-d2d1effectauthor-id2d1effectimpl-prepareforrender)hinzufügen:</span><span class="sxs-lookup"><span data-stu-id="08b11-278">For example, if an effect contained an [**ID2D1OffsetTransform**](/windows/win32/api/d2d1effectauthor/nn-d2d1effectauthor-id2d1offsettransform) and wanted to modify its offset value in response to the effect's Offset property being changed, it would add the following code in [**PrepareForRender**](/windows/win32/api/d2d1effectauthor/nf-d2d1effectauthor-id2d1effectimpl-prepareforrender):</span></span>


```C++
IFACEMETHODIMP SampleEffect::PrepareForRender(D2D1_CHANGE_TYPE changeType)
{
    // All effect properties are DPI independent (specified in DIPs). In this offset
    // example, the offset value provided must be scaled from DIPs to pixels to ensure
    // a consistent appearance at different DPIs (excluding minor scaling artifacts).
    // A context's DPI can be retrieved using the ID2D1EffectContext::GetDPI API.
    
    D2D1_POINT_2L pixelOffset;
    pixelOffset.x = static_cast<LONG>(m_offset.x * (m_dpiX / 96.0f));
    pixelOffset.y = static_cast<LONG>(m_offset.y * (m_dpiY / 96.0f));
    
    // Update the effect's offset transform with the new offset value.
    m_pOffsetTransform->SetOffset(pixelOffset);

    return S_OK;
}
```



## <a name="creating-a-custom-transform"></a><span data-ttu-id="08b11-279">Erstellen einer benutzerdefinierten Transformation</span><span class="sxs-lookup"><span data-stu-id="08b11-279">Creating a custom transform</span></span>

<span data-ttu-id="08b11-280">Um Bild Vorgänge zu implementieren, die über die in [Direct2D](./direct2d-portal.md)bereitgestellten verfügen, müssen Sie benutzerdefinierte Transformationen implementieren.</span><span class="sxs-lookup"><span data-stu-id="08b11-280">To implement image operations beyond what is provided in [Direct2D](./direct2d-portal.md), you must implement custom transforms.</span></span> <span data-ttu-id="08b11-281">Benutzerdefinierte Transformationen können ein Eingabebild willkürlich durch die Verwendung benutzerdefinierter HLSL-Shader ändern.</span><span class="sxs-lookup"><span data-stu-id="08b11-281">Custom transforms can arbitrarily change an input image through the use of custom HLSL shaders.</span></span>

<span data-ttu-id="08b11-282">Transformationen implementieren eine von zwei verschiedenen Schnittstellen, je nachdem, welche Typen von Shadern Sie verwenden.</span><span class="sxs-lookup"><span data-stu-id="08b11-282">Transforms implement one of two different interfaces depending on the types of shaders they use.</span></span> <span data-ttu-id="08b11-283">Transformationen, die Pixel-und/oder Vertex-Shader verwenden, müssen [**ID2D1DrawTransform**](/windows/win32/api/d2d1effectauthor/nn-d2d1effectauthor-id2d1drawtransform)implementieren, während Transformationen mit COMPUTE-Shadern [**ID2D1ComputeTransform**](/windows/win32/api/d2d1effectauthor/nn-d2d1effectauthor-id2d1computetransform)implementieren müssen.</span><span class="sxs-lookup"><span data-stu-id="08b11-283">Transforms using pixel and/or vertex shaders must implement [**ID2D1DrawTransform**](/windows/win32/api/d2d1effectauthor/nn-d2d1effectauthor-id2d1drawtransform), while transforms using compute shaders must implement [**ID2D1ComputeTransform**](/windows/win32/api/d2d1effectauthor/nn-d2d1effectauthor-id2d1computetransform).</span></span> <span data-ttu-id="08b11-284">Diese Schnittstellen erben beide von [**ID2D1Transform**](/windows/win32/api/d2d1effectauthor/nn-d2d1effectauthor-id2d1transform).</span><span class="sxs-lookup"><span data-stu-id="08b11-284">These interfaces both inherit from [**ID2D1Transform**](/windows/win32/api/d2d1effectauthor/nn-d2d1effectauthor-id2d1transform).</span></span> <span data-ttu-id="08b11-285">In diesem Abschnitt geht es um die Implementierung der Funktionalität, die für beides gilt.</span><span class="sxs-lookup"><span data-stu-id="08b11-285">This section focuses on implementing the functionality that is common to both.</span></span>

<span data-ttu-id="08b11-286">Die [**ID2D1Transform**](/windows/win32/api/d2d1effectauthor/nn-d2d1effectauthor-id2d1transform) -Schnittstelle verfügt über vier Methoden zur Implementierung:</span><span class="sxs-lookup"><span data-stu-id="08b11-286">The [**ID2D1Transform**](/windows/win32/api/d2d1effectauthor/nn-d2d1effectauthor-id2d1transform) interface has four methods to implement:</span></span>

### <a name="getinputcount"></a><span data-ttu-id="08b11-287">GetInputCount</span><span class="sxs-lookup"><span data-stu-id="08b11-287">GetInputCount</span></span>

<span data-ttu-id="08b11-288">Diese Methode gibt eine ganze Zahl zurück, die die Eingabe Anzahl für die Transformation darstellt.</span><span class="sxs-lookup"><span data-stu-id="08b11-288">This method returns an integer representing the input count for the transform.</span></span>


```C++
IFACEMETHODIMP_(UINT32) GetInputCount() const
{
    return 1;
}
```



### <a name="mapinputrectstooutputrect"></a><span data-ttu-id="08b11-289">Mapinputrectstooutputrect</span><span class="sxs-lookup"><span data-stu-id="08b11-289">MapInputRectsToOutputRect</span></span>

<span data-ttu-id="08b11-290">[Direct2D](./direct2d-portal.md) Ruft die [**mapinputrectstooutputrect**](/windows/win32/api/d2d1effectauthor/nf-d2d1effectauthor-id2d1transform-mapinputrectstooutputrect) -Methode jedes Mal auf, wenn die Transformation gerendert wird.</span><span class="sxs-lookup"><span data-stu-id="08b11-290">[Direct2D](./direct2d-portal.md) calls the [**MapInputRectsToOutputRect**](/windows/win32/api/d2d1effectauthor/nf-d2d1effectauthor-id2d1transform-mapinputrectstooutputrect) method each time the transform is rendered.</span></span> <span data-ttu-id="08b11-291">Direct2D übergibt ein Rechteck, das die Begrenzungen der einzelnen Eingaben für die Transformation darstellt.</span><span class="sxs-lookup"><span data-stu-id="08b11-291">Direct2D passes a rectangle representing the bounds of each of the inputs to the transform.</span></span> <span data-ttu-id="08b11-292">Die Transformation ist dann dafür verantwortlich, die Begrenzungen des Ausgabe Bilds zu berechnen.</span><span class="sxs-lookup"><span data-stu-id="08b11-292">The transform is then responsible for calculating the bounds of the output image.</span></span> <span data-ttu-id="08b11-293">Die Größe der Rechtecke für alle Methoden in dieser Schnittstelle ([**ID2D1Transform**](/windows/win32/api/d2d1effectauthor/nn-d2d1effectauthor-id2d1transform)) wird in Pixel, nicht in Dips, definiert.</span><span class="sxs-lookup"><span data-stu-id="08b11-293">The size of the rectangles for all the methods on this interface ([**ID2D1Transform**](/windows/win32/api/d2d1effectauthor/nn-d2d1effectauthor-id2d1transform)) are defined in pixels, not DIPs.</span></span>

<span data-ttu-id="08b11-294">Diese Methode ist auch für die Berechnung des Bereichs der Ausgabe verantwortlich, der auf der Grundlage der Logik seines Shaders und der nicht transparenten Bereiche der einzelnen Eingaben nicht transparent ist.</span><span class="sxs-lookup"><span data-stu-id="08b11-294">This method is also responsible for calculating the region of the output that is opaque based on the logic of its shader and the opaque regions of each input.</span></span> <span data-ttu-id="08b11-295">Ein undurchsichtiger Bereich eines Bilds ist so definiert, dass der Alphakanal für das gesamte Rechteck den Wert "1" hat.</span><span class="sxs-lookup"><span data-stu-id="08b11-295">An opaque region of an image is defined as that where the alpha channel is '1' for the entirety of the rectangle.</span></span> <span data-ttu-id="08b11-296">Wenn unklar ist, ob die Ausgabe einer Transformation nicht transparent ist, sollte das transparente Ausgabe Rechteck als sicherer Wert auf (0, 0, 0, 0) festgelegt werden.</span><span class="sxs-lookup"><span data-stu-id="08b11-296">If it is unclear whether a transform's output is opaque, the output opaque rectangle should be set to (0, 0, 0, 0) as a safe value.</span></span> <span data-ttu-id="08b11-297">[Direct2D](./direct2d-portal.md) verwendet diese Informationen, um renderoptimierungen mit "garantiertem nicht transparenten" Inhalt auszuführen.</span><span class="sxs-lookup"><span data-stu-id="08b11-297">[Direct2D](./direct2d-portal.md) uses this info to perform rendering optimizations with 'guaranteed opaque' content.</span></span> <span data-ttu-id="08b11-298">Wenn dieser Wert ungenau ist, kann dies zu einem falschen Rendering führen.</span><span class="sxs-lookup"><span data-stu-id="08b11-298">If this value is inaccurate, it can result in incorrect rendering.</span></span>

<span data-ttu-id="08b11-299">Sie können das Renderingverhalten der Transformation (wie in den Abschnitten 6 bis 8 definiert) während dieser Methode ändern.</span><span class="sxs-lookup"><span data-stu-id="08b11-299">The you can modify the transform's rendering behavior (as defined in sections 6 through 8) during this method.</span></span> <span data-ttu-id="08b11-300">Allerdings können Sie andere Transformationen im Transformations Diagramm oder das Diagramm Layout hier nicht ändern.</span><span class="sxs-lookup"><span data-stu-id="08b11-300">However, the you can't modify other transforms in the transform graph, or the graph layout itself here.</span></span>


```C++
IFACEMETHODIMP SampleTransform::MapInputRectsToOutputRect(
    _In_reads_(inputRectCount) const D2D1_RECT_L* pInputRects,
    _In_reads_(inputRectCount) const D2D1_RECT_L* pInputOpaqueSubRects,
    UINT32 inputRectCount,
    _Out_ D2D1_RECT_L* pOutputRect,
    _Out_ D2D1_RECT_L* pOutputOpaqueSubRect
    )
{
    // This transform is designed to only accept one input.
    if (inputRectCount != 1)
    {
        return E_INVALIDARG;
    }

    // The output of the transform will be the same size as the input.
    *pOutputRect = pInputRects[0];
    // Indicate that the image's opacity has not changed.
    *pOutputOpaqueSubRect = pInputOpaqueSubRects[0];
    // The size of the input image can be saved here for subsequent operations.
    m_inputRect = pInputRects[0];

    return S_OK;
}
```



<span data-ttu-id="08b11-301">Wenn Sie ein komplexeres Beispiel wünschen, sollten Sie überprüfen, wie ein einfacher weich Arbeits Vorgang dargestellt wird:</span><span class="sxs-lookup"><span data-stu-id="08b11-301">For a more complex example, consider how a simple blur operation would be represented:</span></span>

<span data-ttu-id="08b11-302">Wenn bei einem weichzeichenvorgang ein 5-Pixel-RADIUS verwendet wird, muss die Größe des Ausgabe Rechtecks um 5 Pixel erweitert werden (siehe unten).</span><span class="sxs-lookup"><span data-stu-id="08b11-302">If a blur operation uses a 5 pixel radius, the size of the output rectangle must expand by 5 pixels, as shown below.</span></span> <span data-ttu-id="08b11-303">Wenn Sie Rechteck Koordinaten ändern, muss eine Transformation sicherstellen, dass Ihre Logik keine over/Underflows in den Rechteck Koordinaten verursacht.</span><span class="sxs-lookup"><span data-stu-id="08b11-303">When modifying rectangle coordinates, a transform must ensure that its logic does not cause any over/underflows in the rectangle coordinates.</span></span>


```C++
// Expand output image by 5 pixels.

// Do not expand empty input rectangles.
if (pInputRects[0].right  > pInputRects[0].left &&
    pInputRects[0].bottom > pInputRects[0].top
    )
{
    pOutputRect->left   = ((pInputRects[0].left   - 5) < pInputRects[0].left  ) ? (pInputRects[0].left   - 5) : LONG_MIN;
    pOutputRect->top    = ((pInputRects[0].top    - 5) < pInputRects[0].top   ) ? (pInputRects[0].top    - 5) : LONG_MIN;
    pOutputRect->right  = ((pInputRects[0].right  + 5) > pInputRects[0].right ) ? (pInputRects[0].right  + 5) : LONG_MAX;
    pOutputRect->bottom = ((pInputRects[0].bottom + 5) > pInputRects[0].bottom) ? (pInputRects[0].bottom + 5) : LONG_MAX;
}
```



<span data-ttu-id="08b11-304">Da das Bild verschwommen ist, kann ein nicht transparenter Bereich des Bilds nun teilweise transparent sein.</span><span class="sxs-lookup"><span data-stu-id="08b11-304">Because the image is blurred, a region of the image which was opaque may now be partially transparent.</span></span> <span data-ttu-id="08b11-305">Dies liegt daran, dass der Bereich außerhalb des Bilds standardmäßig transparent schwarz ist und diese Transparenz mit dem Bild um die Ränder kombiniert wird.</span><span class="sxs-lookup"><span data-stu-id="08b11-305">This is because the area outside the image defaults to transparent black and this transparency will be blended into the image around the edges.</span></span> <span data-ttu-id="08b11-306">Die Transformation muss dies in den nicht transparenten Rechteck Berechnungen widerspiegeln:</span><span class="sxs-lookup"><span data-stu-id="08b11-306">The transform must reflect this in its output opaque rectangle calculations:</span></span>


```C++
// Shrink opaque region by 5 pixels.
pOutputOpaqueSubRect->left   = pInputOpaqueSubRects[0].left   + 5;
pOutputOpaqueSubRect->top    = pInputOpaqueSubRects[0].top    + 5;
pOutputOpaqueSubRect->right  = pInputOpaqueSubRects[0].right  - 5;
pOutputOpaqueSubRect->bottom = pInputOpaqueSubRects[0].bottom - 5;
```



<span data-ttu-id="08b11-307">Diese Berechnungen werden hier visualisiert:</span><span class="sxs-lookup"><span data-stu-id="08b11-307">These calculations are visualized here:</span></span>

![Darstellung der Rechteck Berechnung.](images/custom-effects2.png)

<span data-ttu-id="08b11-309">Weitere Informationen zu dieser Methode finden Sie auf der Referenzseite zum [**mapinputrectstooutputrect**](/windows/win32/api/d2d1effectauthor/nf-d2d1effectauthor-id2d1transform-mapinputrectstooutputrect) .</span><span class="sxs-lookup"><span data-stu-id="08b11-309">For more info about this method, see the [**MapInputRectsToOutputRect**](/windows/win32/api/d2d1effectauthor/nf-d2d1effectauthor-id2d1transform-mapinputrectstooutputrect) reference page.</span></span>

### <a name="mapoutputrecttoinputrects"></a><span data-ttu-id="08b11-310">Mapoutputrecttinputrects</span><span class="sxs-lookup"><span data-stu-id="08b11-310">MapOutputRectToInputRects</span></span>

<span data-ttu-id="08b11-311">[Direct2D](./direct2d-portal.md) Ruft die [**mapoutputrecttoinputrects**](/windows/win32/api/d2d1effectauthor/nf-d2d1effectauthor-id2d1transform-mapoutputrecttoinputrects) -Methode nach [**mapinputrectstooutputrect**](/windows/win32/api/d2d1effectauthor/nf-d2d1effectauthor-id2d1transform-mapinputrectstooutputrect)auf.</span><span class="sxs-lookup"><span data-stu-id="08b11-311">[Direct2D](./direct2d-portal.md) calls the [**MapOutputRectToInputRects**](/windows/win32/api/d2d1effectauthor/nf-d2d1effectauthor-id2d1transform-mapoutputrecttoinputrects) method after [**MapInputRectsToOutputRect**](/windows/win32/api/d2d1effectauthor/nf-d2d1effectauthor-id2d1transform-mapinputrectstooutputrect).</span></span> <span data-ttu-id="08b11-312">Die Transformation muss den Teil des Bilds berechnen, von dem aus gelesen werden muss, um den angeforderten Ausgabebereich ordnungsgemäß zu rendereln.</span><span class="sxs-lookup"><span data-stu-id="08b11-312">The transform must calculate what portion of the image it needs to read from in order to correctly render the requested output region.</span></span>

<span data-ttu-id="08b11-313">Wie bereits zuvor, wenn eine Auswirkung genau Pixel 1-1 zuordnet, kann Sie das Ausgabe Rechteck an das Eingabe Rechteck übergeben:</span><span class="sxs-lookup"><span data-stu-id="08b11-313">As before, if an effect strictly maps pixels 1-1, it can pass the output rectangle through to the input rectangle:</span></span>


```C++
IFACEMETHODIMP SampleTransform::MapOutputRectToInputRects(
    _In_ const D2D1_RECT_L* pOutputRect,
    _Out_writes_(inputRectCount) D2D1_RECT_L* pInputRects,
    UINT32 inputRectCount
    ) const
{
    // This transform is designed to only accept one input.
    if (inputRectCount != 1)
    {
        return E_INVALIDARG;
    }

    // The input needed for the transform is the same as the visible output.
    pInputRects[0] = *pOutputRect;
    return S_OK;
}
```



<span data-ttu-id="08b11-314">Ebenso, wenn eine Transformation ein Bild verkleinert oder erweitert (wie z. b. das Beispiel "weich"), verwenden Pixel häufig umgebende Pixel, um ihren Wert zu berechnen.</span><span class="sxs-lookup"><span data-stu-id="08b11-314">Likewise, if a transform shrinks or expands an image (like the blur example here), pixels often use surrounding pixels to calculate their value.</span></span> <span data-ttu-id="08b11-315">Bei einem weichungs Wert wird ein Pixel mit den umgebenden Pixeln durchlaufen, auch wenn Sie sich außerhalb der Begrenzungen des Eingabe Bilds befinden.</span><span class="sxs-lookup"><span data-stu-id="08b11-315">With a blur, a pixel is averaged with its surrounding pixels, even if they are outside of the bounds of the input image.</span></span> <span data-ttu-id="08b11-316">Dieses Verhalten wird in der Berechnung widergespiegelt.</span><span class="sxs-lookup"><span data-stu-id="08b11-316">This behavior is reflected in the calculation.</span></span> <span data-ttu-id="08b11-317">Wie zuvor prüft die Transformation beim Erweitern der Koordinaten eines Rechtecks nach Überläufen.</span><span class="sxs-lookup"><span data-stu-id="08b11-317">As before, the transform checks for overflows when expanding a rectangle's coordinates.</span></span>


```C++
// Expand the input rectangle to reflect that more pixels need to 
// be read from than are necessarily rendered in the effect's output.
pInputRects[0].left   = ((pOutputRect->left   - 5) < pOutputRect->left  ) ? (pOutputRect->left   - 5) : LONG_MIN;
pInputRects[0].top    = ((pOutputRect->top    - 5) < pOutputRect->top   ) ? (pOutputRect->top    - 5) : LONG_MIN;
pInputRects[0].right  = ((pOutputRect->right  + 5) > pOutputRect->right ) ? (pOutputRect->right  + 5) : LONG_MAX;
pInputRects[0].bottom = ((pOutputRect->bottom + 5) > pOutputRect->bottom) ? (pOutputRect->bottom + 5) : LONG_MAX;
```



<span data-ttu-id="08b11-318">In dieser Abbildung wird die Berechnung visualisiert.</span><span class="sxs-lookup"><span data-stu-id="08b11-318">This figure visualizes the calculation.</span></span> <span data-ttu-id="08b11-319">[Direct2D](./direct2d-portal.md) prüft automatisch transparente schwarze Pixel, in denen das Eingabebild nicht vorhanden ist, sodass die weich Zeichnung schrittweise mit den vorhandenen Inhalten auf dem Bildschirm kombiniert werden kann.</span><span class="sxs-lookup"><span data-stu-id="08b11-319">[Direct2D](./direct2d-portal.md) automatically samples transparent black pixels where the input image doesn't exist, allowing the blur to be blended gradually with the existing content on the screen.</span></span>

![Abbildung eines Effekts zum Sampling von transparenten schwarzen Pixeln außerhalb eines Rechtecks.](images/custom-effects3.png)

<span data-ttu-id="08b11-321">Wenn die Zuordnung nicht trivial ist, sollte diese Methode das Eingabe Rechteck auf den maximalen Bereich festlegen, um korrekte Ergebnisse sicherzustellen.</span><span class="sxs-lookup"><span data-stu-id="08b11-321">If the mapping is non-trivial, then this method should set the input rectangle to the maximum area to guarantee correct results.</span></span> <span data-ttu-id="08b11-322">Legen Sie hierzu den linken und den oberen Rand auf int \_ Min und den rechten und unteren Rand auf int max fest \_ .</span><span class="sxs-lookup"><span data-stu-id="08b11-322">To do this, set the left and top edges to INT\_MIN, and the right and bottom edges to INT\_MAX.</span></span>

<span data-ttu-id="08b11-323">Weitere Informationen zu dieser Methode finden Sie im Thema [**mapoutputrecttoinputrects**](/windows/win32/api/d2d1effectauthor/nf-d2d1effectauthor-id2d1transform-mapoutputrecttoinputrects) .</span><span class="sxs-lookup"><span data-stu-id="08b11-323">For more info about this method, see the [**MapOutputRectToInputRects**](/windows/win32/api/d2d1effectauthor/nf-d2d1effectauthor-id2d1transform-mapoutputrecttoinputrects) topic.</span></span>

### <a name="mapinvalidrect"></a><span data-ttu-id="08b11-324">Mapinvalidrect</span><span class="sxs-lookup"><span data-stu-id="08b11-324">MapInvalidRect</span></span>

<span data-ttu-id="08b11-325">[Direct2D](./direct2d-portal.md) ruft auch die [**mapinvalidrect**](/windows/win32/api/d2d1effectauthor/nf-d2d1effectauthor-id2d1transform-mapinvalidrect) -Methode auf.</span><span class="sxs-lookup"><span data-stu-id="08b11-325">[Direct2D](./direct2d-portal.md) also calls the [**MapInvalidRect**](/windows/win32/api/d2d1effectauthor/nf-d2d1effectauthor-id2d1transform-mapinvalidrect) method.</span></span> <span data-ttu-id="08b11-326">Anders als bei den [**mapinputrectstooutputrect**](/windows/win32/api/d2d1effectauthor/nf-d2d1effectauthor-id2d1transform-mapinputrectstooutputrect) -und [**mapoutputrecttoinputrects**](/windows/win32/api/d2d1effectauthor/nf-d2d1effectauthor-id2d1transform-mapoutputrecttoinputrects) -Methoden Direct2D ist es jedoch nicht garantiert, Sie zu einem bestimmten Zeitpunkt aufzurufen.</span><span class="sxs-lookup"><span data-stu-id="08b11-326">However, unlike the [**MapInputRectsToOutputRect**](/windows/win32/api/d2d1effectauthor/nf-d2d1effectauthor-id2d1transform-mapinputrectstooutputrect) and [**MapOutputRectToInputRects**](/windows/win32/api/d2d1effectauthor/nf-d2d1effectauthor-id2d1transform-mapoutputrecttoinputrects) methods Direct2D is not guaranteed to call it at any particular time.</span></span> <span data-ttu-id="08b11-327">Diese Methode entscheidet konzeptionell, welcher Teil der Ausgabe einer Transformation erneut gerendert werden muss, wenn ein Teil oder alle Eingaben geändert werden.</span><span class="sxs-lookup"><span data-stu-id="08b11-327">This method conceptually decides what part of a transform's output needs to be re-rendered in response to part or all of its input changing.</span></span> <span data-ttu-id="08b11-328">Es gibt drei verschiedene Szenarios, für die das ungültige Rect einer Transformation berechnet werden soll.</span><span class="sxs-lookup"><span data-stu-id="08b11-328">There are three different scenarios for which to calculate a transform's invalid rect.</span></span>

### <a name="transforms-with-one-to-one-pixel-mapping"></a><span data-ttu-id="08b11-329">Transformationen mit 1-zu-eins-Pixel Zuordnung</span><span class="sxs-lookup"><span data-stu-id="08b11-329">Transforms with one-to-one pixel mapping</span></span>

<span data-ttu-id="08b11-330">Übergeben Sie für Transformationen, die Pixel 1-1 zuordnen, einfach das ungültige Eingabe Rechteck an das ungültige Ausgabe Rechteck:</span><span class="sxs-lookup"><span data-stu-id="08b11-330">For transforms that map pixels 1-1, simply pass the invalid input rectangle through to the invalid output rectangle:</span></span>


```C++
IFACEMETHODIMP SampleTransform::MapInvalidRect(
    UINT32 inputIndex,
    D2D1_RECT_L invalidInputRect,
    _Out_ D2D1_RECT_L* pInvalidOutputRect
    ) const
{
    // This transform is designed to only accept one input.
    if (inputIndex != 0)
    {
        return E_INVALIDARG;
    }

    // If part of the transform's input is invalid, mark the corresponding
    // output region as invalid. 
    *pInvalidOutputRect = invalidInputRect;

    return S_OK;
}
```



### <a name="transforms-with-many-to-many-pixel-mapping"></a><span data-ttu-id="08b11-331">Transformationen mit m:n-pixelzuordnung</span><span class="sxs-lookup"><span data-stu-id="08b11-331">Transforms with many-to-many pixel mapping</span></span>

<span data-ttu-id="08b11-332">Wenn die Ausgabe Pixel einer Transformation von Ihrem umgebenden Bereich abhängen, muss das ungültige Eingabe Rechteck entsprechend erweitert werden.</span><span class="sxs-lookup"><span data-stu-id="08b11-332">When a transform's output pixels are dependent on their surrounding area, the invalid input rectangle must correspondingly be expanded.</span></span> <span data-ttu-id="08b11-333">Dies soll widerspiegeln, dass die Pixel, die das ungültige Eingabe Rechteck umgeben, ebenfalls beeinträchtigt werden und ungültig werden.</span><span class="sxs-lookup"><span data-stu-id="08b11-333">This is to reflect that pixels surrounding the invalid input rectangle will also be affected and become invalid.</span></span> <span data-ttu-id="08b11-334">Beispielsweise wird mit einem Wert von fünf Pixeln die folgende Berechnung verwendet:</span><span class="sxs-lookup"><span data-stu-id="08b11-334">For example, a five pixel blur uses the following calculation:</span></span>


```C++
// Expand the input invalid rectangle by five pixels in each direction. This
// reflects that a change in part of the given input image will cause a change
// in an expanded part of the output image (five pixels in each direction).
pInvalidOutputRect->left   = ((invalidInputRect.left   - 5) < invalidInputRect.left  ) ? (invalidInputRect.left   - 5) : LONG_MIN;
pInvalidOutputRect->top    = ((invalidInputRect.top    - 5) < invalidInputRect.top   ) ? (invalidInputRect.top    - 5) : LONG_MIN;
pInvalidOutputRect->right  = ((invalidInputRect.right  + 5) > invalidInputRect.right ) ? (invalidInputRect.right  + 5) : LONG_MAX;
pInvalidOutputRect->bottom = ((invalidInputRect.bottom + 5) > invalidInputRect.bottom) ? (invalidInputRect.bottom + 5) : LONG_MAX;
```



### <a name="transforms-with-complex-pixel-mapping"></a><span data-ttu-id="08b11-335">Transformationen mit komplexer Pixel Zuordnung</span><span class="sxs-lookup"><span data-stu-id="08b11-335">Transforms with complex pixel mapping</span></span>

<span data-ttu-id="08b11-336">Bei Transformationen, bei denen Eingabe-und Ausgabe Pixel nicht über eine einfache Zuordnung verfügen, kann die gesamte Ausgabe als ungültig markiert werden.</span><span class="sxs-lookup"><span data-stu-id="08b11-336">For transforms where input and output pixels do not have a simple mapping, the entire output can be marked as invalid.</span></span> <span data-ttu-id="08b11-337">Wenn eine Transformation z. b. einfach die durchschnittliche Farbe der Eingabe ausgibt, ändert sich die gesamte Ausgabe der Transformation, wenn sogar ein kleiner Teil der Eingabe geändert wird.</span><span class="sxs-lookup"><span data-stu-id="08b11-337">For example, if a transform simply outputs the average color of the input, the entire output of the transform changes if even a small part of the input is changed.</span></span> <span data-ttu-id="08b11-338">In diesem Fall sollte das ungültige Ausgabe Rechteck auf ein logisch unendliches Rechteck festgelegt werden (siehe unten).</span><span class="sxs-lookup"><span data-stu-id="08b11-338">In this case, the invalid output rectangle should be set to a logically infinite rectangle (shown below).</span></span> <span data-ttu-id="08b11-339">[Direct2D](./direct2d-portal.md) bindet dies automatisch an die Begrenzungen der Ausgabe.</span><span class="sxs-lookup"><span data-stu-id="08b11-339">[Direct2D](./direct2d-portal.md) automatically clamps this to the bounds of the output.</span></span>


```C++
// If any change in the input image affects the entire output, the
// transform should set pInvalidOutputRect to a logically infinite rect.
*pInvalidOutputRect = D2D1::RectL(LONG_MIN, LONG_MIN, LONG_MAX, LONG_MAX);
```



<span data-ttu-id="08b11-340">Weitere Informationen zu dieser Methode finden Sie im Thema [**mapinvalidrect**](/windows/win32/api/d2d1effectauthor/nf-d2d1effectauthor-id2d1transform-mapinvalidrect) .</span><span class="sxs-lookup"><span data-stu-id="08b11-340">For more info about this method, see the [**MapInvalidRect**](/windows/win32/api/d2d1effectauthor/nf-d2d1effectauthor-id2d1transform-mapinvalidrect) topic.</span></span>

<span data-ttu-id="08b11-341">Nachdem Sie diese Methoden implementiert haben, enthält der-Header ihrer Transformation Folgendes:</span><span class="sxs-lookup"><span data-stu-id="08b11-341">Once these methods have been implemented, your transform's header will contain the following:</span></span>


```C++
class SampleTransform : public ID2D1Transform 
{
public:
    SampleTransform();

    // ID2D1TransformNode Methods:
    IFACEMETHODIMP_(UINT32) GetInputCount() const;
    
    // ID2D1Transform Methods:
    IFACEMETHODIMP MapInputRectsToOutputRect(
        _In_reads_(inputRectCount) const D2D1_RECT_L* pInputRects,
        _In_reads_(inputRectCount) const D2D1_RECT_L* pInputOpaqueSubRects,
        UINT32 inputRectCount,
        _Out_ D2D1_RECT_L* pOutputRect,
        _Out_ D2D1_RECT_L* pOutputOpaqueSubRect
        );    

    IFACEMETHODIMP MapOutputRectToInputRects(
        _In_ const D2D1_RECT_L* pOutputRect,
        _Out_writes_(inputRectCount) D2D1_RECT_L* pInputRects,
        UINT32 inputRectCount
        ) const;

    IFACEMETHODIMP MapInvalidRect(
        UINT32 inputIndex,
        D2D1_RECT_L invalidInputRect,
        _Out_ D2D1_RECT_L* pInvalidOutputRect 
        ) const;

    // IUnknown Methods:
    IFACEMETHODIMP_(ULONG) AddRef();
    IFACEMETHODIMP_(ULONG) Release();
    IFACEMETHODIMP QueryInterface(REFIID riid, _Outptr_ void** ppOutput);

private:
    LONG m_cRef; // Internal ref count used by AddRef() and Release() methods.
    D2D1_RECT_L m_inputRect; // Stores the size of the input image.
};
```



## <a name="adding-a-pixel-shader-to-a-custom-transform"></a><span data-ttu-id="08b11-342">Hinzufügen eines Pixelshaders zu einer benutzerdefinierten Transformation</span><span class="sxs-lookup"><span data-stu-id="08b11-342">Adding a pixel shader to a custom transform</span></span>

<span data-ttu-id="08b11-343">Nachdem eine Transformation erstellt wurde, muss Sie einen Shader bereitstellen, der die Bild Pixel bearbeitet.</span><span class="sxs-lookup"><span data-stu-id="08b11-343">Once a transform has been created, it needs to provide a shader that will manipulate the image pixels.</span></span> <span data-ttu-id="08b11-344">In diesem Abschnitt werden die Schritte zum Verwenden eines Pixelshaders mit einer benutzerdefinierten Transformation behandelt.</span><span class="sxs-lookup"><span data-stu-id="08b11-344">This section covers the steps to using a pixel shader with a custom transform.</span></span>

### <a name="implementing-id2d1drawtransform"></a><span data-ttu-id="08b11-345">Implementieren von ID2D1DrawTransform</span><span class="sxs-lookup"><span data-stu-id="08b11-345">Implementing ID2D1DrawTransform</span></span>

<span data-ttu-id="08b11-346">Um einen PixelShader zu verwenden, muss die Transformation die [**ID2D1DrawTransform**](/windows/win32/api/d2d1effectauthor/nn-d2d1effectauthor-id2d1drawtransform) -Schnittstelle implementieren, die von der in Abschnitt 5 beschriebenen [**ID2D1Transform**](/windows/win32/api/d2d1effectauthor/nn-d2d1effectauthor-id2d1transform) -Schnittstelle erbt.</span><span class="sxs-lookup"><span data-stu-id="08b11-346">To use a pixel shader, the transform must implement the [**ID2D1DrawTransform**](/windows/win32/api/d2d1effectauthor/nn-d2d1effectauthor-id2d1drawtransform) interface, which inherits from the [**ID2D1Transform**](/windows/win32/api/d2d1effectauthor/nn-d2d1effectauthor-id2d1transform) interface described in section 5.</span></span> <span data-ttu-id="08b11-347">Diese Schnittstelle enthält eine neue Methode, die implementiert werden soll:</span><span class="sxs-lookup"><span data-stu-id="08b11-347">This interface contains one new method to implement:</span></span>

### <a name="setdrawinfoid2d1drawinfo-pdrawinfo"></a><span data-ttu-id="08b11-348">Setdrawinfo (ID2D1DrawInfo \* pdrawinfo)</span><span class="sxs-lookup"><span data-stu-id="08b11-348">SetDrawInfo(ID2D1DrawInfo \*pDrawInfo)</span></span>

<span data-ttu-id="08b11-349">[Direct2D](./direct2d-portal.md) Ruft die [**setdrawinfo**](/windows/win32/api/d2d1effectauthor/nf-d2d1effectauthor-id2d1drawtransform-setdrawinfo) -Methode auf, wenn die Transformation zum ersten Mal dem Transformations Diagramm eines Effekts hinzugefügt wird.</span><span class="sxs-lookup"><span data-stu-id="08b11-349">[Direct2D](./direct2d-portal.md) calls the [**SetDrawInfo**](/windows/win32/api/d2d1effectauthor/nf-d2d1effectauthor-id2d1drawtransform-setdrawinfo) method when the transform is first added to an effect's transform graph.</span></span> <span data-ttu-id="08b11-350">Diese Methode stellt einen [**ID2D1DrawInfo**](/windows/win32/api/d2d1effectauthor/nn-d2d1effectauthor-id2d1drawinfo) -Parameter bereit, der steuert, wie die Transformation gerendert wird.</span><span class="sxs-lookup"><span data-stu-id="08b11-350">This method provides an [**ID2D1DrawInfo**](/windows/win32/api/d2d1effectauthor/nn-d2d1effectauthor-id2d1drawinfo) parameter that controls how the transform is rendered.</span></span> <span data-ttu-id="08b11-351">Informationen zu den hier verfügbaren Methoden finden Sie im Thema **ID2D1DrawInfo** .</span><span class="sxs-lookup"><span data-stu-id="08b11-351">See the **ID2D1DrawInfo** topic for the methods available here.</span></span>

<span data-ttu-id="08b11-352">Wenn die Transformation diesen Parameter als Klassenmember-Variable speichert, kann auf das *drawinfo* -Objekt zugegriffen werden, und es kann von anderen Methoden wie z. b. Eigenschaften Setter oder [**mapinputrectstooutputrect**](/windows/win32/api/d2d1effectauthor/nf-d2d1effectauthor-id2d1transform-mapinputrectstooutputrect)geändert werden.</span><span class="sxs-lookup"><span data-stu-id="08b11-352">If the transform chooses to store this parameter as a class member variable, the *drawInfo* object can be accessed and changed from other methods such as property setters or [**MapInputRectsToOutputRect**](/windows/win32/api/d2d1effectauthor/nf-d2d1effectauthor-id2d1transform-mapinputrectstooutputrect).</span></span> <span data-ttu-id="08b11-353">Insbesondere kann Sie nicht von den [**mapoutputrectdeinputrects**](/windows/win32/api/d2d1effectauthor/nf-d2d1effectauthor-id2d1transform-mapoutputrecttoinputrects) -oder [**mapinvalidrect**](/windows/win32/api/d2d1effectauthor/nf-d2d1effectauthor-id2d1transform-mapinvalidrect) -Methoden auf [**ID2D1Transform**](/windows/win32/api/d2d1effectauthor/nn-d2d1effectauthor-id2d1transform)aufgerufen werden.</span><span class="sxs-lookup"><span data-stu-id="08b11-353">Notably, it cannot be called from the [**MapOutputRectToInputRects**](/windows/win32/api/d2d1effectauthor/nf-d2d1effectauthor-id2d1transform-mapoutputrecttoinputrects) or [**MapInvalidRect**](/windows/win32/api/d2d1effectauthor/nf-d2d1effectauthor-id2d1transform-mapinvalidrect) methods on [**ID2D1Transform**](/windows/win32/api/d2d1effectauthor/nn-d2d1effectauthor-id2d1transform).</span></span>

### <a name="creating-a-guid-for-the-pixel-shader"></a><span data-ttu-id="08b11-354">Erstellen einer GUID für den Pixelshader</span><span class="sxs-lookup"><span data-stu-id="08b11-354">Creating a GUID for the pixel shader</span></span>

<span data-ttu-id="08b11-355">Als nächstes muss die Transformation eine eindeutige GUID für den Pixelshader selbst definieren.</span><span class="sxs-lookup"><span data-stu-id="08b11-355">Next, the transform must define a unique GUID for the pixel shader itself.</span></span> <span data-ttu-id="08b11-356">Diese wird verwendet, wenn [Direct2D](./direct2d-portal.md) den Shader in den Arbeitsspeicher lädt, und wenn die Transformation den für die Ausführung zu verwendenden Pixelshader auswählt.</span><span class="sxs-lookup"><span data-stu-id="08b11-356">This is used when [Direct2D](./direct2d-portal.md) loads the shader into memory, as well as when the transform chooses which pixel shader to use for execution.</span></span> <span data-ttu-id="08b11-357">Tools wie guidgen.exe, die in Visual Studio enthalten sind, können verwendet werden, um eine zufällige GUID zu generieren.</span><span class="sxs-lookup"><span data-stu-id="08b11-357">Tools such as guidgen.exe, which is included with Visual Studio, can be used to generate a random GUID.</span></span>


```C++
// Example GUID used to uniquely identify HLSL shader. Passed to Direct2D during
// shader load, and used by the transform to identify the shader for the
// ID2D1DrawInfo::SetPixelShader method. The effect author should create a
// unique name for the shader as well as a unique GUID using
// a GUID generation tool.
DEFINE_GUID(GUID_SamplePixelShader, 0x00000000, 0x0000, 0x0000, 0x00, 0x00, 0x00, 0x00, 0x00, 0x00, 0x00, 0x00);
```



### <a name="loading-the-pixel-shader-with-direct2d"></a><span data-ttu-id="08b11-358">Der Pixelshader wird mit Direct2D geladen.</span><span class="sxs-lookup"><span data-stu-id="08b11-358">Loading the pixel shader with Direct2D</span></span>

<span data-ttu-id="08b11-359">Ein Pixelshader muss in den Arbeitsspeicher geladen werden, bevor er von der Transformation verwendet werden kann.</span><span class="sxs-lookup"><span data-stu-id="08b11-359">A pixel shader must be loaded into memory before it can be used by the transform.</span></span>

<span data-ttu-id="08b11-360">Um den Pixelshader in den Arbeitsspeicher zu laden, sollte die Transformation den kompilierten Shader-Bytecode aus dem Lesen. CSO-Datei, die von Visual Studio generiert wurde (Weitere Informationen finden Sie unter [Direct3D](/windows/desktop/direct3d11/atoc-dx-graphics-direct3d-11) -Dokumentation) in ein Bytearray.</span><span class="sxs-lookup"><span data-stu-id="08b11-360">To load the pixel shader into memory, the transform should read the compiled shader byte code from the .CSO file generated by Visual Studio (see [Direct3D](/windows/desktop/direct3d11/atoc-dx-graphics-direct3d-11) documentation for details) into a byte array.</span></span> <span data-ttu-id="08b11-361">Dieses Verfahren wird im [D2DCustomEffects SDK-Beispiel](https://github.com/Microsoft/Windows-universal-samples/tree/master/Samples/D2DCustomEffects)ausführlich erläutert.</span><span class="sxs-lookup"><span data-stu-id="08b11-361">This technique is demonstrated in detail in the [D2DCustomEffects SDK sample](https://github.com/Microsoft/Windows-universal-samples/tree/master/Samples/D2DCustomEffects).</span></span>

<span data-ttu-id="08b11-362">Nachdem die Shader-Daten in ein Bytearray geladen wurden, können Sie die [**loadpixelshader**](/windows/win32/api/d2d1effectauthor/nf-d2d1effectauthor-id2d1effectcontext-loadpixelshader) -Methode für das [**ID2D1EffectContext**](/windows/win32/api/d2d1effectauthor/nn-d2d1effectauthor-id2d1effectcontext) -Objekt des Effekts aufrufen.</span><span class="sxs-lookup"><span data-stu-id="08b11-362">Once the shader data has been loaded into a byte array, call the [**LoadPixelShader**](/windows/win32/api/d2d1effectauthor/nf-d2d1effectauthor-id2d1effectcontext-loadpixelshader) method on the effect's [**ID2D1EffectContext**](/windows/win32/api/d2d1effectauthor/nn-d2d1effectauthor-id2d1effectcontext) object.</span></span> <span data-ttu-id="08b11-363">[Direct2D](./direct2d-portal.md) ignoriert Aufrufe von **loadpixelshader** , wenn ein Shader mit der gleichen GUID bereits geladen wurde.</span><span class="sxs-lookup"><span data-stu-id="08b11-363">[Direct2D](./direct2d-portal.md) ignores calls to **LoadPixelShader** when a shader with the same GUID has already been loaded.</span></span>

<span data-ttu-id="08b11-364">Nachdem ein Pixelshader in den Arbeitsspeicher geladen wurde, muss die Transformation ihn zur Ausführung auswählen, indem er seine GUID an die [**setpixelshader**](/windows/win32/api/d2d1effectauthor/nf-d2d1effectauthor-id2d1drawinfo-setpixelshaderconstantbuffer) -Methode des [**ID2D1DrawInfo**](/windows/win32/api/d2d1effectauthor/nn-d2d1effectauthor-id2d1drawinfo) -Parameters übergibt, der während der [**setdrawinfo**](/windows/win32/api/d2d1effectauthor/nf-d2d1effectauthor-id2d1drawtransform-setdrawinfo) -Methode bereitgestellt wird.</span><span class="sxs-lookup"><span data-stu-id="08b11-364">After a pixel shader has been loaded into memory, the transform needs to select it for execution by passing its GUID to the [**SetPixelShader**](/windows/win32/api/d2d1effectauthor/nf-d2d1effectauthor-id2d1drawinfo-setpixelshaderconstantbuffer) method on the [**ID2D1DrawInfo**](/windows/win32/api/d2d1effectauthor/nn-d2d1effectauthor-id2d1drawinfo) parameter provided during the [**SetDrawInfo**](/windows/win32/api/d2d1effectauthor/nf-d2d1effectauthor-id2d1drawtransform-setdrawinfo) method.</span></span> <span data-ttu-id="08b11-365">Der Pixelshader muss bereits in den Arbeitsspeicher geladen werden, bevor er zur Ausführung ausgewählt wird.</span><span class="sxs-lookup"><span data-stu-id="08b11-365">The pixel shader must be already loaded into memory before being selected for execution.</span></span>

### <a name="changing-shader-operation-with-constant-buffers"></a><span data-ttu-id="08b11-366">Ändern des shadervorgangs mit konstantenpuffern</span><span class="sxs-lookup"><span data-stu-id="08b11-366">Changing shader operation with constant buffers</span></span>

<span data-ttu-id="08b11-367">Um zu ändern, wie ein Shader ausgeführt wird, kann eine Transformation einen konstanten Puffer an den Pixelshader übergeben.</span><span class="sxs-lookup"><span data-stu-id="08b11-367">To change how a shader executes, a transform may pass a constant buffer to the pixel shader.</span></span> <span data-ttu-id="08b11-368">Zu diesem Zweck definiert eine Transformation eine Struktur, die die gewünschten Variablen im Klassen Header enthält:</span><span class="sxs-lookup"><span data-stu-id="08b11-368">To do so, a transform defines a struct that contains the desired variables in the class header:</span></span>


```C++
// This struct defines the constant buffer of the pixel shader.
struct
{
    float valueOne;
    float valueTwo;
} m_constantBuffer;
```



<span data-ttu-id="08b11-369">Die Transformation ruft dann die [**ID2D1DrawInfo:: setpixelshaderconstantbuffer**](/windows/win32/api/d2d1effectauthor/nf-d2d1effectauthor-id2d1drawinfo-setpixelshaderconstantbuffer) -Methode für den [**ID2D1DrawInfo**](/windows/win32/api/d2d1effectauthor/nn-d2d1effectauthor-id2d1drawinfo) -Parameter auf, der in der [**setdrawinfo**](/windows/win32/api/d2d1effectauthor/nf-d2d1effectauthor-id2d1drawtransform-setdrawinfo) -Methode bereitgestellt wird, um diesen Puffer an den Shader zu übergeben.</span><span class="sxs-lookup"><span data-stu-id="08b11-369">The transform then calls the [**ID2D1DrawInfo::SetPixelShaderConstantBuffer**](/windows/win32/api/d2d1effectauthor/nf-d2d1effectauthor-id2d1drawinfo-setpixelshaderconstantbuffer) method on the [**ID2D1DrawInfo**](/windows/win32/api/d2d1effectauthor/nn-d2d1effectauthor-id2d1drawinfo) parameter provided in the [**SetDrawInfo**](/windows/win32/api/d2d1effectauthor/nf-d2d1effectauthor-id2d1drawtransform-setdrawinfo) method to pass this buffer to the shader.</span></span>

<span data-ttu-id="08b11-370">Das [HLSL](/windows/desktop/direct3dhlsl/dx-graphics-hlsl) muss auch eine entsprechende Struktur definieren, die den konstanten Puffer darstellt.</span><span class="sxs-lookup"><span data-stu-id="08b11-370">The [HLSL](/windows/desktop/direct3dhlsl/dx-graphics-hlsl) also needs to define a corresponding struct that represents the constant buffer.</span></span> <span data-ttu-id="08b11-371">Die Variablen, die in der Shader-Struktur enthalten sind, müssen mit denen in der Struktur der Transformation identisch sein.</span><span class="sxs-lookup"><span data-stu-id="08b11-371">The variables contained in the shader's struct must match those in the transform's struct.</span></span>


```C++
cbuffer constants : register(b0)
{
    float valueOne : packoffset(c0.x);
    float valueTwo : packoffset(c0.y);
};
```



<span data-ttu-id="08b11-372">Nachdem der Puffer definiert wurde, können die darin enthaltenen Werte von überall innerhalb des Pixelshader gelesen werden.</span><span class="sxs-lookup"><span data-stu-id="08b11-372">Once the buffer has been defined, the values contained within can be read from anywhere within the pixel shader.</span></span>

### <a name="writing-a-pixel-shader-for-direct2d"></a><span data-ttu-id="08b11-373">Schreiben eines Pixelshaders für Direct2D</span><span class="sxs-lookup"><span data-stu-id="08b11-373">Writing a pixel shader for Direct2D</span></span>

<span data-ttu-id="08b11-374">[Direct2D](./direct2d-portal.md) -Transformationen verwenden Shader, die mithilfe von Standard [HLSL](/windows/desktop/direct3dhlsl/dx-graphics-hlsl)erstellt wurden.</span><span class="sxs-lookup"><span data-stu-id="08b11-374">[Direct2D](./direct2d-portal.md) transforms use shaders authored using standard [HLSL](/windows/desktop/direct3dhlsl/dx-graphics-hlsl).</span></span> <span data-ttu-id="08b11-375">Es gibt jedoch einige wichtige Konzepte zum Schreiben eines Pixelshaders, der aus dem Kontext einer Transformation ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="08b11-375">However, there are a few key concepts to writing a pixel shader that executes from the context of a transform.</span></span> <span data-ttu-id="08b11-376">Ein vollständiges Beispiel für einen vollständig funktionalen Pixelshader finden Sie im [D2DCustomEffects SDK-Beispiel](https://github.com/Microsoft/Windows-universal-samples/tree/master/Samples/D2DCustomEffects).</span><span class="sxs-lookup"><span data-stu-id="08b11-376">For a completed example of a fully functionally pixel shader, see the [D2DCustomEffects SDK sample](https://github.com/Microsoft/Windows-universal-samples/tree/master/Samples/D2DCustomEffects).</span></span>

<span data-ttu-id="08b11-377">[Direct2D](./direct2d-portal.md) ordnet die Eingaben einer Transformation automatisch den [**Texture2D**](/windows/desktop/direct3dhlsl/sm5-object-texture2d) -und [**samplerstate**](/windows/desktop/api/d3d11/nn-d3d11-id3d11samplerstate) -Objekten in HLSL zu.</span><span class="sxs-lookup"><span data-stu-id="08b11-377">[Direct2D](./direct2d-portal.md) automatically maps a transform's inputs to [**Texture2D**](/windows/desktop/direct3dhlsl/sm5-object-texture2d) and [**SamplerState**](/windows/desktop/api/d3d11/nn-d3d11-id3d11samplerstate) objects in the HLSL.</span></span> <span data-ttu-id="08b11-378">Der erste **Texture2D** befindet sich unter Register T0 und der erste **samplerstate** unter Register S0.</span><span class="sxs-lookup"><span data-stu-id="08b11-378">The first **Texture2D** is located at register t0, and the first **SamplerState** is located at register s0.</span></span> <span data-ttu-id="08b11-379">Jede zusätzliche Eingabe befindet sich unter den nächsten entsprechenden Registern (z. b. T1 und S1).</span><span class="sxs-lookup"><span data-stu-id="08b11-379">Each additional input is located at the next corresponding registers (t1 and s1 for example).</span></span> <span data-ttu-id="08b11-380">Die Pixel Daten für eine bestimmte Eingabe können durch Aufrufen von Sample für das **Texture2D** -Objekt und durch Übergabe des entsprechenden **samplerstate** -Objekts und der Texel-Koordinaten entnommen werden.</span><span class="sxs-lookup"><span data-stu-id="08b11-380">Pixel data for a particular input can be sampled by calling Sample on the **Texture2D** object and passing in the corresponding **SamplerState** object and the texel coordinates.</span></span>

<span data-ttu-id="08b11-381">Ein benutzerdefinierter Pixelshader wird einmal für jedes Pixel ausgeführt, das gerendert wird.</span><span class="sxs-lookup"><span data-stu-id="08b11-381">A custom pixel shader is run once for each pixel that is rendered.</span></span> <span data-ttu-id="08b11-382">Jedes Mal, wenn der Shader ausgeführt wird, stellt [Direct2D](./direct2d-portal.md) automatisch drei Parameter bereit, die die aktuelle Ausführungs Position identifizieren:</span><span class="sxs-lookup"><span data-stu-id="08b11-382">Each time the shader is run, [Direct2D](./direct2d-portal.md) automatically provides three parameters that identify its current execution position:</span></span>

-   <span data-ttu-id="08b11-383">Ausgabe des Szene Raums: dieser Parameter stellt die aktuelle Ausführungs Position in Bezug auf die Gesamt-Ziel Oberfläche dar.</span><span class="sxs-lookup"><span data-stu-id="08b11-383">Scene-space output: This parameter represents the current execution position in terms of the overall target surface.</span></span> <span data-ttu-id="08b11-384">Er ist in Pixeln definiert, und die minimalen/maximalen Werte entsprechen den Begrenzungen des Rechtecks, das von [**mapinputrectstooutputrect**](/windows/win32/api/d2d1effectauthor/nf-d2d1effectauthor-id2d1transform-mapinputrectstooutputrect)zurückgegeben wurde.</span><span class="sxs-lookup"><span data-stu-id="08b11-384">It is defined in pixels and its min/max values correspond to the bounds of the rectangle returned by [**MapInputRectsToOutputRect**](/windows/win32/api/d2d1effectauthor/nf-d2d1effectauthor-id2d1transform-mapinputrectstooutputrect).</span></span>
-   <span data-ttu-id="08b11-385">Ausgabe des Ausschneide Raums: dieser Parameter wird von Direct3D verwendet und darf nicht in einem Pixelshader einer Transformation verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="08b11-385">Clip-space output: This parameter is used by Direct3D, and is must not be used in a transform's pixel shader.</span></span>
-   <span data-ttu-id="08b11-386">Texspace Input: dieser Parameter stellt die aktuelle Ausführungs Position in einer bestimmten Eingabe Textur dar.</span><span class="sxs-lookup"><span data-stu-id="08b11-386">Texel-space input: This parameter represents the current execution position in a particular input texture.</span></span> <span data-ttu-id="08b11-387">Ein Shader sollte keinerlei Abhängigkeiten davon annehmen, wie dieser Wert berechnet wird.</span><span class="sxs-lookup"><span data-stu-id="08b11-387">A shader should not take any dependencies on how this value is calculated.</span></span> <span data-ttu-id="08b11-388">Es sollte nur verwendet werden, um die Eingabe des Pixels-Shaders zu übertragen, wie im folgenden Code gezeigt:</span><span class="sxs-lookup"><span data-stu-id="08b11-388">It should only use it to sample the pixel shader's input, as shown in the code below:</span></span>


```C++
Texture2D InputTexture : register(t0);
SamplerState InputSampler : register(s0);

float4 main(
    float4 clipSpaceOutput  : SV_POSITION,
    float4 sceneSpaceOutput : SCENE_POSITION,
    float4 texelSpaceInput0 : TEXCOORD0
    ) : SV_Target
{
    // Samples pixel from ten pixels above current position.

    float2 sampleLocation =
        texelSpaceInput0.xy    // Sample position for the current output pixel.
        + float2(0,-10)        // An offset from which to sample the input, specified in pixels.
        * texelSpaceInput0.zw; // Multiplier that converts pixel offset to sample position offset.

    float4 color = InputTexture.Sample(
        InputSampler,          // Sampler and Texture must match for a given input.
        sampleLocation
        );

    return color;
}
```



## <a name="adding-a-vertex-shader-to-a-custom-transform"></a><span data-ttu-id="08b11-389">Hinzufügen eines Vertex-Shaders zu einer benutzerdefinierten Transformation</span><span class="sxs-lookup"><span data-stu-id="08b11-389">Adding a vertex shader to a custom transform</span></span>

<span data-ttu-id="08b11-390">Mithilfe von Vertex-Shadern können Sie verschiedene Abbild Erstellungs Szenarien ausführen als Pixel-Shader.</span><span class="sxs-lookup"><span data-stu-id="08b11-390">You can use vertex shaders to accomplish different imaging scenarios than pixel shaders.</span></span> <span data-ttu-id="08b11-391">Vertex-Shader können auf Geometrie basierende Bildeffekte durch Transformieren von Vertices durchführen, die ein Bild bilden.</span><span class="sxs-lookup"><span data-stu-id="08b11-391">In particular, vertex shaders can perform geometry-based image effects by transforming vertices that comprise an image.</span></span> <span data-ttu-id="08b11-392">Vertex-Shader können unabhängig von oder in Verbindung mit von der Transformation angegebenen Pixel-Shadern verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="08b11-392">Vertex shaders can be used independently of or in conjunction with transform-specified pixel shaders.</span></span> <span data-ttu-id="08b11-393">Wenn kein Scheitelpunkt-Shader angegeben ist, ersetzt [Direct2D](./direct2d-portal.md) in einem standardmäßigen Vertex-Shader für die Verwendung mit dem benutzerdefinierten Pixelshader.</span><span class="sxs-lookup"><span data-stu-id="08b11-393">If a vertex shader is not specified, [Direct2D](./direct2d-portal.md) substitutes in a default vertex shader for use with the custom pixel shader.</span></span>

<span data-ttu-id="08b11-394">Der Prozess zum Hinzufügen eines Vertex-Shaders zu einer benutzerdefinierten Transformation ähnelt dem eines Pixelshaders – die Transformation implementiert die [**ID2D1DrawTransform**](/windows/win32/api/d2d1effectauthor/nn-d2d1effectauthor-id2d1drawtransform) -Schnittstelle, erstellt eine GUID und (optional) übergibt Konstante Puffer an den Shader.</span><span class="sxs-lookup"><span data-stu-id="08b11-394">The process for adding a vertex shader to a custom transform is similar to that of a pixel shader – the transform implements the [**ID2D1DrawTransform**](/windows/win32/api/d2d1effectauthor/nn-d2d1effectauthor-id2d1drawtransform) interface, creates a GUID, and (optionally) passes constant buffers to the shader.</span></span> <span data-ttu-id="08b11-395">Es gibt jedoch einige wichtige zusätzliche Schritte, die für Vertex-Shader eindeutig sind:</span><span class="sxs-lookup"><span data-stu-id="08b11-395">However, there are a few key additional steps that are unique to vertex shaders:</span></span>

### <a name="creating-a-vertex-buffer"></a><span data-ttu-id="08b11-396">Erstellen eines Scheitelpunkt Puffers</span><span class="sxs-lookup"><span data-stu-id="08b11-396">Creating a vertex buffer</span></span>

<span data-ttu-id="08b11-397">Ein Scheitelpunkt-Shader wird durch Definition an den an ihn weiter gegebenen Scheitel Punkten ausgeführt, nicht an einzelne Pixel.</span><span class="sxs-lookup"><span data-stu-id="08b11-397">A vertex shader by definition executes on vertices passed to it, not individual pixels.</span></span> <span data-ttu-id="08b11-398">Um die Scheitel Punkte für den Shader anzugeben, die auf ausgeführt werden sollen, erstellt eine Transformation einen Vertex-Puffer, der an den Shader übergeben werden soll.</span><span class="sxs-lookup"><span data-stu-id="08b11-398">To specify the vertices for the shader to execute on, a transform creates a vertex buffer to pass to the shader.</span></span> <span data-ttu-id="08b11-399">Das Layout der Scheitelpunkt Puffer geht über den Rahmen dieses Dokuments hinaus.</span><span class="sxs-lookup"><span data-stu-id="08b11-399">The layout of vertex buffers is beyond the scope of this document.</span></span> <span data-ttu-id="08b11-400">Weitere Informationen finden Sie in der [Direct3D-Referenz](/windows/desktop/direct3d11/atoc-dx-graphics-direct3d-11) oder im [D2DCustomEffects SDK-Beispiel](https://github.com/Microsoft/Windows-universal-samples/tree/master/Samples/D2DCustomEffects) für eine Beispiel Implementierung.</span><span class="sxs-lookup"><span data-stu-id="08b11-400">Please see the [Direct3D reference](/windows/desktop/direct3d11/atoc-dx-graphics-direct3d-11) for details, or the [D2DCustomEffects SDK sample](https://github.com/Microsoft/Windows-universal-samples/tree/master/Samples/D2DCustomEffects) for a sample implementation.</span></span>

<span data-ttu-id="08b11-401">Nach dem Erstellen eines Scheitelpunkt Puffers im Arbeitsspeicher verwendet die Transformation [**die Methode "**](/windows/win32/api/d2d1effectauthor/nf-d2d1effectauthor-id2d1effectcontext-createvertexbuffer) Methode" für das [**ID2D1EffectContext**](/windows/win32/api/d2d1effectauthor/nn-d2d1effectauthor-id2d1effectcontext) -Objekt des enthaltenden Effekts, um diese Daten an die GPU zu übergeben.</span><span class="sxs-lookup"><span data-stu-id="08b11-401">After creating a vertex buffer in memory, the transform uses the [**CreateVertexBuffer**](/windows/win32/api/d2d1effectauthor/nf-d2d1effectauthor-id2d1effectcontext-createvertexbuffer) method on the containing effect's [**ID2D1EffectContext**](/windows/win32/api/d2d1effectauthor/nn-d2d1effectauthor-id2d1effectcontext) object to pass that data to the GPU.</span></span> <span data-ttu-id="08b11-402">Weitere Informationen finden Sie im [D2DCustomEffects SDK-Beispiel](https://github.com/Microsoft/Windows-universal-samples/tree/master/Samples/D2DCustomEffects) für eine Beispiel Implementierung.</span><span class="sxs-lookup"><span data-stu-id="08b11-402">Again, see the [D2DCustomEffects SDK sample](https://github.com/Microsoft/Windows-universal-samples/tree/master/Samples/D2DCustomEffects) for a sample implementation.</span></span>

<span data-ttu-id="08b11-403">Wenn kein Scheitelpunkt Puffer von der Transformation angegeben wird, übergibt [Direct2D](./direct2d-portal.md) einen standardmäßigen Vertex-Puffer, der den Speicherort des rechteckigen Bilds darstellt.</span><span class="sxs-lookup"><span data-stu-id="08b11-403">If no vertex buffer is specified by the transform, [Direct2D](./direct2d-portal.md) passes a default vertex buffer representing the rectangular image location.</span></span>

### <a name="changing-setdrawinfo-to-utilize-a-vertex-shader"></a><span data-ttu-id="08b11-404">Ändern von setdrawinfo zum Verwenden eines Scheitelpunkt-Shaders</span><span class="sxs-lookup"><span data-stu-id="08b11-404">Changing SetDrawInfo to utilize a vertex shader</span></span>

<span data-ttu-id="08b11-405">Wie bei Pixel-Shadern muss die Transformation laden und einen Vertex-Shader für die Ausführung auswählen.</span><span class="sxs-lookup"><span data-stu-id="08b11-405">Like with pixel shaders, the transform must load and select a vertex shader for execution.</span></span> <span data-ttu-id="08b11-406">Um den Vertexshader zu laden, ruft er die [**loadvertexshader**](/windows/win32/api/d2d1effectauthor/nf-d2d1effectauthor-id2d1effectcontext-loadvertexshader) -Methode für die [**ID2D1EffectContext**](/windows/win32/api/d2d1effectauthor/nn-d2d1effectauthor-id2d1effectcontext) -Methode auf, die in der Initialize-Methode des Effekts empfangen wird.</span><span class="sxs-lookup"><span data-stu-id="08b11-406">To load the vertex shader, it calls the [**LoadVertexShader**](/windows/win32/api/d2d1effectauthor/nf-d2d1effectauthor-id2d1effectcontext-loadvertexshader) method on the [**ID2D1EffectContext**](/windows/win32/api/d2d1effectauthor/nn-d2d1effectauthor-id2d1effectcontext) method received in the effect's Initialize method.</span></span> <span data-ttu-id="08b11-407">Um den Vertex-Shader für die Ausführung auszuwählen, ruft er [**setvertexprocessing**](/windows/win32/api/d2d1effectauthor/nf-d2d1effectauthor-id2d1drawinfo-setvertexprocessing) für den [**ID2D1DrawInfo**](/windows/win32/api/d2d1effectauthor/nn-d2d1effectauthor-id2d1drawinfo) -Parameter auf, der in der [**setdrawinfo**](/windows/win32/api/d2d1effectauthor/nf-d2d1effectauthor-id2d1drawtransform-setdrawinfo) -Methode der Transformation empfangen wird.</span><span class="sxs-lookup"><span data-stu-id="08b11-407">To select the vertex shader for execution, it calls [**SetVertexProcessing**](/windows/win32/api/d2d1effectauthor/nf-d2d1effectauthor-id2d1drawinfo-setvertexprocessing) on the [**ID2D1DrawInfo**](/windows/win32/api/d2d1effectauthor/nn-d2d1effectauthor-id2d1drawinfo) parameter received in the transform's [**SetDrawInfo**](/windows/win32/api/d2d1effectauthor/nf-d2d1effectauthor-id2d1drawtransform-setdrawinfo) method.</span></span> <span data-ttu-id="08b11-408">Diese Methode akzeptiert eine GUID für einen zuvor geladenen Vertex-Shader sowie (optional) einen zuvor erstellten Vertex-Puffer, auf dem der Shader ausgeführt werden soll.</span><span class="sxs-lookup"><span data-stu-id="08b11-408">This method accepts a GUID for a previously-loaded vertex shader as well as (optionally) a previously-created vertex buffer for the shader to execute on.</span></span>

### <a name="implementing-a-direct2d-vertex-shader"></a><span data-ttu-id="08b11-409">Implementieren eines Direct2D Vertex-Shaders</span><span class="sxs-lookup"><span data-stu-id="08b11-409">Implementing a Direct2D vertex shader</span></span>

<span data-ttu-id="08b11-410">Eine Draw-Transformation kann sowohl einen Pixel-Shader als auch einen Vertexshader enthalten.</span><span class="sxs-lookup"><span data-stu-id="08b11-410">A draw transform can contain both a pixel shader and a vertex shader.</span></span> <span data-ttu-id="08b11-411">Wenn eine Transformation sowohl einen Pixel-Shader als auch einen Vertex-Shader definiert, wird die Ausgabe des Vertex-Shader direkt an den Pixelshader übergeben: die APP kann die Rückgabe Signatur des Vertex-Shaders/der Parameter des Pixel-Shaders anpassen, solange Sie konsistent sind.</span><span class="sxs-lookup"><span data-stu-id="08b11-411">If a transform defines both a pixel shader and a vertex shader, then the output from the vertex shader is given directly to the pixel shader: the app can customize the return signature of the vertex shader / the parameters of the pixel shader as long as they are consistent.</span></span>

<span data-ttu-id="08b11-412">Wenn eine Transformation dagegen nur einen Scheitelpunkt-Shader enthält und auf dem standardmäßigen Passthrough-Pixelshader von [Direct2D](./direct2d-portal.md)basiert, muss Sie die folgende Standardausgabe zurückgeben:</span><span class="sxs-lookup"><span data-stu-id="08b11-412">On the other hand, if a transform only contains a vertex shader, and relies on [Direct2D](./direct2d-portal.md)'s default pass-through pixel shader, it must return the following default output:</span></span>


```C++
struct VSOut
{
    float4 clipSpaceOutput  : SV_POSITION; 
    float4 sceneSpaceOutput : SCENE_POSITION;
    float4 texelSpaceInput0 : TEXCOORD0;  
};
```



<span data-ttu-id="08b11-413">Ein Scheitelpunkt-Shader speichert das Ergebnis seiner Scheitelpunkt Transformationen in der Szenen Raum-Ausgabevariable des Shader.</span><span class="sxs-lookup"><span data-stu-id="08b11-413">A vertex shader stores the result of its vertex transformations in the shader's Scene-space output variable.</span></span> <span data-ttu-id="08b11-414">Um die Ausgabevariablen für den Ausschneide Bereich und die texspace-Eingabevariablen zu berechnen, stellt [Direct2D](./direct2d-portal.md) automatisch Konvertierungs Matrizen in einem konstanten Puffer bereit:</span><span class="sxs-lookup"><span data-stu-id="08b11-414">To compute the Clip-space output and the Texel-space input variables, [Direct2D](./direct2d-portal.md) automatically provides conversion matrices in a constant buffer:</span></span>


```C++
// Constant buffer b0 is used to store the transformation matrices from scene space
// to clip space. Depending on the number of inputs to the vertex shader, there
// may be more or fewer "sceneToInput" matrices.
cbuffer Direct2DTransforms : register(b0)
{
    float2x1 sceneToOutputX;
    float2x1 sceneToOutputY;
    float2x1 sceneToInput0X;
    float2x1 sceneToInput0Y;
};
```



<span data-ttu-id="08b11-415">Ein Beispiel für einen Vertex-Shader-Code finden Sie unten, der die Konvertierungs Matrizen verwendet, um die richtigen Clip-und textzspaces zu berechnen, die von [Direct2D](./direct2d-portal.md)</span><span class="sxs-lookup"><span data-stu-id="08b11-415">Sample vertex shader code can be found below that uses the conversion matrices to calculate the correct clip and texel spaces expected by [Direct2D](./direct2d-portal.md):</span></span>


```C++
// Constant buffer b0 is used to store the transformation matrices from scene space
// to clip space. Depending on the number of inputs to the vertex shader, there
// may be more or fewer "sceneToInput" matrices.
cbuffer Direct2DTransforms : register(b0)
{
    float2x1 sceneToOutputX;
    float2x1 sceneToOutputY;
    float2x1 sceneToInput0X;
    float2x1 sceneToInput0Y;
};

// Default output structure. This can be customized if transform also contains pixel shader.
struct VSOut
{
    float4 clipSpaceOutput  : SV_POSITION; 
    float4 sceneSpaceOutput : SCENE_POSITION;
    float4 texelSpaceInput0 : TEXCOORD0;  
};

// The parameter(s) passed to the vertex shader are defined by the vertex buffer's layout
// as specified by the transform. If no vertex buffer is specified, Direct2D passes two
// triangles representing the rectangular image with the following layout:
//
//    float4 outputScenePosition : OUTPUT_SCENE_POSITION;
//
//    The x and y coordinates of the outputScenePosition variable represent the image's
//    position on the screen. The z and w coordinates are used for perspective and
//    depth-buffering.

VSOut GeometryVS(float4 outputScenePosition : OUTPUT_SCENE_POSITION) 
{
    VSOut output;

    // Compute Scene-space output (vertex simply passed-through here). 
    output.sceneSpaceOutput.x = outputScenePosition.x;
    output.sceneSpaceOutput.y = outputScenePosition.y;
    output.sceneSpaceOutput.z = outputScenePosition.z;
    output.sceneSpaceOutput.w = outputScenePosition.w;

    // Generate standard Clip-space output coordinates.
    output.clipSpaceOutput.x = (output.sceneSpaceOutput.x * sceneToOutputX[0]) +
        output.sceneSpaceOutput.w * sceneToOutputX[1];

    output.clipSpaceOutput.y = (output.sceneSpaceOutput.y * sceneToOutputY[0]) + 
        output.sceneSpaceOutput.w * sceneToOutputY[1];

    output.clipSpaceOutput.z = output.sceneSpaceOutput.z;
    output.clipSpaceOutput.w = output.sceneSpaceOutput.w;

    // Generate standard Texel-space input coordinates.
    output.texelSpaceInput0.x = (outputScenePosition.x * sceneToInput0X[0]) + sceneToInput0X[1];
    output.texelSpaceInput0.y = (outputScenePosition.y * sceneToInput0Y[0]) + sceneToInput0Y[1];
    output.texelSpaceInput0.z = sceneToInput0X[0];
    output.texelSpaceInput0.w = sceneToInput0Y[0];

    return output;  
}
```



<span data-ttu-id="08b11-416">Der obige Code kann als Ausgangspunkt für einen Vertex-Shader verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="08b11-416">The above code can be used as a starting point for a vertex shader.</span></span> <span data-ttu-id="08b11-417">Sie durchläuft lediglich das Eingabebild, ohne Transformationen auszuführen.</span><span class="sxs-lookup"><span data-stu-id="08b11-417">It merely passes through the input image without performing any transforms.</span></span> <span data-ttu-id="08b11-418">Weitere Informationen finden Sie im [D2DCustomEffects SDK-Beispiel](https://github.com/Microsoft/Windows-universal-samples/tree/master/Samples/D2DCustomEffects) für eine vollständig implementierte Vertex-Shader-basierte Transformation.</span><span class="sxs-lookup"><span data-stu-id="08b11-418">Again, see the [D2DCustomEffects SDK sample](https://github.com/Microsoft/Windows-universal-samples/tree/master/Samples/D2DCustomEffects) for a fully-implemented vertex shader-based transform.</span></span>

<span data-ttu-id="08b11-419">Wenn kein Scheitelpunkt Puffer von der Transformation angegeben wird, ersetzt [Direct2D](./direct2d-portal.md) in einem standardmäßigen Vertex-Puffer, der den Speicherort des rechteckigen Bilds darstellt.</span><span class="sxs-lookup"><span data-stu-id="08b11-419">If no vertex buffer is specified by the transform, [Direct2D](./direct2d-portal.md) substitutes in a default vertex buffer representing the rectangular image location.</span></span> <span data-ttu-id="08b11-420">Die Parameter für den Vertex-Shader werden in die Werte der Standard-Shader-Ausgabe geändert:</span><span class="sxs-lookup"><span data-stu-id="08b11-420">The parameters to the vertex shader are changed to those of the default shader output:</span></span>


```C++
struct VSIn
{
    float4 clipSpaceOutput  : SV_POSITION; 
    float4 sceneSpaceOutput : SCENE_POSITION;
    float4 texelSpaceInput0 : TEXCOORD0;  
};
```



<span data-ttu-id="08b11-421">Der Vertex-Shader kann seine Parameter *scenespaceoutput* und *clipspaceoutput* nicht ändern.</span><span class="sxs-lookup"><span data-stu-id="08b11-421">The vertex shader may not modify its *sceneSpaceOutput* and *clipSpaceOutput* parameters.</span></span> <span data-ttu-id="08b11-422">Diese müssen unverändert zurückgegeben werden.</span><span class="sxs-lookup"><span data-stu-id="08b11-422">It must return them unchanged.</span></span> <span data-ttu-id="08b11-423">Der *texelspaceinput* -Parameter kann jedoch für jedes Eingabebild geändert werden.</span><span class="sxs-lookup"><span data-stu-id="08b11-423">It may however modify the *texelSpaceInput* parameter(s) for each input image.</span></span> <span data-ttu-id="08b11-424">Wenn die Transformation auch einen benutzerdefinierten Pixelshader enthält, kann der Vertex-Shader weiterhin zusätzliche benutzerdefinierte Parameter direkt an den Pixelshader übergeben.</span><span class="sxs-lookup"><span data-stu-id="08b11-424">If the transform also contains a custom pixel shader, the vertex shader is still able to pass additional custom parameters directly to the pixel shader.</span></span> <span data-ttu-id="08b11-425">Außerdem wird der benutzerdefinierte Puffer der *scenespace* -Konvertierungs Matrizen (B0) nicht mehr bereitgestellt.</span><span class="sxs-lookup"><span data-stu-id="08b11-425">Additionally, the *sceneSpace* conversion matrices custom buffer (b0) is no longer provided.</span></span>

## <a name="adding-a-compute-shader-to-a-custom-transform"></a><span data-ttu-id="08b11-426">Hinzufügen eines Compute-Shaders zu einer benutzerdefinierten Transformation</span><span class="sxs-lookup"><span data-stu-id="08b11-426">Adding a compute shader to a custom transform</span></span>

<span data-ttu-id="08b11-427">Zum Schluss können benutzerdefinierte Transformationen Compute-Shader für bestimmte gezielte Szenarien nutzen.</span><span class="sxs-lookup"><span data-stu-id="08b11-427">Finally, custom transforms may utilize compute shaders for certain targeted scenarios.</span></span> <span data-ttu-id="08b11-428">Compute-Shader können zum Implementieren komplexer Bildeffekte verwendet werden, die willkürlichen Zugriff auf Eingabe-und Ausgabe Bild Puffer erfordern.</span><span class="sxs-lookup"><span data-stu-id="08b11-428">Compute shaders can be used to implement complex image effects that require arbitrary access to input and output image buffers.</span></span> <span data-ttu-id="08b11-429">Beispielsweise kann ein grundlegender histogrammalgorithmus nicht mit einem Pixelshader implementiert werden, da Einschränkungen für den Speicherzugriff bestehen.</span><span class="sxs-lookup"><span data-stu-id="08b11-429">For example, a basic histogram algorithm cannot be implemented with a pixel shader due to limitations on memory access.</span></span>

<span data-ttu-id="08b11-430">Da Compute-Shader höhere Anforderungen an die Hardware Funktionsebene als Pixel-Shader aufweisen, sollten nach Möglichkeit Pixel-Shader verwendet werden, um einen bestimmten Effekt zu implementieren.</span><span class="sxs-lookup"><span data-stu-id="08b11-430">Because compute shaders have higher hardware feature level requirements than pixel shaders, pixel shaders should be used when possible to implement a given effect.</span></span> <span data-ttu-id="08b11-431">Insbesondere können Compute-Shader nur auf den meisten DirectX 10-Karten der Ebene und höher ausgeführt werden.</span><span class="sxs-lookup"><span data-stu-id="08b11-431">Specifically, compute shaders only run on most DirectX 10 level cards and higher.</span></span> <span data-ttu-id="08b11-432">Wenn eine Transformation einen Compute-Shader verwendet, muss Sie zusätzlich zur Implementierung der [**ID2D1ComputeTransform**](/windows/win32/api/d2d1effectauthor/nn-d2d1effectauthor-id2d1computetransform) -Schnittstelle die entsprechende Hardwareunterstützung während der Instanziierung überprüfen.</span><span class="sxs-lookup"><span data-stu-id="08b11-432">If a transform chooses to use a compute shader, it must check for the appropriate hardware support during instantiation in addition to implementing the [**ID2D1ComputeTransform**](/windows/win32/api/d2d1effectauthor/nn-d2d1effectauthor-id2d1computetransform) interface.</span></span>

### <a name="checking-for-compute-shader-support"></a><span data-ttu-id="08b11-433">Überprüfen der Unterstützung von Compute-Shader</span><span class="sxs-lookup"><span data-stu-id="08b11-433">Checking for Compute Shader support</span></span>

<span data-ttu-id="08b11-434">Wenn ein Effekt einen Compute-Shader verwendet, muss er während seiner Erstellung mithilfe der [**ID2D1EffectContext:: checkfeaturesupport**](/windows/win32/api/d2d1effectauthor/nf-d2d1effectauthor-id2d1effectcontext-checkfeaturesupport) -Methode auf die Unterstützung von Compute-Shader überprüfen.</span><span class="sxs-lookup"><span data-stu-id="08b11-434">If an effect uses a compute shader, it must check for compute shader support during its creation using the [**ID2D1EffectContext::CheckFeatureSupport**](/windows/win32/api/d2d1effectauthor/nf-d2d1effectauthor-id2d1effectcontext-checkfeaturesupport) method.</span></span> <span data-ttu-id="08b11-435">Wenn die GPU keine Compute-Shader unterstützt, muss der Effekt [**D2DERR \_ unzureichende \_ Geräte \_ Funktionen**](direct2d-error-codes.md)zurückgeben.</span><span class="sxs-lookup"><span data-stu-id="08b11-435">If the GPU does not support compute shaders, the effect must return [**D2DERR\_INSUFFICIENT\_DEVICE\_CAPABILITIES**](direct2d-error-codes.md).</span></span>

<span data-ttu-id="08b11-436">Es gibt zwei verschiedene Arten von Compute-Shadern, die von einer Transformation verwendet werden können: Shader Model 4 (DirectX 10) und Shader Model 5 (DirectX 11).</span><span class="sxs-lookup"><span data-stu-id="08b11-436">There are two different types of compute shaders that a transform can use: Shader Model 4 (DirectX 10) and Shader Model 5 (DirectX 11).</span></span> <span data-ttu-id="08b11-437">Es gibt bestimmte Einschränkungen für Shader Model 4-Shader.</span><span class="sxs-lookup"><span data-stu-id="08b11-437">There are certain limitations to Shader Model 4 shaders.</span></span> <span data-ttu-id="08b11-438">Weitere Informationen finden Sie in der [Direct3D](/windows/desktop/direct3d11/atoc-dx-graphics-direct3d-11) -Dokumentation.</span><span class="sxs-lookup"><span data-stu-id="08b11-438">See the [Direct3D](/windows/desktop/direct3d11/atoc-dx-graphics-direct3d-11) documentation for details.</span></span> <span data-ttu-id="08b11-439">Transformationen können beide Typen von Shadern enthalten und können bei Bedarf auf Shader Model 4 zurückgreifen: im [D2DCustomEffects SDK-Beispiel](https://github.com/Microsoft/Windows-universal-samples/tree/master/Samples/D2DCustomEffects) finden Sie eine Implementierung dieses.</span><span class="sxs-lookup"><span data-stu-id="08b11-439">Transforms can contain both types of shaders, and can fall back to Shader Model 4 when required: see the [D2DCustomEffects SDK sample](https://github.com/Microsoft/Windows-universal-samples/tree/master/Samples/D2DCustomEffects) for an implementation of this.</span></span>

### <a name="implement-id2d1computetransform"></a><span data-ttu-id="08b11-440">Implementieren von ID2D1ComputeTransform</span><span class="sxs-lookup"><span data-stu-id="08b11-440">Implement ID2D1ComputeTransform</span></span>

<span data-ttu-id="08b11-441">Diese Schnittstelle enthält zwei neue Methoden, die implementiert werden müssen, zusätzlich zu den in [**ID2D1Transform**](/previous-versions/windows/desktop/legacy/dd371304(v=vs.85)):</span><span class="sxs-lookup"><span data-stu-id="08b11-441">This interface contains two new methods to implement in addition to the ones in [**ID2D1Transform**](/previous-versions/windows/desktop/legacy/dd371304(v=vs.85)):</span></span>

### <a name="setcomputeinfoid2d1computeinfo-pcomputeinfo"></a><span data-ttu-id="08b11-442">Setcomputeingefo (ID2D1ComputeInfo \* pcomputeingefo)</span><span class="sxs-lookup"><span data-stu-id="08b11-442">SetComputeInfo(ID2D1ComputeInfo \*pComputeInfo)</span></span>

<span data-ttu-id="08b11-443">Wie bei Pixel-und Vertex-Shadern ruft [Direct2D](./direct2d-portal.md) die [**setcomputeinfo**](/windows/win32/api/d2d1effectauthor/nf-d2d1effectauthor-id2d1computetransform-setcomputeinfo) -Methode auf, wenn die Transformation zum ersten Mal dem Transformations Diagramm eines Effekts hinzugefügt wird.</span><span class="sxs-lookup"><span data-stu-id="08b11-443">Like with pixel and vertex shaders, [Direct2D](./direct2d-portal.md) calls the [**SetComputeInfo**](/windows/win32/api/d2d1effectauthor/nf-d2d1effectauthor-id2d1computetransform-setcomputeinfo) method when the transform is first added to an effect's transform graph.</span></span> <span data-ttu-id="08b11-444">Diese Methode stellt einen [**ID2D1ComputeInfo**](/windows/win32/api/d2d1effectauthor/nn-d2d1effectauthor-id2d1computeinfo) -Parameter bereit, der steuert, wie die Transformation gerendert wird.</span><span class="sxs-lookup"><span data-stu-id="08b11-444">This method provides an [**ID2D1ComputeInfo**](/windows/win32/api/d2d1effectauthor/nn-d2d1effectauthor-id2d1computeinfo) parameter that controls how the transform is rendered.</span></span> <span data-ttu-id="08b11-445">Dazu gehört auch die Auswahl des Compute-Shaders, der durch die [**ID2D1ComputeInfo:: setcomputeshader**](/windows/win32/api/d2d1effectauthor/nf-d2d1effectauthor-id2d1computeinfo-setcomputeshaderconstantbuffer) -Methode ausgeführt werden soll.</span><span class="sxs-lookup"><span data-stu-id="08b11-445">This includes choosing the compute shader to execute through the [**ID2D1ComputeInfo::SetComputeShader**](/windows/win32/api/d2d1effectauthor/nf-d2d1effectauthor-id2d1computeinfo-setcomputeshaderconstantbuffer) method.</span></span> <span data-ttu-id="08b11-446">Wenn die Transformation diesen Parameter als Klassenmember-Variable speichert, kann auf Sie über eine beliebige Transformations-oder Effekt Methode zugegriffen und diese geändert werden, mit Ausnahme der [**mapoutputrectdeinputrects**](/windows/win32/api/d2d1effectauthor/nf-d2d1effectauthor-id2d1transform-mapoutputrecttoinputrects) -und [**mapinvalidrect**](/windows/win32/api/d2d1effectauthor/nf-d2d1effectauthor-id2d1transform-mapinvalidrect) -Methoden.</span><span class="sxs-lookup"><span data-stu-id="08b11-446">If the transform chooses to store this parameter as a class member variable, it can be accessed and changed from any transform or effect method with the exception of the [**MapOutputRectToInputRects**](/windows/win32/api/d2d1effectauthor/nf-d2d1effectauthor-id2d1transform-mapoutputrecttoinputrects) and [**MapInvalidRect**](/windows/win32/api/d2d1effectauthor/nf-d2d1effectauthor-id2d1transform-mapinvalidrect) methods.</span></span> <span data-ttu-id="08b11-447">Weitere hier verfügbare Methoden finden Sie im Thema **ID2D1ComputeInfo** .</span><span class="sxs-lookup"><span data-stu-id="08b11-447">See the **ID2D1ComputeInfo** topic for other methods available here.</span></span>

### <a name="calculatethreadgroupsid2d1computeinfo-poutputrect-uint32-pdimensionx-uint32-pdimensiony-uint32-pdimensionz"></a><span data-ttu-id="08b11-448">Calculatethrecgroups (ID2D1ComputeInfo \* poutputrect, UInt32 \* pdimensionx, UInt32 \* pdimensiony, UInt32 \* pdimensionz)</span><span class="sxs-lookup"><span data-stu-id="08b11-448">CalculateThreadgroups(ID2D1ComputeInfo \*pOutputRect, UINT32 \*pDimensionX, UINT32 \*pDimensionY, UINT32 \*pDimensionZ)</span></span>

<span data-ttu-id="08b11-449">Während Pixel-Shader pro Pixel ausgeführt werden und Vertex-Shader pro Scheitelpunkt ausgeführt werden, werden Compute-Shader auf der Basis von Thread Group ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="08b11-449">Whereas pixel shaders are executed on a per-pixel basis and vertex shaders are executed on a per-vertex basis, compute shaders are executed on a per-'threadgroup' basis.</span></span> <span data-ttu-id="08b11-450">Eine Thread Gruppe stellt eine Anzahl von Threads dar, die gleichzeitig auf der GPU ausgeführt werden.</span><span class="sxs-lookup"><span data-stu-id="08b11-450">A threadgroup represents a number of threads that execute concurrently on the GPU.</span></span> <span data-ttu-id="08b11-451">Der COMPUTE-Shader-HLSL-Code bestimmt, wie viele Threads pro Thread Group ausgeführt werden sollen.</span><span class="sxs-lookup"><span data-stu-id="08b11-451">The compute shader HLSL code decides how many threads should be executed per threadgroup.</span></span> <span data-ttu-id="08b11-452">Der Effekt skaliert die Anzahl der Thread Gruppen so, dass der Shader die gewünschte Anzahl von Uhrzeiten ausführt, abhängig von der Logik des Shaders.</span><span class="sxs-lookup"><span data-stu-id="08b11-452">The effect scales the number of threadgroups so that the shader executes the desired number of times, depending on the shader's logic.</span></span>

<span data-ttu-id="08b11-453">Die [**calculatethread Groups**](/windows/win32/api/d2d1effectauthor/nf-d2d1effectauthor-id2d1computetransform-calculatethreadgroups) -Methode ermöglicht der Transformation, zu informieren [Direct2D](./direct2d-portal.md) wie viele Thread Gruppen erforderlich sind, basierend auf der Größe des Bilds und den eigenen Kenntnissen des Shader der Transformation.</span><span class="sxs-lookup"><span data-stu-id="08b11-453">The [**CalculateThreadgroups**](/windows/win32/api/d2d1effectauthor/nf-d2d1effectauthor-id2d1computetransform-calculatethreadgroups) method allows the transform to inform [Direct2D](./direct2d-portal.md) how many thread groups are required, based on the size of the image and the transform's own knowledge of the shader.</span></span>

<span data-ttu-id="08b11-454">Die Häufigkeit, mit der der COMPUTE-Shader ausgeführt wird, ist ein Produkt der Thread Group-Anzahl, die hier angegeben ist, und der numThreads-Anmerkung im COMPUTE-Shader- [HLSL](/windows/desktop/direct3dhlsl/dx-graphics-hlsl).</span><span class="sxs-lookup"><span data-stu-id="08b11-454">The number of times the compute shader is executed is a product of the threadgroup counts specified here and the 'numthreads' annotation in the compute shader [HLSL](/windows/desktop/direct3dhlsl/dx-graphics-hlsl).</span></span> <span data-ttu-id="08b11-455">Wenn die Transformation z. b. die Thread Group-Dimensionen auf (2, 2, 1) festlegt, gibt der Shader (3, 3, 1) Threads pro Thread Gruppe an, dann werden 4 Thread Gruppen ausgeführt, von denen jeder über 9 Threads verfügt, sodass insgesamt 36 Thread Instanzen verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="08b11-455">For example, if the transform sets the threadgroup dimensions to be (2,2,1) the shader specifies (3,3,1) threads per threadgroup, then 4 threadgroups will be executed, each with 9 threads in them, for a total of 36 thread instances.</span></span>

<span data-ttu-id="08b11-456">Ein häufiges Szenario ist die Verarbeitung eines Ausgabe Pixels für jede Instanz des Compute-Shaders.</span><span class="sxs-lookup"><span data-stu-id="08b11-456">A common scenario is to process one output pixel for each instance of the compute shader.</span></span> <span data-ttu-id="08b11-457">Um die Anzahl der Thread Gruppen für dieses Szenario zu berechnen, dividiert die Transformation die Breite und Höhe des Bilds durch die entsprechenden x-und y-Dimensionen der "numThreads"-Anmerkung im COMPUTE-Shader- [HLSL](/windows/desktop/direct3dhlsl/dx-graphics-hlsl).</span><span class="sxs-lookup"><span data-stu-id="08b11-457">To calculate the number of thread groups for this scenario, the transform divides the width and height of the image by the respective x and y dimensions of the 'numthreads' annotation in the compute shader [HLSL](/windows/desktop/direct3dhlsl/dx-graphics-hlsl).</span></span>

<span data-ttu-id="08b11-458">Wichtig: Wenn diese Division durchgeführt wird, muss die Anzahl der angeforderten Thread Gruppen immer auf die nächste ganze Zahl aufgerundet werden, andernfalls werden die "restpixel" nicht auf ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="08b11-458">Importantly, if this division is performed, then the number of thread groups requested must always be rounded up to the nearest integer, otherwise the 'remainder' pixels will not be executed upon.</span></span> <span data-ttu-id="08b11-459">Wenn ein Shader (z. b.) ein einzelnes Pixel mit jedem Thread berechnet, würde der Code der Methode wie folgt aussehen.</span><span class="sxs-lookup"><span data-stu-id="08b11-459">If a shader (for example) computes a single pixel with each thread, the method's code would appear as follows.</span></span>


```C++
IFACEMETHODIMP SampleTransform::CalculateThreadgroups(
    _In_ const D2D1_RECT_L* pOutputRect,
    _Out_ UINT32* pDimensionX,
    _Out_ UINT32* pDimensionY,
    _Out_ UINT32* pDimensionZ
    )
{    
    // The input image's dimensions are divided by the corresponding number of threads in each
    // threadgroup. This is specified in the HLSL, and in this example is 24 for both the x and y
    // dimensions. Dividing the image dimensions by these values calculates the number of
    // thread groups that need to be executed.

    *pDimensionX = static_cast<UINT32>(
         ceil((m_inputRect.right - m_inputRect.left) / 24.0f);

    *pDimensionY = static_cast<UINT32>(
         ceil((m_inputRect.bottom - m_inputRect.top) / 24.0f);

    // The z dimension is set to '1' in this example because the shader will
    // only be executed once for each pixel in the two-dimensional input image.
    // This value can be increased to perform additional executions for a given
    // input position.
    *pDimensionZ = 1;

    return S_OK;
}
```



<span data-ttu-id="08b11-460">Der [HLSL](/windows/desktop/direct3dhlsl/dx-graphics-hlsl) verwendet den folgenden Code, um die Anzahl der Threads in den einzelnen Thread Gruppen anzugeben:</span><span class="sxs-lookup"><span data-stu-id="08b11-460">The [HLSL](/windows/desktop/direct3dhlsl/dx-graphics-hlsl) uses the following code to specify the number of threads in each thread group:</span></span>


```hlsl
// numthreads(x, y, z)
// This specifies the number of threads in each dispatched threadgroup. 
// For Shader Model 4, z == 1 and x*y*z <= 768. For Shader Model 5, z <= 64 and x*y*z <= 1024.
[numthreads(24, 24, 1)]
void main(
...
```



<span data-ttu-id="08b11-461">Während der Ausführung werden der aktuelle Thread Group und der aktuelle Thread Index als Parameter an die Shader-Methode übermittelt:</span><span class="sxs-lookup"><span data-stu-id="08b11-461">During execution, the current threadgroup and current thread index are passed as parameters to the shader method:</span></span>


```hlsl
#define NUMTHREADS_X 24
#define NUMTHREADS_Y 24

// numthreads(x, y, z)
// This specifies the number of threads in each dispatched threadgroup.
// For Shader Model 4, z == 1 and x*y*z <= 768. For Shader Model 5, z <= 64 and x*y*z <= 1024.
[numthreads(NUMTHREADS_X, NUMTHREADS_Y, 1)]
void main(
    // dispatchThreadId - Uniquely identifies a given execution of the shader, most commonly used parameter.
    // Definition: (groupId.x * NUM_THREADS_X + groupThreadId.x, groupId.y * NUMTHREADS_Y + groupThreadId.y,
    // groupId.z * NUMTHREADS_Z + groupThreadId.z)
    uint3 dispatchThreadId  : SV_DispatchThreadID,

    // groupThreadId - Identifies an individual thread within a thread group.
    // Range: (0 to NUMTHREADS_X - 1, 0 to NUMTHREADS_Y - 1, 0 to NUMTHREADS_Z - 1)
    uint3 groupThreadId     : SV_GroupThreadID,

    // groupId - Identifies which thread group the individual thread is being executed in.
    // Range defined in ID2D1ComputeTransform::CalculateThreadgroups.
    uint3 groupId           : SV_GroupID, 

    // One dimensional indentifier of a compute shader thread within a thread group.
    // Range: (0 to NUMTHREADS_X * NUMTHREADS_Y * NUMTHREADS_Z - 1)
    uint  groupIndex        : SV_GroupIndex
    )
{
...
```



### <a name="reading-image-data"></a><span data-ttu-id="08b11-462">Lesen von Bilddaten</span><span class="sxs-lookup"><span data-stu-id="08b11-462">Reading image data</span></span>

<span data-ttu-id="08b11-463">Compute-Shader greifen als einzelne zweidimensionale Textur auf das Eingabebild der Transformation zu:</span><span class="sxs-lookup"><span data-stu-id="08b11-463">Compute shaders access the transform's input image as a single two-dimensional texture:</span></span>


```hlsl
Texture2D<float4> InputTexture : register(t0);
SamplerState InputSampler : register(s0);
```



<span data-ttu-id="08b11-464">Wie bei Pixel-Shadern ist es jedoch nicht garantiert, dass die Daten des Bilds in der Textur mit (0,0) beginnen.</span><span class="sxs-lookup"><span data-stu-id="08b11-464">However, like pixel shaders, the image's data is not guaranteed to begin at (0, 0) on the texture.</span></span> <span data-ttu-id="08b11-465">Stattdessen stellt [Direct2D](./direct2d-portal.md) System Konstanten bereit, mit denen Shader eine beliebige Abweichung ausgleichen können:</span><span class="sxs-lookup"><span data-stu-id="08b11-465">Instead, [Direct2D](./direct2d-portal.md) provides system constants that allow shaders to compensate for any offset:</span></span>


```hlsl
// These are default constants passed by D2D.
cbuffer systemConstants : register(b0)
{
    int4 resultRect; // Represents the input rectangle to the shader in terms of pixels.
    float2 sceneToInput0X;
    float2 sceneToInput0Y;
};

// The image does not necessarily begin at (0,0) on InputTexture. The shader needs
// to use the coefficients provided by Direct2D to map the requested image data to
// where it resides on the texture.
float2 ConvertInput0SceneToTexelSpace(float2 inputScenePosition)
{
    float2 ret;
    ret.x = inputScenePosition.x * sceneToInput0X[0] + sceneToInput0X[1];
    ret.y = inputScenePosition.y * sceneToInput0Y[0] + sceneToInput0Y[1];
    
    return ret;
}
```



<span data-ttu-id="08b11-466">Nachdem der obige Konstante Puffer und die angegebene Hilfsmethode definiert wurden, kann der Shader Bild Daten mithilfe folgender Beispiele abgleichen:</span><span class="sxs-lookup"><span data-stu-id="08b11-466">Once the above constant buffer and helper method have been defined, the shader can sample image data using the following:</span></span>


```hlsl
float4 color = InputTexture.SampleLevel(
        InputSampler, 
        ConvertInput0SceneToTexelSpace(
            float2(xIndex + .5, yIndex + .5) + // Add 0.5 to each coordinate to hit the center of the pixel.
            resultRect.xy // Offset sampling location by input image offset.
            ),
        0
        );
```



### <a name="writing-image-data"></a><span data-ttu-id="08b11-467">Schreiben von Bilddaten</span><span class="sxs-lookup"><span data-stu-id="08b11-467">Writing image data</span></span>

<span data-ttu-id="08b11-468">[Direct2D](./direct2d-portal.md) erwartet, dass ein Shader einen Ausgabepuffer für das resultierende Bild definiert.</span><span class="sxs-lookup"><span data-stu-id="08b11-468">[Direct2D](./direct2d-portal.md) expects a shader to define an output buffer for the resulting image to be placed.</span></span> <span data-ttu-id="08b11-469">In Shader Model 4 (DirectX 10) muss es sich um einen eindimensionalen Puffer aufgrund von Funktionseinschränkungen handeln:</span><span class="sxs-lookup"><span data-stu-id="08b11-469">In Shader Model 4 (DirectX 10), this must be a single-dimensional buffer due to feature constraints:</span></span>


```hlsl
// Shader Model 4 does not support RWTexture2D, must use 1D buffer instead.
RWStructuredBuffer<float4> OutputTexture : register(t1);
```



<span data-ttu-id="08b11-470">Die Ausgabe Textur wird zuerst als indizierte Zeile angezeigt, damit das gesamte Bild gespeichert werden kann.</span><span class="sxs-lookup"><span data-stu-id="08b11-470">The output texture is indexed row-first to allow the entire image to be stored.</span></span>


```hlsl
uint imageWidth = resultRect[2] - resultRect[0];
uint imageHeight = resultRect[3] - resultRect[1];
OutputTexture[yIndex * imageWidth + xIndex] = color;
```



<span data-ttu-id="08b11-471">Andererseits können Shader Model 5-Shader (DirectX 11) zweidimensionale Ausgabe Texturen verwenden:</span><span class="sxs-lookup"><span data-stu-id="08b11-471">On the other hand, Shader Model 5 (DirectX 11) shaders can use two-dimensional output textures:</span></span>


```hlsl
RWTexture2D<float4> OutputTexture : register(t1);
```



<span data-ttu-id="08b11-472">Mit Shader Model 5-Shadern bietet [Direct2D](./direct2d-portal.md) einen zusätzlichen Parameter "outpuesffset" im Konstanten Puffer.</span><span class="sxs-lookup"><span data-stu-id="08b11-472">With Shader Model 5 shaders, [Direct2D](./direct2d-portal.md) provides an additional 'outputOffset' parameter in the constant buffer.</span></span> <span data-ttu-id="08b11-473">Die Ausgabe des Shaders sollte durch diesen Betrag ausgelagert werden:</span><span class="sxs-lookup"><span data-stu-id="08b11-473">The shader's output should be offsetted by this amount:</span></span>


```hlsl
OutputTexture[uint2(xIndex, yIndex) + outputOffset.xy] = color;
```



<span data-ttu-id="08b11-474">Unten wird ein vollständiges Pass-Through-Shader-Modell 5-Compute-Shader angezeigt.</span><span class="sxs-lookup"><span data-stu-id="08b11-474">A completed pass-through Shader Model 5 compute shader is shown below.</span></span> <span data-ttu-id="08b11-475">Darin werden die einzelnen Compute-Shader-Threads ein einzelnes Pixel des Eingabe Bilds lesen und schreiben.</span><span class="sxs-lookup"><span data-stu-id="08b11-475">In it, each of the compute shader threads reads and writes a single pixel of the input image.</span></span>


```hlsl
#define NUMTHREADS_X 24
#define NUMTHREADS_Y 24

Texture2D<float4> InputTexture : register(t0);
SamplerState InputSampler : register(s0);

RWTexture2D<float4> OutputTexture : register(t1);

// These are default constants passed by D2D.
cbuffer systemConstants : register(b0)
{
    int4 resultRect; // Represents the region of the output image.
    int2 outputOffset;
    float2 sceneToInput0X;
    float2 sceneToInput0Y;
};

// The image does not necessarily begin at (0,0) on InputTexture. The shader needs
// to use the coefficients provided by Direct2D to map the requested image data to
// where it resides on the texture.
float2 ConvertInput0SceneToTexelSpace(float2 inputScenePosition)
{
    float2 ret;
    ret.x = inputScenePosition.x * sceneToInput0X[0] + sceneToInput0X[1];
    ret.y = inputScenePosition.y * sceneToInput0Y[0] + sceneToInput0Y[1];
    
    return ret;
}

// numthreads(x, y, z)
// This specifies the number of threads in each dispatched threadgroup.
// For Shader Model 5, z <= 64 and x*y*z <= 1024
[numthreads(NUMTHREADS_X, NUMTHREADS_Y, 1)]
void main(
    // dispatchThreadId - Uniquely identifies a given execution of the shader, most commonly used parameter.
    // Definition: (groupId.x * NUM_THREADS_X + groupThreadId.x, groupId.y * NUMTHREADS_Y + groupThreadId.y,
    // groupId.z * NUMTHREADS_Z + groupThreadId.z)
    uint3 dispatchThreadId  : SV_DispatchThreadID,

    // groupThreadId - Identifies an individual thread within a thread group.
    // Range: (0 to NUMTHREADS_X - 1, 0 to NUMTHREADS_Y - 1, 0 to NUMTHREADS_Z - 1)
    uint3 groupThreadId     : SV_GroupThreadID,

    // groupId - Identifies which thread group the individual thread is being executed in.
    // Range defined in DFTVerticalTransform::CalculateThreadgroups.
    uint3 groupId           : SV_GroupID, 

    // One dimensional indentifier of a compute shader thread within a thread group.
    // Range: (0 to NUMTHREADS_X * NUMTHREADS_Y * NUMTHREADS_Z - 1)
    uint  groupIndex        : SV_GroupIndex
    )
{
    uint xIndex = dispatchThreadId.x;
    uint yIndex = dispatchThreadId.y;

    uint imageWidth = resultRect.z - resultRect.x;
    uint imageHeight = resultRect.w - resultRect.y;

    // It is likely that the compute shader will execute beyond the bounds of the input image, since the shader is
    // executed in chunks sized by the threadgroup size defined in ID2D1ComputeTransform::CalculateThreadgroups.
    // For this reason each shader should ensure the current dispatchThreadId is within the bounds of the input
    // image before proceeding.
    if (xIndex >= imageWidth || yIndex >= imageHeight)
    {
        return;
    }

    float4 color = InputTexture.SampleLevel(
        InputSampler, 
        ConvertInput0SceneToTexelSpace(
            float2(xIndex + .5, yIndex + .5) + // Add 0.5 to each coordinate to hit the center of the pixel.
            resultRect.xy // Offset sampling location by image offset.
            ),
        0
        );

    OutputTexture[uint2(xIndex, yIndex) + outputOffset.xy] = color;
```



<span data-ttu-id="08b11-476">Der folgende Code zeigt die äquivalente Shader Model 4-Version des Shaders.</span><span class="sxs-lookup"><span data-stu-id="08b11-476">The code below shows the equivalent Shader Model 4 version of the shader.</span></span> <span data-ttu-id="08b11-477">Beachten Sie, dass der Shader jetzt in einen eindimensionalen Ausgabepuffer gerendert wird.</span><span class="sxs-lookup"><span data-stu-id="08b11-477">Notice that the shader now renders into a single-dimensional output buffer.</span></span>


```hlsl
#define NUMTHREADS_X 24
#define NUMTHREADS_Y 24

Texture2D<float4> InputTexture : register(t0);
SamplerState InputSampler : register(s0);

// Shader Model 4 does not support RWTexture2D, must use one-dimensional buffer instead.
RWStructuredBuffer<float4> OutputTexture : register(t1);

// These are default constants passed by D2D. See PixelShader and VertexShader
// projects for how to pass custom values into a shader.
cbuffer systemConstants : register(b0)
{
    int4 resultRect; // Represents the region of the output image.
    float2 sceneToInput0X;
    float2 sceneToInput0Y;
};

// The image does not necessarily begin at (0,0) on InputTexture. The shader needs
// to use the coefficients provided by Direct2D to map the requested image data to
// where it resides on the texture.
float2 ConvertInput0SceneToTexelSpace(float2 inputScenePosition)
{
    float2 ret;
    ret.x = inputScenePosition.x * sceneToInput0X[0] + sceneToInput0X[1];
    ret.y = inputScenePosition.y * sceneToInput0Y[0] + sceneToInput0Y[1];
    
    return ret;
}

// numthreads(x, y, z)
// This specifies the number of threads in each dispatched threadgroup.
// For Shader Model 4, z == 1 and x*y*z <= 768
[numthreads(NUMTHREADS_X, NUMTHREADS_Y, 1)]
void main(
    // dispatchThreadId - Uniquely identifies a given execution of the shader, most commonly used parameter.
    // Definition: (groupId.x * NUM_THREADS_X + groupThreadId.x, groupId.y * NUMTHREADS_Y + groupThreadId.y, groupId.z * NUMTHREADS_Z + groupThreadId.z)
    uint3 dispatchThreadId  : SV_DispatchThreadID,

    // groupThreadId - Identifies an individual thread within a thread group.
    // Range: (0 to NUMTHREADS_X - 1, 0 to NUMTHREADS_Y - 1, 0 to NUMTHREADS_Z - 1)
    uint3 groupThreadId     : SV_GroupThreadID,

    // groupId - Identifies which thread group the individual thread is being executed in.
    // Range defined in DFTVerticalTransform::CalculateThreadgroups
    uint3 groupId           : SV_GroupID, 

    // One dimensional indentifier of a compute shader thread within a thread group.
    // Range: (0 to NUMTHREADS_X * NUMTHREADS_Y * NUMTHREADS_Z - 1)
    uint  groupIndex        : SV_GroupIndex
    )
{
    uint imageWidth = resultRect[2] - resultRect[0];
    uint imageHeight = resultRect[3] - resultRect[1];

    uint xIndex = dispatchThreadId.x;
    uint yIndex = dispatchThreadId.y;

    // It is likely that the compute shader will execute beyond the bounds of the input image, since the shader is executed in chunks sized by
    // the threadgroup size defined in ID2D1ComputeTransform::CalculateThreadgroups. For this reason each shader should ensure the current
    // dispatchThreadId is within the bounds of the input image before proceeding.
    if (xIndex >= imageWidth || yIndex >= imageHeight)
    {
        return;
    }

    float4 color = InputTexture.SampleLevel(
        InputSampler, 
        ConvertInput0SceneToTexelSpace(
            float2(xIndex + .5, yIndex + .5) + // Add 0.5 to each coordinate to hit the center of the pixel.
            resultRect.xy // Offset sampling location by image offset.
            ),
        0
        );

    OutputTexture[yIndex * imageWidth + xIndex] = color;
}
```



## <a name="related-topics"></a><span data-ttu-id="08b11-478">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="08b11-478">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="08b11-479">D2DCustomEffects SDK-Beispiel</span><span class="sxs-lookup"><span data-stu-id="08b11-479">D2DCustomEffects SDK sample</span></span>](https://github.com/Microsoft/Windows-universal-samples/tree/master/Samples/D2DCustomEffects)
</dt> </dl>

 

 