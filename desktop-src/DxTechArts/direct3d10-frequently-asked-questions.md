---
title: Häufig gestellte Fragen zu Direct3D 10
description: Dieser Artikel enthält einige häufig gestellte Fragen im Zusammenhang mit Direct3D 10 aus der Sicht eines Entwicklers, der eine vorhandene Anwendung von Direct3D 9 (d3d9) auf Direct3D 10 (d3d10) portieren soll.
ms.assetid: da3022ca-b120-d0d7-6747-65b946dbc73c
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7aae228923715400e5ba7e4f795e3ea6bfacfd98
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "104101898"
---
# <a name="direct3d-10-frequently-asked-questions"></a><span data-ttu-id="37f92-103">Häufig gestellte Fragen zu Direct3D 10</span><span class="sxs-lookup"><span data-stu-id="37f92-103">Direct3D 10 Frequently Asked Questions</span></span>

<span data-ttu-id="37f92-104">Dieser Artikel enthält einige häufig gestellte Fragen im Zusammenhang mit Direct3D 10 aus der Sicht eines Entwicklers, der eine vorhandene Anwendung von Direct3D 9 (d3d9) auf Direct3D 10 (d3d10) portieren soll.</span><span class="sxs-lookup"><span data-stu-id="37f92-104">This article contains some of the frequently asked questions surrounding Direct3D 10 from the point of view of a developer who is porting an existing application from Direct3D 9 (D3D9) to Direct3D 10 (D3D10).</span></span>

-   [<span data-ttu-id="37f92-105">Konstantenpuffer</span><span class="sxs-lookup"><span data-stu-id="37f92-105">Constant Buffers</span></span>](#constant-buffers)
-   [<span data-ttu-id="37f92-106">State</span><span class="sxs-lookup"><span data-stu-id="37f92-106">State</span></span>](#state)
-   [<span data-ttu-id="37f92-107">Formate</span><span class="sxs-lookup"><span data-stu-id="37f92-107">Formats</span></span>](#formats)
-   [<span data-ttu-id="37f92-108">Shaderverknüpfung</span><span class="sxs-lookup"><span data-stu-id="37f92-108">Shader Linkage</span></span>](#shader-linkage)
-   [<span data-ttu-id="37f92-109">Draw-Aufrufe</span><span class="sxs-lookup"><span data-stu-id="37f92-109">Draw Calls</span></span>](#draw-calls)
-   [<span data-ttu-id="37f92-110">Ressourcen</span><span class="sxs-lookup"><span data-stu-id="37f92-110">Resources</span></span>](#resources)
-   [<span data-ttu-id="37f92-111">Tiefe als Textur</span><span class="sxs-lookup"><span data-stu-id="37f92-111">Depth as Texture</span></span>](#depth-as-texture)
-   [<span data-ttu-id="37f92-112">MSAA</span><span class="sxs-lookup"><span data-stu-id="37f92-112">MSAA</span></span>](#msaa)
-   [<span data-ttu-id="37f92-113">Abstürze</span><span class="sxs-lookup"><span data-stu-id="37f92-113">Crashes</span></span>](#crashes)
-   [<span data-ttu-id="37f92-114">Prädikat Rendering</span><span class="sxs-lookup"><span data-stu-id="37f92-114">Predicated Rendering</span></span>](#predicated-rendering)
-   [<span data-ttu-id="37f92-115">Geometrie-Shader</span><span class="sxs-lookup"><span data-stu-id="37f92-115">Geometry Shader</span></span>](#geometry-shader)
-   [<span data-ttu-id="37f92-116">HLSL</span><span class="sxs-lookup"><span data-stu-id="37f92-116">HLSL</span></span>](#hlsl)

## <a name="constant-buffers"></a><span data-ttu-id="37f92-117">Konstantenpuffer</span><span class="sxs-lookup"><span data-stu-id="37f92-117">Constant Buffers</span></span>

<dl> <dt>

<span data-ttu-id="37f92-118"><span id="What_is_the_best_way_to_update_constant_buffers_"></span><span id="what_is_the_best_way_to_update_constant_buffers_"></span><span id="WHAT_IS_THE_BEST_WAY_TO_UPDATE_CONSTANT_BUFFERS_"></span>Was ist die beste Möglichkeit, Konstante Puffer zu aktualisieren?</span><span class="sxs-lookup"><span data-stu-id="37f92-118"><span id="What_is_the_best_way_to_update_constant_buffers_"></span><span id="what_is_the_best_way_to_update_constant_buffers_"></span><span id="WHAT_IS_THE_BEST_WAY_TO_UPDATE_CONSTANT_BUFFERS_"></span>What is the best way to update constant buffers?</span></span>
</dt> <dd>

<span data-ttu-id="37f92-119">Updatesubresource und die Zuordnung mit verwerfen sollten ungefähr dieselbe Geschwindigkeit aufweisen.</span><span class="sxs-lookup"><span data-stu-id="37f92-119">UpdateSubresource and Map with Discard should be about the same speed.</span></span> <span data-ttu-id="37f92-120">Wählen Sie zwischen diesen aus, je nachdem, welche Speichermenge den geringsten Speicherplatz kopiert.</span><span class="sxs-lookup"><span data-stu-id="37f92-120">Choose between them depending on which one copies the least amount of memory.</span></span> <span data-ttu-id="37f92-121">Wenn Ihre Daten bereits in einem zusammenhängenden Block im Speicher gespeichert sind, verwenden Sie updatesubresource.</span><span class="sxs-lookup"><span data-stu-id="37f92-121">If you already have your data stored in memory in one contiguous block, use UpdateSubresource.</span></span> <span data-ttu-id="37f92-122">Wenn Sie Daten von anderen Orten sammeln müssen, verwenden Sie Map mit verwerfen.</span><span class="sxs-lookup"><span data-stu-id="37f92-122">If you need to accumulate data from other places, use Map with Discard.</span></span>

</dd> <dt>

<span data-ttu-id="37f92-123"><span id="What_is_the_worst_way_to_organize_constant_buffers_"></span><span id="what_is_the_worst_way_to_organize_constant_buffers_"></span><span id="WHAT_IS_THE_WORST_WAY_TO_ORGANIZE_CONSTANT_BUFFERS_"></span>Was ist die schlechteste Methode zum Organisieren konstanter Puffer?</span><span class="sxs-lookup"><span data-stu-id="37f92-123"><span id="What_is_the_worst_way_to_organize_constant_buffers_"></span><span id="what_is_the_worst_way_to_organize_constant_buffers_"></span><span id="WHAT_IS_THE_WORST_WAY_TO_ORGANIZE_CONSTANT_BUFFERS_"></span>What is the worst way to organize constant buffers?</span></span>
</dt> <dd>

<span data-ttu-id="37f92-124">Die schlechteste Leistung wird erzielt, indem alle Konstanten für einen bestimmten Shader in einen konstanten Puffer versetzt werden.</span><span class="sxs-lookup"><span data-stu-id="37f92-124">The worst performance is realized by putting all constants for a particular shader into one constant buffer.</span></span> <span data-ttu-id="37f92-125">Dies ist oft die einfachste Möglichkeit, von d3d9 zu d3d10 zu portieren. Dies kann jedoch die Leistung beeinträchtigen.</span><span class="sxs-lookup"><span data-stu-id="37f92-125">While this often is the easiest way to port from D3D9 to D3D10, it can cripple performance.</span></span> <span data-ttu-id="37f92-126">Stellen Sie sich beispielsweise ein Szenario vor, in dem der folgende Konstante Puffer verwendet wird:</span><span class="sxs-lookup"><span data-stu-id="37f92-126">For example, consider a scenario that uses the following constant buffer:</span></span>

``` syntax
cbuffer VSGlobalsCB
{
    matrix  ViewProj;
    matrix  Bones[100];
    matrix  World;
    float   SpecPower;
    float4  BDRFCoefficients;
    float   AppTime;
    uint2   RenderTargetSize;
};
```

<span data-ttu-id="37f92-127">Der Puffer ist 6560 bytes.</span><span class="sxs-lookup"><span data-stu-id="37f92-127">The buffer is 6560 bytes.</span></span> <span data-ttu-id="37f92-128">Angenommen, es gibt eine Anwendung mit 1000-Objekten, die gerendert werden sollen, 100 von den gehäuchten Meshes und 900, bei denen es sich um statische Netze handelt.</span><span class="sxs-lookup"><span data-stu-id="37f92-128">Assume there is an application with 1000 objects to be rendered, 100 of which are skinned meshes, and 900 of which are static meshes.</span></span> <span data-ttu-id="37f92-129">Nehmen Sie außerdem an, dass diese Anwendung eine Schatten Zuordnung mit einer Lichtquelle verwendet.</span><span class="sxs-lookup"><span data-stu-id="37f92-129">Also, assume that this application is using shadow mapping with one light source.</span></span> <span data-ttu-id="37f92-130">Dies bedeutet, dass es zwei Durchgänge gibt, eine für die Tiefe, die vom Licht gerendert wird, und eine für den Forward-Renderingdurchlauf.</span><span class="sxs-lookup"><span data-stu-id="37f92-130">This means there are two passes, one for the depth map rendered from the light, and one for the forward rendering pass.</span></span> <span data-ttu-id="37f92-131">Dies führt zu 2000 Draw-aufrufen.</span><span class="sxs-lookup"><span data-stu-id="37f92-131">This results in 2000 draw calls.</span></span> <span data-ttu-id="37f92-132">Obwohl jeder zeichnen-Befehl nicht jeden Teil des Konstanten Puffers aktualisieren muss, wird der gesamte Konstante Puffer weiterhin aktualisiert und an die Karte gesendet.</span><span class="sxs-lookup"><span data-stu-id="37f92-132">Although each draw call does not NEED to update every part of the constant buffer, the entire constant buffer still is updated and sent to the card.</span></span> <span data-ttu-id="37f92-133">Dies führt zu einem Update von 13 MB Daten jedes Frames (2000 Draw-Aufrufe, 6560 KB).</span><span class="sxs-lookup"><span data-stu-id="37f92-133">This results in the update of 13 MB of data every frame (2000 draw calls times 6560 KB).</span></span>

</dd> <dt>

<span data-ttu-id="37f92-134"><span id="What_is_the_best_way_to_organize_my_constant_buffers_"></span><span id="what_is_the_best_way_to_organize_my_constant_buffers_"></span><span id="WHAT_IS_THE_BEST_WAY_TO_ORGANIZE_MY_CONSTANT_BUFFERS_"></span>Was ist die beste Möglichkeit, meine Konstanten Puffer zu organisieren?</span><span class="sxs-lookup"><span data-stu-id="37f92-134"><span id="What_is_the_best_way_to_organize_my_constant_buffers_"></span><span id="what_is_the_best_way_to_organize_my_constant_buffers_"></span><span id="WHAT_IS_THE_BEST_WAY_TO_ORGANIZE_MY_CONSTANT_BUFFERS_"></span>What is the best way to organize my constant buffers?</span></span>
</dt> <dd>

<span data-ttu-id="37f92-135">Die beste Möglichkeit besteht darin, Konstante Puffer nach Aktualisierungshäufigkeit zu organisieren.</span><span class="sxs-lookup"><span data-stu-id="37f92-135">The best way is to organize constant buffers by frequency of update.</span></span> <span data-ttu-id="37f92-136">Konstanten, die bei ähnlichen Frequenzen aktualisiert werden, müssen sich im gleichen Puffer befinden.</span><span class="sxs-lookup"><span data-stu-id="37f92-136">Constants that are updated at similar frequencies should be in the same buffer.</span></span> <span data-ttu-id="37f92-137">Sehen Sie sich beispielsweise das Szenario an: "Was ist die schlechteste Methode zum Organisieren konstanter Puffer?", aber mit einem besseren Konstanten Layout:</span><span class="sxs-lookup"><span data-stu-id="37f92-137">For example, consider the scenario presented under, "What is the worst way to organize constant buffers?," but with a better constant layout:</span></span>

``` syntax
cbuffer VSGlobalPerFrameCB
  { 
    float   AppTime; 
  };
cbuffer VSPerSkinnedCB
  { 
    matrix  Bones[100]; 
  };
cbuffer VSPerStaticCB
  {
    matrix  World;
  };
cbuffer VSPerPassCB
  {
    matrix  ViewProj;
    uint2   RenderTargetSize;
  };
cbuffer VSPerMaterialCB
  {
    float   SpecPower;
    float4  BDRFCoefficients;
  };    
```

<span data-ttu-id="37f92-138">Konstante Puffer werden nach ihrer Aktualisierungshäufigkeit aufgeteilt, aber dies ist nur die Hälfte der Lösung.</span><span class="sxs-lookup"><span data-stu-id="37f92-138">Constant buffers are split by their update frequency, but this only is half of the solution.</span></span> <span data-ttu-id="37f92-139">Die Anwendung muss die Konstanten Puffer ordnungsgemäß aktualisieren, um die Aufteilung in vollem Umfang zu nutzen.</span><span class="sxs-lookup"><span data-stu-id="37f92-139">The application needs to update the constant buffers correctly in order to take full advantage of the split.</span></span> <span data-ttu-id="37f92-140">Wir gehen von der gleichen Szene aus wie oben beschrieben: 900 statische Meshes, 100 häutige Meshes, ein heller Durchlauf und ein vorwärts Durchlauf.</span><span class="sxs-lookup"><span data-stu-id="37f92-140">We will assume the same scene as above: 900 static meshes, 100 skinned meshes, one light pass, and one forward pass.</span></span> <span data-ttu-id="37f92-141">Außerdem wird davon ausgegangen, dass einige Konstante Puffer pro Objekt gespeichert werden.</span><span class="sxs-lookup"><span data-stu-id="37f92-141">We also will assume that some constant buffers per-object will be stored.</span></span> <span data-ttu-id="37f92-142">Dies bedeutet, dass jedes Objekt entweder ein vsperskinnedcb oder ein vsperstaticcb enthält, je nachdem, ob es ein-oder statisch ist.</span><span class="sxs-lookup"><span data-stu-id="37f92-142">This means that each object will contain either a VSPerSkinnedCB or a VSPerStaticCB, depending on whether or not it is skinned or static.</span></span> <span data-ttu-id="37f92-143">Dies geschieht, um zu vermeiden, dass die Anzahl der Matrizen, die über die Pipeline gesendet werden, verdoppelt wird.</span><span class="sxs-lookup"><span data-stu-id="37f92-143">We do this in order to avoid doubling the amount of matrices sent through the pipeline.</span></span>

<span data-ttu-id="37f92-144">Der Frame wird in drei Phasen aufgeteilt.</span><span class="sxs-lookup"><span data-stu-id="37f92-144">We split the frame into three phases.</span></span> <span data-ttu-id="37f92-145">Die erste Phase ist der Anfang des Frames und umfasst kein Rendering, sondern nur konstante Updates.</span><span class="sxs-lookup"><span data-stu-id="37f92-145">The first phase is the beginning of the frame and involves no rendering, just constant updates.</span></span>

<dl> <dt>

<span data-ttu-id="37f92-146"><span id="Begin_Frame"></span><span id="begin_frame"></span><span id="BEGIN_FRAME"></span>**Anfangs Rahmen**</span><span class="sxs-lookup"><span data-stu-id="37f92-146"><span id="Begin_Frame"></span><span id="begin_frame"></span><span id="BEGIN_FRAME"></span>**Begin Frame**</span></span>
</dt> <dd>

-   <span data-ttu-id="37f92-147">Aktualisieren von vsglobalperframecb für die Anwendungszeit (4 Bytes)</span><span class="sxs-lookup"><span data-stu-id="37f92-147">Update VSGlobalPerFrameCB for application time (4 bytes)</span></span>
-   <span data-ttu-id="37f92-148">Update 100 vsperskinnedcb für die 100 häutigen Objekte (640000 Bytes)</span><span class="sxs-lookup"><span data-stu-id="37f92-148">Update 100 VSPerSkinnedCB for the 100 skinned objects (640000 bytes)</span></span>
-   <span data-ttu-id="37f92-149">Vsperstaticcb für 900 statische Objekte aktualisieren (57600 Bytes)</span><span class="sxs-lookup"><span data-stu-id="37f92-149">Update VSPerStaticCB for 900 static objects (57600 bytes)</span></span>

<span data-ttu-id="37f92-150">Der nächste Schritt ist die schattenkarten Übergabe.</span><span class="sxs-lookup"><span data-stu-id="37f92-150">Next is the shadow map pass.</span></span> <span data-ttu-id="37f92-151">Beachten Sie, dass der einzige Konstante Puffer, der tatsächlich aktualisiert wird, vsperpasscb ist.</span><span class="sxs-lookup"><span data-stu-id="37f92-151">Notice that the only constant buffer that actually updates is VSPerPassCB.</span></span> <span data-ttu-id="37f92-152">Alle anderen Konstanten Puffer wurden während der Übergabe des Frame Rahmens aktualisiert.</span><span class="sxs-lookup"><span data-stu-id="37f92-152">All other constant buffers were updated during the begin frame pass.</span></span> <span data-ttu-id="37f92-153">Obwohl wir diese Konstanten Puffer immer noch binden müssen, ist die an die Grafikkarte weiter gegebene Informationsmenge minimal, da die Puffer bereits aktualisiert wurden.</span><span class="sxs-lookup"><span data-stu-id="37f92-153">While we still need to bind these constant buffers, the amount of information passed to the video card is minimal, because the buffers already have been updated.</span></span>

</dd> <dt>

<span data-ttu-id="37f92-154"><span id="Shadow_Pass"></span><span id="shadow_pass"></span><span id="SHADOW_PASS"></span>**Schatten Durchlauf**</span><span class="sxs-lookup"><span data-stu-id="37f92-154"><span id="Shadow_Pass"></span><span id="shadow_pass"></span><span id="SHADOW_PASS"></span>**Shadow Pass**</span></span>
</dt> <dd>

-   <span data-ttu-id="37f92-155">Vsperpasscb aktualisieren (72 Bytes)</span><span class="sxs-lookup"><span data-stu-id="37f92-155">Update VSPerPassCB (72 bytes)</span></span>
-   <span data-ttu-id="37f92-156">Zeichnen Sie 100-Farb veräuchte Netze (100 Bindungen, keine Updates)</span><span class="sxs-lookup"><span data-stu-id="37f92-156">Draw 100 skinned meshes (100 binds, no updates)</span></span>
-   <span data-ttu-id="37f92-157">900 statische Netzen zeichnen (100 Bindungen, keine Updates)</span><span class="sxs-lookup"><span data-stu-id="37f92-157">Draw 900 static meshes (100 binds, no updates)</span></span>

<span data-ttu-id="37f92-158">Ebenso muss der Forward-Renderingdurchlauf nur die Daten pro Material aktualisieren, da Sie nicht pro Mesh gespeichert wurden.</span><span class="sxs-lookup"><span data-stu-id="37f92-158">Similarly, the forward rendering pass only needs to update per-material data, because it was not stored per-mesh.</span></span> <span data-ttu-id="37f92-159">Wenn wir davon ausgehen, dass 500 Materialien in der Szene verwendet werden:</span><span class="sxs-lookup"><span data-stu-id="37f92-159">If we assume that there are 500 materials in use in the scene:</span></span>

</dd> <dt>

<span data-ttu-id="37f92-160"><span id="Forward_Pass"></span><span id="forward_pass"></span><span id="FORWARD_PASS"></span>**Forward-Durchlauf**</span><span class="sxs-lookup"><span data-stu-id="37f92-160"><span id="Forward_Pass"></span><span id="forward_pass"></span><span id="FORWARD_PASS"></span>**Forward Pass**</span></span>
</dt> <dd>

-   <span data-ttu-id="37f92-161">Vsperpasscb aktualisieren (72 Bytes)</span><span class="sxs-lookup"><span data-stu-id="37f92-161">Update VSPerPassCB (72 bytes)</span></span>
-   <span data-ttu-id="37f92-162">Update 500 vspermaterialcbs (10000 Bytes)</span><span class="sxs-lookup"><span data-stu-id="37f92-162">Update 500 VSPerMaterialCBs (10000 bytes)</span></span>

<span data-ttu-id="37f92-163">Dies ergibt insgesamt nur 707 KB.</span><span class="sxs-lookup"><span data-stu-id="37f92-163">This results in a total of just 707 KB.</span></span> <span data-ttu-id="37f92-164">Obwohl es sich hierbei um ein sehr erfunantes Szenario handelt, wird veranschaulicht, wie sehr konstanter Aktualisierungs Aufwand durchsortieren von Konstanten nach Aktualisierungshäufigkeit reduziert werden kann.</span><span class="sxs-lookup"><span data-stu-id="37f92-164">Although this is a very contrived scenario, it illustrates just how much constant update overhead can be reduced by sorting constants by frequency of update.</span></span>

</dd> </dl> </dd> <dt>

<span data-ttu-id="37f92-165"><span id="What_if_I_do_not_have_enough_space_to_store_individual_constant_buffers_for_my_meshes__material__and_so_on___"></span><span id="what_if_i_do_not_have_enough_space_to_store_individual_constant_buffers_for_my_meshes__material__and_so_on___"></span><span id="WHAT_IF_I_DO_NOT_HAVE_ENOUGH_SPACE_TO_STORE_INDIVIDUAL_CONSTANT_BUFFERS_FOR_MY_MESHES__MATERIAL__AND_SO_ON___"></span>Was geschieht, wenn ich nicht genügend Speicherplatz zum Speichern einzelner konstanter Puffer für meine Netze, Materialien usw. habe?</span><span class="sxs-lookup"><span data-stu-id="37f92-165"><span id="What_if_I_do_not_have_enough_space_to_store_individual_constant_buffers_for_my_meshes__material__and_so_on___"></span><span id="what_if_i_do_not_have_enough_space_to_store_individual_constant_buffers_for_my_meshes__material__and_so_on___"></span><span id="WHAT_IF_I_DO_NOT_HAVE_ENOUGH_SPACE_TO_STORE_INDIVIDUAL_CONSTANT_BUFFERS_FOR_MY_MESHES__MATERIAL__AND_SO_ON___"></span>What if I do not have enough space to store individual constant buffers for my meshes, material, and so on?</span></span> 
</dt> <dd>

<span data-ttu-id="37f92-166">Sie können immer ein mehrstufige System konstanter Puffer verwenden.</span><span class="sxs-lookup"><span data-stu-id="37f92-166">You always can use a tiered system of constant buffers.</span></span> <span data-ttu-id="37f92-167">Erstellen Sie Konstante Puffer variabler Größe (16 Bytes, 32 Bytes, 64 Bytes usw.) bis zur größten Konstanten Puffergröße.</span><span class="sxs-lookup"><span data-stu-id="37f92-167">Create variable-sized constant buffers (16 bytes, 32 bytes, 64 bytes, and so on) up to the largest constant buffer size needed.</span></span> <span data-ttu-id="37f92-168">Wenn es an der Zeit ist, einen konstanten Puffer an einen Shader zu binden, wählen Sie den kleinsten Konstanten Puffer aus, der die vom Shader benötigten Daten enthalten kann.</span><span class="sxs-lookup"><span data-stu-id="37f92-168">When it is time to bind a constant buffer to a shader, select the smallest constant buffer that can hold the data needed by the shader.</span></span> <span data-ttu-id="37f92-169">Obwohl dieser Ansatz etwas weniger effizient ist, ist dies ein guter Zwischenschritt.</span><span class="sxs-lookup"><span data-stu-id="37f92-169">Although this approach is slightly less efficient, it is a good intermediate step.</span></span>

</dd> <dt>

<span data-ttu-id="37f92-170"><span id="I_am_sharing_constant_buffers_between_different_shaders._One_shader_may_use_all_of_the_constants__but_another_may_use_some_of_the_constants._What_is_the_best_way_to_update_these___"></span><span id="i_am_sharing_constant_buffers_between_different_shaders._one_shader_may_use_all_of_the_constants__but_another_may_use_some_of_the_constants._what_is_the_best_way_to_update_these___"></span><span id="I_AM_SHARING_CONSTANT_BUFFERS_BETWEEN_DIFFERENT_SHADERS._ONE_SHADER_MAY_USE_ALL_OF_THE_CONSTANTS__BUT_ANOTHER_MAY_USE_SOME_OF_THE_CONSTANTS._WHAT_IS_THE_BEST_WAY_TO_UPDATE_THESE___"></span>Ich gebe Konstante Puffer für verschiedene Shader frei.</span><span class="sxs-lookup"><span data-stu-id="37f92-170"><span id="I_am_sharing_constant_buffers_between_different_shaders._One_shader_may_use_all_of_the_constants__but_another_may_use_some_of_the_constants._What_is_the_best_way_to_update_these___"></span><span id="i_am_sharing_constant_buffers_between_different_shaders._one_shader_may_use_all_of_the_constants__but_another_may_use_some_of_the_constants._what_is_the_best_way_to_update_these___"></span><span id="I_AM_SHARING_CONSTANT_BUFFERS_BETWEEN_DIFFERENT_SHADERS._ONE_SHADER_MAY_USE_ALL_OF_THE_CONSTANTS__BUT_ANOTHER_MAY_USE_SOME_OF_THE_CONSTANTS._WHAT_IS_THE_BEST_WAY_TO_UPDATE_THESE___"></span>I am sharing constant buffers between different shaders.</span></span> <span data-ttu-id="37f92-171">Ein Shader verwendet möglicherweise alle Konstanten, aber eine andere kann einige der Konstanten verwenden.</span><span class="sxs-lookup"><span data-stu-id="37f92-171">One shader may use all of the constants, but another may use some of the constants.</span></span> <span data-ttu-id="37f92-172">Was ist die beste Möglichkeit, diese zu aktualisieren?</span><span class="sxs-lookup"><span data-stu-id="37f92-172">What is the best way to update these?</span></span> 
</dt> <dd>

<span data-ttu-id="37f92-173">Ein Ansatz besteht darin, den konstanten Puffer noch weiter aufzuteilen.</span><span class="sxs-lookup"><span data-stu-id="37f92-173">One approach is to split the constant buffer even further.</span></span> <span data-ttu-id="37f92-174">Es kommt jedoch zu einem Punkt, an dem zu viele Konstante Puffer gebunden sind.</span><span class="sxs-lookup"><span data-stu-id="37f92-174">However, there comes a point at which too many constant buffers are bound.</span></span> <span data-ttu-id="37f92-175">Verschieben Sie in diesem Fall die Konstanten, die von mehreren Shadern wahrscheinlich nicht verwendet werden, an das Ende des Konstanten Puffers.</span><span class="sxs-lookup"><span data-stu-id="37f92-175">In this case, move the constants that are likely to be unused by several shaders to the end of the constant buffer.</span></span> <span data-ttu-id="37f92-176">Wenn Sie die Variablen Daten aus dem Shader erhalten, verwenden Sie das d3d10 \_ SVF \_ used-Flag der d3d10 \_ Shader-Variablen, \_ \_ um zu bestimmen, ob die Variable verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="37f92-176">When getting the variable data from the shader, use the D3D10\_SVF\_USED flag from the D3D10\_SHADER\_VARIABLE\_DESC to determine if the variable is used.</span></span> <span data-ttu-id="37f92-177">Wenn Sie nicht verwendete Variablen am Ende des Konstanten Puffers platzieren, können Sie einen kleineren Puffer an den Shader binden, der diese Variablen nicht verwendet, wodurch die Update Kosten eingespart werden.</span><span class="sxs-lookup"><span data-stu-id="37f92-177">By placing unused variables at the end of the constant buffer, you can bind a smaller buffer to the shader that does not use these variables, thus saving the update cost.</span></span>

</dd> <dt>

<span data-ttu-id="37f92-178"><span id="How_much_can_I_improve_my_frame_rate_if_I_only_upload_my_character_s_bones_once_per_frame_instead_of_once_per_pass_draw___"></span><span id="how_much_can_i_improve_my_frame_rate_if_i_only_upload_my_character_s_bones_once_per_frame_instead_of_once_per_pass_draw___"></span><span id="HOW_MUCH_CAN_I_IMPROVE_MY_FRAME_RATE_IF_I_ONLY_UPLOAD_MY_CHARACTER_S_BONES_ONCE_PER_FRAME_INSTEAD_OF_ONCE_PER_PASS_DRAW___"></span>Wie viel kann ich meine Framerate verbessern, wenn ich meine Zeichen nur einmal pro Frame anstelle von einmal pro Durchlauf/zeichnen Auflade?</span><span class="sxs-lookup"><span data-stu-id="37f92-178"><span id="How_much_can_I_improve_my_frame_rate_if_I_only_upload_my_character_s_bones_once_per_frame_instead_of_once_per_pass_draw___"></span><span id="how_much_can_i_improve_my_frame_rate_if_i_only_upload_my_character_s_bones_once_per_frame_instead_of_once_per_pass_draw___"></span><span id="HOW_MUCH_CAN_I_IMPROVE_MY_FRAME_RATE_IF_I_ONLY_UPLOAD_MY_CHARACTER_S_BONES_ONCE_PER_FRAME_INSTEAD_OF_ONCE_PER_PASS_DRAW___"></span>How much can I improve my frame rate if I only upload my character's bones once per frame instead of once per pass/draw?</span></span> 
</dt> <dd>

<span data-ttu-id="37f92-179">Abhängig von der Menge redundanter Daten können Sie die Framerate zwischen 8 Prozent und 50 Prozent verbessern.</span><span class="sxs-lookup"><span data-stu-id="37f92-179">You can improve frame rate between 8 percent and 50 percent depending on the amount of redundant data.</span></span> <span data-ttu-id="37f92-180">Im schlimmsten Fall wird die Leistung nicht reduziert.</span><span class="sxs-lookup"><span data-stu-id="37f92-180">In the worst case, performance will not be reduced.</span></span>

</dd> <dt>

<span data-ttu-id="37f92-181"><span id="How_many_constant_buffers_should_I_have_bound_at_once__"></span><span id="how_many_constant_buffers_should_i_have_bound_at_once__"></span><span id="HOW_MANY_CONSTANT_BUFFERS_SHOULD_I_HAVE_BOUND_AT_ONCE__"></span>Wie viele Konstante Puffer sollte ich gleichzeitig gebunden haben?</span><span class="sxs-lookup"><span data-stu-id="37f92-181"><span id="How_many_constant_buffers_should_I_have_bound_at_once__"></span><span id="how_many_constant_buffers_should_i_have_bound_at_once__"></span><span id="HOW_MANY_CONSTANT_BUFFERS_SHOULD_I_HAVE_BOUND_AT_ONCE__"></span>How many constant buffers should I have bound at once?</span></span> 
</dt> <dd>

<span data-ttu-id="37f92-182">Binden Sie die Mindestanzahl von konstantenpuffern, die benötigt wird, um alle Ihre Daten in den Shader zu übernehmen.</span><span class="sxs-lookup"><span data-stu-id="37f92-182">Bind the minimum number of constant buffers it takes to get all of your data into the shader.</span></span> <span data-ttu-id="37f92-183">In einem realistischen Szenario ist fünf die empfohlene Anzahl der zu verwendenden Konstanten Puffer.</span><span class="sxs-lookup"><span data-stu-id="37f92-183">In a realistic scenario, five is the recommended number of constant buffers to use.</span></span> <span data-ttu-id="37f92-184">Durch die gemeinsame Verwendung konstanter Puffer zwischen Shader (die Bindung desselben CB an die vs und PS) kann auch die Leistung verbessert werden.</span><span class="sxs-lookup"><span data-stu-id="37f92-184">Sharing constant buffers between shaders (binding the same CB to the VS and PS) also can improve performance.</span></span>

</dd> <dt>

<span data-ttu-id="37f92-185"><span id="Is_there_a_cost_for_binding_constant_buffers_without_using_them__"></span><span id="is_there_a_cost_for_binding_constant_buffers_without_using_them__"></span><span id="IS_THERE_A_COST_FOR_BINDING_CONSTANT_BUFFERS_WITHOUT_USING_THEM__"></span>Gibt es Kosten für das Binden konstanter Puffer, ohne Sie zu verwenden?</span><span class="sxs-lookup"><span data-stu-id="37f92-185"><span id="Is_there_a_cost_for_binding_constant_buffers_without_using_them__"></span><span id="is_there_a_cost_for_binding_constant_buffers_without_using_them__"></span><span id="IS_THERE_A_COST_FOR_BINDING_CONSTANT_BUFFERS_WITHOUT_USING_THEM__"></span>Is there a cost for binding constant buffers without using them?</span></span> 
</dt> <dd>

<span data-ttu-id="37f92-186">Ja, wenn Sie den Puffer nicht verwenden möchten, sollten Sie vssetconsantbuffer oder pssetconstantbuffer nicht aufrufen.</span><span class="sxs-lookup"><span data-stu-id="37f92-186">Yes, if you are not actually going to use the buffer, then do not call VSSetConsantBuffer or PSSetConstantBuffer.</span></span> <span data-ttu-id="37f92-187">Dieser zusätzliche API-Aufwand kann im Verlauf mehrerer Draw-Aufrufe entstehen.</span><span class="sxs-lookup"><span data-stu-id="37f92-187">This extra API overhead can add up over the course of multiple draw calls.</span></span>

</dd> </dl>

## <a name="state"></a><span data-ttu-id="37f92-188">State</span><span class="sxs-lookup"><span data-stu-id="37f92-188">State</span></span>

<dl> <dt>

<span data-ttu-id="37f92-189"><span id="What_is_the_best_way_to_manage_state_in_D3D10___"></span><span id="what_is_the_best_way_to_manage_state_in_d3d10___"></span><span id="WHAT_IS_THE_BEST_WAY_TO_MANAGE_STATE_IN_D3D10___"></span>Was ist die beste Möglichkeit, den Status in d3d10 zu verwalten?</span><span class="sxs-lookup"><span data-stu-id="37f92-189"><span id="What_is_the_best_way_to_manage_state_in_D3D10___"></span><span id="what_is_the_best_way_to_manage_state_in_d3d10___"></span><span id="WHAT_IS_THE_BEST_WAY_TO_MANAGE_STATE_IN_D3D10___"></span>What is the best way to manage state in D3D10?</span></span> 
</dt> <dd>

<span data-ttu-id="37f92-190">Die beste Lösung besteht darin, den gesamten Zustand im Voraus zu kennen und die Zustands Objekte vorab zu erstellen.</span><span class="sxs-lookup"><span data-stu-id="37f92-190">The best solution is to know all of your state up front and to create the state objects up front.</span></span> <span data-ttu-id="37f92-191">Dies bedeutet, dass zum Zeitpunkt der Rendering die Zustands Bindung der einzige Vorgang ist, der ausgeführt werden muss.</span><span class="sxs-lookup"><span data-stu-id="37f92-191">This means that at render time, state binding is the only operation that needs to happen.</span></span> <span data-ttu-id="37f92-192">D3d10 filtert auch Duplikate.</span><span class="sxs-lookup"><span data-stu-id="37f92-192">D3D10 also filter outs duplicates.</span></span>

</dd> <dt>

<span data-ttu-id="37f92-193"><span id="My_game_has_dynamically_loaded_or_has_user-generated_content._I_cannot_load_all_of_my_state_objects_up_front._What_should_I_do___"></span><span id="my_game_has_dynamically_loaded_or_has_user-generated_content._i_cannot_load_all_of_my_state_objects_up_front._what_should_i_do___"></span><span id="MY_GAME_HAS_DYNAMICALLY_LOADED_OR_HAS_USER-GENERATED_CONTENT._I_CANNOT_LOAD_ALL_OF_MY_STATE_OBJECTS_UP_FRONT._WHAT_SHOULD_I_DO___"></span>Mein Spiel wurde dynamisch geladen oder verfügt über benutzergenerierten Inhalt.</span><span class="sxs-lookup"><span data-stu-id="37f92-193"><span id="My_game_has_dynamically_loaded_or_has_user-generated_content._I_cannot_load_all_of_my_state_objects_up_front._What_should_I_do___"></span><span id="my_game_has_dynamically_loaded_or_has_user-generated_content._i_cannot_load_all_of_my_state_objects_up_front._what_should_i_do___"></span><span id="MY_GAME_HAS_DYNAMICALLY_LOADED_OR_HAS_USER-GENERATED_CONTENT._I_CANNOT_LOAD_ALL_OF_MY_STATE_OBJECTS_UP_FRONT._WHAT_SHOULD_I_DO___"></span>My game has dynamically loaded or has user-generated content.</span></span> <span data-ttu-id="37f92-194">Ich kann nicht alle Zustands Objekte im Vordergrund laden.</span><span class="sxs-lookup"><span data-stu-id="37f92-194">I cannot load all of my state objects up front.</span></span> <span data-ttu-id="37f92-195">  Wie sollte ich vorgehen?</span><span class="sxs-lookup"><span data-stu-id="37f92-195">What should I do?</span></span> 
</dt> <dd>

<span data-ttu-id="37f92-196">Hier gibt es zwei Lösungen.</span><span class="sxs-lookup"><span data-stu-id="37f92-196">There are two solutions here.</span></span> <span data-ttu-id="37f92-197">Der erste besteht darin, direkt Zustands Objekte zu erstellen und d3d10 das Herausfiltern von Duplikaten zu ermöglichen.</span><span class="sxs-lookup"><span data-stu-id="37f92-197">The first is to just create state objects on the fly and to let D3D10 filter out duplicates.</span></span> <span data-ttu-id="37f92-198">Dies wird jedoch nicht für Szenarien mit vielen Zustands Objektänderungen pro Frame empfohlen.</span><span class="sxs-lookup"><span data-stu-id="37f92-198">This, however, is not recommended for scenarios with many state object changes per frame.</span></span> <span data-ttu-id="37f92-199">Eine bessere Lösung besteht darin, die Zustands Objekte selbst zu Hashen und nur dann ein Zustands Objekt zu erstellen, wenn ein Objekt, das den Anforderungen entspricht, nicht in der Hash Tabelle gefunden wird.</span><span class="sxs-lookup"><span data-stu-id="37f92-199">A better solution is to hash the state objects yourself and to create a state object only if one that fits the requirements is not found in the hash table.</span></span> <span data-ttu-id="37f92-200">Wenn eine benutzerdefinierte Hash Tabelle verwendet wird, kann eine Anwendung einen schnellen Hash basierend auf dem Anwendungsszenario auswählen, das speziell für diese Anwendung gilt.</span><span class="sxs-lookup"><span data-stu-id="37f92-200">The reasoning behind using a custom hash table is that an application can select a fast hash based upon the usage scenario particular to that application.</span></span> <span data-ttu-id="37f92-201">Wenn eine Anwendung z. b. nur rendertargetschreitemask im blendstate ändert und alle anderen Werte identisch ist, kann die Anwendung einen Hash aus rendertargetschreitemask anstelle der gesamten Struktur generieren.</span><span class="sxs-lookup"><span data-stu-id="37f92-201">For example, if an application only changes the rendertargetwritemask in the BlendState and keeps all other values the same, the application can generate a hash from the rendertargetwritemask instead of the entire structure.</span></span>

</dd> <dt>

<span data-ttu-id="37f92-202"><span id="AlphaTest_state_is_gone._Where_did_it_go___"></span><span id="alphatest_state_is_gone._where_did_it_go___"></span><span id="ALPHATEST_STATE_IS_GONE._WHERE_DID_IT_GO___"></span>Der Alpha-Atest Zustand ist nicht mehr vorhanden.</span><span class="sxs-lookup"><span data-stu-id="37f92-202"><span id="AlphaTest_state_is_gone._Where_did_it_go___"></span><span id="alphatest_state_is_gone._where_did_it_go___"></span><span id="ALPHATEST_STATE_IS_GONE._WHERE_DID_IT_GO___"></span>AlphaTest state is gone.</span></span> <span data-ttu-id="37f92-203">Wo war es?</span><span class="sxs-lookup"><span data-stu-id="37f92-203">Where did it go?</span></span> 
</dt> <dd>

<span data-ttu-id="37f92-204">Alpha Atest sollte jetzt im Shader Leistung aufweisen.</span><span class="sxs-lookup"><span data-stu-id="37f92-204">AlphaTest now should be performance in the shader.</span></span> <span data-ttu-id="37f92-205">Weitere Informationen finden Sie unter fixedfuncemu Sample.</span><span class="sxs-lookup"><span data-stu-id="37f92-205">See the FixedFuncEMU sample.</span></span>

</dd> <dt>

<span data-ttu-id="37f92-206"><span id="What_happened_to_user_clip_planes___"></span><span id="what_happened_to_user_clip_planes___"></span><span id="WHAT_HAPPENED_TO_USER_CLIP_PLANES___"></span>Was ist mit Benutzer Clip-Flächen passiert?</span><span class="sxs-lookup"><span data-stu-id="37f92-206"><span id="What_happened_to_user_clip_planes___"></span><span id="what_happened_to_user_clip_planes___"></span><span id="WHAT_HAPPENED_TO_USER_CLIP_PLANES___"></span>What happened to user clip planes?</span></span> 
</dt> <dd>

<span data-ttu-id="37f92-207">Benutzer Clip Flächen wurden in den Shader verschoben.</span><span class="sxs-lookup"><span data-stu-id="37f92-207">User clip planes have moved into the shader.</span></span> <span data-ttu-id="37f92-208">Hierfür gibt es zwei Möglichkeiten.</span><span class="sxs-lookup"><span data-stu-id="37f92-208">There are two ways to handle this.</span></span> <span data-ttu-id="37f92-209">Der erste Wert ist die Ausgabe \_ von SV clipdistance aus dem Vertex-Shader oder dem Geometry-Shader.</span><span class="sxs-lookup"><span data-stu-id="37f92-209">The first is to output SV\_ClipDistance from the vertex shader or the geometry shader.</span></span> <span data-ttu-id="37f92-210">Die andere Option ist die Verwendung von verwerfen im Pixelshader basierend auf einem Wert, der vom Vertex-Shader oder dem Geometry-Shader nach unten übermittelt wird.</span><span class="sxs-lookup"><span data-stu-id="37f92-210">The other option is to use discard in the pixel shader based upon some value passed down by the vertex shader or the geometry shader.</span></span> <span data-ttu-id="37f92-211">Experimentieren Sie mit beiden, um zu sehen, was für ihr bestimmtes Szenario schneller ist.</span><span class="sxs-lookup"><span data-stu-id="37f92-211">Experiment with both to see which is faster for your particular scenario.</span></span> <span data-ttu-id="37f92-212">Die Verwendung \_ von SV clipdistance könnte dazu führen, dass die Hardware eine Geometrie basierte clippingroutine verwendet, die dazu führen kann, dass Geometrie gebundene Draw-Aufrufe langsamer ausgeführt werden.</span><span class="sxs-lookup"><span data-stu-id="37f92-212">Using SV\_ClipDistance could cause the hardware to use a geometry-based clipping routine that may cause geometry bound draw calls to run slower.</span></span> <span data-ttu-id="37f92-213">Ebenso verlagert die Verwendung von verwerfen die Arbeit in den Pixelshader, was dazu führen kann, dass Pixel gebundene Draw-Aufrufe langsamer ausgeführt werden.</span><span class="sxs-lookup"><span data-stu-id="37f92-213">Likewise, using discard shifts the work to the pixel shader, which may cause pixel-bound draw calls to run slower.</span></span>

</dd> <dt>

<span data-ttu-id="37f92-214"><span id="Clears_do_not_respect_any_state_settings__such_as_my_scissor_rect_settings_in_my_Rasterizer_State.__"></span><span id="clears_do_not_respect_any_state_settings__such_as_my_scissor_rect_settings_in_my_rasterizer_state.__"></span><span id="CLEARS_DO_NOT_RESPECT_ANY_STATE_SETTINGS__SUCH_AS_MY_SCISSOR_RECT_SETTINGS_IN_MY_RASTERIZER_STATE.__"></span>Bei der Löschung werden keine Zustands Einstellungen berücksichtigt, wie z. b. die Einstellungen für den Scheren-Rect in My Rasterizer State.</span><span class="sxs-lookup"><span data-stu-id="37f92-214"><span id="Clears_do_not_respect_any_state_settings__such_as_my_scissor_rect_settings_in_my_Rasterizer_State.__"></span><span id="clears_do_not_respect_any_state_settings__such_as_my_scissor_rect_settings_in_my_rasterizer_state.__"></span><span id="CLEARS_DO_NOT_RESPECT_ANY_STATE_SETTINGS__SUCH_AS_MY_SCISSOR_RECT_SETTINGS_IN_MY_RASTERIZER_STATE.__"></span>Clears do not respect any state settings, such as my scissor rect settings in my Rasterizer State.</span></span> 
</dt> <dd>

<span data-ttu-id="37f92-215">Das Löschen wurde vom Pipeline Status getrennt.</span><span class="sxs-lookup"><span data-stu-id="37f92-215">Clears have been separated from the pipeline state.</span></span> <span data-ttu-id="37f92-216">Um das Verhalten von d3d9 zu erhalten, emulieren Sie die Löschung durch Zeichnen eines voll Bild Quad.</span><span class="sxs-lookup"><span data-stu-id="37f92-216">In order to get D3D9-style behavior, emulate clears by drawing a full-screen quad.</span></span>

</dd> <dt>

<span data-ttu-id="37f92-217"><span id="I_set_my_states_back_to_default_to_try_and_diagnose_a_rendering_error._Now_my_screen_just_shows_black__although_I_know_I_am_drawing_objects_onto_the_screen.__"></span><span id="i_set_my_states_back_to_default_to_try_and_diagnose_a_rendering_error._now_my_screen_just_shows_black__although_i_know_i_am_drawing_objects_onto_the_screen.__"></span><span id="I_SET_MY_STATES_BACK_TO_DEFAULT_TO_TRY_AND_DIAGNOSE_A_RENDERING_ERROR._NOW_MY_SCREEN_JUST_SHOWS_BLACK__ALTHOUGH_I_KNOW_I_AM_DRAWING_OBJECTS_ONTO_THE_SCREEN.__"></span>Ich habe meine Zustände wieder auf den Standardwert festgelegt, um einen Renderingfehler zu diagnostizieren.</span><span class="sxs-lookup"><span data-stu-id="37f92-217"><span id="I_set_my_states_back_to_default_to_try_and_diagnose_a_rendering_error._Now_my_screen_just_shows_black__although_I_know_I_am_drawing_objects_onto_the_screen.__"></span><span id="i_set_my_states_back_to_default_to_try_and_diagnose_a_rendering_error._now_my_screen_just_shows_black__although_i_know_i_am_drawing_objects_onto_the_screen.__"></span><span id="I_SET_MY_STATES_BACK_TO_DEFAULT_TO_TRY_AND_DIAGNOSE_A_RENDERING_ERROR._NOW_MY_SCREEN_JUST_SHOWS_BLACK__ALTHOUGH_I_KNOW_I_AM_DRAWING_OBJECTS_ONTO_THE_SCREEN.__"></span>I set my states back to default to try and diagnose a rendering error.</span></span> <span data-ttu-id="37f92-218">Mein Bildschirm zeigt nur schwarz an, obwohl ich weiß, dass Objekte auf dem Bildschirm gezeichnet werden.</span><span class="sxs-lookup"><span data-stu-id="37f92-218">Now my screen just shows black, although I know I am drawing objects onto the screen.</span></span> 
</dt> <dd>

<span data-ttu-id="37f92-219">Stellen Sie beim Festlegen des Zustands zurück auf die Standardwerte (null) sicher, dass die samplemask im Befehl omsetblendstate niemals 0 (null) ist.</span><span class="sxs-lookup"><span data-stu-id="37f92-219">When setting state back to default values (NULL), ensure that the SampleMask in the call to OMSetBlendState is never zero.</span></span> <span data-ttu-id="37f92-220">Wenn samplemask auf 0 (null) festgelegt ist, werden alle Beispiele logisch und mit 0 (null).</span><span class="sxs-lookup"><span data-stu-id="37f92-220">If SampleMask is set to zero, then all samples will logically AND with zero.</span></span> <span data-ttu-id="37f92-221">In diesem Szenario bestehen keine Beispiele für den Blend-Test.</span><span class="sxs-lookup"><span data-stu-id="37f92-221">In this scenario, no samples will pass the blend test.</span></span>

</dd> <dt>

<span data-ttu-id="37f92-222"><span id="Where_did_the_D3DSAMP_SRGBTEXTURE_state_go___"></span><span id="where_did_the_d3dsamp_srgbtexture_state_go___"></span><span id="WHERE_DID_THE_D3DSAMP_SRGBTEXTURE_STATE_GO___"></span>Wo liegt der D3DSAMP \_ srgbtexture-Status?</span><span class="sxs-lookup"><span data-stu-id="37f92-222"><span id="Where_did_the_D3DSAMP_SRGBTEXTURE_state_go___"></span><span id="where_did_the_d3dsamp_srgbtexture_state_go___"></span><span id="WHERE_DID_THE_D3DSAMP_SRGBTEXTURE_STATE_GO___"></span>Where did the D3DSAMP\_SRGBTEXTURE state go?</span></span> 
</dt> <dd>

<span data-ttu-id="37f92-223">SRGB wurde als Teil des samplingzustands entfernt und ist nun an das Textur Format gebunden.</span><span class="sxs-lookup"><span data-stu-id="37f92-223">SRGB was removed as part of the sampler state and now is tied to the texture format.</span></span> <span data-ttu-id="37f92-224">Das Binden einer sRGB-Textur führt zu derselben Stichprobe, die Sie erhalten, wenn Sie D3DSAMP \_ srgbtexture in Direct3D 9 angegeben haben.</span><span class="sxs-lookup"><span data-stu-id="37f92-224">Binding an SRGB texture will result in the same sampling you would get if you specified D3DSAMP\_SRGBTEXTURE in Direct3D 9.</span></span>

</dd> </dl>

## <a name="formats"></a><span data-ttu-id="37f92-225">Formate</span><span class="sxs-lookup"><span data-stu-id="37f92-225">Formats</span></span>

<dl> <dt>

<span data-ttu-id="37f92-226"><span id="Which_D3D9_format_corresponds_to_which_D3D10_format___"></span><span id="which_d3d9_format_corresponds_to_which_d3d10_format___"></span><span id="WHICH_D3D9_FORMAT_CORRESPONDS_TO_WHICH_D3D10_FORMAT___"></span>Welches d3d9-Format entspricht dem d3d10-Format?</span><span class="sxs-lookup"><span data-stu-id="37f92-226"><span id="Which_D3D9_format_corresponds_to_which_D3D10_format___"></span><span id="which_d3d9_format_corresponds_to_which_d3d10_format___"></span><span id="WHICH_D3D9_FORMAT_CORRESPONDS_TO_WHICH_D3D10_FORMAT___"></span>Which D3D9 format corresponds to which D3D10 format?</span></span> 
</dt> <dd>

<span data-ttu-id="37f92-227">Weitere Informationen finden [Sie unter Direct3D 9 to Direct3D 10 Überlegungen](/windows/desktop/direct3d10/d3d10-graphics-programming-guide-d3d9-to-d3d10-considerations).</span><span class="sxs-lookup"><span data-stu-id="37f92-227">For info, see [Direct3D 9 to Direct3D 10 Considerations](/windows/desktop/direct3d10/d3d10-graphics-programming-guide-d3d9-to-d3d10-considerations).</span></span>

</dd> <dt>

<span data-ttu-id="37f92-228"><span id="What_happened_to_A8R8G8B8_texture_formats___"></span><span id="what_happened_to_a8r8g8b8_texture_formats___"></span><span id="WHAT_HAPPENED_TO_A8R8G8B8_TEXTURE_FORMATS___"></span>Was ist mit A8R8G8B8-Textur Formaten passiert?</span><span class="sxs-lookup"><span data-stu-id="37f92-228"><span id="What_happened_to_A8R8G8B8_texture_formats___"></span><span id="what_happened_to_a8r8g8b8_texture_formats___"></span><span id="WHAT_HAPPENED_TO_A8R8G8B8_TEXTURE_FORMATS___"></span>What happened to A8R8G8B8 texture formats?</span></span> 
</dt> <dd>

<span data-ttu-id="37f92-229">Sie wurden in d3d10 als veraltet markiert.</span><span class="sxs-lookup"><span data-stu-id="37f92-229">They have been deprecated in D3D10.</span></span> <span data-ttu-id="37f92-230">Sie können Ihre Texturen als R8G8B8A8 wieder verwenden, oder Sie können auf die Last ziehen, oder Sie können den Shader in den Shader ziehen.</span><span class="sxs-lookup"><span data-stu-id="37f92-230">You can re-source your textures as R8G8B8A8, or you can swizzle on load, or you can swizzle in the shader.</span></span>

</dd> <dt>

<span data-ttu-id="37f92-231"><span id="How_do_I_use_palettized_textures___"></span><span id="how_do_i_use_palettized_textures___"></span><span id="HOW_DO_I_USE_PALETTIZED_TEXTURES___"></span>Gewusst wie die Verwendung von Paletten-Texturen?</span><span class="sxs-lookup"><span data-stu-id="37f92-231"><span id="How_do_I_use_palettized_textures___"></span><span id="how_do_i_use_palettized_textures___"></span><span id="HOW_DO_I_USE_PALETTIZED_TEXTURES___"></span>How do I use palettized textures?</span></span> 
</dt> <dd>

<span data-ttu-id="37f92-232">Platzieren Sie die Farbpalette in einer Textur oder einem konstanten Puffer, und binden Sie Sie an die Pipeline.</span><span class="sxs-lookup"><span data-stu-id="37f92-232">Place your color palette in a texture or a constant buffer and bind it to the pipeline.</span></span> <span data-ttu-id="37f92-233">Führen Sie im Pixel-Shader eine indirekte Suche mithilfe des Indexes in der in der paletbasierten Textur aus.</span><span class="sxs-lookup"><span data-stu-id="37f92-233">In the pixel shader do an indirect lookup using the index in your palettized texture.</span></span>

</dd> <dt>

<span data-ttu-id="37f92-234"><span id="What_are_these_new_SRGB_formats___"></span><span id="what_are_these_new_srgb_formats___"></span><span id="WHAT_ARE_THESE_NEW_SRGB_FORMATS___"></span>Welche neuen sRGB-Formate sind verfügbar?</span><span class="sxs-lookup"><span data-stu-id="37f92-234"><span id="What_are_these_new_SRGB_formats___"></span><span id="what_are_these_new_srgb_formats___"></span><span id="WHAT_ARE_THESE_NEW_SRGB_FORMATS___"></span>What are these new SRGB formats?</span></span> 
</dt> <dd>

<span data-ttu-id="37f92-235">SRGB wurde als Teil des samplingzustands entfernt und ist nun an das Textur Format gebunden.</span><span class="sxs-lookup"><span data-stu-id="37f92-235">SRGB was removed as part of the sampler state and is now tied to the texture format.</span></span> <span data-ttu-id="37f92-236">Das Binden einer sRGB-Textur führt zu derselben Stichprobe, die Sie erhalten, wenn Sie D3DSAMP \_ srgbtexture in Direct3D 9 angegeben haben.</span><span class="sxs-lookup"><span data-stu-id="37f92-236">Binding an SRGB texture will result in the same sampling you would get if you specified D3DSAMP\_SRGBTEXTURE in Direct3D 9.</span></span>

</dd> <dt>

<span data-ttu-id="37f92-237"><span id="Where_did_triangle_fans_go___"></span><span id="where_did_triangle_fans_go___"></span><span id="WHERE_DID_TRIANGLE_FANS_GO___"></span>Wo sind die Dreiecks Fans unterwegs?</span><span class="sxs-lookup"><span data-stu-id="37f92-237"><span id="Where_did_triangle_fans_go___"></span><span id="where_did_triangle_fans_go___"></span><span id="WHERE_DID_TRIANGLE_FANS_GO___"></span>Where did triangle fans go?</span></span> 
</dt> <dd>

<span data-ttu-id="37f92-238">Dreiecks Fans wurden in d3d10 als veraltet markiert.</span><span class="sxs-lookup"><span data-stu-id="37f92-238">Triangle fans have been deprecated in D3D10.</span></span> <span data-ttu-id="37f92-239">Dreiecks Lüfter müssen entweder in der Inhalts Pipeline oder beim Laden konvertiert werden.</span><span class="sxs-lookup"><span data-stu-id="37f92-239">Triangle fans will need to be converted either in the content pipeline or on load.</span></span>

</dd> </dl>

## <a name="shader-linkage"></a><span data-ttu-id="37f92-240">Shaderverknüpfung</span><span class="sxs-lookup"><span data-stu-id="37f92-240">Shader Linkage</span></span>

<dl> <dt>

<span data-ttu-id="37f92-241"><span id="My_Direct3D_9_shaders_compile_fine_to_Shader_Model_4.0__but_when_I_bind_them_to_the_pipeline__I_get_linkage_errors_showing_up_in_the_debug_output_with_the_debug_runtime.__"></span><span id="my_direct3d_9_shaders_compile_fine_to_shader_model_4.0__but_when_i_bind_them_to_the_pipeline__i_get_linkage_errors_showing_up_in_the_debug_output_with_the_debug_runtime.__"></span><span id="MY_DIRECT3D_9_SHADERS_COMPILE_FINE_TO_SHADER_MODEL_4.0__BUT_WHEN_I_BIND_THEM_TO_THE_PIPELINE__I_GET_LINKAGE_ERRORS_SHOWING_UP_IN_THE_DEBUG_OUTPUT_WITH_THE_DEBUG_RUNTIME.__"></span>Meine Direct3D 9-Shader werden problemlos in Shader-Modell 4,0 kompiliert, aber wenn ich Sie an die Pipeline bindet, erhalte ich Verknüpfungs Fehler, die in der Debug-Ausgabe mit der Debug-Laufzeit angezeigt werden.</span><span class="sxs-lookup"><span data-stu-id="37f92-241"><span id="My_Direct3D_9_shaders_compile_fine_to_Shader_Model_4.0__but_when_I_bind_them_to_the_pipeline__I_get_linkage_errors_showing_up_in_the_debug_output_with_the_debug_runtime.__"></span><span id="my_direct3d_9_shaders_compile_fine_to_shader_model_4.0__but_when_i_bind_them_to_the_pipeline__i_get_linkage_errors_showing_up_in_the_debug_output_with_the_debug_runtime.__"></span><span id="MY_DIRECT3D_9_SHADERS_COMPILE_FINE_TO_SHADER_MODEL_4.0__BUT_WHEN_I_BIND_THEM_TO_THE_PIPELINE__I_GET_LINKAGE_ERRORS_SHOWING_UP_IN_THE_DEBUG_OUTPUT_WITH_THE_DEBUG_RUNTIME.__"></span>My Direct3D 9 shaders compile fine to Shader Model 4.0, but when I bind them to the pipeline, I get linkage errors showing up in the debug output with the debug runtime.</span></span> 
</dt> <dd>

<span data-ttu-id="37f92-242">Die Shader-Verknüpfung ist in d3d10 wesentlich strenger.</span><span class="sxs-lookup"><span data-stu-id="37f92-242">Shader linkage is much stricter in D3D10.</span></span> <span data-ttu-id="37f92-243">Elemente in einer nachfolgenden Phase müssen in der Reihenfolge gelesen werden, in der Sie aus der vorherigen Phase ausgegeben werden.</span><span class="sxs-lookup"><span data-stu-id="37f92-243">Elements in a subsequent stage must be read in the order they are output from the previous stage.</span></span> <span data-ttu-id="37f92-244">Beispiel:</span><span class="sxs-lookup"><span data-stu-id="37f92-244">For example:</span></span>

<span data-ttu-id="37f92-245">Vertex-Shader-Ausgaben:</span><span class="sxs-lookup"><span data-stu-id="37f92-245">A vertex shader outputs:</span></span>

``` syntax
    float4 Pos  : SV_POSITION;
    float3 Norm : NORMAL;
    float2 Tex  : TEXCOORD0;
```

<span data-ttu-id="37f92-246">Ein Pixelshader liest in:</span><span class="sxs-lookup"><span data-stu-id="37f92-246">A pixel shader reads in:</span></span>

``` syntax
        float3 Norm : NORMAL;
        float2 Tex  : TEXCOORD0;
```

<span data-ttu-id="37f92-247">Obwohl die Position im Pixelshader nicht benötigt wird, verursacht dies einen Verknüpfungs Fehler, da die Position vom Vertexshader ausgegeben, aber nicht vom Pixelshader gelesen wird.</span><span class="sxs-lookup"><span data-stu-id="37f92-247">Although the position is not needed in the pixel shader, this will cause a linkage error, because position is being output from the vertex shader, but not read by the pixel shader.</span></span> <span data-ttu-id="37f92-248">Die korrekte Version sieht wie folgt aus:</span><span class="sxs-lookup"><span data-stu-id="37f92-248">The more correct version would look like this:</span></span>

<span data-ttu-id="37f92-249">Vertex-Shader-Ausgaben:</span><span class="sxs-lookup"><span data-stu-id="37f92-249">A vertex shader outputs:</span></span>

``` syntax
        float3 Norm : NORMAL;
        float2 Tex  : TEXCOORD0;
        float4 Pos  : SV_POSITION;
```

<span data-ttu-id="37f92-250">Ein Pixelshader liest in:</span><span class="sxs-lookup"><span data-stu-id="37f92-250">A pixel shader reads in:</span></span>

``` syntax
        float3 Norm : NORMAL;
        float2 Tex  : TEXCOORD0;
```

<span data-ttu-id="37f92-251">In diesem Fall gibt der Vertex-Shader die gleichen Informationen aus, aber jetzt liest der Pixelshader Dinge in der Auftrags Ausgabe.</span><span class="sxs-lookup"><span data-stu-id="37f92-251">In this case, the vertex shader is outputting the same information, but now the pixel shader is reading things in the order output.</span></span> <span data-ttu-id="37f92-252">Da der Pixelshader nichts nach TeX liest, müssen wir uns keine Sorgen machen, dass vs mehr Informationen ausstellt, als das PS liest.</span><span class="sxs-lookup"><span data-stu-id="37f92-252">Because the pixel shader is not reading anything after Tex, we do not have to worry that the VS is outputting more information than the PS is reading.</span></span>

</dd> <dt>

<span data-ttu-id="37f92-253"><span id="I_need_a_shader_signature_in_order_to_create_an_Input_Layout__but_I_load_my_meshes_and_create_layouts_before_creating_shaders._What_do_I_do___"></span><span id="i_need_a_shader_signature_in_order_to_create_an_input_layout__but_i_load_my_meshes_and_create_layouts_before_creating_shaders._what_do_i_do___"></span><span id="I_NEED_A_SHADER_SIGNATURE_IN_ORDER_TO_CREATE_AN_INPUT_LAYOUT__BUT_I_LOAD_MY_MESHES_AND_CREATE_LAYOUTS_BEFORE_CREATING_SHADERS._WHAT_DO_I_DO___"></span>Ich benötige eine shadersignatur, um ein Eingabe Layout zu erstellen, aber ich lade meine Netze und erstelle Layouts vor dem Erstellen von Shadern.</span><span class="sxs-lookup"><span data-stu-id="37f92-253"><span id="I_need_a_shader_signature_in_order_to_create_an_Input_Layout__but_I_load_my_meshes_and_create_layouts_before_creating_shaders._What_do_I_do___"></span><span id="i_need_a_shader_signature_in_order_to_create_an_input_layout__but_i_load_my_meshes_and_create_layouts_before_creating_shaders._what_do_i_do___"></span><span id="I_NEED_A_SHADER_SIGNATURE_IN_ORDER_TO_CREATE_AN_INPUT_LAYOUT__BUT_I_LOAD_MY_MESHES_AND_CREATE_LAYOUTS_BEFORE_CREATING_SHADERS._WHAT_DO_I_DO___"></span>I need a shader signature in order to create an Input Layout, but I load my meshes and create layouts before creating shaders.</span></span> <span data-ttu-id="37f92-254">Wie gehe ich vor?</span><span class="sxs-lookup"><span data-stu-id="37f92-254">What do I do?</span></span> 
</dt> <dd>

<span data-ttu-id="37f92-255">Eine Lösung besteht darin, die Reihenfolge zu wechseln und Shader vor dem Laden von Netzen zu laden.</span><span class="sxs-lookup"><span data-stu-id="37f92-255">One solution is to switch the order and load shaders before loading meshes.</span></span> <span data-ttu-id="37f92-256">Dies ist jedoch viel einfacher zu tun als durchgeführt.</span><span class="sxs-lookup"><span data-stu-id="37f92-256">However, this is much easier said than done.</span></span> <span data-ttu-id="37f92-257">Sie können die Eingabe Layouts immer bei Bedarf erstellen, wenn Sie von der Anwendung benötigt werden.</span><span class="sxs-lookup"><span data-stu-id="37f92-257">You always can create the Input Layouts on demand when needed by the application.</span></span> <span data-ttu-id="37f92-258">Sie müssen eine Version der shadersignatur aufbewahren.</span><span class="sxs-lookup"><span data-stu-id="37f92-258">You will have to keep a version of the shader signature around.</span></span> <span data-ttu-id="37f92-259">Sie sollten einen Hash erstellen, der auf dem Shader und dem Puffer Layout basiert, und das Eingabe Layout nur dann erstellen, wenn eine Übereinstimmung vorhanden ist, die noch nicht vorhanden ist.</span><span class="sxs-lookup"><span data-stu-id="37f92-259">You should create a hash based off of the shader and buffer layout, and only create the Input Layout if one that matches does not exist already.</span></span>

</dd> </dl>

## <a name="draw-calls"></a><span data-ttu-id="37f92-260">Draw-Aufrufe</span><span class="sxs-lookup"><span data-stu-id="37f92-260">Draw Calls</span></span>

<dl> <dt>

<span data-ttu-id="37f92-261"><span id="What_is_my_limit_on_draw_calls_for_D3D10_to_reach_60_Hz__30_Hz___"></span><span id="what_is_my_limit_on_draw_calls_for_d3d10_to_reach_60_hz__30_hz___"></span><span id="WHAT_IS_MY_LIMIT_ON_DRAW_CALLS_FOR_D3D10_TO_REACH_60_HZ__30_HZ___"></span>Was ist meine Beschränkung für Draw-Aufrufe für d3d10, um 60 Hz zu erreichen?</span><span class="sxs-lookup"><span data-stu-id="37f92-261"><span id="What_is_my_limit_on_draw_calls_for_D3D10_to_reach_60_Hz__30_Hz___"></span><span id="what_is_my_limit_on_draw_calls_for_d3d10_to_reach_60_hz__30_hz___"></span><span id="WHAT_IS_MY_LIMIT_ON_DRAW_CALLS_FOR_D3D10_TO_REACH_60_HZ__30_HZ___"></span>What is my limit on draw calls for D3D10 to reach 60 Hz?</span></span> <span data-ttu-id="37f92-262">30 Hz?</span><span class="sxs-lookup"><span data-stu-id="37f92-262">30 Hz?</span></span> 
</dt> <dd>

<span data-ttu-id="37f92-263">Bei Direct3D 9 ist aufgrund der CPU-Kosten pro Draw-Aufruf eine Beschränkung für die Anzahl der Draw-Aufrufe aufgetreten.</span><span class="sxs-lookup"><span data-stu-id="37f92-263">Direct3D 9 had a limitation on the number of draw calls because of the CPU cost per draw call.</span></span> <span data-ttu-id="37f92-264">Auf Direct3D 10 wurden die Kosten für jeden zeichnen-Befehl reduziert.</span><span class="sxs-lookup"><span data-stu-id="37f92-264">On Direct3D 10, the cost of each draw call has been reduced.</span></span> <span data-ttu-id="37f92-265">Es gibt jedoch keine eindeutige Korrelation zwischen Draw-aufrufen und Frameraten.</span><span class="sxs-lookup"><span data-stu-id="37f92-265">However, there is no longer a definite correlation between draw calls and frame rates.</span></span> <span data-ttu-id="37f92-266">Da Draw-Aufrufe häufig viele Support Aufrufe erfordern (Konstante Puffer Aktualisierungen, Textur Bindungen, Zustands Einstellungen usw.), sind die Auswirkungen der-API auf die Frame Rate jetzt eher von der allgemeinen API-Nutzung abhängig, anstatt durch Zeichnen von Ansichts Anzahlen.</span><span class="sxs-lookup"><span data-stu-id="37f92-266">Because draw calls often require many support calls ( constant buffer updates, texture bindings, state setting, and so on) the frame rate impact of the API is now more dependent on the overall API usage as opposed to simply draw call counts.</span></span>

</dd> </dl>

## <a name="resources"></a><span data-ttu-id="37f92-267">Ressourcen</span><span class="sxs-lookup"><span data-stu-id="37f92-267">Resources</span></span>

<dl> <dt>

<span data-ttu-id="37f92-268"><span id="What_resource_usage_type_should_I_use_for_what_operations___"></span><span id="what_resource_usage_type_should_i_use_for_what_operations___"></span><span id="WHAT_RESOURCE_USAGE_TYPE_SHOULD_I_USE_FOR_WHAT_OPERATIONS___"></span>Welchen Ressourcen Verwendungstyp sollte ich für welche Vorgänge verwenden?</span><span class="sxs-lookup"><span data-stu-id="37f92-268"><span id="What_resource_usage_type_should_I_use_for_what_operations___"></span><span id="what_resource_usage_type_should_i_use_for_what_operations___"></span><span id="WHAT_RESOURCE_USAGE_TYPE_SHOULD_I_USE_FOR_WHAT_OPERATIONS___"></span>What resource usage type should I use for what operations?</span></span> 
</dt> <dd>

<span data-ttu-id="37f92-269">Verwenden Sie das folgende Spick Blatt:</span><span class="sxs-lookup"><span data-stu-id="37f92-269">Use the following cheat-sheet:</span></span>

-   <span data-ttu-id="37f92-270">Die CPU aktualisiert die Ressource mehrmals pro Frame: d3d10 \_ Usage \_ Dynamic</span><span class="sxs-lookup"><span data-stu-id="37f92-270">The CPU updates the resource more than once per frame: D3D10\_USAGE\_DYNAMIC</span></span>
-   <span data-ttu-id="37f92-271">Die CPU aktualisiert die Ressource weniger als einmal pro Frame: d3d10 \_ Usage \_ default</span><span class="sxs-lookup"><span data-stu-id="37f92-271">The CPU updates the resource less than once per frame: D3D10\_USAGE\_DEFAULT</span></span>
-   <span data-ttu-id="37f92-272">Die CPU aktualisiert nicht die Ressource: d3d10 \_ Usage \_ unveränderlich</span><span class="sxs-lookup"><span data-stu-id="37f92-272">The CPU does not update the resource: D3D10\_USAGE\_IMMUTABLE</span></span>
-   <span data-ttu-id="37f92-273">Die CPU muss die Ressource lesen: d3d10 \_ Usage \_ Staging</span><span class="sxs-lookup"><span data-stu-id="37f92-273">The CPU needs to read the resource: D3D10\_USAGE\_STAGING</span></span>

<span data-ttu-id="37f92-274">Da Konstante Puffer immer häufig aktualisiert werden sollen, entsprechen Sie nicht dem "Cheat Sheet".</span><span class="sxs-lookup"><span data-stu-id="37f92-274">Because constant buffers are always meant to be update frequently, they do not conform to the "cheat-sheet."</span></span> <span data-ttu-id="37f92-275">Informationen zu den Ressourcentypen, die für konstante Puffer verwendet werden sollen, finden Sie im Abschnitt [Konstantenpuffer](#constant-buffers) .</span><span class="sxs-lookup"><span data-stu-id="37f92-275">For which resource types to use for constant buffers, see the [Constant Buffers](#constant-buffers) section.</span></span>

</dd> <dt>

<span data-ttu-id="37f92-276"><span id="What_happened_to_DrawPrimitiveUP_and_DrawIndexedPrimitiveUP___"></span><span id="what_happened_to_drawprimitiveup_and_drawindexedprimitiveup___"></span><span id="WHAT_HAPPENED_TO_DRAWPRIMITIVEUP_AND_DRAWINDEXEDPRIMITIVEUP___"></span>Was ist mit drawprimitiveup und drawindexedprimitiveup passiert?</span><span class="sxs-lookup"><span data-stu-id="37f92-276"><span id="What_happened_to_DrawPrimitiveUP_and_DrawIndexedPrimitiveUP___"></span><span id="what_happened_to_drawprimitiveup_and_drawindexedprimitiveup___"></span><span id="WHAT_HAPPENED_TO_DRAWPRIMITIVEUP_AND_DRAWINDEXEDPRIMITIVEUP___"></span>What happened to DrawPrimitiveUP and DrawIndexedPrimitiveUP?</span></span> 
</dt> <dd>

<span data-ttu-id="37f92-277">Sie sind in d3d10 nicht mehr vorhanden.</span><span class="sxs-lookup"><span data-stu-id="37f92-277">They are gone in D3D10.</span></span> <span data-ttu-id="37f92-278">Verwenden Sie für Dynamic geometry einen dynamischen Puffer mit hoher d3d10- \_ Verwendung \_ .</span><span class="sxs-lookup"><span data-stu-id="37f92-278">For dynamic geometry use a large D3D10\_USAGE\_DYNAMIC buffer.</span></span> <span data-ttu-id="37f92-279">Ordnen Sie ihn am Anfang des Frames der d3d10 Map- \_ \_ Schreib \_ Verwerfungs zu.</span><span class="sxs-lookup"><span data-stu-id="37f92-279">At the beginning of the frame, map it with D3D10\_MAP\_WRITE\_DISCARD.</span></span> <span data-ttu-id="37f92-280">Bei jedem nachfolgenden Draw-Befehl sollte der Schreib Zeiger über die Position der zuvor gezeichneten Scheitel Punkte hinausgezogen werden, und der Puffer wird mit d3d10 \_ map \_ Write \_ No überschrieben zugeordnet \_ .</span><span class="sxs-lookup"><span data-stu-id="37f92-280">For each subsequent draw call advance the write pointer past the position of the previously drawn vertices and map the buffer with D3D10\_MAP\_WRITE\_NO\_OVERWRITE.</span></span> <span data-ttu-id="37f92-281">Wenn Sie sich am Ende des Puffers vor dem Ende des Frames befinden, umschließen Sie den Schreib Zeiger um den Anfang und die Zuordnung mit d3d10 \_ map \_ Write \_ verwerfen.</span><span class="sxs-lookup"><span data-stu-id="37f92-281">If you near the end of the buffer before the end of the frame, wrap the write pointer around to the beginning and map with D3D10\_MAP\_WRITE\_DISCARD.</span></span>

</dd> <dt>

<span data-ttu-id="37f92-282"><span id="Can_I_write_16-bit_indices_and_32-bit_indices_into_the_same_dynamic_geometry_buffer___"></span><span id="can_i_write_16-bit_indices_and_32-bit_indices_into_the_same_dynamic_geometry_buffer___"></span><span id="CAN_I_WRITE_16-BIT_INDICES_AND_32-BIT_INDICES_INTO_THE_SAME_DYNAMIC_GEOMETRY_BUFFER___"></span>Kann ich 16-Bit-Indizes und 32-Bit-Indizes in denselben dynamischen Geometry-Puffer schreiben?</span><span class="sxs-lookup"><span data-stu-id="37f92-282"><span id="Can_I_write_16-bit_indices_and_32-bit_indices_into_the_same_dynamic_geometry_buffer___"></span><span id="can_i_write_16-bit_indices_and_32-bit_indices_into_the_same_dynamic_geometry_buffer___"></span><span id="CAN_I_WRITE_16-BIT_INDICES_AND_32-BIT_INDICES_INTO_THE_SAME_DYNAMIC_GEOMETRY_BUFFER___"></span>Can I write 16-bit indices and 32-bit indices into the same dynamic geometry buffer?</span></span> 
</dt> <dd>

<span data-ttu-id="37f92-283">Ja, das ist möglich, aber dies kann zu einer Leistungs Einbuße auf bestimmter Hardware werden.</span><span class="sxs-lookup"><span data-stu-id="37f92-283">Yes, you can, but this can incur a performance penalty on certain hardware.</span></span> <span data-ttu-id="37f92-284">Es ist sicherer, separate Puffer für dynamische 16-Bit-Indexdaten und 32-Bit-Indexdaten zu erstellen.</span><span class="sxs-lookup"><span data-stu-id="37f92-284">It is a safer to create separate buffers for dynamic 16-bit index data and 32-bit index data.</span></span>

</dd> <dt>

<span data-ttu-id="37f92-285"><span id="How_do_I_read_data_back_from_the_GPU_to_the_CPU___"></span><span id="how_do_i_read_data_back_from_the_gpu_to_the_cpu___"></span><span id="HOW_DO_I_READ_DATA_BACK_FROM_THE_GPU_TO_THE_CPU___"></span>Gewusst wie Daten von der GPU auf die CPU zurück lesen?</span><span class="sxs-lookup"><span data-stu-id="37f92-285"><span id="How_do_I_read_data_back_from_the_GPU_to_the_CPU___"></span><span id="how_do_i_read_data_back_from_the_gpu_to_the_cpu___"></span><span id="HOW_DO_I_READ_DATA_BACK_FROM_THE_GPU_TO_THE_CPU___"></span>How do I read data back from the GPU to the CPU?</span></span> 
</dt> <dd>

<span data-ttu-id="37f92-286">Sie müssen eine Staging-Ressource verwenden.</span><span class="sxs-lookup"><span data-stu-id="37f92-286">You must use a staging resource.</span></span> <span data-ttu-id="37f92-287">Kopieren Sie die Daten aus der GPU-Ressource mithilfe von copyresource in die stagingressource.</span><span class="sxs-lookup"><span data-stu-id="37f92-287">Copy the data from the GPU resource to the staging resource using CopyResource.</span></span> <span data-ttu-id="37f92-288">Ordnen Sie die stagingressource zu, um die Daten zu lesen.</span><span class="sxs-lookup"><span data-stu-id="37f92-288">Map the staging resource to read the data.</span></span>

</dd> <dt>

<span data-ttu-id="37f92-289"><span id="My_application_was_dependent_on_StretchRect_functionality.__"></span><span id="my_application_was_dependent_on_stretchrect_functionality.__"></span><span id="MY_APPLICATION_WAS_DEPENDENT_ON_STRETCHRECT_FUNCTIONALITY.__"></span>Meine Anwendung war von der stretchrect-Funktion abhängig.</span><span class="sxs-lookup"><span data-stu-id="37f92-289"><span id="My_application_was_dependent_on_StretchRect_functionality.__"></span><span id="my_application_was_dependent_on_stretchrect_functionality.__"></span><span id="MY_APPLICATION_WAS_DEPENDENT_ON_STRETCHRECT_FUNCTIONALITY.__"></span>My application was dependent on StretchRect functionality.</span></span> 
</dt> <dd>

<span data-ttu-id="37f92-290">Da es sich im Wesentlichen um einen Wrapper für grundlegende Direct3D-Funktionen handelt, wurde er aus der API entfernt.</span><span class="sxs-lookup"><span data-stu-id="37f92-290">Because this was essentially a wrapper for basic Direct3D functionality, it was removed from the API.</span></span> <span data-ttu-id="37f92-291">Einige der stretchrect-Funktionen wurden in D3DX10LoadTextureFromTexture verschoben.</span><span class="sxs-lookup"><span data-stu-id="37f92-291">Some of the StretchRect functionality was moved into D3DX10LoadTextureFromTexture.</span></span> <span data-ttu-id="37f92-292">Für Formatkonvertierungen und das Kopieren von Texturen kann D3DX10LoadTextureFromTexture den Auftrag ausführen.</span><span class="sxs-lookup"><span data-stu-id="37f92-292">For format conversions and copying textures, D3DX10LoadTextureFromTexture may do the job.</span></span> <span data-ttu-id="37f92-293">Vorgänge, wie z. b. die Umstellung von einer Größe in eine andere, erfordern jedoch in der Anwendung einen Rendering-zu-Textur-Vorgang.</span><span class="sxs-lookup"><span data-stu-id="37f92-293">However, operations such as converting from one size to another likely will require a render to texture operation in the application.</span></span>

</dd> <dt>

<span data-ttu-id="37f92-294"><span id="There_are_no_offsets_or_sizes_on_Map_calls_for_resources._These_were_there_on_Lock_calls_on_Direct3D_9__why_did_they_change___"></span><span id="there_are_no_offsets_or_sizes_on_map_calls_for_resources._these_were_there_on_lock_calls_on_direct3d_9__why_did_they_change___"></span><span id="THERE_ARE_NO_OFFSETS_OR_SIZES_ON_MAP_CALLS_FOR_RESOURCES._THESE_WERE_THERE_ON_LOCK_CALLS_ON_DIRECT3D_9__WHY_DID_THEY_CHANGE___"></span>Es gibt keine Offsets oder Größen für Zuordnungs Aufrufe für Ressourcen.</span><span class="sxs-lookup"><span data-stu-id="37f92-294"><span id="There_are_no_offsets_or_sizes_on_Map_calls_for_resources._These_were_there_on_Lock_calls_on_Direct3D_9__why_did_they_change___"></span><span id="there_are_no_offsets_or_sizes_on_map_calls_for_resources._these_were_there_on_lock_calls_on_direct3d_9__why_did_they_change___"></span><span id="THERE_ARE_NO_OFFSETS_OR_SIZES_ON_MAP_CALLS_FOR_RESOURCES._THESE_WERE_THERE_ON_LOCK_CALLS_ON_DIRECT3D_9__WHY_DID_THEY_CHANGE___"></span>There are no offsets or sizes on Map calls for resources.</span></span> <span data-ttu-id="37f92-295">Diese waren bei Sperr aufrufen auf Direct3D 9 vorhanden. Warum haben Sie sich geändert?</span><span class="sxs-lookup"><span data-stu-id="37f92-295">These were there on Lock calls on Direct3D 9; why did they change?</span></span> 
</dt> <dd>

<span data-ttu-id="37f92-296">Die Offsets und Größen für Sperr Aufrufe auf Direct3D 9 waren im Grunde genommen API-Übersichtlichkeit und werden oft vom Treiber ignoriert.</span><span class="sxs-lookup"><span data-stu-id="37f92-296">The offsets and sizes on Lock calls on Direct3D 9 were basically API clutter and often ignored by the driver.</span></span> <span data-ttu-id="37f92-297">Offsets sollten stattdessen von der Anwendung aus dem im Map-Befehl zurückgegebenen Zeiger berechnet werden.</span><span class="sxs-lookup"><span data-stu-id="37f92-297">Offsets should be calculated instead by the application from the pointer returned in the Map call.</span></span>

</dd> </dl>

## <a name="depth-as-texture"></a><span data-ttu-id="37f92-298">Tiefe als Textur</span><span class="sxs-lookup"><span data-stu-id="37f92-298">Depth as Texture</span></span>

<dl> <dt>

<span data-ttu-id="37f92-299"><span id="Which_is_faster__Using_depth_as_a_texture_or_writing_depth_to_alpha_and_reading_that___"></span><span id="which_is_faster__using_depth_as_a_texture_or_writing_depth_to_alpha_and_reading_that___"></span><span id="WHICH_IS_FASTER__USING_DEPTH_AS_A_TEXTURE_OR_WRITING_DEPTH_TO_ALPHA_AND_READING_THAT___"></span>Was ist schneller?</span><span class="sxs-lookup"><span data-stu-id="37f92-299"><span id="Which_is_faster__Using_depth_as_a_texture_or_writing_depth_to_alpha_and_reading_that___"></span><span id="which_is_faster__using_depth_as_a_texture_or_writing_depth_to_alpha_and_reading_that___"></span><span id="WHICH_IS_FASTER__USING_DEPTH_AS_A_TEXTURE_OR_WRITING_DEPTH_TO_ALPHA_AND_READING_THAT___"></span>Which is faster?</span></span> <span data-ttu-id="37f92-300">Sie verwenden Tiefe als Textur oder schreiben Tiefe in Alpha und lesen diese?</span><span class="sxs-lookup"><span data-stu-id="37f92-300">Using depth as a texture or writing depth to alpha and reading that?</span></span> 
</dt> <dd>

<span data-ttu-id="37f92-301">Dabei handelt es sich um Anwendungs-und Hardware spezifische Anwendungen.</span><span class="sxs-lookup"><span data-stu-id="37f92-301">This is application and hardware specific.</span></span> <span data-ttu-id="37f92-302">Verwenden Sie, je nachdem, welche Bandbreite eingespart wird.</span><span class="sxs-lookup"><span data-stu-id="37f92-302">Use whichever one saves the most bandwidth.</span></span> <span data-ttu-id="37f92-303">Wenn Sie bereits mehrere Renderziele verwenden und über einen zusätzlichen Kanal verfügen, ist das Schreiben von Tiefe aus dem Shader möglicherweise eine bessere Lösung.</span><span class="sxs-lookup"><span data-stu-id="37f92-303">If you already are using multiple render targets and have an extra channel, then writing depth from the shader may be a better solution.</span></span> <span data-ttu-id="37f92-304">Außerdem können Sie mit dem Schreiben von Tiefe in Alpha oder einem anderen Renderziel lineare tiefen Werte schreiben, mit denen Berechnungen beschleunigt werden können, die auf den tiefen Puffer zugreifen müssen.</span><span class="sxs-lookup"><span data-stu-id="37f92-304">Also, writing depth to alpha or another render target allows you to write linear depth values that may speed up calculations that need to access the depth buffer.</span></span>

</dd> <dt>

<span data-ttu-id="37f92-305"><span id="Can_I_have_a_texture_bound_as_an_input_AND_bound_as_a_depth-stencil_texture_as_long_as_I_disable_depth_writes___"></span><span id="can_i_have_a_texture_bound_as_an_input_and_bound_as_a_depth-stencil_texture_as_long_as_i_disable_depth_writes___"></span><span id="CAN_I_HAVE_A_TEXTURE_BOUND_AS_AN_INPUT_AND_BOUND_AS_A_DEPTH-STENCIL_TEXTURE_AS_LONG_AS_I_DISABLE_DEPTH_WRITES___"></span>Kann eine Textur als Eingabe gebunden und als Tiefe der tiefen Schablone gebunden werden, solange ich die Tiefe von Schreibvorgängen deaktiviere?</span><span class="sxs-lookup"><span data-stu-id="37f92-305"><span id="Can_I_have_a_texture_bound_as_an_input_AND_bound_as_a_depth-stencil_texture_as_long_as_I_disable_depth_writes___"></span><span id="can_i_have_a_texture_bound_as_an_input_and_bound_as_a_depth-stencil_texture_as_long_as_i_disable_depth_writes___"></span><span id="CAN_I_HAVE_A_TEXTURE_BOUND_AS_AN_INPUT_AND_BOUND_AS_A_DEPTH-STENCIL_TEXTURE_AS_LONG_AS_I_DISABLE_DEPTH_WRITES___"></span>Can I have a texture bound as an input AND bound as a depth-stencil texture as long as I disable depth writes?</span></span> 
</dt> <dd>

<span data-ttu-id="37f92-306">Nicht in d3d10.</span><span class="sxs-lookup"><span data-stu-id="37f92-306">Not in D3D10.</span></span>

</dd> </dl>

## <a name="msaa"></a><span data-ttu-id="37f92-307">MSAA</span><span class="sxs-lookup"><span data-stu-id="37f92-307">MSAA</span></span>

<dl> <dt>

<span data-ttu-id="37f92-308"><span id="Can_I_resolve_an_MSAA_depth-stencil_texture___"></span><span id="can_i_resolve_an_msaa_depth-stencil_texture___"></span><span id="CAN_I_RESOLVE_AN_MSAA_DEPTH-STENCIL_TEXTURE___"></span>Kann ich eine MSAA-tiefen Schablone auflösen?</span><span class="sxs-lookup"><span data-stu-id="37f92-308"><span id="Can_I_resolve_an_MSAA_depth-stencil_texture___"></span><span id="can_i_resolve_an_msaa_depth-stencil_texture___"></span><span id="CAN_I_RESOLVE_AN_MSAA_DEPTH-STENCIL_TEXTURE___"></span>Can I resolve an MSAA depth-stencil texture?</span></span> 
</dt> <dd>

<span data-ttu-id="37f92-309">Nicht in d3d10.</span><span class="sxs-lookup"><span data-stu-id="37f92-309">Not in D3D10.</span></span> <span data-ttu-id="37f92-310">Allerdings können Sie Stichproben einzelner Beispiele aus der MSAA-Textur durch sehen.</span><span class="sxs-lookup"><span data-stu-id="37f92-310">However, you can sample individual samples from the MSAA texture.</span></span> <span data-ttu-id="37f92-311">Weitere Informationen finden Sie im Abschnitt [HLSL](#hlsl) .</span><span class="sxs-lookup"><span data-stu-id="37f92-311">See the [HLSL](#hlsl) section for details.</span></span>

</dd> <dt>

<span data-ttu-id="37f92-312"><span id="Why_does_my_application_crash_as_soon_as_I_enable_MSAA___"></span><span id="why_does_my_application_crash_as_soon_as_i_enable_msaa___"></span><span id="WHY_DOES_MY_APPLICATION_CRASH_AS_SOON_AS_I_ENABLE_MSAA___"></span>Warum stürzt meine Anwendung ab, sobald ich MSAA aktiviere?</span><span class="sxs-lookup"><span data-stu-id="37f92-312"><span id="Why_does_my_application_crash_as_soon_as_I_enable_MSAA___"></span><span id="why_does_my_application_crash_as_soon_as_i_enable_msaa___"></span><span id="WHY_DOES_MY_APPLICATION_CRASH_AS_SOON_AS_I_ENABLE_MSAA___"></span>Why does my application crash as soon as I enable MSAA?</span></span> 
</dt> <dd>

<span data-ttu-id="37f92-313">Stellen Sie sicher, dass Sie eine MSAA-Stichproben Anzahl und eine Qualitäts Nummer aktivieren, die tatsächlich vom Treiber aufgelistet werden.</span><span class="sxs-lookup"><span data-stu-id="37f92-313">Ensure you are enabling an MSAA sample count and quality number that actually are enumerated by the driver.</span></span>

</dd> </dl>

## <a name="crashes"></a><span data-ttu-id="37f92-314">Abstürze</span><span class="sxs-lookup"><span data-stu-id="37f92-314">Crashes</span></span>

<dl> <dt>

<span data-ttu-id="37f92-315"><span id="My_application_crashes_in_D3D10_or_in_the_driver_and_I_do_not_know_why.__"></span><span id="my_application_crashes_in_d3d10_or_in_the_driver_and_i_do_not_know_why.__"></span><span id="MY_APPLICATION_CRASHES_IN_D3D10_OR_IN_THE_DRIVER_AND_I_DO_NOT_KNOW_WHY.__"></span>Meine Anwendung stürzt in d3d10 oder im Treiber ab, und ich weiß nicht, warum dies der Fall ist.</span><span class="sxs-lookup"><span data-stu-id="37f92-315"><span id="My_application_crashes_in_D3D10_or_in_the_driver_and_I_do_not_know_why.__"></span><span id="my_application_crashes_in_d3d10_or_in_the_driver_and_i_do_not_know_why.__"></span><span id="MY_APPLICATION_CRASHES_IN_D3D10_OR_IN_THE_DRIVER_AND_I_DO_NOT_KNOW_WHY.__"></span>My application crashes in D3D10 or in the driver and I do not know why.</span></span> 
</dt> <dd>

<span data-ttu-id="37f92-316">Der erste Schritt besteht darin, die Debug-Laufzeit zu aktivieren ([**d3d10 \_ Create \_ Device \_ Debug**](/windows/desktop/api/d3d10/ne-d3d10-d3d10_create_device_flag) Flag an [**D3D10CreateDevice**](/windows/desktop/api/d3d10misc/nf-d3d10misc-d3d10createdevice)).</span><span class="sxs-lookup"><span data-stu-id="37f92-316">The first step is to enable the debug runtime ([**D3D10\_CREATE\_DEVICE\_DEBUG**](/windows/desktop/api/d3d10/ne-d3d10-d3d10_create_device_flag) flag passed into [**D3D10CreateDevice**](/windows/desktop/api/d3d10misc/nf-d3d10misc-d3d10createdevice)).</span></span> <span data-ttu-id="37f92-317">Dadurch werden die häufigsten Fehler als Debugausgaben angezeigt.</span><span class="sxs-lookup"><span data-stu-id="37f92-317">This will expose the most common errors as debug output.</span></span>

</dd> <dt>

<span data-ttu-id="37f92-318"><span id="PIX_crashes_when_I_try_to_use_my_application_with_it.__"></span><span id="pix_crashes_when_i_try_to_use_my_application_with_it.__"></span><span id="PIX_CRASHES_WHEN_I_TRY_TO_USE_MY_APPLICATION_WITH_IT.__"></span>Pix stürzt ab, wenn ich versuche, meine Anwendung mit der Anwendung zu verwenden.</span><span class="sxs-lookup"><span data-stu-id="37f92-318"><span id="PIX_crashes_when_I_try_to_use_my_application_with_it.__"></span><span id="pix_crashes_when_i_try_to_use_my_application_with_it.__"></span><span id="PIX_CRASHES_WHEN_I_TRY_TO_USE_MY_APPLICATION_WITH_IT.__"></span>PIX crashes when I try to use my application with it.</span></span> 
</dt> <dd>

<span data-ttu-id="37f92-319">Der erste Schritt besteht darin, die Debug-Laufzeit zu aktivieren ([**d3d10 \_ Create \_ Device \_ Debug**](/windows/desktop/api/d3d10/ne-d3d10-d3d10_create_device_flag) Flag an [**D3D10CreateDevice**](/windows/desktop/api/d3d10misc/nf-d3d10misc-d3d10createdevice)).</span><span class="sxs-lookup"><span data-stu-id="37f92-319">The first step is to enable the debug runtime ([**D3D10\_CREATE\_DEVICE\_DEBUG**](/windows/desktop/api/d3d10/ne-d3d10-d3d10_create_device_flag) flag passed into [**D3D10CreateDevice**](/windows/desktop/api/d3d10misc/nf-d3d10misc-d3d10createdevice)).</span></span> <span data-ttu-id="37f92-320">Pix hat eine viel höhere Wahrscheinlichkeit, dass ein Absturz erfolgt, wenn die Debugausgabe nicht bereinigt ist.</span><span class="sxs-lookup"><span data-stu-id="37f92-320">PIX has a much higher probability of crashing if the debug output is not clean.</span></span>

</dd> <dt>

<span data-ttu-id="37f92-321"><span id="My_game_runs_out_of_virtual_address_space_on_32-bit_Vista_under_D3D10._It_does_not_have_problems_on_D3D9.__"></span><span id="my_game_runs_out_of_virtual_address_space_on_32-bit_vista_under_d3d10._it_does_not_have_problems_on_d3d9.__"></span><span id="MY_GAME_RUNS_OUT_OF_VIRTUAL_ADDRESS_SPACE_ON_32-BIT_VISTA_UNDER_D3D10._IT_DOES_NOT_HAVE_PROBLEMS_ON_D3D9.__"></span>Mein Spiel läuft auf dem 32-Bit-Vista unter d3d10 auf dem virtuellen Adressraum.</span><span class="sxs-lookup"><span data-stu-id="37f92-321"><span id="My_game_runs_out_of_virtual_address_space_on_32-bit_Vista_under_D3D10._It_does_not_have_problems_on_D3D9.__"></span><span id="my_game_runs_out_of_virtual_address_space_on_32-bit_vista_under_d3d10._it_does_not_have_problems_on_d3d9.__"></span><span id="MY_GAME_RUNS_OUT_OF_VIRTUAL_ADDRESS_SPACE_ON_32-BIT_VISTA_UNDER_D3D10._IT_DOES_NOT_HAVE_PROBLEMS_ON_D3D9.__"></span>My game runs out of virtual address space on 32-bit Vista under D3D10.</span></span> <span data-ttu-id="37f92-322">Auf d3d9 sind keine Probleme aufgetreten.</span><span class="sxs-lookup"><span data-stu-id="37f92-322">It does not have problems on D3D9.</span></span> 
</dt> <dd>

<span data-ttu-id="37f92-323">Bei d3d10 und dem virtuellen Adressraum sind einige Probleme aufgetreten.</span><span class="sxs-lookup"><span data-stu-id="37f92-323">There were some issues with D3D10 and virtual address space.</span></span> <span data-ttu-id="37f92-324">Dies wurde in [KB940105](https://support.microsoft.com/kb/940105)behoben.</span><span class="sxs-lookup"><span data-stu-id="37f92-324">This has been fixed in [KB940105](https://support.microsoft.com/kb/940105).</span></span> <span data-ttu-id="37f92-325">Wenn das Problem nicht behoben wird, stellen Sie sicher, dass Sie nicht mehr Ressourcen erstellen, die in d3d10 zugeordnet werden können, als Sie in d3d9 erstellt haben.</span><span class="sxs-lookup"><span data-stu-id="37f92-325">If that does not fix your problem, ensure you are not creating more resources that can be mapped (locked) in D3D10 than you were creating in D3D9.</span></span> <span data-ttu-id="37f92-326">Stellen Sie sich auch die Portierung auf 64-Bit vor, da dies in Zukunft häufiger wird.</span><span class="sxs-lookup"><span data-stu-id="37f92-326">Also think about porting to 64-bit since this will become more prevalent in the future.</span></span>

</dd> </dl>

## <a name="predicated-rendering"></a><span data-ttu-id="37f92-327">Prädikat Rendering</span><span class="sxs-lookup"><span data-stu-id="37f92-327">Predicated Rendering</span></span>

<dl> <dt>

<span data-ttu-id="37f92-328"><span id="I_used_Predicated_rendering__based_on_occlusion_query_results_._Why_is_my_app_still_the_same_speed___"></span><span id="i_used_predicated_rendering__based_on_occlusion_query_results_._why_is_my_app_still_the_same_speed___"></span><span id="I_USED_PREDICATED_RENDERING__BASED_ON_OCCLUSION_QUERY_RESULTS_._WHY_IS_MY_APP_STILL_THE_SAME_SPEED___"></span>Ich habe ein Prädikat Rendering verwendet (basierend auf den Ergebnissen der Okklusions Abfrage).</span><span class="sxs-lookup"><span data-stu-id="37f92-328"><span id="I_used_Predicated_rendering__based_on_occlusion_query_results_._Why_is_my_app_still_the_same_speed___"></span><span id="i_used_predicated_rendering__based_on_occlusion_query_results_._why_is_my_app_still_the_same_speed___"></span><span id="I_USED_PREDICATED_RENDERING__BASED_ON_OCCLUSION_QUERY_RESULTS_._WHY_IS_MY_APP_STILL_THE_SAME_SPEED___"></span>I used Predicated rendering (based on occlusion query results).</span></span> <span data-ttu-id="37f92-329">Warum wird meine APP immer noch dieselbe Geschwindigkeit haben?</span><span class="sxs-lookup"><span data-stu-id="37f92-329">Why is my app still the same speed?</span></span> 
</dt> <dd>

<span data-ttu-id="37f92-330">Stellen Sie zunächst sicher, dass das Rendering, das Sie überspringen möchten, tatsächlich der Anwendungs Engpass ist.</span><span class="sxs-lookup"><span data-stu-id="37f92-330">First, ensure that the rendering you would like to skip is actually the application bottleneck.</span></span> <span data-ttu-id="37f92-331">Wenn dies nicht der Engpass ist, wird beim Überspringen des Renderings nicht die Framerate unterstützt.</span><span class="sxs-lookup"><span data-stu-id="37f92-331">If it is not the bottleneck, then skipping the rendering will not help frame rate.</span></span>

<span data-ttu-id="37f92-332">Stellen Sie außerdem sicher, dass zwischen dem Problem der Abfrage und dem Rendering, das Sie als Prädikat festlegen möchten, genügend Zeit vergangen ist.</span><span class="sxs-lookup"><span data-stu-id="37f92-332">Second, make sure that enough time has passed between the issue of the query and rendering that you wish to predicate.</span></span> <span data-ttu-id="37f92-333">Wenn die Abfrage nicht durch den Zeitpunkt abgeschlossen ist, zu dem der renderingaufruf auf die GPU trifft, wird das Rendering trotzdem durchzuführen.</span><span class="sxs-lookup"><span data-stu-id="37f92-333">If the query has not finished by the time the render call hits the GPU, the rendering will occur anyway.</span></span>

<span data-ttu-id="37f92-334">Drittens überspringt das Prädikat nur bestimmte Aufrufe.</span><span class="sxs-lookup"><span data-stu-id="37f92-334">Third, predication only skips certain calls.</span></span> <span data-ttu-id="37f92-335">Die übersprungenen Aufrufe sind Draw, Clear, Copy, Update, resolvesubresource und generatemips.</span><span class="sxs-lookup"><span data-stu-id="37f92-335">The calls that are skipped are Draw, Clear, Copy, Update, ResolveSubresource and GenerateMips.</span></span> <span data-ttu-id="37f92-336">Die Zustands Einstellung, IA-Setup, Map und Create-Aufrufe berücksichtigen das Prädikat nicht.</span><span class="sxs-lookup"><span data-stu-id="37f92-336">State setting, IA setup, Map, and Create calls do not respect predication.</span></span> <span data-ttu-id="37f92-337">Wenn eine Menge von Zustands Einstellungs aufrufen für den Draw-Aufruf vorhanden ist, die als Prädikat verwendet werden sollen, werden diese Zustände weiterhin festgelegt.</span><span class="sxs-lookup"><span data-stu-id="37f92-337">If there are a lot of state setting calls around the draw call to be predicated, these states still will be set.</span></span>

</dd> </dl>

## <a name="geometry-shader"></a><span data-ttu-id="37f92-338">Geometrie-Shader</span><span class="sxs-lookup"><span data-stu-id="37f92-338">Geometry Shader</span></span>

<dl> <dt>

<span data-ttu-id="37f92-339"><span id="Should_I_use_the_geometry_shader_to_tessellate_my__insert_anything_here____"></span><span id="should_i_use_the_geometry_shader_to_tessellate_my__insert_anything_here____"></span><span id="SHOULD_I_USE_THE_GEOMETRY_SHADER_TO_TESSELLATE_MY__INSERT_ANYTHING_HERE____"></span>Sollte ich den Geometry-Shader verwenden, um "My" zu Mosaik (hier einfügen)?</span><span class="sxs-lookup"><span data-stu-id="37f92-339"><span id="Should_I_use_the_geometry_shader_to_tessellate_my__insert_anything_here____"></span><span id="should_i_use_the_geometry_shader_to_tessellate_my__insert_anything_here____"></span><span id="SHOULD_I_USE_THE_GEOMETRY_SHADER_TO_TESSELLATE_MY__INSERT_ANYTHING_HERE____"></span>Should I use the geometry shader to tessellate my (insert anything here)?</span></span> 
</dt> <dd>

<span data-ttu-id="37f92-340">Nein.</span><span class="sxs-lookup"><span data-stu-id="37f92-340">No.</span></span> <span data-ttu-id="37f92-341">Der Geometry-Shader sollte nicht für Mosaik verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="37f92-341">The geometry shader should NOT be used for tessellation.</span></span>

</dd> <dt>

<span data-ttu-id="37f92-342"><span id="Can_I_use_the_geometry_shader_to_create_geometry___"></span><span id="can_i_use_the_geometry_shader_to_create_geometry___"></span><span id="CAN_I_USE_THE_GEOMETRY_SHADER_TO_CREATE_GEOMETRY___"></span>Kann ich den Geometry-Shader zum Erstellen von Geometrie verwenden?</span><span class="sxs-lookup"><span data-stu-id="37f92-342"><span id="Can_I_use_the_geometry_shader_to_create_geometry___"></span><span id="can_i_use_the_geometry_shader_to_create_geometry___"></span><span id="CAN_I_USE_THE_GEOMETRY_SHADER_TO_CREATE_GEOMETRY___"></span>Can I use the geometry shader to create geometry?</span></span> 
</dt> <dd>

<span data-ttu-id="37f92-343">Ja, in sehr begrenzten Szenarios.</span><span class="sxs-lookup"><span data-stu-id="37f92-343">Yes, in very limited scenarios.</span></span> <span data-ttu-id="37f92-344">Der Geometry-Shader in aktuellen d3d10 (2008) teilen ist nicht für die Verarbeitung einer großen Erweiterung zuständig.</span><span class="sxs-lookup"><span data-stu-id="37f92-344">The geometry shader in current D3D10 (2008) parts is not equipped to handle much expansion.</span></span> <span data-ttu-id="37f92-345">Dies kann sich in Zukunft ändern.</span><span class="sxs-lookup"><span data-stu-id="37f92-345">This may change in the future.</span></span> <span data-ttu-id="37f92-346">Bei Video Karten Anbietern gibt es möglicherweise einen speziellen Pfad für einen bis vier Erweiterungen, weil Sie über eine vorhandene Hardware verfügen.</span><span class="sxs-lookup"><span data-stu-id="37f92-346">Video card vendors may have a special path for one to four expansions because of existing point-sprite hardware.</span></span> <span data-ttu-id="37f92-347">Alle anderen Erweiterungen müssten sehr eingeschränkt sein.</span><span class="sxs-lookup"><span data-stu-id="37f92-347">Any other expansion would have to be very limited.</span></span> <span data-ttu-id="37f92-348">Die Beispiele "particlesgs" und "pipesgs" erzielen hohe Frameraten, da nur eine begrenzte Erweiterung durchgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="37f92-348">The ParticlesGS and PipesGS samples achieve high frame rates by only doing limited expansion.</span></span> <span data-ttu-id="37f92-349">Pro Frame werden nur einige Punkte erweitert.</span><span class="sxs-lookup"><span data-stu-id="37f92-349">Only a few points are expanded per frame.</span></span>

</dd> <dt>

<span data-ttu-id="37f92-350"><span id="What_should_I_use_the_geometry_shader_for___"></span><span id="what_should_i_use_the_geometry_shader_for___"></span><span id="WHAT_SHOULD_I_USE_THE_GEOMETRY_SHADER_FOR___"></span>Wofür sollte ich den Geometry-Shader verwenden?</span><span class="sxs-lookup"><span data-stu-id="37f92-350"><span id="What_should_I_use_the_geometry_shader_for___"></span><span id="what_should_i_use_the_geometry_shader_for___"></span><span id="WHAT_SHOULD_I_USE_THE_GEOMETRY_SHADER_FOR___"></span>What should I use the geometry shader for?</span></span> 
</dt> <dd>

<span data-ttu-id="37f92-351">Alles, was Vorgänge für einen ganzen primitiven erfordert, wie z. b. die Silhouette-Erkennung, baryzentrische Koordinaten usw.</span><span class="sxs-lookup"><span data-stu-id="37f92-351">Anything that requires operations on an entire primitive such as silhouette detection, barycentric coordinates, and so on.</span></span> <span data-ttu-id="37f92-352">Verwenden Sie diese Option auch zum Auswählen des Slice eines renderzielarrays, an das primitive gesendet werden sollen.</span><span class="sxs-lookup"><span data-stu-id="37f92-352">Also use it to select which slice of a render target array to send primitives to.</span></span>

</dd> <dt>

<span data-ttu-id="37f92-353"><span id="Can_I_output_variable_amounts_of_geometry_from_the_geometry_shader___"></span><span id="can_i_output_variable_amounts_of_geometry_from_the_geometry_shader___"></span><span id="CAN_I_OUTPUT_VARIABLE_AMOUNTS_OF_GEOMETRY_FROM_THE_GEOMETRY_SHADER___"></span>Kann ich Variablen Mengen von Geometrie aus dem Geometry-Shader ausgeben?</span><span class="sxs-lookup"><span data-stu-id="37f92-353"><span id="Can_I_output_variable_amounts_of_geometry_from_the_geometry_shader___"></span><span id="can_i_output_variable_amounts_of_geometry_from_the_geometry_shader___"></span><span id="CAN_I_OUTPUT_VARIABLE_AMOUNTS_OF_GEOMETRY_FROM_THE_GEOMETRY_SHADER___"></span>Can I output variable amounts of geometry from the geometry shader?</span></span> 
</dt> <dd>

<span data-ttu-id="37f92-354">Ja, dies kann jedoch zu Leistungsproblemen führen.</span><span class="sxs-lookup"><span data-stu-id="37f92-354">Yes, but this can cause performance issues.</span></span> <span data-ttu-id="37f92-355">Betrachten Sie das Beispiel für die Ausgabe von 1 Punkt für einen Aufruf und 4 Punkte für einen anderen.</span><span class="sxs-lookup"><span data-stu-id="37f92-355">Take the example of outputting 1 point for one invocation and 4 points for another.</span></span> <span data-ttu-id="37f92-356">Bei der Anpassung innerhalb der Erweiterungs Richtlinien kann dies dazu führen, dass die Geometry-Shader-Threads serialisiert ausgeführt werden.</span><span class="sxs-lookup"><span data-stu-id="37f92-356">While fitting within the expansion guidelines, this can cause the geometry shader threads to run serially.</span></span>

</dd> <dt>

<span data-ttu-id="37f92-357"><span id="How_does_D3D10_know_how_to_generate_adjacency_indices_for_my_mesh__Or__why_does_D3D10_not_render_correctly_when_I_specify_that_the_geometry_shader_needs_adjacency_information.__"></span><span id="how_does_d3d10_know_how_to_generate_adjacency_indices_for_my_mesh__or__why_does_d3d10_not_render_correctly_when_i_specify_that_the_geometry_shader_needs_adjacency_information.__"></span><span id="HOW_DOES_D3D10_KNOW_HOW_TO_GENERATE_ADJACENCY_INDICES_FOR_MY_MESH__OR__WHY_DOES_D3D10_NOT_RENDER_CORRECTLY_WHEN_I_SPECIFY_THAT_THE_GEOMETRY_SHADER_NEEDS_ADJACENCY_INFORMATION.__"></span>Wie kann d3d10 wissen, wie Sie die einstellungsindizes für mein Mesh generieren?</span><span class="sxs-lookup"><span data-stu-id="37f92-357"><span id="How_does_D3D10_know_how_to_generate_adjacency_indices_for_my_mesh__Or__why_does_D3D10_not_render_correctly_when_I_specify_that_the_geometry_shader_needs_adjacency_information.__"></span><span id="how_does_d3d10_know_how_to_generate_adjacency_indices_for_my_mesh__or__why_does_d3d10_not_render_correctly_when_i_specify_that_the_geometry_shader_needs_adjacency_information.__"></span><span id="HOW_DOES_D3D10_KNOW_HOW_TO_GENERATE_ADJACENCY_INDICES_FOR_MY_MESH__OR__WHY_DOES_D3D10_NOT_RENDER_CORRECTLY_WHEN_I_SPECIFY_THAT_THE_GEOMETRY_SHADER_NEEDS_ADJACENCY_INFORMATION.__"></span>How does D3D10 know how to generate adjacency indices for my mesh?</span></span> <span data-ttu-id="37f92-358">Oder warum wird d3d10 nicht ordnungsgemäß Rendering, wenn angegeben wird, dass der Geometry-Shader Informationen zu Informationen benötigt.</span><span class="sxs-lookup"><span data-stu-id="37f92-358">Or, why does D3D10 not render correctly when I specify that the geometry shader needs adjacency information.</span></span> 
</dt> <dd>

<span data-ttu-id="37f92-359">Die Informationen zu den Informationen werden nicht von d3d10, sondern von der Anwendung erstellt.</span><span class="sxs-lookup"><span data-stu-id="37f92-359">The adjacency information is not created by D3D10, but by the application.</span></span> <span data-ttu-id="37f92-360">Die Indikations Indizes werden von der Anwendung generiert und müssen sechs Indizes pro primitiver Zeichen enthalten. die sechs nummerierten Indizes sind die Rand angrenzenden Vertices.</span><span class="sxs-lookup"><span data-stu-id="37f92-360">Adjacency indices are generated by the application and must contain six indices per primitive; of the six, the odd numbered indices are the edge adjacent vertices.</span></span> <span data-ttu-id="37f92-361">ID3DX10Mesh:: generatezuruencyandpoinzreps kann verwendet werden, um diese Daten zu generieren.</span><span class="sxs-lookup"><span data-stu-id="37f92-361">ID3DX10Mesh::GenerateAdjacencyAndPointsReps can be used to generate this data.</span></span>

</dd> </dl>

## <a name="hlsl"></a><span data-ttu-id="37f92-362">HLSL</span><span class="sxs-lookup"><span data-stu-id="37f92-362">HLSL</span></span>

<dl> <dt>

<span data-ttu-id="37f92-363"><span id="Are_integer_and_bitwise_instructions_slow___"></span><span id="are_integer_and_bitwise_instructions_slow___"></span><span id="ARE_INTEGER_AND_BITWISE_INSTRUCTIONS_SLOW___"></span>Sind ganzzahlige und bitweise Anweisungen langsam?</span><span class="sxs-lookup"><span data-stu-id="37f92-363"><span id="Are_integer_and_bitwise_instructions_slow___"></span><span id="are_integer_and_bitwise_instructions_slow___"></span><span id="ARE_INTEGER_AND_BITWISE_INSTRUCTIONS_SLOW___"></span>Are integer and bitwise instructions slow?</span></span> 
</dt> <dd>

<span data-ttu-id="37f92-364">Sie können sein.</span><span class="sxs-lookup"><span data-stu-id="37f92-364">They can be.</span></span> <span data-ttu-id="37f92-365">Verschiedene d3d10-Karten können nur ganzzahlige Vorgänge für eine Teilmenge der verfügbaren Alu-Einheiten ausgeben.</span><span class="sxs-lookup"><span data-stu-id="37f92-365">Various D3D10 cards may be able only to issue integer operations on a subset of the available ALU units.</span></span> <span data-ttu-id="37f92-366">Dies hängt stark von der Hardware ab.</span><span class="sxs-lookup"><span data-stu-id="37f92-366">This is highly dependent on the hardware.</span></span> <span data-ttu-id="37f92-367">Empfehlungen zum Umgang mit ganz Zahl Vorgängen auf der jeweiligen Hardware finden Sie unter Hardwarehersteller.</span><span class="sxs-lookup"><span data-stu-id="37f92-367">See your individual hardware vendor for recommendations on how to address integer operations on that particular hardware.</span></span> <span data-ttu-id="37f92-368">Seien Sie außerdem sehr vorsichtig bei Umwandlungen zwischen Typen.</span><span class="sxs-lookup"><span data-stu-id="37f92-368">Also, be very careful of casts between types.</span></span>

</dd> <dt>

<span data-ttu-id="37f92-369"><span id="What_happened_to_VPOS___"></span><span id="what_happened_to_vpos___"></span><span id="WHAT_HAPPENED_TO_VPOS___"></span>Was ist mit vpos passiert?</span><span class="sxs-lookup"><span data-stu-id="37f92-369"><span id="What_happened_to_VPOS___"></span><span id="what_happened_to_vpos___"></span><span id="WHAT_HAPPENED_TO_VPOS___"></span>What happened to VPOS?</span></span> 
</dt> <dd>

<span data-ttu-id="37f92-370">Wenn Sie eine Eingabe für den Pixelshader als SV- \_ Position deklarieren, erhalten Sie das gleiche Verhalten wie beim Deklarieren als vpos.</span><span class="sxs-lookup"><span data-stu-id="37f92-370">If you declare an input to your pixel shader as SV\_POSITION, you will get the same behavior as declaring it as VPOS.</span></span>

</dd> <dt>

<span data-ttu-id="37f92-371"><span id="How_do_I_sample_an_MSAA_texture___"></span><span id="how_do_i_sample_an_msaa_texture___"></span><span id="HOW_DO_I_SAMPLE_AN_MSAA_TEXTURE___"></span>Gewusst wie Beispiel für eine MSAA-Textur?</span><span class="sxs-lookup"><span data-stu-id="37f92-371"><span id="How_do_I_sample_an_MSAA_texture___"></span><span id="how_do_i_sample_an_msaa_texture___"></span><span id="HOW_DO_I_SAMPLE_AN_MSAA_TEXTURE___"></span>How do I sample an MSAA texture?</span></span> 
</dt> <dd>

<span data-ttu-id="37f92-372">Deklarieren Sie die Textur im Shader als Texture2DMS.</span><span class="sxs-lookup"><span data-stu-id="37f92-372">In your shader, declare your texture as Texture2DMS.</span></span> <span data-ttu-id="37f92-373">Anschließend können Sie einzelne Beispiele mithilfe der Beispiel Methoden aus dem Texture2DMS-Objekt abrufen.</span><span class="sxs-lookup"><span data-stu-id="37f92-373">You then can fetch individual samples using the Sample methods off of the Texture2DMS object.</span></span>

</dd> <dt>

<span data-ttu-id="37f92-374"><span id="How_do_I_tell_if_a_shader_variable_in_a_constant_buffer_actually_is_used___"></span><span id="how_do_i_tell_if_a_shader_variable_in_a_constant_buffer_actually_is_used___"></span><span id="HOW_DO_I_TELL_IF_A_SHADER_VARIABLE_IN_A_CONSTANT_BUFFER_ACTUALLY_IS_USED___"></span>Gewusst wie erkennen, ob eine Shader-Variable in einem konstanten Puffer tatsächlich verwendet wird?</span><span class="sxs-lookup"><span data-stu-id="37f92-374"><span id="How_do_I_tell_if_a_shader_variable_in_a_constant_buffer_actually_is_used___"></span><span id="how_do_i_tell_if_a_shader_variable_in_a_constant_buffer_actually_is_used___"></span><span id="HOW_DO_I_TELL_IF_A_SHADER_VARIABLE_IN_A_CONSTANT_BUFFER_ACTUALLY_IS_USED___"></span>How do I tell if a shader variable in a constant buffer actually is used?</span></span> 
</dt> <dd>

<span data-ttu-id="37f92-375">Sehen Sie sich die reflektierte d3d10 \_ Shader Variable Debug- \_ \_ Struktur für diese Variable an.</span><span class="sxs-lookup"><span data-stu-id="37f92-375">Look at the reflected D3D10\_SHADER\_VARIABLE\_DESC struct for that variable.</span></span> <span data-ttu-id="37f92-376">für uFlags sollte das \_ verwendete Flag d3d10 SVF \_ festgelegt sein.</span><span class="sxs-lookup"><span data-stu-id="37f92-376">uFlags should have the D3D10\_SVF\_USED flag set.</span></span>

</dd> <dt>

<span data-ttu-id="37f92-377"><span id="How_do_I_tell_if_a_shader_variable_in_a_constant_buffer_actually_is_using_FX10___"></span><span id="how_do_i_tell_if_a_shader_variable_in_a_constant_buffer_actually_is_using_fx10___"></span><span id="HOW_DO_I_TELL_IF_A_SHADER_VARIABLE_IN_A_CONSTANT_BUFFER_ACTUALLY_IS_USING_FX10___"></span>Gewusst wie erkennen, ob eine Shader-Variable in einem konstanten Puffer tatsächlich FX10 verwendet?</span><span class="sxs-lookup"><span data-stu-id="37f92-377"><span id="How_do_I_tell_if_a_shader_variable_in_a_constant_buffer_actually_is_using_FX10___"></span><span id="how_do_i_tell_if_a_shader_variable_in_a_constant_buffer_actually_is_using_fx10___"></span><span id="HOW_DO_I_TELL_IF_A_SHADER_VARIABLE_IN_A_CONSTANT_BUFFER_ACTUALLY_IS_USING_FX10___"></span>How do I tell if a shader variable in a constant buffer actually is using FX10?</span></span> 
</dt> <dd>

<span data-ttu-id="37f92-378">Dies ist derzeit nicht möglich, wenn Sie FX10 verwenden.</span><span class="sxs-lookup"><span data-stu-id="37f92-378">This currently is not possible using FX10.</span></span>

</dd> <dt>

<span data-ttu-id="37f92-379"><span id="I_have_no_control_over_constant_buffers_that_FX10_creates._How_are_they_created_and_updated___"></span><span id="i_have_no_control_over_constant_buffers_that_fx10_creates._how_are_they_created_and_updated___"></span><span id="I_HAVE_NO_CONTROL_OVER_CONSTANT_BUFFERS_THAT_FX10_CREATES._HOW_ARE_THEY_CREATED_AND_UPDATED___"></span>Ich habe keine Kontrolle über die Konstanten Puffer, die von FX10 erstellt werden.</span><span class="sxs-lookup"><span data-stu-id="37f92-379"><span id="I_have_no_control_over_constant_buffers_that_FX10_creates._How_are_they_created_and_updated___"></span><span id="i_have_no_control_over_constant_buffers_that_fx10_creates._how_are_they_created_and_updated___"></span><span id="I_HAVE_NO_CONTROL_OVER_CONSTANT_BUFFERS_THAT_FX10_CREATES._HOW_ARE_THEY_CREATED_AND_UPDATED___"></span>I have no control over constant buffers that FX10 creates.</span></span> <span data-ttu-id="37f92-380">Wie werden Sie erstellt und aktualisiert?</span><span class="sxs-lookup"><span data-stu-id="37f92-380">How are they created and updated?</span></span> 
</dt> <dd>

<span data-ttu-id="37f92-381">Alle FX10-verwalteten Konstanten Puffer werden als Standard Ressourcen für die d3d10 \_ -Verwendung erstellt \_ und mithilfe von updatesubresource aktualisiert.</span><span class="sxs-lookup"><span data-stu-id="37f92-381">All FX10-managed constant buffers are created as D3D10\_USAGE\_DEFAULT resources and are updated using UpdateSubresource.</span></span> <span data-ttu-id="37f92-382">Da FX10 einen Sicherungs Speicher für alle Konstanten Daten beibehält, ist updatesubresource der beste Ansatz zum Aktualisieren dieser Daten.</span><span class="sxs-lookup"><span data-stu-id="37f92-382">Because FX10 keeps a backing store of all constant data, UpdateSubresource is the best approach for updating these.</span></span>

</dd> <dt>

<span data-ttu-id="37f92-383"><span id="How_do_I_emulate_the_fixed_function_pipeline_using_shaders___"></span><span id="how_do_i_emulate_the_fixed_function_pipeline_using_shaders___"></span><span id="HOW_DO_I_EMULATE_THE_FIXED_FUNCTION_PIPELINE_USING_SHADERS___"></span>Gewusst wie die Pipeline mit der Fixed-Funktion mithilfe von Shadern emulieren?</span><span class="sxs-lookup"><span data-stu-id="37f92-383"><span id="How_do_I_emulate_the_fixed_function_pipeline_using_shaders___"></span><span id="how_do_i_emulate_the_fixed_function_pipeline_using_shaders___"></span><span id="HOW_DO_I_EMULATE_THE_FIXED_FUNCTION_PIPELINE_USING_SHADERS___"></span>How do I emulate the fixed function pipeline using shaders?</span></span> 
</dt> <dd>

<span data-ttu-id="37f92-384">Siehe fixedfuncemu Sample.</span><span class="sxs-lookup"><span data-stu-id="37f92-384">See FixedFuncEMU sample.</span></span>

</dd> <dt>

<span data-ttu-id="37f92-385"><span id="Should_I_use_the_new__unroll____loop____branch___and_so_on__compiler_hints___"></span><span id="should_i_use_the_new__unroll____loop____branch___and_so_on__compiler_hints___"></span><span id="SHOULD_I_USE_THE_NEW__UNROLL____LOOP____BRANCH___AND_SO_ON__COMPILER_HINTS___"></span>Sollten die neuen \[ \] \[ \] \[ compilerhinweise "auflösen", "Loop", "Branch" usw. verwendet \] werden?</span><span class="sxs-lookup"><span data-stu-id="37f92-385"><span id="Should_I_use_the_new__unroll____loop____branch___and_so_on__compiler_hints___"></span><span id="should_i_use_the_new__unroll____loop____branch___and_so_on__compiler_hints___"></span><span id="SHOULD_I_USE_THE_NEW__UNROLL____LOOP____BRANCH___AND_SO_ON__COMPILER_HINTS___"></span>Should I use the new \[unroll\], \[loop\], \[branch\], and so on, compiler hints?</span></span> 
</dt> <dd>

<span data-ttu-id="37f92-386">Im Allgemeinen nicht.</span><span class="sxs-lookup"><span data-stu-id="37f92-386">In general, no.</span></span> <span data-ttu-id="37f92-387">Der Compiler versucht häufig, beide Methoden zu verwenden und den schnellsten auszuwählen.</span><span class="sxs-lookup"><span data-stu-id="37f92-387">The compiler will often try both ways and choose the fastest one.</span></span> <span data-ttu-id="37f92-388">In einigen Fällen ist es möglicherweise erforderlich, die Registrierung zu verwenden \[ \] , z. b. Wenn ein Textur Abruf innerhalb einer Schleife Zugriff auf einen Farbverlauf benötigt.</span><span class="sxs-lookup"><span data-stu-id="37f92-388">In some cases, it may be necessary to use \[unroll\], for example, when a texture fetch inside a loop needs access to a gradient.</span></span>

</dd> <dt>

<span data-ttu-id="37f92-389"><span id="Does_partial_precision_make_any_difference_on_D3D10__I_can_specify_partial_precision_in_my_D3D9_HLSL__but_not_in_my_D3D10_HLSL.__"></span><span id="does_partial_precision_make_any_difference_on_d3d10__i_can_specify_partial_precision_in_my_d3d9_hlsl__but_not_in_my_d3d10_hlsl.__"></span><span id="DOES_PARTIAL_PRECISION_MAKE_ANY_DIFFERENCE_ON_D3D10__I_CAN_SPECIFY_PARTIAL_PRECISION_IN_MY_D3D9_HLSL__BUT_NOT_IN_MY_D3D10_HLSL.__"></span>Nimmt die partielle Genauigkeit einen Unterschied zu d3d10?</span><span class="sxs-lookup"><span data-stu-id="37f92-389"><span id="Does_partial_precision_make_any_difference_on_D3D10__I_can_specify_partial_precision_in_my_D3D9_HLSL__but_not_in_my_D3D10_HLSL.__"></span><span id="does_partial_precision_make_any_difference_on_d3d10__i_can_specify_partial_precision_in_my_d3d9_hlsl__but_not_in_my_d3d10_hlsl.__"></span><span id="DOES_PARTIAL_PRECISION_MAKE_ANY_DIFFERENCE_ON_D3D10__I_CAN_SPECIFY_PARTIAL_PRECISION_IN_MY_D3D9_HLSL__BUT_NOT_IN_MY_D3D10_HLSL.__"></span>Does partial precision make any difference on D3D10?</span></span> <span data-ttu-id="37f92-390">Ich kann eine partielle Genauigkeit in My d3d9 HLSL angeben, jedoch nicht in My d3d10 HLSL.</span><span class="sxs-lookup"><span data-stu-id="37f92-390">I can specify partial precision in my D3D9 HLSL, but not in my D3D10 HLSL.</span></span> 
</dt> <dd>

<span data-ttu-id="37f92-391">Alle d3d10-Vorgänge werden für die Ausführung mit einer Gleit Komma Genauigkeit von 32 Bit angegeben.</span><span class="sxs-lookup"><span data-stu-id="37f92-391">All D3D10 operations are specified to run at 32-bit floating point precision.</span></span> <span data-ttu-id="37f92-392">Daher sollte die partielle Genauigkeit keinen Unterschied in d3d10 haben.</span><span class="sxs-lookup"><span data-stu-id="37f92-392">Therefore, partial precision should not make any difference in D3D10.</span></span>

</dd> <dt>

<span data-ttu-id="37f92-393"><span id="In_D3D9__I_could_do_HW_PCF_shadow_filtering_by_binding_a_depth_buffer_as_a_texture_and_using_regular_tex2d_hlsl_instructions._How_do_I_do_this_on_D3D10___"></span><span id="in_d3d9__i_could_do_hw_pcf_shadow_filtering_by_binding_a_depth_buffer_as_a_texture_and_using_regular_tex2d_hlsl_instructions._how_do_i_do_this_on_d3d10___"></span><span id="IN_D3D9__I_COULD_DO_HW_PCF_SHADOW_FILTERING_BY_BINDING_A_DEPTH_BUFFER_AS_A_TEXTURE_AND_USING_REGULAR_TEX2D_HLSL_INSTRUCTIONS._HOW_DO_I_DO_THIS_ON_D3D10___"></span>In d3d9 könnte ich eine HW-PCF-Schatten Filterung durchführen, indem ich einen tiefen Puffer als Textur bindet und reguläre tex2d HLSL-Anweisungen verwende.</span><span class="sxs-lookup"><span data-stu-id="37f92-393"><span id="In_D3D9__I_could_do_HW_PCF_shadow_filtering_by_binding_a_depth_buffer_as_a_texture_and_using_regular_tex2d_hlsl_instructions._How_do_I_do_this_on_D3D10___"></span><span id="in_d3d9__i_could_do_hw_pcf_shadow_filtering_by_binding_a_depth_buffer_as_a_texture_and_using_regular_tex2d_hlsl_instructions._how_do_i_do_this_on_d3d10___"></span><span id="IN_D3D9__I_COULD_DO_HW_PCF_SHADOW_FILTERING_BY_BINDING_A_DEPTH_BUFFER_AS_A_TEXTURE_AND_USING_REGULAR_TEX2D_HLSL_INSTRUCTIONS._HOW_DO_I_DO_THIS_ON_D3D10___"></span>In D3D9, I could do HW PCF shadow filtering by binding a depth buffer as a texture and using regular tex2d hlsl instructions.</span></span> <span data-ttu-id="37f92-394">Gewusst wie dies auf d3d10?</span><span class="sxs-lookup"><span data-stu-id="37f92-394">How do I do this on D3D10?</span></span> 
</dt> <dd>

<span data-ttu-id="37f92-395">Sie müssen einen Vergleichs samplerstatus verwenden und samplecmp-Anweisungen verwenden.</span><span class="sxs-lookup"><span data-stu-id="37f92-395">You have to use a comparison sampler state and use SampleCmp instructions.</span></span>

</dd> <dt>

<span data-ttu-id="37f92-396"><span id="How_does_this_register_keyword_work_in_D3D10___"></span><span id="how_does_this_register_keyword_work_in_d3d10___"></span><span id="HOW_DOES_THIS_REGISTER_KEYWORD_WORK_IN_D3D10___"></span>Wie funktioniert dieses Registrierungs Schlüsselwort in d3d10?</span><span class="sxs-lookup"><span data-stu-id="37f92-396"><span id="How_does_this_register_keyword_work_in_D3D10___"></span><span id="how_does_this_register_keyword_work_in_d3d10___"></span><span id="HOW_DOES_THIS_REGISTER_KEYWORD_WORK_IN_D3D10___"></span>How does this register keyword work in D3D10?</span></span> 
</dt> <dd>

<span data-ttu-id="37f92-397">Das Register-Schlüsselwort in d3d10 gilt nun für den Slot, an den eine bestimmte Ressource gebunden ist.</span><span class="sxs-lookup"><span data-stu-id="37f92-397">The register keyword in D3D10 now applies to which slot a particular resource is bound to.</span></span> <span data-ttu-id="37f92-398">In diesem Fall kann die Ressource ein Puffer (konstant oder anderweitig), eine Textur oder ein Sampler sein.</span><span class="sxs-lookup"><span data-stu-id="37f92-398">In this case, the resource can be a Buffer (constant or otherwise), Texture, or Sampler.</span></span>

-   <span data-ttu-id="37f92-399">Verwenden Sie für konstante Puffer die Syntax: Register (bN), wobei N der Eingabe Slot (0-15) ist.</span><span class="sxs-lookup"><span data-stu-id="37f92-399">For constant buffers, use the syntax: register(bN), where N is the input slot (0-15)</span></span>
-   <span data-ttu-id="37f92-400">Verwenden Sie für Texturen die Syntax: Register (tN), wobei N der Eingabe Slot (0-127) ist.</span><span class="sxs-lookup"><span data-stu-id="37f92-400">For textures, use the syntax: register(tN), where N is the input slot (0-127)</span></span>
-   <span data-ttu-id="37f92-401">Verwenden Sie für Samplers die Syntax: Register (SN), wobei N der Eingabe Slot (0-127) ist.</span><span class="sxs-lookup"><span data-stu-id="37f92-401">For samplers, use the syntax: register(sN), where N is the input slot (0-127)</span></span>

</dd> <dt>

<span data-ttu-id="37f92-402"><span id="How_do_I_place_a_variable_inside_a_constant_buffer_if_register_is_just_used_to_specify_where_to_bind_the_entire_buffer___"></span><span id="how_do_i_place_a_variable_inside_a_constant_buffer_if_register_is_just_used_to_specify_where_to_bind_the_entire_buffer___"></span><span id="HOW_DO_I_PLACE_A_VARIABLE_INSIDE_A_CONSTANT_BUFFER_IF_REGISTER_IS_JUST_USED_TO_SPECIFY_WHERE_TO_BIND_THE_ENTIRE_BUFFER___"></span>Gewusst wie eine Variable innerhalb eines konstanten Puffers platzieren, wenn "Register" nur verwendet wird, um anzugeben, wo der gesamte Puffer gebunden werden soll?</span><span class="sxs-lookup"><span data-stu-id="37f92-402"><span id="How_do_I_place_a_variable_inside_a_constant_buffer_if_register_is_just_used_to_specify_where_to_bind_the_entire_buffer___"></span><span id="how_do_i_place_a_variable_inside_a_constant_buffer_if_register_is_just_used_to_specify_where_to_bind_the_entire_buffer___"></span><span id="HOW_DO_I_PLACE_A_VARIABLE_INSIDE_A_CONSTANT_BUFFER_IF_REGISTER_IS_JUST_USED_TO_SPECIFY_WHERE_TO_BIND_THE_ENTIRE_BUFFER___"></span>How do I place a variable inside a constant buffer if register is just used to specify where to bind the entire buffer?</span></span> 
</dt> <dd>

<span data-ttu-id="37f92-403">Verwenden Sie das packoffset-Schlüsselwort.</span><span class="sxs-lookup"><span data-stu-id="37f92-403">Use the packoffset keyword.</span></span> <span data-ttu-id="37f92-404">Das Argument für packoffset hat das Format c \[ 0-4095 \] . \[ x, y, z, w \] .</span><span class="sxs-lookup"><span data-stu-id="37f92-404">The argument to packoffset is in the form of c\[0-4095\].\[x,y,z,w\].</span></span> <span data-ttu-id="37f92-405">Beispiel:</span><span class="sxs-lookup"><span data-stu-id="37f92-405">For example:</span></span>

``` syntax
        cbuffer cbLotsOfEmptySpace
        {
        float   IWaste2Floats   : packoffset(c0.z);
        float4  IWasteMore  : packoffset(c13);
        };
```

<span data-ttu-id="37f92-406">In diesem Konstanten Puffer wird IWaste2Floats bei der dritten Gleit Komma Zahl (12. Byte) im Konstanten Puffer platziert.</span><span class="sxs-lookup"><span data-stu-id="37f92-406">In this constant buffer, IWaste2Floats is placed at the third float (12th byte) in the constant buffer.</span></span> <span data-ttu-id="37f92-407">Iwastemore wird am 13. float4 oder 52nd im Konstanten Puffer platziert.</span><span class="sxs-lookup"><span data-stu-id="37f92-407">IWasteMore is placed at the 13th float4 or 52nd float in the constant buffer.</span></span>

</dd> </dl>

 

 