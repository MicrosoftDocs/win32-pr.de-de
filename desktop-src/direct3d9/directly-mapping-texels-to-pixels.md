---
description: Beim Rendern der 2D-Ausgabe mithilfe von vortransformierten Scheitel Punkten muss sorgfältig vorgegangen werden, um sicherzustellen, dass jeder texturbereich ordnungsgemäß einem einzelnen Pixel Bereich entspricht. andernfalls kann eine Textur Verzerrung auftreten.
ms.assetid: 6faeb1e3-ea6e-4cb1-a1e6-2a9a81b4c0c7
title: Direkte Zuordnung von Texels zu Pixeln (Direct3D 9)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5f86e9d05acff402128ddb83fc97898ff6a21d7c
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/06/2021
ms.locfileid: "104213928"
---
# <a name="directly-mapping-texels-to-pixels-direct3d-9"></a><span data-ttu-id="2d9b9-103">Direkte Zuordnung von Texels zu Pixeln (Direct3D 9)</span><span class="sxs-lookup"><span data-stu-id="2d9b9-103">Directly Mapping Texels to Pixels (Direct3D 9)</span></span>

<span data-ttu-id="2d9b9-104">Beim Rendern der 2D-Ausgabe mithilfe von vortransformierten Scheitel Punkten muss sorgfältig vorgegangen werden, um sicherzustellen, dass jeder texturbereich ordnungsgemäß einem einzelnen Pixel Bereich entspricht. andernfalls kann eine Textur Verzerrung auftreten.</span><span class="sxs-lookup"><span data-stu-id="2d9b9-104">When rendering 2D output using pre-transformed vertices, care must be taken to ensure that each texel area correctly corresponds to a single pixel area, otherwise texture distortion can occur.</span></span> <span data-ttu-id="2d9b9-105">Wenn Sie die Grundlagen des Prozesses verstehen, den Direct3D bei der rasterisierung und Texturierung von Dreiecken befolgt, können Sie sicherstellen, dass Ihre Direct3D-Anwendung die 2D-Ausgabe korrekt</span><span class="sxs-lookup"><span data-stu-id="2d9b9-105">By understanding the basics of the process that Direct3D follows when rasterizing and texturing triangles, you can ensure your Direct3D application correctly renders 2D output.</span></span>

![Abbildung einer 6x6-Auflösungs Anzeige](images/maptex-fig1.png)

<span data-ttu-id="2d9b9-107">Das vorangehende Diagramm zeigt Pixel, die als Quadraten modelliert werden.</span><span class="sxs-lookup"><span data-stu-id="2d9b9-107">The preceding diagram shows pixels that are modeled as squares.</span></span> <span data-ttu-id="2d9b9-108">In der Realität sind Pixel jedoch Punkte und keine Quadrate.</span><span class="sxs-lookup"><span data-stu-id="2d9b9-108">In reality, however, pixels are dots, not squares.</span></span> <span data-ttu-id="2d9b9-109">Jedes Quadrat im vorangehenden Diagramm gibt den Bereich an, der durch das Pixel beleuchtet ist, aber ein Pixel ist immer nur ein Punkt in der Mitte eines Quadrats.</span><span class="sxs-lookup"><span data-stu-id="2d9b9-109">Each square in the preceding diagram indicates the area lit by the pixel, but a pixel is always just a dot at the center of a square.</span></span> <span data-ttu-id="2d9b9-110">Dieser Unterschied ist, obwohl er scheinbar klein ist, wichtig.</span><span class="sxs-lookup"><span data-stu-id="2d9b9-110">This distinction, though seemingly small, is important.</span></span> <span data-ttu-id="2d9b9-111">In der folgenden Abbildung ist eine bessere Darstellung der gleichen Anzeige dargestellt.</span><span class="sxs-lookup"><span data-stu-id="2d9b9-111">A better illustration of the same display is shown in the following diagram.</span></span>

![Abbildung einer Anzeige, die aus Pixeln besteht](images/maptex-fig2.png)

<span data-ttu-id="2d9b9-113">Das vorangehende Diagramm zeigt jedes physische Pixel ordnungsgemäß als Punkt in der Mitte der einzelnen Zellen an.</span><span class="sxs-lookup"><span data-stu-id="2d9b9-113">The preceding diagram correctly shows each physical pixel as a point in the center of each cell.</span></span> <span data-ttu-id="2d9b9-114">Die Bildschirmraum Koordinate (0,0) befindet sich direkt am oberen linken Pixel und somit in der Mitte der linken oberen Zelle.</span><span class="sxs-lookup"><span data-stu-id="2d9b9-114">The screen space coordinate (0, 0) is located directly at the top-left pixel, and therefore at the center of the top-left cell.</span></span> <span data-ttu-id="2d9b9-115">Die linke obere Ecke der Anzeige liegt daher bei (-0,5,-0,5), da es sich um 0,5 Zellen links und 0,5 Zellen aus dem oberen linken Pixel handelt.</span><span class="sxs-lookup"><span data-stu-id="2d9b9-115">The top-left corner of the display is therefore at (-0.5, -0.5) because it is 0.5 cells to the left and 0.5 cells up from the top-left pixel.</span></span> <span data-ttu-id="2d9b9-116">Direct3D führt ein vierfache mit Ecken bei (0,0) und (4, 4) aus, wie in der folgenden Abbildung dargestellt.</span><span class="sxs-lookup"><span data-stu-id="2d9b9-116">Direct3D will render a quad with corners at (0, 0) and (4, 4), as shown in the following illustration.</span></span>

![Darstellung eines Gliederung eines unrasterisierten Quad zwischen (0,0) und (4, 4)](images/maptex-fig3.png)

<span data-ttu-id="2d9b9-118">In der obigen Abbildung wird gezeigt, wo sich das mathematische Vierfache in Bezug auf die Anzeige befindet, aber nicht, wie das Vierfache aussehen wird Direct3D es wird ein-und an die Anzeige gesendet.</span><span class="sxs-lookup"><span data-stu-id="2d9b9-118">The preceding illustration shows where the mathematical quad is in relation to the display, but does not show what the quad will look like once Direct3D rasterizes it and sends it to the display.</span></span> <span data-ttu-id="2d9b9-119">In der Tat ist es für eine Raster Anzeige nicht möglich, das Vierfache genau wie gezeigt auszufüllen, da die Ränder des Quad nicht mit den Begrenzungen zwischen Pixel Zellen übereinstimmen.</span><span class="sxs-lookup"><span data-stu-id="2d9b9-119">In fact, it is impossible for a raster display to fill the quad exactly as shown because the edges of the quad do not coincide with the boundaries between pixel cells.</span></span> <span data-ttu-id="2d9b9-120">Anders ausgedrückt: Da jedes Pixel nur eine einzelne Farbe anzeigen kann, wird jede Pixel Zelle nur mit einer einzelnen Farbe gefüllt. Wenn die Anzeige das Vierfache genau wie gezeigt Rendern würde, müssten die Pixel Zellen entlang des viergs des vierels zwei unterschiedliche Farben anzeigen: blau, wobei durch das vierfach und weiß abgedeckt ist, wo nur der Hintergrund sichtbar ist.</span><span class="sxs-lookup"><span data-stu-id="2d9b9-120">In other words, because each pixel can only display a single color, each pixel cell is filled with only a single color; if the display were to render the quad exactly as shown, the pixel cells along the quad's edge would need to show two distinct colors: blue where covered by the quad and white where only the background is visible.</span></span>

<span data-ttu-id="2d9b9-121">Stattdessen wird die Grafikhardware dafür zuständig, zu bestimmen, welche Pixel aufgefüllt werden sollten, um das Vierfache zu überstehen.</span><span class="sxs-lookup"><span data-stu-id="2d9b9-121">Instead, the graphics hardware is tasked with determining which pixels should be filled to approximate the quad.</span></span> <span data-ttu-id="2d9b9-122">Dieser Prozess wird als rasterization bezeichnet und wird in [rasterisierungsregeln (Direct3D 9)](rasterization-rules.md)ausführlich erläutert.</span><span class="sxs-lookup"><span data-stu-id="2d9b9-122">This process is called rasterization, and is detailed in [Rasterization Rules (Direct3D 9)](rasterization-rules.md).</span></span> <span data-ttu-id="2d9b9-123">In diesem speziellen Fall wird das unregelmäßige Vierfache in der folgenden Abbildung dargestellt.</span><span class="sxs-lookup"><span data-stu-id="2d9b9-123">For this particular case, the rasterized quad is shown in the following illustration.</span></span>

![Abbildung eines unstrukturierten Quad von (0,0) bis (4, 4)](images/maptex-fig4.png)

<span data-ttu-id="2d9b9-125">Beachten Sie, dass das an Direct3D über gebene vierfache Ecken an (0,0) und (4, 4) aufweist, aber die gerastererte Ausgabe (die vorherige Abbildung) die Ecken (-0,5,-0,5) und (3,5, 3.5) enthält.</span><span class="sxs-lookup"><span data-stu-id="2d9b9-125">Note that the quad passed to Direct3D has corners at (0, 0) and (4, 4), but the rasterized output (the preceding illustration) has corners at (-0.5,-0.5) and (3.5,3.5).</span></span> <span data-ttu-id="2d9b9-126">Vergleichen Sie die vorangehenden beiden Abbildungen mit renderingunterschieden.</span><span class="sxs-lookup"><span data-stu-id="2d9b9-126">Compare the preceding two illustrations for rendering differences.</span></span> <span data-ttu-id="2d9b9-127">Wie Sie sehen, ist die tatsächliche Größe der Anzeige die richtige Größe, Sie wurde jedoch um-0,5 Zellen in der x-und y-Richtung verschoben.</span><span class="sxs-lookup"><span data-stu-id="2d9b9-127">You can see that what the display actually renders is the correct size, but has been shifted by -0.5 cells in the x and y directions.</span></span> <span data-ttu-id="2d9b9-128">Mit Ausnahme von Multisampling-Techniken ist dies jedoch die bestmögliche Näherung für das Vierfache.</span><span class="sxs-lookup"><span data-stu-id="2d9b9-128">However, except for multi-sampling techniques, this is the best possible approximation to the quad.</span></span> <span data-ttu-id="2d9b9-129">(Eine ausführliche Abdeckung von Multisampling finden Sie im [Beispiel für AntiAlias](https://msdn.microsoft.com/library/Ee415231(v=VS.85).aspx) .) Beachten Sie, dass der resultierende Bereich der Dimension 5 x 5 statt der gewünschten 4 x 4 ist, wenn der Raster jede Zelle gefüllt hat.</span><span class="sxs-lookup"><span data-stu-id="2d9b9-129">(See the [Antialias Sample](https://msdn.microsoft.com/library/Ee415231(v=VS.85).aspx) for thorough coverage of multi-sampling.) Be aware that if the rasterizer filled every cell the quad crossed, the resulting area would be of dimension 5 x 5 instead of the desired 4 x 4.</span></span>

<span data-ttu-id="2d9b9-130">Wenn Sie davon ausgehen, dass Bildschirm Koordinaten von der oberen linken Ecke des anzeigerasters anstatt vom oberen linken Pixel stammen, wird das Quad genau wie erwartet angezeigt.</span><span class="sxs-lookup"><span data-stu-id="2d9b9-130">If you assume that screen coordinates originate at the top-left corner of the display grid instead of the top-left pixel, the quad appears exactly as expected.</span></span> <span data-ttu-id="2d9b9-131">Der Unterschied wird jedoch deutlich, wenn dem Quad eine Textur zugewiesen wird.</span><span class="sxs-lookup"><span data-stu-id="2d9b9-131">However, the difference becomes clear when the quad is given a texture.</span></span> <span data-ttu-id="2d9b9-132">Die folgende Abbildung zeigt die 4 x 4-Textur, die Sie direkt dem Quad zuordnen.</span><span class="sxs-lookup"><span data-stu-id="2d9b9-132">The following illustration shows the 4 x 4 texture you'll map directly onto the quad.</span></span>

![Abbildung einer 4 x 4-Textur](images/maptex-fig5.png)

<span data-ttu-id="2d9b9-134">Da es sich bei der Textur um 4 x 4 texeln handelt und das Vierfache 4 x 4 Pixel beträgt, können Sie davon ausgehen, dass das eingetextete Quad genau wie die Textur angezeigt wird, unabhängig von der Position auf dem Bildschirm, an der das Vierfache gezeichnet wird</span><span class="sxs-lookup"><span data-stu-id="2d9b9-134">Because the texture is 4 x 4 texels and the quad is 4 x 4 pixels, you might expect the textured quad to appear exactly like the texture regardless of the location on the screen where the quad is drawn.</span></span> <span data-ttu-id="2d9b9-135">Dies ist jedoch nicht der Fall. sogar geringfügige Änderungen an der Position beeinflussen, wie die Textur angezeigt wird.</span><span class="sxs-lookup"><span data-stu-id="2d9b9-135">However, this is not the case; even slight changes in position influence how the texture is displayed.</span></span> <span data-ttu-id="2d9b9-136">In der folgenden Abbildung wird gezeigt, wie ein Quad zwischen (0,0) und (4, 4) angezeigt wird, nachdem es gerastert und strukturiert wurde.</span><span class="sxs-lookup"><span data-stu-id="2d9b9-136">The following illustration shows how a quad between (0, 0) and (4, 4) is displayed after being rasterized and textured.</span></span>

![Abbildung eines strukturierten Quad, gezeichnet von (0,0) und (4, 4)](images/maptex-fig6.png)

<span data-ttu-id="2d9b9-138">Das in der obigen Abbildung gezeichnete vierfache zeigt die texturierte Ausgabe (mit einem linearen Filter Modus und einem Klammer Adressierungs Modus) mit der übergeordneten gerastten Gliederung.</span><span class="sxs-lookup"><span data-stu-id="2d9b9-138">The quad drawn in the preceding illustration shows the textured output (with a linear filtering mode and a clamp addressing mode) with the superimposed rasterized outline.</span></span> <span data-ttu-id="2d9b9-139">Im weiteren Verlauf dieses Artikels wird erläutert, warum die Ausgabe so aussieht, wie Sie aussieht, anstatt Sie wie die Textur zu betrachten. für diejenigen, die die Projekt Mappe wünschen, ist dies der Grund: die Ränder der Eingabe Quad müssen auf den Begrenzungs Linien zwischen Pixel Zellen liegen.</span><span class="sxs-lookup"><span data-stu-id="2d9b9-139">The rest of this article explains exactly why the output looks the way it does instead of looking like the texture, but for those who want the solution, here it is: The edges of the input quad need to lie upon the boundary lines between pixel cells.</span></span> <span data-ttu-id="2d9b9-140">Wenn Sie die x-und y-Quad-Koordinaten einfach um-0,5-Einheiten bewegen, decken textezellen Pixel Zellen perfekt ab, und das Vierfache kann auf dem Bildschirm vollständig neu erstellt werden.</span><span class="sxs-lookup"><span data-stu-id="2d9b9-140">By simply shifting the x and y quad coordinates by -0.5 units, texel cells will perfectly cover pixel cells and the quad can be perfectly recreated on the screen.</span></span> <span data-ttu-id="2d9b9-141">(Die letzte Abbildung in diesem Thema zeigt den Quad an den korrigierten Koordinaten.)</span><span class="sxs-lookup"><span data-stu-id="2d9b9-141">(The last illustration in this topic shows the quad at the corrected coordinates.)</span></span>

<span data-ttu-id="2d9b9-142">Die Details, warum die gerasterte Ausgabe nur geringfügige Ähnlichkeit mit der Eingabe Textur hat, sind direkt mit der Art und Weise verknüpft, in der sich die Texturen Direct3D-Adressen und-Beispiele</span><span class="sxs-lookup"><span data-stu-id="2d9b9-142">The details of why the rasterized output only bears slight resemblance to the input texture are directly related to the way Direct3D addresses and samples textures.</span></span> <span data-ttu-id="2d9b9-143">Dabei wird davon ausgegangen, dass Sie über einen guten Einblick in den [Texturkoordinaten Bereich](texture-coordinates.md) und die [bilineare Textur Filterung](bilinear-texture-filtering.md)verfügen.</span><span class="sxs-lookup"><span data-stu-id="2d9b9-143">What follows assumes you have a good understanding of [texture coordinate space](texture-coordinates.md) And [bilinear texture filtering](bilinear-texture-filtering.md).</span></span>

<span data-ttu-id="2d9b9-144">Wenn wir uns mit der Untersuchung der seltsamen Pixel Ausgabe auseinander bewegen, ist es sinnvoll, die Ausgabe Farbe zurück zum Pixelshader zu verfolgen: der Pixelshader wird für jedes Pixel aufgerufen, das Teil der rasterisierten Form ist.</span><span class="sxs-lookup"><span data-stu-id="2d9b9-144">Getting back to our investigation of the strange pixel output, it makes sense to trace the output color back to the pixel shader: The pixel shader is called for each pixel selected to be part of the rasterized shape.</span></span> <span data-ttu-id="2d9b9-145">Das in einer früheren Abbildung gezeigte voll Bild blaue Quad könnte einen besonders einfachen Shader aufweisen:</span><span class="sxs-lookup"><span data-stu-id="2d9b9-145">The solid blue quad depicted in an earlier illustration could have a particularly simple shader:</span></span>


```
float4 SolidBluePS() : COLOR
{ 
    return float4( 0, 0, 1, 1 );
} 
```



<span data-ttu-id="2d9b9-146">Für das strukturierte vierfache muss der Pixelshader etwas geändert werden:</span><span class="sxs-lookup"><span data-stu-id="2d9b9-146">For the textured quad, the pixel shader has to be changed slightly:</span></span>


```
texture MyTexture;

sampler MySampler = 
sampler_state 
{ 
    Texture = <MyTexture>;
    MinFilter = Linear;
    MagFilter = Linear;
    AddressU = Clamp;
    AddressV = Clamp;
};

float4 TextureLookupPS( float2 vTexCoord : TEXCOORD0 ) : COLOR
{
    return tex2D( MySampler, vTexCoord );
} 
```



<span data-ttu-id="2d9b9-147">Dieser Code setzt voraus, dass die 4 x 4-Textur in MyTexture gespeichert wird.</span><span class="sxs-lookup"><span data-stu-id="2d9b9-147">That code assumes the 4 x 4 texture is stored in MyTexture.</span></span> <span data-ttu-id="2d9b9-148">Wie gezeigt, wird der mysampler-Textur Sampler so festgelegt, dass er eine bilineare Filterung auf MyTexture ausführt.</span><span class="sxs-lookup"><span data-stu-id="2d9b9-148">As shown, the MySampler texture sampler is set to perform bilinear filtering on MyTexture.</span></span> <span data-ttu-id="2d9b9-149">Der Pixelshader wird einmal für jedes gerastererte Pixel aufgerufen, und jedes Mal, wenn die zurückgegebene Farbe die Stichproben Textur Farbe bei vtexcoord ist.</span><span class="sxs-lookup"><span data-stu-id="2d9b9-149">The pixel shader gets called once for each rasterized pixel, and each time the returned color is the sampled texture color at vTexCoord.</span></span> <span data-ttu-id="2d9b9-150">Jedes Mal, wenn der Pixelshader aufgerufen wird, wird das vtexcoord-Argument auf die Texturkoordinaten an diesem Pixel festgelegt.</span><span class="sxs-lookup"><span data-stu-id="2d9b9-150">Each time the pixel shader is called, the vTexCoord argument is set to the texture coordinates at that pixel.</span></span> <span data-ttu-id="2d9b9-151">Dies bedeutet, dass der Shader den Textur Sampler an der genauen Position des Pixels an der genauen Position des Pixels anfordert, wie in der folgenden Abbildung dargestellt.</span><span class="sxs-lookup"><span data-stu-id="2d9b9-151">That means the shader is asking the texture sampler for the filtered texture color at the exact location of the pixel, as detailed in the following illustration.</span></span>

![Abbildung der Stichproben Positionen für Texturkoordinaten](images/maptex-fig7.png)

<span data-ttu-id="2d9b9-153">Die Textur (angezeigte übergeordnete Darstellung) wird direkt an Pixelpositionen (als schwarze Punkte angezeigt) entnommen.</span><span class="sxs-lookup"><span data-stu-id="2d9b9-153">The texture (shown superimposed) is sampled directly at pixel locations (shown as black dots).</span></span> <span data-ttu-id="2d9b9-154">Texturkoordinaten sind von der rasterisierung nicht betroffen (Sie verbleiben im projizierten Bildschirmbereich des ursprünglichen Quad).</span><span class="sxs-lookup"><span data-stu-id="2d9b9-154">Texture coordinates are not affected by rasterization (they remain in the projected screen-space of the original quad).</span></span> <span data-ttu-id="2d9b9-155">Die schwarzen Punkte zeigen an, wo die rasterisierungspixel liegen.</span><span class="sxs-lookup"><span data-stu-id="2d9b9-155">The black dots show where the rasterization pixels are.</span></span> <span data-ttu-id="2d9b9-156">Die Texturkoordinaten an jedem Pixel können leicht durch Interpolation der in jedem Scheitelpunkt gespeicherten Koordinaten bestimmt werden: das Pixel bei (0,0) stimmt mit dem Scheitelpunkt bei (0,0) überein. Daher sind die Texturkoordinaten an diesem Pixel einfach die Texturkoordinaten, die an diesem Scheitelpunkt, UV (0,0, 0,0), gespeichert sind.</span><span class="sxs-lookup"><span data-stu-id="2d9b9-156">The texture coordinates at each pixel are easily determined by interpolating the coordinates stored at each vertex: The pixel at (0,0) coincides with the vertex at (0, 0); therefore, the texture coordinates at that pixel are simply the texture coordinates stored at that vertex, UV (0.0, 0.0).</span></span> <span data-ttu-id="2d9b9-157">Für das Pixel um (3, 1) sind die interpoliert-Koordinaten "UV (0,75, 0,25)", da sich dieses Pixel in drei Vierteln der Textur Breite und ein vierstel seiner Höhe befindet.</span><span class="sxs-lookup"><span data-stu-id="2d9b9-157">For the pixel at (3, 1), the interpolated coordinates are UV (0.75, 0.25) because that pixel is located at three-fourths of the texture's width and one-fourth of its height.</span></span> <span data-ttu-id="2d9b9-158">Diese interpoliert-Koordinaten werden an den Pixelshader übermittelt.</span><span class="sxs-lookup"><span data-stu-id="2d9b9-158">These interpolated coordinates are what get passed to the pixel shader.</span></span>

<span data-ttu-id="2d9b9-159">Die texeln sind in diesem Beispiel nicht mit den Pixeln identisch. jedes Pixel (und somit jeder Stichproben Punkt) wird in der Ecke von vier texeln positioniert.</span><span class="sxs-lookup"><span data-stu-id="2d9b9-159">The texels do not line up with the pixels in this example; each pixel (and therefore each sampling point) is positioned at the corner of four texels.</span></span> <span data-ttu-id="2d9b9-160">Da der Filter Modus auf Linear festgelegt ist, durchläuft der Sampler die Farben der vier texeln, die diese Ecke teilen.</span><span class="sxs-lookup"><span data-stu-id="2d9b9-160">Because the filtering mode is set to Linear, the sampler will average the colors of the four texels sharing that corner.</span></span> <span data-ttu-id="2d9b9-161">Dadurch wird erläutert, warum das Pixel, das als rot erwartet wird, tatsächlich aus drei viertem Grau plus einem vierten rot besteht. das Pixel, das grün sein soll, ist ein Halbton Grau plus ein viertes rot plus ein viertes grün usw.</span><span class="sxs-lookup"><span data-stu-id="2d9b9-161">This explains why the pixel expected to be red is actually three-fourths gray plus one-fourth red, the pixel expected to be green is one-half gray plus one-fourth red plus one-fourth green, and so on.</span></span>

<span data-ttu-id="2d9b9-162">Um dieses Problem zu beheben, müssen Sie lediglich das Vierfache zu den Pixeln zuordnen, zu denen es gerengt wird, und die texeln ordnungsgemäß den Pixeln zuordnen.</span><span class="sxs-lookup"><span data-stu-id="2d9b9-162">To fix this problem, all you need to do is correctly map the quad to the pixels to which it will be rasterized, and thereby correctly map the texels to pixels.</span></span> <span data-ttu-id="2d9b9-163">In der folgenden Abbildung sind die Ergebnisse der Zeichnung desselben viervieres zwischen (-0,5,-0,5) und (3,5, 3,5) dargestellt. Dies ist der von Anfang an vorgesehene Quad.</span><span class="sxs-lookup"><span data-stu-id="2d9b9-163">The following illustration shows the results of drawing the same quad between (-0.5, -0.5) and (3.5, 3.5), which is the quad intended from the outset.</span></span>

![Abbildung eines strukturierten Quad, das mit dem rasterisierten Quad übereinstimmt](images/maptex-fig8.png)

<span data-ttu-id="2d9b9-165">In der obigen Abbildung wird veranschaulicht, dass das Quad (dargestellt von (-0,5,-0,5) bis (3,5, 3,5)) exakt mit dem rasterisierten Bereich übereinstimmt.</span><span class="sxs-lookup"><span data-stu-id="2d9b9-165">The preceding illustration demonstrates that the quad (shown outlined from (-0.5, -0.5) to (3.5, 3.5)) exactly matches the rasterized area.</span></span>

## <a name="summary"></a><span data-ttu-id="2d9b9-166">Zusammenfassung</span><span class="sxs-lookup"><span data-stu-id="2d9b9-166">Summary</span></span>

<span data-ttu-id="2d9b9-167">Zusammenfassend sind Pixel und texeln tatsächlich Punkte, keine Solid-Blöcke.</span><span class="sxs-lookup"><span data-stu-id="2d9b9-167">In summary, pixels and texels are actually points, not solid blocks.</span></span> <span data-ttu-id="2d9b9-168">Der Bildschirmbereich stammt vom oberen linken Pixel, aber die Texturkoordinaten stammen von der oberen linken Ecke des Struktur Rasters.</span><span class="sxs-lookup"><span data-stu-id="2d9b9-168">Screen space originates at the top-left pixel, but texture coordinates originate at the top-left corner of the texture's grid.</span></span> <span data-ttu-id="2d9b9-169">Am wichtigsten ist, dass Sie 0,5 Einheiten von den x-und y-Komponenten Ihrer Scheitelpunkt Positionen subtrahieren, wenn Sie in transformier ter Bildschirmfläche arbeiten, um texeln ordnungsgemäß mit Pixel auszurichten.</span><span class="sxs-lookup"><span data-stu-id="2d9b9-169">Most importantly, remember to subtract 0.5 units from the x and y components of your vertex positions when working in transformed screen space in order to correctly align texels with pixels.</span></span>

<span data-ttu-id="2d9b9-170">Der folgende Code ist ein Beispiel für das versetzen der Scheitel Punkte eines 256 256-Quadrat-Quadrats zum ordnungsgemäßen Anzeigen der Textur 256 by 256 im transformierten Bildschirmbereich.</span><span class="sxs-lookup"><span data-stu-id="2d9b9-170">The following code is an example of offsetting the vertices of a 256 by 256 square to properly display a 256 by 256 texture in transformed screen space.</span></span>


```C++
//define FVF with vertex values in transformed screen space
#define D3DFVF_CUSTOMVERTEX (D3DFVF_XYZRHW|D3DFVF_TEX1)

struct CUSTOMVERTEX
{
    FLOAT x, y, z, rhw; // position
    FLOAT tu, tv;       // texture coordinates
};

//unadjusted vertex values
float left = 0.0f;
float right = 255.0f;
float top = 0.0f;
float bottom = 255.0f;


//256 by 256 rectangle matching 256 by 256 texture
CUSTOMVERTEX vertices[] =
{
    { left,  top,    0.5f, 1.0f, 0.0f, 0.0f}, // x, y, z, rhw, u, v
    { right, top,    0.5f, 1.0f, 1.0f, 0.0f},
    { right, bottom, 0.5f, 1.0f, 1.0f, 1.0f},
    { left,  top,    0.5f, 1.0f, 0.0f, 0.0f},
    { right, bottom, 0.5f, 1.0f, 1.0f, 1.0f},
    { left,  bottom, 0.5f, 1.0f, 0.0f, 1.0f},
    
};
```




```C++
//adjust all the vertices to correctly line up texels with pixels 
for (int i=0; i<6; i++)
{
    vertices[i].x -= 0.5f;
    vertices[i].y -= 0.5f;
}
```



## <a name="related-topics"></a><span data-ttu-id="2d9b9-171">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="2d9b9-171">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="2d9b9-172">Texturkoordinaten</span><span class="sxs-lookup"><span data-stu-id="2d9b9-172">Texture Coordinates</span></span>](texture-coordinates.md)
</dt> </dl>

 

 



