---
description: Konvertiert ein Array von 16-Bit-Gleit Komma Zahlen in 32-Bit-Gleit Komma Zahlen.
ms.assetid: cf07a21d-9ea3-4fbe-ab8f-564e2bbb8d60
title: D3DXFloat16To32Array-Funktion (D3DX10Math. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXFloat16To32Array
api_type:
- LibDef
api_location:
- D3DX10.lib
- D3DX10.dll
ms.openlocfilehash: a813553234c9e59ad34720da6f380977779e5d96
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/15/2021
ms.locfileid: "104354987"
---
# <a name="d3dxfloat16to32array-function-d3dx10mathh"></a><span data-ttu-id="9a55a-103">D3DXFloat16To32Array-Funktion (D3DX10Math. h)</span><span class="sxs-lookup"><span data-stu-id="9a55a-103">D3DXFloat16To32Array function (D3DX10Math.h)</span></span>

<span data-ttu-id="9a55a-104">Konvertiert ein Array von 16-Bit-Gleit Komma Zahlen in 32-Bit-Gleit Komma Zahlen.</span><span class="sxs-lookup"><span data-stu-id="9a55a-104">Converts an array of 16-bit floats to 32-bit floats.</span></span>

## <a name="syntax"></a><span data-ttu-id="9a55a-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="9a55a-105">Syntax</span></span>


```C++
FLOAT* D3DXFloat16To32Array(
  _In_       FLOAT       *pOut,
  _In_ const D3DXFLOAT16 *pIn,
  _In_       UINT        n
);
```



## <a name="parameters"></a><span data-ttu-id="9a55a-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="9a55a-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="9a55a-107">*Pout* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="9a55a-107">*pOut* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="9a55a-108">Typ: **[ **float**](../winprog/windows-data-types.md)\***</span><span class="sxs-lookup"><span data-stu-id="9a55a-108">Type: **[**FLOAT**](../winprog/windows-data-types.md)\***</span></span>

<span data-ttu-id="9a55a-109">Ein Zeiger auf das Array von 32-Bit-Gleit Komma Zahlen.</span><span class="sxs-lookup"><span data-stu-id="9a55a-109">Pointer to the array of 32-bit floats.</span></span>

</dd> <dt>

<span data-ttu-id="9a55a-110">*pIn* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="9a55a-110">*pIn* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="9a55a-111">Typ: **Konstanten [**D3DXFLOAT16**](../direct3d9/d3dxfloat16.md) \***</span><span class="sxs-lookup"><span data-stu-id="9a55a-111">Type: **const [**D3DXFLOAT16**](../direct3d9/d3dxfloat16.md)\***</span></span>

<span data-ttu-id="9a55a-112">Zeiger auf ein Array von 16-Bit-Gleit Komma Zahlen.</span><span class="sxs-lookup"><span data-stu-id="9a55a-112">Pointer to an array of 16-bit floats.</span></span>

</dd> <dt>

<span data-ttu-id="9a55a-113">*n* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="9a55a-113">*n* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="9a55a-114">Typ: **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="9a55a-114">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="9a55a-115">Anzahl der Elemente im Array.</span><span class="sxs-lookup"><span data-stu-id="9a55a-115">Number of elements in the array.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="9a55a-116">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="9a55a-116">Return value</span></span>

<span data-ttu-id="9a55a-117">Typ: **[ **float**](../winprog/windows-data-types.md)\***</span><span class="sxs-lookup"><span data-stu-id="9a55a-117">Type: **[**FLOAT**](../winprog/windows-data-types.md)\***</span></span>

<span data-ttu-id="9a55a-118">Zeiger auf ein Array von 32-Bit-Gleit Komma Zahlen.</span><span class="sxs-lookup"><span data-stu-id="9a55a-118">Pointer to an array of 32-bit floats.</span></span>

## <a name="requirements"></a><span data-ttu-id="9a55a-119">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="9a55a-119">Requirements</span></span>



| <span data-ttu-id="9a55a-120">Anforderung</span><span class="sxs-lookup"><span data-stu-id="9a55a-120">Requirement</span></span> | <span data-ttu-id="9a55a-121">Wert</span><span class="sxs-lookup"><span data-stu-id="9a55a-121">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="9a55a-122">Header</span><span class="sxs-lookup"><span data-stu-id="9a55a-122">Header</span></span><br/>  | <dl> <span data-ttu-id="9a55a-123"><dt>D3DX10Math. h</dt></span><span class="sxs-lookup"><span data-stu-id="9a55a-123"><dt>D3DX10Math.h</dt></span></span> </dl> |
| <span data-ttu-id="9a55a-124">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="9a55a-124">Library</span></span><br/> | <dl> <span data-ttu-id="9a55a-125"><dt>D3dx10. lib</dt></span><span class="sxs-lookup"><span data-stu-id="9a55a-125"><dt>D3DX10.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="9a55a-126">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="9a55a-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="9a55a-127">Mathematische Funktionen</span><span class="sxs-lookup"><span data-stu-id="9a55a-127">Math Functions</span></span>](d3d10-graphics-reference-d3dx10-functions-math.md)
</dt> </dl>

 

 
