---
description: Der Prozentsatz der Zeit, die Daten in der Pipeline verarbeitet.
ms.assetid: eb9dec27-2e45-4897-92af-8415c8fa08d4
title: D3DDEVINFO_D3D9PIPELINETIMINGS-Struktur (D3D9Types. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DDEVINFO_D3D9PIPELINETIMINGS
api_type:
- HeaderDef
api_location:
- D3D9Types.h
ms.openlocfilehash: 627eec0ea93181b14c308ab229ed603412511a91
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/15/2021
ms.locfileid: "106354999"
---
# <a name="d3ddevinfo_d3d9pipelinetimings-structure"></a><span data-ttu-id="235e1-103">D3DDEVINFO \_ D3D9PIPELINETIMINGS-Struktur</span><span class="sxs-lookup"><span data-stu-id="235e1-103">D3DDEVINFO\_D3D9PIPELINETIMINGS structure</span></span>

<span data-ttu-id="235e1-104">Der Prozentsatz der Zeit, die Daten in der Pipeline verarbeitet.</span><span class="sxs-lookup"><span data-stu-id="235e1-104">Percent of time processing data in the pipeline.</span></span>

## <a name="syntax"></a><span data-ttu-id="235e1-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="235e1-105">Syntax</span></span>


```C++
typedef struct D3DDEVINFO_D3D9PIPELINETIMINGS {
  FLOAT VertexProcessingTimePercent;
  FLOAT PixelProcessingTimePercent;
  FLOAT OtherGPUProcessingTimePercent;
  FLOAT GPUIdleTimePercent;
} D3DDEVINFO_D3D9PIPELINETIMINGS, *LPD3DDEVINFO_D3D9PIPELINETIMINGS;
```



## <a name="members"></a><span data-ttu-id="235e1-106">Member</span><span class="sxs-lookup"><span data-stu-id="235e1-106">Members</span></span>

<dl> <dt>

<span data-ttu-id="235e1-107">**Vertexprocessingtimeprozent**</span><span class="sxs-lookup"><span data-stu-id="235e1-107">**VertexProcessingTimePercent**</span></span>
</dt> <dd>

<span data-ttu-id="235e1-108">Typ: **[ **float**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="235e1-108">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

</dd> <dd>

<span data-ttu-id="235e1-109">Der Prozentsatz der Zeit für die Ausführung von Vertex-Shadern.</span><span class="sxs-lookup"><span data-stu-id="235e1-109">Percent of time spent running vertex shaders.</span></span>

</dd> <dt>

<span data-ttu-id="235e1-110">**Pixelprocessingtimeprozent**</span><span class="sxs-lookup"><span data-stu-id="235e1-110">**PixelProcessingTimePercent**</span></span>
</dt> <dd>

<span data-ttu-id="235e1-111">Typ: **[ **float**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="235e1-111">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

</dd> <dd>

<span data-ttu-id="235e1-112">Der Prozentsatz der Zeit für die Ausführung von Pixelshadern.</span><span class="sxs-lookup"><span data-stu-id="235e1-112">Percent of time spent running pixel shaders.</span></span>

</dd> <dt>

<span data-ttu-id="235e1-113">**Othergpuprocessingtimeprozent**</span><span class="sxs-lookup"><span data-stu-id="235e1-113">**OtherGPUProcessingTimePercent**</span></span>
</dt> <dd>

<span data-ttu-id="235e1-114">Typ: **[ **float**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="235e1-114">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

</dd> <dd>

<span data-ttu-id="235e1-115">Der Prozentsatz der Zeit für die Verarbeitung anderer Verarbeitungsvorgänge.</span><span class="sxs-lookup"><span data-stu-id="235e1-115">Percent of time spent doing other processing.</span></span>

</dd> <dt>

<span data-ttu-id="235e1-116">**Gpuidletimeprozent**</span><span class="sxs-lookup"><span data-stu-id="235e1-116">**GPUIdleTimePercent**</span></span>
</dt> <dd>

<span data-ttu-id="235e1-117">Typ: **[ **float**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="235e1-117">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

</dd> <dd>

<span data-ttu-id="235e1-118">Der Prozentsatz der Zeit, die nichts verarbeitet.</span><span class="sxs-lookup"><span data-stu-id="235e1-118">Percent of time not processing anything.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="235e1-119">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="235e1-119">Remarks</span></span>

<span data-ttu-id="235e1-120">Um eine optimale Leistung zu erzielen, wird eine ausgeglichene Auslastung empfohlen.</span><span class="sxs-lookup"><span data-stu-id="235e1-120">For best performance, a balanced load is recommended.</span></span>

## <a name="requirements"></a><span data-ttu-id="235e1-121">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="235e1-121">Requirements</span></span>



| <span data-ttu-id="235e1-122">Anforderung</span><span class="sxs-lookup"><span data-stu-id="235e1-122">Requirement</span></span> | <span data-ttu-id="235e1-123">Wert</span><span class="sxs-lookup"><span data-stu-id="235e1-123">Value</span></span> |
|-------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="235e1-124">Header</span><span class="sxs-lookup"><span data-stu-id="235e1-124">Header</span></span><br/> | <dl> <span data-ttu-id="235e1-125"><dt>D3D9Types. h</dt></span><span class="sxs-lookup"><span data-stu-id="235e1-125"><dt>D3D9Types.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="235e1-126">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="235e1-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="235e1-127">Direct3D-Strukturen</span><span class="sxs-lookup"><span data-stu-id="235e1-127">Direct3D Structures</span></span>](dx9-graphics-reference-d3d-structures.md)
</dt> <dt>

[<span data-ttu-id="235e1-128">**GetData**</span><span class="sxs-lookup"><span data-stu-id="235e1-128">**GetData**</span></span>](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3dquery9-getdata)
</dt> </dl>

 

 
