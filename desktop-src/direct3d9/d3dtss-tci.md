---
description: Funktionsflags für die Treiber Textur Koordinate.
ms.assetid: b15509b4-7db1-429a-9468-be7a11dee505
title: D3DTSS_TCI
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4973e045decd393be2f8a6d340f369761a411a44
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "103958563"
---
# <a name="d3dtss_tci"></a><span data-ttu-id="c1790-103">D3DTSS- \_ TCI</span><span class="sxs-lookup"><span data-stu-id="c1790-103">D3DTSS\_TCI</span></span>

<span data-ttu-id="c1790-104">Funktionsflags für die Treiber Textur Koordinate.</span><span class="sxs-lookup"><span data-stu-id="c1790-104">Driver texture coordinate capability flags.</span></span>



|                                          |             |                                                                                                                                                                                                                      |
|------------------------------------------|-------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="c1790-105">\#definieren</span><span class="sxs-lookup"><span data-stu-id="c1790-105">\#define</span></span>                                 | <span data-ttu-id="c1790-106">Wert</span><span class="sxs-lookup"><span data-stu-id="c1790-106">Value</span></span>       | <span data-ttu-id="c1790-107">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="c1790-107">Description</span></span>                                                                                                                                                                                                          |
| <span data-ttu-id="c1790-108">D3DTSS \_ TCI- \_ passthru</span><span class="sxs-lookup"><span data-stu-id="c1790-108">D3DTSS\_TCI\_PASSTHRU</span></span>                    | <span data-ttu-id="c1790-109">0x00000000L</span><span class="sxs-lookup"><span data-stu-id="c1790-109">0x00000000L</span></span> | <span data-ttu-id="c1790-110">Verwenden Sie die angegebenen Texturkoordinaten, die im Scheitelpunkt Format enthalten sind.</span><span class="sxs-lookup"><span data-stu-id="c1790-110">Use the specified texture coordinates contained within the vertex format.</span></span> <span data-ttu-id="c1790-111">Dieser Wert wird in NULL aufgelöst.</span><span class="sxs-lookup"><span data-stu-id="c1790-111">This value resolves to zero.</span></span>                                                                                                               |
| <span data-ttu-id="c1790-112">D3DTSS \_ TCI \_ cameraspacenormal</span><span class="sxs-lookup"><span data-stu-id="c1790-112">D3DTSS\_TCI\_CAMERASPACENORMAL</span></span>           | <span data-ttu-id="c1790-113">0x00010000l</span><span class="sxs-lookup"><span data-stu-id="c1790-113">0x00010000L</span></span> | <span data-ttu-id="c1790-114">Verwenden Sie den Vertex normal, transformiert in den Kamera Raum, als Eingabe Texturkoordinaten für die Textur Transformation dieses Stufen.</span><span class="sxs-lookup"><span data-stu-id="c1790-114">Use the vertex normal, transformed to camera space, as the input texture coordinates for this stage's texture transformation.</span></span>                                                                                        |
| <span data-ttu-id="c1790-115">D3DTSS \_ TCI \_ cameraspaceposition</span><span class="sxs-lookup"><span data-stu-id="c1790-115">D3DTSS\_TCI\_CAMERASPACEPOSITION</span></span>         | <span data-ttu-id="c1790-116">0x00020000l</span><span class="sxs-lookup"><span data-stu-id="c1790-116">0x00020000L</span></span> | <span data-ttu-id="c1790-117">Verwenden Sie die Vertex-Position, die in den Kamerabereich transformiert wird, als Eingabe Texturkoordinaten für die Textur Transformation dieser Stufe.</span><span class="sxs-lookup"><span data-stu-id="c1790-117">Use the vertex position, transformed to camera space, as the input texture coordinates for this stage's texture transformation.</span></span>                                                                                      |
| <span data-ttu-id="c1790-118">D3DTSS \_ TCI \_ cameraspacereflectionvector</span><span class="sxs-lookup"><span data-stu-id="c1790-118">D3DTSS\_TCI\_CAMERASPACEREFLECTIONVECTOR</span></span> | <span data-ttu-id="c1790-119">0x00030000l</span><span class="sxs-lookup"><span data-stu-id="c1790-119">0x00030000L</span></span> | <span data-ttu-id="c1790-120">Verwenden Sie den reflektionvektor, transformiert in den Kamera Raum, als Eingabe Textur Koordinate für die Textur Transformation dieses Stufen.</span><span class="sxs-lookup"><span data-stu-id="c1790-120">Use the reflection vector, transformed to camera space, as the input texture coordinate for this stage's texture transformation.</span></span> <span data-ttu-id="c1790-121">Der reflektionvektor wird aus der eintexposition der Eingabe und dem normalen Vektor berechnet.</span><span class="sxs-lookup"><span data-stu-id="c1790-121">The reflection vector is computed from the input vertex position and normal vector.</span></span> |
| <span data-ttu-id="c1790-122">D3DTSS \_ TCI- \_ spheremap</span><span class="sxs-lookup"><span data-stu-id="c1790-122">D3DTSS\_TCI\_SPHEREMAP</span></span>                   | <span data-ttu-id="c1790-123">0x00040000l</span><span class="sxs-lookup"><span data-stu-id="c1790-123">0x00040000L</span></span> | <span data-ttu-id="c1790-124">Verwenden Sie die angegebenen Texturkoordinaten für die Kugel Zuordnung.</span><span class="sxs-lookup"><span data-stu-id="c1790-124">Use the specified texture coordinates for sphere mapping.</span></span>                                                                                                                                                            |



 

<span data-ttu-id="c1790-125">Diese Konstanten werden von D3DTSS \_ texcoordindex verwendet.</span><span class="sxs-lookup"><span data-stu-id="c1790-125">These constants are used by D3DTSS\_TEXCOORDINDEX.</span></span>

## <a name="constant-information"></a><span data-ttu-id="c1790-126">Konstante Informationen</span><span class="sxs-lookup"><span data-stu-id="c1790-126">Constant Information</span></span>



|                          |            |
|--------------------------|------------|
| <span data-ttu-id="c1790-127">Header</span><span class="sxs-lookup"><span data-stu-id="c1790-127">Header</span></span>                   | <span data-ttu-id="c1790-128">d3d9caps. h</span><span class="sxs-lookup"><span data-stu-id="c1790-128">d3d9caps.h</span></span> |
| <span data-ttu-id="c1790-129">Mindestens Betriebssystem</span><span class="sxs-lookup"><span data-stu-id="c1790-129">Minimum operating system</span></span> | <span data-ttu-id="c1790-130">Windows 98</span><span class="sxs-lookup"><span data-stu-id="c1790-130">Windows 98</span></span> |



 

## <a name="related-topics"></a><span data-ttu-id="c1790-131">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="c1790-131">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="c1790-132">Direct3D-Konstanten</span><span class="sxs-lookup"><span data-stu-id="c1790-132">Direct3D Constants</span></span>](dx9-graphics-reference-d3d-constants.md)
</dt> </dl>

 

 



