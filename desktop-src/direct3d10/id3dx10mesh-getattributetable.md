---
description: Ruft entweder eine Attribut Tabelle für ein Mesh oder die Anzahl der in einer Attribut Tabelle gespeicherten Einträge für ein Mesh ab.
ms.assetid: cee49eba-c113-49f5-a702-c366401f1f2d
title: 'ID3DX10Mesh:: GetAttributeTable-Methode (d3dx10. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DX10Mesh.GetAttributeTable
api_type:
- COM
api_location:
- D3DX10.lib
- D3DX10.dll
ms.openlocfilehash: 4ff00f3c5d036b3b463bc7c6622de75361b196e6
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/15/2021
ms.locfileid: "106366670"
---
# <a name="id3dx10meshgetattributetable-method"></a><span data-ttu-id="ca849-103">ID3DX10Mesh:: GetAttributeTable-Methode</span><span class="sxs-lookup"><span data-stu-id="ca849-103">ID3DX10Mesh::GetAttributeTable method</span></span>

<span data-ttu-id="ca849-104">Ruft entweder eine Attribut Tabelle für ein Mesh oder die Anzahl der in einer Attribut Tabelle gespeicherten Einträge für ein Mesh ab.</span><span class="sxs-lookup"><span data-stu-id="ca849-104">Retrieves either an attribute table for a mesh, or the number of entries stored in an attribute table for a mesh.</span></span>

## <a name="syntax"></a><span data-ttu-id="ca849-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="ca849-105">Syntax</span></span>


```C++
HRESULT GetAttributeTable(
  [in] D3DX10_ATTRIBUTE_RANGE *pAttribTable,
  [in] UINT                   *pAttribTableSize
);
```



## <a name="parameters"></a><span data-ttu-id="ca849-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="ca849-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="ca849-107">*pattribtable* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="ca849-107">*pAttribTable* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="ca849-108">Type: **[ **d3dx10- \_ Attribut \_ Bereich**](d3dx10-attribute-range.md)\***</span><span class="sxs-lookup"><span data-stu-id="ca849-108">Type: **[**D3DX10\_ATTRIBUTE\_RANGE**](d3dx10-attribute-range.md)\***</span></span>

<span data-ttu-id="ca849-109">Ein Zeiger auf ein Array von \_ d3dx10 \_ -Attribut Bereichs Strukturen, die die Einträge in der Attribut Tabelle des Mesh darstellen.</span><span class="sxs-lookup"><span data-stu-id="ca849-109">Pointer to an array of D3DX10\_ATTRIBUTE\_RANGE structures, representing the entries in the mesh's attribute table.</span></span> <span data-ttu-id="ca849-110">Geben Sie **null** an, um den Wert für pattribtablesize abzurufen.</span><span class="sxs-lookup"><span data-stu-id="ca849-110">Specify **NULL** to retrieve the value for pAttribTableSize.</span></span>

</dd> <dt>

<span data-ttu-id="ca849-111">*pattribtablesize* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="ca849-111">*pAttribTableSize* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="ca849-112">Typ: **[ **uint**](../winprog/windows-data-types.md)\***</span><span class="sxs-lookup"><span data-stu-id="ca849-112">Type: **[**UINT**](../winprog/windows-data-types.md)\***</span></span>

<span data-ttu-id="ca849-113">Ein Zeiger auf die Anzahl der in pattribtable gespeicherten Einträge oder ein Wert, der mit der Anzahl der in der Attribut Tabelle für das Mesh gespeicherten Einträge aufgefüllt werden soll.</span><span class="sxs-lookup"><span data-stu-id="ca849-113">Pointer to either the number of entries stored in pAttribTable or a value to be filled in with the number of entries stored in the attribute table for the mesh.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="ca849-114">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="ca849-114">Return value</span></span>

<span data-ttu-id="ca849-115">Typ: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="ca849-115">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="ca849-116">Der Rückgabewert ist einer der Werte, die in [Direct3D 10-Rückgabe Codes](d3d10-graphics-reference-returnvalues.md)aufgelistet sind.</span><span class="sxs-lookup"><span data-stu-id="ca849-116">The return value is one of the values listed in [Direct3D 10 Return Codes](d3d10-graphics-reference-returnvalues.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="ca849-117">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="ca849-117">Remarks</span></span>

<span data-ttu-id="ca849-118">Eine Attribut Tabelle wird verwendet, um Bereiche des Netzes zu identifizieren, die mit unterschiedlichen Texturen, renderzuständen, Materialien usw. gezeichnet werden müssen.</span><span class="sxs-lookup"><span data-stu-id="ca849-118">An attribute table is used to identify areas of the mesh that need to be drawn with different textures, render states, materials, and so on.</span></span> <span data-ttu-id="ca849-119">Außerdem kann die Anwendung die Attribut Tabelle verwenden, um Teile eines Netzes auszublenden, indem beim Zeichnen des Frames kein angegebener Attribut Bezeichner gezeichnet wird.</span><span class="sxs-lookup"><span data-stu-id="ca849-119">In addition, the application can use the attribute table to hide portions of a mesh by not drawing a given attribute identifier when drawing the frame.</span></span>

## <a name="requirements"></a><span data-ttu-id="ca849-120">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="ca849-120">Requirements</span></span>



| <span data-ttu-id="ca849-121">Anforderung</span><span class="sxs-lookup"><span data-stu-id="ca849-121">Requirement</span></span> | <span data-ttu-id="ca849-122">Wert</span><span class="sxs-lookup"><span data-stu-id="ca849-122">Value</span></span> |
|--------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="ca849-123">Header</span><span class="sxs-lookup"><span data-stu-id="ca849-123">Header</span></span><br/>  | <dl> <span data-ttu-id="ca849-124"><dt>D3dx10. h</dt></span><span class="sxs-lookup"><span data-stu-id="ca849-124"><dt>D3DX10.h</dt></span></span> </dl>   |
| <span data-ttu-id="ca849-125">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="ca849-125">Library</span></span><br/> | <dl> <span data-ttu-id="ca849-126"><dt>D3dx10. lib</dt></span><span class="sxs-lookup"><span data-stu-id="ca849-126"><dt>D3DX10.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="ca849-127">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="ca849-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ca849-128">ID3DX10Mesh</span><span class="sxs-lookup"><span data-stu-id="ca849-128">ID3DX10Mesh</span></span>](id3dx10mesh.md)
</dt> <dt>

[<span data-ttu-id="ca849-129">D3DX-Schnittstellen</span><span class="sxs-lookup"><span data-stu-id="ca849-129">D3DX Interfaces</span></span>](d3d10-graphics-reference-d3dx10-interfaces.md)
</dt> </dl>

 

 
