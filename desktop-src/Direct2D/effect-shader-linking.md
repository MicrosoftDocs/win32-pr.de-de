---
title: Effektshader-Verknüpfung
description: Direct2D verwendet eine Optimierung namens "Effect Shader Linking", die das Rendering mehrerer Effekte Diagramm Rendering in einem einzigen Durchlauf kombiniert.
ms.assetid: 431A5B39-6C84-442D-AC66-0F341E10DF2C
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d0a17691346649b2ddcde7ca4f3e343be6a35a90
ms.sourcegitcommit: b7a1da2711221fa99072079bf52399cbdfc6bd9d
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/05/2021
ms.locfileid: "104351749"
---
# <a name="effect-shader-linking"></a><span data-ttu-id="d8143-103">Effektshader-Verknüpfung</span><span class="sxs-lookup"><span data-stu-id="d8143-103">Effect Shader Linking</span></span>

<span data-ttu-id="d8143-104">Direct2D verwendet eine Optimierung namens "Effect Shader Linking", die das Rendering mehrerer Effekte Diagramm Rendering in einem einzigen Durchlauf kombiniert.</span><span class="sxs-lookup"><span data-stu-id="d8143-104">Direct2D uses an optimization called effect shader linking which combines multiple effect graph rendering passes into a single pass.</span></span>

-   [<span data-ttu-id="d8143-105">Übersicht über die Auswirkung der Shader-Verknüpfung</span><span class="sxs-lookup"><span data-stu-id="d8143-105">Overview of Effect Shader Linking</span></span>](#overview-of-effect-shader-linking)
-   [<span data-ttu-id="d8143-106">Verwenden von Effekt-Shader-Verknüpfung</span><span class="sxs-lookup"><span data-stu-id="d8143-106">Using Effect Shader Linking</span></span>](#using-effect-shader-linking)
-   [<span data-ttu-id="d8143-107">Erstellen eines shaderverknüpfungs-kompatiblen benutzerdefinierten Effekts</span><span class="sxs-lookup"><span data-stu-id="d8143-107">Authoring a shader linking-compatible custom effect</span></span>](#authoring-a-shader-linking-compatible-custom-effect)
-   [<span data-ttu-id="d8143-108">Beispiel-Shader mit Verknüpfungs kompatiblem Effekten</span><span class="sxs-lookup"><span data-stu-id="d8143-108">Example linking-compatible effect shader</span></span>](#example-linking-compatible-effect-shader)
-   [<span data-ttu-id="d8143-109">Kompilieren eines verknüpften kompatiblen Shaders</span><span class="sxs-lookup"><span data-stu-id="d8143-109">Compiling a linking compatible-shader</span></span>](#compiling-a-linking-compatible-shader)
    -   [<span data-ttu-id="d8143-110">Schritt 1: Kompilieren der Exportfunktion</span><span class="sxs-lookup"><span data-stu-id="d8143-110">Step 1: Compile the export function</span></span>](#step-1-compile-the-export-function)
    -   [<span data-ttu-id="d8143-111">Schritt 2: Kompilieren Sie den vollständigen Shader, und Betten Sie die Exportfunktion ein.</span><span class="sxs-lookup"><span data-stu-id="d8143-111">Step 2: Compile the full shader and embed the export function</span></span>](#step-2-compile-the-full-shader-and-embed-the-export-function)
-   [<span data-ttu-id="d8143-112">Funktions Spezifikationen exportieren</span><span class="sxs-lookup"><span data-stu-id="d8143-112">Export function specifications</span></span>](#export-function-specifications)
-   [<span data-ttu-id="d8143-113">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="d8143-113">Related topics</span></span>](#related-topics)

## <a name="overview-of-effect-shader-linking"></a><span data-ttu-id="d8143-114">Übersicht über die Auswirkung der Shader-Verknüpfung</span><span class="sxs-lookup"><span data-stu-id="d8143-114">Overview of Effect Shader Linking</span></span>

<span data-ttu-id="d8143-115">Die Effekt-Shader-Verknüpfungs Optimierungen bauen auf der HLSL-Shader-Verknüpfung auf, einem Direct3D 11,2-Feature, das das Generieren von Pixel-und Vertex-Shadern zur Laufzeit ermöglicht, indem vorkompilierte Shaderfunktionen verknüpft werden.</span><span class="sxs-lookup"><span data-stu-id="d8143-115">The effect shader linking optimizations builds on top of HLSL shader linking, a Direct3D 11.2 feature that allows pixel and vertex shaders to be generated at runtime by linking pre-compiled shader functions.</span></span> <span data-ttu-id="d8143-116">Die folgenden Abbildungen veranschaulichen das Konzept des Effekts von Shader-Verknüpfungen in einem Effekt Diagramm.</span><span class="sxs-lookup"><span data-stu-id="d8143-116">The following figures illustrate the concept of effect shader linking in an effect graph.</span></span> <span data-ttu-id="d8143-117">Die erste Abbildung zeigt ein typisches Direct2D Effect-Diagramm mit vier Renderingtransformationen.</span><span class="sxs-lookup"><span data-stu-id="d8143-117">The first figure shows a typical Direct2D effect graph with four rendering transforms.</span></span> <span data-ttu-id="d8143-118">Ohne Shader-Verknüpfung nutzt jede Transformation einen Renderingdurchlauf und erfordert eine zwischen Oberfläche. in diesem Diagramm sind insgesamt 4 Pass-und 3-zwischenate erforderlich.</span><span class="sxs-lookup"><span data-stu-id="d8143-118">Without shader linking, each transform consumes a rendering pass and requires an intermediate surface; in total, this graph requires 4 passes and 3 intermediates.</span></span>



|                                                                                                             |
|-------------------------------------------------------------------------------------------------------------|
| ![Transformieren des Diagramms ohne shaderverknüpfung: 4 Pass-und 3-Intermediate.](images/shader-transform-graph.png) |



 

<span data-ttu-id="d8143-120">Die zweite Abbildung zeigt das gleiche Effekt Diagramm, in dem jede renderingtransformation durch eine Verknüpf bares-Funktions Version ersetzt wurde.</span><span class="sxs-lookup"><span data-stu-id="d8143-120">The second figure shows the same effect graph where each rendering transform has been replaced with a linkable function version.</span></span> <span data-ttu-id="d8143-121">Direct2D ist in der Lage, das gesamte Diagramm zu verknüpfen und in einem Durchlauf auszuführen, ohne dass ein Vermittler erforderlich ist.</span><span class="sxs-lookup"><span data-stu-id="d8143-121">Direct2D is able link the entire graph and execute it in one pass without requiring any intermediates.</span></span> <span data-ttu-id="d8143-122">Dies kann zu einer deutlichen Verringerung der GPU-Ausführungszeit und zur Verringerung der GPU-Speicherauslastung in Spitzenzeiten.</span><span class="sxs-lookup"><span data-stu-id="d8143-122">This can provide a significant decrease in GPU execution time and reduction in peak GPU memory consumption.</span></span>



|                                                                                                   |
|---------------------------------------------------------------------------------------------------|
| ![Transformieren des Diagramms mit shaderverknüpfung: 1 Durchlauf, 0 zwischen.](images/shader-linking-graph.png) |



 

<span data-ttu-id="d8143-124">Auswirkungen der Shader-Verknüpfung auf einzelne Transformationen innerhalb eines Effekts. Dies bedeutet, dass selbst ein Diagramm mit einem einzelnen Effekt von Shader-Verknüpfungen profitieren kann, wenn dieser Effekt über mehrere gültige Transformationen verfügt.</span><span class="sxs-lookup"><span data-stu-id="d8143-124">Effect shader linking operates on individual transforms within an effect; this means that even a graph with a single effect may benefit from shader linking if that effect has multiple valid transforms.</span></span>

## <a name="using-effect-shader-linking"></a><span data-ttu-id="d8143-125">Verwenden von Effekt-Shader-Verknüpfung</span><span class="sxs-lookup"><span data-stu-id="d8143-125">Using Effect Shader Linking</span></span>

<span data-ttu-id="d8143-126">Wenn Sie eine Direct2D-Anwendung erstellen, die Effekte verwendet, müssen Sie nichts Unternehmen, um den Effekt von Shader-Verknüpfungen zu nutzen.</span><span class="sxs-lookup"><span data-stu-id="d8143-126">If you are building a Direct2D application that uses effects, you don’t need to do anything to take advantage of effect shader linking.</span></span> <span data-ttu-id="d8143-127">Direct2D analysiert automatisch das Effekt Diagramm, um die optimale Methode zum Verknüpfen der einzelnen Transformationen zu ermitteln.</span><span class="sxs-lookup"><span data-stu-id="d8143-127">Direct2D automatically analyzes the effect graph to determine the most optimal way to link each transform.</span></span>

<span data-ttu-id="d8143-128">Autoren von Effekten sind dafür verantwortlich, ihre Wirkung auf eine Weise zu implementieren, die das Verknüpfen von shadereffekten unterstützt. Weitere Informationen finden Sie weiter unten im Abschnitt [Authoring a Shader Linking-Compatible Custom Effect](#authoring-a-shader-linking-compatible-custom-effect) .</span><span class="sxs-lookup"><span data-stu-id="d8143-128">Effect authors are responsible for implementing their effect in a way that supports effect shader linking; for more information, see the [Authoring a shader linking-compatible custom effect](#authoring-a-shader-linking-compatible-custom-effect) section below.</span></span> <span data-ttu-id="d8143-129">Alle integrierten Effekte unterstützen Shader-Verknüpfungen.</span><span class="sxs-lookup"><span data-stu-id="d8143-129">All of the built-in effects support shader linking.</span></span>

<span data-ttu-id="d8143-130">Direct2D verknüpft nur angrenzende Renderingtransformationen in Situationen, in denen es von Vorteil ist.</span><span class="sxs-lookup"><span data-stu-id="d8143-130">Direct2D will only link adjacent rendering transforms in situations where it is beneficial.</span></span> <span data-ttu-id="d8143-131">Bei der Entscheidung, ob zwei Transformationen verknüpft werden sollen, werden mehrere Faktoren berücksichtigt.</span><span class="sxs-lookup"><span data-stu-id="d8143-131">It takes into account multiple factors when determining whether to link two transforms.</span></span> <span data-ttu-id="d8143-132">Beispielsweise wird die Shader-Verknüpfung nicht ausgeführt, wenn eine der Transformationen Scheitelpunkt-oder COMPUTE-Shader verwendet, da nur Pixel-Shader verknüpft werden können.</span><span class="sxs-lookup"><span data-stu-id="d8143-132">For example, shader linking is not performed if one of the transforms uses vertex or compute shaders, as only pixel shaders can be linked.</span></span> <span data-ttu-id="d8143-133">Wenn ein Effekt nicht so erstellt wurde, dass er mit Shader-Verknüpfungen kompatibel ist, werden umgebende Transformationen nicht damit verknüpft.</span><span class="sxs-lookup"><span data-stu-id="d8143-133">Also, if an effect was not authored to be compatible with shader linking, then surrounding transforms will not be linked with it.</span></span>

<span data-ttu-id="d8143-134">Wenn eine solche Verknüpfungs Gefahr besteht, verknüpft Direct2D keine Transformationen neben der Gefahr, sondern versucht trotzdem, den Rest des Diagramms zu verknüpfen.</span><span class="sxs-lookup"><span data-stu-id="d8143-134">In the case that such a linking hazard exists, Direct2D will not link any transforms adjacent to the hazard, but will still attempt to link the remainder of the graph.</span></span>



|                                                                                                             |
|-------------------------------------------------------------------------------------------------------------|
| ![Transformieren des Diagramms mit einer Verknüpfungs Gefahr: 2 Durchlauf, 1 zwischen.](images/shader-linking-graph-hazard.png) |



 

## <a name="authoring-a-shader-linking-compatible-custom-effect"></a><span data-ttu-id="d8143-136">Erstellen eines shaderverknüpfungs-kompatiblen benutzerdefinierten Effekts</span><span class="sxs-lookup"><span data-stu-id="d8143-136">Authoring a shader linking-compatible custom effect</span></span>

<span data-ttu-id="d8143-137">Wenn Sie einen eigenen benutzerdefinierten Direct2D-Effekt erstellen, müssen Sie sicherstellen, dass die zugehörigen Transformationen die Shader-Verknüpfung des Effekts unterstützen.</span><span class="sxs-lookup"><span data-stu-id="d8143-137">If you are authoring your own custom Direct2D effect, you need to ensure that its transforms supports effect shader linking.</span></span> <span data-ttu-id="d8143-138">Dies erfordert einige geringfügige Änderungen daran, wie vorherige benutzerdefinierte Effekte implementiert wurden.</span><span class="sxs-lookup"><span data-stu-id="d8143-138">This requires some minor changes from how previous custom effects were implemented.</span></span> <span data-ttu-id="d8143-139">Wenn eine Transformation innerhalb des benutzerdefinierten Effekts keine shaderverknüpfung unterstützt, wird Sie von Direct2D nicht mit Transformationen verknüpft, die sich in der Ausgabe im Diagramm befinden.</span><span class="sxs-lookup"><span data-stu-id="d8143-139">If a transform within your custom effect does not support shader linking, then Direct2D will not link it with any transforms adjacent to it in the effect graph.</span></span>

<span data-ttu-id="d8143-140">Als Autor eines benutzerdefinierten Effekts sollten Sie verschiedene wichtige Konzepte und Anforderungen beachten:</span><span class="sxs-lookup"><span data-stu-id="d8143-140">As a custom effect author, you should be aware of several key concepts and requirements:</span></span>

-   <span data-ttu-id="d8143-141">**Keine Änderungen an den Effekten der Schnittstellen Implementierungen.**</span><span class="sxs-lookup"><span data-stu-id="d8143-141">**No changes to effect interface implementations**</span></span>

    <span data-ttu-id="d8143-142">Sie müssen keinen Code ändern, der die verschiedenen Wirkungs Schnittstellen, wie z. b. [ID2D1DrawTransform](/windows/win32/api/d2d1effectauthor/nn-d2d1effectauthor-id2d1drawtransform), implementiert.</span><span class="sxs-lookup"><span data-stu-id="d8143-142">You do not need to modify any code implementing the various effect interfaces such as [ID2D1DrawTransform](/windows/win32/api/d2d1effectauthor/nn-d2d1effectauthor-id2d1drawtransform).</span></span>

-   <span data-ttu-id="d8143-143">**Bereitstellen einer vollständigen und Export Funktions Version von Shadern**</span><span class="sxs-lookup"><span data-stu-id="d8143-143">**Provide both a full and export function version of shaders**</span></span>

    <span data-ttu-id="d8143-144">Sie müssen eine Export Funktions Version der Shader Ihres Effekts bereitstellen, die von Direct2D untersucht werden können.</span><span class="sxs-lookup"><span data-stu-id="d8143-144">You must provide an export function version of your effect’s shaders which are linkable by Direct2D.</span></span> <span data-ttu-id="d8143-145">Außerdem müssen Sie auch weiterhin den ursprünglichen vollständigen Shader bereitstellen. Dies liegt daran, dass Direct2D zur Laufzeit die richtige shaderversion auswählt, je nachdem, ob die Shader-Verknüpfung auf einen bestimmten Link im Diagramm angewendet werden soll.</span><span class="sxs-lookup"><span data-stu-id="d8143-145">In addition, you must also continue to provide the original, full shader; this is because Direct2D selects at runtime the right shader version depending on whether shader linking is to be applied to a particular link in the graph.</span></span>

    <span data-ttu-id="d8143-146">Wenn eine Transformation nur das vollständige Pixel-Shader-BLOB (über [ID2D1EffectContext:: loadpixelshader](/windows/win32/api/d2d1effectauthor/nf-d2d1effectauthor-id2d1effectcontext-loadpixelshader)) bereitstellt, wird Sie nicht mit angrenzenden Transformationen verknüpft.</span><span class="sxs-lookup"><span data-stu-id="d8143-146">If a transform only provides the full pixel shader blob (via [ID2D1EffectContext::LoadPixelShader](/windows/win32/api/d2d1effectauthor/nf-d2d1effectauthor-id2d1effectcontext-loadpixelshader)), it will not be linked to adjacent transforms.</span></span>

- <span data-ttu-id="d8143-147">**Hilfsfunktionen**</span><span class="sxs-lookup"><span data-stu-id="d8143-147">**Helper functions**</span></span>

    <span data-ttu-id="d8143-148">Direct2D stellt [HLSL](hlsl-helpers.md) -Hilfsobjekte und-Makros bereit, mit denen automatisch sowohl die vollständigen als auch die Export Funktions Versionen eines Shaders generiert werden.</span><span class="sxs-lookup"><span data-stu-id="d8143-148">Direct2D provides [HLSL helper functions](hlsl-helpers.md) and macros that will automatically generate both the full and export function versions of a shader.</span></span> <span data-ttu-id="d8143-149">Diese Hilfsprogramme finden Sie unter d2d1effecthelpers. hlsli.</span><span class="sxs-lookup"><span data-stu-id="d8143-149">These helpers can be found in d2d1effecthelpers.hlsli.</span></span> <span data-ttu-id="d8143-150">Außerdem können Sie mit dem HLSL-Compiler (FXC) den Export Funktions-Shader in ein privates Feld im vollständigen Shader einfügen.</span><span class="sxs-lookup"><span data-stu-id="d8143-150">In addition, the HLSL compiler (FXC) lets you insert the export function shader into a private field in the full shader.</span></span> <span data-ttu-id="d8143-151">Auf diese Weise müssen Sie nur einmal einen Shader erstellen und beide Versionen gleichzeitig an Direct2D übergeben.</span><span class="sxs-lookup"><span data-stu-id="d8143-151">In this way, you only need to author a shader once and pass both versions to Direct2D simultaneously.</span></span> <span data-ttu-id="d8143-152">Sowohl d2d1effecthelpers. hlsli als auch der FXC-Compiler sind als Teil des Windows SDK enthalten.</span><span class="sxs-lookup"><span data-stu-id="d8143-152">Both d2d1effecthelpers.hlsli and the FXC compiler are included as part of the Windows SDK.</span></span>

    <span data-ttu-id="d8143-153">Die Hilfsfunktionen:</span><span class="sxs-lookup"><span data-stu-id="d8143-153">The helper functions:</span></span>

  - [<span data-ttu-id="d8143-154">D2DGetInput</span><span class="sxs-lookup"><span data-stu-id="d8143-154">D2DGetInput</span></span>](d2dgetinput.md)  
  - [<span data-ttu-id="d8143-155">D2DSampleInput</span><span class="sxs-lookup"><span data-stu-id="d8143-155">D2DSampleInput</span></span>](d2dsampleinput.md)  
  - [<span data-ttu-id="d8143-156">D2DSampleInputAtOffset</span><span class="sxs-lookup"><span data-stu-id="d8143-156">D2DSampleInputAtOffset</span></span>](d2dsampleinputatoffset.md)  
  - [<span data-ttu-id="d8143-157">D2DSampleInputAtPosition</span><span class="sxs-lookup"><span data-stu-id="d8143-157">D2DSampleInputAtPosition</span></span>](d2dsampleinputatposition.md)  
  - [<span data-ttu-id="d8143-158">D2DGetInputCoordinate</span><span class="sxs-lookup"><span data-stu-id="d8143-158">D2DGetInputCoordinate</span></span>](d2dgetinputcoordinate.md)  
  - [<span data-ttu-id="d8143-159">D2DGetScenePosition</span><span class="sxs-lookup"><span data-stu-id="d8143-159">D2DGetScenePosition</span></span>](d2dgetsceneposition.md)  
  - [<span data-ttu-id="d8143-160">D2D \_ PS- \_ Eintrag</span><span class="sxs-lookup"><span data-stu-id="d8143-160">D2D\_PS\_ENTRY</span></span>](d2d-ps-entry.md)  

  <span data-ttu-id="d8143-161">Sie können auch manuell zwei Versionen der einzelnen Shader erstellen und diese zweimal kompilieren, sofern die unten aufgeführten Spezifikationen in den [Export Funktions Spezifikationen](#export-function-specifications) erfüllt sind.</span><span class="sxs-lookup"><span data-stu-id="d8143-161">You can also manually author two versions of each shader and compile them twice, as long as the specifications described below in [Export function specifications](#export-function-specifications) are met.</span></span>

-   <span data-ttu-id="d8143-162">**Nur Pixel-Shader**</span><span class="sxs-lookup"><span data-stu-id="d8143-162">**Pixel shaders only**</span></span>

    <span data-ttu-id="d8143-163">Direct2D bietet keine Unterstützung für das Verknüpfen von COMPUTE-oder Vertex-Shadern.</span><span class="sxs-lookup"><span data-stu-id="d8143-163">Direct2D does not support linking compute or vertex shaders.</span></span> <span data-ttu-id="d8143-164">Wenn Ihre Wirkung jedoch sowohl einen Scheitelpunkt als auch einen PixelShader verwendet, kann die Ausgabe des Pixelshaders weiterhin verknüpft werden.</span><span class="sxs-lookup"><span data-stu-id="d8143-164">However, if your effect uses both a vertex and pixel shader, the output of the pixel shader can still be linked.</span></span>

-   <span data-ttu-id="d8143-165">**Einfaches und komplexes Sampling**</span><span class="sxs-lookup"><span data-stu-id="d8143-165">**Simple versus complex sampling**</span></span>

    <span data-ttu-id="d8143-166">Die Verknüpfung der shaderfunktion funktioniert, indem die Ausgabe eines Pixelshaders mit der Eingabe eines nachfolgenden Pixelshader-Pass verbunden wird.</span><span class="sxs-lookup"><span data-stu-id="d8143-166">Shader function linking works by connecting the output of one pixel shader pass to the input of a subsequent pixel shader pass.</span></span> <span data-ttu-id="d8143-167">Dies ist nur möglich, wenn der verarbeitende Pixelshader nur einen einzelnen Eingabe Wert erfordert, um seine Berechnung auszuführen. Dieser Wert würde normalerweise von der Stichprobenentnahme einer Eingabe Textur in der Textur Koordinate stammen, die vom Vertexshader ausgegeben wird.</span><span class="sxs-lookup"><span data-stu-id="d8143-167">This is only possible when the consuming pixel shader requires only a single input value to perform its computation; this value would normally come from sampling an input texture at the texture coordinate emitted by the vertex shader.</span></span> <span data-ttu-id="d8143-168">Ein solcher Pixel-Shader wird als einfache Stichprobenentnahme bezeichnet.</span><span class="sxs-lookup"><span data-stu-id="d8143-168">Such a pixel shader is said to perform simple sampling.</span></span>

    

    |                                                                                                                                                                                            |
    |--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
    | ![die Graustufen Konvertierung ist ein Beispiel für eine einfache Stichprobenentnahme.](images/simple-sampling.png) |

    

     

    <span data-ttu-id="d8143-171">Einige Pixel-Shader, wie z. b. ein gauscher Weichzeichner, berechnen Ihre Ausgabe aus mehreren Eingabe Beispielen anstelle eines einzelnen Beispiels.</span><span class="sxs-lookup"><span data-stu-id="d8143-171">Some pixel shaders, such as a Gaussian blur, compute their output from multiple input samples rather than just a single sample.</span></span> <span data-ttu-id="d8143-172">Ein solcher Pixel-Shader wird als komplexe Stichprobenentnahme bezeichnet.</span><span class="sxs-lookup"><span data-stu-id="d8143-172">Such a pixel shader is said to perform complex sampling.</span></span>

    

    |                                                                                                                                                           |
    |-----------------------------------------------------------------------------------------------------------------------------------------------------------|
    | ![gauscher Weichzeichner ist ein Beispiel für eine komplexe Stichprobenentnahme.](images/complex-sampling.png) |

    

     

    <span data-ttu-id="d8143-175">Nur Shaderfunktionen mit einfachen Eingaben können von einer anderen shaderfunktion bereitgestellt werden.</span><span class="sxs-lookup"><span data-stu-id="d8143-175">Only shader functions with simple inputs can have their input provided by another shader function.</span></span> <span data-ttu-id="d8143-176">Shader-Funktionen mit komplexen Eingaben müssen mit einer Eingabe Textur für Stichproben bereitgestellt werden.</span><span class="sxs-lookup"><span data-stu-id="d8143-176">Shader functions with complex inputs must be provided with an input texture to sample.</span></span> <span data-ttu-id="d8143-177">Dies bedeutet, dass Direct2D keinen Shader mit komplexen Eingaben mit seinem Vorgänger verknüpft.</span><span class="sxs-lookup"><span data-stu-id="d8143-177">This means that Direct2D will not link a shader with complex inputs to its predecessor.</span></span>

    <span data-ttu-id="d8143-178">Wenn Sie die [Direct2D HLSL](hlsl-helpers.md)-Hilfsprogramme verwenden, müssen Sie im HLSL angeben, ob ein Shader komplexe oder einfache Eingaben verwendet.</span><span class="sxs-lookup"><span data-stu-id="d8143-178">When using the [Direct2D HLSL helpers](hlsl-helpers.md), you must indicate in the HLSL whether a shader uses complex or simple inputs.</span></span>

## <a name="example-linking-compatible-effect-shader"></a><span data-ttu-id="d8143-179">Beispiel-Shader mit Verknüpfungs kompatiblem Effekten</span><span class="sxs-lookup"><span data-stu-id="d8143-179">Example linking-compatible effect shader</span></span>

<span data-ttu-id="d8143-180">Der folgende Code Ausschnitt stellt mithilfe der D2D-Hilfsprogramme einen einfachen Verknüpfungs kompatiblen Effekt-Shader dar:</span><span class="sxs-lookup"><span data-stu-id="d8143-180">Using the D2D helpers, the following code snippet represents a simple linking-compatible effect shader:</span></span>

```syntax
#define D2D_INPUT_COUNT 1
#define D2D_INPUT0_SIMPLE
#include “d2d1effecthelpers.hlsli”

D2D_PS_ENTRY(LinkingCompatiblePixelShader)
{
    float4 input = D2DGetInput(0);
    input.rgb *= input.a;
    return input;
}          
```

<span data-ttu-id="d8143-181">Beachten Sie in diesem kurzen Beispiel, dass keine Funktionsparameter deklariert werden, dass die Anzahl der Eingaben und der Typ der einzelnen Eingaben vor der Einstiegs Funktion deklariert wird. die Eingabe wird durch Aufrufen von [D2DGetInput](d2dgetinput.md)abgerufen, und die Präprozessordirektiven müssen vor dem einschließen der Hilfsdatei definiert werden.</span><span class="sxs-lookup"><span data-stu-id="d8143-181">In this short example note that no function parameters are declared, that the number of inputs and type of each input is declared before the entry function, the input is retrieved by calling [D2DGetInput](d2dgetinput.md), and that preprocessor directives must be defined before the helper file is included.</span></span>

<span data-ttu-id="d8143-182">Ein Verknüpfungs kompatibler Shader muss sowohl einen regulären Einzelpass-Pixel-Shader als auch eine Export-Shader-Funktion bereitstellen.</span><span class="sxs-lookup"><span data-stu-id="d8143-182">A linking-compatible shader must provide both a regular single-pass pixel shader and an export shader function.</span></span> <span data-ttu-id="d8143-183">Mit dem [D2D \_ PS- \_ Eintrags](d2d-ps-entry.md) Makro können alle diese aus demselben Code generiert werden, wenn Sie in Verbindung mit dem Shader-Kompilierungs Skript verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="d8143-183">The [D2D\_PS\_ENTRY](d2d-ps-entry.md) macro allows each of these to be generated from the same code, when used in conjunction with the shader compilation script.</span></span>

<span data-ttu-id="d8143-184">Beim Kompilieren eines vollständigen Shaders werden die Makros in den folgenden Code erweitert, der über eine D2D Effects-kompatible Eingabe Signatur verfügt.</span><span class="sxs-lookup"><span data-stu-id="d8143-184">When compiling a full shader, the macros are expanded into the following code, which has a D2D Effects-compatible input signature.</span></span>

```syntax
Texture2D<float4> InputTexture0;
SamplerState InputSampler0;

float4 LinkingCompatiblePixelShader(
    float4 pos   : SV_POSITION,
    float4 posScene : SCENE_POSITION,
    float4 uv0  : TEXCOORD0
    ) : SV_Target
    {
        float4 input = InputTexture0.Sample(InputSampler0, uv0.xy);
        input.rgb *= input.a;
        return input;
    }    
```

<span data-ttu-id="d8143-185">Wenn eine Export Funktions Version desselben Codes kompiliert wird, wird der folgende Code generiert:</span><span class="sxs-lookup"><span data-stu-id="d8143-185">When compiling an export function version of the same code, the following code is generated:</span></span>

```syntax
// Shader function version
export float4 LinkingCompatiblePixelShader_Function(
    float4 input0 : INPUT0)
    {
        input.rgb *= input.a;
        return input;
    }      
```

<span data-ttu-id="d8143-186">Beachten Sie, dass die Textur Eingabe, die normalerweise durch Sampling eines Texture2D abgerufen wird, durch eine Funktions Eingabe (input0) ersetzt wurde.</span><span class="sxs-lookup"><span data-stu-id="d8143-186">Note that the texture input, normally retrieved by sampling a Texture2D, has been replaced with a function input (input0).</span></span>

<span data-ttu-id="d8143-187">Eine vollständige Beschreibung der Schritte, die Sie zum Schreiben eines Verknüpfungs kompatiblen Effekts ausführen müssen, finden Sie im [Tutorial zu benutzerdefinierten Effekten](custom-effects.md) und im [Beispiel Direct2D Custom Image Effects](https://github.com/microsoft/Windows-universal-samples/tree/master/Samples/D2DCustomEffects).</span><span class="sxs-lookup"><span data-stu-id="d8143-187">To see a full, step by step description of what you need to do to write a linking-compatible effect, see the [Custom effects tutorial](custom-effects.md) and the [Direct2D custom image effects sample](https://github.com/microsoft/Windows-universal-samples/tree/master/Samples/D2DCustomEffects).</span></span>

## <a name="compiling-a-linking-compatible-shader"></a><span data-ttu-id="d8143-188">Kompilieren eines verknüpften kompatiblen Shaders</span><span class="sxs-lookup"><span data-stu-id="d8143-188">Compiling a linking compatible-shader</span></span>

<span data-ttu-id="d8143-189">Damit Sie nicht erreichbar sind, muss das an D2D über gegebene Pixel-Shader-BLOB sowohl die vollständigen als auch die Export Funktions Versionen des Shaders enthalten.</span><span class="sxs-lookup"><span data-stu-id="d8143-189">To be linkable, the pixel shader blob passed to D2D must contain both the full and export function versions of the shader.</span></span> <span data-ttu-id="d8143-190">Dies wird erreicht, indem die kompilierte Exportfunktion in den \_ \_ privaten Datenbereich D3D BLOB eingebettet wird \_ .</span><span class="sxs-lookup"><span data-stu-id="d8143-190">This is accomplished by embedding the compiled export function into the D3D\_BLOB\_PRIVATE\_DATA area.</span></span>

<span data-ttu-id="d8143-191">Wenn die Shader mit den D2D Helper-Funktionen erstellt werden, muss zum Zeitpunkt der Kompilierung ein D2D-Kompilierungs Ziel definiert werden.</span><span class="sxs-lookup"><span data-stu-id="d8143-191">When the shaders are authored with the D2D helper functions, a D2D compilation target must be defined at compilation time.</span></span> <span data-ttu-id="d8143-192">Die Ziel Typen für die Kompilierung sind D2D \_ Full \_ Shader und D2D \_ Function.</span><span class="sxs-lookup"><span data-stu-id="d8143-192">The compilation target types are D2D\_FULL\_SHADER and D2D\_FUNCTION.</span></span>

<span data-ttu-id="d8143-193">Das Kompilieren eines Verknüpfungs kompatiblen Effekt-Shaders ist ein zweistufiger Prozess:</span><span class="sxs-lookup"><span data-stu-id="d8143-193">Compiling a linking-compatible effect shader is a two-step process:</span></span>

-   [<span data-ttu-id="d8143-194">Kompilieren der Export-Funktion</span><span class="sxs-lookup"><span data-stu-id="d8143-194">Compile the export function</span></span>](#step-1-compile-the-export-function)
-   [<span data-ttu-id="d8143-195">Kompilieren Sie den vollen Shader, und Betten Sie die Exportfunktion ein.</span><span class="sxs-lookup"><span data-stu-id="d8143-195">Compile the full shader and embed the export function</span></span>](#step-2-compile-the-full-shader-and-embed-the-export-function)

> [!Note]  
> <span data-ttu-id="d8143-196">Wenn Sie einen Effekt mithilfe von Visual Studio kompilieren, sollten Sie eine Batchdatei erstellen, die beide FXC-Befehle ausführt, und diese Batchdatei als benutzerdefinierten Buildschritt ausführen, der vor dem Kompilierungs Schritt ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="d8143-196">When compiling an effect using Visual Studio, you should create a batch file that executes both FXC commands and run this batch file as a custom build step that runs before the compile step.</span></span>

 

### <a name="step-1-compile-the-export-function"></a><span data-ttu-id="d8143-197">Schritt 1: Kompilieren der Exportfunktion</span><span class="sxs-lookup"><span data-stu-id="d8143-197">Step 1: Compile the export function</span></span>

```syntax
fxc /T <shadermodel> <MyShaderFile>.hlsl /D D2D_FUNCTION /D D2D_ENTRY=<entry> /Fl <MyShaderFile>.fxlib           
```

<span data-ttu-id="d8143-198">Um die Export Funktions Version Ihres Shaders zu kompilieren, müssen Sie die folgenden Flags an FXC übergeben.</span><span class="sxs-lookup"><span data-stu-id="d8143-198">To compile the export function version of your shader, you must pass the following flags to FXC.</span></span>



|                                |                                                                                                                                                                                                                                                           |
|--------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="d8143-199">**Flag**</span><span class="sxs-lookup"><span data-stu-id="d8143-199">**Flag**</span></span>                       | <span data-ttu-id="d8143-200">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="d8143-200">**Description**</span></span>                                                                                                                                                                                                                                           |
| <span data-ttu-id="d8143-201">/T <ShaderModel></span><span class="sxs-lookup"><span data-stu-id="d8143-201">/T <ShaderModel></span></span>         | <span data-ttu-id="d8143-202">Legen <ShaderModel> Sie auf das entsprechende Pixel-Shader-Profil fest, wie in der [FXC-Syntax](/windows/desktop/direct3dtools/dx-graphics-tools-fxc-syntax)definiert.</span><span class="sxs-lookup"><span data-stu-id="d8143-202">Set <ShaderModel> to the appropriate pixel shader profile as defined in [FXC Syntax](/windows/desktop/direct3dtools/dx-graphics-tools-fxc-syntax).</span></span> <span data-ttu-id="d8143-203">Dabei muss es sich um eines der unter "HLSL Shader Linking" aufgeführten Profile handeln.</span><span class="sxs-lookup"><span data-stu-id="d8143-203">This must be one of the profiles listed under “HLSL shader linking”.</span></span> |
| <span data-ttu-id="d8143-204"><MyShaderFile>. HLSL</span><span class="sxs-lookup"><span data-stu-id="d8143-204"><MyShaderFile>.hlsl</span></span>      | <span data-ttu-id="d8143-205">Legen <MyShaderFile> Sie auf den Namen der HLSL-Datei fest.</span><span class="sxs-lookup"><span data-stu-id="d8143-205">Set <MyShaderFile> to the name of the HLSL file.</span></span>                                                                                                                                                                                                    |
| <span data-ttu-id="d8143-206">/D D2D- \_ Funktion</span><span class="sxs-lookup"><span data-stu-id="d8143-206">/D D2D\_FUNCTION</span></span>               | <span data-ttu-id="d8143-207">Diese Definition weist FXC an, die Export Funktions Version des Shaders zu kompilieren.</span><span class="sxs-lookup"><span data-stu-id="d8143-207">This definition instructs FXC to compile the export function version of the shader.</span></span>                                                                                                                                                                       |
| <span data-ttu-id="d8143-208">/D D2D \_ Eintrag =<entry></span><span class="sxs-lookup"><span data-stu-id="d8143-208">/D D2D\_ENTRY=<entry></span></span>    | <span data-ttu-id="d8143-209">Legen <entry> Sie auf den Namen des HLSL-Einstiegs Punkts fest, den Sie im [D2D \_ PS- \_ Eintrags](d2d-ps-entry.md) Makro definiert haben.</span><span class="sxs-lookup"><span data-stu-id="d8143-209">Set <entry> to the name of the HLSL entry point you defined inside the [D2D\_PS\_ENTRY](d2d-ps-entry.md) macro.</span></span>                                                                                                                                    |
| <span data-ttu-id="d8143-210">/FL <MyShaderFile> . fxlib</span><span class="sxs-lookup"><span data-stu-id="d8143-210">/Fl <MyShaderFile>.fxlib</span></span> | <span data-ttu-id="d8143-211">Legen <MyShaderfile> Sie auf fest, wo Sie die Export Funktions Version des Shaders speichern möchten.</span><span class="sxs-lookup"><span data-stu-id="d8143-211">Set <MyShaderfile> to where you want to store the export function version of the shader.</span></span> <span data-ttu-id="d8143-212">Beachten Sie, dass die Erweiterung ". fxlib" lediglich zur Erleichterung der Identifikation dient.</span><span class="sxs-lookup"><span data-stu-id="d8143-212">Note the .fxlib extension is only for ease of identification.</span></span>                                                                                              |



 

### <a name="step-2-compile-the-full-shader-and-embed-the-export-function"></a><span data-ttu-id="d8143-213">Schritt 2: Kompilieren Sie den vollständigen Shader, und Betten Sie die Exportfunktion ein.</span><span class="sxs-lookup"><span data-stu-id="d8143-213">Step 2: Compile the full shader and embed the export function</span></span>

```syntax
fxc /T ps_<shadermodel> <MyShaderFile>.hlsl /D D2D_FULL_SHADER /D D2D_ENTRY=<entry> /E <entry> /setprivate <MyShaderFile>.fxlib /Fo <MyShader>.cso /Fh <MyShader>.h           
```

<span data-ttu-id="d8143-214">Um die vollständige Version Ihres Shaders mit der eingebetteten Exportversion zu kompilieren, müssen Sie die folgenden Flags an FXC übergeben.</span><span class="sxs-lookup"><span data-stu-id="d8143-214">To compile the full version of your shader with embedded export version, you must pass the following flags to FXC.</span></span>



|                                        |                                                                                                                                                                                                                                                                                      |
|----------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="d8143-215">**Flag**</span><span class="sxs-lookup"><span data-stu-id="d8143-215">**Flag**</span></span>                               | <span data-ttu-id="d8143-216">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="d8143-216">**Description**</span></span>                                                                                                                                                                                                                                                                      |
| <span data-ttu-id="d8143-217">/T <ShaderModel></span><span class="sxs-lookup"><span data-stu-id="d8143-217">/T <ShaderModel></span></span>                 | <span data-ttu-id="d8143-218">Legen <ShaderModel> Sie auf das entsprechende Pixel-Shader-Profil fest, wie in der [FXC-Syntax](/windows/desktop/direct3dtools/dx-graphics-tools-fxc-syntax)definiert.</span><span class="sxs-lookup"><span data-stu-id="d8143-218">Set <ShaderModel> to the appropriate pixel shader profile as defined in [FXC Syntax](/windows/desktop/direct3dtools/dx-graphics-tools-fxc-syntax).</span></span> <span data-ttu-id="d8143-219">Dabei muss es sich um das Pixel-Shader-Profil handeln, das dem in Schritt 1 angegebenen Verknüpfungs Profil entspricht.</span><span class="sxs-lookup"><span data-stu-id="d8143-219">This must be the pixel shader profile corresponding to the linking profile specified in Step 1.</span></span> |
| <span data-ttu-id="d8143-220"><MyShaderFile>. HLSL</span><span class="sxs-lookup"><span data-stu-id="d8143-220"><MyShaderFile>.hlsl</span></span>              | <span data-ttu-id="d8143-221">Legen <MyShaderFile> Sie auf den Namen der HLSL-Datei fest.</span><span class="sxs-lookup"><span data-stu-id="d8143-221">Set <MyShaderFile> to the name of the HLSL file.</span></span>                                                                                                                                                                                                                               |
| <span data-ttu-id="d8143-222">/D D2D \_ Full- \_ Shader</span><span class="sxs-lookup"><span data-stu-id="d8143-222">/D D2D\_FULL\_SHADER</span></span>                   | <span data-ttu-id="d8143-223">Diese Definition weist FXC an, die vollständige Version des Shaders zu kompilieren.</span><span class="sxs-lookup"><span data-stu-id="d8143-223">This definition instructs FXC to compile the full version of the shader.</span></span>                                                                                                                                                                                                             |
| <span data-ttu-id="d8143-224">/D D2D \_ Eintrag =<entry></span><span class="sxs-lookup"><span data-stu-id="d8143-224">/D D2D\_ENTRY=<entry></span></span>            | <span data-ttu-id="d8143-225">Legen <entry> Sie auf den Namen des HLSL-Einstiegs Punkts fest, den Sie im D2D \_ PS \_ Entry ()-Makro definiert haben.</span><span class="sxs-lookup"><span data-stu-id="d8143-225">Set <entry> to the name of the HLSL entry point you defined inside the D2D\_PS\_ENTRY() macro.</span></span>                                                                                                                                                                                 |
| <span data-ttu-id="d8143-226">/E <entry></span><span class="sxs-lookup"><span data-stu-id="d8143-226">/E <entry></span></span>                       | <span data-ttu-id="d8143-227">Legen <entry> Sie auf den Namen des HLSL-Einstiegs Punkts fest, den Sie im D2D \_ PS \_ Entry ()-Makro definiert haben.</span><span class="sxs-lookup"><span data-stu-id="d8143-227">Set <entry> to the name of the HLSL entry point you defined inside the D2D\_PS\_ENTRY() macro.</span></span>                                                                                                                                                                                 |
| <span data-ttu-id="d8143-228">/setprivate <MyShaderFile> . fxlib</span><span class="sxs-lookup"><span data-stu-id="d8143-228">/setprivate <MyShaderFile>.fxlib</span></span> | <span data-ttu-id="d8143-229">Dieses Argument weist FXC an, den in Schritt 1 generierten Export Funktions-Shader in den \_ \_ privaten Datenbereich D3D BLOB einzubetten \_ .</span><span class="sxs-lookup"><span data-stu-id="d8143-229">This argument instructs FXC to embed the export function shader generated in step 1 into the D3D\_BLOB\_PRIVATE\_DATA area.</span></span>                                                                                                                                                          |
| <span data-ttu-id="d8143-230">/FO <MyShader> . CSO</span><span class="sxs-lookup"><span data-stu-id="d8143-230">/Fo <MyShader>.cso</span></span>               | <span data-ttu-id="d8143-231">Legen <MyShader> Sie auf fest, wo Sie den abschließenden, kombinierten kompilierten Shader speichern möchten.</span><span class="sxs-lookup"><span data-stu-id="d8143-231">Set <MyShader> to where you want to store the final, combined compiled shader.</span></span>                                                                                                                                                                                                 |
| <span data-ttu-id="d8143-232">/FH <MyShader> . h</span><span class="sxs-lookup"><span data-stu-id="d8143-232">/Fh <MyShader>.h</span></span>                 | <span data-ttu-id="d8143-233">Legen <MyShader> Sie auf fest, wo Sie den abschließenden kombinierten Header speichern möchten.</span><span class="sxs-lookup"><span data-stu-id="d8143-233">Set <MyShader> to where you want to store the final, combined header.</span></span>                                                                                                                                                                                                          |



 

## <a name="export-function-specifications"></a><span data-ttu-id="d8143-234">Funktions Spezifikationen exportieren</span><span class="sxs-lookup"><span data-stu-id="d8143-234">Export function specifications</span></span>

<span data-ttu-id="d8143-235">Es ist möglich – aber nicht empfehlenswert –, einen kompatiblen Effekt-Shader zu erstellen, ohne die von D2D bereitgestellten Hilfsprogramme zu verwenden.</span><span class="sxs-lookup"><span data-stu-id="d8143-235">It is possible – though not recommended – to author a compatible effect shader without using the D2D-provided helpers.</span></span> <span data-ttu-id="d8143-236">Es muss darauf geachtet werden, dass die Eingabe Signaturen der vollständigen Shader-und Exportfunktionen den D2D-Spezifikationen entsprechen.</span><span class="sxs-lookup"><span data-stu-id="d8143-236">Care must be taken to ensure that both the full shader and export function input signatures conform to D2D specifications.</span></span>

<span data-ttu-id="d8143-237">Die Spezifikationen für vollständige Shader sind identisch mit früheren Windows-Versionen.</span><span class="sxs-lookup"><span data-stu-id="d8143-237">The specifications for full shaders are the same as earlier Windows versions.</span></span> <span data-ttu-id="d8143-238">Kurz gesagt, die Pixel-Shader-Eingabeparameter müssen SV \_ -Position, Szenen \_ Position und ein texkoord pro Effekt Eingabe sein.</span><span class="sxs-lookup"><span data-stu-id="d8143-238">Briefly, the pixel shader input parameters must be SV\_POSITION, SCENE\_POSITION, and one TEXCOORD per effect input.</span></span>

<span data-ttu-id="d8143-239">Für die Export-Funktion muss die Funktion ein float4-Wert zurückgeben, und die Eingaben müssen einen der folgenden Typen aufweisen:</span><span class="sxs-lookup"><span data-stu-id="d8143-239">For the export function, the function must return a float4 and its inputs must be one of the following types:</span></span>

-   <span data-ttu-id="d8143-240">Einfache Eingabe</span><span class="sxs-lookup"><span data-stu-id="d8143-240">Simple input</span></span>

    ```syntax
    float4 d2d_inputN : INPUTN         
    ```

    <span data-ttu-id="d8143-241">Bei einfachen Eingaben fügt D2D entweder eine Beispiel Funktion zwischen der Eingabe Textur und der Shader-Funktion ein, oder die Eingabe wird von der Ausgabe einer anderen shaderfunktion bereitgestellt.</span><span class="sxs-lookup"><span data-stu-id="d8143-241">For simple inputs, D2D will either insert a Sample function between the input texture and shader function, or the input will be provided by the output of another shader function.</span></span>

-   <span data-ttu-id="d8143-242">Komplexe Eingabe</span><span class="sxs-lookup"><span data-stu-id="d8143-242">Complex input</span></span>

    ```syntax
    float4 d2d_uvN  : TEXCOORDN                
    ```

    <span data-ttu-id="d8143-243">Bei komplexen Eingaben übergibt D2D nur eine Textur Koordinate, wie in der Dokumentation zu Windows 8 beschrieben.</span><span class="sxs-lookup"><span data-stu-id="d8143-243">For complex inputs, D2D will only pass a texture coordinate as described in Windows 8 documentation.</span></span>

-   <span data-ttu-id="d8143-244">Ausgabe Speicherort</span><span class="sxs-lookup"><span data-stu-id="d8143-244">Output location</span></span>

    ```syntax
    float4 d2d_posScene : SCENE_POSITION                
    ```

    <span data-ttu-id="d8143-245">Es kann nur eine Szenen \_ Positions Eingabe definiert werden.</span><span class="sxs-lookup"><span data-stu-id="d8143-245">Only one SCENE\_POSITION input can be defined.</span></span> <span data-ttu-id="d8143-246">Dieser Parameter sollte nur bei Bedarf eingeschlossen werden, da dieser Parameter nur von einer Funktion pro verknüpftem Shader verwendet werden kann.</span><span class="sxs-lookup"><span data-stu-id="d8143-246">This parameter should only be included when necessary, since only one function per linked shader can utilize this parameter.</span></span>

<span data-ttu-id="d8143-247">Die Semantik muss wie oben beschrieben definiert werden, da D2D die Semantik prüft, um zu entscheiden, wie Funktionen miteinander verknüpft werden sollen.</span><span class="sxs-lookup"><span data-stu-id="d8143-247">The semantics must be defined as above, as D2D will inspect the semantics to decide how to link functions together.</span></span> <span data-ttu-id="d8143-248">Wenn eine Funktions Eingabe nicht mit einem der oben genannten Typen identisch ist, wird die Funktion für Shader-Verknüpfungen abgelehnt.</span><span class="sxs-lookup"><span data-stu-id="d8143-248">If any function input does not match one of the above types, the function will be rejected for shader linking.</span></span>

## <a name="related-topics"></a><span data-ttu-id="d8143-249">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="d8143-249">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="d8143-250">HLSL-Hilfsprogramme</span><span class="sxs-lookup"><span data-stu-id="d8143-250">HLSL Helpers</span></span>](hlsl-helpers.md)
</dt> <dt>

[<span data-ttu-id="d8143-251">ID3D11Linker-Schnittstelle</span><span class="sxs-lookup"><span data-stu-id="d8143-251">ID3D11Linker interface</span></span>](/windows/desktop/api/d3d11shader/nn-d3d11shader-id3d11linker)
</dt> <dt>

[<span data-ttu-id="d8143-252">ID3D11FunctionLinkingGraph-Schnittstelle</span><span class="sxs-lookup"><span data-stu-id="d8143-252">ID3D11FunctionLinkingGraph interface</span></span>](/windows/desktop/api/d3d11shader/nn-d3d11shader-id3d11functionlinkinggraph)
</dt> </dl>

 

 