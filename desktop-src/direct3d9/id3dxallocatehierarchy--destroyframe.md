---
description: Fordert die Aufhebung der Zuordnung eines Frame Objekts an.
ms.assetid: b2793744-1bba-4a2b-938c-44ed316358fd
title: ID3DXAllocateHierarchy::D estroyframe-Methode (D3dx9anim. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXAllocateHierarchy.DestroyFrame
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 4a394501b9967d3f7cb6d3f6b2f30db168438278
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/15/2021
ms.locfileid: "104394242"
---
# <a name="id3dxallocatehierarchydestroyframe-method"></a><span data-ttu-id="14c90-103">ID3DXAllocateHierarchy::D estroyframe-Methode</span><span class="sxs-lookup"><span data-stu-id="14c90-103">ID3DXAllocateHierarchy::DestroyFrame method</span></span>

<span data-ttu-id="14c90-104">Fordert die Aufhebung der Zuordnung eines Frame Objekts an.</span><span class="sxs-lookup"><span data-stu-id="14c90-104">Requests deallocation of a frame object.</span></span>

## <a name="syntax"></a><span data-ttu-id="14c90-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="14c90-105">Syntax</span></span>


```C++
HRESULT DestroyFrame(
  [in] LPD3DXFRAME pFrameToFree
);
```



## <a name="parameters"></a><span data-ttu-id="14c90-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="14c90-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="14c90-107">*pFrame$ Free* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="14c90-107">*pFrameToFree* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="14c90-108">Typ: **[ **LPD3DXFRAME**](d3dxframe.md)**</span><span class="sxs-lookup"><span data-stu-id="14c90-108">Type: **[**LPD3DXFRAME**](d3dxframe.md)**</span></span>

<span data-ttu-id="14c90-109">Zeiger auf den Frame, dessen Zuordnung aufgehoben werden soll.</span><span class="sxs-lookup"><span data-stu-id="14c90-109">Pointer to the frame to be deallocated.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="14c90-110">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="14c90-110">Return value</span></span>

<span data-ttu-id="14c90-111">Typ: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="14c90-111">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="14c90-112">Die Rückgabewerte dieser Methode werden von einem Anwendungsprogrammierer implementiert.</span><span class="sxs-lookup"><span data-stu-id="14c90-112">The return values of this method are implemented by an application programmer.</span></span> <span data-ttu-id="14c90-113">Wenn kein Fehler auftritt, programmieren Sie im Allgemeinen die-Methode, um D3D OK zurückzugeben \_ .</span><span class="sxs-lookup"><span data-stu-id="14c90-113">In general, if no error occurs, program the method to return D3D\_OK.</span></span> <span data-ttu-id="14c90-114">Andernfalls programmieren Sie die Methode, um eine entsprechende Fehlermeldung von D3DERR oder D3DXERR zurückzugeben, da dies dazu führt, dass [**D3DXLoadMeshHierarchyFromX**](d3dxloadmeshhierarchyfromx.md) ebenfalls fehlschlägt, und gibt den Fehler zurück.</span><span class="sxs-lookup"><span data-stu-id="14c90-114">Otherwise, program the method to return an appropriate error message from D3DERR or D3DXERR, as this will cause [**D3DXLoadMeshHierarchyFromX**](d3dxloadmeshhierarchyfromx.md) to fail also, and return the error.</span></span>

## <a name="requirements"></a><span data-ttu-id="14c90-115">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="14c90-115">Requirements</span></span>



| <span data-ttu-id="14c90-116">Anforderung</span><span class="sxs-lookup"><span data-stu-id="14c90-116">Requirement</span></span> | <span data-ttu-id="14c90-117">Wert</span><span class="sxs-lookup"><span data-stu-id="14c90-117">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="14c90-118">Header</span><span class="sxs-lookup"><span data-stu-id="14c90-118">Header</span></span><br/>  | <dl> <span data-ttu-id="14c90-119"><dt>D3dx9anim. h</dt></span><span class="sxs-lookup"><span data-stu-id="14c90-119"><dt>D3dx9anim.h</dt></span></span> </dl> |
| <span data-ttu-id="14c90-120">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="14c90-120">Library</span></span><br/> | <dl> <span data-ttu-id="14c90-121"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="14c90-121"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="14c90-122">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="14c90-122">See also</span></span>

<dl> <dt>

[<span data-ttu-id="14c90-123">ID3DXAllocateHierarchy</span><span class="sxs-lookup"><span data-stu-id="14c90-123">ID3DXAllocateHierarchy</span></span>](id3dxallocatehierarchy.md)
</dt> </dl>

 

 




