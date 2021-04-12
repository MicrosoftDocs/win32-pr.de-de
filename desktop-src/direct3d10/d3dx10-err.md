---
description: Fehler werden durch negative Werte dargestellt und können nicht kombiniert werden.
ms.assetid: 4149ce6d-e87a-4003-b123-5555c6b3b086
title: D3DX10_ERR-Enumeration (d3dx10. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DX10_ERR
api_type:
- HeaderDef
api_location:
- D3DX10.h
ms.openlocfilehash: 098c15999f20a65614d642029b1d1f6e0b600db6
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/15/2021
ms.locfileid: "104219468"
---
# <a name="d3dx10_err-enumeration"></a><span data-ttu-id="53a7e-103">D3dx10 \_ Err-Enumeration</span><span class="sxs-lookup"><span data-stu-id="53a7e-103">D3DX10\_ERR enumeration</span></span>

<span data-ttu-id="53a7e-104">Fehler werden durch negative Werte dargestellt und können nicht kombiniert werden.</span><span class="sxs-lookup"><span data-stu-id="53a7e-104">Errors are represented by negative values and cannot be combined.</span></span> <span data-ttu-id="53a7e-105">Im folgenden finden Sie eine Liste von Werten, die von Methoden zurückgegeben werden können, die in der D3DX Utility Library enthalten sind.</span><span class="sxs-lookup"><span data-stu-id="53a7e-105">The following is a list of values that can be returned by methods included with the D3DX utility library.</span></span> <span data-ttu-id="53a7e-106">In den einzelnen Methodenbeschreibungen finden Sie Listen der Werte, die von den einzelnen Methoden zurückgegeben werden können.</span><span class="sxs-lookup"><span data-stu-id="53a7e-106">See the individual method descriptions for lists of the values that each can return.</span></span> <span data-ttu-id="53a7e-107">Diese Listen sind nicht notwendigerweise vollständig.</span><span class="sxs-lookup"><span data-stu-id="53a7e-107">These lists are not necessarily comprehensive.</span></span>

## <a name="syntax"></a><span data-ttu-id="53a7e-108">Syntax</span><span class="sxs-lookup"><span data-stu-id="53a7e-108">Syntax</span></span>


```C++
typedef enum D3DX10_ERR { 
  D3DX10_ERR_CANNOT_MODIFY_INDEX_BUFFER  = MAKE_DDHRESULT(2900),
  D3DX10_ERR_INVALID_MESH                = MAKE_DDHRESULT(2901),
  D3DX10_ERR_CANNOT_ATTR_SORT            = MAKE_DDHRESULT(2902),
  D3DX10_ERR_SKINNING_NOT_SUPPORTED      = MAKE_DDHRESULT(2903),
  D3DX10_ERR_TOO_MANY_INFLUENCES         = MAKE_DDHRESULT(2904),
  D3DX10_ERR_INVALID_DATA                = MAKE_DDHRESULT(2905),
  D3DX10_ERR_LOADED_MESH_HAS_NO_DATA     = MAKE_DDHRESULT(2906),
  D3DX10_ERR_DUPLICATE_NAMED_FRAGMENT    = MAKE_DDHRESULT(2907),
  D3DX10_ERR_CANNOT_REMOVE_LAST_ITEM     = MAKE_DDHRESULT(2908)
} D3DX10_ERR, *LPD3DX10_ERR;
```



## <a name="constants"></a><span data-ttu-id="53a7e-109">Konstanten</span><span class="sxs-lookup"><span data-stu-id="53a7e-109">Constants</span></span>

<dl> <dt>

<span data-ttu-id="53a7e-110"><span id="D3DX10_ERR_CANNOT_MODIFY_INDEX_BUFFER"></span><span id="d3dx10_err_cannot_modify_index_buffer"></span>**D3dx10 \_ Err \_ kann \_ den \_ Index \_ Puffer nicht ändern**</span><span class="sxs-lookup"><span data-stu-id="53a7e-110"><span id="D3DX10_ERR_CANNOT_MODIFY_INDEX_BUFFER"></span><span id="d3dx10_err_cannot_modify_index_buffer"></span>**D3DX10\_ERR\_CANNOT\_MODIFY\_INDEX\_BUFFER**</span></span>
</dt> <dd>

<span data-ttu-id="53a7e-111">Der Index Puffer kann nicht geändert werden.</span><span class="sxs-lookup"><span data-stu-id="53a7e-111">The index buffer cannot be modified.</span></span>

</dd> <dt>

<span data-ttu-id="53a7e-112"><span id="D3DX10_ERR_INVALID_MESH"></span><span id="d3dx10_err_invalid_mesh"></span>**D3dx10 \_ Err ( \_ ungültiges \_ Mesh)**</span><span class="sxs-lookup"><span data-stu-id="53a7e-112"><span id="D3DX10_ERR_INVALID_MESH"></span><span id="d3dx10_err_invalid_mesh"></span>**D3DX10\_ERR\_INVALID\_MESH**</span></span>
</dt> <dd>

<span data-ttu-id="53a7e-113">Das Mesh ist ungültig.</span><span class="sxs-lookup"><span data-stu-id="53a7e-113">The mesh is invalid.</span></span>

</dd> <dt>

<span data-ttu-id="53a7e-114"><span id="D3DX10_ERR_CANNOT_ATTR_SORT"></span><span id="d3dx10_err_cannot_attr_sort"></span>**D3dx10 \_ Err \_ kann nicht in der \_ \_ Sortierreihenfolge**</span><span class="sxs-lookup"><span data-stu-id="53a7e-114"><span id="D3DX10_ERR_CANNOT_ATTR_SORT"></span><span id="d3dx10_err_cannot_attr_sort"></span>**D3DX10\_ERR\_CANNOT\_ATTR\_SORT**</span></span>
</dt> <dd>

<span data-ttu-id="53a7e-115">Die Attribut Sortierung (D3DXMESHOPT \_ attrsort) wird nicht als Optimierungstechnik unterstützt.</span><span class="sxs-lookup"><span data-stu-id="53a7e-115">Attribute sort (D3DXMESHOPT\_ATTRSORT) is not supported as an optimization technique.</span></span>

</dd> <dt>

<span data-ttu-id="53a7e-116"><span id="D3DX10_ERR_SKINNING_NOT_SUPPORTED"></span><span id="d3dx10_err_skinning_not_supported"></span>**D3dx10 \_ Err- \_ Skinning \_ \_ wird nicht unterstützt.**</span><span class="sxs-lookup"><span data-stu-id="53a7e-116"><span id="D3DX10_ERR_SKINNING_NOT_SUPPORTED"></span><span id="d3dx10_err_skinning_not_supported"></span>**D3DX10\_ERR\_SKINNING\_NOT\_SUPPORTED**</span></span>
</dt> <dd>

<span data-ttu-id="53a7e-117">Das Skinning wird nicht unterstützt.</span><span class="sxs-lookup"><span data-stu-id="53a7e-117">Skinning is not supported.</span></span>

</dd> <dt>

<span data-ttu-id="53a7e-118"><span id="D3DX10_ERR_TOO_MANY_INFLUENCES"></span><span id="d3dx10_err_too_many_influences"></span>**D3dx10 \_ Err \_ zu \_ viele \_ Einflüsse**</span><span class="sxs-lookup"><span data-stu-id="53a7e-118"><span id="D3DX10_ERR_TOO_MANY_INFLUENCES"></span><span id="d3dx10_err_too_many_influences"></span>**D3DX10\_ERR\_TOO\_MANY\_INFLUENCES**</span></span>
</dt> <dd>

<span data-ttu-id="53a7e-119">Es wurden zu viele Einflüsse angegeben.</span><span class="sxs-lookup"><span data-stu-id="53a7e-119">Too many influences specified.</span></span>

</dd> <dt>

<span data-ttu-id="53a7e-120"><span id="D3DX10_ERR_INVALID_DATA"></span><span id="d3dx10_err_invalid_data"></span>**D3dx10 \_ Err \_ ungültige \_ Daten**</span><span class="sxs-lookup"><span data-stu-id="53a7e-120"><span id="D3DX10_ERR_INVALID_DATA"></span><span id="d3dx10_err_invalid_data"></span>**D3DX10\_ERR\_INVALID\_DATA**</span></span>
</dt> <dd>

<span data-ttu-id="53a7e-121">Die Daten sind ungültig.</span><span class="sxs-lookup"><span data-stu-id="53a7e-121">The data is invalid.</span></span>

</dd> <dt>

<span data-ttu-id="53a7e-122"><span id="D3DX10_ERR_LOADED_MESH_HAS_NO_DATA"></span><span id="d3dx10_err_loaded_mesh_has_no_data"></span>**D3dx10 \_ Err \_ geladenes \_ Mesh \_ hat \_ keine \_ Daten**</span><span class="sxs-lookup"><span data-stu-id="53a7e-122"><span id="D3DX10_ERR_LOADED_MESH_HAS_NO_DATA"></span><span id="d3dx10_err_loaded_mesh_has_no_data"></span>**D3DX10\_ERR\_LOADED\_MESH\_HAS\_NO\_DATA**</span></span>
</dt> <dd>

<span data-ttu-id="53a7e-123">Das Mesh weist keine Daten auf.</span><span class="sxs-lookup"><span data-stu-id="53a7e-123">The mesh has no data.</span></span>

</dd> <dt>

<span data-ttu-id="53a7e-124"><span id="D3DX10_ERR_DUPLICATE_NAMED_FRAGMENT"></span><span id="d3dx10_err_duplicate_named_fragment"></span>**D3dx10 \_ Err- \_ doppeltes \_ benanntes \_ Fragment**</span><span class="sxs-lookup"><span data-stu-id="53a7e-124"><span id="D3DX10_ERR_DUPLICATE_NAMED_FRAGMENT"></span><span id="d3dx10_err_duplicate_named_fragment"></span>**D3DX10\_ERR\_DUPLICATE\_NAMED\_FRAGMENT**</span></span>
</dt> <dd>

<span data-ttu-id="53a7e-125">Ein Fragment mit diesem Namen ist bereits vorhanden.</span><span class="sxs-lookup"><span data-stu-id="53a7e-125">A fragment with that name already exists.</span></span>

</dd> <dt>

<span data-ttu-id="53a7e-126"><span id="D3DX10_ERR_CANNOT_REMOVE_LAST_ITEM"></span><span id="d3dx10_err_cannot_remove_last_item"></span>**D3dx10 \_ Err \_ kann \_ das \_ Letzte \_ Element nicht entfernen.**</span><span class="sxs-lookup"><span data-stu-id="53a7e-126"><span id="D3DX10_ERR_CANNOT_REMOVE_LAST_ITEM"></span><span id="d3dx10_err_cannot_remove_last_item"></span>**D3DX10\_ERR\_CANNOT\_REMOVE\_LAST\_ITEM**</span></span>
</dt> <dd>

<span data-ttu-id="53a7e-127">Das letzte Element kann nicht gelöscht werden.</span><span class="sxs-lookup"><span data-stu-id="53a7e-127">The last item cannot be deleted.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="53a7e-128">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="53a7e-128">Remarks</span></span>

<span data-ttu-id="53a7e-129">Der Einrichtungs Code- \_ fakdd wird zum Generieren von Fehlercodes verwendet, wie in den folgenden Makros.</span><span class="sxs-lookup"><span data-stu-id="53a7e-129">The facility code \_FACDD is used to generate error codes, as in the following macros.</span></span>


```
#define _FACDD                  0x876
#define MAKE_DDHRESULT( code )  MAKE_HRESULT( 1, _FACDD, code )
enum _D3DXERR {
    D3DXERR_CANNOTMODIFYINDEXBUFFER = MAKE_DDHRESULT(2900),
    D3DXERR_INVALIDMESH             = MAKE_DDHRESULT(2901),
    ...
    };
```



## <a name="requirements"></a><span data-ttu-id="53a7e-130">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="53a7e-130">Requirements</span></span>



| <span data-ttu-id="53a7e-131">Anforderung</span><span class="sxs-lookup"><span data-stu-id="53a7e-131">Requirement</span></span> | <span data-ttu-id="53a7e-132">Wert</span><span class="sxs-lookup"><span data-stu-id="53a7e-132">Value</span></span> |
|-------------------|-------------------------------------------------------------------------------------|
| <span data-ttu-id="53a7e-133">Header</span><span class="sxs-lookup"><span data-stu-id="53a7e-133">Header</span></span><br/> | <dl> <span data-ttu-id="53a7e-134"><dt>D3dx10. h</dt></span><span class="sxs-lookup"><span data-stu-id="53a7e-134"><dt>D3DX10.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="53a7e-135">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="53a7e-135">See also</span></span>

<dl> <dt>

[<span data-ttu-id="53a7e-136">D3DX-Enumerationen</span><span class="sxs-lookup"><span data-stu-id="53a7e-136">D3DX Enumerations</span></span>](d3d10-graphics-reference-d3dx10-enums.md)
</dt> </dl>

 

 




