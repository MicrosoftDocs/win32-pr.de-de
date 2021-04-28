---
description: 'ID3DX10Mesh::SetAttributeTable-Methode: Legt die Attributtabelle für ein Mesh und die Anzahl der in der Tabelle gespeicherten Einträge fest.'
ms.assetid: 629fd31b-d88a-4650-82ed-ab7c40690986
title: ID3DX10Mesh::SetAttributeTable-Methode (D3DX10.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DX10Mesh.SetAttributeTable
api_type:
- COM
api_location:
- D3DX10.lib
- D3DX10.dll
ms.openlocfilehash: 4e06b181bb512e16e9caaa0d233ebbd3472bfcf8
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2021
ms.locfileid: "108084008"
---
# <a name="id3dx10meshsetattributetable-method"></a><span data-ttu-id="31a42-103">ID3DX10Mesh::SetAttributeTable-Methode</span><span class="sxs-lookup"><span data-stu-id="31a42-103">ID3DX10Mesh::SetAttributeTable method</span></span>

<span data-ttu-id="31a42-104">Legt die Attributtabelle für ein Gitternetz und die Anzahl der in der Tabelle gespeicherten Einträge fest.</span><span class="sxs-lookup"><span data-stu-id="31a42-104">Sets the attribute table for a mesh and the number of entries stored in the table.</span></span>

## <a name="syntax"></a><span data-ttu-id="31a42-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="31a42-105">Syntax</span></span>


```C++
HRESULT SetAttributeTable(
  [in] const D3DX10_ATTRIBUTE_RANGE *pAttribTable,
  [in]       UINT                   cAttribTableSize
);
```



## <a name="parameters"></a><span data-ttu-id="31a42-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="31a42-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="31a42-107">*pAttribTable* \[ In\]</span><span class="sxs-lookup"><span data-stu-id="31a42-107">*pAttribTable* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="31a42-108">Typ: **const [**D3DX10 \_ ATTRIBUTE \_ RANGE**](d3dx10-attribute-range.md) \***</span><span class="sxs-lookup"><span data-stu-id="31a42-108">Type: **const [**D3DX10\_ATTRIBUTE\_RANGE**](d3dx10-attribute-range.md)\***</span></span>

<span data-ttu-id="31a42-109">Zeiger auf ein Array von D3DX10 \_ ATTRIBUTE \_ RANGE-Strukturen, die die Einträge in der Gitternetzattributtabelle darstellen.</span><span class="sxs-lookup"><span data-stu-id="31a42-109">Pointer to an array of D3DX10\_ATTRIBUTE\_RANGE structures, representing the entries in the mesh attribute table.</span></span>

</dd> <dt>

<span data-ttu-id="31a42-110">*cAttribTableSize* \[ In\]</span><span class="sxs-lookup"><span data-stu-id="31a42-110">*cAttribTableSize* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="31a42-111">Typ: **[ **UINT**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="31a42-111">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="31a42-112">Anzahl der Attribute in der Gitternetzattributtabelle.</span><span class="sxs-lookup"><span data-stu-id="31a42-112">Number of attributes in the mesh attribute table.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="31a42-113">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="31a42-113">Return value</span></span>

<span data-ttu-id="31a42-114">Typ: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="31a42-114">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="31a42-115">Der Rückgabewert ist einer der Unter [Direct3D 10-Rückgabecodes aufgeführten Werte.](d3d10-graphics-reference-returnvalues.md)</span><span class="sxs-lookup"><span data-stu-id="31a42-115">The return value is one of the values listed in [Direct3D 10 Return Codes](d3d10-graphics-reference-returnvalues.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="31a42-116">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="31a42-116">Remarks</span></span>

<span data-ttu-id="31a42-117">Wenn eine Anwendung die Informationen in einer Attributtabelle nachverfolgt und die Tabelle infolge von Änderungen an Attributen oder Gesichtern neu ansortiert, ermöglicht diese Methode der Anwendung, die Attributtabellen zu aktualisieren, anstatt ID3DX10Mesh::Optimize erneut auf aufruft.</span><span class="sxs-lookup"><span data-stu-id="31a42-117">If an application keeps track of the information in an attribute table, and rearranges the table as a result of changes to attributes or faces, this method allows the application to update the attribute tables instead of calling ID3DX10Mesh::Optimize again.</span></span>

## <a name="requirements"></a><span data-ttu-id="31a42-118">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="31a42-118">Requirements</span></span>



| <span data-ttu-id="31a42-119">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="31a42-119">Requirement</span></span> | <span data-ttu-id="31a42-120">Wert</span><span class="sxs-lookup"><span data-stu-id="31a42-120">Value</span></span> |
|--------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="31a42-121">Header</span><span class="sxs-lookup"><span data-stu-id="31a42-121">Header</span></span><br/>  | <dl> <span data-ttu-id="31a42-122"><dt>D3DX10.h</dt></span><span class="sxs-lookup"><span data-stu-id="31a42-122"><dt>D3DX10.h</dt></span></span> </dl>   |
| <span data-ttu-id="31a42-123">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="31a42-123">Library</span></span><br/> | <dl> <span data-ttu-id="31a42-124"><dt>D3DX10.lib</dt></span><span class="sxs-lookup"><span data-stu-id="31a42-124"><dt>D3DX10.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="31a42-125">Weitere Informationen</span><span class="sxs-lookup"><span data-stu-id="31a42-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="31a42-126">ID3DX10Mesh</span><span class="sxs-lookup"><span data-stu-id="31a42-126">ID3DX10Mesh</span></span>](id3dx10mesh.md)
</dt> <dt>

[<span data-ttu-id="31a42-127">D3DX-Schnittstellen</span><span class="sxs-lookup"><span data-stu-id="31a42-127">D3DX Interfaces</span></span>](d3d10-graphics-reference-d3dx10-interfaces.md)
</dt> </dl>

 

 
