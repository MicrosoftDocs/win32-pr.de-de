---
description: Fordert die Aufhebung der Zuordnung eines Mesh-Container Objekts an.
ms.assetid: 7a976ba8-6972-4857-b0a9-4ea7a88dc8ac
title: ID3DXAllocateHierarchy::D estroymeshcontainer-Methode (D3dx9anim. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXAllocateHierarchy.DestroyMeshContainer
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 6114c78cefd7415fb11fc30587fa2dc628fb4466
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/15/2021
ms.locfileid: "104531070"
---
# <a name="id3dxallocatehierarchydestroymeshcontainer-method"></a><span data-ttu-id="e089b-103">ID3DXAllocateHierarchy::D estroymeshcontainer-Methode</span><span class="sxs-lookup"><span data-stu-id="e089b-103">ID3DXAllocateHierarchy::DestroyMeshContainer method</span></span>

<span data-ttu-id="e089b-104">Fordert die Aufhebung der Zuordnung eines Mesh-Container Objekts an.</span><span class="sxs-lookup"><span data-stu-id="e089b-104">Requests deallocation of a mesh container object.</span></span>

## <a name="syntax"></a><span data-ttu-id="e089b-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="e089b-105">Syntax</span></span>


```C++
HRESULT DestroyMeshContainer(
  [in] LPD3DXMESHCONTAINER pMeshContainerToFree
);
```



## <a name="parameters"></a><span data-ttu-id="e089b-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="e089b-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="e089b-107">*pmeshcontainerautofree* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="e089b-107">*pMeshContainerToFree* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="e089b-108">Typ: **[ **LPD3DXMESHCONTAINER**](d3dxmeshcontainer.md)**</span><span class="sxs-lookup"><span data-stu-id="e089b-108">Type: **[**LPD3DXMESHCONTAINER**](d3dxmeshcontainer.md)**</span></span>

<span data-ttu-id="e089b-109">Zeiger auf das Mesh-Container Objekt, dessen Zuordnung aufgehoben werden soll.</span><span class="sxs-lookup"><span data-stu-id="e089b-109">Pointer to the mesh container object to be deallocated.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="e089b-110">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="e089b-110">Return value</span></span>

<span data-ttu-id="e089b-111">Typ: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="e089b-111">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="e089b-112">Die Rückgabewerte dieser Methode werden von einem Anwendungsprogrammierer implementiert.</span><span class="sxs-lookup"><span data-stu-id="e089b-112">The return values of this method are implemented by an application programmer.</span></span> <span data-ttu-id="e089b-113">Wenn kein Fehler auftritt, programmieren Sie im Allgemeinen die-Methode, um D3D OK zurückzugeben \_ .</span><span class="sxs-lookup"><span data-stu-id="e089b-113">In general, if no error occurs, program the method to return D3D\_OK.</span></span> <span data-ttu-id="e089b-114">Andernfalls programmieren Sie die Methode, um eine entsprechende Fehlermeldung von D3DERR oder D3DXERR zurückzugeben, da dies dazu führt, dass [**D3DXLoadMeshHierarchyFromX**](d3dxloadmeshhierarchyfromx.md) ebenfalls fehlschlägt, und gibt den Fehler zurück.</span><span class="sxs-lookup"><span data-stu-id="e089b-114">Otherwise, program the method to return an appropriate error message from D3DERR or D3DXERR, as this will cause [**D3DXLoadMeshHierarchyFromX**](d3dxloadmeshhierarchyfromx.md) to fail also, and return the error.</span></span>

## <a name="requirements"></a><span data-ttu-id="e089b-115">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="e089b-115">Requirements</span></span>



| <span data-ttu-id="e089b-116">Anforderung</span><span class="sxs-lookup"><span data-stu-id="e089b-116">Requirement</span></span> | <span data-ttu-id="e089b-117">Wert</span><span class="sxs-lookup"><span data-stu-id="e089b-117">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="e089b-118">Header</span><span class="sxs-lookup"><span data-stu-id="e089b-118">Header</span></span><br/>  | <dl> <span data-ttu-id="e089b-119"><dt>D3dx9anim. h</dt></span><span class="sxs-lookup"><span data-stu-id="e089b-119"><dt>D3dx9anim.h</dt></span></span> </dl> |
| <span data-ttu-id="e089b-120">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="e089b-120">Library</span></span><br/> | <dl> <span data-ttu-id="e089b-121"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="e089b-121"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="e089b-122">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="e089b-122">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e089b-123">ID3DXAllocateHierarchy</span><span class="sxs-lookup"><span data-stu-id="e089b-123">ID3DXAllocateHierarchy</span></span>](id3dxallocatehierarchy.md)
</dt> </dl>

 

 




