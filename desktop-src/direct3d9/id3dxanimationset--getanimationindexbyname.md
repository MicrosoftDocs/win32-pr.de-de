---
description: Ruft den Index einer Animation ab, wenn der Name angegeben wird.
ms.assetid: 6e91a4fe-3202-447b-b486-d29e8da64af2
title: 'ID3DXAnimationSet:: getanimationindexbyname-Methode (D3dx9anim. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXAnimationSet.GetAnimationIndexByName
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: f4d3e5fb39ebcfa5ce906d1f90c2c5c10bdd4b3d
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/15/2021
ms.locfileid: "106367353"
---
# <a name="id3dxanimationsetgetanimationindexbyname-method"></a><span data-ttu-id="35b32-103">ID3DXAnimationSet:: getanimationindexbyname-Methode</span><span class="sxs-lookup"><span data-stu-id="35b32-103">ID3DXAnimationSet::GetAnimationIndexByName method</span></span>

<span data-ttu-id="35b32-104">Ruft den Index einer Animation ab, wenn der Name angegeben wird.</span><span class="sxs-lookup"><span data-stu-id="35b32-104">Gets the index of an animation, given its name.</span></span>

## <a name="syntax"></a><span data-ttu-id="35b32-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="35b32-105">Syntax</span></span>


```C++
HRESULT GetAnimationIndexByName(
  [in]  LPCSTR pName,
  [out] UINT   *pIndex
);
```



## <a name="parameters"></a><span data-ttu-id="35b32-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="35b32-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="35b32-107">*PName* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="35b32-107">*pName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="35b32-108">Typ: **[ **LPCSTR**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="35b32-108">Type: **[**LPCSTR**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="35b32-109">Der Name der Animation.</span><span class="sxs-lookup"><span data-stu-id="35b32-109">Name of the animation.</span></span>

</dd> <dt>

<span data-ttu-id="35b32-110">*pIndex* \[ vorgenommen\]</span><span class="sxs-lookup"><span data-stu-id="35b32-110">*pIndex* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="35b32-111">Typ: **[ **uint**](../winprog/windows-data-types.md)\***</span><span class="sxs-lookup"><span data-stu-id="35b32-111">Type: **[**UINT**](../winprog/windows-data-types.md)\***</span></span>

<span data-ttu-id="35b32-112">Zeiger auf den Animations Index.</span><span class="sxs-lookup"><span data-stu-id="35b32-112">Pointer to the animation index.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="35b32-113">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="35b32-113">Return value</span></span>

<span data-ttu-id="35b32-114">Typ: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="35b32-114">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="35b32-115">Die Rückgabewerte dieser Methode werden von einem Anwendungsprogrammierer implementiert.</span><span class="sxs-lookup"><span data-stu-id="35b32-115">The return values of this method are implemented by an application programmer.</span></span> <span data-ttu-id="35b32-116">Wenn kein Fehler auftritt, programmieren Sie im Allgemeinen die-Methode, um D3D OK zurückzugeben \_ .</span><span class="sxs-lookup"><span data-stu-id="35b32-116">In general, if no error occurs, program the method to return D3D\_OK.</span></span> <span data-ttu-id="35b32-117">Andernfalls programmieren Sie die-Methode, um eine entsprechende Fehlermeldung von [D3DERR](d3derr.md) oder [**D3DXERR**](./d3dxerr.md)zurückzugeben.</span><span class="sxs-lookup"><span data-stu-id="35b32-117">Otherwise, program the method to return an appropriate error message from [D3DERR](d3derr.md) or [**D3DXERR**](./d3dxerr.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="35b32-118">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="35b32-118">Requirements</span></span>



| <span data-ttu-id="35b32-119">Anforderung</span><span class="sxs-lookup"><span data-stu-id="35b32-119">Requirement</span></span> | <span data-ttu-id="35b32-120">Wert</span><span class="sxs-lookup"><span data-stu-id="35b32-120">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="35b32-121">Header</span><span class="sxs-lookup"><span data-stu-id="35b32-121">Header</span></span><br/>  | <dl> <span data-ttu-id="35b32-122"><dt>D3dx9anim. h</dt></span><span class="sxs-lookup"><span data-stu-id="35b32-122"><dt>D3dx9anim.h</dt></span></span> </dl> |
| <span data-ttu-id="35b32-123">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="35b32-123">Library</span></span><br/> | <dl> <span data-ttu-id="35b32-124"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="35b32-124"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="35b32-125">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="35b32-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="35b32-126">ID3DXAnimationSet</span><span class="sxs-lookup"><span data-stu-id="35b32-126">ID3DXAnimationSet</span></span>](id3dxanimationset.md)
</dt> </dl>

 

 
