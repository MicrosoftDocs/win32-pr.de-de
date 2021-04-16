---
description: Material beschreibt die Darstellung von Polygonen in einer 3D-Szene und die Anzeige von Licht.
ms.assetid: vs|directx_sdk|~\materials.htm
title: Material (Direct3D 9)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 64e75953fd5839e1b3e7b9cc89b7331147cdb585
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/06/2021
ms.locfileid: "104566661"
---
# <a name="materials-direct3d-9"></a><span data-ttu-id="a48b7-103">Material (Direct3D 9)</span><span class="sxs-lookup"><span data-stu-id="a48b7-103">Materials (Direct3D 9)</span></span>

<span data-ttu-id="a48b7-104">Material beschreibt die Darstellung von Polygonen in einer 3D-Szene und die Anzeige von Licht.</span><span class="sxs-lookup"><span data-stu-id="a48b7-104">Materials describe how polygons reflect light or appear to emit light in a 3D scene.</span></span> <span data-ttu-id="a48b7-105">Material Properties (Material Properties) erläutert die diffuser-Reflektion eines Materials, Ambient Reflection, Light-und Glanz Merkmale.</span><span class="sxs-lookup"><span data-stu-id="a48b7-105">Material properties detail a material's diffuse reflection, ambient reflection, light emission, and specular highlight characteristics.</span></span> <span data-ttu-id="a48b7-106">Direct3D verwendet die [**D3DMATERIAL9**](d3dmaterial9.md) -Struktur, um alle Material Eigenschafts Informationen zu übertragen.</span><span class="sxs-lookup"><span data-stu-id="a48b7-106">Direct3D uses the [**D3DMATERIAL9**](d3dmaterial9.md) structure to carry all material property information.</span></span> <span data-ttu-id="a48b7-107">Mit Ausnahme der Glanz Eigenschaft wird jede Eigenschaft als RGBA-Farbe beschrieben, die angibt, wie viel der roten, grünen und blauen Teile eines bestimmten Typs von Licht reflektiert wird, und ein Alpha Mischungs Faktor.</span><span class="sxs-lookup"><span data-stu-id="a48b7-107">With the exception of the specular property, each property is described as an RGBA color that represents how much of the red, green, and blue parts of a given type of light it reflects, and an alpha blending factor.</span></span>

## <a name="diffuse-and-ambient-reflection"></a><span data-ttu-id="a48b7-108">Diffuses und Ambient-Reflektion</span><span class="sxs-lookup"><span data-stu-id="a48b7-108">Diffuse and Ambient Reflection</span></span>

<span data-ttu-id="a48b7-109">Die diffusen und Ambient-Member der [**D3DMATERIAL9**](d3dmaterial9.md) -Struktur beschreiben, wie ein Material die Umgebungs-und diffuse Beleuchtung in einer Szene widerspiegelt.</span><span class="sxs-lookup"><span data-stu-id="a48b7-109">The Diffuse and Ambient members of the [**D3DMATERIAL9**](d3dmaterial9.md) structure describe how a material reflects the ambient and diffuse light in a scene.</span></span> <span data-ttu-id="a48b7-110">Da die meisten Szenen viel mehr diffuses Licht als Ambient-Light enthalten, spielt die diffuse Reflektion den größten Teil bei der Bestimmung der Farbe.</span><span class="sxs-lookup"><span data-stu-id="a48b7-110">Because most scenes contain much more diffuse light than ambient light, diffuse reflection plays the largest part in determining color.</span></span> <span data-ttu-id="a48b7-111">Da diffuses Licht direktional ist, wirkt sich der Winkel der Vorkommen für diffuses Licht außerdem auf die Gesamtintensität der Reflektion aus.</span><span class="sxs-lookup"><span data-stu-id="a48b7-111">Additionally, because diffuse light is directional, the angle of incidence for diffuse light affects the overall intensity of the reflection.</span></span> <span data-ttu-id="a48b7-112">Die diffuses Reflektion ist am größten, wenn das Licht einen Scheitelpunkt parallel zum Scheitelpunkt des Scheitel Punkts</span><span class="sxs-lookup"><span data-stu-id="a48b7-112">Diffuse reflection is greatest when the light strikes a vertex parallel to the vertex normal.</span></span> <span data-ttu-id="a48b7-113">Wenn sich der Winkel vergrößert, verringert sich die Auswirkung der diffusen Reflektion.</span><span class="sxs-lookup"><span data-stu-id="a48b7-113">As the angle increases, the effect of diffuse reflection diminishes.</span></span> <span data-ttu-id="a48b7-114">Der dargestellte Licht Wert ist der Kosinus des Winkels zwischen dem eingehenden Licht und dem Scheitelpunkt normal, wie in der folgenden Abbildung dargestellt.</span><span class="sxs-lookup"><span data-stu-id="a48b7-114">The amount of light reflected is the cosine of the angle between the incoming light and the vertex normal, as shown in the following illustration.</span></span>

![Darstellung der Menge der reflektierten Beleuchtung](images/incident.png)

<span data-ttu-id="a48b7-116">Ambient-Reflektion, wie Ambient Light, ist nicht direktional.</span><span class="sxs-lookup"><span data-stu-id="a48b7-116">Ambient reflection, like ambient light, is nondirectional.</span></span> <span data-ttu-id="a48b7-117">Ambient-Reflektion wirkt sich weniger auf die sichtbare Farbe eines gerenderten Objekts aus, wirkt sich aber auf die Gesamtfarbe aus und ist besonders bemerkbar, wenn wenig oder kein diffuses Licht das Material widerspiegelt.</span><span class="sxs-lookup"><span data-stu-id="a48b7-117">Ambient reflection has a lesser impact on the apparent color of a rendered object, but it does affect the overall color and is most noticeable when little or no diffuse light reflects off the material.</span></span> <span data-ttu-id="a48b7-118">Die Ambient-Reflektion eines Materials wird durch das Aufrufen der [**IDirect3DDevice9:: setrenderstate**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-setrenderstate) -Methode mit dem D3DRS Ambient-Flag von der Ambient-Lichtmenge beeinflusst \_ .</span><span class="sxs-lookup"><span data-stu-id="a48b7-118">A material's ambient reflection is affected by the ambient light set for a scene by calling the [**IDirect3DDevice9::SetRenderState**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-setrenderstate) method with the D3DRS\_AMBIENT flag.</span></span>

<span data-ttu-id="a48b7-119">Diffuses und Ambient Reflection arbeiten zusammen, um die wahrgenommene Farbe eines Objekts zu ermitteln, und sind in der Regel identische Werte.</span><span class="sxs-lookup"><span data-stu-id="a48b7-119">Diffuse and ambient reflection work together to determine the perceived color of an object, and are usually identical values.</span></span> <span data-ttu-id="a48b7-120">Zum Rendering eines blauen kristallinen Objekts erstellen Sie z. b. ein Material, das nur die blaue Komponente der diffuses und Ambient-hell darstellt.</span><span class="sxs-lookup"><span data-stu-id="a48b7-120">For example, to render a blue crystalline object, you create a material that reflects only the blue component of diffuse and ambient light.</span></span> <span data-ttu-id="a48b7-121">Wenn Sie in einem Raum mit einem weißen Licht platziert werden, scheint der Kristall blau zu sein.</span><span class="sxs-lookup"><span data-stu-id="a48b7-121">When placed in a room with a white light, the crystal appears to be blue.</span></span> <span data-ttu-id="a48b7-122">In einem Raum, der nur über ein rotes Licht verfügt, wäre der gleiche Kristall aber schwarz, da sein Material kein rotes Licht widerspiegelt.</span><span class="sxs-lookup"><span data-stu-id="a48b7-122">However, in a room that has only red light, the same crystal would appear to be black, because its material doesn't reflect red light.</span></span>

## <a name="emission"></a><span data-ttu-id="a48b7-123">Umwelt</span><span class="sxs-lookup"><span data-stu-id="a48b7-123">Emission</span></span>

<span data-ttu-id="a48b7-124">Material kann verwendet werden, um ein gerendertes Objekt scheinbar selbst zu gestalten.</span><span class="sxs-lookup"><span data-stu-id="a48b7-124">Materials can be used to make a rendered object appear to be self-luminous.</span></span> <span data-ttu-id="a48b7-125">Der emissive-Member der [**D3DMATERIAL9**](d3dmaterial9.md) -Struktur wird verwendet, um die Farbe und Transparenz des ausgegebenen Lichts zu beschreiben.</span><span class="sxs-lookup"><span data-stu-id="a48b7-125">The Emissive member of the [**D3DMATERIAL9**](d3dmaterial9.md) structure is used to describe the color and transparency of the emitted light.</span></span> <span data-ttu-id="a48b7-126">Die Berechnung wirkt sich auf die Farbe eines Objekts aus und kann z. b. ein dunkles Material heller machen und einen Teil der ausgegebenen Farbe annehmen.</span><span class="sxs-lookup"><span data-stu-id="a48b7-126">Emission affects an object's color and can, for example, make a dark material brighter and take on part of the emitted color.</span></span>

<span data-ttu-id="a48b7-127">Sie können die Eigenschaft "selbst leuchtendes" eines Materials verwenden, um die Illusion hinzuzufügen, dass ein Objekt Licht ausgibt, ohne dass der Berechnungs Aufwand für das Hinzufügen eines Lichts zur Szene entsteht.</span><span class="sxs-lookup"><span data-stu-id="a48b7-127">You can use a material's emissive property to add the illusion that an object is emitting light, without incurring the computational overhead of adding a light to the scene.</span></span> <span data-ttu-id="a48b7-128">Im Fall des blauen Kristalls ist die selbst leuchtendes-Eigenschaft nützlich, wenn Sie den Kristall anhellen, aber nicht für andere Objekte in der Szene umwandeln möchten.</span><span class="sxs-lookup"><span data-stu-id="a48b7-128">In the case of the blue crystal, the emissive property is useful if you want to make the crystal appear to light up, but not cast light on other objects in the scene.</span></span> <span data-ttu-id="a48b7-129">Beachten Sie, dass Materialien mit selbst leuchtendes-Eigenschaften kein Licht ausgeben, das von anderen Objekten in einer Szene reflektiert werden kann.</span><span class="sxs-lookup"><span data-stu-id="a48b7-129">Remember, materials with emissive properties don't emit light that can be reflected by other objects in a scene.</span></span> <span data-ttu-id="a48b7-130">Um diese reflektierte Beleuchtung zu erzielen, müssen Sie in der Szene ein zusätzliches Licht platzieren.</span><span class="sxs-lookup"><span data-stu-id="a48b7-130">To achieve this reflected light, you need to place an additional light within the scene.</span></span>

## <a name="specular-reflection"></a><span data-ttu-id="a48b7-131">Glanz Reflektion</span><span class="sxs-lookup"><span data-stu-id="a48b7-131">Specular Reflection</span></span>

<span data-ttu-id="a48b7-132">Die Glanz Reflektion erstellt Hervorhebungen für Objekte, sodass Sie glänzend erscheinen.</span><span class="sxs-lookup"><span data-stu-id="a48b7-132">Specular reflection creates highlights on objects, making them appear shiny.</span></span> <span data-ttu-id="a48b7-133">Die [**D3DMATERIAL9**](d3dmaterial9.md) -Struktur enthält zwei Member, die die Glanz Hervorhebungs Farbe und die Gesamtstruktur des Materials beschreiben.</span><span class="sxs-lookup"><span data-stu-id="a48b7-133">The [**D3DMATERIAL9**](d3dmaterial9.md) structure contains two members that describe the specular highlight color as well as the material's overall shininess.</span></span> <span data-ttu-id="a48b7-134">Sie legen die Farbe der Glanzlichter fest, indem Sie das Glanz Element auf die gewünschte RGBA-Farbe festlegen. die gebräuchlichsten Farben sind weiß oder hellgrau.</span><span class="sxs-lookup"><span data-stu-id="a48b7-134">You establish the color of the specular highlights by setting the Specular member to the desired RGBA color - the most common colors are white or light gray.</span></span> <span data-ttu-id="a48b7-135">Die Werte, die Sie im Power Member festlegen, Steuern, wie scharf die Glanzeffekte sind.</span><span class="sxs-lookup"><span data-stu-id="a48b7-135">The values you set in the Power member control how sharp the specular effects are.</span></span>

<span data-ttu-id="a48b7-136">Glanzlichter können zu drastischen Auswirkungen führen.</span><span class="sxs-lookup"><span data-stu-id="a48b7-136">Specular highlights can create dramatic effects.</span></span> <span data-ttu-id="a48b7-137">Das erneute zeichnen auf der blauen Crystal-Analogie: mit einem größeren Leistungswert werden schärfere Glanzlichter erzeugt, sodass der Kristall scheinbar ziemlich glänzend erscheint.</span><span class="sxs-lookup"><span data-stu-id="a48b7-137">Drawing again on the blue crystal analogy: a larger Power value creates sharper specular highlights, making the crystal appear to be quite shiny.</span></span> <span data-ttu-id="a48b7-138">Kleinere Werte vergrößern den Bereich des Effekts, wodurch eine langweilige Reflektion erstellt wird, die den Kristall Sinn macht.</span><span class="sxs-lookup"><span data-stu-id="a48b7-138">Smaller values increase the area of the effect, creating a dull reflection that make the crystal look frosty.</span></span> <span data-ttu-id="a48b7-139">Wenn Sie ein Objekt wirklich Matt machen möchten, legen Sie den-Wert für das-Element auf NULL und die Farbe in Glanz auf Schwarz fest.</span><span class="sxs-lookup"><span data-stu-id="a48b7-139">To make an object truly matte, set the Power member to zero and the color in Specular to black.</span></span> <span data-ttu-id="a48b7-140">Experimentieren Sie mit verschiedenen Reflexions Stufen, um eine realistische Darstellung Ihrer Bedürfnisse zu schaffen.</span><span class="sxs-lookup"><span data-stu-id="a48b7-140">Experiment with different levels of reflection to produce a realistic appearance for your needs.</span></span> <span data-ttu-id="a48b7-141">Die folgende Abbildung zeigt zwei identische Modelle.</span><span class="sxs-lookup"><span data-stu-id="a48b7-141">The following illustration shows two identical models.</span></span> <span data-ttu-id="a48b7-142">Auf der linken Seite wird eine Glanz Fähigkeit von 10 verwendet. das Modell auf der rechten Seite hat keine Glanz Reflektion.</span><span class="sxs-lookup"><span data-stu-id="a48b7-142">The one on the left uses a specular reflection power of 10; the model on the right has no specular reflection.</span></span>

![Abbildung von Glanz reflektionstypen](images/spechigh.png)

## <a name="setting-material-properties"></a><span data-ttu-id="a48b7-144">Festlegen von Material Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="a48b7-144">Setting Material Properties</span></span>

<span data-ttu-id="a48b7-145">Direct3D-renderinggeräte können jeweils mit einem Satz von Materialeigenschaften gerendert werden.</span><span class="sxs-lookup"><span data-stu-id="a48b7-145">Direct3D rendering devices can render with one set of material properties at a time.</span></span>

<span data-ttu-id="a48b7-146">In einer C++-Anwendung legen Sie die Materialeigenschaften fest, die das System verwendet, indem Sie eine [**D3DMATERIAL9**](d3dmaterial9.md) -Struktur vorbereiten und dann die [**IDirect3DDevice9:: setmaterial**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-setmaterial) -Methode aufrufen.</span><span class="sxs-lookup"><span data-stu-id="a48b7-146">In a C++ application, you set the material properties that the system uses by preparing a [**D3DMATERIAL9**](d3dmaterial9.md) structure, and then calling the [**IDirect3DDevice9::SetMaterial**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-setmaterial) method.</span></span>

<span data-ttu-id="a48b7-147">Um die [**D3DMATERIAL9**](d3dmaterial9.md) -Struktur für die Verwendung vorzubereiten, legen Sie die Eigenschafts Informationen in der-Struktur fest, um den gewünschten Effekt beim Rendern zu erzielen.</span><span class="sxs-lookup"><span data-stu-id="a48b7-147">To prepare the [**D3DMATERIAL9**](d3dmaterial9.md) structure for use, set the property information in the structure to create the desired effect during rendering.</span></span> <span data-ttu-id="a48b7-148">Im folgenden Codebeispiel wird die **D3DMATERIAL9** -Struktur für ein Violettes Material mit scharfen weißen Glanzlichtern eingerichtet.</span><span class="sxs-lookup"><span data-stu-id="a48b7-148">The following code example sets up the **D3DMATERIAL9** structure for a purple material with sharp white specular highlights.</span></span>


```
D3DMATERIAL9 mat;

// Set the RGBA for diffuse reflection.
mat.Diffuse.r = 0.5f;
mat.Diffuse.g = 0.0f;
mat.Diffuse.b = 0.5f;
mat.Diffuse.a = 1.0f;

// Set the RGBA for ambient reflection.
mat.Ambient.r = 0.5f;
mat.Ambient.g = 0.0f;
mat.Ambient.b = 0.5f;
mat.Ambient.a = 1.0f;

// Set the color and sharpness of specular highlights.
mat.Specular.r = 1.0f;
mat.Specular.g = 1.0f;
mat.Specular.b = 1.0f;
mat.Specular.a = 1.0f;
mat.Power = 50.0f;

// Set the RGBA for emissive color.
mat.Emissive.r = 0.0f;
mat.Emissive.g = 0.0f;
mat.Emissive.b = 0.0f;
mat.Emissive.a = 0.0f;
```



<span data-ttu-id="a48b7-149">Nachdem Sie die [**D3DMATERIAL9**](d3dmaterial9.md) -Struktur vorbereitet haben, wenden Sie die Eigenschaften an, indem Sie die [**IDirect3DDevice9:: setmaterial**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-setmaterial) -Methode des renderinggeräts aufrufen.</span><span class="sxs-lookup"><span data-stu-id="a48b7-149">After preparing the [**D3DMATERIAL9**](d3dmaterial9.md) structure, you apply the properties by calling the [**IDirect3DDevice9::SetMaterial**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-setmaterial) method of the rendering device.</span></span> <span data-ttu-id="a48b7-150">Diese Methode akzeptiert die Adresse einer vorbereiteten **D3DMATERIAL9** -Struktur als einzigen Parameter.</span><span class="sxs-lookup"><span data-stu-id="a48b7-150">This method accepts the address of a prepared **D3DMATERIAL9** structure as its only parameter.</span></span> <span data-ttu-id="a48b7-151">**IDirect3DDevice9:: setmaterial** kann nach Bedarf mit neuen Informationen aufgerufen werden, um die Materialeigenschaften für das Gerät zu aktualisieren.</span><span class="sxs-lookup"><span data-stu-id="a48b7-151">You can call **IDirect3DDevice9::SetMaterial** with new information as needed to update the material properties for the device.</span></span> <span data-ttu-id="a48b7-152">Das folgende Codebeispiel zeigt, wie dies im Code aussehen könnte.</span><span class="sxs-lookup"><span data-stu-id="a48b7-152">The following code example shows how this might look in code.</span></span>


```
// This code example uses the material properties defined for 
// the mat variable earlier in this topic. The pd3dDev is assumed
// to be a valid pointer to an IDirect3DDevice9 interface.
HRESULT hr;
hr = pd3dDev->SetMaterial(&mat);
if(FAILED(hr))
{
    // Code to handle the error goes here.
}
```



<span data-ttu-id="a48b7-153">Wenn Sie ein Direct3D-Gerät erstellen, wird das aktuelle Material automatisch auf den in der folgenden Tabelle angezeigten Standardwert festgelegt.</span><span class="sxs-lookup"><span data-stu-id="a48b7-153">When you create a Direct3D device, the current material is automatically set to the default shown in the following table.</span></span>



| <span data-ttu-id="a48b7-154">Member</span><span class="sxs-lookup"><span data-stu-id="a48b7-154">Member</span></span>   | <span data-ttu-id="a48b7-155">Wert</span><span class="sxs-lookup"><span data-stu-id="a48b7-155">Value</span></span>                |
|----------|----------------------|
| <span data-ttu-id="a48b7-156">Diffus</span><span class="sxs-lookup"><span data-stu-id="a48b7-156">Diffuse</span></span>  | <span data-ttu-id="a48b7-157">(R:0, g:0, b:0, a:0)</span><span class="sxs-lookup"><span data-stu-id="a48b7-157">(R:0, G:0, B:0, A:0)</span></span> |
| <span data-ttu-id="a48b7-158">Glänzend</span><span class="sxs-lookup"><span data-stu-id="a48b7-158">Specular</span></span> | <span data-ttu-id="a48b7-159">(R:0, g:0, b:0, a:0)</span><span class="sxs-lookup"><span data-stu-id="a48b7-159">(R:0, G:0, B:0, A:0)</span></span> |
| <span data-ttu-id="a48b7-160">Umgebend</span><span class="sxs-lookup"><span data-stu-id="a48b7-160">Ambient</span></span>  | <span data-ttu-id="a48b7-161">(R:0, g:0, b:0, a:0)</span><span class="sxs-lookup"><span data-stu-id="a48b7-161">(R:0, G:0, B:0, A:0)</span></span> |
| <span data-ttu-id="a48b7-162">Selbstleuchtend</span><span class="sxs-lookup"><span data-stu-id="a48b7-162">Emissive</span></span> | <span data-ttu-id="a48b7-163">(R:0, g:0, b:0, a:0)</span><span class="sxs-lookup"><span data-stu-id="a48b7-163">(R:0, G:0, B:0, A:0)</span></span> |
| <span data-ttu-id="a48b7-164">Leistung</span><span class="sxs-lookup"><span data-stu-id="a48b7-164">Power</span></span>    | <span data-ttu-id="a48b7-165">(0,0)</span><span class="sxs-lookup"><span data-stu-id="a48b7-165">(0.0)</span></span>                |



 

## <a name="retrieving-material-properties"></a><span data-ttu-id="a48b7-166">Abrufen von Material Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="a48b7-166">Retrieving Material Properties</span></span>

<span data-ttu-id="a48b7-167">Sie rufen die Materialeigenschaften ab, die das renderinggerät zurzeit durch Aufrufen der [**IDirect3DDevice9:: getmaterial**](/windows/desktop/api) -Methode für das Gerät verwendet.</span><span class="sxs-lookup"><span data-stu-id="a48b7-167">You retrieve the material properties that the rendering device is currently using by calling the [**IDirect3DDevice9::GetMaterial**](/windows/desktop/api) method for the device.</span></span> <span data-ttu-id="a48b7-168">Anders als bei der [**IDirect3DDevice9:: setmaterial**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-setmaterial) -Methode erfordert **IDirect3DDevice9:: getmaterial** keine Vorbereitung.</span><span class="sxs-lookup"><span data-stu-id="a48b7-168">Unlike the [**IDirect3DDevice9::SetMaterial**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-setmaterial) method, **IDirect3DDevice9::GetMaterial** doesn't require preparation.</span></span> <span data-ttu-id="a48b7-169">Die **IDirect3DDevice9:: getmaterial** -Methode akzeptiert die Adresse einer [**D3DMATERIAL9**](d3dmaterial9.md) -Struktur und füllt die bereitgestellte-Struktur mit Informationen auf, die die aktuellen Materialeigenschaften vor der Rückgabe beschreiben.</span><span class="sxs-lookup"><span data-stu-id="a48b7-169">The **IDirect3DDevice9::GetMaterial** method accepts the address of a [**D3DMATERIAL9**](d3dmaterial9.md) structure, and fills the provided structure with information describing the current material properties before returning.</span></span>


```
// For this example, the pd3dDev variable is assumed to 
// be a valid pointer to an IDirect3DDevice9 interface.
HRESULT hr;
D3DMATERIAL9 mat;

hr = pd3dDev->GetMaterial(&mat);
if(FAILED(hr))
{
    // Code to handle the error goes here.
}
```



> [!Note]  
> <span data-ttu-id="a48b7-170">Wenn die Anwendung keine Materialeigenschaften für das Rendering angibt, verwendet das System ein Standardmaterial.</span><span class="sxs-lookup"><span data-stu-id="a48b7-170">If your application does not specify material properties for rendering, the system uses a default material.</span></span> <span data-ttu-id="a48b7-171">Das Standardmaterial reflektiert alle diffusen Licht weißen, z. b. ohne Ambient-oder Glanz Reflektion und ohne selbst leuchtendes Farbe.</span><span class="sxs-lookup"><span data-stu-id="a48b7-171">The default material reflects all diffuse light - white, for example - with no ambient or specular reflection, and no emissive color.</span></span>

 

## <a name="related-topics"></a><span data-ttu-id="a48b7-172">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="a48b7-172">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="a48b7-173">Beleuchtung und Materialien</span><span class="sxs-lookup"><span data-stu-id="a48b7-173">Lights and Materials</span></span>](lights-and-materials.md)
</dt> </dl>

 

 
