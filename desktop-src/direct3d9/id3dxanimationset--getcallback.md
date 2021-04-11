---
description: Ruft Informationen zu einem bestimmten Rückruf im Animations Satz ab.
ms.assetid: e8388bfc-5438-4216-a98f-dd0dbca12c87
title: 'ID3DXAnimationSet:: getCallback-Methode (D3dx9anim. h)'
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
ms.openlocfilehash: f4cde6c9d51fd29c0412f33b34ca7bea8260dfea
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/15/2021
ms.locfileid: "104219699"
---
# <a name="id3dxanimationsetgetcallback-method"></a><span data-ttu-id="bc099-103">ID3DXAnimationSet:: getCallback-Methode</span><span class="sxs-lookup"><span data-stu-id="bc099-103">ID3DXAnimationSet::GetCallback method</span></span>

<span data-ttu-id="bc099-104">Ruft Informationen zu einem bestimmten Rückruf im Animations Satz ab.</span><span class="sxs-lookup"><span data-stu-id="bc099-104">Gets information about a specific callback in the animation set.</span></span>

## <a name="syntax"></a><span data-ttu-id="bc099-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="bc099-105">Syntax</span></span>


```C++
HRESULT GetCallback(
  [in]  DOUBLE Position,
  [in]  DWORD  Flags,
  [out] DOUBLE *pCallbackPosition,
  [out] LPVOID *ppCallbackData
);
```



## <a name="parameters"></a><span data-ttu-id="bc099-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="bc099-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="bc099-107">*Position* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="bc099-107">*Position* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="bc099-108">Typ: **[ **Double**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="bc099-108">Type: **[**DOUBLE**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="bc099-109">Die Position, an der Rückrufe gesucht werden sollen.</span><span class="sxs-lookup"><span data-stu-id="bc099-109">Position from which to find callbacks.</span></span>

</dd> <dt>

<span data-ttu-id="bc099-110">*Flags* \[in\]</span><span class="sxs-lookup"><span data-stu-id="bc099-110">*Flags* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="bc099-111">Typ: **[ **DWORD**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="bc099-111">Type: **[**DWORD**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="bc099-112">Rückruf Suchflags.</span><span class="sxs-lookup"><span data-stu-id="bc099-112">Callback search flags.</span></span> <span data-ttu-id="bc099-113">Dieser Parameter kann auf eine Kombination aus einem oder mehreren Flags aus [**D3DXCALLBACK- \_ \_ Suchflags**](./d3dxcallback-search-flags.md)festgelegt werden.</span><span class="sxs-lookup"><span data-stu-id="bc099-113">This parameter can be set to a combination of one or more flags from [**D3DXCALLBACK\_SEARCH\_FLAGS**](./d3dxcallback-search-flags.md).</span></span>

</dd> <dt>

<span data-ttu-id="bc099-114">*pcallbackposition* \[ vorgenommen\]</span><span class="sxs-lookup"><span data-stu-id="bc099-114">*pCallbackPosition* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="bc099-115">Typ: **[ **Double**](../winprog/windows-data-types.md)\***</span><span class="sxs-lookup"><span data-stu-id="bc099-115">Type: **[**DOUBLE**](../winprog/windows-data-types.md)\***</span></span>

<span data-ttu-id="bc099-116">Ein Zeiger auf die Position des Rückrufs.</span><span class="sxs-lookup"><span data-stu-id="bc099-116">Pointer to the position of the callback.</span></span>

</dd> <dt>

<span data-ttu-id="bc099-117">*ppcallbackdata* \[ vorgenommen\]</span><span class="sxs-lookup"><span data-stu-id="bc099-117">*ppCallbackData* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="bc099-118">Typ: **[ **LPVOID**](../winprog/windows-data-types.md)\***</span><span class="sxs-lookup"><span data-stu-id="bc099-118">Type: **[**LPVOID**](../winprog/windows-data-types.md)\***</span></span>

<span data-ttu-id="bc099-119">Adresse des Rückruf Daten Zeigers.</span><span class="sxs-lookup"><span data-stu-id="bc099-119">Address of the callback data pointer.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="bc099-120">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="bc099-120">Return value</span></span>

<span data-ttu-id="bc099-121">Typ: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="bc099-121">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="bc099-122">Die Rückgabewerte dieser Methode werden von einem Anwendungsprogrammierer implementiert.</span><span class="sxs-lookup"><span data-stu-id="bc099-122">The return values of this method are implemented by an application programmer.</span></span> <span data-ttu-id="bc099-123">Wenn kein Fehler auftritt, programmieren Sie im Allgemeinen die-Methode, um D3D OK zurückzugeben \_ .</span><span class="sxs-lookup"><span data-stu-id="bc099-123">In general, if no error occurs, program the method to return D3D\_OK.</span></span> <span data-ttu-id="bc099-124">Andernfalls programmieren Sie die-Methode, um eine entsprechende Fehlermeldung von [D3DERR](d3derr.md) oder [**D3DXERR**](./d3dxerr.md)zurückzugeben.</span><span class="sxs-lookup"><span data-stu-id="bc099-124">Otherwise, program the method to return an appropriate error message from [D3DERR](d3derr.md) or [**D3DXERR**](./d3dxerr.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="bc099-125">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="bc099-125">Requirements</span></span>



| <span data-ttu-id="bc099-126">Anforderung</span><span class="sxs-lookup"><span data-stu-id="bc099-126">Requirement</span></span> | <span data-ttu-id="bc099-127">Wert</span><span class="sxs-lookup"><span data-stu-id="bc099-127">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="bc099-128">Header</span><span class="sxs-lookup"><span data-stu-id="bc099-128">Header</span></span><br/>  | <dl> <span data-ttu-id="bc099-129"><dt>D3dx9anim. h</dt></span><span class="sxs-lookup"><span data-stu-id="bc099-129"><dt>D3dx9anim.h</dt></span></span> </dl> |
| <span data-ttu-id="bc099-130">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="bc099-130">Library</span></span><br/> | <dl> <span data-ttu-id="bc099-131"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="bc099-131"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="bc099-132">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="bc099-132">See also</span></span>

<dl> <dt>

[<span data-ttu-id="bc099-133">ID3DXAnimationSet</span><span class="sxs-lookup"><span data-stu-id="bc099-133">ID3DXAnimationSet</span></span>](id3dxanimationset.md)
</dt> </dl>

 

 
