---
description: Konvertiert ein Array von 32-Bit-Gleit Komma Zahlen in 16-Bit-Gleit Komma Zahlen.
ms.assetid: 00f7ae77-d2b5-4244-8fe9-6fea475700b7
title: D3DXFloat32To16Array-Funktion (D3dx9math. h)
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
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 360aebd5dd1af45fdc6fb5b9c23c514252f0ccf3
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/15/2021
ms.locfileid: "106371914"
---
# <a name="d3dxfloat32to16array-function-d3dx9mathh"></a><span data-ttu-id="99dc5-103">D3DXFloat32To16Array-Funktion (D3dx9math. h)</span><span class="sxs-lookup"><span data-stu-id="99dc5-103">D3DXFloat32To16Array function (D3dx9math.h)</span></span>

<span data-ttu-id="99dc5-104">Konvertiert ein Array von 32-Bit-Gleit Komma Zahlen in 16-Bit-Gleit Komma Zahlen.</span><span class="sxs-lookup"><span data-stu-id="99dc5-104">Converts an array of 32-bit floats to 16-bit floats.</span></span>

## <a name="syntax"></a><span data-ttu-id="99dc5-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="99dc5-105">Syntax</span></span>


```C++
D3DXFLOAT16* D3DXFloat32To16Array(
  _Inout_       D3DXFLOAT16 *pOut,
  _In_    const FLOAT       *pIn,
  _In_          UINT        n
);
```



## <a name="parameters"></a><span data-ttu-id="99dc5-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="99dc5-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="99dc5-107">*Pout* \[ in, out\]</span><span class="sxs-lookup"><span data-stu-id="99dc5-107">*pOut* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="99dc5-108">Typ: **[ **D3DXFLOAT16**](d3dxfloat16.md)\***</span><span class="sxs-lookup"><span data-stu-id="99dc5-108">Type: **[**D3DXFLOAT16**](d3dxfloat16.md)\***</span></span>

<span data-ttu-id="99dc5-109">Zeiger auf das Array von 16-Bit-Gleit Komma Zahlen.</span><span class="sxs-lookup"><span data-stu-id="99dc5-109">Pointer to the array of 16-bit floats.</span></span>

</dd> <dt>

<span data-ttu-id="99dc5-110">*pIn* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="99dc5-110">*pIn* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="99dc5-111">Typ: Konstante **[**float**](../winprog/windows-data-types.md) \***</span><span class="sxs-lookup"><span data-stu-id="99dc5-111">Type: **const [**FLOAT**](../winprog/windows-data-types.md)\***</span></span>

<span data-ttu-id="99dc5-112">Zeiger auf ein Array von 32-Bit-Gleit Komma Zahlen.</span><span class="sxs-lookup"><span data-stu-id="99dc5-112">Pointer to an array of 32-bit floats.</span></span>

</dd> <dt>

<span data-ttu-id="99dc5-113">*n* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="99dc5-113">*n* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="99dc5-114">Typ: **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="99dc5-114">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="99dc5-115">Die Anzahl der Elemente im Array.</span><span class="sxs-lookup"><span data-stu-id="99dc5-115">The number of elements in the array.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="99dc5-116">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="99dc5-116">Return value</span></span>

<span data-ttu-id="99dc5-117">Typ: **[ **D3DXFLOAT16**](d3dxfloat16.md)\***</span><span class="sxs-lookup"><span data-stu-id="99dc5-117">Type: **[**D3DXFLOAT16**](d3dxfloat16.md)\***</span></span>

<span data-ttu-id="99dc5-118">Zeiger auf ein Array von 16-Bit-Gleit Komma Zahlen.</span><span class="sxs-lookup"><span data-stu-id="99dc5-118">Pointer to an array of 16-bit floats.</span></span>

## <a name="requirements"></a><span data-ttu-id="99dc5-119">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="99dc5-119">Requirements</span></span>



| <span data-ttu-id="99dc5-120">Anforderung</span><span class="sxs-lookup"><span data-stu-id="99dc5-120">Requirement</span></span> | <span data-ttu-id="99dc5-121">Wert</span><span class="sxs-lookup"><span data-stu-id="99dc5-121">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="99dc5-122">Header</span><span class="sxs-lookup"><span data-stu-id="99dc5-122">Header</span></span><br/>  | <dl> <span data-ttu-id="99dc5-123"><dt>D3dx9math. h</dt></span><span class="sxs-lookup"><span data-stu-id="99dc5-123"><dt>D3dx9math.h</dt></span></span> </dl> |
| <span data-ttu-id="99dc5-124">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="99dc5-124">Library</span></span><br/> | <dl> <span data-ttu-id="99dc5-125"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="99dc5-125"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="99dc5-126">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="99dc5-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="99dc5-127">Mathematische Funktionen</span><span class="sxs-lookup"><span data-stu-id="99dc5-127">Math Functions</span></span>](dx9-graphics-reference-d3dx-functions-math.md)
</dt> </dl>

 

 
