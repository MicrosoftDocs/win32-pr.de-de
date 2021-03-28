---
title: Benutzer Clip Flächen auf Featureebene 9 Hardware
description: Ab Windows 8 unterstützt Microsoft High Level Shader Language (HLSL) eine Syntax, die Sie mit der Microsoft Direct3D 11-API zum Angeben von Benutzer Clip Flächen auf Featureebene 9 \_ x und höher verwenden können.
ms.assetid: C51FB0E5-94C3-4E7F-AC33-E5F0F26EDC11
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 968831ca39f2501a44b00f202fd8dfda1f92d1e7
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "104315572"
---
# <a name="user-clip-planes-on-feature-level-9-hardware"></a><span data-ttu-id="10a03-103">Benutzer Clip Flächen auf Featureebene 9 Hardware</span><span class="sxs-lookup"><span data-stu-id="10a03-103">User clip planes on feature level 9 hardware</span></span>

<span data-ttu-id="10a03-104">Ab Windows 8 unterstützt Microsoft High Level Shader Language (HLSL) eine Syntax, die Sie mit der Microsoft Direct3D 11-API zum Angeben von Benutzer Clip Flächen auf [Featureebene](/windows/desktop/direct3d11/overviews-direct3d-11-devices-downlevel-intro) 9 \_ x und höher verwenden können.</span><span class="sxs-lookup"><span data-stu-id="10a03-104">Starting with Windows 8, Microsoft High Level Shader Language (HLSL) supports a syntax that you can use with the Microsoft Direct3D 11 API to specify user clip planes on [feature level](/windows/desktop/direct3d11/overviews-direct3d-11-devices-downlevel-intro) 9\_x and higher.</span></span> <span data-ttu-id="10a03-105">Sie können diese Clip-Plane-Syntax verwenden, um einen Shader zu schreiben, und dann dieses Shader-Objekt mit der Direct3D 11-API verwenden, um Sie auf allen Direct3D-Funktionsebenen auszuführen.</span><span class="sxs-lookup"><span data-stu-id="10a03-105">You can use this clip-planes syntax to write a shader, and then use that shader object with the Direct3D 11 API to run on all Direct3D feature levels.</span></span>

-   [<span data-ttu-id="10a03-106">Hintergrund</span><span class="sxs-lookup"><span data-stu-id="10a03-106">Background</span></span>](#background-reading)
-   [<span data-ttu-id="10a03-107">Syntax</span><span class="sxs-lookup"><span data-stu-id="10a03-107">Syntax</span></span>](#syntax)
-   [<span data-ttu-id="10a03-108">Erstellen von Clip-Flächen im Clip Bereich auf Featureebene 9 und höher</span><span class="sxs-lookup"><span data-stu-id="10a03-108">Creating clip planes in clip space on feature level 9 and higher</span></span>](#creating-clip-planes-in-clip-space-on-feature-level-9-and-higher)
    -   [<span data-ttu-id="10a03-109">Hintergrund Lesevorgänge</span><span class="sxs-lookup"><span data-stu-id="10a03-109">Background reading</span></span>](#background-reading)
    -   [<span data-ttu-id="10a03-110">10 Level9-Funktionsebenen</span><span class="sxs-lookup"><span data-stu-id="10a03-110">10Level9 feature levels</span></span>](#10level9-feature-levels)
    -   [<span data-ttu-id="10a03-111">"Clip Plane Math"</span><span class="sxs-lookup"><span data-stu-id="10a03-111">Clip plane math</span></span>](#clip-plane-math)
    -   [<span data-ttu-id="10a03-112">Clipping im Anzeigebereich</span><span class="sxs-lookup"><span data-stu-id="10a03-112">Clipping in view space</span></span>](#clipping-in-view-space)
    -   [<span data-ttu-id="10a03-113">Projektions Matrix</span><span class="sxs-lookup"><span data-stu-id="10a03-113">Projection matrix</span></span>](#projection-matrix)
    -   [<span data-ttu-id="10a03-114">Clip Space Clip-Ebene</span><span class="sxs-lookup"><span data-stu-id="10a03-114">Clip space clip plane</span></span>](#clip-space-clip-plane)
-   [<span data-ttu-id="10a03-115">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="10a03-115">Related topics</span></span>](#related-topics)

## <a name="background"></a><span data-ttu-id="10a03-116">Hintergrund</span><span class="sxs-lookup"><span data-stu-id="10a03-116">Background</span></span>

<span data-ttu-id="10a03-117">Sie können in der Microsoft Direct3D 9-API über [**IDirect3DDevice9:: setclipplane**](/windows/desktop/api/d3d9/nf-d3d9-idirect3ddevice9-setclipplane) -und [**IDirect3DDevice9:: getclipplane**](/windows/desktop/api/d3d9/nf-d3d9-idirect3ddevice9-getclipplane) -Methoden auf Benutzer Clip Flächen zugreifen.</span><span class="sxs-lookup"><span data-stu-id="10a03-117">You can access user clip planes in the Microsoft Direct3D 9 API via [**IDirect3DDevice9::SetClipPlane**](/windows/desktop/api/d3d9/nf-d3d9-idirect3ddevice9-setclipplane) and [**IDirect3DDevice9::GetClipPlane**](/windows/desktop/api/d3d9/nf-d3d9-idirect3ddevice9-getclipplane) methods.</span></span> <span data-ttu-id="10a03-118">In Microsoft Direct3D 10 und höher können Sie auf Benutzer Clip Flächen über die Semantik " [SV \_ clipdistance](dx-graphics-hlsl-semantics.md) " zugreifen.</span><span class="sxs-lookup"><span data-stu-id="10a03-118">In Microsoft Direct3D 10 and later, you can access user clip planes through the [SV\_ClipDistance](dx-graphics-hlsl-semantics.md) semantic.</span></span> <span data-ttu-id="10a03-119">Doch vor Windows 8 war "SV \_ clipdistance" in den [](/windows/desktop/direct3d11/overviews-direct3d-11-devices-downlevel-intro) \_ APIs Direct3D 10 oder Direct3D 11 nicht für die Funktionsebene 9 x-Hardware verfügbar.</span><span class="sxs-lookup"><span data-stu-id="10a03-119">But before Windows 8, SV\_ClipDistance was not available for [feature level](/windows/desktop/direct3d11/overviews-direct3d-11-devices-downlevel-intro) 9\_x hardware in the Direct3D 10 or Direct3D 11 APIs.</span></span> <span data-ttu-id="10a03-120">Vor Windows 8 war die einzige Möglichkeit für den Zugriff auf Benutzer Clip-und Featureebene mit 9 \_ x-Hardware die API Direct3D 9.</span><span class="sxs-lookup"><span data-stu-id="10a03-120">So, before Windows 8, the only way to access user clip planes with feature level 9\_x hardware was through the Direct3D 9 API.</span></span> <span data-ttu-id="10a03-121">Direct3D Windows Store-Apps können die Direct3D 9-API nicht verwenden.</span><span class="sxs-lookup"><span data-stu-id="10a03-121">Direct3D Windows Store apps can't use the Direct3D 9 API.</span></span> <span data-ttu-id="10a03-122">Hier wird die Syntax beschrieben, die Sie verwenden können, um über die Direct3D 11-API auf Featureebene 9 x und höher auf Benutzer Clip Flächen zuzugreifen \_ .</span><span class="sxs-lookup"><span data-stu-id="10a03-122">Here we describe the syntax that you can use to access user clip planes through the Direct3D 11 API on feature level 9\_x and higher.</span></span>

<span data-ttu-id="10a03-123">-Apps verwenden Clip Flächen, um eine Reihe von nicht sichtbaren Ebenen innerhalb der 3D-Welt zu definieren, die alle gezeichneten primitiven Ausschneiden (lösen).</span><span class="sxs-lookup"><span data-stu-id="10a03-123">Apps use clip planes to define a set of invisible planes within the 3D world that clip (throw away) all drawn primitives.</span></span> <span data-ttu-id="10a03-124">Windows zeichnet kein Pixel, das sich auf der negativen Seite von Clip Flächen befindet.</span><span class="sxs-lookup"><span data-stu-id="10a03-124">Windows won't draw any pixel that is on the negative side of any clip planes.</span></span> <span data-ttu-id="10a03-125">Apps können dann mithilfe von Clip-Ebenen planare Reflektionen Rendering.</span><span class="sxs-lookup"><span data-stu-id="10a03-125">Apps can then use clip planes to render planar reflections.</span></span>

## <a name="syntax"></a><span data-ttu-id="10a03-126">Syntax</span><span class="sxs-lookup"><span data-stu-id="10a03-126">Syntax</span></span>

<span data-ttu-id="10a03-127">Verwenden Sie diese Syntax, um Clip-Ebenen als Funktions Attribute in einer [Funktionsdeklaration](dx-graphics-hlsl-function-syntax.md)zu deklarieren.</span><span class="sxs-lookup"><span data-stu-id="10a03-127">Use this syntax to declare clip planes as function attributes in a [function declaration](dx-graphics-hlsl-function-syntax.md).</span></span> <span data-ttu-id="10a03-128">Hier verwenden wir beispielsweise die Syntax für ein Vertex-Shader-Fragment:</span><span class="sxs-lookup"><span data-stu-id="10a03-128">For example, here we use the syntax on a vertex shader fragment:</span></span>

``` syntax
cbuffer ClipPlaneConstantBuffer 
{
       float4 clipPlane1;
       float4 clipPlane2;
};

[clipplanes(clipPlane1,clipPlane2)]
VertexShaderOutput main(VertexShaderInput input)
{
       // the rest of the vertex shader doesn't refer to the clip plane
 
       …
 
       return output;
}
```

<span data-ttu-id="10a03-129">Dieses Beispiel für ein Scheitelpunkt-Shader-Fragment deutet auf zwei Clip-Flächen hin.</span><span class="sxs-lookup"><span data-stu-id="10a03-129">This example for a vertex shader fragment denotes two clip planes.</span></span> <span data-ttu-id="10a03-130">Es zeigt, dass Sie das neue **clipplane** -Attribut in eckigen Klammern direkt vor dem Rückgabewert des Vertexshaders platzieren müssen.</span><span class="sxs-lookup"><span data-stu-id="10a03-130">It shows that you need to place the new **clipplanes** attribute within square brackets immediately before the return value of the vertex shader.</span></span> <span data-ttu-id="10a03-131">Innerhalb von Klammern nach dem **clipplane** -Attribut geben Sie eine Liste von bis zu 6 **float4** Konstanten an, die die ebenenkoeffizienten für die einzelnen aktiven Clip Ebenen definieren.</span><span class="sxs-lookup"><span data-stu-id="10a03-131">Within parentheses after the **clipplanes** attribute, you provide a list of up to 6 **float4** constants that define the plane coefficients for each active clip plane.</span></span> <span data-ttu-id="10a03-132">Das Beispiel zeigt auch, dass Sie die Koeffizienten der einzelnen Ebenen in einem konstanten Puffer erstellen müssen.</span><span class="sxs-lookup"><span data-stu-id="10a03-132">The example also shows that you need to make the coefficients of each plane reside in a constant buffer.</span></span>

> [!Note]  
> <span data-ttu-id="10a03-133">Es ist keine Syntax verfügbar, um eine Clip-Ebene dynamisch zu deaktivieren.</span><span class="sxs-lookup"><span data-stu-id="10a03-133">There is no syntax available to disable a clip plane dynamically.</span></span> <span data-ttu-id="10a03-134">Sie müssen entweder einen anderweitig identischen Shader ohne **clipplane** -Attribut neu kompilieren, oder die APP kann die Koeffizienten im Konstanten Puffer auf 0 (null) festlegen, sodass sich die Ebene nicht mehr auf Geometrie auswirkt.</span><span class="sxs-lookup"><span data-stu-id="10a03-134">You must either recompile an otherwise identical shader with no **clipplanes** attribute, or your app can set the coefficients in your constant buffer to zero so that the plane no longer affects any geometry.</span></span>

 

<span data-ttu-id="10a03-135">Diese Syntax ist für jedes 4,0-oder spätere Scheitelpunkt-Shader-Ziel verfügbar, das vs \_ 4 \_ 0 \_ Level \_ 9 \_ 1 und vs \_ 4 \_ 0 \_ Level \_ 9 \_ 3 umfasst.</span><span class="sxs-lookup"><span data-stu-id="10a03-135">This syntax is available for any 4.0 or later vertex shader target, which includes vs\_4\_0\_level\_9\_1 and vs\_4\_0\_level\_9\_3.</span></span>

## <a name="creating-clip-planes-in-clip-space-on-feature-level-9-and-higher"></a><span data-ttu-id="10a03-136">Erstellen von Clip-Flächen im Clip Bereich auf Featureebene 9 und höher</span><span class="sxs-lookup"><span data-stu-id="10a03-136">Creating clip planes in clip space on feature level 9 and higher</span></span>

<span data-ttu-id="10a03-137">Hier wird gezeigt, wie Sie Clip-und Ausschneide Flächen auf [Featureebene](/windows/desktop/direct3d11/overviews-direct3d-11-devices-downlevel-intro) 9 \_ x und höher erstellen.</span><span class="sxs-lookup"><span data-stu-id="10a03-137">Here we show how to create clip planes in clip space on [feature level](/windows/desktop/direct3d11/overviews-direct3d-11-devices-downlevel-intro) 9\_x and higher.</span></span>

### <a name="background-reading"></a><span data-ttu-id="10a03-138">Hintergrund Lesevorgänge</span><span class="sxs-lookup"><span data-stu-id="10a03-138">Background reading</span></span>

<span data-ttu-id="10a03-139">"Einführung in 3D-Spieleprogrammierung mit DirectX 10" von Frank D. Luna erläutert den mathematischen Hintergrund der Grafik (Kapitel 1, 2 und 3), die Sie benötigen, und die verschiedenen Leerzeichen und Leerzeichen Transformationen, die im Vertex-Shader (Abschnitte 5,6 und 5,8) vorkommen.</span><span class="sxs-lookup"><span data-stu-id="10a03-139">"Introduction to 3D Game Programming with DirectX 10" by Frank D. Luna explains the graphics math background (chapters 1, 2 and 3) you need, and the various spaces and space transformations that occur in the vertex shader (sections 5.6 and 5.8).</span></span>

### <a name="10level9-feature-levels"></a><span data-ttu-id="10a03-140">10 Level9-Funktionsebenen</span><span class="sxs-lookup"><span data-stu-id="10a03-140">10Level9 feature levels</span></span>

<span data-ttu-id="10a03-141">In Direct3D 10 und höher können Sie alle Bereiche, die sinnvoll sind, im Raum der Welt und im Bereich von Sicht Vorschauen.</span><span class="sxs-lookup"><span data-stu-id="10a03-141">In Direct3D 10 and later, you can clip in any space that makes sense, often in world space or view space.</span></span> <span data-ttu-id="10a03-142">In Direct3D 9 wird jedoch Clip Space verwendet, bei dem es sich um einen vorperspektiven-Projektions Bereich handelt.</span><span class="sxs-lookup"><span data-stu-id="10a03-142">But Direct3D 9 uses clip space, which is pre perspective divide projection space.</span></span> <span data-ttu-id="10a03-143">Vektoren befinden sich im Ausschneide Bereich, wenn der Vertexshader Sie an Stufen übergibt, die in der [Grafik Pipeline](/windows/desktop/direct3d11/overviews-direct3d-11-graphics-pipeline)befolgt werden.</span><span class="sxs-lookup"><span data-stu-id="10a03-143">Vectors are in clip space when the vertex shader passes them to stages that follow in the [graphics pipeline](/windows/desktop/direct3d11/overviews-direct3d-11-graphics-pipeline).</span></span>

<span data-ttu-id="10a03-144">Wenn Sie eine Windows Store-App schreiben, müssen Sie die featureebenen 10level9 ([Funktionsebene](/windows/desktop/direct3d11/overviews-direct3d-11-devices-downlevel-intro) 9 \_ x) verwenden, damit die APP auf Featureebene mit 9 \_ x und höherer Hardware ausgeführt werden kann.</span><span class="sxs-lookup"><span data-stu-id="10a03-144">When you write a Windows Store app, you must use 10Level9 feature levels ([feature level](/windows/desktop/direct3d11/overviews-direct3d-11-devices-downlevel-intro) 9\_x) so the app can run on feature level 9\_x and higher hardware.</span></span> <span data-ttu-id="10a03-145">Da Ihre APP die Featureebene 9 \_ x und höher unterstützt, müssen Sie auch die gängige Funktion zum Anwenden von Clip-Flächen im Clip Bereich verwenden.</span><span class="sxs-lookup"><span data-stu-id="10a03-145">Because your app supports feature level 9\_x and higher, you must also use the common capability of applying clip planes in clip space.</span></span>

<span data-ttu-id="10a03-146">Wenn Sie einen Vertex-Shader mit vs \_ 4 \_ 0 \_ Level \_ 9 \_ 1 oder höher kompilieren, kann der Vertexshader das **clipplane** -Attribut verwenden.</span><span class="sxs-lookup"><span data-stu-id="10a03-146">When you compile a vertex shader with vs\_4\_0\_level\_9\_1 or later, that vertex shader can use the **clipplanes** attribute.</span></span> <span data-ttu-id="10a03-147">Ein Direct3D 10-Objekt oder ein späteres Objekt verfügt über ein Punktprodukt des ausgegebenen Vertex, das jede der im-Attribut angegebenen globalen **float4** -Konstanten enthält.</span><span class="sxs-lookup"><span data-stu-id="10a03-147">A Direct3D 10 or later object has a dot product of the emitted vertex that contains each of the **float4** global constants specified in the attribute.</span></span> <span data-ttu-id="10a03-148">Das Direct3D 9-Objekt verfügt über genügend Metadaten, damit die 10level9-Laufzeit die entsprechenden Aufrufe an [**IDirect3DDevice9:: setclipplane**](/windows/desktop/api/d3d9/nf-d3d9-idirect3ddevice9-setclipplane)ausgibt.</span><span class="sxs-lookup"><span data-stu-id="10a03-148">The Direct3D 9 object has enough meta data to cause the 10Level9 runtime to issue the appropriate calls to [**IDirect3DDevice9::SetClipPlane**](/windows/desktop/api/d3d9/nf-d3d9-idirect3ddevice9-setclipplane).</span></span>

### <a name="clip-plane-math"></a><span data-ttu-id="10a03-149">"Clip Plane Math"</span><span class="sxs-lookup"><span data-stu-id="10a03-149">Clip plane math</span></span>

<span data-ttu-id="10a03-150">Eine Clip Ebene wird durch einen Vektor mit vier Komponenten definiert.</span><span class="sxs-lookup"><span data-stu-id="10a03-150">A clip plane is defined by a vector with 4 components.</span></span> <span data-ttu-id="10a03-151">Die ersten drei Komponenten definieren einen x-, y-und z-Vektor, der vom Ursprung im Bereich ausgeht, den wir ausschneiden möchten.</span><span class="sxs-lookup"><span data-stu-id="10a03-151">The first three components define an x, y, z vector that emanates from the origin in the space we want to clip.</span></span> <span data-ttu-id="10a03-152">Dieser Vektor impliziert eine Ebene, die senkrecht zum Vektor und durch den Ursprung verläuft.</span><span class="sxs-lookup"><span data-stu-id="10a03-152">This vector implies a plane, perpendicular to the vector and running through the origin.</span></span> <span data-ttu-id="10a03-153">Windows behält alle Pixel auf der Vektor Seite der Ebene bei und schneidet alle Pixel hinter der Ebene ab.</span><span class="sxs-lookup"><span data-stu-id="10a03-153">Windows keeps all pixels on the vector side of the plane and clips all pixels behind the plane.</span></span> <span data-ttu-id="10a03-154">Die Komponente "weiter w" überträgt die Ebene zurück und bewirkt, dass Windows einen kürzeren Clip bewirkt (ein negativer Wert bewirkt, dass Fenster mehr) entlang der Vektor Linie angezeigt werden.</span><span class="sxs-lookup"><span data-stu-id="10a03-154">The forth w component pushes the plane back and causes Windows to clip less (a negative w causes Windows to clip more) along the vector line.</span></span> <span data-ttu-id="10a03-155">Wenn die x-, y-und z-Komponenten einen (normalisierten) Einheits Vektor bilden, überträgt w die Einheiten der Ebene w zurück.</span><span class="sxs-lookup"><span data-stu-id="10a03-155">If the x, y, z components compose a unit (normalized) vector, w pushes the plane w units back.</span></span>

<span data-ttu-id="10a03-156">Die von der GPU (Graphics Processing Unit) durchgeführte Mathematik ist ein einfaches Punktprodukt zwischen dem Scheitelpunkt Vektor (x, y, z, 1) und dem Vektor der Clippingebene.</span><span class="sxs-lookup"><span data-stu-id="10a03-156">The math that the graphics processing unit (GPU) performs to determine clipping is a simple dot product between the vertex vector (x, y, z, 1) and the clipping plane vector.</span></span> <span data-ttu-id="10a03-157">Dieser mathematische Vorgang erstellt eine Projektions Länge auf dem Clip Ebenen-Vektor.</span><span class="sxs-lookup"><span data-stu-id="10a03-157">This math operation creates a projection length on the clip plane vector.</span></span> <span data-ttu-id="10a03-158">Ein negatives Punktprodukt zeigt den Scheitelpunkt auf der ausgeschnittenen Seite der Ebene an.</span><span class="sxs-lookup"><span data-stu-id="10a03-158">A negative dot product shows the vertex to be on the clipped side of the plane.</span></span>

### <a name="clipping-in-view-space"></a><span data-ttu-id="10a03-159">Clipping im Anzeigebereich</span><span class="sxs-lookup"><span data-stu-id="10a03-159">Clipping in view space</span></span>

<span data-ttu-id="10a03-160">Hier ist unser Scheitelpunkt im Ansichts Bereich:</span><span class="sxs-lookup"><span data-stu-id="10a03-160">Here is our vertex in view space:</span></span>

![Scheitelpunkt im Anzeigebereich](images/vertex-clip.png)

<span data-ttu-id="10a03-162">Hier sehen Sie unsere Ausschneide Ebene im Anzeigebereich:</span><span class="sxs-lookup"><span data-stu-id="10a03-162">Here is our clip plane in view space:</span></span>

![Ausschneide Ebene im Anzeigebereich](images/clip-plane-view.png)

<span data-ttu-id="10a03-164">Hier ist das Punktprodukt von Vertex und clisebene im Ansichts Raum:</span><span class="sxs-lookup"><span data-stu-id="10a03-164">Here is the dot product of vertex and clip plane in view space:</span></span>

<span data-ttu-id="10a03-165">Clipdistance = **v** = **C**  =  *v* ₓ *c* ₓ +*v*<sub>y</sub>*c*<sub>y</sub>  +  *v*<sub>z</sub>*c*<sub>z</sub>  +  *c*<sub>w</sub></span><span class="sxs-lookup"><span data-stu-id="10a03-165">ClipDistance = **v** · **C** = *v* ₓ *C* ₓ +*v*<sub>y</sub>*C*<sub>y</sub> + *v*<sub>z</sub>*C*<sub>z</sub> + *C*<sub>w</sub></span></span>

<span data-ttu-id="10a03-166">Diese mathematische Operation funktioniert für ein Direct3D 10-Objekt oder ein späteres Objekt, funktioniert aber nicht für ein Direct3D 9-Objekt.</span><span class="sxs-lookup"><span data-stu-id="10a03-166">This math operation works for a Direct3D 10 or later object but won't work for a Direct3D 9 object.</span></span> <span data-ttu-id="10a03-167">Für Direct3D 9 müssen wir zuerst unsere Projektions Transformation in Clip Space durchlaufen.</span><span class="sxs-lookup"><span data-stu-id="10a03-167">For Direct3D 9, we must first get through our projection transform into clip space.</span></span>

### <a name="projection-matrix"></a><span data-ttu-id="10a03-168">Projektions Matrix</span><span class="sxs-lookup"><span data-stu-id="10a03-168">Projection matrix</span></span>

<span data-ttu-id="10a03-169">Eine Projektions Matrix wandelt einen Scheitelpunkt aus dem Ansichts Raum um (wobei der Ursprung das Auge des Viewers ist, + x nach rechts, + y ist hoch und + z direkt vorwärts) in den Clip Bereich.</span><span class="sxs-lookup"><span data-stu-id="10a03-169">A projection matrix transforms a vertex from view space (where the origin is the viewer's eye, +x is to the right, +y is up, and +z is straight ahead) into clip space.</span></span> <span data-ttu-id="10a03-170">Die Projektions Matrix gibt den Scheitelpunkt für das Hardware Clipping und die [rasterisierungsphase](/windows/desktop/direct3d11/d3d10-graphics-programming-guide-rasterizer-stage)wieder.</span><span class="sxs-lookup"><span data-stu-id="10a03-170">The projection matrix readies the vertex for hardware clipping and the [rasterization stage](/windows/desktop/direct3d11/d3d10-graphics-programming-guide-rasterizer-stage).</span></span> <span data-ttu-id="10a03-171">Dies ist eine standardmäßige Perspektiven Matrix (andere Projektionen erfordern unterschiedliche mathematische):</span><span class="sxs-lookup"><span data-stu-id="10a03-171">Here is a standard perspective matrix (other projections require different math):</span></span>

<dl> <span data-ttu-id="10a03-172">*r*   -Verhältnis der Fensterbreite/-Höhe</span><span class="sxs-lookup"><span data-stu-id="10a03-172">*r*  ratio of window width/height</span></span>  
<span data-ttu-id="10a03-173">   Anzeige Winkel von i</span><span class="sxs-lookup"><span data-stu-id="10a03-173">*α*  viewing angle</span></span>  
<span data-ttu-id="10a03-174">*f* -   Entfernung vom Viewer zur äußersten Ebene</span><span class="sxs-lookup"><span data-stu-id="10a03-174">*f*  distance from the viewer to the far plane</span></span>  
<span data-ttu-id="10a03-175">*n*   Entfernung vom Viewer zur near-Ebene</span><span class="sxs-lookup"><span data-stu-id="10a03-175">*n*  distance from the viewer to the near plane</span></span>
</dl><span data-ttu-id="10a03-176">![Projektions Matrix](images/projection-matrix.png)</span><span class="sxs-lookup"><span data-stu-id="10a03-176">![projection matrix](images/projection-matrix.png)</span></span>

<span data-ttu-id="10a03-177">Die nächste Matrix ist eine vereinfachte Version der vorherigen Matrix.</span><span class="sxs-lookup"><span data-stu-id="10a03-177">The next matrix is a simplified version of the previous matrix.</span></span> <span data-ttu-id="10a03-178">Die Matrix wird vereinfacht, sodass Sie später im Matrix Multiplikations Vorgang verwendet werden kann.</span><span class="sxs-lookup"><span data-stu-id="10a03-178">We show the matrix simplified so we can use it later in the matrix multiply operation.</span></span>

![vereinfachte Projektions Matrix](images/projection-matrix2.png)

<span data-ttu-id="10a03-180">Nun transformieren wir den Scheitelpunkt Scheitelpunkt in einen Clip Bereich mit einer Matrix Multiplikation:</span><span class="sxs-lookup"><span data-stu-id="10a03-180">Now we transform our view space vertex into clip space with a matrix multiply:</span></span>

![Matrix multiplizieren](images/matrix-multiply.png)

<span data-ttu-id="10a03-182">Bei der Matrix Multiplikation werden unsere x-und y-Komponenten nur geringfügig angepasst, aber unsere z-und w-Komponenten sind recht verändert.</span><span class="sxs-lookup"><span data-stu-id="10a03-182">In our matrix multiply operation, our x and y components are only slightly adjusted, but our z and w components are quite mangled.</span></span> <span data-ttu-id="10a03-183">Unsere clisebene gibt uns nicht mehr, was wir wollen.</span><span class="sxs-lookup"><span data-stu-id="10a03-183">Our clip plane won't give us what we want any more.</span></span>

### <a name="clip-space-clip-plane"></a><span data-ttu-id="10a03-184">Clip Space Clip-Ebene</span><span class="sxs-lookup"><span data-stu-id="10a03-184">Clip space clip plane</span></span>

<span data-ttu-id="10a03-185">Hier möchten wir eine Clip Space-Clip-Ebene erstellen, deren Punktprodukt mit dem Clip Space-Scheitelpunkt denselben Wert wie v = hat. **C** im Abschnitt [Clipping im Bereich Anzeige](#clipping-in-view-space) Bereich.</span><span class="sxs-lookup"><span data-stu-id="10a03-185">Here we want to create a clip space clip plane whose dot product with our clip space vertex gives us the same value as **v · C** in the [Clipping in view space](#clipping-in-view-space) section.</span></span>

![clipbene](images/clip-space-clip-plane.png)

<span data-ttu-id="10a03-187">**v** **C**  =  **v P** **C**<sub>P</sub></span><span class="sxs-lookup"><span data-stu-id="10a03-187">**v** · **C** = **v P** · **C**<sub>P</sub></span></span>

<span data-ttu-id="10a03-188">*v* ₓ *c* ₓ +*v*<sub>y</sub>*c*<sub>y</sub>  +  *v*<sub>z</sub>*c*<sub>z</sub>  +  *c*<sub>w</sub>  =  *v* ₓ *p* ₓ *C*<sub>p ₓ</sub>  + *v*<sub>y</sub>*p*<sub>y</sub>*C*<sub>p <sub>y</sub></sub>  +  *v*<sub>z</sub>*A*<sub>y</sub>*c*<sub>p <sub>z</sub></sub>  +  *BC*<sub>p <sub>z</sub></sub>  +  *v*<sub>z</sub>*c*<sub>p <sub>w</sub></sub></span><span class="sxs-lookup"><span data-stu-id="10a03-188">*v* ₓ *C* ₓ +*v*<sub>y</sub>*C*<sub>y</sub> + *v*<sub>z</sub>*C*<sub>z</sub> + *C*<sub>w</sub> = *v* ₓ *P* ₓ *C*<sub>Pₓ</sub> +*v*<sub>y</sub>*P*<sub>y</sub>*C*<sub>P <sub>y</sub></sub> + *v*<sub>z</sub>*A*<sub>y</sub>*C*<sub>P <sub>z</sub></sub> + *BC*<sub>P <sub>z</sub></sub> + *v*<sub>z</sub>*C*<sub>P<sub>w</sub></sub></span></span>

<span data-ttu-id="10a03-189">Nun können wir den vorangehenden mathematischen Vorgang von der Scheitelpunkt Komponente in vier separate Gleichungen aufteilen:</span><span class="sxs-lookup"><span data-stu-id="10a03-189">Now we can break the preceding math operation up by vertex component into four separate equations:</span></span>

![x-Scheitelpunkt Komponente des Clip-Plane-Produkts](images/clip-space-clip-plane-equ1.png)

![y-Scheitelpunkt Komponente des Clip-Plane-Produkts](images/clip-space-clip-plane-equ2.png)

![w-Scheitelpunkt Komponente des Clip-Plane-Produkts](images/clip-space-clip-plane-equ3.png)

![z-Scheitelpunkt Komponente des Clip-Plane-Produkts](images/clip-space-clip-plane-equ4.png)

<span data-ttu-id="10a03-194">Unsere Ausschneide Ebene des Ansichts Raums und unsere Projektions Matrix werden abgeleitet</span><span class="sxs-lookup"><span data-stu-id="10a03-194">Our view space clip plane and our projection matrix derive and give us our clip space clip plane.</span></span>

![Clip Space Clip-Ebene](images/clip-space-clip-plane-matrix.png)

## <a name="related-topics"></a><span data-ttu-id="10a03-196">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="10a03-196">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="10a03-197">Programmieranleitung für HLSL</span><span class="sxs-lookup"><span data-stu-id="10a03-197">Programming Guide for HLSL</span></span>](dx-graphics-hlsl-pguide.md)
</dt> <dt>

[<span data-ttu-id="10a03-198">Syntax der Funktionsdeklaration</span><span class="sxs-lookup"><span data-stu-id="10a03-198">Function Declaration Syntax</span></span>](dx-graphics-hlsl-function-syntax.md)
</dt> </dl>

 

 