---
description: Treibertexturkoordinatenfunktionsflags.
ms.assetid: b15509b4-7db1-429a-9468-be7a11dee505
title: D3DTSS_TCI
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 58746f17eb18b679a4dfe4957ac46236baeec35d
ms.sourcegitcommit: b40a986d5ded926ae7617119cdd35d99b533bad9
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 05/24/2021
ms.locfileid: "110342975"
---
# <a name="d3dtss_tci"></a><span data-ttu-id="03a92-103">D3DTSS \_ TCI</span><span class="sxs-lookup"><span data-stu-id="03a92-103">D3DTSS\_TCI</span></span>

<span data-ttu-id="03a92-104">Treibertexturkoordinatenfunktionsflags.</span><span class="sxs-lookup"><span data-stu-id="03a92-104">Driver texture coordinate capability flags.</span></span>



| <span data-ttu-id="03a92-105">\#Definieren</span><span class="sxs-lookup"><span data-stu-id="03a92-105">\#define</span></span>                                 | <span data-ttu-id="03a92-106">Wert</span><span class="sxs-lookup"><span data-stu-id="03a92-106">Value</span></span>       | <span data-ttu-id="03a92-107">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="03a92-107">Description</span></span>                                                                                                                                                                                                          |
|------------------------------------------|-------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="03a92-108">D3DTSS \_ TCI \_ PASSTHRU</span><span class="sxs-lookup"><span data-stu-id="03a92-108">D3DTSS\_TCI\_PASSTHRU</span></span>                    | <span data-ttu-id="03a92-109">0x00000000L</span><span class="sxs-lookup"><span data-stu-id="03a92-109">0x00000000L</span></span> | <span data-ttu-id="03a92-110">Verwenden Sie die angegebenen Texturkoordinaten, die im Scheitelpunktformat enthalten sind.</span><span class="sxs-lookup"><span data-stu-id="03a92-110">Use the specified texture coordinates contained within the vertex format.</span></span> <span data-ttu-id="03a92-111">Dieser Wert wird in 0 (null) gelöst.</span><span class="sxs-lookup"><span data-stu-id="03a92-111">This value resolves to zero.</span></span>                                                                                                               |
| <span data-ttu-id="03a92-112">D3DTSS \_ TCI \_ CAMERASPACENORMAL</span><span class="sxs-lookup"><span data-stu-id="03a92-112">D3DTSS\_TCI\_CAMERASPACENORMAL</span></span>           | <span data-ttu-id="03a92-113">0x00010000L</span><span class="sxs-lookup"><span data-stu-id="03a92-113">0x00010000L</span></span> | <span data-ttu-id="03a92-114">Verwenden Sie den Scheitelpunkt normal, transformiert in den Kameraraum, als Eingabetexturkoordinaten für die Texturtransformation dieser Phase.</span><span class="sxs-lookup"><span data-stu-id="03a92-114">Use the vertex normal, transformed to camera space, as the input texture coordinates for this stage's texture transformation.</span></span>                                                                                        |
| <span data-ttu-id="03a92-115">D3DTSS \_ TCI \_ CAMERASPACEPOSITION</span><span class="sxs-lookup"><span data-stu-id="03a92-115">D3DTSS\_TCI\_CAMERASPACEPOSITION</span></span>         | <span data-ttu-id="03a92-116">0x00020000L</span><span class="sxs-lookup"><span data-stu-id="03a92-116">0x00020000L</span></span> | <span data-ttu-id="03a92-117">Verwenden Sie die Scheitelpunktposition, transformiert in den Kameraraum, als Eingabetexturkoordinaten für die Texturtransformation dieser Stufe.</span><span class="sxs-lookup"><span data-stu-id="03a92-117">Use the vertex position, transformed to camera space, as the input texture coordinates for this stage's texture transformation.</span></span>                                                                                      |
| <span data-ttu-id="03a92-118">D3DTSS \_ TCI \_ CAMERASPACEREFLECTIONVECTOR</span><span class="sxs-lookup"><span data-stu-id="03a92-118">D3DTSS\_TCI\_CAMERASPACEREFLECTIONVECTOR</span></span> | <span data-ttu-id="03a92-119">0x00030000L</span><span class="sxs-lookup"><span data-stu-id="03a92-119">0x00030000L</span></span> | <span data-ttu-id="03a92-120">Verwenden Sie den Reflektionsvektor, der in den Kameraraum transformiert wird, als Eingabetexturkoordinate für die Texturtransformation dieser Stufe.</span><span class="sxs-lookup"><span data-stu-id="03a92-120">Use the reflection vector, transformed to camera space, as the input texture coordinate for this stage's texture transformation.</span></span> <span data-ttu-id="03a92-121">Der Reflektionsvektor wird aus der Position des Eingabe-Scheitelpunkts und dem normalen Vektor berechnet.</span><span class="sxs-lookup"><span data-stu-id="03a92-121">The reflection vector is computed from the input vertex position and normal vector.</span></span> |
| <span data-ttu-id="03a92-122">D3DTSS \_ TCI \_ SPHEREMAP</span><span class="sxs-lookup"><span data-stu-id="03a92-122">D3DTSS\_TCI\_SPHEREMAP</span></span>                   | <span data-ttu-id="03a92-123">0x00040000L</span><span class="sxs-lookup"><span data-stu-id="03a92-123">0x00040000L</span></span> | <span data-ttu-id="03a92-124">Verwenden Sie die angegebenen Texturkoordinaten für die Kugelzuordnung.</span><span class="sxs-lookup"><span data-stu-id="03a92-124">Use the specified texture coordinates for sphere mapping.</span></span>                                                                                                                                                            |



 

<span data-ttu-id="03a92-125">Diese Konstanten werden von D3DTSS \_ TEXCOORDINDEX verwendet.</span><span class="sxs-lookup"><span data-stu-id="03a92-125">These constants are used by D3DTSS\_TEXCOORDINDEX.</span></span>

## <a name="constant-information"></a><span data-ttu-id="03a92-126">Konstanteninformationen</span><span class="sxs-lookup"><span data-stu-id="03a92-126">Constant Information</span></span>



|  <span data-ttu-id="03a92-127">Anforderung</span><span class="sxs-lookup"><span data-stu-id="03a92-127">Requirement</span></span>                        | <span data-ttu-id="03a92-128">Wert</span><span class="sxs-lookup"><span data-stu-id="03a92-128">Value</span></span>           |
|--------------------------|------------|
| <span data-ttu-id="03a92-129">Header</span><span class="sxs-lookup"><span data-stu-id="03a92-129">Header</span></span>                   | <span data-ttu-id="03a92-130">d3d9caps.h</span><span class="sxs-lookup"><span data-stu-id="03a92-130">d3d9caps.h</span></span> |
| <span data-ttu-id="03a92-131">Mindestbetriebssystem</span><span class="sxs-lookup"><span data-stu-id="03a92-131">Minimum operating system</span></span> | <span data-ttu-id="03a92-132">Windows 98</span><span class="sxs-lookup"><span data-stu-id="03a92-132">Windows 98</span></span> |



 

## <a name="related-topics"></a><span data-ttu-id="03a92-133">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="03a92-133">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="03a92-134">Direct3D-Konstanten</span><span class="sxs-lookup"><span data-stu-id="03a92-134">Direct3D Constants</span></span>](dx9-graphics-reference-d3d-constants.md)
</dt> </dl>

 

 



