---
description: Texturkoordinaten in Direct3D können ein, zwei, drei oder vier Gleit Komma Elemente enthalten, um Texturen mit unterschiedlichen Dimensions Ebenen zu behandeln.
ms.assetid: d841af62-41b0-4b80-960b-4630b9a7210c
title: Texturkoordinaten Formate (Direct3D 9)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3c95eada1cf21f0a4db38589794b08b88023e72d
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/06/2021
ms.locfileid: "103747616"
---
# <a name="texture-coordinate-formats-direct3d-9"></a><span data-ttu-id="91361-103">Texturkoordinaten Formate (Direct3D 9)</span><span class="sxs-lookup"><span data-stu-id="91361-103">Texture Coordinate Formats (Direct3D 9)</span></span>

<span data-ttu-id="91361-104">Texturkoordinaten in Direct3D können ein, zwei, drei oder vier Gleit Komma Elemente enthalten, um Texturen mit unterschiedlichen Dimensions Ebenen zu behandeln.</span><span class="sxs-lookup"><span data-stu-id="91361-104">Texture coordinates in Direct3D can include one, two, three, or four floating point elements to address textures with varying levels of dimension.</span></span> <span data-ttu-id="91361-105">Eine 1D-Textur: eine Textur Oberfläche mit Dimensionen von 1-nach-n-texeln-wird von einer Textur Koordinate adressiert.</span><span class="sxs-lookup"><span data-stu-id="91361-105">A 1D texture - a texture surface with dimensions of 1-by-n texels - is addressed by one texture coordinate.</span></span> <span data-ttu-id="91361-106">Die gängigsten Fälle, 2D-Texturen, werden mit zwei Texturkoordinaten adressiert, die häufig als Sie und v bezeichnet werden.</span><span class="sxs-lookup"><span data-stu-id="91361-106">The most common case, 2D textures, are addressed with two texture coordinates commonly called u and v.</span></span> <span data-ttu-id="91361-107">Direct3D unterstützt zwei Arten von 3D-Texturen, kubische Umgebungs Zuordnungen und volumetexturen.</span><span class="sxs-lookup"><span data-stu-id="91361-107">Direct3D supports two types of 3D textures, cubic-environment maps and volume textures.</span></span> <span data-ttu-id="91361-108">Kubische Umgebungs Zuordnungen sind nicht wirklich 3D, aber Sie werden mit einem Vektor mit drei Elementen adressiert.</span><span class="sxs-lookup"><span data-stu-id="91361-108">Cubic environment maps aren't truly 3D, but they are addressed with a 3-element vector.</span></span> <span data-ttu-id="91361-109">Weitere Informationen finden Sie unter [Zuordnung von kubischen Umgebungen (Direct3D 9)](cubic-environment-mapping.md).</span><span class="sxs-lookup"><span data-stu-id="91361-109">For details, see [Cubic Environment Mapping (Direct3D 9)](cubic-environment-mapping.md).</span></span>

<span data-ttu-id="91361-110">Wie in " [Fixed Function f VF Codes (Direct3D 9)](fixed-function-fvf-codes.md)" beschrieben, codieren Anwendungen Texturkoordinaten im Vertex-Format.</span><span class="sxs-lookup"><span data-stu-id="91361-110">As described in [Fixed Function FVF Codes (Direct3D 9)](fixed-function-fvf-codes.md), applications encode texture coordinates in the vertex format.</span></span> <span data-ttu-id="91361-111">Das Vertex-Format kann mehrere Sätze von Texturkoordinaten enthalten.</span><span class="sxs-lookup"><span data-stu-id="91361-111">The vertex format can include multiple sets of texture coordinates.</span></span> <span data-ttu-id="91361-112">Verwenden Sie die D3DFVF \_ TEX0 bis D3DFVF \_ TEX8 [D3DFVF](d3dfvf.md) , um ein Scheitelpunkt Format zu beschreiben, das keine Texturkoordinaten enthält, oder bis zu acht Sets.</span><span class="sxs-lookup"><span data-stu-id="91361-112">Use the D3DFVF\_TEX0 through D3DFVF\_TEX8 [D3DFVF](d3dfvf.md) to describe a vertex format that includes no texture coordinates, or as many as eight sets.</span></span>

<span data-ttu-id="91361-113">Jeder Texturkoordinaten Satz kann zwischen einem und vier Elementen aufweisen.</span><span class="sxs-lookup"><span data-stu-id="91361-113">Each texture coordinate set can have between one and four elements.</span></span> <span data-ttu-id="91361-114">Die D3DFVF \_ TEXTUREFORMAT1 through D3DFVF \_ TEXTUREFORMAT4-Flags beschreiben die Anzahl von Elementen in einer Textur Koordinate in einer Menge, diese Flags werden jedoch nicht von sich selbst verwendet.</span><span class="sxs-lookup"><span data-stu-id="91361-114">The D3DFVF\_TEXTUREFORMAT1 through D3DFVF\_TEXTUREFORMAT4 flags describe the number of elements in a texture coordinate in a set, but these flags aren't used by themselves.</span></span> <span data-ttu-id="91361-115">Stattdessen verwendet der [**D3DFVF \_ texcoordsizen**](d3dfvf-texcoordsizen.md) -Satz von Makros diese Flags, um Bitmuster zu erstellen, die die Anzahl der Elemente beschreiben, die von einem bestimmten Satz von Texturkoordinaten im Vertex-Format verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="91361-115">Rather, the [**D3DFVF\_TEXCOORDSIZEN**](d3dfvf-texcoordsizen.md) set of macros use these flags to create bit patterns that describe the number of elements used by a particular set of texture coordinates in the vertex format.</span></span> <span data-ttu-id="91361-116">Diese Makros akzeptieren einen einzelnen Parameter, der den Index des Koordinaten Satzes identifiziert, dessen Anzahl von Elementen definiert wird.</span><span class="sxs-lookup"><span data-stu-id="91361-116">These macros accept a single parameter that identifies the index of the coordinate set whose number of elements is being defined.</span></span> <span data-ttu-id="91361-117">Im folgenden Beispiel wird veranschaulicht, wie diese Makros verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="91361-117">The following example illustrates how these macros are used.</span></span>


```
// This vertex format contains two sets of texture coordinates.
// The first set (index 0) has 2 elements, and the second set 
// has 1 element. The description for this vertex format would be: 
//     dwFVF = D3DFVF_XYZ  | D3DFVF_NORMAL | D3DFVF_DIFFUSE | D3DFVF_TEX2 |
//             D3DFVF_TEXCOORDSIZE2(0) | D3DFVF_TEXCOORDSIZE1(1); 
//
typedef struct CVF
{
    D3DVECTOR position;
    D3DVECTOR normal;
    D3DCOLOR  diffuse;
    float     u, v;   // 1st set, 2D
    float     t;      // 2nd set, 1D
} CustomVertexFormat;
```



> [!Note]  
> <span data-ttu-id="91361-118">Mit Ausnahme von kubischen Umgebungs Zuordnungen und volumetexturen können Rasterizers keine Texturen mithilfe von mehr als zwei Elementen adressieren.</span><span class="sxs-lookup"><span data-stu-id="91361-118">With the exception of cubic-environment maps and volume textures, rasterizers cannot address textures by using any more than two elements.</span></span> <span data-ttu-id="91361-119">Anwendungen können bis zu drei Elemente für eine Textur Koordinate bereitstellen, aber nur, wenn es sich bei der Textur um eine cubemap, eine volumetextur oder das \_ Flag D3DTTFF projiziertes Textur Transform handelt.</span><span class="sxs-lookup"><span data-stu-id="91361-119">Applications can supply up to three elements for a texture coordinate, but only if the texture is a cube map, a volume texture, or the D3DTTFF\_PROJECTED texture transform flag is used.</span></span> <span data-ttu-id="91361-120">Das \_ Flag D3DTTFF projibewirkt, dass der Raster die ersten beiden Elemente durch das dritte Element (oder n) dividiert.</span><span class="sxs-lookup"><span data-stu-id="91361-120">The D3DTTFF\_PROJECTED flag causes the rasterizer to divide the first two elements by the third (or n) element.</span></span> <span data-ttu-id="91361-121">Weitere Informationen finden Sie unter [Texturkoordinaten Transformationen (Direct3D 9)](texture-coordinate-transformations.md).</span><span class="sxs-lookup"><span data-stu-id="91361-121">For more information, see [Texture Coordinate Transformations (Direct3D 9)](texture-coordinate-transformations.md).</span></span>

 

## <a name="related-topics"></a><span data-ttu-id="91361-122">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="91361-122">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="91361-123">Texturkoordinaten</span><span class="sxs-lookup"><span data-stu-id="91361-123">Texture Coordinates</span></span>](texture-coordinates.md)
</dt> </dl>

 

 



