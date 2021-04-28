---
description: 'D3DXLoadMeshHierarchyFromXInMemory-Funktion: Lädt die erste Framehierarchie aus einer X-Datei.'
ms.assetid: 428e5cfb-d6a5-4a7f-b082-2d8898e65490
title: D3DXLoadMeshHierarchyFromXInMemory-Funktion (D3dx9anim.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXLoadMeshHierarchyFromXInMemory
api_type:
- LibDef
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 551810c839e619985d9a380197553f5fe4fc9be8
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2021
ms.locfileid: "108098208"
---
# <a name="d3dxloadmeshhierarchyfromxinmemory-function"></a><span data-ttu-id="1c1ce-103">D3DXLoadMeshHierarchyFromXInMemory-Funktion</span><span class="sxs-lookup"><span data-stu-id="1c1ce-103">D3DXLoadMeshHierarchyFromXInMemory function</span></span>

<span data-ttu-id="1c1ce-104">Lädt die erste Framehierarchie aus einer X-Datei.</span><span class="sxs-lookup"><span data-stu-id="1c1ce-104">Loads the first frame hierarchy from a .x file.</span></span>

## <a name="syntax"></a><span data-ttu-id="1c1ce-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="1c1ce-105">Syntax</span></span>


```C++
HRESULT D3DXLoadMeshHierarchyFromXInMemory(
  _In_  LPCVOID                   pMemory,
  _In_  DWORD                     SizeOfMemory,
  _In_  DWORD                     MeshOptions,
  _In_  LPDIRECT3DDEVICE9         pDevice,
  _In_  LPD3DXALLOCATEHIERARCHY   pAlloc,
  _In_  LPD3DXLOADUSERDATA        pUserDataLoader,
  _Out_ LPD3DXFRAME               *ppFrameHeirarchy,
  _Out_ LPD3DXANIMATIONCONTROLLER *ppAnimController
);
```



## <a name="parameters"></a><span data-ttu-id="1c1ce-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="1c1ce-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="1c1ce-107">*pMemory* \[ In\]</span><span class="sxs-lookup"><span data-stu-id="1c1ce-107">*pMemory* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="1c1ce-108">Typ: **[ **LPCVOID**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="1c1ce-108">Type: **[**LPCVOID**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="1c1ce-109">Zeiger auf einen Puffer, der die Gitternetzhierarchie enthält.</span><span class="sxs-lookup"><span data-stu-id="1c1ce-109">Pointer to a buffer that contains the mesh hierarchy.</span></span>

</dd> <dt>

<span data-ttu-id="1c1ce-110">*SizeOfMemory* \[ In\]</span><span class="sxs-lookup"><span data-stu-id="1c1ce-110">*SizeOfMemory* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="1c1ce-111">Typ: **[ **DWORD**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="1c1ce-111">Type: **[**DWORD**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="1c1ce-112">Größe des pMemory-Puffers in Bytes.</span><span class="sxs-lookup"><span data-stu-id="1c1ce-112">Size of the pMemory buffer, in bytes.</span></span>

</dd> <dt>

<span data-ttu-id="1c1ce-113">*MeshOptions* \[ In\]</span><span class="sxs-lookup"><span data-stu-id="1c1ce-113">*MeshOptions* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="1c1ce-114">Typ: **[ **DWORD**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="1c1ce-114">Type: **[**DWORD**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="1c1ce-115">Kombination von mindestens einem Flag aus der [**D3DXMESH-Enumeration,**](./d3dxmesh.md) die Erstellungsoptionen für das Gitternetz angeben.</span><span class="sxs-lookup"><span data-stu-id="1c1ce-115">Combination of one or more flags from the [**D3DXMESH**](./d3dxmesh.md) enumeration that specify creation options for the mesh.</span></span>

</dd> <dt>

<span data-ttu-id="1c1ce-116">*pDevice* \[ In\]</span><span class="sxs-lookup"><span data-stu-id="1c1ce-116">*pDevice* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="1c1ce-117">Typ: **[ **LPDIRECT3DDEVICE9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9)**</span><span class="sxs-lookup"><span data-stu-id="1c1ce-117">Type: **[**LPDIRECT3DDEVICE9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9)**</span></span>

<span data-ttu-id="1c1ce-118">Zeiger auf eine [**IDirect3DDevice9-Schnittstelle,**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9) das dem Gittermodell zugeordnete Geräteobjekt.</span><span class="sxs-lookup"><span data-stu-id="1c1ce-118">Pointer to an [**IDirect3DDevice9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9) interface, the device object associated with the mesh.</span></span>

</dd> <dt>

<span data-ttu-id="1c1ce-119">*pAlloc* \[ In\]</span><span class="sxs-lookup"><span data-stu-id="1c1ce-119">*pAlloc* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="1c1ce-120">Typ: **[ **LPD3DXALLOCATEHIERARCHY**](id3dxallocatehierarchy.md)**</span><span class="sxs-lookup"><span data-stu-id="1c1ce-120">Type: **[**LPD3DXALLOCATEHIERARCHY**](id3dxallocatehierarchy.md)**</span></span>

<span data-ttu-id="1c1ce-121">Zeiger auf eine [**ID3DXAllocateHierarchy-Schnittstelle.**](id3dxallocatehierarchy.md)</span><span class="sxs-lookup"><span data-stu-id="1c1ce-121">Pointer to an [**ID3DXAllocateHierarchy**](id3dxallocatehierarchy.md) interface.</span></span>

</dd> <dt>

<span data-ttu-id="1c1ce-122">*pUserDataLoader* \[ In\]</span><span class="sxs-lookup"><span data-stu-id="1c1ce-122">*pUserDataLoader* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="1c1ce-123">Typ: **[ **LPD3DXLOADUSERDATA**](id3dxloaduserdata.md)**</span><span class="sxs-lookup"><span data-stu-id="1c1ce-123">Type: **[**LPD3DXLOADUSERDATA**](id3dxloaduserdata.md)**</span></span>

<span data-ttu-id="1c1ce-124">Von der Anwendung bereitgestellte Schnittstelle, die das Laden von Benutzerdaten ermöglicht.</span><span class="sxs-lookup"><span data-stu-id="1c1ce-124">Application provided interface that allows loading of user data.</span></span> <span data-ttu-id="1c1ce-125">Siehe [**ID3DXLoadUserData.**](id3dxloaduserdata.md)</span><span class="sxs-lookup"><span data-stu-id="1c1ce-125">See [**ID3DXLoadUserData**](id3dxloaduserdata.md).</span></span>

</dd> <dt>

<span data-ttu-id="1c1ce-126">*ppFrameHeirarchy* \[ out\]</span><span class="sxs-lookup"><span data-stu-id="1c1ce-126">*ppFrameHeirarchy* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="1c1ce-127">Typ: **[ **LPD3DXFRAME**](d3dxframe.md)\***</span><span class="sxs-lookup"><span data-stu-id="1c1ce-127">Type: **[**LPD3DXFRAME**](d3dxframe.md)\***</span></span>

<span data-ttu-id="1c1ce-128">Gibt einen Zeiger auf die geladene Rahmenhierarchie zurück.</span><span class="sxs-lookup"><span data-stu-id="1c1ce-128">Returns a pointer to the loaded frame hierarchy.</span></span> <span data-ttu-id="1c1ce-129">Siehe [**D3DXFRAME**](d3dxframe.md).</span><span class="sxs-lookup"><span data-stu-id="1c1ce-129">See [**D3DXFRAME**](d3dxframe.md).</span></span>

</dd> <dt>

<span data-ttu-id="1c1ce-130">*ppAnimController* \[ out\]</span><span class="sxs-lookup"><span data-stu-id="1c1ce-130">*ppAnimController* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="1c1ce-131">Typ: **[ **LPD3DXANIMATIONCONTROLLER**](id3dxanimationcontroller.md)\***</span><span class="sxs-lookup"><span data-stu-id="1c1ce-131">Type: **[**LPD3DXANIMATIONCONTROLLER**](id3dxanimationcontroller.md)\***</span></span>

<span data-ttu-id="1c1ce-132">Gibt einen Zeiger auf den Animationscontroller zurück, der der Animation in der X-Datei entspricht.</span><span class="sxs-lookup"><span data-stu-id="1c1ce-132">Returns a pointer to the animation controller corresponding to animation in the .x file.</span></span> <span data-ttu-id="1c1ce-133">Dies wird mit Standardspuren und Ereignissen erstellt.</span><span class="sxs-lookup"><span data-stu-id="1c1ce-133">This is created with default tracks and events.</span></span> <span data-ttu-id="1c1ce-134">Siehe [**ID3DXAnimationController.**](id3dxanimationcontroller.md)</span><span class="sxs-lookup"><span data-stu-id="1c1ce-134">See [**ID3DXAnimationController**](id3dxanimationcontroller.md).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="1c1ce-135">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="1c1ce-135">Return value</span></span>

<span data-ttu-id="1c1ce-136">Typ: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="1c1ce-136">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="1c1ce-137">Wenn die Funktion erfolgreich ausgeführt wird, lautet der Rückgabewert D3D \_ OK.</span><span class="sxs-lookup"><span data-stu-id="1c1ce-137">If the function succeeds, the return value is D3D\_OK.</span></span> <span data-ttu-id="1c1ce-138">Wenn die Funktion fehlschlägt, kann der Rückgabewert einer der folgenden Werte sein: D3DERR \_ INVALIDCALL, E \_ OUTOFMEMORY.</span><span class="sxs-lookup"><span data-stu-id="1c1ce-138">If the function fails, the return value can be one of the following values: D3DERR\_INVALIDCALL, E\_OUTOFMEMORY.</span></span>

## <a name="remarks"></a><span data-ttu-id="1c1ce-139">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="1c1ce-139">Remarks</span></span>

<span data-ttu-id="1c1ce-140">Alle Gitternetze in der Datei werden in ein Ausgabegitternetz reduziert.</span><span class="sxs-lookup"><span data-stu-id="1c1ce-140">All the meshes in the file will be collapsed into one output mesh.</span></span> <span data-ttu-id="1c1ce-141">Wenn die Datei eine Rahmenhierarchie enthält, werden alle Transformationen auf das Gitternetz angewendet.</span><span class="sxs-lookup"><span data-stu-id="1c1ce-141">If the file contains a frame hierarchy, all the transformations will be applied to the mesh.</span></span>

## <a name="requirements"></a><span data-ttu-id="1c1ce-142">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="1c1ce-142">Requirements</span></span>



| <span data-ttu-id="1c1ce-143">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="1c1ce-143">Requirement</span></span> | <span data-ttu-id="1c1ce-144">Wert</span><span class="sxs-lookup"><span data-stu-id="1c1ce-144">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="1c1ce-145">Header</span><span class="sxs-lookup"><span data-stu-id="1c1ce-145">Header</span></span><br/>  | <dl> <span data-ttu-id="1c1ce-146"><dt>D3dx9anim.h</dt></span><span class="sxs-lookup"><span data-stu-id="1c1ce-146"><dt>D3dx9anim.h</dt></span></span> </dl> |
| <span data-ttu-id="1c1ce-147">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="1c1ce-147">Library</span></span><br/> | <dl> <span data-ttu-id="1c1ce-148"><dt>D3dx9.lib</dt></span><span class="sxs-lookup"><span data-stu-id="1c1ce-148"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="1c1ce-149">Weitere Informationen</span><span class="sxs-lookup"><span data-stu-id="1c1ce-149">See also</span></span>

<dl> <dt>

[<span data-ttu-id="1c1ce-150">Animationsfunktionen</span><span class="sxs-lookup"><span data-stu-id="1c1ce-150">Animation Functions</span></span>](dx9-graphics-reference-d3dx-functions-animation.md)
</dt> </dl>

 

 
