---
description: Legt die Attribut Tabelle für ein Mesh und die Anzahl der in der Tabelle gespeicherten Einträge fest.
ms.assetid: 22d46708-cffd-48da-bdad-8a43f9076356
title: ID3DXMesh::-Methode (D3DX9Mesh. h)
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
ms.openlocfilehash: 17ae3458bffd05114415a92538a8ce8ef2cc847e
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/15/2021
ms.locfileid: "106353345"
---
# <a name="id3dxmeshsetattributetable-method"></a><span data-ttu-id="545d4-103">ID3DXMesh::-Methode</span><span class="sxs-lookup"><span data-stu-id="545d4-103">ID3DXMesh::SetAttributeTable method</span></span>

<span data-ttu-id="545d4-104">Legt die Attribut Tabelle für ein Mesh und die Anzahl der in der Tabelle gespeicherten Einträge fest.</span><span class="sxs-lookup"><span data-stu-id="545d4-104">Sets the attribute table for a mesh and the number of entries stored in the table.</span></span>

## <a name="syntax"></a><span data-ttu-id="545d4-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="545d4-105">Syntax</span></span>


```C++
HRESULT SetAttributeTable(
  [in] const D3DXATTRIBUTERANGE *pAttribTable,
  [in]       DWORD              cAttribTableSize
);
```



## <a name="parameters"></a><span data-ttu-id="545d4-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="545d4-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="545d4-107">*pattribtable* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="545d4-107">*pAttribTable* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="545d4-108">Typ: **Konstanten [**D3DXATTRIBUTERANGE**](d3dxattributerange.md) \***</span><span class="sxs-lookup"><span data-stu-id="545d4-108">Type: **const [**D3DXATTRIBUTERANGE**](d3dxattributerange.md)\***</span></span>

<span data-ttu-id="545d4-109">Ein Zeiger auf ein Array von [**D3DXATTRIBUTERANGE**](d3dxattributerange.md) -Strukturen, die die Einträge in der Tabelle des Mesh-Attributs darstellen.</span><span class="sxs-lookup"><span data-stu-id="545d4-109">Pointer to an array of [**D3DXATTRIBUTERANGE**](d3dxattributerange.md) structures, representing the entries in the mesh attribute table.</span></span>

</dd> <dt>

<span data-ttu-id="545d4-110">"" "" "".  \[ in\]</span><span class="sxs-lookup"><span data-stu-id="545d4-110">*cAttribTableSize* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="545d4-111">Typ: **[ **DWORD**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="545d4-111">Type: **[**DWORD**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="545d4-112">Anzahl von Attributen in der Tabelle "Mesh-Attribut".</span><span class="sxs-lookup"><span data-stu-id="545d4-112">Number of attributes in the mesh attribute table.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="545d4-113">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="545d4-113">Return value</span></span>

<span data-ttu-id="545d4-114">Typ: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="545d4-114">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="545d4-115">Wenn die Methode erfolgreich ausgeführt wird, ist der Rückgabewert D3D \_ OK.</span><span class="sxs-lookup"><span data-stu-id="545d4-115">If the method succeeds, the return value is D3D\_OK.</span></span> <span data-ttu-id="545d4-116">Wenn die Methode fehlschlägt, kann der Rückgabewert einer der folgenden sein: D3DERR \_ invalidcall, E \_ outo fmemory.</span><span class="sxs-lookup"><span data-stu-id="545d4-116">If the method fails, the return value can be one of the following: D3DERR\_INVALIDCALL, E\_OUTOFMEMORY.</span></span>

## <a name="remarks"></a><span data-ttu-id="545d4-117">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="545d4-117">Remarks</span></span>

<span data-ttu-id="545d4-118">Wenn eine Anwendung die Informationen in einer Attribut Tabelle nachverfolgt und die Tabelle als Ergebnis von Änderungen an Attributen oder Gesichtern neu anordnet, ermöglicht diese Methode der Anwendung, die Attribut Tabellen zu aktualisieren, anstatt [**ID3DXMesh:: optimiert**](id3dxmesh--optimize.md) erneut aufzurufende.</span><span class="sxs-lookup"><span data-stu-id="545d4-118">If an application keeps track of the information in an attribute table, and rearranges the table as a result of changes to attributes or faces, this method allows the application to update the attribute tables instead of calling [**ID3DXMesh::Optimize**](id3dxmesh--optimize.md) again.</span></span>

## <a name="requirements"></a><span data-ttu-id="545d4-119">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="545d4-119">Requirements</span></span>



| <span data-ttu-id="545d4-120">Anforderung</span><span class="sxs-lookup"><span data-stu-id="545d4-120">Requirement</span></span> | <span data-ttu-id="545d4-121">Wert</span><span class="sxs-lookup"><span data-stu-id="545d4-121">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="545d4-122">Header</span><span class="sxs-lookup"><span data-stu-id="545d4-122">Header</span></span><br/>  | <dl> <span data-ttu-id="545d4-123"><dt>D3DX9Mesh. h</dt></span><span class="sxs-lookup"><span data-stu-id="545d4-123"><dt>D3DX9Mesh.h</dt></span></span> </dl> |
| <span data-ttu-id="545d4-124">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="545d4-124">Library</span></span><br/> | <dl> <span data-ttu-id="545d4-125"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="545d4-125"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="545d4-126">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="545d4-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="545d4-127">ID3DXMesh</span><span class="sxs-lookup"><span data-stu-id="545d4-127">ID3DXMesh</span></span>](id3dxmesh.md)
</dt> <dt>

[<span data-ttu-id="545d4-128">**ID3DXMesh:: LockAttributeBuffer**</span><span class="sxs-lookup"><span data-stu-id="545d4-128">**ID3DXMesh::LockAttributeBuffer**</span></span>](id3dxmesh--lockattributebuffer.md)
</dt> <dt>

<span data-ttu-id="545d4-129">**ID3DXMesh:: LockAttributeBuffer**</span><span class="sxs-lookup"><span data-stu-id="545d4-129">**ID3DXMesh::LockAttributeBuffer**</span></span>
</dt> </dl>

 

 
