---
description: 'ID3DX10Mesh::GetAttributeTable-Methode: Ruft entweder eine Attributtabelle für ein Gitternetz oder die Anzahl von Einträgen ab, die in einer Attributtabelle für ein Gitternetz gespeichert sind.'
ms.assetid: cee49eba-c113-49f5-a702-c366401f1f2d
title: ID3DX10Mesh::GetAttributeTable-Methode (D3DX10.h)
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
ms.openlocfilehash: e7fc503af1a290b27fea81d0c2aba6b84393323b
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2021
ms.locfileid: "108083988"
---
# <a name="id3dx10meshgetattributetable-method"></a><span data-ttu-id="15a8a-103">ID3DX10Mesh::GetAttributeTable-Methode</span><span class="sxs-lookup"><span data-stu-id="15a8a-103">ID3DX10Mesh::GetAttributeTable method</span></span>

<span data-ttu-id="15a8a-104">Ruft entweder eine Attributtabelle für ein Gitternetz oder die Anzahl von Einträgen ab, die in einer Attributtabelle für ein Gitternetz gespeichert sind.</span><span class="sxs-lookup"><span data-stu-id="15a8a-104">Retrieves either an attribute table for a mesh, or the number of entries stored in an attribute table for a mesh.</span></span>

## <a name="syntax"></a><span data-ttu-id="15a8a-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="15a8a-105">Syntax</span></span>


```C++
HRESULT GetAttributeTable(
  [in] D3DX10_ATTRIBUTE_RANGE *pAttribTable,
  [in] UINT                   *pAttribTableSize
);
```



## <a name="parameters"></a><span data-ttu-id="15a8a-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="15a8a-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="15a8a-107">*pAttribTable* \[ In\]</span><span class="sxs-lookup"><span data-stu-id="15a8a-107">*pAttribTable* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="15a8a-108">Typ: **[ **D3DX10-ATTRIBUTBEREICH \_ \_**](d3dx10-attribute-range.md)\***</span><span class="sxs-lookup"><span data-stu-id="15a8a-108">Type: **[**D3DX10\_ATTRIBUTE\_RANGE**](d3dx10-attribute-range.md)\***</span></span>

<span data-ttu-id="15a8a-109">Zeiger auf ein Array von D3DX10 ATTRIBUTE RANGE-Strukturen, die die Einträge \_ in der \_ Attributtabelle des Gitters darstellen.</span><span class="sxs-lookup"><span data-stu-id="15a8a-109">Pointer to an array of D3DX10\_ATTRIBUTE\_RANGE structures, representing the entries in the mesh's attribute table.</span></span> <span data-ttu-id="15a8a-110">Geben **Sie NULL** an, um den Wert für pAttribTableSize abzurufen.</span><span class="sxs-lookup"><span data-stu-id="15a8a-110">Specify **NULL** to retrieve the value for pAttribTableSize.</span></span>

</dd> <dt>

<span data-ttu-id="15a8a-111">*pAttribTableSize* \[ In\]</span><span class="sxs-lookup"><span data-stu-id="15a8a-111">*pAttribTableSize* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="15a8a-112">Typ: **[ **UINT**](../winprog/windows-data-types.md)\***</span><span class="sxs-lookup"><span data-stu-id="15a8a-112">Type: **[**UINT**](../winprog/windows-data-types.md)\***</span></span>

<span data-ttu-id="15a8a-113">Zeiger auf die Anzahl der in pAttribTable gespeicherten Einträge oder auf einen Wert, der mit der Anzahl von Einträgen aufgefüllt werden soll, die in der Attributtabelle für das Gitternetz gespeichert sind.</span><span class="sxs-lookup"><span data-stu-id="15a8a-113">Pointer to either the number of entries stored in pAttribTable or a value to be filled in with the number of entries stored in the attribute table for the mesh.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="15a8a-114">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="15a8a-114">Return value</span></span>

<span data-ttu-id="15a8a-115">Typ: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="15a8a-115">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="15a8a-116">Der Rückgabewert ist einer der Unter [Direct3D 10-Rückgabecodes aufgeführten Werte.](d3d10-graphics-reference-returnvalues.md)</span><span class="sxs-lookup"><span data-stu-id="15a8a-116">The return value is one of the values listed in [Direct3D 10 Return Codes](d3d10-graphics-reference-returnvalues.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="15a8a-117">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="15a8a-117">Remarks</span></span>

<span data-ttu-id="15a8a-118">Eine Attributtabelle wird verwendet, um Bereiche des Gitters zu identifizieren, die mit unterschiedlichen Texturen, Renderzuständen, Materialien und so weiter gezeichnet werden müssen.</span><span class="sxs-lookup"><span data-stu-id="15a8a-118">An attribute table is used to identify areas of the mesh that need to be drawn with different textures, render states, materials, and so on.</span></span> <span data-ttu-id="15a8a-119">Darüber hinaus kann die Anwendung die Attributtabelle verwenden, um Teile eines Gitters auszublenden, indem beim Zeichnen des Rahmens kein angegebener Attributbezeichner gezeichnunget wird.</span><span class="sxs-lookup"><span data-stu-id="15a8a-119">In addition, the application can use the attribute table to hide portions of a mesh by not drawing a given attribute identifier when drawing the frame.</span></span>

## <a name="requirements"></a><span data-ttu-id="15a8a-120">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="15a8a-120">Requirements</span></span>



| <span data-ttu-id="15a8a-121">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="15a8a-121">Requirement</span></span> | <span data-ttu-id="15a8a-122">Wert</span><span class="sxs-lookup"><span data-stu-id="15a8a-122">Value</span></span> |
|--------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="15a8a-123">Header</span><span class="sxs-lookup"><span data-stu-id="15a8a-123">Header</span></span><br/>  | <dl> <span data-ttu-id="15a8a-124"><dt>D3DX10.h</dt></span><span class="sxs-lookup"><span data-stu-id="15a8a-124"><dt>D3DX10.h</dt></span></span> </dl>   |
| <span data-ttu-id="15a8a-125">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="15a8a-125">Library</span></span><br/> | <dl> <span data-ttu-id="15a8a-126"><dt>D3DX10.lib</dt></span><span class="sxs-lookup"><span data-stu-id="15a8a-126"><dt>D3DX10.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="15a8a-127">Weitere Informationen</span><span class="sxs-lookup"><span data-stu-id="15a8a-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="15a8a-128">ID3DX10Mesh</span><span class="sxs-lookup"><span data-stu-id="15a8a-128">ID3DX10Mesh</span></span>](id3dx10mesh.md)
</dt> <dt>

[<span data-ttu-id="15a8a-129">D3DX-Schnittstellen</span><span class="sxs-lookup"><span data-stu-id="15a8a-129">D3DX Interfaces</span></span>](d3d10-graphics-reference-d3dx10-interfaces.md)
</dt> </dl>

 

 
