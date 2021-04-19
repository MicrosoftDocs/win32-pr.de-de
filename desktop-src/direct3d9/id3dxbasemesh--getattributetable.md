---
description: Ruft entweder eine Attribut Tabelle für ein Mesh oder die Anzahl der in einer Attribut Tabelle gespeicherten Einträge für ein Mesh ab.
ms.assetid: 15b24137-0ff9-4299-971b-90fa4ef2686d
title: 'ID3DXBaseMesh:: GetAttributeTable-Methode (D3DX9Mesh. h)'
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
ms.openlocfilehash: 70c93c8f477655200418793f53706731b42a47ac
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/15/2021
ms.locfileid: "106370442"
---
# <a name="id3dxbasemeshgetattributetable-method"></a><span data-ttu-id="30cd1-103">ID3DXBaseMesh:: GetAttributeTable-Methode</span><span class="sxs-lookup"><span data-stu-id="30cd1-103">ID3DXBaseMesh::GetAttributeTable method</span></span>

<span data-ttu-id="30cd1-104">Ruft entweder eine Attribut Tabelle für ein Mesh oder die Anzahl der in einer Attribut Tabelle gespeicherten Einträge für ein Mesh ab.</span><span class="sxs-lookup"><span data-stu-id="30cd1-104">Retrieves either an attribute table for a mesh, or the number of entries stored in an attribute table for a mesh.</span></span>

## <a name="syntax"></a><span data-ttu-id="30cd1-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="30cd1-105">Syntax</span></span>


```C++
HRESULT GetAttributeTable(
  [in, out] D3DXATTRIBUTERANGE *pAttribTable,
  [in, out] DWORD              *pAttribTableSize
);
```



## <a name="parameters"></a><span data-ttu-id="30cd1-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="30cd1-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="30cd1-107">*pattribtable* \[ in, out\]</span><span class="sxs-lookup"><span data-stu-id="30cd1-107">*pAttribTable* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="30cd1-108">Typ: **[ **D3DXATTRIBUTERANGE**](d3dxattributerange.md)\***</span><span class="sxs-lookup"><span data-stu-id="30cd1-108">Type: **[**D3DXATTRIBUTERANGE**](d3dxattributerange.md)\***</span></span>

<span data-ttu-id="30cd1-109">Zeiger auf ein Array von [**D3DXATTRIBUTERANGE**](d3dxattributerange.md) -Strukturen, das die Einträge in der Attribut Tabelle des Mesh darstellt.</span><span class="sxs-lookup"><span data-stu-id="30cd1-109">Pointer to an array of [**D3DXATTRIBUTERANGE**](d3dxattributerange.md) structures, representing the entries in the mesh's attribute table.</span></span> <span data-ttu-id="30cd1-110">Geben Sie **null** an, um den Wert für pattribtablesize abzurufen.</span><span class="sxs-lookup"><span data-stu-id="30cd1-110">Specify **NULL** to retrieve the value for pAttribTableSize.</span></span>

</dd> <dt>

<span data-ttu-id="30cd1-111">*pattribtablesize* \[ in, out\]</span><span class="sxs-lookup"><span data-stu-id="30cd1-111">*pAttribTableSize* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="30cd1-112">Typ: **[ **DWORD**](../winprog/windows-data-types.md)\***</span><span class="sxs-lookup"><span data-stu-id="30cd1-112">Type: **[**DWORD**](../winprog/windows-data-types.md)\***</span></span>

<span data-ttu-id="30cd1-113">Ein Zeiger auf die Anzahl der in pattribtable gespeicherten Einträge oder ein Wert, der mit der Anzahl der in der Attribut Tabelle für das Mesh gespeicherten Einträge aufgefüllt werden soll.</span><span class="sxs-lookup"><span data-stu-id="30cd1-113">Pointer to either the number of entries stored in pAttribTable or a value to be filled in with the number of entries stored in the attribute table for the mesh.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="30cd1-114">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="30cd1-114">Return value</span></span>

<span data-ttu-id="30cd1-115">Typ: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="30cd1-115">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="30cd1-116">Wenn die Methode erfolgreich ausgeführt wird, ist der Rückgabewert D3D \_ OK.</span><span class="sxs-lookup"><span data-stu-id="30cd1-116">If the method succeeds, the return value is D3D\_OK.</span></span> <span data-ttu-id="30cd1-117">Wenn die Methode fehlschlägt, kann der Rückgabewert "D3DERR \_ invalidcall" lauten.</span><span class="sxs-lookup"><span data-stu-id="30cd1-117">If the method fails, the return value can be D3DERR\_INVALIDCALL.</span></span>

## <a name="remarks"></a><span data-ttu-id="30cd1-118">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="30cd1-118">Remarks</span></span>

<span data-ttu-id="30cd1-119">Eine Attribut Tabelle wird von [**ID3DXMesh:: optimiert**](id3dxmesh--optimize.md) erstellt und D3DXMESHOPT \_ attrsort für den flags-Parameter übergeben.</span><span class="sxs-lookup"><span data-stu-id="30cd1-119">An attribute table is created by [**ID3DXMesh::Optimize**](id3dxmesh--optimize.md) and passing D3DXMESHOPT\_ATTRSORT for the Flags parameter.</span></span>

<span data-ttu-id="30cd1-120">Eine Attribut Tabelle wird verwendet, um Bereiche des Netzes zu identifizieren, die mit unterschiedlichen Texturen, renderzuständen, Materialien usw. gezeichnet werden müssen.</span><span class="sxs-lookup"><span data-stu-id="30cd1-120">An attribute table is used to identify areas of the mesh that need to be drawn with different textures, render states, materials, and so on.</span></span> <span data-ttu-id="30cd1-121">Außerdem kann die Anwendung die Attribut Tabelle verwenden, um Teile eines Netzes auszublenden, indem beim Zeichnen des Frames kein angegebener Attribut Bezeichner gezeichnet wird.</span><span class="sxs-lookup"><span data-stu-id="30cd1-121">In addition, the application can use the attribute table to hide portions of a mesh by not drawing a given attribute identifier when drawing the frame.</span></span>

## <a name="requirements"></a><span data-ttu-id="30cd1-122">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="30cd1-122">Requirements</span></span>



| <span data-ttu-id="30cd1-123">Anforderung</span><span class="sxs-lookup"><span data-stu-id="30cd1-123">Requirement</span></span> | <span data-ttu-id="30cd1-124">Wert</span><span class="sxs-lookup"><span data-stu-id="30cd1-124">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="30cd1-125">Header</span><span class="sxs-lookup"><span data-stu-id="30cd1-125">Header</span></span><br/>  | <dl> <span data-ttu-id="30cd1-126"><dt>D3DX9Mesh. h</dt></span><span class="sxs-lookup"><span data-stu-id="30cd1-126"><dt>D3DX9Mesh.h</dt></span></span> </dl> |
| <span data-ttu-id="30cd1-127">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="30cd1-127">Library</span></span><br/> | <dl> <span data-ttu-id="30cd1-128"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="30cd1-128"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="30cd1-129">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="30cd1-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="30cd1-130">ID3DXBaseMesh</span><span class="sxs-lookup"><span data-stu-id="30cd1-130">ID3DXBaseMesh</span></span>](id3dxbasemesh.md)
</dt> </dl>

 

 
