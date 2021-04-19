---
description: Wendet das softwareskinning auf die Ziel Vertices basierend auf den aktuellen Matrizen an.
ms.assetid: 4858dfd4-dc0d-4852-9165-8ae1b40386d4
title: 'ID3DXSkinInfo:: updateskinnedmesh-Methode (D3DX9Mesh. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXSkinInfo.UpdateSkinnedMesh
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 645e6ae1e1cb84991b352c250b137cd3ae2491f0
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/15/2021
ms.locfileid: "106367340"
---
# <a name="id3dxskininfoupdateskinnedmesh-method"></a><span data-ttu-id="85603-103">ID3DXSkinInfo:: updateskinnedmesh-Methode</span><span class="sxs-lookup"><span data-stu-id="85603-103">ID3DXSkinInfo::UpdateSkinnedMesh method</span></span>

<span data-ttu-id="85603-104">Wendet das softwareskinning auf die Ziel Vertices basierend auf den aktuellen Matrizen an.</span><span class="sxs-lookup"><span data-stu-id="85603-104">Applies software skinning to the target vertices based on the current matrices.</span></span>

## <a name="syntax"></a><span data-ttu-id="85603-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="85603-105">Syntax</span></span>


```C++
HRESULT UpdateSkinnedMesh(
  [in] const D3DXMATRIX *pBoneTransforms,
  [in] const D3DXMATRIX *pBoneInvTransposeTransforms,
  [in]       LPCVOID    pVerticesSrc,
  [in]       PVOID      pVerticesDst
);
```



## <a name="parameters"></a><span data-ttu-id="85603-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="85603-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="85603-107">*pbonetransformationen* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="85603-107">*pBoneTransforms* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="85603-108">Typ: **Konstanten [**D3DXMATRIX**](d3dxmatrix.md) \***</span><span class="sxs-lookup"><span data-stu-id="85603-108">Type: **const [**D3DXMATRIX**](d3dxmatrix.md)\***</span></span>

<span data-ttu-id="85603-109">Matrix Transformationsmatrix.</span><span class="sxs-lookup"><span data-stu-id="85603-109">Bone transform matrix.</span></span>

</dd> <dt>

<span data-ttu-id="85603-110">*pboneinvtranspo/Transformationen* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="85603-110">*pBoneInvTransposeTransforms* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="85603-111">Typ: **Konstanten [**D3DXMATRIX**](d3dxmatrix.md) \***</span><span class="sxs-lookup"><span data-stu-id="85603-111">Type: **const [**D3DXMATRIX**](d3dxmatrix.md)\***</span></span>

<span data-ttu-id="85603-112">Umgekehrte Umwandlung der "Bone Transform"-Matrix.</span><span class="sxs-lookup"><span data-stu-id="85603-112">Inverse transpose of the bone transform matrix.</span></span>

</dd> <dt>

<span data-ttu-id="85603-113">*pverticessrc* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="85603-113">*pVerticesSrc* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="85603-114">Geben Sie Folgendes ein: **[ **lpcvoid**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="85603-114">Type: **[**LPCVOID**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="85603-115">Zeiger auf den Puffer, der die Quell Vertices enthält.</span><span class="sxs-lookup"><span data-stu-id="85603-115">Pointer to the buffer containing the source vertices.</span></span>

</dd> <dt>

<span data-ttu-id="85603-116">*pverticesdst* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="85603-116">*pVerticesDst* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="85603-117">Typ: **[ **pVoid**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="85603-117">Type: **[**PVOID**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="85603-118">Zeiger auf den Puffer, der die Ziel Vertices enthält.</span><span class="sxs-lookup"><span data-stu-id="85603-118">Pointer to the buffer containing the destination vertices.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="85603-119">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="85603-119">Return value</span></span>

<span data-ttu-id="85603-120">Typ: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="85603-120">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="85603-121">Wenn die Methode erfolgreich ausgeführt wird, ist der Rückgabewert D3D \_ OK.</span><span class="sxs-lookup"><span data-stu-id="85603-121">If the method succeeds, the return value is D3D\_OK.</span></span> <span data-ttu-id="85603-122">Wenn die Methode fehlschlägt, kann der Rückgabewert "D3DERR \_ invalidcall" lauten.</span><span class="sxs-lookup"><span data-stu-id="85603-122">If the method fails, the return value can be D3DERR\_INVALIDCALL.</span></span>

## <a name="remarks"></a><span data-ttu-id="85603-123">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="85603-123">Remarks</span></span>

<span data-ttu-id="85603-124">Wenn diese Methode verwendet wird, um Vertices mit zwei Positions Elementen zu verwenden, wird das zweite Positions Element mit der Umkehrung des knotes und nicht mit dem Knochen selbst gespaut.</span><span class="sxs-lookup"><span data-stu-id="85603-124">When used to skin vertices with two position elements, this method skins the second position element with the inverse of the bone instead of the bone itself.</span></span>

## <a name="requirements"></a><span data-ttu-id="85603-125">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="85603-125">Requirements</span></span>



| <span data-ttu-id="85603-126">Anforderung</span><span class="sxs-lookup"><span data-stu-id="85603-126">Requirement</span></span> | <span data-ttu-id="85603-127">Wert</span><span class="sxs-lookup"><span data-stu-id="85603-127">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="85603-128">Header</span><span class="sxs-lookup"><span data-stu-id="85603-128">Header</span></span><br/>  | <dl> <span data-ttu-id="85603-129"><dt>D3DX9Mesh. h</dt></span><span class="sxs-lookup"><span data-stu-id="85603-129"><dt>D3DX9Mesh.h</dt></span></span> </dl> |
| <span data-ttu-id="85603-130">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="85603-130">Library</span></span><br/> | <dl> <span data-ttu-id="85603-131"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="85603-131"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="85603-132">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="85603-132">See also</span></span>

<dl> <dt>

[<span data-ttu-id="85603-133">ID3DXSkinInfo</span><span class="sxs-lookup"><span data-stu-id="85603-133">ID3DXSkinInfo</span></span>](id3dxskininfo.md)
</dt> </dl>

 

 
