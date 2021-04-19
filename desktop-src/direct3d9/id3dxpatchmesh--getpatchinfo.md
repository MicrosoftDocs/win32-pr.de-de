---
description: Ruft die Attribute des Patches ab.
ms.assetid: 601a3275-25ea-4e16-8297-a9fc1f5fdd49
title: 'ID3DXPatchMesh:: getpatchinfo-Methode (D3DX9Mesh. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXPatchMesh.GetPatchInfo
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 70308857aa66551ed371dbe511acb6bd2d211bfb
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/15/2021
ms.locfileid: "106364371"
---
# <a name="id3dxpatchmeshgetpatchinfo-method"></a><span data-ttu-id="329fd-103">ID3DXPatchMesh:: getpatchinfo-Methode</span><span class="sxs-lookup"><span data-stu-id="329fd-103">ID3DXPatchMesh::GetPatchInfo method</span></span>

<span data-ttu-id="329fd-104">Ruft die Attribute des Patches ab.</span><span class="sxs-lookup"><span data-stu-id="329fd-104">Gets the attributes of the patch.</span></span>

## <a name="syntax"></a><span data-ttu-id="329fd-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="329fd-105">Syntax</span></span>


```C++
HRESULT GetPatchInfo(
  [out, retval] LPD3DXPATCHINFO PatchInfo
);
```



## <a name="parameters"></a><span data-ttu-id="329fd-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="329fd-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="329fd-107">*Patchinfo* \[ Out, retval\]</span><span class="sxs-lookup"><span data-stu-id="329fd-107">*PatchInfo* \[out, retval\]</span></span>
</dt> <dd>

<span data-ttu-id="329fd-108">Typ: **[ **LPD3DXPATCHINFO**](d3dxpatchinfo.md)**</span><span class="sxs-lookup"><span data-stu-id="329fd-108">Type: **[**LPD3DXPATCHINFO**](d3dxpatchinfo.md)**</span></span>

<span data-ttu-id="329fd-109">Ein Zeiger auf die Strukturen, die die Patchattribute enthalten.</span><span class="sxs-lookup"><span data-stu-id="329fd-109">Pointer to the structures containing the patch attributes.</span></span> <span data-ttu-id="329fd-110">Weitere Informationen zu Patch-Attributen finden Sie unter [**D3DXPATCHINFO**](d3dxpatchinfo.md).</span><span class="sxs-lookup"><span data-stu-id="329fd-110">For more information about patch attributes, see [**D3DXPATCHINFO**](d3dxpatchinfo.md).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="329fd-111">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="329fd-111">Return value</span></span>

<span data-ttu-id="329fd-112">Typ: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="329fd-112">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="329fd-113">Wenn die Methode erfolgreich ausgeführt wird, ist der Rückgabewert D3D \_ OK.</span><span class="sxs-lookup"><span data-stu-id="329fd-113">If the method succeeds, the return value is D3D\_OK.</span></span> <span data-ttu-id="329fd-114">Wenn die Methode fehlschlägt, kann der Rückgabewert einer der folgenden sein: D3DERR \_ invalidcall, E \_ outo fmemory.</span><span class="sxs-lookup"><span data-stu-id="329fd-114">If the method fails, the return value can be one of the following: D3DERR\_INVALIDCALL, E\_OUTOFMEMORY.</span></span>

## <a name="requirements"></a><span data-ttu-id="329fd-115">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="329fd-115">Requirements</span></span>



| <span data-ttu-id="329fd-116">Anforderung</span><span class="sxs-lookup"><span data-stu-id="329fd-116">Requirement</span></span> | <span data-ttu-id="329fd-117">Wert</span><span class="sxs-lookup"><span data-stu-id="329fd-117">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="329fd-118">Header</span><span class="sxs-lookup"><span data-stu-id="329fd-118">Header</span></span><br/>  | <dl> <span data-ttu-id="329fd-119"><dt>D3DX9Mesh. h</dt></span><span class="sxs-lookup"><span data-stu-id="329fd-119"><dt>D3DX9Mesh.h</dt></span></span> </dl> |
| <span data-ttu-id="329fd-120">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="329fd-120">Library</span></span><br/> | <dl> <span data-ttu-id="329fd-121"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="329fd-121"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="329fd-122">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="329fd-122">See also</span></span>

<dl> <dt>

[<span data-ttu-id="329fd-123">ID3DXPatchMesh</span><span class="sxs-lookup"><span data-stu-id="329fd-123">ID3DXPatchMesh</span></span>](id3dxpatchmesh.md)
</dt> </dl>

 

 




