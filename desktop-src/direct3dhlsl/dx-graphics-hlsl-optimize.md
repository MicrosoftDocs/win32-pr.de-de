---
title: Optimieren von HLSL-Shadern
description: In diesem Abschnitt werden allgemeine Strategien beschrieben, mit denen Sie Ihre Shader optimieren können. Diese Strategien können auf Shader angewendet werden, die in einer beliebigen Sprache auf einer beliebigen Plattform geschrieben sind.
ms.assetid: 014b9cb3-a489-48d7-8174-b97de168bf3a
keywords:
- High-Level-Shader-Sprache
- HLSL, Leistung
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 06d3bb806e98e489020aa1755ef2a6c952459d86
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "104037350"
---
# <a name="optimizing-hlsl-shaders"></a><span data-ttu-id="6d160-106">Optimieren von HLSL-Shadern</span><span class="sxs-lookup"><span data-stu-id="6d160-106">Optimizing HLSL Shaders</span></span>

<span data-ttu-id="6d160-107">In diesem Abschnitt werden allgemeine Strategien beschrieben, mit denen Sie Ihre Shader optimieren können.</span><span class="sxs-lookup"><span data-stu-id="6d160-107">This section describes general-purpose strategies that you can use to optimize your shaders.</span></span> <span data-ttu-id="6d160-108">Diese Strategien können auf Shader angewendet werden, die in einer beliebigen Sprache auf einer beliebigen Plattform geschrieben sind.</span><span class="sxs-lookup"><span data-stu-id="6d160-108">You can apply these strategies to shaders that are written in any language, on any platform.</span></span>

-   [<span data-ttu-id="6d160-109">Informationen zum Ausführen von shaderberechnungen</span><span class="sxs-lookup"><span data-stu-id="6d160-109">Know Where To Perform Shader Calculations</span></span>](#know-where-to-perform-shader-calculations)
-   [<span data-ttu-id="6d160-110">Unnötige Anweisungen überspringen</span><span class="sxs-lookup"><span data-stu-id="6d160-110">Skip Unnecessary Instructions</span></span>](#skip-unnecessary-instructions)
-   [<span data-ttu-id="6d160-111">Paket Variablen und interpolanten</span><span class="sxs-lookup"><span data-stu-id="6d160-111">Pack Variables and Interpolants</span></span>](#pack-variables-and-interpolants)
-   [<span data-ttu-id="6d160-112">Reduzieren der Shader-Komplexität</span><span class="sxs-lookup"><span data-stu-id="6d160-112">Reduce Shader Complexity</span></span>](#reduce-shader-complexity)
-   [<span data-ttu-id="6d160-113">Verwandte Themen</span><span class="sxs-lookup"><span data-stu-id="6d160-113">Related Topics</span></span>](#related-topics)
-   [<span data-ttu-id="6d160-114">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="6d160-114">Related topics</span></span>](#related-topics)

## <a name="know-where-to-perform-shader-calculations"></a><span data-ttu-id="6d160-115">Informationen zum Ausführen von shaderberechnungen</span><span class="sxs-lookup"><span data-stu-id="6d160-115">Know Where To Perform Shader Calculations</span></span>

<span data-ttu-id="6d160-116">Vertexshader führen Vorgänge aus, die das Abrufen von Scheitel Punkten und das Durchführen einer Matrix Transformation für Scheitelpunkt Daten einschließen.</span><span class="sxs-lookup"><span data-stu-id="6d160-116">Vertex shaders perform operations that include fetching vertices and performing matrix transformation of vertex data.</span></span> <span data-ttu-id="6d160-117">Normalerweise werden Vertex-Shader einmal pro Scheitelpunkt ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="6d160-117">Typically, vertex shaders are executed once per vertex.</span></span>

<span data-ttu-id="6d160-118">Pixel-Shader führen Vorgänge aus, die das Abrufen von Textur Daten und das Durchführen von Beleuchtungsberechnungen einschließen.</span><span class="sxs-lookup"><span data-stu-id="6d160-118">Pixel Shaders perform operations that include fetching texture data and performing lighting calculations.</span></span> <span data-ttu-id="6d160-119">In der Regel werden Pixel-Shader für einen bestimmten Teil der Geometrie einmal pro Pixel ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="6d160-119">Typically, pixel shaders are executed once per pixel for a given piece of geometry.</span></span>

<span data-ttu-id="6d160-120">In der Regel werden Pixel-Ausrichtungs Scheitel Punkte in einer Szene angezeigt, sodass Pixel-Shader häufiger als Vertex-Shader ausgeführt werden.</span><span class="sxs-lookup"><span data-stu-id="6d160-120">Typically, pixels outnumber vertices in a scene, so pixel shaders execute more often than vertex shaders.</span></span>

<span data-ttu-id="6d160-121">Beachten Sie beim Entwerfen von shaderalgorithmen Folgendes:</span><span class="sxs-lookup"><span data-stu-id="6d160-121">When you design shader algorithms, keep the following in mind:</span></span>

-   <span data-ttu-id="6d160-122">Ausführen von Berechnungen für den Vertex-Shader, wenn möglich.</span><span class="sxs-lookup"><span data-stu-id="6d160-122">Perform calculations on the vertex shader if possible.</span></span> <span data-ttu-id="6d160-123">Eine Berechnung, die für einen PixelShader ausgeführt wird, ist wesentlich teurer als eine Berechnung, die für einen Scheitelpunkt-Shader ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="6d160-123">A calculation that is performed on a pixel shader is much more expensive than a calculation that is performed on a vertex shader.</span></span>
-   <span data-ttu-id="6d160-124">Verwenden Sie ggf. nach Scheitelpunkt Berechnungen, um die Leistung in Situationen wie dichten Netzen zu verbessern.</span><span class="sxs-lookup"><span data-stu-id="6d160-124">Consider using per-vertex calculations to improve performance in situations such as dense meshes.</span></span> <span data-ttu-id="6d160-125">Bei dichten Netzen können pro-Vertex-Berechnungen Ergebnisse erzeugen, die sich visuell nicht von den Ergebnissen unterscheiden, die mit pro Pixel-Berechnungen erzeugt wurden.</span><span class="sxs-lookup"><span data-stu-id="6d160-125">For dense meshes, per-vertex calculations may produce results that are visually indistinguishable from results produced with per-pixel calculations.</span></span>

## <a name="skip-unnecessary-instructions"></a><span data-ttu-id="6d160-126">Unnötige Anweisungen überspringen</span><span class="sxs-lookup"><span data-stu-id="6d160-126">Skip Unnecessary Instructions</span></span>

<span data-ttu-id="6d160-127">In HLSL bietet dynamische Verzweigung die Möglichkeit, die Anzahl der ausgeführten Anweisungen einzuschränken.</span><span class="sxs-lookup"><span data-stu-id="6d160-127">In HLSL, dynamic branching provides the ability to limit the number of instructions that are executed.</span></span> <span data-ttu-id="6d160-128">Daher kann die dynamische Verzweigung helfen, die shaderausführungszeit zu beschleunigen.</span><span class="sxs-lookup"><span data-stu-id="6d160-128">Therefore, dynamic branching can help speed up shader execution time.</span></span> <span data-ttu-id="6d160-129">Wenn Geometrie oder Pixel nicht angezeigt werden, verwenden Sie dynamische Verzweigungen, um den Shader zu beenden oder um Anweisungen einzuschränken.</span><span class="sxs-lookup"><span data-stu-id="6d160-129">If geometry or pixels are not displayed, use dynamic branching to exit the shader or to limit instructions.</span></span> <span data-ttu-id="6d160-130">Wenn z. b. ein Pixel nicht beleuchtet wird, gibt es keinen Punkt, an dem der Beleuchtungs Algorithmus ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="6d160-130">For example, if a pixel is not lit, there is no point in executing the lighting algorithm.</span></span>

<span data-ttu-id="6d160-131">In der folgenden Tabelle sind einige Fälle aufgeführt, in denen Sie Bedingungen im Shader testen und dynamische Verzweigungen verwenden können, um unnötige Anweisungen zu überspringen.</span><span class="sxs-lookup"><span data-stu-id="6d160-131">The following table lists some cases where you can test conditions in your shader and use dynamic branching to skip unnecessary instructions.</span></span> <span data-ttu-id="6d160-132">Die Tabelle ist nicht vollständig.</span><span class="sxs-lookup"><span data-stu-id="6d160-132">The table not comprehensive.</span></span> <span data-ttu-id="6d160-133">Vielmehr soll Sie Ihnen Ideen zur Optimierung Ihres Codes vermitteln.</span><span class="sxs-lookup"><span data-stu-id="6d160-133">Rather, it is intended to give you ideas for optimizing your code.</span></span>



| <span data-ttu-id="6d160-134">Zu überprüfen Bedingung</span><span class="sxs-lookup"><span data-stu-id="6d160-134">Condition to Check</span></span>                                    | <span data-ttu-id="6d160-135">Antwort im Shader</span><span class="sxs-lookup"><span data-stu-id="6d160-135">Response in the Shader</span></span>       |
|-------------------------------------------------------|------------------------------|
| <span data-ttu-id="6d160-136">Bei der Alpha Überprüfung wird festgelegt, dass ein Pixel nicht angezeigt wird.</span><span class="sxs-lookup"><span data-stu-id="6d160-136">Alpha check determines that a pixel will not be seen.</span></span> | <span data-ttu-id="6d160-137">Überspringen Sie den Rest des Shader.</span><span class="sxs-lookup"><span data-stu-id="6d160-137">Skip the rest of the shader.</span></span> |
| <span data-ttu-id="6d160-138">Das Pixel oder die Geometrie ist vollständig verstopft.</span><span class="sxs-lookup"><span data-stu-id="6d160-138">The pixel or geometry is fully fogged.</span></span>                | <span data-ttu-id="6d160-139">Überspringen Sie den Rest des Shader.</span><span class="sxs-lookup"><span data-stu-id="6d160-139">Skip the rest of the shader.</span></span> |
| <span data-ttu-id="6d160-140">Die Skin-Gewichtungen sind NULL.</span><span class="sxs-lookup"><span data-stu-id="6d160-140">Skin weights are zero.</span></span>                                | <span data-ttu-id="6d160-141">Überspringen von Knochen.</span><span class="sxs-lookup"><span data-stu-id="6d160-141">Skip bones.</span></span>                  |
| <span data-ttu-id="6d160-142">Die leichte Dämpfung ist 0 (null).</span><span class="sxs-lookup"><span data-stu-id="6d160-142">Light attenuation is zero.</span></span>                            | <span data-ttu-id="6d160-143">Beleuchtung überspringen.</span><span class="sxs-lookup"><span data-stu-id="6d160-143">Skip lighting.</span></span>               |
| <span data-ttu-id="6d160-144">Nicht positiver lambertian-Begriff.</span><span class="sxs-lookup"><span data-stu-id="6d160-144">Non-positive Lambertian term.</span></span>                         | <span data-ttu-id="6d160-145">Beleuchtung überspringen.</span><span class="sxs-lookup"><span data-stu-id="6d160-145">Skip lighting.</span></span>               |



 

## <a name="pack-variables-and-interpolants"></a><span data-ttu-id="6d160-146">Paket Variablen und interpolanten</span><span class="sxs-lookup"><span data-stu-id="6d160-146">Pack Variables and Interpolants</span></span>

<span data-ttu-id="6d160-147">Berücksichtigen Sie den für Shader-Daten erforderlichen Speicherplatz.</span><span class="sxs-lookup"><span data-stu-id="6d160-147">Be mindful of the space required for shader data.</span></span> <span data-ttu-id="6d160-148">Verpacken Sie so viele Informationen wie möglich in eine Variable oder interpolant.</span><span class="sxs-lookup"><span data-stu-id="6d160-148">Pack as much information into a variable or interpolant as possible.</span></span> <span data-ttu-id="6d160-149">Manchmal können die Informationen aus zwei Variablen in den Speicherbereich einer einzelnen Variablen gepackt werden.</span><span class="sxs-lookup"><span data-stu-id="6d160-149">Sometimes, the information from two variables can be packed into the memory space of a single variable.</span></span>

## <a name="reduce-shader-complexity"></a><span data-ttu-id="6d160-150">Reduzieren der Shader-Komplexität</span><span class="sxs-lookup"><span data-stu-id="6d160-150">Reduce Shader Complexity</span></span>

<span data-ttu-id="6d160-151">Halten Sie Ihre Shader klein und einfach.</span><span class="sxs-lookup"><span data-stu-id="6d160-151">Keep your shaders small and simple.</span></span> <span data-ttu-id="6d160-152">Im Allgemeinen werden Shader mit weniger Anweisungen schneller ausgeführt als Shader mit weiteren Anweisungen.</span><span class="sxs-lookup"><span data-stu-id="6d160-152">In general, shaders with fewer instructions execute more quickly than shaders with more instructions.</span></span> <span data-ttu-id="6d160-153">Es ist auch einfacher, kleinere, weniger komplexe Shader zu Debuggen und zu optimieren.</span><span class="sxs-lookup"><span data-stu-id="6d160-153">It is also easier to debug and optimize smaller, less complex shaders.</span></span>

## <a name="related-topics"></a><span data-ttu-id="6d160-154">Verwandte Themen</span><span class="sxs-lookup"><span data-stu-id="6d160-154">Related Topics</span></span>

[<span data-ttu-id="6d160-155">Programmieranleitung für HLSL</span><span class="sxs-lookup"><span data-stu-id="6d160-155">Programming Guide for HLSL</span></span>](dx-graphics-hlsl-pguide.md)


## <a name="related-topics"></a><span data-ttu-id="6d160-156">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="6d160-156">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="6d160-157">Programmieranleitung für HLSL</span><span class="sxs-lookup"><span data-stu-id="6d160-157">Programming Guide for HLSL</span></span>](dx-graphics-hlsl-pguide.md)
</dt> </dl>

 

 




