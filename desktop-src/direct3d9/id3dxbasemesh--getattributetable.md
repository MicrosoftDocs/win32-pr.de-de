---
description: 'ID3DXBaseMesh::GetAttributeTable-Methode: Ruft entweder eine Attributtabelle für ein Gitternetz oder die Anzahl von Einträgen ab, die in einer Attributtabelle für ein Gitternetz gespeichert sind.'
ms.assetid: 15b24137-0ff9-4299-971b-90fa4ef2686d
title: ID3DXBaseMesh::GetAttributeTable-Methode (D3DX9Mesh.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXBaseMesh.GetAttributeTable
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 7f5d27de884f72b46db900487e26f1099bf30949
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2021
ms.locfileid: "108115448"
---
# <a name="id3dxbasemeshgetattributetable-method"></a><span data-ttu-id="1e6d7-103">ID3DXBaseMesh::GetAttributeTable-Methode</span><span class="sxs-lookup"><span data-stu-id="1e6d7-103">ID3DXBaseMesh::GetAttributeTable method</span></span>

<span data-ttu-id="1e6d7-104">Ruft entweder eine Attributtabelle für ein Gitternetz oder die Anzahl der Einträge ab, die in einer Attributtabelle für ein Gitternetz gespeichert sind.</span><span class="sxs-lookup"><span data-stu-id="1e6d7-104">Retrieves either an attribute table for a mesh, or the number of entries stored in an attribute table for a mesh.</span></span>

## <a name="syntax"></a><span data-ttu-id="1e6d7-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="1e6d7-105">Syntax</span></span>


```C++
HRESULT GetAttributeTable(
  [in, out] D3DXATTRIBUTERANGE *pAttribTable,
  [in, out] DWORD              *pAttribTableSize
);
```



## <a name="parameters"></a><span data-ttu-id="1e6d7-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="1e6d7-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="1e6d7-107">*pAttribTable* \[ in, out\]</span><span class="sxs-lookup"><span data-stu-id="1e6d7-107">*pAttribTable* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="1e6d7-108">Typ: **[ **D3DXATTRIBUTERANGE**](d3dxattributerange.md)\***</span><span class="sxs-lookup"><span data-stu-id="1e6d7-108">Type: **[**D3DXATTRIBUTERANGE**](d3dxattributerange.md)\***</span></span>

<span data-ttu-id="1e6d7-109">Zeiger auf ein Array von [**D3DXATTRIBUTERANGE-Strukturen,**](d3dxattributerange.md) das die Einträge in der Attributtabelle des Gitters darstellt.</span><span class="sxs-lookup"><span data-stu-id="1e6d7-109">Pointer to an array of [**D3DXATTRIBUTERANGE**](d3dxattributerange.md) structures, representing the entries in the mesh's attribute table.</span></span> <span data-ttu-id="1e6d7-110">Geben Sie **NULL** an, um den Wert für pAttribTableSize abzurufen.</span><span class="sxs-lookup"><span data-stu-id="1e6d7-110">Specify **NULL** to retrieve the value for pAttribTableSize.</span></span>

</dd> <dt>

<span data-ttu-id="1e6d7-111">*pAttribTableSize* \[ in, out\]</span><span class="sxs-lookup"><span data-stu-id="1e6d7-111">*pAttribTableSize* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="1e6d7-112">Typ: **[ **DWORD**](../winprog/windows-data-types.md)\***</span><span class="sxs-lookup"><span data-stu-id="1e6d7-112">Type: **[**DWORD**](../winprog/windows-data-types.md)\***</span></span>

<span data-ttu-id="1e6d7-113">Zeiger auf die Anzahl der in pAttribTable gespeicherten Einträge oder auf einen Wert, der mit der Anzahl von Einträgen gefüllt werden soll, die in der Attributtabelle für das Gitternetz gespeichert sind.</span><span class="sxs-lookup"><span data-stu-id="1e6d7-113">Pointer to either the number of entries stored in pAttribTable or a value to be filled in with the number of entries stored in the attribute table for the mesh.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="1e6d7-114">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="1e6d7-114">Return value</span></span>

<span data-ttu-id="1e6d7-115">Typ: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="1e6d7-115">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="1e6d7-116">Wenn die Methode erfolgreich ist, lautet der Rückgabewert D3D \_ OK.</span><span class="sxs-lookup"><span data-stu-id="1e6d7-116">If the method succeeds, the return value is D3D\_OK.</span></span> <span data-ttu-id="1e6d7-117">Wenn die Methode fehlschlägt, kann der Rückgabewert D3DERR \_ INVALIDCALL sein.</span><span class="sxs-lookup"><span data-stu-id="1e6d7-117">If the method fails, the return value can be D3DERR\_INVALIDCALL.</span></span>

## <a name="remarks"></a><span data-ttu-id="1e6d7-118">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="1e6d7-118">Remarks</span></span>

<span data-ttu-id="1e6d7-119">Eine Attributtabelle wird von [**ID3DXMesh::Optimize**](id3dxmesh--optimize.md) erstellt und D3DXMESHOPT \_ ATTRSORT für den Flags-Parameter übergeben.</span><span class="sxs-lookup"><span data-stu-id="1e6d7-119">An attribute table is created by [**ID3DXMesh::Optimize**](id3dxmesh--optimize.md) and passing D3DXMESHOPT\_ATTRSORT for the Flags parameter.</span></span>

<span data-ttu-id="1e6d7-120">Eine Attributtabelle wird verwendet, um Bereiche des Gitternetzes zu identifizieren, die mit unterschiedlichen Texturen, Renderzuständen, Materialien usw. gezeichnet werden müssen.</span><span class="sxs-lookup"><span data-stu-id="1e6d7-120">An attribute table is used to identify areas of the mesh that need to be drawn with different textures, render states, materials, and so on.</span></span> <span data-ttu-id="1e6d7-121">Darüber hinaus kann die Anwendung die Attributtabelle verwenden, um Teile eines Gitternetzes auszublenden, indem beim Zeichnen des Rahmens kein angegebener Attributbezeichner gezeichnet wird.</span><span class="sxs-lookup"><span data-stu-id="1e6d7-121">In addition, the application can use the attribute table to hide portions of a mesh by not drawing a given attribute identifier when drawing the frame.</span></span>

## <a name="requirements"></a><span data-ttu-id="1e6d7-122">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="1e6d7-122">Requirements</span></span>



| <span data-ttu-id="1e6d7-123">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="1e6d7-123">Requirement</span></span> | <span data-ttu-id="1e6d7-124">Wert</span><span class="sxs-lookup"><span data-stu-id="1e6d7-124">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="1e6d7-125">Header</span><span class="sxs-lookup"><span data-stu-id="1e6d7-125">Header</span></span><br/>  | <dl> <span data-ttu-id="1e6d7-126"><dt>D3DX9Mesh.h</dt></span><span class="sxs-lookup"><span data-stu-id="1e6d7-126"><dt>D3DX9Mesh.h</dt></span></span> </dl> |
| <span data-ttu-id="1e6d7-127">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="1e6d7-127">Library</span></span><br/> | <dl> <span data-ttu-id="1e6d7-128"><dt>D3dx9.lib</dt></span><span class="sxs-lookup"><span data-stu-id="1e6d7-128"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="1e6d7-129">Weitere Informationen</span><span class="sxs-lookup"><span data-stu-id="1e6d7-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="1e6d7-130">ID3DXBaseMesh</span><span class="sxs-lookup"><span data-stu-id="1e6d7-130">ID3DXBaseMesh</span></span>](id3dxbasemesh.md)
</dt> </dl>

 

 
