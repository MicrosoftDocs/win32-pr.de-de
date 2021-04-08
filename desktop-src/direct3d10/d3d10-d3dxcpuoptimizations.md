---
description: Aktiviert oder deaktiviert CPU-Optimierungen.
ms.assetid: 6f73df12-f2fc-4651-b0f7-f7a55e534d3d
title: D3DXCpuOptimizations-Funktion (D3DX10Math. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXCpuOptimizations
api_type:
- LibDef
api_location:
- D3DX10.lib
- D3DX10.dll
ms.openlocfilehash: a0ef276e6d3303acd77c9580b55a9aa49dbe2087
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/15/2021
ms.locfileid: "103762201"
---
# <a name="d3dxcpuoptimizations-function"></a><span data-ttu-id="d1778-103">D3DXCpuOptimizations-Funktion</span><span class="sxs-lookup"><span data-stu-id="d1778-103">D3DXCpuOptimizations function</span></span>

<span data-ttu-id="d1778-104">Aktiviert oder deaktiviert CPU-Optimierungen.</span><span class="sxs-lookup"><span data-stu-id="d1778-104">Enables or disables CPU optimizations.</span></span>

## <a name="syntax"></a><span data-ttu-id="d1778-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="d1778-105">Syntax</span></span>


```C++
D3DX_CPU_OPTIMIZATION D3DXCpuOptimizations(
  _In_ BOOL Enable
);
```



## <a name="parameters"></a><span data-ttu-id="d1778-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="d1778-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="d1778-107">*Aktivieren* \[ von in\]</span><span class="sxs-lookup"><span data-stu-id="d1778-107">*Enable* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="d1778-108">Typ: **[ **bool**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="d1778-108">Type: **[**BOOL**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="d1778-109">" **True** ", um CPU-Optimierungen zu aktivieren; andernfalls **false**.</span><span class="sxs-lookup"><span data-stu-id="d1778-109">**TRUE** to enable CPU optimizations; otherwise **FALSE**.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="d1778-110">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="d1778-110">Return value</span></span>

<span data-ttu-id="d1778-111">Type: **[ **D3DX \_ CPU \_ Optimization**](d3dx-cpu-optimization.md)**</span><span class="sxs-lookup"><span data-stu-id="d1778-111">Type: **[**D3DX\_CPU\_OPTIMIZATION**](d3dx-cpu-optimization.md)**</span></span>

<span data-ttu-id="d1778-112">Gibt den Typ der erkannten CPU zurück, für den Optimierungen vorhanden sind (siehe [**D3DX \_ CPU \_ Optimization**](d3dx-cpu-optimization.md)).</span><span class="sxs-lookup"><span data-stu-id="d1778-112">Returns the type of CPU detected, and for which optimizations exist (see [**D3DX\_CPU\_OPTIMIZATION**](d3dx-cpu-optimization.md)).</span></span>

## <a name="requirements"></a><span data-ttu-id="d1778-113">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="d1778-113">Requirements</span></span>



| <span data-ttu-id="d1778-114">Anforderung</span><span class="sxs-lookup"><span data-stu-id="d1778-114">Requirement</span></span> | <span data-ttu-id="d1778-115">Wert</span><span class="sxs-lookup"><span data-stu-id="d1778-115">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="d1778-116">Header</span><span class="sxs-lookup"><span data-stu-id="d1778-116">Header</span></span><br/>  | <dl> <span data-ttu-id="d1778-117"><dt>D3DX10Math. h</dt></span><span class="sxs-lookup"><span data-stu-id="d1778-117"><dt>D3DX10Math.h</dt></span></span> </dl> |
| <span data-ttu-id="d1778-118">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="d1778-118">Library</span></span><br/> | <dl> <span data-ttu-id="d1778-119"><dt>D3dx10. lib</dt></span><span class="sxs-lookup"><span data-stu-id="d1778-119"><dt>D3DX10.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="d1778-120">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="d1778-120">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d1778-121">Mathematische Funktionen</span><span class="sxs-lookup"><span data-stu-id="d1778-121">Math Functions</span></span>](d3d10-graphics-reference-d3dx10-functions-math.md)
</dt> </dl>

 

 
