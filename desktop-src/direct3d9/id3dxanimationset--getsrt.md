---
description: Ruft die Skalierungs-, Drehungs-und Übersetzungs Werte des Animations Satzes ab.
ms.assetid: 84fc56f3-15bf-4e27-ad06-57fab94f3a33
title: 'ID3DXAnimationSet:: getrt-Methode (D3dx9anim. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXAnimationSet.GetSRT
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: b70243dd9aa2f304d80eaff2e2cc7695dad43379
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/15/2021
ms.locfileid: "106355842"
---
# <a name="id3dxanimationsetgetsrt-method"></a><span data-ttu-id="e775c-103">ID3DXAnimationSet:: gezrt-Methode</span><span class="sxs-lookup"><span data-stu-id="e775c-103">ID3DXAnimationSet::GetSRT method</span></span>

<span data-ttu-id="e775c-104">Ruft die Skalierungs-, Drehungs-und Übersetzungs Werte des Animations Satzes ab.</span><span class="sxs-lookup"><span data-stu-id="e775c-104">Gets the scale, rotation, and translation values of the animation set.</span></span>

## <a name="syntax"></a><span data-ttu-id="e775c-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="e775c-105">Syntax</span></span>


```C++
HRESULT GetSRT(
  [in]  DOUBLE         PeriodicPosition,
  [in]  UINT           Animation,
  [out] D3DXVECTOR3    *pScale,
  [out] D3DXQUATERNION *pRotation,
  [out] D3DXVECTOR3    *pTranslation
);
```



## <a name="parameters"></a><span data-ttu-id="e775c-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="e775c-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="e775c-107">*PeriodicPosition* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="e775c-107">*PeriodicPosition* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="e775c-108">Typ: **[ **Double**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="e775c-108">Type: **[**DOUBLE**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="e775c-109">Die Position des Animations Satzes.</span><span class="sxs-lookup"><span data-stu-id="e775c-109">Position of the animation set.</span></span> <span data-ttu-id="e775c-110">Die Position kann durch Aufrufen von [**ID3DXAnimationSet:: GetPeriodicPosition**](id3dxanimationset--getperiodicposition.md)abgerufen werden.</span><span class="sxs-lookup"><span data-stu-id="e775c-110">The position can be obtained by calling [**ID3DXAnimationSet::GetPeriodicPosition**](id3dxanimationset--getperiodicposition.md).</span></span>

</dd> <dt>

<span data-ttu-id="e775c-111">*Animation* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="e775c-111">*Animation* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="e775c-112">Typ: **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="e775c-112">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="e775c-113">Animations Index.</span><span class="sxs-lookup"><span data-stu-id="e775c-113">Animation index.</span></span>

</dd> <dt>

<span data-ttu-id="e775c-114">*pscale* \[ vorgenommen\]</span><span class="sxs-lookup"><span data-stu-id="e775c-114">*pScale* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="e775c-115">Typ: **[ **D3DXVECTOR3**](d3dxvector3.md)\***</span><span class="sxs-lookup"><span data-stu-id="e775c-115">Type: **[**D3DXVECTOR3**](d3dxvector3.md)\***</span></span>

<span data-ttu-id="e775c-116">Ein Zeiger auf den [**D3DXVECTOR3**](d3dxvector3.md) -Vektor, der die Skala des Animations Satzes beschreibt.</span><span class="sxs-lookup"><span data-stu-id="e775c-116">Pointer to the [**D3DXVECTOR3**](d3dxvector3.md) vector that describes the scale of the animation set.</span></span>

</dd> <dt>

<span data-ttu-id="e775c-117">*protation* \[ vorgenommen\]</span><span class="sxs-lookup"><span data-stu-id="e775c-117">*pRotation* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="e775c-118">Typ: **[ **D3DXQUATERNION**](d3dxquaternion.md)\***</span><span class="sxs-lookup"><span data-stu-id="e775c-118">Type: **[**D3DXQUATERNION**](d3dxquaternion.md)\***</span></span>

<span data-ttu-id="e775c-119">Ein Zeiger auf die [**D3DXQUATERNION**](d3dxquaternion.md) Quaternion, die die Drehung des Animations Satzes beschreibt.</span><span class="sxs-lookup"><span data-stu-id="e775c-119">Pointer to the [**D3DXQUATERNION**](d3dxquaternion.md) quaternion that describes the rotation of the animation set.</span></span>

</dd> <dt>

<span data-ttu-id="e775c-120">*ptranslation* \[ vorgenommen\]</span><span class="sxs-lookup"><span data-stu-id="e775c-120">*pTranslation* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="e775c-121">Typ: **[ **D3DXVECTOR3**](d3dxvector3.md)\***</span><span class="sxs-lookup"><span data-stu-id="e775c-121">Type: **[**D3DXVECTOR3**](d3dxvector3.md)\***</span></span>

<span data-ttu-id="e775c-122">Ein Zeiger auf den [**D3DXVECTOR3**](d3dxvector3.md) -Vektor, der die Übersetzung des Animations Satzes beschreibt.</span><span class="sxs-lookup"><span data-stu-id="e775c-122">Pointer to the [**D3DXVECTOR3**](d3dxvector3.md) vector that describes the translation of the animation set.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="e775c-123">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="e775c-123">Return value</span></span>

<span data-ttu-id="e775c-124">Typ: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="e775c-124">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="e775c-125">Die Rückgabewerte dieser Methode werden von einem Anwendungsprogrammierer implementiert.</span><span class="sxs-lookup"><span data-stu-id="e775c-125">The return values of this method are implemented by an application programmer.</span></span> <span data-ttu-id="e775c-126">Wenn kein Fehler auftritt, programmieren Sie im Allgemeinen die-Methode, um D3D OK zurückzugeben \_ .</span><span class="sxs-lookup"><span data-stu-id="e775c-126">In general, if no error occurs, program the method to return D3D\_OK.</span></span> <span data-ttu-id="e775c-127">Andernfalls programmieren Sie die-Methode, um eine entsprechende Fehlermeldung von [D3DERR](d3derr.md) oder [**D3DXERR**](./d3dxerr.md)zurückzugeben.</span><span class="sxs-lookup"><span data-stu-id="e775c-127">Otherwise, program the method to return an appropriate error message from [D3DERR](d3derr.md) or [**D3DXERR**](./d3dxerr.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="e775c-128">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="e775c-128">Requirements</span></span>



| <span data-ttu-id="e775c-129">Anforderung</span><span class="sxs-lookup"><span data-stu-id="e775c-129">Requirement</span></span> | <span data-ttu-id="e775c-130">Wert</span><span class="sxs-lookup"><span data-stu-id="e775c-130">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="e775c-131">Header</span><span class="sxs-lookup"><span data-stu-id="e775c-131">Header</span></span><br/>  | <dl> <span data-ttu-id="e775c-132"><dt>D3dx9anim. h</dt></span><span class="sxs-lookup"><span data-stu-id="e775c-132"><dt>D3dx9anim.h</dt></span></span> </dl> |
| <span data-ttu-id="e775c-133">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="e775c-133">Library</span></span><br/> | <dl> <span data-ttu-id="e775c-134"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="e775c-134"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="e775c-135">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="e775c-135">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e775c-136">ID3DXAnimationSet</span><span class="sxs-lookup"><span data-stu-id="e775c-136">ID3DXAnimationSet</span></span>](id3dxanimationset.md)
</dt> </dl>

 

 
