---
description: Durchsatz Metriken, um die Leistung einer Anwendung besser zu verstehen.
ms.assetid: c0bcf060-a0ed-4c85-9554-398ffe4b4235
title: D3DDEVINFO_D3D9BANDWIDTHTIMINGS-Struktur (D3D9Types. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DDEVINFO_D3D9BANDWIDTHTIMINGS
api_type:
- HeaderDef
api_location:
- D3D9Types.h
ms.openlocfilehash: 3bfb98045e645f20fa77cf8523040b995f6c254a
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/15/2021
ms.locfileid: "104219473"
---
# <a name="d3ddevinfo_d3d9bandwidthtimings-structure"></a><span data-ttu-id="ed862-103">D3DDEVINFO \_ D3D9BANDWIDTHTIMINGS-Struktur</span><span class="sxs-lookup"><span data-stu-id="ed862-103">D3DDEVINFO\_D3D9BANDWIDTHTIMINGS structure</span></span>

<span data-ttu-id="ed862-104">Durchsatz Metriken, um die Leistung einer Anwendung besser zu verstehen.</span><span class="sxs-lookup"><span data-stu-id="ed862-104">Throughput metrics for help in understanding the performance of an application.</span></span>

## <a name="syntax"></a><span data-ttu-id="ed862-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="ed862-105">Syntax</span></span>


```C++
typedef struct D3DDEVINFO_D3D9BANDWIDTHTIMINGS {
  FLOAT MaxBandwidthUtilized;
  FLOAT FrontEndUploadMemoryUtilizedPercent;
  FLOAT VertexRateUtilizedPercent;
  FLOAT TriangleSetupRateUtilizedPercent;
  FLOAT FillRateUtilizedPercent;
} D3DDEVINFO_D3D9BANDWIDTHTIMINGS, *LPD3DDEVINFO_D3D9BANDWIDTHTIMINGS;
```



## <a name="members"></a><span data-ttu-id="ed862-106">Member</span><span class="sxs-lookup"><span data-stu-id="ed862-106">Members</span></span>

<dl> <dt>

<span data-ttu-id="ed862-107">**Maxbandwidthausgelastet**</span><span class="sxs-lookup"><span data-stu-id="ed862-107">**MaxBandwidthUtilized**</span></span>
</dt> <dd>

<span data-ttu-id="ed862-108">Typ: **[ **float**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="ed862-108">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

</dd> <dd>

<span data-ttu-id="ed862-109">Die Bandbreite oder maximale Datenübertragungsrate von der Host-CPU zur GPU.</span><span class="sxs-lookup"><span data-stu-id="ed862-109">The bandwidth or maximum data transfer rate from the host CPU to the GPU.</span></span> <span data-ttu-id="ed862-110">Dabei handelt es sich in der Regel um die Bandbreite des PCI-oder AGP-Busses, der die CPU und die GPU verbindet.</span><span class="sxs-lookup"><span data-stu-id="ed862-110">This is typically the bandwidth of the PCI or AGP bus which connects the CPU and the GPU.</span></span>

</dd> <dt>

<span data-ttu-id="ed862-111">**Frontenduploadmemoryutilizedprozent**</span><span class="sxs-lookup"><span data-stu-id="ed862-111">**FrontEndUploadMemoryUtilizedPercent**</span></span>
</dt> <dd>

<span data-ttu-id="ed862-112">Typ: **[ **float**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="ed862-112">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

</dd> <dd>

<span data-ttu-id="ed862-113">Arbeitsspeicher Auslastung in Prozent beim Hochladen von Daten von der Host-CPU auf die GPU.</span><span class="sxs-lookup"><span data-stu-id="ed862-113">Memory utilized percentage when uploading data from the host CPU to the GPU.</span></span>

</dd> <dt>

<span data-ttu-id="ed862-114">**Vertexrateutilizedprozent**</span><span class="sxs-lookup"><span data-stu-id="ed862-114">**VertexRateUtilizedPercent**</span></span>
</dt> <dd>

<span data-ttu-id="ed862-115">Typ: **[ **float**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="ed862-115">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

</dd> <dd>

<span data-ttu-id="ed862-116">Vertex-Durchsatz Prozentsatz.</span><span class="sxs-lookup"><span data-stu-id="ed862-116">Vertex throughput percentage.</span></span> <span data-ttu-id="ed862-117">Dies ist die Anzahl der verarbeiteten Scheitel Punkte im Vergleich zur theoretischen maximalen Vertex-Verarbeitungsrate.</span><span class="sxs-lookup"><span data-stu-id="ed862-117">This is the number of vertices processed compared to the theoretical maximum vertex processing rate.</span></span>

</dd> <dt>

<span data-ttu-id="ed862-118">**"" "" ".**</span><span class="sxs-lookup"><span data-stu-id="ed862-118">**TriangleSetupRateUtilizedPercent**</span></span>
</dt> <dd>

<span data-ttu-id="ed862-119">Typ: **[ **float**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="ed862-119">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

</dd> <dd>

<span data-ttu-id="ed862-120">Prozentsatz der Dreiecks Einrichtung in Prozent.</span><span class="sxs-lookup"><span data-stu-id="ed862-120">Triangle set-up throughput percentage.</span></span> <span data-ttu-id="ed862-121">Dies ist die Anzahl der Dreiecke, die für die rasterisierung im Vergleich zur theoretischen maximalen Dreiecks Einrichtung festgelegt sind.</span><span class="sxs-lookup"><span data-stu-id="ed862-121">This is the number of triangles that are set up for rasterization compared to the theoretical maximum triangle set-up rate.</span></span>

</dd> <dt>

<span data-ttu-id="ed862-122">**Fillrateutilizedprozent**</span><span class="sxs-lookup"><span data-stu-id="ed862-122">**FillRateUtilizedPercent**</span></span>
</dt> <dd>

<span data-ttu-id="ed862-123">Typ: **[ **float**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="ed862-123">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

</dd> <dd>

<span data-ttu-id="ed862-124">Prozentsatz der Pixel Füll Durchsatz.</span><span class="sxs-lookup"><span data-stu-id="ed862-124">Pixel fill throughput percentage.</span></span> <span data-ttu-id="ed862-125">Dies ist die Anzahl der Pixel, die im Vergleich zur theoretischen Pixel Füllung aufgefüllt werden.</span><span class="sxs-lookup"><span data-stu-id="ed862-125">This is the number of pixels that are filled compared to the theoretical pixel fill.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="ed862-126">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="ed862-126">Requirements</span></span>



| <span data-ttu-id="ed862-127">Anforderung</span><span class="sxs-lookup"><span data-stu-id="ed862-127">Requirement</span></span> | <span data-ttu-id="ed862-128">Wert</span><span class="sxs-lookup"><span data-stu-id="ed862-128">Value</span></span> |
|-------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="ed862-129">Header</span><span class="sxs-lookup"><span data-stu-id="ed862-129">Header</span></span><br/> | <dl> <span data-ttu-id="ed862-130"><dt>D3D9Types. h</dt></span><span class="sxs-lookup"><span data-stu-id="ed862-130"><dt>D3D9Types.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="ed862-131">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="ed862-131">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ed862-132">Direct3D-Strukturen</span><span class="sxs-lookup"><span data-stu-id="ed862-132">Direct3D Structures</span></span>](dx9-graphics-reference-d3d-structures.md)
</dt> <dt>

[<span data-ttu-id="ed862-133">**GetData**</span><span class="sxs-lookup"><span data-stu-id="ed862-133">**GetData**</span></span>](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3dquery9-getdata)
</dt> </dl>

 

 
