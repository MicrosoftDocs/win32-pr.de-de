---
description: Definiert eine grundlegende Material Farbe, die entweder auf ein ganzes Mesh oder auf die einzelnen Flächen eines Netzes angewendet werden kann. Die Stromversorgung ist der Glanz Exponent des Materials.
ms.assetid: vs|directx_sdk|~\material.htm
title: Material
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 54c13d201152350a8a61950bb609f73cbdb2a3aa
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/06/2021
ms.locfileid: "104480702"
---
# <a name="material"></a><span data-ttu-id="91464-104">Material</span><span class="sxs-lookup"><span data-stu-id="91464-104">Material</span></span>

<span data-ttu-id="91464-105">Definiert eine grundlegende Material Farbe, die entweder auf ein ganzes Mesh oder auf die einzelnen Flächen eines Netzes angewendet werden kann.</span><span class="sxs-lookup"><span data-stu-id="91464-105">Defines a basic material color that can be applied to either a complete mesh or a mesh's individual faces.</span></span> <span data-ttu-id="91464-106">Die Stromversorgung ist der Glanz Exponent des Materials.</span><span class="sxs-lookup"><span data-stu-id="91464-106">The power is the specular exponent of the material.</span></span>

``` syntax
template Material
{
    < 3D82AB4D-62DA-11CF-AB39-0020AF71E433 >
    ColorRGBA faceColor;
    FLOAT power;
    ColorRGB specularColor;
    ColorRGB emissiveColor;
    [...]
} 
```

<span data-ttu-id="91464-107">Hierbei gilt:</span><span class="sxs-lookup"><span data-stu-id="91464-107">Where:</span></span>

-   <span data-ttu-id="91464-108">fakecolor-Vordergrundfarbe.</span><span class="sxs-lookup"><span data-stu-id="91464-108">faceColor - Face color.</span></span> <span data-ttu-id="91464-109">Eine colorrgba-Vorlage.</span><span class="sxs-lookup"><span data-stu-id="91464-109">A ColorRGBA template.</span></span> <span data-ttu-id="91464-110">Siehe [**colorrgba**](colorrgba.md).</span><span class="sxs-lookup"><span data-stu-id="91464-110">See [**ColorRGBA**](colorrgba.md).</span></span>
-   <span data-ttu-id="91464-111">Glanz Farben-Exponent für Energie Material.</span><span class="sxs-lookup"><span data-stu-id="91464-111">power - Material specular color exponent.</span></span>
-   <span data-ttu-id="91464-112">SpecularColor-Material Glanz Farbe.</span><span class="sxs-lookup"><span data-stu-id="91464-112">specularColor - Material specular color.</span></span> <span data-ttu-id="91464-113">Eine colorrgb-Vorlage.</span><span class="sxs-lookup"><span data-stu-id="91464-113">A ColorRGB template.</span></span> <span data-ttu-id="91464-114">Siehe [**colorrgb**](colorrgb.md).</span><span class="sxs-lookup"><span data-stu-id="91464-114">See [**ColorRGB**](colorrgb.md).</span></span>
-   <span data-ttu-id="91464-115">emissivecolor-Material selbst leuchtendes Color.</span><span class="sxs-lookup"><span data-stu-id="91464-115">emissiveColor - Material emissive color.</span></span> <span data-ttu-id="91464-116">Eine colorrgb-Vorlage.</span><span class="sxs-lookup"><span data-stu-id="91464-116">A ColorRGB template.</span></span> <span data-ttu-id="91464-117">Siehe [**colorrgb**](colorrgb.md).</span><span class="sxs-lookup"><span data-stu-id="91464-117">See [**ColorRGB**](colorrgb.md).</span></span>

> [!Note]  
> <span data-ttu-id="91464-118">Die Umgebungs Farbe erfordert eine Alpha Komponente.</span><span class="sxs-lookup"><span data-stu-id="91464-118">The ambient color requires an alpha component.</span></span>

 

<span data-ttu-id="91464-119">[**Texturefilename**](texturefilename.md) ist ein optionales Datenobjekt.</span><span class="sxs-lookup"><span data-stu-id="91464-119">[**TextureFilename**](texturefilename.md) is an optional data object.</span></span> <span data-ttu-id="91464-120">Wenn dieses Objekt nicht vorhanden ist, wird das Gesicht nicht texturiert.</span><span class="sxs-lookup"><span data-stu-id="91464-120">If this object is not present, the face is untextured.</span></span>

## <a name="see-also"></a><span data-ttu-id="91464-121">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="91464-121">See also</span></span>

<dl> <dt>

[<span data-ttu-id="91464-122">Vorlagen</span><span class="sxs-lookup"><span data-stu-id="91464-122">Templates</span></span>](dx9-graphics-reference-x-file-format-templates.md)
</dt> </dl>

 

 



