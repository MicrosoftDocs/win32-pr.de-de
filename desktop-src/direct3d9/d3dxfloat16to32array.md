---
description: Konvertiert ein Array von 16-Bit-Gleit Komma Zahlen in 32-Bit-Gleit Komma Zahlen.
ms.assetid: cabb2888-76e4-403b-99ab-f7d62478bf43
title: D3DXFloat16To32Array-Funktion (D3dx9math. h)
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
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 6760ce36341883c26030df91d3d46b5b21fdb012
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/15/2021
ms.locfileid: "106355011"
---
# <a name="d3dxfloat16to32array-function-d3dx9mathh"></a><span data-ttu-id="84483-103">D3DXFloat16To32Array-Funktion (D3dx9math. h)</span><span class="sxs-lookup"><span data-stu-id="84483-103">D3DXFloat16To32Array function (D3dx9math.h)</span></span>

<span data-ttu-id="84483-104">Konvertiert ein Array von 16-Bit-Gleit Komma Zahlen in 32-Bit-Gleit Komma Zahlen.</span><span class="sxs-lookup"><span data-stu-id="84483-104">Converts an array of 16-bit floats to 32-bit floats.</span></span>

## <a name="syntax"></a><span data-ttu-id="84483-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="84483-105">Syntax</span></span>


```C++
FLOAT* D3DXFloat16To32Array(
  _Inout_       FLOAT       *pOut,
  _In_    const D3DXFLOAT16 *pIn,
  _In_          UINT        n
);
```



## <a name="parameters"></a><span data-ttu-id="84483-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="84483-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="84483-107">*Pout* \[ in, out\]</span><span class="sxs-lookup"><span data-stu-id="84483-107">*pOut* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="84483-108">Typ: **[ **float**](../winprog/windows-data-types.md)\***</span><span class="sxs-lookup"><span data-stu-id="84483-108">Type: **[**FLOAT**](../winprog/windows-data-types.md)\***</span></span>

<span data-ttu-id="84483-109">Ein Zeiger auf das Array von 32-Bit-Gleit Komma Zahlen.</span><span class="sxs-lookup"><span data-stu-id="84483-109">Pointer to the array of 32-bit floats.</span></span>

</dd> <dt>

<span data-ttu-id="84483-110">*pIn* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="84483-110">*pIn* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="84483-111">Typ: **Konstanten [**D3DXFLOAT16**](d3dxfloat16.md) \***</span><span class="sxs-lookup"><span data-stu-id="84483-111">Type: **const [**D3DXFLOAT16**](d3dxfloat16.md)\***</span></span>

<span data-ttu-id="84483-112">Zeiger auf ein Array von 16-Bit-Gleit Komma Zahlen.</span><span class="sxs-lookup"><span data-stu-id="84483-112">Pointer to an array of 16-bit floats.</span></span>

</dd> <dt>

<span data-ttu-id="84483-113">*n* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="84483-113">*n* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="84483-114">Typ: **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="84483-114">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="84483-115">Anzahl der Elemente im Array.</span><span class="sxs-lookup"><span data-stu-id="84483-115">Number of elements in the array.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="84483-116">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="84483-116">Return value</span></span>

<span data-ttu-id="84483-117">Typ: **[ **float**](../winprog/windows-data-types.md)\***</span><span class="sxs-lookup"><span data-stu-id="84483-117">Type: **[**FLOAT**](../winprog/windows-data-types.md)\***</span></span>

<span data-ttu-id="84483-118">Zeiger auf ein Array von 32-Bit-Gleit Komma Zahlen.</span><span class="sxs-lookup"><span data-stu-id="84483-118">Pointer to an array of 32-bit floats.</span></span>

## <a name="requirements"></a><span data-ttu-id="84483-119">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="84483-119">Requirements</span></span>



| <span data-ttu-id="84483-120">Anforderung</span><span class="sxs-lookup"><span data-stu-id="84483-120">Requirement</span></span> | <span data-ttu-id="84483-121">Wert</span><span class="sxs-lookup"><span data-stu-id="84483-121">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="84483-122">Header</span><span class="sxs-lookup"><span data-stu-id="84483-122">Header</span></span><br/>  | <dl> <span data-ttu-id="84483-123"><dt>D3dx9math. h</dt></span><span class="sxs-lookup"><span data-stu-id="84483-123"><dt>D3dx9math.h</dt></span></span> </dl> |
| <span data-ttu-id="84483-124">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="84483-124">Library</span></span><br/> | <dl> <span data-ttu-id="84483-125"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="84483-125"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="84483-126">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="84483-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="84483-127">Mathematische Funktionen</span><span class="sxs-lookup"><span data-stu-id="84483-127">Math Functions</span></span>](dx9-graphics-reference-d3dx-functions-math.md)
</dt> </dl>

 

 
