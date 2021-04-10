---
description: Legt die Attribut Tabelle für ein Mesh und die Anzahl der in der Tabelle gespeicherten Einträge fest.
ms.assetid: 629fd31b-d88a-4650-82ed-ab7c40690986
title: ID3DX10Mesh::-Methode (d3dx10. h)
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
ms.openlocfilehash: 808349b3f7456ebf3f8e1c3a7f9fdf2236db4beb
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/15/2021
ms.locfileid: "104219609"
---
# <a name="id3dx10meshsetattributetable-method"></a><span data-ttu-id="5e160-103">ID3DX10Mesh::-Methode</span><span class="sxs-lookup"><span data-stu-id="5e160-103">ID3DX10Mesh::SetAttributeTable method</span></span>

<span data-ttu-id="5e160-104">Legt die Attribut Tabelle für ein Mesh und die Anzahl der in der Tabelle gespeicherten Einträge fest.</span><span class="sxs-lookup"><span data-stu-id="5e160-104">Sets the attribute table for a mesh and the number of entries stored in the table.</span></span>

## <a name="syntax"></a><span data-ttu-id="5e160-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="5e160-105">Syntax</span></span>


```C++
HRESULT SetAttributeTable(
  [in] const D3DX10_ATTRIBUTE_RANGE *pAttribTable,
  [in]       UINT                   cAttribTableSize
);
```



## <a name="parameters"></a><span data-ttu-id="5e160-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="5e160-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="5e160-107">*pattribtable* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="5e160-107">*pAttribTable* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="5e160-108">Type: **Konstanten [**d3dx10 \_ Attribut \_ Bereich**](d3dx10-attribute-range.md) \***</span><span class="sxs-lookup"><span data-stu-id="5e160-108">Type: **const [**D3DX10\_ATTRIBUTE\_RANGE**](d3dx10-attribute-range.md)\***</span></span>

<span data-ttu-id="5e160-109">Ein Zeiger auf ein Array von d3dx10- \_ Attribut \_ Bereichs Strukturen, die die Einträge in der Tabelle des Mesh-Attributs darstellen.</span><span class="sxs-lookup"><span data-stu-id="5e160-109">Pointer to an array of D3DX10\_ATTRIBUTE\_RANGE structures, representing the entries in the mesh attribute table.</span></span>

</dd> <dt>

<span data-ttu-id="5e160-110">"" "" "".  \[ in\]</span><span class="sxs-lookup"><span data-stu-id="5e160-110">*cAttribTableSize* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="5e160-111">Typ: **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="5e160-111">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="5e160-112">Anzahl von Attributen in der Tabelle "Mesh-Attribut".</span><span class="sxs-lookup"><span data-stu-id="5e160-112">Number of attributes in the mesh attribute table.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="5e160-113">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="5e160-113">Return value</span></span>

<span data-ttu-id="5e160-114">Typ: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="5e160-114">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="5e160-115">Der Rückgabewert ist einer der Werte, die in [Direct3D 10-Rückgabe Codes](d3d10-graphics-reference-returnvalues.md)aufgelistet sind.</span><span class="sxs-lookup"><span data-stu-id="5e160-115">The return value is one of the values listed in [Direct3D 10 Return Codes](d3d10-graphics-reference-returnvalues.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="5e160-116">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="5e160-116">Remarks</span></span>

<span data-ttu-id="5e160-117">Wenn eine Anwendung die Informationen in einer Attribut Tabelle nachverfolgt und die Tabelle als Ergebnis von Änderungen an Attributen oder Gesichtern neu anordnet, ermöglicht diese Methode der Anwendung, die Attribut Tabellen zu aktualisieren, anstatt ID3DX10Mesh:: optimiert erneut aufzurufende.</span><span class="sxs-lookup"><span data-stu-id="5e160-117">If an application keeps track of the information in an attribute table, and rearranges the table as a result of changes to attributes or faces, this method allows the application to update the attribute tables instead of calling ID3DX10Mesh::Optimize again.</span></span>

## <a name="requirements"></a><span data-ttu-id="5e160-118">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="5e160-118">Requirements</span></span>



| <span data-ttu-id="5e160-119">Anforderung</span><span class="sxs-lookup"><span data-stu-id="5e160-119">Requirement</span></span> | <span data-ttu-id="5e160-120">Wert</span><span class="sxs-lookup"><span data-stu-id="5e160-120">Value</span></span> |
|--------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="5e160-121">Header</span><span class="sxs-lookup"><span data-stu-id="5e160-121">Header</span></span><br/>  | <dl> <span data-ttu-id="5e160-122"><dt>D3dx10. h</dt></span><span class="sxs-lookup"><span data-stu-id="5e160-122"><dt>D3DX10.h</dt></span></span> </dl>   |
| <span data-ttu-id="5e160-123">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="5e160-123">Library</span></span><br/> | <dl> <span data-ttu-id="5e160-124"><dt>D3dx10. lib</dt></span><span class="sxs-lookup"><span data-stu-id="5e160-124"><dt>D3DX10.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="5e160-125">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="5e160-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="5e160-126">ID3DX10Mesh</span><span class="sxs-lookup"><span data-stu-id="5e160-126">ID3DX10Mesh</span></span>](id3dx10mesh.md)
</dt> <dt>

[<span data-ttu-id="5e160-127">D3DX-Schnittstellen</span><span class="sxs-lookup"><span data-stu-id="5e160-127">D3DX Interfaces</span></span>](d3d10-graphics-reference-d3dx10-interfaces.md)
</dt> </dl>

 

 
