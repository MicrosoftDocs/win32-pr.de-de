---
description: Die emissive-Beleuchtung wird durch einen einzelnen Begriff beschrieben.
ms.assetid: b6ccf274-a6c5-4b26-8c43-c857c2c24e0f
title: Emissive-Beleuchtung (Direct3D 9)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 19cb0566d2409fb68e5fbbdca1cc609c31120e95
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/06/2021
ms.locfileid: "106343119"
---
# <a name="emissive-lighting-direct3d-9"></a><span data-ttu-id="6419a-103">Emissive-Beleuchtung (Direct3D 9)</span><span class="sxs-lookup"><span data-stu-id="6419a-103">Emissive Lighting (Direct3D 9)</span></span>

<span data-ttu-id="6419a-104">Die emissive-Beleuchtung wird durch einen einzelnen Begriff beschrieben.</span><span class="sxs-lookup"><span data-stu-id="6419a-104">Emissive lighting is described by a single term.</span></span>

<span data-ttu-id="6419a-105">Emissive Beleuchtung = c ₑ</span><span class="sxs-lookup"><span data-stu-id="6419a-105">Emissive Lighting = Cₑ</span></span>

<span data-ttu-id="6419a-106">Hierbei gilt:</span><span class="sxs-lookup"><span data-stu-id="6419a-106">Where:</span></span>



| <span data-ttu-id="6419a-107">Parameter</span><span class="sxs-lookup"><span data-stu-id="6419a-107">Parameter</span></span> | <span data-ttu-id="6419a-108">Standardwert</span><span class="sxs-lookup"><span data-stu-id="6419a-108">Default value</span></span> | <span data-ttu-id="6419a-109">type</span><span class="sxs-lookup"><span data-stu-id="6419a-109">Type</span></span>          | <span data-ttu-id="6419a-110">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="6419a-110">Description</span></span>     |
|-----------|---------------|---------------|-----------------|
| <span data-ttu-id="6419a-111">C ₑ</span><span class="sxs-lookup"><span data-stu-id="6419a-111">Cₑ</span></span>        | <span data-ttu-id="6419a-112">(0, 0, 0, 0)</span><span class="sxs-lookup"><span data-stu-id="6419a-112">(0,0,0,0)</span></span>     | <span data-ttu-id="6419a-113">D3DCOLORVALUE</span><span class="sxs-lookup"><span data-stu-id="6419a-113">D3DCOLORVALUE</span></span> | <span data-ttu-id="6419a-114">Emissive-Farbe.</span><span class="sxs-lookup"><span data-stu-id="6419a-114">Emissive color.</span></span> |



 

<span data-ttu-id="6419a-115">Der Wert für c ₑ lautet wie folgt:</span><span class="sxs-lookup"><span data-stu-id="6419a-115">The value for Cₑ is either:</span></span>

-   <span data-ttu-id="6419a-116">Vertex color1, wenn emissivematerialsource = D3DMCS \_ color1 und die erste Scheitelpunkt Farbe in der Vertex-Deklaration angegeben wird.</span><span class="sxs-lookup"><span data-stu-id="6419a-116">vertex color1, if EMISSIVEMATERIALSOURCE = D3DMCS\_COLOR1, and the first vertex color is supplied in the vertex declaration.</span></span>
-   <span data-ttu-id="6419a-117">Vertex color2, wenn emissivematerialsource = D3DMCS \_ color2 und die zweite Scheitelpunkt Farbe in der Vertex-Deklaration angegeben wird.</span><span class="sxs-lookup"><span data-stu-id="6419a-117">vertex color2, if EMISSIVEMATERIALSOURCE = D3DMCS\_COLOR2, and the second vertex color is supplied in the vertex declaration.</span></span>
-   <span data-ttu-id="6419a-118">Material-selbst leuchtendes-Farbe</span><span class="sxs-lookup"><span data-stu-id="6419a-118">material emissive color</span></span>

> [!Note]  
> <span data-ttu-id="6419a-119">Wenn eine der Optionen "emissivematerialsource" verwendet wird und die Scheitelpunkt Farbe nicht angegeben wird, wird die selbst leuchtendes-Farbe des Materials verwendet.</span><span class="sxs-lookup"><span data-stu-id="6419a-119">If either EMISSIVEMATERIALSOURCE option is used, and the vertex color is not provided, the material emissive color is used.</span></span>

 

## <a name="example"></a><span data-ttu-id="6419a-120">Beispiel</span><span class="sxs-lookup"><span data-stu-id="6419a-120">Example</span></span>

<span data-ttu-id="6419a-121">In diesem Beispiel wird das-Objekt mithilfe der Szene Ambient Light und einer Material Ambient-Farbe gefärbt.</span><span class="sxs-lookup"><span data-stu-id="6419a-121">In this example, the object is colored using the scene ambient light and a material ambient color.</span></span> <span data-ttu-id="6419a-122">Der Code wird unten dargestellt.</span><span class="sxs-lookup"><span data-stu-id="6419a-122">The code is shown below.</span></span>


```
// create material
D3DMATERIAL9 mtrl;
ZeroMemory( &mtrl, sizeof(mtrl) );
mtrl.Emissive.r = 0.0f;
mtrl.Emissive.g = 0.75f;
mtrl.Emissive.b = 0.0f;
mtrl.Emissive.a = 0.0f;
m_pd3dDevice->SetMaterial( &mtrl );
m_pd3dDevice->SetRenderState(D3DRS_EMISSIVEMATERIALSOURCE, D3DMCS_MATERIAL);
```



<span data-ttu-id="6419a-123">Gemäß der Gleichung ist die resultierende Farbe für die Objekt Vertices die Material Farbe.</span><span class="sxs-lookup"><span data-stu-id="6419a-123">According to the equation, the resulting color for the object vertices is the material color.</span></span>

<span data-ttu-id="6419a-124">In der folgenden Abbildung wird die Material Farbe angezeigt, die grün ist.</span><span class="sxs-lookup"><span data-stu-id="6419a-124">The following illustration shows the material color, which is green.</span></span> <span data-ttu-id="6419a-125">Emissive Light beleuchtet alle Objekt Scheitel Punkte mit der gleichen Farbe.</span><span class="sxs-lookup"><span data-stu-id="6419a-125">Emissive light lights all object vertices with the same color.</span></span> <span data-ttu-id="6419a-126">Er ist nicht abhängig von der Scheitelpunkt normalen oder der Lichtrichtung.</span><span class="sxs-lookup"><span data-stu-id="6419a-126">It is not dependent on the vertex normal or the light direction.</span></span> <span data-ttu-id="6419a-127">Folglich sieht die Kugel wie ein 2D-Kreis aus, da es keinen Unterschied gibt, um die Oberfläche des Objekts zu schattieren.</span><span class="sxs-lookup"><span data-stu-id="6419a-127">As a result, the sphere looks like a 2D circle because there is no difference in shading around the surface of the object.</span></span>

![Abbildung einer grünen Kugel](images/lighte.jpg)

<span data-ttu-id="6419a-129">In der folgenden Abbildung wird gezeigt, wie das selbst leuchtendes-Licht mit den anderen drei Arten von Lichtern in den vorherigen Beispielen kombiniert werden kann.</span><span class="sxs-lookup"><span data-stu-id="6419a-129">The following illustration shows how the emissive light blends with the other three types of lights, from the previous examples.</span></span> <span data-ttu-id="6419a-130">Auf der rechten Seite der Kugel gibt es eine Mischung aus dem grünen selbst leuchtendes-und dem roten Ambient-Licht.</span><span class="sxs-lookup"><span data-stu-id="6419a-130">On the right side of the sphere, there is a blend of the green emissive and the red ambient light.</span></span> <span data-ttu-id="6419a-131">Auf der linken Seite der Kugel wird das grüne Rand Licht mit rotem Ambient und diffuses Licht kombiniert, das einen roten Farbverlauf erzeugt.</span><span class="sxs-lookup"><span data-stu-id="6419a-131">On the left side of the sphere, the green emissive light blends with red ambient and diffuse light producing a red gradient.</span></span> <span data-ttu-id="6419a-132">Die Glanz Markierung ist weiß in der Mitte und erstellt einen gelben Ring, da der Glanz helle Wert stark abfällt, wodurch sich die Umgebungs-, diffusen und abzurufenden hellen Werte, die miteinander verknüpft sind, hervorgehoben lassen.</span><span class="sxs-lookup"><span data-stu-id="6419a-132">The specular highlight is white in the center and creates a yellow ring as the specular light value falls off sharply leaving the ambient, diffuse and emissive light values which blend together to make yellow.</span></span>

![Abbildung einer grünen Kugel mit selbst leuchtendes Light](images/lightadse.jpg)

## <a name="related-topics"></a><span data-ttu-id="6419a-134">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="6419a-134">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="6419a-135">Mathematik der Beleuchtung</span><span class="sxs-lookup"><span data-stu-id="6419a-135">Mathematics of Lighting</span></span>](mathematics-of-lighting.md)
</dt> </dl>

 

 



