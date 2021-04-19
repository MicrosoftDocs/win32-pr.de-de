---
description: Fordert die Zuordnung eines Mesh-Container Objekts an.
ms.assetid: ec66b393-016b-4572-94dc-5c8903b506a3
title: 'ID3DXAllocateHierarchy:: samatemeshcontainer-Methode (D3dx9anim. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXAllocateHierarchy.CreateMeshContainer
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 0351290b8dee260d52362702d520b01e1bcb7af3
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/15/2021
ms.locfileid: "106364345"
---
# <a name="id3dxallocatehierarchycreatemeshcontainer-method"></a><span data-ttu-id="c7cca-103">ID3DXAllocateHierarchy:: samatemeshcontainer-Methode</span><span class="sxs-lookup"><span data-stu-id="c7cca-103">ID3DXAllocateHierarchy::CreateMeshContainer method</span></span>

<span data-ttu-id="c7cca-104">Fordert die Zuordnung eines Mesh-Container Objekts an.</span><span class="sxs-lookup"><span data-stu-id="c7cca-104">Requests allocation of a mesh container object.</span></span>

## <a name="syntax"></a><span data-ttu-id="c7cca-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="c7cca-105">Syntax</span></span>


```C++
HRESULT CreateMeshContainer(
  [in]                LPCSTR              Name,
  [in]          const D3DXMESHDATA        *pMeshData,
  [in]          const D3DXMATERIAL        *pMaterials,
  [in]          const D3DXEFFECTINSTANCE  *pEffectInstances,
  [in]                DWORD               NumMaterials,
  [in]          const DWORD               *pAdjacency,
  [in]                LPD3DXSKININFO      pSkinInfo,
  [out, retval]       LPD3DXMESHCONTAINER *ppNewMeshContainer
);
```



## <a name="parameters"></a><span data-ttu-id="c7cca-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="c7cca-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="c7cca-107">*Name* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="c7cca-107">*Name* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="c7cca-108">Typ: **[ **LPCSTR**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="c7cca-108">Type: **[**LPCSTR**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="c7cca-109">Der Name des Netzes.</span><span class="sxs-lookup"><span data-stu-id="c7cca-109">Name of the mesh.</span></span>

</dd> <dt>

<span data-ttu-id="c7cca-110">*pmeshdata* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="c7cca-110">*pMeshData* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="c7cca-111">Typ: **Konstanten [**D3DXMESHDATA**](d3dxmeshdata.md) \***</span><span class="sxs-lookup"><span data-stu-id="c7cca-111">Type: **const [**D3DXMESHDATA**](d3dxmeshdata.md)\***</span></span>

<span data-ttu-id="c7cca-112">Zeiger auf die Mesh-Datenstruktur.</span><span class="sxs-lookup"><span data-stu-id="c7cca-112">Pointer to the mesh data structure.</span></span> <span data-ttu-id="c7cca-113">Siehe [**D3DXMESHDATA**](d3dxmeshdata.md).</span><span class="sxs-lookup"><span data-stu-id="c7cca-113">See [**D3DXMESHDATA**](d3dxmeshdata.md).</span></span>

</dd> <dt>

<span data-ttu-id="c7cca-114">*pmaterials* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="c7cca-114">*pMaterials* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="c7cca-115">Typ: **Konstanten [**D3DXMATERIAL**](d3dxmaterial.md) \***</span><span class="sxs-lookup"><span data-stu-id="c7cca-115">Type: **const [**D3DXMATERIAL**](d3dxmaterial.md)\***</span></span>

<span data-ttu-id="c7cca-116">Ein Array von Material, das im Mesh verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="c7cca-116">Array of materials used in the mesh.</span></span>

</dd> <dt>

<span data-ttu-id="c7cca-117">" *Peer-ectinhaltungen* \[ " in\]</span><span class="sxs-lookup"><span data-stu-id="c7cca-117">*pEffectInstances* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="c7cca-118">Typ: **Konstanten [**D3DXEFFECTINSTANCE**](d3dxeffectinstance.md) \***</span><span class="sxs-lookup"><span data-stu-id="c7cca-118">Type: **const [**D3DXEFFECTINSTANCE**](d3dxeffectinstance.md)\***</span></span>

<span data-ttu-id="c7cca-119">Array von Effekt Instanzen, die im Mesh verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="c7cca-119">Array of effect instances used in the mesh.</span></span> <span data-ttu-id="c7cca-120">Siehe [**D3DXEFFECTINSTANCE**](d3dxeffectinstance.md).</span><span class="sxs-lookup"><span data-stu-id="c7cca-120">See [**D3DXEFFECTINSTANCE**](d3dxeffectinstance.md).</span></span>

</dd> <dt>

<span data-ttu-id="c7cca-121">*Nummaterial* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="c7cca-121">*NumMaterials* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="c7cca-122">Typ: **[ **DWORD**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="c7cca-122">Type: **[**DWORD**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="c7cca-123">Anzahl der Materialien im Material Array.</span><span class="sxs-lookup"><span data-stu-id="c7cca-123">Number of materials in the materials array.</span></span>

</dd> <dt>

<span data-ttu-id="c7cca-124">*padjacency* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="c7cca-124">*pAdjacency* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="c7cca-125">Typ: Konstante **[**DWORD**](../winprog/windows-data-types.md) \***</span><span class="sxs-lookup"><span data-stu-id="c7cca-125">Type: **const [**DWORD**](../winprog/windows-data-types.md)\***</span></span>

<span data-ttu-id="c7cca-126">Das Array für das Mesh.</span><span class="sxs-lookup"><span data-stu-id="c7cca-126">Adjacency array for the mesh.</span></span>

</dd> <dt>

<span data-ttu-id="c7cca-127">*pskininfo* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="c7cca-127">*pSkinInfo* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="c7cca-128">Typ: **[ **LPD3DXSKININFO**](id3dxskininfo.md)**</span><span class="sxs-lookup"><span data-stu-id="c7cca-128">Type: **[**LPD3DXSKININFO**](id3dxskininfo.md)**</span></span>

<span data-ttu-id="c7cca-129">Zeiger auf das Skin-Mesh-Objekt, wenn Skin-Daten gefunden werden.</span><span class="sxs-lookup"><span data-stu-id="c7cca-129">Pointer to the skin mesh object if skin data is found.</span></span> <span data-ttu-id="c7cca-130">Siehe [**ID3DXSkinInfo**](id3dxskininfo.md).</span><span class="sxs-lookup"><span data-stu-id="c7cca-130">See [**ID3DXSkinInfo**](id3dxskininfo.md).</span></span>

</dd> <dt>

<span data-ttu-id="c7cca-131">*ppnewmeshcontainer* \[ Out, retval\]</span><span class="sxs-lookup"><span data-stu-id="c7cca-131">*ppNewMeshContainer* \[out, retval\]</span></span>
</dt> <dd>

<span data-ttu-id="c7cca-132">Typ: **[ **LPD3DXMESHCONTAINER**](d3dxmeshcontainer.md)\***</span><span class="sxs-lookup"><span data-stu-id="c7cca-132">Type: **[**LPD3DXMESHCONTAINER**](d3dxmeshcontainer.md)\***</span></span>

<span data-ttu-id="c7cca-133">Gibt den erstellten Mesh-Container zurück.</span><span class="sxs-lookup"><span data-stu-id="c7cca-133">Returns the created mesh container.</span></span> <span data-ttu-id="c7cca-134">Siehe [**D3DXMESHCONTAINER**](d3dxmeshcontainer.md).</span><span class="sxs-lookup"><span data-stu-id="c7cca-134">See [**D3DXMESHCONTAINER**](d3dxmeshcontainer.md).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="c7cca-135">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="c7cca-135">Return value</span></span>

<span data-ttu-id="c7cca-136">Typ: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="c7cca-136">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="c7cca-137">Die Rückgabewerte dieser Methode werden von einem Anwendungsprogrammierer implementiert.</span><span class="sxs-lookup"><span data-stu-id="c7cca-137">The return values of this method are implemented by an application programmer.</span></span> <span data-ttu-id="c7cca-138">Wenn kein Fehler auftritt, programmieren Sie im Allgemeinen die-Methode, um D3D OK zurückzugeben \_ .</span><span class="sxs-lookup"><span data-stu-id="c7cca-138">In general, if no error occurs, program the method to return D3D\_OK.</span></span> <span data-ttu-id="c7cca-139">Andernfalls programmieren Sie die Methode, um eine entsprechende Fehlermeldung von D3DERR oder D3DXERR zurückzugeben, da dies dazu führt, dass [**D3DXLoadMeshHierarchyFromX**](d3dxloadmeshhierarchyfromx.md) ebenfalls fehlschlägt, und gibt den Fehler zurück.</span><span class="sxs-lookup"><span data-stu-id="c7cca-139">Otherwise, program the method to return an appropriate error message from D3DERR or D3DXERR, as this will cause [**D3DXLoadMeshHierarchyFromX**](d3dxloadmeshhierarchyfromx.md) to fail also, and return the error.</span></span>

## <a name="requirements"></a><span data-ttu-id="c7cca-140">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="c7cca-140">Requirements</span></span>



| <span data-ttu-id="c7cca-141">Anforderung</span><span class="sxs-lookup"><span data-stu-id="c7cca-141">Requirement</span></span> | <span data-ttu-id="c7cca-142">Wert</span><span class="sxs-lookup"><span data-stu-id="c7cca-142">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="c7cca-143">Header</span><span class="sxs-lookup"><span data-stu-id="c7cca-143">Header</span></span><br/>  | <dl> <span data-ttu-id="c7cca-144"><dt>D3dx9anim. h</dt></span><span class="sxs-lookup"><span data-stu-id="c7cca-144"><dt>D3dx9anim.h</dt></span></span> </dl> |
| <span data-ttu-id="c7cca-145">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="c7cca-145">Library</span></span><br/> | <dl> <span data-ttu-id="c7cca-146"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="c7cca-146"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="c7cca-147">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="c7cca-147">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c7cca-148">ID3DXAllocateHierarchy</span><span class="sxs-lookup"><span data-stu-id="c7cca-148">ID3DXAllocateHierarchy</span></span>](id3dxallocatehierarchy.md)
</dt> </dl>

 

 
