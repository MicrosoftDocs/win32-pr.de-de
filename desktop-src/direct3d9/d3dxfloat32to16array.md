---
description: 'D3DXFloat32To16Array-Funktion (D3dx9math.h): Konvertiert ein Array von 32-Bit-Gleitkommaen in 16-Bit-Gleitkommakomma.'
ms.assetid: 00f7ae77-d2b5-4244-8fe9-6fea475700b7
title: D3DXFloat32To16Array-Funktion (D3dx9math.h)
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
ms.openlocfilehash: dc00df150c48e285d5478eb9b11df6c5203d6bcc
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2021
ms.locfileid: "108094258"
---
# <a name="d3dxfloat32to16array-function-d3dx9mathh"></a><span data-ttu-id="0ec84-103">D3DXFloat32To16Array-Funktion (D3dx9math.h)</span><span class="sxs-lookup"><span data-stu-id="0ec84-103">D3DXFloat32To16Array function (D3dx9math.h)</span></span>

<span data-ttu-id="0ec84-104">Konvertiert ein Array von 32-Bit-Gleitkommaen in 16-Bit-Gleitkommakomma.</span><span class="sxs-lookup"><span data-stu-id="0ec84-104">Converts an array of 32-bit floats to 16-bit floats.</span></span>

## <a name="syntax"></a><span data-ttu-id="0ec84-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="0ec84-105">Syntax</span></span>


```C++
D3DXFLOAT16* D3DXFloat32To16Array(
  _Inout_       D3DXFLOAT16 *pOut,
  _In_    const FLOAT       *pIn,
  _In_          UINT        n
);
```



## <a name="parameters"></a><span data-ttu-id="0ec84-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="0ec84-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="0ec84-107">*pOut* \[ in, out\]</span><span class="sxs-lookup"><span data-stu-id="0ec84-107">*pOut* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="0ec84-108">Typ: **[ **D3DXFLOAT16**](d3dxfloat16.md)\***</span><span class="sxs-lookup"><span data-stu-id="0ec84-108">Type: **[**D3DXFLOAT16**](d3dxfloat16.md)\***</span></span>

<span data-ttu-id="0ec84-109">Zeiger auf das Array von 16-Bit-Gleitkommaen.</span><span class="sxs-lookup"><span data-stu-id="0ec84-109">Pointer to the array of 16-bit floats.</span></span>

</dd> <dt>

<span data-ttu-id="0ec84-110">*pIn* \[ In\]</span><span class="sxs-lookup"><span data-stu-id="0ec84-110">*pIn* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="0ec84-111">Typ: **const [**FLOAT**](../winprog/windows-data-types.md) \***</span><span class="sxs-lookup"><span data-stu-id="0ec84-111">Type: **const [**FLOAT**](../winprog/windows-data-types.md)\***</span></span>

<span data-ttu-id="0ec84-112">Zeiger auf ein Array von 32-Bit-Gleitkommaen.</span><span class="sxs-lookup"><span data-stu-id="0ec84-112">Pointer to an array of 32-bit floats.</span></span>

</dd> <dt>

<span data-ttu-id="0ec84-113">*n* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="0ec84-113">*n* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="0ec84-114">Typ: **[ **UINT**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="0ec84-114">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="0ec84-115">Die Anzahl der Elemente im Array.</span><span class="sxs-lookup"><span data-stu-id="0ec84-115">The number of elements in the array.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="0ec84-116">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="0ec84-116">Return value</span></span>

<span data-ttu-id="0ec84-117">Typ: **[ **D3DXFLOAT16**](d3dxfloat16.md)\***</span><span class="sxs-lookup"><span data-stu-id="0ec84-117">Type: **[**D3DXFLOAT16**](d3dxfloat16.md)\***</span></span>

<span data-ttu-id="0ec84-118">Zeiger auf ein Array von 16-Bit-Gleitkommaen.</span><span class="sxs-lookup"><span data-stu-id="0ec84-118">Pointer to an array of 16-bit floats.</span></span>

## <a name="requirements"></a><span data-ttu-id="0ec84-119">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="0ec84-119">Requirements</span></span>



| <span data-ttu-id="0ec84-120">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="0ec84-120">Requirement</span></span> | <span data-ttu-id="0ec84-121">Wert</span><span class="sxs-lookup"><span data-stu-id="0ec84-121">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="0ec84-122">Header</span><span class="sxs-lookup"><span data-stu-id="0ec84-122">Header</span></span><br/>  | <dl> <span data-ttu-id="0ec84-123"><dt>D3dx9math.h</dt></span><span class="sxs-lookup"><span data-stu-id="0ec84-123"><dt>D3dx9math.h</dt></span></span> </dl> |
| <span data-ttu-id="0ec84-124">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="0ec84-124">Library</span></span><br/> | <dl> <span data-ttu-id="0ec84-125"><dt>D3dx9.lib</dt></span><span class="sxs-lookup"><span data-stu-id="0ec84-125"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="0ec84-126">Weitere Informationen</span><span class="sxs-lookup"><span data-stu-id="0ec84-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="0ec84-127">Mathematische Funktionen</span><span class="sxs-lookup"><span data-stu-id="0ec84-127">Math Functions</span></span>](dx9-graphics-reference-d3dx-functions-math.md)
</dt> </dl>

 

 
