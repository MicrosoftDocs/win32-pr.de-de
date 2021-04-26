---
description: Funktionsflags für die Treibertexturkoordinaten.
ms.assetid: b15509b4-7db1-429a-9468-be7a11dee505
title: D3DTSS_TCI
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1da9ca23ebc4dd121527721a9d10a2db55a4d555
ms.sourcegitcommit: b6fe9acffad983c14864b8fe0296f6025cb1f961
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/26/2021
ms.locfileid: "107995257"
---
# <a name="d3dtss_tci"></a><span data-ttu-id="f26a9-103">D3DTSS \_ TCI</span><span class="sxs-lookup"><span data-stu-id="f26a9-103">D3DTSS\_TCI</span></span>

<span data-ttu-id="f26a9-104">Funktionsflags für die Treibertexturkoordinaten.</span><span class="sxs-lookup"><span data-stu-id="f26a9-104">Driver texture coordinate capability flags.</span></span>



| <span data-ttu-id="f26a9-105">\#Definieren</span><span class="sxs-lookup"><span data-stu-id="f26a9-105">\#define</span></span>                                 | <span data-ttu-id="f26a9-106">Wert</span><span class="sxs-lookup"><span data-stu-id="f26a9-106">Value</span></span>       | <span data-ttu-id="f26a9-107">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="f26a9-107">Description</span></span>                                                                                                                                                                                                          |
|------------------------------------------|-------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="f26a9-108">D3DTSS \_ TCI \_ PASSTHRU</span><span class="sxs-lookup"><span data-stu-id="f26a9-108">D3DTSS\_TCI\_PASSTHRU</span></span>                    | <span data-ttu-id="f26a9-109">0x00000000L</span><span class="sxs-lookup"><span data-stu-id="f26a9-109">0x00000000L</span></span> | <span data-ttu-id="f26a9-110">Verwenden Sie die angegebenen Texturkoordinaten, die im Scheitelpunktformat enthalten sind.</span><span class="sxs-lookup"><span data-stu-id="f26a9-110">Use the specified texture coordinates contained within the vertex format.</span></span> <span data-ttu-id="f26a9-111">Dieser Wert wird in 0 (null) aufgelöst.</span><span class="sxs-lookup"><span data-stu-id="f26a9-111">This value resolves to zero.</span></span>                                                                                                               |
| <span data-ttu-id="f26a9-112">D3DTSS \_ TCI \_ CAMERASPACENORMAL</span><span class="sxs-lookup"><span data-stu-id="f26a9-112">D3DTSS\_TCI\_CAMERASPACENORMAL</span></span>           | <span data-ttu-id="f26a9-113">0x00010000L</span><span class="sxs-lookup"><span data-stu-id="f26a9-113">0x00010000L</span></span> | <span data-ttu-id="f26a9-114">Verwenden Sie die Vertexnorm, die in den Kameraraum transformiert ist, als Eingabetexturkoordinaten für die Texturtransformation dieser Phase.</span><span class="sxs-lookup"><span data-stu-id="f26a9-114">Use the vertex normal, transformed to camera space, as the input texture coordinates for this stage's texture transformation.</span></span>                                                                                        |
| <span data-ttu-id="f26a9-115">D3DTSS \_ TCI \_ CAMERASPACEPOSITION</span><span class="sxs-lookup"><span data-stu-id="f26a9-115">D3DTSS\_TCI\_CAMERASPACEPOSITION</span></span>         | <span data-ttu-id="f26a9-116">0x00020000L</span><span class="sxs-lookup"><span data-stu-id="f26a9-116">0x00020000L</span></span> | <span data-ttu-id="f26a9-117">Verwenden Sie die in den Kameraraum transformierte Scheitelpunktposition als Eingabetexturkoordinaten für die Texturtransformation dieser Phase.</span><span class="sxs-lookup"><span data-stu-id="f26a9-117">Use the vertex position, transformed to camera space, as the input texture coordinates for this stage's texture transformation.</span></span>                                                                                      |
| <span data-ttu-id="f26a9-118">D3DTSS \_ TCI \_ CAMERASPACEREFLECTIONVECTOR</span><span class="sxs-lookup"><span data-stu-id="f26a9-118">D3DTSS\_TCI\_CAMERASPACEREFLECTIONVECTOR</span></span> | <span data-ttu-id="f26a9-119">0x00030000L</span><span class="sxs-lookup"><span data-stu-id="f26a9-119">0x00030000L</span></span> | <span data-ttu-id="f26a9-120">Verwenden Sie den in den Kameraraum transformierten Reflektionsvektor als Eingabetexturkoordinate für die Texturtransformation dieser Phase.</span><span class="sxs-lookup"><span data-stu-id="f26a9-120">Use the reflection vector, transformed to camera space, as the input texture coordinate for this stage's texture transformation.</span></span> <span data-ttu-id="f26a9-121">Der Reflektionsvektor wird aus der Eingabevertexposition und dem normalen Vektor berechnet.</span><span class="sxs-lookup"><span data-stu-id="f26a9-121">The reflection vector is computed from the input vertex position and normal vector.</span></span> |
| <span data-ttu-id="f26a9-122">D3DTSS \_ TCI \_ SPHEREMAP</span><span class="sxs-lookup"><span data-stu-id="f26a9-122">D3DTSS\_TCI\_SPHEREMAP</span></span>                   | <span data-ttu-id="f26a9-123">0x00040000L</span><span class="sxs-lookup"><span data-stu-id="f26a9-123">0x00040000L</span></span> | <span data-ttu-id="f26a9-124">Verwenden Sie die angegebenen Texturkoordinaten für die Kugelzuordnung.</span><span class="sxs-lookup"><span data-stu-id="f26a9-124">Use the specified texture coordinates for sphere mapping.</span></span>                                                                                                                                                            |



 

<span data-ttu-id="f26a9-125">Diese Konstanten werden von D3DTSS \_ TEXCOORDINDEX verwendet.</span><span class="sxs-lookup"><span data-stu-id="f26a9-125">These constants are used by D3DTSS\_TEXCOORDINDEX.</span></span>

## <a name="constant-information"></a><span data-ttu-id="f26a9-126">Konstante Informationen</span><span class="sxs-lookup"><span data-stu-id="f26a9-126">Constant Information</span></span>



|                          |            |
|--------------------------|------------|
| <span data-ttu-id="f26a9-127">Header</span><span class="sxs-lookup"><span data-stu-id="f26a9-127">Header</span></span>                   | <span data-ttu-id="f26a9-128">d3d9caps.h</span><span class="sxs-lookup"><span data-stu-id="f26a9-128">d3d9caps.h</span></span> |
| <span data-ttu-id="f26a9-129">Mindestbetriebssystem</span><span class="sxs-lookup"><span data-stu-id="f26a9-129">Minimum operating system</span></span> | <span data-ttu-id="f26a9-130">Windows 98</span><span class="sxs-lookup"><span data-stu-id="f26a9-130">Windows 98</span></span> |



 

## <a name="related-topics"></a><span data-ttu-id="f26a9-131">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="f26a9-131">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="f26a9-132">Direct3D-Konstanten</span><span class="sxs-lookup"><span data-stu-id="f26a9-132">Direct3D Constants</span></span>](dx9-graphics-reference-d3d-constants.md)
</dt> </dl>

 

 



