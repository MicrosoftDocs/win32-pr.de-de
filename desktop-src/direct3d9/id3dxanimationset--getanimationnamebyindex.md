---
description: Ruft den Namen einer Animation ab, wenn der Index angegeben wird.
ms.assetid: vs|directx_sdk|~\id3dxanimationset__getanimationnamebyindex.htm
title: 'ID3DXAnimationSet:: getanimationnamebyindex-Methode (D3dx9anim. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXAnimationSet.GetAnimationNameByIndex
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 820b21fa69fd7007bdd1971e83ea44368dce5cc2
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/15/2021
ms.locfileid: "106364369"
---
# <a name="id3dxanimationsetgetanimationnamebyindex-method"></a><span data-ttu-id="fb6cd-103">ID3DXAnimationSet:: getanimationnamebyindex-Methode</span><span class="sxs-lookup"><span data-stu-id="fb6cd-103">ID3DXAnimationSet::GetAnimationNameByIndex method</span></span>

<span data-ttu-id="fb6cd-104">Ruft den Namen einer Animation ab, wenn der Index angegeben wird.</span><span class="sxs-lookup"><span data-stu-id="fb6cd-104">Gets the name of an animation, given its index.</span></span>

## <a name="syntax"></a><span data-ttu-id="fb6cd-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="fb6cd-105">Syntax</span></span>


```C++
HRESULT GetAnimationNameByIndex(
  [in]  UINT   Index,
  [out] LPCSTR *ppName
);
```



## <a name="parameters"></a><span data-ttu-id="fb6cd-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="fb6cd-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="fb6cd-107">*Index* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="fb6cd-107">*Index* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="fb6cd-108">Typ: **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="fb6cd-108">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="fb6cd-109">Der Index der Animation.</span><span class="sxs-lookup"><span data-stu-id="fb6cd-109">Index of the animation.</span></span>

</dd> <dt>

<span data-ttu-id="fb6cd-110">*ppName* \[ vorgenommen\]</span><span class="sxs-lookup"><span data-stu-id="fb6cd-110">*ppName* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="fb6cd-111">Typ: **[ **LPCSTR**](../winprog/windows-data-types.md)\***</span><span class="sxs-lookup"><span data-stu-id="fb6cd-111">Type: **[**LPCSTR**](../winprog/windows-data-types.md)\***</span></span>

<span data-ttu-id="fb6cd-112">Adresse eines Zeigers auf eine Zeichenfolge, die den Animations Namen empfängt.</span><span class="sxs-lookup"><span data-stu-id="fb6cd-112">Address of a pointer to a string that receives the animation name.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="fb6cd-113">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="fb6cd-113">Return value</span></span>

<span data-ttu-id="fb6cd-114">Typ: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="fb6cd-114">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="fb6cd-115">Die Rückgabewerte dieser Methode werden von einem Anwendungsprogrammierer implementiert.</span><span class="sxs-lookup"><span data-stu-id="fb6cd-115">The return values of this method are implemented by an application programmer.</span></span> <span data-ttu-id="fb6cd-116">Wenn kein Fehler auftritt, programmieren Sie im Allgemeinen die-Methode, um D3D OK zurückzugeben \_ .</span><span class="sxs-lookup"><span data-stu-id="fb6cd-116">In general, if no error occurs, program the method to return D3D\_OK.</span></span> <span data-ttu-id="fb6cd-117">Andernfalls programmieren Sie die-Methode, um eine entsprechende Fehlermeldung von [D3DERR](d3derr.md) oder [**D3DXERR**](./d3dxerr.md)zurückzugeben.</span><span class="sxs-lookup"><span data-stu-id="fb6cd-117">Otherwise, program the method to return an appropriate error message from [D3DERR](d3derr.md) or [**D3DXERR**](./d3dxerr.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="fb6cd-118">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="fb6cd-118">Requirements</span></span>



| <span data-ttu-id="fb6cd-119">Anforderung</span><span class="sxs-lookup"><span data-stu-id="fb6cd-119">Requirement</span></span> | <span data-ttu-id="fb6cd-120">Wert</span><span class="sxs-lookup"><span data-stu-id="fb6cd-120">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="fb6cd-121">Header</span><span class="sxs-lookup"><span data-stu-id="fb6cd-121">Header</span></span><br/>  | <dl> <span data-ttu-id="fb6cd-122"><dt>D3dx9anim. h</dt></span><span class="sxs-lookup"><span data-stu-id="fb6cd-122"><dt>D3dx9anim.h</dt></span></span> </dl> |
| <span data-ttu-id="fb6cd-123">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="fb6cd-123">Library</span></span><br/> | <dl> <span data-ttu-id="fb6cd-124"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="fb6cd-124"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="fb6cd-125">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="fb6cd-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="fb6cd-126">ID3DXAnimationSet</span><span class="sxs-lookup"><span data-stu-id="fb6cd-126">ID3DXAnimationSet</span></span>](id3dxanimationset.md)
</dt> </dl>

 

 
