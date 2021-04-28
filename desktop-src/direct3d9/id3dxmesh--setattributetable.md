---
description: 'ID3DXMesh::SetAttributeTable-Methode: Legt die Attributtabelle für ein Gitternetz und die Anzahl der in der Tabelle gespeicherten Einträge fest.'
ms.assetid: 22d46708-cffd-48da-bdad-8a43f9076356
title: ID3DXMesh::SetAttributeTable-Methode (D3DX9Mesh.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXMesh.SetAttributeTable
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: a4cdb503e934ca00b41482601b59266eee750365
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2021
ms.locfileid: "108093348"
---
# <a name="id3dxmeshsetattributetable-method"></a><span data-ttu-id="14bbe-103">ID3DXMesh::SetAttributeTable-Methode</span><span class="sxs-lookup"><span data-stu-id="14bbe-103">ID3DXMesh::SetAttributeTable method</span></span>

<span data-ttu-id="14bbe-104">Legt die Attributtabelle für ein Gitternetz und die Anzahl der in der Tabelle gespeicherten Einträge fest.</span><span class="sxs-lookup"><span data-stu-id="14bbe-104">Sets the attribute table for a mesh and the number of entries stored in the table.</span></span>

## <a name="syntax"></a><span data-ttu-id="14bbe-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="14bbe-105">Syntax</span></span>


```C++
HRESULT SetAttributeTable(
  [in] const D3DXATTRIBUTERANGE *pAttribTable,
  [in]       DWORD              cAttribTableSize
);
```



## <a name="parameters"></a><span data-ttu-id="14bbe-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="14bbe-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="14bbe-107">*pAttribTable* \[ In\]</span><span class="sxs-lookup"><span data-stu-id="14bbe-107">*pAttribTable* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="14bbe-108">Typ: **const [**D3DXATTRIBUTERANGE**](d3dxattributerange.md) \***</span><span class="sxs-lookup"><span data-stu-id="14bbe-108">Type: **const [**D3DXATTRIBUTERANGE**](d3dxattributerange.md)\***</span></span>

<span data-ttu-id="14bbe-109">Zeiger auf ein Array von [**D3DXATTRIBUTERANGE-Strukturen,**](d3dxattributerange.md) das die Einträge in der Meshattributtabelle darstellt.</span><span class="sxs-lookup"><span data-stu-id="14bbe-109">Pointer to an array of [**D3DXATTRIBUTERANGE**](d3dxattributerange.md) structures, representing the entries in the mesh attribute table.</span></span>

</dd> <dt>

<span data-ttu-id="14bbe-110">*cAttribTableSize* \[ In\]</span><span class="sxs-lookup"><span data-stu-id="14bbe-110">*cAttribTableSize* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="14bbe-111">Typ: **[ **DWORD**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="14bbe-111">Type: **[**DWORD**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="14bbe-112">Anzahl der Attribute in der Meshattributtabelle.</span><span class="sxs-lookup"><span data-stu-id="14bbe-112">Number of attributes in the mesh attribute table.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="14bbe-113">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="14bbe-113">Return value</span></span>

<span data-ttu-id="14bbe-114">Typ: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="14bbe-114">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="14bbe-115">Wenn die Methode erfolgreich ist, lautet der Rückgabewert D3D \_ OK.</span><span class="sxs-lookup"><span data-stu-id="14bbe-115">If the method succeeds, the return value is D3D\_OK.</span></span> <span data-ttu-id="14bbe-116">Wenn die Methode fehlschlägt, kann der Rückgabewert einer der folgenden Werte sein: D3DERR \_ INVALIDCALL, E \_ OUTOFMEMORY.</span><span class="sxs-lookup"><span data-stu-id="14bbe-116">If the method fails, the return value can be one of the following: D3DERR\_INVALIDCALL, E\_OUTOFMEMORY.</span></span>

## <a name="remarks"></a><span data-ttu-id="14bbe-117">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="14bbe-117">Remarks</span></span>

<span data-ttu-id="14bbe-118">Wenn eine Anwendung die Informationen in einer Attributtabelle nachverfolgt und die Tabelle aufgrund von Änderungen an Attributen oder Gesichtern neu anordnt, ermöglicht diese Methode der Anwendung, die Attributtabellen zu aktualisieren, anstatt [**ID3DXMesh::Optimize**](id3dxmesh--optimize.md) erneut aufzurufen.</span><span class="sxs-lookup"><span data-stu-id="14bbe-118">If an application keeps track of the information in an attribute table, and rearranges the table as a result of changes to attributes or faces, this method allows the application to update the attribute tables instead of calling [**ID3DXMesh::Optimize**](id3dxmesh--optimize.md) again.</span></span>

## <a name="requirements"></a><span data-ttu-id="14bbe-119">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="14bbe-119">Requirements</span></span>



| <span data-ttu-id="14bbe-120">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="14bbe-120">Requirement</span></span> | <span data-ttu-id="14bbe-121">Wert</span><span class="sxs-lookup"><span data-stu-id="14bbe-121">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="14bbe-122">Header</span><span class="sxs-lookup"><span data-stu-id="14bbe-122">Header</span></span><br/>  | <dl> <span data-ttu-id="14bbe-123"><dt>D3DX9Mesh.h</dt></span><span class="sxs-lookup"><span data-stu-id="14bbe-123"><dt>D3DX9Mesh.h</dt></span></span> </dl> |
| <span data-ttu-id="14bbe-124">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="14bbe-124">Library</span></span><br/> | <dl> <span data-ttu-id="14bbe-125"><dt>D3dx9.lib</dt></span><span class="sxs-lookup"><span data-stu-id="14bbe-125"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="14bbe-126">Weitere Informationen</span><span class="sxs-lookup"><span data-stu-id="14bbe-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="14bbe-127">ID3DXMesh</span><span class="sxs-lookup"><span data-stu-id="14bbe-127">ID3DXMesh</span></span>](id3dxmesh.md)
</dt> <dt>

[<span data-ttu-id="14bbe-128">**ID3DXMesh::LockAttributeBuffer**</span><span class="sxs-lookup"><span data-stu-id="14bbe-128">**ID3DXMesh::LockAttributeBuffer**</span></span>](id3dxmesh--lockattributebuffer.md)
</dt> <dt>

<span data-ttu-id="14bbe-129">**ID3DXMesh::LockAttributeBuffer**</span><span class="sxs-lookup"><span data-stu-id="14bbe-129">**ID3DXMesh::LockAttributeBuffer**</span></span>
</dt> </dl>

 

 
