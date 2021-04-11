---
description: Gibt die Identitäts-Quaternion zurück.
ms.assetid: 8088897b-5755-4ea0-afef-bd49d1921f5c
title: D3DXQuaternionIdentity-Funktion (D3dx9math. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXQuaternionIdentity
api_type:
- LibDef
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: e2db9dd0638f5ba67b2dc2e8b8c248889225aaca
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/15/2021
ms.locfileid: "104354646"
---
# <a name="d3dxquaternionidentity-function"></a><span data-ttu-id="76546-103">D3DXQuaternionIdentity-Funktion</span><span class="sxs-lookup"><span data-stu-id="76546-103">D3DXQuaternionIdentity function</span></span>

<span data-ttu-id="76546-104">Gibt die Identitäts-Quaternion zurück.</span><span class="sxs-lookup"><span data-stu-id="76546-104">Returns the identity quaternion.</span></span>

## <a name="syntax"></a><span data-ttu-id="76546-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="76546-105">Syntax</span></span>


```C++
D3DXQUATERNION* D3DXQuaternionIdentity(
  _Inout_ D3DXQUATERNION *pOut
);
```



## <a name="parameters"></a><span data-ttu-id="76546-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="76546-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="76546-107">*Pout* \[ in, out\]</span><span class="sxs-lookup"><span data-stu-id="76546-107">*pOut* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="76546-108">Typ: **[ **D3DXQUATERNION**](d3dxquaternion.md)\***</span><span class="sxs-lookup"><span data-stu-id="76546-108">Type: **[**D3DXQUATERNION**](d3dxquaternion.md)\***</span></span>

<span data-ttu-id="76546-109">Ein Zeiger auf die [**D3DXQUATERNION**](d3dxquaternion.md) -Struktur, die das Ergebnis des Vorgangs ist.</span><span class="sxs-lookup"><span data-stu-id="76546-109">Pointer to the [**D3DXQUATERNION**](d3dxquaternion.md) structure that is the result of the operation.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="76546-110">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="76546-110">Return value</span></span>

<span data-ttu-id="76546-111">Typ: **[ **D3DXQUATERNION**](d3dxquaternion.md)\***</span><span class="sxs-lookup"><span data-stu-id="76546-111">Type: **[**D3DXQUATERNION**](d3dxquaternion.md)\***</span></span>

<span data-ttu-id="76546-112">Ein Zeiger auf die [**D3DXQUATERNION**](d3dxquaternion.md) -Struktur, die die Identitäts-Quaternion ist.</span><span class="sxs-lookup"><span data-stu-id="76546-112">Pointer to the [**D3DXQUATERNION**](d3dxquaternion.md) structure that is the identity quaternion.</span></span>

## <a name="remarks"></a><span data-ttu-id="76546-113">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="76546-113">Remarks</span></span>

<span data-ttu-id="76546-114">Wenn eine Quaternion (x, y, z, w) angegeben wird, gibt die **D3DXQuaternionIdentity** -Funktion die Quaternion (0,0) zurück.</span><span class="sxs-lookup"><span data-stu-id="76546-114">Given a quaternion (x, y, z, w), the **D3DXQuaternionIdentity** function will return the quaternion (0, 0, 0, 1).</span></span>

<span data-ttu-id="76546-115">Der Rückgabewert für diese Funktion ist derselbe Wert, der im *Pout* -Parameter zurückgegeben wird.</span><span class="sxs-lookup"><span data-stu-id="76546-115">The return value for this function is the same value returned in the *pOut* parameter.</span></span> <span data-ttu-id="76546-116">Auf diese Weise kann die **D3DXQuaternionIdentity** -Funktion als Parameter für eine andere Funktion verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="76546-116">In this way, the **D3DXQuaternionIdentity** function can be used as a parameter for another function.</span></span>

<span data-ttu-id="76546-117">Verwenden Sie [**D3DXQuaternionNormalize**](d3dxquaternionnormalize.md) für eine beliebige Quaternion-Eingabe, die nicht bereits normalisiert ist.</span><span class="sxs-lookup"><span data-stu-id="76546-117">Use [**D3DXQuaternionNormalize**](d3dxquaternionnormalize.md) for any quaternion input that is not already normalized.</span></span>

## <a name="requirements"></a><span data-ttu-id="76546-118">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="76546-118">Requirements</span></span>



| <span data-ttu-id="76546-119">Anforderung</span><span class="sxs-lookup"><span data-stu-id="76546-119">Requirement</span></span> | <span data-ttu-id="76546-120">Wert</span><span class="sxs-lookup"><span data-stu-id="76546-120">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="76546-121">Header</span><span class="sxs-lookup"><span data-stu-id="76546-121">Header</span></span><br/>  | <dl> <span data-ttu-id="76546-122"><dt>D3dx9math. h</dt></span><span class="sxs-lookup"><span data-stu-id="76546-122"><dt>D3dx9math.h</dt></span></span> </dl> |
| <span data-ttu-id="76546-123">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="76546-123">Library</span></span><br/> | <dl> <span data-ttu-id="76546-124"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="76546-124"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="76546-125">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="76546-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="76546-126">Mathematische Funktionen</span><span class="sxs-lookup"><span data-stu-id="76546-126">Math Functions</span></span>](dx9-graphics-reference-d3dx-functions-math.md)
</dt> <dt>

[<span data-ttu-id="76546-127">**D3DXQuaternionIsIdentity**</span><span class="sxs-lookup"><span data-stu-id="76546-127">**D3DXQuaternionIsIdentity**</span></span>](d3dxquaternionisidentity.md)
</dt> </dl>

 

 




