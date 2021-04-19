---
description: Konvertiert ein Array von 32-Bit-Gleit Komma Zahlen in 16-Bit-Gleit Komma Zahlen.
ms.assetid: 2114cf25-cc83-4c4a-9db5-ecc0f8ff1e85
title: D3DXFloat32To16Array-Funktion (D3DX10Math. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXFloat32To16Array
api_type:
- LibDef
api_location:
- D3DX10.lib
- D3DX10.dll
ms.openlocfilehash: a4c116212be0ffa71ee35939d0a30a40cbb773b3
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/15/2021
ms.locfileid: "106361892"
---
# <a name="d3dxfloat32to16array-function-d3dx10mathh"></a><span data-ttu-id="43f74-103">D3DXFloat32To16Array-Funktion (D3DX10Math. h)</span><span class="sxs-lookup"><span data-stu-id="43f74-103">D3DXFloat32To16Array function (D3DX10Math.h)</span></span>

<span data-ttu-id="43f74-104">Konvertiert ein Array von 32-Bit-Gleit Komma Zahlen in 16-Bit-Gleit Komma Zahlen.</span><span class="sxs-lookup"><span data-stu-id="43f74-104">Converts an array of 32-bit floats to 16-bit floats.</span></span>

## <a name="syntax"></a><span data-ttu-id="43f74-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="43f74-105">Syntax</span></span>


```C++
D3DXFLOAT16* D3DXFloat32To16Array(
  _In_       D3DXFLOAT16 *pOut,
  _In_ const FLOAT       *pIn,
  _In_       UINT        n
);
```



## <a name="parameters"></a><span data-ttu-id="43f74-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="43f74-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="43f74-107">*Pout* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="43f74-107">*pOut* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="43f74-108">Typ: **[ **D3DXFLOAT16**](../direct3d9/d3dxfloat16.md)\***</span><span class="sxs-lookup"><span data-stu-id="43f74-108">Type: **[**D3DXFLOAT16**](../direct3d9/d3dxfloat16.md)\***</span></span>

<span data-ttu-id="43f74-109">Zeiger auf das Array von 16-Bit-Gleit Komma Zahlen.</span><span class="sxs-lookup"><span data-stu-id="43f74-109">Pointer to the array of 16-bit floats.</span></span>

</dd> <dt>

<span data-ttu-id="43f74-110">*pIn* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="43f74-110">*pIn* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="43f74-111">Typ: Konstante **[**float**](../winprog/windows-data-types.md) \***</span><span class="sxs-lookup"><span data-stu-id="43f74-111">Type: **const [**FLOAT**](../winprog/windows-data-types.md)\***</span></span>

<span data-ttu-id="43f74-112">Zeiger auf ein Array von 32-Bit-Gleit Komma Zahlen.</span><span class="sxs-lookup"><span data-stu-id="43f74-112">Pointer to an array of 32-bit floats.</span></span>

</dd> <dt>

<span data-ttu-id="43f74-113">*n* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="43f74-113">*n* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="43f74-114">Typ: **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="43f74-114">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="43f74-115">Die Anzahl der Elemente im Array.</span><span class="sxs-lookup"><span data-stu-id="43f74-115">The number of elements in the array.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="43f74-116">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="43f74-116">Return value</span></span>

<span data-ttu-id="43f74-117">Typ: **[ **D3DXFLOAT16**](../direct3d9/d3dxfloat16.md)\***</span><span class="sxs-lookup"><span data-stu-id="43f74-117">Type: **[**D3DXFLOAT16**](../direct3d9/d3dxfloat16.md)\***</span></span>

<span data-ttu-id="43f74-118">Zeiger auf ein Array von 16-Bit-Gleit Komma Zahlen.</span><span class="sxs-lookup"><span data-stu-id="43f74-118">Pointer to an array of 16-bit floats.</span></span>

## <a name="requirements"></a><span data-ttu-id="43f74-119">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="43f74-119">Requirements</span></span>



| <span data-ttu-id="43f74-120">Anforderung</span><span class="sxs-lookup"><span data-stu-id="43f74-120">Requirement</span></span> | <span data-ttu-id="43f74-121">Wert</span><span class="sxs-lookup"><span data-stu-id="43f74-121">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="43f74-122">Header</span><span class="sxs-lookup"><span data-stu-id="43f74-122">Header</span></span><br/>  | <dl> <span data-ttu-id="43f74-123"><dt>D3DX10Math. h</dt></span><span class="sxs-lookup"><span data-stu-id="43f74-123"><dt>D3DX10Math.h</dt></span></span> </dl> |
| <span data-ttu-id="43f74-124">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="43f74-124">Library</span></span><br/> | <dl> <span data-ttu-id="43f74-125"><dt>D3dx10. lib</dt></span><span class="sxs-lookup"><span data-stu-id="43f74-125"><dt>D3DX10.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="43f74-126">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="43f74-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="43f74-127">Mathematische Funktionen</span><span class="sxs-lookup"><span data-stu-id="43f74-127">Math Functions</span></span>](d3d10-graphics-reference-d3dx10-functions-math.md)
</dt> </dl>

 

 
