---
description: Fordert die Zuordnung eines Frame Objekts an.
ms.assetid: 977e40d6-bf49-44b6-ac95-88e7f778ea50
title: 'ID3DXAllocateHierarchy:: kreateframe-Methode (D3dx9anim. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXAllocateHierarchy.CreateFrame
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: d6a3a13dd4d3b3dfaffb26632ff6ad5cc8666f86
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/15/2021
ms.locfileid: "106371932"
---
# <a name="id3dxallocatehierarchycreateframe-method"></a><span data-ttu-id="906e2-103">ID3DXAllocateHierarchy:: kreateframe-Methode</span><span class="sxs-lookup"><span data-stu-id="906e2-103">ID3DXAllocateHierarchy::CreateFrame method</span></span>

<span data-ttu-id="906e2-104">Fordert die Zuordnung eines Frame Objekts an.</span><span class="sxs-lookup"><span data-stu-id="906e2-104">Requests allocation of a frame object.</span></span>

## <a name="syntax"></a><span data-ttu-id="906e2-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="906e2-105">Syntax</span></span>


```C++
HRESULT CreateFrame(
  [in]          LPCSTR      Name,
  [out, retval] LPD3DXFRAME *ppNewFrame
);
```



## <a name="parameters"></a><span data-ttu-id="906e2-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="906e2-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="906e2-107">*Name* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="906e2-107">*Name* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="906e2-108">Typ: **[ **LPCSTR**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="906e2-108">Type: **[**LPCSTR**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="906e2-109">Der Name des Frames, der erstellt werden soll.</span><span class="sxs-lookup"><span data-stu-id="906e2-109">Name of the frame to be created.</span></span>

</dd> <dt>

<span data-ttu-id="906e2-110">*ppnewframe* \[ Out, retval\]</span><span class="sxs-lookup"><span data-stu-id="906e2-110">*ppNewFrame* \[out, retval\]</span></span>
</dt> <dd>

<span data-ttu-id="906e2-111">Typ: **[ **LPD3DXFRAME**](d3dxframe.md)\***</span><span class="sxs-lookup"><span data-stu-id="906e2-111">Type: **[**LPD3DXFRAME**](d3dxframe.md)\***</span></span>

<span data-ttu-id="906e2-112">Gibt das erstellte Frame Objekt zurück.</span><span class="sxs-lookup"><span data-stu-id="906e2-112">Returns the created frame object.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="906e2-113">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="906e2-113">Return value</span></span>

<span data-ttu-id="906e2-114">Typ: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="906e2-114">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="906e2-115">Die Rückgabewerte dieser Methode werden von einem Anwendungsprogrammierer implementiert.</span><span class="sxs-lookup"><span data-stu-id="906e2-115">The return values of this method are implemented by an application programmer.</span></span> <span data-ttu-id="906e2-116">Wenn kein Fehler auftritt, programmieren Sie im Allgemeinen die-Methode, um D3D OK zurückzugeben \_ .</span><span class="sxs-lookup"><span data-stu-id="906e2-116">In general, if no error occurs, program the method to return D3D\_OK.</span></span> <span data-ttu-id="906e2-117">Andernfalls programmieren Sie die Methode, um eine entsprechende Fehlermeldung von D3DERR oder D3DXERR zurückzugeben, da dies dazu führt, dass [**D3DXLoadMeshHierarchyFromX**](d3dxloadmeshhierarchyfromx.md) ebenfalls fehlschlägt, und gibt den Fehler zurück.</span><span class="sxs-lookup"><span data-stu-id="906e2-117">Otherwise, program the method to return an appropriate error message from D3DERR or D3DXERR, as this will cause [**D3DXLoadMeshHierarchyFromX**](d3dxloadmeshhierarchyfromx.md) to fail also, and return the error.</span></span>

## <a name="requirements"></a><span data-ttu-id="906e2-118">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="906e2-118">Requirements</span></span>



| <span data-ttu-id="906e2-119">Anforderung</span><span class="sxs-lookup"><span data-stu-id="906e2-119">Requirement</span></span> | <span data-ttu-id="906e2-120">Wert</span><span class="sxs-lookup"><span data-stu-id="906e2-120">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="906e2-121">Header</span><span class="sxs-lookup"><span data-stu-id="906e2-121">Header</span></span><br/>  | <dl> <span data-ttu-id="906e2-122"><dt>D3dx9anim. h</dt></span><span class="sxs-lookup"><span data-stu-id="906e2-122"><dt>D3dx9anim.h</dt></span></span> </dl> |
| <span data-ttu-id="906e2-123">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="906e2-123">Library</span></span><br/> | <dl> <span data-ttu-id="906e2-124"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="906e2-124"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="906e2-125">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="906e2-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="906e2-126">ID3DXAllocateHierarchy</span><span class="sxs-lookup"><span data-stu-id="906e2-126">ID3DXAllocateHierarchy</span></span>](id3dxallocatehierarchy.md)
</dt> </dl>

 

 
