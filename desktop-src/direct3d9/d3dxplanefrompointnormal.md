---
description: 'D3DXPlaneFromPointNormal-Funktion (D3dx9math.h): Erstellt eine Ebene von einem Punkt und einer Normalen.'
ms.assetid: af396bbb-09b7-492f-a25f-9c950da7e605
title: D3DXPlaneFromPointNormal-Funktion (D3dx9math.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXPlaneFromPointNormal
api_type:
- LibDef
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: e34765d150932d6a7b3b0293e603237ffb2b45ad
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2021
ms.locfileid: "108098088"
---
# <a name="d3dxplanefrompointnormal-function-d3dx9mathh"></a><span data-ttu-id="297ed-103">D3DXPlaneFromPointNormal-Funktion (D3dx9math.h)</span><span class="sxs-lookup"><span data-stu-id="297ed-103">D3DXPlaneFromPointNormal function (D3dx9math.h)</span></span>

<span data-ttu-id="297ed-104">Erstellt eine Ebene aus einem Punkt und einer Normalen.</span><span class="sxs-lookup"><span data-stu-id="297ed-104">Constructs a plane from a point and a normal.</span></span>

## <a name="syntax"></a><span data-ttu-id="297ed-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="297ed-105">Syntax</span></span>


```C++
D3DXPLANE* D3DXPlaneFromPointNormal(
  _Inout_       D3DXPLANE   *pOut,
  _In_    const D3DXVECTOR3 *pPoint,
  _In_    const D3DXVECTOR3 *pNormal
);
```



## <a name="parameters"></a><span data-ttu-id="297ed-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="297ed-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="297ed-107">*pOut* \[ in, out\]</span><span class="sxs-lookup"><span data-stu-id="297ed-107">*pOut* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="297ed-108">Typ: **[ **D3DXPLANE**](d3dxplane.md)\***</span><span class="sxs-lookup"><span data-stu-id="297ed-108">Type: **[**D3DXPLANE**](d3dxplane.md)\***</span></span>

<span data-ttu-id="297ed-109">Zeiger auf die [**D3DXPLANE-Struktur,**](d3dxplane.md) die das Ergebnis des Vorgangs ist.</span><span class="sxs-lookup"><span data-stu-id="297ed-109">Pointer to the [**D3DXPLANE**](d3dxplane.md) structure that is the result of the operation.</span></span>

</dd> <dt>

<span data-ttu-id="297ed-110">*pPoint* \[ In\]</span><span class="sxs-lookup"><span data-stu-id="297ed-110">*pPoint* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="297ed-111">Typ: **const [**D3DXVECTOR3**](d3dxvector3.md) \***</span><span class="sxs-lookup"><span data-stu-id="297ed-111">Type: **const [**D3DXVECTOR3**](d3dxvector3.md)\***</span></span>

<span data-ttu-id="297ed-112">Zeiger auf eine [**D3DXVECTOR3-Struktur,**](d3dxvector3.md) die den Punkt definiert, der zum Erstellen der Ebene verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="297ed-112">Pointer to a [**D3DXVECTOR3**](d3dxvector3.md) structure, defining the point used to construct the plane.</span></span>

</dd> <dt>

<span data-ttu-id="297ed-113">*pNormal* \[ In\]</span><span class="sxs-lookup"><span data-stu-id="297ed-113">*pNormal* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="297ed-114">Typ: **const [**D3DXVECTOR3**](d3dxvector3.md) \***</span><span class="sxs-lookup"><span data-stu-id="297ed-114">Type: **const [**D3DXVECTOR3**](d3dxvector3.md)\***</span></span>

<span data-ttu-id="297ed-115">Zeiger auf eine [**D3DXVECTOR3-Struktur,**](d3dxvector3.md) die die zum Erstellen der Ebene verwendete Normalstruktur definiert.</span><span class="sxs-lookup"><span data-stu-id="297ed-115">Pointer to a [**D3DXVECTOR3**](d3dxvector3.md) structure, defining the normal used to construct the plane.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="297ed-116">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="297ed-116">Return value</span></span>

<span data-ttu-id="297ed-117">Typ: **[ **D3DXPLANE**](d3dxplane.md)\***</span><span class="sxs-lookup"><span data-stu-id="297ed-117">Type: **[**D3DXPLANE**](d3dxplane.md)\***</span></span>

<span data-ttu-id="297ed-118">Zeiger auf die [**D3DXPLANE-Struktur,**](d3dxplane.md) die vom Punkt und der Normalität erstellt wurde.</span><span class="sxs-lookup"><span data-stu-id="297ed-118">Pointer to the [**D3DXPLANE**](d3dxplane.md) structure constructed from the point and the normal.</span></span>

## <a name="remarks"></a><span data-ttu-id="297ed-119">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="297ed-119">Remarks</span></span>

<span data-ttu-id="297ed-120">Der Rückgabewert für diese Funktion ist der gleiche Wert, der im *pOut-Parameter* zurückgegeben wird.</span><span class="sxs-lookup"><span data-stu-id="297ed-120">The return value for this function is the same value returned in the *pOut* parameter.</span></span> <span data-ttu-id="297ed-121">Auf diese Weise kann die **D3DXPlaneFromPointNormal-Funktion** als Parameter für eine andere Funktion verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="297ed-121">In this way, the **D3DXPlaneFromPointNormal** function can be used as a parameter for another function.</span></span>

## <a name="requirements"></a><span data-ttu-id="297ed-122">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="297ed-122">Requirements</span></span>



| <span data-ttu-id="297ed-123">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="297ed-123">Requirement</span></span> | <span data-ttu-id="297ed-124">Wert</span><span class="sxs-lookup"><span data-stu-id="297ed-124">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="297ed-125">Header</span><span class="sxs-lookup"><span data-stu-id="297ed-125">Header</span></span><br/>  | <dl> <span data-ttu-id="297ed-126"><dt>D3dx9math.h</dt></span><span class="sxs-lookup"><span data-stu-id="297ed-126"><dt>D3dx9math.h</dt></span></span> </dl> |
| <span data-ttu-id="297ed-127">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="297ed-127">Library</span></span><br/> | <dl> <span data-ttu-id="297ed-128"><dt>D3dx9.lib</dt></span><span class="sxs-lookup"><span data-stu-id="297ed-128"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="297ed-129">Weitere Informationen</span><span class="sxs-lookup"><span data-stu-id="297ed-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="297ed-130">Mathematische Funktionen</span><span class="sxs-lookup"><span data-stu-id="297ed-130">Math Functions</span></span>](dx9-graphics-reference-d3dx-functions-math.md)
</dt> <dt>

[<span data-ttu-id="297ed-131">**D3DXPlaneFromPoints**</span><span class="sxs-lookup"><span data-stu-id="297ed-131">**D3DXPlaneFromPoints**</span></span>](d3dxplanefrompoints.md)
</dt> </dl>

 

 




