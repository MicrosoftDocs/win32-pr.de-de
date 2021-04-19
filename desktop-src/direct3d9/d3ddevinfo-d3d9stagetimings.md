---
description: Der Prozentsatz der Zeit, die shaderdaten verarbeitet.
ms.assetid: 388bb943-c25f-4b50-b7e4-d6259f1186c2
title: D3DDEVINFO_D3D9STAGETIMINGS-Struktur (D3D9Types. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DDEVINFO_D3D9STAGETIMINGS
api_type:
- HeaderDef
api_location:
- D3D9Types.h
ms.openlocfilehash: cf8c9522decfcbb09a60aff0bee65ca05a0f5eeb
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/15/2021
ms.locfileid: "106355796"
---
# <a name="d3ddevinfo_d3d9stagetimings-structure"></a><span data-ttu-id="9258b-103">D3DDEVINFO \_ D3D9STAGETIMINGS-Struktur</span><span class="sxs-lookup"><span data-stu-id="9258b-103">D3DDEVINFO\_D3D9STAGETIMINGS structure</span></span>

<span data-ttu-id="9258b-104">Der Prozentsatz der Zeit, die shaderdaten verarbeitet.</span><span class="sxs-lookup"><span data-stu-id="9258b-104">Percent of time processing shader data.</span></span>

## <a name="syntax"></a><span data-ttu-id="9258b-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="9258b-105">Syntax</span></span>


```C++
typedef struct D3DDEVINFO_D3D9STAGETIMINGS {
  FLOAT MemoryProcessingPercent;
  FLOAT ComputationProcessingPercent;
} D3DDEVINFO_D3D9STAGETIMINGS, *LPD3DDEVINFO_D3D9STAGETIMINGS;
```



## <a name="members"></a><span data-ttu-id="9258b-106">Member</span><span class="sxs-lookup"><span data-stu-id="9258b-106">Members</span></span>

<dl> <dt>

<span data-ttu-id="9258b-107">**Memoryprocessingprozent**</span><span class="sxs-lookup"><span data-stu-id="9258b-107">**MemoryProcessingPercent**</span></span>
</dt> <dd>

<span data-ttu-id="9258b-108">Typ: **[ **float**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="9258b-108">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

</dd> <dd>

<span data-ttu-id="9258b-109">Der Prozentsatz der Zeit im Shader, der für Speicherzugriffe aufgewendet wurde.</span><span class="sxs-lookup"><span data-stu-id="9258b-109">Percent of time in shader spent on memory accesses.</span></span>

</dd> <dt>

<span data-ttu-id="9258b-110">**Computationprocessingprozent**</span><span class="sxs-lookup"><span data-stu-id="9258b-110">**ComputationProcessingPercent**</span></span>
</dt> <dd>

<span data-ttu-id="9258b-111">Typ: **[ **float**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="9258b-111">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

</dd> <dd>

<span data-ttu-id="9258b-112">Prozentsatz der Zeit Verarbeitung (Verschieben von Daten in Registern oder Durchführung mathematischer Vorgänge).</span><span class="sxs-lookup"><span data-stu-id="9258b-112">Percent of time processing (moving data around in registers or doing mathematical operations).</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="9258b-113">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="9258b-113">Remarks</span></span>

<span data-ttu-id="9258b-114">Um eine optimale Leistung zu erzielen, wird eine ausgeglichene Auslastung empfohlen.</span><span class="sxs-lookup"><span data-stu-id="9258b-114">For best performance, a balanced load is recommended.</span></span>

## <a name="requirements"></a><span data-ttu-id="9258b-115">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="9258b-115">Requirements</span></span>



| <span data-ttu-id="9258b-116">Anforderung</span><span class="sxs-lookup"><span data-stu-id="9258b-116">Requirement</span></span> | <span data-ttu-id="9258b-117">Wert</span><span class="sxs-lookup"><span data-stu-id="9258b-117">Value</span></span> |
|-------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="9258b-118">Header</span><span class="sxs-lookup"><span data-stu-id="9258b-118">Header</span></span><br/> | <dl> <span data-ttu-id="9258b-119"><dt>D3D9Types. h</dt></span><span class="sxs-lookup"><span data-stu-id="9258b-119"><dt>D3D9Types.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="9258b-120">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="9258b-120">See also</span></span>

<dl> <dt>

[<span data-ttu-id="9258b-121">Direct3D-Strukturen</span><span class="sxs-lookup"><span data-stu-id="9258b-121">Direct3D Structures</span></span>](dx9-graphics-reference-d3d-structures.md)
</dt> <dt>

[<span data-ttu-id="9258b-122">**GetData**</span><span class="sxs-lookup"><span data-stu-id="9258b-122">**GetData**</span></span>](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3dquery9-getdata)
</dt> </dl>

 

 
