---
description: 'D3DXQuaternionNormalize-Funktion (D3dx9math.h): Berechnet eine Einheitslängen-Quaternion.'
ms.assetid: 31f56c2b-96b0-4110-a5b9-ce09983779b6
title: D3DXQuaternionNormalize-Funktion (D3dx9math.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXQuaternionNormalize
api_type:
- LibDef
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: a5d4a7938b96d3d8693fd2091fcbd4f664f465c5
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2021
ms.locfileid: "108094038"
---
# <a name="d3dxquaternionnormalize-function-d3dx9mathh"></a><span data-ttu-id="112c5-103">D3DXQuaternionNormalize-Funktion (D3dx9math.h)</span><span class="sxs-lookup"><span data-stu-id="112c5-103">D3DXQuaternionNormalize function (D3dx9math.h)</span></span>

<span data-ttu-id="112c5-104">Berechnet eine Einheitslängen-Quaternion.</span><span class="sxs-lookup"><span data-stu-id="112c5-104">Computes a unit length quaternion.</span></span>

## <a name="syntax"></a><span data-ttu-id="112c5-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="112c5-105">Syntax</span></span>


```C++
D3DXQUATERNION* D3DXQuaternionNormalize(
  _Inout_       D3DXQUATERNION *pOut,
  _In_    const D3DXQUATERNION *pQ
);
```



## <a name="parameters"></a><span data-ttu-id="112c5-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="112c5-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="112c5-107">*pOut* \[ in, out\]</span><span class="sxs-lookup"><span data-stu-id="112c5-107">*pOut* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="112c5-108">Typ: **[ **D3DXQUATERNION**](d3dxquaternion.md)\***</span><span class="sxs-lookup"><span data-stu-id="112c5-108">Type: **[**D3DXQUATERNION**](d3dxquaternion.md)\***</span></span>

<span data-ttu-id="112c5-109">Zeiger auf die [**D3DXQUATERNION-Struktur,**](d3dxquaternion.md) die das Ergebnis des Vorgangs ist.</span><span class="sxs-lookup"><span data-stu-id="112c5-109">Pointer to the [**D3DXQUATERNION**](d3dxquaternion.md) structure that is the result of the operation.</span></span>

</dd> <dt>

<span data-ttu-id="112c5-110">*pQ* \[ In\]</span><span class="sxs-lookup"><span data-stu-id="112c5-110">*pQ* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="112c5-111">Typ: **const [**D3DXQUATERNION**](d3dxquaternion.md) \***</span><span class="sxs-lookup"><span data-stu-id="112c5-111">Type: **const [**D3DXQUATERNION**](d3dxquaternion.md)\***</span></span>

<span data-ttu-id="112c5-112">Zeiger auf die [**D3DXQUATERNION-Quellstruktur.**](d3dxquaternion.md)</span><span class="sxs-lookup"><span data-stu-id="112c5-112">Pointer to the source [**D3DXQUATERNION**](d3dxquaternion.md) structure.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="112c5-113">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="112c5-113">Return value</span></span>

<span data-ttu-id="112c5-114">Typ: **[ **D3DXQUATERNION**](d3dxquaternion.md)\***</span><span class="sxs-lookup"><span data-stu-id="112c5-114">Type: **[**D3DXQUATERNION**](d3dxquaternion.md)\***</span></span>

<span data-ttu-id="112c5-115">Zeiger auf eine [**D3DXQUATERNION-Struktur,**](d3dxquaternion.md) die die Normalität der Quaternion ist.</span><span class="sxs-lookup"><span data-stu-id="112c5-115">Pointer to a [**D3DXQUATERNION**](d3dxquaternion.md) structure that is the normal of the quaternion.</span></span>

## <a name="remarks"></a><span data-ttu-id="112c5-116">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="112c5-116">Remarks</span></span>

<span data-ttu-id="112c5-117">Der Rückgabewert für diese Funktion ist der gleiche Wert, der im *pOut-Parameter* zurückgegeben wird.</span><span class="sxs-lookup"><span data-stu-id="112c5-117">The return value for this function is the same value returned in the *pOut* parameter.</span></span> <span data-ttu-id="112c5-118">Auf diese Weise kann die **D3DXQuaternionNormalize-Funktion** als Parameter für eine andere Funktion verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="112c5-118">In this way, the **D3DXQuaternionNormalize** function can be used as a parameter for another function.</span></span>

## <a name="requirements"></a><span data-ttu-id="112c5-119">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="112c5-119">Requirements</span></span>



| <span data-ttu-id="112c5-120">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="112c5-120">Requirement</span></span> | <span data-ttu-id="112c5-121">Wert</span><span class="sxs-lookup"><span data-stu-id="112c5-121">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="112c5-122">Header</span><span class="sxs-lookup"><span data-stu-id="112c5-122">Header</span></span><br/>  | <dl> <span data-ttu-id="112c5-123"><dt>D3dx9math.h</dt></span><span class="sxs-lookup"><span data-stu-id="112c5-123"><dt>D3dx9math.h</dt></span></span> </dl> |
| <span data-ttu-id="112c5-124">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="112c5-124">Library</span></span><br/> | <dl> <span data-ttu-id="112c5-125"><dt>D3dx9.lib</dt></span><span class="sxs-lookup"><span data-stu-id="112c5-125"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="112c5-126">Weitere Informationen</span><span class="sxs-lookup"><span data-stu-id="112c5-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="112c5-127">Mathematische Funktionen</span><span class="sxs-lookup"><span data-stu-id="112c5-127">Math Functions</span></span>](dx9-graphics-reference-d3dx-functions-math.md)
</dt> <dt>

[<span data-ttu-id="112c5-128">**D3DXQuaternionInverse**</span><span class="sxs-lookup"><span data-stu-id="112c5-128">**D3DXQuaternionInverse**</span></span>](d3dxquaternioninverse.md)
</dt> </dl>

 

 




