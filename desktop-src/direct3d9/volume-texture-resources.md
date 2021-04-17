---
description: Volumetexturen sind dreidimensionale Auflistungen von Pixeln (texeln), mit denen ein zweidimensionales primitiv gezeichnet werden kann, z. b. ein Dreieck oder eine Linie.
ms.assetid: 1d692501-a524-4ad4-8779-d71f1bda7bc9
title: Volumetextur-Ressourcen (Direct3D 9)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 67c66ff97d04e3c7c6c0a032f9a230dfd511b38c
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/06/2021
ms.locfileid: "104557716"
---
# <a name="volume-texture-resources-direct3d-9"></a><span data-ttu-id="565a7-103">Volumetextur-Ressourcen (Direct3D 9)</span><span class="sxs-lookup"><span data-stu-id="565a7-103">Volume Texture Resources (Direct3D 9)</span></span>

<span data-ttu-id="565a7-104">Volumetexturen sind dreidimensionale Auflistungen von Pixeln (texeln), mit denen ein zweidimensionales primitiv gezeichnet werden kann, z. b. ein Dreieck oder eine Linie.</span><span class="sxs-lookup"><span data-stu-id="565a7-104">Volume textures are three-dimensional collections of pixels (texels) that can be used to paint a two-dimensional primitive such as a triangle or a line.</span></span> <span data-ttu-id="565a7-105">Für jeden Scheitelpunkt eines primitiven, der mit einem Volume strukturiert werden soll, sind drei-Element-Texturkoordinaten erforderlich.</span><span class="sxs-lookup"><span data-stu-id="565a7-105">Three-element texture coordinates are required for each vertex of a primitive that is to be textured with a volume.</span></span> <span data-ttu-id="565a7-106">Wenn das primitive gezeichnet wird, wird jedes enthaltene Pixel mit dem Farbwert von einem Pixel innerhalb des Volumes gefüllt, und zwar entsprechend den Regeln der zweidimensionalen Textur.</span><span class="sxs-lookup"><span data-stu-id="565a7-106">As the primitive is drawn, each contained pixel is filled with the color value from some pixel within the volume, in accordance with rules analogous to the two-dimensional texture case.</span></span> <span data-ttu-id="565a7-107">Volumes werden nicht direkt gerendert, da keine dreidimensionalen primitiven vorhanden sind, die mit Ihnen gezeichnet werden können.</span><span class="sxs-lookup"><span data-stu-id="565a7-107">Volumes are not rendered directly because there are no three-dimensional primitives that can be painted with them.</span></span>

<span data-ttu-id="565a7-108">Volumetexturen können für besondere Effekte verwendet werden, z. b. für den Nebel, die Explosionen usw.</span><span class="sxs-lookup"><span data-stu-id="565a7-108">You can use volume textures for special effects such as patchy fog, explosions, and so on.</span></span>

<span data-ttu-id="565a7-109">Volumes sind in Slices angeordnet und können als Breite x Höhe 2D-Oberflächen gestapelt werden, um eine Breite x-Tiefe von Höhen zu bilden.</span><span class="sxs-lookup"><span data-stu-id="565a7-109">Volumes are organized into slices and can be thought of as width x height 2D surfaces stacked to make a width x height x depth volume.</span></span> <span data-ttu-id="565a7-110">Jeder Slice ist eine einzelne Zeile.</span><span class="sxs-lookup"><span data-stu-id="565a7-110">Each slice is a single row.</span></span> <span data-ttu-id="565a7-111">Volumes können nachfolgende Ebenen aufweisen, bei denen die Dimensionen der einzelnen Ebenen auf die Hälfte der Dimensionen der vorherigen Ebene gekürzt werden.</span><span class="sxs-lookup"><span data-stu-id="565a7-111">Volumes can have subsequent levels in which the dimensions of each level are truncated to half the dimensions of the previous level.</span></span> <span data-ttu-id="565a7-112">Das folgende Diagramm zeigt, wie eine volumetextur mit mehreren Ebenen aussieht.</span><span class="sxs-lookup"><span data-stu-id="565a7-112">The following diagram shows what a volume texture with multiple levels looks like.</span></span>

![Diagramm einer volumetextur mit 8x2x4, 4x1x2 und 2x1x1-cubedarstellungen](images/level123.png)

## <a name="creating-a-volume-texture"></a><span data-ttu-id="565a7-114">Erstellen einer volumetextur</span><span class="sxs-lookup"><span data-stu-id="565a7-114">Creating a Volume Texture</span></span>

<span data-ttu-id="565a7-115">Die folgenden Codebeispiele zeigen die Schritte, die für die Verwendung einer Volumestruktur erforderlich sind.</span><span class="sxs-lookup"><span data-stu-id="565a7-115">The code examples below show the steps required to use a volume texture.</span></span>

<span data-ttu-id="565a7-116">Geben Sie zunächst einen benutzerdefinierten Scheitelpunkt mit drei Texturkoordinaten für jeden Scheitelpunkt an, wie in diesem Codebeispiel dargestellt.</span><span class="sxs-lookup"><span data-stu-id="565a7-116">First, specify a custom vertex type that has three texture coordinates for each vertex, as shown in this code example.</span></span>


```
struct VOLUMEVERTEX
{
    FLOAT x, y, z;
    DWORD color;
    FLOAT tu, tv, tw;
};

#define D3DFVF_VOLUMEVERTEX (D3DFVF_XYZ|D3DFVF_DIFFUSE|
                             D3DFVF_TEX1|D3DFVF_TEXCOORDSIZE3(0))
```



<span data-ttu-id="565a7-117">Füllen Sie als nächstes die Scheitel Punkte mit Daten.</span><span class="sxs-lookup"><span data-stu-id="565a7-117">Next, fill the vertices with data.</span></span>


```
VOLUMEVERTEX g_vVertices[4] =
{
    { 1.0f, 1.0f, 0.0f, 0xffffffff, 1.0f, 1.0f, 0.0f },
    {-1.0f, 1.0f, 0.0f, 0xffffffff, 0.0f, 1.0f, 0.0f },
    { 1.0f,-1.0f, 0.0f, 0xffffffff, 1.0f, 0.0f, 0.0f },
    {-1.0f,-1.0f, 0.0f, 0xffffffff, 0.0f, 0.0f, 0.0f }
};
```



<span data-ttu-id="565a7-118">Erstellen Sie nun einen Scheitelpunkt Puffer, und füllen Sie ihn mit Daten aus den Scheitel Punkten aus.</span><span class="sxs-lookup"><span data-stu-id="565a7-118">Now, create a vertex buffer and fill it with data from the vertices.</span></span>

<span data-ttu-id="565a7-119">Der nächste Schritt besteht in der Verwendung der [**IDirect3DDevice9:: kreatevolumetexture**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-createvolumetexture) -Methode zum Erstellen einer Volumestruktur, wie in diesem Codebeispiel gezeigt.</span><span class="sxs-lookup"><span data-stu-id="565a7-119">The next step is to use the [**IDirect3DDevice9::CreateVolumeTexture**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-createvolumetexture) method to create a volume texture, as shown in this code example.</span></span>


```
LPDIRECT3DVOLUMETEXTURE9 pVolumeTexture;
d3dDevice->CreateVolumeTexture( 8, 4, 4, 1, 0, D3DFMT_R8G8B8,D3DPOOL_MANAGED, 
                                &pVolumeTexture );
```



<span data-ttu-id="565a7-120">Legen Sie vor dem Rendern des primitiven die aktuelle Textur auf die oben erstellte volumetextur fest.</span><span class="sxs-lookup"><span data-stu-id="565a7-120">Before rendering the primitive, set the current texture to the volume texture created above.</span></span> <span data-ttu-id="565a7-121">Das folgende Codebeispiel zeigt den gesamten Renderingprozess für einen Dreiecke.</span><span class="sxs-lookup"><span data-stu-id="565a7-121">The code example below shows the entire rendering process for a strip of triangles.</span></span>


```
if( SUCCEEDED( d3dDevice->BeginScene() ) )
{
    // Draw the quad, with the volume texture.
    d3dDevice->SetTexture( 0, pVolumeTexture );
    d3dDevice->SetFVF( D3DFVF_VOLUMEVERTEX );
    d3dDevice->SetStreamSource( 0, pVB, sizeof(VOLUMEVERTEX) );
    d3dDevice->DrawPrimitive( D3DPT_TRIANGLESTRIP, 0, 2);

   // End the scene.
   d3dDevice->EndScene();
}
```



## <a name="related-topics"></a><span data-ttu-id="565a7-122">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="565a7-122">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="565a7-123">Direct3D-Texturen</span><span class="sxs-lookup"><span data-stu-id="565a7-123">Direct3D Textures</span></span>](direct3d-textures.md)
</dt> </dl>

 

 
