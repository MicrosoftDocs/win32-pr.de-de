---
title: Ausgabe Register
description: Ausgabe Register
ms.assetid: 44148185-1051-44b9-afde-a2ecd76c829f
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: e4a0b397d17b841877796bd9c33432896208ed6d
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "104992751"
---
# <a name="output-registers"></a><span data-ttu-id="724fe-103">Ausgabe Register</span><span class="sxs-lookup"><span data-stu-id="724fe-103">Output Registers</span></span>

-   <span data-ttu-id="724fe-104">Vertex-Farb Register</span><span class="sxs-lookup"><span data-stu-id="724fe-104">Vertex Color Register</span></span>
-   <span data-ttu-id="724fe-105">Nebelregister</span><span class="sxs-lookup"><span data-stu-id="724fe-105">Fog Register</span></span>
-   <span data-ttu-id="724fe-106">Positions \_ Register</span><span class="sxs-lookup"><span data-stu-id="724fe-106">Position\_Register</span></span>
-   <span data-ttu-id="724fe-107">Punkt \_ Größe \_ registrieren</span><span class="sxs-lookup"><span data-stu-id="724fe-107">Point\_Size\_Register</span></span>
-   <span data-ttu-id="724fe-108">Textur \_ Koordinaten \_ Register</span><span class="sxs-lookup"><span data-stu-id="724fe-108">Texture\_Coordinate\_Register</span></span>

<span data-ttu-id="724fe-109">Register Namen wird ein Kleinbuchstabe o vorangestellt, der angibt, dass die Ausgabe Register schreibgeschützt sind.</span><span class="sxs-lookup"><span data-stu-id="724fe-109">Register names are preceded by a lowercase letter o, indicating that the output registers are write-only.</span></span>

## <a name="vertex-color-register---od0-od1"></a><span data-ttu-id="724fe-110">Vertex-Farb Register-oD0, oD1</span><span class="sxs-lookup"><span data-stu-id="724fe-110">Vertex Color Register - oD0, oD1</span></span>

<span data-ttu-id="724fe-111">oD0 ist das diffuse Farbregister.</span><span class="sxs-lookup"><span data-stu-id="724fe-111">oD0 is the diffuse color register.</span></span> <span data-ttu-id="724fe-112">oD1 ist das Glanz Farben Register.</span><span class="sxs-lookup"><span data-stu-id="724fe-112">oD1 is the specular color register.</span></span> <span data-ttu-id="724fe-113">Der oD0-Wert wird interpoliert und in das Eingabe Farbregister 0 (V0) des Pixel-Shaders geschrieben.</span><span class="sxs-lookup"><span data-stu-id="724fe-113">The oD0 value is interpolated and is written to the input color register 0 (v0) of the pixel shader.</span></span> <span data-ttu-id="724fe-114">Der oD1-Wert wird interpoliert und in das Eingabe Farbregister 1 (v1) des Pixel-Shaders geschrieben.</span><span class="sxs-lookup"><span data-stu-id="724fe-114">The oD1 value is interpolated and written to the input color register 1 (v1) of the pixel shader.</span></span> <span data-ttu-id="724fe-115">Weitere Informationen zu Pixel-Shader-Farb Registern finden Sie unter Registern.</span><span class="sxs-lookup"><span data-stu-id="724fe-115">For more information about pixel shader color registers, see Registers.</span></span>



| <span data-ttu-id="724fe-116">Vertex-Shader-Versionen</span><span class="sxs-lookup"><span data-stu-id="724fe-116">Vertex shader versions</span></span> | <span data-ttu-id="724fe-117">1\_1</span><span class="sxs-lookup"><span data-stu-id="724fe-117">1\_1</span></span> | <span data-ttu-id="724fe-118">2 \_ 0</span><span class="sxs-lookup"><span data-stu-id="724fe-118">2\_0</span></span> | <span data-ttu-id="724fe-119">2 \_ SW</span><span class="sxs-lookup"><span data-stu-id="724fe-119">2\_sw</span></span> | <span data-ttu-id="724fe-120">2 \_ x</span><span class="sxs-lookup"><span data-stu-id="724fe-120">2\_x</span></span> | <span data-ttu-id="724fe-121">3 \_ 0</span><span class="sxs-lookup"><span data-stu-id="724fe-121">3\_0</span></span> | <span data-ttu-id="724fe-122">3 \_ SW</span><span class="sxs-lookup"><span data-stu-id="724fe-122">3\_sw</span></span> |
|------------------------|------|------|-------|------|------|-------|
| <span data-ttu-id="724fe-123">Vertex-Farb Register</span><span class="sxs-lookup"><span data-stu-id="724fe-123">Vertex Color Register</span></span>  | <span data-ttu-id="724fe-124">x</span><span class="sxs-lookup"><span data-stu-id="724fe-124">x</span></span>    | <span data-ttu-id="724fe-125">x</span><span class="sxs-lookup"><span data-stu-id="724fe-125">x</span></span>    | <span data-ttu-id="724fe-126">x</span><span class="sxs-lookup"><span data-stu-id="724fe-126">x</span></span>     | <span data-ttu-id="724fe-127">x</span><span class="sxs-lookup"><span data-stu-id="724fe-127">x</span></span>    |      |       |



 

## <a name="fog-register---ofog"></a><span data-ttu-id="724fe-128">Nebelregister-ofog</span><span class="sxs-lookup"><span data-stu-id="724fe-128">Fog Register - oFog</span></span>

<span data-ttu-id="724fe-129">Der Ausgabe Nebel Wert wird registriert.</span><span class="sxs-lookup"><span data-stu-id="724fe-129">The output fog value registers.</span></span> <span data-ttu-id="724fe-130">Der Wert ist der zu interinterdende Nebel Faktor und wird dann an die Tabelle mit den Nebel geroutet.</span><span class="sxs-lookup"><span data-stu-id="724fe-130">The value is the fog factor to be interpolated and then routed to the fog table.</span></span> <span data-ttu-id="724fe-131">Es wird nur die skalarx-Komponente des Nebels verwendet.</span><span class="sxs-lookup"><span data-stu-id="724fe-131">Only the scalar x-component of the fog is used.</span></span> <span data-ttu-id="724fe-132">Werte werden zwischen null und eins geklammert, bevor Sie an den Rasterizer übergeben werden.</span><span class="sxs-lookup"><span data-stu-id="724fe-132">Values are clamped between zero and one before passing to the rasterizer.</span></span>



| <span data-ttu-id="724fe-133">Vertex-Shader-Versionen</span><span class="sxs-lookup"><span data-stu-id="724fe-133">Vertex shader versions</span></span> | <span data-ttu-id="724fe-134">1\_1</span><span class="sxs-lookup"><span data-stu-id="724fe-134">1\_1</span></span> | <span data-ttu-id="724fe-135">2 \_ 0</span><span class="sxs-lookup"><span data-stu-id="724fe-135">2\_0</span></span> | <span data-ttu-id="724fe-136">2 \_ SW</span><span class="sxs-lookup"><span data-stu-id="724fe-136">2\_sw</span></span> | <span data-ttu-id="724fe-137">2 \_ x</span><span class="sxs-lookup"><span data-stu-id="724fe-137">2\_x</span></span> | <span data-ttu-id="724fe-138">3 \_ 0</span><span class="sxs-lookup"><span data-stu-id="724fe-138">3\_0</span></span> | <span data-ttu-id="724fe-139">3 \_ SW</span><span class="sxs-lookup"><span data-stu-id="724fe-139">3\_sw</span></span> |
|------------------------|------|------|-------|------|------|-------|
| <span data-ttu-id="724fe-140">Nebelregister</span><span class="sxs-lookup"><span data-stu-id="724fe-140">Fog Register</span></span>           | <span data-ttu-id="724fe-141">x</span><span class="sxs-lookup"><span data-stu-id="724fe-141">x</span></span>    | <span data-ttu-id="724fe-142">x</span><span class="sxs-lookup"><span data-stu-id="724fe-142">x</span></span>    | <span data-ttu-id="724fe-143">x</span><span class="sxs-lookup"><span data-stu-id="724fe-143">x</span></span>     | <span data-ttu-id="724fe-144">x</span><span class="sxs-lookup"><span data-stu-id="724fe-144">x</span></span>    |      |       |



 

## <a name="position-register---opos"></a><span data-ttu-id="724fe-145">Positions Register-OPOS</span><span class="sxs-lookup"><span data-stu-id="724fe-145">Position Register - oPos</span></span>

<span data-ttu-id="724fe-146">Die Ausgabe Position wird registriert.</span><span class="sxs-lookup"><span data-stu-id="724fe-146">The output position registers.</span></span> <span data-ttu-id="724fe-147">Der Wert ist die Position im homogenen Clippingbereich.</span><span class="sxs-lookup"><span data-stu-id="724fe-147">The value is the position in homogeneous clipping space.</span></span> <span data-ttu-id="724fe-148">Dieser Wert muss vom Vertex-Shader geschrieben werden.</span><span class="sxs-lookup"><span data-stu-id="724fe-148">This value must be written by the vertex shader.</span></span>



| <span data-ttu-id="724fe-149">Vertex-Shader-Versionen</span><span class="sxs-lookup"><span data-stu-id="724fe-149">Vertex shader versions</span></span> | <span data-ttu-id="724fe-150">1\_1</span><span class="sxs-lookup"><span data-stu-id="724fe-150">1\_1</span></span> | <span data-ttu-id="724fe-151">2 \_ 0</span><span class="sxs-lookup"><span data-stu-id="724fe-151">2\_0</span></span> | <span data-ttu-id="724fe-152">2 \_ SW</span><span class="sxs-lookup"><span data-stu-id="724fe-152">2\_sw</span></span> | <span data-ttu-id="724fe-153">2 \_ x</span><span class="sxs-lookup"><span data-stu-id="724fe-153">2\_x</span></span> | <span data-ttu-id="724fe-154">3 \_ 0</span><span class="sxs-lookup"><span data-stu-id="724fe-154">3\_0</span></span> | <span data-ttu-id="724fe-155">3 \_ SW</span><span class="sxs-lookup"><span data-stu-id="724fe-155">3\_sw</span></span> |
|------------------------|------|------|-------|------|------|-------|
| <span data-ttu-id="724fe-156">Positions Register</span><span class="sxs-lookup"><span data-stu-id="724fe-156">Position Register</span></span>      | <span data-ttu-id="724fe-157">x</span><span class="sxs-lookup"><span data-stu-id="724fe-157">x</span></span>    | <span data-ttu-id="724fe-158">x</span><span class="sxs-lookup"><span data-stu-id="724fe-158">x</span></span>    | <span data-ttu-id="724fe-159">x</span><span class="sxs-lookup"><span data-stu-id="724fe-159">x</span></span>     | <span data-ttu-id="724fe-160">x</span><span class="sxs-lookup"><span data-stu-id="724fe-160">x</span></span>    |      |       |



 

## <a name="point-size-register---opts"></a><span data-ttu-id="724fe-161">Punktgröße registrieren-OPTS</span><span class="sxs-lookup"><span data-stu-id="724fe-161">Point Size Register - oPts</span></span>

<span data-ttu-id="724fe-162">Die Ausgabepunkt Größen Register.</span><span class="sxs-lookup"><span data-stu-id="724fe-162">The output point-size registers.</span></span> <span data-ttu-id="724fe-163">Es wird nur die skalare x-Komponente der Punktgröße verwendet.</span><span class="sxs-lookup"><span data-stu-id="724fe-163">Only the scalar x-component of the point size is used.</span></span>



| <span data-ttu-id="724fe-164">Vertex-Shader-Versionen</span><span class="sxs-lookup"><span data-stu-id="724fe-164">Vertex shader versions</span></span> | <span data-ttu-id="724fe-165">1\_1</span><span class="sxs-lookup"><span data-stu-id="724fe-165">1\_1</span></span> | <span data-ttu-id="724fe-166">2 \_ 0</span><span class="sxs-lookup"><span data-stu-id="724fe-166">2\_0</span></span> | <span data-ttu-id="724fe-167">2 \_ SW</span><span class="sxs-lookup"><span data-stu-id="724fe-167">2\_sw</span></span> | <span data-ttu-id="724fe-168">2 \_ x</span><span class="sxs-lookup"><span data-stu-id="724fe-168">2\_x</span></span> | <span data-ttu-id="724fe-169">3 \_ 0</span><span class="sxs-lookup"><span data-stu-id="724fe-169">3\_0</span></span> | <span data-ttu-id="724fe-170">3 \_ SW</span><span class="sxs-lookup"><span data-stu-id="724fe-170">3\_sw</span></span> |
|------------------------|------|------|-------|------|------|-------|
| <span data-ttu-id="724fe-171">Punktgröße registrieren</span><span class="sxs-lookup"><span data-stu-id="724fe-171">Point Size Register</span></span>    | <span data-ttu-id="724fe-172">x</span><span class="sxs-lookup"><span data-stu-id="724fe-172">x</span></span>    | <span data-ttu-id="724fe-173">x</span><span class="sxs-lookup"><span data-stu-id="724fe-173">x</span></span>    | <span data-ttu-id="724fe-174">x</span><span class="sxs-lookup"><span data-stu-id="724fe-174">x</span></span>     | <span data-ttu-id="724fe-175">x</span><span class="sxs-lookup"><span data-stu-id="724fe-175">x</span></span>    |      |       |



 

## <a name="texture-coordinate-register---ot0-to-ot7"></a><span data-ttu-id="724fe-176">Texturkoordinaten Register-oT0 to oT7</span><span class="sxs-lookup"><span data-stu-id="724fe-176">Texture Coordinate Register - oT0 to oT7</span></span>

<span data-ttu-id="724fe-177">Die Ausgabe Texturkoordinaten werden registriert.</span><span class="sxs-lookup"><span data-stu-id="724fe-177">The output texture coordinates registers.</span></span> <span data-ttu-id="724fe-178">Dabei handelt es sich hierbei um ein Array von Ausgabedaten Registern, die durchlaufen und als Texturkoordinaten durch die Textur-samplingphasen zum Weiterleiten von Daten an den Pixelshader verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="724fe-178">Specifically, these are an array of output data registers that are iterated and used as texture coordinates by the texture sampling stages routing data to the pixel shader.</span></span>



| <span data-ttu-id="724fe-179">Vertex-Shader-Versionen</span><span class="sxs-lookup"><span data-stu-id="724fe-179">Vertex shader versions</span></span>      | <span data-ttu-id="724fe-180">1\_1</span><span class="sxs-lookup"><span data-stu-id="724fe-180">1\_1</span></span> | <span data-ttu-id="724fe-181">2 \_ 0</span><span class="sxs-lookup"><span data-stu-id="724fe-181">2\_0</span></span> | <span data-ttu-id="724fe-182">2 \_ SW</span><span class="sxs-lookup"><span data-stu-id="724fe-182">2\_sw</span></span> | <span data-ttu-id="724fe-183">2 \_ x</span><span class="sxs-lookup"><span data-stu-id="724fe-183">2\_x</span></span> | <span data-ttu-id="724fe-184">3 \_ 0</span><span class="sxs-lookup"><span data-stu-id="724fe-184">3\_0</span></span> | <span data-ttu-id="724fe-185">3 \_ SW</span><span class="sxs-lookup"><span data-stu-id="724fe-185">3\_sw</span></span> |
|-----------------------------|------|------|-------|------|------|-------|
| <span data-ttu-id="724fe-186">Texturkoordinaten Register</span><span class="sxs-lookup"><span data-stu-id="724fe-186">Texture Coordinate Register</span></span> | <span data-ttu-id="724fe-187">x</span><span class="sxs-lookup"><span data-stu-id="724fe-187">x</span></span>    | <span data-ttu-id="724fe-188">x</span><span class="sxs-lookup"><span data-stu-id="724fe-188">x</span></span>    | <span data-ttu-id="724fe-189">x</span><span class="sxs-lookup"><span data-stu-id="724fe-189">x</span></span>     | <span data-ttu-id="724fe-190">x</span><span class="sxs-lookup"><span data-stu-id="724fe-190">x</span></span>    |      |       |



 

<span data-ttu-id="724fe-191">Beim Schreiben in ein Texturkoordinaten Register wird empfohlen, nur so viele Gleit Komma Werte wie die Dimension der entsprechenden Textur Zuordnung zu übergeben.</span><span class="sxs-lookup"><span data-stu-id="724fe-191">When writing to a texture coordinate register, it is recommended to pass only as many floating point values as the dimension of the corresponding texture map.</span></span> <span data-ttu-id="724fe-192">Steuern der mit einem-Modifizierer bestandenen Werte.</span><span class="sxs-lookup"><span data-stu-id="724fe-192">Control the values passed with a modifier.</span></span> <span data-ttu-id="724fe-193">Verwenden Sie beispielsweise. XY für eine 2D-Textur Zuordnung.</span><span class="sxs-lookup"><span data-stu-id="724fe-193">For example, use .xy for a 2D texture map.</span></span>

<span data-ttu-id="724fe-194">Wenn die Textur Projektion für eine Textur Phase aktiviert ist, müssen alle vier Gleit Komma Werte in das entsprechende Textur Register geschrieben werden.</span><span class="sxs-lookup"><span data-stu-id="724fe-194">When texture projection is enabled for a texture stage, all four floating point values must be written to the corresponding texture register.</span></span>

<span data-ttu-id="724fe-195">Jedes der D3DTTFF \* Textur Transformations Flags sollte NULL sein, wenn die programmierbare Pipeline verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="724fe-195">Any of the D3DTTFF\* texture transform flags should be zero when the programmable pipeline is being used.</span></span>

### <a name="texture-coordinate-range"></a><span data-ttu-id="724fe-196">Texturkoordinaten Bereich</span><span class="sxs-lookup"><span data-stu-id="724fe-196">Texture Coordinate Range</span></span>

<span data-ttu-id="724fe-197">Objekt-Vertex-Daten liefern Eingabe Texturkoordinaten.</span><span class="sxs-lookup"><span data-stu-id="724fe-197">Object vertex data supplies input texture coordinates.</span></span> <span data-ttu-id="724fe-198">Objekte, die keine gekachelten Texturen verwenden, weisen häufig Texturkoordinaten im Bereich von \[ 0 bis 1 auf \] .</span><span class="sxs-lookup"><span data-stu-id="724fe-198">Objects that do not used tiled textures commonly have texture coordinates in the range \[0,1\].</span></span> <span data-ttu-id="724fe-199">Objekte mit Kacheln, wie z. b. Terrain, haben in der Regel Texturkoordinaten, die von \[ -?, +? ab liegen \] ?</span><span class="sxs-lookup"><span data-stu-id="724fe-199">Objects that use tiled textures, such as terrain, typically have texture coordinates that range from \[-?,+?\] where ?</span></span> <span data-ttu-id="724fe-200">kann eine große Gleit Komma Zahl sein.</span><span class="sxs-lookup"><span data-stu-id="724fe-200">can be a large floating point number.</span></span>

<span data-ttu-id="724fe-201">Die Texturkoordinaten Interpolation wird für Scheitelpunkt Daten für die rasterisierung ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="724fe-201">Texture coordinate interpolation is performed on vertex data for rasterization.</span></span> <span data-ttu-id="724fe-202">Während der rasterisierung werden Texturkoordinaten zwischen Objekt Scheitel Punkten interpoliert, durch Textur Umbrüchen geändert und durch die Textur Größe (auch durch Berücksichtigung des Textur Adress Modus) skaliert, sodass ein ganzzahliger Index erzeugt wird.</span><span class="sxs-lookup"><span data-stu-id="724fe-202">During rasterization, texture coordinates are interpolated between object vertices, modified by texture wrapping and scaled by the texture size (also taking into account texture address mode) to produce an integer index.</span></span> <span data-ttu-id="724fe-203">Der Index wird dann verwendet, um eine Textur Suche auszuführen.</span><span class="sxs-lookup"><span data-stu-id="724fe-203">The index is then used to perform a texture lookup.</span></span> <span data-ttu-id="724fe-204">Mit MaxTextureRepeat kann bestimmt werden, wie oft eine Textur gekachelt werden kann.</span><span class="sxs-lookup"><span data-stu-id="724fe-204">MaxTextureRepeat can be used to determine how many times a texture can be tiled.</span></span>

<span data-ttu-id="724fe-205">Wenn Texturkoordinaten direkt in einem Pixelshader (mit texcoord oder texcrd) gelesen werden, hängt der Bereich der Textur Koordinate von der Anweisung und der Pixel-Shader-Version ab.</span><span class="sxs-lookup"><span data-stu-id="724fe-205">If texture coordinates are read directly into a pixel shader (using texcoord or texcrd), the texture coordinate range depends on the instruction and the pixel shader version.</span></span>

## <a name="related-topics"></a><span data-ttu-id="724fe-206">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="724fe-206">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="724fe-207">Vertex-Shader-Register</span><span class="sxs-lookup"><span data-stu-id="724fe-207">Vertex Shader Registers</span></span>](dx9-graphics-reference-asm-vs-registers.md)
</dt> </dl>

 

 




