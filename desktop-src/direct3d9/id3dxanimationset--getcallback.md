---
description: 'ID3DXAnimationSet::GetCallback-Methode: Ruft Informationen zu einem bestimmten Rückruf im Animationssatz ab.'
ms.assetid: e8388bfc-5438-4216-a98f-dd0dbca12c87
title: ID3DXAnimationSet::GetCallback-Methode (D3dx9anim.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXAnimationSet.GetCallback
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 563c1007cc471ab10a9609e776da69b7c5ed493b
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2021
ms.locfileid: "108097538"
---
# <a name="id3dxanimationsetgetcallback-method"></a><span data-ttu-id="b1e05-103">ID3DXAnimationSet::GetCallback-Methode</span><span class="sxs-lookup"><span data-stu-id="b1e05-103">ID3DXAnimationSet::GetCallback method</span></span>

<span data-ttu-id="b1e05-104">Ruft Informationen zu einem bestimmten Rückruf im Animationssatz ab.</span><span class="sxs-lookup"><span data-stu-id="b1e05-104">Gets information about a specific callback in the animation set.</span></span>

## <a name="syntax"></a><span data-ttu-id="b1e05-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="b1e05-105">Syntax</span></span>


```C++
HRESULT GetCallback(
  [in]  DOUBLE Position,
  [in]  DWORD  Flags,
  [out] DOUBLE *pCallbackPosition,
  [out] LPVOID *ppCallbackData
);
```



## <a name="parameters"></a><span data-ttu-id="b1e05-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="b1e05-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="b1e05-107">*Position* \[ In\]</span><span class="sxs-lookup"><span data-stu-id="b1e05-107">*Position* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="b1e05-108">Typ: **[ **DOUBLE**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="b1e05-108">Type: **[**DOUBLE**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="b1e05-109">Position, an der Rückrufe zu finden sind.</span><span class="sxs-lookup"><span data-stu-id="b1e05-109">Position from which to find callbacks.</span></span>

</dd> <dt>

<span data-ttu-id="b1e05-110">*Flags* \[in\]</span><span class="sxs-lookup"><span data-stu-id="b1e05-110">*Flags* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="b1e05-111">Typ: **[ **DWORD**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="b1e05-111">Type: **[**DWORD**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="b1e05-112">Rückrufsuchflags.</span><span class="sxs-lookup"><span data-stu-id="b1e05-112">Callback search flags.</span></span> <span data-ttu-id="b1e05-113">Dieser Parameter kann auf eine Kombination aus mindestens einem Flag aus [**D3DXCALLBACK-SUCHFLAgs \_ \_ festgelegt werden.**](./d3dxcallback-search-flags.md)</span><span class="sxs-lookup"><span data-stu-id="b1e05-113">This parameter can be set to a combination of one or more flags from [**D3DXCALLBACK\_SEARCH\_FLAGS**](./d3dxcallback-search-flags.md).</span></span>

</dd> <dt>

<span data-ttu-id="b1e05-114">*pCallbackPosition* \[ out\]</span><span class="sxs-lookup"><span data-stu-id="b1e05-114">*pCallbackPosition* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="b1e05-115">Typ: **[ **DOUBLE**](../winprog/windows-data-types.md)\***</span><span class="sxs-lookup"><span data-stu-id="b1e05-115">Type: **[**DOUBLE**](../winprog/windows-data-types.md)\***</span></span>

<span data-ttu-id="b1e05-116">Zeiger auf die Position des Rückrufs.</span><span class="sxs-lookup"><span data-stu-id="b1e05-116">Pointer to the position of the callback.</span></span>

</dd> <dt>

<span data-ttu-id="b1e05-117">*ppCallbackData* \[ out\]</span><span class="sxs-lookup"><span data-stu-id="b1e05-117">*ppCallbackData* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="b1e05-118">Typ: **[ **LPVOID**](../winprog/windows-data-types.md)\***</span><span class="sxs-lookup"><span data-stu-id="b1e05-118">Type: **[**LPVOID**](../winprog/windows-data-types.md)\***</span></span>

<span data-ttu-id="b1e05-119">Adresse des Rückrufdatenzeigers.</span><span class="sxs-lookup"><span data-stu-id="b1e05-119">Address of the callback data pointer.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="b1e05-120">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="b1e05-120">Return value</span></span>

<span data-ttu-id="b1e05-121">Typ: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="b1e05-121">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="b1e05-122">Die Rückgabewerte dieser Methode werden von einem Anwendungsprogrammierer implementiert.</span><span class="sxs-lookup"><span data-stu-id="b1e05-122">The return values of this method are implemented by an application programmer.</span></span> <span data-ttu-id="b1e05-123">Wenn kein Fehler auftritt, programmieren Sie im Allgemeinen die -Methode so, dass D3D \_ OK zurückgegeben wird.</span><span class="sxs-lookup"><span data-stu-id="b1e05-123">In general, if no error occurs, program the method to return D3D\_OK.</span></span> <span data-ttu-id="b1e05-124">Programmieren Sie andernfalls die -Methode so, dass eine entsprechende Fehlermeldung von [D3DERR](d3derr.md) oder [**D3DXERR zurückgegeben wird.**](./d3dxerr.md)</span><span class="sxs-lookup"><span data-stu-id="b1e05-124">Otherwise, program the method to return an appropriate error message from [D3DERR](d3derr.md) or [**D3DXERR**](./d3dxerr.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="b1e05-125">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="b1e05-125">Requirements</span></span>



| <span data-ttu-id="b1e05-126">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="b1e05-126">Requirement</span></span> | <span data-ttu-id="b1e05-127">Wert</span><span class="sxs-lookup"><span data-stu-id="b1e05-127">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="b1e05-128">Header</span><span class="sxs-lookup"><span data-stu-id="b1e05-128">Header</span></span><br/>  | <dl> <span data-ttu-id="b1e05-129"><dt>D3dx9anim.h</dt></span><span class="sxs-lookup"><span data-stu-id="b1e05-129"><dt>D3dx9anim.h</dt></span></span> </dl> |
| <span data-ttu-id="b1e05-130">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="b1e05-130">Library</span></span><br/> | <dl> <span data-ttu-id="b1e05-131"><dt>D3dx9.lib</dt></span><span class="sxs-lookup"><span data-stu-id="b1e05-131"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="b1e05-132">Weitere Informationen</span><span class="sxs-lookup"><span data-stu-id="b1e05-132">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b1e05-133">ID3DXAnimationSet</span><span class="sxs-lookup"><span data-stu-id="b1e05-133">ID3DXAnimationSet</span></span>](id3dxanimationset.md)
</dt> </dl>

 

 
