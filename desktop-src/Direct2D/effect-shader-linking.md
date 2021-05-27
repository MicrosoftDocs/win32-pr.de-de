---
title: Effektshader-Verknüpfung
description: Direct2D verwendet eine Optimierung namens Effekt-Shaderverknüpfung, bei der das Rendern mehrerer Effektdiagramme in einem einzelnen Durchgang kombiniert wird.
ms.assetid: 431A5B39-6C84-442D-AC66-0F341E10DF2C
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 75b6bad2170f2b897a5cf8ac3086a74945efa8bf
ms.sourcegitcommit: f848119a8faa29b27585f4df53f6e50ee9666684
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 05/27/2021
ms.locfileid: "110549235"
---
# <a name="effect-shader-linking"></a><span data-ttu-id="9a766-103">Effektshader-Verknüpfung</span><span class="sxs-lookup"><span data-stu-id="9a766-103">Effect Shader Linking</span></span>

<span data-ttu-id="9a766-104">Direct2D verwendet eine Optimierung namens Effekt-Shaderverknüpfung, bei der das Rendern mehrerer Effektdiagramme in einem einzelnen Durchgang kombiniert wird.</span><span class="sxs-lookup"><span data-stu-id="9a766-104">Direct2D uses an optimization called effect shader linking which combines multiple effect graph rendering passes into a single pass.</span></span>

-   [<span data-ttu-id="9a766-105">Übersicht über das Verknüpfen von Effekt-Shadern</span><span class="sxs-lookup"><span data-stu-id="9a766-105">Overview of Effect Shader Linking</span></span>](#overview-of-effect-shader-linking)
-   [<span data-ttu-id="9a766-106">Verwenden der Verknüpfung von Effekt-Shadern</span><span class="sxs-lookup"><span data-stu-id="9a766-106">Using Effect Shader Linking</span></span>](#using-effect-shader-linking)
-   [<span data-ttu-id="9a766-107">Erstellen eines shaderlinkkompatiblen benutzerdefinierten Effekts</span><span class="sxs-lookup"><span data-stu-id="9a766-107">Authoring a shader linking-compatible custom effect</span></span>](#authoring-a-shader-linking-compatible-custom-effect)
-   [<span data-ttu-id="9a766-108">Beispiel für einen verknüpfungskompatiblen Effekt-Shader</span><span class="sxs-lookup"><span data-stu-id="9a766-108">Example linking-compatible effect shader</span></span>](#example-linking-compatible-effect-shader)
-   [<span data-ttu-id="9a766-109">Kompilieren eines verknüpfungskompatiblen Shaders</span><span class="sxs-lookup"><span data-stu-id="9a766-109">Compiling a linking compatible-shader</span></span>](#compiling-a-linking-compatible-shader)
    -   [<span data-ttu-id="9a766-110">Schritt 1: Kompilieren der Exportfunktion</span><span class="sxs-lookup"><span data-stu-id="9a766-110">Step 1: Compile the export function</span></span>](#step-1-compile-the-export-function)
    -   [<span data-ttu-id="9a766-111">Schritt 2: Kompilieren des vollständigen Shaders und Einbetten der Exportfunktion</span><span class="sxs-lookup"><span data-stu-id="9a766-111">Step 2: Compile the full shader and embed the export function</span></span>](#step-2-compile-the-full-shader-and-embed-the-export-function)
-   [<span data-ttu-id="9a766-112">Exportieren von Funktionsspezifikationen</span><span class="sxs-lookup"><span data-stu-id="9a766-112">Export function specifications</span></span>](#export-function-specifications)
-   [<span data-ttu-id="9a766-113">Verwandte Themen</span><span class="sxs-lookup"><span data-stu-id="9a766-113">Related topics</span></span>](#related-topics)

## <a name="overview-of-effect-shader-linking"></a><span data-ttu-id="9a766-114">Übersicht über das Verknüpfen von Effekt-Shadern</span><span class="sxs-lookup"><span data-stu-id="9a766-114">Overview of Effect Shader Linking</span></span>

<span data-ttu-id="9a766-115">Die Optimierungen für Shaderverknüpfungen bauen auf HLSL-Shaderverknüpfungen auf, einem Direct3D 11.2-Feature, mit dem Pixel- und Vertex-Shader zur Laufzeit durch Verknüpfen vor kompilierter Shaderfunktionen generiert werden können.</span><span class="sxs-lookup"><span data-stu-id="9a766-115">The effect shader linking optimizations builds on top of HLSL shader linking, a Direct3D 11.2 feature that allows pixel and vertex shaders to be generated at runtime by linking pre-compiled shader functions.</span></span> <span data-ttu-id="9a766-116">Die folgenden Abbildungen veranschaulichen das Konzept der Verknüpfung von Effekt-Shadern in einem Effektdiagramm.</span><span class="sxs-lookup"><span data-stu-id="9a766-116">The following figures illustrate the concept of effect shader linking in an effect graph.</span></span> <span data-ttu-id="9a766-117">Die erste Abbildung zeigt ein typisches Direct2D-Effektdiagramm mit vier Renderingtransformationen.</span><span class="sxs-lookup"><span data-stu-id="9a766-117">The first figure shows a typical Direct2D effect graph with four rendering transforms.</span></span> <span data-ttu-id="9a766-118">Ohne Shaderverknüpfung verbraucht jede Transformation einen Renderingpass und erfordert eine Zwischenoberfläche. Insgesamt erfordert dieses Diagramm 4 Durchläufe und 3 Zwischenergebnisse.</span><span class="sxs-lookup"><span data-stu-id="9a766-118">Without shader linking, each transform consumes a rendering pass and requires an intermediate surface; in total, this graph requires 4 passes and 3 intermediates.</span></span>

![Transformationsdiagramm ohne Shaderverknüpfung: 4 Durchläufe und 3 Zwischenergebnisse.](images/shader-transform-graph.png)

<span data-ttu-id="9a766-120">Die zweite Abbildung zeigt dasselbe Effektdiagramm, in dem jede Renderingtransformation durch eine linkbare Funktionsversion ersetzt wurde.</span><span class="sxs-lookup"><span data-stu-id="9a766-120">The second figure shows the same effect graph where each rendering transform has been replaced with a linkable function version.</span></span> <span data-ttu-id="9a766-121">Direct2D kann das gesamte Diagramm verknüpfen und in einem Durchgang ausführen, ohne dass Zwischenergebnisse erforderlich sind.</span><span class="sxs-lookup"><span data-stu-id="9a766-121">Direct2D is able link the entire graph and execute it in one pass without requiring any intermediates.</span></span> <span data-ttu-id="9a766-122">Dies kann zu einer erheblichen Verringerung der GPU-Ausführungszeit und einer Verringerung der GPU-Arbeitsspeicherspitze führen.</span><span class="sxs-lookup"><span data-stu-id="9a766-122">This can provide a significant decrease in GPU execution time and reduction in peak GPU memory consumption.</span></span>

![Transformationsdiagramm mit Shaderverknüpfung: 1 Durchlauf, 0 Zwischenstufen.](images/shader-linking-graph.png)



 

<span data-ttu-id="9a766-124">Die Effekt-Shaderverknüpfung arbeitet mit einzelnen Transformationen innerhalb eines Effekts. Dies bedeutet, dass auch ein Graph mit einem einzigen Effekt von der Shaderverknüpfung profitieren kann, wenn dieser Effekt mehrere gültige Transformationen hat.</span><span class="sxs-lookup"><span data-stu-id="9a766-124">Effect shader linking operates on individual transforms within an effect; this means that even a graph with a single effect may benefit from shader linking if that effect has multiple valid transforms.</span></span>

## <a name="using-effect-shader-linking"></a><span data-ttu-id="9a766-125">Verwenden von Effekt-Shaderverknüpfungen</span><span class="sxs-lookup"><span data-stu-id="9a766-125">Using Effect Shader Linking</span></span>

<span data-ttu-id="9a766-126">Wenn Sie eine Direct2D-Anwendung erstellen, die Effekte verwendet, müssen Sie nichts unternehmen, um die Effekt-Shaderverknüpfung zu nutzen.</span><span class="sxs-lookup"><span data-stu-id="9a766-126">If you are building a Direct2D application that uses effects, you don’t need to do anything to take advantage of effect shader linking.</span></span> <span data-ttu-id="9a766-127">Direct2D analysiert automatisch das Effektdiagramm, um die optimale Methode zum Verknüpfen der einzelnen Transformationen zu ermitteln.</span><span class="sxs-lookup"><span data-stu-id="9a766-127">Direct2D automatically analyzes the effect graph to determine the most optimal way to link each transform.</span></span>

<span data-ttu-id="9a766-128">Effektautoren sind dafür verantwortlich, ihre Auswirkungen auf eine Weise zu implementieren, die das Verknüpfen von Effekt-Shadern unterstützt. Weitere Informationen finden Sie weiter unten im Abschnitt [Erstellen eines shaderverknüpfungskompatiblen benutzerdefinierten Effekts.](#authoring-a-shader-linking-compatible-custom-effect)</span><span class="sxs-lookup"><span data-stu-id="9a766-128">Effect authors are responsible for implementing their effect in a way that supports effect shader linking; for more information, see the [Authoring a shader linking-compatible custom effect](#authoring-a-shader-linking-compatible-custom-effect) section below.</span></span> <span data-ttu-id="9a766-129">Alle integrierten Effekte unterstützen die Shaderverknüpfung.</span><span class="sxs-lookup"><span data-stu-id="9a766-129">All of the built-in effects support shader linking.</span></span>

<span data-ttu-id="9a766-130">Direct2D verknüpft nur benachbarte Renderingtransformationen in Situationen, in denen dies vorteilhaft ist.</span><span class="sxs-lookup"><span data-stu-id="9a766-130">Direct2D will only link adjacent rendering transforms in situations where it is beneficial.</span></span> <span data-ttu-id="9a766-131">Bei der Entscheidung, ob zwei Transformationen verknüpft werden sollen, werden mehrere Faktoren berücksichtigt.</span><span class="sxs-lookup"><span data-stu-id="9a766-131">It takes into account multiple factors when determining whether to link two transforms.</span></span> <span data-ttu-id="9a766-132">Beispielsweise wird die Shaderverknüpfung nicht ausgeführt, wenn eine der Transformationen Scheitelpunkt- oder Compute-Shader verwendet, da nur Pixel-Shader verknüpft werden können.</span><span class="sxs-lookup"><span data-stu-id="9a766-132">For example, shader linking is not performed if one of the transforms uses vertex or compute shaders, as only pixel shaders can be linked.</span></span> <span data-ttu-id="9a766-133">Wenn ein Effekt nicht so erstellt wurde, dass er mit der Shaderverknüpfung kompatibel ist, werden umgebende Transformationen nicht damit verknüpft.</span><span class="sxs-lookup"><span data-stu-id="9a766-133">Also, if an effect was not authored to be compatible with shader linking, then surrounding transforms will not be linked with it.</span></span>

<span data-ttu-id="9a766-134">Falls eine solche Verknüpfungsgefahr vorliegt, verknüpft Direct2D keine Transformationen neben der Gefahr, sondern versucht weiterhin, den Rest des Diagramms zu verknüpfen.</span><span class="sxs-lookup"><span data-stu-id="9a766-134">In the case that such a linking hazard exists, Direct2D will not link any transforms adjacent to the hazard, but will still attempt to link the remainder of the graph.</span></span>

![Transformieren eines Diagramms mit einer Verknüpfungsgefahr: 2 Durchläufe, 1 Zwischendiagramm.](images/shader-linking-graph-hazard.png)

## <a name="authoring-a-shader-linking-compatible-custom-effect"></a><span data-ttu-id="9a766-136">Erstellen eines mit Shaderverknüpfung kompatiblen benutzerdefinierten Effekts</span><span class="sxs-lookup"><span data-stu-id="9a766-136">Authoring a shader linking-compatible custom effect</span></span>

<span data-ttu-id="9a766-137">Wenn Sie Einen eigenen benutzerdefinierten Direct2D-Effekt erstellen, müssen Sie sicherstellen, dass die Transformationen das Verknüpfen von Effekt-Shadern unterstützen.</span><span class="sxs-lookup"><span data-stu-id="9a766-137">If you are authoring your own custom Direct2D effect, you need to ensure that its transforms supports effect shader linking.</span></span> <span data-ttu-id="9a766-138">Dies erfordert einige geringfügige Änderungen an der Implementierung vorheriger benutzerdefinierter Effekte.</span><span class="sxs-lookup"><span data-stu-id="9a766-138">This requires some minor changes from how previous custom effects were implemented.</span></span> <span data-ttu-id="9a766-139">Wenn eine Transformation innerhalb Ihres benutzerdefinierten Effekts keine Shaderverknüpfung unterstützt, verknüpft Direct2D sie nicht mit transformationsgrenzend im Effektdiagramm.</span><span class="sxs-lookup"><span data-stu-id="9a766-139">If a transform within your custom effect does not support shader linking, then Direct2D will not link it with any transforms adjacent to it in the effect graph.</span></span>

<span data-ttu-id="9a766-140">Als Benutzerdefinierter Effektautor sollten Sie sich mehrerer wichtiger Konzepte und Anforderungen bewusst sein:</span><span class="sxs-lookup"><span data-stu-id="9a766-140">As a custom effect author, you should be aware of several key concepts and requirements:</span></span>

-   <span data-ttu-id="9a766-141">**Keine Änderungen an Auswirkungsschnittstellenimplementierungen**</span><span class="sxs-lookup"><span data-stu-id="9a766-141">**No changes to effect interface implementations**</span></span>

    <span data-ttu-id="9a766-142">Sie müssen keinen Code ändern, der die verschiedenen Effektschnittstellen wie [ID2D1DrawTransform implementiert.](/windows/win32/api/d2d1effectauthor/nn-d2d1effectauthor-id2d1drawtransform)</span><span class="sxs-lookup"><span data-stu-id="9a766-142">You do not need to modify any code implementing the various effect interfaces such as [ID2D1DrawTransform](/windows/win32/api/d2d1effectauthor/nn-d2d1effectauthor-id2d1drawtransform).</span></span>

-   <span data-ttu-id="9a766-143">**Bereitstellen einer vollständigen und einer Exportfunktionsversion von Shadern**</span><span class="sxs-lookup"><span data-stu-id="9a766-143">**Provide both a full and export function version of shaders**</span></span>

    <span data-ttu-id="9a766-144">Sie müssen eine Exportfunktionsversion der Shader Ihres Effekts bereitstellen, die von Direct2D verlinkbar sind.</span><span class="sxs-lookup"><span data-stu-id="9a766-144">You must provide an export function version of your effect’s shaders which are linkable by Direct2D.</span></span> <span data-ttu-id="9a766-145">Darüber hinaus müssen Sie weiterhin den ursprünglichen, vollständigen Shader bereitstellen. Dies liegt daran, dass Direct2D zur Laufzeit die richtige Shaderversion auswählt, je nachdem, ob shader linking auf einen bestimmten Link im Diagramm angewendet werden soll.</span><span class="sxs-lookup"><span data-stu-id="9a766-145">In addition, you must also continue to provide the original, full shader; this is because Direct2D selects at runtime the right shader version depending on whether shader linking is to be applied to a particular link in the graph.</span></span>

    <span data-ttu-id="9a766-146">Wenn eine Transformation nur das vollständige Pixelsshaderblob (über [ID2D1EffectContext::LoadPixelShader)](/windows/win32/api/d2d1effectauthor/nf-d2d1effectauthor-id2d1effectcontext-loadpixelshader)bietet, wird es nicht mit angrenzenden Transformationen verknüpft.</span><span class="sxs-lookup"><span data-stu-id="9a766-146">If a transform only provides the full pixel shader blob (via [ID2D1EffectContext::LoadPixelShader](/windows/win32/api/d2d1effectauthor/nf-d2d1effectauthor-id2d1effectcontext-loadpixelshader)), it will not be linked to adjacent transforms.</span></span>

- <span data-ttu-id="9a766-147">**Hilfsfunktionen**</span><span class="sxs-lookup"><span data-stu-id="9a766-147">**Helper functions**</span></span>

    <span data-ttu-id="9a766-148">Direct2D stellt [HLSL-Hilfsfunktionen](hlsl-helpers.md) und -Makros zur Verfügung, die automatisch sowohl die vollständige als auch die Exportfunktionsversion eines Shaders generieren.</span><span class="sxs-lookup"><span data-stu-id="9a766-148">Direct2D provides [HLSL helper functions](hlsl-helpers.md) and macros that will automatically generate both the full and export function versions of a shader.</span></span> <span data-ttu-id="9a766-149">Diese Hilfsatoren finden Sie in d2d1effecthelpers.hlsli.</span><span class="sxs-lookup"><span data-stu-id="9a766-149">These helpers can be found in d2d1effecthelpers.hlsli.</span></span> <span data-ttu-id="9a766-150">Darüber hinaus können Sie mit dem HLSL-Compiler (FXC) den Shader der Exportfunktion in ein privates Feld im vollständigen Shader einfügen.</span><span class="sxs-lookup"><span data-stu-id="9a766-150">In addition, the HLSL compiler (FXC) lets you insert the export function shader into a private field in the full shader.</span></span> <span data-ttu-id="9a766-151">Auf diese Weise müssen Sie einen Shader nur einmal erstellen und beide Versionen gleichzeitig an Direct2D übergeben.</span><span class="sxs-lookup"><span data-stu-id="9a766-151">In this way, you only need to author a shader once and pass both versions to Direct2D simultaneously.</span></span> <span data-ttu-id="9a766-152">Sowohl d2d1effecthelpers.hlsli als auch der FXC-Compiler sind als Teil der Windows SDK.</span><span class="sxs-lookup"><span data-stu-id="9a766-152">Both d2d1effecthelpers.hlsli and the FXC compiler are included as part of the Windows SDK.</span></span>

    <span data-ttu-id="9a766-153">Die Hilfsfunktionen:</span><span class="sxs-lookup"><span data-stu-id="9a766-153">The helper functions:</span></span>

  - [<span data-ttu-id="9a766-154">D2DGetInput</span><span class="sxs-lookup"><span data-stu-id="9a766-154">D2DGetInput</span></span>](d2dgetinput.md)  
  - [<span data-ttu-id="9a766-155">D2DSampleInput</span><span class="sxs-lookup"><span data-stu-id="9a766-155">D2DSampleInput</span></span>](d2dsampleinput.md)  
  - [<span data-ttu-id="9a766-156">D2DSampleInputAtOffset</span><span class="sxs-lookup"><span data-stu-id="9a766-156">D2DSampleInputAtOffset</span></span>](d2dsampleinputatoffset.md)  
  - [<span data-ttu-id="9a766-157">D2DSampleInputAtPosition</span><span class="sxs-lookup"><span data-stu-id="9a766-157">D2DSampleInputAtPosition</span></span>](d2dsampleinputatposition.md)  
  - [<span data-ttu-id="9a766-158">D2DGetInputCoordinate</span><span class="sxs-lookup"><span data-stu-id="9a766-158">D2DGetInputCoordinate</span></span>](d2dgetinputcoordinate.md)  
  - [<span data-ttu-id="9a766-159">D2DGetScenePosition</span><span class="sxs-lookup"><span data-stu-id="9a766-159">D2DGetScenePosition</span></span>](d2dgetsceneposition.md)  
  - [<span data-ttu-id="9a766-160">D2D \_ \_ PS-EINTRAG</span><span class="sxs-lookup"><span data-stu-id="9a766-160">D2D\_PS\_ENTRY</span></span>](d2d-ps-entry.md)  

  <span data-ttu-id="9a766-161">Sie können auch manuell zwei Versionen jedes Shaders erstellen und sie zweimal kompilieren, solange die unten unter [Exportieren](#export-function-specifications) von Funktionsspezifikationen beschriebenen Spezifikationen erfüllt sind.</span><span class="sxs-lookup"><span data-stu-id="9a766-161">You can also manually author two versions of each shader and compile them twice, as long as the specifications described below in [Export function specifications](#export-function-specifications) are met.</span></span>

-   <span data-ttu-id="9a766-162">**Nur Pixel-Shader**</span><span class="sxs-lookup"><span data-stu-id="9a766-162">**Pixel shaders only**</span></span>

    <span data-ttu-id="9a766-163">Direct2D unterstützt keine Verknüpfung von Compute- oder Vertex-Shadern.</span><span class="sxs-lookup"><span data-stu-id="9a766-163">Direct2D does not support linking compute or vertex shaders.</span></span> <span data-ttu-id="9a766-164">Wenn Ihr Effekt jedoch sowohl einen Scheitelpunkt- als auch einen Pixel-Shader verwendet, kann die Ausgabe des Pixel-Shaders weiterhin verknüpft werden.</span><span class="sxs-lookup"><span data-stu-id="9a766-164">However, if your effect uses both a vertex and pixel shader, the output of the pixel shader can still be linked.</span></span>

-   <span data-ttu-id="9a766-165">**Einfaches und komplexes Sampling**</span><span class="sxs-lookup"><span data-stu-id="9a766-165">**Simple versus complex sampling**</span></span>

    <span data-ttu-id="9a766-166">Die Shaderfunktionsverknüpfung funktioniert, indem die Ausgabe eines Pixelshaderdurchlaufs mit der Eingabe eines nachfolgenden Pixelshaderdurchlaufs verbunden wird.</span><span class="sxs-lookup"><span data-stu-id="9a766-166">Shader function linking works by connecting the output of one pixel shader pass to the input of a subsequent pixel shader pass.</span></span> <span data-ttu-id="9a766-167">Dies ist nur möglich, wenn der verbrauchende Pixel-Shader nur einen einzelnen Eingabewert für die Berechnung benötigt. Dieser Wert stammt normalerweise aus der Stichprobenentnahme einer Eingabetextur an der Texturkoordinate, die vom Vertex-Shader ausgegeben wird.</span><span class="sxs-lookup"><span data-stu-id="9a766-167">This is only possible when the consuming pixel shader requires only a single input value to perform its computation; this value would normally come from sampling an input texture at the texture coordinate emitted by the vertex shader.</span></span> <span data-ttu-id="9a766-168">Ein solcher Pixelshader wird als einfache Stichprobenentnahme bezeichnet.</span><span class="sxs-lookup"><span data-stu-id="9a766-168">Such a pixel shader is said to perform simple sampling.</span></span>

    ![Die Graustufenkonvertierung ist ein Beispiel für eine einfache Stichprobenentnahme.](images/simple-sampling.png)

    <span data-ttu-id="9a766-171">Einige Pixel-Shader, z. B. ein Gaußsches Weichzeichner, berechnen ihre Ausgabe aus mehreren Eingabebeispielen und nicht nur aus einer einzelnen Stichprobe.</span><span class="sxs-lookup"><span data-stu-id="9a766-171">Some pixel shaders, such as a Gaussian blur, compute their output from multiple input samples rather than just a single sample.</span></span> <span data-ttu-id="9a766-172">Ein solcher Pixelshader wird als komplexe Stichprobenentnahme bezeichnet.</span><span class="sxs-lookup"><span data-stu-id="9a766-172">Such a pixel shader is said to perform complex sampling.</span></span>

    

    ![der weichzeichnerische Weichzeichner ist ein Beispiel für eine komplexe Stichprobenentnahme.](images/complex-sampling.png)

    
    <span data-ttu-id="9a766-175">Nur Shaderfunktionen mit einfachen Eingaben können ihre Eingaben von einer anderen Shaderfunktion erhalten.</span><span class="sxs-lookup"><span data-stu-id="9a766-175">Only shader functions with simple inputs can have their input provided by another shader function.</span></span> <span data-ttu-id="9a766-176">Shaderfunktionen mit komplexen Eingaben müssen mit einer Eingabetextur für die Stichprobenentnahme bereitgestellt werden.</span><span class="sxs-lookup"><span data-stu-id="9a766-176">Shader functions with complex inputs must be provided with an input texture to sample.</span></span> <span data-ttu-id="9a766-177">Dies bedeutet, dass Direct2D einen Shader nicht mit komplexen Eingaben mit seinem Vorgänger verknüpft.</span><span class="sxs-lookup"><span data-stu-id="9a766-177">This means that Direct2D will not link a shader with complex inputs to its predecessor.</span></span>

    <span data-ttu-id="9a766-178">Wenn Sie die [Direct2D HLSL-Hilfatoren](hlsl-helpers.md)verwenden, müssen Sie in der HLSL angeben, ob ein Shader komplexe oder einfache Eingaben verwendet.</span><span class="sxs-lookup"><span data-stu-id="9a766-178">When using the [Direct2D HLSL helpers](hlsl-helpers.md), you must indicate in the HLSL whether a shader uses complex or simple inputs.</span></span>

## <a name="example-linking-compatible-effect-shader"></a><span data-ttu-id="9a766-179">Beispiel für einen verknüpfungskompatiblen Effekt-Shader</span><span class="sxs-lookup"><span data-stu-id="9a766-179">Example linking-compatible effect shader</span></span>

<span data-ttu-id="9a766-180">Mithilfe der D2D-Hilfatoren stellt der folgende Codeausschnitt einen einfachen verlinkungskompatiblen Effekt-Shader dar:</span><span class="sxs-lookup"><span data-stu-id="9a766-180">Using the D2D helpers, the following code snippet represents a simple linking-compatible effect shader:</span></span>

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

<span data-ttu-id="9a766-181">Beachten Sie in diesem kurzen Beispiel, dass keine Funktionsparameter deklariert werden, dass die Anzahl der Eingaben und der Typ jeder Eingabe vor der Eingabefunktion deklariert wird, die Eingabe durch Aufrufen von [D2DGetInput](d2dgetinput.md)abgerufen wird und dass Präprozessordirektiven definiert werden müssen, bevor die Hilfsdatei eingeschlossen wird.</span><span class="sxs-lookup"><span data-stu-id="9a766-181">In this short example note that no function parameters are declared, that the number of inputs and type of each input is declared before the entry function, the input is retrieved by calling [D2DGetInput](d2dgetinput.md), and that preprocessor directives must be defined before the helper file is included.</span></span>

<span data-ttu-id="9a766-182">Ein mit Verknüpfungen kompatibler Shader muss sowohl einen regulären Einzelpasspixel-Shader als auch eine Export-Shaderfunktion bereitstellen.</span><span class="sxs-lookup"><span data-stu-id="9a766-182">A linking-compatible shader must provide both a regular single-pass pixel shader and an export shader function.</span></span> <span data-ttu-id="9a766-183">Das [D2D \_ PS \_ ENTRY-Makro](d2d-ps-entry.md) ermöglicht es, jede dieser Makros aus demselben Code zu erstellen, wenn sie in Verbindung mit dem Shaderkompilierungsskript verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="9a766-183">The [D2D\_PS\_ENTRY](d2d-ps-entry.md) macro allows each of these to be generated from the same code, when used in conjunction with the shader compilation script.</span></span>

<span data-ttu-id="9a766-184">Beim Kompilieren eines vollständigen Shaders werden die Makros in den folgenden Code erweitert, der über eine D2D Effects-kompatible Eingabesignatur verfügt.</span><span class="sxs-lookup"><span data-stu-id="9a766-184">When compiling a full shader, the macros are expanded into the following code, which has a D2D Effects-compatible input signature.</span></span>

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

<span data-ttu-id="9a766-185">Beim Kompilieren einer Exportfunktionsversion desselben Codes wird der folgende Code generiert:</span><span class="sxs-lookup"><span data-stu-id="9a766-185">When compiling an export function version of the same code, the following code is generated:</span></span>

```syntax
// Shader function version
export float4 LinkingCompatiblePixelShader_Function(
    float4 input0 : INPUT0)
    {
        input.rgb *= input.a;
        return input;
    }      
```

<span data-ttu-id="9a766-186">Beachten Sie, dass die Textureingabe, die normalerweise durch Sampling eines Texture2D abgerufen wird, durch eine Funktionseingabe (input0) ersetzt wurde.</span><span class="sxs-lookup"><span data-stu-id="9a766-186">Note that the texture input, normally retrieved by sampling a Texture2D, has been replaced with a function input (input0).</span></span>

<span data-ttu-id="9a766-187">Eine vollständige, schrittweise Beschreibung der Schritte, die Sie zum Schreiben eines verknüpfungskompatiblen Effekts benötigen, finden Sie im Tutorial Zu benutzerdefinierten Effekten und im Beispiel für [benutzerdefinierte Direct2D-Bildeffekte.](https://github.com/microsoft/Windows-universal-samples/tree/master/Samples/D2DCustomEffects) [](custom-effects.md)</span><span class="sxs-lookup"><span data-stu-id="9a766-187">To see a full, step by step description of what you need to do to write a linking-compatible effect, see the [Custom effects tutorial](custom-effects.md) and the [Direct2D custom image effects sample](https://github.com/microsoft/Windows-universal-samples/tree/master/Samples/D2DCustomEffects).</span></span>

## <a name="compiling-a-linking-compatible-shader"></a><span data-ttu-id="9a766-188">Kompilieren eines verknüpfungskompatiblen Shaders</span><span class="sxs-lookup"><span data-stu-id="9a766-188">Compiling a linking compatible-shader</span></span>

<span data-ttu-id="9a766-189">Um verlinkbar zu sein, muss das an D2D übergebene Pixel-Shaderblob sowohl die vollständige als auch die Exportfunktionsversion des Shaders enthalten.</span><span class="sxs-lookup"><span data-stu-id="9a766-189">To be linkable, the pixel shader blob passed to D2D must contain both the full and export function versions of the shader.</span></span> <span data-ttu-id="9a766-190">Dies wird erreicht, indem die kompilierte Exportfunktion in den D3D \_ BLOB \_ PRIVATE \_ DATA-Bereich eingebettet wird.</span><span class="sxs-lookup"><span data-stu-id="9a766-190">This is accomplished by embedding the compiled export function into the D3D\_BLOB\_PRIVATE\_DATA area.</span></span>

<span data-ttu-id="9a766-191">Wenn die Shader mit den D2D-Hilfsfunktionen erstellen, muss zum Zeitpunkt der Kompilierung ein D2D-Kompilierungsziel definiert werden.</span><span class="sxs-lookup"><span data-stu-id="9a766-191">When the shaders are authored with the D2D helper functions, a D2D compilation target must be defined at compilation time.</span></span> <span data-ttu-id="9a766-192">Die Kompilierungszieltypen sind D2D \_ FULL \_ SHADER und D2D \_ FUNCTION.</span><span class="sxs-lookup"><span data-stu-id="9a766-192">The compilation target types are D2D\_FULL\_SHADER and D2D\_FUNCTION.</span></span>

<span data-ttu-id="9a766-193">Das Kompilieren eines verknüpfungskompatiblen Effekt-Shaders ist ein zweistufiger Prozess:</span><span class="sxs-lookup"><span data-stu-id="9a766-193">Compiling a linking-compatible effect shader is a two-step process:</span></span>

-   [<span data-ttu-id="9a766-194">Kompilieren der Exportfunktion</span><span class="sxs-lookup"><span data-stu-id="9a766-194">Compile the export function</span></span>](#step-1-compile-the-export-function)
-   [<span data-ttu-id="9a766-195">Kompilieren des vollständigen Shaders und Einbetten der Exportfunktion</span><span class="sxs-lookup"><span data-stu-id="9a766-195">Compile the full shader and embed the export function</span></span>](#step-2-compile-the-full-shader-and-embed-the-export-function)

> [!Note]  
> <span data-ttu-id="9a766-196">Beim Kompilieren eines Effekts mit Visual Studio sollten Sie eine Batchdatei erstellen, die beide FXC-Befehle ausführt und diese Batchdatei als benutzerdefinierten Buildschritt ausführt, der vor dem Kompilierungsschritt ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="9a766-196">When compiling an effect using Visual Studio, you should create a batch file that executes both FXC commands and run this batch file as a custom build step that runs before the compile step.</span></span>

 

### <a name="step-1-compile-the-export-function"></a><span data-ttu-id="9a766-197">Schritt 1: Kompilieren der Exportfunktion</span><span class="sxs-lookup"><span data-stu-id="9a766-197">Step 1: Compile the export function</span></span>

```syntax
fxc /T <shadermodel> <MyShaderFile>.hlsl /D D2D_FUNCTION /D D2D_ENTRY=<entry> /Fl <MyShaderFile>.fxlib           
```

<span data-ttu-id="9a766-198">Um die Exportfunktionsversion Ihres Shaders zu kompilieren, müssen Sie die folgenden Flags an FXC übergeben.</span><span class="sxs-lookup"><span data-stu-id="9a766-198">To compile the export function version of your shader, you must pass the following flags to FXC.</span></span>



|    <span data-ttu-id="9a766-199">Flag</span><span class="sxs-lookup"><span data-stu-id="9a766-199">Flag</span></span>                            |    <span data-ttu-id="9a766-200">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="9a766-200">Description</span></span>                       |
|--------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="9a766-201">/T <ShaderModel></span><span class="sxs-lookup"><span data-stu-id="9a766-201">/T <ShaderModel></span></span>         | <span data-ttu-id="9a766-202">Legen <ShaderModel> Sie auf das entsprechende Pixel-Shaderprofil fest, wie in [FXC-Syntax definiert.](/windows/desktop/direct3dtools/dx-graphics-tools-fxc-syntax)</span><span class="sxs-lookup"><span data-stu-id="9a766-202">Set <ShaderModel> to the appropriate pixel shader profile as defined in [FXC Syntax](/windows/desktop/direct3dtools/dx-graphics-tools-fxc-syntax).</span></span> <span data-ttu-id="9a766-203">Dies muss eines der Unter "HLSL-Shaderverknüpfungen" aufgeführten Profile sein.</span><span class="sxs-lookup"><span data-stu-id="9a766-203">This must be one of the profiles listed under “HLSL shader linking”.</span></span> |
| <span data-ttu-id="9a766-204"><MyShaderFile>.hlsl</span><span class="sxs-lookup"><span data-stu-id="9a766-204"><MyShaderFile>.hlsl</span></span>      | <span data-ttu-id="9a766-205">Legen Sie <MyShaderFile> auf den Namen der HLSL-Datei fest.</span><span class="sxs-lookup"><span data-stu-id="9a766-205">Set <MyShaderFile> to the name of the HLSL file.</span></span>                                                                                                                                                                                                    |
| <span data-ttu-id="9a766-206">/D \_ D2D-FUNKTION</span><span class="sxs-lookup"><span data-stu-id="9a766-206">/D D2D\_FUNCTION</span></span>               | <span data-ttu-id="9a766-207">Diese Definition weist FXC an, die Exportfunktionsversion des Shaders zu kompilieren.</span><span class="sxs-lookup"><span data-stu-id="9a766-207">This definition instructs FXC to compile the export function version of the shader.</span></span>                                                                                                                                                                       |
| <span data-ttu-id="9a766-208">/D D2D \_ ENTRY=<entry></span><span class="sxs-lookup"><span data-stu-id="9a766-208">/D D2D\_ENTRY=<entry></span></span>    | <span data-ttu-id="9a766-209">Legen Sie <entry> auf den Namen des HLSL-Einstiegspunkts fest, den Sie im [D2D \_ PS \_ ENTRY-Makro](d2d-ps-entry.md) definiert haben.</span><span class="sxs-lookup"><span data-stu-id="9a766-209">Set <entry> to the name of the HLSL entry point you defined inside the [D2D\_PS\_ENTRY](d2d-ps-entry.md) macro.</span></span>                                                                                                                                    |
| <span data-ttu-id="9a766-210">/Fl <MyShaderFile> .fxlib</span><span class="sxs-lookup"><span data-stu-id="9a766-210">/Fl <MyShaderFile>.fxlib</span></span> | <span data-ttu-id="9a766-211">Legen <MyShaderfile> Sie auf fest, wo Sie die Exportfunktionsversion des Shaders speichern möchten.</span><span class="sxs-lookup"><span data-stu-id="9a766-211">Set <MyShaderfile> to where you want to store the export function version of the shader.</span></span> <span data-ttu-id="9a766-212">Beachten Sie, dass die Erweiterung .fxlib nur zur einfacheren Identifizierung dient.</span><span class="sxs-lookup"><span data-stu-id="9a766-212">Note the .fxlib extension is only for ease of identification.</span></span>                                                                                              |

### <a name="step-2-compile-the-full-shader-and-embed-the-export-function"></a><span data-ttu-id="9a766-213">Schritt 2: Kompilieren des vollständigen Shaders und Einbetten der Exportfunktion</span><span class="sxs-lookup"><span data-stu-id="9a766-213">Step 2: Compile the full shader and embed the export function</span></span>

```syntax
fxc /T ps_<shadermodel> <MyShaderFile>.hlsl /D D2D_FULL_SHADER /D D2D_ENTRY=<entry> /E <entry> /setprivate <MyShaderFile>.fxlib /Fo <MyShader>.cso /Fh <MyShader>.h           
```

<span data-ttu-id="9a766-214">Um die Vollversion Ihres Shaders mit eingebetteter Exportversion zu kompilieren, müssen Sie die folgenden Flags an FXC übergeben.</span><span class="sxs-lookup"><span data-stu-id="9a766-214">To compile the full version of your shader with embedded export version, you must pass the following flags to FXC.</span></span>



|    <span data-ttu-id="9a766-215">Flag</span><span class="sxs-lookup"><span data-stu-id="9a766-215">Flag</span></span>                                    |    <span data-ttu-id="9a766-216">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="9a766-216">Description</span></span>                     |
|----------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="9a766-217">/T <ShaderModel></span><span class="sxs-lookup"><span data-stu-id="9a766-217">/T <ShaderModel></span></span>                 | <span data-ttu-id="9a766-218">Legen Sie <ShaderModel> auf das entsprechende Pixel-Shaderprofil fest, wie in [FXC-Syntax](/windows/desktop/direct3dtools/dx-graphics-tools-fxc-syntax)definiert.</span><span class="sxs-lookup"><span data-stu-id="9a766-218">Set <ShaderModel> to the appropriate pixel shader profile as defined in [FXC Syntax](/windows/desktop/direct3dtools/dx-graphics-tools-fxc-syntax).</span></span> <span data-ttu-id="9a766-219">Dies muss das Pixel-Shaderprofil sein, das dem in Schritt 1 angegebenen Verknüpfungsprofil entspricht.</span><span class="sxs-lookup"><span data-stu-id="9a766-219">This must be the pixel shader profile corresponding to the linking profile specified in Step 1.</span></span> |
| <span data-ttu-id="9a766-220"><MyShaderFile>.hlsl</span><span class="sxs-lookup"><span data-stu-id="9a766-220"><MyShaderFile>.hlsl</span></span>              | <span data-ttu-id="9a766-221">Legen Sie <MyShaderFile> auf den Namen der HLSL-Datei fest.</span><span class="sxs-lookup"><span data-stu-id="9a766-221">Set <MyShaderFile> to the name of the HLSL file.</span></span>                                                                                                                                                                                                                               |
| <span data-ttu-id="9a766-222">/D D2D \_ FULL \_ SHADER</span><span class="sxs-lookup"><span data-stu-id="9a766-222">/D D2D\_FULL\_SHADER</span></span>                   | <span data-ttu-id="9a766-223">Diese Definition weist FXC an, die Vollversion des Shaders zu kompilieren.</span><span class="sxs-lookup"><span data-stu-id="9a766-223">This definition instructs FXC to compile the full version of the shader.</span></span>                                                                                                                                                                                                             |
| <span data-ttu-id="9a766-224">/D D2D \_ ENTRY=<entry></span><span class="sxs-lookup"><span data-stu-id="9a766-224">/D D2D\_ENTRY=<entry></span></span>            | <span data-ttu-id="9a766-225">Legen Sie <entry> auf den Namen des HLSL-Einstiegspunkts fest, den Sie im D2D PS \_ \_ ENTRY()-Makro definiert haben.</span><span class="sxs-lookup"><span data-stu-id="9a766-225">Set <entry> to the name of the HLSL entry point you defined inside the D2D\_PS\_ENTRY() macro.</span></span>                                                                                                                                                                                 |
| <span data-ttu-id="9a766-226">/E <entry></span><span class="sxs-lookup"><span data-stu-id="9a766-226">/E <entry></span></span>                       | <span data-ttu-id="9a766-227">Legen <entry> Sie auf den Namen des HLSL-Einstiegspunkts fest, den Sie im D2D PS \_ \_ ENTRY()-Makro definiert haben.</span><span class="sxs-lookup"><span data-stu-id="9a766-227">Set <entry> to the name of the HLSL entry point you defined inside the D2D\_PS\_ENTRY() macro.</span></span>                                                                                                                                                                                 |
| <span data-ttu-id="9a766-228">/setprivate <MyShaderFile> .fxlib</span><span class="sxs-lookup"><span data-stu-id="9a766-228">/setprivate <MyShaderFile>.fxlib</span></span> | <span data-ttu-id="9a766-229">Dieses Argument weist FXC an, den in Schritt 1 generierten Shader der Exportfunktion in den D3D \_ BLOB \_ PRIVATE \_ DATA-Bereich einbetten.</span><span class="sxs-lookup"><span data-stu-id="9a766-229">This argument instructs FXC to embed the export function shader generated in step 1 into the D3D\_BLOB\_PRIVATE\_DATA area.</span></span>                                                                                                                                                          |
| <span data-ttu-id="9a766-230">/Fo <MyShader> .cso</span><span class="sxs-lookup"><span data-stu-id="9a766-230">/Fo <MyShader>.cso</span></span>               | <span data-ttu-id="9a766-231">Legen <MyShader> Sie auf den Ort fest, an dem Sie den endgültigen, kombinierten kompilierten Shader speichern möchten.</span><span class="sxs-lookup"><span data-stu-id="9a766-231">Set <MyShader> to where you want to store the final, combined compiled shader.</span></span>                                                                                                                                                                                                 |
| <span data-ttu-id="9a766-232">/Kann <MyShader> .h</span><span class="sxs-lookup"><span data-stu-id="9a766-232">/Fh <MyShader>.h</span></span>                 | <span data-ttu-id="9a766-233">Legen <MyShader> Sie auf den Ort fest, an dem Sie den endgültigen kombinierten Header speichern möchten.</span><span class="sxs-lookup"><span data-stu-id="9a766-233">Set <MyShader> to where you want to store the final, combined header.</span></span>                                                                                                                                                                                                          |

## <a name="export-function-specifications"></a><span data-ttu-id="9a766-234">Exportieren von Funktionsspezifikationen</span><span class="sxs-lookup"><span data-stu-id="9a766-234">Export function specifications</span></span>

<span data-ttu-id="9a766-235">Es ist möglich , aber nicht zu empfehlen, einen kompatiblen Effekt-Shader zu erstellen, ohne die von D2D bereitgestellten Hilfsatoren zu verwenden.</span><span class="sxs-lookup"><span data-stu-id="9a766-235">It is possible – though not recommended – to author a compatible effect shader without using the D2D-provided helpers.</span></span> <span data-ttu-id="9a766-236">Es muss sichergestellt werden, dass sowohl der vollständige Shader als auch die Eingabesignaturen der Exportfunktion den D2D-Spezifikationen entsprechen.</span><span class="sxs-lookup"><span data-stu-id="9a766-236">Care must be taken to ensure that both the full shader and export function input signatures conform to D2D specifications.</span></span>

<span data-ttu-id="9a766-237">Die Spezifikationen für vollständige Shader sind identisch mit früheren Windows-Versionen.</span><span class="sxs-lookup"><span data-stu-id="9a766-237">The specifications for full shaders are the same as earlier Windows versions.</span></span> <span data-ttu-id="9a766-238">Kurz gesagt: Die Eingabeparameter für den Pixel-Shader müssen SV \_ POSITION, SCENE \_ POSITION und eine TEXCOORD-Eingabe pro Effekt sein.</span><span class="sxs-lookup"><span data-stu-id="9a766-238">Briefly, the pixel shader input parameters must be SV\_POSITION, SCENE\_POSITION, and one TEXCOORD per effect input.</span></span>

<span data-ttu-id="9a766-239">Für die Exportfunktion muss die Funktion float4 zurückgeben, und ihre Eingaben müssen einen der folgenden Typen haben:</span><span class="sxs-lookup"><span data-stu-id="9a766-239">For the export function, the function must return a float4 and its inputs must be one of the following types:</span></span>

-   <span data-ttu-id="9a766-240">Einfache Eingabe</span><span class="sxs-lookup"><span data-stu-id="9a766-240">Simple input</span></span>

    ```syntax
    float4 d2d_inputN : INPUTN         
    ```

    <span data-ttu-id="9a766-241">Bei einfachen Eingaben fügt D2D entweder eine Sample-Funktion zwischen der Eingabetextur und der Shaderfunktion ein, oder die Eingabe wird durch die Ausgabe einer anderen Shaderfunktion bereitgestellt.</span><span class="sxs-lookup"><span data-stu-id="9a766-241">For simple inputs, D2D will either insert a Sample function between the input texture and shader function, or the input will be provided by the output of another shader function.</span></span>

-   <span data-ttu-id="9a766-242">Komplexe Eingabe</span><span class="sxs-lookup"><span data-stu-id="9a766-242">Complex input</span></span>

    ```syntax
    float4 d2d_uvN  : TEXCOORDN                
    ```

    <span data-ttu-id="9a766-243">Bei komplexen Eingaben wird von D2D nur eine Texturkoordinate übergeben, wie in der Windows 8 beschrieben.</span><span class="sxs-lookup"><span data-stu-id="9a766-243">For complex inputs, D2D will only pass a texture coordinate as described in Windows 8 documentation.</span></span>

-   <span data-ttu-id="9a766-244">Ausgabespeicherort</span><span class="sxs-lookup"><span data-stu-id="9a766-244">Output location</span></span>

    ```syntax
    float4 d2d_posScene : SCENE_POSITION                
    ```

    <span data-ttu-id="9a766-245">Es kann nur \_ eine SCENE POSITION-Eingabe definiert werden.</span><span class="sxs-lookup"><span data-stu-id="9a766-245">Only one SCENE\_POSITION input can be defined.</span></span> <span data-ttu-id="9a766-246">Dieser Parameter sollte nur bei Bedarf eingeschlossen werden, da nur eine Funktion pro verknüpften Shader diesen Parameter verwenden kann.</span><span class="sxs-lookup"><span data-stu-id="9a766-246">This parameter should only be included when necessary, since only one function per linked shader can utilize this parameter.</span></span>

<span data-ttu-id="9a766-247">Die Semantik muss wie oben definiert werden, da D2D die Semantik untersucht, um zu entscheiden, wie Funktionen miteinander verknüpft werden sollen.</span><span class="sxs-lookup"><span data-stu-id="9a766-247">The semantics must be defined as above, as D2D will inspect the semantics to decide how to link functions together.</span></span> <span data-ttu-id="9a766-248">Wenn eine Funktionseingabe nicht mit einem der oben genannten Typen übereinstimmt, wird die Funktion für die Shaderverknüpfung abgelehnt.</span><span class="sxs-lookup"><span data-stu-id="9a766-248">If any function input does not match one of the above types, the function will be rejected for shader linking.</span></span>

## <a name="related-topics"></a><span data-ttu-id="9a766-249">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="9a766-249">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="9a766-250">HLSL-Hilfatoren</span><span class="sxs-lookup"><span data-stu-id="9a766-250">HLSL Helpers</span></span>](hlsl-helpers.md)
</dt> <dt>

[<span data-ttu-id="9a766-251">ID3D11Linker-Schnittstelle</span><span class="sxs-lookup"><span data-stu-id="9a766-251">ID3D11Linker interface</span></span>](/windows/desktop/api/d3d11shader/nn-d3d11shader-id3d11linker)
</dt> <dt>

[<span data-ttu-id="9a766-252">ID3D11FunctionLinkingGraph-Schnittstelle</span><span class="sxs-lookup"><span data-stu-id="9a766-252">ID3D11FunctionLinkingGraph interface</span></span>](/windows/desktop/api/d3d11shader/nn-d3d11shader-id3d11functionlinkinggraph)
</dt> </dl>

 

 