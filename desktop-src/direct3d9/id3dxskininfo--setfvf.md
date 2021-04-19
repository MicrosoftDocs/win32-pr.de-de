---
description: Legt den Typ des flexiblen Vertex-Formats (FVF) fest.
ms.assetid: e581dcd4-7e17-4c36-aac9-c2942924cf51
title: 'ID3DXSkinInfo:: setf VF-Methode (D3DX9Mesh. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXSkinInfo.SetFVF
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 010385597442ba1546c20122f6551fca0cfcf81c
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/15/2021
ms.locfileid: "106370394"
---
# <a name="id3dxskininfosetfvf-method"></a><span data-ttu-id="dbe89-103">ID3DXSkinInfo:: setf VF-Methode</span><span class="sxs-lookup"><span data-stu-id="dbe89-103">ID3DXSkinInfo::SetFVF method</span></span>

<span data-ttu-id="dbe89-104">Legt den Typ des flexiblen Vertex-Formats (FVF) fest.</span><span class="sxs-lookup"><span data-stu-id="dbe89-104">Sets the flexible vertex format (FVF) type.</span></span>

## <a name="syntax"></a><span data-ttu-id="dbe89-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="dbe89-105">Syntax</span></span>


```C++
HRESULT SetFVF(
  [in] DWORD FVF
);
```



## <a name="parameters"></a><span data-ttu-id="dbe89-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="dbe89-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="dbe89-107">*F-VF* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="dbe89-107">*FVF* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="dbe89-108">Typ: **[ **DWORD**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="dbe89-108">Type: **[**DWORD**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="dbe89-109">Flexibles Vertex-Format.</span><span class="sxs-lookup"><span data-stu-id="dbe89-109">Flexible vertex format.</span></span> <span data-ttu-id="dbe89-110">Siehe [D3DFVF](d3dfvf.md).</span><span class="sxs-lookup"><span data-stu-id="dbe89-110">See [D3DFVF](d3dfvf.md).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="dbe89-111">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="dbe89-111">Return value</span></span>

<span data-ttu-id="dbe89-112">Typ: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="dbe89-112">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="dbe89-113">Wenn die Methode erfolgreich ausgeführt wird, ist der Rückgabewert D3D \_ OK.</span><span class="sxs-lookup"><span data-stu-id="dbe89-113">If the method succeeds, the return value is D3D\_OK.</span></span> <span data-ttu-id="dbe89-114">Wenn die Methode fehlschlägt, kann der Rückgabewert "D3DERR \_ invalidcall" lauten.</span><span class="sxs-lookup"><span data-stu-id="dbe89-114">If the method fails, the return value can be D3DERR\_INVALIDCALL.</span></span>

## <a name="requirements"></a><span data-ttu-id="dbe89-115">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="dbe89-115">Requirements</span></span>



| <span data-ttu-id="dbe89-116">Anforderung</span><span class="sxs-lookup"><span data-stu-id="dbe89-116">Requirement</span></span> | <span data-ttu-id="dbe89-117">Wert</span><span class="sxs-lookup"><span data-stu-id="dbe89-117">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="dbe89-118">Header</span><span class="sxs-lookup"><span data-stu-id="dbe89-118">Header</span></span><br/>  | <dl> <span data-ttu-id="dbe89-119"><dt>D3DX9Mesh. h</dt></span><span class="sxs-lookup"><span data-stu-id="dbe89-119"><dt>D3DX9Mesh.h</dt></span></span> </dl> |
| <span data-ttu-id="dbe89-120">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="dbe89-120">Library</span></span><br/> | <dl> <span data-ttu-id="dbe89-121"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="dbe89-121"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="dbe89-122">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="dbe89-122">See also</span></span>

<dl> <dt>

[<span data-ttu-id="dbe89-123">ID3DXSkinInfo</span><span class="sxs-lookup"><span data-stu-id="dbe89-123">ID3DXSkinInfo</span></span>](id3dxskininfo.md)
</dt> </dl>

 

 
